
# Complex Empirical Orthogonal Functions (CEOFs)

Complex Empirical Orthogonal Functions (CEOFs) extend the concept of EOFs to complex-valued data, capturing both the amplitude and phase of oscillatory patterns. This is particularly useful in analyzing waveforms and other oscillatory phenomena.

## Key Concepts:

### Amplitude and Phase Information:
- **Amplitude**: The magnitude of the complex EOF represents the strength of the pattern.
- **Phase**: The argument (or angle) of the complex EOF represents the phase of the oscillation.

### Mathematical Definition:

Given a complex data matrix \( \mathbf{Z} \) with dimensions \( m \times n \) (where \( m \) is the number of time steps and \( n \) is the number of spatial points), the complex covariance matrix \( \mathbf{C} \) is given by:

\[
\mathbf{C} = \frac{1}{m-1} \mathbf{Z}^H \mathbf{Z}
\]

Where:
- \( \mathbf{Z}^H \) is the conjugate transpose of \( \mathbf{Z} \).

Perform eigenvalue decomposition on \( \mathbf{C} \) to obtain the complex EOFs and their corresponding eigenvalues.

### Time Series (Complex Principal Components):

The time series corresponding to each CEOF are obtained by projecting the original complex data onto the complex EOFs:

\[
\mathbf{PC} = \mathbf{Z} \mathbf{E}
\]

Where:
- \( \mathbf{PC} \) represents the complex time series associated with each CEOF.

### Summary:
CEOFs are useful for analyzing data with oscillatory behavior, providing insights into both the magnitude and phase of the dominant modes of variability.
