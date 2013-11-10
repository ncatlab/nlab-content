
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

In [[functional analysis]] and related areas of mathematics _stereotype spaces_ are [[topological vector spaces]] defined by a special variant of reflexivity condition. They form a class of spaces with a series of remarkable properties, in particular, this class is very wide (for instance, it contains all [[Fréchet spaces]] and thus, all [[Banach spaces]]), it consists of spaces satisfying a natural condition of completeness, and it forms a [[closed monoidal category]] with the standard analytical tools for constructing new spaces, like taking closed subspace, quotient space, projective and injective limits, the space of operators, tensor products, etc.

* From Wikipedia: [Stereotype space](https://en.wikipedia.org/wiki/Stereotype_space) 

## Definition 

Let $X$ be a [[topological vector space]] over the [[complex numbers]] $\mathbb{C}$. Let $X^\ast$ be the vector space of continuous linear functionals $X \to \mathbb{C}$ endowed with the [[topology]] of uniform convergence on [[totally bounded space|totally bounded]] subsets of $X$[^fine]. This $X^\ast$ is a topological vector space, and may be regarded as a form of dual space of $X$. This construction defines a [[contravariant functor]] $(-)^\ast$ on the category of topological vector spaces. 

There is a canonical [[natural transformation]] $i_X: X \to X^{\ast\ast}$, sending $x \in X$ to the functional defined by $i(x)(f) \coloneqq f(x)$. 

+-- {: .num_defn} 
###### Definition 
A TVS $X$ is a **stereotype space** if $i_X$ is an [[isomorphism]]. 
=-- 

There is another way of characterizing stereotype spaces $X$ directly in terms of the TVS structure on $X$. We say that a TVS $X$ is *pseudo-complete* if every totally bounded [[Cauchy net]] in $X$ converges. Next, call a subset $C$ of $X$ *capacious* if, for every totally bounded set $A \subset X$, there exists a finite set of elements $x_1, \ldots, x_n$ such that every $y \in \bar{A}$ is contained in some translate $x_i + C$. Then, say that $X$ is *pseudo-saturated* if every closed convex balanced capacious subset of $0$ is a neighborhood of $0$ (this can be regarded as a weakening of the notion of barreledness). 

+-- {: .num_theorem} 
###### Theorem 
A TVS $X$ is a stereotype space if and only if it is locally convex, pseudo-complete, and pseudo-saturated. 
=-- 

## Basic results 

+-- {: .num_prop} 
###### Proposition 
The inclusion of pseudo-saturated locally convex TVS, as a [[full subcategory]] of locally convex TVS, is [[coreflection|coreflective]]. The right adjoint to the inclusion takes $X$ to a space denoted $X^\triangle$, called the *pseudo-saturation* of $X$. If $X$ is pseudo-complete, so is $X^\triangle$. 
=-- 

Let $X$, $Y$ be stereotype spaces, and let $L(X, Y)$ be the space of continuous linear maps $X \to Y$. Then $L(X, Y)$ is locally convex, and as $Y$ is pseudo-complete, it follows that $L(X, Y)$ is also pseudo-complete. However, $L(X, Y)$ might not be pseudo-saturated. Let $Hom(X, Y)$ be the pseudo-saturation of $L(X, Y)$, so that $Hom(X, Y)$ is a stereotype space. This construction endows the category of stereotype spaces with a [[closed category]] structure, with unit $\mathbb{C}$. We have $X^\ast \cong Hom(X, \mathbb{C})$. 

+-- {: .num_theorem} 
###### Theorem 
The category of stereotype spaces, as a closed category with duality $(-)^\ast$, acquires a structure of complete and cocomplete $\ast$-[[star-autonomous category|autonomous]] category. 
=-- 

In slightly more detail, a tensor product on stereotype spaces may be defined by the formula $X \otimes Y \coloneqq Hom(X, Y^\ast)^\ast$. Then for stereotype spaces $X, Y, Z$ there is a natural isomorphism 

$$\hom(X \otimes Y, Z) \cong \hom(X, Hom(Y, Z))$$ 

and there are associativity, symmetry, and unit constraints on $\otimes$ so that in this way, stereotype spaces form a [[closed monoidal category|symmetric monoidal closed category]]. By taking $D = I = \mathbb{C}$ as dualizing object, it is moreover $\ast$-autonomous. It is not, however, autonomous in the sense of [[compact closed categories]], i.e., we do not have an isomorphism between $(X \otimes Y)^\ast$ and $X^\ast \otimes Y^\ast$. Rather, we get a second tensor product via the formula 

$$X \odot Y \coloneqq (X^\ast \otimes Y^\ast)^\ast$$ 

and this tensor product plays the role of multiplicative disjunction in [[linear logic]] (where we regard $\ast$-autonomous categories as models of multiplicative linear logic). 

## References 

* S.S. Akbarov, _Pontryagin duality in the theory of topological vector spaces and in topological algebra_, Journal of Mathematical Sciences 113 (2) (2203), 179&#8211;349. 

[^fine]: In other words, the smallest topology on $X^\ast$ that includes all sets $L(B, U) \coloneqq \{f: X \to \mathbb{C}: f(B) \subseteq U\}$ where $B$ is totally bounded in $X$ and $U$ is open in $\mathbb{C}$. 