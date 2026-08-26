
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

The **arithmetical hierarchy** or **arithmetic hierarchy** or **Kleene–Mostowski hierarchy** is a hierarchy used in [[computability theory]] to classify certain [[subsets]] of the [[natural numbers]] based upon the [[complexity]] of the [[first-order logic|first-order]] formulas that define them. 

## In constructive mathematics

In [[constructive mathematics]], the intuitionistic analogue of the arithmetical hierarchy is used to identify certain subsets $S \subseteq \Omega$ of the [[set of truth values]] as [[subobject classifier|classifiers for subsets]] on the arithmetical hierarchy, where functions $\chi_P:\mathbb{N} \to S$ are the [[characteristic function]] for the subsets $P$ of the natural numbers on the arithmetical hierarchy that $S$ represents. 

[Burr 2004](#Burr04) defined an intuitionistic analogue of the arithmetical hierarchy which coincides with the classical arithmetical hierarchy under [[excluded middle]]. In particular, Burr inductively defines the subsets $\Psi_n \subseteq \Omega$ as the analogue of the subsets $\Sigma_n \subseteq \Omega$ and $\Phi_n \subseteq \Omega$ as the analogue of the subsets $\Pi_n \subseteq \Omega$: 

1. For $n = 0$, $\Psi_0 \equiv \Sigma_0 \equiv \Psi_0 \equiv \Pi_0 \equiv \Delta_0 \equiv \mathbb{2} \subseteq \Omega$ where $\mathbb{2}$ is the set of [[booleans]]
2. For $n = 1$, 
$$\Psi_1 \equiv \Sigma_1 \equiv \{P \in \Omega \vert \exists A \in \mathbb{2}^\mathbb{N}.P \iff \exists n \in \mathbb{N}.A(n)\}$$ 
$$\Phi_1 \equiv \Pi_1 \equiv \{P \in \Omega \vert \exists A \in \mathbb{2}^\mathbb{N}.P \iff \forall n \in \mathbb{N}.A(n)\}$$
3. For $n \geq 2$, 
$$\Psi_{n} \equiv \{P \in \Omega \vert \exists A \in (\Phi_{n - 1})^\mathbb{N}.P \iff \exists n \in \mathbb{N}.A(n)\}$$
$$\Phi_{n} \equiv \{P \in \Omega \vert \exists A \in (\Phi_{n - 1})^\mathbb{N}.\exists B \in (\Phi_{n - 2})^{\mathbb{N} \times \mathbb{N}}.P \iff \forall m \in \mathbb{N}.A(m) \to \exists n \in \mathbb{N}.B(m, n)\}$$

If we try define the intutionistic analogue of the $\Delta_n$ subsets for finite $n$ as $\Delta_n \equiv \Phi_n \cap \Psi_n$, we find out that $\Delta_n$ ends up being just the set of [[booleans]]; hence Burr's hierarchy does not include the $\Delta_n$ subsets. 

For example, the set of [[semidecidable truth values]] $\Psi_1 \subseteq \Omega$ is the classifier for semidecidable subsets, such that any function $\chi_P:\mathbb{N} \to \Psi_1$ is the characteristic function of a semidecidable subset $P \subseteq \mathbb{N}$. From this perspective, [Diener 2018](#Diener18) considers the various [[principles of omniscience]] as the $\Psi_1$ analogue of various constructive [[taboos]] in the [[propositional logic]] (which [Diener 2018](#Diener18) denotes using the classical $\Sigma_1^0$ instead of the intuitionistic $\Psi_1$): 

1. the [[limited principle of omniscience]] is $\Psi_1$-[[excluded middle]]
2. the [[weak limited principle of omniscience]] is $\Psi_1$-[[weak excluded middle]]
3. [[Markov's principle]] is the $\Psi_1$-[[double negation law]]
4. the [[lesser limited principle of omniscience]] is $\Psi_1$-[[De Morgan's law]]

One can extend the intuitionistic arithmetical hierarchy to the $\alpha$-recursive $\Psi_\alpha$ and $\Phi_\alpha$ by using a constructive notion of recursive [[ordinal]] such as the ordinals first defined by [[Per Martin-Löf]] in 1970 and which appear in [Coquand, Lombardi, & Neuwirth 2024](#CLN24). 

### Hyperarithmetical subsets

The supremum of the entire intuitionistic arithmetical hierarchy, including all the $\alpha$-recursive levels, is denoted as $\Delta_1^1$ and represents the beginning of the analytical hierarchy, the hyperarithmetical subsets. The classifier of hyperarithmetical subsets $\Delta_1^1 \subseteq \Omega$ has the property of being the [[initial object|initial]] [[sigma-complete Heyting algebra|$\sigma$-complete Heyting algebra]], and elements of $\Delta_1^1$ can be called *hyperarithmetical truth values* or *hyperarithmetical propositions*. Functions $\chi_P:\mathbb{N} \to \Delta_1^1$ are [[characteristic functions]] for hyperarithmetical subsets $P$ of the [[natural numbers]]. 

Since the hyperarithmetical subset classifier $\Delta_1^1$ is a $\sigma$-complete Heyting subalgebra of the set of all truth values $\Omega$, it is a [[sigma-frame|$\sigma$-subframe]] of $\Omega$ and can be used to define [[Dedekind cuts]] and a form of the [[Dedekind real numbers]] that sits in between the ones defined using [[quasidecidable]] Dedekind cuts and the ones defined using all Dedekind cuts, $\mathbb{R}_\mathrm{C} \subseteq \mathbb{R}_\mathrm{Q} \subseteq \mathbb{R}_\mathrm{HA} \subseteq \mathbb{R}_\mathrm{D}$. 

However, in the presence of the [[limited principle of omniscience]], the [[initial object|initial]] [[sigma-complete Heyting algebra|$\sigma$-complete Heyting algebra]] is just the [[boolean domain]], and so the [[limited principle of omniscience]] completely collapses the intuitionistic arithmetical hierarchy as a hierarchy of subsets of $\Omega$. The hierarchy of real numbers also partially collapses: the Cauchy reals, quasidecidable Dedekind reals, and hyperarithmetical Dedekind reals all coincide with each other since all of them are [[discrete fields]] in the presence of the [[limited principle of omniscience]], $\mathbb{R}_\mathrm{C} = \mathbb{R}_\mathrm{Q} = \mathbb{R}_\mathrm{HA} \subseteq \mathbb{R}_\mathrm{D}$. 

[[Phoa's principle]] can never hold for the hyperarithmetical subset classifier since $\Delta_1^1$ is a [[Heyting algebra]]. Thus, Phoa's principle for the [[distributive lattices]] of either the [[semidecidable truth values]] or the [[quasidecidable truth values]] is enough to keep $\Delta_1^1$ distinct from the set of semidecidable truth values and the set of quasidecidable truth values, and similarly keep $\mathbb{R}_\mathrm{HA}$ distinct from both the Cauchy reals and the quasidecidable Dedekind reals. 

## Related concepts

* [[decidability]], which correspond to $\Delta_0$ in the arithmetical hierarchy

* [[semidecidability]], which correspond to $\Psi_1 \equiv \Sigma_1$ in the arithmetical hierarchy

## References

* {#Burr04} [[Wolfgang Burr]]: *The intuitionistic arithmetical hierarchy*, in: J. Van Eijck, V. Van Oostrom, A. Visser (eds.): *Logic Colloquium ’99*, Lecture Notes in Logic **17**, Cambridge University Press (2004) 510--59 &lbrack;[doi:10.1017/9781316755921.004](https://doi.org/10.1017/9781316755921.004)&rbrack;

* {#Diener18} [[Hannes Diener]]: *Constructive Reverse Mathematics*, Habil. thesis, Univ. Siegen (2018) &lbrack;[arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306)&rbrack;

* [[Takayuki Kihara]]: *The Arithmetical Hierarchy: A Realizability-Theoretic Perspective*, to appear in Journal of Mathematical Logic &lbrack;[arXiv:2410.15795](https://arxiv.org/abs/2410.15795)&rbrack;

* [[Joan Moschovakis]]: *Intuitionistic Logic*, The Stanford Encyclopedia of Philosophy (Summer 2024 Edition), Edward N. Zalta & Uri Nodelman (eds.) &lbrack;[web](https://plato.stanford.edu/archives/sum2024/entries/logic-intuitionistic/)&rbrack; 

* {#CLN24} [[Thierry Coquand]], [[Henri Lombardi]], [[Stefan Neuwirth]]: *Constructive theory of ordinals*. In: Marco Benini, Olaf Beyersdorff, Michael Rathjen, Peter Michael Schuster: Mathematics for Computation - M4C, World Scientific, pp.287-318, 2023, 978-981-124-521-3 &lbrack;[doi:10.1142/9789811245220_0012](https://doi.org/10.1142/9789811245220_0012), [arXiv:2201.04352](https://arxiv.org/abs/2201.04352)&rbrack;

* Wikipedia, *[Arithmetical hierarchy](https://en.wikipedia.org/wiki/Arithmetical_hierarchy)*

[[!redirects arithmetical hierarchy]]
[[!redirects arithmetic hierarchy]]
[[!redirects Kleene–Mostowski hierarchy]]

[[!redirects intuitionistic arithmetical hierarchy]]
[[!redirects intuitionistic arithmetic hierarchy]]
[[!redirects intuitionistic Kleene–Mostowski hierarchy]]

[[!redirects hyperarithmetical]]
[[!redirects hyperarithmetical subset]]
[[!redirects hyperarithmetical subsets]]
[[!redirects hyperarithmetical truth value]]
[[!redirects hyperarithmetical truth values]]
[[!redirects hyperarithmetical proposition]]
[[!redirects hyperarithmetical propositions]]

[[!redirects initial sigma-complete Heyting algebra]]
[[!redirects initial σ-complete Heyting algebra]]