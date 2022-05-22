
> Not to be confused with the [[Hurwitz theorem]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The first nonzero [[homotopy group]] and [[ordinary homology|ordinary]]/[[singular homology]] [[homology group|group]] of a [[simply-connected topological space]] occur in the same dimension and are [[isomorphism|isomorphic]].


## Hurewicz homomorphism
 {#HurewiczHomomorphismSection}

### For topological spaces

+-- {: .num_defn #HurewiczHomomorphism}
###### Definition 
**(Hurewicz homomorphism)**

For $(X,x)$ a [[pointed object|pointed]] [[topological space]], the **Hurewicz homomorphism** is the [[function]]

$$
  \Phi : \pi_k(X,x) \to H_k(X)
$$

from the $k$th [[homotopy group]] of $(X,x)$ to the $k$th [[singular homology]] group defined by sending

$$
  \Phi : (f : S^k \to X)_{\sim} \mapsto f_*[S_k]
$$

a representative singular $k$-sphere $f$ in $X$ to the push-forward along $f$ of the [[fundamental class]] $[S_k] \in H_k(S^k) \simeq \mathbb{Z}$.


=--

+-- {: .num_remark}
###### Remark

The Hurewicz homomorphism is a [[natural transformation]] between

$$
  \Phi : \pi_k(-) \to H_k(-)
$$

between [[functors]] $Top^{*/} \to $ [[Ab]].

=--

### For spectra
 {#ForSpectra}

The above construction has an immediate analog in [[stable homotopy theory]]:

For $R$ a [[ring]], its [[Eilenberg-MacLane spectrum]] is an [[E-infinity ring]] and hence receives a canonical [[unit]] homomorphism $\mathbb{S} \longrightarrow H R$ from the [[sphere spectrum]].

Under [[smash product]] and passing to [[stable homotopy group]], this induces a [[natural transformation]] from [[stable homotopy groups]] of $X$ (its [[stable homotopy homology theory]]) to [[ordinary homology]] of $X$ with [[coefficients]] in $R$:

$$
  \pi^{st}_\bullet(X)
  \;\simeq\;
  \pi_\bullet( \mathbb{S} \wedge X_+ )
  \longrightarrow
  \pi_\bullet( H R \wedge X_+ )
  \simeq
  H_\bullet(X,R)
  \,.
$$

If here the [[Eilenberg-MacLane spectrum]] $H R$ is replaced by any other [[E-infinity ring spectrum]] the analogous construction is called the _[[Boardman homomorphism]]_.


## Hurewicz theorem
 {#HurewiczTheorem}

In general, [[homology theory|homology]] is a coarser invariant than [[homotopy type|homotopy]], and [[ordinary homology]] is the coarsest of all [[generalized homology]]-invariants. Therefore the Hurewicz homomorphism (Def. \ref{HurewiczHomomorphism}) is bound to lose information, in general. 

Indeed, the Hurewicz homomorphism exhibits a kind of abelianization of the [[homotopy type]] (in the sense of [[stable homotopy theory]], see at *[[Boardman homomorphism]]* for more on this), a statement that in low degrees is true in the plain sense of *[[abelianization]]*: this is the content of Prop. \ref{HurewiczTheoremInDegreeZero} and Prop. \ref{HurewiczTheoremInDegreeOne} below.

While in higher degrees the Hurewicz homomorphism is in general far from being an isomorphism, the thrust of the Hurewicz theorem is to show that high connectivity is a sufficient condition to ensure that it is. This is Theorem \ref{HurewiczTheoremInDegreeTwoAndHigher} below.



\begin{proposition}\label{HurewiczTheoremInDegreeZero}
**(in degree 0)**
\linebreak
For $X$ a topological space, the Hurewicz homomorphism (Def. \ref{HurewiczHomomorphism}) in degree 0 exhibits an [[isomorphism]] between the [[free abelian group]] $\mathbb{Z}[\pi_0(X)]$ on the set of [[connected components]] of $X$ and the degree-0 singular homlogy:

$$
  \mathbb{Z}[\pi_0(X)]
   \simeq
  H_0(X)
  \,.
$$

\end{proposition}


Since a [[homotopy group]] in [[positive number|positive]] degree depends on the [[homotopy type]] of the [[connected component]] of the base point, while the [[ordinary homology]] does not depend on a basepoint, it is interesting to compare these groups only for the case that $X$ is connected:

\begin{proposition}\label{HurewiczTheoremInDegreeOne}
**(in degree 1)**
\linebreak
For $X$ a [[connected topological space]] the [[Hurewicz homomorphism]] (Def. \ref{HurewiczHomomorphism})
in degree 1

$$
  \Phi \colon \pi_1(X,x) \longrightarrow H_1(X)
$$

is [[surjection|surjective]]. Its [[kernel]] is the [[commutator subgroup]]
of $\pi_1(X,x)$. Therefore it induces an [[isomorphism]] from the [[abelianization]] $\pi_1(X,x)^{ab} \coloneqq \pi_1(X,x)/[\pi_1,\pi_1]$:


$$
  \pi_1(X,x)^{ab}
  \overset{\simeq}{\longrightarrow}
  H_1(X)
  \,.
$$

\end{proposition}



\begin{theorem}\label{HurewiczTheoremInDegreeTwoAndHigher}
**(in degree $\geq 2$)**
\linebreak
If a [[topological space]] (or [[infinity-groupoid]]) $X$ is [[n-connected object in an (infinity,1)-topos|(n-1)-connected]] for $n \geq 2$ then the [[Hurewicz homomorphism]], Def. \ref{HurewiczHomomorphism} 

$$
  \Phi  
  \;\colon\; 
  \pi_n(X,x) 
    \longrightarrow 
  H_n(X)
$$

is an [[isomorphism]].

\end{theorem}

A proof is spelled out for instance with theorem 2.1 in ([Hutchings](#Hutchings)).

+-- {: .num_remark}
###### Remark

With the [[universal coefficient theorem]] a corresponding statement follows for the [[cohomology group]] $H^n(X,A)$.

=--


## Related concepts

* [[Boardman homomorphism]]

* [[Hopf degree theorem]]

* The _[[Adams spectral sequence]]_ is a vast generalization of the computation of [[homotopy groups]] from [[cohomology groups]] via the Hurewicz theorem.


## References

The original reference is:

* [[Witold Hurewicz]], Koninklijke Akademie van Wetenschappen: Proceedings of the Section of Sciences 38 (1935), 112–119.  Mathematics. — Beiträge zur Topologie der Deformationen (I. Höherdimensionale Homotopiegruppen).  $[$[gbooks](https://books.google.ru/books/about/Beitr%C3%A4ge_zur_Topologie_der_Deformatione.html?id=lge_ygAACAAJ&redir_esc=y)$]$

This article is reproduced on pages 341–348 of

* [Collected Works of Witold Hurewicz](https://bookstore.ams.org/cworks-4).  (Edited by Krystyna Kuperberg.)  American Mathematical Society, 1995.  ISBN 0-8218-0011-6

The [[simplicial homotopy theory|simplicial]] version is due to

* [[Daniel M. Kan]],  _The Hurewicz theorem_, 1958 Symposium internacional de topología algebraica (International symposium on algebraic topology), pp. 225–231 Universidad Nacional Autónoma de México and UNESCO, Mexico City.

The basic statement is for instance in

* [[Allen Hatcher]], _Algebraic Topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html))

Lecture notes:

* {#Hutchings} [[Michael Hutchings]], _Introduction to higher homotopy groups and obstruction theory_ (2011) ([pdf](http://math.berkeley.edu/~hutching/teach/215b-2011/homotopy.pdf))

* {#Kobin16} Andrew Kobin, Section 7.3 of: _Algebraic Topology_, 2016 ([[KobinAT2016.pdf:file]])

For discussion in [[stable homotopy theory]] modeled on [[symmetric spectra]] is in 

* {#Schwede12} [[Stefan Schwede]], part II, prop. 6.30 of _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

See also

* wikipedia, _[Hurewicz theorem](http://en.wikipedia.org/wiki/Hurewicz_theorem)_

In the generality of the [[Boardman homomorphism]]:

* [[Frank Adams]], Part II.6 of _[[Stable homotopy and generalised homology]]_, 1974

Discussion of the stable Hurewicz homomorphism includes

* [[Akhil Mathew]], _Torsion exponents in stable homotopy and the Hurewicz homomorphism_, Algebr. Geom. Topol. 16 (2016) 1025-1041 ([arXiv:1501.07561](https://arxiv.org/abs/1501.07561))

Proof of the [[Hurewicz theorem]] in [[homotopy type theory]], hence in general [[(∞,1)-toposes]]:

* [[Daniel Christensen]], [[Luis Scoccola]], _The Hurewicz theorem in Homotopy Type Theory_ ([arXiv:2007.05833](https://arxiv.org/abs/2007.05833))



[[!redirects Hurewicz theorem]]
[[!redirects Hurewicz Theorem]]
[[!redirects Hurewicz' theorem]]
[[!redirects Hurewicz' Theorem]]
[[!redirects Hurewicz’ theorem]]
[[!redirects Hurewicz’ Theorem]]
[[!redirects Hurewicz\' theorem]]
[[!redirects Hurewicz\' Theorem]]
[[!redirects Hurewicz's theorem]]
[[!redirects Hurewicz's Theorem]]
[[!redirects Hurewicz’s theorem]]
[[!redirects Hurewicz’s Theorem]]
[[!redirects Hurewicz\'s theorem]]
[[!redirects Hurewicz\'s Theorem]]

[[!redirects Hurewicz homomorphism]]
