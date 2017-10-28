##CUDA Programming Model: A Highly Multithreaded Coprocessor
The GPU is viewd as a compute device
- is a coprocessor to the CPU or HOST
- Has its own DRAM(device memory)
- Runs many threads in parallel

Data parallel portions of an application are executed on the device as kernel which run in parallel on many threads.

Difference between GPU and CPU threads
- GPU threads are extremely lightweight
  * very little creation overhead
- GPU needs 1000s of threads for full efficiency
  * multi core COU  needs only a few




