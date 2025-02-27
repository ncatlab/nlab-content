

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of *enriched monads* is that of *[[monads]]* in the context of [[enriched category theory]]: For $V$ a [[base of enrichment]], a $V$-enriched monad is a [[monad]] [[internalization|internal]] to the [[2-category]] [[VCat]] of $V$-[[enriched categories]]. 

Generally (except in the base case $V = $ [[Set]]) the [[structure]] of a $V$-enriched monad on a $V$-[[enriched category]] $\mathbf{C}$ is *stronger* than that of the [[underlying]] monad on the underlying [[Set]]-category $C$, whence one also speaks of *[[strong monads]]* (*a priori* a different notion, which however coincides with that of enriched monads under mild conditions, such as when $V$ is [[closed monoidal category|closed]], see [there](strong+monad#LeftStrongMonadsAreEnrichedMonads)).

The concept of enriched monads is key for the application of [[monads in computer science]], since a [[monad]] coded verbatim in a [[functional programming language]] --- where [[function types]] $X \to Y$ are to be [[categorical semantics|interpreted]] not as external [[hom-sets]] but as [[internal homs]] in the ambient [[closed monoidal category]] $V$ of [[data types]] --- is really a $V$-enriched monad (hence typically a [[strong monad]]).


## Definition

Let 

* $(V, \otimes, I)$ be a [[symmetric monoidal category]] which serves as the [[base of enrichment]], 

  with $I$ denoting its [[unit object]].

* $\mathbf{C}$ be a $V$-[[enriched category]] 

  with [[underlying]] [[Set]]-category denoted $C$, and

  with [[hom-objects]] between any pais of [[objects]] $X, Y$ denoted $\mathbf{C}(X,Y) \,\in\, V$.

\begin{definition}
A *$V$-enriched monad* on $\mathbf{C}$ is, in [[Kleisli triple]]-presentation (eg. [McDermott & Uustalu 2022, Def. 5.8](#McDermottUustalu22)):

* for every object $X \,\in\, \mathbf{C}$, an object $T(X) \,\in\,\mathbf{C}$;

* for every object $X \,\in\,\mathbf{C}$, a morphism in $V$ of the form

  $$
   ret_X 
     \;\colon\; 
    I \to \mathbf{C}\big(X,T(X)\big)
  $$ 

  (the *[[monad unit]]*)

* for all [[pairs]] of objects $X,Y$ of $mathbf{C}$, a morphism  in $V$ of the form

  $$
    bind_{X,Y}
      \;\colon\; 
    \mathbf{C}\big(X,T(Y)\big) 
      \to 
    \mathbf{C}\big(T(X),T(Y)\big)
  $$

  (the *[[Kleisli extension]]* or *bind*-operation)

such that the structural equations on a [[Kleisli triple]]

1. $bind(f) \circ ret_X = f$,

1. $bind(ret_X\big) = id$

1. $bind(g) \circ bind(f) = bind\big(bind(g) \circ f\big)$

hold for [[generalized elements]] $f$, $g$ of the [[hom-objects]] $\mathbf{C}\big(X,\,T(Y)\big)$, $\mathbf{C}\big(Y,\,T(Z)\big)$, which means that the following [[commuting diagram|diagrams commute]] in $V$ for all objects $X, Y, Z$ of $\mathbf{C}$:

\begin{tikzcd}[column sep=60pt]
  &
  \mathbf{C}\big(T(X),\, T(Y)\big)
  \ar[
    dr,
    "{
      \mathbf{C}\big(
        \mathrm{ret}_X
        ,\,
        T(Y)
     \big)
    }"{sloped}
  ]
  \\
  \mathbf{C}\big(
    X
    ,\,
    T(Y)
  \big)
  \ar[
    ur,
    "{
      \mathrm{bind}_{X,Y}
    }"{sloped}
  ]
  \ar[
    rr,
    equals
  ]
  &&
  \mathbf{C}\big(
    X
    ,\,
    T(Y)
  \big)  
\end{tikzcd}

\begin{tikzcd}[column sep=60pt]
  &
  \mathbf{C}\big(
    X
    ,\,
    T(X)
  \big)
  \ar[
    dr,
    "{
      \mathrm{bind}_{X,X}
    }"{sloped}
  ]
  \\
  I
  \ar[
    ur,
    "{
      \mathrm{ret}_X
    }"{sloped}
  ]
  \ar[
    rr,
    "{ 
      \mathrm{id}_{T(X)} 
    }"{swap}
  ]
  &&
  \mathbf{C}\big(
    T(X)
    ,\,
    T(Y)
  \big)  
