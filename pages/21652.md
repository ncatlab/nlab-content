

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A variant of the notion of [[determinant]] for [[matrices]] with values in [[division rings]] (such as the [[quaternions]]).

## Definition

Dieudonné showed that if $K$ is a division ring then there is a group isomorphism

$$ \alpha \colon GL(n,K)/[GL(n,K), GL(n,K)] \xrightarrow{\sim} K^\times/[K^\times, K^\times] $$

where $GL(n,K)$ is the group of invertible $n \times n$ matrices with entries in $K$, $K^\times = GL(1,K)$ is called the [[group of units]] of $K$, and $G/[G,G]$ is the [[abelianization]] of the group $G$.  This group isomorphism is uniquely determined by the following properties:

* if a row of the matrix $T$ is left multiplied by $a \in K^\times$ then $\alpha(T)$ is left multiplied by $[a] \in K^\times/[K^\times K^\times]$
* if a multiple of one row of $T$ is added to another row of $T$, then $\alpha(T)$ is unchanged
* If two rows of $T$ are exchanged, then $\alpha(T)$ is multiplied by $[-1] \in K^\times/[K^\times, K^\times]$.

Composing this isomorphism $\alpha$ with the quotient map $GL(n,K) \to GL(n,K) / [GL(n,K), GL(n,K)]$ gives the **Dieudonné determinant**

$$ det \colon GL(n,K) \to K^\times / [K^\times, K^\times] $$

## The quaternionic case

In the quaternionic case we have a further group isomorphism 

$$ \mathbb{H}^\times / [\mathbb{H}^\times, \mathbb{H}^\times] \to \mathbb{R}_{\gt 0} $$

where $\mathbb{R}_{\gt 0}$ is made into a group using multiplication, coming from the fact that $[\mathbb{H}^\times, \mathbb{H}^\times ] $ is the group of quaternions $q$ with $|q| = 1$, and any invertible quaternion can uniquely be written as $a q$ where $a \in \mathbb{R}_{\gt 0}$ and $|q| = 1$.  Thus, in this case we can write the Dieudonné determinant more concretely as a group homomorphism

$$ det \colon GL(n,\mathbb{H}) \to \mathbb{R}_{\gt 0} $$

Furthermore, for $n \times n$ quaternionic matrix $T$ of that is not invertible, we can define $det(T) = 0$, thus extending the Dieudonné determinant to a map

$$ det \colon M_n(\mathbb{H}) \to \mathbb{R}_{\ge 0} $$

where $\mathrm{M}_n(\mathbb{H})$ is the algebra of $n \times n$ matrices with quaternion entries.   This is a monoid homomorphism:

$$  det(S T) = det(S) det(T), \qquad det(1) = 1 $$

##  Relation to the Study determinant

There is another determinant for quaternionic matrices, the **Study determinant**, defined as follows.  Any matrix $T \in \mathrm{M}_n(\mathbb{H})$ determines by right multiplication a morphism of left $\mathbb{H}$-modules $T \colon \mathbb{H}^n \to \mathbb{H}^n$.  Choosing any element $i \in \mathbb{H}$ with $i^2 = -1$ gives $\mathbb{H}^n$ the structure of a left $\mathbb{C}$-module: indeed, a complex vector space of dimension $2n$.  In this way we can identify $T \colon \mathbb{H}^n \to \mathbb{H}^n$ with a complex-linear transformation of a complex vector space, and define its determinant in the usual way for such a transformation.  This determinant turns out not to depend on the choice of $i \in \mathbb{H}$ with $i^2 = -1$, and it is called the **Study determinant** $sdet(T)$.   It clearly obeys

$$  sdet(S T) = sdet(S) sdet(T), \qquad sdet(1) = 1 $$

*A priori* it is complex-valued, but in fact one can show (see Aslaksen's paper below) that

$$ sdet(T) = det(T)^2 $$

where the determinant at right is the Dieudonné determinant.   Thus in fact the Study determinant of an $n \times n$ quaternionic matrix defines a monoid homomorphism

$$ det \colon GL(n,\mathbb{H}) \to \mathbb{R}_{\gt 0} $$

which contains exactly as much information as the Dieudonné determinant.

##  Applications 

The [[special linear group]] $\mathrm{SL}(n,\mathbb{H})$ over the [[quaternions]] is defined to be the group of $n \times n$ quaternionic matrices for which the Dieudonné determinant equals 1, or equivalently for which the Study determinant equals 1.   Though it is not immediately obvious, any quaternionic unitary matrix has Dieudonné determinant 1.  Thus the [[quaternionic unitary group]] is a subgroup of $\mathrm{SL}(n,\mathbb{H})$.   So, unlike the real and complex cases, there is no additional concept of "special unitary group" in the quaternionic case.

## References

The concept is due to

* [[Jean Dieudonné]], _Les déterminants sur un corps non commutatif_,  Bulletin de la Société Mathématique de France, Volume 71  (1943), p. 27-45  ([numdam:BSMF_1943__71__27_0](http://www.numdam.org/item/?id=BSMF_1943__71__27_0)) 

Exposition and review:

* Helmer Aslaksen, _Quaternionic determinants_,  The Mathematical Intelligencer 18, 57–65 (1996) ([doi:10.1007/BF03024312](https://doi.org/10.1007/BF03024312), [pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.65.877&rep=rep1&type=pdf))

See also:

* Wikipedia, _[Dieudonné determinant](https://en.wikipedia.org/wiki/Dieudonn%C3%A9_determinant)_

Further discussion:

* {#CohenDeLeo99} Nir Cohen, Stefano De Leo, _The quaternionic determinant_, El. J. Lin. Alg. 7, 100-111 (2000) ([arXiv:math-ph/9907015](https://arxiv.org/abs/math-ph/9907015))

* [[Nigel Hitchin]], _$SL(2)$ over the octonions_ ([arXiv:1805.02224](https://arxiv.org/abs/1805.02224))


[[!redirects Dieudonné determinants]]
[[!redirects Dieudonne determinant]]
[[!redirects Dieudonne determinants]]
