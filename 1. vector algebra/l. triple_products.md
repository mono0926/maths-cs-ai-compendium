# Triple Products

There are two types of triple products in vector calculus: the **scalar triple product** and the **vector triple product**.

## Scalar Triple Product

The scalar triple product can be calculated using the determinant of a 3x3 matrix formed by the three vectors:

```
a · (b × c) = | a₁  a₂  a₃ |
              | b₁  b₂  b₃ |
              | c₁  c₂  c₃ |
```

## Vector Triple Product

The vector triple product can be expanded using the following identity:

a × (b × c) = (a · c)b - (a · b)c

## Properties

1. **Cyclic permutation:** a · (b × c) = b · (c × a) = c · (a × b)
2. **Non-associativity:** a × (b × c) ≠ (a × b) × c
3. The absolute value of the scalar triple product gives the **volume of the parallelepiped** formed by the three vectors as edges.
4. If the scalar triple product is zero, the vectors are **coplanar** (lie in the same plane).
5. The vector triple product results in a vector that lies in the **plane spanned by b and c**.
