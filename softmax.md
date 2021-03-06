### Softmax

Observation x is a vector of logits and most of the values are greater than 1 then softmax gives a kind of pseudo probablilty that give a high probability to the largest value. It works very badly if all the values of x are less than 1.

### let x = \[2, 6, 1, 4, 3]

#### Simple Prob<sub>i</sub> = x<sub>i</sub> / sum(x)

#### &nbsp;softmax(__x__) = \[&pi;<sub>1</sub>, &pi;<sub>2</sub>, ... &pi;<sub>n</sub>\] 

where ![](softmax-def.png)

![](softmax.png)
Notice how softmax pushes up the max value and supresses the lesser values.

#### Now if we scales x / 10  giving \[0.2, 0.6, 0.1, 0.4, 0.3]

The relative sizes of the vales have not changes so the simple probability remanins the same, but look how the changes the softmax  values; now softmax is largely useless.

![](softmax-small-values.png)



### Exp-normalize trick


The exp function overflows very easily even for relatively small integers say 500, but we can use the following property of the exponential to overcome this issue.

Noting that _exp(a+b)  = exp(a)exp(b)_  



SoftMax(__x__)  = exp(x<sub>i</sub>) / &sum; exp(__x__)

SoftMax(__x__) = exp(x<sub>i</sub>-b)*exp(b) / &sum;(exp(__x__-b)*exp(b))<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= exp(x<sub>i</sub>-b) / &sum;(exp(x-b))<br> &nbsp;&nbsp;&nbsp;where b is max __x__
           
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;log &pi;<sub>i</sub> = x<sub>i</sub> − logsumexp(__x__)<br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;logsumexp(__x__)=b+log &sum; exp(x<sub>i</sub>−b)

 
 Exp-normalize is the gradient of log-sum-exp.




Γ Δ Θ Λ Ξ Π Σ Φ Ψ Ω
α β γ δ ε ζ η θ ι κ λ μ
ν ξ π ρ ς σ τ υ φ χ ψ ω
ϐ ϑ ϒ ϕ ϖ Ϛ Ϟ Ϡ ϰ ϱ ϲ
