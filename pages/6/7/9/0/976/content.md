#Motivation and history#

While [[homotopy theory]] is suitable for the study of (locally) good [[topological space]]s, it fails to give useful information for bad spaces, whose classical examples are the [[warsaw.gif:file]], [Sierpinski gasket](http://en.wikipedia.org/wiki/Sierpinski_triangle), [p-adic solenoid](http://en.wikipedia.org/wiki/Solenoid_%28mathematics%29) and so on. Even if our principal interest is in good spaces, bad spaces arise in their study. For example, in the study of dynamical systems on manifolds, an important issue are the attractors of such systems, which are typically fractal sets. The intuitive idea of shape theory is to define invariants of topological spaces by approximating them with good spaces, either by considerations of embedding into good spaces, or by considering abstract inverse systems of good spaces. 

The shape theory has been first introduced by Polish mathematician [Karol Borsuk](http://www-groups.dcs.st-and.ac.uk/~history/Mathematicians/Borsuk.html) in the 1960s. The modern version of shape theory is developed in terms of inverse systems ([[pro-object]]s) introduced in this setup by S. Marde&#353;i&#263;, J. Segal and independently, by Tim Porter (thesis, 1971). 

Shape theory is a '[[Čech methods|Čech homotopy theory]]', having a similar relationship to &#268;ech homology as homotopy theory based on the singular complex construction has to singular homology.


For many applications one needs more refined invariants which build up [[strong shape theory]], while sometimes more crude versions may be useful, for example the recent theory of [[coarse shape]]. In fact, the origins of both shape theory and strong shape theory go back further to work by [Lefshetz](http://www-groups.dcs.st-and.ac.uk/~history/Mathematicians/Lefschetz.html) and his student, D. Christie (thesis plus article, D.E. Christie, _Net homotopy for compacta_,  Trans. Amer. Math. Soc., 56 (1944) 275--308). Christie considered a 2-truncated form of strong shape theory, categorically this corresponds to a lax or op-lax 2-categorical version of shape theory.


M. Batanin further elucidated strong shape theory from a categorical and 2-categorical point of view, but his approach is still not much used. His 1997 paper, shows the connections between this theory and a homotopy theory of simplicial [[distributor|distributors]] linked to $A_{\infty}$-categories.

The strong shape theory of compact spaces is related to certain constructions on the corresponding (commutative) $C^*$-algebras of functions.  This is related to the algebraic K-theory of such commutative $C^*$-algebras.  Extensions to non-commutative $C^*$-algebras have been made.

As shape theory is a [[Čech methods|Čech homotopy theory]], what is the corresponding construction for strong shape. The answer is Steenrod--Sitnikov homology and this is discussed in Marde&#353;i&#263;'s book, Strong Shape and Homology, (see below).  Many of the themes of homotopy coherence and related ideas occur in this theory and this suggests an infinity categorical approach (closely related to Batanin's) may be important.

#Abstract shape category#

The shape category associated to a pair $(C,D)$ of a category $C$ and a [[dense subcategory]] $D$ (of good objects) in the second sense, that is for every object $X$ in $C$ there is its $D$-expansion, that is a universal object $\bar{X}$ in the category $pro D$ of [[pro-object]]s in $D$, together with a map $X\to\bar{X}$ in $pro D$, which is universal (initial) among all such. The shape category has the same objects as $C$ and its morphisms are equivalence classes of maps between the $D$-expansions.

A more [[categorical shape theory|categorical form of shape theory]] was studied by Deleanu and Hilton in a series of papers in the 1970s. They consider a more general setting of a functor $K : D \to C$ which in the classical Borsuk case would be the inclusion of the homotopy category of compact [[polytope|polyhedra]] into that of all compact [[metric space]]s. 

This was developed further by Bourn and Cordier, and a strong shape version was then found by Batanin.


#References#

See also $n$lab entries [[shape fibration]]...and references 

* D.A. Edwards and H. M. Hastings, (1976), &#268;ech and Steenrod homotopy theories with applications to geometric topology, Lecture Notes in Maths. 542, Springer-Verlag. 
* J.T. Lisica and S. Marde&#353;i&#263;, Coherent prohomotopy and strong shape theory, Glasnik Mat. 19(39) (1984) 335--399. 
* J.-M. Cordier and T. Porter, (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008). 
* S. Marde&#353;i&#263;, J. Segal, (1982) Shape Theory, North 
Holland. 
* [[Sibe Mardesic|S. Mardešić]], Strong Shape and Homology, Springer monographs in mathematics, Springer-Verlag. 
* D.  Bourn and J.-M. Cordier, [Distributeurs et th&#233;orie de la forme](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1980__21_2), Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 21,(1980), no. 2, 161--188.
* M. A. Batanin, [Categorical strong shape theory](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1997__38_1_3_0), Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 38 (1997), no. 1, 3--66.
* (more)