
---

> 大全。

# Solving Technique

[Jump to navigation](https://www.sudopedia.org/wiki/Solving_Technique#column-one)[Jump to search](https://www.sudopedia.org/wiki/Solving_Technique#searchInput)

These are the methods used to [solve a Sudoku](https://sudokusolver.net/). There are many different solving techniques discovered in the last few years, mainly because there is a large community of puzzlers who share their knowledge on the various [Sudoku Forums](https://www.sudopedia.org/wiki/Sudoku_Forums "Sudoku Forums"). For crossword answers and solvers we would recommend [xWord.com](https://xword.com/)

Because there are so many, a rough subclassification has been made:

## Contents

- [1Singles](https://www.sudopedia.org/wiki/Solving_Technique#Singles)
- [2Intersections](https://www.sudopedia.org/wiki/Solving_Technique#Intersections)
- [3Subsets](https://www.sudopedia.org/wiki/Solving_Technique#Subsets)
- [4Fish](https://www.sudopedia.org/wiki/Solving_Technique#Fish)
- [5Single Digit Patterns](https://www.sudopedia.org/wiki/Solving_Technique#Single_Digit_Patterns)
- [6Coloring](https://www.sudopedia.org/wiki/Solving_Technique#Coloring)
- [7Uniqueness](https://www.sudopedia.org/wiki/Solving_Technique#Uniqueness)
- [8Chains and Loops](https://www.sudopedia.org/wiki/Solving_Technique#Chains_and_Loops)
- [9Wings](https://www.sudopedia.org/wiki/Solving_Technique#Wings)
- [10Almost Locked Sets](https://www.sudopedia.org/wiki/Solving_Technique#Almost_Locked_Sets)
- [11Enumeration on Selected Cells](https://www.sudopedia.org/wiki/Solving_Technique#Enumeration_on_Selected_Cells)
- [12Miscellaneous](https://www.sudopedia.org/wiki/Solving_Technique#Miscellaneous)
- [13Techniques of Last Resort](https://www.sudopedia.org/wiki/Solving_Technique#Techniques_of_Last_Resort)
- [14Brute Force](https://www.sudopedia.org/wiki/Solving_Technique#Brute_Force)

## [Singles](https://www.sudopedia.org/wiki/Single "Single")

[Full House](https://www.sudopedia.org/wiki/Full_House "Full House")

A [house](https://www.sudopedia.org/wiki/House "House") with a single empty [cell](https://www.sudopedia.org/wiki/Cell "Cell").

[Last Digit](https://www.sudopedia.org/wiki/Last_Digit "Last Digit")

The last instance of a [digit](https://www.sudopedia.org/wiki/Digit "Digit").

[Hidden Single](https://www.sudopedia.org/wiki/Hidden_Single "Hidden Single") | [Pinned Digit](https://www.sudopedia.org/wiki/Pinned_Digit "Pinned Digit")

A single candidate remaining for a digit in a house.

[Naked Single](https://www.sudopedia.org/wiki/Naked_Single "Naked Single") | [Forced Digit](https://www.sudopedia.org/wiki/Forced_Digit "Forced Digit") | [Sole Candidate](https://www.sudopedia.org/wiki/Sole_Candidate "Sole Candidate")

A single candidate remaining in a cell.

## [Intersections](https://www.sudopedia.org/wiki/Intersection "Intersection")

[Locked Candidates](https://www.sudopedia.org/wiki/Locked_Candidates "Locked Candidates") | Intersection Removal | Line-Box Interaction | Pointing (Pair, Triple) | Claiming

[Candidates](https://www.sudopedia.org/wiki/Candidate "Candidate") are locked in the [intersection](https://www.sudopedia.org/wiki/Intersection "Intersection") of a [line](https://www.sudopedia.org/wiki/Line "Line") and a [box](https://www.sudopedia.org/wiki/Box "Box").

[Locked Pair](https://www.sudopedia.org/wiki/Locked_Pair "Locked Pair")

A [Naked Pair](https://www.sudopedia.org/wiki/Naked_Pair "Naked Pair") located in a single intersection.

[Locked Triple](https://www.sudopedia.org/index.php?title=Locked_Triple&action=edit&redlink=1 "Locked Triple (page does not exist)")

A [Naked Triple](https://www.sudopedia.org/wiki/Naked_Triple "Naked Triple") located in a single intersection.

[Almost Locked Candidates](https://www.sudopedia.org/index.php?title=Almost_Locked_Candidates&action=edit&redlink=1 "Almost Locked Candidates (page does not exist)")

A box-line intersection where the line or the box contains an [Almost Locked Set](https://www.sudopedia.org/wiki/Almost_Locked_Set "Almost Locked Set"), and the remaining cells in the line or box outside the intersection does not contain digits from the Almost Locked Set.

## [Subsets](https://www.sudopedia.org/wiki/Subset "Subset")

[Naked Subset](https://www.sudopedia.org/wiki/Naked_Subset "Naked Subset")

**N** cells with candidates for **N** digits.

[Naked Pair](https://www.sudopedia.org/wiki/Naked_Pair "Naked Pair")

**2** cells with candidates for **2** digits.

[Naked Triple](https://www.sudopedia.org/wiki/Naked_Triple "Naked Triple")

**3** cells with candidates for **3** digits.

[Naked Quad](https://www.sudopedia.org/wiki/Naked_Quad "Naked Quad")

**4** cells with candidates for **4** digits.

[Hidden Subset](https://www.sudopedia.org/wiki/Hidden_Subset "Hidden Subset")

**N** digits with candidates in **N** cells.

[Hidden Pair](https://www.sudopedia.org/wiki/Hidden_Pair "Hidden Pair")

**2** digits with candidates in **2** cells.

[Hidden Triple](https://www.sudopedia.org/wiki/Hidden_Triple "Hidden Triple")

**3** digits with candidates in **3** cells.

[Hidden Quad](https://www.sudopedia.org/wiki/Hidden_Quad "Hidden Quad")

**4** digits with candidates in **4** cells.

## [Fish](https://www.sudopedia.org/wiki/Fish "Fish")

Basic Fish

Rows and columns only.

[X-Wing](https://www.sudopedia.org/wiki/X-Wing "X-Wing")

2 rows vs. 2 columns

[Swordfish](https://www.sudopedia.org/wiki/Swordfish "Swordfish")

3 rows vs. 3 columns

[Jellyfish](https://www.sudopedia.org/wiki/Jellyfish "Jellyfish")

4 rows vs. 4 columns

[Squirmbag](https://www.sudopedia.org/index.php?title=Squirmbag&action=edit&redlink=1 "Squirmbag (page does not exist)")

5 rows vs. 5 columns

[Finned Fish](https://www.sudopedia.org/wiki/Finned_Fish "Finned Fish")

Fish patterns with additional candidates in a single box.

[Sashimi Fish](https://www.sudopedia.org/wiki/Sashimi_Fish "Sashimi Fish")

Incomplete basic fish patterns with a [fin](https://www.sudopedia.org/wiki/Fin "Fin").

[Franken Fish](https://www.sudopedia.org/index.php?title=Franken_Fish&action=edit&redlink=1 "Franken Fish (page does not exist)")

Fish patterns that include box constraints.

[Mutant Fish](https://www.sudopedia.org/index.php?title=Mutant_Fish&action=edit&redlink=1 "Mutant Fish (page does not exist)")

Fish patterns with mixed sets of constraints.

[Kraken Fish](https://www.sudopedia.org/index.php?title=Kraken_Fish&action=edit&redlink=1 "Kraken Fish (page does not exist)")

A fish pattern with indirect connections to a candidate which can be eliminated.

## Single Digit Patterns

[Skyscraper](https://www.sudopedia.org/wiki/Skyscraper "Skyscraper")

Two parallel strong links, weakly connected at the base.

[2-String Kite](https://www.sudopedia.org/wiki/2-String_Kite "2-String Kite")

Two crossing strong links, weakly connected in a box.

[Empty Rectangle](https://www.sudopedia.org/wiki/Empty_Rectangle "Empty Rectangle")

A single-digit technique that makes use of a [box](https://www.sudopedia.org/wiki/Box "Box") whose [candidates](https://www.sudopedia.org/wiki/Candidates "Candidates") for that [digit](https://www.sudopedia.org/wiki/Digit "Digit") are contained within the union of a [boxrow](https://www.sudopedia.org/wiki/Boxrow "Boxrow") and a [boxcol](https://www.sudopedia.org/wiki/Boxcol "Boxcol").

## [Coloring](https://www.sudopedia.org/wiki/Coloring "Coloring")

[Simple Colors](https://www.sudopedia.org/wiki/Simple_Colors "Simple Colors")

Uses only 2 colors to form a single color [cluster](https://www.sudopedia.org/wiki/Cluster "Cluster").

[Multi-Colors](https://www.sudopedia.org/wiki/Multi-Colors "Multi-Colors") | [Supercoloring](https://www.sudopedia.org/index.php?title=Supercoloring&action=edit&redlink=1 "Supercoloring (page does not exist)")

Uses multiple colors (4, 6 or a higher multiple of 2) to form multiple color clusters.

[Weak Colors](https://www.sudopedia.org/wiki/Weak_Colors "Weak Colors")

Extends Simple-Colors by the use of [hinge](https://www.sudopedia.org/wiki/Hinge "Hinge") linkages.

[X-Colors](https://www.sudopedia.org/wiki/X-Colors "X-Colors")

Uses only 2 colors, but also takes the [implications](https://www.sudopedia.org/wiki/Implication "Implication") for each color into account.

[Color Trap](https://www.sudopedia.org/wiki/Color_Trap "Color Trap")

A technique that uses a single cluster to eliminate candidates outside the cluster.

[Color Wrap](https://www.sudopedia.org/wiki/Color_Wrap "Color Wrap")

A technique that uses a single cluster to detect a [contradiction](https://www.sudopedia.org/wiki/Contradiction "Contradiction") in one of the colors.

[Color Wing](https://www.sudopedia.org/wiki/Color_Wing "Color Wing")

A technique that uses multiple clusters to eliminate candidates outside these clusters. Same as Multi-Colors.

[3D Medusa](https://www.sudopedia.org/wiki/3D_Medusa "3D Medusa") Coloring | [Advanced Coloring](https://www.sudopedia.org/wiki/Advanced_Coloring "Advanced Coloring") | [Ultracoloring](https://www.sudopedia.org/wiki/Ultracoloring "Ultracoloring")

A set of techniques that uses colors on multiple digits.

## Uniqueness

[Uniqueness Test](https://www.sudopedia.org/wiki/Uniqueness_Test "Uniqueness Test")

A set of techniques that avoids the [Unique Rectangle](https://www.sudopedia.org/wiki/Unique_Rectangle "Unique Rectangle") [deadly pattern](https://www.sudopedia.org/wiki/Deadly_pattern "Deadly pattern").

[Avoidable Rectangle](https://www.sudopedia.org/index.php?title=Avoidable_Rectangle&action=edit&redlink=1 "Avoidable Rectangle (page does not exist)")

A set of techniques that avoids the [Unique Rectangle](https://www.sudopedia.org/wiki/Unique_Rectangle "Unique Rectangle") [deadly pattern](https://www.sudopedia.org/wiki/Deadly_pattern "Deadly pattern"). Perhaps unique in solving techniques in that it employs solved [cells](https://www.sudopedia.org/wiki/Cell "Cell") as well as those unsolved.

[Bivalue Universal Grave](https://www.sudopedia.org/wiki/Bivalue_Universal_Grave "Bivalue Universal Grave")

A set of techniques that avoids the [Bivalue Universal Grave](https://www.sudopedia.org/wiki/Bivalue_Universal_Grave "Bivalue Universal Grave") [deadly pattern](https://www.sudopedia.org/wiki/Deadly_pattern "Deadly pattern").

[BUG Lite](https://www.sudopedia.org/wiki/BUG_Lite "BUG Lite")

A set of techniques that avoids the [BUG Lite](https://www.sudopedia.org/wiki/BUG_Lite "BUG Lite") [deadly pattern](https://www.sudopedia.org/wiki/Deadly_pattern "Deadly pattern").

[Uniqueness Controversy](https://www.sudopedia.org/wiki/Uniqueness_Controversy "Uniqueness Controversy")

These solving techniques assume that the [Sudoku](https://www.sudopedia.org/wiki/Sudoku "Sudoku") puzzle has a unique solution. It is not universally accepted that this assumption is a valid one.

## [Chains](https://www.sudopedia.org/wiki/Chain "Chain") and [Loops](https://www.sudopedia.org/wiki/Loop "Loop")

[Forcing Chain](https://www.sudopedia.org/wiki/Forcing_Chain "Forcing Chain")

Generic term for any type of chain.

[X-Chain](https://www.sudopedia.org/wiki/X-Chain "X-Chain")

Single digit chain of cells.

[XY-Chain](https://www.sudopedia.org/wiki/XY-Chain "XY-Chain")

Chain of [bivalue](https://www.sudopedia.org/wiki/Bivalue "Bivalue") cells.

[Remote Pairs](https://www.sudopedia.org/index.php?title=Remote_Pairs&action=edit&redlink=1 "Remote Pairs (page does not exist)")

Simplified form of XY-Chain, involving only two digits.

[Fishy Cycle](https://www.sudopedia.org/wiki/Fishy_Cycle "Fishy Cycle") | X-Cycle

Single digit [continuous](https://www.sudopedia.org/wiki/Continuous "Continuous") loop.

[Broken Wing](https://www.sudopedia.org/wiki/Broken_Wing "Broken Wing")

Eliminations caused by loops of odd length.

[Nice Loops](https://www.sudopedia.org/wiki/Nice_Loop "Nice Loop")

Several types of loops formed by cells following strict rules and a notation system.

[Double Implication Chain](https://www.sudopedia.org/wiki/Double_Implication_Chain "Double Implication Chain") | DIC

There are 2 interpretations circulating. The first originates from a reliable source [[1]](http://www.sudoku.com/forums/viewtopic.php?t=2143).

- A Forcing Chain that has implications in both directions.
- 2 Forcing Chains starting from a bivalue cell or a [bilocal](https://www.sudopedia.org/wiki/Bilocal "Bilocal") unit showing a [verity](https://www.sudopedia.org/wiki/Verity "Verity").

[Alternating Inference Chain](https://www.sudopedia.org/wiki/Alternating_Inference_Chain "Alternating Inference Chain") | AIC

A chain where each node is a candidate, with alternating strong and weak inference.

[Oriented Chains](https://www.sudopedia.org/index.php?title=Oriented_Chains&action=edit&redlink=1 "Oriented Chains (page does not exist)")

Oriented chains are generalisations of the basic xy-chains. The central idea is that the information collected from previous candidates in a chain (and/or from the target) can be used to select the next candidates. Oriented chains are either 2D or 3D:

- oriented 2D chains: xyt-chains, xyz-chains and xyzt-chains, together with their "hidden" counterparts: hxyt-chains, hxyz-chains and hxyzt-chains;

- [oriented 3D chains](https://www.sudopedia.org/index.php?title=Oriented_3D_chains&action=edit&redlink=1 "Oriented 3D chains (page does not exist)"): nrct-chains, nrcz-chains, nrczt-chains.

(The original reference to all these chains is the book "The Hidden Logic of Sudoku". Further web references forthcoming)

## Wings

[XY-Wing](https://www.sudopedia.org/wiki/XY-Wing "XY-Wing")

Three [cells](https://www.sudopedia.org/wiki/Cell "Cell") with [pivot](https://www.sudopedia.org/wiki/Pivot "Pivot") cell **XY** and two [pincer](https://www.sudopedia.org/index.php?title=Pincer&action=edit&redlink=1 "Pincer (page does not exist)") cells **XZ** and **YZ**.

[XYZ-Wing](https://www.sudopedia.org/index.php?title=XYZ-Wing&action=edit&redlink=1 "XYZ-Wing (page does not exist)")

Three [cells](https://www.sudopedia.org/wiki/Cell "Cell") with [pivot](https://www.sudopedia.org/wiki/Pivot "Pivot") cell **XYZ** and two [pincer](https://www.sudopedia.org/index.php?title=Pincer&action=edit&redlink=1 "Pincer (page does not exist)") cells **XZ** and **YZ**.

[WXYZ-Wing](https://www.sudopedia.org/index.php?title=WXYZ-Wing&action=edit&redlink=1 "WXYZ-Wing (page does not exist)")

Four [cells](https://www.sudopedia.org/wiki/Cell "Cell") with [pivot](https://www.sudopedia.org/wiki/Pivot "Pivot") cell **WXYZ** and three [pincer](https://www.sudopedia.org/index.php?title=Pincer&action=edit&redlink=1 "Pincer (page does not exist)") cells **WZ**, **XZ** and **YZ**.

[W-Wing](https://www.sudopedia.org/wiki/W-Wing "W-Wing")

Four [cells](https://www.sudopedia.org/wiki/Cell "Cell") in a [chain](https://www.sudopedia.org/wiki/Chain "Chain"): a cell **WX**, a cell with **X** as a [candidate](https://www.sudopedia.org/wiki/Candidate "Candidate"), another cell with **X** as a [candidate](https://www.sudopedia.org/wiki/Candidate "Candidate"), another cell **WX**, such that the two cells containing **X** as a [candidate](https://www.sudopedia.org/wiki/Candidate "Candidate") have a [strong link](https://www.sudopedia.org/wiki/Strong_link "Strong link").

## [Almost Locked Sets](https://www.sudopedia.org/wiki/Almost_Locked_Set "Almost Locked Set")

[ALS-XZ](https://www.sudopedia.org/wiki/ALS-XZ "ALS-XZ") rule

2 Almost Locked Sets with [restricted common](https://www.sudopedia.org/wiki/Restricted_common "Restricted common") digit **X** perform eliminations for common digit **Z**.

[ALS-XY-Wing](https://www.sudopedia.org/wiki/ALS-XY-Wing "ALS-XY-Wing") rule

3 Almost Locked Sets with 2 restricted common digits **Y** and **Z** perform eliminations for common digit **X**.

[ALS-XY-Chain](https://www.sudopedia.org/wiki/ALS-XY-Chain "ALS-XY-Chain")

Very similar to [XY-Chain](https://www.sudopedia.org/wiki/XY-Chain "XY-Chain"), except that the [nodes](https://www.sudopedia.org/wiki/Node "Node") in the [chain](https://www.sudopedia.org/wiki/Chain "Chain") are Almost Locked Sets.

[Death Blossom](https://www.sudopedia.org/wiki/Death_Blossom "Death Blossom")

A stem cell of N candidates pointing to N petals, each an Almost Locked Set.

## Enumeration on Selected Cells

[Aligned Pair Exclusion](https://www.sudopedia.org/wiki/Aligned_Pair_Exclusion "Aligned Pair Exclusion")

Checks combinations of [digits](https://www.sudopedia.org/wiki/Digits "Digits") in a pair of [cells](https://www.sudopedia.org/wiki/Cells "Cells") located in an [intersection](https://www.sudopedia.org/wiki/Intersection "Intersection").

[Aligned Triple Exclusion](https://www.sudopedia.org/wiki/Aligned_Triple_Exclusion "Aligned Triple Exclusion")

Checks combinations of [digits](https://www.sudopedia.org/wiki/Digits "Digits") in a triple of [cells](https://www.sudopedia.org/wiki/Cells "Cells") located in an [intersection](https://www.sudopedia.org/wiki/Intersection "Intersection").

[Subset Exclusion](https://www.sudopedia.org/wiki/Subset_Exclusion "Subset Exclusion")

Extension of [Aligned Pair Exclusion](https://www.sudopedia.org/wiki/Aligned_Pair_Exclusion "Aligned Pair Exclusion") to arbitrary sets that need not be aligned.

## Miscellaneous

[Sue de Coq](https://www.sudopedia.org/index.php?title=Sue_de_Coq&action=edit&redlink=1 "Sue de Coq (page does not exist)")

Uses two intersecting sets **A** and **B**, where **A** is a set of N cells with N candidates in a line, **B** is a set of N cells with N candidates in a box, and the sets **A - B** and **B - A** have no common candidates.

[Subset Counting](https://www.sudopedia.org/index.php?title=Subset_Counting&action=edit&redlink=1 "Subset Counting (page does not exist)") | [Extended Subset Principle](https://www.sudopedia.org/index.php?title=Extended_Subset_Principle&action=edit&redlink=1 "Extended Subset Principle (page does not exist)")

Considers the number of times a digit can be placed in a selected subset of cells.

[Braid Analysis](https://www.sudopedia.org/wiki/Braid_Analysis "Braid Analysis") | [Braiding](https://www.sudopedia.org/wiki/Braiding "Braiding") | [Traveling Pairs](https://www.sudopedia.org/index.php?title=Traveling_Pairs&action=edit&redlink=1 "Traveling Pairs (page does not exist)")

Analyzes the distribution of digits in a [chute](https://www.sudopedia.org/wiki/Chute "Chute"), especially how pairs repeat in a chute.

[Constraint Subsets](https://www.sudopedia.org/index.php?title=Constraint_Subsets&action=edit&redlink=1 "Constraint Subsets (page does not exist)")

Generalized view of [subset](https://www.sudopedia.org/wiki/Subset "Subset") and [fish](https://www.sudopedia.org/wiki/Fish "Fish") techniques.

[Equivalence Marks](https://www.sudopedia.org/wiki/Equivalence_Marks "Equivalence Marks")

Similar to [coloring](https://www.sudopedia.org/wiki/Coloring "Coloring"), but uses marks instead of colors to represent parity.

[Gurth's Symmetrical Placement](https://www.sudopedia.org/index.php?title=Gurth%27s_Symmetrical_Placement&action=edit&redlink=1 "Gurth's Symmetrical Placement (page does not exist)")

Technique for puzzles with rotational symmetry.

## Techniques of Last Resort

Most of these techniques are controversial. They are either too complex to be used by human solvers, or they require a lot of extra work, or they are not based on logic.

[Forcing Net](https://www.sudopedia.org/wiki/Forcing_Net "Forcing Net")

A general term for techniques that investigate branching chains.

[Tabling](https://www.sudopedia.org/wiki/Tabling "Tabling") | Trebor's Tables

All implications for each move are collected in tables.

[Graded Equivalence Marks](https://www.sudopedia.org/wiki/Graded_Equivalence_Marks "Graded Equivalence Marks") | GEM

A system of marking candidates starting from 2 complementary starting positions.

[Bowman Bingo](https://www.sudopedia.org/wiki/Bowman_Bingo "Bowman Bingo")

A systematic approach to investigate implications.

[Trial & Error](https://www.sudopedia.org/index.php?title=Trial_%26_Error&action=edit&redlink=1 "Trial & Error (page does not exist)") | [Ariadne's Thread](https://www.sudopedia.org/wiki/Ariadne%27s_Thread "Ariadne's Thread") | [Bifurcation](https://www.sudopedia.org/wiki/Bifurcation "Bifurcation")

The implications for a single move are investigated.

[Nishio](https://www.sudopedia.org/wiki/Nishio "Nishio")

Trial & Error limited to single digit.

[Templating](https://www.sudopedia.org/wiki/Templating "Templating") | [Pattern Overlay Method](https://www.sudopedia.org/wiki/Pattern_Overlay_Method "Pattern Overlay Method") | POM

All possible ways to place a digit in the remaining candidate space are investigated.

[Guessing](https://www.sudopedia.org/wiki/Guess "Guess")

Random moves are made, without any logic behind them.

## Brute Force

These are primarily designed for computer solver programs.

- [Backtracking Algorithms](https://www.sudopedia.org/index.php?title=Backtracking_Algorithms&action=edit&redlink=1 "Backtracking Algorithms (page does not exist)").

If you are looking for the [New York Times Crossword Answers](https://nytsolver.com/). Daily Puzzle games have become quite popular especially after the global phenomenon Wordle. To see all [Daily Puzzle Answers](https://gameanswers.com/) visit the website linked on this page. You can now play the Internet's favorite game [Wordle online](https://dailypuzzles.com/games/wordle)

[Category](https://www.sudopedia.org/wiki/Special:Categories "Special:Categories"): 

- [Solving Techniques](https://www.sudopedia.org/wiki/Category:Solving_Techniques "Category:Solving Techniques")

---

