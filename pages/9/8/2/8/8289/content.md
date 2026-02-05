
> This article is about [[functors]] on [[product categories]]. For morphisms between [[bicategories]] see *[[2-functor]]* and *[[pseudofunctor]]*.  

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}



## Definition

By a *bifunctor* (short for _binary functor_, that is $2$-ary) or **functor of two variables** is simply a _[[functor]]_ whose [[domain]] is a [[product category]]:

For $C_1$, $C_2$ and $D$ [[categories]], a functor

$$
  F \;\colon\; C_1 \times C_2 \longrightarrow D
$$

is also called a _bifunctor_ from $C_1$ and $C_2$ to $D$.


\begin{remark}\label{Terminology}
**(terminology)**
\linebreak
While the term *[[bicategories]]* is used for ([[weak 2-category|weak]]) *[[2-categories]]*, the terminology "bifunctor" is not used in this context, instead one speaks of *[[pseudo-functors]]* or *[[2-functors]]* between [[bicategories]]/[[2-categories]].

In fact, even for the sense of a functor of 2 variable, the term "bifunctor" may not be used as frequently anymore as it used to, except maybe in parts of [[computer science]] and in [[model category]]-theory (cf. *[[Quillen bifunctor]]*).
\end{remark}

## Examples

Famous bifunctors are 

* the [[hom functor]]

  $$
    Hom(-,-) : C^{op} \times C \to Set
  $$

  on any [[locally small category]] $C$, or if $C$ is a [[closed category]], the [[internal hom]] functor

  $$
    [-,-] : C^{op} \times C \to C
    \,.
  $$

* on every [[monoidal category]] $(C, \otimes)$ the [[tensor product]] functor

  $$
    \otimes : C \times C \to C
  $$

A bifunctor of the form $D^{op} \times C \to Set$ is called a [[profunctor]].


## Related concepts

* [[extranatural transformation]]

* [[binary function]], [[bilinear map]], [[multilinear map]]

* [[binary morphism]]

* **bifunctor**, [[two-variable adjunction]], [[Quillen bifunctor]] 

  [[end]]/[[coend]]

* [[multifunctor]]


## References

In the generality of [[enriched category theory]] (hence for [[enriched functors]] on [[enriched product categories]]):

* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §III.4 of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

* [[Richard Garner]], and [[Ignacio López Franco]]. "Commutativity." Journal of Pure and Applied Algebra 220.5 (2016): 1707-1751.

* [[Nicola Gambino]], [[Richard Garner]], and [[Christina Vasilakopoulou]]. "A unified treatment of commuting tensor products of categories, operads, symmetric multicategories and their bimodules." [arXiv:2511.14402](https://arxiv.org/abs/2511.14402) (2025).

[[!redirects bifunctor]]
[[!redirects bifunctors]]
[[!redirects binary functor]]
[[!redirects binary functors]]
[[!redirects 2-ary functor]]
[[!redirects 2-ary functors]]
[[!redirects functor of two variables]]
[[!redirects functors of two variables]]
[[!redirects functor of 2 variables]]
[[!redirects functors of 2 variables]]
