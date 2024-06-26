
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

In [[topology]], the [[fundamental theorem of covering spaces]] says that for a sufficiently nice [[topological space]], the [[fundamental group]] at a point can be reconstructed as a group of [[deck transformations]] of the [[universal covering space]], which is the same as the [[automorphism]]s of the [[fiber]] over that point of the projection map. The deck transformations are [[monodromies]] induced by loops at the base point. 

The functor which assigns to a point the fiber over it, generalizes to [[fiber functors]] in the [[Tannaka duality|Tannakian formalism]] of Grothendieck which defines in more general setups the [[fundamental groupoid]] as the group of automorphisms of the appropriate fiber functor. See also at *[[fundamental group of a topos]]*.

Now, Grothendieck's [[Galois theory]] means to generalize to the context of [[schemes]] this familiar correspondence between

[[covering spaces]] of $X$ : $\pi_1(X)$[[action|-sets]]

for  [[locally path-connected space|locally path connected]], [[semi-locally simply connected space|semilocally simply connected]] [[topological spaces]] $X$. 

The objects on the left are not difficult to define for schemes (at least naively -- one really needs trivialisations over &#233;tale [[coverage|covers]]), but it may not be entirely immediate what the [[fundamental group]] defined in terms of loops should be.

The reason Galois's name is attached to this theory is that in the case of the scheme $Spec(k)$ associated to a field $k$, the objects corresponding to the covering spaces are simply the schemes $Spec(k')$ for [[field extension]]s $k'$, and the fundamental group of $Spec(k)$ is the [[Galois group]] of $k$.  More generally Grothendieck's Galois theory assigns to any scheme $X$ an [[algebraic fundamental group]] $\pi_1(X)$, which is a [[profinite group]].

### Generalizations

The basic idea of Grothendieck's Galois theory may be extended to objects in an [[topos]] -- leading to a notion of [[fundamental group of a topos]] --  and then further to objects in any [[(∞,1)-topos]]. For more on this see [[homotopy group of an ∞-stack]].

## Details

### Preliminaries

+-- {: .un_defn}
###### Definition
Given an arrow $f:x \to y$ in a category $C$ the _category of arrows compatible with $f$_, denoted $Comp(f)$ is the full [[subcategory]] of the [[undercategory]] $x \downarrow C$ on the arrows that [[coequalizer|coequalize]] the same pairs $g,h:w\rightrightarrows x$ that $f$ does.
=--

+-- {: .un_defn}
###### Definition
An arrow $f:x\to y$ in a category $C$ is a _[[strict epimorphism]]_ if it is [[initial object|initial]] in $Comp(f)$.
=--

It is not obvious, but a strict epimorphism is an epimorphism.

### Grothendieck's axioms

In what follows, Let $C$ be a [[category]] and $F:C \to Set$ a [[functor]]. The axioms presented here are as in

J. P. Murre, _Lectures on an introduction to Grothendieck's theory of the fundamental group_, Tata Inst. of Fund. Res. Lectures on Mathematics 40, Bombay, 1967. iv+176+iv pp.

and copied also in 

* [[Eduardo Dubuc]], C. S. de la Vega _On the Galois theory of Grothendieck_, Bol. Acad. Nac. Cienc. (Cordoba) **65** (2000) 111--136. [arXiv](http://arxiv.org/abs/math.CT/0009145)

Some terminology: $X\in C$ is called _finite_ if $F(X)$ is a finite [[set]]. Let $\int_F C$ denote the [[category of elements]] of $F$, in which an object $(X,a)$ is called finite if $X$ is finite.

* **G0)** The full subcategory of $\int_F C$ on the finite objects is [[cofinal subcategory|cofinal]].

* **G1)** $C$ has all finite [[limit]]s

* **G2)** $C$ has an [[initial object]], finite [[coproduct]]s and [[quotient object|quotients]] by finite [[group]]s

