
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _[[Lie algebra]]_ may be formulated [[internalization|internal to]] general [[linear category|linear]] [[monoidal categories]] ([[tensor categories]]). This general definition of _Lie algebra objects internal to tensor categories_ subsumes variants of Lie algebras such as [[super Lie algebras]]. 

## Definition

Consider a [[commutative unital ring]] $k$, and a (strict for simplicity) [[symmetric monoidal category|symmetric monoidal]] $k$-[[linear category]] $(\mathcal{C},\otimes,1)$ with [[braiding]] $\tau$.

A **[[Lie algebra object]]** in $(\mathcal{C},\otimes,1,\tau)$ is 

1. an [[object]] 

   $$
     L \in \mathcal{C}
   $$

1. [[morphism]] (the [[Lie bracket]])

   $$
     [-,-] \;\colon\; L \otimes L \to L
   $$

such that the following conditions hold:

1. [[Jacobi identity]]:

   $$
     \left[-,\left[-,-\right]\right]
       +
     \left[-,\left[-,-\right]\right]
     \circ(id_L\otimes\tau_{L,L})
     \circ(\tau\otimes id_L)
     +
     \left[-,\left[-,-\right]\right]
       \circ 
     (\tau_{L,L}\otimes id_L)\circ (id_L\otimes\tau_{L,L}) = 0
   $$ 

1. skew-symmetry:

   $$
     \begin{aligned}
       & 
       \phantom{+}
       [-,-]
       \\
       &
       +
       [-,-]\circ \tau_{L,L} 
       \\
       & = \phantom{+} 0
     \end{aligned}
   $$

Equivalently, Lie algebra objects  are the [[algebras over an operad]] over a certain quadratic [[operad]], called the [[Lie operad]], which is the [[Koszul dual]] of the [[commutative algebra operad]].

## Examples

Examples of types of [[Lie algebra objects]]:

If $k$ is the ring $\mathbb{Z}$ of [[integers]] and $\mathcal{C} = $ $k$[[Mod]] = [[Ab]] is the [[category]] of [[abelian groups]] equipped with the [[tensor product of abelian groups]], then a Lie algebra object is called a _[[Lie ring]]_.

If $k$ is a [[field]] and $\mathcal{C} =$ [[Vect]] is the [[category]] of [[vector spaces]] over $k$ equipped with the [[tensor product of vector spaces]] then a Lie algebra object is an ordinary_[[Lie algebra|Lie k-algebra]]_. 

If $k$ is a [[field]] and $\mathcal{C}$ = [[sVect]] is the [[category]] of [[super vector spaces]] over $k$, then a Lie algebra object is a  _[[super Lie algebra]]_.

## Related concepts

* [[Lie algebra weight system]]


[[!redirects Lie algebra objects]]

[[!redirects internal Lie algebra]]
[[!redirects internal Lie algebras]]

[[!redirects Lie ring]]
[[!redirects Lie rings]]

