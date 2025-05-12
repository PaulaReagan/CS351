|Thread<br>Count|Wall Clock<br>Time|User Time|System Time|Speedup|
|:--:|--:|--:|--:|:--:|
|1|14.48|13.84| 0.45|1.00|
|2| 8.06|14.98| 0.54| 1.80|
|3| 5.45|14.78| 0.54| 2.66|
|4| 4.31|14.97| 0.72| 3.36|
|5| 3.72|15.61| 0.86| 3.89|
|6| 3.26|16.02| 0.94| 4.44|
|7| 2.94|16.22| 1.11| 4.93|
|8| 2.61|15.96| 1.21| 5.55|
|16| 1.94|18.02| 2.89| 7.46|
|24| 1.83|18.31| 7.25| 7.91|
|32| 1.77|18.27|14.47| 8.18|
|40| 1.75|17.63|24.74| 8.27|
|48| 1.85|17.15|30.96| 7.83|
|56| 1.81|16.83|39.43| 8.00|
|64| 1.81|16.89|45.39| 8.00|
|72| 1.83|16.93|47.21| 7.91|
|80| 1.89|17.05|38.01| 7.66|

Question 1: Max Speed-Up Factor
Yes using threads and speeding up can be better, but that doesn't mean
maxing speed in all circumstances since all threads share memory and cacche lines
so if there is over use of threads there may be no time spend doing useful computations 
in the meantime, there is no extra throughput, they are all using the
same data paths.

Question 2: Amdahl's Laws

I don't think you can get perfect sclaing, p would have to be equal to 1
which means that the entire program is parallleliable, althought we've
spoken on parallization before and that it isn't always ideal to have
the entire program parallizable, also I don't think everything can be
completely parallized and there are hardware limitations in some cases
the more cores that are added.

Question 3: Amdahl's Estimates

$$ serial = \frac{0.01007}{1.7966} = 0.00561 $$

$p$ = 0.9944

$$ speedup = \frac{1}{1 - 0.994 + \frac{0.994}{16}} = 1.989$$

$y=mx+b$ = 0.606x + 1.32
$m$ = 0.606

No the linear trend don't continue as you add more threads, there
is a plateau of the values and you cannot continue to infinitly harness
more, it makes sense that there are diminishing returned and some
sort of $"limit"$

Since p cant equal 1 to get a perfect 0 for 1-p, we will see values just
getting smaller and smaller, essentially flattening out, and that's where
the curve is happening because we have that limiting p value of 1
