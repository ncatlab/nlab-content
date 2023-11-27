


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

What is called **BF-theory** is a [[topological quantum field theory]] defined by an [[action functional]] $S_{BF}$  on a space of certain [[connection on a bundle|connections]] and [[differential forms]] over a [[4-manifold]] $X$, such that locally on $X$ the [[space of field histories]] is given by 

1. [[Lie algebra-valued 1-forms]] $\;A$ with values in some [[Lie algebra]] $\mathfrak{g}_1$ and with [[field strength]]/[[curvature]] 2-form $F_A$;

1. [[differential 2-forms]] $\;B$ with values in some [[Lie algebra]] $\mathfrak{g}_2$, 

1. together with

   1. a homomorphism $\partial \colon \mathfrak{g}_2 \to \mathfrak{g}_1$ 

   1. an [[invariant polynomial]] $\langle -,- \rangle$

by

$$
  S_{BF} 
  \;\colon\; 
  (A,B) \;\mapsto\; 
  \int_X \langle F_A \wedge \partial B\rangle 
  \,.
$$

There is not much of a proposal in the literature for how to make sense of this expression globally. It has been observed that it looks like the action functional is one on [[∞-Lie algebra-valued forms]] with values in a [[strict Lie 2-algebra]] $\mathfrak{g} = (\mathfrak{g}_2 \stackrel{\partial}{\to} \mathfrak{g}_1)$.

This would suggest that the BF-action functional is to be regarded as a functional on the [[space]] ([[2-groupoid]]) of $G$-[[principal 2-bundles]]
with [[connection on a 2-bundle]], where $G = (G_2 \to G_1)$ is a [[Lie 2-group]] integrating $\mathfrak{g}$.

If one couples to the above action functional that for [[topological Yang-Mills theory]] and a [[cosmological constant]] with coefficients as in

$$
  \int_X( \langle F_A \wedge B\rangle - \frac{1}{2} \langle F_A \wedge F_A\rangle - \frac{1}{2}\langle \partial B \wedge \partial B\rangle)
$$

then this is the [[generalized Chern-Simons theory]] action functional induced from the canonical [[Chern-Simons element]] on the [[strict Lie 2-algebra]] $\mathfrak{g}$. See [[Chern-Simons element]] for details.



## Applications

Much of the interest in BF-theory results from the fact that on a 4-dimensional manifold, to some extent the [[Einstein-Hilbert action]] for [[gravity]] may be encoded in BF-theory form. See [[gravity as a BF-theory]].


## References

BF theory was maybe first considered in

* [[Gary Horowitz]], _Exactly soluable diffeomorphism invariant theories_ Commun. Math. Phys. 125, 417-437 (1989)

The observation that the BF-theory action functional looks like it should be read as a functional on a space of  [[∞-Lie algebra valued forms]] with values in a [[strict Lie 2-algebra]] possibly appears in print first in <a href="http://arxiv.org/PS_cache/hep-th/pdf/0309/0309173v2.pdf#page=22">section 3.9</a> of 

* [[Florian Girelli]], Hendryk Pfeiffer, _Higher gauge theory -- differential versus integral formulation_, [arXiv:hep-th/0309173](http://arxiv.org/abs/hep-th/0309173)

The observation that coupled to [[topological Yang-Mills theory]] it can be read as the [[schreiber:∞-Chern-Simons theory]] action functional on [[connections on 2-bundles]] is in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-conections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)
{#SSSI}

and a more comprehensive discussion is in section 4.3 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .

See also

* Aristide Baratin, Florian Girelli, Daniele Oriti,  _Diffeomorphisms in group field theories_, Physical Review D, vol. 83, Issue 10, id. 104051, [doi](http://dx.doi.org/10.1103/PhysRevD.83.104051), [arxiv/1101.0590](http://arxiv.org/abs/1101.0590)

There is a more general BFCG action introduced by Girelli, Pfeiffer and Popescu
which has been shown to be a special case of the categorified BF-theory
in

* Jo&#227;o Martins, Aleksandar Mikovi&#263;, _Lie crossed modules and gauge-invariant actions for 2-BF theories_, Adv. Theor. Math. Phys. __15__:4 (2011), 913-1199 [euclid](http://projecteuclid.org/euclid.atmp/1339438351)

Relation to [[Einstein gravity]] (in [[first-order formulation of gravity|first-order formulation]]):

* Mariano Celada, Diego Gonz&#225;lez, Merced Montesinos, _BF gravity_ &lbrack;[arxiv/1610.02020](https://arxiv.org/abs/1610.02020)&rbrack;

* [[Alberto S. Cattaneo]], [[Leon Menger]], [[Michele Schiavina]], *Gravity with torsion as deformed BF theory* &lbrack;[arXiv:2310.01877](https://arxiv.org/abs/2310.01877)&rbrack;


On a version of BF-theory in [[arithmetic]] related to non-[[orientation|orientability]] of [[arithmetic schemes]]:

* [[Magnus Carlson]], [[Minhyong Kim]], _A note on abelian arithmetic BF-theory_, ([arXiv:1911.02236](https://arxiv.org/abs/1911.02236))


[[!redirects BF theory]]
