
# &#201;tale schemes
* table of contents
{: toc}

## Definition

Let $k$ be a field.

An _&#233;tale $k$-scheme_ is defined to be a directed colimit of $k$-[[ring spectrum|spectra]] $Sp_k k'$ of finite separable field-extensions $k'$ of $k$.

An _&#233;tale formal $k$-scheme_ is defined to be a directed colimit of [[formal spectrum|formal k-spectra]] $Spf_k k'$ of finite separable field-extensions $k^'$ of $k$.


## Properties

We give a characterization of &#233;tale $k$-schemes and &#233;tale formal $k$-schemes in terms of [[constant scheme|constant schemes]]:

The category $Sch_k$ of $k$-schemes is [[copower|copowered (= tensored)]] over $Set$. We define the _constant $k$-scheme_ on a set $E$ by

$$E_k \coloneqq E \otimes Sp_k k = \coprod_{e\in E} Sp_k k$$

For a scheme $X$ we compute $M_k(E_k,E) = Set(Sp_k k,X)^E = X(k)^E = Set(E,X(k))$ and see that there is an adjunction

$$((-)_k \dashv (-)(k))\colon Sch_k \to Set$$

A _constant formal scheme_ is defined to be a completion of constant scheme. The completion functor induces an equivalence between the category of constant schemes and the category of constant formal schemes.

+-- {: .num_remark}
###### Remark
Let $X$ be a $k$-scheme or a formal $k$-scheme. Then the following statements are equivalent:


1. $X$ is &#233;tale.

2. $X \otimes_k \overline k$ is constant.

3. $X \otimes_k k_s$ is constant.
where $\overline k$ denotes an algebraic closure of $k$, $k_s$ denotes the subextension of $\overline k$ consisting of all separable elements of $\overline k$ and $\otimes_k$ denotes skalar extension.
=--

+-- {: .proof}
###### Proof
$X$ is &#233;tale iff its scalar extension $X\otimes_k k_s$ is &#233;tale. And a $k_s$-scheme is &#233;tale iff it is constant.
=--

+-- {: .num_prop}
###### Proposition
The functor

$$\begin{cases}
Sch_{et}\to Gal(k\hookrightarrow k_s)-Set
\\
X\mapsto X(k_s)
\end{cases}$$

from the category of [[étale scheme|étale schemes]] to the category of sets equipped with an [[action]] of the absolute Galois group is an equivalence of categories.

This statement is an instance of the main theorem of [[Grothendieck's Galois theory]] in the classical case of fields.
=--

Since this functor preserves products we have the analogue statement for [[group schemes]]:

+-- {: .num_defn}
###### Definition

The functor

$$\begin{cases}
GrSch_{et}\to Gal(k\hookrightarrow k_s)-Mod
\\
X\mapsto X(k_s)
\end{cases}$$

from the category of [[étale group scheme|étale group schemes]] to the category of [[Galois module|Galois modules]] of the [[absolute Galois group]] of $k$ is an equivalence of categories.
=--

If now the [[characteristic]] of $k$ is a prime number $p$ there is a relation of &#233;tale [[formal scheme|formal schemes]] resp. &#233;tale [[group scheme|group schemes]] and the [[Frobenius morphism]]:

+-- {: .num_prop}
###### Proposition
Let $X$ be a k-[[formal scheme]] resp. a [[locally algebraic scheme]].

Then $X$ is &#233;tale iff the [[Frobenius morphism]] $F:X\to X^{(p)}$ is a monomorphism resp. an isomorphism.
=--

## References

Michel [[Demazure, lectures on p-divisible groups]], sections I.8 and II.2, [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)


[[!redirects etale scheme]]
[[!redirects etale schemes]]
[[!redirects étale scheme]]
[[!redirects étale schemes]]
