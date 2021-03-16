

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Proof nets_ are a graphical way to denote [[proofs]] in [[linear logic]].

They were introduced by [[Jean-Yves Girard|J.-Y. Girard]] in 1987 in order to remove spurious notational redundancies introduced by sequential rule application or indeterminacy of [[cut elimination]] and can be viewed as graphical normal forms of proofs freed from 'the bureaucracy of syntax' (Girard).

Bearing in mind the [[categorical semantics]] of (multiplicative intuitionistic) [[linear logic]] in (closed) [[monoidal categories]], proof nets are closely related to [[Kelly-Mac Lane graphs]] that are used to track compositions of [[extranatural transformations]] definable in such categorical structures. More generally they may be compared to [[string diagrams]] that are evaluated in these categories (with various ways of making the comparison more precise). Proof nets for full linear logic have been thus described by [Melli&#232;s 06](#Mellies06) as string diagrams equipped with "boxes" to account for the [[exponential modality]]. 

With [[linear logic]]/[[linear type theory]] interpreted as [[quantum logic]]/[[quantum computation]], proof nets correspond to [[quantum circuits]] or [[Feynman diagrams]] ([Blute-Panangaden](#BlutePanangaden)).

## Definition 

We begin by describing proof nets for multiplicative linear logic (MLL), which is interpretable in $\ast$-[[star-autonomous category|autonomous]] categories. Similar proof nets may be given for other forms of [[linear type theory]] such as multiplicative intuitionistic linear logic, which is interpretable in [[symmetric monoidal category|symmetric]] [[closed monoidal categories]]. 

### Proof structures 

Before describing proof nets, we start with Girard's notion of _proof structure_. It is simplest to describe the [[cut rule|cut]]-free version, as this is closely connected with the notion of [[Kelly-Mac Lane graph]], or KM-graph for short. We need just a few preliminaries. 

[[formula|Formulas]] in MLL may be built from an alphabet $\mathbf{T}$ of propositional variables and two constants $\mathbf{1}$, $\bot$ by applying operations $\otimes$ and $\multimap$. (Negation may be defined by $\neg A \coloneqq A \multimap \bot$, and the multiplicative disjunction by $A \parr B \coloneqq \neg A \multimap B$. To get formulas in MILL, simply drop $\bot$.) The construction of a formula may be displayed as a binary [[planar tree]]. 

We consider two-sided [[sequents]] $\Gamma = A_1, \ldots, A_m \vdash \Delta = B_1, \ldots, B_n$, wherein the formulas of $\Gamma$ to the left of the turnstyle are called _negative_ and the formulas of $\Delta$ are called _positive_. Subformulas of these formulas acquire signs according to the following rules: 

* The subformulas $S, T$ of $S \otimes T$ have the same sign as $S \otimes T$. 

* The subformula $T$ of $S \multimap T$ has the same sign as $S \multimap T$, while $S$ has the opposite sign. 

We indicate the sign of a subformula using a superscript, e.g., $S^+$. 

+-- {: .num_defn} 
###### Definition 
A (cut-free) _proof structure_ of type $\Gamma \to \Delta$ (in the language of MLL) is a directed graph whose vertices are subformulas of the formulas of $\Gamma, \Delta$, and whose edges are either 

* "KM-links" (Kelly-Mac Lane links) which are of the form $t^- \to t^+$ between two subformula occurrences of the same variable $t \in \mathbf{T}$ but with opposite sign (always oriented from a negative occurrence to a positive occurrence); 

* Edges in binary construction trees of the formulas $A_i, B_j$, oriented according to the following rules: 

$$\array{
 & & (S \otimes T)^- & & \qquad S^+ & & & & T^+ & & & & (S \multimap T)^- & & \qquad S^- & & & & T^+ \\ 
 & \swarrow & & \searrow & \qquad & \searrow & & \swarrow & & & & \nearrow & & \searrow & \qquad & \nwarrow & & \swarrow & \\ 
S^- & & & & T^- \qquad & & (S \otimes T)^+ & & & S^+ & & & & & T^- \qquad & & (S \multimap T)^+
}$$ 
=-- 

For a proof structure of type $\Gamma \to \Delta$, it is clear that the only information not determined from $\Gamma$ and $\Delta$ are the KM-links. These KM-links give a KM-graph. 

MLL formulas $A$ and proof structures of type $A \to B$ form a category $Struct[\mathbf{T}]$. Composition of proof structures is given by composing the underlying KM-graphs; identity proof structures are given by identity KM-graphs. 

In fact this category of proof structures is a $\ast$-autonomous category. As objects are MLL formulas, it is clear how $\otimes$ and $\multimap$ are defined on objects. 

### Proof nets 

Proof nets are those proof structures that arise by taking the KM-graphs of morphisms that are definable in the language of $\ast$-autonomous categories. Or, in the language of Girard, proof nets are those proof structures which are "correct" or "valid" (i.e., derivable from a sequent deduction, in a sense explained below). 

More exactly, let $F[\mathbf{T}]$ be the free $\ast$-autonomous category on $\mathbf{T}$ (as discrete category), viewing $\ast$-autonomous categories and functors that preserve $\ast$-autonomous structure _strictly_ as a 1-category that is 1-monadic over $Cat$, the category of small categories and functors. Observe that the objects of $F[\mathbf{T}]$ may be identified with MLL formulas. We view the morphisms of $F[\mathbf{T}]$ as representing morphisms that are definable (starting with the datum $\mathbf{T}$). 

As $Struct[\mathbf{T}]$ is $\ast$-autonomous, the obvious inclusion $\mathbf{T} \hookrightarrow Struct[\mathbf{T}]$ induces a unique strict $\ast$-autonomous functor $S: F[\mathbf{T}] \to Struct[\mathbf{T}]$, which may be called the _graphical semantics_ functor. 

+-- {: .num_defn} 
###### Definition 
A **proof net** (in the language of MLL) of type $A \to B$ is a proof structure $\pi$ of the form $S(f)$, the graphical semantics of some arrow $f: A \to B$ in $F[\mathbf{T}]$. 
=-- 

The following theorem for MLL proof nets, proved by Richard Blute in his thesis, is similar in content to the [[coherence theorem]] for [[symmetric monoidal category|symmetric]] [[closed monoidal categories]] proved by Kelly-Mac Lane. 

+-- {: .num_theorem} 
###### Theorem 
The restriction of $S: F[\mathbf{T}] \to Struct[\mathbf{T}]$ to the full subcategory consisting of objects isomorphic to formulas with no subformula occurrences of $\mathbf{1}$ or $\bot$ is faithful. 
=-- 

For a cedent of formulas $\Gamma = A_1, \ldots, A_n$, let $\bigotimes \Gamma$ be the formula $A_1 \otimes \ldots \otimes A_n$ (associated to the left, say, if one is to be persnickety), and let $\parr \Gamma$ be the formula $A_1 \parr \ldots \parr A_n$. Each proof structure $\pi: \Gamma \to \Delta$ determines (and is determined by) a unique proof structure ${|\pi|}: \bigotimes \Gamma \to \parr \Delta$ with the same underlying KM-graph as $\pi$. 

Then, more generally we may define a proof net of type $\Gamma \to \Delta$ to be a proof structure $\pi: \Gamma \to \Delta$ such that ${|\pi|}$ is a proof net according to the definition above. 

Alternatively, we may define proof nets by reference to MLL sequent calculus, as follows. 

### Nets of sequent deductions {#NetDeductions} 

To each deduction or derivation tree in MLL sequent calculus, one may give an associated proof net. This is by induction; one considers the last step of a deduction $\delta$ whose premises have given derivations $\delta_i: \Gamma_i \to \Delta_i$, which have been given assigned proof nets $N(\delta_i)$, and uses this to assign a net to the full deduction $\delta$. 

We recall the rules for MLL over a list of variable types $\mathbf{T}$, and associated rules for forming nets. As remarked above, for a deduction $\delta$ of a given sequent $\Gamma \to \Delta$, the net $N(\delta)$ is determined up to its KM-links, and so we will give just the rules for computing the KM-graph.

The rules for forming KM-graphs will sound pretty repetitive! But don't worry; that just means they're really easy. In summary, all we do for each rule besides the axioms is take the disjoint union of the KM-graphs occurring for the (derivations of the) premises, to get the KM-graph of the conclusion. 

+-- {: .num_remark} 
###### Remark 
By the _[[cut rule|Hauptsatz]]_, i.e., cut-elimination theorem, we omit consideration of the cut rule. It is however interesting to consider the meaning of the cut-elimination algorithm in terms of proof nets; someone who is sufficiently savvy with graphics may wish to include material here. 
=-- 

1. Axiom 
$$\frac{}{\displaystyle t \vdash t}\; id,$$ 
where $t \in \mathbf{T}$. Here the net of the conclusion consists of the KM-graph $t^- \to t^+$. 

1. Structural rule 
$$\frac{\displaystyle \delta': \Gamma, A, B, \Delta \vdash \Sigma}{\displaystyle \Gamma, B, A, \Delta \vdash \Sigma}\; exchange$$ 
Here there is an identification between the sets of subformula occurrences for the premise and conclusion, and under this identification the proof net for $\delta$ is the same as the proof net for $\delta'$. 

1. Unit rules (logical rules for units). There are four of these: 
$$\frac{}{\displaystyle \; \vdash \mathbf{1}}\; \mathbf{1}_+$$ 
For $\mathbf{1}_+$, the KM-graph of the conclusion is empty.  
$$\frac{}{\displaystyle \bot \vdash \; }\; \bot_{-}$$ 
For $\bot_{-}$, the KM-graph of the conclusion is empty. 
$$\frac{\displaystyle \delta': \Gamma, \Delta \vdash \Sigma}{\displaystyle \Gamma, \mathbf{1}, \Delta \vdash \Sigma}\; \mathbf{1}_{-}$$ 
For $\mathbf{1}_{-}$, there is an identification between the variable subformula occurrences in the premise and in the conclusion. Under this identification, the KM-graph for $\delta$ is the same as for $\delta'$. 
$$\frac{\displaystyle \delta': \Gamma \vdash \Delta, \Sigma}{\displaystyle \Gamma \vdash \Delta, \bot, \Sigma}\; \bot_+$$ 
For $\bot_+$, there is an identification between the variable subformula occurrences in the premise and in the conclusion. Under this identification, the KM-graph for $\delta$ is the same as for $\delta'$. 

1. Logical rules for $\otimes$ and $\multimap$. There are four of these. 
$$\frac{\displaystyle \delta': \Gamma, A, B, \Delta \vdash \Sigma}{\displaystyle \Gamma, A \otimes B, \Delta \vdash \Sigma}\; \otimes_{-}$$ 
For $\otimes_{-}$, there is an identification between the variable subformula occurrences in the premise and in the conclusion. Under this identification, the KM-graph for $\delta$ is the same as for $\delta'$. 
$$\frac{\displaystyle \delta': \Gamma, A \vdash B, \Delta}{\displaystyle \Gamma \vdash A \multimap B, \Delta}\; \multimap_+$$ 
For $\multimap_+$, there is an identification between the variable subformula occurrences in the premise and in the conclusion. Under this identification, the KM-graph for $\delta$ is the same as for $\delta'$. 
$$\frac{\displaystyle \delta_1: \Gamma \vdash \Delta, A \qquad \delta_2: \Sigma \vdash B, \Omega}{\Gamma, \Sigma \vdash \Delta, A \otimes B, \Omega}\; \otimes_+$$ 
In the case $\otimes_+$, the set of variable subformula occurrences in the conclusion is identified with the disjoint union of those for the premises, and under this identification the KM-graph of $\delta$ is the disjoint union of the KM-graphs for $\delta_1$ and $\delta_2$. 
$$\frac{\displaystyle \delta_1: \Sigma, B \vdash \Omega \qquad \delta_2: \Gamma \vdash A, \Delta \qquad }{\Sigma, A \multimap B, \Gamma \vdash \Omega, \Delta}\; \multimap_{-}$$ 
In the case $\multimap_{-}$, the set of variable subformula occurrences in the conclusion is identified with the disjoint union of those for the premises, and under this ientification the KM-graph of $\delta$ is the disjoint union of the KM-graphs for $\delta_1$ and $\delta_2$. 



## Graphical criterion for validity 

In his original Linear Logic paper, Girard gave an interesting purely graphical criterion for a proof structure to be a proof net (i.e., "valid"), based on his so-called "cyclic trips" and "longtrip criterion". Later this criterion was simplified and improved by Danos and Regnier, who at the same time showed that validity of a proof structure could be decided in polynomial time. We give this criterion below. (**N.B.** this criterion as given by them works for proof structures of type $A \to B$ where there are no subformula occurrences of $\mathbf{1}$ and $\bot$. It may be extended to work for all formulas if we use a more refined notion of proof structure, called a unit-extended proof structure, as described below.) 

+-- {: .num_defn} 
###### Definition 
A **par switch** (a $\parr$-switch) in a proof structure is a subgraph of one of the two forms 

$$\array{
 & & (S \otimes T)^- & & & & S^- & & & & T^+ \\ 
 & \swarrow & & \searrow & & & & \nwarrow & & \swarrow \\ 
S^- & & & & T^- & & & & (S \multimap T)^+ & & 
}$$ 

where $(S \otimes T)^-$ or $(S \multimap T)^+$ is a subformula node of the proof structure. (A $\otimes$ switch in a proof structure is similarly a subgraph consisting of a subformula node $(S \otimes T)^+$ or $(S \multimap T)^-$ and its two children in the binary construction tree, and the edges connecting them.) 

A **network** of a proof structure $\pi$ is obtained by removing exactly one of the two edges from each par switch of $\pi$. 
=-- 

+-- {: .num_theorem} 
###### Theorem 
**(Girard, Danos-Regnier)** 
A proof structure $\pi$ is a proof net if every network of $\pi$ is a connected acyclic graph (considered as an unoriented graph, forgetting edge orientations). 
=-- 

+-- {: .num_remark} 
###### Remark 
The proof is quite technical, but it is of fundamental importance in the analysis of proof nets. The method is to "sequentialize" a proof structure that satisfies this graphical criterion (i.e., provide a sequent deduction for it). This is by an inductive procedure which first removes consideration of outer par switches (replacing a proof structure of type $\Gamma, A \otimes B, \Delta \to \Sigma$ by an 'equivalent' structure of type $\Gamma, A, B, \Delta \to \Sigma$, and similarly a proof structure of type $\Gamma \to A \multimap B, \Delta$ by an equivalent one of type $\Gamma, A \to B, \Delta$). Once these have been removed, the hard part is to show there exists an outer $\otimes$ switch with parent $(A \otimes B)^+$ or $(A \multimap B)^-$, such that removal of the parent and edges to its children splits the graph cleanly into two connected components, each of which then satisfies the graphical criterion. The proof of existence is by a tricky combinatorial analysis on graphs. Once this is done, each of the two graph components is sequentializable by the inductive hypothesis, and the induction can then be pushed through. 
=-- 

+-- {: .num_remark} 
###### Remark 
[[François Métayer]] ([1994](#Metayer94)) showed that the Danos-Regnier criterion on a proof structure's 'convergence to a proofnet' can equivalently be expressed as a criterion on the [[homology]] of a suitable associated graph.
=--

The Danos-Regnier criterion, stated according to the definition above, might appear exponential in complexity since it appears to involve checking that every one of the $2^p$ networks, where $p$ is the number of par switches, is connected and acyclic. However, Danos and Regnier gave a beautiful simplification which in fact gives an algorithm for deciding validity of a proof structure in polynomial time. (More recently, the problem has actually been shown to be complete for non-deterministic log space [JdNM08](#JdNM08).)

+-- {: .num_remark #DR} 
###### Description 
Informally, what one does is draw an arc between the two edges of each par switch (in the manner of secondary school geometry, when one wishes to indicate an angle between two lines), and then applies a series of graph reductions: 

* At each step in the series, any un-arced edge between two distinct nodes may be contracted to a single node; 

* At each step of the series, any configuration consisting of two distinct nodes and a pair of arced edges between them may be contracted to a point, 

* A graph consisting of a single node and no edges reduces to itself. 
=-- 

+-- {: .num_prop} 
###### Proposition 
**(Danos-Regnier)** 
A proof structure is a proof net if and only if any series of graph reductions eventually reduces it to a graph with a single node and no edges. 
=-- 

## Unit-extended proof nets 

In his thesis, Trimble introduced a refinement of proof structures, designed to take the units $\mathbf{1}$ and $\bot$, particularly their actions and co-actions on other objects, more explicitly into account. 

+-- {: .num_defn} 
###### Definition 
A **unit-extended proof structure** of type $\Gamma \to \Delta$ is a proof structure $\pi: \Gamma \to \Delta$ together with a function from the set of subformula occurrences of $\mathbf{1}^-$ to the set of subformulas, and a function from the set of subformula occurrences of $\bot^+$ to the set of subformulas. 
=-- 

Unit-extended proof structures are considered as graphs, by adjoining to $\pi$ an edge $\mathbf{1}^- \to S$ for each subformula occurrence $\mathbf{1}^-$ that maps to $S$ under the first function, and another edge $T \to \bot^+$ for each subformula occurrence $\bot^+$ that maps to $T$ under the second function. This means for instance that for the sequent $\mathbf{1} \vdash \bot$, there is just one unit-extended proof structure of type $\mathbf{1} \to \bot$, and it consists of a _pair_ of edges from $\mathbf{1}^-$ to $\bot^+$. 

To each MLL sequent deduction, one can associate a unit-extended proof structure, or rather a set of proof structures. 

* For the axioms $t \vdash t$, the associated unit-extended proof structure is of course the KM-graph $t^- \to t^+$. 

* For each of the rules $exchange$, $\mathbf{1}_+$, $\bot_{-}$, $\otimes_{-}$, $\otimes_+$, $\multimap_{-}$, $\multimap_+$, if unit-extended proof structures $\gamma_i$ (i.e., sets of unit edges and KM-links) have been associated to derivations of the premises, then associated to the final deduction (obtained by applying that rule) is the proof structure obtained by taking the disjoint union of the $\gamma_i$. 

* This leaves the two unit rules $\mathbf{1}_{-}$, $\bot_+$. For the rule 
$$\frac{\displaystyle \delta': \Gamma, \Delta \vdash \Sigma}{\displaystyle \Gamma, \mathbf{1}, \Delta \vdash \Sigma}\; \mathbf{1}_{-},$$ 
if $\gamma'$ is a unit-extended proof structure for $\delta'$, then associated to the final deduction $\delta$ is any unit-extended proof structure obtained by adjoining to $\gamma'$ a unit edge from the occurrence of $\mathbf{1}^-$ introduced in the conclusion, to any subformula node occurring in $\gamma': \Gamma, \Delta \to \Sigma$. 
Similarly, for the rule 
$$\frac{\displaystyle \delta': \Gamma \vdash \Delta, \Sigma}{\displaystyle \Gamma \vdash \Delta, \bot, \Sigma}\; \bot_+,$$ 
if $\gamma'$ is a unit-extended proof structure for $\delta'$, then associated to the final deduction $\delta$ is any unit-extended proof structure obtained by adjoining to $\gamma'$ a unit edge going to the occurrence of $\bot_+$ introduced in the conclusion, from any subformula node occurring in $\gamma': \Gamma, \Delta \to \Sigma$. 

+-- {: .num_defn} 
###### Definition 
A **unit-extended proof net** is a unit-extended proof structure that is associated with some MLL sequent deduction. 
=-- 

The notion of network for unit-extended proof structures is the same as for ordinary proof structures: a network is obtained by removing just one edge from each par-switch. The Danos-Regnier criterion for validity goes through without modification: 

+-- {: .num_theorem} 
###### Theorem 
A unit-extended proof structure is a unit-extended proof net if and only if each of its networks is an acyclic connected graph (ignoring edge orientations). 
=-- 

The simplified algorithm for deciding validity, in terms of a series of [graph reductions](#DR), also goes through for unit-extended proof structures without any modification. 

## Comparison to string diagrams 

There are various possibilities for translating the language of proof nets into a language of [[string diagrams]]. Some of these possibilities are subject to a debate on how liberally one would like to understand "string diagrams", but the idea that both proof nets and string diagrams open possibilities for rapid-fire graphical calculations in similar-looking ways should be taken seriously. 

(I'll come back to this. I want to think some more on how I want to say it.) 

## References

Proofnets originated with Girard's seminal paper introducing linear logic: 

* {#Girard87} [[Jean-Yves Girard]] , _Linear Logic_ , Theor. Comp. Sci. **50** (1987) pp. 1-102. ([draft](http://iml.univ-mrs.fr/~girard/Synsem.pdf.gz))

* {#Trimble94} [[Todd Trimble]], _Linear Logic, Bimodules, and Full Coherence for Autonomous Categories_, Rutgers 1994

* {#BCST96} [[Richard Blute]], [[J.R.B. Cockett]], [[R. A. G. Seely]], [[Todd Trimble]], _Natural deduction and coherence for weakly distributive categories_, JPAA 113 (1996), 229-296. ([web](http://www.sciencedirect.com/science/article/pii/002240499500159X))

* {#JdNM08} Paulin Jacob&#233; de Naurois and Virgile Mogbil, _Correctness of Linear Logic Proof Structures is NL-Complete_ ([pdf](https://hal.archives-ouvertes.fr/hal-00360894/document))

* Fran&#231;ois Lamarche, _Proof nets for intuitionistic linear logic: Essential nets_ ([pdf](http://hal.inria.fr/docs/00/34/73/36/PDF/prfnet1.pdf))

* [[Paul-André Melliès]], _A topological correctness criterion for non-commutative logic_ , London Mathematical Society Lecture Notes Series 316, 2004. ([pdf](https://hal.inria.fr/hal-00154204/document))
 
* {#Mellies06} [[Paul-André Melliès]], _Functorial boxes in string diagrams_, Proceedings of _Computer Science Logic 2006_ in Szeged, Hungary. 2006 ([pdf](https://www.irif.fr/~mellies/papers/Mellies06csl.pdf))

* [[Paul-André Melliès]], _Categorical semantics of linear logic_ ([pdf](http://profs.sci.univr.it/~bellin/panorama.pdf))

* {#Metayer94} [[François Métayer]], _Homology of proofnets_ ,Arch. Math. Logic **33** (1994) pp.169-188. ([draft](http://www.pps.univ-paris-diderot.fr/~metayer/PDF/hpn.pdf))

* Dominic J. D. Hughes, *Unification nets: canonical proof net quantifiers* [arxiv](https://arxiv.org/abs/1802.03224)

Relation to [[Feynman diagrams]] is discussed in

* {#BlutePanangaden} [[Richard Blute]], [[Prakash Panangaden]], _Proof nets as formal Feynman diagrams_ ([pdf](http://www.indiana.edu/~iulg/qliqc/phi.pdf))


[[!redirects proof nets]]