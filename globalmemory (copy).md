##CUDA API
CUDA Highlights: Easy and Lightweight
The API is an extension to the ANSI C programming language
- Low learning curve
The hardware is designed to enable lightweight runtime and driver
- High performance
##A Small Detour: A Matrix Data Type
- Not part of CUDA
- it will be frequently used in many examples
- 2D matrix
- single precision float elemnets
- width * height elements
- Pitch meaningful when the matrix is actually a sub-matrix of another matrix
- data elements allocated and attached to elements
##CUDA Device Memory Allocation
cudaMalloc()
- Allocates object in the device Global memory
- Requires two paramenters
- Address of a pointer to the Allocated object.
- Size of allocated object
cudaFree()
- Frees object from device Global memory
- pointer to freed object.
-Allocate a 64* =64 single precision float array
- Attach the allocated storage to Md.elements.
- "d" is often ued to indicate a device data structure.
BLOCK_SIZE = 64;
Matrix Md
int size = BLOCK_SIZE * BLOCK_SIZE * sizeof(float);

cudaMalloc((void**)&Md.elements, size);
cudaFree(Md.elements);
##CUDA HOST- Device data Transfer
cudaMemcpy()

-memory data transfer
-Requires four parameters
  Pointer to source 
  Pointer to destination
  Number of bytes copied
  Type of transfer 
   -Host to Host
   -Host to Device
   -Device to Host
   -Device to Device
Asynchronous in CUDA 1.0

