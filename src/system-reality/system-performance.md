---
minutes: 10
---

# Performance and Locality

There's more to performance than asymptotic complexity.

- Constant factors matter
- Exact operation count does not predict performance
  - 10-to-1 improvement depending on how code is written
  - Exploiting time and space locality to improve performance
  - Optimization opportunities at multiple levels: algorithm, data representations, function calls, loops
- Need to understand system to optimize performance
  - How programs compiled and executed
  - How to improve performance without sacrificing modularity and generality
    - It must be allocated and managed
    - Many applications are memory-dominated

## Access Pattern
Which code runs faster? Why?
```c,editable
void copyij(int src[2048][2048], int dst[2048][2048]) {
  int i,j;
  for (i = 0; i < 2048; i++)
    for (j = 0; j < 2048; j++)
      dst[i][j] = src[i][j]
```

```c,editable
void copyij(int src[2048][2048], int dst[2048][2048]) {
  int i,j;
  for (j = 0; j < 2048; j++)
    for (i = 0; i < 2048; i++)
      dst[i][j] = src[i][j]
```

<details>

Based on hierarchical memory orgranization, copyij is 20x (4.3ms) faster than copy ji (81.8ms)
on 2.0 GHz i7 Haswell due to how the program steps through multidimensional array with lowered cache-miss rates.

Similar performance improvement is seen in analytics engine based on serialization format (Arrow, Parquet) which
organize data in column-oriented instead of row-oriented (as in transactional database) and gain higher performance for analytical functions. 

</details>
