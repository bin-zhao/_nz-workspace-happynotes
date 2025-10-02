
---

https://medium.com/data-science/a-visual-understanding-of-neural-networks-64083c7eb29c

# A Visual Understanding of Neural Networks

## The math behind neural networks visually explained

[

![[fbd791e55a6564837fb45ecc19dcae22_MD5.jpg]]





](https://medium.com/@reza-bagheri79?source=post_page---byline--64083c7eb29c---------------------------------------)

[Reza Bagheri](https://medium.com/@reza-bagheri79?source=post_page---byline--64083c7eb29c---------------------------------------)

Follow

27 min read

·

Jan 11, 2025

768

11

[

](https://medium.com/plans?dimension=post_audio_button&postId=64083c7eb29c&source=upgrade_membership---post_audio_button-----------------------------------------)

![[ba922fd3bb50bd3101f136ed96fa7f6a_MD5.png]]

Image generated using DALL-E

==Artificial neural networks are the most powerful and at the same time the most complicated machine learning models. They are particularly useful for complex tasks where traditional machine learning algorithms fail. The main advantage of neural networks is their ability to learn intricate patterns and relationships in data, even when the data is highly dimensional or unstructured.==

Many articles discuss the math behind neural networks. Topics like different activation functions, forward and backpropagation algorithms, gradient descent, and optimization methods are discussed in detail. In this article, we take a different approach and present a visual understanding of a neural network layer by layer. We will first focus on the visual explanation of single-layer neural networks in both classification and regression problems and their similarities to other machine learning models. Then we will discuss the importance of hidden layers and non-linear activation functions. All the visualizations are created using Python.

_All the images in this article were created by the author._

## **Neural networks for classification**

We start with classification problems. The simplest type of classification problem is a _binary classification_ in which the target has only two categories or labels. If the target has more than two labels, then we have a _multi-class classification_ problem.

## **Single-layer networks: perceptron**

A single-layer neural network is the simplest form of an artificial neural network. Here we only have an input layer which receives the input data and an output layer that produces the output of the network. The input layer isn’t considered a true layer in this network since it merely passes the input data. That’s why this architecture is called a single-layer network. Perceptron, the first neural network ever created, is the simplest example of a single-layer neural network.

The perceptron was created in 1957 by Frank Rosenblatt. He believed that perceptron can simulate brain principles, with the ability to learn and make decisions. The original perceptron was designed to solve a binary classification problem.

Figure 1 shows the architecture of a perceptron. The input data has _n_ features denoted by _x_₁ to _x_n_. The target _y_ has only two labels (_y_=0 and _y_=1).

![[1f45a4b13213206bfd26a927458898e6_MD5.png]]

Figure 1

The input layer receives the features and passes them to the output layer. The neuron in the output layer calculates the weighted sum of the input features. Each input feature, _x_ᵢ, is associated with the weight _w_ᵢ. The neuron multiplies each input by its corresponding weight and sums up the results. A bias term, _w_₀, is also added to this sum. If we denote the sum by _z,_ we have:

![[90e3bd61c57f9bfbada825a68f31119d_MD5.png]]

The activation function is a step function defined as:

![[1d3cd82cfad9ccbdf9214edda8a31cc4_MD5.png]]

This activation function is plotted in Figure 2.

![[d5e866498b8f0b23f729028765d63615_MD5.png]]

Figure 2

The output of the perceptron denoted by _y_^ is calculated as follows:

![[8dd022a73cd37bb1444f63870db62334_MD5.png]]

To visualize how a perceptron works, we use a simple training dataset with only two features _x_₁ and _x_₂. This dataset is created in Listing 1. It is defined randomly, and the target _y_ has only two labels (_y_=0 and _y_=1). We also import all the Python libraries needed in this article at the beginning of this listing. The dataset is plotted in Figure 3.

# Listing 1  
  
import numpy as np  
import matplotlib.pyplot as plt  
from matplotlib.colors import ListedColormap  
from sklearn.preprocessing import StandardScaler  
from sklearn.linear_model import LogisticRegression  
import random  
import tensorflow as tf  
from tensorflow.keras.models import Sequential, Model  
from tensorflow.keras.layers import Dense, Input  
from tensorflow.keras.utils import to_categorical  
from tensorflow.keras import backend  
  
np.random.seed(3)  
n = 30  
X1 = np.random.randn(n,2)  
  
y1 = np.random.choice((0, 1),size=n)  
X1[y1>0,0] -= 4  
X1[y1>0,1] += 4  
scaler = StandardScaler()  
X1 = scaler.fit_transform(X1)  
  
plt.figure(figsize=(5, 5))  
marker_colors = ['red', 'blue']  
target_labels = np.unique(y1)  
n = len(target_labels)  
for i, label in enumerate(target_labels):  
    plt.scatter(X1[y1==label, 0], X1[y1==label,1], label="y="+str(label),  
                edgecolor="white", color=marker_colors[i])  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='best', fontsize=11)  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlim([-2.3, 1.8])  
plt.ylim([-1.9, 2.2])  
plt.show()

![[77f1b25d5d43392e088aebc2177ba52b_MD5.png]]

Figure 3

This article does not go into detail about the neural network training process. Instead, we focus on the behaviour of an already trained neural network. In Listing 2, we define and train a perceptron using the previous dataset.

# Listing 2  
  
class Perceptron(object):  
    def __init__(self, eta=0.01, epochs=50):  
        self.eta = eta  
        self.epochs = epochs  
  
    def fit(self, X, y):  
  
        self.w = np.zeros(1 + X.shape[1])  
  
        for epoch in range(self.epochs):  
            for xi, target in zip(X, y):  
                error = target - self.predict(xi)  
                self.w[1:] +=  self.eta * error * xi  
                self.w[0] +=  self.eta * error  
        return self  
  
    def net_input(self, X):  
        return np.dot(X, self.w[1:]) + self.w[0]  
  
    def predict(self, X):  
        return np.where(self.net_input(X) >= 0.0, 1, 0)  
  
perc = Perceptron(epochs=150, eta=0.05)  
perc.fit(X1, y1)

Now we want to see how this model classifies our training dataset. Hence, we define a function that plots the decision boundary of the trained neural network. This function defined in Listing 3, creates a mesh grid on the 2D space and then uses a trained model to predict the target of all the points on that grid. The points with different labels are colored differently. Therefore, the decision boundary of the model can be visualized using this function.

# Listing 3  
  
def plot_boundary(X, y, clf, lims, alpha=1):  
    gx1, gx2 = np.meshgrid(np.arange(lims[0], lims[1],  
                                    (lims[1]-lims[0])/500.0),  
                           np.arange(lims[2], lims[3],  
                                    (lims[3]-lims[2])/500.0))  
    backgd_colors = ['lightsalmon', 'aqua', 'lightgreen', 'yellow']  
    marker_colors = ['red', 'blue', 'green', 'orange']  
    gx1l = gx1.flatten()  
    gx2l = gx2.flatten()  
    gx = np.vstack((gx1l,gx2l)).T  
    gyhat = clf.predict(gx)  
    if len(gyhat.shape)==1:  
        gyhat = gyhat.reshape(len(gyhat), 1)  
    if gyhat.shape[1] > 1:  
        gyhat = gyhat.argmax(axis=1)  
    gyhat = gyhat.reshape(gx1.shape)  
    target_labels = np.unique(y)  
    n = len(target_labels)  
    plt.pcolormesh(gx1, gx2, gyhat, cmap=ListedColormap(backgd_colors[:n]))  
    for i, label in enumerate(target_labels):  
        plt.scatter(X[y==label, 0], X[y==label,1],  
                    label="y="+str(label),  
                    alpha=alpha, edgecolor="white",  
                    color=marker_colors[i])

Now, we use this function to plot the decision boundary of the perceptron for the training dataset. The result is shown in Figure 4.

# Listing 4  
  
plt.figure(figsize=(5, 5))  
# Plot the vector w  
plt.quiver([0], [0], perc.w[1], perc.w[2], color=['black'],  
           width=0.008, angles='xy', scale_units='xy',  
           scale=0.4, zorder=5)  
# Plot the boundary  
plot_boundary(X1, y1, perc, lims=[-2.3, 1.8, -1.9, 2.2])  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='best', fontsize=11)  
plt.xlim([-2.3, 1.8])  
plt.ylim([-1.9, 2.2])  
plt.show()

![[12769b6b4f85b0c21926a1152fa27cdf_MD5.png]]

Figure 4

The figure clearly shows that the decision boundary is a straight line. We define the vector **_w_** using the weights of the perceptron:

![[a7fa3d5fb8badacd94e1667337fabd12_MD5.png]]

This vector is also plotted in Figure 4, which shows that it is perpendicular to the decision boundary of the perceptron (the vector was small, so we scaled it in the plot). We can now explain the mathematical reasons behind these results.

For a dataset with two features, we have:

![[2308a32a2e8ec051741485f1f1d7468e_MD5.png]]

Based on Equation 1, we know that the predicted label of all the data points for which _z_=0 is 1. On the other hand, the predicted label for any data point with _z_<0 will be 0. Hence, the decision boundary is the location of the data points for which _z_=0, and it is defined by the following equation:

![[2786ca1f6267238179f5e17eb0ab1abe_MD5.png]]

This is the equation of a straight line, and the normal vector of this line (the vector which is perpendicular to this line) is:

![[a7fa3d5fb8badacd94e1667337fabd12_MD5.png]]

This explains why the decision boundary is perpendicular to the vector **_w_**.

## **Single-layer networks: sigmoid neuron**

The perceptron can predict the label of a data point, but it cannot provide the prediction probability. In fact, this network cannot tell you how confident it is in its prediction. We need a different activation function called _sigmoid_ to get the prediction probability. The sigmoid activation function is defined as follows:

![[34d2720ad32506ec4590f5c5616b0736_MD5.png]]

A plot of this function is given in Figure 5.

![[bca7c568c95f78edfb1a3f11a3834974_MD5.png]]

Figure 5

We know that the probability of an event is a number between 0 and 1. As this plot shows the range of the sigmoid function is (0, 1), so it can be used to represent the probability of an outcome. Now, we replace the activation function of the perceptron with a sigmoid function to get the network shown in Figure 6.

![[273ad9aa5eb54a02b0a0c1cb0af789be_MD5.png]]

Figure 6

In this network, we denote the output of the network with _p_, so we can write:

![[90e3bd61c57f9bfbada825a68f31119d_MD5.png]]

![[9cbad46d53e84b1088c997e712750a15_MD5.png]]

Here _p_ is the probability that the predicted label is 1 (_y_^=1). To obtain the predicted target, we must compare this probability with a threshold which is 0.5 by default:

![[f2ab75f06a8411a9ec07d38c660955a5_MD5.png]]

To visualize this network, we use the dataset defined in Listing 1 to train it. Listing 5 creates this network using the `keras` library.

# Listing 5  
  
np.random.seed(0)  
random.seed(0)  
tf.random.set_seed(0)  
  
model1 = Sequential()  
model1.add(Dense(1, activation='sigmoid', input_shape=(2,)))  
  
model1.compile(loss = 'binary_crossentropy',   
               optimizer='adam', metrics=['accuracy'])  
model1.summary()

The cost function of this neural network is called _cross-entropy_. Next, we use the dataset defined in Listing 1 to train this model.

# Listing 6  
  
history1 = model1.fit(X1, y1, epochs=1500, verbose=0, batch_size=X1.shape[0])  
plt.plot(history1.history['accuracy'])  
plt.title('Accuracy vs Epochs')  
plt.ylabel('Accuracy')  
plt.xlabel('Epoch')  
plt.show()

Figure 7 shows the plot of accuracy versus epochs for this model.

![[71d18fa4ec150f14aa1501b6cc502385_MD5.png]]

Figure 7

After training the model, we can retrieve the weights of the output layer (_w_₁ and _w_₂).

# Listing 7  
  
output_layer_weights = model1.layers[0].get_weights()[0]  
model1_w1, model1_w2 = output_layer_weights[0, 0], output_layer_weights[1, 0]

Finally, we plot the decision boundary of this network. The result is shown in Figure 8.

# Listing 8  
  
plt.figure(figsize=(5, 5))  
# Plot the vector w  
output_layer_weights = model1.layers[0].get_weights()[0]  
plt.quiver([0], [0], model1_w1,  
           model1_w2, color=['black'],  
           width=0.008, angles='xy', scale_units='xy',  
           scale=1, zorder=5)  
# Plot the boundary  
plot_boundary(X1, y1, model1, lims=[-2.3, 1.8, -1.9, 2.2])  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='best', fontsize=11)  
plt.xlim([-2.3, 1.8])  
plt.ylim([-1.9, 2.2])  
plt.show()

