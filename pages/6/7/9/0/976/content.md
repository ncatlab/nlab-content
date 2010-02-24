

#Contents#
* automatic table of contents goes here
{:toc}

## Motivation and history

While [[homotopy theory]] is suitable for the study of (locally) good [[topological space]]s, it fails to give useful information for 'bad' spaces, whose classical examples include  the [[warsaw.gif:file]], [Sierpinski gasket](http://en.wikipedia.org/wiki/Sierpinski_triangle), [p-adic solenoid](http://en.wikipedia.org/wiki/Solenoid_%28mathematics%29) and so on. Even if our principal interest is in good spaces, bad spaces arise in their study. For example, in the study of dynamical systems on manifolds, an important issue are the attractors of such systems, which are typically fractal sets. The intuitive idea of shape theory is to define invariants of quite general topological spaces by approximating them with 'good' spaces, either by considerations of embedding into good spaces, or by considering abstract inverse systems of good spaces. 

Shape theory was first explicitly introduced by Polish mathematician [Karol Borsuk](http://www-groups.dcs.st-and.ac.uk/~history/Mathematicians/Borsuk.html) in the 1960s. The modern version of shape theory is developed in terms of inverse systems of absolute neighbourhood retracts (ANRs) (which are [[pro-object]]s) introduced in this setup by S. Marde&#353;i&#263;, J. Segal (1971) and independently, in a slightly different form, by [[Tim Porter]] (thesis, 1971). 

Shape theory is a '[[?ech methods|?ech homotopy theory]]', having a similar relationship to &#268;ech homology as homotopy theory based on the singular complex construction has to singular homology. In fact, the origins of both shape theory and strong shape theory go back than further Borsuk's initial papers  to work by [Lefshetz](http://www-groups.dcs.st-and.ac.uk/~history/Mathematicians/Lefschetz.html) and his student, D. Christie (thesis plus article, D.E. Christie, _Net homotopy for compacta_,  Trans. Amer. Math. Soc., 56 (1944) 275--308). Christie considered a 2-truncated form of strong shape theory, categorically this corresponds to a lax or op-lax 2-categorical version of shape theory.
Although many of the initial ideas were developed by Christie, the paper went unnoticed until Borsuk developed his slightly different approach in the 1960s.


For many applications one needs more refined invariants which build up [[strong shape theory]], while sometimes more crude versions may be useful, for example the recent theory of [[coarse shape]]. Strong Shape Theory developed in the 1970s through the work of Edwards and Hastings (lecture notes, see below), Porter, and others.


M. Batanin further elucidated strong shape theory from a categorical and 2-categorical point of view, but his approach is still not much used. His 1997 paper, shows the connections between this theory and a homotopy theory of simplicial [[distributor|distributors]] linked to $A_{\infty}$-categories.

The strong shape theory of compact spaces is related to certain constructions on the corresponding (commutative) $C^*$-algebras of functions.  This is related to the algebraic K-theory of such commutative $C^*$-algebras.  Extensions to non-commutative $C^*$-algebras have been made.

As shape theory is a [[?ech methods|?ech homotopy theory]], its corresponding homology is Cech homlogy, but what is the corresponding construction for strong shape. The answer is Steenrod--Sitnikov homology and this is discussed in Marde&#353;i&#263;'s book, _Strong Shape and Homology_, (see below).  Many of the themes of homotopy coherence and related ideas occur in this theory and this suggests an infinity categorical approach (closely related to Batanin's) may be important.  This seems to be emerging with interpretations of work by Toen and Vezzosi, and by Lurie.

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

A more [[categorical shape theory|categorical form of shape theory]] was studied by Deleanu and Hilton in a series of papers in the 1970s. They consider a more general setting of a functor $K : D \to C$, which in the classical Borsuk case would be the inclusion of the homotopy category of compact [[polytope|polyhedra]] into that of all compact [[metric space]]s. 

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
* K. Borsuk, _Concerning homotopy properties of compacta_, Fund Math. 62 (1968) 223-254
* K. Borsuk, _Theory of Shape_, Monografie Matematyczne Tom 59,Warszawa 1975.

The 'ANR-systems' approach of Marde&#353;i&#263; and Segal appeared in
* S. Marde&#353;i&#263; and J. Segal, _Shapes of compacta and ANR-systems, Fund. Math. 72 (1971) 41-59,

and is fully developed in 

* S. Marde&#353;i&#263;, J. Segal, (1982) Shape Theory, North 
Holland. 

The more or less equivalent pro-object approach was independently developed by Porter in 

* T. Porter, _Cech homotopy I_, Jour. London Math. Soc., 1, 6, 1973, pp. 429-436.
* T. Porter, _Cech homotopy II_, Jour. London Math. Soc., 2, 6, 1973, pp. 667-675.

References relating more to strong shape  theory include:

* D.A. Edwards and H. M. Hastings, (1976), &#268;ech and Steenrod homotopy theories with applications to geometric topology, Lecture Notes in Maths. 542, Springer-Verlag. 
* J.T. Lisica and S. Marde&#353;i&#263;, Coherent prohomotopy and strong shape theory, Glasnik Mat. 19(39) (1984) 335--399. 

* [[Sibe Mardesic|S. Marde?i?]], Strong Shape and Homology, Springer monographs in mathematics, Springer-Verlag. 

* M. A. Batanin, [Categorical strong shape theory](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1997__38_1_3_0), Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 38 (1997), no. 1, 3--66.

* T. Porter, _Stability Results for Topological Spaces_, Math. Zeit. 150, 1974, pp. 1-21.

* T. Porter, [Abstract homotopy theory in procategories](archive.numdam.org/article/CTGDC_1976__17_2_113_0.pdf)
, Cahiers Top. G&#233;om. Diff., 17, 1976, pp. 113-124;

* T. Porter,  [Coherent prohomotopical algebra](archive.numdam.org/article/CTGDC_1977__18_2_139_0.pdf), Cahiers Top.G&#233;om.Diff., 18, (1978) pp. 139-179;

* T. Porter, [Coherent prohomotopy theory](archive.numdam.org/article/CTGDC_1978__19_1_3_0.pdf), Cahiers Top. G&#233;om. Diff., 19, (1978) pp. 3-46. 

These last three papers developed a version of the [[BrownAHT]] to pro-categories of simplicial sets and of chain complexes, so as to give [[strong shape theory]] a better foundation and toolbox of homotopical methods. These methods were complementary to those of Edwards and Hastings, (listed above), who used a Quillen model category structure on the pro-category.

References to the categorical forms of shape theory include

* A. Deleanu and P.J. Hilton, On the categorical shape of a functor, Fund. Math. 97 (1977) 157 - 176.

* A. Deleanu and P.J. Hilton, Borsuk's shape and Grothendieck categories of pro-objects, Math. Proc. Camb. Phil. Soc. 79 (1976) 473-482.

* D.  Bourn and J.-M. Cordier, [Distributeurs et th&#233;orie de la forme](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1980__21_2), Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 21,(1980), no. 2, 161--188.

and

* J.-M. Cordier and T. Porter, (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008),

which explores categorical methods in the area. 

(more)