
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

\begin{definition}\label{InverseMorphism}
**([[inverse morphisms]])** \linebreak
An **inverse** of a [[morphism]] $f \colon X \to Y$ in a [[category]] or [[unital magmoid]] (or an element of a [[monoid]] or [[unital magma]]) is another morphism $f^{-1} \colon Y \to X$ which is both a [[left-inverse]] (a [[retraction]]) as well as a [[right-inverse]] (a [[section]]) of $f$, in that 
$$
  f \circ f^{-1} \,=\, id_Y \colon Y \to Y 
$$
[[equality|equals]] the [[identity morphism]] on $Y$ 
and
$$
  f^{-1} \circ f \,=\, id_X \colon X \to X 
$$
[[equality|equals]] the [[identity morphism]] on $X$.
\end{definition}

\begin{definition}\label{Isomorphism}
A [[morphism]] that has an [[inverse morphism]] (Def. \ref{InverseMorphism}) is called an *[[isomorphism]]*.
\end{definition}

\begin{remark}
A ([[small category|small]]) [[category]] in which all morphisms have inverses is called a *[[groupoid]]*.
\end{remark}

## Properties


\begin{prop}\label{InversesAreUnique}
**([[inverse morphisms]] are unique)** \linebreak
  If $f$ is an [[isomorphism]] (Def. \ref{Isomorphism}) with [[inverse morphism]] $f^{-1}$ (Def. \ref{InverseMorphism}), then any [[left inverse]] as well as any [[right inverse]] is already an actual [[inverse morphism]] and in fact is [[equality|equal]] to $f^{-1}$.
\end{prop}
In particular, [[inverse morphisms]] are unique when they exist.
\begin{proof}
  Let $g$ be a [[left inverse]], hence such that $g \circ f \,=\, id$. 
  Write $f^{-1}$ for the actual inverse, hence such that
  $f^{-1} \circ f \,=\, id$ and $f \circ f^{-1} \,=\, id$.  
  Then the following sequence of equalities implies that
  $g = f^{-1}$:
  $$
  \begin{aligned}
    g 
    & \;=\;
    g \circ id
    \\
    & \;=\;
    g \circ ( f \circ f^{-1} )
    \\
    & \;=\;
    (g \circ f) \circ f^{-1}
    \\
    & \;=\;
    id \circ f^{-1}
    \\
    & \;=\;
    f^{-1}
    \,.
  \end{aligned}
  $$
Here all steps use just the definitions of the various morphisms, except the third step, which uses [[associativity]] of [[composition]] in any [[category]].

An analogous argument applies to right inverses; and either argument applies to actual inverses.
\end{proof}

\begin{prop}
  Let $f$ be an [[isomorphism]] (Def. \ref{Isomorphism}).
  Then the inverse morphism $\left(f^{-1}\right)^{-1}$ of an inverse morphism $f^{-1}$ (Def. \ref{InverseMorphism}) exists and is [[equality|equal]] to the original morphism:
$$
  \left(f^{-1}\right)^{-1}
  \;=\;
  f
  \,.
$$
\end{prop}
\begin{proof}
  By the uniqueness of inverses (Prop. \ref{InversesAreUnique}) for $f^{-1}$.
\end{proof}


## Examples

\begin{example}\label{IdentityMorphismsAreTheirOwnInverses}
**([[identity morphisms]] are their own [[inverse morphisms]])** \linebreak
Any [[identity morphism]]  is its own inverse morphism (Def. \ref{InverseMorphism}):
$$
  id^{-1} \,=\, id
  \,.
$$
\end{example}


\begin{example}
In a [[balanced category]], such as in a [[topos]] (in particular in [[Sets]]) every morphism that is both a [[monomorphism]] and well as an [[epimorphism]] is actually an [[isomorphism]] and thus has an [[inverse morphism]]. 

To see that this is not generally the case, notice that any [[partial order]] is an (necessarily unbalanced) category where every morphism is both a monomorphism as well as an epimorphism, but only its [[identity morphisms]] have [[inverse morphisms]] (as they must, by Exp.  \ref{IdentityMorphismsAreTheirOwnInverses}). 
\end{example}


## In non-unital contexts

In a [[magmoid]] or [[semicategory]] (or an element of a [[semigroup]] or [[magma]]), a morphism $f:a \to b$ has a unique __[[retraction]]__ $f^{-1}:b \to a$ if 

* for every morphism $g:b \to c$, $g \circ (f^{-1} \circ f) = g$,

* for every morphism $g:c \to a$, $(f^{-1} \circ f) \circ g = g$,

and a morphism $f:a \to b$ has a unique __[[section]]__ $f^{-1}:b \to a$ if 

* for every morphism $g:a \to c$, $g \circ (f \circ f^{-1}) = g$,

* for every morphism $g:a \to c$, $(f \circ f^{-1})\circ g = g$,

A morphism $f:a \to b$ has a unique __inverse__ if it has a retraction that is also a section. 

## Related concepts

* [[inverse morphism]], [[inverse function]]

* [[weak inverse]]

* [[inversion involution]]


[[!redirects inverse]]
[[!redirects inverses]]
[[!redirects inverse element]]
[[!redirects inverse elements]]
[[!redirects inverse of an element]]
[[!redirects inverses of an element]]
[[!redirects inverses of elements]]
[[!redirects invertible element]]
[[!redirects invertible elements]]

[[!redirects inverse morphism]]
[[!redirects inverse morphisms]]
[[!redirects inverse of a morphism]]
[[!redirects inverses of a morphism]]
[[!redirects inverses of morphisms]]
[[!redirects invertible morphism]]
[[!redirects invertible morphisms]]
