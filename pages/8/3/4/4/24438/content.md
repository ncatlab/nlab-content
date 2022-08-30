## Idea 

Some [[symmetric monoidal categories]] have a notion of [[duality]] without being a [[*-autonomous category]]. However, they can be a weak $*$-autonomous category.

## Definition

\begin{definition}
A _weak $*$-autonomous category_  is a [[symmetric monoidal
category|symmetric]] [[closed monoidal category]] $\langle
C,\otimes, I,\multimap\rangle$ with an object
$\bot$ such that the canonical morphism
$$ d_A: A \to (A \multimap \bot) \multimap \bot ,$$
which is the transpose of the [[evaluation map]]
$$ ev_{A,\bot}: (A \multimap \bot) \otimes A \to \bot ,$$
is a [[monomorphism]] for all $A$.  (Here, $\multimap$ denotes the [[internal hom]].)
\end{definition}

A $*$-autonomous category is a weak $*$-autonomous category such that for every object $A$, $d_{A}: A \to (A \multimap \bot) \multimap \bot$ is an isomorphism.

A strictly weak $*$-autonomous category is a weak $*$-autonomous category such that for at least one object $A$, $d_{A}$ is not an isomorphism. Equivalently, a strictly weak $*$-autonomous category is a $*$-autonomous category which is not a $*$-autonomous category.

## Example

* For every [[field]] $\mathbb{K}$, the category $Vec_{\mathbb{K}}$ is a strict weak $*$-autonomous category.
* For every [[commutative ring]] $R$, the category $Mod_{R}$ is a strict weak $*$-autonomous category.

## Related concepts

[[*-autonomous category]]
[[closed monoidal category]]


