[[!redirects Galois deformation rings]]

#Contents#
* table of contents
{:toc}

## Idea

A *Galois deformation ring* is the [[ring]] that [[representable functor|represents]] the [[deformation functor]] $\mathrm{Def}_{\overline{\rho}}$ that assigns to a complete [[Noetherian ring|Noetherian]] local $W(\mathbb{F})$-algebra $A$ the set of deformations (equivalence classes of lifts) of a fixed residual representation $\overline{\rho}:\Gal(\overline{F}/F)\to GL_{n}(\mathbb{F})$ to $A$.

They were first introduced by Mazur, and find application in modularity, i.e. showing that a [[Galois representation]] comes from a [[modular form]]. As such they are instrumental in the proof of the [[Taniyama-Shimura conjecture]].

## Definitions

Let $F$ be a [[number field]], let $\mathbb{F}$ be a [[finite field]], with ring of [[Witt vectors]] $W(\mathbb{F})$, and let $\overline{\rho} \colon \Gal(\overline{F}/F)\to GL_{n}(\mathbb{F})$ be a [[linear representation]]. In reference to $\mathbb{F}$ being the [[residue field]] of $W(\mathbb{F})$ we refer to $\overline{\rho}$ as a *residual representation*.

\begin{definition}
Let $A$ be a complete Noetherian $W(\mathbb{F})$-algebra. A _lift_, or *framed deformation*, of $\overline{\rho}$ is a [[Galois representation]] $\rho \colon \Gal(\overline{F}/F)\to GL_{n}(A)$ such that reduction of $\rho$ by the unique [[maximal ideal]] $\mathfrak{m}$ of $A$ gives back $\overline{\rho}$.
\end{definition}

\begin{definition}
A *deformation* is an [[equivalence class]] of lifts, where two lifts are considered equivalent if they are [[conjugation action|conjugate]] by an element of the [[kernel]] of the reduction map.
\end{definition}

\begin{definition}\label{FramedDeformationFunctor}
The *framed deformation functor * $\mathrm{Def}_{\overline{\rho}}^{\Box}$ is the functor assigns to a complete Noetherian local algebra $A$ the set of lifts of $\overline{\rho}$ to $A$.
\end{definition}

\begin{theorem}
The framed deformation functor $\mathrm{Def}_{\overline{\rho}}^{\Box}$ (Def. \ref{FramedDeformationFunctor}) is represented by a lift $\rho(R_{\overline{\rho}}^{\Box})$. We refer to the ring $R_{\overline{\rho}}^{\Box}$ as the *universal framed deformation ring*.
\end{theorem}

\begin{definition}
The *deformation functor* $\mathrm{Def}_{\overline{\rho}}^{\Box}$ is the functor assigns to a complete Noetherian local algebra $A$ the set of lifts of $\overline{\rho}$ to $A$
\end{definition}

\begin{definition}
We say that $\overline{\rho}$ is *Schur* if $\mathrm{End}_{\mathbb{F}[\mathrm{Gal}(\overline{F}/F)]}\overline{\rho}=\mathbb{F}$.
\end{definition}

\begin{theorem}
Let $\overline{\rho}$ be Schur. Then the deformation functor $\mathrm{Def}_{\overline{\rho}}$ is represented by a deformation $\rho(R_{\overline{\rho}}^{\Box})$. We refer to the ring $R_{\overline{\rho}}$ as the *universal deformation ring*.
\end{theorem}

## Tangent spaces and Galois cohomology

(...)

## Related

* [[deformation theory]]

## References

* [[Toby Gee]], _Modularity Lifting Theorems: Notes for Arizona Winter School_, [pdf](http://wwwf.imperial.ac.uk/~tsg/Index_files/ArizonaWinterSchool2013.pdf)


[[!redirects Galois deformation rings]]