\end{tikzcd}

\begin{tikzcd}[sep=60pt]
  \mathbf{C}\big(
    Y
    ,\,
    T(Z)
  \big)
  \otimes
  \mathbf{C}\big(
    X
    ,\,
    T(Y)
  \big)
  \ar[
    rr,
    "{
      \mathrm{bind}_{Y,Z}
      \otimes
      \mathrm{Id}
    }"
  ]
  \ar[
    dd,
    "{
      \mathrm{bind}_{Y,Z}
      \,\otimes\,
      \mathrm{bind}_{X,Y}
    }"{description}
  ]
  &&
  \mathbf{C}\big(
    T(Y)
    ,\,
    T(Z)
  \big)
  \otimes
  \mathbf{C}\big(
    X
    ,\,
    T(Y)
  \big)
  \ar[
    d,
    "{
      \circ_{{}_{X, T(Y), T(Z)}}
    }"
  ]
  \\
  &&
  \mathbf{C}\big(
    X
    ,\,
    T(Z)
  \big)  
  \ar[
    d,
    "{
      \mathrm{bind}_{X,Z}
    }"
  ]
  \\
  \mathbf{C}\big(
    T(Y)
    ,\,
    T(Z)
  \big)    
  \otimes
  \mathbf{C}\big(
    T(X)
    ,\,
    T(Y)
  \big)    
  \ar[
    rr,
    "{
      \circ_{{}_{T(X), T(Y), T(Z)}}
    }"{swap}
  ]
  &&
  \mathbf{C}\big(
    T(X)
    ,\,
    T(Z)
  \big)  
\end{tikzcd}


\end{definition}

## Properties


