# Examples: Time Complexity Analysis

1.  ```java
    for (int i = 0; i < n; i++) {
        print(i);
    }
    ```
    Time Complexity: Since we have to print all `n` elements, it's \( O(n) \).

2.  ```java
    for (int i = 0; i < n; i+=2){
        print(i);
    }
    ```
    Time Complexity: This loop will execute for \( n/2 \) iterations, so it's \( O(n/2) \) or \( O(n) \).

3.  ```java
    for (int i = 0; i < n; i++){
        for (int j = 0; j < n; j++){
            print("hello");
        }
    }
    ```
    Time Complexity: This loop will execute \( n^2 \) iterations, so it's \( O(n^2) \).

4.  ```java
    for (int i = 0; i < n; i++){
        for (int j = i; j < n; j++){
            print("hello");
        }
    }
    ```
    **Iterations:**
    *   For \( i = 0 \), `j` goes from \( 0 \) to \( n-1 \) (n iterations)
    *   For \( i = 1 \), `j` goes from \( 1 \) to \( n-1 \) (n-1 iterations)
    *   For \( i = 2 \), `j` goes from \( 2 \) to \( n-1 \) (n-2 iterations)
    *   ...
    *   For \( i = n-1 \), `j` goes from \( n-1 \) to \( n-1 \) (1 iteration)

    Therefore, no. of iterations = \( n + (n-1) + (n-2) + \dots + 1 = \frac{n(n+1)}{2} \).

    So, it's \( O(n^2) \).

5.  ```java
    p = 0;
    for (int i = 1; p <= n; i++){
        p = p + i;
    }
    ```
    Here, `p` accumulates values like \( 1, 1+2, 1+2+3, \dots, 1+2+\dots+k \).
    We are looking for `k` such that \( p \approx n \).
    The sum \( 1 + 2 + \dots + k = \frac{k(k+1)}{2} \).
    So, we have \( \frac{k(k+1)}{2} \approx n \), which means \( k^2 \approx 2n \).
    Therefore, \( k \approx \sqrt{2n} \).

    Time Complexity: \( O(\sqrt{n}) \).

6.  ```java
    for (int i = 1; i < n; i=i*2){ // Assuming i starts at 1, otherwise i*2 starts at 0 and stays 0
        print(i);
    }
    ```
    Time Complexity: Since `i` is multiplied by 2 in each step, it's \( O(\log_2(n)) \).

7.  ```java
    for (int i = n; i >= 1; i=i/2){
        print(i);
    }
    ```
    In 1st iteration \( i = n \),
    In 2nd iteration \( i = n/2 \),
    In 3rd iteration \( i = n/4 \),
    In 4th iteration \( i = n/8 \),
    ...
    The loop continues as long as \( n/2^k \ge 1 \).
    This implies \( n \ge 2^k \), or \( k \le \log_2(n) \).

    Time Complexity: \( O(\log_2(n)) \).

8.  ```java
    for (int i = 0; i*i < n; i++){
        print(i);
    }
    ```
    The loop continues as long as \( i^2 < n \), which means \( i < \sqrt{n} \).
    So, `i` will go from \( 0 \) up to \( \lfloor \sqrt{n} - \epsilon \rfloor \).

    Time Complexity: \( O(\sqrt{n}) \).

9.  ```java
    for (int i = 0; i < n; i++){
        for (int j = 1; j < n; j = j*2){ // Assuming j starts at 1, otherwise j*2 starts at 0 and stays 0
            print("hello");
        }
    }
    ```
    The outer loop runs `n` times.
    The inner loop runs \( \log_2(n) \) times (similar to example 6).

    Time complexity: \( O(n \log n) \).