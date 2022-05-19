
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea ##

Recall ([here](partial+order#AsACategoryWithExtraProperties)) that a [[poset]] may be understood as a [[skeleton|skeletal]] [[(0,1)-category]], hence as a skeletal [[enriched category|category enriched]] over the [[cartesian monoidal category|cartesian monoidal]] [[poset]] of [[truth values]]. 
In generalization, one may speak of enriching posets over other [[monoidal posets]].

## Defintion ##

Let $(M, \leq, \wedge, \top)$ be a [[monoidal poset]], such as a [[meet-semilattice]]. A **$M$-enriched [[poset]]** or **poset enriched over/in $M$** is a type $P$ with a [[binary function]] $o:P \times P \to M$ such that 

* for every $a \in P$, $b \in P$, and $c \in P$, $o(a, b) \wedge o(b, c) \leq o(a, c)$

* for every $a \in P$, $\top \leq o(a, a)$. 

## Examples ##

* An ordinary [[poset]] is just an $\Omega$-enriched poset, with $\Omega$ the set of [[truth values]]. 

* A [[Lawvere metric space]] is a $\overline{\mathbb{R}_{\geq 0}}$-enriched poset, where $\overline{\mathbb{R}_{\geq 0}}$ are the [[non-negative number|non-negative]] [[extended real number|extended]] [[Dedekind real numbers]]. 

* A set with an [[irreflexive]] [[comparison]], such as an [[apartness relation]] or a [[linear order]], is an $\Omega^\op$-enriched poset, where the [[co-Heyting algebra]] $\Omega^\op$ is the [[opposite poset]] of the set of [[truth values]] $\Omega$. 

## See also ##

* [[meet-semilattice]]

* [[Lawvere metric space]]
* [[enriched category]] (for the (1, 1)-category version)


[[!redirects enriched posets]]

