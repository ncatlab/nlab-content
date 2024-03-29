
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[foliation]]-theory the _Bott connection_ is a certain characteristic [[connection on a bundle|connection]] on the [[conormal bundle]] of the [[foliation]].

## Definition

+-- {: .num_defn }
###### Definition

For $X$ a [[smooth manifold]] and $\mathcal{P} \hookrightarrow T X$ a [[foliation]] of $X$, incarnated as a subbundle of the [[tangent bundle]], the corresponding [[conormal bundle]]

$$
  \mathcal{P}^\perp  \hookrightarrow T^* X
$$

is the annihilator of $\mathcal{P}$ under the pairing of covectors with vectors. The corresponding **Bott connection** is the [[covariant derivative]] of vectors $X \in \Gamma(\mathcal{P})$ on covectors $\xi \in \Gamma(\mathcal{P}^\perp)$ given by the [[Lie derivative]]

$$
  \nabla_X \;\colon\; \xi \mapsto \mathcal{L}_X \xi = \iota_X d_{dR} \xi
  \,.
$$

=--

Similarly there is a Bott connection along $\mathcal{P}$ along the [[normal bundle]] $T X / \mathcal{P}$. More generally, one speaks of _a Bott connection_ for any connection on the (co)normal bundle and defined on all vector fields on $X$ which restricts to the above along leaves.

## References

The notion originates in

* [[Raoul Bott]], _Lectures on characteristic classes and foliations, in Lectures on algebraic and differential topology_, Springer Lecture Notes in Mathematics, 279, (1972)

in the study of [[characteristic classes]] of [[foliations]]. Further developments are in 

* Jonathan Bowden, _On foliated characteristic classes of transversally symplectic foliations_ ([arXiv:1108.1919](https://arxiv.org/abs/1108.1919))

Used in the context of secondary characteristic classes for Lie algebroids in Sec. 2.3 of

* [[Marius Crainic]], [[Rui Loja Fernandes]], _Secondary characteristic classes of Lie algebroids_,
In: u. Carow-Watamura, y. Maeda, s. Watamura (eds), Quantum Field Theory and Noncommutative Geometry. Springer Lecture Notes in Physics __662__ [doi](https://doi.org/10.1007/11342786_9)


[[!redirects Bott connections]]

