
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

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    \downarrow && \downarrow^{\mathrlap{\epsilon \otimes id}}
    \\
    A
    &\underset{id}{\longrightarrow}& A
  }
  \,.
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    \downarrow && \downarrow^{\mathrlap{id \otimes \epsilon}}
    \\
    A
    &\underset{id}{\longrightarrow}& A
  }
  \,.
$$


## Related concepts

* [[associativity]], [[co-associativity]]

[[!redirects counitality]]
