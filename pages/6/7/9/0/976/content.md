
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Motivation

While the idea of a [[homotopy type]]  is very suitable for the study of (locally) good [[topological space|topological spaces]], the [[weak homotopy type]] fails to give useful information for 'bad' spaces, of which classical examples include  the [[Warsaw Circle]], [Sierpinski gasket](http://en.wikipedia.org/wiki/Sierpinski_triangle), [[p-adic solenoid]] and so on. Even if our initial and principal interest is more often than not in good spaces, bad spaces arise naturally in their study. For example, in the study of dynamical systems on manifolds, an important issue is the study of  the attractors of such systems, which are typically fractal sets, and thus not 'locally nice' at all! The intuitive idea of shape theory is to define invariants of quite general topological spaces by approximating them with 'good' spaces, either by  embedding them into good spaces, and looking at open or polyhedral neighborhoods of them, or by considering abstract inverse systems of good spaces. The two approaches are closely related.

## Idea

If there are few maps from polyhedra (e.g. from spheres) into the space, then the [[weak homotopy type]] may tell too little about the space. 
Therefore one "expands" the space into a successive system of spaces which are good recipients of maps from polyhedra (e.g. [[absolute retract|absolute neighborhood retracts]] (ANRs), polyhedra) and one adapts the homotopy theory to such expansions. The analogue of (strong) homotopy type in this setting is the shape of a space; the shape is an invariant of the strong homotopy type and agrees with it on the ANRs for metric spaces and on the polyhedra. It is more crude for other spaces, but more suitable than the weak homotopy type, or more exactly gives complementary information. Instead of embedding a space, one may abstractly expand or resolve the space or its homotopy class into a pro-object in a category of nice spaces. [[Strong shape theory]] is a variant which is closer to the usual kind of  homotopy, is more geometric and has more homotopy theoretic constructions available in its 'toolkit'. It differs by passing to the homotopy category at a later stage in the theory, so one gets homotopy coherent approximating systems rather than homotopy commutative ones. 


## History

Shape theory was first explicitly introduced by Polish mathematician [Karol Borsuk](http://www-groups.dcs.st-and.ac.uk/~history/Biographies/Borsuk.html) in the 1960s, although Christie, a student of Lefshetz, had done some initial development work on the same basic idea much earlier. One of the modern versions of shape theory is developed in terms of inverse systems of [[absolute retract|absolute neighbourhood retracts]] (ANRs) (which are [[pro-object|pro-objects]] in the homotopy category of polyhedra).  These were introduced in this setting by [[Sibe Mardesic|S. Mardešić]], and [[Jack Segal|J. Segal]] (1971) and independently, in a slightly different form, by [[Tim Porter]] (thesis, 1971), using the more combinatorial framework of [[pro-objects]] in the category of simplicial sets. This latter approach also indicated the possible link with the &#233;tale homotopy theory of Artin and Mazur, (Springer Lecture Notes 100).

Shape theory is a '[[Cech methods|&#268;ech homotopy theory]]', having a similar relationship to &#268;ech homology as homotopy theory, based on the singular complex construction, has to singular homology. In fact, as mentioned above, the origins of both shape theory and strong shape theory go back than further Borsuk's initial papers  to work by [Lefshetz](http://www-groups.dcs.st-and.ac.uk/~history/Mathematicians/Lefschetz.html) and his student, D. Christie (thesis plus article, D.E. Christie, _Net homotopy for compacta_,  [Trans. Amer. Math. Soc., 56 (1944) 275--308](www.ams.org/journals/tran/1944-056-00/home.html)). Christie considered a 2-truncated form of strong shape theory, categorically this corresponds to a lax or op-lax 2-categorical version of shape theory.
Although many of the initial ideas were developed by Christie, the paper went unnoticed until Borsuk developed his slightly different approach in the late 1960s.


For many applications one needs more refined invariants which build up [[strong shape theory]], while sometimes more crude versions may be useful, for example the recent theory of [[coarse shape]]. 

Strong Shape Theory developed in the 1970s through the work of Edwards and Hastings (lecture notes, see below), Porter, Quigley, and others.  It has, especially in the approach pioneered by Edwards and Hastings, strong links to [[proper homotopy theory]].  The links are a form of duality related to some of the more geometric duality theorems of classical cohomology.


M. Batanin further elucidated strong shape theory from a categorical and 2-categorical point of view, but his approach is as yet not much used. His 1997 paper, shows the connections between this theory and a homotopy theory of simplicial [[distributor|distributors]] linked to $A_{\infty}$-categories.

The structure of the [[strong shape theory]] of compact spaces is related to certain structure and constructions on the corresponding (commutative) $C^*$-algebras of functions.  These are related to the algebraic K-theory of such commutative $C^*$-algebras.  Extensions to non-commutative $C^*$-algebras have been made; see ([Blackadar](#Blackadar)) and ([Dadarkat](#Dadarlat)) below, for a start.

As shape theory is a [[Čech methods|Čech homotopy theory]], its corresponding homology is Čech homology, but what is the corresponding construction for strong shape? The answer is Steenrod--Sitnikov homology. This is discussed in Marde&#353;i&#263;'s book, _Strong Shape and Homology_, (see below).  Many of the themes of homotopy coherence and related ideas occur in this theory and this suggests an infinity categorical approach (closely related to Batanin's) may be important.  This seems to be emerging with interpretations of work by Toen and Vezzosi, and by Lurie, and perhaps suggests a review of Batanin's work from that new viewpoint.

## Borsuk's shape theory 

This was the original form and applies to compact metric spaces.  It uses the fact that any compact metric space can be embedded in the [[Hilbert Cube]]. For any such embedded compact metric spaces, $X$ and $Y$, one considers **shape maps** from the collection of open neighbourhoods of $X$ to those of $Y$.  These shape maps are families of continuous maps satisfying a compatibility relationship ' up to homotopy'.  These compose nicely and form the Borsuk shape category.  Two spaces have the same shape if they are isomorphic in this category. Full details of the definition of such shape morphisms are given in the separate entry, [[Borsuk shape theory]]. 

A remarkable and beautiful theorem of Chapman (the Chapman complement theorem) shows that the shape of two compact metric spaces, $X$ and $Y$ embedded in the [[Hilbert cube|pseudo-interior]] of the Hilbert cube, $Q$, have the same shape if and only if their complements $Q\setminus X$ and $Q\setminus Y$ are homeomorphic.


## Strong shape via $\infty$-topos theory
 {#StrongShapeViaInfinityToposTheory}

To any topological space $X$ there is associated
its [[(infinity,1)-category of (infinity,1)-sheaves|$\infty$-category of $\infty$-sheaves]] (with respect to its [[site]] of [[open subsets]]), which is an [[(infinity,1)-topos|$\infty$-topos]]. Many properties of "[[spaces]]" are shared or may be modeled by [[(infinity,1)-topos|$\infty$-toposes]], in particular there is a general and canonical notion of [[shape of an (infinity,1)-topos|shape of an $\infty$-topos]] (see there for more).

At least when $X$ is a [[compact Hausdorff space]], then its strong shape in the classical sense of [Mardešić & Segal 1971](#MardesicSegal71) does agree with the [[shape of an (infinity,1)-topos|$\infty$-topos theoretic shape]] of its [[(infinity,1)-category of (infinity,1)-sheaves|$\infty$-category of $\infty$-sheaves]].

This fact must have motivated the terminology in [Toën-Vezzosi 2002](shape+of+an+infinity1-topos#ToenVezzosi02) and in [Lurie 2009, Sec. 7.1.6](#Lurie09); it is made explicit in [Hoyois 2013, Rem. 2.13](#Hoyois13).



## Abstract shape category

### Idea

The idea of abstract shape theory is very simple. You have a category, $C$, of objects that you want to study.  (In Borsuk's classical topological case this was the (homotopy) category of compact metric spaces.) You  have a well behaved set of methods that work well for some subcategory, $D$, of those objects (polyhedra in Borsuk's case, where the methods were those of homotopy theory). The categorical idea that can be glimpsed behind the topological constructions of topological shape theory is that of replacing an object $X$ of $C$ with approximations to $X$ by objects of $D$, (so 'approximating' a compact metric space by polyhedra, for instance). Categorically this replaces the object $X$ by the [[comma category]], $(X/D)$, which comes with a projection functor to $D$, which 'records' the approximating $D$-object for each approximation. 
You then use your invariants for objects in $D$ to define (and study) the more general objects in $C$. This does not come without consequences as you obtain new types of maps, (shape maps) between the objects of $C$, namely functors between the comma categories that respect the projections.  The objects of $C$ together with your new shape maps form the shape category of your situation.


### Definition

The **shape category** $Shape(C,D)$ is associated to a pair $(C,D)$ of a category $C$ and a [[dense subcategory]] $D$.

Here _dense subcategory_ is used in the second sense of that term: for every object $X$ in $C$ there is its $D$-expansion, which is the object $\bar{X}$ in the category $pro D$ of [[pro-object|pro-objects]] in $D$ that is universal ([[initial object|initial]]) with the property that it is equipped with a morphism $X\to\bar{X}$ in $pro D$. 

The shape category $Shape(C,D)$ has 

* the same objects as $C$ 

* its morphisms are equivalence classes of maps between 
  the $D$-expansions.

A more [[categorical shape theory|categorical form of shape theory]] was studied by Deleanu and Hilton in a series of papers in the 1970s. They consider a more general setting of a functor $K : D \to C$, which in the classical Borsuk case would be the inclusion of the homotopy category of compact [[simplicial complex|polyhedra]] into that of all compact [[metric space|metric spaces]]. 

This was developed further by Bourn and Cordier, and a strong shape version was then found by Batanin.


### Examples

#### Pro-spaces in a shape context

The classical application of shape theoretic idea is to the study of [[topological space|topological spaces]] that do not have the [[homotopy type]] of a [[CW-complex]]. This is the case obtained from the above general setup by choosing

* $C =$ [[HoTop]]${}_{he}$ the [[homotopy category]] of the category [[Top]] of all [[topological space|topological spaces]] localised at the **[[homotopy equivalence|homotopy equivalences]]**;

* $D = Ho(CW Cplx)$ the full [[subcategory]] given by [[CW-complex|CW-complexes]].

More on this is in the section [Shape theory for topological spaces](ForTopSpaces) below and in [[Cech homotopy]].

#### Profinite groups

Consider the category $C =$[[Grp]] of groups and its subcategory $D$ of finite group. A shape map between two groups is a map between their [[profinite completion of a group|profinite completions]].  This sort of behaviour is quite general as this form of abstract shape theory is related to equational completions; see

* Gildenhuys and Kennison, _Equational completions, model induced triples and pro-objects_, J. Pure Applied Algebra, 4 (1971) 317-346.

This aspect is explored reasonably fully in the book by Cordier and Porter (see below).

A different terminology and slightly different emphasis is often used within the shape theoretic literature as it corresponds more to the geometric intuition needed there, deriving originally from the important classical motivation of Borsuk, [[Sibe Mardesic|Mardešić]], and [[J. Segal|Segal]].



  


## Applications of Shape Theory

### Geometric Topology

### Dynamical Systems

In a [[dynamical system]], the [[attractor|attractors]] are rarely polyhedra and their homotopy properties correspond more nearly to shape theoretic ones than to standard homotopy theoretic ones.  This seems first to have been studied by [[Hastings]] in 1988, (see references) and more recently has been explored in papers by [[José Sanjurjo]] and his coworkers, see below.  Adapting this idea [[Luis Javier Hernandez|Hernandez]], [[Teresa Rivas]] and [[José García Calcines]] have been using ideas developed for [[proper homotopy theory]] and shape involving [[pro-spaces]],  to describe limiting properties of dynamical systems.


## Related concepts

* [[shape fibration]], [[approximate fibration]]


* [[shape]], [[shape modality]], [[shape of an (infinity,1)-topos]]

* [[strong shape theory]], [[Borsuk's shape theory]]

* [[geometric realization]]

* [[topology]]


## References

The original references:

* [[Karol Borsuk]], _Concerning homotopy properties of compacta_, Fund Math. 62 (1968) 223-254

* [[Karol Borsuk]], _Theory of Shape_, Monografie Matematyczne Tom 59, Warszawa 1975 ([mathscinet:0418088](https://mathscinet.ams.org/mathscinet-getitem?mr=0418088))

* [[Karol Borsuk]], [[Jerzy Dydak]], _What is the theory of shape?_, Bulletin of the Australian Mathematical Society, 1980, 22(2), 161-198, ([doi:10.1017/S000497270000647X](https://doi.org/10.1017/S000497270000647X))

* {#MardesicSegal71} [[Sibe Mardesic|S. Mardešić]], [[Jack Segal]], _Shapes of compacta and ANR-systems, Fund. Math. 72 (1971) 41-59 ([dml:214361](https://eudml.org/doc/214361), [pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm72/fm7214.pdf))

* [[Sibe Mardesic|S. Mardešić]], [[Jack Segal]], _Shape theory. The inverse system approach_, North-Holland Mathematical Library, 26. North-Holland, Amsterdam - New York, 1982.

Textbook accounts:

* {#DydakSegal78} [[Jerzy Dydak]], [[Jack Segal]], _Shape Theory_, Lecture Notes in Mathematics, Springer 1978 ([doi:10.1007/BFb0067572](https://link.springer.com/book/10.1007/BFb0067572))

Relation of this classical shape theory to ordinary [[homotopy type]] and to the notion of [[shape of an (infinity,1)-topos|shape of an$\infty$-topos]]:

* {#Lurie09} [[Jacob Lurie]], Section 7.1.6 in: _[[Higher Topos Theory]]_

* {#Hoyois13} [[Marc Hoyois]], Def. 2.3 in: _Higher Galois theory_, Algebraic & Geometric Topology __17__ 1 (2017) 567-643 ([arxiv/1506.07155](https://arxiv.org/abs/1506.07155), [doi:10.2140/agt.2017.17.567](https://doi.org/10.2140/agt.2017.17.567))

See also:

* {#Wang17} Jintao Wang, Theorem 4.6 of: _Theory of Compact Hausdorff Shape_ ([arXiv:1708.07346](https://arxiv.org/abs/1708.07346))

\linebreak

A general [[category theory|category theoretic]]-approach is given in

* W. Holszty&#324;ski, _An extension and axiomatic characterization of Borsuk's theory of shape_, Fund. Math. 70 (1971) no. 2, 157&#8211;168 [pdf](https://www.impan.pl/shop/en/publication/transaction/download/product/79189)


The more or less equivalent pro-object approach was independently developed by Porter in 

* [[Tim Porter|T. Porter]], _&#268;ech homotopy I_, Jour. London Math. Soc., 1, 6, 1973, pp. 429-436 [doi](https://dx.doi.org/10.1112/jlms/s2-6.3.429)

* [[Tim Porter|T. Porter]], _&#268;ech homotopy II_, Jour. London Math. Soc., 2, 6, 1973, pp. 667-675 [doi](https://dx.doi.org/10.1112/jlms/s2-6.4.667)

References relating more to strong shape  theory include:

* D.A. Edwards and H. M. Hastings, (1976), &#268;ech and Steenrod homotopy theories with applications to geometric topology, Lecture Notes in Maths. 542, Springer-Verlag, [pdf](http://www.math.uga.edu/~davide/Cech_and_Steenrod_Homotopy_Theories_with_Applications_to_Geometric_Topology.pdf) 

* J.T. Lisica and [[Sibe Mardesic|S. Mardešić]], Coherent prohomotopy and strong shape theory, Glasnik Mat. 19(39) (1984) 335--399. 

* [[Sibe Mardesic|S. Mardešić]], _Strong shape and homology_, Springer monographs in mathematics, Springer-Verlag. 

* [[Michael Batanin]], [Categorical strong shape theory](http://www.numdam.org/item/CTGDC_1997__38_1_3_0/), Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 38 (1997), no. 1, 3--66.

* [[T. Porter]], _Stability Results for Topological Spaces_, Math. Zeit. 150, 1974, pp. 1-21.

* [[T. Porter]], _Abstract homotopy theory in procategories_, Cahiers Top. G&#233;om. Diff., 17, 1976, pp. 113-124, [numdam](http://archive.numdam.org/article/CTGDC_1976__17_2_113_0.pdf)

* [[T. Porter]],  _Coherent prohomotopical algebra_, [numdam](http://archive.numdam.org/article/CTGDC_1977__18_2_139_0.pdf), Cahiers Top. G&#233;om. Diff. __18__, (1978) pp. 139-179;

* [[T. Porter]], _Coherent prohomotopy theory_, Cahiers Top. G&#233;om. Diff. __19__, (1978) pp. 3-46, [numdam](http://archive.numdam.org/article/CTGDC_1978__19_1_3_0.pdf). 

These last three papers developed a version of the [[BrownAHT]] to pro-categories of simplicial sets and of chain complexes, so as to give [[strong shape theory]] a better foundation and toolbox of homotopical methods. These methods were complementary to those of Edwards and Hastings, (listed above), who used a Quillen model category structure on the pro-category.

References to the categorical forms of shape theory include

* A. Deleanu, P.J. Hilton, _On the categorical shape of a functor_, Fund. Math. 97 (1977) 157 - 176.

* A. Deleanu, P.J. Hilton, _Borsuk's shape and Grothendieck categories of pro-objects_, Math. Proc. Camb. Phil. Soc. 79 (1976) 473-482.


* [[Dominique Bourn]], [[Jean-Marc Cordier]], _Distributeurs et th&#233;orie de la forme_, Cah. Top. G&#233;om. Diff. Cat. **21** no.2 (1980) pp.161-189. ([numdam:CTGDC_1980__21_2_161_0](http://www.numdam.org/item/CTGDC_1980__21_2_161_0), [pdf](http://www.numdam.org/item/CTGDC_1980__21_2_161_0.pdf))

  > (via [[profunctors]])

and

* [[Jean-Marc Cordier|J.-M. Cordier]] and [[Tim Porter|T. Porter]], (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008),

which explores categorical methods in the area. 

The relationship between invariants of $C^*$-algebras and the shape of their spectra was explored in

* {#Blackadar} [[Bruce Blackadar]], _Shape theory for $C^*$-algebras_, Math. Scand. 56 (1985) 249 -  275, [journal link](http://www.mscand.dk/article.php?id=2767).
 


The links are with K-theory and Kasparov's theory. This connection and a related one to 'asymptotic morphisms' is explored in some neat notes by Anderson and Grodal:

* [Noncommutative topology - homotopy functors and E-theory](http://www.math.ku.dk/~jg/papers/etheory.html)

That connection with [[asymptotic morphisms]] is fully explored in the work of [[Marius Dadarlat|Dadarlat]]; see his papers,

* [[Marius Dadarlat|Marius Dādārlat]], _Shape theory and asymptotic morphisms for C$^\ast$-algebras_,  Duke Math. J. 73(3):687-711, 1994, [MR95c:46117](http://www.ams.org/mathscinet-getitem?mr=1262931), [doi](http://dx.doi.org/10.1215/S0012-7094-94-07327-4)
 {#Dadarlat}

* [[Marius Dadarlat|Marius Dādārlat]], Terry A. Loring, _Deformations of topological spaces predicted by E-theory_, in Algebraic methods in operator theory, pages 316-327. Birkh&#228;user 1994. 

For links with dynamical systems see the early paper

*  [[H. M. Hastings]], _Shape theory and dynamical systems_ in M.G.Markely and 
W.Perizzo: The structure of attractors in dynamical systems, Lect. Notes in 
Math. 688 (1978) 150-160. Springer-Verlag. 

and more recently

*  [[Joel W. Robbin]], [[Dietmar A. Salamon]], _Dynamical systems, shape theory and the Conley  index_, Ergodic Theory Dynam. Systems 8 (1988) 375 -  393,

* A. Giraldo, M. A. Mor&#243;n, F. R. Ruiz del Portal, [[J. M. R. Sanjurjo]], _Shape of global attractors in topological spaces_, Nonlinear Analysis 60 (2005) 837 - 847 [doi](https://dx.doi.org/10.1016/j.na.2004.03.036)

* J. J. S&#225;nchez-Gabites, [[J. M. R. Sanjurjo|José M. R. Sanjurjo]], _Shape properties of the boundary of attractors_, Glas. Mat. Ser. III 42(62) (2007), no. 1, 117&#8211;130

*  J. Garc&#237;a Calcines, [[Luis Javier Hernández|L. J. Hernández]] and [[Teresa Rivas|M.T. Rivas]],  _Limit and end functors of dynamical systems via exterior spaces, _ [Preprint (2011)](http://www.unirioja.es/cu/luhernan/puben.html).

[[!redirects shape of a topological space]]