![[1bf38d41b5160de09cc77a04c1b068ff_MD5.png]]

Figure 8

Again we see that the decision boundary is a straight line. We define the vector **_w_** using the weights of the output layer:

![[a7fa3d5fb8badacd94e1667337fabd12_MD5.png]]

The vector **_w_** is perpendicular to the decision boundary, just as we saw with the perceptron. Let’s explain the mathematical reasons behind these results. According to Equation 2, the predicted label of all the data points for which _p_=0.5 is 1. On the other hand, the predicted label for any data point with _p_<0.5 will be 0. As a result, the decision boundary is the location of all the data points for which _p_=0.5:

![[a1f7eefd63f6d763d8e65193fc6fab56_MD5.png]]

Hence, the decision boundary is the location of all the data points defined by the following equation:

![[2786ca1f6267238179f5e17eb0ab1abe_MD5.png]]

As mentioned before, this is the equation of a straight line, and the normal vector of this line (the vector which is perpendicular to this line) is:

![[a7fa3d5fb8badacd94e1667337fabd12_MD5.png]]

## **Adding more features**

So far, we only considered a toy dataset with only two features. Let’s see what happens when we have three features. Listing 9 defines another dataset with 3 features. This dataset is plotted in Figure 9.

# Listing 9  
  
np.random.seed(0)  
xt1 = np.random.randn(50, 3) * 0.4 + np.array([-2, 1, 0])  
xt2 = np.random.randn(50, 3) * 0.4 + np.array([1, 4, 3])  
y2 = np.array(50*[0]+50*[1])  
X2 = np.vstack((xt1, xt2))  
scaler = StandardScaler()  
X2 = scaler.fit_transform(X2)  
  
