# Vector Subspaces

A **vector subspace** is a subset of a vector space that itself satisfies all the properties of a vector space. In other words, it is a smaller vector space contained within a larger one. Vector subspaces obey the first two properties of vector spaces (closure under addition and scalar multiplication).

## Examples

1. The **kernel** (null space) and **range** (column space) of a linear transformation are subspaces.
2. **Eigenspaces:** The set of eigenvectors associated with a specific eigenvalue of a linear transformation forms a subspace.
3. Any line, plane, or hyperplane through the origin.
4. The set of all polynomials is a subspace of the space of all functions.

## Null Vector Space

The **null vector space** (also known as the zero vector space or trivial vector space) is the simplest possible vector space. It contains only one element: the zero vector (denoted as **0**).

- The null vector space serves as a base case for many theorems and proofs in linear algebra.
- It is a subspace of every vector space.

## Kernel and Injectivity

The kernel (or null space) of a linear transformation is a null vector space if and only if the transformation is **injective** (one-to-one).

To show that T is injective, we need to prove that if T(x₁, y₁) = T(x₂, y₂), then (x₁, y₁) = (x₂, y₂).

For example, the following linear transformation is injective:

T(x, y) = (x, y, x + y)
