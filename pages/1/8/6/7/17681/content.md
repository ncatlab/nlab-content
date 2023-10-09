
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

In [[functional programming]] using [[monads (in computer science)|monads for computational effects]], *monad transformers* &lbrack;[Espinosa 1994 §4](#Espinosa94), [1995 §2.6](#Espinosa95)&rbrack; are type constructors which take one monad to another in a compatible way.


In practice this is typically motivated by and used for *combining* a monadic effect $\mathcal{E}_{new}$ into any given one $\mathcal{E}$ by $\mathcal{E} \mapsto \mathcal{E}_{new} \circ \mathcal{E} $ via a universal [[distributive law]].

Formally, a monad transformer on a given category $\mathbf{C}$ (of [[data types|data]] [[types]]) is a [[pointed endofunctor]] on the [category of monads](monad#TransformationOfMonadsOnFixedCategory) $Mnd(\mathbf{C})$ (this is made explicit in [Winitzki 2022, p. 474](#Winitzki22)), namely:

1. an [[endofunctor]] $\mathcal{E} \mapsto \mathcal{E}'$ taking monads to monads

1. for each $\mathcal{E}$ a [morphism of monads](monad#TransformationOfMonadsOnFixedCategory) $trans_{\mathcal{E}} \,\colon\, \mathcal{E} \longrightarrow \mathcal{E}'$ (a *[[monad transformation]]*)

1. such that these are [[natural transformations|natural]] with respect to [morphism of monads](monad#TransformationOfMonadsOnFixedCategory).

This construction is sometimes viewed (see [HP07](#HP07), and at *[[Eff]]*) as a complication resulting from passing to monads from the setting of [[Lawvere theories]], where any two theories may be naturally combined.


## Details
 {#Details}

The following Def. \ref{MonadTransformer} is essentially the notion in [Liang, Hudak & Jones 1995, left column of p. 339 ](#LiangHudakJones95), as now commonly used in [[Haskell]] (see the *[Haskell Transformer class](https://hackage.haskell.org/package/transformers-0.5.6.2/docs/Control-Monad-Trans-Class.html#g:1)*).

\begin{remark}
\label{PointedEndofunctorConditionOrNot}
These authors, and the [[functional programming]]/[[Haskell]]-community following them, insist that "$trans_{(\text{-})}$" (eq:UnderlyingNaturalTransformation) --- which they denote "$lift \text{-}$" ---  is not just a transformation between a single pair of monads, but a component a [[pointed endofunctor]] on the whole category of monads. This further condition may be considered (or not) in addition to the following discussion.
\end{remark}

\begin{definition}
\label{MonadTransformer}
  Given monads $\mathcal{E}$, $\mathcal{E}'$ on the same [[category]] $\mathbf{C}$, a *monad transformer* between them is:

* a system of [[morphisms]]

  \[
     \label{UnderlyingNaturalTransformation}
     D \,\colon\, Type
     \;\;\;\;\;\;
     \vdash
     \;\;\;\;\;\;
     trans_D 
       \,\colon\, 
     \mathcal{E}(D) \to \mathcal{E}'(D)
  \]

which

1. preserves the return-operations, in that

   \[
     \label{RespectForReturnOperation}
     trans \circ ret^{\mathcal{E}}
     \;=\;
     ret^{\mathcal{E}'}
     \,,
   \]

1. preserves the bind-operations, in that for
   $prog_{12}\,\colon\, D_1 \to \mathcal{E}(D_2)$
   and
   $prog_{23}\,\colon\, D_2 \to \mathcal{E}(D_3)$
   
   we have

   \[
     \label{RespectForBindOperation}
     trans_{D_3}
     \circ
     \Big(
       \big( bind^{\mathcal{E}} prog_{23} \big)
       \circ
       prog_{12}
     \Big)
     \;\;=\;\;
     bind^{\mathcal{E}'}
     \Big(
       \big(
         trans_{D_3} \circ prog_{23}
       \big)
     \Big)
     \circ
     \big(
       trans_{D_2} \circ prog_{12}
     \big)
     \mathrlap{\,.}
   \] 

\end{definition}

In [Schrijvers, Piróg, Wu & Jaskelioff 2019 p. 99](#SchrijversPirógWuJaskelioff19) the analogous condition is stated in terms of the join-operation. We may check that these are equivalent:

\begin{proposition}
\label{EquivalenceOfDefinitions}
  A system of transformations $trans_D \,\colon\, \mathcal{E}(D) \to \mathcal{E}'(D)$ is a monad transformer in the sense of Def. \ref{MonadTransformer} (cf. Rem. \ref{PointedEndofunctorConditionOrNot}) iff it is a [homomorphism of monads](monad#TransformationOfMonadsOnFixedCategory) (in the original sense of [Maranda 1966](monad#Maranda66)), i.e.: 

1. a [[natural transformation]] $\trans \,\colon\, \mathcal{E} \to \mathcal{E}'$ of the [[underlying]] [[functors]],

1. respecting the [[unit of a monad|unit/return-operation]], in that the following [[commuting diagram|diagrams commute]]:

   \[
     \label{RespectForTheUnit}
     \array{
       D 
         &\overset{ret^{\mathcal{E}}_D}{\longrightarrow}&
       \mathcal{E}(D)
       \\
       \mathllap{{}^{id}}\Big\downarrow 
         && 
       \Big\downarrow\mathrlap{{}^{trans_D}}
       \\
       D 
         &\underset{ret^{\mathcal{E}'}_D}{\longrightarrow}&
       \mathcal{E}'(D)
     }
   \]

1. respecting the join-operation (the "monad multiplication"), in that it makes the following [[commuting diagram|diagram commute]]:

\begin{tikzcd}[sep=large]
  \mathcal{E}\big(\mathcal{E}(\mbox{-})\big)
  \ar[
     rr,
     "{
       \mathrm{trans}_{{}_{\mathcal{E}(\mbox{-})}}
     }"{description}
  ]
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}}_{(\mbox{-})}
    }"{description}
  ]
  &&
  \mathcal{E}'\big(\mathcal{E}(\text{-})\big)
  \ar[
    rr,
    "{
      \mathcal{E}'(\mathrm{trans}_{(\mbox{-})})
    }"{description}
  ]
  &&
  \mathcal{E}'\big(\mathcal{E}'(\text{-})\big)
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}'}_{(\mbox{-})}
    }"{description}
  ]
  \\
  \\
  \mathcal{E}(\mbox{-})
  \ar[
    rrrr,
    "{ 
       \mathrm{trans}_{(\mbox{-})} 
    }"{description}
  ]
  &&&&
  \mathcal{E}'(\mbox{-})
\end{tikzcd}

\end{proposition}
\begin{proof}
Recall that the relation between the bind- and join-operations is:

\[
  \label{BindFromJoin}
  bind^{\mathcal{E}} \big( f \,\colon\, D_1 \to \mathcal{E}(D_2) \big)
  \;\equiv\;
  join^{\mathcal{E}}_{D_2} \circ \mathcal{E}(f)
\]

and 

\[
  \label{FunctorFromBind}
 \mathcal{E}(f \,\colon\, D_1 \to D_2)
 \;\equiv\;
 bind^{\mathcal{E}}
 \big(
   D_1 
     \xrightarrow{\; f \;} 
   D_2
     \xrightarrow{\; ret^{\mathcal{E}}_{D_2} \;}
   \mathcal{E}(D_2)
 \big) 
\]

\[
  \label{JoinFromBind}
  join^{\mathcal{E}}_{D}
  \;\equiv\;
  bind^{\mathcal{E}}\big( id_{\mathcal{E}(D)} \big)
  \,.
\]


Now in one direction: 
Given a [morphism of monads](monad#TransformationOfMonadsOnFixedCategory) $trans \,\colon\, \mathcal{E} \to \mathcal{E}'$,
then consider the [[pasting diagram]] of the above square with the [[naturality square]] of $trans$ as follows:

\begin{tikzcd}[sep=large]
  D_1
  \ar[
    rr,
    "{ 
      \mathrm{prog}_{12} 
    }"{description}
  ]
  &&
  \mathcal{E}(D_2)
  \ar[
     rr,
     "{
       \mathrm{trans}_{D_2}
     }"{description}
  ]
  \ar[
    dd,
    "{
      \mathcal{E}(\mathrm{prog}_{23})
    }"{description}
  ]
  &&
  \mathcal{E}'(D_2)
  \ar[
    dd,
    "{
      \mathcal{E}'(\mathrm{prog}_{23})
    }"{description}
  ]
  \\
  \\
  &&
  \mathcal{E}\big(\mathcal{E}(D_3)\big)
  \ar[
     rr,
     "{
       \mathrm{trans}_{{}_{\mathcal{E}(D_3)}}
     }"{description}
  ]
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}}_{D_3}
    }"{description}
  ]
  &&
  \mathcal{E}'\big(\mathcal{E}(D_3)\big)
  \ar[
    rr,
    "{
      \mathcal{E}'(\mathrm{trans}_{D_3})
    }"{description}
  ]
  &&
  \mathcal{E}'\big(\mathcal{E}'(D_3)\big)
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}'}_{D_3}
    }"{description}
  ]
  \\
  \\
  &&
  \mathcal{E}(D_3)
  \ar[
    rrrr,
    "{ 
       \mathrm{trans}_{D_3} 
    }"{description}
  ]
  &&&&
  \mathcal{E}'(D_3)
