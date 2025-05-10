
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Let $L$ be a [[distributive lattice]]. **Phoa's principle** states that for all [[endofunctions]] $f:L \to L$ and elements $x \in L$:
$$f(x) = f(\top) \wedge (x \vee f(\bot))$$

More generally, let $L$ be a bounded [[semilattice]], that is, a semilattice with an [[absorbing element]]. **Phoa's principle** states that every [[endofunction]] $f:L \to L$ is [[monotonic]] and the precomposition function $h \mapsto h \circ i:L^L \to L^\mathbb{2}$ by the [[embedding]] $i:\mathbb{2} \hookrightarrow L$ is an embedding. 

In [[Pos]] the category of [[posets]] and [[monotonic functions]], Phoa's principle holds for the [[boolean domain]] $\mathbb{2}$. In [[synthetic Stone duality]], Phoa's principle holds for the [[type of propositions|type of]] [[open propositions]] $\mathrm{Open}$. 

## Related concepts

* [[distributive lattice]]

* [[flat distributive lattice]]

* [[directed univalence]]

* [[synthetic domain theory]]

## References

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#CGM} [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *Directed Univalence in Synthetic Stone Duality*, unfinished draft; LaTeX documents can be found [here](https://github.com/felixwellen/synthetic-zariski/tree/main/condensed-univalence). 

* {#PS25} [[Leoni Pugh]], [[Jonathan Sterling]], *When is the partial map classifier a Sierpiński cone?* ([arXiv:2504.06789](https://arxiv.org/abs/2504.06789))

[[!redirects Phoa's principle]]
[[!redirects Phoa principle]]