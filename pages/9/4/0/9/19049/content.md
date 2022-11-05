

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

The _store comonad_ (also _costate comonad_, as it is [[left adjoint]] to the *[[state monad]]*) is a [[comonad|co-]][[monad (in computer science)]] used to implement computational storage and retrieval of [[data]] ([[databases]]) in [[functional programming]].

Concretely, the [[coalgebra over a comonad|coalgebras]] over the store monad are equivalently the well-behaved *[[lenses (in computer science)|lense]]-data structures* ([O’Connor (2010)](#O’Connor10), [(2011)](#O’Connor11);
see [there](lens+in+computer+science#LensesAreCostateCoalgebras)) used to inspect and edit fields ("views") in [[databases]].

## Definition

On a [[cartesian closed category]], the costate comonad is that induced by the [[internal hom]]-[[adjoint functor|adjunction]] ([[left adjoint]] to the [[state monad]]).

In detail: As a comonadic triple $(D,\varepsilon,\delta)$ it is given by an [[endofunctor]],
$$
D X : X \rightarrow W \times [W,X],
$$
with [[natural transformations]] the counit,
$$
\varepsilon : D X \rightarrow X 
$$
$$
\varepsilon(v,f) \mapsto f(v),
$$
usually called **extract** and comultiplication,
$$
\delta: D X \rightarrow D D X
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


## Related concepts

* [[maybe monad]],

* [[continuation monad]]

* [[state monad]]

* [[function monad]] (reader monad)



## References

### General

(...)

### Related to lenses

The observation that [[lenses (in computer science)]] are equivalently the [[coalgebra over a comonad|coalgebras]] of the [[costate comonad]] (cf.  *[[monads in computer science]]*) is due  to:

* {#O’Connor10} [[Russell O’Connor]], *Lenses Are Exactly the Coalgebras for the Store Comonad* (30th Nov 2010) &lbrack;[r6research:23705](https://r6research.livejournal.com/23705.html)&rbrack;

* {#O’Connor11} [[Russell O'Connor]], *Functor is to Lens as Applicative is to Biplate: Introducing Multiplate*, contribution to [ICFP '11: ACM SIGPLAN International Conference on Functional Programming](https://dl.acm.org/doi/proceedings/10.1145/2036918) (2011) &lbrack;[arXiv:1103.2841](https://arxiv.org/abs/1103.2841)&rbrack;

Early review:

* [[Jeremy Gibbons]], *[Lenses are the coalgebras for the costate comonad](https://patternsinfp.wordpress.com/2011/01/31/lenses-are-the-coalgebras-for-the-costate-comonad/)* (2011)

Further details:

* {#GibbonsJohnson12} [[Jeremy Gibbons]], [[Michael Johnson]], *Relating Algebraic and Coalgebraic Descriptions of Lenses*, Electronic Communications of the EASST **49** (2012) &lbrack;[doi:10.14279/tuj.eceasst.49.726](http://dx.doi.org/10.14279/tuj.eceasst.49.726), [pdf](http://www.cs.ox.ac.uk/jeremy.gibbons/publications/colens.pdf)&rbrack;

Further review:

* [[Bartosz Milewski]], *[Lenses, Stores, and Yoneda](https://bartoszmilewski.com/2013/10/08/lenses-stores-and-yoneda/)* (2013)

[[!redirects store comonads]]

[[!redirects costate comonad]]
[[!redirects costate comonads]]


