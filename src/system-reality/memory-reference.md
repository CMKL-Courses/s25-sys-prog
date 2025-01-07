---
minutes: 10
---

# Memory Matters

Random Access Memory is an Unphysical abstraction

- Memory is not unbounded
  - It must be allocated and managed
  - Many applications are memory-dominated
- Memory referencing bugs especially pernicious
  - Effects are distant in both time and space
- Memory performance is not uniform
  - Cache and virtual memory effects can greatly affect program performance
  - Adapting program to characteristics of memory system can lead to major speed improvements

## Memory Referencing Bug
What would be the result of calling fun(i) where i is in 0..5 ?
```c,editable
typedef struct {
  int a[2];
  double d;
} struct_t;

double fun(int i) {
  volatile struct_t s;
  s.d = 3.14;
  s.a[i] = 1073741824; /* Possibly out of bounds */
  return s.d;
}
```

<details>

fun(0) -> 3.14

fun(1) -> 3.14

fun(2) -> 3.1399998664856

fun(3) -> 2.00000061035156

fun(4) -> 3.14

fun(5) -> Segmentation fault

</details>
