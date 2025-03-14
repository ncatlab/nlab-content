
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Hochschild-Kostant-Rosenberg theorem_ identifies the [[Hochschild homology]] and cohomology of certain [[algebras]] with their [[modules]] of [[Kähler differentials]] and [[derivations]], respectively.


## Details

### For commutative $k$-algebras

First notice that we always have the following statement about the situation in degree 1.

+-- {: .num_prop }
###### Proposition

For a $k$-[[associative algebra|algebra]] $R$, its [[module]] of [[Kähler differential]]s coincides with its first [[Hochschild homology]]

$$
  \Omega(R/k) \simeq H_1(R,R)
  \,.
$$


=--

Write $\Omega^0(R/k) := R \simeq HH_0(R,R)$.

The HKR-theorem generalizes this to higher degrees.

#### As an isomorphism of chain complexes

For $n \geq 2$ write $\Omega^n(R/k) = \wedge^n_R \Omega(R/k)$ for the $n$-fold [[exterior algebra|wedge product]] of $\Omega(R/k)$ with itself: the degree $n$-K&#228;hler forms.

+-- {: .num_theorem }
###### Theorem

The isomorphism $\Omega^1(R/k) \simeq H_1(R,R)$ extends to a graded ring morphism

$$
  \psi : \Omega^\bullet(R/k) \to H_\bullet(R,R)
  \,.
$$

=--

If the $k$-algebra $R$ is sufficiently well-behaved, then this morphism is an [[isomorphism]] that identifies the Hochschild homology of $R$ in degree $n$ with $\Omega^n(R/k)$ for all $n$:

+-- {: .num_theorem }
###### Theorem
**(Hochschild-Kostant-Rosenberg theorem)**

If $k$ is a [[field]] and $A$ a commutative $k$-[[algebra]] which is 

* essentially of finite type (finitely presented)

* [[smooth scheme|smooth]] over $k$, meaning:

  * the  $A$-[[module]] of [[Kähler differential]]s $\Omega^1_k(A)$ is a [[projective object]] in $A Mod$_k.

then there is an [[isomorphism]] of graded $k$-algebras

$$
  \psi : \Omega^\bullet(A/k) \stackrel{\simeq}{\to}
  H_\bullet(A,A)
  \,.
$$

Moreover, dually, there is an isomorphism of Hochschild cohomology with wedge products of derivations:

$$
  \wedge^\bullet_A Der_k(A,A) \simeq HH^\bullet(A,A)
  \,.
$$


=--

+-- {: .proof}
###### Proof

This is reviewed for instance as theorem 9.4.7 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

or as theorem 9.1.3 in [Ginzburg](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=44).

=--

#### As an isomorphism of $\infty$-algebras

Actually, the HKR theorem holds on the level of chains: there is a [[quasi-isomorphism]] of [[chain complexes]] from [[polyvector field]]s (with zero differential) to the [[Hochschild cohomology|Hochschild cochain complex]] (with Hochschild differential).

The HKR map is a map of dg vector spaces, but not a map of 
[[dg-algebra]]s nor a map of [[dg-Lie algebra]]s. However, the [[Kontsevich formality|formality theorem]] of [[Maxim Kontsevich]] states that nevertheless the HKR map can be extended to an $L_\infty$ quasi-isomorphism. See [this MO post](http://mathoverflow.net/questions/32889/a-few-questions-about-kontsevich-formality) for details. 

The HKR map is only an isomorphism of vector spaces, not an isomorphism of algebras. In order to make it an isomorphism of algebras, one must add a "correction" by the square root of the $\hat{A}$ class. In the case of the quantization of linear Poisson structures (when the quantization becomes a universal enveloping algebra of a Lie algebra) this refines the [[Duflo isomorphism]]. See Kontsevich and Caldararu.


### For non-commutative algebras

There is also a noncommutative analogue due to [[Alain Connes]]. 

(...)

### For dg-algebras

Discussion for [[dg-algebras]] is in ([Cattaneo-Fiorenza-Longoni 05](#CattaneoFiorenzaLongoni05)).

### For ring spectra in homotopy theory
 {#ForRingSpectra}

Randy McCarthy and Vahagn Minasian have also proven an HKR theorem in the setting of [[higher algebra]] in [[stable homotopy theory]], where [[associative algebras]] are generalized to [[A-∞ algebras]], where the role of Hochschild homology is played by [[topological Hochschild homology]] and that of [[Kähler differentials]] by [[topological André-Quillen homology]] Again, this works under a certain smoothness property:

+-- {: .num_prop }
###### Proposition

For a connective smooth [[E-∞ ring]] $A$, the (natural) derivative map 

$$
  THH(A)\to \Sigma TAQ(A)
$$ 

from [[topological Hochschild homology]] to [[topological André-Quillen homology]] has a [[section]] in the [[(∞,1)-category of ∞-modules]] over $A$ which induces an equivalence of $A$-algebras 

$$
  \mathbb{P}_A\Sigma TAQ(A)\simeq THH(A),
$$ 

where $\mathbb{P}$ is the free symmetric algebra triple. 

=--

This is due to ([McCarthy-Manasian 03](#McCarthyManasian03)).


## References

The original source is

* [[Gerhard Hochschild]], [[Bertram Kostant]], [[Alexander Rosenberg]], _Differential forms on regular affine algebras_, Transactions AMS __102__ (1962), No.3, 383--408 (reprinted in G. P. Hochschild, Collected Papers. Volume I 1955-1966, Springer 2009, 265-290) [DOI:10.2307/1993614](http://dx.doi.org/10.2307/1993614).

Standard textbook references include

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_ section 9.4 

* [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603)) section 4, Theorem 9.1.3

Discussion in [[positive number|positive]] [[characteristic]] is in

* {#AntieauVezzosi17} [[Benjamin Antieau]], [[Gabriele Vezzosi]], _A remark on the Hochschild-Kostant-Rosenberg theorem in characteristic $p$_ ([arXiv:1710.06039](https://arxiv.org/abs/1710.06039))

A new approach to the generalized HKR isomorphism is proposed in 

* Dima Arinkin, Andrei Caldararu, _When is the self-intersection of a subvariety a fibration?_, [arxiv/1007.1671](http://arxiv.org/abs/1007.1671)

The version for dg-algebras is discussed in 

* {#CattaneoFiorenzaLongoni05} [[Alberto Cattaneo]], [[Domenico Fiorenza]], Riccardo Longoni, _On the Hochschild-Kostant-Rosenberg map for graded manifolds_, Int. Math. Res. Not. 2005, no. 62, 3899-3918 ([arXiv:math/0503380](http://arxiv.org/abs/math/0503380))

The version for $E_\infty$-algebras is discussed in

* {#McCarthyManasian03} Randy McCarthy, Vahagn Minasian, _HKR Theorem for Smooth $S$-algebras_, [arxiv:math/0306243](http://arxiv.org/pdf/math/0306243v1.pdf)

[[!redirects HKR theorem]]
[[!redirects HKR]]
[[!redirects Hochschild-Kostant-Rosenberg]]
[[!redirects Hochschild--Kostant--Rosenberg]]
[[!redirects Hochschild–Kostant–Rosenberg theorem]]
[[!redirects Hochschild–Kostant–Rosenberg's theorem]]
[[!redirects Hochschild--Kostant--Rosenberg theorem]]
[[!redirects Hochschild-Kostant-Rosenberg isomorphism]]
[[!redirects Hochschild-Kostant-Rosenberg map]]