* **G3)** Given $f:x\to z$ in $C$ there is a factorisation $x \stackrel{e}{\to} y \stackrel{i}{\to} z$ where $e$ is a strict epimorphism and $i$ is a mono. Also, $y$ is assumed to be a [[coproduct|direct sum]]mand of $z$.

* **G4)** $F$ preserves finite limits

* **G5)** $F$ preserves initial object, finite sums, quotients by finite group actions and sends strict epimorphisms to surjections

* **G6)** $F$ reflects isomorphisms

***

The functor $F$ is called the *fibre functor*, and the pair $(C,F)$ is sometimes called a *Galois category*.


It follows from the axioms that $F$ is a [[pro-representable functor]]. The [[automorphism group]] of the [[pro-object]] $P$ representing $F$ is (should be. I'm not familiar enough with pro-objects) a [[profinite group]] $\pi$. This acts on $F(X) = [P,-]$ by precomposition (talking out of my depth here -- it's getting a bit vague) and so $F$ lifts to a functor to $\pi-Set$, and Grothendieck's result is that this functor is an [[equivalence of categories]].

There are several modifications one can make the above. In the case that $C$ is the category of covering spaces of a nice enough space, the functor $F$ is [[representable functor|representable]] by the [[universal covering space]], and so there is a 'representable' version of the above, not needing to utilise profinite groups. One can also consider just the connected-objects version, and end up with an equivalence to the category of _[[transitive action|transitive]]_ $\pi$-sets.

## The classical case of fields

Even for the classical case of the inclusion of [[field]]s, Grothendieck's Galois theorem gives more general statement than the previously known. This is the Grothendieck's version of the Galois correspondence theorem for fields:

Let $K \subset L$ be a finite dimensional [[Galois extension]] of fields. Let $Gal[L : K]$ denote the group of $K$-automorphisms of $L$ and $Gal [L : K]-finSet$ the category of finite $Gal[L : K]$-sets. By $SplitfinAlg_K(L)$ denote the finite dimensional $K$-algebras which are split over $L$; here $L$ itself is an object. Consider the [[representable functor]] $h_L = Hom_K(-,L):SplitfinAlg_K(L)\to Set$. It takes values in the [[subcategory]] of finite sets and it comes with a canonical $Gal[L : K]$-action. In other words, this functor factors through $Gal [L : K]-finSet$. Moreover, the corresponding functor 

$$
SplitfinAlg_K(L)\to Gal [L : K]-finSet
$$ 

is an [[equivalence of categories]]. 

There is an infinitary version as well, generalizing the classical Galois theorem on infinitary Galois extensions. 

Thus let $K\subset L$ be an arbitrary Galois extension. Now $Gal[L:K]$ denotes the profinite Galois group and $Gal[L:K]-profinSpace$ the category or profinite $Gal[L:K]$-spaces. $SplitAlg_K(L)$ denotes the category of $K$-algebras split over $L$ (possible infinite-dimensional). Then there is a canonical anti-equivalence of categories

$$
SplitAlg_K(L)\to Gal [L : K]-profinSpace
$$

(factorizing a profinite-space version of the representable functor $Hom_K(-,L)$).  

A special case of this is the following: the category of [[étale scheme|étale k-schemes]] reps. [[étale group scheme|étale group schemes]] for a field $k$ is equivalent to the category of sets equipped with an [[action]] of the [[absolute Galois group]] reps. to the category of [[Galois module|Galois modules]] of the absolute Galois group.

## Galois theorem for locales and topoi

Let $E$ be a [[Grothendieck topos]]. Then there exist an open [[localic groupoid]] $G$ such that $E$ is equivalent to the category of &#233;tale presheaves over $G$. ([Joyal & Tierney 1984](#JoyalTierney84), see also at *[[classifying topos of a localic groupoid]]*).


## Related entries

* [[classifying topos of a localic groupoid]]

## References

The original development of the theory by [[Grothendieck]]  is in 

