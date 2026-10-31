# Approximate Nearest Neighbor (ANN) Search

This ANN project implements efficient data structures in C++ to index and search high-dimensional vector data.

## Features
* **Custom Data Structures:** Includes a `DataVector` class for mathematical vector operations (Euclidean distance, dot product, norms) and a `VectorDataset` class for managing collections of vectors loaded from CSV files.
* **K-Dimensional Tree (KD-Tree):** Implements KD-Tree indexing for multidimensional space partitioning and fast k-nearest neighbor queries.
* **Random Projection Tree (RP-Tree):** Implements RP-Trees for handling higher-dimensional data by partitioning space based on projections onto random vectors.
* **Benchmarking:** Built-in timing modules to evaluate the performance of tree building, data loading, and query searching.

## File Structure
* `DataVector.h` & `DataVector.cpp`: Defines the core vector operations.
* `VectorDataSet.h`: Handles reading and parsing of CSV datasets into memory.
* `TreeIndex.h` & `TreeIndex.cpp`: Contains the core `TreeIndex` base class, along with the `KDTreeIndex` and `RPTreeIndex` implementations. The `main()` execution loop is also located here for benchmarking.

## Prerequisites
* A C++ compiler that supports C++11 or higher (e.g., GCC, Clang).

## Setup and Execution

1. **Prepare Datasets:** Ensure your training and testing CSV files (e.g., `fmnist-train.csv` and `fmnist-test.csv`) are placed in the root directory alongside the source code.
2. **Compile:** Run the following command in your terminal to compile the code (using the `-O3` flag for optimization):
   ```bash
   g++ -std=c++11 -O3 -o ann_search TreeIndex.cpp DataVector.cpp
