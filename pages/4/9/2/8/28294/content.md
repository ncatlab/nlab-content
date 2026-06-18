
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

A general mathematical formalization of the correspondence goes back to [Kellendonk, Richter & Schulz-Baldes 2002](#KellendonkRichterSchulz-Baldes2002), in the context of the [[K-theory classification of topological phases of matter]]: Here one considers a [[short exact sequence]] of [[C-star algebras|$C^\ast$-algebras]] (typically a Toeplitz extension, cf. [Arici & Mesland 2020](#AriciMesland2020))

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

whose entries are meant to reflect (cf. [Prodan & Schulz-Baldes 2016 §3](#ProdanSchulz-Baldes2016)), respectively the ([[noncommutative geometry|noncommutative]]) [[geometry]] of the bulk ($A_{blk}$) and the boundary ($A_{bdr}$) inside the full bulk-boundary system ($A_{full}$). Then in the induced [[long exact sequence]] in [[operator K-theory]] (discussed by  [Pimsner & Voiculescu 1980](#PimsnerVoiculescu1980) when (eq:SESOfCStarAlgebras) is a Toeptlitz extension)

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

* [[holographic principle]]

## References

### General

Monographs:

* [[B. Andrei Bernevig]], [[Taylor L. Hughes]]: *Hall Conductance and Edge Modes: The Bulk-Edge Correspondence*, chapter 6 in: *Topological Insulators and Topological Superconductors*, Princeton University Press (2013) &lbrack;[ISBN:9780691151755](https://press.princeton.edu/books/hardcover/9780691151755/topological-insulators-and-topological-superconductors), [jstor:j.ctt19cc2gc](https://www.jstor.org/stable/j.ctt19cc2gc)&rbrack;

* {#ProdanSchulz-Baldes2016} [[Emil Prodan]], [[Hermann Schulz-Baldes]]: *Bulk and Boundary Invariants for Complex Topological Insulators -- From K-Theory to Physics*, Springer (2016) &lbrack;[doi:10.1007/978-3-319-29351-6](https://doi.org/10.1007/978-3-319-29351-6)&rbrack;

More on the [[C-star algebra|$C^\ast$-algebras]] involved:

* {#AriciMesland2020} Francesca Arici, [[Bram Mesland]]: *Toeplitz extensions in noncommutative topology and mathematical physics*, in: *Geometric Methods in Physics XXXVIII*, Trends in Mathematics, Birkhäuser (2020) \[<a href="https://doi.org/10.1007/978-3-030-53305-2_1">doi:10.1007/978-3-030-53305-2_1</a>, [arXiv:1911.05823](https://arxiv.org/abs/1911.05823)\]

Original discussion for [[integer quantum Hall systems]]:

* {#KellendonkRichterSchulz-Baldes2002} [[Johannes Kellendonk]], Thomas Richter, [[Hermann Schulz-Baldes]]: *Edge current channels and Chern numbers in the integer quantum Hall effect*, Rev. Math. Phys. **14** 1 (2002) 87–119 \[<a href="https://doi.org/10.1142/S0129055X02001107">doi:10.1142/S0129055X02001107</a>\] 

* [[Johannes Kellendonk]], [[Hermann Schulz-Baldes]]: *Quantization of edge currents for continuous magnetic operators*, J. Funct. Anal. **209** (2004) 388-413 \[<a href="https://doi.org/10.1016/S0022-1236(03)00174-5">doi:10.1016/S0022-1236(03)00174-5</a>, [arXiv:math-ph/0405021](https://arxiv.org/abs/math-ph/0405021)\]

* [[Johannes Kellendonk]], [[Hermann Schulz-Baldes]]: *Boundary maps for $C^\ast$-crossed products with $\mathbb{R}$ with an application to the quantum Hall effect*, Commun. Math. Phys. **249** (2004) 611-637 \[<a href="https://doi.org/10.1007/s00220-004-1122-7">doi:10.1007/s00220-004-1122-7</a>, [arXiv:math-ph/0405022](https://arxiv.org/abs/math-ph/0405022)\]

using:

* {#PimsnerVoiculescu1980} M. Pimsner and D. Voiculescu: *Exact sequences for K-groups of certain cross-products of $C^\ast$-algebras*, J. Op. Theory **4** (1980) 93–118 &lbrack;[pdf](https://www.theta.ro/jot/archive/1980-004-001/1980-004-001-005.pdf), [[PimsnerVoiculescu-LES.pdf:file]]&rbrack;

Further discussion for [[quantum Hall systems]]:

* Jennifer Cano, [[Meng Cheng]], Michael Mulligan, [[Chetan Nayak]], Eugeniu Plamadeala, Jon Yard: *Bulk-Edge Correspondence in $2+1$-Dimensional Abelian Topological Phases*, Phys. Rev. B **89** (2014) 115116 &lbrack;[arXiv:1310.5708](https://arxiv.org/abs/1310.5708), [doi:10.1103/PhysRevB.89.115116](https://doi.org/10.1103/PhysRevB.89.115116)&rbrack;

* {#Tong16} [[David Tong]]: §6.2 in: *The Quantum Hall Effect*, lecture notes (2016) &lbrack;[arXiv:1606.06687](https://arxiv.org/abs/1606.06687), [course webpage](https://www.damtp.cam.ac.uk/user/tong/qhe.html), [pdf](http://www.damtp.cam.ac.uk/user/tong/qhe/qhe.pdf), [[Tong-QuantumHallEffect.pdf:file]]&rbrack;

* [[Andrea Cappelli]], Lorenzo Maffi: *Bulk-Boundary Correspondence in the Quantum Hall Effect*, J. Phys. A: Math. Theor. **51** (2018) 365401 \[<a href="https://doi.org/10.1088/1751-8121/aad0ab">doi:10.1088/1751-8121/aad0ab</a>, [arXiv:1801.03759](https://arxiv.org/abs/1801.03759)\]

Monograph account:

* [[Eduardo Fradkin]]: *The bulk-edge correspondence*, §15.4 in: *Field Theories of Condensed Matter Physics*, Cambridge University Press (2013) &lbrack;ISBN: 9781139015509, [doi:10.1017/CBO9781139015509](https://doi.org/10.1017/CBO9781139015509), [pdf](http://home.ustc.edu.cn/~gengb/200923/Fradkin,%20Field%20Theories%20of%20Condensed%20Matter%20Physics.pdf)&rbrack;


Further examples:

* Jacob Shapiro: *The Bulk-Edge Correspondence in Three Simple Cases*, Reviews in Mathematical Physics **32** 03 (2020) 2030003 (2020) \[<a href="https://doi.org/10.1142/S0129055X20300034">doi:10.1142/S0129055X20300034</a>, [arXiv:1710.10649](https://arxiv.org/abs/1710.10649)\]


Via [[Kasparov K-theory]]:

* [[Chris Bourne]], [[Alan L. Carey]], [[Adam Rennie]]: *The bulk-edge correspondence for the quantum Hall effect in Kasparov theory*, Lett Math Phys **105** (2015) 1253–1273 \[<a href="https://doi.org/10.1007/s11005-015-0781-y">doi:10.1007/s11005-015-0781-y</a>, [arXiv:1411.7527](https://arxiv.org/abs/1411.7527)\]
  > (for [[quantum Hall systems]])

* [[Chris Bourne]], Johannes Kellendonk, [[Adam Rennie]]: *The K-theoretic bulk-edge correspondence for topological insulators*,  Ann. Henri Poincaré 18 (2017) 1833–1866  \[<a href="https://doi.org/10.1007/s00023-016-0541-2">doi:10.1007/s00023-016-0541-2</a>, [arXiv:1604.02337](https://arxiv.org/abs/1604.02337)\]

See also:

* Zixian Zhou, Liang-Liang Wan: *Proof of bulk-edge correspondence for band topology by Toeplitz algebra*, Journal of Physics A: Mathematical and Theoretical **57** 46 (2024) 465203 \[<a href="https://doi.org/10.1088/1751-8121/ad8aab">doi:10.1088/1751-8121/ad8aab</a>, [arXiv:2410.19539](https://arxiv.org/abs/2410.19539)\]

For [[topological order]] in [[fractional quantum Hall systems]]:

* {#SS26} [[Hisham Sati]], [[Urs Schreiber]]: [[schreiber:Bulk-Edge Correspondence via Higher Gauge Theory]] &lbrack;[arXiv:2605.10232](https://arxiv.org/abs/2605.10232)&rbrack;

In the context of [[rational CFT]] with [[noninvertible symmetries]], in the spirit of the [[FRS theorem]]:

* [[Terry Gannon]], Brandon C. Rayhaun: *Hypergroup Symmetry in Relative Quantum Field Theories and Chiral Algebras* &lbrack;[arXiv:2606.05279](https://arxiv.org/abs/2606.05279)&rbrack;

See also:

* Yizhou Ma, Gen Yue, Tian Lan: *Bulk-boundary correspondence of $(1+1)D$ symmetric gapped phases* &lbrack;[arXiv:2606.19137](https://arxiv.org/abs/2606.19137)&rbrack;



### Under T-Duality

[[!include T-duality in K-theory classification of topological phases -- references]]


[[!redirects bulk-boundary correspondences]]

[[!redirects bulk-edge correspondence]]
[[!redirects bulk-edge correspondences]]

