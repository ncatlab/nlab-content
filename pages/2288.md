
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Stable homotopy theory_ is [[homotopy theory]] in the case that the operations of [[looping and delooping]] are _[[equivalence of (infinity,1)-categories|equivalences]]_.

As [[homotopy theory]] is the study of [[homotopy types]], so _stable homotopy theory_ is the study of [[stable homotopy types]]. As [[homotopy theory]] in generality is [[(∞,1)-category theory]] (or maybe [[(∞,1)-topos theory]]), so stable homotopy theory in generality is the theory of [[stable (∞,1)-categories]].

More specifically, if one thinks of classical [[homotopy theory]] as the study of (just) the [[(∞,1)-category]] $L_{whe}$[[Top]] $\simeq$ [[∞Grpd]] of [[topological spaces]] modulo [[weak homotopy equivalence]] ([[∞-groupoids]]), or rather of its [[homotopy category of an (infinity,1)-category|homotopy category]] $Ho(Top)$, then stable homotopy theory is the study of the corresponding [[stabilization]]: To every suitable [[(∞,1)-category]] is associated its corresponding [[stable (∞,1)-category]] of [[spectrum objects]]. For $L_{whe}$[[Top]] this is the [[stable (∞,1)-category of spectra]], $Sp(L_{whe}Top)$. **Stable homotopy theory** is the study of $Sp(Top)$, or rather of its [[homotopy category of an (infinity,1)-category|homotopy category]], the [[stable homotopy category]] $Ho(Sp(L_{whe}Top))$.

For detailed introduction to the stable homotopy theory of spectra see at _[[Introduction to Stable homotopy theory]]_.

By definition a [[stable homotopy type]] is one on which [[suspension]] and hence [[looping and delooping]] act as an [[equivalence]]. Historically people considered in plain [[homotopy theory]] statements that became true after sufficiently many [[suspensions]], hence once the process of taking [[suspensions]] "stabilizes". Whence the name.

## Applications

### Higher algebra

The study of [[monoid object in a monoidal (infinity,1)-category]] in a [[stable (∞,1)-category]] is the [[homotopy theory|homotopy-theoretic]] version of [[commutative algebra]], hence _[[higher algebra]]_ and [[higher linear algebra]].

A tool of central importance in stable homotopy theory and its application to [[higher algebra]] is the [[symmetric monoidal smash product of spectra]] which allows us to describe [[A-∞ rings]] and [[E-∞ rings]] as ordinary [[monoid]] objects in a [[model category]] that presents $Sp(Top)$. ("[[brave new algebra]]").



## Related concepts

* [[homotopy theory]], [[homotopy type theory]]

* [[stable homotopy category]], [[(infinity,1)-category of spectra]]

* [[Spanier-Whitehead duality]], [[Anderson duality]]

  * [[S-theory]]

* [[stable (infinity,1)-category]]

* [[parameterized homotopy theory]], [[parameterized stable homotopy theory]]

* [[rational stable homotopy theory]]

* [[cohesive stable homotopy theory]]

* [[noncommutative stable homotopy theory]]

* [[chromatic homotopy theory]]

* [[K(n)-local stable homotopy theory]] 

* [[generalized homology theory]], [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]]

* [[stable homotopy homology theory]]

When the spaces and spectra in question carry an [[infinity-action]] of a [[group]] $G$ the theory refines to 

* [[equivariant stable homotopy theory]], [[global equivariant stable homotopy theory]].

