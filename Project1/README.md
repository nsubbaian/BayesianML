## Conjugate Priors. 

Code up 2 simulations. Simulation 1 you should generate Bernoulli random variables and estimate the probability p. Compare the ML estimate and an estimate made using conjugate priors. Use at least 2 different sets of parameters for the conjugate prior, one that is a "good" initial guess, and one that is a very bad initial guess.

The eqn for the ML estimate is 2.7 in your textbook. The update equations for the Beta conjugate prior are eqn 2.18.

Plot the mean squared error vs number of observations for the ML and Bayesian estimates. Put them all on one plot with a legend. For the Bayesian estimate, you should also plot the prior/posterior density. Do a 2x2 plot, in the upper left, show the initial density, bottom right show the final, the other 2 show the density at a couple steps along the way. If you are feeling fancy and free, you can easily make a movie showing the density as it changes per observation.

The second simulation, you should do the same thing, except for the Gaussian with unknown mean, known variance case. The ML estimate is eqn 2.143, and the conj prior update equations are 2.141 and 2.142. Plot the same things are you did for the Bernoulli.

If you are feeling especially brave and want a stretch goal, you can do this all one more time for a Gaussian with both unknown mean and variance. In this case you'll have a 2-D prior pdf, so you'll need to surface/mesh plot the posterior density, and you'd need to compute 2 MSEs. The corresponding conj prior is a normal gamma distribution, and the update equations are here (https://en.wikipedia.org/wiki/Normal-gamma_distribution)

Helpful link: https://towardsdatascience.com/conjugate-prior-explained-75957dc80bfb
