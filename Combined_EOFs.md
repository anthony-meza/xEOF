
# Combined Empirical Orthogonal Functions (Combined EOFs)

Combined Empirical Orthogonal Functions (Combined EOFs) are an extension of EOF analysis that is used to analyze coupled patterns of variability between multiple datasets. This technique is useful for identifying common modes of variability across different fields or regions.

## Key Concepts:

### Combined Dataset:
- **Data Matrices**: Typically, you have multiple datasets (e.g., \( \mathbf{X} \) and \( \mathbf{Y} \)) that you want to analyze together. These datasets are concatenated along the spatial dimension to form a combined dataset.
- **Covariance Matrix**: Compute the covariance matrix of the combined dataset to capture the relationships between all variables across datasets.
- **Eigenvalue Decomposition**: Perform eigenvalue decomposition on the covariance matrix to extract the combined EOF modes.

### Mathematical Definition:

Given two datasets \( \mathbf{X} \) with dimensions \( m \times p \) and \( \mathbf{Y} \) with dimensions \( m \times q \) (where \( m \) is the number of time steps, and \( p \) and \( q \) are the number of spatial points in each dataset), the combined dataset \( \mathbf{Z} \) is formed by concatenating \( \mathbf{X} \) and \( \mathbf{Y} \):

\[
\mathbf{Z} = [\mathbf{X}, \mathbf{Y}]
\]

The combined dataset \( \mathbf{Z} \) will have dimensions \( m \times (p+q) \).

Compute the covariance matrix \( \mathbf{C} \) of the combined dataset:

\[
\mathbf{C} = \frac{1}{m-1} \mathbf{Z}^T \mathbf{Z}
\]

Perform eigenvalue decomposition on \( \mathbf{C} \):

\[
\mathbf{C} = \mathbf{E} \mathbf{\Lambda} \mathbf{E}^T
\]

Where:
- \( \mathbf{E} \) contains the eigenvectors (Combined EOFs).
- \( \mathbf{\Lambda} \) contains the eigenvalues, representing the variance explained by each Combined EOF.

### Time Series (Combined Principal Components):

The time series (Combined Principal Components, CPCs) corresponding to each Combined EOF are obtained by projecting the original combined dataset onto the Combined EOFs:

\[
\mathbf{CPC} = \mathbf{Z} \mathbf{E}
\]

Where:
- \( \mathbf{CPC} \) represents the time series associated with each Combined EOF.

### Summary:
Combined EOFs are useful for identifying common modes of variability across multiple datasets, making them a powerful tool for studying interconnected processes in different regions or fields.
