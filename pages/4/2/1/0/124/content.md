

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents #
* table of contents
{:toc}

## Idea 
 {#Idea}

There are various different perspectives on the notion of _topos_.   One is that a topos is a [[category]] that looks like a category of [[space]]s that sit by [[local homeomorphism]]s over a given base [[space]]: all spaces that are _locally modeled on_ a given base space.

The archetypical class of examples are [[sheaf topos]]es $Sh(X) = Et(X)$ over a [[topological space]] $X$: these are the categories of [[étale space]]s over $X$, topological spaces $Y$ that are equipped with a [[local homeomorphisms]] $Y \to X$. 

When $X = *$ is the [[point]], this is just the category [[Set]] of all [[sets]]: spaces that are _modeled on the point_ . This is the archetypical topos itself. 

What makes the notion of topos powerful is the following fact: even though the general topos contains objects that are considerably different from and possibly considerably richer than plain sets and even richer than &#233;tale spaces over a topological space, the general abstract [[category theory|category theoretic]] properties of every topos are essentially the same as those of [[Set]]. For instance in every topos all small [[limits]] and [[colimits]] exist and it is [[cartesian closed category|cartesian closed]] (even [[locally cartesian closed category|locally]]). This means that a large number of constructions in [[Set]] have immediate analogs [[internalization|internal to]] every topos, and the analogs of the statements about these constructions that are true in $Set$ are true in _every_ topos. 

On the one hand this may be thought of as saying that toposes are _very nice categories of spaces_ in that whatever construction on spaces one thinks of 
-- for instance formation of [[quotient]]s or of [[fiber product]]s or of [[mapping space]]s --
the resulting space with the expected general abstract properties will exist in the topos. In this sense toposes are _convenient categories_ for geometry -- as in: [[convenient category of topological spaces]], but even more convenient than that.

On the other hand, by de-emphasizing the geometric interpretation of their objects and just using their good abstract properties, this means that toposes are contexts with a powerful [[internal logic]]. The internal logic of toposes is [[intuitionistic logic|intuitionistic]] [[higher order logic]]. This means that, while the [[law of excluded middle]] and the [[axiom of choice]] may fail, apart from that, every logical statement not depending on these does hold [[internalization|internal to]] _every_ topos.

For this reason toposes are often studied as abstract contexts "in which one can do mathematics", independently of their interpretation as categories of spaces. These two points of views on toposes, as being about geometry and about logic at the same time, is part of the richness of topos theory.

On a third hand, however, we can de-emphasize the role of the objects of the topos and instead treat the topos itself as a "generalized space" (and in particular, a [[vertical categorification|categorified]] space).  We then consider the topos $Sh(X)$ as a representative of $X$ itself, while toposes not of this form are "honestly generalized" spaces.  This point of view is supported by the fact that the assignment $X\mapsto Sh(X)$ is a full embedding of (sufficiently nice) topological spaces into toposes, and that many topological properties of a space $X$ can be detected at the level of $Sh(X)$.  (This is even more true once we pass to [[(∞,1)-toposes]].)

From this point of view, the objects of a topos (regarded as a category) should be thought of instead as *sheaves on* that topos (regarded as a generalized space).  And just as sheaves on a topological space can be identified with local homeomorphisms over it, such "sheaves on a topos" (i.e. objects of the topos *qua* category) can be identified with other *toposes* that sit over the given topos via a [[étale geometric morphism|local homeomorphism of toposes]].


Finally, mixing this point of view with the second one, we can regard toposes over a given topos $E$ instead as "toposes in the $E$-world of mathematics."  For this reason, the theory of toposes over a given base is formally quite similar to that of arbitrary toposes.  And coming full circle, this fact allows the use of "base change arguments" as a very useful technical tool, even if our interest is only in one or two particular toposes *qua* categories.

### 'What a topos is like:'

 (i) 'A topos is a category of sheaves on a site'

 (ii) 'A topos is a category with finite limits and power-objects'

 (iii) 'A topos is (the embodiment of) an intuitionistic higher-order theory'

 (iv) 'A topos is (the extensional essence of) a first-order (infinitary) geometric theory'

 (v) 'A topos is a totally cocomplete object in the meta-2-category CART of cartesian (i.e. , finitely complete) categories'

 (vi) 'A topos is a generalized space'

 (vii) 'A topos is a semantics for intuitionistic formal systems'

 (viii) 'A topos is a Morita equivalence class of continuous groupoids'

 (ix) 'A topos is the category of maps of a power allegory'

 (x) 'A topos is a category whose canonical indexing over itself is complete and well-powered'

 (xi) 'A topos is the spatial manifestation of a giraud frame'

 (xii) 'A topos is a setting for synthetic differential geometry'

 (xiii) 'A topos is a setting for synthetic domain theory',

And so on. But the important thing about the elephant is that 'however you approach it, it is still the same animal'. [[Elephant]]

## Definitions

The general notion of _topos_ is that of

* [Elementary toposes](#ElementaryTopos).

A specialization of this which is important enough that much of the literature implicitly takes it to be the general definition is the notion of 

* [Grothendieck/sheaf toposes](#SheafToposes)

This is the notion relevant for applications in [[geometry]] and [[geometric logic]], whereas the notion of elementary toposes is relevant for more general applications in [[logic]].

For standard notions of mathematics to be available [[internal logic|inside]] a given topos one typically at least needs a [[natural numbers object]]. Its existence is guaranteed by the axioms of a sheaf topos, but not by the more general axioms of an elementary topos. Adding the existence of a natural numbers object to the axioms of an elementary topos yields the notion of a 

* [W-topos](#WToposes).

### Elementary toposes
 {#ElementaryTopos}

A quick formal definition is that an **elementary topos** is a [[category]] which

1. has [[finitely complete category|finite limits]],

1. is [[cartesian closed category|cartesian closed]], and

1. has a [[subobject classifier]].

There are alternative ways to state the definition; for instance,

1. has [[finite limit]]s and
2. has [[power objects]].

In a way, however, these concise definitions can be misleading, because a topos has a great deal of other structure, which plays a very important role but just happens to follow automatically from these basic axioms.  Most importantly, an elementary topos is all of the following:

*  [[locally cartesian closed category|locally cartesian closed]],
*  [[finitely cocomplete category|finitely cocomplete]],
*  a [[Heyting category]],
*  a [[pretopos]].

The last two imply that it has an [[internal logic]] that resembles ordinary mathematical reasoning, and the presence of exponentials and power objects means that this logic is [[higher order logic|higher order]].

### Grothendieck/sheaf toposes
 {#SheafToposes}

The above is the definition of an *elementary* topos.  We also have the (historically earlier) notion of [[Grothendieck topos]]: a __Grothendieck topos__ is a topos that is neither too small nor too large, in that it is:

*  [[cocomplete category|cocomplete]] (not too small), and
*  has a [[small set|small]] [[generating set]] (not too large).

Equivalently, a Grothendieck topos is any category [[equivalence of categories|equivalent]] to the [[category of sheaves]] on some 
[[small category|small]] [[site]].


### $W$-toposes
 {#WToposes}

There is a further elementary property of [[Set]] that might have gone into the definition of elementary topos but historically did not: the existence of a [[natural numbers object]].  Any topos with this property is called a __topos with NNO__ or a __$W$-topos__.  The latter term comes from the result that any such topos must have (not only an NNO but also) all [[W-types]].

### Toposes over a base

* [[base topos]]

### Morphisms of toposes

There are two kinds of [[homomorphisms]] between toposes that one considers:

* [[geometric morphism]] -- this is the kind of morphism that regards a topos as a generalized [[topological space]].

* [[logical morphism]] -- this is the kind of morphism that regards a topos in terms of its [[internal logic]].

Accordingly there is a [[2-category]] [[Topos]] of toposes, whose 

* [[object]]s are toposes;

* [[morphism]]s are [[geometric morphism]]s;

* [[2-morphism]]s are [[natural transformation]]s between the [[functor]]s underlying the geometric morphisms.



## Properties

### Extensivity

Every topos is an [[extensive category]].  For [[Grothendieck toposes]], infinitary extensivity is part of the characterizing [[Giraud's theorem]].  For elementary toposes, see [[toposes are extensive]].

### Adhesiveness

Every topos is an [[adhesive category]]. For [[Grothendieck toposes]] this follows immediately from the adhesion of [[Set]], for elementary toposes it is due to ([Lack-Sobocinski](#LackSobocinski)).

### Epimorphisms

In a topos [[epimorphism]]s are stable under [[pullback]] and hence the [[(epi, mono) factorization system]] in a topos is a [[stable factorization system]].


### Relation to abelian categories

While crucially different from [[abelian categories]], there is some intimate relation between toposes and abelian categories. For more on that see [[AT category]].


### Reasoning in a topos 

Any result in [[ordinary mathematics]] whose proof is [[finite mathematics|finitist]] and [[constructive mathematics|constructive]] automatically holds in any topos.  If you remove the restriction that the proof be finitist, then the result holds in any topos with a [[natural numbers object]]; if you remove the restrictions that the proof be constructive, then the result holds in any [[boolean topos]].  On the other hand, if you add the restriction that the proof be predicative in the weaker sense used by constructivists, then the result may fail in some toposes but holds in any $\Pi$-[[Pi-pretopos|pretopos]]; if you add the restriction that the proof be predicative in a stronger sense, then the result holds in any [[Heyting pretopos]].

Therefore, one can prove results in toposes and similar categories by reasoning, not about the [[objects]] and [[morphisms]] in the topos themselves, but instead about [[sets]] and [[functions]] in the normal language of structural [[set theory]], which is more familiar to most mathematicians.  One merely has to be careful about what axioms one uses to get results of sufficient generality.

The [[internal logic|internal language]] of a topos is called [[Mitchell-Bénabou language]].



## Examples {#Examples}

### Specific examples and key results

* The archetypical topos is [[Set]]. Notice that this happens to be a [[Grothendieck topos]]: it is the [[category of sheaves]] on the [[point]].

  The [[full subcategory]] [[FinSet]] is also an elementary topos, and the inclusion functor $FinSet \hookrightarrow Set$ is a [[logical morphism]]. This is not a Grothendieck topos.

  More generally, for $\kappa$ a [[cardinal|strong limit cardinal]] the full subcategory $Set_\kappa$ of sets or [[cardinality]] less than $\kappa$ is a topos.

* For $C$ any (small) [[site]], the [[category of sheaves]] $Sh(C)$ is a [[Grothendieck topos]].  Either by definition or by [[Giraud's theorem]], every Grothendieck topos arises in this way.  Important examples include:

  * The case where the [[Grothendieck topology]] is the trivial one, so that also all categories of [[presheaf|presheaves]] (on small categories) are (Grothendieck) toposes.

  * The case of sheaves on (the [[site]] given by the [[category of open subsets]] of) a [[topological space]], or more generally a [[locale]].

  * The category $G Set$ of [[set]]s equipped with the [[action]] of a [[group]] $G$: this is the topos of presheaves on the category $\mathbf{B}G$ which is the [[delooping]] [[groupoid]] of $G$.

 * Continuing the last example above, if $G$ is a topological group, the category $G Set$ of [[category of G-sets|sets with a continuous action of G]] (that is, the action map $G\times X\to X$ is [[continuous map|continuous]], where $X$ has the [[discrete topology]]) is a topos, and in fact a Grothendieck topos (though this may not be obvious).

 * More generally, $G$ may be a [[topological groupoid]], or even a [[localic groupoid]].  In fact, it is a theorem that every Grothendieck topos can be presented as the topos of "continuous sheaves" on a localic groupoid.

* Again if $G$ is a topological group, the category $Unif(G)$ of *[[uniformly continuous map|uniformly continuous]]* $G$-sets is also a topos, but not (in general) one of Grothendieck's.  For example, if $G$ is the [[profinite completion]] of $\mathbb{Z}$, then a continuous $G$-set is a $\mathbb{Z}$-set all of whose orbits are finite, while a uniformly continuous one is a $\mathbb{Z}$-set with a finite upper bound on the size of all its orbits.

* For $E$ a topos and $X \in E$ any [[object]], also the [[overcategory]] or [[slice category]] $E/X$ is again a topos. ([[Elephant]], A.2.3.2). See also [[over-topos]]. 

* If $E$ is a topos and $j \colon E \to E$ is a [[exact functor|lex]] idempotent monad, the category of $j$-algebras is a topos. Each such $j$ corresponds to a [[Lawvere-Tierney topology]] in $E$, and the category of $j$-algebras is equivalent to the category of sheaves for this topology. An example is the [[double negation|double-negation topology]]. 

* An obvious example of an elementary topos that is not a Grothendieck topos is the category [[FinSet]] of finite sets.  More generally, for any [[strong limit cardinal]] $\kappa$, the category of sets of cardinality $\lt\kappa$ is an elementary topos, and as long as $\kappa \gt\omega$ it has a [[NNO]]. $Set_{\lt \kappa}$ doesn't even admit a geometric morphism to $Set$.

* Since the definition of elementary topos is "algebraic," there exist [[free topos]]es generated by various kinds of data. The category of toposes (and [[logical functor]]s) is [[2-monadic]] over the 2-category of categories, functors, and natural isomorphisms. It has an [[initial object]] which is sometimes called *the free topos*.  More generally, any [[higher-order logic|higher-order]] [[type theory]] (of the sort which can be interpreted in the [[internal logic]] of a topos) generates a free topos containing a model of that theory.  Such toposes (for a consistent theory) are never Grothendieck's.

* If $G$ is a [[large category|large]] [[groupoid]] with a small set of objects, then the category $[G,Set]$ (which makes sense if we define "large" and "small" relative to a [[Grothendieck universe]]) is a topos, but not in general a Grothendieck topos.  Note that this topos is in fact [[complete category|complete]] and cocomplete, but it does not have a small generating set, and so is an [[unbounded topos]].

* If $\mathcal{F}$ is a [[filter]] of [[subterminal objects]] in any topos $E$, then there is a [[filterquotient]] topos $E//\mathcal{F}$.  Grothendieck-ness (and completeness and cocompleteness) are not in general preserved by this construction.

* If $C$ and $D$ are toposes and $F\colon C\to D$ is a [[lex functor]], then there is a topos $Gl(F)$ called the [[Artin gluing]] of $C$ and $D$ along $F$, and defined to be the [[comma category]] $(D/F)$.  If $C$ and $D$ are Grothendieck toposes then $Gl(F)$ is a $Set$-topos. If $F$ is [[accessible functor|accessible]], then $Gl(F)$ is again Grothendieck (hence [[bounded geometric morphism|bounded]]), but in general it may not be. (Note, though, that it is not clear whether it can be proven in ZFC that there exist any inaccessible lex functors between Grothendieck toposes, although from a proper class of [[measurable cardinal]]s one can construct an inaccessible lex endofunctor of $Set$.)

* The [[Eilenberg-Moore category|category of coalgebras]] for any [[exact functor|lex]] [[comonad]] on a topos is again a topos: a [[topos of algebras over a monad|topos of coalgebras]], and if the comonad is [[accessible functor|accessible]], this construction preserves Grothendieck-ness.  If the comonad is not accessible, then this topos is unbounded.

  For instance the [[Artin gluing]] $Gl(F)$ is equivalent to the category of coalgebras for the comonad on the topos $C\times D$ defined by $(c,d) \mapsto (c, d\times F(c))$. 

* More generally, the category of coalgebras for any [[preserved limit|pullback-preserving]] comonad on a topos is again a topos. This covers both the preceding result and also the overcategory (slice category) result above, since $E/X$ is the category of coalgebras for the pullback-preserving comonad given by $X \times - \colon E \to E$. It also covers Artin gluing along a pullback-preserving functor. 

* More generally still, [[Todd Trimble]] has a notion called a "modal operator" on a topos, from which one can construct a new topos of "$G$-structures": see [[toddtrimble:Three topos theorems in one]]. Special cases include the pullback-preserving comonad result just mentioned, and the result that the category of algebras for a lex [[idempotent monad]] is a topos. A related idea is Toby Kenney's notion of lex distributive [[diad]], from which one can also construct a topos.

* From any [[partial combinatory algebra]] one can construct a [[realizability topos]], whose [[internal logic]] is "computable" or "effective" mathematics relative to that PCA.  In particular, for [[Kleene's first algebra]], one obtains the [[effective topos]], the most-studied of realizability toposes.  Realizability toposes are generally not Grothendieck toposes. 

* A topos can also be constructed from any [[tripos]].  This includes realizability toposes as well as toposes of sheaves on locales. 

### Classes of examples

For various applications one uses toposes that have [[stuff, structure, property|extra structure or properties]].

* In the [[foundations]] of mathematics, one often studies [[well-pointed toposes]], especially models of [[ETCS]] as potential replacements for the category [[Set]].

* In [[synthetic differential geometry]] one studies [[smooth topos]]es as a context for axiomatic [[differential geometry]].




## Related concepts

* [[(0,1)-topos]]

* **topos**
 
  [[category of sheaves]]

  [[base topos]], [[indexed topos]] 

  [[predicative topos]]

  [[boolean topos]]

  [[local topos]], [[locally connected topos]], [[connected topos]], [[cohesive topos]]

  [[predicative topos]]

  [[pretopos]], [[Π-pretopos]], [[ΠW-pretopos]], [[list-arithmetic pretopos]]

  [[smooth structure on a topos]]

  [[monoidal topos]]

  [[isotropy group of a topos]]

  [[test topos]]

* [[(∞,1)-topos]] 

  * [[model topos]]

  * [[(∞,1)-category of (∞,1)-sheaves]]

  * [[elementary (∞,1)-topos]] 

  * [[(n,1)-topos]]

* [[2-topos]], [[(∞,2)-topos]], [[(∞,2)-sheaf]]

* [[(∞,n)-topos]]

[[!include locally presentable categories - table]]



## References {#References}

### Introductions

Introductions to [[topos theory]] include 

* [[Ross Street]], _A survey of topos theory_ (notes for students, 1978) [pdf](http://www.math.mq.edu.au/~street/ToposSurvey.pdf)

* [[Tom Leinster]], _[[Leinster2010|An informal introduction to topos theory]]_ (2010)

* [[Francis Borceux]], _Some glances at topos theory_, [pdf](https://tcsc.lakecomoschool.org/files/2018/01/Borceux.pdf).

An introduction amplifying the simple but important case of [[presheaf toposes]] is

* Marie La Palme Reyes, [[Gonzalo E. Reyes]], Houman Zolfaghari,
_Generic figures and their glueings.  A constructive approach to functor categories_, Polimetrica (2008), ISBN: 8876990046.
[pdf](https://marieetgonzalo.files.wordpress.com/2004/06/generic-figures.pdf).

A quick introduction of the basic facts of [[Grothendieck topos]] theory is Chapter I, "Background in topos theory" in 

* [[Ieke Moerdijk]], _[[Classifying Spaces and Classifying Topoi]]_, Lecture Notes in Mathematics 1616 (1995), Springer

Course notes covering both [[Grothendieck toposes]] and the [[effective topos]]:

* [[Ieke Moerdijk]], [[Jaap van Oosten]], _Topos Theory_, Master class notes (2007) ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/toposmoeder.pdf))

A gentle basic introduction is 

* [[John Baez]], [Topos Theory in a Nutshell](http://math.ucr.edu/home/baez/topos.html).

### Videos

* [[André Joyal]], _[[A crash course in topos theory -- The big picture]]_, lecture series at [Topos à l'IHES](https://indico.math.cnrs.fr/event/747/), November 2015, Paris 

* MathProofsable, Category Theory - Toposes [video playlist] (https://www.youtube.com/watch?v=gKYpvyQPhZo&list=PL4FD0wu2mjWM3ZSxXBj4LRNsNKWZYaT7k) 

### Textbooks

Modern textbooks include the following two.

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_.

* [[Francis Borceux]], _[[Handbook of Categorical Algebra]], Volume 3_.

Other sources include

* [[Oswald Wyler]], _[[Lecture Notes on Topoi and Quasitopoi]]_, World Scientific 1991.

### Monographs

A early monograph is

* [[Peter Johnstone]], _Topos theory_, London Math. Soc. Monographs __10__, Acad. Press 1977, xxiii+367 pp. (Dover reprint 2014)

This later grew into the more detailed

* [[Peter Johnstone]], [[Elephant|Sketches of an elephant: a topos theory compendium]]

Other sources include the following.

* [[Michael Barr]], [[Charles Wells]], _Toposes, Triples, and Theories_ , Springer Heidelberg 1985. ([TAC reprint](http://www.tac.mta.ca/tac/reprints/articles/12/tr12.pdf))

### Classifying toposes

* [[Ieke Moerdijk]], _[[Classifying Spaces and Classifying Topoi]]_, Lecture Notes in Mathematics 1616 (1995), Springer.
ISBN: 978-3-540-60319-1.
[doi](https://doi.org/10.1007/BFb0094441)

* [[Olivia Caramello]], _Theories, Sites, Toposes_, Oxford University Press, 2017.
[doi](https://doi.org/10.1007/BFb0094441)

### Categorical logic and elementary toposes

* [[Colin McLarty]], _[[Elementary Categories, Elementary Toposes]]_, Oxford University Press 1992 (reprinted in 2005)

* [[Jonathan Chapman]], [[Frederick Rowbottom]], _[[Relative Category Theory and Geometric Morphisms.  A Logical Approach]]_, Oxford University Press 1992.

* [[J. L. Bell]], _[[Toposes and Local Set Theories.  An Introduction]]_, Oxford University Press 1988.

* [[Robert Goldblatt]], _Topoi. The categorial analysis of logic_, Studies in Logic and the Foundations of Math. __98__, North-Holland Publ. Co., Amsterdam, 1979, 1984; (Rus. transl. Mir Publ., Moscow 1983). 

* [[Joachim Lambek]], [[Philip J. Scott]], _[[Introduction to higher order categorical logic]]_. Cambridge Studies in Advanced Mathematics 7 (1986).
ISBN: 0-521-24665-2.

* [[Bart Jacobs]], _[[Categorical logic and type theory]]_, Studies in Logic and the Foundations of Mathematics 141 (1999).  North-Holland Publishing Co.
ISBN: 0-444-50170-3

### Algebra, ringed toposes, algebraic geometry

* [[Monique Hakim]], _[[Topos annelés et schémas relatifs]]_, Ergebnisse der Mathematik und ihrer Grenzgebiete 64 (1972),
ISBN 3-540-05573-8, 0-387-05573-8.

* [[Francis Borceux]], [[Gilberte van den Bossche]], _Algebra in a localic topos with applications to ring theory_, Lecture Notes in Mathematics 1038 (1983),
ISBN: 3-540-12711-9.

### Quantum theory

* [[Cecilia Flori]], _A first course in topos quantum theory_. Lecture Notes in Physics 868 (2013).
ISBN: 978-3-642-35712-1; 978-3-642-35713-8

* [[Cecilia Flori]], _A second course in topos quantum theory_. Lecture Notes in Physics 944 (2018).
ISBN: 978-3-319-71107-2; 978-3-319-71108-9

### Original articles

Original source of (Grothendieck) topoi:

* [[SGA4]] Exposé IV by Grothendieck and Verdier (and Exposé V for cohomology in a (Grothendieck) topos)

That every topos is an [[adhesive category]] is discussed in 

* [[Stephen Lack]], Pawel Sobociński, _Toposes are adhesive_ ([pdf](http://users.ecs.soton.ac.uk/ps/papers/toposesAdhesive.pdf))
 {#LackSobocinski}

### History

* [[Colin McLarty]], _The Uses and Abuses of the History of Topos Theory_ , Brit. J. Phil. Sci., 41 (1990) ([JSTOR](http://www.jstor.org/stable/687825)) [PDF](http://bjps.oxfordjournals.org/content/41/3/351.full.pdf) ([direct link](http://www.cwru.edu/artsci/phil/UsesandAbuses%20HistoryToposTheory.pdf))

* [[John W. Gray]], _Fragments of the history of sheaf theory_,
in: Applications of Sheaves, pp. 1–79,
Lecture Notes in Mathematics 753,
ISBN: 978-3-540-09564-4,
[doi](https://doi.org/10.1007/BFb0061812).

According to appendix C.1 in

* {#LawvereRosebrugh03} [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_ , Cambridge UP  2003. ([web](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics))

> "Topos" is a Greek term intended to describe the objects studied by
"[analysis situs](http://en.wikipedia.org/wiki/Analysis_Situs_%28paper%29)," the Latin term previously established by Poincar&#233; to signify the science of place [or situation]; in keeping with those ideas, a $\mathcal{U}$-topos was shown to have presentations in various "sites".

A historical analysis of Grothendieck's 1973 Buffalo lecture series on toposes and their precedents is in

* {#McLarty18} [[Colin McLarty]], _Grothendieck's 1973 topos lectures_, Séminaire Lectures grothendieckiennes, 3 May (2018) ([YouTube video](https://www.youtube.com/watch?v=hhWT5V0oaSI))

[[!redirects topos]]
[[!redirects topoi]]
[[!redirects toposes]]
[[!redirects elementary topos]]
[[!redirects elementary topoi]]
[[!redirects elementary toposes]]
[[!redirects Lawvere-Tierney topos]]
[[!redirects Lawvere-Tierney topoi]]
[[!redirects Lawvere-Tierney toposes]]
[[!redirects Lawvere–Tierney topos]]
[[!redirects Lawvere–Tierney topoi]]
[[!redirects Lawvere–Tierney toposes]]
[[!redirects Lawvere--Tierney topos]]
[[!redirects Lawvere--Tierney topoi]]
[[!redirects Lawvere--Tierney toposes]]

[[!redirects W-topos]]
[[!redirects W-topoi]]
[[!redirects W-toposes]]
[[!redirects topos with NNO]]
[[!redirects topoi with NNO]]
[[!redirects toposes with NNO]]
[[!redirects topos with an NNO]]
[[!redirects topoi with NNOs]]
[[!redirects toposes with NNOs]]