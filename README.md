# Leetcode 894. All Possible Full Binary Trees (Medium)

# Problem 

Given an integer n, return a list of all possible full binary trees with n nodes. Each node of each tree in the answer must have Node.val == 0.

Each element of the answer is the root node of one possible tree. You may return the final list of trees in any order.

A full binary tree is a binary tree where each node has exactly 0 or 2 children.

# Solution O(N^2)

If n is odd, return an empty list, because all full binary trees have an odd number of elements, if n is 1 return a node with no children, if n is 3 return a node with 2 children as leaf nodes. If n is larger than 3, then iterate through all possible sizes of the left child tree and the right child tree, they will add up to 1 less than n and both will be odd. From there append all combinations of left trees and rights trees together that have related sizes and return a list of all trees possible. This function is cached, so each size of n will only need to be computed once.
