
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

[[!redirects theory of pointed objects]]
[[!redirects theory of inhabited objects]]

#Contents#
* table of contents
{:toc}

##Idea
The _theory of objects_ is the logical theory whose models in a category $\mathcal{C}$ are precisely the objects of $\mathcal{C}$.

## Definition

The _theory of objects_ $\mathbb{O}$ is the [[theory]] with no axioms over the [[signature (in logic)|signature]] with a single [[type]] and no primitive symbols except [[equality]].

## Properties

Of course, $\mathbb{O}$ is a [[geometric theory]], and as [[models]] for $\mathbb{O}$ in a [[topos]] $\mathcal{E}$ correspond to [[objects]] of $\mathcal{E}$, we can use its [[classifying topos]] to get a representation of the objects of $\mathcal{E}$.

+-- {: .num_prop}
###### Proposition

The [[classifying topos]] for the theory of objects is the [[presheaf topos]] $[FinSet, Set]$ over the [[opposite category]] of the category [[FinSet]] of [[finite sets]].
=--

See at _[[classifying topos for the theory of objects]]_.

##Further Remarks

* For more general base toposes $\mathcal{S}$, it is a theorem due to [[Andreas Blass]] that the theory of objects has a classifying topos precisely if $\mathcal{S}$ has a [[natural numbers object]].

* A step up on the ladder of logical complexity is the **theory of inhabited objects** $\mathbb{O}_\exists$ that adds to $\mathbb{O}$ the existential axiom $\top\vdash(\exists x)\top$. Its classifying topos $Set[\mathbb{O}_\exists]$ is the functor category $[FinSet_\exists, Set]$ with $FinSet_\exists$ the _category of finite nonempty sets_. It has the property that every topos $\mathcal{E}$ admits a [[localic topos|localic morphism]] to $Set[\mathbb{O}_\exists]$.[^fine] 

[^fine]: cf. Johnstone (2002 II, p.773) and [[Andre Joyal|Joyal-Tierney (1984)]]. For some further information on $FinSet_\exists$ see the references at [[generic interval]].

* If instead of an additional axiom one adds a single constant symbol to the signature of $\mathbb{O}$ one obtains the **theory of pointed objects** $\mathbb{O}_\ast$ i.e. the empty theory relative to the signature with a single sort and a single constant. Its models are pointed objects and its classifying topos is $[FinSet_\ast,Set]$. (See the discussion&references at [[classifying topos for the theory of objects]].)

* In the syntax-free approach to geometric theories of Johnstone (2002, I B4.2) the **theory of objects** corresponds to the forgetful functor sending an $\mathcal{S}$-topos to its underlying category. (See at [[geometric theory]] the section on the functorial definition.)

## Related Concepts

* [[theory of decidable objects]]

## References

Sections B4.2, D3.2 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

