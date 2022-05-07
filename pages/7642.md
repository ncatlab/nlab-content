
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The naive [[2-category]] $Cat(S)$ of [[internal categories]] in a category $S$ does not have enough [[equivalences]] in general, due to the failure of the [[axiom of choice]] in $S$. The [[functors]] which _should_ be equivalences are called **weak equivalences**, and one often works with the [[bicategory of fractions|localisation]] of $Cat(S)$ at the weak equivalences. Roughly speaking, a weak equivalence is a functor which is 'fully faithful' and 'essentially surjective', but these terms need to be interpreted appropriately.

The concept of weak equivalences first arose in work of Bunge and Par&#233; on stack completions of internal categories.

## Definition


Let $f:X\to Y$ be a functor between categories internal to some category $S$. $f$ is **fully faithful** if the following diagram is a pullback
$$
\begin{matrix}
  X_1& \stackrel{f_1}{\to} & Y_1 \\
  \downarrow&& \downarrow \\
  X_0\times X_0 &\underset{f_0\times f_0}{\to} & Y_0\times Y_0
\end{matrix}
$$

To discuss the analogue of essential surjectivity, we need a notion of 'surjectivity', as this does not generalise cleanly from $Set$. If we are working in a topos, a natural choice is to take epimorphisms, but weaker ambient categories are sometimes needed. A natural choice is to work in a unary [[site]], where the covers are taken as the 'surjective' maps.

Given a functor $f:X\to Y$ internal to a unary site $(S,J)$, $f$ is **essentially $J$-surjective** if the map $t\circ pr_2:X_0 \times_{f_0,Y_0,s}Y_1 \to Y_0$ is a $J$-cover.

We then define an internal functor to be a **$J$-equivalence** if it is fully faithful and essentially $J$-surjective.

## Related concepts

* [[anafunctor]]

* [[equivalence of categories]], [[weak equivalence]]

[[!redirects weak equivalencs of internal categories]]

## References

* M. Bunge, R. Par&#233;, _Stacks and equivalence of indexed categories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 20 no. 4 (1979), p. 373-399 [NUMDAM](http://www.numdam.org/item?id=CTGDC_1979__20_4_373_0)
* [[T. Everaert]], [[R.W.Kieboom]] and [[Tim Van der Linden]], _Model structures for homotopy of internal categories_, Theory and Applications of Categories 15 (2005), no. 3, 66-94. ([journal](http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html))
* [[David Roberts]], _Internal categories, anafunctors and localisation_, Theory and Applications of Categories, 26 (2012) No. 29, pp 788-829. ([journal](http://www.tac.mta.ca/tac/volumes/26/29/26-29abs.html))
 