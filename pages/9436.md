
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Many algebraic objects have a [[representation theory]] in which they act on other things; for example, [[groups]] often act on sets and [[algebras]] act on [[modules]].
In these situations, the acting object can often be viewed as an example of the type of thing acted upon: a group has an underlying set and an algebra has an underlying module.
The multiplication in the acting object then defines an action of the object on this unstructured copy of itself.
This is called the **regular representation** and is an extremely useful representation to study as it only involves the object itself, whence is in a sense *canonical*, but contains a lot of information, as opposed to, say, the [[trivial representation]] (which is also canonical).


## Definition

The definition is the same in each case, but we shall give the actual definitions for the usual suspects.

+-- {: .num_defn #grpreg}
###### Definition

Let $G$ be a [[group]] with multiplication $\mu$.  Let us write ${|G|}$ for the underlying set of $G$.  The **left regular representation** of $G$ is 

1. as a [[permutation representation]]: the action $G \times {|G|} \to {|G|}$ defined by $g \cdot h = \mu(g,h)$;

1. as a [[linear representation]]: the corresponding representation on the [[linear span]] of $G$.

The **right regular representation** is defined analogously.
=--

+-- {: .num_defn #algreg}
###### Definition
Let $A$ be an [[associative unital algebra]] with multiplication $\mu$.  Let us write ${|A|}$ for the underlying module of $A$.  The **left regular representation** of $A$ is the action $A \otimes {|A|} \to {|A|}$ defined by $a \cdot m = \mu(a,m)$.

The **right regular representation** is defined analogously.
=--

These can be seen as examples of a more general concept.

+-- {: .num_defn #monrep}
###### Definition
Let $(C,\otimes,I)$ be a [[monoidal category]].  Let $M = ({|M|},\mu,\eta)$ be a [[monoid]] in $C$, where ${|M|}$ is the underlying object of $M$ in $C$.
The **regular representation** of $M$ is the action of $M$ on ${|M|}$ induced by the product $\mu$.
=--

## Properties
 {#Properties}

* The regular representation of $G$ as a linear representation is the [[induced representation]] $Ind_{1}^G 1$ of the trivial representation along the inclusion of the trivial [[subgroup]].

\begin{prop}
Over the [[complex numbers]], the regular representation of a [[finite group]] is a [[direct sum]] that contains each [[irreducible representation]] $\rho_i$ with multiplicity its dimension 

$$
  \mathbb{C}[G]
  \;\simeq\;
  \underset{i}{\sum}
  dim_{\mathbb{C}}(\rho_i)
    \cdot
  \rho_i
  \,.
$$
\end{prop}
(e.g. [tom Dieck 09, Thm. (1.10.2)](#tomDieck09) and using [[Schur's lemma]] for the complex case)

## Related concepts

* [[trivial representation]]

* [[alternating representation]]

## References

Lecture notes include

* {#tomDieck09} [[Tammo tom Dieck]], section 1.10 of _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))


[[!redirects regular representation]]
[[!redirects regular representations]]
