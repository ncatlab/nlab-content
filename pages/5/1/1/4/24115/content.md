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
{:toc}

## Idea

In a [[finitely cocomplete category]], the [[dual]] of a [[subobject classifier]]. 

## Definition

In a category $C$ with [[finite colimits]], a quotient object coclassifier is an object $Q$ with an [[epimorphism]] $\epsilon:Q \to \mathbb{0}$ into the [[initial object]] $\mathbb{0}$, such that for every [[epimorphism]] $f:X \to U$ there is a unique morphism $\digamma_U:Q \to X$ such that there is a [[pushout]] [[diagram]] of the form


$$
  \array{
    Q &\stackrel{\epsilon}{\to}& \mathbb{0}   
    \\
    \downarrow^{\digamma_U} && \downarrow^{\exists !}
    \\
    X &\stackrel{f}{\to}& U
  }
  \,.
$$

## See also

* [[subobject classifier]]

* [[finitely cocomplete category]]

* [[cotopos]]