

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

The concept of enriched monads is key for the application of [[monads in computer science]], since a [[monad]] coded verbatim in a [[functional programming language]] --- where [[function types]] $X \to Y$ are to be [[categorical semantics|interpreted]] not as external [[hom-sets]] but as [[internal homs]] in the ambient [[closed monoidal category]] $V$ of [[data types]] --- is really a $V$-enriched monad (hence typicall a [[strong monad]]).


## Definition

Let 

* $(V, \otimes, I)$ be a [[symmetric monoidal category]] which serves as the [[base of enrichment]], 

  with $I$ denoting its [[unit object]].

* $\mathbf{C}$ be a $V$-[[enriched category]] 

  with [[underlying]] [[Set]]-category denoted $C$, and

  with [[hom-objects]] between any pais of [[objects]] $X, Y$ denoted $\mathbf{C}(X,Y) \,\in\, V$.

\begin{definition}
A *$V$-enriched monad* on $\mathbf{C}$ is, in [[Kleisli triple]]-presentation:

* for every object $X \,\in\, \mathbf{C}$, an object $T(X) \,\in\,\mathbf{C}$;

* for every object $X \,\in\,\mathbf{C}$, a morphism in $V$ of the form

  $$
   \eta_X 
     \;\colon\; 
    I \to \mathbf{C}\big(X,T(X)\big)
  $$ 

  (the *[[monad unit]]*)

* for all [[pairs]] of objects $X,Y$ of $mathbf{C}$, a morphism  in $V$ of the form

  $$
    (\text{-})^\ast 
      \;\colon\; 
    \mathbf{C}\big(X,T(Y)\big) 
      \to 
    \mathbf{C}\big(T(X),T(Y)\big)
  $$

  (the *[[Kleisli extension]]* or *bind*-operation)

such that for all morphisms $f \colon X \to T(Y)$ and $g \colon Y \to T(Z)$ in $C$ the following holds:

1. $f^\ast \circ \eta_X = f$,

1. $\big(\eta_X\big)^\ast = id$

1. $g^\ast \circ f^\ast = (g^\ast \circ f)^\ast$. 

\end{definition}

## Properties

### Relation to strong monads

\begin{remark}
If $C$ is $V$-enriched with [[copowers]], e.g. if $V=C$, then $V$ acts on $C$. In this circumstance, a $V$-enriched monad on $C$ is the same thing as a $V$-[[strong monad]] on $C$. 
\end{remark}

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

* [[Max Kelly]], [[John Power]], *Adjunctions whose counits are coequalizers and presentations of finitary enriched monads*, Journal of Pure and Applied Algebra **89** (1993) &lbrack;<a href="https://doi.org/10.1016/0022-4049(93)90092-8">doi:10.1016/0022-4049(93)90092-8</a>&rbrack;

* [[John Power]], *Enriched Lawvere theories*, Theory and Applications of Categories **6** 7 (1999) 83-93 &lbrack;[tac:6-07](http://www.tac.mta.ca/tac/volumes/6/n7/6-07abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/6/n7/n7.pdf)&rbrack;

* [[Eduardo Dubuc]], *Kan Extensions in Enriched Category Theory*, Lecture Notes in Mathematics **145**, Springer (1970) &lbrack;[doi:10.1007/BFb0060485](https://doi.org/10.1007/BFb0060485)&rbrack;


[[!redirects enriched monads]]
