

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A __comonad__ (or cotriple) on a [[category]] $A$ is a [[comonoid]] in the [[monoidal category]] of endofunctors $A \to A$. More generally, a comonad in a [[2-category]] $E$ is a [[comonoid]] in the [[monoidal category]] $E(X,X)$ for some [[object]] $X\in K$.

Just as a monad may be defined for any 2-category, $E$, as a [[lax 2-functor]] from $\mathbf{1}$ to $E$, so a comonad in $E$ is an oplax 2-functor from $\mathbf{1} \to E$.

See at _[[monad]]_ for more.

## Properties

### Coalgebras

A **[[coalgebra over a comonad]]** (or **comodule**) over a comonad $C$ on a category $A$ is an object $a\in A$ with a map $a\to C a$ satisfying dual axioms to those for an [[algebra over a monad]].  The category of coalgebras is called its (co-)[[Eilenberg-Moore category]] and satisfies a universal property dual to that of the [[Eilenberg-Moore object]] for a monad; it can thereby be internalized to any [[2-category]].  The [[forgetful functor]] from the category of coalgebras to the category $A$ is called a [[comonadic functor]].  Similarly, a comonad also has a [[co-Kleisli category]].

### Comonadic homology and descent

Any comonad on $A$ induces an augmented [[simplicial object|simplicial]] [[endofunctor]] of $A$ consisting of its iterates.  If $A$ is an [[abelian category]] and the comonad is [[additive monad|additive]], then this is the basis of [[comonadic homology]].  [[algebra for a monad|Comodules]] (= coalgebras) over the comonad with underlying endofunctor $M_R\mapsto M_R\otimes_R S$ in $R$-$Mod$ for the  extension of rings $R\hookrightarrow S$ correspond to the [[descent]] data for that extension. [[zoranskoda:gluing categories from localizations|Gluing of categories from localizations]] may also be formalized via comonads.

### Mixed distributive laws

[[distributive law|Distributive laws]] between a monad and a comonad are so-called _mixed_ distributive laws; a special case has been rediscovered in physics under the name _entwining structures_ (Brzezi&#324;ski, Majid 1997). Their theory is often studied in the connection with the theory of comonads in the bicategory of rings, modules and morphisms of modules, that is [[coring]]s. There is a homomorphism of bicategories from a bicategory of entwinings to a bicategory of corings ([&#352;koda 2008](http://front.math.ucdavis.edu/0805.4611)), which is an analogue of the 2-functor $comp$ (R. Street, _Formal theory of monads_, JPAA 1972) of strict 2-categories in the case of distributive laws of monads (recall also that a distributive law among monads corresponds to a monad in the 2-category of monads).

## Examples

* [[necessity]]

* [[writer comonad]]

* [[store comonad]]

* [[flat modality]], [[infinitesimal flat modality]], [[reduction modality]], [[bosonic modality]]

* [[jet comonad]]

## Related concepts

* [[model structure on coalgebras over a comonad]]


## References

Some introductory material on [[comonads]], [[coalgebra over a comonad|coalgebras]] and [[co-Kleisli morphisms]] can be found in

* [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_, Chapter 5. ([arXiv](http://arxiv.org/abs/1912.10642))


[[!redirects comonads]]
[[!redirects cotriple]]
[[!redirects cotriples]]
