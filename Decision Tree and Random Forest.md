### What is Decision Tree? ### . 
Decision tree is a type of supervised learning algorithm (having both input and output variable  
and a mapping function from input to the output). It is a tree like structure, each time the tree  
node (stands for a group of data sets) is split into two or more homogeneous set basing on splitting   
rule.   
#### How to choose the attribute/value to split on at each level of the tree? #### . 
![Imgur1](https://i.imgur.com/fuIkOnL.png) . 
What is better split? Better split will give lower classification error.  
**Idea:** Calculate classification error of this decision stump.  
![Imgur2](https://i.imgur.com/0Q7pDJk.png=100*20) . 
![Imgur3](https://i.imgur.com/dq4COfl.png=100*20) . 
So splitting on credit gives better result, then Credit will be first selection.  
**Feature split selection algorithm** . 
1. Given a subset of data M (a node in a tree) . 
2. For each feature hi(x):  
  1). Split data of M according to feature hi(x)
  2). Compute classification error split
3. Choose feature h*(x) with lowest classification error .   
The algorithm selection is also based on type of target variables, there is detailed explanation in the [link](https://clearpredictions.com/Home/DecisionTree).  
**When to stop splitting? When should a node be declared a leaf?** . 
1. All data in the same nodes have same class value (No classification error).  
2. All data in the same nodes have the same attribute value (x1,...,xm), return  
a leaf node that predicts the majority of the class values as output
**If the tree is too large, how can it be pruned?**  
There are pre-pruning (stops growing the tree earlier, before it perfectly classifies the training set)   
and post-pruning (allows the tree to perfectly classify the training set, and then post prune the tree)  
The most common approach to determine the correct final size is:   
Use a distinct dataset from the training set (called validation set), to evaluate the effect of post-pruning  
nodes from the tree.  
If someone interested in the implementation from scratch in python, can check the article  
[How To Implement The Decision Tree Algorithm From Scratch In Python](https://machinelearningmastery.com/implement-decision-tree-algorithm-scratch-python/)  



