# Why Time Complexity?

Time complexity is the number of operations performed by an algorithm. 
It is a measure of how the running time of an algorithm grows as the input size increases.

# Growth Notation

We don’t care about actual milliseconds because:

Different machines run code differently.
We only care about how fast time grows as input grows.


That’s why we use asymptotic notations:

(a) Big-O (O) – Upper Bound

Worst-case performance.
> Example: It won’t be slower than this.
If algo takes at most n^2 steps, we write O(n^2).

```
// Example: Linear Search
public int linearSearch(int[] arr, int target) {
    for (int i = 0; i < arr.length; i++) {
        if (arr[i] == target) return i; // Found
    }
    return -1; // Not Found
}
```

In worst case (target not found), we check all n elements → O(n).


(b) Big-Omega (Ω) – Lower Bound

Best-case performance.
> Example: It will take at least this much time.
For the same linear search:

Best case = target at index 0 → only 1 check → Ω(1).


(c) Big-Theta (Θ) – Tight Bound

When best case and worst case grow at the same rate.
> Example: Exact growth rate.
```
// Example: Print all array elements
public void printAll(int[] arr) {
    for (int i = 0; i < arr.length; i++) {
        System.out.println(arr[i]);
    }
}
```

Always does n operations.
Best case = worst case = n → Θ(n).