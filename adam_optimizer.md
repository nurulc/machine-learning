## Javascript version of the adam optimizer

```Javascript
class Adam {
    constructor(nparams, beta_1=0.9, beta_2=0.999, epsilon=1e-8) {
        this.nparams= nparams;
        this.beta_1= beta_1;
        this.beta_2= beta_2;
        this.epsilon= epsilon;

        this.m= []; 
        this.v= [];
        for(var i= 0 ; i < this.nparams ; ++i) {
            this.m[i]= 0; // Initialize 1st moment vector
            this.v[i]= 0; // Initialize 2nd moment vector
        }
        this.t= 0; //Initialize timestep
        this.b1t = beta_1;
        this.b2t = beta_2;
    }
    get_update(alpha, g) { // alpha is the learning rate, g is the gradient
        this.t += 1;
        let updates= new Array(this.nparams);
        const {m,v,b,beta_1,beta_2, b1t, b2t, epsilon, nparams} = this;
         
        for(var i= 0 ; i < nparams ; ++i) {
            m[i]= beta_1*m[i] + (1-beta_1)*g[i]; // Update biased first moment estimate
            v[i]= beta_2*v[i] + (1-beta_2)*g[i]*g[i]; // Update biased second raw moment estimate
            var mub= m[i]/(1 - b1t); // Compute bias-corrected first moment estimate
            var vub= v[i]/(1 - b2t); // Compute bias-corrected second raw moment estimate
            updates[i]= - alpha * mub / ( Math.sqrt(vub) + epsilon  ); // Return parameter updates
        }
        this.b1t *= beta_1*beta_1;
        this.b2t *= beta_2*beta_2;
        return updates;
    };
}
```
