# CMPS 2200 Reciation 5
## Answers

**Name:** Shira Rozenthal and Zachary Wiel


Place all written answers from `recitation-06.md` here for easier grading.






- **1b.**


SORTED: 

|   n |   qsort-fixed-pivot |   qsort-random-pivot |
|-----|---------------------|----------------------|
|   5 |               0.024 |                0.031 |
|  10 |               0.042 |                0.040 |
|  15 |               0.063 |                0.061 |
|  25 |               0.153 |                0.103 |
|  50 |               0.458 |                0.216 |
|  75 |               1.016 |                0.419 |
| 100 |               1.984 |                0.518 |
| 150 |               3.591 |                0.735 |
| 250 |              10.288 |                1.255 |
| 500 |              36.998 |                2.922 |


UNSORTED: 

|   n |   qsort-fixed-pivot |   qsort-random-pivot |
|-----|---------------------|----------------------|
|   5 |               0.021 |                0.028 |
|  10 |               0.031 |                0.038 |
|  15 |               0.046 |                0.058 |
|  25 |               0.081 |                0.102 |
|  50 |               0.179 |                0.223 |
|  75 |               0.288 |                0.389 |
| 100 |               0.682 |                0.474 |
| 150 |               0.597 |                1.115 |
| 250 |               1.320 |                1.609 |
| 500 |               2.778 |                3.483 |


Looking at the tables above, it is inefficient to use a sorted list with a fixed pivot table — especially as input size increases. This makes sense because selecting the first element of a sorted list is not a very efficient way to split it, and so the algorithm essentially goes one element at a time. 
While the runtimes above are comporable, using a randomized list or pivot value is evidently more efficient. 



- **1c.**

|   n |   qsort-fixed-pivot |   qsort-random-pivot |   tim_sort |
|-----|---------------------|----------------------|------------|
|   5 |               0.023 |                0.031 |      0.002 |
|  10 |               0.041 |                0.049 |      0.001 |
|  15 |               0.063 |                0.063 |      0.001 |
|  25 |               0.143 |                0.205 |      0.002 |
|  50 |               0.498 |                0.229 |      0.002 |
|  75 |               0.970 |                0.374 |      0.002 |
| 100 |               1.528 |                0.518 |      0.002 |
| 150 |               3.301 |                0.756 |      0.003 |
| 250 |               9.848 |                1.500 |      0.005 |
| 500 |              36.061 |                2.958 |      0.008 |


UNSORTED: 

|   n |   qsort-fixed-pivot |   qsort-random-pivot |   tim_sort |
|-----|---------------------|----------------------|------------|
|   5 |               0.023 |                0.021 |      0.002 |
|  10 |               0.038 |                0.039 |      0.001 |
|  15 |               0.048 |                0.066 |      0.001 |
|  25 |               0.137 |                0.136 |      0.003 |
|  50 |               0.195 |                0.261 |      0.005 |
|  75 |               0.352 |                0.352 |      0.008 |
| 100 |               0.416 |                0.525 |      0.010 |
| 150 |               0.596 |                0.771 |      0.070 |
| 250 |               1.187 |                1.272 |      0.028 |
| 500 |               2.592 |                2.979 |      0.051 |

Looking at the tables above, we can see that tim_sort is significantly faster than the other two implementation. It provides by far the best runtimes, regardless of whether it takes in a sorted or randomized list. 