This project comprises three CUDA programming exercises:

Sum of First n Integers:

Iterative Approach: Calculates the sum of the first n integers using a loop.

Formula-Based Approach: Calculates the sum using the direct formula.

Vector Addition:

Implements vector addition using statically defined global variables.

Records kernel execution time.

Calculates theoretical and measured memory bandwidth.

Prerequisites
NVIDIA GPU with CUDA support.

CUDA Toolkit installed.

C++ compiler compatible with CUDA.

Compilation
Use the NVIDIA CUDA Compiler (nvcc) to compile the program:

bash
Copy
Edit
nvcc -O3 -o cuda_exercises cuda_exercises.cu
Execution
Run the compiled executable:

bash
Copy
Edit
./cuda_exercises
Exercises
1. Sum of First n Integers
a. Iterative Approach
Description: Calculates the sum by iterating from 1 to n.

Implementation: Each thread computes the sum independently.

b. Formula-Based Approach
Description: Uses the formula sum = n * (n + 1) / 2.

Implementation: Each thread applies the formula directly.

2. Vector Addition
Description: Adds two vectors of size N element-wise.

Implementation:

Uses statically defined global device arrays.

Launches a kernel where each thread computes one element of the result vector.

Measures kernel execution time using CUDA events.

Calculates:

Theoretical Memory Bandwidth: Based on device properties.

Measured Memory Bandwidth: Based on actual data transfer and execution time.

Sample Output
yaml
Copy
Edit
Vector addition successful.
Kernel execution time: 0.123456 ms
Theoretical Memory Bandwidth: 320.00 GB/s
Measured Memory Bandwidth: 150.00 GB/s
Note: Actual output will vary based on hardware and system load.

Profiling
To profile the application using nvprof:

bash
Copy
Edit
nvprof ./cuda_exercises
