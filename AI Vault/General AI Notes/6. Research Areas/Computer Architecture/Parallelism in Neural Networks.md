
different operations within a convolution can be assigned to diffrent cores of a procesor. You are dealing with so many data points that parallelism is actually a must.

The data pipeline in neural networks can allow you to run multiple batches through different layers at the same time. For example: While batch 1 is running in layer 3, batch 2 can be running in layer 2 on a different core and batch 3 can be running in layer 1 on a third core.

Yo can synchronize all of this. That is the base level idea behind data pipelining.

Data pipelining is a way to squeeze as much.

GPUs are so good at running neural networks because they have CUDA cores that will allow someone to run a ton of operations in parallel. Pipelining is the process of making the CUDA kernels run as efficiently as possible.

>![tip]The hardware that AI runs on is like the shovels in a gold rush. No matter who strikes gold, the person selling shovels is going to make money.





### The CUDA Core
CUDA cores have their own set of instructions: CUDA. CUDA is an assembly language much like RISC-V.

CUDA cores go inside of a streaming multiprocessor. Tensor units are like CUDA cores on steroids, but they're much more expensive.

These cores are NOT general purpose. They are literally just for doing massive parallel computations at once.

Since you have linux, you can just download the CUDA toolkit. It has it's own compiler, NVCC, and it is written in a form of C++. Languages like verilog are used only to program the *extremely* low level.

#### CUDA Tips:
Always pass a pointer from the starting address of your memory when working on data in CUDA.


