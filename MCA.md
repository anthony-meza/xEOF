
# Maximum Covariance Analysis (MCA)

Maximum Covariance Analysis (MCA) is a technique used to identify coupled patterns between two different datasets by finding pairs of patterns that explain the maximum covariance between them.

## Key Concepts:

### Cross-Covariance Matrix:
- **Covariance**: Compute the cross-covariance matrix between two datasets to capture the relationships between them.

### Singular Value Decomposition (SVD):
- **SVD**: Perform SVD on the cross-covariance matrix to extract the modes of variability that maximize the covariance between the two datasets.

### Mathematical Definition:

Given two datasets \( \mathbf{X} \) with dimensions \( m \times p \) and \( \mathbf{Y} \) with dimensions \( m \times q \) (where \( m \) is the number of time steps, \( p \) and \( q \) are the number of spatial points in each dataset), compute the cross-covariance matrix:

\[
\mathbf{C}_{XY} = \frac{1}{m-1} \mathbf{X}^T \mathbf{Y}
\]

Perform SVD on \( \mathbf{C}_{XY} \):

\[
\mathbf{C}_{XY} = \mathbf{U} \mathbf{\Sigma} \mathbf{V}^T
\]

Where:
- \( \mathbf{U} \) and \( \mathbf{V} \) are the spatial patterns for each dataset.
- \( \mathbf{\Sigma} \) contains the singular values representing the magnitude of covariance explained by each mode.

### Summary:
MCA identifies coupled patterns of variability between two datasets, making it a powerful tool for studying interactions between different physical processes.
