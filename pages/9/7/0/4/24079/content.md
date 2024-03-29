+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory - contents]]
=--
#### Analysis
+--{: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea ##

Recall ([here](partial+order#AsACategoryWithExtraProperties)) that a [[set]] may be understood as a [[thin category|thin]] [[univalent dagger category|univalent]] (0,1)-dagger category, hence as a thin univalent [[enriched category|dagger-category enriched]] over the [[cartesian monoidal category|cartesian monoidal]] [[proset]] of [[truth values]]. 
In generalization, one may speak of enriching preorders over other [[monoidal posets]].

## Defintion ##

Let $(M, \leq, \otimes, 1)$ be a [[monoidal poset]]. A **$M$-enriched [[symmetric proset]]** or **symmetric proset enriched over/in $M$** is a [[set]] $P$ with a [[binary function]] $o:P \times P \to M$ such that 

* for every $a \in P$, $b \in P$, and $c \in P$, $o(a, b) \otimes o(b, c) \leq o(a, c)$

* for every $a \in P$ and $b \in P$, $o(a, b) \leq o(b, a)$ 

* for every $a \in P$, $1 \leq o(a, a)$

An **$M$-enriched [[set]]** or **set enriched over/in $M$** is an $M$-enriched symmetric proset which additinally satisfies $1 \leq o(a, b) \Rightarrow a = b$. 

For $M$-enriched sets, $o(a, b) = o(b, a)$, $o(a, a) = 1$, and $1 = o(a, b) \Rightarrow a = b$. 

## Examples ##

* An ordinary [[set]] is just an $\Omega$-enriched set, with $\Omega$ the set of [[truth values]]. 

* A [[metric space]] is a $(\mathbb{R}_{\geq 0}, \geq, +, 0)$-enriched set, where $\mathbb{R}_{\geq 0}$ are the [[non-negative number|non-negative]] [[Dedekind real numbers]]. 

* Given any [[Archimedean integral domain]] $A$ and an Archimedean integral subdomain $B \subseteq A$, then $B$ is an $(A_{\geq 0}, \geq, +, 0)$-enriched set, where $A_{\geq 0}$ is the non-negative elements of $A$. 

* A set with an [[apartness relation]] is an $\Omega^\op$-enriched symmetric proset, where the [[co-Heyting algebra]] $\Omega^\op$ is the [[opposite poset]] of the set of [[truth values]] $\Omega$. 

## See also ##

* [[pseudometric space]]
* [[Archimedean integral domain]]
* [[enriched proset]]

[[!redirects enriched set]]
[[!redirects enriched sets]]
[[!redirects enriched symmetric proset]]
[[!redirects enriched symmetric prosets]]