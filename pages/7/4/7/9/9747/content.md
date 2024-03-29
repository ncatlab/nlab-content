__Noncommutative rational identities__ are formally studied in

* S. A. Amitsur, _Rational identities and application to
algebra and geometry_, J. Alg. __3__ (1966), 304--359.
* P. M. Cohn, _Free rings and their relations_, Academic Press 1971.

As explained in the Cohn's book, one can define the division ring of __noncommutative rational functions__ on a given alphabet.

Given a commutative field $k$
(_field of constants_), and a finite set $X = \{x_1,\ldots,x_n\}$,
consider the free algebra on $X$ (in the sense of universal algebra)
of signature $\{ +_2, \cdot_2, (\,)^{-1}_1, -_1\}$
and with constants in $k$ and denote it by $\mathcal{R}(X,k)$.
Expressions like $0^{-1}$ and $(x-x)^{-1}$ are in $\mathcal{R}(X,k)$
as no relations are imposed (one starts with terms which are elements
of $X\cup k$ and continues by nesting sequence of algebraic
operations eventually connecting all terms).
Let $R$ be an associative $k$-algebra, and $\phi : X\to R$
a map of sets. Then there is
a subset $\mathcal{R}_\phi \subset \mathcal{R}(X,k)$
and a map $\phi_* : \mathcal{R}_\phi\to R$ uniquely determined by the rules

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

For every $f \in \mathcal{R}(X,k)$ define $\mathrm{Dom}_\phi\,f$ to be the
set of all $|X|$-tuples $\vec{r} = (r_1,\ldots,r_{|X|}) \in R^{|X|}$
such that $f \in \mathcal{R}_\phi$ where $\phi = \phi_{\vec{r}}$ satisfies
$\phi(x_i) = r_i$ for $i = 1,\ldots, |X|$. Those $f$ for which
$\mathrm{Dom}_\phi f \neq \emptyset$ are called nondegenerate. It is clear
that $f \notin\mathcal{R}_\phi$ iff there is a subexpression in $f$ of the form
$(f_0)^{-1}$ where $f_0 \in \mathcal{R}_\phi$ and $\phi_*(f_0)$ is not
invertible in $R$.

* [[I. M. Gel'fand]], [[V. Retakh|V. S. Retakh]], _Determinants
of matrices over noncommutative rings_, Funct. Anal. Appl. __25__ (1991), no.2, pp. 91--102; engl. transl. __21__ (1991), pp. 51--58; _A theory of noncommutative
determinants and characteristic functions of graphs_,
Funct. Anal. Appl. __26__ (1992), no.4, pp. 231--246.
* [[Zoran Škoda]], _Universal noncommutative flag variety_, preprint (the exposition above is mainly taken from here)

It is used in the study of [[skewfield]]s, [[Cohn localization]], [[quasideterminant]]s, noncommutative integrable systems and so on.

* Natalia Iyudu, Stanislav Shkarin, _A proof of the Kontsevich periodicity conjecture_, [arxiv/1305.1965](http://arxiv.org/abs/1305.1965)

* [[M. Kontsevich]], _Noncommutative identities_, writeup of the 2011 MPIM Bonn Arbeitstagung talk, [arxiv/1109.2469](http://arxiv.org/abs/1109.2469)

category: algebra
[[!redirects noncommutative rational functions]]
[[!redirects noncommutative rational identity]]
[[!redirects noncommutative rational identities]]