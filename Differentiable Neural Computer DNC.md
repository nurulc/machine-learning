# DNC (2017)

Very interesting concept for using memory in a Neural Network. The model seems to be rather complex. The key ideas are as follows:

1. The CPU in this model is a neural net
2. It has a finite amount of memory 
3. The memory is addressed by content and not by address as in a conventional computer
4. Content is is matched using a [dot product](dot%20product.md)
5. The machine executes in series of time steps
6. At each time step it combines the input and a memory (vector) and psses it to the neural network
7. The previous timestep provides the key to find the next element
8. All operations are completely differentiable, so gradient descent can be used to update all aspects of the machine
    1. Where to fetch
    2. Where to store
    3. Generate next output


* [Differentiable neural computers | DeepMind](https://deepmind.com/blog/differentiable-neural-computers/)
* [DNC | Nature](https://www.nature.com/articles/nature19477)
* [DNC | Shiraj | Youtube](https://www.youtube.com/watch?v=r5XKzjTFCZQ)
* [The Future of Deep Learning Research | Youtube]( https://www.youtube.com/watch?v=WTnxE0wjZaM)
* [Improved DNC](http://papers.nips.cc/paper/6298-scaling-memory-augmented-neural-networks-with-sparse-reads-and-writes.pdf) - A bit difficult to read
