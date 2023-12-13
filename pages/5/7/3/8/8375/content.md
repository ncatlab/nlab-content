
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Arity classes
* table of contents
{: toc}

## Idea

An *arity class* is a class of [[cardinalities]] which is suitable to be the collection of [[arity|arities]] for the operations in an [[algebraic theory]].


## Definition

An **arity class** is a [[class]] $\kappa$ of [[small set|small]] [[cardinalities]] such that

1. $1\in\kappa$.

2. $\kappa$ is closed under indexed sums: if $\lambda\in\kappa$ and     $\alpha: \lambda \to\kappa$, then $\sum_{i\in \lambda} \alpha(i)$ is also in $\kappa$.

3. $\kappa$ is closed under indexed decompositions: if $\lambda\in\kappa$ and $\sum_{i\in \lambda} \alpha(i)\in \kappa$, then each $\alpha(i)$ is also in $\kappa$.

A [[set]] or [[family]] is called **$\kappa$-small** if its cardinality belongs to $\kappa$.  A [[theory]] or other object with a collection of "operations" whose inputs are all $\kappa$-small is called **$\kappa$-ary**.

+-- {: .un_remark}
###### Remark
By [[induction]], the second condition implies closure under iterated indexed sums, in the sense that for any $n\ge 2$, we have
$$\sum_{i_1\in\lambda_1} \; \sum_{i_2\in\lambda_2(i_1)} \cdots
  \sum_{i_{n-1} \in\lambda_{n-1}(i_1,\dots,i_{n-2})} \lambda_n(i_1,\dots,i_{n-1})
$$
is in $\kappa$ if all the $\lambda$'s are.  The first condition may be regarded as the case $n=0$ of this (the case $n=1$ being just "$\lambda\in\kappa$ iff $\lambda\in\kappa$").
=--

+-- {: .un_remark}
###### Remark
An alternative, more category-theoretic, way to state the second and third conditions is that for any [[function]] $f:I\to J$, if ${|J|}\in\kappa$, then ${|I|}\in\kappa$ if and only if all fibers of $f$ are in $\kappa$.
=--


## Examples

* The set $\{1\}$ is an arity class.  A $\{1\}$-ary object is called **unary**.

* The set $\{0,1\}$ is an arity class.  A$\{0,1\}$-ary object is called **subunary**.

* The set $\omega = \mathbb{N} = \{0,1,2,3\dots\}$ is an arity class.  An $\omega$-ary object is called **finitary**.

* For any [[regular cardinal]] $\kappa$, the set of all cardinalities strictly less than $\kappa$ is an arity class, which we abusively denote also by $\kappa$.  The previous example $\omega$ is a special case of this, as is $\{0,1\}$ if we consider $2$ to be a regular cardinal.

* In particular, if $\kappa$ is the "size of the universe" --- e.g., an [[inaccessible cardinal]] for which we have chosen to call sets of cardinality $\lt\kappa$ [[small set|small]], or literally the proper-class cardinality of the [[universe]], depending on how one thinks of it ---, then it is an arity class.  In this case we call $\kappa$-ary objects **infinitary** or $\infty$-ary.

In [[classical mathematics]], these examples in fact exhaust *all* arity classes.  Classically, if $\lambda$ is any cardinal number strictly greater than $1$, then for any cardinal numbers $\mu\le \nu$, we can write $\nu$ as a $\lambda$-indexed sum containing $\mu$.  Hence, if an arity class contains any cardinality $\gt 1$, it must be down-closed, and a down-closed arity class must arise from a regular cardinal.

In [[constructive mathematics]], however, not every arity class besides $\{1\}$ must be downward-closed, and not every downward-closed arity class must arise from a regular cardinal.  Arguably, however, in constructive mathematics one should consider downward-closed arity classes instead of regular cardinals.


## Related pages

* [[algebraic theory]]

* [[∞-ary exact category]], [[∞-ary site]]

* [[arity space]]

## References

* [[Michael Shulman]], "Exact completions and small sheaves".  *Theory and Applications of Categories*, Vol. 27, 2012, No. 7, pp 97-173.  [Free online](http://www.tac.mta.ca/tac/volumes/27/7/27-07abs.html)

[[!redirects arity class]]
[[!redirects arity classes]]

[[!redirects unary]]
[[!redirects subunary]]
[[!redirects finitary]]

[[!redirects n-ary]]

[[!redirects κ-ary]]
[[!redirects kappa-ary]]

[[!redirects ∞-ary]]
[[!redirects infinitary]]
[[!redirects infinity-ary]]
