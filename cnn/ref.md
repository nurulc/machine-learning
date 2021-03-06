# CNN

A Convolutional neural netwoks ar often used for image processing.

* Typical CNN
![](../images/Typical_cnn.png)

### Subsampling
Is a method of reducing the size of and image or feature map to make further processing easier. The trick is to capture the salient data into the reduced map.

Example - [max pooling](https://computersciencewiki.org/index.php/Max-pooling_/_Pooling) involves fplitting the data into patches taking the maximum from each patch to give a subsampled result.

## Advantages

* High parallelization [see discussion here](https://medium.com/@esaliya/model-parallelism-in-deep-learning-is-not-what-you-think-94d2f81e82ed),[another article on parallism](https://www.groundai.com/project/efficient-and-robust-parallel-dnn-training-through-model-parallelism-on-multi-gpu-platform/), and [another on memory efficiency](https://medium.com/@SeoJaeDuk/archived-post-optimizing-memory-efficiency-for-deep-convolutional-neural-network-accelerators-86643bb79f36)
* [Lower memory bandwidth](https://medium.com/@culurciello/computation-and-memory-bandwidth-in-deep-neural-networks-16cbac63ebd5)
