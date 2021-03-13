
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

given by forming the [[Cartesian product]] with $W$.

In the context of [[monad (in computer science)|monads in computer science]] this is called the _writer comonad_. This is of interest in [[functional programming]] languages such as [[Haskell]], where a [[program]] for the form $X \longrightarrow W \times Y$ behaves like taking input of type $X$ to output of type $Y$ while in addition producing output ("side effect") of type $W$.

If here $W$ is equipped with the structure of a [[monoid]], then $W \times (-)$ also canonically inherits the structure of a [[monad]], allowing aggregation of a program's $W$ outputs, corresponding to a sort of side channel. (See _[[writer monad]]_.)  

## Properties

### Relation to reader monad and state monad

In a [[cartesian closed category]]/[[type theory]] $\mathcal{C}$, the writer comonad $W\times (-)$ is [[left adjoint]] to the [[reader monad]] $[W,-]$.

The composite of writer comonad followed by reader monad is the [[state monad]].


### In terms of dependent type theory

If the type system is even a [[locally Cartesian closed category]]/[[dependent type theory]] then for each type $W$ there is the [[base change]] [[adjoint triple]]

$$
  \mathcal{C}_{/W}
    \stackrel{\overset{\sum_W}{\longrightarrow}}{\stackrel{\overset{W^\ast}{\longleftarrow}}{\underset{\prod_W}{\longrightarrow}}}
  \mathcal{C}
$$

In terms of this then the writer comonad is equivalently the composite

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

* {#Wadler92} [[Philip Wadler]], _[The essence of functional programming](https://page.mi.fu-berlin.de/scravy/realworldhaskell/materialien/the-essence-of-functional-programming.pdf)_, 1992.

* {#Verdier14} [[Olivier Verdier]], _[The Reader and Writer Monads and Comonads](http://www.olivierverdier.com/posts/2014/12/31/reader-writer-monad-comonad/)_, 2014


[[!redirects writer comonads]]