* [[Alexander Grothendieck]], (1971), *[[SGA1]] -- Revetements  &#233;tales et groupe fondamental*, Lecture Notes in Maths. 224, Springer-Verlag. 

See also:

* J. P. Murre, _Lectures on an introduction to Grothendieck's theory of the fundamental group_, Tata Inst. of Fund. Res. Lectures on Mathematics _40_, Bombay, 1967. iv+176+iv pp. 

* {#JoyalTierney84} [[André Joyal]], [[Myles Tierney]], *An extension of the Galois theory of Grothendieck*,  Mem. Amer. Math. Soc. **309** (1984) &lbrack;[ISBN:978-1-4704-0722-3](https://bookstore.ams.org/memo-51-309)&rbrack;


A more recent treatment can be found in

* [[Eduardo Dubuc]], C. S. de la Vega, _On the Galois theory of Grothendieck_, Bol. Acad. Nac. Cienc. (Cordoba) **65** (2000) 111--136. [arXiv:math.CT/0009145](http://arxiv.org/abs/math.CT/0009145)

and more related categorical and topos theoretic aspects in

* [[Eduardo Dubuc]], _Localic Galois theory_, Adv. Math. __175__:1 (2003), 144&#8211;167 <a href="http://dx.doi.org/10.1016/S0001-8708(02)00046-4">doi</a>; _On the representation theory of Galois and atomic topoi_, JPAA __186__:3 (2004) 233&#8211;275 <a href="http://dx.doi.org/10.1016/S0022-4049(03)00141-5">doi</a>

A very approachable account is given in 

* Marco Ant&#242;nio Delgado Robalo, _Galois theory towards dessins d'enfants_, masters thesis, Lisboa 2009, [pdf](https://fenix.tecnico.ulisboa.pt/downloadFile/395139415315/dissertacao.pdf)

(This has the advantage of looking towards Grothendieck's [[children's drawing|dessins d'enfants]].)

Some basic intuitions are explained in 

* Pierre Cartier, _A mad day's work: from Grothendieck to Connes and Kontsevich The evolution of concepts of space and symmetry_, Bull. Amer. Math. Soc. __38__ (2001), 389-408, [pdf](http://www.ams.org/bull/2001-38-04/S0273-0979-01-00913-2/S0273-0979-01-00913-2.pdf)

The construction for general [[topos]]es is described in section 8.4 of

* [[Peter Johnstone]], _Topos theory_, Academic Press (1977)

and, a current state-of-the-art description is in 

* [[Marta Bunge]], _Galois groupoids and covering morphisms in topos theory_,  Galois theory, Hopf algebras, and semiabelian categories,  131--161, Fields Inst. Commun. __43__, Amer. Math. Soc., Providence, RI, 2004, [links](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.15.7071).

A modern approach from classical via Grothendieck up to [[categorical Galois theory]] based on precategories and adjunctions is in 

* [[Francis Borceux]], [[George Janelidze]], _[[Galois Theories]]_, Cambridge Studies in Adv. Math. __72__, 2001. xiv+341 pp.

The application of a general Tannakian theorem of Saavaedra Rivano, as corrected by Deligne, to the "[[differential Galois theory]]" for differential instead of algebraic equations is in the last chapter of Deligne's [[Catégories Tannakiennes]].

* [[George Janelidze]], Dietmar Schumacher, [[Ross Street]], _Galois theory in variable categories_, Applied Categorical Structures __1__, Number 1, 103-110, DOI: [10.1007/BF00872989](https://doi.org/10.1007/BF00872989)
* Federico G. Lastaria, _On separable algebras in Grothendieck Galois theory_, Le Matematiche 51:3, 1996, [link](http://www.dmi.unict.it/ojs/index.php/lematematiche/article/view/464/0)


[[!redirects Grothendieck Galois theory]]
[[!redirects Grothendieck's Galois theory]]
[[!redirects Grothendieck-Galois theory]]
[[!redirects Grothendieck--Galois theory]]


category: Galois theory