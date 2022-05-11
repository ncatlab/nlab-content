+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Group theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A $\mathbb{Z}$-[[Weyl algebra]].

## Definition 

### Finitely generated Weyl rings

Given an [[abelian group]] $G$, the **$n$-th Weyl ring** is a [[ring]] $A_n(G)$ with 

* an abelian group [[homomorphism]] $g:G \to A_n(G)$ 

* a function $x:[1, n] \to A_n(G)$

* a function $\partial:[1, n] \to A_n(G)$

such that 

* for every number $i, j \in [1,n]$, $x(i) \cdot x(j) = x(j) \cdot x(i)$ 

* for every number $i, j \in [1,n]$, $\partial(i) \cdot \partial(j) = \partial(j) \cdot \partial(i)$

* for every number $i \in [1,n]$, $\partial(i) \cdot x(i) - x(i) \cdot \partial(i) = 1$

* for every number $i, j \in [1,n]$, $i \neq j$ implies $\partial(i) \cdot x(j) - x(j) \cdot \partial(i) = 0$

* for every other ring $R$ with abelian group homomorphism $h:G \to R$ with 

  * a function $x:[1, n] \to R$

  * a function $\partial:[1, n] \to R$

where 

  * for every number $i, j \in [1,n]$, $x(i) \cdot x(j) = x(j) \cdot x(i)$ 

  * for every number $i, j \in [1,n]$, $\partial(i) \cdot \partial(j) = \partial(j) \cdot \partial(i)$

  * for every number $i \in [1,n]$, $\partial(i) \cdot x(i) - x(i) \cdot \partial(i) = 1$

  * for every number $i, j \in [1,n]$, $i \neq j$ implies $\partial(i) \cdot x(j) - x(j) \cdot \partial(i) = 0$

there is a unique ring homomorphism $i:A_n(G) \to R$ such that $i \circ g = h$. 

### General Weyl rings

Given an [[abelian group]] $G$ and a set $S$ with [[stable equality]], the **$S$-generated Weyl ring** is a [[ring]] $A(S,G)$ with 

* an abelian group [[homomorphism]] $g:G \to A(S,G)$ 

* a function $x:S \to A(S,G)$

* a function $\partial:S \to A(S,G)$

such that 

* for every number $i, j \in S$, $x(i) \cdot x(j) = x(j) \cdot x(i)$ 

* for every number $i, j \in S$, $\partial(i) \cdot \partial(j) = \partial(j) \cdot \partial(i)$

* for every number $i \in S$, $\partial(i) \cdot x(i) - x(i) \cdot \partial(i) = 1$

* for every number $i, j \in S$, $i \neq j$ implies $\partial(i) \cdot x(j) - x(j) \cdot \partial(i) = 0$

* for every other ring $R$ with abelian group homomorphism $h:G \to R$ with 

  * a function $x:S \to R$

  * a function $\partial:S \to R$

where 

  * for every number $i, j \in S$, $x(i) \cdot x(j) = x(j) \cdot x(i)$ 

  * for every number $i, j \in S$, $\partial(i) \cdot \partial(j) = \partial(j) \cdot \partial(i)$

  * for every number $i \in S$, $\partial(i) \cdot x(i) - x(i) \cdot \partial(i) = 1$

  * for every number $i, j \in S$, $i \neq j$ implies $\partial(i) \cdot x(j) - x(j) \cdot \partial(i) = 0$

there is a unique ring homomorphism $i:A(S,G) \to R$ such that $i \circ g = h$. 

## See also

* [[ring]]

* [[tensor ring]]

* [[symmetric ring]]

* [[exterior ring]]

* [[Clifford ring]]

* [[Weyl algebra]]

[[!redirects Weyl rings]]