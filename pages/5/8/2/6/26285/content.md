
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[quadratic form|quadratic]]/[[Hermitian forms]] and in particular of [[Hermitian K-theory]], by the *hyperbolic functor* one refers to the construction which sends a [[module]] $\mathscr{V}$ over a given ([[star-algebra|star]]-)[[ground ring]] $R$ to its [[direct sum]] 
$$
  \mathscr{V}
  \;\mapsto\;
  H(\mathscr{V})
  \;\coloneqq\;
  \mathscr{V}
  \oplus
  \mathscr{V}^\ast
$$
with its  ([[anti-dual linear space|anti]]-)[[linear dual]] and then equipped with the ([[sesquilinear form|sesqui]]- or) [[bilinear form]]

$$
  \array{
    H(\mathscr{V})
    \otimes
    H(\mathscr{V})
    &\longrightarrow&
    R
  }
$$
which on the mixed summands is (the [[complex conjugation|conjugation]] of) the [[evaluation]] map
$$
  \mathscr{V} \otimes \mathscr{V}^\ast
  \longrightarrow
  R
$$
and vanishing on the homogeneous summands.

This construction extends to [[functor]] from the [[core groupoid]] [[Mod|of $R$-modules]] to that of [[inner product spaces]] with [[isometries]] between them, by sending an [[isomorphism]] $\phi \colon \mathscr{V} \overset{\sim}{\to} \mathscr{W}$ to its [[direct sum]] with the [[dual linear map]] of its [[inverse morphism|inverse]]:

$$
  \phi \,\mapsto\, \phi \oplus (\phi^{-1})^\ast
  \,.
$$

Regarded with suitable $\mathbb{Z}/2 \times \mathbb{Z}/2$-[[equivariant homotopy theory|equivariance]], the hyperbolic functor establishes an equivalence between [[KR-theory]] and [[topological Hermitian K-theory]] (see the references [there](Hermitian+K-theory#ReferencesTopologicalHermitianKTheory)).


## Example

\begin{example}
  In the simple special case that the [[ground ring]] is the [[real numbers]] $\mathbb{R}$ and $\mathscr{V}$ is also $\mathbb{R}$, regared as the 1-dimensional [[vector space]] over itself, and finally identifying $\mathbb{R}^\ast \simeq \mathbb{R}$, canonically, the hyperbolic construction on $\mathbb{R}$ is the [[plane]] $\mathbb{R}^2 = \mathbb{R} \oplus \mathbb{R}$ equipped with its standard [[Minkowski metric]]. 

Here the subspaces of fixed non-vanishing [[norm]] are the usual [[hyperbolas]]. This gives the name "hyperbolic form" to all modules of the above form $\mathscr{V} \oplus \mathscr{V}^\ast$.
\end{example}

## References


The term "hyperbolic functor" seems to originate with:

* [[Hyman Bass]] (notes by Amit Roy), §5.2 in: *Lectures on Topics in Algebraic K-Theory*, Tata Institute of Fundamental Research (1965) &lbrack;[[Bass-HyperbolicFunctor.pdf:file]]&rbrack;

See also:

* {#Wall69} [[C. T. C. Wall]] (ed. [[Andrew Ranicki]]), p. 177 of: *Surgery on compact Manifolds*, Math. Surveys and Monographs **69** (1969) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/books/scm.pdf)&rbrack;

Further discussion in the context of [[Hermitian K-theory]]:

* [[Max Karoubi]], [[Orlando Villamayor]], p. 60 of *K-théorie algébrique et K-théorie topologique II*, Math. Scand. **32** (1973) 57-86 &lbrack;[jstor:24490565](https://www.jstor.org/stable/24490565)&rbrack;

* [[Max Karoubi]], pp. 307 (7 of 111) in: *Périodicité de la K-théorie hermitienne*, in: [[Hyman Bass]] (ed.), *Algebraic K-Theory III -- Hermitian K-Theory and Geometric Applications*, Lecture Notes in Mathematics **343** (1973) 301-411 &lbrack;[doi:10.1007/BFb0061366](https://doi.org/10.1007/BFb0061366)&rbrack;

* [[Anthony Bak]], §3 in: *Grothendieck Groups of Modules and Forms Over Commutative Orders*, American Journal of Mathematics, **99** 1 (1977) 107-120 &lbrack;[jstor:2374010](https://www.jstor.org/stable/2374010), [doi:10.2307/2374010](https://doi.org/10.2307/2374010)&rbrack;

See also:

* [[Richard Elman]], [[Nikita Karpenko]], [[Alexander Merkurjev]], p. 4 of: *Algebraic and Geometric Theory of Quadratic Forms*, Colloquium Publication **56**, AMS (2008) &lbrack;[ams:coll-56](https://bookstore.ams.org/coll-56), [pdf](https://www.math.ucla.edu/~rse/old_book/Kniga.pdf)&rbrack;

* [[Matthew B. Young]], p. 15 of: *Self-Dual Hall modules*, PhD thesis, Stony Brook (2013) &lbrack;[pdf](https://www.math.stonybrook.edu/alumni/2013-Matthew-Young.pdf), [[Young-HallModules.pdf:file]]&rbrack;

* [[Marco Schlichting]], p. 8 of: *Higher $K$-Theory of Forms I. From Rings to Exact Categories*, Journal of the Institute of Mathematics of Jussieu **20** 4 (2021) 1205-1273 &lbrack;[doi:10.1017/S1474748019000410](https://doi.org/10.1017/S1474748019000410)&rbrack;

[[!redirects hyperbolic functors]]

[[!redirects hyperbolic form]]
[[!redirects hyperbolic forms]]


