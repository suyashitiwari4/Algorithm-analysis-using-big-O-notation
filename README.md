# Report on Algorithms Using Big-O Notation

# Introduction

In computer science, algorithms are compared based on their efficiency. Two major factors are considered: time complexity, which measures how the execution time of an algorithm grows with the input size, and space complexity, which measures how much memory an algorithm requires. To represent these complexities, we use mathematical notations, and the most widely used among them is Big-O notation.

# Big-O Notation

Big-O notation is used to describe the upper bound of an algorithm’s growth rate. It essentially tells us how an algorithm scales in the worst case as the input size increases. Formally, if the runtime of an algorithm is represented by a function f(n), then we say that f(n) is O(g(n)) if there exists a constant C such that f(n) is always less than or equal to C × g(n) for sufficiently large n. In simple terms, Big-O ignores constant factors and lower-order terms and focuses only on the dominant factor that grows the fastest as the input size increases.

# Common Time Complexities

There are several common growth rates that describe how different algorithms behave. An algorithm that takes constant time, denoted as O(1), runs in the same time regardless of input size, such as accessing an element in an array. A logarithmic time algorithm, O(log n), becomes faster as the input doubles, and a common example is binary search. Linear time, O(n), grows directly in proportion to the input size, and a simple linear search falls into this category. A linearithmic time algorithm, O(n log n), grows slightly faster than linear time and is typical of efficient sorting algorithms like merge sort or quick sort in average cases. Quadratic time, O(n²), appears when nested loops are used, as in bubble sort or insertion sort. Exponential time, O(2ⁿ), becomes impractical very quickly, such as solving the Towers of Hanoi or recursive brute-force approaches. The slowest is factorial time, O(n!), which occurs when an algorithm generates all permutations of a set.

# Examples of Algorithm Analysis

Consider the linear search algorithm. It scans each element of the array until it finds the target value. In the best case, if the first element matches, the algorithm finishes in constant time, O(1). In the worst case, if the element is at the last position or not present at all, every element must be checked, giving a time complexity of O(n).

Now take binary search as another example. This algorithm requires the array to be sorted. It repeatedly divides the search interval in half, checking the middle element at each step. If the target value equals the middle element, the search stops. Otherwise, it continues in either the left or right half. Since the search space reduces by half with each step, the time complexity is logarithmic, or O(log n).

Another case is bubble sort, a simple sorting algorithm. In bubble sort, each element is compared with its adjacent element, and they are swapped if they are in the wrong order. This process is repeated until the list is sorted. Due to its nested loops, bubble sort requires O(n²) time in the worst case. However, if the list is already sorted, it can finish in O(n) time because no swaps are needed.

# Big-O vs Other Notations

While Big-O is the most common notation, there are two others: Big-Omega (Ω) and Big-Theta (Θ). Big-Omega represents the best case or lower bound of an algorithm, while Big-Theta represents a tight bound, meaning the algorithm’s performance in the average case. For instance, in linear search, the best case occurs when the element is found at the beginning, which is Ω(1). The worst case is O(n), and the average case is Θ(n).

# Conclusion

Big-O notation provides a mathematical way to compare algorithms independent of hardware or programming language. By analyzing complexities, we can select efficient algorithms for large inputs, ensuring optimized performance.
