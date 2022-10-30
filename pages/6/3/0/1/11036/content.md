

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

Bearing in mind the [[categorical semantics]] of (multiplicative intuitionistic) [[linear logic]] in [[monoidal categories]], proof nets are closely related to [[Kelly-Mac Lane graphs]] that are used to track compositions of extranatural transformations definable in such categorical structures. More generally they may be compared to [[string diagrams]] that are evaluated in these categories. 
Proof nets for full linear logic have been thus described by [Melli&#232;s 06](#Mellies06) as string diagrams equipped with "boxes" to account for the [[exponential modality]]. 

With [[linear logic]]/[[linear type theory]] interpreted as [[quantum logic]]/[[quantum computation]], proof nets correspond to [[quantum circuits]] or [[Feynman diagrams]] ([Blute Panangaden](#BlutePanangaden)).

## Definition 

We begin by describing proof nets for multiplicative linear logic (MLL), which is interpretable in $\ast$-[[star-autonomous category|autonomous]] categories. Similar proof nets may be given for other forms of [[linear type theory]] such as multiplicative intuitionistic linear logic, which is interpretable in [[symmetric monoidal category|symmetric]] [[closed monoidal categories]]. 

### Proof structures 

Before describing proof nets, we start with Girard's notion of _proof structure_. It is simplest to describe the cut-free version, as this is closely connected with the notion of [[Kelly-Mac Lane graph]], or KM-graph for short. We need just a few preliminaries. 

[[formula|Formulas]] in MLL may be built from an alphabet $\mathbf{T}$ of propositional variables and two constants $\mathbf{1}$, $\bot$ by applying operations $\otimes$ and $\multimap$. The construction of a formula may be displayed as a binary planar tree. 

We consider two-sided sequents $\Gamma = A_1, \ldots, A_m \vdash \Delta = B_1, \ldots, B_n$, wherein the formulas of $\Gamma$ to the left of the turnstyle are called _negative_ and the formulas of $\Delta$ are called _positive_. Subformulas of these formulas acquire signs according to the following rules: 

* The subformulas $S, T$ of $S \otimes T$ have the same sign as $S \otimes T$. 

* The subformula $T$ of $S \multimap T$ has the same sign as $S \multimap T$, while $S$ has the opposite sign. 

We indicate the sign of a subformula using a superscript, e.g., $S^+$. 

+-- {: .num_defn} 
###### Definition 
A (cut-free) _proof structure_ of type $\Gamma \to \Delta$ (in the language of MLL) is a directed graph whose vertices are subformulas of the formulas of $\Gamma, \Delta$, and whose edges are either 

* "KM-links" (Kelly-Mac Lane links) which are of the form $t^- \to t^+$ between two subformula occurrences of the same variable $t \in \mathbf{T}$ but with opposite sign (always oriented from a negative occurrence to a positive occurrence); 

* Edges in binary construction trees of the formulas $A_i, B_j$, oriented according to the following rules: 

$$\array{
 & & (S \otimes T)^- & & \qquad S^+ & & & & T^+ \qquad & & (S \multimap T)^- & & \qquad S^- & & & & T^+ \\ 
 & \swarrow & & \searrow & \qquad & \searrow & & \swarrow & \qquad  & \nearrow & & \searrow & \qquad & \nwarrow & & \swarrow & \\ 
S^- & & & & T^- \qquad & & (S \otimes T)^+ \qquad S^+ & & & & T^- \qquad & & (S \multimap T)^+
}$$ 
=-- 

For a proof structure of type $\Gamma \to \Delta$, it is clear that the only information not determined from $\Gamma$ and $\Delta$ are the KM-links. These KM-links give a KM-graph. 

MLL formulas $A$ and proof structures of type $A \to B$ form a category $Struct[\mathbf{T}]$. Composition of proof structures is given by composing the underlying KM-graphs; identity proof structures are given by identity KM-graphs. 

In fact this category of proof structures is a $\ast$-autonomous category. As objects are MLL formulas, it is clear how $\otimes$ and $\multimap$ are defined on objects. (To be continued.) 

### Proof nets 

Proof nets are those proof structures that arise by taking the KM-graphs of morphisms that are definable in the language of $\ast$-autonomous categories. 

More exactly, let $F[\mathbf{T}]$ be the free $\ast$-autonomous category on $\mathbf{T}$ (as discrete category), viewing $\ast$-autonomous categories and functors that preserve $\ast$-autonomous category _strictly_ as a 1-category that is 1-monadic over $Cat$, the category of small categories and functors. Observe that the objects of $F[\mathbf{T}]$ may be identified with MLL formulas. We view the morphisms of $F[\mathbf{T}]$ as representing morphisms that are definable (starting with the datum $\mathbf{T}$). 

As $Struct[\mathbf{T}]$ is $\ast$-autonomous, the obvious inclusion $\mathbf{T} \hookrightarrow Struct[\mathbf{T}]$ induces a unique strict $\ast$-autonomous functor $S: F[\mathbf{T}] \to Struct[\mathbf{T}]$. 

+-- {: .num_defn} 
###### Definition 
A **proof net** (in the language of MLL) of type $A \to B$ is a proof structure $\pi$ of that type that is of the form $S(f)$, for some arrow $f: A \to B$ in $F[\mathbf{T}]$. 
=-- 

(To be continued.) 


## References

* [[Paul-André Melliès]], _Functorial boxes in string diagrams_, Procceding of _Computer Science Logic 2006_ in Szeged, Hungary. 2006 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/functorial-boxes.pdf))
 {#Mellies06}

* Francois Lamarche, _Proof nets for intuitionistic linear logic: Essential nets_ ([pdf](http://hal.inria.fr/docs/00/34/73/36/PDF/prfnet1.pdf))

* [[Paul-André Melliès]], _Categorical semantics of linear logic_ ([pdf](http://profs.sci.univr.it/~bellin/panorama.pdf))

Relation to [[Feynman diagrams]] is discussed in

* {#BlutePanangaden} [[Richard Blute]], [[Prakash Panangaden]], _Proof nets as formal Feynman diagrams_ ([pdf](http://www.indiana.edu/~iulg/qliqc/phi.pdf))


[[!redirects proof nets]]