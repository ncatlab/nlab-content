

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _store comonad_ (also _costate comonad_) is a co[[monad (in computer science)]] used to implement computational storage and retrieval of data in [[functional programming]].

As a comonadic triple $(D,\varepsilon,\delta)$ it is given by an [[endofunctor]],
$$
DX : X \rightarrow W \times [W,X],
$$
with [[natural transformations]] the counit,
$$
\varepsilon : DX \rightarrow Id_X 
$$
$$
\varepsilon(v,f) \mapsto f(v),
$$
usually called **extract** and comultiplication,
$$
\delta: DX \rightarrow DDX
$$
$$
\delta (s, v) \mapsto (s, \lambda  s' . (s', v)),
$$ 

simply called **duplicate**.
## Properties

### Realization in dependent type theory

In a [[locally Cartesian closed category]]/[[dependent type theory]] $\mathbf{H}$, then to every type $W$ is associated its [[base change]] [[adjoint triple]]

$$
  \mathbf{H}_{/W}
   \stackrel{\overset{\sum_W}{\longrightarrow}}{\stackrel{\overset{W^\ast}{\longleftarrow}}{\underset{\prod_W}{\longrightarrow}}}
  \mathbf{H}
  \,.
$$

In terms of this the store comonad is the composite

$$
  Store = \sum_W W^\ast \prod_W W^\ast 
$$

of [[context extension]], followed by [[dependent product]] , followed by [[context extension]], followed by [[dependent sum]].

Here $\prod_W W^\ast = [W,-]$ is called the _[[function monad]]_ or _[[reader monad]]_ and $\sum_W W^\ast = W \times (-)$ is the _[[writer comonad]]_.

## Reference
* [[Bartosz Milewski]], [Lenses, Stores, and Yoneda](https://bartoszmilewski.com/2013/10/08/lenses-stores-and-yoneda/)

* Jeremy Gibbons, [Lenses are the coalgebras for the costate comonad](https://patternsinfp.wordpress.com/2011/01/31/lenses-are-the-coalgebras-for-the-costate-comonad/)

## Related concepts

* [[maybe monad]],

* [[continuation monad]]

* [[state monad]]

* [[function monad]] (reader monad)

[[!redirects costate comonad]]
