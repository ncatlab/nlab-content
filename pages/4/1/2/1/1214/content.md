
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


A __Malcev category__ is a [[finitely complete category|left exact category]] (= having [[finite limits]]) in which any [[reflexive relation|reflexive]] [[internal relation]] is an [[congruence|equivalence relation]]. Equivalently, the [[fibers]] of its [[fibration of points]] are [[unital category|unital]] (equivalently the fibers of the fibration of points are strongly unital). 

## Examples

\begin{example}\label{GroupsFormAMalcevCategory}
 The category [[Grp]] of all [[groups]] (including [[non-abelian groups]]) is a Malcev category ([Borceux & Bourn 2004, Ex. 2.2.4](#BorceuxBourn04)). More generally, for $\mathcal{C}$ any category with [[finite limits]], the category $Grp(\mathcal{C})$ of [[group objects]] [[internalization|internal]] to $\mathcal{C}$ is a Malcev category.
\end{example}


More generally, the category of $T$-algebras for any [[Lawvere theory]] $T$ which contains a group operation (an $\Omega$-[[Omega-group|group]]). Other examples include the category, $Heyt$, of [[Heyting algebra]]s and the category of left closed [[magma]]s. The dual category to an [[elementary topos]] is a Malcev category. ([Borceux & Bourn 2004, Ex. 2.2.5-7](#BorceuxBourn04))  A [[Malcev variety]] is a [[variety of algebras]] whose category of models is a Malcev category.

## Properties

\begin{proposition}
In any Malcev category, every [[internal category]] is an [[internal groupoid]].
\end{proposition}

\begin{proposition}
The category of [[internal categories]] and functors in an exact Mal’cev category is an exact Mal’cev category. ([Gran 1999, Theorem 3.2](#Gran99))
\end{proposition}

## Related notions

* [[subtractive category]]

* [[Goursat category]]

* [[internal crossed module]]

## References

* {#BorceuxBourn04} [[Francis Borceux]], [[Dominique Bourn]], _[[Mal'cev, protomodular, homological and semi-abelian categories]]_, Mathematics and Its Applications __566__, Kluwer 2004 ([doi:10.1007/978-1-4020-1962-3](https://link.springer.com/book/10.1007/978-1-4020-1962-3))

* [[Dominique Bourn]], [_From Groups to Categorial Algebra : Introduction to Protomodular and Mal’tsev Categories_](https://doi.org/10.1007/978-3-319-57219-2), Compact Textbooks in Mathematics, Birkhäuser 2017 (textbook)

* {#Gran99} [[Marino Gran]], _Internal categories in Mal’cev categories_, Journal of Pure and Applied Algebra **143** 1-3 (1999) 221-229 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(98)00112-1">doi:10.1016/S0022-4049(98)00112-1</a>&rbrack;

[[!redirects Malcev categories]]

[[!redirects Mal'cev categories]]
[[!redirects Mal'cev category]]
[[!redirects Mal&#39;cev category]]
[[!redirects Malʹcev category]]
[[!redirects Malcev category]]
[[!redirects Maltsev category]]
[[!redirects Мальцев category]]