## History
 {#History}

> Stable homotopy theory began around 1937 with the [[Freudenthal suspension theorem]]. $[$...$]$ Stable phenomena had of course appeared earlier, at least implicitly: [[reduced cohomology|reduced]] [[generalized homology|homology]] and [[generalized (Eilenberg-Steenrod) cohomology|cohomology]] are examples of functors that are invariant under suspension without limitation on dimension.

> Stable homotopy theory emerged as a distinct branch of [[algebraic topology]] with Adams' introduction of [[Adams spectral sequence|his eponymous spectral sequence]] and his spectacular conceptual use of the notion of stable phenomena in his solution to the [[Hopf invariant one]] problem.

> Its centrality was reinforced by two related developments that occurred at very nearly the same time, in the late 1950's. One was the introduction of [[generalized (Eilenberg-Steenrod) cohomology|generalized homology and cohomology theories]] and especially [[K-theory]], by Atiyah and Hirzebruch. The other was the work of Thom which showed how to reduce the problem of classifying manifolds up to cobordism to a problem, more importantly, a solvable problem, in stable homotopy theory $[$ [[Thom spectrum]] $]$.

> The reduction of geometric phenomena to solvable problems in stable homotopy theory
has remained an important mathematical theme, the most recent major success being Stolz's use of [[spin bordism|Spin cobordism]] to study the classication of manifolds with positive scalar curvature. 

> In an entirely different direction, the early 1970's saw Quillen's introduction of higher [[algebraic K-theory]] and the recognition by Segal and others that it could be viewed as a construction in stable homotopy theory. With algebraic K-theory as an intermediary, there has been a growing volume of work that relates algebraic geometry to stable homotopy theory. With Waldhausen's introduction of the algebraic K-theory of spaces in the late 1970's, stable homotopy became a bridge between algebraic K-theory and the study of diffeomorphisms of manifolds. 

> Within algebraic topology, the study of stable homotopy theory has been and remains the focus of much of the best work in the subject. 

> ([Elmendorf-Kriz-May 95, p. 2](#ElmendorfKrizMay95))

## References

The original direct definitions of the [[stable homotopy category]] (for precursors see at _[[Spanier-Whitehead category]]_) is due to

* {#Boardman65} [[Michael Boardman]], _Stable homotopy theory_, mimeographed notes, University of Warwick, 1965 onward

Early accounts:

* {#Vogt69} [[Rainer Vogt]], _Boardman's stable homotopy category_, lectures, spring 1969

* {#Cohen70} J. M. Cohen, _Stable Homotopy_, Springer Lecture Notes in Math., No. 165,  Springer-Verlag, Berlin, 1970. 

* [[Dieter Puppe]], _On the stable homotopy category_, Topology and its application (1973)  ([[PuppeStableHomotopyCategory.pdf:file]])

* {#Adams74} [[Frank Adams]], Part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

A fun scan of the (pre-)history of the [[stable homotopy category]]:

* [[Peter May]], _The hare and the hedgehog_, speech at [[Michael Boardman]]'s birthday meeting ([txt](http://hopf.math.purdue.edu/May/boardman.txt))

Quick surveys:

* {#Malkiewich14} [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](https://people.math.binghamton.edu/malkiewich/stable.pdf), [[MalkiewichStableHomotopyCategory.pdf:file]])

* [[Dylan Wilson]], _Introduction to stable homotopy theory_ ([pdf](https://etale.site/livetex/wcatss/sht1.pdf), [[WilsonStableHomotopyTheory.pdf:file]])

* [[Aaron Mazel-Gee]], _An introduction to spectra_ ([pdf](https://math.berkeley.edu/~aaron/writing/an-introduction-to-spectra.pdf))

Lecture notes:

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])

* [[Urs Schreiber]], _[[Introduction to Stable homotopy theory]]_, Bonn 2016

* [[David Barnes]], [[Constanze Roitzheim]], _Foundations of Stable Homotopy Theory_, Cambridge University Press 2020 ([doi:10.1017/9781108636575](https://doi.org/10.1017/9781108636575))

* [[Denis Nardin]], _Introduction to stable homotopy theory_, Regensburg 2021 ([webpage](https://homepages.uni-regensburg.de/~nad22969/stable-homotopy-theory2020.php), [pdf](https://homepages.uni-regensburg.de/~nad22969/stable-homotopy-2020/stable-homotopy.pdf), [video](https://www.youtube.com/watch?v=v5Rr_Z8QsOs&list=PLQuS12Ap6va-VgI5cdIjdHquIH3sLCLdJ))


See also:

* Glossary for stable and chromatic honotopy theory ([[StableChromaticGlossary.pdf:file]])

Models with [[symmetric monoidal smash product of spectra]]:

for [[S-modules]]:

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland, (1995) pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

for [[symmetric spectra]]

* [[Stefan Schwede]], _Symmetric spectra_ ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

for [[orthogonal spectra]]:

* [[Stefan Schwede]], _[[Global homotopy theory]]_ (take $\mathcal{F} = \{1\}$, on p. 4, to be the trivial collection of groups, in order to specialize from [[global equivariant stable homotopy theory]] to plain stable homotopy theory).

A survey of formalisms used in stable homotopy theory -- tools to present the [[triangulated category|triangulated]] [[homotopy category]] of a  [[stable (infinity,1)-category]] -- is in

* [[Neil Strickland]], _Axiomatic stable homotopy - a survey_ ([arXiv:math.AT/0307143](http://front.math.ucdavis.edu/0307.5143))

* [[Mark Hovey]], [[John Palmieri]], [[Neil Strickland]],  _Axiomatic stable homotopy theory_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/axiomatic.pdf))

An account in terms of [[(∞,1)-category theory]] is in section 1 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

Brief indications of open questions and future directions (as of 2013) of [[algebraic topology]] and [[stable homotopy theory]] are in 

* [[Tyler Lawson]], _The future_, Talbot lectures 2013 ([pdf](http://math.mit.edu/conferences/talbot/2013/19-Lawson-thefuture.pdf))

[[!redirects stable homotopy theories]]
