
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of *quantum relations* of [Weaver 2010](#Weaver10), [Weaver & Kuperberg 2011](#WeaverKuperberg11) is a "[[quantum physics|quantum]]" or [[noncommutative geometry]]/[[noncommutative measure theory]]-version of the basic notion of [[relations]] on sets.

Concretely, they define a quantum relation on a [[von Neumann algebra]] $\mathcal{A}$ equipped with an embedding $\mathcal{A} \subset \mathcal{B}\mathscr{H}$ (into the [[bounded operators]] on some [[Hilbert space]]) as an operator [[bimodule]] over the [[commutant]] of $\mathcal{A}$ which is $\ast$-closed in the [[weak operator topology]], and explain why this (non-obvious) definition is sensible; for instance it has good application to [[quantum error correction]].

According to [Kornell 2020](#Kornell20), and in mild paraphrase (following the discussion at *[[dependent linear type]]* and *[[quantum circuits via dependent linear types]]*):

* **[[quantum sets]]** are  [[indexed sets]] of [[finite-dimensional Hilbert spaces]], hence finite-[[rank of a vector bundle|rank]] [[Hilbert bundle|Hilbert]]-[[vector bundles]] over a [[discrete topological spaces]] regarded as a [[sets]], and regarded as equipped with the [[external tensor product]] $\boxtimes$ [of vector bundles](VectBund#TensorMonoidalStructure);

* a **quantum relation** between quantum sets $(x \colon X) \times \mathscr{H}_x$ and $(x' \colon X') \times \mathscr{H}'_x$ is a [[monomorphism]] from a quantum set $\big((x,x') \colon X \times X'\big) \times \mathscr{R}_{(x,x')}$ to $\mathscr{H}^\ast_\bullet \boxtimes \mathscr{H}'_\bullet$:

  $$
    (x,x') \colon X \times X'
    \;\;\;
    \vdash
    \;\;\;
    \mathscr{R}_{(x,y)}
    \hookrightarrow
    \mathscr{H}^\ast_{(x,y)} 
      \otimes
    \mathscr{H}^'_{(x,y)} 
  $$

With [[composition]] the evident [[matrix multiplication]] ([Kornell 2020 (5)](#Kornell20)), quantum relations between quantum sets form a [[category]] $qRel$, which is a [[dagger-compact category]]. 

As such, this serves as [[categorical semantics]] for [[quantum programming languages]] like [[Quipper]] equipped with term recursion, via [[quantum CPOs]] ([Kornell, Lindenhovius & Mislove 2021](#KornellLindenhoviusMislove21)).


## Related concepts

* [[quantum set]]

* [[quantum CPO]]

## References

* {#Weaver10} [[Nik Weaver]], *Quantum relations* &lbrack;[arXiv:1005.0354](https://arxiv.org/abs/1005.0354)&rbrack;

* {#WeaverKuperberg11} [[Nik Weaver]], [[Greg Kuperberg]], *A von Neumann Algebra Approach to Quantum Metrics/Quantum Relations*, Memoirs of the AMS **215** (2011) 1010 &lbrack;[ams:memo-215-1010](https://bookstore.ams.org/memo-215-1010)&rbrack;

* {#Kornell20} [[Andre Kornell]], *Quantum Sets*, J. Math. Phys. **61** 102202 (2020) &lbrack;[doi:10.1063/1.5054128](https://doi.org/10.1063/1.5054128)&rbrack;

  > (cf. *[[quantum set]]*)

* [[Andre Kornell]], *Discrete quantum structures* &lbrack;[arXiv:2004.04377](https://arxiv.org/abs/2004.04377)&rbrack;

* [[Andre Kornell]], *Discrete quantum structures I: Quantum predicate logic*, J. Noncommut. Geom. (2023) &lbrack;[doi:10.4171/jncg/531](https://doi.org/10.4171/jncg/531)&rbrack;

* {#KornellLindenhoviusMislove21} [[Andre Kornell]], [[Bert Lindenhovius]], [[Michael Mislove]], §2 in: *Quantum CPOs*, EPTCS **340** (2021) 174-187 &lbrack;[arXiv:2109.02196](https://arxiv.org/abs/2109.02196), [doi:10.4204/EPTCS.340.9](https://doi.org/10.4204/EPTCS.340.9)&rbrack;

  > (in the context of [[quantum CPOs]])


[[!redirects quantum relations]]


