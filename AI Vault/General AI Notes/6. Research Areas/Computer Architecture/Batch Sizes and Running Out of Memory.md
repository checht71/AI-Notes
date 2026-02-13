You only have a certain amount of cores in your GPU. Multiple GPUS can be connected via NVLink.

When you are doing your calculations, all of the intermediates from each convolution, each neuron, each weight and each activation function output must be stored somewhere.

If you have a very large batch size, your memory is going to be filled up really quick, since you have to store all of this information. When you run out of memory, there is nowhere to store the intermediate results. Lowering the batch size also lowers the size of the information that needs to be stored.

Check out memory hierarchy.

When you run a neural network on a CPU, you have a cache and RAM. The CPU will offload all of the intermediates into the RAM.

[[Batch Sizes|More on batch sizes]]
