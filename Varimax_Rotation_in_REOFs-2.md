
# Varimax Rotation in Rotated Empirical Orthogonal Functions (REOFs)

Varimax rotation is a statistical technique used to simplify the interpretation of factor analysis results, including Empirical Orthogonal Functions (EOFs). In the context of EOF analysis, varimax rotation is applied to the EOF modes to obtain Rotated Empirical Orthogonal Functions (REOFs). The goal of varimax rotation is to make the patterns more localized and interpretable.

## Key Concepts

### EOF Modes
- **EOF Modes**: These are the spatial patterns obtained from the standard EOF analysis. They represent the dominant modes of variability in the data.
- **Principal Components (PCs)**: These are the time series associated with each EOF mode, showing how the strength of each mode varies over time.

### Varimax Rotation
- **Rotation**: Varimax rotation is an orthogonal rotation technique that maximizes the variance of the squared loadings of a factor (or EOF mode) across variables. In simpler terms, it makes the EOF modes more interpretable by making the loading patterns more distinct.
- **Orthogonal Rotation**: Varimax rotation preserves the orthogonality (independence) of the rotated EOF modes, ensuring that they remain uncorrelated with each other.

## Mathematical Procedure

### 1. Initial EOF Analysis
Perform the standard EOF analysis to obtain the EOF modes and the associated principal components (PCs). This involves:

- Computing the covariance matrix of the data.
- Performing Singular Value Decomposition (SVD) on the covariance matrix.
- Extracting the EOF modes (spatial patterns) and PCs (time series).

### 2. Rotation Matrix Initialization
Initialize the rotation matrix as an identity matrix. The rotation matrix will be used to transform the EOF modes into REOFs.

$$
\mathbf{R} = \mathbf{I}
$$

Where:
- $$\mathbf{R}$$ is the rotation matrix.
- $$\mathbf{I}$$ is the identity matrix.

### 3. Iterative Rotation
Apply the following steps iteratively to maximize the variance of the squared loadings:

1. **Transform the EOF Modes**: Multiply the EOF modes by the rotation matrix.

$$
\mathbf{Z} = \mathbf{E} \mathbf{R}
$$

Where:
- $$\mathbf{Z}$$ is the transformed EOF modes.
- $$\mathbf{E}$$ is the matrix of EOF modes.

2. **Compute the Squared Loadings**: Square the transformed EOF modes.

$$
\mathbf{L} = \mathbf{Z}^2
$$

Where:
- $$\mathbf{L}$$ is the matrix of squared loadings.

3. **Perform SVD on the Squared Loadings**: Perform SVD on the matrix formed by the product of the transformed EOF modes and their squared loadings.

$$
\mathbf{U}, \mathbf{S}, \mathbf{V}^T = \text{SVD}(\mathbf{Z}^T \mathbf{L})
$$

4. **Update the Rotation Matrix**: Update the rotation matrix by multiplying it with the orthogonal matrices obtained from the SVD.

$$
\mathbf{R} = \mathbf{U} \mathbf{V}^T
$$

5. **Check for Convergence**: Repeat steps 1-4 until the change in the rotation matrix is sufficiently small (i.e., the process has converged).

### 4. Apply Rotation
Once the rotation matrix has converged, apply it to the original EOF modes to obtain the rotated EOFs (REOFs):

$$
\mathbf{REOF} = \mathbf{E} \mathbf{R}
$$

### 5. Interpretation
The resulting REOFs are spatial patterns that are typically more localized and interpretable than the original EOFs. The associated principal components (PCs) remain the same, but the spatial patterns are now rotated to maximize the variance of the squared loadings.

## Summary

Varimax rotation is a powerful technique used to enhance the interpretability of EOF modes by rotating them to produce Rotated EOFs (REOFs). The rotation process involves maximizing the variance of the squared loadings across variables, resulting in spatial patterns that are more distinct and easier to interpret. This technique is widely used in meteorology, oceanography, and other fields where EOF analysis is applied.

