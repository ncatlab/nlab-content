
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _conformal compactification_ is an [[embedding]] of a non-[[compact topological space|compact]] [[Lorentzian manifold]] into a [[compact]] Lorentzian manifold as a [[dense subspace|dense]] [[open subset|open]] [[subspace]], such that the embedding is a [[conformal map]] .

## Example

The (or rather, _any_) conformal compactification $\overline{M}$ of (flat) [[Minkowski space]] $M = \mathbb{R}^{n,1}$ is important in various treatments of behaviour at infinity of physics thereon (see e.g. _[[Penrose-Hawking theorem]]_).

Section 4.2 of [Nikolov & Todorov 2004](#NikolovTodorov04) gives a thorough geometric discussion of the construction and gives explicit expressions in coordinates, and shows that (the underlying manifold of) this $\overline{M}$ is in fact $(S^n \times S^1)/\{\pm 1\}$, for a specific embedding of $S^n\times S^1$ in $\mathbb{R}^{n+1,2}$, and the action by scalar multiplication.

Let $q(x,t)$ be the standard indefinite quadratic form of signature $(n,1)$ on $\mathbb{R}^{n,1}$ and define the following map $\mathbb{R}^{n,1} \to \mathbb{R}^{n+1,2} \simeq \mathbb{R}^{n,1}\times \mathbb{R}^{1,1}$:
$$
\tilde{C}\colon (x,t) \mapsto (x,t,\frac{1-q(x,t)}{2},\frac{-1-q(x,t)}{2})
$$
This is a diffeomorphism on its image, which can be described as the intersection of the hyperplane $v-w=1$ and the quadric $q(x,t) + q'(v,w)=0$, where $(v,w)$ are coordinates on $\mathbb{R}^{1,1}$ with the quadratic form $q'(v,w) = v^2-w^2$. In particular, the image of this map avoids the origin in $\mathbb{R}^{n+1,2}$, and rearranging the defining equation for the quadric we get $|x|^2 + v^2 = t^2 + w^2$ $=K$, say, where $K\neq 0$. We can then scale $\tilde{C}(x,t)$ to $C(x,t)$ so that $K=1$, which means $C(x,t) \in S^n\times S^1$. [TODO: calculate this normalisation] Then the final quotient by $\{\pm 1\}$ gives the desired dense embedding $\mathbb{R}^{n,1} \to (S^n\times S^1)/\{\pm 1\}$.

One could also skip the normalisation step if desired, and pass directly to the quotient by $\mathbb{R}^\times \simeq \mathbb{R}_{\gt0}^* \times \{\pm 1\}$, treating $\tilde{C}(x,t)$ as homogeneous coordinates.



The blog post ([Wong 2009](#Wong09))) gives a discussion of comformal compactification in general, with Minkowski space as an example. It describes the underlying manifold of (the 'usual' construction of) $\overline{M}$ is $S^n\times S^1$, but then clarifies that this is a 'double cover'.

A conformal compactification, of _complexified_ [[Minkowski spacetime]] $\mathbb{R}^{3,1}$, is given by the [[Klein quadric]]. (eg, [Fioresi-Lledo-Varadarajan 07, section 2](#FioresiLledoVaradarajan07)). This plays a key role in the _[[twistor correspondence]]_.

## Related entries

* [[conformal geometry]]

* [[compactification]]

* [[asymptotically flat spacetime]]

## References

* [[Roger Penrose]], _Relativistic Symmetry Groups_, in A.O.Barut (ed.), _Group Theory in Non-Linear Problems: Lectures Presented at the NATO Advanced Study Institute on Mathematical Physics_  (1974)

* Valentina, _Conformal compactifications_ &lbrack;[[Valentina-ConformalCompactifications.pdf:file]]&rbrack; 

* Jörg Frauendiener, *Conformal Infinity*,  Living Rev. Relativ. **7** 1 (2004) &lbrack;[doi:10.12942/lrr-2004-1](https://doi.org/10.12942/lrr-2004-1)&rbrack;


* {#NikolovTodorov04} Nikolay M. Nikolov, [[Ivan T. Todorov]], §4.2 in: *Lectures on Elliptic Functions and Modular Forms in Conformal Field Theory*, in: *[Modern Mathematical Physocs](https://inspirehep.net/literature/885417)*, Proceedings of: *[3rd Summer School in Modern Mathematical Physics (MPHYS3)](https://inspirehep.net/conferences/976156)* (2004) 1-93 &lbrack;[arXiv:math-ph/0412039](http://arxiv.org/abs/math-ph/0412039), [InSpire:674206](https://inspirehep.net/literature/674206)&rbrack;

* {#FioresiLledoVaradarajan07} Rita Fioresi, Maria A. Lledo, [[Veeravalli Varadarajan]], _The Minkowski and conformal superspaces_, J. Math. Phys. **48** (2007) 113505 &lbrack;[arXiv:math/0609813](https://arxiv.org/abs/math/0609813), [doi:10.1142/8972](https://doi.org/10.1142/8972)&rbrack;

* {#Wong09} Willie Wong, _Conformal compactification of space-time_ ([web](https://qnlw.info/post/conformal-compactification-spacetime/)) (2009).

* {#Frances11} [[Charles Frances]], *The conformal boundary of anti-de Sitter space-times*, in: *AdS/CFTCorrespondence: Einstein Metrics and Their Conformal Boundaries*, IRMA Lectures in Mathematical and Theoretical Physics, EMS (2011) 205-216 &lbrack;[ems:irma/9/206](https://ems.press/books/irma/9/206), [hal:03195056](https://hal.science/hal-03195056), [pdf](https://hal.science/hal-03195056v1/document)&rbrack;

[[!redirects conformal compactifications]]

[[!redirects conformal boundary]]


[[!redirects conformal boundaries]]



