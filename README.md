# GCD of Two Numbers Using Recursion

## Problem Statement

Given two integers `a` and `b`, find their Greatest Common Divisor (GCD) using recursion.

The GCD of two numbers is the largest positive integer that divides both numbers without leaving a remainder.

## Example

Input:
```text
12 18
```

Output:
```text
Gcd : 6
```

## Approach

1. If `a` is 0, return `b`.
2. If `b` is 0, return `a`.
3. Otherwise, recursively call `gcd(b, a % b)`.
4. Continue until one of the numbers becomes 0.

## Java Solution

```java
import java.util.*;

class Main {
    static int gcd(int a, int b) {
        if (a == 0) {
            return b;
        }

        if (b == 0) {
            return a;
        }

        return gcd(b, a % b);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        System.out.println("Gcd : " + gcd(a, b));
    }
}
```

## Recursion Trace

For:

```text
a = 12, b = 18
```

```text
gcd(12, 18)
→ gcd(18, 12)

gcd(18, 12)
→ gcd(12, 6)

gcd(12, 6)
→ gcd(6, 0)

gcd(6, 0)
→ 6
```

Final Answer:

```text
Gcd : 6
```

## Complexity Analysis

- Time Complexity: O(log(min(a, b)))
- Space Complexity: O(log(min(a, b))) due to recursion stack

## Tags

`Recursion` `Math` `Euclidean Algorithm` `Number Theory`
