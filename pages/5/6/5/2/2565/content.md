Information geometry aims to apply the techniques of [[differential geometry]] to statistics. Often it is useful to think of a family of probability distributions as a _statistical_ [[manifold]]. For example, normal distributions form a 2-dimensional manifold, parameterised by $(\mu, \sigma)$, mean and standard deviation. On such manifolds there are notions of [[Riemannian metric]], [[connection]], [[curvature]], and so on, of statistical relevance.

One of the founders of the subject is Shun-ichi [Amari](http://www.brain.riken.jp/labs/mns/amari/home-E.html).

##Resources##

*  Shun-ichi Amari, MaxEnt 2007 [lecture](http://video.google.com/videoplay?docid=2175767568645553282#)
*  Shun-ichi Amari, ETVC08 [lecture](http://videolectures.net/etvc08_amari_igaia/).
*  Shun-ichi Amari, Hiroshi Nagaoka, _Methods of information geometry_, Transactions of mathematical monographs; v. 191, American Mathematical Society, 2000. 
*  Sanjoy Dasgupta, [lecture](http://videolectures.net/mlss05us_dasgupta_ig/).
*  Blog [post](http://golem.ph.utexas.edu/category/2006/11/infinitedimensional_exponentia.html).

##Discussion##

[[Tim Porter]]: I have looked briefly at the Methods of Info Geom book and it seemed to me to be distantly related to what the eminent statistician David Kendall used to do.  He and some coauthors wrote a very nice book called: Shape and Shape Theory (nothing to do with Borsuk's Shape Theory). The theory may be of relevance as it used differential geometric techniques.  (Incidently there are some nice questions concerning the space of configurations of various types that would be a good source for student project work in it.) 

My query is whether the link is a strong one between the Amari stuff and those Kendall Shape space calculations.  Kendall's theory and some similar work by Bookstein is widely used in identifcation algorithms using a feature space. In case the link is only faint I will leave it at that for the moment.  Any thoughts anyone?

***

[[Eric]]: This comment is separate from Tim's so I separate it with a line...

**The following material is speculative**

There is another concept that deserves to be called something like **information geometry**, but seems distinct to me. Any relations would be interesting to dig out. 

The idea is to note that random processes form a vector space. For instance, given random processes $X_i$, the linear combination

$$X = \sum_i \omega_i X_i$$

is also a random process. If the random process is a "[stable](http://en.wikipedia.org/wiki/Stable_distribution)" process, then things are even nicer. The special case of Gaussian distributions are particularly nice because everything you can know about them is encoded in the two parameters $\mu$ (mean of the process) and $\sigma$ (standard deviation of the process).

Each of the differentials may be expressed as

$$dX_i = \mu_i dt + \sigma_i dW_i$$

where $dW_i$ is a standard Brownian motion with $\mu = 0$ and $\sigma = 1$.

We can interpret the $dW_i$ as spanning a cotangent space of some kind of stochastic manifold (I'm not using that term in any kind of standard way, so name clashes are likely).

If you have $N$ such processes, the dimension of the space they span depends on the rank of the covariance matrix

$$\Sigma_{i,j} = \cov(dW_i,dW_j).$$

The matrix $\Sigma$ is symmetric and positive semi-definite. However, if the rank of $\Sigma$ is $n$, we can find $n$ uncorrelated differentials $de_i$ and construct a covariance matrix

$$g_{i,j} = \cov(de_i,de_j) = \delta_{i,j}.$$

This matrix is symmetric and positive definite. Therefore, on the space spanned by the $de_i$, we can think of the covariance matrix $g$ as a **metric tensor**.

Now, we can re-express any Gaussian process via

$$X_i = \mu_i dt + \sum_j \sigma_{i,j} de_j.$$

Comparing this with the previous expression we see that

$$\sigma_i dW_i = \sum_j \sigma_{i,j} de_j.$$

Furthermore,

$$\sigma^2_i = \sum_j \sigma^2_{i,j}$$

which is just the familiar expression for the variance of the sum of uncorrelated processes.

The neat thing comes when you bring $dt$ back into the picture.

Since we can interpret the covariance matrix $g$ as a metric tensor on a **space**, we can extend this to a Lorentzian metric on spacetime by specifying

$$g_{t,i} = g(dt,de_i) = 0$$

and

$$g_{t,t} = g(dt,dt) = -1.$$

With this extension of the metric, we have

$$|X_i|^2 = g(X_i,X_i) = \sigma^2_i - \mu^2_i.$$

Therefore at each point of our manifold, we have a light cone with a velocity-like value given by

$$c_i = \frac{\mu_i}{\sigma_i}.$$

This is a Minkowski version of something that could be called **information geometry** but is different than that described above.

Each process $X_i$ defines a point of our manifold and $\mu_i,\sigma_i$ defines a light cone at that point.

If you have two processes $X_i$ and $X_0$, we can also look at their difference 

$$\bar{X}_i = X_i - X_0.$$

Then

$$d\bar{X}_i = (\mu_i-\mu_0) dt + \bar{\sigma}_i d\bar{W}_i.$$

The relative light-cone is then

$$\bar{c}_i = \frac{\mu_i-\mu_0}{\bar{\sigma}_i}.$$

Now, this applies to finance by letting $X_i$ be the log of the price of some security and letting $X_0$ be the log of the price of some benchmark. With this financial interpretation, the $dX_i$ is the **return** of the security and $d\bar{X}_i$ is the **excess return**.

The light cone at the security $X_i$ is known as the **Sharpe ratio** and the light cone at the relative security $\bar{X}_i$ is known as the **information ratio**.

To further the analogy, you could define an absolute light cone for which all other light cones are compared. This absolute light cone is closely related to a **risk aversion**.

Aside from the application to finance (which might not be of much interest to the nLab), I think the analogy between mean-variance space and Minkowski space is interesting. The relation to tradition **information geometry** is not 100% clear, but it is not totally unrelated either.