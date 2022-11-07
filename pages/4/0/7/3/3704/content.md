
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

> under construction



#Contents#
* table of contents
{:toc}

## Idea

Central aspects of _finite_ [[quantum mechanics]] (with finite-dimensional [[space of states|state space]], notably for [[tensor products]] of [[qbit]] states) and [[quantum computation]] follow formally from the formal properties of the [[category]] [[Hilb|FinHilb]] of [[finite-dimensional vector space|finite-dimensional]] [[Hilbert spaces]]. These properties are axiomatized by saying that [[Hilb]] is an example of a _[[†-compact category]]_.

Conversely, much of finite quantum mechanics and quantum computation can be formulated in _any_ &#8224;-compact category, and general reasoning about &#8224;-compact categories themselves yields results about quantum mechanics and quantum computation.

A transparent [[string diagram]] calculus in &#8224;-compact categories as exposed in ([Coecke, Kindergarten quantum mechanics](#CoeckeKindergarten)) provides an intuitive and powerful tool for reasoning in $\dagger$-compact categories.


## Quantum mechanical concepts in $\dagger$-compact categories

Let $(C,\otimes,I, \dagger)$ be a [[†-compact category]].

We list various concepts in quantum mechanics and their corresponding incarnation in terms of structures in $C$.

### Classical measurement outcomes

An [[observable]] in quantum mechanics formulated on a [[Hilbert space]] is modeled by a [[self-adjoint operator]], and the classical measurement outcomes of this operator provide, at least under some assumptions, an [[orthogonal basis]] on the [[Hilbert space]].

That, more abstractly, the notion of orthogonal basis of an object can be phrased intrinsically inside any suitable $\dagger$-compact category is the point made in ([CoeckePavlovicVicary](#CoeckePavlovicVicary)). 


### Complex phases

The underlying "algebra of quantum amplitudes" of the corresponding quantum mechanical system is the [[endomorphism]] [[monoid]] of the tensor unit

$$
  \mathbb{C}_C = End_C(I)
  \,.
$$


In ([Vicary](#Vicary)) it is shown that in $\dagger$-compact categories with all finite limits over certain "tree-like" diagrams compatible with the $\dagger$-structure, this $\mathbb{C}_C$ has the properties that

* it is a [[field]] of characteristic 0 with involution $\dagger$;

* the subfield $\mathbb{R}_C$ fixed under $\dagger$ is [[order]]able.

If furthermore every bounded sequence of measurements in $C$ with values in $\mathbb{R}_C$ has a least upper bound, then it follows that this field coincides with the [[complex number]]s 

$$
  \mathbb{C}_C = \mathbb{C}
$$

and moreover

$$
  \mathbb{R}_C = \mathbb{R}
  \,.
$$



### Completely positive maps {#ComplPosMaps}

The behaviour of [[quantum channel]]s and _completely positive maps_ has an elegant categorical description in terms of $\dagger$-compact categories. See ([Selinger](#SelingerPositive) and [Coecke](#CoeckePositive)).


## Quantum logic

[[symmetric monoidal categories|Symmetric monoidal categories]] such as [[†-compact categories]] have as [[internal logic]] a fragment of [[linear logic]] and as [[type theory]] a flavor of [[linear type theory]]. In this fashion everything that can be formally said about quantum mechanics in terms of [[†-compact categories]] has an equivalent expression in [[formal logic]]/[[type theory]]. It has been argued ([Abramsky-Duncan 05](#AbramskyDuncan05), [Duncan 06](#Duncan06)) that this [[linear logic]]/[[linear type theory]] of quantum mechanics is the correct formalization of "[[quantum logic]]". An exposition of this point of view is in ([Baez-Stay 09](#BaezStay09)).


## Related concepts

* [[quantum circuit]]

* [[quantum teleportation]]

* [[order-theoretic structure in quantum mechanics]]

* [[linear logic]], [[linear type theory]], [[quantum logic]], [[quantum computing]]

* [[JBW-algebraic quantum mechanics]]

* [[tensor network]], [[string diagram]]

## References
 {#References}

[[!include quantum information theory via string diagrams -- references]]
 

The role of [[complex numbers]] in general $\dagger$-compact categories:

* {#Vicary} [[Jamie Vicary]], _Completeness of $\dagger$-categories and the complex numbers_ ([arXiv:0807.2927](http://arxiv.org/abs/0807.2927)) 


[[!redirects quantum information theory via dagger-compact categories]] 

[[!redirects finite quantum mechanics in terms of †-compact categories]]
[[!redirects finite quantum mechanics in terms of dagger-compact categories]]

[[!redirects quantum mechanics in terms of †-compact categories]]
[[!redirects quantum mechanics in terms of dagger-compact categories]]

[[!redirects finite quantum physics in terms of dagger-compact categories]]
[[!redirects quantum information theory in terms of dagger-compact categories]]

