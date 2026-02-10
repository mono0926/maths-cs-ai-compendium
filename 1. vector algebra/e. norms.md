# Norms

The **norm** of a vector quantifies its magnitude. Technically, it is the distance between a vector and the origin. This heavily uses the **absolute value** (modulus of a number), which is the distance from zero regardless of direction and is always non-negative.

## Properties of a Norm

1. **Non-negativity:** ‖v‖ ≥ 0 for all v ∈ V, and ‖v‖ = 0 if and only if v = **0** (the zero vector).
2. **Absolute Homogeneity:** ‖αv‖ = |α|‖v‖ for all v ∈ V and α ∈ F.
3. **Triangle Inequality:** ‖u + v‖ ≤ ‖u‖ + ‖v‖ for all u, v ∈ V.

## Examples

1. **Euclidean Norm (L2):** ‖v‖₂ = √(v₁² + v₂² + ... + vₙ²)
2. **Taxicab / Manhattan Norm (L1):** ‖v‖₁ = |v₁| + |v₂| + ... + |vₙ|
3. **Maximum / L-infinity Norm:** ‖v‖∞ = max(|v₁|, |v₂|, ..., |vₙ|)
4. **Generalised Lp Norm:** ‖v‖ₚ = (|v₁|ᵖ + |v₂|ᵖ + ... + |vₙ|ᵖ)^(1/p)

## Norms vs Metrics

A metric is more general: it deals with two variables and requires symmetry. A norm is defined for vectors, quantifies single vectors, and does not need symmetry.

**Every norm induces a metric, but not every metric comes from a norm.**

For example, given a vector v = (x, y):

- Norm: ‖v‖₂ = √(x² + y²)
- Induced metric for two vectors u = (x₁, y₁) and v = (x₂, y₂): d(u, v) = ‖u - v‖₂ = √((x₁ - x₂)² + (y₁ - y₂)²), which is the Euclidean distance.
