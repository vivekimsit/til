> Testing should begin with the assumption that the program does hold errors - which,
in fact, is rather likely - and that we need to find them.
Testing is executing the program with the goal of finding as many errors as possible.

[Topcoder Article](https://www.topcoder.com/tc?module=Static&d1=features&d2=080706)

Some tips from other sources:

* Look at all / operators and check that the divisor is never 0

* Look at all * operators and check that the product fits in your data structure, eg. int

* Look at the size of your arrays and check that they never go out of bounds

* Look at all < operators and check that they shouldn't be <=
