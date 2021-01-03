
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

While the idea of a [[homotopy type]]  is very suitable for the study of (locally) good [[topological space]]s, the [[weak homotopy type]] fails to give useful information for 'bad' spaces, of which classical examples include  the [[Warsaw Circle]], [Sierpinski gasket](http://en.wikipedia.org/wiki/Sierpinski_triangle), [[p-adic solenoid]] and so on. Even if our initial and principal interest is more often than not in good spaces, bad spaces arise naturally in their study. For example, in the study of dynamical systems on manifolds, an important issue is the study of  the attractors of such systems, which are typically fractal sets, and thus not 'locally nice' at all! The intuitive idea of shape theory is to define invariants of quite general topological spaces by approximating them with 'good' spaces, either by  embedding them into good spaces, and looking at open or polyhedral neighborhoods of them, or by considering abstract inverse systems of good spaces. The two approaches are closely related.

## Idea

If there are few maps from polyhedra (e.g. from spheres) into the space, then the [[weak homotopy type]] may tell too little about the space. 
Therefore one "expands" the space into a successive system of spaces which are good recipients of maps from polyhedra (e.g. absolute neighborhood retracts (ANRs), polyhedra) and one adapts the homotopy theory to such expansions. The analogue of (strong) homotopy type in this setting is the shape of a space; the shape is an invariant of the strong homotopy type and agrees with it on the ANRs for metric spaces and on the polyhedra. It is more crude for other spaces, but more suitable than the weak homotopy type, or more exactly gives complementary information. Instead of embedding a space, one may abstractly expand or resolve the space or its homotopy class into a pro-object in a category of nice spaces. [[Strong shape theory]] is a variant which is closer to the usual kind of  homotopy, is more geometric and has more homotopy theoretic constructions available in its 'toolkit'. It differs by passing to the homotopy category at a later stage in the theory, so one gets homotopy coherent approximating systems rather than homotopy commutative ones. 


## History

Shape theory was first explicitly introduced by Polish mathematician [Karol Borsuk](http://www-groups.dcs.st-and.ac.uk/~history/Biographies/Borsuk.html) in the 1960s, although Christie, a student of Lefshetz, had done some initial development work on the same basic idea much earlier. One of the modern versions of shape theory is developed in terms of inverse systems of absolute neighbourhood retracts (ANRs) (which are [[pro-object]]s in the homotopy category of polyhedra).  These were introduced in this setting by [[Sibe Mardesic|S. Mardešić]], and [[Jack Segal|J. Segal]] (1971) and independently, in a slightly different form, by [[Tim Porter]] (thesis, 1971), using the more combinatorial framework of [[pro-objects]] in the category of simplicial sets. This latter approach also indicated the possible link with the &#233;tale homotopy theory of Artin and Mazur, (Springer Lecture Notes 100).

Shape theory is a '[[Cech methods|&#268;ech homotopy theory]]', having a similar relationship to &#268;ech homology as homotopy theory, based on the singular complex construction, has to singular homology. In fact, as mentioned above, the origins of both shape theory and strong shape theory go back than further Borsuk's initial papers  to work by [Lefshetz](http://www-groups.dcs.st-and.ac.uk/~history/Mathematicians/Lefschetz.html) and his student, D. Christie (thesis plus article, D.E. Christie, _Net homotopy for compacta_,  [Trans. Amer. Math. Soc., 56 (1944) 275--308](www.ams.org/journals/tran/1944-056-00/home.html)). Christie considered a 2-truncated form of strong shape theory, categorically this corresponds to a lax or op-lax 2-categorical version of shape theory.
Although many of the initial ideas were developed by Christie, the paper went unnoticed until Borsuk developed his slightly different approach in the late 1960s.


For many applications one needs more refined invariants which build up [[strong shape theory]], while sometimes more crude versions may be useful, for example the recent theory of [[coarse shape]]. 

Strong Shape Theory developed in the 1970s through the work of Edwards and Hastings (lecture notes, see below), Porter, Quigley, and others.  It has, especially in the approach pioneered by Edwards and Hastings, strong links to [[proper homotopy theory]].  The links are a form of duality related to some of the more geometric duality theorems of classical cohomology.


M. Batanin further elucidated strong shape theory from a categorical and 2-categorical point of view, but his approach is as yet not much used. His 1997 paper, shows the connections between this theory and a homotopy theory of simplicial [[distributor|distributors]] linked to $A_{\infty}$-categories.

The structure of the [[strong shape theory]] of compact spaces is related to certain structure and constructions on the corresponding (commutative) $C^*$-algebras of functions.  These are related to the algebraic K-theory of such commutative $C^*$-algebras.  Extensions to non-commutative $C^*$-algebras have been made; see ([Blackadar](#Blackadar)) and ([Dadarkat](#Dadarlat)) below, for a start.

As shape theory is a [[Čech methods|Čech homotopy theory]], its corresponding homology is Čech homology, but what is the corresponding construction for strong shape? The answer is Steenrod--Sitnikov homology. This is discussed in Marde&#353;i&#263;'s book, _Strong Shape and Homology_, (see below).  Many of the themes of homotopy coherence and related ideas occur in this theory and this suggests an infinity categorical approach (closely related to Batanin's) may be important.  This seems to be emerging with interpretations of work by Toen and Vezzosi, and by Lurie, and perhaps suggests a review of Batanin's work from that new viewpoint.

##Borsuk's shape theory (K. Borsuk, (1968))##
This was the original form and applies to compact metric spaces.  It uses the fact that any compact metric space can be embedded in the [[Hilbert Cube]]. For any such embedded compact metric spaces, $X$ and $Y$, one considers **shape maps** from the collection of open neighbourhoods of $X$ to those of $Y$.  These shape maps are families of continuous maps satisfying a compatibility relationship ' up to homotopy'.  These compose nicely and form the Borsuk shape category.  Two spaces have the same shape if they are isomorphic in this category. Full details of the definition of such shape morphisms are given in the separate entry, [[Borsuk shape theory]]. 

A remarkable and beautiful theorem of Chapman (the Chapman complement theorem) shows that the shape of two compact metric spaces, $X$ and $Y$ embedded in the [[Hilbert cube|pseudo-interior]] of the Hilbert cube, $Q$, have the same shape if and only if their complements $Q\setminus X$ and $Q\setminus Y$ are homeomorphic.

##ANR-systems approach (Marde&#353;i&#263; and Segal (1970))##

Absolute neighborhood retract (ANR)

## Abstract shape category

### Idea

The idea of abstract shape theory is very simple. You have a category, $C$, of objects that you want to study.  (In Borsuk's classical topological case this was the (homotopy) category of compact metric spaces.) You  have a well behaved set of methods that work well for some subcategory, $D$, of those objects (polyhedra in Borsuk's case, where the methods were those of homotopy theory). The categorical idea that can be glimpsed behind the topological constructions of topological shape theory is that of replacing an object $X$ of $C$ with approximations to $X$ by objects of $D$, (so 'approximating' a compact metric space by polyhedra, for instance). Categorically this replaces the object $X$ by the [[comma category]], $(X/D)$, which comes with a projection functor to $D$, which 'records' the approximating $D$-object for each approximation. 
You then use your invariants for objects in $D$ to define (and study) the more general objects in $C$. This does not come without consequences as you obtain new types of maps, (shape maps) between the objects of $C$, namely functors between the comma categories that respect the projections.  The objects of $C$ together with your new shape maps form the shape category of your situation.


### Definition

The **shape category** $Shape(C,D)$ is associated to a pair $(C,D)$ of a category $C$ and a [[dense subcategory]] $D$.

Here _dense subcategory_ is used in the second sense of that term: for every object $X$ in $C$ there is its $D$-expansion, which is the object $\bar{X}$ in the category $pro D$ of [[pro-object]]s in $D$ that is universal ([[initial object|initial]]) with the property that it is equipped with a morphism $X\to\bar{X}$ in $pro D$. 

The shape category $Shape(C,D)$ has 

* the same objects as $C$ 

* its morphisms are equivalence classes of maps between 
  the $D$-expansions.

A more [[categorical shape theory|categorical form of shape theory]] was studied by Deleanu and Hilton in a series of papers in the 1970s. They consider a more general setting of a functor $K : D \to C$, which in the classical Borsuk case would be the inclusion of the homotopy category of compact [[simplicial complex|polyhedra]] into that of all compact [[metric space]]s. 

This was developed further by Bourn and Cordier, and a strong shape version was then found by Batanin.


### Examples

#### Pro-spaces in a shape context

The classical application of shape theoretic idea is to the study of [[topological space]]s that do not have the [[homotopy type]] of a [[CW-complex]]. This is the case obtained from the above general setup by choosing

* $C =$ [[HoTop]]${}_{he}$ the [[homotopy category]] of the category [[Top]] of all [[topological space]]s localised at the **[[homotopy equivalence]]s**;

* $D = Ho(CW Cplx)$ the full [[subcategory]] given by [[CW-complex]]es.

More on this is in the section [Shape theory for topological spaces](ForTopSpaces) below and in [[Cech homotopy]].

#### Profinite groups

Consider the category $C =$[[Grp]] of groups and its subcategory $D$ of finite group. A shape map between two groups is a map between their [[profinite completion of a group|profinite completion]]s.  This sort of behaviour is quite general as this form of abstract shape theory is related to equational completions; see

* Gildenhuys and Kennison, _Equational completions, model induced triples and pro-objects_, J. Pure Applied Algebra, 4 (1971) 317-346.

This aspect is explored reasonably fully in the book by Cordier and Porter (see below).

A different terminology and slightly different emphasis is often used within the shape theoretic literature as it corresponds more to the geometric intuition needed there, deriving originally from the important classical motivation of Borsuk, [[Sibe Mardesic|Mardešić]], and [[J. Segal|Segal]].


## Shape theory for topological spaces {#ForTopSpaces}

### Definition

...


### Strong shape in terms of $(\infty,1)$-sheaves on a space

There is a way to study the [[strong shape theory]] of a [[topological space]] $X$ in terms of [[∞-stack]]s on $X$, i.e. in terms of the [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(X) := Sh_{(\infty,1)}(Op(X))$ on the [[category of open subsets]] of $X$. This is described in

* [[Bertrand Toen]] and [[Gabriele Vezzosi]], _Segal topoi and stacks over Segal categories_ in Proceedings of the
Program _Stacks, Intersection theory and Non-abelian Hodge Theory_ , MSRI, Berkeley, January-May 2002 ([arXiv:math/0212330](http://arxiv.org/abs/math/0212330)) 

and in section 7.1.6 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

For more details see [[shape of an (infinity,1)-topos]].

This theory fits into the general picture above of a subcategory $D\subset C$, where now $C$ is the $(\infty,1)$-category of $(\infty,1)$-toposes, while $D$ is the category of $\infty$-groupoids, regarded as their presheaf $(\infty,1)$-toposes.  Thus, the "shape" of an $(\infty,1)$-topos $X$ is the functor $Hom(X,-)\colon \infty Gpd \to \infty Gpd$.

Alternately, since a [[geometric morphism]] from an $(\infty,1)$-topos $X$ into presheaves on an $\infty$-groupoid $K$ is the same as a [[global section]] of the [[constant ∞-stack]] $L Const(K)$ over $X$, we can also describe this functor as the composite
$$
  \infty Grpd \xrightarrow{LConst}
  Sh_{(\infty,1)}(X)
  \xrightarrow{\Gamma}
  \infty Grpd
  \,.
$$
Thus, we can equivalently describe the shape of $X$ by mapping out of it into topological spaces _over_ $X$ that are at least fiberwise nice topological spaces: in other words, to look at $\infty$-[[covering space]]s over $X$.

Now, for a [[small category|small]] [[(∞,1)-category]] $C$, a functor $C \to \infty Grpd$ that preserves finite limits may be thought of as a [[pro-object]] in $C$.  Now $\infty Gpd$ is not small, but one may hope that the functors $Shape(X)\colon \infty Gpd \to \infty Gpd$ arising in this way are determined by a small amount of data, and thus give honest pro-$\infty$-groupoids.

We can, if we wish, define for the nonce
$$
  Pro(\infty Grpd) \subset Func(\infty Grpd, \infty Grpd)^{op}
$$
to be the fully subcategory of [[(∞,1)-functor]]s that preserve finite limits, although as discussed above this is not quite correct.  We call the objects in $Pro(\infty Grpd)$ **pro-spaces** or **shapes**.  Notice that by the [[homotopy hypothesis]]-theorem, we can think here of $\infty Grpd \simeq Top_{cg,wH}$ as the category of [[nice topological space]]s, considered up to [[homotopy equivalence]].

The first description of shapes makes it obviously functorial in [[geometric morphisms]] of $(\infty,1)$-toposes.  This can be seen from the second definition as well: given $(f^* \dashv f_*) \colon \mathbf{H} \to \mathbf{K}$, the [[unit of an adjunction|unit]] $Id_{\mathbf{K}} \to f_* \circ f^*$ induces a transformation

$$
  \Gamma_{\mathbf{K}}\circ LConst_{\mathbf{K}}

  \to 
  \Gamma_{\mathbf{K}}
   \circ 
    f_*
    \circ   
    f^* 
   \circ  LConst_{\mathbf{K}}
  \simeq
  \Gamma_{\mathbf{H}}\circ LConst_{\mathbf{H}}
$$

that may be regarded as a morphism of shapes

$$
  Shape(f) : Shape(\mathbf{K}) \to Shape(\mathbf{H})
  \,.
$$

We say the geometric morphism $f$ is a **shape invariance** if $Shape(f)$ is an equivalence of pro-spaces.

+-- {: .un_prop }
###### Proposition

For $f : X \to Y$ a continuous map of [[paracompact space]]s, the induced geometric morphism $(f^* \dashv f*) : Sh_{(\infty,1)}(X) \to Sh_{(\infty,1)}(Y)$ is a shape equivalence, precisely if for each [[CW-complex]] $K$ the map 

$$
  Top(Y,K) \to Top(X,K)
$$

is an equivalence.


=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 7.1.6.8]].

=--


##Applications of Shape Theory

###Geometric Topology

### Dynamical Systems

In a [[dynamical system]], the [[attractor]]s are rarely polyhedra and their homotopy properties correspond more nearly to shape theoretic ones than to standard homotopy theoretic ones.  This seems first to have been studied by [[Hastings]] in 1988, (see references) and more recently has been explored in papers by [[José Sanjurjo]] and his coworkers, see below.  Adapting this idea [[Luis Javier Hernandez|Hernandez]], [[Teresa Rivas]] and [[José García Calcines]] have been using ideas developed for [[proper homotopy theory]] and shape involving [[pro-spaces]],  to describe limiting properties of dynamical systems.


## Related concepts

* [[shape fibration]], [[approximate fibration]]


* [[shape]], [[shape modality]], [[shape of an (infinity,1)-topos]]

* [[strong shape theory]], [[Borsuk's shape theory]]

* [[geometric realization]]

* [[topology]]


## References

The original references for the shape theory of metric compacta are:

* [[Karol Borsuk]], _Concerning homotopy properties of compacta_, Fund Math. 62 (1968) 223-254

* [[Karol Borsuk]], _Theory of Shape_, Monografie Matematyczne Tom 59, Warszawa 1975 ([mathscinet:0418088](https://mathscinet.ams.org/mathscinet-getitem?mr=0418088))

* [[Karol Borsuk]], [[Jerzy Dydak]], _What is the theory of shape?_, Bulletin of the Australian Mathematical Society, 1980, 22(2), 161-198, ([doi:10.1017/S000497270000647X](https://doi.org/10.1017/S000497270000647X))

Textbook accounts:

* {#DydakSegal78} [[Jerzy Dydak]], [[Jack Segal]], _Shape Theory_, Lecture Notes in Mathematics, Springer 1978 ([doi:10.1007/BFb0067572](https://link.springer.com/book/10.1007/BFb0067572))

Relation of shape to ordinary [[homotopy type]]:

* [[Jacob Lurie]], Section 7.1.6 in: _[[Higher Topos Theory]]_

* {#Wang17} Jintao Wang, Theorem 4.6 of: _Theory of Compact Hausdorff Shape_ ([arXiv:1708.07346](https://arxiv.org/abs/1708.07346))

A general [[category theory|category theoretic]]-approach is given in

* W. Holszty&#324;ski, _An extension and axiomatic characterization of Borsuk's theory of shape_, Fund. Math. 70 (1971) no. 2, 157&#8211;168 [pdf](https://www.impan.pl/shop/en/publication/transaction/download/product/79189)

The 'ANR-systems' approach of Marde&#353;i&#263; and Segal appeared a bit later in

* [[Sibe Mardesic|S. Mardešić]], [[Jack Segal]], _Shapes of compacta and ANR-systems, Fund. Math. 72 (1971) 41-59,

and is fully developed in 

* [[Sibe Mardesic|S. Mardešić]], [[Jack Segal]], _Shape theory. The inverse system approach_, North-Holland Mathematical Library, 26. North-Holland, Amsterdam - New York, 1982.

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

* D.  Bourn, [[Jean-Marc Cordier|J.-M. Cordier]], _Distributeurs et th&#233;orie de la forme_, Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 21,(1980), no. 2, 161--188, [numdam](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1980__21_2).

and

* [[Jean-Marc Cordier|J.-M. Cordier]] and [[Tim Porter|T. Porter]], (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008),

which explores categorical methods in the area. 

The relationship between invariants of $C^*$-algebras and the shape of their spectra was explored in

* [[Bruce Blackadar]], _Shape theory for $C^*$-algebras_, Math. Scand. 56 (1985) 249 -  275, [journal link](http://www.mscand.dk/article.php?id=2767).
 {#Blackadar}


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

*  [[Joel W. Robbin]], Dietmar A. Salamon, _Dynamical systems, shape theory and the Conley  index_, Ergodic Theory Dynam. Systems 8 (1988) 375 -  393,

* A. Giraldo, M. A. Mor&#243;n, F. R. Ruiz del Portal, [[J. M. R. Sanjurjo]], _Shape of global attractors in topological spaces_, Nonlinear Analysis 60 (2005) 837 - 847 [doi](https://dx.doi.org/10.1016/j.na.2004.03.036)

* J. J. S&#225;nchez-Gabites, [[J. M. R. Sanjurjo|José M. R. Sanjurjo]], _Shape properties of the boundary of attractors_, Glas. Mat. Ser. III 42(62) (2007), no. 1, 117&#8211;130

*  J. Garc&#237;a Calcines, [[Luis Javier Hernández|L. J. Hernández]] and [[Teresa Rivas|M.T. Rivas]],  _Limit and end functors of dynamical systems via exterior spaces, _ [Preprint (2011)](http://www.unirioja.es/cu/luhernan/puben.html).

[[!redirects shape of a topological space]]
