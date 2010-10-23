

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called **BF-theory** is a [[topological quantum field theory]] defined by an [[action functional]] $S_{BF}$  on a space of certain [[connection on a bundle|connections]] and forms over a 4-[[dimensional]] [[smooth manifold]] $X$, such that locally on $X$ the configuration space is given by [[Lie algebra-valued 1-form]]s $A$ with values in some $\mathfrak{g}_1$ and 2-forms $B$ with values in some $\mathfrak{g}_2$, together with a homomorphism $\partial : \mathfrak{g}_2 \to \mathfrak{g}_1$ and an [[invariant polynomial]] $\langle -,- \rangle$, as

$$
  S_{BF} : (A,B) \mapsto \int_X \langle F_A \wedge \partial B\rangle 
  \,,
$$

where $F_A$ is the [[curvature]] 2-form of $A$.

There is not much of a proposal in the literature for what exactly that would or should mean globally. It has been observed that it looks like the action functional is one on [[∞-Lie algebra-valued forms]] with values in a [[strict Lie 2-algebra]] $\mathfrak{g} = (\mathfrak{g}_2 \stackrel{\partial}{\to} \mathfrak{g}_1)$.

This would suggest that the BF-action functional is to be regarded as a functional on the [[space]] ([[2-groupoid]]) of $G$-[[principal 2-bundle]]s with [[connection on a 2-bundle]], where $G = (G_2 \to G_1)$ is a [[Lie 2-group]] integrating $\mathfrak{g}$.

If one couples to the above action functional that for [[topological Yang-Mills theory]] and a [[cosmological constant]] with coefficients as in

$$
  \int_X( \langle F_A \wedge B\rangle - \frac{1}{2} \langle F_A \wedge F_A\rangle - \frac{1}{2}\langle \partial B \wedge \partial B\rangle)
$$

then this is the [[generalized Chern-Simons theory]] action functional indiced from the canonical [[Chern-Simons element]] on the [[strict Lie 2-algebra]] $\mathfrak{g}$. See [[Chern-Simons element]] for details.



## Applicatins

Much of the interest in BF-theory results from the fact that on a 4-dimensional manifold, to some extent the [[Einstein-Hilbert action]] for [[gravity]] may be encoded in BF-theory form. See [[gravity as a BF-theory]].


## References

The observation that the BF-theory action functional looks like it should be read as a functional on a space of  [[∞-Lie algebra valued forms]] with values in a [[strict Lie 2-algebra]] possibly appears in print first in <a href="http://arxiv.org/PS_cache/hep-th/pdf/0309/0309173v2.pdf#page=22">section 3.9</a> of 

* Florian Girelli, Hendryk Pfeiffer, _Higher gauge theory -- differential versus integral formulation_ ([arXiv](http://arxiv.org/abs/hep-th/0309173)) .

The observation that it can be read as the [[∞-Chern-Simons theory]] action functional on [[connections on 2-bundles]] is in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-conections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>))
{#SSSI}

For more on this see [[Chern-Simons element]].



[[!redirects BF theory]]
