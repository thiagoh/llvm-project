# Improved rpcalc

Improvement of the rpcalc

```
$ bison improved_rpcalc.y && g++ -lm improved_rpcalc.tab.c -o improved_rpcalc && ./improved_rpcalc

4 2 ^ 
4.000000 ^ 2.000000 -> 16
result -> 16

5 2 /
5.000000 / 2.000000 -> 2.5
result -> 2.5

321 2 * 2 ^ 333 /
321.000000 * 2.000000 -> 642
642.000000 ^ 2.000000 -> 412164
412164.000000 / 333.000000 -> 1237.72973
result -> 1237.72973

9 8 7 6 5 4 3 2 1 * * * * * * * *
2.000000 * 1.000000 -> 2
3.000000 * 2.000000 -> 6
4.000000 * 6.000000 -> 24
5.000000 * 24.000000 -> 120
6.000000 * 120.000000 -> 720
7.000000 * 720.000000 -> 5040
8.000000 * 5040.000000 -> 40320
9.000000 * 40320.000000 -> 362880
result -> 362880

6 5 4 3 2 1 * * * * * 2 ^ 64 /
2.000000 * 1.000000 -> 2
3.000000 * 2.000000 -> 6
4.000000 * 6.000000 -> 24
5.000000 * 24.000000 -> 120
6.000000 * 120.000000 -> 720
720.000000 ^ 2.000000 -> 518400
518400.000000 / 64.000000 -> 8100
result -> 8100

```