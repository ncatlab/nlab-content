
# Persistent homology
* table of contents
{: toc}

##Idea 

Persistent homology is a [[homology theory]] adapted to a [[computation|computational]] context. It keeps track of homology classes which stay 'persistent' when the approximate image of a space gets refined to higher resolutions.  


## More detail

We suppose given a 'data cloud of samples', $P\subset \mathbb{R}^m$, from some space $X$, yielding a [[simplicial complex]] $S_\rho(X)$ for each $\rho \gt 0$ via one of the family of simplicial complex approximation methods that are listed below (TO BE ADDED).  For these, the important idea to retain is that if $\rho \lt \rho^\prime$, then 

$$S_\rho(X) \hookrightarrow S_{\rho^\prime}(X),$$

so we get a 'filtration structure' on the complex.

The idea of *persistent homology* is to look for features that persist for some range of parameter values.  Typically a feature, such as a hole, will initially not be observed, then will appear, and after a range of values of the parameter it will disappear again. A typical feature will be a [[Betti number]] of the complex, $S_\rho(X)$, which then will vary with the parameter $\rho$.


## Talks

* [[ACT-OIT.pdf|Slides:file]] for a talk by [[Tim Porter]] in 2008.


## References

* Robert MacPherson, Benjamin Schweinhart, _Measuring shape with topology_, J. Math. Phys. __53__, 073516 (2012); [doi](http://dx.doi.org/10.1063/1.4737391)
* A. Zomorodian, G. Carlsson, _Computing persistent homology_, Discrete Comput. Geom. __33__, 249&#8211;274 (2005)
* Ulrich Bauer, Michael Kerber, Jan Reininghaus, _Clear and compress: computing persistent homology in chunks_, [arxiv/1303.0477](http://arxiv.org/abs/1303.0477)
* Robert J. Adler, Omer Bobrowski, Matthew S. Borman, Eliran Subag, Shmuel Weinberger, _Persistent homology for random fields and complexes_ Institute of Mathematical Statistics Collections __6__:124&#8211;143, 2010 [arxiv/1003.1001](http://arxiv.org/abs/1003.1001)
* Robert J. Adler, Omer Bobrowski, Shmuel Weinberger, _Crackle: the persistent homology of noise_, [arxiv/1301.1466](http://arxiv.org/abs/1301.1466)
* Pawe&#322; D&#322;otko, Hubert Wagner, _Computing homology and persistent homology using iterated Morse decomposition_, [arxiv/1210.1429](http://arxiv.org/abs/1210.1429)


category: topology

[[!redirects persistent homology]]
[[!redirects persistent homology theory]]
