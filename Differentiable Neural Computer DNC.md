# DNC (2017)

Very interesting concept for using memory in a Neural Network. The model seems to be rather complex. The key ideas are as follows:

1. The CPU in this model is a neural net
2. It has a finite amount of memory 
3. The memory is addressed by content and not by address as in a conventional computer
4. Content is is matched using a [dot product](dot product.md)
5. The machine executes in series of time steps
6. At each time step it combines the input and a memory (vector) and apsses it to the neural network
7. The previous timestep provides the ke

[Differentiable neural computers | DeepMind](https://deepmind.com/blog/differentiable-neural-computers/)

