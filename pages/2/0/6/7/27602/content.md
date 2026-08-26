
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

\tableofcontents

## Idea

*Phoa's principle* is a principle used to axiomatize [[Sierpinski space]] in [[synthetic topology]] and [[synthetic domain theory]]. Phoa's principle is also called the *Phoa principle* in [Bauer & Taylor 2009](#BT09). 

Phoa's principle is named after [[Wesley Phoa]]. 

## Definition

Let $L$ be a [[01-bounded semilattice]], that is, a semilattice with an [[absorbing element]]. **Phoa's principle** states that every [[endofunction]] $f:L \to L$ is [[monotonic]] and the precomposition function $h \mapsto h \circ i:L^L \to L^\mathbb{2}$ by the [[embedding]] $i:\mathbb{2} \hookrightarrow L$ of the [[booleans]] into $L$ is an embedding. 

If $L$ is a [[distributive lattice]], then Phoa's principle is equivalent to the linear interpolation condition that for all [[endofunctions]] $f:L \to L$ and elements $x \in L$:
$$f(x) = f(\top) \wedge (x \vee f(\bot))$$

## Properties

There are many types of distributive lattices for which non-trivial such distributive lattices cannot satisfy Phoa's principle. 

\begin{theorem} 
Suppose $L$ is a distributive lattice $L$ with an endpoint-swapping [[endofunction]] $\neg:L \to L$, where $\neg(\top) = \bot$ and $\neg(\bot) = \top$. Then the only such distributive lattice $L$ for which Phoa's principle holds is the trivial Heyting algebra.
{#EndpointSwap} 
\end{theorem}

\begin{proof}
Applying the function $x \mapsto \neg x$ to the linear interpolation condition for the distributive lattice yields 
$$\neg x = \neg (\top) \wedge (x \vee \neg \bot) = \bot \wedge (x \vee \top) = \bot$$
Substituting $\bot$ into the equation yields 
$$\neg \bot = \top = \bot$$
which is precisely the condition that $L$ be a trivial such distributive lattice. 
\end{proof}

\begin{lemma}
Suppose $L$ is a [[Heyting algebra]] for which Phoa's principle holds. Then $L$ is the trivial Heyting algebra.
\end{lemma}

\begin{proof}
$L$ being a Heyting algebra implies that $L$ has a Heyting implication $x, y \mapsto x \to y$ and thus a Heyting [[logical negation|negation]] function $x \mapsto \neg x$ defined by $\neg x \coloneqq x \to \bot$ such that $\neg(\top) = \bot$ and $\neg(\bot) = \top$. Hence, by [the first theorem](#EndpointSwap), $L$ is the trivial Heyting algebra if Phoa's principle holds. 
\end{proof}

\begin{theorem}
Suppose $L$ is a [[De Morgan algebra]] for which Phoa's principle holds. Then $L$ is the trivial De Morgan algebra.
\end{theorem}

\begin{proof}
$L$ being a De Morgan algebra implies that $L$ has an [[involution]] $x \mapsto \neg x$ such that $\neg(\top) = \bot$ and $\neg(\bot) = \top$. Hence, by [the first theorem](#EndpointSwap), $L$ is the trivial De Morgan algebra if Phoa's principle holds. 
\end{proof}

\begin{lemma}
Suppose $L$ is a [[finite set|finite]] [[distributive lattice]] for which Phoa's principle holds. Then $L$ is the trivial distributive lattice.
\end{lemma}

\begin{proof}
If $L$ is a finite distributive lattice, then there are many such functions $f:L \to L$ such that $f(\top) = \bot$ and $f(\bot) = \top$ definable using [the universal property of the finite set with $n$ elements](https://unimath.github.io/agda-unimath/univalent-combinatorics.universal-property-standard-finite-types.html?highlight=universal%20property%20of%20finite%20types#the-universal-property-of-the-standard-finite-types). Hence, by [the first theorem](#EndpointSwap), $L$ is the trivial distributive lattice if Phoa's principle holds. 
\end{proof}

\begin{lemma}
There are no [[distributive lattices]] $L$, whose carrier set is the set of [[natural numbers]], for which Phoa's principle holds. 
\end{lemma}

\begin{proof}
Suppose that $L$ is a [[distributive lattice]] whose carrier set is the set of [[natural numbers]]. Then there are many such functions $f:L \to L$ such that $f(\top) = \bot$ and $f(\bot) = \top$ definable using the universal property of the natural numbers. Hence, by [the first theorem](#EndpointSwap), $L$ is the trivial distributive lattice if Phoa's principle holds, which contradicts that the carrier set of $L$ is the set of natural numbers. 
\end{proof}

## Examples

* In [[Pos]] the category of [[posets]] and [[monotonic functions]], Phoa's principle holds for the [[boolean domain]] $\mathbb{2}$. 

* In [[synthetic Stone duality]], Phoa's principle holds for the [[type of propositions|type of]] [[open propositions]] $\mathrm{Open}$. 

* In [[synthetic domain theory]] and [[synthetic topology]], Phoa's principle holds for a [[dominance]] $\Omega$. 

## Related concepts

* [[distributive lattice]]

* [[flat distributive lattice]]

* [[01-bounded semilattice]]

* [[sigma-frame]]

* [[directed univalence]]

* [[domain theory]], [[synthetic domain theory]]

* [[synthetic quasi-coherence]]

* [[Sierpinski space]]

## References

* [[Wesley Phoa]]: *Domain theory in realizability toposes*, PhD thesis, Trinity College, Cambridge (November 1990) &lbrack;[lfcs:91/ECS-LFCS-91-171](https://www.lfcs.inf.ed.ac.uk/reports/91/ECS-LFCS-91-171), [pdf](https://www.lfcs.inf.ed.ac.uk/reports/91/ECS-LFCS-91-171/ECS-LFCS-91-171.pdf)&rbrack;

* [[Paul Taylor]], *The Fixed Point Property in Synthetic Domain Theory*, Proceedings Sixth Annual IEEE Symposium on Logic in Computer Science, &lbrack;[doi:10.1109/LICS.1991.151640](https://doi.org/10.1109/LICS.1991.151640), [pdf](https://www.paultaylor.eu/ASD/fixpps/fixpps.pdf)&rbrack;

* {#BT09} [[Andrej Bauer]], [[Paul Taylor]], *The Dedekind reals in abstract Stone duality*, Mathematical Structures in Computer Science **19** 4 (2009) 757-838 &lbrack;[doi:10.1017/S0960129509007695](https://doi.org/10.1017/S0960129509007695), [pdf](https://www.paultaylor.eu/ASD/dedras/dedras.pdf)&rbrack;

* [[Davorin Lešnik]], *Synthetic Topology and Constructive Metric Spaces* &lbrack;[arXiv:2104.10399](https://arxiv.org/abs/2104.10399)&rbrack;

* [[Davorin Lešnik]], "Synthetic Topology". In: [[Douglas Bridges]], [[Hajime Ishihara]], [[Michael Rathjen]], [[Helmut Schwichtenberg]], editors, *Handbook of Constructive Mathematics*, Encyclopedia of Mathematics and its Applications, Cambridge University Press, pp. 445 - 482, 04 May 2023. &lbrack;[doi:10.1017/9781009039888.018](https://doi.org/10.1017/9781009039888.018)&rbrack;

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#CGM} [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *Directed Univalence in Synthetic Stone Duality*, unfinished draft; LaTeX documents can be found [here](https://github.com/felixwellen/synthetic-zariski/tree/main/condensed-univalence). 

* [[Jonathan Sterling]], *Baby steps in higher domain theory*, talk at [Homotopy Type Theory and Computing – Classical and Quantum](https://nyuad.nyu.edu/en/events/2024/april/homotopy-type-theory-and-computing.html), [[Center for Quantum and Topological Systems]] ([video](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_b57uwin3?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_b57uwin3))

* {#PS25} [[Leoni Pugh]], [[Jonathan Sterling]], *When is the partial map classifier a Sierpiński cone?* ([arXiv:2504.06789](https://arxiv.org/abs/2504.06789))

* [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* ([arXiv:2505.13096](https://arxiv.org/abs/2505.13096))

* [[Fredrik Bakke]], [[Jonathan Sterling]], [[Mark Damuni Williams]], [[Lingyuan Ye]], *The Synthetic Sierpiński Cone* ([arXiv:2605.00773](https://arxiv.org/abs/2605.00773))

* *Constructive subtleties about the Sierpinski Space*, Mathematics StackExchange. ([web](https://math.stackexchange.com/questions/5085280/constructive-subtleties-about-the-sierpinski-space/5085447))

[[!redirects Phoa's principle]]
[[!redirects Phoa principle]]
