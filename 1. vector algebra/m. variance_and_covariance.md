# Variance and Covariance

## Variance

The **variance** of a vector x measures the dispersion of its components:

Var(x) = Σ(xᵢ - x̄)² / n

where x̄ is the mean of x.

## Covariance

The **covariance** of two vectors x and y measures the direction of the relationship between them:

Cov(x, y) = Σ((xᵢ - x̄)(yᵢ - ȳ)) / n

- A **positive** covariance means both variables tend to be high or low at the same time.
- A **negative** covariance means when one variable is high, the other tends to be low.

## Covariance Matrix

For a set of variables X₁, X₂, ..., Xₙ, the covariance matrix is:

```
    | Cov(X₁,X₁)  Cov(X₁,X₂)  ...  Cov(X₁,Xₙ) |
    | Cov(X₂,X₁)  Cov(X₂,X₂)  ...  Cov(X₂,Xₙ) |
    |     ⋮            ⋮         ⋱       ⋮        |
    | Cov(Xₙ,X₁)  Cov(Xₙ,X₂)  ...  Cov(Xₙ,Xₙ) |
```

The diagonal entries are the variances of each variable, and the off-diagonal entries capture the pairwise covariances.
