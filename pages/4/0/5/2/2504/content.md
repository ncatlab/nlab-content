[[!redirects supergravity Lie 3-algebra]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The _supergravity Lie 3-algebra_ $\mathfrak{sugra}(10,1)$ or [[M2-brane]] extension $\mathfrak{m}2\mathfrak{brane}$ is a [[super L-∞ algebra]]  that is a shifted [[∞-Lie algebra cohomology|extension]]

$$
  0 \to b^2 \mathbb{R} \to 
  \mathfrak{sugra}(10,1) \to
  \mathfrak{siso}(10,1)
  \to
  0
$$

of the [[super Poincare Lie algebra]] $\mathfrak{siso}(10,1)$ in 10+1 dimensions induced by the exceptional degree 4-[[Lie algebra cohomology|super Lie algebra cocycle]]

$$
  \mu_4 = \bar \psi \wedge \Gamma^{a b} \psi \wedge e_a \wedge e_b
  \;\;
  \in CE(\mathfrak{siso}(10,1))
  \,.
$$

This is the same mechanism by which the [[String Lie 2-algebra]] is a shifted central extension of $\mathfrak{so}(n)$.

## Properties

### The Chevalley-Eilenberg algebra

+-- {: .num_prop #TheCEAlgebra}
###### Proposition

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{sugra}(10,1))$ is generated on 

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* a single element $c$ of degree $(3,even)$ 

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

with the differential defined by

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi
$$

$$
  d_{CE} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
$$

$$
  d_{CE} \, c = \frac{1}{2}\bar \psi \Gamma^{a b} \wedge \psi \wedge e_a \wedge e_b
  \,.
$$

=--

> (fill in details)


### Hidden super Lie 1-algebra

At the end of ([D'Auria-Fre 82](#DAuriaFr82)) the authors ask for a super Lie 1-algebra $\mathfrak{g}$, equipped with a degree-3 element $A$ in its [[Chevalley-Eilenberg algebra]], and equipped with a homomorphism $p\colon \mathfrak{g}\longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}$ such that the pullback of the 4-cocycle $\mu_4$ along $p$ is trivialized by $A$:

$$
  p^\ast \mu_4 = d_{CE}A
  \,.
$$

In the [[model structure on L-infinity algebras|homotopy theory of L-infinity algebra]] this means that

$$
  \array{
     \mathfrak{g} &\longrightarrow& \ast
     \\
     {}^{\mathllap{p}}
     \downarrow
       &\swArrow_{\mathrlap{A}}&
     \downarrow
     \\
     \mathbb{R}^{10,1\vert \mathbf{32}}
       &\underset{\mu_4}{\longrightarrow}&
     \mathbf{B}^3 \mathbb{R}
  }
  \,.
$$

Compare this to the characterization of $\mathfrak{sugra}(10,1)$ as the [[homotopy fiber]] of $\mu_4$, hence as the _universal_ solution to this situation

$$
  \array{
     \mathfrak{sugra}(10,1) &\longrightarrow& \ast
     \\
     \downarrow
       &\swArrow_{}&
     \downarrow
     \\
     \mathbb{R}^{10,1\vert \mathbf{32}}
       &\underset{\mu_4}{\longrightarrow}&
     \mathbf{B}^3 \mathbb{R}
  }
  \,.
$$

In any case, in ([D'Auria-Fre 82](#DAuriaFr82)) possible choices for $p \colon \mathfrak{g} \to \mathbb{R}^{10,1\vert\mathbf{32}}$ are found. 

Curiously, the bosonic [[body]] of $\mathfrak{g}$ is such that when adapted to a compactification to 4d, then it is the [[exceptional tangent bundle]] on which the [[U-duality]] group [[E7]] has a canonical action.

In ([BAIPV 04](#BAIPV04)) these solutions are shown to extend to a 1-parameter family of solutions. Further comments are in ([Andrianopoli-D'Auria-Ravera 16](#AndrianopoliDAuriaRavera16)).

### Relation to M5-brane action functional

The supergravity Lie 3-algebra carries a 7-cocycle (the one that induces the [[supergravity Lie 6-algebra]]-extension of it). The corresponding WZW term is that of the [[M5-brane]] in its [[Green-Schwarz action functional]]-like formulation. 

[[!include brane scan]] 

### Relation to the 11-dimensional polyvector super Poincar&#233;-algebra
 {#Polyvector}

#### Via derivations

+-- {: .num_prop }
###### Proposition


Let $\mathfrak{der}(\mathfrak{sugra}(10,1))$ be the [[automorphism ∞-Lie algebra]] of $\mathfrak{sugra}(10,1)$. This is a [[dg-Lie algebra]]. Write
$\mathfrak{der}(\mathfrak{sugra}(10,1))_0$ for the ordinary [[Lie algebra]] in degree 0.

This is [[isomorphic]] to the polyvector-extension of the [[super Poincaré Lie algebra]] (see there) in $d = 10+1$ -- the 
"[[M-theory super Lie algebra]]" -- with "2-brane central charge": the Lie algebra spanned by generators
$\{P_a, Q_\alpha, J_{a b}, Z^{a b}\}$ and graded Lie brackets those of the [[super Poincaré Lie algebra]] as well as

$$
  [Q_\alpha, Q_\beta] = i (C \Gamma^a)_{\alpha \beta} P_a + (C \Gamma_{a b})Z^{a b} 
$$

$$
  [Q_\alpha, Z^{a b}] = 2 i (C \Gamma^{[a})_{\alpha \beta}Q^{b]\beta}
$$

etc.

=--

This observation appears implicitly in ([Castellani 05, section 3.1](#Castellani05)), see ([FSS 13](#FSS13)). 


+-- {: .proof}
###### Proof

With the presentation of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{sugra}(10,1))$ as in prop. \ref{TheCEAlgebra} above, the generators are identified with [[derivation]]s on $CE(\mathfrak{sugra}(10,1))$ as

$$
  P_a = [d_{CE}, \frac{\partial}{\partial e^a} ]
$$

and

$$
  Q_\alpha = [d_{CE}, \frac{\partial}{\partial \psi^\alpha} ]
$$

and

$$
  J_{a b} = [d_{CE}, \frac{\partial}{\partial \omega^{a b}} ]
$$

and

$$
  Z^{a b} = [d_{CE}, e^a \wedge e^b \wedge \frac{\partial}{\partial c}]
$$

etc. With this it is straightforward to compute the commutators.
Notably the last term in 

$$
  [Q_\alpha, Q_\beta] = i (C \Gamma^a)_{\alpha \beta} P_a + (C \Gamma_{a b})Z^{a b} 
$$

arises from the contraction of the 4-cocycle $\bar \psi \Gamma^{a b} \wedge \psi \wedge e_a \wedge e_b$ with $\frac{\partial}{\partial \psi^\alpha}\wedge \frac{\partial}{\partial \psi^\beta}$.

=--

#### Via the Heisenberg Lie 3-algebras

(...)

## Applications

The field configurations of 11-dimensional [[supergravity]] may be identified with [[∞-Lie algebra-valued forms]] with values in $\mathfrak{sugra}(10,1)$.
See [[D'Auria-Fre formulation of supergravity]].

## Related concepts

[[supergravity Lie 6-algebra]] $\to$ **supergravity Lie 3-algebra** $\to$ [[super Poincaré Lie algebra]]

* [[4d supergravity Lie 2-algebra]]

* [[extended supersymmetry]]

* [[type II supergravity Lie 2-algebra]]

* [[type II supersymmetry algebra]]

* [[M-theory supersymmetry algebra]]


## References

The [[Chevalley-Eilenberg algebra]] of $\mathfrak{sugra}(10,1)$ first appears in (3.15) of

* {#DAuriaFr82} [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982)

and later in the textbook

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_


The manifest interpretation of this as a [[Lie 3-algebra]] and the supergravity field content as [[∞-Lie algebra valued forms]] with values in this is mentioned in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:L-∞ algebra connections]]_

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_
 

A systematic study of the super-[[Lie algebra cohomology]] involved is in

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry I_ ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_ ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))

See also [[division algebra and supersymmetry]].

Further discussion of its "hidden" super Lie algebra includes

* {#BAIPV04} [[Igor Bandos]], [[José de Azcárraga]], J.M. Izquierdo, M. Picon, O. Varela, _On the underlying gauge group structure of D=11 supergravity_, Phys.Lett.B596:145-155,2004 ([arXiv;hep-th/0406020](http://arxiv.org/abs/hep-th/0406020))

* [[Igor Bandos]], [[Jose de Azcarraga]], Moises Picon, Oscar Varela, _On the formulation of $D=11$ supergravity and the composite nature of its three-from field_, Annals Phys. 317 (2005) 238-279 ([arXiv:hep-th/0409100](https://arxiv.org/abs/hep-th/0409100))

* {#AndrianopoliDAuriaRavera16} L. Andrianopoli, [[Riccardo D'Auria]], L. Ravera, _Hidden Gauge Structure of Supersymmetric Free Differential Algebras_ ([arXiv:1606.07328](https://arxiv.org/abs/1606.07328))

Further review:

* [[Lucrezia Ravera]], *On the hidden symmetries of $D=11$ supergravity* ([arXiv:2112.00445](https://arxiv.org/abs/2112.00445))


The computation of the automorphism Lie algebra of $\mathfrak{sugra}(10,1)$ is in 

* {#Castellani05} [[Leonardo Castellani]], _Lie derivatives along antisymmetric tensors and the M-theory superalgebra_, J. Phys. Math. Volume 3 (2011), 1-7. ([arXiv:hep-th/0508213](http://arxiv.org/abs/hep-th/0508213))
 

A similar argument with more explicit use of the Lie 3-algebra as underlying the [[Green-Schwarz action functional|Green-Schwarz-like action functional]] for the [[M5-brane]] is in 

* [[Dmitri Sorokin]], [[Paul Townsend]], _M-theory superalgebra from the M-5-brane_, Phys. Lett. B412 (1997) 265-273 ([arXiv:hep-th/9708003](http://arxiv.org/abs/hep-th/9708003))

[[!redirects m2brane]]