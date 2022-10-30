
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Over the [[complex numbers]] an [[elliptic curve]] (hence a [[complex manifold|complex]] [[torus]]) may be, and often is, presented as a [[quotient]] of the [[complex plane]] by a framed [[lattice]], determined by a point $\tau$ in the [[upper half plane]] $\mathfrak{h}$. But indeed this data determines a [[framed elliptic curve]], namely the underlying [[curve]] $\Sigma$ together with the "edges along which it is glued" by this construction. These are equivalently a choice of [[ordering|ordered]] [[basis]] 

$$
  (a_1,a_2)\in H_1(\Sigma,\mathbb{Z})
$$

of the first [[ordinary homology]] of $\Sigma$ with [[integer]] [[coefficients]] (and vanishing [[intersection number]]).  The [[special linear group]] $SL_2(\mathbb{Z})$ naturally acts on this data (by [[Möbius transformations]] on $\tau$) and the [[quotient]] [[projection]] exhibits an infinite [[covering]] ([[atlas]]) of the  [[moduli stack of elliptic curves]] over the complex numebrs

$$
  \mathfrak{h} \longrightarrow \mathfrak{h}//SL_2(\mathbb{C}) \simeq \mathcal{M}_{ell}(\mathbb{C})
  \,.
$$

The concept of _level structure_ on an elliptic curve is a structure weaker than that of a [[framed elliptic curve|framing]] which analogously gives a [[finite number|finite]] [[covering]]. Instead of considering cycles in integral homology, a _level $n$-structure_ for [[natural number]] $B$ is given by cycles in homology with [[coefficients]] just in the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ (e.g. [Hain 08, def. 4.6](#Hain08)).

On such level-$n$ data now acts instead just the group $SL_2(\mathbb{Z}/n\mathbb{Z})$. The [[kernel]] of the [[projection]] maps is called the _level $n$-subgroup_ (an example of a _[[congruence subgroup]]_)

$$
  \Gamma(n) \to SL_2(\mathbb{Z}) \to SL_2(\mathbb{Z}/n\mathbb{Z})
  \,.
$$

There is then a moduli stack of complex elliptic curves with level $n$-structure

$$
  \mathcal{M}_{ell}[n](\mathbb{C}) \simeq \mathfrak{h}//\Gamma_n
$$

and this is now a finite cover (of rank the [[order of a group|order]] of the [[finite group]] $SL_2(\mathbb{Z}/n\mathbb{Z})$) of the actual moduli stack of complex elliptic curves

$$
  \mathcal{M}_{ell}[n](\mathbb{C})
  \longrightarrow
  \mathcal{M}_{ell}[n](\mathbb{C})//SL_2(\mathbb{Z}/n\mathbb{Z})
  \simeq
  \mathcal{M}_{ell}(\mathbb{C})
  \,.
$$



## References

Over the complex numebers:

* {#Hain08} Richard Hain, section 4.2 of _Lectures on Moduli Spaces of Elliptic Curves_ ([arXiv:0812.1803](http://arxiv.org/abs/0812.1803))

Over general base rings:

* {#MahowaldRezk09} [[Mark Mahowald]] [[Charles Rezk]], _Topological modular forms of level 3_, Pure Appl. Math. Quar. 5 (2009) 853-872 ([pdf](http://www.math.uiuc.edu/~rezk/tmf3-paper-final.pdf))

* {#HillLawson13} [[Michael Hill]], [[Tyler Lawson]], _Topological modular forms with level structure_ ([arXiv:1312.7394](http://arxiv.org/abs/1312.7394))

[[!redirects level structures on an elliptic curve]]

[[!redirects level structures on elliptic curves]]

[[!redirects level N-structure]]
[[!redirects level N structure]]
[[!redirects level N-structures]]
[[!redirects level N structures]]

[[!redirects level n-structure]]
[[!redirects level n structure]]
[[!redirects level n-structures]]
[[!redirects level n structures]]


[[!redirects level n subgroup]]
[[!redirects level n subgroups]]



[[!redirects level n-structure on an elliptic curve]]
[[!redirects level n-structure on elliptic curves]]