
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

+-- {: .un_defn}
###### Definition

In [[category theory]], a [[commutative square]]

$$
  \array{
    q
    & \longrightarrow &
    a
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    b
    &
    \longrightarrow
    &
    c
  }
$$

in a [[category]] with [[finite limits]] is (sometimes) called an **epi-pullback** (or **quasi-pullback** or **epi cartesian-square**) if the canonical morphism $q\to a\times_c b$ to the [[fiber product]]  (induced by its [[universal property]]) is an [[epimorphism]].

Spcifically, the object $q$ is then called an **epi-pullback** or **quasi-pullback** of the span $b\to c\leftarrow a$.

=--

## Examples

\begin{proposition}
For a [[topos]] $T$ and $T^I$ its [[arrow category]] which is a topos, epi-pullback squares (in $T$) form a [[class]] of [[open morphisms]] in $T^I$.
\end{proposition}

\begin{proposition}
Lax [[double functors]] $Rel(A) \to Rel(B)$ are equivalent to [[functors]] $A \to B$ preserving quasi-pullbacks.
\end{proposition}

## Related pages

* [[pullback]]

## References

- [[Robert Paré]], _Some things about double categories_, Talk at _Virtual Double Categories Workshop_ 2022, [pdf](https://bryceclarke.github.io/virtual-double-categories-workshop/slides/robert-pare.pdf)
