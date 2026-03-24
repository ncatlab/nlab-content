> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak

***

**Bulk-Boundary correspondence**

In [[solid state physics]], specifically in the discussion of [[topological phases of matter]], the *bulk-boundary correspondence* (or *bulk-edge correspondence*, due to its historical roots in 2D systems such as exhibiting the [[quantum Hall effect]]) states broadly that for [[topological phase of matter|topological systems]] on a [[manifold with boundary|domain with boundary]] the topological [[bulk]] [[quantum observables|observables]] correspond to certain [[boundary]] [[quantum observables|observables]] (*[[edge modes]]*).

The general physics intuition is that the nontrivial topological twist in the [[bulk]] must somehow "unwind" at the boundary in order to interpolate to the trivial topological situation beyond the boundary. That "unwinding" is exhibited by "[[edge mode]]" dynamics on the boundary, which hence corresponds to the bulk topological phase.

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

* Zixian Zhou, Liang-Liang Wan: *Proof of bulk-edge correspondence for band topology by Toeplitz algebra*, Journal of Physics A: Mathematical and Theoretical **57** 46 (2024) 465203 \[<a href="https://doi.org/10.1088/1751-8121/ad8aab">doi:10.1088/1751-8121/ad8aab</a>, [arXiv:2410.19539](https://arxiv.org/abs/2410.19539)\]


[[!include T-duality in K-theory classification of topological phases -- references]]


\linebreak


## Nonconservative mathematical adjectives

In the practice of the naming of concepts in [[mathematics]], it happens that an adjective added to a term not just qualifies that term but actually contradicts it. 

For instance "[[partial functions]]" are not special kinds of functions but are, generally, not functions at all. (More examples are listed below.) This is in contrast to cases like "[[abelian groups]]", which are indeed special kinds of [[groups]].

Hence such *nonconservative adjectives* are modifiers in mathematical terminology that fundamentally alter, negate, or expand the defining axioms of a base term, rather than simply restricting them.

In linguistics one speaks in such cases of *[privative adjectives](https://en.wikipedia.org/wiki/Privative_adjective)*. For example a "fake X" is not an "X", hence "fake" is a privative adjective in the English language.

While strict logic may suggest to avoid nonconservative/privative adjectives, their use in mathematics is pragmatic and the meaning is typically suggestive and readily grasped, instead of misleading. For instance the intended meaning of "[[manifolds with boundary]]" is clear, and yet (if the boundary is non-empty) these are not strictly speaking "[[manifolds]]", whence "with boundary" is a nonconservative qualifier.

Accordingly, an earlier suggestion in this entry to refer to nonconservatively qualified terminology as "red herrings" is (while it may have gained some popularity, though maybe for the wrong reason) not really appropriate, as "red herrings" in the figurative sense are deliberately misleading.



### FQH Excitation modes



On multiple modes resolving the would-be single GMP mode for [FQH excitations](quantum+Hall+effect#CollectiveExcitations) 

near filling fraction $\nu = 1/4$:

* Dung Xuan Nguyen, [[F. D. M. Haldane]], [[Edward H. Rezayi]], [[Dam Thanh Son]], Kun Yang: *Multiple Magnetorotons and Spectral Sum Rules in Fractional Quantum Hall Systems*, Phys. Rev. Lett. **128** (2022) 246402 \[<a href="https://doi.org/10.1103/PhysRevLett.128.246402">doi:10.1103/PhysRevLett.128.246402</a>, [arXiv:2111.10593](https://arxiv.org/abs/2111.10593), suppl:[pdf](https://journals.aps.org/prl/supplemental/10.1103/PhysRevLett.128.246402/Supp.pdf)\]

at [Jain filling fractions](quantum+Hall+effect#CompositeParticlePicture) $n/(2 p n \pm 1)$ with ${\vert n \vert}\geq 2$ (e.g. $\nu = 2/5, 3/7, 2/9, 2/7$):

* [[Ajit C. Balram]], Zhao Liu, [[Andrey Gromov]], [[Zlatko Papić]]: *Very-High-Energy Collective States of Partons in Fractional Quantum Hall Liquids*, Phys. Rev. X **12** (2022) 021008 \[<a href="https://doi.org/10.1103/PhysRevX.12.021008">doi:10.1103/PhysRevX.12.021008</a>, [arXiv:2111.10395](https://arxiv.org/abs/2111.10395)\]

at filling fractions $\nu  = n/(4 n \pm 1)$:

* [[Ajit C. Balram]], G. J. Sreejith, [[Jainendra K. Jain]]: *Splitting of Girvin-MacDonald-Platzman density wave and the nature of chiral gravitons in fractional quantum Hall effect*, Phys. Rev. Lett. **133** (2024) 246605 \[<a href="https://doi.org/10.1103/PhysRevLett.133.246605">doi:10.1103/PhysRevLett.133.246605</a>, [arXiv:2406.02730](https://arxiv.org/abs/2406.02730)\]

in FQH liquids that are not fully spin-polarized:

* Rakesh K. Dora, [[Ajit C. Balram]]: *Dispersion of collective modes in spinful fractional quantum Hall states on the sphere* \[<a href="https://arxiv.org/abs/2509.13100">arXiv:2509.13100</a>\] 

\linebreak

\begin{example}
In the category of [[schemes]] the subcategory of [[affine schemes]] is dense, see [[affine scheme#AffineSchemesFullSubcategoryOfOppositeOfRings|here]].
\end{example}

\begin{example}
In the category of [[smooth manifolds]], the full subcategory whose objects are given by $\mathbb{R}^n$ for $n\geq 1$ with the standard smooth structure, is dense.
\end{example}

Proof: The restricted Yoneda to the full subcategory spanned by ${\{R\}}$ is faithful, hence so is when restricted to the subcat spanned by $\{R,R^2\}$. To see fullness when restricted to the subcat spanned by $\{R,R^2\}$, suppose we are given a morphism $\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ of presheaves on $\mod_{\{R,R^2\}}$. Given $x\in M$, write $z_x\in N$ for the image of $1\in R$ of the induced map $R\to N$ from $R\to M,1\mapsto x$. Write $[x,y]:R^2\to M$ for the map sending $(1,0)$ and $(0,1)$ to $x$ and $y$, respectively, and write $z_{[x,y]}:R^2\to N$ for the induced map. Then $z_{[x,y]}=[z_x,z_y]$ by compatibility with the $i$-th component map $c_i:R\to R^2$, $i=1,2$. Thus, compatibility with the diagonal map $\Delta:R\to R^2$ gives $z_{x+y}=\Delta^*z_{[x,y]}=\Delta^*[z_x,z_y]=z_x+z_y$. On the other hand, given $r\in R$, compatibility with $r: k\to k$ gives $z_{r x}=rz_x$. Thus $x\mapsto z_x$ defines a map $f:M\to N$ of $R$-modules such that $f^*:\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ is the morphism we began with.



## Definition

A complex (or real) [[extended C*-algebra]] whose bounded part is a [[von Neumann algebra]].

Equivalently (by a theorem due to Dixon and Zakirov–Chilin), a complex (or real) [[*-algebra]] $A$ of closed densely defined unbounded operators on a [[Hilbert space]] closed under the operations of strong sum, strong multiplication, passing to adjoints, contains all scalar multiples of the identity operator, for every $x\in A$ we have $(1+x^*x)^{-1}\in A$ (equivalently, $x$ is affiliated with $A_b$), and the [[*-subalgebra]] $A_b$ of bounded operators in $A$ is a [[von Neumann algebra]].

## Properties

For any [[von Neumann algebra]] there is a unique (up to a unique isomorphism) maximal extended von Neumann algebra that has $A$ as its bounded part, namely, the extended von Neumann algebra of locally measurable operators affiliated with $A$.

The [[reduction theory]] for [[von Neumann algebras]] can be extended to the case of extended von Neumann algebras.

## References

* P. G. Dixon, _Generalized B*-algebras_, Proceedings of the London Mathematical Society s3-21:4 (1970), 693-715.  [DOI](https://doi.org/10.1112/plms/s3-21.4.693).

  **  establishes functional calculus for commutative extended C*-algebras and Gelfand-Neumark theorem for noncommutative extended C*-algebras
  ** defines “concrete” C*-algebras in Definition 7.1
  ** shows that “abstract” and “concrete” extended C*-algebras are the same notion, see Theorem 7.13

* P. G. Dixon, _Unbounded operator algebras_, Proceedings of the London Mathematical Society s3-23:1 (1971), 53-69.  [DOI](https://doi.org/10.1112/plms/s3-23.1.53).

  **  defines “concrete” extended von Neumann algebras (called EW*-algebras there) in Definition 1.2
  ** develops reduction theory in Section 3
  ** studies measurable operators in Section 4 and 5
  ** studies locally measurable operators in Section 6 and 7

* B. S. Zakirov, V. I. Chilin, _Abstract characterization of EW*-algebras_, Functional Analysis and Its Applications 25:1 (1991), 63-64.  [DOI](https://doi.org/10.1007/bf01090683).

  *  shows that “abstract” and “concrete” extended von Neumann algebras are the same

  *  proves that extended von Neumann algebras are precisely those [[extended C*-algebras]] whose bounded part is a [[von Neumann algebra]]
