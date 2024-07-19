## Idea

Rational function over an associative $k$-algebra $R$ should be a class of expressions involving operations in noncommutative polynomial ring combined with the operation of formal inverse modulo which are evaluable for at least at some choice of variables in $R$ in a chosen associative algebra modulo identities which are true after evaluation at common evaluation points. 

## Definitions

The division ring of __noncommutative rational functions__ on a given alphabet is defined in Cohn's book essentially as follows.

### Noncommutative rational expressions

Given a commutative field $k$
("field of constants"), and a finite set $X = \{x_1,\ldots,x_n\}$ ("alphabet"),
consider the free algebra on $X$ (in the sense of universal algebra)
of signature $\{ +_2, \cdot_2, (\,)^{-1}_1, -_1\}$
and with constants in $k$ and denote it by $\mathcal{R}(X,k)$.
Expressions like $0^{-1}$ and $(x-x)^{-1}$ are in $\mathcal{R}(X,k)$
as no relations are imposed (one starts with terms which are elements
of $X\cup k$ and continues by nesting sequence of algebraic
operations eventually connecting all terms). 
The elements of $\mathcal{R}(X,k)$ are sometimes called noncommutative rational expressions on alphabet $X$.

Let $R$ be an associative $k$-algebra, and $\phi : X\to R$
a map of sets. Then there is
a subset $\mathcal{R}_\phi \subset \mathcal{R}(X,k)$ (of $\phi$-"evaluables") and a map $\phi_* : \mathcal{R}_\phi\to R$ uniquely determined by the rules

* (constants evaluate) If $c \in k$ then $c \in \mathcal{R}_\phi$
and $\phi_*(c) = c$.

* (variables evaluate) If $x \in X$ then $x \in \mathcal{R}_\phi$
and $\phi_*(x) = \phi(x)$.

* (sums, products and negatives of evaluables evaluate)
If $f, g \in\mathcal{R}_\phi$, then $f+g, f\cdot g, -f \in\mathcal{R}_\phi$,
$\phi_*(f+g) = \phi_*(f) + \phi_*(g)$, $\phi_*(f\cdot g) =
\phi_*(f)\cdot\phi_*(g)$ and $\phi_*(-f) = -\phi_*(f)$.

* If $g \in \mathcal{R}_\phi$, and $\phi_*(g)$ is invertible in $R$,
then $g^{-1}\in \mathcal{R}_\phi$ and $\phi_*(g^{-1}) = \phi_*(g)^{-1}$.

### Domains

For every $f \in \mathcal{R}(X,k)$ define $\mathrm{Dom}\,f$ to be the
set of all $|X|$-tuples $\vec{r} = (r_1,\ldots,r_{|X|}) \in R^{|X|}$
such that $f \in \mathcal{R}_\phi$ where $\phi = \phi_{\vec{r}}$ satisfies
$\phi(x_i) = r_i$ for $i = 1,\ldots, |X|$. Those $f$ for which
$\mathrm{Dom} f \neq \emptyset$ are called nondegenerate. It is clear
that $f \notin\mathcal{R}_\phi$ iff there is a subexpression in $f$ of the form
$(f_0)^{-1}$ where $f_0 \in \mathcal{R}_\phi$ and $\phi_*(f_0)$ is not invertible in $R$. 

### Equivalence of expressions

Two rational expressions with nonempty domains are equivalent if their domains have nonempty intersection and their evaluations agree at the intersection of domains, i.e. $f\sim g$ if
$\forall\vec{r}\in Dom\,f\cap Dom\,g$ $\phi_{\vec{r}*}(f) = \phi_{\vec{r}*}(g)$.

### Noncommutative rational functions

The equivalence classes of noncommutative rational expressions with nonempty domain are called noncommutative rational functions in variables in $X$ of $k$-algebra $R$. The domain of a rational function is the union of domains of all its representatives. If $k$ is an infinite field and under some conditions on $R$, noncommutative rational functions in alphabet $X$ over algebra $R$ naturally form a [[division ring]] (skewfield). 

### Free skewfield

If $R$ is the matrix ring $M_n(k)$ then all noncommutative rational functions in alphabet $X$ form a skewfield traditionally denoted by $k\lt\!\!\!\!\!(\,X\!\!\gt\!\!\!\!\!)$. It is the universal field of fractions of the noncommutative polynomial ring $k[X]$.

Amitsur considered instead $R = D$ where $D$ is any skewfield which is infinite-dimensional over its center $Z(D)$, where $Z(D)$ is infinite as well. He obtained the universal field of fractions which does not depend on $D$ in this construction either. 

## Properties

Cohn proved that if in the free skewfield any full matrix is invertible. An $n\times n$ matrix $A$ is full if it can not be factorized as $A_1 A_2$ where $A_1$ is $n\times r$, $A_2$ is $r\times n$ and $r\lt n$.

## Literature

__Noncommutative rational identities__ are formally studied in

* [[Shimshon Amitsur|S. A. Amitsur]], _Rational identities and application to algebra and geometry_, J. Alg. __3__ (1966) 304--359.
* [[P. M. Cohn]], _Free rings and their relations_, Academic Press 1971. 
* [[George M. Bergman]], _Rational relations and rational identities in division rings. I_, J. Algebra __43__ (1976) 252--266

The division ring of noncommutative rational functions on a given alphabet is defined in Cohn's book.

* [[George M. Bergman]], _Skew fields of noncommutative rational functions, after Amitsur_. In Séminaire Schützenberger–Lentin–Nivat, Année 1969/1970, No. 16. Paris 1970 [EuDML](http://eudml.org/doc/112813)
* [[P. M. Cohn]], _Universal skew fields of fractions_, Symposia in Mathematics __8__ (1972) 135--148
* C. Reutenauer, _Inversion heights of free fields_, Selecta Mathematica, N. S. __2__:1 (1996) 93--109 [pdf](https://reutenauer.math.uqam.ca/wp-content/uploads/2024/04/Inversion-height.pdf)
* [[I. M. Gel'fand]], [[V. Retakh|V. S. Retakh]], _Determinants of matrices over noncommutative rings_, Funkc. Anal. Pril. __25__:2 (1991) 91--102; engl. transl. Funct. Anal. Appl. __21__(1991) 51--58; _A theory of noncommutative determinants and characteristic functions of graphs_, Funkc. Anal. Pril. __26__:4 (1992) 231--246.
* [[Zoran Škoda]], _Universal noncommutative flag variety_, preprint (the exposition above is mainly taken from here)
* Daniel Krob, _Expressions rationelles sur un anneau_, in Marie-Paule Malliavin, Topics in invariant theory, Springer LNM 1478

Relation to free Lie algebras is in

* A. I. Lichtman, _On universal fields of fractions for
free algebras_, J. Alg. 231 (2000) 652--676 [doi](https://doi.org/10.1006/jabr.2000.8344)

It is used in the study of [[skewfield]]s, [[Cohn localization]], [[quasideterminant]]s, noncommutative integrable systems and so on.

* Natalia Iyudu, Stanislav Shkarin, _A proof of the Kontsevich periodicity conjecture_, Duke Math. J. 164, no. 13 (2015) 2539--2575 [doi](https://doi.org/10.1215/00127094-3146603) [arXiv:1305.1965](https://arxiv.org/abs/1305.1965)

* [[M. Kontsevich]], _Noncommutative identities_, writeup of the 2011 MPIM Bonn Arbeitstagung talk, [arXiv:1109.2469](https://arxiv.org/abs/1109.2469)

category: algebra
[[!redirects noncommutative rational functions]]
[[!redirects noncommutative rational identity]]
[[!redirects noncommutative rational identities]]