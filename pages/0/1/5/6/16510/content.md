
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

## Idea

In a [[cartesian closed category]]/[[type theory]] $\mathcal{C}$, given any [[object]]/[[type]] $W$ there is a [[comonad]]

$$
  W \times (-) \colon \mathcal{C} \to \mathcal{C}
$$

given by forming the [[Cartesian product]] with $W$, with the [[coproduct]] induced by the [[diagonal map]] on $W$ and the [[counit of a comonad|counit]] induced by the [[terminal object|terminal map]] $W \to \ast$.

Notice then if $W$ is furthermore equipped with the structure of a [[monoid]], then $W \times (-)$ also canonically inherits the structure of a [[monad]], allowing aggregation of a program's $W$ outputs, corresponding to a sort of side channel. Equipped with this [[monad]]-structure, the operation $W \times (-)$ is known as the *[[writer monad]]*, see there for more.

On the other hand, the canonical comonad structure on $W \times (-)$ is [[left adjoint]] to the [[reader monad]], so that it is known as the *reader comonad* (eg. in the [[Haskell]] documentation for *[Control.Comonad.Reader](https://hackage.haskell.org/package/category-extras-0.53.0/docs/Control-Comonad-Reader.html)*) or *coreader comonad* (eg. [Ahman & Uustalu (2019)](#AhmanUustalu19)).

## Properties

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



## Related concepts

* [[writer monad]]

* [[maybe monad]]

* [[continuation monad]]

* [[reader monad]], [[state monad]]

## References

Eg.

* {#AhmanUustalu19} Danel Ahman, Tarmo Uustalu, p. 3 of: *Decomposing Comonad Morphisms*, CALCO 2019, Leibniz International Proceedings in Informatics (LIPIcs) **139** (2019) &lbrack;[doi:10.4230/LIPIcs.CALCO.2019.14](https://doi.org/10.4230/LIPIcs.CALCO.2019.14)&rbrack;


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


[[!redirects writer comonad]]
[[!redirects writer comonads]]

