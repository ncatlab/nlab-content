

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


The concept _[[monad]]_ in the context of [[enriched category theory]], so a monad in the 2-category [[VCat]] of $V$-enriched categories. 

## Kleisli presentation 

The Kleisli presentation of a $V$-enriched monad on a $V$-category $C$ comprises

* for every object $X$, an object $T(X)$;

* for every object $X$, a morphism $\eta_X:I \to C(X,T(X))$ in $V$;

* for objects $X,Y$, a morphism $\ast:C(X,T(Y))\to C(T(X),T(Y))$ in $V$;

such that 

* $f^\ast\circ \eta = f$,

* $\eta^\ast = id$, and 

* $
g^\ast\circ f^\ast = (g^\ast f)^\ast$. 

In the setting of [[monad (in computer science)]], $V=C$ is typically a [[cartesian closed category]] and $T$ needs to exist in the internal language of $V$, so $T$ is necessarily enriched. For example, if $V$ is the [[syntactic category]] of a programming language, then all the definable monads in the language are $V$-enriched. 

If $C$ is $V$-enriched with copowers, e.g. if $V=C$, then $V$ acts on $C$. In this circumstance, a $V$-enriched monad on $C$ is the same thing as a $V$-[[strong monad]] on $C$. 

## Examples

* In the case in of enrichment by [[truth values]], a monad is a [[closure operator]] on a poset.

## References 

* [[Max Kelly]] and [[John Power]], *Adjunctions whose counits are coequalizers and presentations of finitary enriched monads*, Journal of Pure and Applied Algebra vol 89, 1993. ([pdf](https://core.ac.uk/download/pdf/82761050.pdf)).

* [[John Power]], _Enriched Lawvere theories_, ([tac](http://www.tac.mta.ca/tac/volumes/6/n7/6-07abs.html))

* [[Eduardo Dubuc]], _Kan Extensions in Enriched Category Theory_, Springer, 1970.


## Related entries

* [[strong monad]]

* [[additive monad]]

* [[monad (in computer science)]]

* [[tensorial strength]]

* [[enriched adjunction]]

* [[enriched Lawvere theory]]

[[!redirects enriched monads]]
