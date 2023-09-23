
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

The following Def. \ref{MonadTransformer} is essentially the notion in [Liang, Hudak & Jones 1995, left column of p. 339 ](#LiangHudakJones95). 

> The key point being their condition for the respect of the bind-operation, which we state as (eq:RespectForBindOperation) below. These authors do not seem to *demand* [[natural transformation|naturality]] of the transformation (eq:UnderlyingNaturalTransformation), though their examples all are natural. On the other hand, these authors insist that $trans$ (eq:UnderlyingNaturalTransformation) is not just a transformation between a single pair of monads, but a component of what would be a [[pointed endofunctor]] on the whole category of monads... if they demanded naturality.

\begin{definition}
\label{MonadTransformer}
  Given monads $\mathcal{E}$, $\mathcal{E}'$ on the same [[category]] $\mathbf{C}$, a *monad transformer* between them is:

* a [[natural transformation]] of the [[underlying]] [[functors]]

  \[
     \label{UnderlyingNaturalTransformation}
     trans \,\colon\, \mathcal{E} \to \mathcal{E}'
  \]

which

1. preserves the return-operations, in that

   $$
     trans \circ ret^{\mathcal{E}}
     \;=\;
     ret^{\mathcal{E}'}
   $$

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
   \] 

\end{definition}

\begin{proposition}
  A natural transformation $trans \,\colon\, \mathcal{E} \to \mathcal{E}'$ is a monad transformer in the sense of Def. \ref{MonadTransformer} iff it is a [homomorphism of monads](monad#TransformationOfMonadsOnFixedCategory) (in the original sense of [Maranda 1966](monad#Maranda66)), i.e.: besides respecting the [[unit of a monad|unit/return-operation]] it also respects the join-operation (the "monad multiplication"), in that it makes the following [[commuting diagram|diagrams commute]]:

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
  \mathcal{E}\big(\mathcal{E}'(\text{-})\big)
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

$$
  bind^{\mathcal{E}} \big( f \,\colon\, D_1 \to \mathcal{E}(D_2) \big)
  \;\equiv\;
  join^{\mathcal{E}}_{D_2} \circ \mathcal{E}(f)
$$

and 

$$
  join^{\mathcal{E}}_{D}
  \;\equiv\;
  bind^{\mathcal{E}}\big( id_{\mathcal{E}(D)} \big)
  \,.
$$


Now in one direction: If the above square commutes then consider its [[pasting diagram]] with the [[naturality square]] of $trans$ as follows

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

Going diagonally through this [[commuting diagram]]: The total left and bottom composite is the left hand side of (eq:RespectForBindOperation) and the total top and right composite is the right hand side of (eq:RespectForBindOperation), thus proving their equality.

In the other direction, if (eq:RespectForBindOperation) holds then its restriction to the case $prog_{12} \,\equiv\, id \,\equiv\, prog_{23}$ yields the above commtuting diagram.
\end{proof}


## Related concepts

* [[monad transformation]]

## References

Original discussion:

* {#Espinosa94} [[David A. Espinosa]], §3.2 in: *Building Interpreters by Transforming Stratified Monads* (1994) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-StratifiedMonads.pdf:file]]&rbrack;

* {#Espinosa95} [[David A. Espinosa]], §2.6 in: *Semantic Lego*, PhD thesis, Columbia University (1995) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-SemanticLego.pdf:file]], slides:[pdf](https://github.com/davidespinosa01/papers/blob/346c2ded6af78805701106d51daee8f7a756c948/E/Espinosa%20David/espinosa-thesis-slides.pdf), [[Espinosa-SemanticLego-slides.pdf:file]]&rbrack;

* {#LiangHudakJones95} Sheng Liang, [[Paul Hudak]], [[Mark Jones]], *Monad transformers and modular interpreters*, POPL '95 (1995) 333–343 &lbrack;[doi:10.1145/199448.199528](https://doi.org/10.1145/199448.199528)&rbrack;


Textbook account:

* {#Winitzki22} [[Sergei Winitzki]], Section 14 of: *The Science of Functional Programming -- A tutorial, with examples in Scala* (2022) &lbrack;[leanpub:sofp](https://leanpub.com/sofp), [github:sofp](https://github.com/winitzki/sofp)&rbrack;

See also:

* Wikipedia, *[Monad transformer](https://en.wikipedia.org/wiki/Monad_transformer)*

* Haskell, *[Monad transformers](https://en.wikibooks.org/wiki/Haskell/Monad_transformers)*

* Bryan O'Sullivan, Don Stewart, and John Goerzen, _Monad transformers_, [Chapter 18](http://book.realworldhaskell.org/read/monad-transformers.html) of *Real World Haskell*

* [[Mauro Jaskelioff]], [[Eugenio Moggi]], *Monad Transformers as Monoid Transformers*, Theoretical Computer Science **411** 51–52 (2010) 4441-4466 &lbrack;[doi:10.1016/j.tcs.2010.09.011](https://doi.org/10.1016/j.tcs.2010.09.011), [pdf](http://www.disi.unige.it/person/MoggiE/ftp/tcs10.pdf)&rbrack;

* {#HP07} [[Martin Hyland]], [[John Power]], _The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads_, Electronic Notes in Theoretical Computer Science (ENTCS) **172** (2007) 437-458  &lbrack;[pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf)&rbrack;

* Oleksandr Manzyuk, _Calculating monad transformers with category theory_ (2012) &lbrack;[pdf](https://oleksandrmanzyuk.files.wordpress.com/2012/02/calc-mts-with-cat-th1.pdf)&rbrack;


* [[Maciej Piróg]], *Eilenberg--Moore Monoids and Backtracking Monad Transformers*, EPTCS **207** (2016) 23-56 &lbrack;[ar](https://arxiv.org/abs/1604.01184), [doi:10.4204/EPTCS.207.2](https://doi.org/10.4204/EPTCS.207.2)&rbrack

* Chung-Chieh Shan, _Monad transformers_ (2020) &lbrack;[blog post](http://conway.rutgers.edu/~ccshan/wiki/blog/posts/Monad_transformers/)&rbrack;


[[!redirects monad transformers]]

