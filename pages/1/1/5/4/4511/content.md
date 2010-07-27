
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In the context of [[homological algebra]], the _$Tor$-functor_ is the left [[derived functor]] of the [[tensor product]].

Together with the [[Ext-functor]] it constitutes one of the central operations of interest in homological algebra.

## Details


Given a ring $R$ the bifunctor $\otimes_R : Mod_{R}\times _{R}Mod\to Ab$ is right exact. Its left [[derived functor]]s $Tor(-,B)$ and $Tor(A,-)$ with respect to one argument with fixed another, if they exist, are parts of a bifunctor $Tor : Mod_{R}\times _{R}Mod\to Ab$. If there are sufficiently many [[projective objects]] in both $Mod_{R}$ and $_{R}Mod$, both are equal to balancing $Tor$, which is the bifunctor obtained by taking the homology of total complex of a bicomplex of $Hom$-s in which $A\otimes B$ is resolved by taking a projective resolution in each argument. 

## References

* [[Charles Weibel]], _An introduction to homological algebra_,  Cambridge Studies in Adv. Math. 38, CUP 1994

* H. Cartan, S. Eilenberg, _Homological algebra_, Princeton Univ. Press 1956.

* M. Kashiwara and P. Schapira, _[[Categories and Sheaves]]_, Springer (2000)

* S. I . Gelfand, Yu. I. Manin, _Methods of homological algebra_

[[!redirects Tor-functor]]
[[!redirects Tor functor]]
[[!redirects Tor-functors]]
[[!redirects Tor functors]]