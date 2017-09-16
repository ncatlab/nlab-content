#Idea#

In the context of [[synthetic differential geometry]] a [[differential form]] $\omega$ of degree $k$ on a [[manifold]] $X$ is literally a function on the space of _infinitesimal cubes_ or _infinitesimal simplices_ in $X$.

We give the definition as availalable in the literature and then interpret this in a more unified way in terms of [[(infinity,1)-quantity|(∞,1)-quantities]].

# Definition #

## differential forms ##

An **infinitesimal $k$-simplex** in a synthetic differential space $X$ is a collection of $k+1$-points in $X$ that are pairwise infinitesimal neighbours.

The functions on the space of infinitesimal $k$-simplices form a [[generalized smooth algebra]] $C^\infty(X^{\Delta^k_{inf}})$.

A **differential $k$-form** on $X$ is an element in this function algebra that has the property that it vanishes on degenerate infinitesimal simplices.

See definition 3.1.1 in 

* Anders Kock, _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-kopi.pdf))

for this simplicial definition. See the following definitions for the cubical variants and their interrelation.

See also section 4.1 of

* Moerdijk-Reyes,  [[Models for Smooth Infinitesimal Analysis]]

for the cubical version.

We observe here that we may characterize this object $\Omega^k(X) \subset C^\infty(X^{\Delta^k_{inf}})$ as follows:

for $k \geq 1$ there are the obvious images 

$$
  s_i^*
  :
  C^\infty(X^{\Delta^{k}_{inf}})
  \to 
  C^\infty(X^{\Delta^{k-1}_{inf}}) 
$$

of the [[simplicial set|degeneracy maps]]. As one can see, these act by restricting a function on infinitesimal $k$-simplices to the degenerate ones and regarding these then as a $(k-1)$-simplex.

Therefore we may characterize the subobject $\Omega^k(X) \hookrightarrow C^\infty(X^{\Delta^k_{inf}})$ as the joint kernel of the degeneracy maps
$$ 
  \Omega^k(X) = \cap_{i = 0}^{k-1} ker(s_i^*)
  \,.
$$

## coboundary operator ##

According to section 3.2 of Andres Kock's book, the coboundary operator $d : \Omega^k(X) \to \Omega^{k+1}(X)$ sends a differential $k$-form $\omega$ to the $(k+1)$-form $d \omega$  that on an infinitesimal $(k+1)$-simplex $(x_0, x_1, \cdots, x_{k+1})$ in $X$ evaluates to

$$
  d\omega(x_0, x_1, \cdots, x_{k+1})
  :=
  \sum_{i=0^{k+1}}
  \omega(x_1, \cdots , \hat{x_i}, \cdots, x_{k+1})
  \,,
$$

where the hat indicates that the corresponding variable is omitted, as usual.

We recognize this as the alternating sum of the [[simplicial identities|face maps]] 
$\partial_i^*$
of the [[simplicial object|cosimplicial object]] $C^\infty(X^{\Delta_{inf}^\bullet})$.

$$
  d := \sum_{i=0}^{k+1} \partial_i^* : 
  \Omega^k(X) \to \Omega^{k+1}(X)
  \,.
$$

These constructions remind one and should be compared with the [[Dold-Kan correspondence]]. In particular with its _dual_ (cosimplicial) version as recalled in section 4 of [CastiglioniCortinas](http://arxiv.org/PS_cache/math/pdf/0306/0306289v3.pdf)

In total this should show the following

+-- {: .un_prop}
###### Proposition

Let $X$ be a synthetic differential space and $C^\infty(X^{\Delta_{inf}^\bullet})$ the [[simplicial object|cosimplicial object]] of [[generalized smooth algebra]]s of functions on the spaces of infinitesimal $k$-simplices in $X$.

Then the deRham complex $(\Omega^\bullet(X), d)$ of differential forms on $X$ is the normalized [[Moore complex]] of the cosimplicial object $C^\infty(X^{\Delta_{inf}^\bullet})$.
=--

In other words, in as far as the Dold-Kan correspondence is an equivalence, we find that:

the object of differential forms on $X$ _is_ the cosimplicial [[generalized smooth algebra]] $C^\infty(X^{\Delta_{inf}^k})$.



# References #

* Anders Kock, _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-kopi.pdf))

* Moerdijk-Reyes,  [[Models for Smooth Infinitesimal Analysis]]

* Castiglioni, Cortinas, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0306/0306289v3.pdf))