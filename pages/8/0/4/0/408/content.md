
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

The notion of _adjunction of two variables_ is a natural  generalization of both that of:

1. [[internal homs]] in a [[biclosed monoidal category]] 

2. $V$-[[enriched categories]] having [[powers]] and [[copowers]] (see [[powered and copowered category]])


## Definition

Let $C$, $D$ and $E$ be [[categories]]. An **adjunction of two variables** or **two-variable adjunction**

$$
 (\otimes, hom_l, hom_r) 
 \,\colon\, 
  C \times D \longrightarrow E
$$

consists of [[bifunctors]] of this form

$$
\begin{aligned}
  \otimes & \colon C \times D \longrightarrow E
  \\
  hom_l & \colon C^{op} \times E \longrightarrow D
  \\
  hom_r & \colon D^{op} \times E \longrightarrow C
\end{aligned}
$$

together with [[natural isomorphism]] of this form:

$$
  c \in C,\, d \in D,\, e \in E
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  E\big(c \otimes d,\, e\big)
  \;\simeq\;
  D\big(d,\, hom_l(c,e)\big)
  \;\simeq\;
  C\big(c,\, hom_r(d,e)\big)
  \,.
$$

## Cyclicity

If $(\otimes, hom_l, hom_r) : C \times D \to E$ is a two-variable adjunction, then so are
$$
 (hom_l^{op}, \otimes^{op}, hom_r) : E^{op} \times C \to D^{op}
$$
and
$$
 (hom_r^{op}, hom_l, \otimes^{op}) : D\times E^{op} \to C^{op}.
$$
giving an action of the [[cyclic group]] of order 3.  This can be made to look more symmetrical by regarding the original two-variable adjunction as a "two-variable left adjunction" $C\times D \to E^{op}$; see [Cheng-Gurski-Riehl](#CGR).

## Adjunctions of $n$ variables

There is a straightforward generalization to an adjunction of $n$ variables, which involves $n+1$ categories and $n+1$ functors.  Adjunctions of $n$ variables assemble into a 2-[[multicategory]].  They also have a corresponding notion of [[mates]]; see [Cheng-Gurski-Riehl](#CGR).

This 2-multicategory can also be promoted to a 2-[[polycategory]]; see [Shulman](#Shulman).


## Related concepts

* [[adjoint functor]]

* [[Quillen bifunctor]]

* [[parameterized monad]]

## References

Under the name "*adjunction with a parameter*" the concept appears in p. 102 of:

* {#MacLane71} [[Saunders MacLane]], §IV.7, Thm. 3 (p. 100) of: _[[Categories Work|Categories for the working mathematician]]_, Graduate Texts in Mathematics, Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

Under the name "*THC-situation*" the concept is discussed in:

* [[John Gray]], Def. 1.1 in: *Closed categories, lax limits and homotopy limits*. J. Pure Appl. Algebra **19** (1980) 127 - 158 &lbrack;<a href="https://doi.org/10.1016/0022-4049(80)90098-5">doi:10.1016/0022-4049(80)90098-5</a>&rbrack;

The terminology *adjunction of two variables* is used in:

* {#Hovey99} [[Mark Hovey]], Def. 4.1.12 in: *[[Model Categories]]*, Mathematical Surveys and Monographs, **63** AMS (1999) &lbrack;[ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover)&rbrack;

and:

* [[Emily Riehl]], Def. 4.3.7 in: _[[Category Theory in Context]]_, Dover Publications (2017)

Generalization to $n$-variable adjunctions:

* {#CGR} [[Eugenia Cheng]], [[Nick Gurski]], [[Emily Riehl]], "Multivariable adjunctions and mates" &lbrack;[arXiv:1208.4520](http://arxiv.org/abs/1208.4520)&rbrack;

* [[Rene Guitart]], *Trijunctions and triadic Galois connections*. Cah. Topol. Géom. Différ. Catég. 54 (2013), no. 1, 13-27, ([pdf](https://cahierstgdc.com/wp-content/uploads/2017/04/Guitart_54-1.pdf))

* {#Shulman} [[Mike Shulman]], *The 2-Chu-Dialectica construction and the polycategory of multivariable adjunctions*, [arxiv:1806.06082](https://arxiv.org/abs/1806.06082), [blog post](https://golem.ph.utexas.edu/category/2017/11/the_polycategory_of_multivaria.html)

[[!redirects two-variable adjunction]]
[[!redirects two-variable adjunctions]]
[[!redirects 2-variable adjunction]]
[[!redirects 2-variable adjunctions]]
[[!redirects adjunction of two variables]]
[[!redirects adjunctions of two variables]]
[[!redirects adjunction of 2 variables]]
[[!redirects adjunctions of 2 variables]]
[[!redirects n-variable adjunction]]
[[!redirects n-variable adjunctions]]
[[!redirects adjunction of n variables]]
[[!redirects adjunctions of n variables]]
[[!redirects multivariable adjunction]]
[[!redirects multivariable adjunctions]]
[[!redirects multi-variable adjunction]]
[[!redirects multi-variable adjunctions]]

[[!redirects THC-situation]]
[[!redirects THC situation]]
[[!redirects THC-situations]]
[[!redirects THC situations]]

[[!redirects trijunction]]
[[!redirects trijunctions]]

[[!redirects adjunction with a parameter]]
[[!redirects adjunctions with a parameter]]
