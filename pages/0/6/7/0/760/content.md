
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

## Definitions and terminology

A **split monomorphism** in a [[category]] $C$ is a [[morphism]] $m\colon A \to B$ in $C$ such that there exists a morphism $r\colon B \to A$ such that the [[composite]] $r \circ m$ equals the [[identity morphism]] $1_A$.  Then the morphism $r$, which satisfies the [[duality|dual]] condition, is a __[[split epimorphism]]__.

We say that:

* $r$ is a __[[retraction]]__ of $m$,

* $m$ is a __[[section]]__ of $r$,

* $A$ is a __[[retract]]__ of $B$,

* the pair $(r,m)$ is a __[[split idempotent|splitting]]__ of the [[idempotent]] $m \circ r\colon B \to B$.

A split monomorphism in $C$ can be equivalently defined as a morphism $m\colon A \to B$ such that for every [[object]] $X\colon C$, the [[function]] $C(m,X)$ is a [[surjection]] in $\mathbf{Set}$; a preimage of $1_A$ under $C(m,A)$ yields a retraction $r$.

Alternatively, it is also possible to define a split monomorphism as an __absolute monomorphism__: a morphism such that for every functor $F$ out of $C$, $F(m)$ is a [[monomorphism]].  From the definition as a morphism having a retraction, it is obvious that any split monomorphism is absolute; conversely, that the image of $m$ under the [[representable functor]] $C(1,A)$ is a monomorphism reduces to the characterization above.


## Properties

\begin{proposition}
Any split monomorphism is a [[monomorphism]], in fact a [[regular monomorphism]] (it is the [[equalizer]] of $m\circ r$ and $1_B$), and therefore also a [[strong monomorphism]], an [[extremal monomorphism]], and (of course) a [[monomorphism]].
\end{proposition}

Evident but important and in contrast to general [[monomorphisms]]:
\begin{proposition}
  All [[functors]] preserve split monomorphisms.
\end{proposition}

\begin{proposition}
  A morphism is an [[isomorphism]] if and only if it is an [[epimorphism]] and a split monomorphism.
\end{proposition}

For a proof, see [Yuan 2012](#Yuan12).


## Examples

### In vector spaces

In the category [[Vect]] of [[finite dimensional vector spaces]] (over any [[field]]) every monomorphism $V_1 \hookrightarrow V_2$ splits. The corresponding [[idempotent]] is the [[projection]] onto $V_1$ in $V_2$.

## In higher category theory

In [[higher category theory]], we may still consider the notion of "split monomorphism", i.e. a morphism $m\colon A \to B$ in $C$ such that there exists a morphism $r\colon B \to A$ with $r \circ m$ being [[equivalence|equivalent]] to the identity of $A$.  However, in a higher category, such a morphism $m$ will not necessarily be a "monomorphism", that is, it need not be $(-1)$-[[truncated object|truncated]].

In general, we can say that in an $(n,1)$-[[(n,1)-category|category]], a "split monomorphism" will be $(n-2)$-truncated.  Thus:

* in a [[(0,1)-category]] (a [[poset]]), a split mono is $(-2)$-truncated, i.e. an [[isomorphism]];

* in a [[1-category]], a split mono is $(-1)$-truncated, i.e. a [[monomorphism]];

* in a [[(2,1)-category]], a split mono is $0$-truncated, i.e. a [[discrete morphism]];

* in an [[(∞,1)-category]], a split mono is not necessarily truncated at any finite level.

## Related concepts

* [[monomorphism]]

* [[split epimorphism]]

* [[propositions as projections]]

## References

* [[Saunders MacLane]], §I.5 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#Yuan12} [[Qiaochu Yuan]], *[Split epimorphisms and split monomorphisms](https://qchu.wordpress.com/2012/10/01/split-epimorphisms-and-split-monomorphisms/)*, blog post (2012), 


[[!redirects split monomorphism]]

[[!redirects split monomorphisms]]
[[!redirects split mono]]
[[!redirects split monos]]
[[!redirects split monic]]
[[!redirects split monics]]

[[!redirects absolute monomorphism]]
[[!redirects absolute monomorphisms]]
[[!redirects absolute mono]]
[[!redirects absolute monos]]
[[!redirects absolute monic]]
[[!redirects absolute monics]]
