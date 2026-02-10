# Metrics

A **metric** is a function that defines a distance between two vectors. It is a way to quantify how similar or dissimilar two vectors are.

## Properties of a Metric

1. **Non-negativity:** The distance between two vectors is always non-negative.
2. **Identity of Indiscernibles:** The distance between two vectors is zero if and only if the vectors are identical.
3. **Symmetry:** The distance between vector A and vector B is the same as the distance between vector B and vector A.
4. **Triangle Inequality:** The distance between vector A and vector C is less than or equal to the sum of the distances between A and B, and B and C.

## Examples

1. **Manhattan Distance:** d(p, q) = |p₁ - q₁| + |p₂ - q₂| + ... + |pₙ - qₙ|
2. **Hamming Distance:** d(p, q) = number of positions where pᵢ ≠ qᵢ
3. **Chebyshev Distance:** d(p, q) = max(|p₁ - q₁|, |p₂ - q₂|, ..., |pₙ - qₙ|)
4. **Euclidean Distance**
5. **Cosine Similarity**
