
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called the _thick subcategory theorem_ gives a characterization of all [[thick subcategories]] of the [[stable homotopy category]] of [[p-localization|p-local]] [[finite spectra]].

This is a consequence of the [[nilpotence theorem]].

## Statement

For $n \in \mathbb{N}$, write $K(n)$ for the [[Morava K-theory]] [[spectrum]].

Say that a $p$-local finite spectrum $X$ has _type $n$_ if $K(n)_\ast(X) \neq 0$ but $K(k)_\ast(X) \simeq 0$ for all $k \lt n$. (e.g. [Lurie, def. 6](#Lurie)).

Write $Spectra^{fin}_p \hookrightarrow Spectra$ be the [[full subcategory]] of the [[(infinity,1)-category of spectra]] on the [[p-localization|p-local]] [[finite spectra]].

The **thick subcategory theorem** says that thick subcategories of $Spectra^{fin}_p$ are precisely the full subcategories on the spectra of type $\geq n$, for some $n$. (e.g. [Lurie, theorem 8](#Lurie)).

In other words, the thick subcategories are the [[kernels]] of $K(n)_\ast$ (for any given prime). 

## Applications

The thick subcategory theorem serves to determine the [[prime spectrum of a symmetric monoidal stable (∞,1)-category]] of the [[stable homotopy theory]].

(For an exposition see [MazelGee 13, around slide 9](#MazelGee13)).

## References

The original article is

* [[Michael Hopkins]], [[Jeff Smith]], _Nilpotence and stable homotopy theory_ II. Ann. of Math. (2),148(1):1&#8211;49, 1998

Further discussion is in 

* Alain Jeanneret, [[Peter Landweber]], [[Douglas Ravenel]], _A note on the thick subcategory theorem_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/jlr.pdf))

* {#Lurie} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, lecture 26, _Thick subcategories_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture26.pdf))

Some big-picture motivation is in 

* {#MazelGee13} [[Aaron Mazel-Gee]], _You could've invented $tmf$_, April 2013 ([pdf slides](http://math.berkeley.edu/~aaron/writing/ustars-tmf-beamer.pdf))
