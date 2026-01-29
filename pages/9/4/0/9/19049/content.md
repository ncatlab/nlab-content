

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

The _store comonad_ (also _costate comonad_, as it is in a sense dual to the *[[state monad]]*) is a [[comonad|co-]][[monad (in computer science)]] used to implement computational storage and retrieval of [[data]] ([[databases]]) in [[functional programming]].

Concretely, the [[coalgebra over a comonad|coalgebras]] over the store monad are equivalently the well-behaved *[[lenses (in computer science)|lens]]-data structures* ([O’Connor (2010)](#O’Connor10), [(2011)](#O’Connor11);
see [there](lens+in+computer+science#LensesAreCostateCoalgebras)) used to inspect and edit fields ("views") in [[databases]].

## Definition

### On a cartesian closed category
 {#OnACartesianClosedCategory}

By default, the costate comonad is understood to be defined on a [[cartesian closed category]] $(\mathcal{C}, \times \ast)$ whose [[internal hom]] we denote by $[\text{-}, \text{-}]$.

This means that given an [[object]] $S \in \mathcal{C}$ there is a pair of [[adjoint functors]]

\[
  \label{CartesianInternalHomAdjunction}
  \mathcal{C}
  \underoverset
    {\underset{[S,\text{-}]}{\longrightarrow}}
    {\overset{S \times (\text{-})}{\longleftarrow}}
    {\;\; \bot \;\;}
  \mathcal{C}
  \,.
\] 

Notice that 

* the [[unit of an adjunction|unit]] of this adjunction (being the [[adjunct]] of the [[identity morphism]] on ${S \times D}$) is:

  \[
    \label{InternalHomAdjunctionUnit}
    \array{
      D
      &
      \overset{
        ret^{ S State }_D
      }{\longrightarrow}
      &
      \big[ S ,\, S \times D \big]
      \\
      d &\mapsto& \big( s \mapsto (s,d)  \big)
      \mathrlap{\,,}
    }
  \]

* the [[counit of an adjunction|counit]] of this adjunction (being the [[adjunct]] of the [[identity morphism]] on ${[S,D]}$) is the [[evaluation map]]

  \[
    \label{InternalHomAdjunctionCoUnit}
    \array{
      S \times [S,D]
      &
      \overset{
        obt^{S Store}_D
      }{\longrightarrow}
      &
      D
      \\
      \big(
        s, f
      \big)
      &\mapsto&
      f(s)
      \mathrlap{\,.}
    }
  \]

While  the $S$-[[state monad]] is the [[monad]] [induced](monad#RelationBetweenAdjunctionsAndMonads) by this adjunction (eq:CartesianInternalHomAdjunction)

  $$
    S State 
      \,\coloneqq\, 
    \big[
      S
      ,\,
      S \times (\text{-})
    \big]
  $$

the *$S$-store comonad* is the induced comonad

$$
  S Store
  \,\coloneqq\,
  S \times \big[ S,\, (\text{-}) \big]
  \,.
$$

whose [[counit of a comonad|counit]] is (eq:InternalHomAdjunctionCoUnit) and whose duplicate operation (comonad coproduct) is given by the unit (eq:InternalHomAdjunctionUnit) as

$$
  \array{
    S \times [S, D]
    &
    \overset{
      S \times 
      ret^{S State}_{[S,D]}
    }
    {\longrightarrow}
    &
    S \times \big[S, S \times [S,D] \big]
    \\
    (s, f)
    &\mapsto&
    \Big(
      s
      ,\,
      \big(
        s' 
        \,\mapsto\,
        (s', f) 
      \big)
    \Big)
  }
$$

Therefore the [[comonadic extend operation]] sends a [[coKleisli morphism]]

$$
  \mathcal{O}
  \,\colon\,
  S \times [S,D]
  \longrightarrow
  D'
$$

to

$$
  \array{
    \mathllap{
      extend^{ S Store }_{D,D'} \mathcal{O}
      \;\;\colon\;\;
    }
    S \times [S,D]
    &\overset{
      S \times ret^{S State}_{[S,D]}
    }{\longrightarrow}&
    S \times \big[ S \times [S,D]  \big]
    &\overset{
      S \times \big[ S, \mathcal{O} \big]
    }{\longrightarrow}&
    S \times [S, D']
    \\
    (s,f)
    &\mapsto&
    \Big(
      s
      ,\,
      \big(
        s' 
        \,\mapsto\,
        (s', f) 
      \big)
    \Big)   
    &\mapsto&
    \Big(
      s
      ,\,
      \big(
        s' 
        \,\mapsto\,
        \mathcal{O}(s',f)
      \big)
    \Big)   
    \mathrlap{\,.}
  }
$$

In applications of [[comonads in computer science]] one thinks of 

* $S$ as an address type,

* $[S,D]$ a data base of $S$-indexed $D$-data

hence of the $S Store$-comonad on $D$ as providing the computational context consisting of data base (of "stored $D$-values", whence the name *store comonad*) and an address.

Thus the *obtain*-operation (eq:InternalHomAdjunctionCoUnit) literally obtains (reads, extracts) the memory content at the given address.

### On closed monoidal categories

More generally, for $(\mathcal{C}, \otimes, \mathbb{1})$ a [[closed monoidal category]] (not necessarily [[cartesian closed category|cartesian]]), every object $D$ still still gives an [[internal-hom]] [[adjoint functor|adjunction]] of the form (eq:CartesianInternalHomAdjunction)

\[
  \label{MonoidalInternalHomAdjunction}
  \mathcal{C}
  \underoverset
    {\underset{[S,\text{-}]}{\longrightarrow}}
    {\overset{S \otimes (\text{-})}{\longleftarrow}}
    {\;\; \bot \;\;}
  \mathcal{C}
\] 

and the [induced](monad#RelationBetweenAdjunctionsAndMonads) [[monad]] and [[comonad]] may be understood as [[substructural logic|substructural]] forms of the [[state monad]] and store comonad, respectively.

Particularly when $\mathcal{C} \,\equiv\, Mod_{\mathbb{C}}$ is the [[category of vector bundles|category of]] [[complex vector spaces]] ("$\mathbb{C}$-[[linear spaces]]") this gives a [[linear type theory|linear]] form of the costate comonad, discussed at

* *[[quantum costate comonad]]*.


## Properties

### Realization by base change

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



### Store-Comodules are Lenses
 {#LabelStoreComodulesAreLenses}

We spell out the data of [[comodule over a comonad|comodules]] over the classical Store comonad defined [above](#OnACartesianClosedCategory).

> (Beware that we are switching from using "$S$" for the state space to using it for the argument of the comonad -- this in order to be closer to the notation used at *[[lens in computer science]]*.)

Unwinding the definitions, a $V$-store [[comodule over a comonad|comodule]] [[structure]] on a type $S$ is a [[map]] of the form

\[
  \label{ComoduleMap}
  \array{
    S
    &
    \overset{
      \big(
        get
        ,\, 
        \widetilde{put}
      \big)
    }{\longrightarrow}
    &
    V \times [V, S]    
    \\
    s
    &\mapsto&
    \big(
      get(s)
      ,\,
      put(-,s)
    \big)
  }
\]

and hence consists, equivalently, of a [[pair]] of [[functions]] of the form

\[
  \label{LensStructureMaps}
  \begin{array}{l}
    get \;\colon\; S \to V \,,
    \\
    put \;\colon\; V \times S \to S \,.
  \end{array}
\]

On this data, the counitality condition of a comodule (eq:ComoduleMap) requires that the following composite is the [[identity morphism|identity]]

$$
  \array{
    S
    &
    \overset{
      \big(
        get
        ,\, 
        \widetilde{put}
      \big)
    }{\longrightarrow}
    &
    V \times [V, S]    
    &
    \overset{
      obt^{ V Store }_S
      \equiv
      ev 
    }{\longrightarrow}
    &
    S
    \\
    s 
    &\mapsto&
    \big(
      get(s)
      ,\,
      put(-,s)
    \big)
    &\mapsto&
    put\big(
      get(s)
      ,\,
      s
    \big)
    \mathrlap{\,,}
  }
$$

hence that

\[
  \label{GetPutLaw}
  s \in S
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  put\big(
    get(s)
    ,\,
    s
  \big)  
  \;=\;
  s
  \mathrlap{\,,}
\]

while the coaction property requires that the following [[commuting diagram|diagram commutes]]

\begin{tikzcd}[  
  column sep=4pt
]
  V \times [V,S]
  \ar[
    rrrrr,
    "{
      \mathrm{dupl}^{ V\mathrm{Store} }_S
    }"
  ]
  &[-5pt]
  &&&[-150pt]
  &[-30pt]
  V \times \Big[ 
    V 
    ,\,
    \big[
      V 
      \times 
      [V,S] 
    \big]
  \Big]
  \\
  &
  \big(
    \mathrm{get}(s)
    ,\,
    \mathrm{put}(-,s)
  \big)
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  \Big(
    \mathrm{get}(s)
    ,\,
    v' \mapsto \big(v', \mathrm{put}(-,s)\big) 
  \Big)
  \\
  &&&& 
  \bigg(
    \mathrm{get}(s)
    ,\,
    v'
    \mapsto
    \Big(
      \mathrm{get}\big(\mathrm{put}(v',s)\big)
      ,\,
      \mathrm{put}\big(-, \mathrm{put}(v',s)\big)      
    \Big)
  \bigg)
  \ar[ul, equals]
  \\
  & 
  &&& 
  \\
  & 
  s 
  \ar[rrr, phantom, "{ \mapsto }"]
  \ar[uuu, phantom, "{ \mapsto }"{sloped}]
  &&& 
  \big(
    \mathrm{get}(s)
    ,\,
    v' \mapsto \mathrm{put}(v',s)
  \big)
  \ar[uu, phantom, "{ \mapsto }"{sloped}]
  \\
  S 
  \ar[
    rrrrr,
    "{
      \big(
        \mathrm{get}
        ,\,
        \widetilde{\mathrm{put}}
      \big)
    }"{swap}
  ]
  \ar[
    uuuuu,
    "{
      \big(
        \mathrm{get}
        ,\,
        \widetilde{\mathrm{put}}
      \big)
    }"
  ]
  &&&&&
  V \times [V, S]
  \ar[
    uuuuu,
    "{
      V \times \Big[
        V
        ,\,
        \big(
          \mathrm{get}
          ,\,
          \widetilde{\mathrm{put}}
        \big)       
      \Big]
    }"{swap}
  ]
\end{tikzcd}

which amounts to the two conditions

\[
  \label{PutGetLaw}
  v \in V
  ,\;
  s \in S
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  get\big( put(v,s) \big)
  \,=\,
  v
\]

and

\[
  \label{PutPutLaw}
  \label{}
  v, v' \in V
  ,\,
  s \in S
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  put\big(
    v
    ,\,
    put(v', s)
  \big)
  \,=\,
  put(v,\, s)
\]

This data --- a pair of maps (eq:LensStructureMaps) satisfying the *get-put law* (eq:GetPutLaw), the *put-get law* (eq:PutGetLaw) and the *put-put law* (eq:PutPutLaw) -- is known as a *lawful [[lens in computer science]]* (see [there](#lens+in+computer+science#Lens)).

Hence, as first observed by [O’Connor 2010](#O’Connor10):

\begin{proposition}
Classical $V$-store [[comodule over a comonad|comodules]] are equivalently [[lawful lenses]] with "view" $V$.
\end{proposition}


## Related concepts

* [[quantum costate comonad]]

* [[maybe monad]],

* [[continuation monad]]

* [[state monad]]

* [[function monad]] (reader monad)



## References

### General

* {#Milewski19} [[Bartosz Milewski]] (compiled by Igal Tabachnik), §23.6 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;

* {#Uustalu21} [[Tarmo Uustalu]], slide 14 of: *Monads and Interaction Lecture 3* , lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021) &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs3.pdf), [[Uustalu-Monads3.pdf:file]]&rbrack;

### Relation to lenses

The observation that [[lenses (in computer science)]] are equivalently the [[coalgebra over a comonad|coalgebras]] of the [[costate comonad]] (cf.  *[[monads in computer science]]*) is due  to:

* {#O’Connor10} [[Russell O’Connor]], *Lenses Are Exactly the Coalgebras for the Store Comonad* (30th Nov 2010) &lbrack;[r6research:23705](https://r6research.livejournal.com/23705.html)&rbrack;

* {#O’Connor11} [[Russell O'Connor]], *Functor is to Lens as Applicative is to Biplate: Introducing Multiplate*, contribution to [ICFP '11: ACM SIGPLAN International Conference on Functional Programming](https://dl.acm.org/doi/proceedings/10.1145/2036918) (2011) &lbrack;[arXiv:1103.2841](https://arxiv.org/abs/1103.2841)&rbrack;

Early review:

* [[Jeremy Gibbons]], *[Lenses are the coalgebras for the costate comonad](https://patternsinfp.wordpress.com/2011/01/31/lenses-are-the-coalgebras-for-the-costate-comonad/)* (2011)

Further details:

* {#GibbonsJohnson12} [[Jeremy Gibbons]], [[Michael Johnson]], *Relating Algebraic and Coalgebraic Descriptions of Lenses*, Electronic Communications of the EASST **49** (2012) &lbrack;[doi:10.14279/tuj.eceasst.49.726](http://dx.doi.org/10.14279/tuj.eceasst.49.726), [pdf](http://www.cs.ox.ac.uk/jeremy.gibbons/publications/colens.pdf)&rbrack;

Further review:

* [[Bartosz Milewski]], *[Lenses, Stores, and Yoneda](https://bartoszmilewski.com/2013/10/08/lenses-stores-and-yoneda/)* (2013)

* [[Bartosz Milewski]], pp 240 in: *The Dao of Functional Programming* (2023) &lbrack;[pdf](https://github.com/BartoszMilewski/Publications/blob/master/TheDaoOfFP/DaoFP.pdf), [github](https://github.com/BartoszMilewski/Publications/tree/master/TheDaoOfFP)&rbrack;



[[!redirects store comonads]]

[[!redirects costate comonad]]
[[!redirects costate comonads]]


