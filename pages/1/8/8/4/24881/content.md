
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[formal dual]] of *[[unitality]]*:

An object in a [[monoidal category]] which is equipped with a [[comultiplication]] map which satisfies both co-unitality and [[co-associativity]] is called a *[[co-monoid]]*.

## Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes)$ and an [[object]] $A$ in $\mathcal{C}$ equipped with a morphism ("[[co-multiplication]]") $\Delta \colon A \longrightarrow A \otimes A$, and a morphism $\epsilon \colon A \longrightarrow 1$, $\epsilon$ is called a *counit* if the following [[commuting diagram|diagrams commute]]


\begin{tikzcd}[sep=20pt]
  &
  A \otimes A
  \ar[
    dr,
    "{ \epsilon \otimes \mathrm{id} }"
  ]
  \\
  A
  \ar[
    ur,
    "{ \Delta }"
  ]
  \ar[
    rr,
    equals
  ]
  &&
  A
  \mathrlap{\,,}
\end{tikzcd}
\begin{tikzcd}[sep=20pt]
  &
  A \otimes A
  \ar[
    dr,
    "{ \mathrm{id} \otimes \epsilon }"
  ]
  \\
  A
  \ar[
    ur,
    "{ \Delta }"
  ]
  \ar[
    rr,
    equals
  ]
  &&
  A
  \mathrlap{\,.}
\end{tikzcd}


## Related concepts

* [[associativity]], [[co-associativity]]

[[!redirects counitality]]
