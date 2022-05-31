
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

## Idea

The [[enriched category theory|enriched]] generalization of the notion of *[[monotone function]]*.

## Definition

Given two preorders $A, B$ [[enriched preorder|enriched in]] a [[monoidal poset]] $M$, an **$M$-enriched monotone** is a function $f: A \to B$ such that  
$$o_A(x, y) \leq o_B(f(x), f(y))$$ 
for all $x \in A$ and $y \in A$. 

## Examples

* Let $M$ be $\Omega$, the set of [[truth values]], so that $A$ and $B$ are [[preorders]]. The $\Omega$-enriched monotones between $A$ and $B$ are monotones between $A$ and $B$.

* Let $M$ be $(\mathbb{R}_{\geq 0}, \geq, +, 0)$, the [[non-negative number|non-negative]] [[Dedekind real numbers]] with the preorder relation being greater than $\geq$, the monoidal operation being addition $+$, and the monoidal unit being zero $0$, so that $A$ and $B$ are [[quasipseudometric spaces]]. The $\mathbb{R}_{\geq 0}$-enriched monotones between $A$ and $B$ are distance-decreasing maps between $A$ and $B$.

## See also

* [[enriched preorder]]

* [[enriched monotone preorder]]

* [[quasipseudometric space]]

[[!redirects enriched monotones]]