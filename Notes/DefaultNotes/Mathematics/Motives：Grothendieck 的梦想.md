
---

https://zhuanlan.zhihu.com/p/681501229

---

[![[a5d30afa945236503e568b0634b68a95_MD5.jpg]]](https://www.zhihu.com/people/xiao-cai-ji-6-47)

[研数学 习物理](https://www.zhihu.com/people/xiao-cai-ji-6-47)

”研数学 习物理“公众号的同步

​**写在前面：** 本文我们介绍代数几何以及代数 K 理论中的 Motives , 原作者为 James S.Milne , 之前在[《数学译林》](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E3%80%8A%E6%95%B0%E5%AD%A6%E8%AF%91%E6%9E%97%E3%80%8B&zhida_source=entity)上徐克舰老师发表了关于此文的译文 ，由于《数学译林》官网上无法找到年代久远的文章 , 小编也将此文翻译了一遍 , 在翻译过程中略有改动 , 但不影响作者原来想表达的意思 .

## **0.前言**

1964的时候 [Grothendieck](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=Grothendieck&zhida_source=entity) 在给 Serre 的一封信中提到了 Motive 的概念 . 后来他又写道 , 在他有幸发现的东西中 , 它们是最充满神秘感的且可能形成了最强有力的发现工具 . 在这篇文章中 , 我们将试图解释什么是 Motive 以及为什么 Grothendieck 如此重视它们的原因 .

## **1.拓扑中的上同调**

考虑一个 2n 维紧致实流形 X , 存在 X 的上[同调群](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%90%8C%E8%B0%83%E7%BE%A4&zhida_source=entity)

H0(X,Q),H1(X,Q),⋯,H2n(X,Q)

是满足 Poincaré 对偶( Hi 对偶于 H2n−i )的有限维 Q-向量空间 , 且同时满足 Lefschetz [不动点定理](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E4%B8%8D%E5%8A%A8%E7%82%B9%E5%AE%9A%E7%90%86&zhida_source=entity)等 , 事实上有很多种方法来定义这些上同调群 , 如奇异上链 , Čech 上同调和导出函子 , 但不同的方式均给出了完全相同的群 , 假如它们满足 Eilenberg-Steenrod 公理体系 . 当 X 是复解析流形时 , 则有 de Rham 上同调群 HdRi(X) , 这些都是 C 上的向量空间 , 但它们不是新的群 , 毕竟有下面的[典范同构](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%85%B8%E8%8C%83%E5%90%8C%E6%9E%84&zhida_source=entity)

HdRi(X)≅Hi(X,Q)⊗QC

然而当 X 是 Kahler 流形时 , de Rham 上同调群具有 Hodge 分解 , 因此能提供更多的信息 .

## **2.代数几何中的上同调**

现在我们考虑一个在代数闭域 k 上的 n 维非异[射影代数簇](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%B0%84%E5%BD%B1%E4%BB%A3%E6%95%B0%E7%B0%87&zhida_source=entity) X , 则 X 由 k 上的一些多项式来定义 , 且上述非异射影的条件意味着当 k=C 时 , 则簇上的一些点 k(C) 构成了一个 2n 维紧致流形 .

Weil 的关于代数簇上的坐标在有限域中的点的个数的工作使得他在1949年提出了著名的 Weil 猜想 , 即给出了有限域上[方程的解](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E6%96%B9%E7%A8%8B%E7%9A%84%E8%A7%A3&zhida_source=entity)的个数与相应的复系数方程定义的簇的拓扑性质之间的关系 . 特别地 , 他发现这些点的个数似乎是由 C 上的某种类似的代数簇的 [Betti 数](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=Betti+%E6%95%B0&zhida_source=entity)所确定 . 例如对于 p [元有限域](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%85%83%E6%9C%89%E9%99%90%E5%9F%9F&zhida_source=entity) Fp=Z/pZ 上的亏格为 g 的曲线 X , 其中 p 是素数 , 曲线 X 上的点的个数 |X(Fp)| 满足下面的不等式

||X(Fp)|−p−1|≤2gp12

其中 g 是曲线 X 的亏格 .

Weil 能通过计算 Fp 上的相同维数和次数超曲面上的点的个数来预测 C 上的某些超曲线的 Betti 数 , 事实上他的猜测被 Dolbeault 证实 . 很显然 Weil 的大多数猜想都来源于代数簇的[上同调理论](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E4%B8%8A%E5%90%8C%E8%B0%83%E7%90%86%E8%AE%BA&zhida_source=entity)中具有的一些良好的性质( Q 系数 , 恰当的 Betti 数 , Poincaré [对偶定理](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%AF%B9%E5%81%B6%E5%AE%9A%E7%90%86&zhida_source=entity) , Lefschetz 不动点定理等) , 事实上正如我们看到的那样 , 并不存在这样的具有 Q 系数的上同调理论 , 但在接下来的几年里 , 数学家们试图寻找一个除了 Q 以外系数属于某些特征零的域上的好的上同调理论 . 最终在20世纪60年代 , Grothendieck 定义了平展上同调(étale cohomology)和晶体上同调([crystalline cohomology](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=crystalline+cohomology&zhida_source=entity)) , 并证明了用代数方法定义的 de Rham 上同调在域的特征零的点处具有良好的性质 , 然后问题就转化为我们具有太多的良好的上同调理论 .

每一个素数 l 除了在 Q 上通常的赋值以外 , 还存在另一种由 |lrmn|=l−r 定义的赋值 , 其中 m,n∈Z 且不被 l 整除 . 每一次赋值使得 Q 成为一个新的[度量空间](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%BA%A6%E9%87%8F%E7%A9%BA%E9%97%B4&zhida_source=entity) , 然后将这些新的度量空间完备化以后我们就可以得到一些域 Q2 , Q3 , Q5 , ⋯ , R . 对每一个不同于特征 k 的素数 l , 平展上同调给出了下面的上同调群

Het0(X,Ql),Het1(X,Ql),⋯,Het2n(X,Ql)

这些都是 Ql 上的有限维向量空间且满足 Poincaré 对偶定理以及 Lefschetz 不动点定理等 , 同样前面提到的 de Rham 上同调群 HdRi(X) 也是域 k 上的有限维向量空间 , 而且特征 p≠0 时存在晶体上同调群是特征零的域上的有限维向量空间 , 这里的特征零的域指的是系数属于 k 的 Witt 向量环的分次域 .

这些上同调理论不可能是相同的 , 因为它们在不同的域上给出了向量空间 , 但它们也绝非毫无关联 , 比如映射的迹 αi:Hi(X)→Hi(X) 是由代数簇 X 之间的[正则映射](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E6%AD%A3%E5%88%99%E6%98%A0%E5%B0%84&zhida_source=entity) α:X→X 所诱导出来的一个与上同调理论无关的有理数 . 因此种种现象表明似乎是存在由代数方法定义的 Q 上同调群 Hi(X,Q) 使得 Heti(X,Ql)≅Hi(X,Q)⊗QQl , 但我们知道并不是这样 .

## **3.为什么不存在由代数定义的 Q 上同调**

为什么不存在由代数定义的 Q 上同调即从代数簇到 Q-向量空间的函子来诱导 Grothendieck 所定义的这些不同的上同调 , 那么我们给出两种解释 , 第一种适用于非零特征域 k , 而第二种适用于任意特征域 k .

(i) 第一种解释

椭圆曲线 E 是亏格为 1 且具有特定的点的曲线 , 这里特定的点是群结构的零元 . 在 C 上 E(C) 是一个 Abel 群且同构于关于格 Λ 的商群 , 因此从拓扑角度来讲 E(C) 是环面 . 而 E 的[自同态](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E8%87%AA%E5%90%8C%E6%80%81&zhida_source=entity)是满足 αΛ=Λ 的复数 α 定义的映射 z+Λ↦αz+Λ , 于是我们很容易就得到了 End(E) 是秩为 1 或 2 的 Z-模 , 进而有 End(E)Q=Q 或者 End(E)Q 是 Q 上的一个[二次扩域](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E4%BA%8C%E6%AC%A1%E6%89%A9%E5%9F%9F&zhida_source=entity) . 那么上同调群 H1(X(C),Q) 作为一个 Q-[向量空间的维数](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%90%91%E9%87%8F%E7%A9%BA%E9%97%B4%E7%9A%84%E7%BB%B4%E6%95%B0&zhida_source=entity)为 2 , 而在第二种情形下则是一个 1 维 End(E)Q-向量空间 , 这里 End(E)Q=End(E)⊗Q .

在特征 p≠0 时存在第三种可能性 , 即End(E)Q 可能成为一个 Q 上的 4 次可除代数 , 这是一个非交换域 , 而这种可除代数能作用于其上的最小的 Q-向量空间是 4 维的 . 因此不存在 Q-向量空间 H1(E,Q) 成为一个 End(E)Q-模且满足 H1(E,Ql)≅H1(E,Q)⊗QQl .

(ii) 第二种解释

令 X 是特征为零的代数闭域 k 上的非异射影簇 , 当我们选择一个嵌入 k↪C , 就得到了一个[复流形](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%A4%8D%E6%B5%81%E5%BD%A2&zhida_source=entity) X(C) 且满足

Heti(X,Ql)≅Hi(X(C),Q)⊗QlHdRi(X)⊗kC≅Hi(X(C),Q)⊗QC

换句话说 , 每一个嵌入 k↪C 确实定义了在不同的上同调群上的 Q-结构 , 然而不同的嵌入给出了不同的 Q-结构 , 这意味着它们不是来源于通过代数方法定义的 Q-上同调 .

当我们注意到这一点后 , 由于 X 是由只有有限多个系数的有限多个多项式所定义 , 故它在 k 的子域 k0 上存在一个模 X0 使得 k 是 k0 的有限 Galois 扩张 , 即可以设 Γ=Gal(k/k0) 是 k 在 k0 上的 Galois 群 , 于是选择这样一个模就确定了 Γ 在 Heti(X,Ql) 上的一个作用 . 如果 k0 上不同的从 k 到 C 的嵌入给出了Heti(X,Ql) 中相同的子空间 Hi(X(C),Q) , 那么 Γ 在 Heti(X,Ql) 上的作用可以使得 Hi(X,Q) 稳定化 . 但是无限 Galois 群是不可数的而 Hi(X,Q) 是可数的 , 这意味着可以诱导出 Γ 在 Heti(X,Ql) 上作用的一个有限商群 , 然而这通常是不正确的 . 粗略地讲 , Tate 猜想表明当 k0 是 Q 上有限生成扩张时 , Galois 群在 Aut(Heti(X,Ql)) 的像很大程度上只由代数链(cycle)的存在性限制 .

同理可知 , 能够在 Ql-上同调上给出 Q-结构的代数定义的上同调将使得 Γ 诱导出有限商群的作用 , 因此不可能存在一种 Q-上同调理论来诱导出 Grothendieck 所定义的所有这些不同的上同调理论 , 但是我们该如何解释种种迹象都表明似乎存在这样的事实 , 此时 Grothendieck 的回答是 Motive 理论 .

## **4.代数链**

在正式讨论 Motive 理论之前 , 我们需要解释一下代数链 .

(i)定义

设 X 是域 k 上的 n 维非异射影代数簇 , 而 X 上的素链就是 X 上的一个闭子簇 Z , 其中 Z 不能表示为两个真闭子代数簇的并 , 它的余维数是 n−dim⁡Z , 如果 Z1 和 Z2 都是素链 , 那么有

codim(Z1∩Z2)≤codim(Z1)+codim(Z2)

当上式等号成立时就意味着 Z1 和 Z2 是真相交(intersect properly) .

设 Cr(X) 是 X 的余维数为 r 的代数链群 , 即是由余维数为 r 的素链生成的自由 Abel 群 , 而两个代数链 γ1 和 γ2 被称为真相交是指 γ1 的每个素链与 γ2 的每个素链真相交 , 这样的情形下我们称 γ1⋅γ2 为交积(insertsection product) , 其中交积定义为余维数 codimZ1+codimZ2 的链 , 如下图所示

![[c56fd0c1d48b3319a47975cdf81fadb4_MD5.webp]]

因此我们用这种方式得到了部分有定义的映射

Cr(X)×Cs(Y)→Cr+s(X)

为了得到在整个集合上有定义的映射 , 我们需要移动代数链 . X 的两个代数链 γ 和 γ′ 为有理等价(rationally equivalent)是指存在 X×P1 上的一个代数链使得 γ−γ′ 作为 P1 上某一点上的纤维和 0 作为第二个点上的纤维 , 这就给出了相当于代数上的同伦等价的一个等价关系 , 特别地 , 任意两个代数链 γ1 和 γ2 都分别有理等价于真相交的代数链 γ1′ 和 γ2′ , 且 γ1′⋅γ2′ 的有理等价类不依赖于 γ1′ 和 γ2′ 的选择 . 于是令 Cratr(X) 表示相应的商群 , 那么就由交积定义了一个[双线性映射](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%8F%8C%E7%BA%BF%E6%80%A7%E6%98%A0%E5%B0%84&zhida_source=entity)

Cratr(X)×Crats(Y)→Cratr+s(X)

再设 Crat∗(X)=⨁r=0dim⁡XCratr(X) , 这是一个 Q-代数 , 称为 X 的 Chow 环 .

事实上[射影平面](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%B0%84%E5%BD%B1%E5%B9%B3%E9%9D%A2&zhida_source=entity) P2 上余维数为 1 的素链是由不可约齐次多项式 P(x0,x1,x2) 定义的曲线 , 且由多项式定义的两个素链彼此有理等价当且仅当这两个多项式具有相同的次数 , 此时有 Crat1(P2)≅Z 且它以 P2 中任意直线所在的类为基 . 而 P1×P1 中余维数为 1 的素链是由一个关于每一对 (x0,x1) 和 (y0,y1) 均为可分齐次[不可约多项式](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E4%B8%8D%E5%8F%AF%E7%BA%A6%E5%A4%9A%E9%A1%B9%E5%BC%8F&zhida_source=entity) p(x0,x1;y0,y1) 定义的曲线 , 故这个链的有理等价类有一对次数所决定 , 此时有 Crat1(P1×P1)≅Z×Z 且以 {0}×P1 和 P1×{0} 的类为基 , 那么对角 Δp1 与 {0}×P1+P1×{0} 有理等价 .

我们需要作出一些解释 . 有理等价(rationally equivalent)是指能够在等价类上给出映射 Cr(X)×Cs(Y)→Cr+s(X) 的最精细的代数链的等价关系且满足某些自然条件 . 而最粗略的这种等价关系是数值等价(numerical equivalent) , 即两个代数链 γ 和 γ′ 对所有的具有余维数的代数链 δ 满足 γ⋅δ=γ′⋅δ , 其中余维数是由相交数所定义 , 那么代数链的数值等价类构成环 Cnum∗(X)=⨁r=0dim⁡XCnumr(X) ， 这是 Chow 环的商环 . 因此从现在开始 ∼ 表示有理等价 rat 或数值等价 num .

(ii)链映射

对所有的我们感兴趣的上同调理论 , 存在一个链等价类映射

cl:Crat∗(X)Q→H∗(X)=⨁r=02dim⁡XHr(X)

将次数翻倍后以及将交积映为杯积(cup product) .

(iii) 多值映射或对应

我们仅仅对反变函子的上同调理论感兴趣 , 即由一个代数簇的正则映射 f:Y→X 可以定义同态 Hi(f):Hi(X)→Hi(Y) . 事实上这是一个很弱的条件 , 因为一般来说从一个代数簇到另一个代数簇之间的正则映射是很少的 , 相反我们应该允许使用多值映射 , 更确切地说可以称之为对应(correspondence) .

定义从 X 到 Y 的 r 次对应群为

Corrr(X,Y)=Cdim⁡X+r(X×Y)

事实上正则映射 f:Y→X 的图(graph) Γf 属于 Cdim⁡X(Y×X) , 而它的转置 ΓfT 属于 Cdim⁡X(X×Y)=Corr0(X,Y) , 这表明从 Y 到 X 的正则映射定义了一个从 X 到 Y 的 0 次对应 . 那么这个从 X 到 Y 的 0 次对应 γ 定义了一个同态

H∗(X)→H∗(Y) , x↦q∗(p∗x∪cl(γ))

其中 p 和 q 是投影映射 X←pX×Y→qY , 于是由 ΓfT 给出的上同调的映射和由 f 给出的上同调的映射是一致的 , 因此我们有下面的记号

Corr∼r(X,Y)=Corrr(X,Y)/∼Corr∼r(X,Y)Q=Corr∼r(X,Y)⊗ZQ

## **5. Motive 的定义**

Grothendieck 的想法是应该存在一个泛上同调理论且它的取值由 Motive 构成的 Q-范畴 M(k) , 这里的关于域 k 上的 Motive 是指类似于 k 上的代数概形的 l-adic 上同调群且不依赖于 l 的取值 , 同时可以根据代数链理论推出 , 它具有整结构或 Q 结构 , 但遗憾的是无法去定义这个由 Motive 构成的 Abel 范畴 . 因此 M(k) 应该是一个类似于有限维 Q-向量空间范畴 VecQ 的范畴但不是完全相似 , 特别地 , Hom(X,Y) 应该是一个有限维 Q-向量空间 , M(k) 应该是一个 Abel 范畴 , 进而 M(k) 应该是一个 Q 上的 Tanaka 范畴 , 故存在一个泛上同调理论 非异射影簇X⇝hX:非异射影簇→M(k) , 尤其是每一个代数簇 X 上应该定义一个 Motive hX , 以及每一个从 X 到 Y 的 0 次对应可以定义一个同态 hX→hY , 同理一个正则映射 f:Y→X 也应该定义了一个同态 hX→hY , 而每一个好的上同调理论(例如 Weil 上同调)应该可以唯一通过 X⇝hX 分解 .

(i) 首次尝试

我们可以简单地将 M∼(k) 定义为这样的范畴 , 即对域 k 上的每一个非异射影簇 X 上存在对象 hX , 而态射则是由 Hom(hX,hY)=Corr∼0(X,Y)Q 定义 , 以及态射的合成就是对应的合成 , 故 M∼(k) 是一个范畴 , 但这样却存在着明显地缺陷 , 如果一个 Q-向量空间 V 的自同态 e 满足 e2=e , 那么它可以将这个向量空间分解成 0 和 1 的[特征子空间](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E7%89%B9%E5%BE%81%E5%AD%90%E7%A9%BA%E9%97%B4&zhida_source=entity) , 即 V=Ker(e)⊕eV , 设 (W,f) 是不同于 (V,e) 的另一个对 , 此时在 HomQ(V,W) 中有

HomQ(eV,fW)≅f∘HomQ(V,W)∘e

同样的结论在任意的 Abel 范畴中也成立 . 因此如果我们希望 M∼(k) 成为 Abel 范畴 , 那么至少应该把幂等态射的像也添加到

End(hX)=Corr∼0(X,X)Q=C∼dim⁡X(X×X)Q

中去 , 其中这里的 Q-向量空间为 Q-线性空间 .

(ii) 二次尝试

现在我们对定义 M∼(k) 为怎样的范畴进行这样的尝试 , 即 M∼(k) 的对象为二元对 h(X,e) , 其中 X 为非异射影簇以及 e 为环 Corr∼0(X,X)Q 中的[幂等元](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%B9%82%E7%AD%89%E5%85%83&zhida_source=entity) , 而态射则由

Hom(h(X,e),h(Y,f))=f∘Corr∼0(X,Y)Q∘e

定义 , 这里的 Hom(h(X,e),h(Y,f)) 是 Corr∼0(X,Y)Q 的子集 , 这正是我们想要的结果 . 事实上关于有理等价还是数值等价的有效 Motive 范畴是依赖于 ∼ 的选择并记作 M∼eff(k) . 而前面定义的 Motive 范畴可以看作是由 h(X,ΔX) 为对象构成的全子范畴 .

根据上面的讨论结果 , 我们可以得到 Corrrat0(P1,P1)=Z⊕Z 且 e0=(1,0) 和 e0′=(0,1) 则分别由 {0}×P1 和 P1×{0} 所代表 , 与分解 ΔP1∼e0+e0′ 相对应 , 我们可以得到分解 h(P1,ΔP1)=h0P1⊕h0′P1 , 其中 h0P1=h(P1,e0) 和 h′0P1=h(P1,e0′) , 而这个结果在 Mrateff(k) 和 Mnumeff(k) 中都成立 , 我们记 L=h0P1 和 L′=h′0P1 .

从某种意义上讲 , 有效 Motive 范畴是最有用的 , 事实上在研究具有 Z 系数而不是 Q 系数的有限域上的有效 Motive 范畴时 , Niranjan Ramachandran 和 Grothendieck 发现了这样的范畴中的 Ext 的阶数和 Zeta-函数的特殊值之间存在一个非常美妙的关系 , 而从有效 Motive 范畴过渡到 Motive 的整个范畴时这个关系却不存在了 , 但一般情况下则更倾向于一个在其中的每一个对象都存在对偶的范畴 , 那么我们可以将 L′ 取逆来实现它 .

(iii) 三次尝试

继续对范畴 M∼(k) 的定义进行尝试 , 现在设 M∼(k) 的对象为三元对 h(X,e,m) , 其中 X 为非异射影簇 , e 是环 Corr∼0(X,X)Q 中的幂等元 , 而 m∈Z , 于是态射定义为

Hom(h(X,e,m),h(Y,f,n))=f∘Corr∼n−m(X,Y)Q∘e

这就是 k 上的 Motive 范畴 , 而前两次定义的 Motive 范畴可以看作是由 h(X,e,0) 为对象的全子范畴 . 有时候称 Mrat(k) 为 Chow Motive 范畴或有理 Motive 范畴 , 而称 Mnum(k) 为 Grothendieck Motive 范畴或数值 Motive 范畴 .

## **6. 什么是 Motive 范畴**

(i) M∼(k) 范畴的性质

态射集合 Hom 是 Q-向量空间 , 如果 ∼ 为 num , 那么它是有限维的向量空间 , 但其它情形一般不是有限维的 . 由于 Motive 范畴的直和是存在的 , 故 M∼(k) 是[加法范畴](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%8A%A0%E6%B3%95%E8%8C%83%E7%95%B4&zhida_source=entity) , 即满足

h(X,e,m)⊕h(Y,f,m)=h(X⊔Y,e⊕f,m)

而 Motive 范畴 M 的自同态环中的一个幂等元 f 能将 M 分解为 f 的核与 f 的像的直和 , 于是 M∼(k) 是一个伪 Abel 范畴 , 即如果 M=h(X,e,m) , 那么有 M∼(k) 是加法范畴 , 即满足

M=h(X,e−efe,m)⊕h(X,efe,m)

事实上 Mnum(k) 范畴是一个 Abel 范畴且是半单范畴 , 但一般 M∼(k) 一般不是 Abel 范畴 , 只有当 k 是有限域的代数扩域时 M∼(k) 有可能是 Abel 范畴 , 此时自然函子 Mrat(k)→Mnum(k) 是一个范畴等价 . 其实 M∼(k) 上具有良好的[张量积](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%BC%A0%E9%87%8F%E7%A7%AF&zhida_source=entity)结构且定义为

h(X,e,m)⊗h(Y,f,n)=h(X×Y,e×f,m+n)

令 hX=h(X,ΔX,0) , 则有 hX⊗hY=h(X×Y) , 因此对于 X⇝hX , 我们有 Kunneth 公式成立 . 上面的结论对有效 Motive 范畴也是成立的 , 但是在 M∼(k) 范畴中 , 其对象存在对偶 , 这表明对于每个 Motive 范畴 M , 均存在对偶 Motive 范畴 M∨ 以及赋值映射 ev:M∨⊗M→1 且满足某种泛性质 , 其中 1=h0P1 , 当 X 为具有连通性质的非异射影代数簇时我们有

h(X,e,m)∨=h(X,et,dim⁡X−m)

值得一提的是 , 尽管 Mrat(k) 不是 Abel 范畴 , 但它依然是非常重要的范畴 , 尤其是它包含了比 Mnum(k) 更多的信息 .

(ii) X⇝hX 函子是泛上同调理论么？

当然函子 X⇝hX 将 X 映为其 Chow Motive 范畴 hX 是存在泛性质的 , 这几乎可以是在反复强调 , 良好的上同调理论是可以通过 Mrat(k) 进行分解的理论 . 然而对于 Mnum(k) 却存在如下问题 , 即一个数值等价于零的对应将给出 Motive 范畴之间的零映射 , 但一般情况下我们不知道 Mnum(k) 在上同调上是否也可以定义零映射 , 于是为了使一个良好的上同调理论能通过 Mnum(k) 分解 , 则必须满足下面的猜想 .

> 猜想1：如果一个代数链数值等价于零 , 那么这个代数链的上同调类也为零 .  

换句话说 , 如果 cl(γ)≠0 , 那么 γ 不可能数值等价于零 , 再结合 Poincaré 对偶定理 , 我们可以将上述猜想重新描述为如果存在上同调类 γ′ 满足 cl(γ)∪γ′≠0 , 那么存在一个代数链 γ″ 使得 γ⋅γ″≠0 . 因此猜想1是一个关于代数链的存在性的断言 . 遗憾的是我们无法证明代数链的存在性 , 具体地说当我们希望一个上同调是代数的即为代数链类 , 目前我们无法给出具体的证明 . 这是目前算术几何和代数几何的主要问题 . 事实上在域的特征为零时 , 猜想1对于 Abel 簇是成立的且可以由 Hodge 猜想推出 .

(iii) 为什么范畴 hX 不是分次的？

当我们假设上面的猜想1是成立的 , 那么每一个良好的上同调理论 H 的确能通过函子 X⇝hX 来分解 . 这意味着存在从 Mnum(k) 到 H 的基域上的向量空间范畴的函子 ω 使得

ω(hX)=H∗(X)=⨁i=02dim⁡XHi(X)

显然存在 hX 上的一个分解使得 hX 能成为每个良好的上同调理论所具有的 H∗(X) 分解的基础 , 事实上对于 P1 根据 h(P1,ΔP1)=h0P1⊕h0′P1 可知其正确性 , 其中 h0P1=h(P1,e0) 和 h′0P1=h(P1,e0′) , 下面我们给出一个由 Grothendieck 提出的猜想 .

> 猜想2：在环 End(hX)=Cnumdim⁡X(X×X) 中 , 对角态射 ΔX 可以典范地分解为正交幂等元的和  
> ΔX=π0+π1+⋯+π2dim⁡X即上面这个表达式定义了下面的一个分解  
> hX=h0X⊕h1X⊕⋯⊕h2dim⁡XX其中 hiX=h(X,πi,0) , 而这个分解应该满足这样的性质 , 即对于每个满足猜想1的良好的上同调理论 , 则给出分解  
> H∗(X)=H0(X)⊕H1(X)⊕⋯⊕H2dim⁡X(X)

事实上猜想2也是关于代数链的存在性的断言 , 故也是很困难的一个猜想 , 而对于有限域上非异射影簇和特征零的 Abel 簇 , 猜想2是成立的 , 其中有限域上的非异射影簇意味着对于某个 Frobenius 映射的多项式可用于分解 Motive 范畴 , 而特征零的 Abel 簇则意味着根据定义可知 Abel 簇具有交换群的结果 , 映射 m:X→X 可用于分解 hX , 其中 X∈Z .

我们不妨假设猜想2是正确的 , 此时我们可以讨论 Motive 范畴的权 , 已知 Motive 范畴 hiX 的权为 i 以及 h(X,πi,m) 的权为 i−2m , 于是纯粹 Motive 范畴是指 Motive 范畴上具有单一的权 , 而每个 Motive 范畴均为纯粹 Motive 范畴的直和 . 因此只有证明了猜想2和猜想1 , Grothendieck 的梦想才能实现 .

注：Murre 曾经猜测 ΔX=π0+π1+⋯+π2dim⁡X 这样的分解即使在 End(hX)=Cnumdim⁡X(X×X) 中也是存在的 , 目前已经证明 Murre 的猜想等价于 Beilinson 和 Bloch 关于 Chow 群上的一个令人感兴趣的滤链的存在性的猜想 .

(iv) 什么是 Tannakian 范畴？

一个[仿射群](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E4%BB%BF%E5%B0%84%E7%BE%A4&zhida_source=entity)是一个矩阵群 , 可能这个矩阵群是无限维的 , 更确切地说 , 仿射群是域上的仿射群概形且未必是有限型概形 , 而每个这样的群都是那些能够计算出某个 GLn 的子群的仿射代数群概形的逆向极限 . 对于 Q 上的仿射群 G , 它在有限维 Q-向量空间上的表示的全体构成一个附带了张量积和对偶的 Abel 范畴 RepQ(G) , 而遗忘函子则是一个从 RepQ(G) 到 VecQ 的保持张量积的忠实函子 .

Q 上的一个中性 Tannakian 范畴 T 是指一个附带了张量积和对偶 , 并存在到 VecQ 的保持张量积的忠实正合函子的 Abel 范畴 . 这样一个函子 ω 的张量积[自同构](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E8%87%AA%E5%90%8C%E6%9E%84&zhida_source=entity)构成了一个仿射群 G , 且函子 ω 的选取决定了范畴的等价 T→RepQ(G) . 故一个中性 Tannakian 范畴就是一个没有指定遗忘函子的仿射群的表示范畴的抽象形式 , 这类似于向量空间是 kn 上没有指定基的抽象形式 .

而 Q 上的一个 Tannakian 范畴 T 但未必是中性范畴却是指一个附带张量积和对偶 , 并存在到某些特征零的域但不一定是 Q 上的向量空间范畴且保持张量积的忠实正合函子的 Abel 范畴 , 同时我们要求满足 End(1)=Q , 其中对所有的 X∈T , 1 是满足 1⊗X≅X≅X⊗1 的对象 , 那么这样的函子的选取给出了从 T 到仿射群胚范畴的一个范畴等价 .

(v) Mnum(k) 是 Tannakian 范畴么？

答案是否定的 , Mnum(k) 不是 Tannakian 范畴 . 在一个附带张量积和对偶的 Abel 范畴 T 中可以定义一个对象的自同态的迹且被任意忠实正合函子 ω:T→VecQ 所保持 , 故对于对象 M 的[恒同映射](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E6%81%92%E5%90%8C%E6%98%A0%E5%B0%84&zhida_source=entity) u 有

Tr(u|M)=Tr(ω(u)|ω(M))=dimQ⁡ω(M)

这就是向量空间的维数 , 故 Tr(u|M) 一定是非负整数 . 于是对于簇 X 的恒同映射 u , Tr(u|hX) 是 X 的 Euler-Poincaré 特征也就是 Betti 数的交错和 . 如果 X 是亏格为 g 的曲线 , 那么我们可以得到

Tr(u|hX)=dim⁡H0−dim⁡H1+dim⁡H2=2−2g

而 Tr(u|hX) 可以是负整数 , 这说明不存在忠实正合张量函子 ω:Mnum(k)→VecQ .

为了修正它 , 我们不得不改变张量积的结构的内在机制 . 不妨假设猜想2成立 , 则每个 Motive 范畴均存在分解 hX=h0X⊕h1X⊕⋯⊕h2dim⁡XX . 如果当 i,j 为奇数时 , 那么需要改变典范同构 hiX⊗hjX≅hjX⊗hiX 的负号 , 此时 Tr(u|hX) 就变成 X 的 Betti 数的和而不是交错和 , 于是 Mnum(k) 就成为 Tannakian 范畴 , 即如果域 k 的特征为零 , 那么 Mnum(k) 为中性 Tannakian 范畴 , 其它情形则是非中性 Tannakian 范畴 . 因此当 k 是有限域的[代数扩张](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E4%BB%A3%E6%95%B0%E6%89%A9%E5%BC%A0&zhida_source=entity)时 , Mnum(k) 为非中性 Tannakian 范畴 , 但由于猜想1还没有被完全证明 , 故我们并不清楚标准的上同调是否可以通过 Mnum(k) 进行分解 .

## **7.重温 Weil 猜想**

(i) Zeta-函数

设 X 是有限域 Fp 上的非异射影簇 , 接下来固定 Fp 的一个代数闭包 F , 对每一个 m , F 有唯一的 pm 元子域 Fpm , 令 X(Fpm) 为 X 上坐标在 Fpm 中的点的集合 , 事实上这是一个有限集 , 故 X 的 Zeta-函数 Z(X,t) 定义为

log⁡Z(X,t)=∑m≥1|X(Fpm)|tmm

如果 X=P0 为单点 , 那么对任意的 m 有 |X(Fpm)|=1 , 于是有

log⁡Z(X,t)=∑m≥1tmm=log⁡11−t

此时 Z(X,t)=11−t . 如果 X=P1 为直线 , 那么对任意的 m 有 |X(Fpm)|=1+pm , 于是有

log⁡Z(X,t)=∑m≥1(1+pm)tmm=log⁡1(1−t)(1−pt)

此时 Z(X,t)=1(1−t)(1−pt) .

(ii) Weil 的基础性工作

A.Weil 证明了对于有限域 Fp 上的亏格为 g 的曲线 , 有

Z(X,t)=P1(t)(1−t)(1−pt) , P1(t)∈Z[t]P1(t)=(1−a1t)(1−a2t)⋯(1−a2gt) , |ai|=p12

特别地 , 上面的结果表明 |X(Fp)|=1+p−∑i=12gai , 故得到

||X(Fp)|−1−p|=|∑i=12gai|≤2qp12

Weil 关于上面的这些结论的证明本质上利用了曲线的 [Jacobi](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=Jacobi&zhida_source=entity) 簇 , 对于 C 上亏格为 g 的曲线 X , X(C) 是亏格为 g 的 Riemann 曲面 , 故 X(C) 上的全纯微分构成了一个 g 维复向量空间 Ω1(X) , 且同调群 H1(X(C),Z) 是秩为 2g 的自由 Z-模 . 而 H1(X(C),Z) 中的一个元素 γ 定义了 Ω1(X) 的[对偶空间](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%AF%B9%E5%81%B6%E7%A9%BA%E9%97%B4&zhida_source=entity) Ω1(X)∨ 中的一个元素 ω↦∫γω , 事实上在这之前 Abel 和 Jacobi 等人的时期就已经知道了映射 ω↦∫γω 将 H1(X(C),Z) 映为 Ω1(X)∨ 中的一个格 Λ , 故商空间 J(X)=Ω1(X)∨/Λ 是一个复环面 , 即选择 Ω1(X) 的一个基就可以定义一个同构 J(X)≅Cg/Λ , 进而 J(X) 的自同态是 Ω1(X)∨ 将 Λ 映为自身的[线性自同态](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E7%BA%BF%E6%80%A7%E8%87%AA%E5%90%8C%E6%80%81&zhida_source=entity) , 由此可知 End(J(X)) 是有限生成 Z-模 . 因此 End(J(X))Q 是一个有限秩的 Q-代数 , 而 X 的任意极化(polarization)定义了 End(J(X))Q 的一个对合(involution)映射 α↦α† , 由于对任意非零的 α 迹 Tr(αα†)>0 ， 故 End(J(X))Q 为正定 .

复环面 J(X) 是一个代数簇 , 事实上 Weil 本人在研究这些问题时也不清楚该如何定义不同于 C 的域上的曲线的 Jacobi 簇 , 在当时的那个年代 , 代数几何的基础还不适合他的这些工作 , 于是他为了证明 Z(X,t)=P1(t)(1−t)(1−pt) 和 P1(t)=(1−a1t)(1−a2t)⋯(1−a2gt) 两个式子提供坚实的基础 , 其中 P1(t)∈Z[t] 和 |ai|=p12 , Weil 不得不重写[代数几何基础](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E4%BB%A3%E6%95%B0%E5%87%A0%E4%BD%95%E5%9F%BA%E7%A1%80&zhida_source=entity) , 然后就可以在任意的域上发展 Jacobi 簇的理论 .

而对于有限域 Fp 上的任意簇 X , 存在一个正则映射 π:X→X , 我们称之为 Frobenius 映射 , 这个映射在 X 上的点的作用为 (a0:a1:⋯:an)↦(a0p:a1p:⋯:anp) 且满足这样的性质即 πm 在 X(F) 上的作用的不动点恰好是 X(Fp) 中的元素 . Weil 证明了 Lefschetz 不动点公式 , 这就使得他证明了对于 Fp 上的曲线 X 有

Z(X,t)=P1(t)(1−t)(1−pt)

其中 p1(t) 等于 π 在 J(X) 上的作用的[特征多项式](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E7%89%B9%E5%BE%81%E5%A4%9A%E9%A1%B9%E5%BC%8F&zhida_source=entity)且该多项式具有整系数 . 而 X 的极化的选择定义了 End(J(X))Q 上的一个对合映射 , 同时也证明了 End(J(X))Q 是正定的 , 然后就推出了不等式 |ai|\<p^(1/2) .

(iii) Weil 猜想的陈述

Weil 关于曲线和其他的代数簇的结果发表了下面的猜想 , 即对于有限域 Fp 上的 n 维非异射影簇 X , 则得到

Z(X,t)=P1(t)P3(t)⋯P2n−1(t)(1−t)P2(t)P4(t)⋯P2n−2(t)(1−pt) , Pi(t)∈Z[t]Pi(t)=(1−ai1t)(1−ai2t)⋯(1−aibit) , |aij|=pi2 , j=1,2,⋯,bi

进而如果 X 是 Q 上的簇 X~ 的模 p 约化 , 那么 bi 作为 Pi(t) 的次数是复流形 X~(C) 的 Betti 数 .

(iv) [标准猜想](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E6%A0%87%E5%87%86%E7%8C%9C%E6%83%B3&zhida_source=entity)和 Weil 猜想

在 Grothendieck 定义平展上同调(étale cohomology)时 , 他和他的合作者们证明了一个不动点定理—— Lefschetz 不动点定理 , 这使得他们证明了

Z(X,t)=P1(t)P3(t)⋯P2n−1(t)(1−t)P2(t)P4(t)⋯P2n−2(t)(1−pt)

其中 Pi(t)=(1−ai1t)(1−ai2t)⋯(1−aibit) 为 Frobenius 映射 π 在 Heti(X,Ql) 上作用的特征多项式 , 此时还无法断定多项式 Pi 的系数在 Z 中但可以确定在 Ql 中 , 同时也无法排除是否会依赖于 l .

而 Grothendieck 提出了两个猜想 , 分别为 Lefschetz 标准猜想和 Hodge 标准猜想 , 如果这些猜想被证明 , 那么数学家们就可以通过簇的 Motive 理论代替曲线的 Jacobi 理论 , 并且将 Weil 关于曲线情形的 Weil 猜想的证明推广到任意维的代数簇的情形中去 . 事实上猜想2是 Lefschetz 标准猜想的弱形式 , 那么猜想2连同猜想1将意味着存在一个良好的 Motive 理论以及上面的

Z(X,t)=P1(t)P3(t)⋯P2n−1(t)(1−t)P2(t)P4(t)⋯P2n−2(t)(1−pt)

成立 , 同时 Pi(t)=(1−ai1t)(1−ai2t)⋯(1−aibit) 是Frobenius 映射 π 作用在 Motive 范畴 hiX 上的特征多项式 , 这里 Pi(t) 的系数在 Ql 中且不依赖于 l , 进而根据一番简单的讨论可知 Pi(t) 的系数在 Z 中 .

Hodge 标准猜想是一个正面的断言 , 它意味着每个 Motive 范畴的自同态代数具有一个正定的对合函子 , 我们不妨假设 Hodge 标准猜想是正确的 , 那么可以根据 Weil 的讨论方法证明 Pi(t)=(1−ai1t)(1−ai2t)⋯(1−aibit) 是成立的 . 对于特征零的情形 , Hodge 标准猜想可以用解析方法证明 , 而对于非零特征的情形 , 仅在少数的簇上成立 , 然而 Pi(t)=(1−ai1t)(1−ai2t)⋯(1−aibit) 也能用 Hodge 猜想和 Tate 猜想推出 . 而 Deligne 使用了非常巧妙的方法成功地证明了 Weil 猜想 , 他的证明不使用标准猜想 , 因此 Grothendieck 宣布 , 标准猜想的证明连同非特征零情形的奇点消解问题是代数几何中最紧迫的任务 , 至今依然保持正确 .

## **8. Motive 范畴的 Zeta-函数**

(i) Q 上的簇的 Zeta-函数

设 X 是 Q 上的非异射影簇 , 我们将定义 X 的多项式去分母后具有整系数 , 然后将这些方程模素数 p 就可以得到有限域 Fp 上的一个射影簇 Xp , 此时如果 Xp 仍为非异射影簇 , 那么称 p 是好的(good) , 事实上除有限个素数以外所有的素数都是好的 , 但还应该包含对应于坏的(bad)素数和实数的因子 , 在后面的讨论中我们会忽略这有限个坏的因子 , 于是我们可以定义 X 的 Zeta-函数为

ζ(X,s)=∏pZ(Xp,p−s)

当 X=P0 为单点时则有 ζ(X,s)=∏p11−p−s , 这就是 Riemann Zeta-函数 , 而当 X=P1 为直线时则有

ζ(X,s)=∏p1(1−p−s)(1−p1−s)=ζ(s)ζ(s−1)

考虑 Q 上的椭圆曲线 E , 对于好的 p , 我们有

ζ(Ep,t)=(1−apt)(1−a¯pt)(1−t)(1−pt)

其中 ap+a¯p∈Z 和 apa¯p=p , 以及 |ap|=p12 , 故得到

ζ(E,s)=ζ(s)ζ(s−1)L(E,s)

其中

L(E,s)=∏p1(1−app−s)(1−a¯pp−s)

(ii) Motive 范畴的 Zeta-函数

首先考虑有限域 Fp 上的 Motive 范畴 , 事实上我们无法用一个 Motive 范畴 M 的坐标或者域 Fpm 中的点来定义 Fp 上的 Motive 范畴 M 的 Zeta-函数 , 这是因为这根本没有定义 . 然后既然我们已经知道了 M(Fp) 是 Tannakian 范畴 , 而在任意 Tannakian 范畴中 , 对象的自同态具有特征多项式 , 如果 i 是奇数 , 那么就可以定义 Fp 上权为 i 的纯粹 Motive 范畴 M 的 Zeta-函数 Z(M,t) 为 M 的 Frobenius 映射的特征多项式 , 如果 i 是偶数 , 那么定义权为 i 的纯粹 Motive 范畴 M 的 Zeta-函数 Z(M,t) 为 M 的 Frobenius 映射的特征多项式的倒数 . 由于这个特征多项式的系数在 Q 中 , 如果 M 是有效 Motive 范畴 , 那么这个特征多项式的系数在 Z 中 , 故对于相同权的 Motive 范畴 M1 和 M2 就得到

Z(M1⊕M2,t)=Z(M1,t)⋅Z(M2,t)

根据上面的公式就可以将定义扩展到所有的 Motive 范畴 .

下面我们来讨论如何与簇的 Zeta-函数相联系 . 设 X 是 Fp 上的 n 维[光滑射影簇](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%85%89%E6%BB%91%E5%B0%84%E5%BD%B1%E7%B0%87&zhida_source=entity) , 而 Grothendieck 和他的合作者们证明了

Z(X,t)=P1(t)P3(t)⋯P2n−1(t)P0(t)P2(t)⋯P2n(t)

其中 Pi(t) 是簇 X 的 Frobenius 映射作用在平展上同调群 Heti(XF,Ql) 上的特征多项式 , 而 l 为任意不等于 p 的素数 , 因此 Pi(t) 可能依赖于 l . 现在我们假设对 l-adic 平展上同调猜想1成立 , 则存在函子 ω:M(Fp)→VecQl 使得 ω(hiX)=Heti(XF,Ql) , 且这个函子保持特征多项式 , 这意味着有 Z(hiX,t)=Pi(X,t)(−1)i+1 , 这里 Pi(X,t) 是系数属于 Z 的特征多项式且不依赖于 l , 进而不同于 Deligne 的工作 , 我们可以根据猜想2和猜想1推出

Z(X,t)=P1(t)P3(t)⋯P2n−1(t)(1−t)P2(t)P4(t)⋯P2n−2(t)(1−pt)

从而有

Z(X,t)=Z(h0X,t)Z(h1X,t)⋯Z(h2nX,t)

再根据下面的两个式子

hX=h0X⊕h1X⊕⋯⊕h2dim⁡XXZ(M1⊕M2,t)=Z(M1,t)⋅Z(M2,t)

可知有

Z(h0X,t)Z(h1X,t)⋯Z(h2nX,t)=Z(hX,t)

因此 Z(X,t)=Z(hX,t) .

而 Q 上的 Motive 范畴 M 可以由一个 Q 上的一个光滑射影簇 X , 一个 X×X 上的代数链 γ 以及一个整数 m 来刻画 , 除去有限多个坏的(bad)素数 p , 对所有好的(good)素数 p , 约化 X 和 γ 就可以给出 Fp 上的 Motive 范畴 Mp , 于是我们可以定义 ζ(M,s)=∏pZ(Mp,p−s) , 其中 ζ(h0(P1))=ζ(s) 和 ζ(h2(P1))=ζ(s−1) , 而对于椭圆曲线 E , 我们有 hE=h0E⊕h1E⊕h2E , 因此得到

ζ(hE,s)=ζ(h0E,s)⋅ζ(h1E,s)⋅ζ(h2E,s)=ζ(s)⋅L(E,s)−1⋅ζ(s−1)

值得注意的是 , 在没有假设任何未被证明的猜想的情形下 , 我们定义了 Q 上的 Motive 范畴且对这个范畴中的每个对象均赋予了一个 Zeta-函数 , 这个 Zeta-函数是一个关于复变量 s 的函数 , 数学家们猜想它会具有许多奇妙的性质 , 于是称这样的函数为 Motive 范畴的 L-函数 . 另一方面 , 我们甚至可以用完全不同点的方法 , 即从模形式 , 自守形式或者更为一般的自守表示来构造自守 L-函数 L(s) , 定义这样的函数不需要借助代数几何 .

下面的猜想来自于 Langlands 纲领 , 模性大猜想(Big Modularity Conjecture)是一个具有指导意义的基本原则 .

> 猜想3(模性大猜想):每个 Motive 的 L-函数都是自守 L-函数的交错积(alternating product) .  

设 E 是 Q 上的椭圆曲线 , 根据上面的模性猜想可知 , ζ(h1E,s) 是模形式的 Mellin 变换 , 而 Wiles 等人对这个猜想的证明正好是 Fermat 大定理的证明中的主要关键步骤 .

## **9. Birch-Swinnerton-Dyer 猜想和一些神秘的平方项**

设 E 是 Q 上的椭圆曲线 , 从1960年开始 , 三位数学家 Birch , Swinnerton 和 Dyer 就在研究自守 L-函数 L(E,s) 在 s=1 附近的情形并提出了著名的 Birch-Swinnerton-Dyer 猜想( BSD 猜想) . 令 L(E,1)∗ 是 L(E,s) 关于 s−1 的[幂级数](https://zhida.zhihu.com/search?content_id=239574824&content_type=Article&match_order=1&q=%E5%B9%82%E7%BA%A7%E6%95%B0&zhida_source=entity)展开式中的第一个非零系数 , 于是他们断言 已知项神秘项L(E,1)∗={已知项}⋅{神秘项} , 其中神秘项是 E 的 Tate-Shafarevich 群的阶数 , 如果这些神秘项是有限的 , 那么它们为平方数 .

与此同时 , Birch , Swinnerton 和 Dyer 还研究了

L3(E,s)=∏p1(1−ap3p−s)(1−a¯p3p−s)

在 s=2 附近的情形 , 通过计算它们也发现了 已知项神秘项L3(E,s)={已知项}⋅{神秘项} , 其中神秘性的平方项可以很大 , 甚至可以达到 2041 , 这究竟是什么呢？

根据上面的讨论可以知道 L(E,s)−1=ζ(h1E,s) , 于是我们将 Birch-Swinnerton-Dyer 猜想看作是关于 h1E 的断言 , 目前为止这一猜想已经扩展到了 Q 上的所有 Motive 范畴 , 且可以证明存在 Motive 范畴 M 使得

h1(E)⊗h1(E)⊗h1(E)=3h1(E,ΔE,−1)⊕M

以及 ζ(M,s)=L3(E,s)−1 , 因此这些神秘的平方项就是 Motive 范畴 M 的 Tate-Shafarevich 群 .

## **10. 总结**

严格地讲 M(k) 应该被称为纯粹 Motive 范畴 , 它对应于域 k 上非异射影簇 . Grothendieck 还预言存在混合 Motive 范畴并对应于 k 上所有的簇构成的范畴 , 而这个范畴不再是半单范畴 , 但每个混合 Motive 范畴应该具有一个滤链 , 这个滤链的因子(quotient)均为纯粹 Motive 范畴 . 目前还无法给出混合 Motive 范畴的明确定义 , 甚至连猜想的定义也没有 , 但是一些数学家已经构造了一些三角化范畴来作为混合 Motive 范畴的导出范畴的候选 , 当然还需在这些三角化范畴的其中一个范畴上定义一个 t-结构使得其中心为混合 Motive 范畴自身 .

Grothendieck 自己并没有发表任何关于 Motive 的文章 , 但是在他未发表的手稿中以及他和 Serre 的信中却经常提到 Motive , 最早解释这一理论的是 Demazure 和 Kleiman的文章 , 有关于 Motive 的会议论文集则综述了到20世纪90年代为止关于 Motive 的所知结果和进展 , 特别是 Kleiman 的文章讨论了Grothendieck 的标准猜想 , 而 Scholl 的文章则论述了 Motive 范畴的构造 , James S.Milne 的第一篇文章解释了标准猜想对 Weil 猜想的应用 , 目前André 的书是目前关于 Motive 理论的最好的一般性导引 , 这包括了混合 Motive 的最新进展 , 但还有一本由 Murre , Nagel 和 Peters 所著的书对 Murre 的各种关于 Motive 的系列讲座进行了深入的扩展 .

**后记：**全文的最后我们给出 James S.Milne 的原文《Motives——Grothendieck's Dream》, 需要阅读原文的可以直接扫码下载 .


