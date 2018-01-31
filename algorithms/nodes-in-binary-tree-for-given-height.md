![Binary Tree](https://www.interviewcake.com/images/svgs/fibonacci__binary_tree_recursive.svg?bust=163)

We can notice this is a binary tree ↴ whose height is n, which means the total number of nodes is O(2^n).

So our total runtime is O(2^n). That's an "exponential time cost," since the nn is in an exponent.
Exponential costs are terrible. This is way worse than O(n^2) or even O(n^{100}).

Our recurrence tree above essentially gets twice as big each time we add 1 to n.
So as nn gets really big, our runtime quickly spirals out of control.

The craziness of our time cost comes from the fact that we're doing so much repeat work.
How can we avoid doing this repeat work?

- For unit increase in height the size of tree gets doubled.

- Exponential algorithms are the worst one.
