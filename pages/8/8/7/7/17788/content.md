

#Contents#
* table of contents
{:toc}


## Idea

The [[formal  dual]] of [[associativity]].

## Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes)$ and an [[object]] $A$ in $\mathcal{C}$ equipped with morphism ("[[co-multiplication]]") $\Delta \colon A \longrightarrow A \otimes A$, then this is _co-associative_ if the following [[commuting diagram|diagram commutes]]

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    \downarrow && \downarrow^{\mathrlap{\Delta \otimes id}}
    \\
    A \otimes A
    &\underset{id \otimes \Delta}{\longrightarrow}& A \otimes A \otimes A
  }
  \,.
$$

If in addition there is a [[counit]] on $A$ for which the coproduct satisfies [[co-unitality]], then $A$ is called a  [[co-monoid]] in $(\mathcal{C}, \otimes)$.

[[!redirects coassociativity]]
