
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

Let $G$ be a [[compact Lie group]] and write $L G$ for its _[[loop group]]_. See there for details and notation.

Write 

$$
  t_\theta \colon L G \to L G
$$

for the [[automorphism]] which rotates loops by an [[angle]] $\theta$. 

The corresponding [[semidirect product group]] we write $L G \rtimes S^1$

+-- {: .num_defn }
###### Definition

Let $V$ be a [[topological vector space]]. A linear representation

$$
  S^1 \to Aut(V)
$$

of the [[circle group]] is called **positive** if $\exp(i \theta)$ acts by $\exp(i A \theta)$ where $A \in End(V)$ is a [[linear operator]] with positive [[spectrum of an operator|spectrum]].

A linear [[representation]] 

$$
  \rho : L G \to Aut(V)
$$

is said to have **positive energy** or to be a **positive energy representation** if it extends to a representation of the [[semidirect product group]] $L G \rtimes S^1$ such that the restriction to $S^1$ is positive.

=--


## Properties

### Relation to quantum group representations

See [this MO discussion](http://mathoverflow.net/q/178113/381).

## Related concepts

* [[quantization of loop groups]]

* [[conformal block]]

* [[equivariant elliptic cohomology]]

* [[twisted ad-equivariant K-theory]]

* [[twisted ad-equivariant Tate K-theory]]

* [[Loop Groups and Twisted K-Theory]]


## References

### General

The standard textbook on loop groups is

* Andrew Pressley, [[Graeme Segal]], _Loop groups_ Oxford University Press (1988)
  {#PressleySegal}

A review talk is 

* [[Graeme Segal]], _Loop groups_ ([pdf](http://people.mpim-bonn.mpg.de/zagier/files/doi/10.1007/BFb0084581/chapter08.pdf))
 {#Segal}

Discussion in the context of [[string theory]] (the [[Witten genus]]) is in 

* [[Kefeng Liu]], section 2.2 of _On modular invariance and rigidity theorems_, J. Differential Geom. Volume 41, Number 2 (1995), 247-514 ([EUCLID](http://projecteuclid.org/euclid.jdg/1214456221), [pdf](http://www.math.ucla.edu/~liu/Research/loja.pdf))

### Relation to ad-equivariant K-theory

On [[twisted ad-equivariant K-theory]] of [[compact Lie groups]] and the identification with the [[Verlinde ring]] of [[positive energy representations]] of their [[loop group]]:

* [[Daniel S. Freed]], _The Verlinde algebra is twisted equivariant K-theory_, Turk. J. Math 25 (2001) 159-167 ([arXiv:math/0101038](https://arxiv.org/abs/math/0101038))


{#FHT}
* [[Daniel S. Freed]], [[Michael Hopkins]], [[Constantin Teleman]],  

  1. _[[Loop Groups and Twisted K-Theory]] I_, 

     J. Topology, 4 (2011), 737-789  
   
     ([arXiv:0711.1906](http://arxiv.org/abs/0711.1906), [doi:10.1112/jtopol/jtr019](https://doi.org/10.1112/jtopol/jtr019))

  1. _[[Loop Groups and Twisted K-Theory]] II_, 

     J. Amer. Math. Soc. 26 (2013), 595-644  

     ([arXiv:0511232](http://arxiv.org/abs/math/0511232), [doi:10.1090/S0894-0347-2013-00761-4](https://doi.org/10.1090/S0894-0347-2013-00761-4))

  1. _[[Loop Groups and Twisted K-Theory]] III_, 

     Annals of Mathematics, Volume 174 (2011) 947-1007 

     ([arXiv:math/0312155](http://arxiv.org/abs/math/0312155), [doi:10.4007/annals.2011.174.2.5](http://dx.doi.org/10.4007/annals.2011.174.2.5))

* [[Daniel S. Freed]], [[Constantin Teleman]], 

  _Dirac families for loop groups as matrix factorizations_, 

  Comptes Rendus Mathematique, Volume 353, Issue 5, May 2015, Pages 415-419

  ([arxiv/1409.6051](http://arxiv.org/abs/1409.6051), [doi:10.1016/j.crma.2015.02.011](https://doi.org/10.1016/j.crma.2015.02.011))



[[!redirects positive energy representation]]
[[!redirects positive energy representations]]
