
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

The __trefoil knot__ is a famous example of a [[knot]]. In the list of knots, ordered by  [[crossing number]], it is the first 'real' knot one meets, being the simplest non-trivial knot. (The first knot listed is usually the '[[unknot]]', i.e. the unknotted circle.) The trefoil has crossing number 3.



Here is the traditional [[knot diagram]] for the trefoil knot:

[[!include trefoil knot - SVG]]

\begin{tikzpicture}
\foreach \n in {0,1,2} {
\begin{scope}[
  rotate=\n*120-4
]
\draw[line width=2]
 (0,-1)
   .. controls
   (-1,.2) and (-2,2) ..
 (0,2)
   .. controls
   (1,2) and (1,1) ..
  (.9,.7);
\end{scope}
};
\end{tikzpicture}


Here is an alternative depiction with [[bridge number]] 2:

[[!include trefoil knot (2 bridge) - SVG]]

\begin{remark}
To include one of the above `svg` pictures on a page, write <nowiki><code>[[!include trefoil knot - SVG]]</code></nowiki> or <nowiki><code>[[!include trefoil knot (2 bridge) - SVG]]</code></nowiki>.
\end{remark}

## Related entries

* [[unknot]]

* [[figure eight knot]]

## Properties

The [[knot group]] of the trefoil knot (calculated either by the Dehn or Wirtinger presentations) has two very useful presentations:

* $\langle x,y \mid x y x=y x y\rangle$, which is the [[braid group]], **Br 3**;

*  $\langle a,b | a^2= b^3\rangle$, in which the pair of numbers, $(2,3)$, is apparent.  These reflect the fact that the trefoil is a $(2,3)$-[[torus knot]]. (Of course, it is also a (3,2)-torus knot.)



category : knot theory
[[!redirects trefoil knot]]
[[!redirects trefoil knots]]
[[!redirects Trefoil knot]]
[[!redirects Trefoil Knot]]
[[!redirects trefoil]]
[[!redirects Trefoil]]
