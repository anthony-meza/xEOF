
# Empirical Orthogonal Functions (EOFs)

Empirical Orthogonal Functions (EOFs) are a powerful tool for analyzing spatial-temporal datasets by decomposing the data into orthogonal modes of variability. These modes capture the dominant patterns of variability in the data.

## Key Concepts:

### EOF Analysis:
- **Data Matrix**: The data is typically organized as a matrix where each column represents a spatial variable, and each row represents a time step.
- **SVD for EOFs**: The data matrix can be decomposed using Singular Value Decomposition (SVD) to extract the principal components (EOFs).
- **EOF Modes**: The left singular vectors from the SVD represent the spatial patterns of variability (EOFs).
- **Principal Components (PCs)**: The right singular vectors scaled by the singular values represent the time series associated with each EOF, representing how the strength of the spatial pattern varies over time.

### Mathematical Procedure:

Given a data matrix $\mathbf{X}$ with dimensions $m \times n$ (where $m$ is the number of time steps and $n$ is the number of spatial points), perform SVD:

$$
\mathbf{X} = \mathbf{U} \mathbf{\Sigma} \mathbf{V}^T
$$

Where:
- $\mathbf{U}$ (dimensions $m \times m$) contains the left singular vectors (EOF modes).
- $\mathbf{\Sigma}$ (dimensions $m \times n$) is a diagonal matrix containing the singular values.
- $\mathbf{V}^T$ (dimensions $n \times n$) contains the right singular vectors.

### Spatial Patterns (EOF Modes):
The spatial patterns (EOF modes) are given by the columns of $\mathbf{U}$.

### Time Series (Principal Components):
The time series (Principal Components, PCs) are obtained by multiplying the right singular vectors by the singular values:

$$
\mathbf{PC} = \mathbf{U} \mathbf{\Sigma}
$$

### Summary:
EOF analysis is a method used to identify the most important patterns of variability in spatial-temporal data, making it a cornerstone technique in fields like meteorology, oceanography, and climate science.
