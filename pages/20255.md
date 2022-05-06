
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the [[string theory]]-literature "$I_8$" is the standard notation for a certain [[characteristic class]] of [[manifolds]] (of their [[tangent bundles]]): It is a [[rational numbers|rational]] linear combination of the [[cup product|cup square]] of the [[first fractional Pontryagin class]]  with itself, and the [[second Pontryagin class]]:

\[
  \label{TheTerm}
  I_8
  \;\coloneqq\;
  \tfrac{1}{48}
  \Big(
    p_2 \;-\; \big( \tfrac{1}{2} p_1\big)^2
  \Big)
  \;\; 
  \in
  H^8\big( -, \mathbb{Q}\big)
  \,.
\]

In general this is a [[cohomology class]] in [[ordinary cohomology]] with [[rational number|rational]] [[coefficients]], though in applications it appears in further rational combination with other classes that in total yield a class in [[integral cohomology]].

The expression (eq:TheTerm) controls certain [[quantum anomaly cancellation]] in [[M-theory]] and [[type IIA string theory]] ([Vafa-Witten 95](#VafaWitten95), [Duff-Liu-Minasian 95 (3.10) with (3.14)](#DuffLiuMinasian95)). Since it was first obtain as a [[1-loop]]-contribution in [[perturbative quantum gravity|perturbative quantum]] [[supergravity]], it is often known as _the one-loop anomaly term_ or the _one-loop anomaly polynomial_ in [[M-theory]]/[[type IIA string theory]].

## Properties

### Relation to M5-brane anomalies

Consider an 11-dimensional [[spin structure|spin]]-[[manifold]] $X^{(11)}$ and a 2-parameter family of 6-dimensional [[submanifolds]] $Q_{M5} \hookrightarrow X^{(11)}$. When regarded as a family of [[worldvolumes]] of an [[M5-brane]], the family of [[normal bundles]] $N_X Q_{M5}$ of this inclusion carries a [[characteristic class]]

$$
  I^{M5}
  \;\coloneqq\;
  I^{M5}_{\psi} 
  + 
  I_{C}
  \;\in\;
  H^8(F \times Q_{M5},\mathbb{Z})
$$

where

1. the first summand is the class of the [[chiral anomaly]] of [[chiral fermions]] on $Q_{M5}$ ([Witten 96 (5.1)](#Witten96)), 

1. the second term the class of the [[quantum anomaly]] of a [[self-dual higher gauge field]] ([Witten 96 (5.4)](#Witten96))

Moreover, there is the restriction of the $I_8$-term (eq:TheTerm) to $Q_{M5}$, hence to the [[tangent bundle]] of $X^{11}$ to $Q_{M5}$ (the "anomaly inflow" from the [[bulk spacetime]] to the M5-brane)

$$
  I_8\vert_{M5}
  \;\coloneqq\;
   I_8
   \big(
     T_{Q_{M5}} X
   \big)
  \;\in\;
  H^8(F \times Q_{M5},\mathbb{Z})
  \,.
$$

The sum of these cohomology classes, evaluated on the [[fundamental class]] of $Q_{M5}$ is proportional to the [[second Pontryagin class]] of the [[normal bundle]]

$$
  I^{M5}
  \;+\;
  I_8\vert_{M5}
  \;=\;
  \tfrac{1}{24} p_2(N_{Q_{M5}})
$$

([Witten 96 (5.7)](#Witten96))

\linebreak

## Related concepts

* [[Pontryagin classes]], [[Stiefel-Whitney classes]], [[Wu classes]], [[Euler class]]

* [[C-field tadpole cancellation]]


## References

The term showed  in [[string theory]]/[[M-theory]] [[anomaly cancellation]] in 

* {#VafaWitten95} [[Cumrun Vafa]], [[Edward Witten]], _A One-Loop Test Of String Duality_, Nucl.Phys.B447:261-270, 1995 ([arXiv:hep-th/9505053](https://arxiv.org/abs/hep-th/9505053))

* {#DuffLiuMinasian95} [[Mike Duff]], James T. Liu, [[Ruben Minasian]], _Eleven Dimensional Origin of String/String Duality: A One Loop Test_, Nucl.Phys. B452 (1995) 261-282 ([arXiv:hep-th/9506126](https://arxiv.org/abs/hep-th/9506126))

* {#Witten96} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J.Geom.Phys.22:103-133, 1997 ([arXiv:hep-th/9610234](https://arxiv.org/abs/hep-th/9610234))

For further discussion see

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ , 
  
  part I, Proc. Symp. Pure Math. 81 (2010), 181-236 ([arXiv:1001.5020](http://arXiv.org/abs/1001.5020)), 

  part _II: Twisted $String$ and $String^c$ structures_, J. Australian Math. Soc. 90 (2011), 93-108 ([arXiv:1007.5419](http://arxiv.org/abs/1007.5419)); 

  part _III: Twisted higher structures_, Int. J. Geom. Meth. Mod. Phys. 8 (2011), 1097-1116 ([arXiv:1008.1755](http://arxiv.org/abs/1008.1755))

[[!redirects one-loop anomaly polynomial I8]]
