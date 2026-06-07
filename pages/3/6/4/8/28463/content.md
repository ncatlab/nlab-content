
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


\tableofcontents


## Definition

\begin{definition}
Given a [[triple]] of [[triangulated categories]] $\mathcal{C}, \mathcal{C}', \mathcal{D}$, then a *triangulated bifunctor* 

$$
  F 
  \,\colon\,
  \mathcal{C} 
    \times
  \mathcal{C}'
  \longrightarrow
  \mathcal{D}
$$

is a [[bifunctor]] which is a [[triangulated functor]] in each variable and respects translation coherently, in that it:

1. (additivity) is [[additive functor|additive]],

1. (triangulation) preserves distinguished triangles in each variable,

1. (translation) is equipped with [[natural isomorphisms]]

   \[
     \begin{array}{ccc}
       F\big(\Sigma X, Y\big)
       &\underoverset{\sim}{\theta_{X,Y}}{\longrightarrow}&
       \Sigma F\big(X,Y\big)
       \\
       F\big(X, \Sigma Y\big)
       &\underoverset{\sim}{\theta'_{X,Y}}{\longrightarrow}&
       \Sigma F\big(X,Y\big)
     \end{array}
   \]

   such that the following [[diagram]] *anti-*commutes (one [[composition|composite]] equals minus the other):

   \[
     \begin{array}{ccc}
       F(\Sigma X, \Sigma Y)
       &\overset{\theta_{X,\Sigma Y}}{\longrightarrow}&
       \Sigma F(X,\Sigma Y)
       \\
       \mathllap{{}^{\theta'_{\Sigma X, Y}}}
       \big\downarrow
       &&
       \big\downarrow
       \mathrlap{{}^{\Sigma \theta'_{X,Y}}}
       \\
       \Sigma F(\Sigma X, Y)
       &\underset{\Sigma \theta_{X,Y}}{\longrightarrow}&  
       \Sigma^2 F(X,Y)
       \mathrlap{\,.}
     \end{array}
   \]

\end{definition}

([Kashiwara & Schapira 2006 Def. 10.3.6 with 10.1.1(v)](#KashiwaraSchapira2006))

## Related entries

* [[monoidal triangulated category]]

## References

* {#KashiwaraSchapira2006} [[Masaki Kashiwara]], [[Pierre Schapira]]; Def. 10.3.6, 10.1.1(v) in: _[[Categories and Sheaves]]_, Grundlehren der Mathematischen Wissenschaften **332**, Springer (2006) \[<a href="https://link.springer.com/book/10.1007/3-540-27950-4">doi:10.1007/3-540-27950-4</a>, [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)\]

[[!redirects triangulated bifunctors]]
