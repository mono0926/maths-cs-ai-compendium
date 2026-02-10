# Vector Calculus

## Gradient

The **gradient** vector at a point indicates the direction of steepest ascent of a scalar field, and its magnitude is the rate of change in that direction. Think of it as the "slope" of the field at a given point.

In Cartesian coordinates:

∇f = (∂f/∂x, ∂f/∂y, ∂f/∂z)

It operates on a **scalar field** and produces a **vector field**.

**Example:** Consider a temperature distribution in a room. The gradient of this temperature field would point from cooler regions to warmer regions, and its magnitude would indicate how quickly the temperature changes.

## Divergence

The **divergence** at a point measures the net flow of a vector field out of an infinitesimal volume around that point. It indicates whether the field is a **source** (positive divergence) or a **sink** (negative divergence).

∇ · F = ∂F₁/∂x + ∂F₂/∂y + ∂F₃/∂z

It operates on a **vector field** and produces a **scalar field**.

**Example:** Imagine water flowing in a pipe. The divergence of the velocity field would be positive where the water is entering the pipe (source) and negative where it is leaving (sink).

## Curl

The **curl** at a point measures the tendency of the vector field to rotate around that point. The direction of the curl vector indicates the axis of rotation, and its magnitude indicates the strength of rotation.

∇ × F = (∂F₃/∂y - ∂F₂/∂z, ∂F₁/∂z - ∂F₃/∂x, ∂F₂/∂x - ∂F₁/∂y)

It operates on a **vector field** and produces a **vector field**.

**Example:** Think of a whirlpool. The curl of the velocity field would be nonzero around the centre of the whirlpool, indicating the swirling motion.
