
> The term *Hilbert module* is an abbreviation both for a Hilbert C\*-module (discussed here) and the analogous notion of *[[Hilbert Q-modules]]* (see there), where $Q$ is a [[quantale]] (or a [[locale]], in particular).


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--


# Hilbert modules
* table of contents
{: toc}


## Idea

The notion of _Hilbert C\*-module_ (or simply _Hilbert module_) is a generalization of the notion of _[[Hilbert space]]_ where the algebra of [[complex numbers]] is replaced by a possibly more general [[C*-algebra]] $A$. In particular a Hilbert $A$-module has an [[inner product]] which takes values not in $\mathbb{C}$, but in $A$, and such that [[complex conjugation]] is replaced by the [[star-algebra|star-operation]] in $A$.

Hilbert C\*-modules naturally appear as modules over [[groupoid convolution algebras]]. Refined to [[Hilbert C*-bimodules]] they serve as generalized [[homomorphism]] between [[C*-algebras]] in [[noncommutative topology]], and, when further equipped with a left weak [[Fredholm module]] as [[cocycles]] in [[KK-theory]].

## Definition
 {#Definition}

+-- {: .num_defn #HilbertCStarModule}
###### Definition

For $B \in $ [[C*Alg]], a [[Hilbert C*-module]] over $B$ is 

1. a [[complex numbers|complex]] [[vector space]] $H$;

1. equipped with an [[action]] of $B$ from the right;

1. equipped with a [[sesquilinear map]] (linear in the second argument)

   $$
     \langle -,-\rangle \,\colon\, H \times H \to B
   $$

   (the $B$-valued [[inner product]])

such that 

1. $\langle -,-\rangle$ behaves like a positive definite [[Hermitian form|Hermitian]] [[inner product]] over $B$ in that for all $x,y \in H$ and $b \in B$ we have

   1. $\langle x,y\rangle^\ast = \langle y,x\rangle$

   1. $\langle x,x\rangle \geq 0$ (in the sense of [[positive elements]] in $B$)

   1. $\langle x,x\rangle = 0$ precisely if $x = 0$;

   1. $\langle x,y \cdot b\rangle = \langle x,y \rangle \cdot b $

1. $H$ is [[complete space|complete]] with respect to the [[norm]]

   ${\Vert x \Vert_H} \coloneqq {\Vert \langle x,x\rangle\Vert_B}^{1/2}$.

=--

+-- {: .num_remark}
###### Remark

In addition to the explicit $B$-linearity in the second argument under right multiplicatojn

$$
  \langle v, w \cdot b\rangle = \langle v,w\rangle \cdot b
$$

the axioms imply conjugate $B$-linearity in the first argument and under left multiplication

$$
  \langle v \cdot b,w\rangle = b^\ast \cdot \langle v,w\rangle
  \,.
$$

Because:

$$  
  \begin{aligned}
    \langle v \cdot b,w\rangle
    & =
    \langle w,  v\cdot b\rangle^\ast
    \\
    & = \left( \left\langle w,v\right\rangle \cdot b\right)^\ast
    \\
    & = b^\ast \cdot \langle w,v\rangle^\ast
    \\
    & = b^\ast \cdot \langle v,w\rangle
  \end{aligned}
  \,.
$$
=--



## Examples
 {#Examples}

First of all we have:

+-- {: .num_example }
###### Example

An ordinary complex [[Hilbert space]] is a Hilbert $\mathbb{C}$-module.

=--

The archetypical class of examples of Hilbert C\*-modules for [[commutative C*-algebras]] is the following. The general definition \ref{HilbertCStarModule} may be understood as the generalization of the structure of this example to [[noncommutative topology|non-commutative C*-algebras]]. See also remark \ref{TheTrivialHilbertBundleAndL2} below.

+-- {: .num_example #FromAHilbertSpaceBundle}
###### Example

Let $X$ be a [[locally compact topological space]] and write $C_0(X)$ for its [[C*-algebra]] of [[continuous functions]] [[vanishing at infinity]].

Let $E \to X$ be a [[fiber bundle]] of [[Hilbert spaces]] over $X$, hence a canonically [[associated bundle]] to a [[unitary group]]-[[principal bundle]]. Then the space $\Gamma_0(E)$ of continuous compactly supported [[sections]] is a Hilbert C\*-module over $C_0(X)$ with $C_0(X)$-valued [[inner product]] $\langle -,-\rangle$ the pointwise inner product in the [[Hilbert space]] [[fiber]] of $E$:

$$
  \langle \sigma_1, \sigma_2\rangle(x)
  \coloneqq
  \langle \sigma_1(y), \sigma_2(y)\rangle_{E_y}
  \;\in C_0(X)\,,
  \;\;\;\;\;\;
  \sigma_1, \sigma_2 \in \Gamma(E), \; x \in X
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Every Hilbert $C_0(X)$-module arises, up to [[isomorphism]], as in example \ref{FromAHilbertSpaceBundle}.

=--

+-- {: .num_example #CAstAlgebraAsModuleOverItself}
###### Example

Every C\*-algebra $A$ is a Hilbert $A$-module over itself when equipped by with the $A$-valued inner product given simply by

$$
  \langle a_1,a_2\rangle \coloneqq a_1^\ast \cdot a \;\;\in A
$$

=--

+-- {: .num_remark }
###### Remark

In view of the archetypical example \ref{FromAHilbertSpaceBundle}, example \ref{CAstAlgebraAsModuleOverItself} may be interpreted as exhibiting the trivial [[complex line bundle]] over whatever space $A$ is the C\*-algebra of functions on (an actual [[topological space]] if $A$ is a [[commutative C*-algebra]] or else the [[noncommutative topology]] defined as the formal dual of $A$).

=--

+-- {: .num_example #L2}
###### Example

For $A \in $ [[C*Alg]], let $\ell^2 A$ be the space of those [[sequences]] $\{a_n \in A\}_{n \in \mathbb{N}}$ of elements in $A$ such that the [[series]] $\sum_n a_n^\ast a_n$ [[convergence|converges]]. This is a Hilbert $A$-module when equipped with the degreewise $A$-[[C*-representation]], with the $A$-valued inner product

$$ 
  \langle \{a_n\}, \{b_n\}\rangle
  \coloneqq
  \sum_n a_n^\ast b_n
$$

and after [[completion]] with under the induced [[norm]].

This $\ell^2 A$ is sometimes called the **standard Hilbert $A$-module**.

=--

+-- {: .num_remark #TheTrivialHilbertBundleAndL2}
###### Remark

In view of example \ref{FromAHilbertSpaceBundle} we may think of example \ref{L2} as exhibiting the trivial countably-infinite dimensional [[Hilbert space]] bundle over the space dual to $A$.

This is because the [[unitary group]] $U(\mathcal{H})$ of an infinite-dimensional [[separable Hilbert space]] $\mathcal{H}$ is [[contractible topological space|contractible]] (by [[Kuiper's theorem]]), hence so is the [[classifying space]], and so unitary $\mathcal{H}$-fiber bundles (over actual topological spaces) all trivializable. Since moreover $\mathcal{H} \simeq \ell^2(\mathbb{C})$ the Hilbert module of example \ref{FromAHilbertSpaceBundle} for the trivial $\mathcal{H}$-bundle over $C_0(X)$ is equivalent to $\ell^2(C_0(X))$. Example \ref{L2} generalizes this to arbitrary C\*-algebras $A$.

=--



## Properties

### C\*-algebras of adjointable operators on a Hilbert module

+-- {: .num_defn #AdjointableOperator}
###### Definition

For $A \in $ [[C*Alg]] and $H$ a Hilbert $A$-module, def. \ref{HilbertCStarModule}, a $\mathbb{C}$-[[linear operator]] $F \colon H \to H$ is called **adjointable** if there is an [[adjoint operator]] $F^\ast \colon H \to H$ with respect to the $A$-valued inner product in the sense that

$$
  \langle F -, -\rangle = \langle -,F^\ast -\rangle
  \,.
$$ 

=--

+-- {: .num_prop }
###### Proposition

The adjointable operators on a Hilbert $A$-module, def. \ref{AdjointableOperator}, form a [[Banach algebra|Banach]] [[star-algebra]]. 

For $A$ itself regarded as a Hilbert $A$-module as in example \ref{CAstAlgebraAsModuleOverItself}, this is the [[multiplier algebra]] of $A$.

=--

### Compact operators on a Hilbert C\*-module

+-- {: .num_defn #CompactOperator}
###### Definition

For $H_1, H_2$ two Hilbert C\*-modules, an adjointable operator $T \colon H_1 \to H_2$, def. \ref{AdjointableOperator}, is of **finite rank** if it is of the form

$$
  T \colon v \mapsto \sum_{i = 1}^n w_i \langle v_i, v\rangle
$$

for vectors $v_i \in H_1$ and $w_i \in H_2$.  $T$ is called a **generalized compact operator** if it is in the norm-closure of finite-rank operators.

=--

Typically one writes $\mathcal{K}(H_1, H_2)$ for the space of generalized complact operators.

### Fredholm operators

+-- {: .num_defn }
###### Definition

An operator $F \colon H_1 \to H_2$ is called a **generalized [[Fredholm operator]]** if there exists an operator $S \colon H_2 \to H_1$ (then called a [[parametrix]] for $F$) such that both

$ F \circ S - id_{H_2}$ and $S \circ F - id_{H_1}$

are [[compact operators]] according to def. \ref{CompactOperator}.

=--


## Applications

* Kasparov's [[KK-theory]] is formulated in terms of Hilbert (bi)modules

## Related concepts

* [[Hilbert bimodule]]

* [[Mishchenko-Fomenko index theorem]]

* [[duality between algebra and geometry]]

## References

Hilbert C\*-modules were introduced by [[Irving Kaplansky]] in

* Irving Kaplansky, _Modules over operator algebras_, Amer. J. Math. __75__ (1953) 839--853

Contemporary references are

* [[Bruce Blackadar]], _[[K-Theory for Operator Algebras]]_, section 13
* wikipedia, _[Hilbert C\*-module](http://en.wikipedia.org/wiki/Hilbert_C*-module)_
* E. Christopher Lance, _Hilbert C\*-modules, A toolkit for operator algebraists_,  London Math. Soc. Lec. Note Ser. __210__, Cambridge Univ. Press 1995

[[!redirects Hilbert module]]
[[!redirects Hilbert modules]]
[[!redirects Hilbert C*-module]]
[[!redirects Hilbert C*-modules]]
[[!redirects Hilbert C-star-module]]
[[!redirects Hilbert C-star-modules]]
