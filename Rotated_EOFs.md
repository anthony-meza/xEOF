
# Rotated Empirical Orthogonal Functions (REOFs)

Rotated EOFs (REOFs) involve rotating the EOFs to achieve more localized and interpretable patterns, often using Varimax rotation. This is useful when the original EOFs are not well localized.

## Key Concepts:

### Varimax Rotation:
- **Rotation**: Rotate the EOFs to maximize the variance captured by each mode, making the modes more interpretable.
- **Localized Patterns**: The resulting REOFs are often more physically meaningful and easier to interpret.

### Mathematical Procedure:

Given the EOFs obtained from SVD, the Varimax rotation maximizes the sum of the variances of the squared loadings:

$$
\sum_{i} \sum_{j} \left[ R_{ij}^2 - \frac{1}{p} \sum_{i} R_{ij}^2 \right]^2
$$

Where $R_{ij}$ are the elements of the rotation matrix.

### Time Series (Rotated Principal Components):
The time series corresponding to each REOF are obtained by projecting the original data onto the rotated EOFs:

$$
\mathbf{RPC} = \mathbf{X} \mathbf{RE}
$$

Where:
- $\mathbf{RPC}$ represents the time series associated with each REOF.
- $\mathbf{RE}$ represents the rotated EOFs.

### Summary:
REOFs improve the interpretability of EOFs by localizing the variance captured by each mode, making them particularly useful in fields like meteorology and oceanography.
