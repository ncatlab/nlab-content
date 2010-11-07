

#Contents#
* automatic table of contents goes here
{:toc}

## Motivation and history

While [[homotopy theory]] is suitable for the study of (locally) good [[topological space]]s, it fails to give useful information for 'bad' spaces, of which classical examples include  the [[Warsaw Circle]], [Sierpinski gasket](http://en.wikipedia.org/wiki/Sierpinski_triangle), [p-adic solenoid](http://en.wikipedia.org/wiki/Solenoid_%28mathematics%29) and so on. Even if our initial and principal interest is in good spaces, bad spaces arise naturally in their study. For example, in the study of dynamical systems on manifolds, an important issue is the study of  the attractors of such systems, which are typically fractal sets, and thus not 'locally nice' at all! The intuitive idea of shape theory is to define invariants of quite general topological spaces by approximating them with 'good' spaces, either by  embedding them into good spaces, and looking at open or polyhedral neighborhoods of them, or by considering abstract inverse systems of good spaces. The two approaches are closely related.

Shape theory was first explicitly introduced by Polish mathematician [Karol Borsuk](http://www-groups.dcs.st-and.ac.uk/~history/Biographies/Borsuk.html) in the 1960s. The modern version of shape theory is developed in terms of inverse systems of absolute neighbourhood retracts (ANRs) (which are [[pro-object]]s) introduced in this setup by [[Sibe Mardesic|S. Marde?i?]], and [[Jack Segal|J. Segal]] (1971) and independently, in a slightly different form, by [[Tim Porter]] (thesis, 1971), using the more combinatorial framework of [[pro-objects]] in the category of simplicial sets. 

Shape theory is a '[[Cech methods|?ech homotopy theory]]', having a similar relationship to &#268;ech homology as homotopy theory, based on the singular complex construction, has to singular homology. In fact, the origins of both shape theory and strong shape theory go back than further Borsuk's initial papers  to work by [Lefshetz](http://www-groups.dcs.st-and.ac.uk/~history/Mathematicians/Lefschetz.html) and his student, D. Christie (thesis plus article, D.E. Christie, _Net homotopy for compacta_,  Trans. Amer. Math. Soc., 56 (1944) 275--308). Christie considered a 2-truncated form of strong shape theory, categorically this corresponds to a lax or op-lax 2-categorical version of shape theory.
Although many of the initial ideas were developed by Christie, the paper went unnoticed until Borsuk developed his slightly different approach in the 1960s.


For many applications one needs more refined invariants which build up [[strong shape theory]], while sometimes more crude versions may be useful, for example the recent theory of [[coarse shape]]. 

Strong Shape Theory developed in the 1970s through the work of Edwards and Hastings (lecture notes, see below), Porter, and others.  It has, especially in the approach pioneered by Edwards and Hastings, strong links to [[proper homotopy theory]].  The links are a form of duality related to some of the more geometric duality theorems of classical cohomology.


M. Batanin further elucidated strong shape theory from a categorical and 2-categorical point of view, but his approach is as yet not much used. His 1997 paper, shows the connections between this theory and a homotopy theory of simplicial [[distributor|distributors]] linked to $A_{\infty}$-categories.

The structure of the [[strong shape theory]] of compact spaces is related to certain structure and constructions on the corresponding (commutative) $C^*$-algebras of functions.  These are related to the algebraic K-theory of such commutative $C^*$-algebras.  Extensions to non-commutative $C^*$-algebras have been made; see the papers by Blackadar and [[Marius Dadarlat|Dadarlat]] below, for a start.

As shape theory is a [[?ech methods|?ech homotopy theory]], its corresponding homology is Cech homology, but what is the corresponding construction for strong shape. The answer is Steenrod--Sitnikov homology. This is discussed in Marde&#353;i&#263;'s book, _Strong Shape and Homology_, (see below).  Many of the themes of homotopy coherence and related ideas occur in this theory and this suggests an infinity categorical approach (closely related to Batanin's) may be important.  This seems to be emerging with interpretations of work by Toen and Vezzosi, and by Lurie, and perhaps suggests a review of Batanin's work from that new viewpoint.

##Borsuk's shape theory (K. Borsuk, (1968))##
This was the original form and applies to compact metric spaces.  It uses the fact that any compact metric space can be embedded in the [[Hilbert Cube]]. For any such embedded compact metric spaces, $X$ and $Y$, one considers **shape maps** from the collection of open neighbourhoods of $X$ to those of $Y$.  These shape maps are families of continuous maps satisfying a compatibility relationship ' up to homotopy'.  These compose nicely and form the Borsuk shape category.  Two spaces have the same shape if they are isomorphic in this category. Full details of the definition of such shape morphisms are given in the separate entry, [[Borsuk shape theory]]. 

A remarkable and beautiful theorem of Chapman (the Chapman complement theorem) shows that the shape of two compact metric spaces, $X$ and $Y$ embedded in the [[Hilbert cube|pseudo-interior]] of the Hilbert cube, $Q$, have the same shape if and only if their complements $Q\setminus X$ and $Q\setminus Y$ are homeomorphic.

##ANR-systems approach (Marde&#353;i&#263; and Segal (1970))##
## Abstract shape category

### Idea

The idea of abstract shape theory is very simple. You have a category, $C$, of objects that you want to study.  (In Borsuk's classical topological case this was the (homotopy) category of compact metric spaces.) You  have a well behaved set of methods that work well for some subcategory, $D$, of those objects (polyhedra in Borsuk's case, where the methods were those of homotopy theory). The categorical idea that can be glimpsed behind the topological constructions of topological shape theory is that of replacing an object $X$ of $C$ with approximations to $X$ by objects of $D$, (so 'approximating' a compact metric space by polyhedra, for instance). Categorically this replaces the object $X$ by the [[comma category]], $(X/D)$, which comes with a projection functor to $D$, which 'records' the approximating $D$-object for each approximation. 
You then use your invariants for objects in $D$ to define (and study) the more general objects in $C$. This does not come without consequences as you obtain new types of maps, (shape maps) between the objects of $C$, namely functors between the comma categories that respect the projections.  The objects of $C$ together with your new shape maps for the shape category of your situation.


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

A different terminology and slightly different emphasis is often used within the shape theoretic literature as it corresponds more to the geometric intuition needed there, deriving originally from the important classical motivation of Borsuk, [[Sibe Marde?i?|Marde?i?]], and [[J. Segal|Segal]].


## Shape theory for topological spaces {#ForTopSpaces}

### Definition

...


### Strong shape in terms of $(\infty,1)$-sheaves on a space

There is a way to study the strong shape theory of a topological space $X$ in terms of [[∞-stack]]s on $X$, i.e. in terms of the [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(X) := Sh_{(\infty,1)}(Op(X))$ on the [[category of open subsets]] of $X$. This is described in

* [[Bertrand Toen]] and [[Gabriele Vezzosi]], _Segal topoi and stacks over Segal categories_ in Proceedings of the
Program _Stacks, Intersection theory and Non-abelian Hodge Theory_ , MSRI, Berkeley, January-May 2002 ([arXiv:math/0212330](http://arxiv1.library.cornell.edu/abs/math/0212330)) 

and in section 7.1.6 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

For more details see [[shape of an (infinity,1)-topos]].

The idea here is to analyse $X$ by, roughly, mapping _out_ of it into topological spaces _over_ $X$ that are at least fiberwise nice topological spaces: in other words, to look at $\infty$-[[covering space]]s over $X$.

For each $\infty$-groupoid $K$ let $LConst_K$ be the corresponding [[constant ∞-stack]] over $X$ and let $\Gamma(LConst_K) \in \infty Grpd$ be its [[global section]]s, i.e. the $\infty$-groupoid of maps from $X$ to the $\infty$-[[covering space]] represented by $LConst_K$.

This operation provides an endofunctor

$$
  \infty Grpd \stackrel{LConst}{\to}
  Sh_{(\infty,1)}(X)
  \stackrel{\Gamma}{\to}
  \infty Grpd
  \,.
$$

And this functor preserves finite [[limit]]s: that's because the pair

$$
  (LConst \dashv \Gamma) : Sh_{(\infty,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}
  \infty Grpd
$$

is the terminal [[global section]] [[geometric morphism]] of [[(∞,1)-topos]]es and so $LConst$ preserves finite limits. $\Gamma$, being the [[right adjoint]] preserves of course all limits.

For a [[small category|small]] [[(∞,1)-category]] $C$, a functor $C \to \infty Grpd$ that preserves finite limits may be thought of as a [[pro-object]] in $C$. Motivated by this observation it makes sense to set

$$
  Pro(\infty Grpd) \subset Func(\infty Grpd, \infty Grpd)^{op}
$$

on those [[(∞,1)-functor]]s that preserve finite limits. Call an object in $Pro(\infty Grpd)$ a **pro-space** or **shape**. Notice that by the [[homotopy hypothesis]]-theorem we should think here of $\infty Grpd \simeq Top_{cg,wH}$ as the category of [[nice topological space]]s.

Then the above constuction assigns to each $X \in Top$ its strong **shape**

$$
  Shape(X) := \Gamma \circ LConst \in Pro(\infty Grpd)
  \,.
$$

Given a [[geometric morphism]] 

$$
  (f^* \dashv f_*) : \mathbf{H} \to \mathbf{K}
$$

of [[(∞,1)-topos]]es, the unit $Id_{\mathbf{K}} \to f_* \circ f^*$ of the adjunction induces a transformation

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

The geometric morphism $f$ is a **shape invariance** if $Shape(f)$ is an equivalence of pro-spaces.

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

## References

See also $n$lab entries [[shape fibration]], [[approximate fibration]], ... and references 

The original references for the shape theory of metric compacta are: 
* [[K. Borsuk]], _Concerning homotopy properties of compacta_, Fund Math. 62 (1968) 223-254
* [[K. Borsuk]], _Theory of Shape_, Monografie Matematyczne Tom 59,Warszawa 1975.

The 'ANR-systems' approach of Marde&#353;i&#263; and Segal appeared in

* [[Sibe Mardesic|S. Marde?i?]] and J. Segal, _Shapes of compacta and ANR-systems, Fund. Math. 72 (1971) 41-59,

and is fully developed in 

* [[Sibe Mardesic|S. Marde?i?]], J. Segal, (1982) Shape Theory, North 
Holland. 

The more or less equivalent pro-object approach was independently developed by Porter in 

* [[Tim Porter|T. Porter]], _Cech homotopy I_, Jour. London Math. Soc., 1, 6, 1973, pp. 429-436.
* [[Tim Porter|T. Porter]], _Cech homotopy II_, Jour. London Math. Soc., 2, 6, 1973, pp. 667-675.

References relating more to strong shape  theory include:

* D.A. Edwards and H. M. Hastings, (1976), &#268;ech and Steenrod homotopy theories with applications to geometric topology, Lecture Notes in Maths. 542, Springer-Verlag, [pdf](http://www.math.uga.edu/~davide/Cech_and_Steenrod_Homotopy_Theories_with_Applications_to_Geometric_Topology.pdf) 
* J.T. Lisica and [[Sibe Mardesic|S. Marde?i?]], Coherent prohomotopy and strong shape theory, Glasnik Mat. 19(39) (1984) 335--399. 

* [[Sibe Mardesic|S. Marde?i?]], _Strong shape and homology_, Springer monographs in mathematics, Springer-Verlag. 

* [[Michael Batanin]], [Categorical strong shape theory](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1997__38_1_3_0), Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 38 (1997), no. 1, 3--66.

* [[Tim Porter]], _Stability Results for Topological Spaces_, Math. Zeit. 150, 1974, pp. 1-21.

* [[T. Porter]], [Abstract homotopy theory in procategories](archive.numdam.org/article/CTGDC_1976__17_2_113_0.pdf)
, Cahiers Top. G&#233;om. Diff., 17, 1976, pp. 113-124;

* [[T. Porter]],  [Coherent prohomotopical algebra](archive.numdam.org/article/CTGDC_1977__18_2_139_0.pdf), Cahiers Top.G&#233;om.Diff., 18, (1978) pp. 139-179;

* [[T. Porter]], [Coherent prohomotopy theory](archive.numdam.org/article/CTGDC_1978__19_1_3_0.pdf), Cahiers Top. G&#233;om. Diff., 19, (1978) pp. 3-46. 

These last three papers developed a version of the [[BrownAHT]] to pro-categories of simplicial sets and of chain complexes, so as to give [[strong shape theory]] a better foundation and toolbox of homotopical methods. These methods were complementary to those of Edwards and Hastings, (listed above), who used a Quillen model category structure on the pro-category.

References to the categorical forms of shape theory include

* A. Deleanu, P.J. Hilton, _On the categorical shape of a functor_, Fund. Math. 97 (1977) 157 - 176.

* A. Deleanu, P.J. Hilton, _Borsuk's shape and Grothendieck categories of pro-objects_, Math. Proc. Camb. Phil. Soc. 79 (1976) 473-482.

* D.  Bourn, [[Jean-Marc Cordier|J.-M. Cordier]], [Distributeurs et th&#233;orie de la forme](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1980__21_2), Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 21,(1980), no. 2, 161--188.

and

* [[Jean-Marc Cordier|J.-M. Cordier]] and [[Tim Porter|T. Porter]], (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008),

which explores categorical methods in the area. 

The relationship between invariants of $C^*$-algebras and the shape of their spectra was explored in

* B. A. Blackadar, _Shape theory for $C^*$-algebras_, Math. Scand. 56 (1985) 249 -  275, [journal link](http://www.mscand.dk/article.php?id=2767).

The links are with K-theory and Kasparov's theory. This connection and a related one to 'asymptotic morphisms' is explored in some neat notes by Anderson and Grodal:

* [Noncommutative topology - homotopy functors and E-theory](http://www.math.ku.dk/~jg/papers/etheory.html)

That connection with [[asymptotic morphisms]] is fully explored in the work of [[Marius Dadarlat|Dadarlat]]; see his papers,

* [[Marius Dadarlat|Marius D?d?rlat]], _Shape theory and asymptotic morphisms for C*-algebras_,  Duke Math. J., 73(3):687-711, 1994.
* [[Marius Dadarlat|Marius D?d?rlat]], Terry A. Loring, _Deformations of topological spaces predicted by E-theory_, in Algebraic methods in operator theory, pages 316-327. Birkh&#228;user 1994. 