+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The *external direct sum* or *external Whitney sum* of [[vector bundles]] is the operation which from a [[pair]] of [[vector bundles]] $\mathscr{V} \,\in\,$ [[Vect(X)]], $\mathscr{W} \,\in\,$ [[Vect(X)|$Vect(Y)$]] over possibly different base spaces $X,\ Y \,\in\,$ [[Top]] forms the [[direct sum of vector bundles]] ("[[Whitney sum]]") $(-)\bigoplus(-)$ of their [[pullback of a bundle|pullback]] to the [[product space]] $X \times Y$ of their base spaces:

$$
  \array{
    Vect(X) \times Vect(Y)
    &\oversey{\boxplus}{\longrightarrow}&
    Vect(X\times Y)
    \\
    \big(
      \mathscr{V}
      ,\,
      \mathscr{W}
    \big)
    &\mapsto&
    \big(
      (pr_X)^\ast \mathscr{V}
    \big)
    \oplus_{X \times Y}
    \big(
      (pr_Y)^\ast \mathscr{W}
    \big)
  }
$$

Since the [[Whitney sum]] $\oplus \,\colon\, Vect(X \times Y) \times Vect(X \times Y) \longrightarrow Vect(X \times Y)$ is the [[Cartesian product]] in [[Vect(X)|$Vect(X \times Y)$]], one may understand the external Whitney sum as the Cartesian product in the [[Grothendieck construction]] $\int_{X} Vect(X)$, see the the example [there](Grothendieck+construction#CartesianProductInGrothendieckConstruction).

## Related concepts

* [[external tensor product]]

* [[external tensor product of vector bundles]]

* [[direct sum of vector bundles]]

## References

Discussion in the context of [[topological K-theory]]:

* [[Max Karoubi]], §4.9 in: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften **226** Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3)&rbrack;

[[!redirects external direct sums of vector bundles]]

[[!redirects external Whitney sum of vector bundles]]
[[!redirects external Whitney sums of vector bundles]]


