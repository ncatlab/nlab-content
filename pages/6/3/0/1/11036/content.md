

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

[[formula|Formulas]] in MLL are built from an alphabet $T$ of propositional variables and two constants $\top$, $\bot$ by applying operations $\otimes$ and $\multimap$. The construction of a formula may be displayed as a binary planar tree. 

We consider two-sided sequents $\Gamma = A_1, \ldots, A_m \vdash \Delta = B_1, \ldots, B_n$, wherein the formulas of $\Gamma$ to the left of the turnstyle are called _negative_ and the formulas of $\Delta$ are called _positive_. Subformulas of these formulas acquire signs according to the following rules: 

* The subformulas $S, T$ of $S \otimes T$ have the same sign as $S \otimes T$. 

* The subformula $T$ of $S \multimap T$ has the same sign as $S \multimap T$, while $S$ has the opposite sign. 

We indicate the sign of a subformula using a superscript, e.g., $S^+$. 

+-- {: .num_defn} 
###### Definition 
A (cut-free) _proof structure_ of type $\Gamma \to \Delta$ is a directed graph whose vertices are subformulas and whose edges are either 

* "KM-links" (Kelly-Mac Lane links) which are of the form $t^- \to t^+$ between two subformula occurrences of the same variable $t \in T$ but with opposite sign (always oriented from a negative occurrence to a positive occurrence); 

* Edges in binary construction trees of the formulas $A_i, B_j$, oriented according to the following rules: 

$$\array{
 & & (S \otimes T)^- & & \qquad S^+ & & & & T^+ \\ 
 & \swarrow & & \searrow & \qquad & \searrow & & \swarrow & \\ 
S^- & & & & T^- \qquad & & (S \otimes T)^+
}$$ 

$$\array{
 & & (S \multimap T)^- & & \qquad S^- & & & & T^+ \\ 
 & \nearrow & & \searrow & \qquad & \nwarrow & & \swarrow & \\ 
S^+ & & & & T^- \qquad & & (S \multimap T)^+
}$$
=-- 

(To be continued) 

## References

* [[Paul-André Melliès]], _Functorial boxes in string diagrams_, Procceding of _Computer Science Logic 2006_ in Szeged, Hungary. 2006 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/functorial-boxes.pdf))
 {#Mellies06}

* Francois Lamarche, _Proof nets for intuitionistic linear logic: Essential nets_ ([pdf](http://hal.inria.fr/docs/00/34/73/36/PDF/prfnet1.pdf))

* [[Paul-André Melliès]], _Categorical semantics of linear logic_ ([pdf](http://profs.sci.univr.it/~bellin/panorama.pdf))

Relation to [[Feynman diagrams]] is discussed in

* {#BlutePanangaden} [[Richard Blute]], [[Prakash Panangaden]], _Proof nets as formal Feynman diagrams_ ([pdf](http://www.indiana.edu/~iulg/qliqc/phi.pdf))


[[!redirects proof nets]]