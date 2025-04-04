
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given an object $W$ in a [[category]] $\mathcal{C}$, if all binary [[cartesian products]] with $W$ exist, then taking the cartesian product with $W$ assembles into a [[comonad]]

$$
  W \times (-) 
  \;\colon\; 
  \mathcal{C} \longrightarrow \mathcal{C}
$$

whose [[comultiplication]] is induced by the [[diagonal map]] on $W$ and whose [[counit of a comonad|counit]] is induced by the [[terminal object|terminal map]] $W \to \ast$.

When $W$ is furthermore equipped with the [[structure]] of a [[monoid]], then $W \times (-)$ also canonically inherits the structure of a [[monad]]. (Regarded as a [[monad in computer science]] this models the aggregation of a program's $W$-typed outputs, corresponding to a sort of side channel.) Equipped with this [[monad]]-structure, the operation $W \times (-)$ is known as the *[[writer monad]]*, see there for more.

On the other hand, if $W$ is further [[exponentiable object|exponentiable]] then $W \times (-)$ is [[left adjoint]] to the [[reader monad]] $W \to -$, so that it is known as the **reader comonad** (eg. in the [[Haskell]] documentation for *[Control.Comonad.Reader](https://hackage.haskell.org/package/category-extras-0.53.0/docs/Control-Comonad-Reader.html)*) or **coreader comonad** (e.g. [Ahman & Uustalu (2019)](#AhmanUustalu19)). It is also known as the **product comonad** (e.g. [Uustalu & Vene 2008, p. 270](#UustaluVene08)) and the **environment comonad** (eg. in the [[Haskell]] documentation for *[Control.Comonad.Env](https://hackage.haskell.org/package/comonad-5.0.8/docs/Control-Comonad-Env.html)*).

Coreader comonads in $\mathcal{C}^op$ are [[exception monads]] in $\mathcal{C}$, because products turn into [[coproducts]].

## Properties

### As an indexed comonad

If all binary cartesian products in $C$ exist, then the coreader comonad extends to a $C$-indexed comonad on $C$, i.e. a functor $C \to Comonad$. If $C$ has a [[terminal object]] $1$, then the environment comonad $1 \times -$ is isomorphic to the identity comonad.

### Generalization to tensor products

If $C$ is a [[monoidal category]] rather than having all binary products, then tensoring with an object $\Gamma \otimes -$ can be given an analogous comonad structure when $\Gamma$ has a [[comonoid]] structure. In a [[cartesian monoidal category]] every object has a unique comonoid structure, which is what induces the coreader comonad. Even without assuming objects carry comonoid structures, the action sending $\Gamma$ to the functor $\Gamma \otimes -$ defines a strong [[monoidal functor]] from $C$ to the monoidal category of endofunctors $[C,C]$, a degenerate kind of [[graded monad|graded comonad]].

### Relation to reader monad and state monad

In a [[cartesian closed category]]/[[type theory]] $\mathcal{C}$, the coreader comonad $W\times (-)$ is [[left adjoint]] to the [[reader monad]] $[W,-]$.

The composite of coreader comonad followed by reader monad is the [[state monad]].


### In terms of dependent type theory

If the type system is even a [[locally Cartesian closed category]]/[[dependent type theory]] then for each type $W$ there is the [[base change]] [[adjoint triple]]

$$
  \mathcal{C}_{/W}
    \stackrel{\overset{\sum_W}{\longrightarrow}}{\stackrel{\overset{W^\ast}{\longleftarrow}}{\underset{\prod_W}{\longrightarrow}}}
  \mathcal{C}
$$

In terms of this then the coreader comonad is equivalently the composite

$$
  \sum_W W^\ast = W\times (-) \;\colon\; \mathcal{C} \longrightarrow \mathcal{C}
$$

of [[context extension]] followed by [[dependent sum]].

One may also think of this as being the [[integral transform]] through the span

$$
  \ast \leftarrow W \rightarrow \ast
$$

(with trivial kernel) or as the [[polynomial functor]] associated with the span 

$$
  \ast \leftarrow W \stackrel{id}{\rightarrow} W \rightarrow \ast
  \,.
$$

## Coalgebras

A [[coalgebra of a comonad|coalgebra]] of the coreader comonad $W \times -$ is equivalent to simply a morphism $A \to W$ for $A$ the carrier of the co-algebra. Furthermore, the category of coalgebras is the isomorphic to the [[slice category]] over $W$. This shows that if all cartesian products with $W$ exist, then the forgetful functor $\Sigma_W \colon C / W \to C$ is [[comonadic]].


## Related concepts

[[!include reader-writer (co)monads -- table]]

* [[maybe monad]]

* [[continuation monad]]

* [[state monad]]

* [[exception monad]]

## References

Eg.

* {#AhmanUustalu19} [[Danel Ahman]], [[Tarmo Uustalu]], p. 3 of: *Decomposing Comonad Morphisms*, CALCO 2019, Leibniz International Proceedings in Informatics (LIPIcs) **139** (2019) &lbrack;[doi:10.4230/LIPIcs.CALCO.2019.14](https://doi.org/10.4230/LIPIcs.CALCO.2019.14)&rbrack;

* [[Tarmo Uustalu]], p. 13 of: *Monads and Interaction Lecture 3*, lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021) &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs3.pdf), [[Uustalu-Monads3.pdf:file]]&rbrack;

* {#UustaluVene08} [[Tarmo Uustalu]], [[Varmo Vene]], *Comonadic Notions of Computation*, Electronic Notes in Theoretical Computer Science **203** 5 (2008) 263-284 &lbrack;[doi:10.1016/j.entcs.2008.05.029](https://doi.org/10.1016/j.entcs.2008.05.029)&rbrack;

In [[Haskell]]:

* *[Control.Comonad.Reader](https://hackage.haskell.org/package/category-extras-0.53.0/docs/Control-Comonad-Reader.html)*

See also:

* {#Wadler92} [[Philip Wadler]], _[The essence of functional programming](https://page.mi.fu-berlin.de/scravy/realworldhaskell/materialien/the-essence-of-functional-programming.pdf)_, 1992.

* {#Verdier14} [[Olivier Verdier]], _[The Reader and Writer Monads and Comonads](http://www.olivierverdier.com/posts/2014/12/31/reader-writer-monad-comonad/)_, 2014


[[!redirects reader comonad]]
[[!redirects reader comonads]]

[[!redirects coreader comonad]]
[[!redirects coreader comonads]]

[[!redirects co-reader comonad]]
[[!redirects co-reader comonads]]

[[!redirects product comonad]]
[[!redirects environment comonad]]


[[!redirects writer comonad]]
[[!redirects writer comonads]]

