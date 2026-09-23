# Paint House

**LeetCode Problem:** 256
**Language:** Python

## Problem

There are several houses that need to be painted using three different colors.

Each house has a different painting cost for each color.

The rule is that two neighboring houses cannot have the same color.

The goal is to find the minimum total cost required to paint all the houses.

For example:

```text
Input:
[[17,2,17],
 [16,16,5],
 [14,3,19]]

Output:
10
```

The minimum cost is achieved by choosing different colors for neighboring houses.

## Approach

This problem can be solved using Dynamic Programming.

For each house, we calculate the minimum cost of painting it with each of the three colors.

When choosing a color for the current house, the previous house must have one of the other two colors.

For example, if the current house is painted with color `0`, we add its cost to the minimum cost of painting the previous house with color `1` or color `2`.

The same process is applied to the other two colors.

After processing all houses, the minimum value among the three choices for the last house is the answer.

## Example

For:

```text
[[17,2,17],
 [16,16,5],
 [14,3,19]]
```

The minimum valid combination has a total cost of:

```text
10
```

## Complexity

* Time: O(n)
* Space: O(1) extra space

The input array is updated directly, so no additional DP table is required.

## Key Learning

This problem helped me practice:

* Dynamic Programming
* Minimum cost problems
* State transitions
* Choosing between multiple previous states
* Optimizing space usage

## Conclusion

By keeping the minimum cost for each color as we move through the houses, we can solve the problem efficiently without creating a separate DP array.

**Author: T. Nandhini**