### Relation to strong and monoidal monads
 {#RelationToStrongMonads}

\begin{proposition}
\label{EquivalenceBetweenStrengthAndEnrichment}
**(equivalence between $V$-strength and $V$-enrichment)**
For 

* $V$ a [[closed monoidal category]]

* $\mathbf{C}$, $\mathbf{D}$ a [[pair]] of $V$-[[enriched categories]]

  which are also $V$-[[tensoring|tensored]] (=[[copower|copowered]]) 

then there is a [[bijection]] between the [[structures]] of

* $V$-[[strong functors]] and $V$-[[enriched functors]] $\mathbf{C} \to \mathbf{D}$

on the [[underlying]] [[functors]],

and for any pair $F$, $G$ of such a [[bijection]] between

* $V$-[[strong natural transformations]] and $V$-[[enriched natural transformation]] $F \to G$

It follows in particular that there is a [[bijection]] between

* $V$-[[strong monads]] and $V$-[[enriched monads]]

on such $\mathbf{C}$.
\end{proposition}
([Ratkovic 2012, §3.2](#Ratkovic12); [McDermott & Uustalu 2022, Prop. 5.4, 5.8](#McDermottUustalu22))

\begin{remark}
  For $V$ a [[closed monoidal category]] the further assumptions in Prop. \ref{EquivalenceBetweenStrengthAndEnrichment} apply to $\mathbf{C} = \mathbf{D} \coloneqq \mathbf{V}$ being the canonical self-enrichment of $V$.
\end{remark}

Moreover:

\begin{proposition}
\label{RelationBetweenCommutativeStrongMonadsAndSymmetricMonoidalMonads}
For $V$ a [[symmetric monoidal closed category]], there is a [[bijection]] between the [[structures]] of

* [[commutative monad|commutative]]$\;$[[strong monads]] and [[symmetric monoidal functor|symmetric]] [[monoidal monads]]

on [[underlying]] [[monads]] on $V$.

\end{proposition}
([Kock 1972, Thm. 3.2](monoidal+monad#Kock72), review in [GLLN08, §7.3, §A.4](monoidal+monad#GLLN08), [Ratkovic 2012, Prop. 3.3.9](#Ratkovic12))

Hence from combining Prop. \ref{EquivalenceBetweenStrengthAndEnrichment} with Prop. \ref{RelationBetweenCommutativeStrongMonadsAndSymmetricMonoidalMonads} we get:
\begin{prop}
For $V$ a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with $\mathbf{V}$ denoting its self-[[enriched category]], every [[symmetric monoidal functor|symmetric]] [[monoidal monad]] on $V$ gives the [[structure]] of a $V$-[[enriched monad]] on $\mathbf{V}$.
\end{prop}

## Examples

\begin{example}
In the case in of enrichment by [[truth values]], a monad is a [[closure operator]] on a [[poset]].
\end{example}

\begin{remark}
In the application of [[monads in computer science]], $\mathbf{C} = \mathbf{V}$ is typically the [[base of enrichment]] itself, canonically enriched over itself. 
For classical computing this is typically a [[cartesian closed category]].

Since declaring a monad in a [[functional programming language]] means to define it in the [[internal language]] of $V$, such [[monads in computer science]] are actually enriched, see the discussion [there](monad+in+computer+science#RefinedIdea).

For example, if $V$ is the [[syntactic category]] of a [[programming language]], then all the definable monads in the language are $V$-enriched.
\end{remark}



## Related entries

* [[strong monad]]

* [[monoidal monad]]

* [[additive monad]]

* [[monad (in computer science)]]

* [[tensorial strength]]

* [[enriched adjunction]]

* [[enriched Lawvere theory]]

## References 

* {#Ratkovic12} [[Kruna S. Ratkovic]], *Strength and Enrichment*, Section 3.2 of: *Morita theory in enriched context* (2012) &lbrack;[arXiv:1302.2774](https://arxiv.org/abs/1302.2774), [hal:tel-00785301](https://theses.hal.science/tel-00785301/document)&rbrack;
 
* {#McDermottUustalu22} [[Dylan McDermott]], [[Tarmo Uustalu]], Def. 5.6 in: *What Makes a Strong Monad?*, EPTCS **360** (2022) 113-133 &lbrack;[arXiv:2207.00851](https://arxiv.org/abs/2207.00851), [doi:10.4204/EPTCS.360.6](https://doi.org/10.4204/EPTCS.360.6)&rbrack;


See also:

* [[Max Kelly]], [[John Power]], *Adjunctions whose counits are coequalizers and presentations of finitary enriched monads*, Journal of Pure and Applied Algebra **89** (1993) &lbrack;<a href="https://doi.org/10.1016/0022-4049(93)90092-8">doi:10.1016/0022-4049(93)90092-8</a>&rbrack;

* [[John Power]], *Enriched Lawvere theories*, Theory and Applications of Categories **6** 7 (1999) 83-93 &lbrack;[tac:6-07](http://www.tac.mta.ca/tac/volumes/6/n7/6-07abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/6/n7/n7.pdf)&rbrack;

* [[Eduardo Dubuc]], *Kan Extensions in Enriched Category Theory*, Lecture Notes in Mathematics **145**, Springer (1970) &lbrack;[doi:10.1007/BFb0060485](https://doi.org/10.1007/BFb0060485)&rbrack;


[[!redirects enriched monads]]
