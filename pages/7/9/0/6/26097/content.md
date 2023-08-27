
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *list monad* or *free monoid monad* is the [[monad]] on [[Sets]] (with evident generalization to more general [[monoidal categories]]) 

$$
  \array{
    \mathllap{List \;\colon\;}
    Set &\longrightarrow& Set
    \\
    S &\mapsto& S^\ast
  }
$$

which sends a [[set]] $S$ to the [[underlying set]] $U\big(F(S)\big)$ of the [[free monoid]] $F(S) \equiv S^\ast$ on $S$, hence the set of (finite) [[lists]] ([[string (computer science)|strings]]) of [[elements]] of $S$.

Its join operation is by [[concatenation|concatenating]] a list-of-lists to a single list, and its [[unit of a monad|unit]] assigns to an element of $S$ the list consisting of that single element.

The [[Eilenberg-Moore category]] of [[module over a monad|modules]] over the list monad is the [[category of monoids]] $Mon$:

\begin{tikzcd}
  \mathrm{Mon}
  \ar[
    rr,
    shift right=8pt, 
    "{ U }"{swap}
  ]
  \ar[
    from=rr,
    shift right=8pt, 
    "{ F }"{swap}
  ]
  \ar[
    rr,
    phantom,
    "{ \scalebox{.7}{$\bot$} }"
  ]
  &&
  \mathrm{Set}
\end{tikzcd}

## Related pages

* [[monoid]], [[free monoid]]

* [[list]], [[string (computer science)]]

* [[writer monad]]

* [[nondeterministic computation]]

## References

Discussion of the list monad as a [[monad in computer science]] (in [[Haskell]]):

* [[Bartosz Milewski]], *The List Monad*, School of Haskell (2014) &lbrack;[web](https://www.schoolofhaskell.com/school/starting-with-haskell/basics-of-haskell/13-the-list-monad)&rbrack;

* {#Milewski19} [[Bartosz Milewski]], pp. 304 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;


[[!redirects list monads]]

[[!redirects free monoid monad]]
[[!redirects free monoid monads]]

[[!redirects free monoid functor]]
[[!redirects free monoid functors]]
