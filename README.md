# 60_wrapBinarySearch

Helper: Darius

count = log_2(n)

As the size of the problem increases to size n, the run time will increase to only log_2(n). This means that the calculation time grows much more slowly than the size of the problem may grow.

![Image of Graph](https://qph.fs.quoracdn.net/main-qimg-1741b1c66102be1ff533b29a5871240c)

# Recursive Binary Search
0. Given a sorted integer array of length n, find the index of a value in O(logn) time.
1. When I am asked to return the index of a value in an array of length n, the recursive abstraction can return the index of a value in an array of length n/2.
2.
  - Decision to choose the base case or the recursive cases
    * Is the low bound higher than the high bound?
  - Instructions for Solving the Base Cases
    * return -2
    * Determine the <i>middle page</i> to check and compare the given value to value at <i>middle page</i> - If the comparison is equal to 0, return <i>middle page</i>
  - Instructions for Solving the Recursive Cases
    * Determine the <i>middle page</i> to check and compare the given value to value at <i>middle page</i> (Leftover processing)
    * Conditional: (Combiner)
      * First case: the comparison is less than 0
        * return the binary search of the array from <i>start</i> to <i>middle page</i> - 1
      * Second case: the comparison is greater than 0
        * return the binary search of the array from <i>middle page</i> + 1 to <i>end</i>
