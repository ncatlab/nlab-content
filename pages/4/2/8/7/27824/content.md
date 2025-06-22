
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[duality]] [[axiom]] used in various branches of [[synthetic mathematics]], such as 

* [[synthetic algebraic geometry]] 

* [[synthetic (infinity,1)-category theory]]

* [[synthetic domain theory]]

* [[synthetic topology]]

  * [[synthetic Stone duality]]

* [[synthetic differential geometry]]

The axiom of synthetic quasi-coherence is a more general version of the [[Kock-Lawvere axiom]] in [[synthetic differential geometry]] as it can apply to [[algebras]] of a generic [[model]] of a [[Horn theory]] rather than just the [[Weil algebras]] of a generic [[local ring]]. 

## Definition

Let $\mathbb{T}$ be a [[Horn theory]] and let $U_\mathbb{T}$ be the generic [[model]] of the theory $\mathbb{T}$. A *[[homomorphism]]* between two models of $\mathbb{T}$ is a [[function]] which preserves all the [[signature (in logic)|signatures]] of the theory $\mathbb{T}$. An *$U_\mathbb{T}$-algebra* consists of a $\mathbb{T}$-model $A$ with a homomorphism $h:U_\mathbb{T} \to A$. An *$U_\mathbb{T}$-algebra homomorphism* on an $U_\mathbb{T}$-algebra $A$ is a homomorphism from $A$ to $U_\mathbb{T}$. The *[[spectrum]]* of $A$ is the set of $U_\mathbb{T}$-algebra homomorphisms: 

$$\mathrm{Spec}(A) \coloneqq \mathrm{hom}_{U_\mathbb{T}\mathrm{Alg}}(A, U_\mathbb{T})$$

An $U_\mathbb{T}$-algebra $A$ is **quasi-coherent** if the canonical evaluation homomorphism

$$\lambda a.\lambda f.f(a):A \to {U_\mathbb{T}}^{\mathrm{Spec}(A)}$$

is an [[isomorphism]]. 

\begin{definition}
The **axiom SQCP** or **synthetic quasi-coherence for the univariate polynomial algebra** states that the free $U_\mathbb{T}$-algebra on one generator $U_\mathbb{T}[x]$ is quasi-coherent.
\end{definition} 

[[Phoa's principle]] for [[distributive lattices]] is equivalent in strength to the axiom SQCP for $U_\mathbb{T}$-algebras where $\mathbb{T}$ is the [[Lawvere theory]] of [[distributive lattices]]. 

An $U_\mathbb{T}$-algebra $A$ is *finitely quotiented* if there is a [[natural number]] $n$ and two [[finite set|finite]] families of elements $a, b:\mathrm{Fin}(n) \to U_\mathbb{T}$ in the generic model such that $A$ is [[isomorphic]] to the quotient algebra $U_\mathbb{T} / a = b$. 

\begin{definition}
The **axiom SQCI** or **synthetic quasi-coherence for finitely quotiented algebras** states that every finitely quotiented $U_\mathbb{T}$-algebra of $U_\mathbb{T}$ is quasi-coherent. 
\end{definition}

In applications to [[synthetic algebraic geometry]] and [[synthetic (infinity,1)-category theory]], one usually considers the notion of synthetic quasi-coherence as applying to finitely presented algebras: A *[[finitely presented]] $U_\mathbb{T}$-algebra* is an $U_\mathbb{T}$-algebra $A$ which is isomorphic to a quotient of the free $U_\mathbb{T}$-algebra on a [[finite set]] of [[generators]]. 

\begin{definition}
The **axiom SQCF** or **synthetic quasi-coherence for finitely presented algebras** states that all finitely presented $U_\mathbb{T}$-algebras $A$ are quasi-coherent.
\end{definition}

In applications to [[synthetic topology]], such as [[synthetic Stone duality]], as well as [[synthetic domain theory]], one usually considers the notion of synthetic quasi-coherence as applying to countably presented algebras: A *countably presented $U_\mathbb{T}$-algebra* is an $U_\mathbb{T}$-algebra $A$ which is isomorphic to a quotient of the free $U_\mathbb{T}$-algebra on a [[countable set]] of [[generators]]. 

\begin{definition}
The **axiom SQCC** or **synthetic quasi-coherence for countably presented algebras** states that all countably presented $U_\mathbb{T}$-algebras $A$ are quasi-coherent. 
\end{definition}

In applications to [[synthetic differential geometry]], one considers Artinian $U_\mathbb{T}$-algebras, i.e. $U_\mathbb{T}$-algebras that satisfy the [[descending chain condition]]. 

\begin{definition}
The **axiom SQCA** or **synthetic quasi-coherence for Artinian algebras** states that all Artinian $U_\mathbb{T}$-algebras are quasi-coherent. 
\end{definition}

The [[Kock-Lawvere axiom]] is the axiom of synthetic quasi-coherence for Artinian $U_\mathbb{T}$-algebras with $\mathbb{T}$ the [[Horn theory]] of a [[local ring]] (hence by the definitions given on this page, every $U_\mathbb{T}$-algebra is a local ring and every Artinian $U_\mathbb{T}$-algebra is a [[Weil algebra]]). 

## Related concepts

* [[Phoa's principle]]

* [[Kock-Lawvere axiom]]

* [[simplicial type theory]]

* [[distributive lattice]]

* [[sigma-frame]]

## References

* [[Ingo Blechschmidt]], *Using the internal language of toposes in algebraic geometry*, PhD thesis (2017) &lbrack;[pdf](https://rawgit.com/iblech/internal-methods/master/notes.pdf), [[Blechschmidt-InternalLanguage.pdf:file]]&rbrack;

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* [[Felix Cherubini]], [[Thierry Coquand]], [[Matthias Hutzler]]: *A foundation for synthetic algebraic geometry*, Mathematical Structures in Computer Science **34** Special Issue 9: *Advances in Homotopy type theory* (2024) 1008-1053 &lbrack;[doi:10.1017/S0960129524000239](https://doi.org/10.1017/S0960129524000239), [arXiv:2307.00073](https://arxiv.org/abs/2307.00073)&rbrack;

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203))

* {#PS25} [[Leoni Pugh]], [[Jonathan Sterling]], *When is the partial map classifier a Sierpiński cone?* ([arXiv:2504.06789](https://arxiv.org/abs/2504.06789))

* [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* ([arXiv:2505.13096](https://arxiv.org/abs/2505.13096))

[[!redirects quasicoherent algebra]]
[[!redirects quasi-coherent algebra]]

[[!redirects synthetic quasicoherence]]
[[!redirects synthetic quasi-coherence]]

[[!redirects axiom of synthetic quasicoherence]]
[[!redirects axiom of synthetic quasi-coherence]]

[[!redirects synthetic quasicoherence axiom]]
[[!redirects synthetic quasi-coherence axiom]]

[[!redirects SQCI]]
[[!redirects axiom SQCI]]
[[!redirects SQCI axiom]]

[[!redirects SQCP]]
[[!redirects axiom SQCP]]
[[!redirects SQCP axiom]]

[[!redirects SQCF]]
[[!redirects axiom SQCF]]
[[!redirects SQCF axiom]]

[[!redirects SQCC]]
[[!redirects axiom SQCC]]
[[!redirects SQCC axiom]]

[[!redirects SQCA]]
[[!redirects axiom SQCA]]
[[!redirects SQCA axiom]]