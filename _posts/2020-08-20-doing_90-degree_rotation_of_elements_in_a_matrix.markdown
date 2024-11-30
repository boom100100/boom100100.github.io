---
layout: post
title:      "Doing 90-Degree Rotation of Elements in a Matrix"
permalink:  doing_90-degree_rotation_of_elements_in_a_matrix
---



## Problem:

Rotate a matrix in shape of X.length, Y.length where X is elements in the outer level and Y is elements in each inner level.
Assume X.length == Y.length.
Also assume X must be an odd number.

## Input-outputs:

Case 1: x = y = 3
[[1, 2, 3], [4, 5, 6], [7, 8, 9]] => [[7, 4, 1], [8, 5, 2], [9, 6, 3]]

Case 2: x = y = 5
[[1, 2, 3, 4, 5], [6, 7, 8, 9, 10], [11, 12, 13, 14, 15], [16, 17, 18, 19, 20], [21, 22, 23, 24, 25]] => [[21, 16, 11, 6, 1], [22, 17, 12, 7, 2], [23, 18, 13, 8, 3], [24, 19, 14, 9, 4], [25, 20, 15, 10, 5]]

## Solution:

Starting with plotting the points of the first and second position allows two patterns to emerge. The movement of each nested element in case 1 is as follows:

(0, 0) => (0, 2)
(0, 1) => (1, 2)
(0, 2) => (2, 2)

(1, 0) => (0, 1)
(1, 1) => (1, 1)
(1, 2) => (2, 1)

(2, 0) => (0, 0)
(2, 1) => (1, 0)
(2, 2) => (2, 0)

Finding the solution requires determining what changed from one point to the next. We should focus on each coordinate individually, instead of both at once.

We'll start with X. From (0, 0) to (0, 2), it's clear that new_x == old_x. But the next coordinate pair disrupts that pattern, so this is not the rate of change. However, it is also true here that new_x == old_y. The same is true going down the entire line of coordinates. So to figure out new_x, our code will need access to old_y.

Thus far, we must code (old_y, new_y), also written as (new_x, new_y). Now, let's figure out new_y.

In (old_x, old_y), we see that old_x is constant from one row to the next, whereas y varies. Similarly, in (new_x, new_y), new_y is constant, and x varies. The 90-degree rotation caused this to happen. Since an element must be placed within a space that already exists, potential y-coordinates are limited to a range of 0 to (matrix.length - 1). Finally, since new_x has a relationship with old_y, we can assume that new_y has a relationship with old_x, even though they clearly aren't consistently equal to each other.

Putting these facts together,  let's make a relationship that matches the expected value for new_y: (matrix.length - 1) - old_x = new_y. Tested on all coordinates, this demonstrates that new_y is, in fact, related to old_x.

So, the new coordinate pattern is (old_y, ((matrix.length - 1) - old_x))

While this solution reflects a clockwise rotation, these same steps can help calculate a counterclockwise rotation.

## How to Implement:

Coding this solution changes the value of all nested elements in the matrix, so the first step is to create a deep clone of the matrix. Next, iterate through each element in the clone, and change it to match (new_x, new_y) as described above. Then, return the edited matrix.

## Use case:

Rotating values by 90 degrees is useful when working with images, videos, iFrames, and other things that take the shape of a square. Any square block element can make this transformation, and even whole screens can do this change.
