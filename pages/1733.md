
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Algebraic topology_ refers to the application of methods of [[algebra]] to problems in [[topology]]. More specifically,
the method of algebraic topology is to assign [[homeomorphism]]/[[homotopy]]-[[invariants]] to [[topological spaces]], or more systematically, to the construction  and applications of [[functors]] from some [[category]] of topological objects  (e.g. [[Hausdorff spaces]], topological [[fibre bundles]]) to some algebraic category (e.g. [[abelian groups]],
[[modules]] over the [[Steenrod algebra]]). Landing in an algebraic category aids to the computability, 
but typically loses some information (say getting from 
a topological spaces with a continuum or more points 
to rather discrete algebraic structures).


### The idea of functorial invariants

The basic idea of the functorial method for the problem of existence of morphisms is the following: 
If $F:A\to B$ is a [[functor]] 
(we present here a general statement, but in the above context 
$A$ is a category of topological objects
and $B$ some category of algebraic objects) 
and $d:D\to A$ a [[diagram]] in $A$ then
$F\circ d$ is a diagram in $B$. 
If one can fill certain additional
arrow $f$ in the diagram $d$ making the extended diagram commutative,
then $F(f)$ is a morphism between the corresponding vertices in $B$ extending $F\circ d$ to a commutative diagram.
Thus if we prove that there is no morphism extending $F\circ d$ then
there was no morphism extending $d$ in the first place. 
Therefore, the functorial method is very suitable to prove 
_negative_ existence for morphisms. Sometimes,
however, there is a theorem showing that some set of invariants
completely characterizes a problem hence being able to show
positive existence or uniqueness for maps or spaces.
For the uniqueness for morphisms, it is enough to show that $F$ is
faithful and that there is at most one solution for the existence
problem in the target category. 
Faithful functors in this context are rare, 
but it is sufficient for $F$ to be faithful on some subcategory $A_p$
of $A$ containing at least all morphisms which are 
the possible candidates for the solution of 
the particular existence problem for morphisms.

## Overview of methods

The archetypical example is the classification of [[surfaces]] via their [[Euler characteristic]]. But as this example already shows, algebraic topology tends to be less about [[topological spaces]] themselves as rather about the [[homotopy types]] which they [[homotopy hypothesis|present]]. Therefore the topological invariants in question
are typically homotopy invariants of spaces with some exceptions, like the [[shape theory|shape invariants]] for spaces with bad local behaviour.   

Hence modern algebraic topology is to a large extent the application of algebraic methods to [[homotopy theory]]. 

A general and powerful such method is the assignment of [[homology]] and [[cohomology]] [[groups]] to topological spaces, such that these [[abelian groups]] depend only on the [[homotopy type]]. The simplest such are [[ordinary homology]] and [[ordinary cohomology]] groups, given by [[singular simplicial complexes]]. This way algebraic topology makes use of tools of [[homological algebra]]. 

The [[axiom|axiomatization]] of the properties of such [[cohomology]] group assignments is what led to the formulation of the trinity of concepts of _[[category]]_, _[[functor]]_ and _[[natural transformations]]_, and algebraic topology has come to make intensive use of [[category theory]].

In particular this leads to the formulation of  [[generalized (Eilenberg-Steenrod) cohomology]] theories which detect more information about classes of homotopy types. By the [[Brown representability theorem]] such are represented by [[spectra]] (generalizing [[chain complexes]]), hence [[stable homotopy types]], and this way algebraic topology comes to use and be about [[stable homotopy theory]]. 

Still finer invariants of [[homotopy types]] are detected by further refinements of these "algebraic" structures, for instance to [[multiplicative cohomology theories]], to  [[equivariant homotopy theory]]/[[equivariant stable homotopy theory]] and so forth. The construction and analysis of these requires the intimate combination of algebra and homotopy theory to [[higher category theory]] and [[higher algebra]], notably embodied in the [[universal algebra|universal]] higher algebra of [[operads]].

The central tool for breaking down all this [[higher algebra|higher algebraic]] data into computable pieces are [[spectral sequences]], which are maybe the main heavy-lifting workhorses of algebraic topology.

## Related entries

