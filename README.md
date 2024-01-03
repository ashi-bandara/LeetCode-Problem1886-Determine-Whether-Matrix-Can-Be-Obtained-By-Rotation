
# LeetCode Challenge D20
## Achievements
[![image.png](https://i.postimg.cc/J4VTgVfn/image.png)](https://postimg.cc/23GFbJ8R)

This solution outperformed 100% of Java users on LeetCode according to runtime metrics.


## Overview

Welcome to my LeetCode solution repository! This project addresses the coding challenge presented by [1886.  Determine Whether Matrix Can Be Obtained By Rotation](https://leetcode.com/problems/determine-whether-matrix-can-be-obtained-by-rotation/). Below, you'll find details about the problem, my approach to solving it, and the implemented solution.

## Problem Statement
Given two `n x n` binary matrices `mat` and `target`, return `true` _if it is possible to make_ `mat` _equal to_ `target` _by  **rotating**_ `mat` _in  **90-degree increments**, or_ `false` _otherwise._

**Example**

![](https://assets.leetcode.com/uploads/2021/05/20/grid3.png)

>**Input:** mat = [[0,1],[1,0]], target = [[1,0],[0,1]]
>
>**Output:** true
>
>**Explanation:** We can rotate mat 90 degrees clockwise to make mat equal target.

**Language Used**
> Java

**Difficulty**
> Easy

## Solution Overview
My solution to this question was pretty much a brute force attempt. Basically, using a loop, the code rotates the matrix until the input matrix equals the target matrix. I initially attempted to use the deepEquals method to check if the matrices were equal to each other, but it seemed to have affected the runtime, therefore I decided to have another method `areArraysEqual` to check element by element if the matrices are identical.

In the `rotateBy90` method, first the input 2D array was transposed, i.e. rows and columns were interchanged excluding the diagonal and then to complete the clockwise rotation by 90 degrees, the rows were reversed. About the decision to clone the matrix instead of altering it directly was picked up when I was searching on the formula to rotate a 2D array, which actually increases the readability and helps the code maintain the accuracy. 
