
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

The *list monad* or *free monoid monad* is the [[monad]] on [[Sets]] (or generally on a [[distributive monoidal category]]) 

$$
  \array{
    \mathllap{List \;\colon\;}
    Set &\longrightarrow& Set
    \\
    S 
      &\mapsto& 
    \displaystyle{
     \underset{n \colon \mathbb{N}}{\textstyle{\coprod}}
    }
    S^{\times n}
  }
$$

which sends a [[set]] $S$ to the [[underlying set]] $U\big(F(S)\big)$ of the [[free monoid]] $F(S) \equiv S^\ast$ on $S$, hence the set of  [[lists]] ([[string (computer science)|strings]]) of [[elements]] of $S$, hence of $n$-[[tuples]] $(s_1, s_2, \cdots, s_n) \colon S^{\times n}$ for any [[natural number]] $n$.

Its join operation is by [[concatenation|concatenating]] a list-of-lists to a single list, 

\begin{tikzcd}[sep=0pt]
    \mathrm{List}
    \big(
      \mathrm{List}(D)
    \big)
    \ar[
      rr,
      "{
        \mathrm{join}^{\mathrm{List}}_D
      }"
    ]
    &&
    \mathrm{List}(D)
    \\
    \scalebox{.8}{$
    \left(
      \def\arraystretch{1}
      \begin{array}{l}
      (d_{11}, \cdots, d_{1 n_1}),
      \\
      \;\;\;\;\vdots
      \\
      (d_{k 1},  \cdots, d_{1 n_k})
      \end{array}
    \right)
    $}
    &\scalebox{.8}{$\mapsto$}&
    \scalebox{.8}{$
    \big(
      d_{11}, \cdots, d_{1 n_1}
      ,\,
      \cdots
      ,\,
      d_{k 1}, \cdots, d_{k n_k}
    \big)
    $}
\end{tikzcd}

and its [[unit of a monad|unit]] assigns to an element of $S$ the list consisting of that single element:

\begin{tikzcd}[sep=0pt]
    D
    \ar[
      rr,
      "{
        \mathrm{ret}
          ^{ \mathrm{List} }
          _{ D }
      }"
    ]
    &&
    \mathrm{List}(D)
    \\
    d &\mapsto& (d)
\end{tikzcd}


The [[Eilenberg-Moore category]] of [[module over a monad|modules]] over the list monad is the [[category of monoids]] $Mon$:

\begin{tikzcd}
  \mathrm{Mon}
  \ar[
    rr,
    shift right=8pt, 
    "{ U^{\mathrm{List}} }"{swap}
  ]
  \ar[
    from=rr,
    shift right=8pt, 
    "{ F^{\mathrm{List}} }"{swap}
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

* [[Philip Wadler]], §2.1 in: *Comprehending Monads*, in: _Conference on Lisp and functional programming_, ACM Press (1990) &lbrack;[[WadlerMonads.pdf:file]], [doi:10.1145/91556.91592](https://doi.org/10.1145/91556.91592)&rbrack;

* [[Philip Wadler]], §5.1 in: *Monads for functional programming*, in M. Broy (eds.) *Program Design Calculi* NATO ASI Series, **118** Springer (1992) &lbrack;[doi;10.1007/978-3-662-02880-3_8](https://doi.org/10.1007/978-3-662-02880-3_8), [pdf](https://homepages.inf.ed.ac.uk/wadler/papers/marktoberdorf/baastad.pdf)&rbrack;

* [[Philip Wadler]], §2.7 in: *The essence of functional programming*, *POPL '92: Principles of programming languages* (1992) 1-14 &lbrack;[doi:10.1145/143165.143169](https://doi.org/10.1145/143165.143169), [pdf](https://jgbm.github.io/eecs762f19/papers/wadler-monads.pdf)&rbrack;


* [[Bartosz Milewski]], *The List Monad*, School of Haskell (2014) &lbrack;[web](https://www.schoolofhaskell.com/school/starting-with-haskell/basics-of-haskell/13-the-list-monad)&rbrack;

* {#Milewski19} [[Bartosz Milewski]], pp. 304 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;


[[!redirects list monads]]

[[!redirects free monoid monad]]
[[!redirects free monoid monads]]

[[!redirects free monoid functor]]
[[!redirects free monoid functors]]
