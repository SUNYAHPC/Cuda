##Thread Batching: Grids and Blocks
A kernel is executed as a grid of thread blocks
- All threads share data memory space


A thread block is a batch of threads that can cooperate with each other by:
- Synchronizing their execution
- For hazard-free shared memory accesses
- Efficiently sharing data through a low latency shared memory
- Two threads from two different blocks cannot cooperate

##Block and THreads
Threads and blocks have IDS
- So each thread can decide what data to work on
- Block ID: 1D or 2D
- Thread ID: 1D,2D or 3D
Simplifies memory addressing when processing multidimensional data.
- Image processing
- Solving PDEs on volumes.

##CUDA Device Memory Space Overview
Each Thread can
- R/w per thread registers
- R/W per thread local memory
- R/W per- block shared memor

- R/W per- grid global memory
- Read only per-grid constant memory
- Read only per-grid texture memory

The Host can R/W global,constant and texture memories

