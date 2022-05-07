
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **finite limit** is a [[limit]] over a finite [[diagram]] - that is, one whose shape is a [[finite category]].

More generally, in [[higher category theory]], a finite limit is a [[limit]] of a diagram that is a finite [[(n,r)-category]].

A [[category]] that has all finite limits is called a *[[finitely complete category]]* or a (finitary) *[[essentially algebraic theory]]*.

A [[functor]] that [[preserved limit|preserves]] all finite limits is called *[[left exact functor]]*, a *lex functor*, a *cartesian functor*, or a *finitely continuous functor*.   

The [[2-category]] of [[finitely complete categories]], [[left exact functors]] and [[natural transformations]] is often denoted *[[Lex]]*.

## Examples
  {#Examples}
 
\begin{example}
  A [[product]] is a finite limit iff it is a [[finite product]], hence if its factors are [[indexed set|indexed]] by a [[finite set]]. 

In particular, [[binary products]] are finite limits and the [[terminal object]] (being the [[limit]] over the [[empty diagram]]) is a finite limit.
\end{example}

\begin{example}
  Other common finite limits are [[pullbacks]] and [[equalizers]].
\end{example}

\begin{example}
  The [[fixed locus]] of a [[group action]] is a finite limit if the group in question is a [[finite group]].
\end{example}

\begin{example}
  The [[functor]] of [[geometric realization]] of [[simplicial sets]]
  into [[compactly generated topological spaces]]
  [[preserved limit|preserves]] finite limits (is a [[left exact functor]]), see [there](geometric+realization#GeometricRealizationIsLeftExact).

More generally, the [[functor]] of  [[geometric realization of simplicial topological spaces]] (with respect to [[compactly generated topological spaces]]) preserves finite limits (by [this Prop.](geometric+realization+of+simplicial+topological+spaces#GeometricRealizationPreservesFiniteLimits)).
\end{example}

## Properties
 {#Properties}

+-- {: .num_prop #FiniteLimitsFromPullbacksAndTerminalObject}
###### Proposition

For a [[category]] $\mathcal{C}$ the following are equivalent:

1. $\mathcal{C}$ has all [[finite limits]].

1. $\mathcal{C}$ has all [[equalizers]] and [[binary  products]].

1. $\mathcal{C}$ has all [[pullbacks]] and a [[terminal object]].

In fact, either class of limits may be expressed in terms of another, so that for a [[functor]] $F \;\colon\; \mathcal{C} \to \mathcal{D}$ the following are equivalent:

1. $F$ [[preserved limit|preserves]] [[finite limits]].

1. $F$ [[preserved limit|preserves]] [[equalizers]] and [[binary products]].

1. $F$ [[preserved limit|preserves]] [[pullbacks]] and the [[terminal object]].


=--

(The first statement may be found, e.g., in [Borceux 1994, Prop. 2.8.2](#Borceux94). From the proof there the second statement immediately follows.)

\begin{remark}
The equivalence of the first two items in Prop. \ref{FiniteLimitsFromPullbacksAndTerminalObject} is the finite analog of 
how a category with equalizers and all small products has all [[small limits]].  
\end{remark}

\begin{remark}\label{LFiniteLimits}
Prop. \ref{FiniteLimitsFromPullbacksAndTerminalObject} implies that finite limits are contained in the [[saturation of a class of limits|saturation]] of the class containing only [[finite products]] and [[equalizers]], and also that of the class containing only [[pullbacks]] and [[terminal objects]].  

But the existence of finite limits in fact implies that of the larger class of [[L-finite limits]], and this is the largest class of limits implied by the existence of finite limits. Therefore [[L-finite limits]] constitute the full [[saturation of a class of limits|saturation class]] of both equalizers+finite products as well as pullbacks+terminal objects.
\end{remark}


## Related concepts

* [[finite (∞,1)-limit]]

* [[finite set]], [[finite group]], [[finite category]]

## References

Textbook account:

* {#Borceux94} [[Francis Borceux]], around Def. 2.8.2 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994)
([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))



[[!redirects finite limits]]
[[!redirects finite colimit]]
[[!redirects finite colimits]]
