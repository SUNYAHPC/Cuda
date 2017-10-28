##CUDA
#“Compute Unified Device Architecture”
General purpose programming model
- User kicks off batches of threads on the GPU
- GPU = dedicated super-threaded, massively data parallel co-processor Targeted software stack
- Compute oriented drivers, language, and tools Driver for loading computation programs into GPU
- Standalone Driver - Optimized for computation 
- Interface designed for compute - graphics free API
- Data sharing with OpenGL buffer objects 
- Guaranteed maximum download & readback speeds
- Explicit GPU memory management
##Parallel Computing on a GPU
-NVIDIA GPU Computing Architecture
-Via a separate HW interface 
-In laptops, desktops, workstations, servers

**8-series GPUs deliver 50 to 200 GFLOPS on compiled parallel C applications**
GPU parallelism is doubling every year Programming model scales transparently
Programmable in C with CUDA tools
Multithreaded SPMD model uses application  data parallelism and thread parallelism

program 1

__device__ float filter[N]; 

__global__ void convolve (float *image)  {

  __shared__ float region[M];
  ... 

  region[threadIdx] = image[i]; 

  __syncthreads()  
  ... 

  image[j] = result;
}

// Allocate GPU memory
void *myimage = cudaMalloc(bytes)


// 100 blocks, 10 threads per block
convolve<<<100, 10>>> (myimage);


