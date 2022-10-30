
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

The _state monad_ is a [[monad (in computer science)]] used to implement computational side-effects in [[functional programming]].

A [[functional program]] with 

1. input of ([[data type|data-]])[[type]] $X$, 

1. output of [[type]] $Y$ 

1. and "mutable state" of [[type]] $W$ 

   (e.g. the state of a "random access memory" device, cf. [Yates (2019), p. 26 & Fig. 1.10](#Yates19)) 

is clearly a [[function]] ([[morphism]]) of [[function type]] betwen the [[product types]] with $W$: 

$$
  prog 
    \;\colon\;
  X \times W 
    \longrightarrow 
  Y \times W
  \,.
$$ 

Now, under the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the ([[Cartesian product]] $\dashv$ [[internal hom]])-[[adjoint functor|adjunction]], this is equivalently given by its [[adjunct]], which is a function into the [[function type]] $[-,-]$ ([[internal hom]]):

$$
  X \longrightarrow [W, W \times Y ]
 \,.
$$

Here the operation $[W, W\times (-)]$ is the [[monad]] on the type system which is induced by the above [[adjunction]]; and this latter function is naturally regarded as a morphism in the [[Kleisli category]] of this monad. 

In the context of [[monad (in computer science)|monads in computer science]], this monad $[W, W\times (-)] \colon \mathbf{H} \to \mathbf{H}$ is called the _state monad_ for mutable states of type $W$.

## Properties

### Realization in dependent type theory

In a [[locally Cartesian closed category]]/[[dependent type theory]] $\mathbf{H}$, then to every type $W$ is associated its [[base change]] [[adjoint triple]]

$$
  \mathbf{H}_{/W}
   \stackrel{\overset{\sum_W}{\longrightarrow}}{\stackrel{\overset{W^\ast}{\longleftarrow}}{\underset{\prod_W}{\longrightarrow}}}
  \mathbf{H}
  \,.
$$

In terms of this the state monad is the composite

$$
  State = \prod_W W^\ast \sum_W W^\ast
$$

of [[context extension]] followed by [[dependent sum]], followed by [[context extension]], followed by [[dependent product]].

Here $\prod_W W^\ast = [W,-]$ is called the _[[function monad]]_ or _[[reader monad]]_ and $\sum_W W^\ast = W \times (-)$ is the _[[writer comonad]]_.


## Related concepts

* [[maybe monad]],

* [[continuation monad]]

* [[function monad]] (reader monad)

* [[QRAM]]

## References 

The abstract notion of the state monad:

* {#PlotkinPower02} [[Gordon Plotkin]], [[John Power]], Section 3 of: *Notions of computation determine monads* In: M. Nielsen, U. Engberg, (eds.) FOSSACS 2002. LNCS, Lecture Notes in Computer Science **2303**,  Springer (2002) 342-356 &lbrack;[doi:10.1007/3-540-45931-6_24p](https://doi.org/10.1007/3-540-45931-6_24)&rbrack;

Concrete applications via implementation in [[Haskell]]:

* {#Yates19} Ryan Yates, *Improving Haskell Transactional Memory* (2019) &lbrack;[hdl:1802/35367](https://hdl.handle.net/1802/35367), [pdf](file:///C:/Users/us13/Downloads/Yates_rochester_0188E_11946.pdf)&rbrack;


In the generality of the *local* state monad:

* [Plotkin & Power (2002), Sec. 4](#PlotkinPower02)

* [[Paul-André Melliès]], *Local States in String Diagrams*, In: G. Dowek (eds.) *Rewriting and Typed Lambda Calculi* RTA TLCA 2014, Lecture Notes in Computer Science **8560**, Springer (2014) &lbrack;[doi:10.1007/978-3-319-08918-8_23](https://doi.org/10.1007/978-3-319-08918-8_23)&rbrack;

[[!redirects state monads]]

[[!redirects local state monad]]
[[!redirects local state monads]]

[[!redirects random access memory]]
[[!redirects random access memories]]

[[!redirects RAM]]
[[!redirects RAMs]]