fig = plt.figure(figsize=(7, 7))  
ax = fig.add_subplot(111, projection='3d')  
  
ax.scatter(X2[y2==0, 0], X2[y2==0,1], X2[y2==0,2],  
           label="y=0", alpha=0.8, color="red")  
ax.scatter(X2[y2==1, 0], X2[y2==1,1], X2[y2==1,2],  
           label="y=1", alpha=0.8, color="blue")  
ax.legend(loc="upper left", fontsize=12)  
ax.set_xlabel("$x_1$", fontsize=18)  
ax.set_ylabel("$x_2$", fontsize=18)  
ax.set_zlabel("$x_3$", fontsize=15, labelpad=-0.5)  
ax.view_init(5, -50)  
plt.show()

![[22622a50b2df419a6fe0cb475c4932ce_MD5.png]]

Figure 9

Now we create a new network with a sigmoid neuron and train it using this dataset.

# Listing 10  
  
backend.clear_session()  
np.random.seed(0)  
random.seed(0)  
tf.random.set_seed(0)  
  
model2 = Sequential()  
model2.add(Dense(1, activation='sigmoid', input_shape=(3,)))  
  
model2.compile(loss = 'binary_crossentropy',   
               optimizer='adam', metrics=['accuracy'])  
history2 = model2.fit(X2, y2, epochs=1500, verbose=0,  
                      batch_size=X2.shape[0])

Next, we retrieve the weights of the output layer in the trained model and plot the data points and the decision boundary of the model in Figure 10.

# Listing 11  
  
model2_w0 = output_layer_biases[0]  
model2_w1,  model2_w2,  model2_w3 = output_layer_weights[0, 0], \  
      output_layer_weights[1, 0], output_layer_weights[2, 0]  
  
fig = plt.figure(figsize=(7, 7))  
ax = fig.add_subplot(111, projection='3d')  
  
lims=[-2, 2, -2, 2]  
ga1, ga2 = np.meshgrid(np.arange(lims[0], lims[1], (lims[1]-lims[0])/500.0),  
                       np.arange(lims[2], lims[3], (lims[3]-lims[2])/500.0))  
  
ga1l = ga1.flatten()  
ga2l = ga2.flatten()  
ga3 = -(model2_w0 + model2_w1*ga1l + model2_w2*ga2l) / model2_w3  
ga3 = ga3.reshape(500, 500)  
ax.plot_surface(ga1, ga2, ga3, alpha=0.5)  
ax.quiver([0], [0], [0], model2_w1, model2_w2, model2_w3,  
          color=['black'], length=0.5, zorder=5)  
ax.scatter(X2[y2==0, 0], X2[y2==0,1], X2[y2==0,2],  
           label="y=0", alpha=0.8, color="red")  
ax.scatter(X2[y2==1, 0], X2[y2==1,1], X2[y2==1,2],  
           label="y=1", alpha=0.8, color="blue")  
ax.legend(loc="upper left", fontsize=12)  
ax.set_xlabel("$x_1$", fontsize=16)  
ax.set_ylabel("$x_2$", fontsize=16)  
ax.set_zlabel("$x_3$", fontsize=15, labelpad=-0.5)  
ax.view_init(5, -50)  
plt.show()

![[18455d9ce15900a8f4685a4241b11f54_MD5.png]]

Figure 10

As this figure shows the decision boundary is a plane perpendicular to the vector

![[0c0d7f58519ea4e1c88596e1e7027b2b_MD5.png]]

which is formed using the weights of the output layer. Here the decision boundary was calculated as follows:

![[cba34ecee8afc1f94e85ea64fc236d92_MD5.png]]

So, the decision boundary is the solution of this equation

![[cf5a4cd63d27a36a6385aa87645b5492_MD5.png]]

This is the equation of a plane, and the vector **_w (_**defined in Equation 3) is the normal vector of this plane.

## **Linear classifiers**

What happens if we have more than 3 features in the input data? We can easily extend the same idea to find the decision boundary of a network with _n_ features for a perceptron or a sigmoid neuron. In both cases, the decision boundary is the solution to this equation:

![[1325ff685e9b97684a43cef41dde8746_MD5.png]]

This equation describes a hyperplane in an _n_-dimensional space which is perpendicular to the vector

![[e82971b8c84bd51929d66d24cfb34468_MD5.png]]

In 2D space, the hyperplane becomes a 1-dimensional line while in 3D space, it becomes a 2D plane. A line or a plane has no curvature, and though we cannot visualize hyperplanes in higher dimensions, the concept remains the same. In _n_-dimensional space, a hyperplane is an _n_-1-dimensional subspace which is flat and has no curvature.

In machine learning, a _linear classifier_ is a classification model that makes its decisions based on a linear combination of the input features. As a result, the decision boundary of a linear classifier is a hyperplane. Perceptron and sigmoid neurons are two examples of a linear classifier.

It is worth mentioning that a sigmoid neuron with a cross-entropy cost function is equivalent to a logistic regression model. The next Listing trains a logistic regression model (from the `scikit-learn` library) on the 2D dataset defined in Listing 1. The decision boundary of this model is plotted in Figure 11. Though it is a straight line, it is not exactly the same line obtained with a sigmoid neuron in Figure 8.

