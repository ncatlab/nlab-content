
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


# $Hilb$
* table of contents
{: toc}

## Definition

A [[category]] whose [[objects]] are [[Hilbert spaces]] is typically denoted $Hilb$ or similar. 

There are different choices of [[morphisms]] in use, such as all [[linear maps]] or just the [[short linear maps]] (linear maps of norm at most $1$).

One may regard $Hilb$ as a [[dagger category]] with [[morphisms]] the [[bounded operator|bounded]] linear maps between them and the dagger operation assigning [[adjoint operators]]. The [[full subcategory]] $Fin Hilb$ of [[finite-dimensional vector space|finite-dimensional]] Hilbert spaces becomes a [[dagger compact category]].

Note that either way, the [[core]] (of [[isomorphisms]] in the first case, or of [[unitary operator|unitary]] isomorphisms in the other case) is the same [[groupoid]], whose morphisms are all invertible linear maps of norm exactly $1$.

In any case, the [[forgetful functor]] from $Hilb$ to [[Vect]] is [[faithful functor|faithful]], confirming the intuition that a Hilbert space is a vector space equipped with [[extra structure]].  $Hilb$ is also a [[full subcategory]] of [[Ban]], the category of [[Banach spaces]].

### Explicit definition

Assuming [[excluded middle]], $Hilb_\mathbb{R}$ is a [[concrete category|concrete]] [[dagger category]] with 

* a tensor product $\otimes$ and tensor unit $\Iota$, such that $(Hilb_\mathbb{R},\otimes,\Iota)$ is a [[symmetric monoidal dagger category]] and $\Iota$ is a [[simple object]] and a monoidal [[separator]], 

* a biproduct $\oplus$ and zero object $0$ such that $(Hilb_\mathbb{R},\oplus,0)$ is a [[semiadditive dagger category]]

* a [[dagger equaliser]] $eq$ such that $(Hilb_\mathbb{R},\oplus,0,eq)$ is a [[finitely complete dagger category]]

* a [[directed colimit]] $\underset{\rightarrow}\lim F$ for any inductive system $F$ in the wide sub-dagger category of objects and [[dagger monomorphisms]]. 

* a morphism $g:B \to C$ for any [[dagger monomorphism]] $f:A \to B$ such that $g = eq(f,0_B \circ 0_A^\dagger)$

However, without excluded middle, this definition fails to result in the category of Hilbert spaces over the real or complex numbers. That a dagger monomorphism $f:H \to I$ is either zero or invertible (in a symmetric monoidal dagger category where $\Iota$ is a simple monoidal separator) implies excluded middle, and [[Solèr’s theorem]] also implies excluded middle. It is currently unknown what modifications are needed to the axioms and to Solèr’s theorem to result in a definition valid without propositional excluded middle in the type theory. It is also unknown what type of real or complex numbers would be derived from the modified axioms and modified Soler's theorem in constructive mathematics. 

## Related concepts

* [[quantum mechanics]]

* [[finite quantum mechanics in terms of dagger-compact categories]]

* [[tensor product of Banach spaces]]

* [[semiadditive dagger category]]

* [[compact closed dagger category]]

## References

A pedagogical description of the [[monoidal category]] structure on $Hilb$ with an emphasis on their role in [[quantum mechanics]] and their relation to [[nCob]]:

* [[John Baez]], _The monoidal category of Hilbert spaces_ ([web](http://math.ucr.edu/home/baez/quantum/node4.html))


An [[axiom|axiomatic]] characterization of the [[dagger-category]] of Hilbert spaces, with [[linear maps]] between them:

* {#HeunenKornell21} [[Chris Heunen]], [[Andre Kornell]], *Axioms for the category of Hilbert spaces* ([arXiv:2109.07418](https://arxiv.org/abs/2109.07418))


category: category

[[!redirects HilbertSpaces]]
