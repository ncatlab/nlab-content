
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Homological algebra studies [[categories of chain complexes]] $Ch_\bullet(\mathcal{A})$ (in [[abelian categories]] $\mathcal{A}$) using _[[chain homology]]_ as the basic invariant (therefore the name). It is a simple fragment of and serves as a computational tool for [[stable homotopy theory]], and hence (by extension) also unstable [[homotopy theory]].

An archetypical motivating example for homological algebra is the [[chain complex]] $C_\bullet(X)$ of [[singular chains]] in a [[topological space]] $X$: [[formal linear combinations]] of [[simplices]] in $X$. The [[chain homology]] of $C_\bullet(X)$, called the _[[singular homology]]_ $H_\bullet(X)$ of $X$, is a linear approximation to the [[homotopy groups]] of $X$.  Accordingly, the chain complex $C_\bullet(X)$ itself serves as a linearized approximation to the [[homotopy type]] of $X$. 

### As a toolbox in stable homotopy theory

With homological algebra thus being a topic in stabilized [[homotopy theory]], it is really the study of [[stable (∞,1)-categories]] [[(∞,1)-category of chain complexes|of chain complexes]] (and thus, by the stable [Dold-Kan correspondence](module%20spectrum#StableDoldKanCorrespondence), of Eilenberg-MacLane [[module spectra]]).

Historically this modern perspective has developed only in stages out of more "concrete" (more [[category theory|1-categorical]]) notions, which now form the body of homological algebra, in the form of a box of tools for computing linearized problems in homotopy theory.

1. The notion of _[[quasi-isomorphism]]_ between chain complexes -- [[chain maps]] which induce [[isomorphisms]] on [[homology groups]] -- is the stable version of [[weak homotopy equivalences]] of topological spaces. The _[[derived category]]_ of chain complexes $D(\mathcal{A})$ obtained by [[localization|localizing]] $Ch_\bullet(\mathcal{A})$ at these [[weak equivalences]] is the corresponding _[[homotopy category]]_, the context where all [[chain maps]] are identified up to [[chain homotopy]] between good representatives of these objects.  (On the other hand, in more general situations this correspondence is less immediate, and the notion of quasi-isomorphism may not be the best choice; see at _[[Whitehead theorem]]_.)

1. By the discussion at _[[localization]]_ the morphisms in $D(\mathcal{A})$ are [[zig-zags]] of [[chain maps]] that involve [[resolutions]] by non-isomorphic but [[quasi-isomorphism|quasi-isomorphic]] chain complexes. By the various [[model structures on chain complexes]] these resolutions can concretely be constructed as _[[injective resolutions]]_, _[[projective resolutions]]_ and/or more general sorts of resolutions (such as [[flat resolutions]], soft, flabby, etc.) of chain complexes, and much of the theory revolves around handling these.

1. Notably, [[functors]] between categories of chain complexes may extend to functors on these derived categories by evaluating them on suitable resolutions -- accordingly called _[[derived functors]]_.  (In homological algebra, the phrase "derived functor" is traditionally applied to the *homology groups* of what abstract homotopy theory calls the "derived functor", these being the invariants that one can compute.)  Much of the theory revolves around computing and characterizing derived functors, for instance in the definition of [[abelian sheaf cohomology]] and hence there are powerful tools for these computations, notably [[spectral sequences]].

1. However, the [[derived category]] $D(\mathcal{A})$ is still a rather coarse approximation to the full [[stable (∞,1)-category]] [[(∞,1)-category of chain complexes|of chain complexes]] in $\mathcal{A}$. There is a series of extra property and structures added to it which gives better approximations, and large parts of modern homological algebra study these: 

   First of all the derived category is automatically a [[triangulated category]], which is a means of remembering the operation of _[[suspension]]_ and _de-suspension_ ([[looping]]) of chain complexes. Further structure added to these goes by names such as _[[enhanced triangulated category]]_.  A [[stable derivator]] is a strong enhancement which encodes basically all the requisite structure for internal computations.  Finally, the further promotion of these to _[[stable model categories]]_ or _[[pretriangulated dg-categories]]/linear [[A-∞ categories]]_ of chain complexes makes them capture the full information present in the [[stable (∞,1)-category]].


### Non-abelian variants

There are variants of the tools of homological algebra that can also be applied to more non-linear phenomena, see for instance at [[Dold-Kan correspondence]] the section _[non-abelian case](Dold-Kan%20correspondence#StatementGeneral)_.  These include non-Abelian (co)homology and crossed and quadratic versions that use a small degree of non-linearity in the models.  These latter theories make extensive use of techniques from [[homotopical algebra]] in the wide sense of that term and [[simplicial homotopy theory]] to avoid the crushing of homotopical information that can occur when passing to chain complexes.



## Entries in homological algebra ##

[[!include homological algebra - contents]]

## References ##

### General

A first introduction is in 

* [[Charles Weibel]], _[[An introduction to homological algebra]]_,  Cambridge Studies in Adv. Math. 38, CUP 1994

A more comprehensive development of the theory is in sections 8 and 12-18 of

* [[Masaki Kashiwara]], [[Pierre Schapira]], _Categories and Sheaves_,  Grundlehren der Mathematischen Wissenschaften __332__, Springer (2006)

following

* [[A. Grothendieck]], _Sur quelques points d'alg&#232;bre homologique_, [[Tohoku]], [part1](http://projecteuclid.org/euclid.tmj/1178244774), [part2](http://projecteuclid.org/euclid.tmj/1178244774)

Non-abelian variants of this are disussed in

* [[Francis Borceux]], [[Dominique Bourn]], _[[Borceux-Bourn|Mal'cev, protomodular, homological and semi-abelian categories]]_, Mathematics and Its Applications __566__, Kluwer (2004)


The foundations of the formulation in the context of [[stable (∞,1)-category]] theory is in

* [[Jacob Lurie]], _[[Stable Infinity-Categories]]_, ([math.CT/0608228](http://www.arXiv.org/abs/math.CT/0608228))

Other references include

* [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, Princeton Univ. Press 1956.

* I. Bucur, A. Deleanu, _Introduction to the theory of categories and functors_, 1968

* S. I . Gelfand, [[Yu. I. Manin]], _Methods of homological algebra_

* Springer Online Encyclopeadia of Mathematics: [homological algebra](http://eom.springer.de/H/h047710.htm)


### Lecture notes and course notes

* [[Ieke Moerdijk]], _Notes on homological algebra_, course notes (2007), 

* [[Alexander Beilinson]], _Introduction to homological algebra_ (handwritten notes, summer 2007, pdf) [lec1](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-1.pdf), [lec2](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-2.pdf), [lec3](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-3.pdf), [lec4](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-4.pdf)

* [[Rick Jardine]], _Homological algebra_, course notes, 2009  ([index](http://www.math.uwo.ca/~jardine/papers/HomAlg/index.shtml))

* [[Pierre Schapira]], _Categories and homological algebra_, lecture notes (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))


### History

* [[Charles Weibel]], _A history of homological algebra_, [dvi](http://www.math.rutgers.edu/~weibel/HA-history.dvi)