Though the logistic regression and sigmoid neuron (with the cross-entropy cost function) are equivalent models, different approaches are used to find their paramters during the training process. In an aneural network, the gradient descent algorithm with random initialization is used for training, however, the logistic regression model uses a deterministic solver called lbfgs (Limited-memory Broyden–Fletcher–Goldfarb–Shanno) for that purpose. As a result, the final values of the parameters in these two models may differ, changing the position of the decision boundary line.

# Listing 12  
  
# Comparing with a logistic regression model  
lr_model = LogisticRegression().fit(X1, y1)  
  
plt.figure(figsize=(5, 5))  
# Plot the boundary  
plot_boundary(X1, y1, lr_model, lims=[-2.3, 1.8, -1.9, 2.2])  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='best', fontsize=11)  
plt.xlim([-2.3, 1.8])  
plt.ylim([-1.9, 2.2])  
plt.show()

![[29e7a743f0792d393efb155e78a8acbe_MD5.png]]

Figure 11

## **Multi-class classification and the softmax layer**

Our attention has been on a binary classification problem so far. If the target of the dataset has more than two labels, then we have a multi-class classification problem, and a _softmax layer_ is needed for such a problem. Suppose that a dataset has _n_ features and its target has _C_ labels. This dataset can be used for training a single-layer neural network with a softmax layer shown in Figure 12.

![[1174e8c91ae693154214d6d66e265e50_MD5.png]]

Figure 12

The softmax function is a generalization of the sigmoid function to a multi-class classification problem in which the target has more than 2 labels. The neurons in the output layer give a linear combination of the input features:

![[3ddd5e1beffc2c3bffb3597f2553f807_MD5.png]]

Each output of the softmax layer is calculated as follows:

![[21cdfd36c57f9f08ca9d170bff323100_MD5.png]]

In this equation, _pᵢ_ represents the probability of the predicted target being equal to _i_th label. In the end, the predicted label is the one with the highest probability:

![[c587937b49308977cb621b398118ac2a_MD5.png]]

Now we create another toy dataset to visualize the softmax layer. In this dataset, we have two features and the target has 3 labels. It is plotted in Figure 13.

# Listing 13  
  
np.random.seed(0)  
xt1 = np.random.randn(50, 2) * 0.4 + np.array([2, 1])  
xt2 = np.random.randn(50, 2) * 0.7 + np.array([6, 4])  
xt3 = np.random.randn(50, 2) * 0.5 + np.array([2, 6])  
  
y3 = np.array(50*[1]+50*[2]+50*[3])  
X3 = np.vstack((xt1, xt2, xt3))  
scaler = StandardScaler()  
X3 = scaler.fit_transform(X3)  
  
plt.figure(figsize=(6, 6))  
plt.scatter(X3[y3==1, 0], X3[y3==1,1], label="y=1", alpha=0.7, color="red")  
plt.scatter(X3[y3==2, 0], X3[y3==2,1], label="y=2", alpha=0.7, color="blue")  
plt.scatter(X3[y3==3, 0], X3[y3==3,1], label="y=3", alpha=0.7, color="green")  
plt.legend(loc="best", fontsize=11)  
plt.xlabel("$x_1$", fontsize=16)  
plt.ylabel("$x_2$", fontsize=16)  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.show()

![[6220d880e278629b97091ff3683137c4_MD5.png]]

Figure 13

Next, we create a single-layer neural network and train it using this dataset. This network has a softmax layer.

# Listing 14  
  
backend.clear_session()  
np.random.seed(0)  
random.seed(0)  
tf.random.set_seed(0)  
y3_categorical = to_categorical(y3-1, num_classes=3)  
model3 = Sequential()  
model3.add(Dense(3, activation='softmax', input_shape=(2,)))  
model3.compile(loss = 'categorical_crossentropy',  
               optimizer='adam', metrics=['accuracy'])  
history3 = model3.fit(X3, y3_categorical, epochs=2200,  
                      verbose=0, batch_size=X3.shape[0])

Next, we retrieve the weight and biases of this network:

# Listing 15  
  
output_layer_weights = model3.layers[-1].get_weights()[0]  
output_layer_biases = model3.layers[-1].get_weights()[1]  
  
model3_w10, model3_w20, model3_w30 = output_layer_biases[0], \  
output_layer_biases[1], output_layer_biases[2]  
  
model3_w1 = output_layer_weights[:, 0]  
model3_w2 = output_layer_weights[:, 1]  
model3_w3 = output_layer_weights[:, 2]

Finally, we can plot the decision boundary of this model using Listing 16.

# Listing 16  
  
plt.figure(figsize=(5, 5))  
plt.quiver([1.7], [0.7], model3_w3[0]-model3_w2[0],  
           model3_w3[1]-model3_w2[1], color=['black'],  
           width=0.008, angles='xy', scale_units='xy',  
           scale=1, zorder=5)  
plt.quiver([-0.5], [-2.2], model3_w2[0]-model3_w1[0],  
           model3_w2[1]-model3_w1[1], color=['black'],  
           width=0.008, angles='xy', scale_units='xy',  
           scale=1, zorder=5)  
plt.quiver([-1.8], [-1.7], model3_w3[0]-model3_w1[0],  
           model3_w3[1]-model3_w1[1], color=['black'],  
           width=0.008, angles='xy', scale_units='xy',  
           scale=1, zorder=5)  
plt.text(0.25, 1.85, "$\mathregular{w_3-w_2}$", color="black",  
         fontsize=12, weight="bold", style="italic")  
plt.text(1.2, -1.1, "$\mathregular{w_2-w_1}$", color="black",  
         fontsize=12, weight="bold", style="italic")  
plt.text(-1.5, -0.5, "$\mathregular{w_3-w_1}$", color="black",  
         fontsize=12, weight="bold", style="italic")  
plot_boundary(X3, y3, model3,lims=[-2.2, 2.4, -2.5, 2.1],  
              alpha= 0.7)  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='best', fontsize=11)  
plt.xlim([-2.2, 2.4])  
plt.ylim([-2.5, 2.1])  
plt.show()

![[8549111eedb729e4ad7ceff12061ec93_MD5.png]]

Figure 14

As Figure 14 shows, softmax creates 3 decision boundaries each being a straight line. For example, the decision boundary between labels 1 and 2 is the location of the points with an equal prediction probability for labels 1 and 2. Hence we can write:

![[6860bfe86800d13063c26fd1fa589c3d_MD5.png]]

![[6547338adb7d8f3bf041dde835e10cd5_MD5.png]]

By simplifying the last equation we get:

![[ee024a7a61cffdceea50fc5a61265d9b_MD5.png]]

