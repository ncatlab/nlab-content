

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--




# Contents #
* autamatic table of contents goes here
{:toc}


## Idea 

A _topos_ is a [[category]] that resembles the category [[Set]] of sets and functions enough that we can use it as a 'universe' to do ordinary mathematics in.  Ordinary mathematical reasoning (with some restrictions) suffices to prove results [[internalisation|internal]] to any topos.

A topos in this sense is sometimes called an __elementary topos__ or a __Lawvere--Tierney topos__ to distinguish it from the original but more specific [[Grothendieck topos]].

While crucially different from [[abelian categories]], there is some intimate relation between toposes and abelian categories. For more on that see [[AT category]].

## Definition 

A quick formal definition is that an **(elementary) topos** is a [[category]] which

1. has [[finitely complete category|finite limits]],
1. is [[cartesian closed category|cartesian closed]], and
1. has a [[subobject classifier]].

There are alternative ways to state the definition; for instance,

1. [[finite limit]]s and
2. [[power objects]].

In a way, however, these concise definitions can be misleading, because a topos has a great deal of other structure, which plays a very important role but just happens to follow automatically from these basic axioms.  Most importantly, a topos is:

*  [[locally cartesian closed category|locally cartesian closed]],
*  [[finitely cocomplete category|finitely cocomplete]],
*  a [[Heyting category]],
*  a [[pretopos]].

The last two imply that it has an [[internal logic]] that resembles ordinary mathematical reasoning, and the presence of exponentials and power objects means that this logic is [[higher order logic|higher order]].

There are two kinds of morphisms between toposes that one considers:

* [[geometric morphism]] -- this is the kind of morphism that regards a topos as a generalized [[topological space]].

* [[logical morphism]] -- this is the kind of morphism that regards a topos in terms of its [[internal logic]].

Accordingly there is a [[2-category]] [[Toposes]] of toposes.


## Reasoning in a topos 

Any result in ordinary mathematics whose proof is [[finite mathematics|finitist]] and [[constructive mathematics|constructive]] automatically holds in any topos.  If you remove the restriction that the proof be finitist, then the result holds in any topos with a [[natural numbers object]]; if you remove the restrictions that the proof be constructive, then the result holds in any [[boolean topos]].  On the other hand, if you add the restriction that the proof be predicative in the weaker sense used by constructivists, then the result may fail in some toposes but holds in any $\Pi$-[[Pi-pretopos|pretopos]]; if you add the restriction that the proof by predicative in a stronger sense, then the result holds in any [[Heyting pretopos]].

Therefore, one can prove results in toposes and similar categories by reasoning, not about the [[objects]] and [[morphisms]] in the topos themselves, but instead about [[sets]] and [[functions]] in the normal language of structural [[set theory]], which is more familiar to most mathematicians.  One merely has to be careful about what axioms one uses to get results of sufficient generality.

For more on this idea, see [[internal logic]].

## Examples {#Examples}

* The archetypical topos is [[Set]]. Notice that this happens to be a [[Grothendieck topos]]: this is the [[category of sheaves]] on the [[point]].

  The [[full subcategory]] [[FinSet]] is also a topos, and the inclusion functor $FinSet \hookrightarrow Set$ is a [[logical morphism]].

  More generally, for $\kappa$ a [[cardinal|strong limit cardinal]] the full subcategory $Set_\kappa$ of sets or [[cardinality]] less than $\kappa$ is a topos.

