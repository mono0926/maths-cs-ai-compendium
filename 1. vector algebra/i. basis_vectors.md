# Basis Vectors

**Basis vectors** are the fundamental vectors in the Euclidean plane from which transformations start. They define the coordinate system.

A set of basis vectors is a set of **linearly independent** vectors that **span** a vector space. This means they have two key properties:

1. **Linear Independence:** No basis vector can be expressed as a linear combination of the others. Each contributes unique information with no redundancy.
2. **Spanning Property:** Every vector in the vector space can be expressed as a unique linear combination of the basis vectors.

## Key Facts

- A vector space can have multiple different bases, but all bases for a given vector space have the **same number of vectors**.
- The number of basis vectors determines the **dimension** of the vector space.
- The coefficients used in the linear combination to represent a vector with respect to a basis are called the **coordinates** of the vector.

## Standard Bases

**Standard Basis for R²:**
- **i** = (1, 0) — points in the positive x-direction
- **j** = (0, 1) — points in the positive y-direction
- Any vector in R² can be written as: (x, y) = x**i** + y**j**

**Standard Basis for R³:**
- **i** = (1, 0, 0)
- **j** = (0, 1, 0)
- **k** = (0, 0, 1)

While the standard basis is common, vector spaces can have other bases. For example, in R², the vectors (1, 1) and (-1, 1) also form a valid basis.

## Change of Basis

A **change of basis** involves expressing the same vector with respect to a different set of basis vectors. The transformation is represented by a **change of basis matrix**, which converts coordinates from one basis to another.

If you have two bases B (old) and B' (new), the change of basis matrix **P** from B to B' is formed by expressing each vector in B' as a linear combination of the vectors in B. The columns of P are the coordinates of the vectors in B' with respect to B.

Simply multiply the original vector by the change of basis matrix to get the vector in the new basis.

**The change of basis matrix is always invertible** — you can go back from new coordinates to old coordinates by multiplying by the inverse of P.

### Example

Change of basis matrix from B = {(1, 0), (0, 1)} to B' = {(1, 1), (-1, 1)}:

Solving:
- (1, 1) = 1·(1, 0) + 1·(0, 1)
- (-1, 1) = -1·(1, 0) + 1·(0, 1)

The change of basis matrix is:

```
P = | 1  -1 |
    | 1   1 |
```
