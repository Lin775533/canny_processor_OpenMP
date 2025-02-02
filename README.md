# Gaussian Blur Parallelization in Canny Edge Detection

This project demonstrates parallel implementations of the Gaussian blur operation using OpenMP and Pthreads. Both versions optimize the horizontal (`blur_x`) and vertical (`blur_y`) blur operations in the Canny edge detection algorithm.

## OpenMP Implementation

### Overview

The OpenMP version leverages OpenMP directives for automatic thread management and workload distribution. This implementation focuses on optimizing nested loops in both blur operations while maintaining computational accuracy.

### Implementation Details

```c
// Blur operations parallelized using OpenMP directives
#pragma omp parallel for collapse(2)
for (r = 0; r < rows; r++) {
    for (c = 0; c < cols; c++) {
        // Blur computation
    }
}
```

### Performance Results

* Initial `blur_x` parallelization achieved a 16.3% improvement in processing time
* Additional `blur_y` optimization resulted in a 10.3% performance increase
* Total execution time was reduced from 0.836s to 0.750s
