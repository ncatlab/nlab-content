[[!redirects Shrinking wedge of circles]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Hawaiian earring space** is a famous counterexample in [[algebraic topology]] which shows the need for care in hypotheses to develop a good theory of [[covering space]]s. 

It is an example of a space which is not [[semi-locally simply connected space|semi-locally simply connected]]. 

The term “Hawaiian earring” is by far the most common name for this space
and is used in hundreds of papers.
Rarely, other terms can be found in the literature, such as “clamshell”,
“infinite earring”, and “shrinking wedge of circles”.
\cite{Dudley} is an early reference that mentions the terms “clamshell”
and “Hawaiian earring”.

## Definition

The Hawaiian earring space is the [[topological space]] defined to be the set 

$$\bigcup_{n \in \mathbb{N}} \{(x, y) \in \mathbb{R}^2: (x - 1/2^n)^2 + y^2 = 1/2^{2n}\}$$

endowed with [[subspace topology]] inherited from $\mathbb{R}^2$. 

More abstractly: the Hawaiian earring space can be described up to [[homeomorphism]] as the [[one-point compactification]] of a [[coproduct]] (in [[Top]]; a [[disjoint union space]]) of [[countably infinite set|countably]] many open [[intervals]]. This shows that the specific radii converging to zero (which was taken to be $1/2^n$ above) don't actually matter. 

Every neighborhood of $(0, 0)$ has non-contractible loops inside it (this would not be the case under the CW topology, i.e., the evident [[quotient space]] of countably many circles with the [[coproduct]] or [[disjoint union topological space|disjoint sum topology]], making the result a countable bouquet of circles). 

Viewed in terms of [[general topology]], it would be hard to sell the Hawaiian earring as a genuinely "pathological space": it is [[compactum|compact, Hausdorff]], [[connected space|connected and locally path-connected]], etc. It's really through the lens of algebraic topology and particularly the classical theory of covering spaces that it seems strange (it is not a [[CW complex]], it is not semi-locally simply connected, its [[fundamental group]] is hard to compute). 

## Related concepts

* [[Warsaw circle]]

## References

* {#Dudley} R. M. Dudley, _Continuity of homomorphisms_, Duke Math. J. 28:4 (1961), 587-594. [doi:10.1215/S0012-7094-61-02859-9](https://doi.org/10.1215/S0012-7094-61-02859-9).

[[!redirects Hawaiian earring spaces]]
[[!redirects Hawaiian earring]]
[[!redirects Hawaiian earrings]]
[[!redirects clamshell]]
[[!redirects clamshells]]
[[!redirects shrinking wedge of circles]]
[[!redirects shrinking wedges of circles]]
[[!redirects infinite earring]]
[[!redirects infinite earrings]]
[[!redirects infinite earring space]]
[[!redirects infinite earring spaces]]
