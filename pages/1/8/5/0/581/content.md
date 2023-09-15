
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

A **split epimorphism** in a [[category]] $C$ is a [[morphism]] $e\colon A \to B$ in $C$ such that there exists a morphism $s\colon B \to A$ such that the [[composite]] $e \circ s$ equals the [[identity morphism]] $1_B$.  Then the morphism $s$, which satisfies the [[duality|dual]] condition, is a __[[split monomorphism]]__.

We say that:

* $s$ is a __[[section]]__ of $e$,

* $e$ is a __[[retraction]]__ of $s$,

* $B$ is a __[[retract]]__ of $A$,

* the pair $(e,s)$ is a __[[split idempotent|splitting]]__ of the [[idempotent]] $s \circ e\colon A \to A$.  

A split epimorphism in $C$ can be equivalently defined as a morphism $e\colon A \to B$ such that for every [[object]] $X\colon C$, the [[function]] $C(X,e)$ is a [[surjection]] in $\mathbf{Set}$; the preimage of $1_B$ under $C(B,e)$ yields a section $s$.

Alternatively, it is also possible to define a split epimorphism as an __absolute epimorphism__: a morphism such that for every [[functor]] $F$ out of $C$, $F(e)$ is an [[epimorphism]].  From the definition as a morphism having a section, it is obvious that any split epimorphism is absolute; conversely, that the image of $e$ under the representable functor $C(B,1)$ is an epimorphism reduces to the characterization above.


## Properties

\begin{proposition}
Any split epimorphism is automatically a [[regular epimorphism]] (it is the [[coequalizer]] of $s\circ e$ and $1_A$), and therefore also a [[strong epimorphism]], an [[extremal epimorphism]], and (of course) an [[epimorphism]].
\end{proposition}

Evident but important and in contrast to general [[epimorphisms]]:
\begin{proposition}
  All [[functors]] preserve split epimorphisms.
\end{proposition}

\begin{proposition}
  A morphism is an [[isomorphism]] if and only if it is an [[monomorphism]] and a split epimorphism.
\end{proposition}

For a proof, see [Yuan 2012](#Yuan12).

\begin{proposition}
**(relation to the [[axiom of choice]])**
\linebreak
The [[axiom of choice]] [[internal logic|internal]] to a category $C$ can be phrased as "all epimorphisms are split."  In [[Set]] this is equivalent to the usual axiom of choice; in many other categories it may be true without assuming the axiom of choice (in $Set$), or it may be false regardless of the axiom of choice.
\end{proposition}


## Applications

The notion of split epimorphism arises often as a condition on [[fibrations]] in [[categories of chain complexes]]. See there for details.


## Examples
 {#Examples}

\begin{example}
  In [[Sets]] the [[axiom of choice]] is the statement that every epimorphism ([[surjective map]]) is split.
\end{example}

\begin{example}
Assuming the [[axiom of choice]] and thus the [[basis theorem]], every epimorphism in [[Vect]] is split:

For $\phi\colon V \to W$ a surjective [[linear map]], we can find an isomorphism $V \simeq ker(\phi) \oplus V'$. Then $\phi|_{V'}$ is an isomorphism, and its inverse $W \to V' \hookrightarrow ker(\phi) \oplus V'$ is a section of $\phi$.

For more on this see at *[[split exact sequence]]* the section *[Of free modules and vector spaces](split+exact+sequence#OfVectorSpaces)*
\end{example}

## Related concepts

* [[epimorphism]]

* [[split monomorphism]]

* [[idempotent]]

## References

* [[Saunders MacLane]], §I.5 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#Yuan12} [[Qiaochu Yuan]], *[Split epimorphisms and split monomorphisms](https://qchu.wordpress.com/2012/10/01/split-epimorphisms-and-split-monomorphisms/)*, blog post (2012)

[[!redirects split epimorphisms]]

[[!redirects split epi]]
[[!redirects split epis]]
[[!redirects split epic]]

[[!redirects absolute epimorphism]]
[[!redirects absolute epimorphisms]]
[[!redirects absolute epi]]
[[!redirects absolute epis]]
[[!redirects absolute epic]]

[[!redirects split surjection]]
[[!redirects split surjections]]
