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



# Contents 
* table of contents 
{: toc}

## Idea 

A realizability topos is a [[topos]] which embodies the [[realizability interpretation]] of [[intuitionistic mathematics|intuitionistic]] [[number theory]] (due to Kleene) as part of its [[internal logic]]. Realizability toposes form an important class of [[elementary toposes]] that are not [[Grothendieck toposes]], and don't even have a [[geometric morphism]] to [[Set]].

The input datum for forming a realizability topos is a [[partial combinatory algebra]], or PCA. 

* When the PCA is [[Kleene's first algebra]] $\mathcal{K}_1$, the resulting topos is called the [[effective topos]] $RT(\mathcal{K}_1)$. 

* When the PCA is [[Kleene's second algebra]] $\mathcal{K}_2$ then $RT(\mathcal{K}_2)$ is the [[function realizability topos]].


## Constructions 

There are a number of approaches toward constructing realizability toposes. One is through [[tripos]] theory, and another is through assemblies (actually the latter is a family of related approaches).

Let $A$ be a [[partial combinatory algebra|PCA]] --- in [[Set]], for simplicity, but similar constructions usually work over other base toposes.


### Via tripos theory 

There is a [[tripos]] whose base category is $Set$ and for which the preorder $P_A(X)$ of $X$-indexed predicates is the set $P(A)^X$ of functions from $X$ to the [[powerset]] $P(A)$ of $A$.  The order relation sets $\phi \le \psi$ if there exists $a\in A$ such that $b\in \phi(x)$ implies $a\cdot b \in \psi(x)$ for all $x$; note that $a$ must be chosen uniformly across all $x\in X$.

Applying the tripos-to-topos construction to this tripos produces the realizability topos over $A$.  See [[tripos]] for details.


### Via assemblies 

+-- {: .num_defn} 
###### Definition 
An **assembly** $X$ consists of a set ${|X|}$ and a function $[-]_X \colon {|X|} \to P_{\ge 1}(A)$, where $P_{\ge 1}(A)$ denotes the set of [[inhabited set|inhabited]] subsets of $A$.  An assembly is **partitioned** if $[-]_X$ takes values in singletons, i.e. is a function ${|X|} \to A$.

A **morphism** $X \to Y$ between assemblies is a function $f \colon {|X|} \to {|Y|}$ for which there exists $a \in A$ such that for all $x\in X$ and $b\in [x]_X$, $a\cdot b$ is defined and belongs to $[f(x)]_Y$.
=--

The categories of assemblies and partitioned assemblies are denoted $Ass_A$ and $PAss_A$ respectively.

+-- {: .num_prop} 
###### Proposition 
$Ass_A$ and $PAss_A$ are finitary [[extensive category|lextensive]].  Moreover, $Ass_A$ is [[regular category|regular]] and [[locally cartesian closed category|locally cartesian closed]].
=-- 

+-- {: .num_defn} 
###### Theorem
$Ass_A$ is the [[reg/lex completion]] of $PAss_A$.  Therefore, [[ex/lex completion]] of $PAss_A$ coincides with the [[ex/reg completion]] of $Ass_A$.  This category is a [[topos]], called the **realizability topos** of $A$. 
=-- 

+-- {: .num_remark #pax}
###### Remark 
A general result about the ex/lex completion $C_{ex/lex}$ of a left exact category $C$ is that it has enough regular [[projective object|projectives]], meaning objects $P$ such that $\hom(P, -) \colon C_{ex/lex} \to Set$ preserves regular epis. In fact, the regular projective objects coincide with the objects of $C$ (as a subcategory of $C_{ex/lex}$). Of course, when $C_{ex/lex}$ is a topos, where every epi is regular, this means $C_{ex/lex}$ has enough projectives, or satisfies (external) [[COSHEP]]. It also satisfies internal [[COSHEP]], since binary products of projectives, i.e., products of objects of $C$, are again objects of $C$ (see [this result](/nlab/show/internally+projective+object#enough)). 
=--

+-- {: .num_remark #ac}
###### Remark
The fact that a realizability topos is an ex/lex completion depends on the [[axiom of choice]] for [[Set]], since it requires the partitioned assemblies to be projective objects therein.  In the absence of the axiom of choice, the projective objects in a realizability topos are the (isomorphs of) partitioned assemblies whose underlying set is [[projective object|projective]] in [[Set]].  Thus, if [[COSHEP]] holds in [[Set]], then a realizability topos is the ex/wlex completion of the category of such "projective partitioned assemblies" (wlex because this category may not have finite limits, only weak finite limits).  Without some choice principle, the realizability topos may not be an ex/wlex completion at all; but it is still an ex/reg completion of $Ass_A$.
=--


## Properties

### Axiomatic characterization
 {#Characterization}

The following is a statement characterizing realizability toposes which is analogous to the [[Giraud axioms]] characterizing [[Grothendieck toposes]].

+-- {: .num_theorem}
###### Theorem

A [[locally small category]] $\mathcal{E}$ is ([[equivalence of categories|equivalent]] to) a realizability topos precisely if

1. $\mathcal{E}$ is [[exact category|exact]] and [[locally cartesian closed category|locally cartesian closed]];

1. $\mathcal{E}$ has [[enough projectives]] and the [[full subcategory]] $Proj(\mathcal{E}) \hookrightarrow \mathcal{E}$ has all [[finite limits]];

1. the [[global section]] [[functor]] $\Gamma \coloneqq \mathcal{E}(\ast,-) \colon \mathcal{E}\longrightarrow $ [[Set]] 

   1. has a [[right adjoint]]  $\nabla \colon Set \hookrightarrow \mathcal{E}$ (which is necessarily a [[reflective subcategory|reflective inclusion]] making $\nabla \Gamma$ a finite-limit preserving [[idempotent monad]]/[[closure operator]]);

   1. $\nabla$ factors through $Proj(\mathcal{E})$;

1. there exists an object $D \in Proj(\mathcal{E})$ such that

   1. $D$ is $\nabla\Gamma$-[[separated presheaf|separated]] (in that its $(\Gamma \dashv \nabla)$-[[unit of a monad|unit]] is a [[monomorphism]]);

   1. all $\nabla \Gamma$-[closed](closure+operator#InducedClosureOnSlices) [[regular epimorphisms]] have the [[left lifting property]] against $D\to \ast$;

   1. for every [[projective object]] $P$ there is a $\nabla \Gamma$-[closed morphism](closure+operator#InducedClosureOnSlices) $P \to D$.

=--

This is due to ([Frey 14](#Frey14))


## Related concepts

* [[realizability]]

* [[realizability model]]


## References 

* {#Vermeeren09} [[Stijn Vermeeren]], _Realizability Toposes_, 2009 ([pdf](http://stijnvermeeren.be/download/mathematics/essay.pdf))

* Mat&#237;as Menni, Exact completions and toposes. Ph.D. Thesis, University of Edinburgh (2000). ([web](http://www.lfcs.inf.ed.ac.uk/reports/00/ECS-LFCS-00-424/)) 

A characterization of realizability toposes analogous to the [[Giraud axioms]] for [[Grothendieck toposes]] is given in 

* {#Frey14} [[Jonas Frey]], _Characterizing partitioned assemblies and realizability toposes_ ([arXiv:1404.6997](http://arxiv.org/abs/1404.6997))


[[!redirects realizability topos]]
[[!redirects realizability topoi]]
[[!redirects realizability toposes]]
[[!redirects realisability topos]]
[[!redirects realisability topoi]]
[[!redirects realisability toposes]]

[[!redirects Realizability topos]]
[[!redirects Realizability topoi]]
[[!redirects Realizability toposes]]
[[!redirects Realisability topos]]
[[!redirects Realisability topoi]]
[[!redirects Realisability toposes]]

[[!redirects assembly]]
[[!redirects assemblies]]
