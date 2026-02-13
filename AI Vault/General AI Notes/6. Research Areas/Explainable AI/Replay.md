[Link](https://spectrum.ieee.org/catastrophic-forgetting-deep-learning)
Replay is the reactivation of one or more neural patterns, which are similar to the activation patterns seen during waking experiences.


## Types of Replay:

1. Experience Replay
	Experience replay is where an AI is fed examples that it had already gone over earlier in the dataset so that it will not forget them.
	
	**Advantages:**
	
	- Helps mitigate [[Catastrophic Forgetting]] by regularly exposing the model to past data.
	- Simple to implement and adapt to various continual learning scenarios.
	
	**Disadvantages:**
	
	- Requires additional memory to store past experiences, which can be a constraint in resource-limited settings.
	- Computational overhead due to periodic retraining on a mixed set of new and old data.
2. **Generative Replay (GR)**
    
    - **Description**: Instead of storing actual past experiences, a generative model (such as a GAN or a VAE) is trained to generate synthetic samples of past data. The generative model then generates pseudo-experiences for retraining the main model.
    - **Example**: Using a Variational Autoencoder (VAE) to generate samples that resemble past experiences and using these generated samples in the training process.
    - **Advantages**: Reduces the need for large memory buffers to store actual data. Can generate a potentially infinite variety of past experiences.
    - **Disadvantages**: Training and maintaining a high-quality generative model can be challenging and computationally intensive.
3. **Compressed Experience Replay (CER)**
    
    - **Description**: Combines aspects of experience replay and generative replay by storing compressed representations of past experiences rather than raw data. This can involve techniques like autoencoders to compress data before storage.
    - **Example**: Storing the latent space representations of experiences using an autoencoder and then decoding these representations during replay.
    - **Advantages**: More efficient use of memory compared to raw experience replay. Potentially faster retrieval and replay processes.
    - **Disadvantages**: Requires effective compression methods that retain essential information without significant loss.
4. **Cumulative Replay**
    
    - **Description**: All experiences are retained and replayed periodically. This method typically involves replaying a combination of new and all past experiences during each training session.
    - **Example**: Keeping a growing buffer that accumulates all experiences and sampling from this buffer during each training iteration.
    - **Advantages**: Ensures that all past knowledge is consistently reinforced.
    - **Disadvantages**: Memory and computational requirements grow over time, making it impractical for very long sequences of tasks.
5. **Prioritized Experience Replay (PER)**
    
    - **Description**: This variation of experience replay involves prioritizing certain experiences over others based on their importance, such as the prediction error or some measure of novelty.
    - **Example**: Sampling experiences that have high temporal-difference error more frequently in reinforcement learning tasks.
    - **Advantages**: Focuses on the most informative experiences, potentially improving learning efficiency.
    - **Disadvantages**: Requires a mechanism to prioritize and manage experiences, which adds complexity.