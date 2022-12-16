
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

\tableofcontents


## Idea

A **strict factorization system** is like an [[orthogonal factorization system]], but the factorizations are specified uniquely on the nose, rather than merely up to [[isomorphism]].

## Definition

A **strict factorization system** on a category $C$ comprises [[wide subcategories]] $E$ and $M$ of $C$ such that every morphism in $C$ factors as $m e$ for $e \in E$ and $m \in M$.

Note that a strict factorization system is not necessarily an [[orthogonal factorization system]], since $E$ and $M$ may not contain the isomorphisms in $C$. However, for every strict factorization system, there is a unique orthogonal factorization system containing it, given by closing $E$ under postcomposition by isomorphisms and closing $M$ under precomposition by isomorphisms (see §2.1 of [Grandis (2000)](#Grandis00)).

## As distributive laws in a bicategory

One reason strict factorization systems are of interest is that they can be identified with [[distributive laws]] in the [[bicategory]] of [[spans]], as shown by [Rosebrugh & Wood (2002)](#RosebrughWood02).

Ordinary orthogonal factorization systems can be similarly characterized by:

* using a type of relaxed [[distributive law]], as in [Rosebrugh & Wood (2002)](#RosebrughWood02);

* using [[wreaths]] as in [Lack & Street (2002)](#LackStreet02);

* by working in the [[bicategory]] of [[profunctors]] instead, as in [Lack (2004)](#Lack04) (see also [[factorization system over a subcategory]]); or by

* using [[weak distributive laws]], as in [Böhm (2012)](#Böhm12).

## References

Strict factorization systems were defined in:

* {#Grandis00} [[Marco Grandis]]. _Weak subobjects and the epi-monic completion of a category_. Journal of Pure and Applied Algebra 154.1-3 (2000): 193-212.

See also:

* {#RosebrughWood02} [[Robert Rosebrugh]], [[Richard J. Wood]], *Distributive Laws and Factorization*, Journal of Pure and Applied Algebra **175** 1–3 (2002) 327-353 &lbrack;<a href="http://dx.doi.org/10.1016/S0022-4049(02)00140-8">doi:10.1016/S0022-4049(02)00140-8</a>[pdf](http://www.mta.ca/~rrosebru/articles/fac.pdf)&rbrack;

* {#LackStreet02} [[Stephen Lack]], [[Ross Street]], *The formal theory of monads II*, J. Pure Appl. Alg. **175** 1–3 (2002) 243-265 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00137-8">doi:10.1016/S0022-4049(02)00137-8</a>&rbrack;

* {#Lack04} [[Stephen Lack]], *Composing PROPs*, Theory and Applications of Categories, **13** 9 (2004) 147-163 &lbrack;[tac:13-09](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html)&rbrack;

* {#Böhm12} [[Gabriella Böhm]], *Factorization systems induced by weak distributive laws*, Appl. Categ. Structures **20** 3 (2012) 275-302 &lbrack;[doi:10.1007/s10485-010-9243-y](https://doi.org/10.1007/s10485-010-9243-y), [arXiv:1009.0732](https://arxiv.org/abs/1009.0732)&rbrack;


[[!redirects strict factorization systems]]
[[!redirects strict factorisation system]]
[[!redirects strict factorisation systems]]

