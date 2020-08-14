## the last mini project on sampling methods is as follows:

First part of the sampling methods project is to perform rejection sampling  to draw samples from a Gaussian mixture model. 
 
Use the same mixture model from the EM project, and I suggest using regular normal RV for the proposal distribution. Draw samples using this method and plot a histogram of the generated samples against your GMM.
 
 
Part two of the sampling methods mini-project is to re-do the first part of your linear regression project using MCMC to find an estimate for the weights.
 
Reuse your project 2 to generate the same training data. Just do this for 25 training samples
 
Use Equation 3.10 as the likelihood function, to be used with the training samples you generated. You may select any distribution you want for the prior on the weights, and recall that the posterior density on the weights w is proportional to the likelihood x prior
 
Use the Metropolis algorithm as defined in equation 11.33 to compute an estimate of the weights.
 
A few practical tips - you'll need to use the log of the posterior, i.e.  log (likelihood x prior) instead of the actual probabilities, due to numerical precision problems that will crop up with 25 training observations.
 
Remember to give the Markov chain a chance to 'burn in' and let it run for a few hundred samples or so before you start using those samples to compute an average on the weights.
 
The actual 'burn in' time is dependent on the proposal distribution you choose.
 
The proposal distribution you use can be different for each step of the algorithm - note this is different than in rejection sampling. A common choice is to recenter the proposal distribution on the previous stored sample.  See the bottom of page 541- top of 542 for a more detailed explanation of this.
 
Extra things you can do for fun:
 
-  Choose any old distribution for the prior on the weights. It should still work. No analytic solution required! This is one of the strengths of MCMC, it works when you can't find an analytic solution
 
- Add a completely useless feature to your dataset (like just make another column and put random data in it). Add a 3rd weight to your model. What does MCMC learn about the distribution of this weight?

- If you are really brave, take MCMC all the way to the finish line and do the second part of your linear regression project too, making predictions using the predictive posterior. This requires a nested run of MCMC, a good explanation of how it works is here. 