This is again, the equation of a straight line. If we define the vector **_w_**_ᵢ_ as:

![[7e0ecf6f31a05f5c546da71c09d25327_MD5.png]]

The normal vector of this line can be written as:

![[68bf6ce8749fec6f5ef44bd5adee68ee_MD5.png]]

Hence the decision boundary is perpendicular to **_w_**₂ -**_w_**₁. Similarly, it can be shown that the other decision boundaries are all straight lines and the line between the labels _i_ and _j_ is perpendicular to the vector **_w_**_ᵢ_-**_w_**__j_.

More generally, if we have _n_ features in the training dataset, the decision boundaries will be hyperplanes in an _n_-dimensional space. Here, the hyperplane for the labels _i_ and _j_ is perpendicular to the vector **_w_**_ᵢ_-**_w_**__j_ where

![[b9bd9a4eab6d7bc0067bcc56927ead93_MD5.png]]

A single-layer neural network with a softmax activation is a generalization of a linear classifeir to higher dimensions. It continues to use hyperplanes to predict the target’s label, but more than one hyperplane is required for predicting all labels.

All the datasets shown so far were _linearly separable_ which means that we can separate the data points with different labels using hyperplanes. In reality, a dataset is rarely linearly separable. In the following section, we will look at the difficulties of classifying non-linearly separable datasets.

## **Multiple-layer networks**

Listing 17 creates a toy dataset which is not linearly separable. This dataset is plotted in Figure 15.

# Listing 17  
  
np.random.seed(0)  
n = 1550  
Xt1 = np.random.uniform(low=[0, 0], high=[4, 4], size=(n,2))  
drop = (Xt1[:, 0] < 3) & (Xt1[:, 1] < 3)  
Xt1 = Xt1[~drop]  
yt1= np.ones(len(Xt1))  
  
Xt2 = np.random.uniform(low=[0, 0], high=[4, 4], size=(n,2))  
drop = (Xt2[:, 0] > 2.3) | (Xt2[:, 1] > 2.3)  
  
Xt2 = Xt2[~drop]  
yt2= np.zeros(len(Xt2))  
  
X4 = np.concatenate([Xt1, Xt2])  
y4 = np.concatenate([yt1, yt2])  
  
scaler = StandardScaler()  
X4 = scaler.fit_transform(X4)  
  
colors = ['red', 'blue']  
plt.figure(figsize=(6, 6))  
for i in np.unique(y4):  
    plt.scatter(X4[y4==i, 0], X4[y4==i, 1], label = "y="+str(i),  
                color=colors[int(i)], edgecolor="white", s=50)  
  
plt.xlim([-1.9, 1.9])  
plt.ylim([-1.9, 1.9])  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='upper right', fontsize=11, framealpha=1)  
plt.show()

![[7559331831d3782183060f81adf019e3_MD5.png]]

Figure 15

This dataset has two features and a binary target. First, we try to use it to train a sigmoid neuron.

# Listing 18  
  
backend.clear_session()  
np.random.seed(2)  
random.seed(2)  
tf.random.set_seed(2)  
  
model4 = Sequential()  
model4.add(Dense(1, activation='sigmoid', input_shape=(2,)))  
model4.compile(loss = 'binary_crossentropy',   
               optimizer='adam', metrics=['accuracy'])  
history4 = model4.fit(X4, y4, epochs=4000, verbose=0,  
                      batch_size=X4.shape[0])

After training the network, we can plot the decision boundary using Listing 19. Figure 16 shows this plot.

# Listing 19  
  
plt.figure(figsize=(5,5))  
plot_boundary(X4, y4, model5, lims=[-2, 2, -2, 2])  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='upper right', fontsize=11, framealpha=1)  
plt.xlim([-1.9, 1.9])  
plt.ylim([-1.9, 1.9])  
plt.show()

![[a269163e2a0e6d04f2721940dce58157_MD5.png]]

Figure 16

The decision boundary is a straight line, as expected. However, in this dataset, a straight line cannot separate data points with different labels since the dataset is not linearly separable. We can only separate a fraction of the data points using this model resulting in a low prediction accuracy.

## **Hidden layers**

We learned that a single-layer neural network acts as a linear classifier. So, before proceeding to the output layer, we must first convert the original dataset into a linearly separable one. That is precisely what the _hidden layers_ in a multi-layer network do. The input layer receives the features from the original dataset. The features are then transferred to one or more hidden layers, which attempt to turn them into linearly separable features. Finally, the new features are transmitted to the output layer, which acts as a linear classifier.

The performance of a multiple-layer network is determined by the hidden layers’ capacity to linearize the input dataset. If the hidden layer is unable to turn the original dataset into a linearly separable one (or at least something close to it), the output layer will fail to provide an accurate classification.

Let’s create a multiple-layer network that can be trained using the previous dataset. Listing 20 defines a neural network with one hidden layer, depicted in Figure 17.

# Listing 20  
  
backend.clear_session()  
np.random.seed(2)  
random.seed(2)  
tf.random.set_seed(2)  
  
input_layer = Input(shape=(2,))  
hidden_layer = Dense(3, activation='relu')(input_layer)  
output_layer = Dense(1, activation='sigmoid')(hidden_layer)  
model5 = Model(inputs=input_layer, outputs=output_layer)  
  
model5.compile(loss = 'binary_crossentropy', optimizer='adam',  
               metrics=['accuracy'])

![[5ae639142b2b86b32613636ea2ad6157_MD5.png]]

Figure 17

The input layer has 2 neurons since the dataset has only two features. The hidden layer has 3 neurons, and each neuron has a ReLU (Rectified Linear Unit) activation function. This nonlinear activation function is defined as follows:

![[93b2497ba2e263174cb9b3c25ac8be1f_MD5.png]]

Figure 18 shows a plot of ReLU.

![[f0283601c7470a95195709ade6d47d2a_MD5.png]]

Figure 18

Finally, we have a sigmoid neuron in the output layer. Now, we train this model using our dataset and plot the decision boundary.

# Listing 21  
  
history5 = model5.fit(X4, y4, epochs=2200, verbose=0,  
                      batch_size=X4.shape[0])  
  
plt.figure(figsize=(5,5))  
plot_boundary(X4, y4, model5, lims=[-2, 2, -2, 2])  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='upper right', fontsize=11, framealpha=1)  
plt.xlim([-1.9, 1.9])  
plt.ylim([-1.9, 1.9])  
plt.show()

![[7f05fc00d5ff318cc01e1f4c0a8f81e5_MD5.png]]

Figure 19

