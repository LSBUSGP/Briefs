# Shuffle

A puzzle game requires a script to semi-randomly shuffle its game pieces. Each shuffle should mix the components given and be as unpredictable as possible, but should also avoid repetition of the same piece in subsequent shuffles. For example, the first 4 components of a new shuffle shouldn't contain the last 4 components of the previous one. The number of components in the list and the limit on repeating values must be customisable through the `Inspector`.

You will be provided with a list of integers representing the individual components. You must return a new shuffle each time the `Shuffle` function is called. You must additionally provide a program to test the shuffle function to ensure that it meets the repetition requirements. This test must also include a demonstration test case to show that it can catch errors.

![Image of a puzzle game with different puzzle pieces](https://www.focuseducational.com/images/user/fullsize/shapes.jpg "puzzle pieces")

You must include the following in your Unity package:

1. a script containing the shuffle function
2. a test script and scene that stress-tests the function
3. a scene that demonstrates the test program can catch errors in sequences
4. documentation
