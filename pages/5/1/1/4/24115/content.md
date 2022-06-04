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

The notion of a *quotient object coclassifier* in a [[finitely cocomplete category]] is [[abstract duality|dual]] to that of a *[[subobject classifier]]* in a [[finitely complete category]]. 

## Definition

In a category $C$ with [[finite colimits]], a quotient object coclassifier is an object $Q$ with an [[epimorphism]] $\epsilon:Q \to \mathbb{0}$ into the [[initial object]] $\mathbb{0}$, such that for every [[epimorphism]] $f:X \to U$ there is a unique morphism $\digamma_U:Q \to X$ such that there is a [[pushout]] [[diagram]] of the form


$$
  \array{
    Q 
      &\overset{\epsilon}{\longrightarrow}& 
    \mathbb{0}   
    \\
    \big\downarrow {}^{\mathrlap{\digamma_U}} 
    && 
    \big\downarrow {}^{\mathrlap{\exists !}}
    \\
    X &\underset{f}{\longrightarrow}& U
  }
  \,.
$$

## See also

* [[subobject classifier]]

* [[finitely cocomplete category]]

* [[cotopos]]