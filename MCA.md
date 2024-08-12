
# Maximum Covariance Analysis (MCA)

Maximum Covariance Analysis (MCA) is a technique used to identify coupled patterns between two different datasets by finding pairs of patterns that explain the maximum covariance between them.

## Key Concepts:

### Cross-Covariance Matrix:
- **Covariance**: Compute the cross-covariance matrix between two datasets to capture the relationships between them.

### Singular Value Decomposition (SVD):
- **SVD**: Perform SVD on the cross-covariance matrix to extract the modes of variability that maximize the covariance between the two datasets.

### Mathematical Procedure:

Given two datasets $\mathbf{X}$ with dimensions $m \times p$ and $\mathbf{Y}$ with dimensions $m \times q$ (where $m$ is the number of time steps, $p$ and $q$ are the number of spatial points in each dataset), compute the cross-covariance matrix:

$$
\mathbf{C}_{XY} = \frac{1}{m-1} \mathbf{X}^T \mathbf{Y}
$$

Perform SVD on $\mathbf{C}_{XY}$:

$$
\mathbf{C}_{XY} = \mathbf{U} \mathbf{\Sigma} \mathbf{V}^T
$$

Where:
- $\mathbf{U}$ and $\mathbf{V}$ are the spatial patterns for each dataset.
- $\mathbf{\Sigma}$ contains the singular values representing the magnitude of covariance explained by each mode.

### Time Series (Expansion Coefficients):

The time series (expansion coefficients) corresponding to the MCA modes are obtained by projecting the original data onto the MCA modes:

$$
\mathbf{PC}_X = \mathbf{X} \mathbf{U}
$$
$$
\mathbf{PC}_Y = \mathbf{Y} \mathbf{V}
$$

Where:
- $\mathbf{PC}_X$ and $\mathbf{PC}_Y$ represent the time series associated with the MCA modes for datasets $\mathbf{X}$ and $\mathbf{Y}$, respectively.

### Summary:
MCA identifies coupled patterns of variability between two datasets, making it a powerful tool for studying interactions between different physical processes.