The model can properly separate the data points with labels 0 and 1, but the decision boundary is not a straight line anymore. How the model could achieve that? Let’s take a look at the output of the hidden and output layers. Listing 22 plots the output of the hidden layer (Figure 20). Please note that we have three neurons in the hidden layer and their output is denoted by _a_₁, _a_₂ and _a_₃. Hence, we need to plot them in a 3D space. In this case, the decision boundary of the output layer is a plane that separates the data points of the hidden space.

# Listing 22  
  
hidden_layer_model = Model(inputs=model5.input,  
                           outputs=model5.layers[1].output)  
hidden_layer_output = hidden_layer_model.predict(X4)  
output_layer_weights = model5.layers[-1].get_weights()[0]  
output_layer_biases = model5.layers[-1].get_weights()[1]  
  
 w0 = output_layer_biases[0]  
 w1, w2, w3= output_layer_weights[0, 0], \  
  output_layer_weights[1, 0], output_layer_weights[2, 0]  
  
fig = plt.figure(figsize=(7, 7))  
ax = fig.add_subplot(111, projection='3d')  
# Plot the bounday  
lims=[0, 4, 0, 4]  
ga1, ga2 = np.meshgrid(np.arange(lims[0], lims[1], (lims[1]-lims[0])/500.0),  
                       np.arange(lims[2], lims[3], (lims[3]-lims[2])/500.0))  
  
ga1l = ga1.flatten()  
ga2l = ga2.flatten()  
ga3 = (0.5 - (w0 + w1*ga1l + w2*ga2l)) / w3  
ga3 = ga3.reshape(500, 500)  
ax.plot_surface(ga1, ga2, ga3, alpha=0.5)  
  
marker_colors = ['red', 'blue']  
target_labels = np.unique(y4)  
n = len(target_labels)  
for i, label in enumerate(target_labels):  
    ax.scatter(hidden_layer_output[y4==label, 0],  
               hidden_layer_output[y4==label, 1],  
               hidden_layer_output[y4==label, 2],  
               label="y="+str(label),  
               color=marker_colors[i])  
  
ax.view_init(0, 25)  
ax.set_xlabel('$a_1$', fontsize=14)  
ax.set_ylabel('$a_2$', fontsize=14)  
ax.set_zlabel('$a_3$', fontsize=14)  
ax.legend(loc="best")  
plt.show()

![[74e628edd6b1522ebbaa8abbb5115c29_MD5.png]]

Figure 20

The original dataset was two-dimensional and non-linearly separable. Hence the hidden layer transformed it into a 3D dataset which is now linearly separable. Then the plane created by the output layer easily classifies it.

So, we conclude that the nonlinear decision boundary shown in Figure 19 is like an illusion, and we still have a linear classifier at the output layer. However, when the plane is mapped to the original 2D dataset, it appears as a nonlinear decision boundary (Figure 21).

![[19300ccc677026cea1e228196dbf6ab1_MD5.png]]

Figure 21

## **The game of dimensions**

When a data point passes through each layer of a neural network, the number of neurons in that layer determines its dimension. Here each neuron encodes one of the dimensions. Since the original dataset is 2D, we need two neurons in the input layer. The hidden layer has three neurons, so it transforms the 2D data points into 3D data points. The additional dimension somehow unfolds the input dataset and helps with converting it into a linearly separable dataset. Finally, the output layer is simply a linear classifier in a 3D space.

The performance of a multiple-layer network is determined by the hidden layers’ capacity to linearize the input dataset. The hidden layer of the neural network defined in this example could transform the original dataset into a linearly separable dataset. In reality, though, that isn’t always possible. A dataset that is roughly linearly separable is sometimes the best result that the hidden layer can produce. As a result, certain data points may be mislabeled by the output layer. However, this is acceptable as long as the model’s overall accuracy is sufficient for practical applications.

Additionally, it is common to have a neural network with multiple hidden layers. In that case, the hidden layers combine to create a linearly separable dataset in the end.

## **The need for a nonlinear action function**

It is crucial to have a nonlinear activation function (such as ReLU) in the hidden layers. We can explain the importance of nonlinear activation functions using an example. Let’s replace the ReLU activation functions in the previous neural network with a linear activation function. A linear activation function is defined as follows:

![[1eaf705c55cf282ac0e8d0349de73dca_MD5.png]]

Figure 22 shows the plot of this activation function.

![[9c519ea9d422977e599f2cc9536fa007_MD5.png]]

Figure 22

Let’s now use a linear activation function for the hidden layer of the prior neural network in Figure 17. This redesigned neural network is illustrated in Figure 23.

![[a642c5fa3219bd1fa5f7bb36a3cc8241_MD5.png]]

Figure 23

Listing 23 defines the neural network and trains it with the previous dataset. The decision boundary is plotted in Figure 24.

# Listing 23  
  
backend.clear_session()  
np.random.seed(2)  
random.seed(2)  
tf.random.set_seed(2)  
  
input_layer = Input(shape=(2,))  
hidden_layer_linear = Dense(3, activation='linear')(input_layer)  
output_layer = Dense(1, activation='sigmoid')(hidden_layer_linear)  
model6 = Model(inputs=input_layer, outputs=output_layer)  
  
model6.compile(loss = 'binary_crossentropy',  
               optimizer='adam', metrics=['accuracy'])  
  
history6 = model6.fit(X4, y4, epochs=1000, verbose=0,  
                      batch_size=X4.shape[0])  
  
plt.figure(figsize=(5,5))  
plot_boundary(X4, y4, model6, lims=[-2, 2, -2, 2])  
ax = plt.gca()  
ax.set_aspect('equal')  
plt.xlabel('$x_1$', fontsize=16)  
plt.ylabel('$x_2$', fontsize=16)  
plt.legend(loc='upper right', fontsize=11, framealpha=1)  
plt.xlim([-1.9, 1.9])  
plt.ylim([-1.9, 1.9])  
plt.show()

![[21c3e49d029b2df95555ab2489efa101_MD5.png]]

Figure 24

We see that the decision boundary is still a straight line. This means that the hidden layer fails to linearize the dataset. Let’s explain the reason for that. Since we are using a linear activation function, the output of the hidden layer is as follows:

![[0b6d116c1f0467e127b83bccbee2e3e2_MD5.png]]

![[42fc240c66eb3d087df1e4d39194102b_MD5.png]]

![[dba6fd23a0cb8d5c7388c57a126305ee_MD5.png]]

These equations can be expressed in a vector form:

![[8481ab81e350122c657aa5f220e7fe0a_MD5.png]]

This means that each data point in the _a_₁_a_₂_a_₃ space is on a plane parallel to the vectors:

