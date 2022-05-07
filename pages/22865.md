

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The smallest [[simplicial set]] whose [[homotopy type]] in the [[classical homotopy category]] is that of the [[circle]] has precisely two non-degenerate [[simplices]], one in degree 0 -- a single [[vertex]] -- and one in degree 1 -- a single [[edge]] which is a [[loop]] on that vertex:

$$
  S \;\coloneqq\; \Delta[1]/\partial \Delta[1]
  \,.
$$

Despite or maybe because its simplicity, the minimal simplicial circle plays a central role in many constructions, notably in the context of [[cyclic homology]] (e.g. [Loday 1992, 7.1.2](#Loday92)).


## Properties

\begin{example}
  The [[normalized chain complex]] of the [[free simplicial abelian group]] of the minimal simplicial circle $S$ has the group of [[integers]] in degrees 0 and 1, and all [[differentials]] are [[zero morphism|zero]]:
$$
  N_\bullet \circ \mathbb{Z}(S)
  \;\simeq\;
  \left[
  \array{
    \vdots
    \\
    \big\downarrow
    \\
    0
    \\
    \big\downarrow
    \\
    \mathbb{Z}
    \\
    \big\downarrow {}^{\mathrlap{ 0 }}
    \\
    \mathbb{Z}
  }
  \;\;
  \right]
  \;\simeq\;
  \mathbb{Z} \oplus \mathbb{Z}[1]
  \,.
$$
\end{example}


## Related concepts

* [[circle]], [[unit circle]], [[circle type]], [[circle group]]

* [[cyclic category]]

  [[cyclic object]], [[cyclic set]], [[cyclic space]]
 
  [[cyclic homology]], [[cyclic cohomology]]

* [[inertia groupoid]]


## References

Discussion in relation to the [[cyclic category]] and [[cyclic sets]]/[[cyclic spaces]]:

* {#Loday92} [[Jean-Louis Loday]], *Cyclic Spaces and $S^1$-Equivariant Homology* ([doi:10.1007/978-3-662-21739-9_7](https://link.springer.com/chapter/10.1007/978-3-662-21739-9_7))

  Chapter 7 in: *Cyclic Homology*, Grundlehren **301**, Springer 1992 ([doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9))

