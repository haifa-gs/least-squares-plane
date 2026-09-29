# least-squares-plane
Proof of Concept Course – Least-squares plane fitting from data
# Least-Squares Plane Fitting


This repository contains the work carried out for the Proof of Concept assignment.

The objective is to develop a Python-based solution that:

* Imports 3D point data from a `.txt` file.
* Computes the plane that best fits the data using the **least-squares method**.
* Displays the original 3D points.
* Displays the calculated least-squares plane in a 3D representation.
* Presents the resulting plane equation and fitting results.

## Repository Structure

```text
least-squares-plane/
│
├── README.md
│
├── data/
│   └── data.txt
│
├── notebook/
│   └── least_squares_plane.ipynb
│
└── src/
    └── plane_fitting.py
```

### Files and Folders

**`README.md`**

This file provides an overview of the project, its objective, repository structure, and methodology.

**`data/data.txt`**

Contains the 3D point cloud used for the plane fitting. Each line contains three numerical values corresponding to:

```text
x  y  z
```

The three columns represent the coordinates of each point in a 3D Cartesian coordinate system.

**`notebook/least_squares_plane.ipynb`**

Jupyter Notebook presenting the complete work carried out for the assignment, including:

1. Importing the required Python libraries.
2. Loading the 3D data from `data.txt`.
3. Preparing the data for computation.
4. Computing the least-squares plane.
5. Determining the plane coefficients.
6. Displaying the plane equation.
7. Visualizing the original points and fitted plane in 3D.
8. Evaluating the fitting result.

**`src/plane_fitting.py`**

Python source code containing the plane-fitting implementation. It is separated from the notebook to keep the project organized and reusable.

## Mathematical Approach

The fitted plane is expressed in the form:

$$
z = ax + by + c
$$

where:

* \(a\) is the coefficient associated with \(x\),
* \(b\) is the coefficient associated with \(y\),
* \(c\) is the intercept.

For a set of measured points \((x_i,y_i,z_i)\), the coefficients are obtained by minimizing the sum of squared vertical errors:

$$
\min_{a,b,c}\sum_{i=1}^{n}
\left(z_i-(ax_i+by_i+c)\right)^2
$$

The resulting plane represents the least-squares approximation of the input 3D point cloud.

## Technologies

The project uses:

* **Python**
* **Jupyter Notebook**
* **NumPy**
* **Matplotlib**

## How to Use

Open the notebook:

```text
notebook/least_squares_plane.ipynb
```

and execute the cells sequentially.

The notebook reads the input data from:

```text
data/data.txt
```

and produces the least-squares plane and its 3D visualization.

## Author

**Master's Student – Advanced Manufacturing & Smart Systems (IN2P)**

This repository was created as part of the **Proof of Concept** course assignment.
