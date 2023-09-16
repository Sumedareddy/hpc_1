# Matrix Multiplication with OpenMP

## Code Explanation

This program performs the following steps:

1. **Command-Line Arguments**: It accepts two command-line arguments - `matrix_size` and `num_threads`. These arguments determine the size of the matrices and the number of threads to use for parallel execution.

2. **Memory Allocation**: Dynamic memory allocation is used to create three matrices `A`, `B`, and `C`. These matrices will hold the input matrices and the result of matrix multiplication.

3. **Initialization**: Matrices `A` and `B` are initialized with the value 2, while matrix `C` is initialized with zeros.

4. **Parallel Matrix Multiplication**: The core matrix multiplication operation is parallelized using OpenMP. The `#pragma omp parallel for` directive splits the work among multiple threads. Each thread calculates a portion of the result matrix `C`.

5. **Timing**: The program measures the elapsed time for the matrix multiplication using the `gettimeofday` function. This provides a measure of the program's performance.

6. **Memory Deallocation**: After the matrix multiplication is complete, memory is deallocated to prevent memory leaks.

## How to Compile and Run

To compile the program, open a terminal and navigate to the directory containing the code. Use the following command:

```bash
gcc -o matrix_multiplication matrix_multiplication.c -fopenmp
```

This command compiles the code with OpenMP support and generates an executable named matrix_multiplication.

To run the program, use the following command:
```bash
./matrix_multiplication <matrix_size> <num_threads>
```

For finding nth power of the matrix:
```bash
./matrix_multiplication <matrix_size> <exponent> <num_threads>
```

Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2
```

For nth power:
Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2 4
```

This will perform matrix multiplication with matrices of size 1000x1000 using 4 threads.

## Output

The program will display the size of the matrices, the number of threads used, and the elapsed time for matrix multiplication.

Graph for the same are as below:

1. **OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/2c7a26e8-21ac-4fad-9a25-91f7e81205ce)

     ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/91f76257-2b14-4493-8903-379069b1fb95)

     ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/1e94ce87-affd-424f-83c6-6d7d711261e6)

   
2. **Nth Power of Matrix with OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/fa3758c3-aae2-4eb3-ae5b-d32cad262dee)

     ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/4bf20f37-2797-45aa-b3e6-ad247c57a988)

     ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/832d2358-bb25-41a8-87f7-85b671892165)


## Conclusion

This C program demonstrates how to use OpenMP to parallelize matrix multiplication, improving the performance of the computation. You can adjust the matrix size and the number of threads to observe the impact on execution time.




# Block Matrix Multiplication

```markdown
# Block Matrix Multiplication

Compile the program using a C compiler. For example:

gcc -o block_matrix_mult block_matrix_mult.c -fopenmp
```

Here, block_matrix_mult is the name of the executable.

To run the program, use the following command-line format:
```bash
./block_matrix_mult <matrix_size> <num_threads> <block_size>
```

For nth power of a matrix using BMM:
```bash
./block_matrix_mult <matrix_size> <exponent> <num_threads> <block_size>
```

<matrix_size>: The size of the square matrices (e.g., 100 for a 100x100 matrix).
<block_size>: The size of the square blocks (e.g., 10 for a 10x10 block).
For example, to multiply two 100x100 matrices using 10x10 blocks:

```bash
./block_matrix_mult 1024 6 4
```

For nth power:
```bash
./block_matrix_mult 1024 2 6 4
```

## Output
The program will display the size of the matrices, the block size, and the result of the multiplication.

1. **BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/366c34c9-55b3-4eb1-bebb-9aaa3f6a73fc)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/607512c0-d6f7-4f36-acc3-d5a1dc849bfb)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/6e8d905f-5c6e-4730-a728-e014e11a6fd3)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/19c9c129-137c-4ebe-ae41-f03ce7f855a7)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/e790309e-12a6-4a39-a80d-c9c7d37e654b)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/5ec131c9-3380-4c83-b7e1-bfcd753619d2)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/3ca97db2-182a-47f1-aa20-5ed82e747240)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/32f15d88-1017-4771-9349-f5d95fc829cf)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/734fb3e3-e702-485a-98a2-2f8311be25ea)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/4f3c3d37-3c45-4163-8b56-10acf996a951)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/544a2452-9c23-4b30-9200-7dfe37f82669)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/ceb944d4-9431-4c8d-a82d-19a32c7d4380)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/792e336b-8728-40a7-82be-9281440917e8)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/1a07c006-311b-4d71-97dd-97210db7883d)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/5c6aba1e-ba9d-4611-af42-be113739884c)


3. **Nth Power of Matrix with BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/60703ee2-39b3-44af-bdc4-81c9e3b8aded)

   ![image](https://github.com/Sumedareddy/hpc_1/assets/145221872/a7dcc100-0fa4-425a-9448-7de619f98646)


## Memory Management
The program dynamically allocates memory for matrices A, B, and C, as well as for the block buffers. It frees the allocated memory after the multiplication is complete to prevent memory leaks.