* For $C$ any (small) [[site]], the [[category of sheaves]] $Sh(C)$ is a [[Grothendieck topos]].  Either by definition or by [[Giraud's theorem]], every Grothendieck topos arises in this way.  Important examples include:

  * The case where the [[Grothendieck topology]] is the trivial one, so that also all categories of [[presheaf|presheaves]] (on small categories) are (Grothendieck) toposes.

  * The case of sheaves on a [[topological space]], or more generally a [[locale]].

  * The category $G Set$ of [[set]]s equipped with the [[action]] of a [[group]] $G$: this is the topos of presheaves on the category $\mathbf{B}G$ which is the [[delooping]] [[groupoid]] of $G$.

* For $E$ a topos and $X \in E$ any [[object]], also the [[overcategory]]
  $E/X$ is again a topos. ([[Elephant]], A.2.3.2). 

* If $G$ is a [[topological group]], then the category $Cont(G)$ of sets with a *continuous* action of $G$ (that is, the action map $G\times X\to X$ is [[continuous map|continuous]], where $X$ has the [[discrete topology]]) is a topos, and in fact a Grothendieck topos (though this may not be obvious).  More generally, $G$ may be a [[topological groupoid]], or even a [[localic groupoid]].  In fact, it is a theorem that every Grothendieck topos can be presented as the topos of "continuous sheaves" on a localic groupoid.

* Again if $G$ is a topological group, the category $Unif(G)$ of *[[uniformly continuous map|uniformly continuous]]* $G$-sets is also a topos, but not (in general) one of Grothendieck's.  For example, if $G$ is the [[profinite completion]] of $\mathbb{Z}$, then a continuous $G$-set is a $\mathbb{Z}$-set all of whose orbits are finite, while a uniformly continuous one is a $\mathbb{Z}$-set with a finite upper bound on the size of all its orbits.

* An obvious example of an elementary topos that is not a Grothendieck topos is the category [[FinSet]] of finite sets.  More generally, for any [[strong limit cardinal]] $\kappa$, the category of sets of cardinality $\lt\kappa$ is an elementary topos, and as long as $\kappa \gt\omega$ it has a [[NNO]].

* Since the definition of elementary topos is "algebraic," there exist [[free topos]]es generated by various kinds of data.  In particular, the category of toposes (and [[logical functor]]s) has an [[initial object]] which is sometimes called *the free topos*.  More generally, any [[higher-order logic|higher-order]] [[type theory]] (of the sort which can be interpreted in the [[internal logic]] of a topos) generates a free topos containing a model of that theory.  Such toposes (for a consistent theory) are never Grothendieck's.

* If $G$ is a [[large category|large]] [[groupoid]] with a small set of objects, then the category $[G,Set]$ (which makes sense if we define "large" and "small" relative to a [[Grothendieck universe]]) is a topos, but not in general a Grothendieck topos.  Note that this topos is in fact [[complete category|complete]] and cocomplete, but it does not have a small generating set.

* If $\mathcal{F}$ is a [[filter]] of [[subterminal objects]] in any topos $E$, then there is a [[filterquotient]] topos $E//\mathcal{F}$.  Grothendieck-ness (and completeness and cocompleteness) are not in general preserved by this construction.

* If $C$ and $D$ are toposes and $F\colon C\to D$ is a [[lex functor]], then there is a topos $Gl(F)$ called the [[Artin gluing]] of $C$ and $D$ along $F$, and defined to be the [[comma category]] $(D/F)$.  If $C$ and $D$ are Grothendieck toposes and $F$ is [[accessible functor|accessible]], then $Gl(F)$ is again Grothendieck, but in general it may not be.  (Note, though, that it is not clear whether it can be proven in ZFC that there exist any inaccessible lex functors between Grothendieck toposes, although from a proper class of [[measurable cardinal]]s one can construct an inaccessible lex endofunctor of $Set$.)

* The category of coalgebras for any lex [[comonad]] on a topos is again a topos, and if the comonad is accessible, this construction preserves Grothendieck-ness.  The Artin gluing $Gl(F)$ is equivalent to the category of coalgebras for the comonad on the topos $C\times D$ defined by $(c,d) \mapsto (c, d\times F(c))$.

* [[Todd Trimble]] has a notion called a "modal operator" on a topos, from which one can construct a new topos of "$G$-structures": see [[toddtrimble:Three topos theorems in one]].  A possibly related idea is Toby Kenney's notion of lex distributive [[diad]], from which one can also construct a topos.

* From any [[partial combinatory algebra]] one can construct a [[realizability topos]], whose [[internal logic]] is "computable" or "effective" mathematics relative to that PCA.  In particular, for [[Kleene's first algebra]], one obtains the [[effective topos]], the most-studied of realizability toposes.  Realizability toposes are generally not Grothendieck toposes.

* A topos can also be constructed from any [[tripos]].  This includes realizability toposes as well as toposes of sheaves on locales.


### Special classes 

For various applications one uses toposes that have [[stuff, structure, property|extra structure or properties]].

* In [[synthetic differential geometry]] one studies [[smooth topos]]es as a context for axiomatic [[differential geometry]].

* In the [[foundations]] of mathematics, one often studies [[well-pointed toposes]], especially models of [[ETCS]] as potential replacements for the category [[Set]].


## Higher toposes 

The analogs of topos theory in [[higher category theory]] is [[higher topos theory]]. 

* A well developed case is that of [[(∞,1)-topos]]es.

* A bit of theory also exists for [[2-topos]]es.

* By [[negative thinking]], a [[(0,1)-topos]] is a [[Heyting algebra]].


## Related entries

* [[(0,1)-topos]]

* **topos**

* [[2-topos]]

* [[(∞,1)-sheaf]] / [[∞-stack]]





## References {#References}

For an introduction, try:

* [[John Baez]], [Topos Theory in a Nutshell](http://math.ucr.edu/home/baez/topos.html).

Another survey is in

* [[Ross Street]], _A survey of topos theory_ (notes for students, 1978) [pdf](http://www.math.mq.edu.au/~street/ToposSurvey.pdf)

A standard textbook is

* [[Peter Johnstone]], _Topos theory_, London Math. Soc. Monographs __10__, Acad. Press 1977, xxiii+367 pp.

This later grew into the more detailed

* [[Peter Johnstone]], [[Elephant|Sketches of an elephant: a topos theory compendium]]

A quick introduction of the basic facts of [[Grothendieck topos]] theory is chapter I, "Background in topos theory" in 

* [[Ieke Moerdijk]], _Classifying Spaces and Classifying Topoi_ Lecture Notes in Mathematics 1616, Springer (1995)

A standard textbook on this case is

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

There is also

* R. Goldblatt, _Topoi. The categorial analysis of logic_, Studies in Logic and the Foundations of Math. __98__, North-Holland Publ. Co., Amsterdam, 1979, 1984; (Rus. transl. Mir Publ., Moscow 1983).



[[!redirects topoi]]
[[!redirects toposes]]
[[!redirects Lawvere-Tierney topos]]
[[!redirects Lawvere--Tierney topos]]
[[!redirects Lawvere?Tierney topos]]
[[!redirects elementary topos]]
[[!redirects Lawvere-Tierney topoi]]
[[!redirects Lawvere--Tierney topoi]]
[[!redirects Lawvere?Tierney topoi]]
[[!redirects elementary topoi]]
[[!redirects Lawvere-Tierney toposes]]
[[!redirects Lawvere--Tierney toposes]]
[[!redirects Lawvere?Tierney toposes]]
[[!redirects elementary toposes]]