![[318069d9e0c281aae37ae8232856a478_MD5.png]]

Listing 24 plots the output of the hidden layer with the vectors **_v_**₁ and **_v_**₂. This plot is shown on the right-hand side of Figure 25.

# Listing 24  
  
fig = plt.figure(figsize=(7, 7))  
ax = fig.add_subplot(111, projection='3d')  
# Plot the bounday  
lims=[-3, 4, -3, 4]  
ga1, ga2 = np.meshgrid(np.arange(lims[0], lims[1], (lims[1]-lims[0])/500.0),  
                       np.arange(lims[2], lims[3], (lims[3]-lims[2])/500.0))  
  
ga1l = ga1.flatten()  
ga2l = ga2.flatten()  
ga3 = (0.5 - (w0 + w1*ga1l + w2*ga2l)) / w3  
ga3 = ga3.reshape(500, 500)  
ax.plot_surface(ga1, ga2, ga3, alpha=0)  
  
  
marker_colors = ['red', 'blue']  
target_labels = np.unique(y4)  
n = len(target_labels)  
for i, label in enumerate(target_labels):  
    ax.scatter(hidden_layer_output[y4==label, 0],  
               hidden_layer_output[y4==label, 1],  
               hidden_layer_output[y4==label, 2],  
               label="y="+str(label),  
               color=marker_colors[i], alpha=0.15)  
  
ax.quiver([0], [0], [0], hidden_layer_weights[0,0],  
          hidden_layer_weights[0,1], hidden_layer_weights[0,2],  
          color=['black'], length=1.1, zorder=15)  
ax.quiver([0], [0], [0], hidden_layer_weights[1,0],  
          hidden_layer_weights[1,1], hidden_layer_weights[1,2],  
          color=['black'], length=1.1, zorder=15)  
  
ax.view_init(30, 100)  
ax.set_xlabel('$a_1$', fontsize=14)  
ax.set_ylabel('$a_2$', fontsize=14)  
ax.set_zlabel('$a_3$', fontsize=14)  
ax.legend(loc="best")  
plt.show()

![[cd8eb6f32a5d4980c1a8c3899f4ef242_MD5.png]]

Figure 25

The data points in the _a_₁_a_₂_a_₃ space are apparently 3 dimensional, however, their mathematical dimension is 2 since they all lie on a 2D plane. While the hidden layer has 3 neurons, it cannot generate a real 3D dataset. It can only rotate the original dataset in a 3D space and stretch it along the vectors **_v_**₁ and **_v_**₂. However, these operations don’t break the structure of the original dataset and the transformed dataset remains non-linearly separable. Hence, the plane created by the output layer cannot classify the data points properly. When this plane is mapped back into the 2D space, it appears as a straight line (Figure 26).

![[b173a930aa72da74a110fce7388be02c_MD5.png]]

Figure 26

In conclusion, the number of neurons in the hidden layer is not the only factor that defines the mathematical dimension of the transformed dataset. Without a nonlinear activation function, the mathematical dimension of the original dataset doesn’t change, and the hidden layer fails to serve its purpose.

## **Neural networks for regression**

In this section, we will see how a neural network can solve a regression problem. In a regression problem, the target of the dataset is a continuous variable. We first create an example of such a dataset in Listing 25 and plot it in Figure 27.

# Listing 25  
  
np.random.seed(0)  
num_points = 100  
X5 = np.linspace(0,1, num_points)  
y5 = -(X5-0.5)**2 + 0.25  
  
fig = plt.figure(figsize=(5, 5))  
plt.scatter(X5, y5)  
plt.xlabel('x', fontsize=14)  
plt.ylabel('y', fontsize=14)  
plt.show()

![[ca92bd0c7b9497f2caaf7f2738820476_MD5.png]]

Figure 27

## **Single-layer networks**

We first try a single-layer neural network. Here the output layer has a single neuron with a linear activation function. This neural network is shown in Figure 28.

![[3d698316dbd8b97c5f194373cac18f21_MD5.png]]

Figure 28

Its output can be written as:

![[860de6829c6c8eb522ebb433a55bee5c_MD5.png]]

Now if we use a Mean Squared Error (MSE) cost function for that, it becomes like a linear regression model. Listing 26 uses the previous dataset to train such a network. Since the dataset has only one feature, the neural network ends up having only one neuron (Figure 29).

![[c5e2be5a65e2ddc326fe09ee1b89dc95_MD5.png]]

Figure 29

# Listing 26  
  
backend.clear_session()  
np.random.seed(0)  
random.seed(0)  
tf.random.set_seed(0)  
  
model6 = Sequential()  
model6.add(Dense(1, activation='linear', input_shape=(1,)))  
model6.compile(optimizer='adam', loss='mse', metrics=['mse'])  
history7 = model6.fit(X5, y5, epochs=500, verbose=0,  
                      batch_size=X5.shape[0])

After training the model, we can plot its prediction versus the original data points.

# Listing 27  
  
X5_test = np.linspace(0,1, 1000)  
yhat1 = model6.predict(X5_test)  
  
fig = plt.figure(figsize=(5, 5))  
plt.scatter(X5, y5, label="Train data")  
plt.plot(X5_test, yhat1, color="red", label="Prediction")  
plt.xlabel('x', fontsize=14)  
plt.ylabel('y', fontsize=14)  
plt.legend(loc="best", fontsize=11)  
plt.show()

![[f4509f58f039d3fa3e4f42c72d39920b_MD5.png]]

Figure 30

So, we conclude that a single-layer neural network with a linear activation function and an MSE cost function behaves similarly to a linear regression model.

## **Multiple-layer networks**

To learn a nonlinear dataset, we need to add hidden layers. Figure 31 shows an example of such a network. Here we have one hidden layer with linear activation functions.

![[30652587325966dd08a9227e8d7a99e2_MD5.png]]

Figure 31

However, this neural network also acts like a linear regression model. To explain the reason for that, we first write the outputs of the hidden layer:

![[b60fb4a2169942a21139d206b00e3c94_MD5.png]]

Now, we can calculate the output of the neural network:

![[1a3251296546f479fda78af82c585226_MD5.png]]

This means that with an MSE cost function, the neural network is still behaving like a linear model. To avoid this problem, we need to use a nonlinear activation function in the hidden layer.

In the next example, we replace the activation functions of the hidden layer with ReLU as shown in Figure 32. Here, the hidden layer has 10 neurons.

![[4e28450bf3e5a48a472c24cba14902f4_MD5.png]]

Figure 32

Listing 28 implements and trains this neural network.

# Listing 28  
  
