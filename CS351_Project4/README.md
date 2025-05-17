iotaGPUOutput
|Vector<br>Length|Wall Clock<br>Time|User Time|System Time|
|:--:|--:|--:|--:|
|10| 0.29| 0.00| 0.28|
|100| 0.21| 0.01| 0.20|
|1000| 0.21| 0.00| 0.20|
|10000| 0.21| 0.01| 0.19|
|100000| 0.20| 0.00| 0.19|
|1000000| 0.22| 0.01| 0.20|
|5000000| 0.24| 0.01| 0.22|
|100000000| 0.90| 0.20| 0.69|
|500000000| 3.45| 0.81| 2.63|
|1000000000| 6.26| 1.53| 4.72|
|5000000000|36.70| 7.90|28.80|

iotCPUOutput
|Vector<br>Length|Wall Clock<br>Time|User Time|System Time|
|:--:|--:|--:|--:|
|10| 0.00| 0.00| 0.00|
|100| 0.00| 0.00| 0.00|
|1000| 0.00| 0.00| 0.00|
|10000| 0.00| 0.00| 0.00|
|100000| 0.00| 0.00| 0.00|
|1000000| 0.00| 0.00| 0.00|
|5000000| 0.02| 0.00| 0.02|
|100000000| 0.51| 0.08| 0.43|
|500000000| 2.62| 0.42| 2.20|
|1000000000| 5.24| 0.85| 4.38|
|5000000000|35.00| 6.17|28.83|

I was expecting the GPU to run faster than the CPU, so it was surprising that in this
case the opposite actually happened. This may be because of the loop for the CPU rather
 than the gpu needing to copy the data from memory, and launching the kernel

![image](https://github.com/user-attachments/assets/cb8a51c9-210c-4180-8ee6-58fb08de726a)
