### Softmax

Observation x is a vector of logits and most of the values are greater than 1 then softmax gives a kind of pseudo probablilty that give a high probability to the largest value. It works very badly if all the values of x are less than 1.

let x = [2, 6, 1, 4, 3]








### Exp-normalize trick

Noting that exp(a+b)  = exp(a)exp(b)  


```
SoftMax(x)  = exp(x[i]) / Sum(exp(x))

SoftMax(x) = exp(x[i]-b)*exp(b) / Sum(exp(x-b)*exp(b))
           = exp(x[i]-b)/Sum(exp(x-b)) where b is max x
           
           log π[i] =x[i]−logsumexp(x)
           logsumexp(x)=b+log ∑ exp(x[j]−b)
 ```
 
 Exp-normalize is the gradient of log-sum-exp.
