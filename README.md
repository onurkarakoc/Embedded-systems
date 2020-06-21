# Embedded-systems

* Assn1: In this assignment, you are required to run a set of experiments and analyze the results in order to understand the cache behavior of programs, how different cache designs affect program execution, how a program can be tuned for a specific cache configuration.
You will use the cache simulator (allcache) provided in Pin tool [1] to collect cache miss rates. You need to compile and run the matrix multiplication code provided as part of this assignment, then you will run the program by using the simulator as discussed in the lab session (or you can learn from the Pin user guide: https://software.intel.com/sites/landingpage/pintool/docs/97619/Pin/html )
You will run the matrix multiplication program for a set of configurations with the following L1 cache parameters in the cache simulator:
  L1 Size
16
16
16
32
64
16
16
Block size
16
16
16
16
16
32
8
L1 Associativity
1
2
4
1
1
1
1

* Assn3: In this assignment, you are required to run a set of experiments and analyze the results in order to understand the effect of the compiler optimizations and how a program can be tuned for performance optimization.
First, you will compile the matrix multiplication code provided as part of this assignment by using gcc compiler (https://gcc.gnu.org/). In this part, you will change the optimization levels (https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html) provided by gcc, which are -O0, -O1, -O2, -O3, -Ofast.
Second, you will modify the code and explore the possible performance optimizations other than the compiler provides including:
Eliminate function call: Instead of having the function “muld”, place the code inside this function into the line it is called.
Accumulate in temporary: Instead of storing the intermediate results in res[i][j] (stored in memory), define a temporary variable (stored in register) and accumulate the values in this variable, then update the array element at the end of the loop.
Loop unrolling: Unroll the inner loop (with index k) by 2 times.
