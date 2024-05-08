Artificial intelligence is such a broad term at this point that it is hard to even know where to start. Everything from the NPCs in video games to the recommendations your search engine gives you fall under the umbrella of AI. You could essentially call AI a program that learns something and applies what it learns. As of 2024, there's a frenzy to make newer and smarter AI models. The field makes so much progress that it's hard for even some of my most brilliant professors to keep up with all of the new model types and techniques that 
## Types of AI
There are a ton of types of AI not listed here, but these types are what you'll mostly find within this notebook.
### Neural Networks
Neural networks are what most people think of when they think of AI, whether they know it or not.
You take information that you want to have AI analyze for you and [[Creating Robust Datasets|create a dataset]]. This could be anything from images to raw data. You select an architecture and parameters and train the model on your data and it will learn about it. After that, you test it with some examples that it has not seen before to make sure that it is on the right track. Then you deploy your model and have it make predictions about outcomes based on the previous data that you fed it.

Training an AI is at its core just a minimization problem. You select a [[Model Evaluation|metric to evaluate your model]] so you can understand how good it is, and a [[Cost & Loss Functions|loss function]] so that your AI can understand which direction it needs to go in order to get better at predictions.
### [[Reinforcement Learning Overview|Reinforcement Learning]]
Reinforcement learning is one of the most unique interesting forms of machine learning. This type of machine learning does not have a bunch of practical uses outside of creating NPCs in video games at the moment. The main difference between an NPC that uses AI and one that does not is that one learns and the other does not. A non-AI based NPC has it's behavior hard coded into it. Everything that it does has been explicitly designed by a programmer. Reinforcement learning creates an NPC, often referred to as an "agent", which learns its behavior from the environment. Usually the training process involves evolution. Multiple versions of the AI model are run at once. The best performing out of the batch are kept and slightly tweaked copies are made for the next generation.




