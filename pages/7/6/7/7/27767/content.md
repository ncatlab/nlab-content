
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

An *assembly* is a mathematical structure on a [[partial combinatory algebra]] used to construct [[realizability toposes]] and used for the [[categorical semantics]] of [[impredicative universes]] in [[type theory]]. 

## Definition

Given a [[partial combinatory algebra]] $A$, an **$A$-valued assembly** $X$ consists of a set ${|X|}$ and any one of these equivalent structures:

* a [[family of sets]] $(E_X(x))_{x \in |X|}$ such that each $E_X(x)$ is an [[inhabited sets|inhabited]] [[subset]] of $A$ for all $x \in A$. 

* a [[multivalued function]] $E_X \colon {|X|} \to P_{\ge 1}(A)$ from $|X|$ to $A$, where $P_{\ge 1}(A)$ denotes the set of [[inhabited set|inhabited]] subsets of $A$. 

* an [[entire relation]] $E_X(x, a)$ indexed by $x \in |X|$ and $a \in A$.

\begin{remark}
The **assemblies** or **$\omega$-sets** of [Uemura 2019](#Uemura19) are precisely the $\mathbb{N}$-valued assemblies. 
\end{remark}

Given a [[partial combinatory algebra]] $A$, an assembly is **partitioned** if, for each definition above respectively, 

* each $E_X(x)$ is a [[singleton]] for all $x \in |X|$, 

* the [[multivalued function]] $E_X$ takes values in singletons, i.e. is a function ${|X|} \to A$.

* the [[entire relation]] $E_X$ is a [[functional relation]]. 

## The category of assemblies

Let $A$ be a [[partial combinatory algebra]]. 

\begin{definition}
A **morphism** $X \to Y$ between $A$-valued assemblies is a function $f \colon {|X|} \to {|Y|}$ for which there exists $a \in A$ such that for all $x\in X$ and $b\in E_X(x)$, $a\cdot b$ is defined and belongs to $E_Y(f(x))$.
\end{definition}

\begin{definition}
The **category of $A$-valued assemblies** is the [[category]] whose objects are $A$-valued assemblies, and whose [[morphisms]] are morphisms as defined above. 
\end{definition}

The category of $A$-valued assemblies is denoted $\mathrm{Asm}(A)$ ([Maietti, Pasquali, & Rosolini 2019](#MPR19), [Awodey & Emmenegger 2025](#AE25)) or $\mathrm{Ass}(A)$ ([Vermeeren 2009](#Vermeeren09)). The category of partitioned $A$-valued assemblies is denoted $\mathrm{PAsm}(A)$ ([Frey 2014](#Frey14)) or $\mathbb{P}$ ([Awodey & Emmenegger 2025](#AE25)) or $\mathrm{PAss}(A)$.

**Note:** *Due to confusion with the English language obscenity, the nLab now discourages the usage of the term "Ass" and "PAss" on the nLab itself to refer to the category of assemblies and partitioned assemblies respectively, instead preferring the alternate terms listed. If you encounter uses of this sort elsewhere on the nLab, please replace them if possible.* 

\begin{theorem}
$\mathrm{Asm}(A)$ and $\mathrm{PAsm}(A)$ are finitary [[extensive category|lextensive]].  Moreover, $\mathrm{Asm}(A)$ is [[regular category|regular]] and [[locally cartesian closed category|locally cartesian closed]].
\end{theorem}

\begin{theorem}
The [[realizability topos]] is the [[ex/reg completion]] of $\mathrm{Asm}(A)$. 
\end{theorem}

\begin{theorem}
In the presence of the [[axiom of choice]], $\mathrm{Asm}(A)$ is the [[reg/lex completion]] of $\mathrm{PAsm}(A)$ and the realizability topos is the [[ex/lex completion]] of $\mathrm{PAsm}(A)$. 
\end{theorem}

+-- {: .num_remark #pax}
###### Remark 
A general result about the ex/lex completion $C_{ex/lex}$ of a left exact category $C$ is that it has enough regular [[projective object|projectives]], meaning objects $P$ such that $\hom(P, -) \colon C_{ex/lex} \to Set$ preserves regular epis. In fact, the regular projective objects coincide with the objects of $C$ (as a subcategory of $C_{ex/lex}$). Of course, when $C_{ex/lex}$ is a topos, where every epi is regular, this means $C_{ex/lex}$ has enough projectives, or satisfies (external) [[COSHEP]]. It also satisfies internal [[COSHEP]], since binary products of projectives, i.e., products of objects of $C$, are again objects of $C$ (see [this result](/nlab/show/internally+projective+object#enough)). 
=--

+-- {: .num_remark #ac}
###### Remark
The fact that a realizability topos is an ex/lex completion depends on the [[axiom of choice]] for [[Set]], since it requires the partitioned assemblies to be projective objects therein.  In the absence of the axiom of choice, the projective objects in a realizability topos are the (isomorphs of) partitioned assemblies whose underlying set is [[projective object|projective]] in [[Set]].  Thus, if [[COSHEP]] holds in [[Set]], then a realizability topos is the ex/wlex completion of the category of such "projective partitioned assemblies" (wlex because this category may not have finite limits, only weak finite limits).  Without some choice principle, the realizability topos may not be an ex/wlex completion at all; but it is still an ex/reg completion of $\mathrm{Asm}(A)$.
=--

## Related concepts

* [[realizability]]

* [[realizability topos]]

* [[impredicative polymorphism]]

## References

* {#Vermeeren09} [[Stijn Vermeeren]], _Realizability Toposes_, 2009 ([pdf](http://stijnvermeeren.be/download/mathematics/essay.pdf))

* {#Frey14} [[Jonas Frey]], _Characterizing partitioned assemblies and realizability toposes_ ([arXiv:1404.6997](http://arxiv.org/abs/1404.6997))

* {#Uemura19} [[Taichi Uemura]], *Cubical Assemblies, a Univalent and Impredicative Universe and a Failure of Propositional Resizing*, in 24th International Conference on Types for Proofs and Programs (TYPES 2018). Leibniz International Proceedings in Informatics (LIPIcs), Volume 130, pp. 7:1-7:20, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2019) ([doi:10.4230/LIPIcs.TYPES.2018.7](https://doi.org/10.4230/LIPIcs.TYPES.2018.7), [arXiv:1803.06649](https://arxiv.org/abs/1803.06649))

* {#MPR19} [[Maria Emilia Maietti]], [[Fabio Pasquali]], [[Giuseppe Rosolini]], *Elementary Quotient Completions, Church's Thesis, and Partioned Assemblies*, Logical Methods in Computer Science, Volume 15, Issue 2 (June 25, 2019). &lbrack;[doi:10.23638/LMCS-15(2:21)2019](https://doi.org/10.23638/LMCS-15%282%3A21%292019), [arXiv:1802.06400](https://arxiv.org/abs/1802.06400)&rbrack;

* {#AE25} [[Steve Awodey]], [[Jacopo Emmenegger]], *Toward the effective 2-topos* &lbrack;[arXiv:2503.24279](https://arxiv.org/abs/2503.24279)&rbrack;

[[!redirects assembly]]
[[!redirects assemblies]]

[[!redirects partitioned assembly]]
[[!redirects partitioned assemblies]]

[[!redirects category of assemblies]]
[[!redirects categories of assemblies]]

[[!redirects category of partitioned assemblies]]
[[!redirects categories of partitioned assemblies]]

[[!redirects omega-set]]
[[!redirects omega-sets]]

[[!redirects partitioned omega-set]]
[[!redirects partitioned omega-sets]]

[[!redirects category of omega-set]]
[[!redirects categories of omega-sets]]

[[!redirects category of partitioned omega-set]]
[[!redirects categories of partitioned omega-sets]]

[[!redirects ω-set]]
[[!redirects ω-sets]]

[[!redirects partitioned ω-set]]
[[!redirects partitioned ω-sets]]

[[!redirects category of ω-set]]
[[!redirects categories of ω-sets]]

[[!redirects category of partitioned ω-set]]
[[!redirects categories of partitioned ω-sets]]

[[!redirects Asm]]
[[!redirects PAsm]]

[[!redirects PAss]]

[[!redirects ωSet]]
[[!redirects PωSet]]