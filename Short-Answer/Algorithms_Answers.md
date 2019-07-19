Add your answers to the Algorithms exercises here.

a) O(n)
    This is because you are iterating one time over a range of length(n^3), but you are incrementing by (n^2), which means there are n steps ((n^3)/(n^2)) to iterate through, which is linear

b) O(n^3)
    The innermost loop has 10 iterations regardless of the size of n, making it a constant that can be ignored. Each other loop is O(n), and because all three are nested, they are multiplied together

c)O(n)
    the function bunnyEars makes one recursive call each time it decrements n by one, meaning it performs one additional action for each increase in n, which is linear

Exercise II:
    I would implement an algorithm similar to a binary search. Because we know the floors are in order of height, (such that all floors at or above _f_ will break the egg, and all floors below _f_ will not), we essentially have a sorted list of floors.

    I would start by dropping an egg from the middle floor. If the egg breaks, we know we are at or above _f_, so I would repeat the test, now assuming the previous middle floor is the top floor, and calculating a new middle floor with the same bottom floor as the previous test.  Similarly, if the egg does not break, we are below _f_, and I would instead repeat the same test with the previous middle floor as the bottom floor, and the same top floor as the previous test. 

    This will be repeated until there is one floor left to test. If the egg breaks, that floor is _f_. If the egg does not break, we know that the next floor up must be _f_