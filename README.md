# C-Struct-Layout-and-Cache-Efficiency-Analyzer

This project, titled 'Struct Layout and Cache Efficiency Analyzer,' is developed in C to investigate the impact of different struct layouts on cache performance. It emphasizes the importance of memory layout in struct design and its implications for computational efficiency.

Key Features:

Performance Measurement: Implements clock_gettime() for precise timing of various struct-based computations.
Struct Layouts: Compares two struct types - int_field_t (individual int fields) and arr_field_t (arrays of ints) to demonstrate the impact of memory stride.

Optimization Approaches: Includes both base and optimized (optm) versions for each struct type, showcasing effective optimization techniques.

Efficiency Analysis: Demonstrates a notable reduction in CPU time through optimizations, providing insights into efficient data structuring and loop unrolling.

Versatile Usage: The tool can be run with customizable parameters for array length and iteration count, allowing users to observe performance across different scales.
Performance Metrics:

int_field_base vs arr_field_base: Demonstrates the difference in memory layout where int_field_base has an ABABAB pattern, leading to memory stride, while arr_field_base follows an AAAAABBBBB pattern, reducing the stride.
optm versions: Showcases fewer loop checks and the elimination of memory stride, leading to more efficient computations.
Usage:

./struct_stride <arr_length> <num_iters>

Example Output:

method: int_field_base CPU time: 1.2345e-01 sec   sum: 0
method: arr_field_base CPU time: 1.2345e-01 sec   sum: 0
method: int_field_optm CPU time: 1.2345e-01 sec   sum: 0
method: arr_field_optm CPU time: 1.2345e-01 sec   sum: 0
