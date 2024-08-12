
# Complex Empirical Orthogonal Functions (CEOFs)

Complex Empirical Orthogonal Functions (CEOFs) extend the concept of EOFs to complex-valued data, capturing both the amplitude and phase of oscillatory patterns. This is particularly useful in analyzing waveforms and other oscillatory phenomena.

## Key Concepts:

### Amplitude and Phase Information:
- **Amplitude**: The magnitude of the complex EOF represents the strength of the pattern.
- **Phase**: The argument (or angle) of the complex EOF represents the phase of the oscillation.

### Mathematical Procedure:

Given a complex data matrix $\mathbf{Z}$ with dimensions $m \times n$ (where $m$ is the number of time steps and $n$ is the number of spatial points), perform SVD:

$$
\mathbf{Z} = \mathbf{U} \mathbf{\Sigma} \mathbf{V}^T
$$

Where:
- $\mathbf{U}$ contains the left singular vectors (Complex EOF modes).
- $\mathbf{\Sigma}$ contains the singular values.
- $\mathbf{V}^T$ contains the right singular vectors.

### Spatial Patterns (Complex EOF Modes):
The spatial patterns (Complex EOF modes) are given by the columns of $\mathbf{U}$.

### Time Series (Complex Principal Components):
The time series corresponding to each CEOF are obtained by multiplying the right singular vectors by the singular values:

$$
\mathbf{PC} = \mathbf{U} \mathbf{\Sigma}
$$

### Summary:
CEOFs are useful for analyzing data with oscillatory behavior, providing insights into both the magnitude and phase of the dominant modes of variability.