backend.clear_session()  
np.random.seed(15)  
random.seed(15)  
tf.random.set_seed(15)  
  
input_layer = Input(shape=(1,))  
x = Dense(10, activation='relu')(input_layer)  
output_layer = Dense(1, activation='linear')(x)  
model7 = Model(inputs=input_layer, outputs=output_layer)  
  
model7.compile(optimizer='adam', loss='mse', metrics=['mse'])  
  
history8 = model7.fit(X5, y5, epochs=1500, verbose=0,  
                      batch_size=X5.shape[0])  
  
hidden_layer_model = Model(inputs=model7.input,  
                           outputs=model7.layers[1].output)  
hidden_layer_output = hidden_layer_model.predict(X5_test)  
output_layer_weights = model7.layers[-1].get_weights()[0]  
output_layer_biases = model7.layers[-1].get_weights()[1]

After training, we can finally plot the prediction of this neural network.

# Listing 29  
  
X5_test = np.linspace(0,1, 1000)  
yhat2 = model7.predict(X5_test)  
  
fig = plt.figure(figsize=(5, 5))  
plt.scatter(X5, y5, label="Train data", alpha=0.7)  
plt.plot(X5_test, yhat2, color="red", label="Prediction")  
plt.xlabel('x', fontsize=14)  
plt.ylabel('y', fontsize=14)  
plt.legend(loc="best", fontsize=11)  
plt.show()

![[b1df6e6f8b352193f678fe46f0c22fe2_MD5.png]]

Figure 33

We see that the network can now generate a nonlinear prediction. Let’s take a look at the hidden layer. The next Listing plots the outputs of the hidden layer _a_₁..._a_₁₀ in Figure 34. The output neuron first multiplies each _aᵢ_ by its corresponding weight (_wᵢ_^[1]_aᵢ_). Finally, it computes the following sum

![[7777920738a15306a4b2619824f99f8a_MD5.png]]

which is the prediction of the neural network. All these terms are plotted in Figure 34.

# Listing 30  
  
fig, axs = plt.subplots(10, 4, figsize=(18, 24))  
plt.subplots_adjust(wspace=0.55, hspace=0.2)  
  
for i in range(10):  
    axs[i, 0].plot(X5_test, hidden_layer_output[:, i], color="black")  
    axs[i, 1].plot(X5_test,   
                   hidden_layer_output[:, i]*output_layer_weights[i],  
                   color="black")  
    axs[i, 0].set_ylabel(r'$a_{%d}$' % (i+1), fontsize=21)  
    axs[i, 1].set_ylabel(r'$w^{[1]}_{%d}a_{%d}$' % (i+1, i+1), fontsize=21)  
    axs[i, 2].axis('off')  
    axs[i, 3].axis('off')  
axs[i, 0].set_xlabel("x", fontsize=21)  
axs[i, 1].set_xlabel("x", fontsize=21)  
  
axs[4, 2].axis('on')  
axs[6, 2].axis('on')  
axs[4, 2].plot(X5_test, [output_layer_biases]*len(X5_test))  
axs[6, 2].plot(X5_test,  
               (hidden_layer_output*output_layer_weights.T).sum(axis=1))  
axs[6, 2].set_xlabel("x", fontsize=21)  
axs[4, 2].set_ylabel("$w^{[1]}_0$", fontsize=21)  
axs[4, 2].set_xlabel("x", fontsize=21)  
axs[6, 2].set_ylabel("Sum", fontsize=21)  
axs[5, 3].axis('on')  
axs[5, 3].scatter(X5, y5, alpha=0.3)  
axs[5, 3].plot(X5_test, yhat2, color="red")  
axs[5, 3].set_xlabel("x", fontsize=21)  
axs[5, 3].set_ylabel("$\hat{y}$", fontsize=21)  
plt.show()  

![[64cc4078737fb29342ac6629330a1c75_MD5.png]]

Figure 34

In our neural network, each neuron in the hidden layer has a ReLU activation function. We showed the plot of the ReLU activation function in Figure 18. It consists of two lines that intersect at the origin. The one on the left is horizontal, while the other has a slope of one. The weight and bias of each neuron in the hidden layer modifies the shape of ReLU. It can change the location of the intersection point, the order of these lines, and the slope of the non-horizontal line. After that, the weight of the output layer can also change the slope of the non-horizontal line. An example of such changes is shown in Figure 35.

![[9e5002e65a24709fa37dc41ffd83779e_MD5.png]]

Figure 35

The modified ReLU functions are then combined to approximate the shape of the target of the dataset, as shown in Figure 36. Each modified ReLU function has a simple structure, but a large number of them when combined can approximate any continuous function. At the end, the bias of the output layer is added to the sum of the ReLU functions to adjust them vertically.

![[07e9ceb5a106dff4de2ea8a885586b17_MD5.png]]

Figure 36

The _Universal Approximation Theorem_ states that a feedforward neural network with one hidden layer containing a sufficiently large number of neurons can approximate any continuous function on a subset of inputs with any desired accuracy, provided the activation function is non-constant, bounded, and continuous. To demonstrate this in practice, we used the same neural network from Listing 28, but with 400 neurons in the hidden layer this time. Figure 37 shows the prediction of this neural network. You can see that adding more neurons to the hidden layer significantly improves the neural network’s ability to approximate the target.

![[eae009955af7315ec92ed60b8bafc5cc_MD5.png]]

Figure 37

In this article, we presented a visual understanding of neural networks and the role that each layer plays in making the final prediction. We started with perceptrons and showed the limitations of a single-layer network. We saw that in a classification problem, a single-layer neural network is equal to a linear classifier and in a regression problem the behaviour is like a linear regression mode. The role of hidden layers and nonlinear activation function was explained. In a classification problem, the hidden layer tries to linearize a non-linearly separable dataset. In regression problems, the output of the neurons in the hidden layer is like nonlinear building blocks that are added together to make the final prediction.

[

## Get an email whenever Reza Bagheri publishes.

### Get an email whenever Reza Bagheri publishes. By signing up, you will create a Medium account if you don't already have…

reza-bagheri79.medium.com



](https://reza-bagheri79.medium.com/subscribe?source=post_page-----64083c7eb29c---------------------------------------)

I hope that you enjoyed reading this article. If you feel my articles are helpful, please follow me on Medium. All the Code Listings in this article are available for download as a Jupyter Notebook from GitHub at:

[https://github.com/reza-bagheri/neural_nets_visualization/blob/main/neural_nets_visulization.ipynb](https://github.com/reza-bagheri/neural_nets_visualization/blob/main/neural_nets_visulization.ipynb)

---

