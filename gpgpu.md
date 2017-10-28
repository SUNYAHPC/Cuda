##What is GPGPU
General Purpose computation using GPU in applications other than 3D graphics
 -GPU accelerates critical path of application 
Data parallel algorithms leverage GPU attributes
- Large data arrays, streaming throughput
- Fine-grain SIMD parallelism 
- Low-latency floating point (FP) computation 

Applications – see //GPGPU.org 
- Game effects (FX) physics, image processing 
- Physical modeling, computational engineering, matrix algebra,convolution, correlation, sorting.

##Previous GPGPU Constraints

Dealing with graphics API
- Working with the corner cases of the graphics API

Addressing modes
- Limited texture size/dimension

Shader capabilities
- Limited outputs

Instruction sets
-Lacks of Integer & bit ops

Communication limited
-Between pixels
- Scatter a[i]=p


