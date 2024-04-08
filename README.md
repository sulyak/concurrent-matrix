# Concurrent matrix operations
This program uses pthreads to do matrix computations in paralell.

# Running
Compile with `gcc -o main main.c` and run `./main`

# What it does
it reads a list of files from `entrada.in`, each file contains two 10x10 matrix.


Program flow:
P -> CP1 -> CP2 -> CP3 -> C.

Where `P` is a producer, `CPX` are consumer-produces and `C` is a consumer.

`P` reads the matrix files.
`CP1` performs a matrix multiplication from the two original matrixes.
`CP2` calculates the sum of the columns from the previous matrix.
`CP3` calculates the sum of the previous values. 
`C` stores the results of previous operations to the file `saida.out`

