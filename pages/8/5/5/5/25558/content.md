
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **crossed group** is a [[presheaf]] with additional symmetry given by a fiberwise [[group]] structure and actions on the morphisms of the underlying [[category]].

## Definition

+-- {: .num_defn }
###### Definition

For $S$ a [[small category]], a **crossed $S$-group** is a [[presheaf]] $G : S^{op} \to Set$ equipped with

1. for each object $s \in S$ a group structure on $G_s$;

1. for all $s, r\in S$ a left $G_r$-[[action]] on the [[hom-set]] $S(s,r)$ ;

such that for all morphisms $\alpha : s \to r$ and $\beta : t \to s$ in $S$ and $g,h \in G_r$ we have

1. $g_*( \alpha \circ \beta)  = g_*(\alpha) \circ \alpha^*(g)_* \beta$;

1. $g_* (id_r) = id_r$;

1. $\alpha^* (g \cdot h) = h_*(\alpha)^*(g)\cdot \alpha^*(h)$;

1. $\alpha^*(e_r) = e_s$;

where $g_*$, $h_*$ denotes the group action and 

$\alpha^* : G_r \to G_s$ the presheaf map. 

The **total category** $S G$ of an crossed $S$-group $G$ is the category with the same objects as $S$, and with morphisms $r \to s$ being pairs $(\alpha, g) \in S(s,r)\times G_r$ and with composition defined by

$$
  (\alpha, g) \circ (\beta, h)
  = 
  (\alpha \cdot g_*(\beta), \beta^*(g) \cdot h)
  \,.
$$ 

=--

([Ber-Moe, def. 2.1](#BergerMoerdijk)).

## Examples

* In case, $G$ is constant, i.e. $G_s=G$ and $\alpha^*(g)=g$ for all $s,\alpha \in S$, $S G$ reduces to the [[Grothendieck construction]] for the functor $G\to Cat$ that picks out $S$.

* Let $\Omega_{pl}$ be the category of finite planar [[tree|trees]]. Then the category $\Omega$ of non-planar finite rooted [[tree|trees]] arises as the total category of an $\Omega_{pl}$-crossed group which to a _planar_ tree $T$ assigns its group of non-planar automorphisms. This example is somewhat typical, since $\Omega_{pl}$ is a strict [[Reedy category]] where all automorphisms are trivial which gets enhanced with non-trivial symmetries to $\Omega$, now a [[generalized Reedy category]] (cf. below).

## Properties

+-- {: .num_defn }
###### Definition

If $S$ is equipped with a generalized Reedy structure, then an $S$-crossed group $G$ is called **compatible** with that generalized Reedy structure if 

1. the $G$-action respects $S^+$ and $S^-$;

1. if $\alpha : r \to s$ is in $S^-$ and $g \in G_s$ such that $\alpha^* (g) = e_r$ and $g_*(\alpha) = \alpha$, then $g = e_s$.

=--

+-- {: .num_prop }
###### Proposition

Let $S$ be a strict [[Reedy category]] and let $G$ be a compatible $S$-crossed group. Then there exists a unique dualizabe generalized Reedy structure on $S G$ for which the embedding $S \hookrightarrow S G$ is a morphism of generalized Reedy categories.

=--

([Ber-Moe, prop. 2.10](#BergerMoerdijk)).

## Remarks

* A related notion is "thickening" (cf. [Cisinski (8.5.8; 2006)](#Cisinski), [Isaacson (2010)](#Isaacson2010)).

## Related entries

* [[skew-simplicial set]]

* [[generalized Reedy category]]

* [[crossed homomorphism]]

* [[cyclic set]]

* [[symmetric set]]

* [[quaternionic set]]


## References

* [[Michael Batanin]], [[Martin Markl]], _Crossed interval groups and operations on the Hochschild cohomology_, arXiv:0803.2249 (2008). ([abstract](https://arxiv.org/abs/0803.2249))

* [[Clemens Berger]], [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_ (2008) ([arXiv:0809.3341](http://arxiv.org/abs/0809.3341))
 {#BergerMoerdijk}

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie|Les préfaisceaux comme modèles des types d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski}

* [[Tobias Dyckerhoff]], [[Mikhail Kapranov]], _Crossed simplicial groups and structured surfaces_, arXiv:1403.5799 (2014). ([abstract](https://arxiv.org/abs/1403.5799))

* B. L. Feigin, B. L. Tsygan, _Additive K-theory_, pp.67-203 in LNM 1289 Springer Heidelberg 1986.

* Zbigniew Fiedorowicz, [[Jean-Louis Loday]], _Crossed simplicial groups and their associated homology_, Trans. AMS **326** pp.57-87 (1991).

* {#Isaacson2010} [[Samuel Isaacson]], _Symmetric cubical sets_, Journal of Pure and Applied Algebra **215** (2011). ([arXiv](https://arxiv.org/abs/0910.4948), [doi:10.1016/j.jpaa.2010.08.001](http://dx.doi.org/10.1016/j.jpaa.2010.08.001))

* R. Krasauskas, _Skew-simplicial groups_, Lithuanian Math. J. **27** pp.47-54 (1987).

* [[Jean-Louis Loday]], _Cyclic Homology_, Springer Heidelberg 1998$^2$.

* Walker H. Stern, _Structured topological field theories via crossed simplicial groups_, arXiv:1603.02614 (2016). ([abstract](https://arxiv.org/abs/1603.02614))

* [[Jun Yoshida]], _A general method to construct cube-like categories and applications to homotopy theory_, arXiv:1502.07539. ([abstract](https://arxiv.org/abs/1502.07539))

* [[Jun Yoshida]], _Colimits and limits of crossed groups_, arXiv:1802.06644 (2018). ([abstract](https://arxiv.org/abs/1802.06644))


[[!redirects crossed groups]]




