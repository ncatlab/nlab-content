#Idea#

Recall that ( _geometric_ ) [[T-duality]] is an operation acting on tuples consisting of

* a manifold $X$
  : with the structure of a principal torus bundle $T^n \to X \to X/T^n$
* equipped with a gerbe 
  : with connection
* and possibly with elements in twisted K-theory
  : refined to elements in differential twisted K-theory
* and notably equipped with
  : a (pseudo)Riemannian metric.

The idea of **topological T-duality** is to disregard the Riemannian metric. 

While the idea of [[T-duality]] originates in [[string theory]], topological T-duality has become a field of study in pure mathematics in its own right. Its formalization originates in _BunkeSchick05_ and _BunkeRumpfSchick08_

In the language of [[bi-brane]]s a topological T-duality transformation is a bi-brane of a special kind between the two gerbes involved. The induced pull-push operation (in [[groupoidification]] and [[geometric function theory]]) on (sheaves of sections of, or K-classes of) (twisted) vector bundles is essentially the Fourier-Mukai transformation. More on the bi-brane interpretation of (topological and non-topological) T-duality is in _SarkissianSchweigert08_.


#Definition#

Two tuples $(X_i \to B, G_i)_{i = 1,2}$ consisting of a $T^n$-bundle $X_i$ over a manifold $B$ and a line bundle gerbe $G_i \to X_i$ over $X$ are **topological T-duals** if there exists an isomorphism $u$ of the two line bundle gerbes pulled back to the [[pullback|fiber product]] correspondence space $X_1 \times_B X_2$:

$$
  \array{
    && pr_1^* G_1 && \stackrel{u}{\leftarrow}
    && pr_2^* G_2
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    G_1 &&&& X_1 \times_B X_2 &&&& G_2
    \\
    & \searrow && \swarrow && \searrow && \swarrow
    \\
    && X_1 &&&& X_2
    \\
    &&& \searrow &&& \swarrow
    \\
    &&&& B
  }
$$

of a certain prescribed form (see [p. 9](http://arxiv.org/PS_cache/math/pdf/0501/0501487v5.pdf#page=9)) of _BunkeRumpfSchick08_.


#References#

* **BunkeSchick05** U. Bunke and T. Schick, _On the topology of T-duality_ ([pdf](http://www.uni-math.gwdg.de/schick/publ/totduali.pdf))

* **BunkeRumpfSchick08** U. Bunke, P. Rumpf and T. Schick, _The topology of $T$-duality for $T^n$-bundles_ ([arXiv](http://arxiv.org/abs/math.GT/0501487))

There is a [[C*-algebra]]ic version of toplogical T-duality, discussed for instance at

* V. Mathai & J. Rosenberg, _T-Duality for Torus Bundles with H-Fluxes via Noncommutative Topology_ ([arXiv](http://arxiv.org/abs/hep-th/0401168))

The [[bi-brane]] perspective on T-duality is amplified in

* G. Sarkissian and C. Schweigert, _Some remarks on defects and duality_ ([arXiv](http://arxiv.org/abs/0810.3159))

#Blog resources#

A transcript a a talk by Varghese Mathai on topological T-duality is here:

* _Mathai on T-duality_:

  * I: [Overview](http://golem.ph.utexas.edu/string/archives/000827.html)

  * II: [T-dual K-classes by Fourier-Mukai](http://golem.ph.utexas.edu/string/archives/000828.html).

Remarks on the relation to higher linear maps are at

* U. Schreiber, _Fourier-Mukai, T-Duality and other linear 2-Maps_ ([blog](http://golem.ph.utexas.edu/string/archives/000825.html))

The interpretation in terms of pull-push of sections of differential cocycles appears at

* U. Schreiber, _QFT of Charged n-Particle: T-Duality_ ([blog](QFT of Charged n-Particle: T-Duality))