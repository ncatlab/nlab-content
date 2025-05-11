
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

Let $L$ be a [[01-bounded semilattice]], that is, a semilattice with an [[absorbing element]]. **Phoa's principle** states that every [[endofunction]] $f:L \to L$ is [[monotonic]] and the precomposition function $h \mapsto h \circ i:L^L \to L^\mathbb{2}$ by the [[embedding]] $i:\mathbb{2} \hookrightarrow L$ of the [[booleans]] into $L$ is an embedding. 

If $L$ is a [[distributive lattice]], then Phoa's principle is equivalent to the linear interpolation condition that for all [[endofunctions]] $f:L \to L$ and elements $x \in L$:
$$f(x) = f(\top) \wedge (x \vee f(\bot))$$

In [[Pos]] the category of [[posets]] and [[monotonic functions]], Phoa's principle holds for the [[boolean domain]] $\mathbb{2}$. In [[synthetic Stone duality]], Phoa's principle holds for the [[type of propositions|type of]] [[open propositions]] $\mathrm{Open}$. In [[synthetic domain theory]], Phoa's principle holds for a [[dominance]] $\Omega$. 

## Related concepts

* [[distributive lattice]]

* [[flat distributive lattice]]

* [[01-bounded semilattice]]

* [[directed univalence]]

* [[synthetic domain theory]]

## References

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#CGM} [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *Directed Univalence in Synthetic Stone Duality*, unfinished draft; LaTeX documents can be found [here](https://github.com/felixwellen/synthetic-zariski/tree/main/condensed-univalence). 

* [[Jonathan Sterling]], *Baby steps in higher domain theory*, talk at [Homotopy Type Theory and Computing – Classical and Quantum](https://nyuad.nyu.edu/en/events/2024/april/homotopy-type-theory-and-computing.html), [[Center for Quantum and Topological Systems]] ([video](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_b57uwin3?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_b57uwin3))

* {#PS25} [[Leoni Pugh]], [[Jonathan Sterling]], *When is the partial map classifier a Sierpiński cone?* ([arXiv:2504.06789](https://arxiv.org/abs/2504.06789))

[[!redirects Phoa's principle]]
[[!redirects Phoa principle]]