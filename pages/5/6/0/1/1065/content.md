
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

In an [[abelian category]] $\mathcal{A}$, _homological algebra_ is the [[homotopy theory]] of [[chain complexes]] in $\mathcal{A}$ up to [[quasi-isomorphism of chain complexes]]. Hence it is the study of the [[(infinity,1)-categorical localization]] of the [[category of chain complexes]] at the class of [[quasi-isomorphism of chain complexes|quasi-isomorphisms]], or in other words the [[derived (infinity,1)-category]] of $\mathcal{A}$.

When considering nonnegatively graded chain complexes, homological algebra may be viewed as a linearized version of the [[homotopy theory]] of [[homotopy types]] or [[infinity-groupoids]], by the [[Dold-Kan correspondence]]. When considering unbounded chain complexes, it may be viewed as a linearized and stabilized version, by the [[stable Dold-Kan correspondence]]. Conversely, we may view [[homotopical algebra]] as a nonabelian generalization of homological algebra.

Hence homological algebra is

* The study of a particularly simple sort of [[stable (∞,1)-categories]], namely those derived from categories of chain complexes.  See _[As a toolbox in stable homotopy theory](#ToolboxInStableHomotopyTheory)_ below and the discussion at [[cosmic cube]].

* The study of properties of [[modules]] over [[rings]] of various types, by the use of methods adapted from [[topology|topological]] [[homology theory]].

* A simple fragment of, and toolbox for, [[stable homotopy theory]] --- and hence, by extension, unstable [[homotopy theory]].  From this point of view,  an archetypical motivating example is the [[chain complex]] $C_\bullet(X)$ of [[singular chains]] in a [[topological space]] $X$, whose [[chain homology]] is the _[[singular homology]]_ $H_\bullet(X)$ of $X$, which is a linear approximation to the [[homotopy groups]] of $X$.  Accordingly, $C_\bullet(X)$ itself serves as a linearized approximation to the [[homotopy type]] of $X$.


### As a toolbox in stable homotopy theory
 {#ToolboxInStableHomotopyTheory}

With homological algebra being a topic in stabilized [[homotopy theory]], it is really the study of [[stable (∞,1)-categories]] [[(∞,1)-category of chain complexes|of chain complexes]] -- and thus, by the stable [Dold-Kan correspondence](module%20spectrum#StableDoldKanCorrespondence), of Eilenberg-MacLane [[module spectra]].

Historically this modern perspective has developed only in stages out of more "concrete" (more [[category theory|1-categorical]]) notions, which now form the body of homological algebra, in the form of a box of tools for computing linearized problems in homotopy theory. The following list indicates how these traditional notions serve to present constructions in stable homotopy theory.

1. The notion of _[[quasi-isomorphism]]_ between chain complexes -- [[chain maps]] which induce [[isomorphisms]] on [[homology groups]] -- is the stable version of [[weak homotopy equivalences]] of topological spaces. The _[[derived category]]_ of chain complexes $D(\mathcal{A})$ obtained by [[localization|localizing]] $Ch_\bullet(\mathcal{A})$ at these [[weak equivalences]] is the corresponding _[[homotopy category]]_, the context where all [[chain maps]] are identified up to [[chain homotopy]] between good representatives of these objects.  (On the other hand, in more general situations this correspondence is less immediate, and the notion of quasi-isomorphism may not be the best choice; see at _[[Whitehead theorem]]_.)

1. By the discussion at _[[localization]]_ the morphisms in $D(\mathcal{A})$ are [[zig-zags]] of [[chain maps]] that involve [[resolutions]] by non-isomorphic but [[quasi-isomorphism|quasi-isomorphic]] chain complexes. By the various [[model structures on chain complexes]] these resolutions can concretely be constructed as _[[injective resolutions]]_, _[[projective resolutions]]_ and/or more general sorts of resolutions (such as [[flat resolutions]], soft, flabby, etc.) of chain complexes, and much of the theory revolves around handling these.

1. Notably, [[functors]] between categories of chain complexes may extend to functors on these derived categories by evaluating them on suitable resolutions -- accordingly called _[[derived functors]]_.  (In homological algebra, the phrase "derived functor" is traditionally applied to the *homology groups* of what abstract homotopy theory calls the "derived functor", these being the invariants that one can compute.)  Much of the theory revolves around computing and characterizing derived functors, for instance in the definition of [[abelian sheaf cohomology]] and hence there are powerful tools for these computations, notably [[spectral sequences]].

1. However, the [[derived category]] $D(\mathcal{A})$ is still a rather coarse approximation to the full [[stable (∞,1)-category]] [[(∞,1)-category of chain complexes|of chain complexes]] in $\mathcal{A}$. There is a series of extra property and structures added to it which gives better approximations, and large parts of modern homological algebra study these: 

   First of all the derived category is automatically a [[triangulated category]], which is a means of remembering the operation of _[[suspension]]_ and _de-suspension_ ([[looping]]) of chain complexes. Further structure added to these goes by names such as _[[enhanced triangulated category]]_.  A [[stable derivator]] is a strong enhancement which encodes basically all the requisite structure for internal computations.  Finally, the further promotion of these to _[[stable model categories]]_ or _[[pretriangulated dg-categories]]/linear [[A-∞ categories]]_ of chain complexes makes them capture the full information present in the [[stable (∞,1)-category]].

1. [[algebra|Algebra]] in [[stable homotopy theory]] is _[[higher algebra]]_ over [[E-∞ rings]], and _homological algebra_ provides approximations to that: by the [[stable Dold-Kan correspondence]] [[chain complexes]] of $R$-[[modules]] are a presentation for [[Eilenberg-Mac Lane spectrum|HR]]-[[module spectra]]. Moreover, [[A-infinity algebras]] in $HR$-module spectra [are presented by](http://www.ncatlab.org/nlab/show/model+structure+on+dg-algebras#RelationToAInfinityAlgebras) [[dg-algebras]], hence by ordinary [[associative algebras]] in [[chain complexes]]. Similarly [[E-infinity algebras]] [are presented by](http://www.ncatlab.org/nlab/show/model+structure+on+dg-algebras#RelationToEInfinityAlgebras) [[commutative dg-algebras]], hence by [[commutative monoid|commutative algebras]] internal to chain complexes. By variation of this theme a multitude of notions in [[higher algebra]] finds their representation in homological algebra, for instance [[L-∞ algebras]] in terms of [[dg-Lie algebras]]: [[Lie algebras]] internal to chain complexes.

### Non-abelian variants

There are variants of the tools of homological algebra that can also be applied to more non-linear phenomena, see for instance at [[Dold-Kan correspondence]] the section _[non-abelian case](Dold-Kan%20correspondence#StatementGeneral)_.  These include non-Abelian (co)homology and crossed and quadratic versions that use a small degree of non-linearity in the models.  These latter theories make extensive use of techniques from [[homotopical algebra]] in the wide sense of that term and [[simplicial homotopy theory]] to avoid the crushing of homotopical information that can occur when passing to chain complexes.




## Entries in homological algebra ##

[[!include homological algebra - contents]]


## References
 {#References}

The following lists references on homological algebra:

* [General](#ReferencesGeneral)

* [Lecture notes and course notes](#LectureNotes)

* [History](#ReferencesHistory)


### General
 {#ReferencesGeneral}

Classical accounts:

* {#EilenbergMacLane42} [[Samuel Eilenberg]], [[Saunders MacLane]], *Group Extensions and Homology*, Annals of Mathematics **43** 4 (1942) 757-831 &lbrack;[doi:10.2307/1968966](https://doi.org/10.2307/1968966), [jstor:1968966](https://www.jstor.org/stable/1968966)&rbrack;


* D. A. Buchsbaum, _Exact categories and duality_, Transactions of the American Mathematical Society Vol. 80, No. 1 (1955), pp. 1-34 ([JSTOR](http://www.jstor.org/stable/1993003))

* {#CartanEilenberg56} [[Henri Cartan]], [[Samuel Eilenberg]], *[[Homological Algebra]]*, Princeton Univ. Press (1956), Princeton Mathematical Series **19** (1999) &lbrack;[ISBN:9780691049915](https://press.princeton.edu/books/paperback/9780691049915/homological-algebra-pms-19-volume-19), [doi:10.1515/9781400883844](https://doi.org/10.1515/9781400883844), [pdf](http://www.math.stonybrook.edu/~mmovshev/BOOKS/homologicalalgeb033541mbp.pdf)&rbrack;
 
* [[A. Grothendieck]], _[[Tohoku|Sur quelques points d'algèbre homologique]]_ (1957)  ([part1](http://projecteuclid.org/euclid.tmj/1178244774), [part2](http://projecteuclid.org/euclid.tmj/1178244774))

* {#Godement58} [[Roger Godement]], *Topologie algébrique et theorie des faisceaux*, Actualités Sci. Ind. **1252**, Hermann, Paris (1958) &lbrack;[webpage](https://www.editions-hermann.fr/livre/topologie-algebrique-et-theorie-des-faisceaux-roger-godement), [[Godement-TopologieAlgebrique.pdf:file]]&rbrack;

* [[Saunders MacLane]], *Homology*, Grundlehren der Mathematischen Wissenschaften **114**, Springer (1963, 1974), reprinted as: Classics in Mathematics, Springer (1995)  &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/maclane_homology.pdf), [doi:10.1007/978-3-642-62029-4](https://doi.org/10.1007/978-3-642-62029-4)&rbrack;

* {#HiltonStammbach71} [[Peter Hilton]],  [[Urs Stammbach]], _A course in homological algebra_, Springer-Verlag, New York, 1971, Graduate Texts in Mathematics **4** &lbrack;[doi:10.1007/978-1-4419-8566-8](https://link.springer.com/book/10.1007/978-1-4419-8566-8), [pdf](https://www.sas.rochester.edu/mth/sites/doug-ravenel/otherpapers/hilton-stammbach.pdf)&rbrack;

* [[Saunders Mac Lane]]: _Homology_ (1975) reprinted as Classics in Mathematics. Springer (1995) &lbrack;[doi:10.1007/978-3-642-62029-4](https://link.springer.com/book/10.1007/978-3-642-62029-4), ISBN:3-540-58662-8&rbrack;

* [[Sergei Gelfand]], [[Yuri Manin]]: *[[Methods of homological algebra]]*,  transl. from the 1988 Russian (Nauka Publ.) original, Springer (1996, 2002) &lbrack;[doi:10.1007/978-3-662-12492-5](https://doi.org/10.1007/978-3-662-12492-5)&rbrack;


A standard modern textbook introduction is

* {#Weibel94} [[Charles Weibel]], *[[An introduction to homological algebra]]*,  Cambridge Studies in Adv. Math. **38**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9781139644136](https://doi.org/10.1017/CBO9781139644136), [pdf](https://www.sas.rochester.edu/mth/sites/doug-ravenel/otherpapers/weibel-homv2.pdf)&rbrack;

and a more systematic modern development of the theory is in sections 8 and 12-18 of

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_,  Grundlehren der Mathematischen Wissenschaften __332__, Springer (2006)

Non-abelian variants of homological algebra are disussed for instance in

* [[Francis Borceux]], [[Dominique Bourn]], _[[Borceux-Bourn|Mal'cev, protomodular, homological and semi-abelian categories]]_, Mathematics and Its Applications __566__, Kluwer (2004)


The foundations of the formulation in the broader context of [[stable (∞,1)-category]] theory is in

* [[Jacob Lurie]], _[[Stable Infinity-Categories]]_, ([math.CT/0608228](http://www.arXiv.org/abs/math.CT/0608228))

Other textbooks include

* I. Bucur, A. Deleanu, _Introduction to the theory of categories and functors_, 1968


See also:

* Wikipedia, _[Homological algebra](http://en.wikipedia.org/wiki/Homological_algebra)_

* Springer Online Encyclopeadia of Mathematics: [homological algebra](http://eom.springer.de/H/h047710.htm)


### Lecture notes and course notes
 {#LectureNotes}

* [[Alexander Beilinson]], _Introduction to homological algebra_ (handwritten notes, summer 2007, pdf) [lec1](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-1.pdf), [lec2](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-2.pdf), [lec3](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-3.pdf), [lec4](http://www.math.uchicago.edu/~mitya/beilinson/hom-alg-4.pdf)

* {#Collins06} Julia Collins, _Homological algebra_ (2006) &lbrack;[pdf](http://www.maths.ed.ac.uk/~s0681349/HomologicalAlgebra.pdf)&rbrack;
 

* [[Rick Jardine]], _Homological algebra_, course notes, 2009  ([index](http://www.math.uwo.ca/~jardine/papers/HomAlg/index.shtml))

* [[Peter May]], _Notes on Tor and Ext_ ([pdf](http://www.math.uchicago.edu/~may/MISC/TorExt.pdf))
 {#May}

* [[Pierre Schapira]], _Categories and homological algebra_, lecture notes (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))

* [[Urs Schreiber]], _[[schreiber:Introduction to Homological Algebra]]_


### In constructive mathematics

Discussion of homological algebra in [[constructive mathematics]]:


* {#CoquandSpiwack} [[Thierry Coquand]], [[Arnaud Spiwack]], *Towards constructive homological algebra in type theory*, in: *Towards Mechanized Mathematical Assistants. MKM Calculemus 2007*,  Lecture Notes in Computer Science **4573** Springer (2007) &lbrack;[doi:10.1007/978-3-540-73086-6_4](https://doi.org/10.1007/978-3-540-73086-6_4), [pdf](https://hal.inria.fr/inria-00432525/document)&rbrack;

  > (via [[type theory]])


* [[Julio Rubio]], [[Francis Sergeraert]], _Constructive homological algebra and applications_ &lbrack;[arXiv:1208.3816](http://arxiv.org/abs/1208.3816)&rbrack;


 



### History
 {#ReferencesHistory}

* [[Charles Weibel]], _A history of homological algebra_, [dvi](http://www.math.rutgers.edu/~weibel/HA-history.dvi)

From the introduction of [Collins 2006](#Collins06):

> The word "[[homology]]" was first used in a [[topology|topological]] context by [[Poincaré]] in 1895, who used it to think about [[manifolds]] which were the [[boundaries]] of higher-dimensional manifolds. It was [[Emmy Noether]] in the 1920s who began thinking of homology in terms of [[groups]], and who developed algebraic techniques such as the idea of [[modules]] over a [[ring]]. These are both absolutely crucial ingredients in the modern theory of homological algebra, yet for the next twenty years homology theory was to remain confined to the realm of topology.

> In 1942 came the first move forward towards homological algebra as we know it today, with the arrival of a [paper by Samuel Eilenberg and Saunders MacLane](#EilenbergMacLane42). In it we find [[Hom]] and [[Ext]] defined for the very first time, and along with it the notions of a [[functor]] and [[natural isomorphism]]. These were needed to provide a precise language for talking about the properties of $Hom(A,B)$; in particular the fact that it varies naturally, contravariantly in $A$ and covariantly in $B$. 

> Only three years later this language [was expanded](category#EilenbergMacLane45) to include [[category]] and [[natural equivalence]]. However, this terminology was not widely accepted by the mathematical community until the appearance of [Cartan and Eilenberg's book](#CartanEilenberg56). Cartan and Eilenberg's book was truly a revolution in the subject, and in fact it was here that the term "Homological Algebra" was first coined. The book used [[derived functors]] in a systematic way which united all the previous [[homology theories]], which in the past ten years had arisen in [[group theory]], [[Lie algebras]] and [[algebraic geometry]]. The sheer list of terms that were first defined in this book may give the reader an idea of how much of this project is due to the existence of that one book! They defined what it means for an object to be [[projective object|projective]] or [[injective object|injective]], and defined the notions of [[projective resolution|projective]] and [[injective resolutions]]. It is here that we find the first mention of $Hom$ being [[left exact functor|left exact]] and the first occurrence of $Ext^n$ as the [[right derived functors]] of $Hom$.


