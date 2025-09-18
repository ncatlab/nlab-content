

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[theorem]] due to [Fox 1976](#Fox76) characterizes the [[cartesian products]] in a [[cartesian monoidal category]] as an [[algebraic structure]] given by [[natural transformations]] rather than in terms of a [[universal property|universal]] [[property]].

## Statement

Fox's original theorem is as follows.

\begin{theorem}
  The forgetful functor from the category of [[cartesian monoidal categories]] and [[strict monoidal functors]] into the category of [[symmetric monoidal categories]] and strict monoidal functors admits a [[right adjoint]], given by the construction of the category of [[cocommutative comonoids]].
\end{theorem}

(Note that the forgetful functor also has a [[left adjoint]], by [[2-monad|two-dimensional monad theory]].)

However, the following corollary (and variants) are often also referred to simply as "Fox's theorem":

\begin{corollary}
A [[symmetric monoidal category]] is [[cartesian monoidal category|cartesian]] if and only if it is [[isomorphic]] to its own category of [[cocommutative comonoid|cocommutative]] [[comonoids]]. Thus every object is equipped with a unique cocommutative comonoid structure, and these structures are respected by all maps.
\end{corollary}

## Related concepts

* [[semicartesian monoidal category]]

*  [[comonoid]]

* [[gs-monoidal category]], [[Markov category]]

## Reference

The original article:

* {#Fox76} [[Thomas Fox]]: *Coalgebras and cartesian categories*, Communications in Algebra **4** 7 (1976) 665-667 &lbrack;[doi:10.1080/00927877608822127](https://doi.org/10.1080/00927877608822127), [pdf](https://www.tandfonline.com/doi/pdf/10.1080/00927877608822127)&rbrack;

A survey of theorems extending Fox's original theorem:

* [[Nathanael Arkor]], *Magmal characterisations of cocartesian categories* &lbrack;[arXiv:2508.11615](https://arxiv.org/abs/2508.11615)&rbrack;

[[!redirects Fox theorem]]
