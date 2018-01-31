We could use a cute, recursive function to solve the problem. But that would cost O(2^n)
time as opposed to n time in bottom-up solutions. Massive difference!

In general, whenever you have a recursive solution to a problem, think about what's actually happening on the call stack.
An iterative solution might be more efficient.
