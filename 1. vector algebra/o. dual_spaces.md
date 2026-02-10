# Dual Spaces

The **dual space** of a vector space V, denoted V*, is the set of all **linear functionals** on V. A linear functional is a linear map from V to its field of scalars (usually ℝ or ℂ). In simpler terms, a linear functional takes a vector as input and returns a scalar as output.

## Duality Pairing

The **duality pairing** is a bilinear map that associates a vector v in V and a linear functional φ in V* with a scalar, denoted ⟨φ, v⟩ or φ(v).

### Properties

1. **Linearity in the first argument:** ⟨aφ + bψ, v⟩ = a⟨φ, v⟩ + b⟨ψ, v⟩ for all scalars a, b and linear functionals φ, ψ
2. **Linearity in the second argument:** ⟨φ, au + bv⟩ = a⟨φ, u⟩ + b⟨φ, v⟩ for all scalars a, b and vectors u, v

## Dual Basis

Given a basis {e₁, e₂, ..., eₙ} for V, there exists a unique **dual basis** {e₁*, e₂*, ..., eₙ*} for V* such that:

⟨eᵢ*, eⱼ⟩ = δᵢⱼ

where δᵢⱼ is the **Kronecker delta** (1 if i = j, 0 otherwise). The dual basis vectors act as "projection functions" onto the original basis vectors.

## The Dot Product as Duality

In Euclidean space, the dot product between two vectors can be seen as a duality pairing. Given a vector v, the dot product with v defines a linear functional φ(u) = u · v.

Think of a vector space as a collection of arrows. Each arrow has a length and direction. Now imagine a different collection of arrows, each representing a way to measure the projection of the first set of arrows onto a particular direction. These "measuring arrows" are essentially linear functionals, and they live in the dual space.

- The dot product is the bridge between these two worlds. When you take the dot product of a vector with another vector (acting as a measuring arrow), you get a number representing the projection of the first vector onto the direction of the second, scaled by its length.
- The coordinates of **w** = (a, b) define the weights of the linear combination of the components of **v** = (x, y), yielding v · w = ax + by.
