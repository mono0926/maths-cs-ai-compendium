# Dot Product

The **dot product** is an inner product defined on Euclidean space. In a vector space, it multiplies two vectors together to produce a scalar.

## Cosine Rule

The cosine rule (law of cosines) relates the lengths of the sides of a triangle to the cosine of one of its angles. It is a generalisation of the Pythagorean theorem:

c² = a² + b² - 2ab cos(C)

By analysing the cosine of an angle, you can determine whether the triangle is:
- **Acute** — cosine is positive
- **Obtuse** — cosine is negative
- **Right** — cosine is zero

## Definition

The dot product between **a** and **b** can be viewed as the projection of **a** onto **b**, scaled by the length of **b**:

a · b = ‖a‖ ‖b‖ cos(θ)

This is derived from the cosine rule.

## Properties

1. **Commutativity:** a · b = b · a
2. **Distributivity:** a · (b + c) = a · b + a · c
3. **Scalar Multiplication:** (ka) · b = a · (kb) = k(a · b)
4. **Relationship with Magnitude:** a · a = ‖a‖²
5. **Orthogonality:** Two non-zero vectors are orthogonal (perpendicular) if and only if their dot product is zero.
6. **Parallel Vectors:** If two vectors are parallel, their dot product is simply the product of their magnitudes.
7. **Unit Vectors:** The dot product of two unit vectors is simply the cosine of the angle between them.

## Projection

The **projection** of a vector **a** onto **b** is given by:

proj_b(a) = ((a · b) / ‖b‖²) b

It can be thought of as the shadow cast by the original vector onto the direction vector.

## Cosine Similarity

The **cosine similarity** between two vectors is the cosine of their inclination angle:

cos(θ) = (A · B) / (‖A‖ ‖B‖)

Properties:
1. Ranges from -1 to 1.
2. A value of **1** means the vectors point in the same direction (θ = 0°).
3. A value of **-1** means the vectors point in opposite directions (θ = 180°).
4. A value of **0** means the vectors are orthogonal (θ = 90°).
