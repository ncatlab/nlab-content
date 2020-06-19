
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

[[!redirects theory of pointed objects]]
[[!redirects theory of inhabited objects]]

#Contents#
* table of contents
{:toc}

##Idea
The _theory of objects_ is the logical theory whose models in a category $\mathcal{C}$ are precisely the objects of $\mathcal{C}$. From an algebraic perspective one can think of it as the theory of an algebra with no operations.

## Definition

The _theory of objects_ $\mathbb{O}$ is the [[theory]] with no axioms over the [[signature (in logic)|signature]] with a single [[type]] and no primitive symbols except [[equality]].

## Properties

Of course, $\mathbb{O}$ is a [[geometric theory]], and as [[models]] for $\mathbb{O}$ in a [[topos]] $\mathcal{E}$ correspond to [[objects]] of $\mathcal{E}$, we can use its [[classifying topos]] to get a representation of the objects of $\mathcal{E}$.

+-- {: .num_prop}
###### Proposition

The [[classifying topos]] for the theory of objects is the [[presheaf topos]] $[FinSet, Set]$ over the [[opposite category]] of the category [[FinSet]] of [[finite sets]].
=--

This follows from the fact that $\mathbb{O}$ is the [[algebraic theory]] of a 1-sorted algebra without operations whence its algebras are merely sets. The classifying topos for algebraic theories is quite generally given by the presheaf topos on the opposite of the category of finitely presentable models in our case just the finite sets.

For a direct proof see at _[[classifying topos for the theory of objects]]_.
For base toposes $\mathcal{S}$ other than $Set$, it is a theorem due to [[Andreas Blass]] that the theory of objects has a classifying topos precisely if $\mathcal{S}$ has a [[natural numbers object]].

In the syntax-free approach to geometric theories of Johnstone (2002, I B4.2) the **theory of objects** corresponds to the forgetful functor sending an $\mathcal{S}$-topos to its underlying category. (See at [[geometric theory]] the section on the functorial definition.)

## Quotient and other related theories

* A step up on the ladder of logical complexity is the **theory of inhabited objects** $\mathbb{O}_\exists$ that adds to $\mathbb{O}$ the existential axiom $\top\vdash(\exists x)\top$. Its classifying topos $Set[\mathbb{O}_\exists]$ is the functor category $[FinSet_\exists, Set]$ with $FinSet_\exists$ the _category of finite nonempty sets_. It has the property that every topos $\mathcal{E}$ admits a [[localic topos|localic morphism]] to $Set[\mathbb{O}_\exists]$.[^fine] 

[^fine]: cf. Johnstone (2002 II, p.773) and [[Andre Joyal|Joyal-Tierney (1984)]]. For some further information on $FinSet_\exists$ see the references at [[generic interval]].

* When viewed as algebraic theory the initial algebra (in $Set$) is the empty set which satisfies $(\exists x)\top\vdash\bot$. Adding the sequent to the theory of objects one obtains the **theory of empty objects** $\mathbb{O}_\emptyset$, its models are the [[initial object|initial objects]]. Its classifying topos is $Set$ with $\emptyset$ as generic object. Whence the duality between quotient theories and subtoposes implies that $Set[\mathbb{O}]$ contains $Set[\mathbb{O}_\emptyset]$. The pattern that the classifying topos of an algebraic theory contains a copy of $Set$ as a [[subtopos]] classifying $Th(\mathfrak{A}_0)$ i.e. the theory of all geometric sequents holding at the initial algebra $\mathfrak{A}_0$ in Set is valid more generally (see at [[geometric type theory]] for another example).

* If instead of an additional axiom one adds a single constant symbol to the signature of $\mathbb{O}$ one obtains the **theory of pointed objects** $\mathbb{O}_\ast$ i.e. the empty theory relative to the signature with a single sort and a single constant. Its models are pointed objects and its classifying topos is $[FinSet_\ast,Set]$. (See the discussion&references at [[classifying topos for the theory of objects]].)

* The **theory of morphisms** $\mathbb{O}^2$ is the theory with no sequents over the signature with two sort symbols $O^0$, $O^1$ and a function symbol $f_O:O^0\to O^1$. It is the [[theory of model homomorphisms|theory of $\mathbb{O}$-model homomorphisms]] and its models in a Grothendieck topos $\mathcal{E}$ are the morphisms of $\mathcal{E}$. It is the [[exponentiable topos|dual theory]] of the theory classified by the [[Sierpinski topos]] $Set^2$, or in other words, its [[classifying topos]] is $Set[\mathbb{O}^2]=Set[\mathbb{O}]^{Set^2}$.

## Related Concepts

* [[theory of decidable objects]]

* [[theory of model homomorphisms]]

## References

Sections B4.2, D3.2 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

