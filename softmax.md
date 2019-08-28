### Softmax


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
