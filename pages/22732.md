
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### Chern insulators

In [[solid state physics]], a [[topological insulator]] which is *not* "[[symmetry protected topological phase|protected by any symmetry]]" has a [[valence bundle]] $V$ over the [[Brillouin torus]] $\mathbb{R}^d$ which is a [[complex vector bundle]] unconstrained by any reality or other conditions, and hence whose class in [[complex K-theory]] $KU^0(\mathbb{T}^d)$ is thought to classify the [[topological phase of matter|topological phase]] of the "unprotected" [[topological insulator]], according to the expected [[K-theory classification of topological phases of matter]].

Now the [[Brillouin torus]] of a realistic material is of effective [[dimension of a manifold|dimension]] $d \leq 3$ and over spaces of these dimensions the only [[characteristic class]] of a [[complex vector bundle]] is its [[first Chern class]]  $c_1(V) \,\in\, H^2\big(\mathbb{T}^d; \, \mathbb{Z}\big)$. Specifically for effectively 2-dimensional materials, the first *Chern number* $c_1[V] = \int_{\mathbb{T}^2} c_1(V) \,\in\, \mathcal{C}$ coincides with this K-theory class:

\begin{tikzcd}[row sep=2pt, column sep=0pt]
  KU^0
  \big(
    \mathbb{T}^2_\ast
  \big)
  &\simeq&
  KU^0
  \big(
    S^2_\ast
  \big)
  &\simeq&
  \mathbb{Z}
  \\
  {[V]} 
  \ar[rrrr, |->]
  &&&&
  c_1[V]
\end{tikzcd}

For this reason such "symmetry un-protected" topological insulators are commonly known as *Chern insulators* and the [[first Chern class|first Chern number]] of their [[valence bundle]] is regarded as labeling their [[topological phases of matter|topological phase]].

### Haldane model & QAHE

While mathematically the case without any quantum symmetry is the simplest one, physically this typically has to be realized with more effort by starting with a symmetry-protected material (such as [[graphene]]) and then "[[symmetry breaking|breaking]]" its symmetries (either by manipulating the material in the lab or, quite often, just theoretically by adding more terms to the Hamiltonian of its theoretical model).

Therefore it is regarded as a seminal achievement when the *[[Haldane model]]* was found, which *intrinsically* breaks the symmetries of an idealized  graphene-like model (by [[spin-orbit coupling]]) and which is generally regarded as the archetype of a (model for a) Chern insulator.

An *extrinsic* way to break the [[time-reversal symmetry]] of a material like [[graphene]] is to simply place it in an external [[magnetic field]]; in this case one sometimes speaks of a *[[quantum Hall material]]*, instead. 

With reference to this relation, the intrinsic effect that breaks the [[time-reversal symmetry]] of some material to a Chern insulator-phase are also known as a *[[quantum anomalous Hall effect]]* (QAHE).


### Chern semi-metals

Notice that for genuinely 3-dimensional [[crystal|crystalline]] [[insulators]] the [[first Chern class]] is necessarily trivial (since there are no 2-[[cycles]] in the [[3-torus]]). But if such insulator is deformed (mentally at least) to a [[semi-metal]] with band gap closures over isolated nodal points $\{k_1, \cdots, k_N\}$ in the [[Brillouin torus]], then the relevant domain space becomes the [[complement]] $\mathbb{T}^3 \setminus \{k_1, \cdots, k_N\}$, and this does admit non-trivial Chern numbers, corresponding to the evaluation of $c_1(V)$ on any [[2-sphere]] surrounding the $I$th nodal point which now measures the topological protection of the semimetal phase (see eg. [Mathai-Thiang 17b](semi-metal#MathaiThiang17b) for a transparent account). 

Some authors speak of "Chern semi-metals" to amplify this.


## Related concepts

* [[topological insulator]]

* [[K-theory classification of topological phases of matter]]



## References

* {#Vanderbilt18} [[David Vanderbilt]],  Section 5.1 of: *Berry Phases in Electronic Structure Theory -- Electric Polarization, Orbital Magnetization and Topological Insulators*, Cambridge University Press (2018) ([doi:10.1017/9781316662205](https://doi.org/10.1017/9781316662205))


* Panagiotis Kotetes, Chapter 5 of: *Topological Insulators*, IOP Science 2019 ([ISBN:978-1-68174-517-6](https://iopscience.iop.org/book/978-1-68174-517-6))


* N. Regnault, B. Andrei Bernevig, *Fractional Chern Insulator*, Phys. Rev. X 1, 021014 (2011) ([arXiv:1105.4867](https://arxiv.org/abs/1105.4867))

[[!redirects Chern insulators]]

[[!redirects quantum anomalous Hall effect]]

[[!redirects Chern semimetal]]
[[!redirects Chern semimetals]]

[[!redirects Chern semi-metal]]
[[!redirects Chern semi-metals]]