\end{tikzcd}

Going diagonally through this [[commuting diagram]] and using (eq:BindFromJoin): The total left and bottom composite is the left hand side of (eq:RespectForBindOperation) and the total top and right composite is the right hand side of (eq:RespectForBindOperation), thus proving their equality.

In the other direction, if (eq:RespectForBindOperation) holds then its restriction to the case $prog_{12} \,\equiv\, id \,\equiv\, prog_{23}$ immediately yields, by (eq:JoinFromBind), the above commtuting diagram expressing respect for the join.

{#NaturalityFollows} It just remains to see that the system of transformations $trans_{(\text{-})}$ (eq:UnderlyingNaturalTransformation) is necessarily [[natural transformation|natural]]. This is shown by the following sequence of equalities, for $prog \,\colon\, D_1 \to D_2$:


$$
  \begin{array}{ll}
    trans_{D_2}  \circ \mathcal{E}(prog)
    \\
    \;=\;
    trans_{D_2}
    \circ
    bind^{\mathcal{E}}\big(
      D_1 
        \xrightarrow{ prog } 
      D_2
        \xrightarrow{ ret^{\mathcal{E}}_D }
      \mathcal{E}(D_2)
    \big)
    \\
    \;=\;
    bind^{\mathcal{E}'}\big(
      D_1 
        \xrightarrow{ prog } 
      D_2
        \xrightarrow{ ret^{\mathcal{E}}_D }
      \mathcal{E}(D_2)
        \xrightarrow{ trans_{D_2} }
      \mathcal{E}'(D_2)
    \big)
    \circ
    trans_{D_1}
    \\
    \;=\;
    bind^{\mathcal{E}'}\big(
      D_1 
        \xrightarrow{ prog } 
      D_2
        \xrightarrow{ ret^{\mathcal{E}'}_D }
      \mathcal{E}'(D_2)
    \big)
    \circ
    trans_{D_1}
    \\
    \;=\;
    \mathcal{E}'(prog)
    \circ
    trans_{D_1}
    \mathrlap{\,,}
  \end{array}
$$

where we used, in order of appearance: (eq:FunctorFromBind), (eq:RespectForBindOperation), (eq:RespectForTheUnit) and finally (eq:FunctorFromBind) again.
\end{proof}

\begin{remark}
\label{MonadTransformationsActCovariantlyOnKleisliCategories}
**(monad transformations act covariantly on Kleisli categories)**
\linebreak
  The conditions (eq:RespectForReturnOperation) and (eq:RespectForBindOperation) equivalently say that the monad transformation $trans$ (eq:UnderlyingNaturalTransformation) induces a functor between the respective [[Kleisli categories]]

  \begin{tikzcd}[
    row sep=2pt
  ]
    &
    \mathbf{C}
    \ar[
      dl, 
      end anchor={[yshift=2pt]},
      "{ F_{\mathcal{E}} }"{swap}
    ]
    \ar[
      dr, 
      end anchor={[yshift=4pt]},
      "{ F_{\mathcal{E}'} }"
    ]
    \\
    \mathbf{C}_{\mathcal{E}}
    \ar[
      rr
    ]
    &&
    \mathbf{C}_{\mathcal{E}'}
    \\
    \mathcal{E}(D_1)
    \xrightarrow{ \phi }
    \mathcal{E}(D_2)
    &\mapsto&
    \mathrm{bind}
      ^{ \mathcal{E}' }
    \bigg(
    D_1
    \xrightarrow{
      \mathrm{ret}
        ^{ \mathcal{E} }
        _{ D_1 }
    }
    \mathcal{E}(D_1)
    \xrightarrow{ \phi }
    \mathcal{E}(D_2)
    \xrightarrow{
      \mathrm{trans}
        _{ D_2 }
    }
    \mathcal{E}'(D_2)
    \bigg)
    \,.
  \end{tikzcd}

As shown, this respects the [free-module](algebra+over+a+monad#FreeAlgebras) functors 

\begin{tikzcd}[
  row sep=5, column sep=10
]
  \mathbf{C}
  \ar[rr, "{ F_{\mathcal{E}} }"]
  &&
  \mathbf{C}_{\mathcal{E}}
  \\
  D_1 \xrightarrow{f} D_2
  &\mapsto&
  \mathcal{E}(D_1) \xrightarrow{ \mathcal{E}(f) } 
  \mathcal{E}(D_2)
\end{tikzcd}

because the following [[commuting diagram|diagram commutes]]:

\begin{tikzcd}[sep=20pt]
    D_1
    \ar[
      rr,
      "{
        \mathrm{ret}
          ^{ \mathcal{E} }
          _{ D_1 }
      }"
    ]
    \ar[dd, equals]
    &&
    \mathcal{E}(D_1)
    \ar[
      rr,
      "{ \mathcal{E}(f) }"
    ]
    \ar[
      dd,
      "{ \mathrm{trans}_{D_1} }"{description}
    ]
    &&
    \mathcal{E}(D_2)
    \ar[
      dd,
      "{
        \mathrm{trans}
          _{ D_2 }
      }"{description}
    ]
    \\
    \\
    D_1
    \ar[
      rr,
      "{
        \mathrm{ret}
          ^{ \mathcal{E}' }
          _{ D_1 }
      }"
    ]
    &&
    \mathcal{E}'(D_1)
    \ar[
      rr,
      "{ \mathcal{E}'(f) }"
    ]
    &&
    \mathcal{E}'(D_2)
\end{tikzcd}

Since it is evident that composite monad transformations give composite such functors, this means that assigning [[Kleisli categories]] to [[monads]] on $\mathbf{C}$ extends to a [[functor]] of the form:

\begin{tikzcd}[sep=0pt]
  \mathrm{Mnd}(\mathbf{C})
  \ar[
     rr
  ]
  &&
  \mathrm{Cat}^{\mathbf{C}/}
  \\
  \mathcal{E} &\mapsto& \mathbf{C}_{\mathcal{E}}
\end{tikzcd}

This is probably the functor alluded to in [Linton 1969, Lem. 10.2](#Linton69). 
\end{remark}

## Related concepts

* [[monad transformation]]

## References

Original discussion:

* {#Espinosa94} [[David A. Espinosa]], §3.2 in: *Building Interpreters by Transforming Stratified Monads* (1994) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-StratifiedMonads.pdf:file]]&rbrack;

* {#Espinosa95} [[David A. Espinosa]], §2.6 in: *Semantic Lego*, PhD thesis, Columbia University (1995) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-SemanticLego.pdf:file]], slides:[pdf](https://github.com/davidespinosa01/papers/blob/346c2ded6af78805701106d51daee8f7a756c948/E/Espinosa%20David/espinosa-thesis-slides.pdf), [[Espinosa-SemanticLego-slides.pdf:file]]&rbrack;

* {#LiangHudakJones95} Sheng Liang, [[Paul Hudak]], [[Mark Jones]], *Monad transformers and modular interpreters*, POPL '95 (1995) 333–343 &lbrack;[doi:10.1145/199448.199528](https://doi.org/10.1145/199448.199528)&rbrack;

* {#SchrijversPirógWuJaskelioff19} Tom Schrijvers, Maciej Piróg, Nicolas Wu, Mauro Jaskelioff: *Monad transformers and modular algebraic effects: what binds them together*, in: *Haskell 2019: Proceedings of the 12th ACM SIGPLAN International Symposium on Haskell* (2019) 98–113 &lbrack;[doi:10.1145/3331545.3342595](https://doi.org/10.1145/3331545.3342595)&rbrack;


Textbook account:

* {#Winitzki22} [[Sergei Winitzki]], Section 14 of: *The Science of Functional Programming -- A tutorial, with examples in Scala* (2022) &lbrack;[leanpub:sofp](https://leanpub.com/sofp), [github:sofp](https://github.com/winitzki/sofp)&rbrack;

See also:

* Wikipedia, *[Monad transformer](https://en.wikipedia.org/wiki/Monad_transformer)*

* Haskell, *[Monad transformers](https://en.wikibooks.org/wiki/Haskell/Monad_transformers)*

* [hackage.haskell.org/package/transformers-0.5.6.2/docs/Control-Monad-Trans-Class.html](https://hackage.haskell.org/package/transformers-0.5.6.2/docs/Control-Monad-Trans-Class.html)

* Bryan O'Sullivan, Don Stewart, and John Goerzen, _Monad transformers_, [Chapter 18](http://book.realworldhaskell.org/read/monad-transformers.html) of *Real World Haskell*

* [[Mauro Jaskelioff]], [[Eugenio Moggi]], *Monad Transformers as Monoid Transformers*, Theoretical Computer Science **411** 51–52 (2010) 4441-4466 &lbrack;[doi:10.1016/j.tcs.2010.09.011](https://doi.org/10.1016/j.tcs.2010.09.011), [pdf](http://www.disi.unige.it/person/MoggiE/ftp/tcs10.pdf)&rbrack;

* {#HP07} [[Martin Hyland]], [[John Power]], _The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads_, Electronic Notes in Theoretical Computer Science (ENTCS) **172** (2007) 437-458  &lbrack;[pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf)&rbrack;

* Mauro Jaskelioff, *Monatron: An Extensible Monad Transformer Library*, in: *Implementation and Application of Functional Languages. IFL 2008*, Lecture Notes in Computer Science **5836** (2011) 233–248 &lbrack;[doi:10.1007/978-3-642-24452-0_13](https://doi.org/10.1007/978-3-642-24452-0_13)&rbrack;
     

* Oleksandr Manzyuk, _Calculating monad transformers with category theory_ (2012) &lbrack;[pdf](https://oleksandrmanzyuk.files.wordpress.com/2012/02/calc-mts-with-cat-th1.pdf)&rbrack;


* [[Maciej Piróg]], *Eilenberg--Moore Monoids and Backtracking Monad Transformers*, EPTCS **207** (2016) 23-56 &lbrack;[ar](https://arxiv.org/abs/1604.01184), [doi:10.4204/EPTCS.207.2](https://doi.org/10.4204/EPTCS.207.2)&rbrack

* Chung-Chieh Shan, _Monad transformers_ (2020) &lbrack;[blog post](http://conway.rutgers.edu/~ccshan/wiki/blog/posts/Monad_transformers/)&rbrack;


[[!redirects monad transformers]]

