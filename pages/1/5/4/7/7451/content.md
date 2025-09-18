[[!redirects epi-pullback]]
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

in a [[category]] with [[finite limits]] is called a **quasi-pullback** if the canonical morphism $q\to a\times_c b$ to the [[fiber product]]  (induced by its [[universal property]]) is an [[epimorphism]].

Spcifically, the object $q$ is then called a **quasi-pullback** of the span $b\to c\leftarrow a$.

=--

## Examples

\begin{proposition}
For a [[topos]] $T$ and $T^I$ its [[arrow category]] which is a topos, quasi-pullback squares (in $T$) form a [[class]] of [[open morphisms]] in $T^I$.
\end{proposition}

Recall that, for every [[regular category]] $A$, there is a [[double category]] [[Rel]]$(A)$ of relations.

\begin{proposition}
[[double functors|Functors]] $Rel(A) \to Rel(B)$ between [[double categories]] of [[relations]] are equivalent to [[functors]] $A \to B$ preserving quasi-pullbacks.
\end{proposition}

## Related pages

* [[pullback]]

## References

- [[André Joyal]] and [[Ieke Moerdijk]], _A completeness theorem for open maps_, Annals of Pure and Applied Logic 70.1 (1994): 51-86.

- [[Robert Paré]], _Some things about double categories_, Talk at _Virtual Double Categories Workshop_ 2022, [pdf](https://bryceclarke.github.io/virtual-double-categories-workshop/slides/robert-pare.pdf)
