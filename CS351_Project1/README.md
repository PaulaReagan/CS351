
|Hash #|Optimization|Real Time|User Time|System Time|Memory Usage<br>(KB)|Throughput|Performance<br>Improvement|
|:--:|--:|--:|--:|--:|--:|--:|:--:|
|   hash-00 |       -g          |       356.84  |       342.70  |       10.16   |       2880        |       0.045   |   1.00    |
|   hash-01 |       -g          |       21.79   |       16.52   |       2.38    |       2880        |       0.734   |   16.23   |
|   hash-02 |       -g          |       16.02   |       14.31   |       1.26    |       2892        |       1.00    |   22.27   |
|   hash-03 |       -g          |       16.46   |       15.06   |       1.28    |       2880        |       0.973   |   21.68   |
|   hash-04 |       -g          |       14.37   |       13.74   |       0.46    |       5012360     |       1.11    |   24.84   |
|           |                   |               |               |               |                   |               |           |
|   hash-00 |       -O2         |       342.32  |       330.24  |       7.86    |       2880        |       0.047   |   1.00    |
|   hash-01 |       -O2         |       8.37    |       6.93    |       1.07    |       2880        |       1.91    |   40.88   |   
|   hash-02 |       -O2         |       7.97    |       6.83    |       1.05    |       2880        |       2.01    |   42.92   |
|   hash-03 |       -O2         |       8.08    |       6.82    |       1.13    |       2880        |       1.98    |   42.37   |
|   hash-04 |       -O2         |       7.34    |       6.64    |       1.50    |       5012352     |       2.18    |   46.64   |
|           |                   |               |               |               |                   |               |           |
|   hash-00 | -O2 -funroll-loops|       347.42  |       333.78  |       6.06    |       2880        |       0.0046  |   1.0     |
|   hash-01 | -O2 -funroll-loops|       8.26    |       6.83    |       1.34    |       2304        |       1.937   |   42.051  |
|   hash-O2 | -O2 -funroll-loops|       8.18    |       6.77    |       1.31    |       3456        |       1.956   |   42.472  |
|   hash-03 | -O2 -funroll-loops|       8.29    |       6.82    |       1.31    |       2880        |       1.93    |   41.908  |
|   hash-04 | -O2 -funroll-loops|       7.12    |       6.46    |       0.57    |       5011776     |       2.247   |   48.79   |



Question 1:
The operations that account for most of the hash-00 runtime is the time to read the file each time and computing hash functions for each block
Question 2:
The time difference between the allocation methods are about the same speed so there is not much difference between them.
Question 3:
The difference between for hash-03 is also about the same and has not much difference
Question 4:
Because of mmap the file pages are a part of address space 
Question 5:
Because of mmap the file pages are a part of address space 