*  [[basic problems of algebraic topology]], [[topology]], [[differential topology]]
*  [[homotopy theory]], [[shape theory]], [[nonabelian algebraic topology]], [[rational homotopy theory]]
*  [[homotopy lifting property]], [[Hurewicz fibration]], [[Hurewicz connection]], [[Serre fibration]]
*  [[homotopy extension property]], [[Hurewicz cofibration]], [[deformation retract]]
*  [[suspension]], [[loop space]], [[mapping cylinder]], [[mapping cone]], [[mapping cocylinder]]
*  [[cohomology]], [[spectrum]], [[Brown representability theorem]]
*  [[fundamental group]], [[fundamental groupoid]] 
*  [[homotopy group]], [[Eckmann-Hilton duality]], [[H-space]], [[Whitehead product]]
*  [[topological K-theory]], [[complex cobordism]], [[elliptic cohomology]], [[tmf]]
*  [[CW complex]], [[CW approximation]], [[simplicial complex]], [[simplicial set]]  
*  [[model category]], [[model structure on topological spaces]], [[homotopy category]]
*  [[fibration sequence]], [[cofibration sequence]] 
*  [[Freudenthal suspension theorem]], [[Whitehead theorem]] 

## References

Textbooks:

* [[Samuel Eilenberg]], [[Norman Steenrod]], _Foundations of Algebraic Topology_, Princeton University Press 1952 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/eilestee.pdf), [ISBN:9780691653297](https://press.princeton.edu/books/hardcover/9780691653297/foundations-of-algebraic-topology))

* {#Spanier66} [[Edwin Spanier]], _Algebraic topology_, Springer 1966 ([doi:10.1007/978-1-4684-9322-1](https://link.springer.com/book/10.1007/978-1-4684-9322-1))

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975 ([doi:10.1007/978-3-642-61923-6](https://link.springer.com/book/10.1007/978-3-642-61923-6))

* [[Peter May]], _[[A concise course in algebraic topology]]_,   University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* [[Peter May]], [[Kate Ponto]], _[[More concise algebraic topology]]_,   University of Chicago Press (2012) ([ISBN:9780226511795](https://press.uchicago.edu/ucp/books/book/chicago/M/bo12322308.html), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf))

* [[Dai Tamaki]], [[Akira Kono]], _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

* {#tomDieck2008} [[Tammo tom Dieck]],  _Algebraic topology_, European Mathematical Society, Zürich (2008) ([doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86))

* {#Hatcher} [[Allen Hatcher]], _[Algebraic Topology](https://www.math.cornell.edu/~hatcher/AT/ATpage.html)_

Lecture notes:

* {#HopkinsMathew} [[Michael Hopkins]] (notes by [[Akhil Mathew]]), _algebraic topology -- Lectures_ ([pdf](http://people.fas.harvard.edu/~amathew/ATnotes.pdf))

* [[Friedhelm Waldhausen]], _Algebraische Topologie_ I ([pdf](https://www.math.uni-bielefeld.de/~fw/at.pdf)) , II ([pdf](https://www.math.uni-bielefeld.de/~fw/at_II.pdf)), III ([pdf](https://www.math.uni-bielefeld.de/~fw/at_III.pdf)) ([web](https://www.math.uni-bielefeld.de/~fw/))

* [[James F. Davis]] and [[Paul Kirk]], _Lecture notes in algebraic topology_ ([pdf](http://www.indiana.edu/~jfdavis/teaching/m623/book.pdf))

* [[Gereon Quick]], _[Advanced algebraic topology](https://folk.ntnu.no/gereonq/Math231br.html)_, 2014

Survey of various subjects in algebraic topology:

* {#James95} [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_ 1995

Survey with relation to [[differential topology]]:

* [[Sergei Novikov]], _Topology I -- General survey_, in: Encyclopedia of Mathematical Sciences Vol. 12, Springer 1986 ([doi:10.1007/978-3-662-10579-5](https://link.springer.com/book/10.1007/978-3-662-10579-5), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/novikovsurv.pdf))

* [[Jean Dieudonné]], _A History of Algebraic and Differential Topology, 1900 - 1960_, Modern Birkh&auml;user Classics 2009 ([ISBN:978-0-8176-4907-4](https://www.springer.com/de/book/9780817649067))

A textbook with an emphasis on [[homotopy theory]] is in 

* Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

Some interactive 3D demos can be found at

* [[Neil Strickland]], *Interactive pages for Algebraic Topology*, [web site](http://neil-strickland.staff.shef.ac.uk/courses/MAS435/demos/)



Further online resources include

* [a thread on this at MathOverflow](http://mathoverflow.net/questions/18041/algebraic-topology-beyond-the-basicsany-texts-bridging-the-gap).


Brief indications of open questions and future directions (as of 2013) of [[algebraic topology]] and [[stable homotopy theory]] are in 

* [[Tyler Lawson]], _The future_, Talbot lectures 2013 ([pdf](http://math.mit.edu/conferences/talbot/2013/19-Lawson-thefuture.pdf))


