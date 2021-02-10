

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

The _Dieudonné determinant_ is a variant of the notion of [[determinant]] which applies to [[matrices]] with values in [[division rings]], such as the [[quaternions]]. It is crucial for making sense of the notion of "[[special linear group]]" over such coefficients, such as the group [[SL(2,H)]] over the [[quaternions]] 

## Definition

[Dieudonné 43](#Dieudonne) showed that for $K$ a [[division ring]], there is a [[group homomorphism|group]] [[isomorphism]] of the form

\[
  \label{TheGroupIsomorphism}
  \alpha 
    \;\colon\;
  GL(n,K)/[GL(n,K), GL(n,K)] 
   \xrightarrow{\;\;\sim\;\;} 
  K^\times/[K^\times, K^\times] 
  \,,
\]

where 

* $GL(n,K)$ is the [[group]] of $n \times n$ [[invertible  matrices]] with entries in $K$, 

* $K^\times = GL(1,K)$ is the [[group of units]] of $K$, 

* and $G/[G,G]$ is the [[abelianization]] of the group $G$.  

Moreover, this group isomorphism (eq:TheGroupIsomorphism)
is uniquely determined by the following properties:

* If a row of the matrix $T$ is left multiplied by $a \in K^\times$ then $\alpha(T)$ is left multiplied by $[a] \in K^\times/[K^\times K^\times]$.

* If a multiple of one row of $T$ is added to another row of $T$, then $\alpha(T)$ is unchanged.

* If two consecutive rows of $T$ are exchanged, then $\alpha(T)$ is multiplied by $[-1] \in K^\times/[K^\times, K^\times]$.

Composing the isomorphism $\alpha$ (eq:TheGroupIsomorphism)
with the [[quotient]] [[coprojection]] 

$$
  q
    \,\colon\,
  GL(n,K) 
    \longrightarrow 
  GL(n,K) / [GL(n,K), GL(n,K)]
$$

gives the **Dieudonné determinant**

\[
  \label{TheDieudonneDeterminant}
  det_{Dieu}
  \,\coloneqq\,
  q \circ \alpha
   \;\colon\; 
  GL(n,K) 
   \longrightarrow
  K^\times / [K^\times, K^\times]
  \,. 
\]

## The quaternionic case

In the case that $K = \mathbb{H}$ is the [[quaternions]],  we have a further group isomorphism 

$$ 
  \mathbb{H}^\times 
  / 
  [
    \mathbb{H}^\times, 
    \mathbb{H}^\times
  ] 
   \longrightarrow
 \mathbb{R}_{\gt 0} 
$$

where $\mathbb{R}_{\gt 0}$ is made into a group using [[multiplication]] of [[real numbers]], coming from the fact that now the [[commutator subgroup]] $[\mathbb{H}^\times, \mathbb{H}^\times] $ is the group [[Sp(1)]] of unit quaternions $q$ with $|q| = 1$, and that any invertible quaternion can uniquely be written as $a q$ where $a \in \mathbb{R}_{\gt 0}$ and $\left\vert q \right\vert = 1$.  

Thus, in this case we can write the Dieudonné determinant (eq:TheDieudonneDeterminant)
more concretely as a [[group homomorphism]] of the form

$$ 
  det_{Dieu} 
    \,\colon\, 
  GL(n,\mathbb{H}) 
    \longrightarrow 
  \mathbb{R}_{\gt 0} 
  \,.
$$

Furthermore, for any $n \times n$ quaternionic matrix $T$ that is not invertible, setting $det(T) \coloneqq 0$  [[extension|extends]] the Dieudonné determinant to a [[function]] of the form

\[
  \label{DieudonneDetOverQuaternions}
  det_{Dieu} 
    \;\colon\;
  M_n(\mathbb{H}) 
    \longrightarrow 
  \mathbb{R}_{\ge 0} 
  \,,
\]

where $\mathrm{M}_n(\mathbb{H})$ is now the full [[matrix algebra]] of $n \times n$ matrices with [[quaternion]] entries.  This function (eq:DieudonneDetOverQuaternions) is a [[monoid]] [[homomorphism]], in that:

\[
  \label{QuaternionicDieudonneIsMonoidHomomorphism}
  det_{Dieu}(S T) 
    \,=\,
  det_{Dieu}(S) 
  det_{Dieu}(T), 
   \qquad 
  det_{Dieu}(1) = 1 
  \,.
\]

##  Relation to the Study determinant

There is another notion of determinant for [[quaternion|quaternionic]] [[matrices]], the **Study determinant**, defined as follows:

 Any matrix $T \in \mathrm{M}_n(\mathbb{H})$ determines by right multiplication a [[homomorphism]] of left $\mathbb{H}$-[[modules]] $T \colon \mathbb{H}^n \to \mathbb{H}^n$.  Choosing any element $i \in \mathbb{H}$ with $i^2 = -1$ gives $\mathbb{H}^n$ the structure of a left $\mathbb{C}$-module: indeed, a [[complex vector space]] of dimension $2n$.  In this way we can identify $T \colon \mathbb{H}^n \to \mathbb{H}^n$ with a [[complex numbers|complex]]-[[linear transformation]] of a complex vector space, and define its [[determinant]] in the usual way for such a transformation.  

This determinant turns out not to depend on the choice of $i \in \mathbb{H}$ with $i^2 = -1$, and it is called the **Study determinant** $sdet(T)$.  

It clearly obeys

$$  sdet(S T) = sdet(S) sdet(T), \qquad sdet(1) = 1 
  \,.
$$

*A priori* this is complex-valued, but in fact one can show (see [Arlaksen 96](#Arlaksen96)) that

$$ 
  sdet(T) = det_{Dieu}(T)^2 
  \,,
$$

where the determinant on the right is the Dieudonné determinant (eq:DieudonneDetOverQuaternions), and hence real-valued.   

Thus, by (eq:QuaternionicDieudonneIsMonoidHomomorphism), also the Study determinant on $n \times n$ quaternionic matrices defines a monoid homomorphism

$$ 
  sdet 
    \;\colon\;
  GL(n,\mathbb{H}) 
   \longrightarrow 
  \mathbb{R}_{\gt 0} 
$$

which contains exactly as much information as the Dieudonné determinant.

##  Applications 

The [[special linear group]] $\mathrm{SL}(n,\mathbb{H})$ over the [[quaternions]] (e.g. [[SL(2,H)]]) is defined to be the group of $n \times n$ quaternionic matrices for which the Dieudonné determinant equals 1, or equivalently for which the Study determinant equals 1.  

Though it is not immediately obvious, any quaternionic unitary matrix has Dieudonné determinant 1.  Thus the [[quaternionic unitary group]] [[Sp(n)]] is a subgroup of $\mathrm{SL}(n,\mathbb{H})$.  

Therefore, unlike the real and complex cases, there is no additional concept of "special unitary group" in the quaternionic case.

## References

The concept is due to

* {#Dieudonne43}  [[Jean Dieudonné]], _Les déterminants sur un corps non commutatif_,  Bulletin de la Société Mathématique de France, Volume 71  (1943), p. 27-45  ([numdam:BSMF_1943__71__27_0](http://www.numdam.org/item/?id=BSMF_1943__71__27_0)) 

Exposition and review:

* {#Arlaksen96} Helmer Aslaksen, _Quaternionic determinants_,  The Mathematical Intelligencer 18, 57–65 (1996) ([doi:10.1007/BF03024312](https://doi.org/10.1007/BF03024312), [pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.65.877&rep=rep1&type=pdf))

See also:

* Wikipedia, _[Dieudonné determinant](https://en.wikipedia.org/wiki/Dieudonn%C3%A9_determinant)_

Further discussion:

* {#CohenDeLeo99} Nir Cohen, Stefano De Leo, _The quaternionic determinant_, El. J. Lin. Alg. 7, 100-111 (2000) ([arXiv:math-ph/9907015](https://arxiv.org/abs/math-ph/9907015))

* [[Nigel Hitchin]], _$SL(2)$ over the octonions_ ([arXiv:1805.02224](https://arxiv.org/abs/1805.02224))


[[!redirects Dieudonné determinants]]
[[!redirects Dieudonne determinant]]
[[!redirects Dieudonne determinants]]
