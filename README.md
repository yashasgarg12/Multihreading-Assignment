<img width="999" alt="Screenshot 2024-04-13 at 5 51 15 PM" src="https://github.com/yashasgarg12/Multihreading-Assignment/assets/107528489/a65d0e06-819c-48ee-bf80-fe50b2cf0dad">



## Methodology: Multithreaded Matrix Multiplication with Performance Analysis

This code implements a multithreaded approach to perform matrix multiplication while analyzing the impact of thread count on performance. Here's a breakdown of the key steps:

**1. Problem Definition:**

- The code multiplies a set of random matrices (`num_matrices`) of size `n x n` with a constant identity matrix of the same size.
- It measures the execution time for different numbers of threads (1 to 8) to evaluate the potential benefits of multithreading.

**2. Multithreading Strategy:**

- Similar to the previous version, the workload is divided into smaller chunks based on the number of available CPU cores (`num_cores`).
- Each thread is assigned a specific row range (`start_row` to `end_row`) of the resulting product matrices (`result_matrices`).

**3. Key Functions:**

- **`multiply_matrix`** (same as before): Performs row-wise multiplication of a random matrix with the constant matrix.
- **`generate_random_matrices`** (same as before): Generates a list of random matrices.
- **`get_cpu_usage`** (same as before, optional): Monitors CPU usage during execution.
- **`main` function:**
    - Defines matrix sizes and the number of matrices to generate.
    - Creates random matrices and an empty list (`result_matrices`) to store the products.
    - **Performance Analysis Loop:**
        - Iterates through different numbers of threads (1 to 8).
            - Records the start time.
            - Creates and starts threads, assigning each a specific row range for multiplication.
            - Waits for all threads to finish.
            - Records the end time and calculates the execution time.
            - Stores the execution time for this thread count.
            - Optionally monitors and prints CPU and memory usage during execution.
    - Plots the execution time vs. the number of threads to visualize the performance impact.
    - Optionally prints or processes the resulting product matrices.
    - Plots the average values of each resulting matrix (optional).
    - Writes the execution time data to a CSV file for further analysis.

**4. Libraries Used:**

- **NumPy (`np`):** Provides efficient numerical operations on multidimensional arrays.
- **Threading (`threading`):** Enables creating and managing multiple threads for concurrent execution.
- **Optional: `psutil`:** Used for monitoring CPU usage (if enabled).
- **Optional: `matplotlib.pyplot` (`plt`):** Used for creating plots (if enabled).
- **`time`:** Measures execution time.
- **`csv`:** Used for writing data to a CSV file.

**5. Analysis and Output:**

- The code generates two plots:
    - One plot shows the execution time for different numbers of threads.
    - The other plot visualizes the average values of each resulting matrix.
- It also writes the execution time data to a CSV file for further analysis. This allows you to compare the performance impact of using different thread counts.

**6. Conclusion:**

This code demonstrates a more comprehensive approach to multithreaded matrix multiplication. It not only performs the calculations but also analyzes the performance by measuring execution time for different thread configurations. This analysis helps you understand how thread count affects performance and determine the optimal number of threads for your specific hardware and workload.

<img width="761" alt="Screenshot 2024-04-13 at 5 51 28 PM" src="https://github.com/yashasgarg12/Multihreading-Assignment/assets/107528489/ba925211-1796-455c-9517-a0bf4156e66d"><img width="294" alt="Screenshot 2024-04-13 at 5 52 05 PM" src="https://github.com/yashasgarg12/Multihreading-Assignment/assets/107528489/670cd8dc-1d90-4c6f-8998-99f8ce04e19f">

