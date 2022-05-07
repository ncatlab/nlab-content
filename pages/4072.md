
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



## Properties
 {#Properties}

+-- {: .num_prop #FiniteLimitsFromPullbacksAndTerminalObject}
###### Proposition

$\,$

A [[category]] that has all finite [[products]] and all [[equalizers]] also has all finite limits.

A [[category]] that has all [[pullbacks]] and a [[terminal object]] also has all finite limits.

=--

(e.g. [Borceux 1994, Prop. 2.8.2](#Borceux94))

This is analogous to how a category with _all_ small products and equalizers has all small [[limits]].  

\begin{remark}\label{LFiniteLimits}

More precisely, finite limits are contained in the [[saturation of a class of limits|saturation]] of the class containing only [[finite products]] and [[equalizers]], and also that of the class containing only pullbacks and terminal objects.  (The actual saturation is somewhat larger than this --- it is the class of [[L-finite limits]].)

\end{remark}


## Related concepts

A [[category]] that has all finite limits is called a [[finitely complete category]] or a (finitary) [[essentially algebraic theory]].

A [[functor]] that preserves finite limits is called [[left exact functor]], a _lex_ functor, a _cartesian_ functor, or a _finitely continuous_ functor.   The 2-category of finitely complete categories, left exact functors and natural transformations is called [[Lex]].

For the analog notion in [[(∞,1)-category theory]] see [[finite (∞,1)-limit]].

## References

Textbook account:

* {#Borceux94} [[Francis Borceux]], around Def. 2.8.2 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994)
([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))



[[!redirects finite limits]]
[[!redirects finite colimit]]
[[!redirects finite colimits]]
