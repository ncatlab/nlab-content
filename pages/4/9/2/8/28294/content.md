
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
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[solid state physics]], specifically in the discussion of [[topological phases of matter]], the *bulk-boundary correspondence* (or *bulk-edge correspondence*, due to its historical roots in 2D systems such as exhibiting the [[quantum Hall effect]]) states, broadly, that for [[topological phase of matter|topological systems]] on a [[manifold with boundary|domain with boundary]] the topological [[bulk]] [[quantum observables|observables]] correspond to certain [[boundary]] [[quantum observables|observables]] (*[[edge modes]]*).

The general physics intuition is that the nontrivial topological twist in the [[bulk]] must somehow "unwind" at the boundary in order to interpolate to the trivial topological situation beyond the boundary. That "unwinding" is exhibited by "[[edge mode]]" dynamics on the boundary, which hence corresponds to the [[bulk]] [[topological phase of matter|topological phase]].

A general mathematical formalization of the correspondence is usually discussed in the context of the [[K-theory classification of topological phases of matter]]: Concretely, one considers a [[short exact sequence]] of [[C-star algebras|$C^\ast$-algebras]] (typically a Toeplitz extension, cf. [Arici & Mesland 2020](#AriciMesland2020))

\[
  \label{SESOfCStarAlgebras}
  0 
    \to 
  A_{bdr}
    \longrightarrow
  A_{full}
    \longrightarrow
  A_{blk}
    \to 
  0
  \mathrlap{\,,}
\]

whose entries are meant to reflect (cf. [Prodan & Schulz-Baldes 2016 §3](#ProdanSchulz-Baldes2016)), respectively the ([[noncommutative geometry|noncommutative]]) [[geometry]] of the bulk ($A_{blk}$) and the boundary ($A_{bdr}$) inside the full bulk-boundary system ($A_{full}$). Then in the induced [[long exact sequence]] in [[operator K-theory]] (called the *Pimsner–Voiculescu exact sequence* when (eq:SESOfCStarAlgebras) is a Toeptlitz extension)

$$
  \cdots
    \to
  K_{n}(A_{bdr})
    \longrightarrow
  K_{n}(A_{full})
    \longrightarrow
  K_{n}(A_{blk})
    \overset{ \partial }{\longrightarrow}
  K_{n-1}(A_{bdr})
    \longrightarrow
  K_{n-1}(A_{full})
    \longrightarrow
  K_{n-1}(A_{blk})
$$

the [[connecting homomorphism]]

$$
  K_{0}(A_{blk})
    \overset{ \partial }{\longrightarrow}
  K_{-1}(A_{bdr})
$$

maps bulk observables to boundary observables. With due care, the image of this [[connecting homomorphism]] under (schematically) certain [[trace]] operations $\mathcal{T}$ becomes an [[equality]] between bulk and boundary "invariants":

$$
  \mathcal{T}(\partial)
  \,\colon\,
  \mathcal{T}\big( K_{0}(A_{blk}) \big)
  =
  \mathcal{T}\big( K_{-1}(A_{bdr}) \big)
  \mathrlap{\,.}
$$

(cf. [P&S-B '16 Thm. 5.5.1](#ProdanSchulz-Baldes2016))


## Related concepts

* [[edge mode]]

* [[asymptotic symmetry]]


## References

### General

Monograph:

* {#ProdanSchulz-Baldes2016} [[Emil Prodan]], [[Hermann Schulz-Baldes]]: *Bulk and Boundary Invariants for Complex Topological Insulators -- From K-Theory to Physics*, Springer (2016) &lbrack;[doi:10.1007/978-3-319-29351-6](https://doi.org/10.1007/978-3-319-29351-6)&rbrack;

More on the [[C-star algebra|$C^\ast$-algebras]] involved:

* {#AriciMesland2020} Francesca Arici, [[Bram Mesland]]: *Toeplitz extensions in noncommutative topology and mathematical physics*, in: *Geometric Methods in Physics XXXVIII*, Trends in Mathematics, Birkhäuser (2020) \[<a href="https://doi.org/10.1007/978-3-030-53305-2_1">doi:10.1007/978-3-030-53305-2_1</a>, [arXiv:1911.05823](https://arxiv.org/abs/1911.05823)\]

Examples:

* Jacob Shapiro: *The Bulk-Edge Correspondence in Three Simple Cases*, Reviews in Mathematical Physics **32** 03 (2020) 2030003 (2020) \[<a href="https://doi.org/10.1142/S0129055X20300034">doi:10.1142/S0129055X20300034</a>, [arXiv:1710.10649](https://arxiv.org/abs/1710.10649)\]

Further discussion:

* Chris Bourne, [[Alan L. Carey]], Adam Rennie: *The bulk-edge correspondence for the quantum Hall effect in Kasparov theory*, Lett Math Phys **105** (2015) 1253–1273 \[<a href="https://doi.org/10.1007/s11005-015-0781-y">doi:10.1007/s11005-015-0781-y</a>, [arXiv:1411.7527](https://arxiv.org/abs/1411.7527)\]
  > (for [[quantum Hall systems]] using [[Kasparov K-theory]])


* Zixian Zhou, Liang-Liang Wan: *Proof of bulk-edge correspondence for band topology by Toeplitz algebra*, Journal of Physics A: Mathematical and Theoretical **57** 46 (2024) 465203 \[<a href="https://doi.org/10.1088/1751-8121/ad8aab">doi:10.1088/1751-8121/ad8aab</a>, [arXiv:2410.19539](https://arxiv.org/abs/2410.19539)\]



### Under T-Duality

[[!include T-duality in K-theory classification of topological phases -- references]]


[[!redirects bulk-boundary correspondences]]

[[!redirects bulk-edge correspondence]]
[[!redirects bulk-edge correspondences]]

