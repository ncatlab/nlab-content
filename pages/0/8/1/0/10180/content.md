
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

The [[classifying topos]] $\mathcal{S}[\mathbb{O}]$ for the [[theory of objects]] $\mathbb{O}$, or the **object classifier**, as it is also called[^termin], is  the [[presheaf topos]] $[FinSet, Set]$ on the [[opposite category]] of [[FinSet]].

What motivates the terminology, is that for any [[topos]] $E$, [[geometric morphisms]] $E \to \mathcal{S}[\mathbb{O}]$ correspond to [[objects]] of $E$.

This is because by [a standard fact](morphism+of+sites#LemmaForClassifyingToposes) [[geometric morphisms]]

$$
  E \to PSh(FinSet^{op})
$$

are equivalent to [[morphisms of sites]]

$$
  E \leftarrow FinSet^{op}
$$

hence to [[finite limit]]-preserving such [[functors]]. Since finite limits in $FinSet^{op}$ are [[finite colimits]] in [[FinSet]] and since $FinSet$ is generated under finite colimits from the singleton set $\ast$, such functors are uniquely determined by their image of $\ast$, hence by a choice of object in $E$.


[^termin]: As this is not to be confused with the notion of an [[object classifier]] in an [[(∞,1)-topos]], we prefer to call it in full the _classifying topos for the theory of objects_.

[^ultra]: For another remarkable property of this inclusion functor see at [[ultrafilter monad]].

The construction is due to [[Gavin Wraith]] and constituted an important step towards the general theorem on the existence of [[classifying topos|classifying toposes]] for geometric theories in the early development of [[topos theory]].

Similarly 

* $PSh(FinSet_\ast^{op})$ is the classifying topos for [[pointed objects]].

* write $Fin\infty Grpd$ for the [[full sub-(∞,1)-category]] on [[∞Grpd]] which is generated under [[finite (∞,1)-colimits]] from the point $\ast$ ([[Higher Algebra|HA, def. 1.4.2.8]]), then the [[(∞,1)-presheaf (∞,1)-topos]] $PSh_\infty(Fin\infty Grpd^{op})$ is the [[classifying (∞,1)-topos]] for objects;

* write $Fin\infty Grpd_\ast$ for pointed finite $\infty$-groupoids in this sense, then $PSh_\infty((Fin\infty Grpd_\ast)^{op})$ is the classifying $(\infty,1)$-topos for pointed objects. See also at _[[spectrum object]]_ _[via excisive functors](spectrum%20object#ViaExcisiveFunctors)_.


## Properties

### Generic object

The _generic_ or **universal object** $U$ is the inclusion $FinSet\hookrightarrow Set$: every object $X$ of $E$ arises from some geometric morphism $f$ as $X\cong f^\ast(U)$.[^ultra]

### The symbolic link to algebra

As the role of the object classifier bears some resemblance to the role of the [[polynomial ring]] $k[x]$ over a ground ring $k$ that 'classifies' elements of k-algebras $A$ via $A\cong Hom_k(k[x], A)$, it is traditionally denoted $\mathcal{S}[U]$, the 'adjunction' of the free (=generic) object to the base topos $\mathcal{S}$, in our case $Set$.

The analogy between topos theory and algebra is pursued further in Bunge&Funk (2006) where, in the context of [[Lawvere distribution|topos distributions]] and the '[[symmetric algebra]]' of a topos (aka the [[symmetric topos]]), $\mathcal{S}[U]$ is shown to play the role of the [[real line]] $\mathbf R$ in [[functional analysis]].

### The relative case

What concerns base toposes $\mathcal{S}$ other than $Set$, it is a theorem due to [[Andreas Blass]] ([Blass 1989](#blass)) that _$\mathcal{S}$ has an object classifier $\mathcal{S}[\mathbb{O}]$ precisely if $\mathcal{S}$ has a [[natural number object]]_.

A consequence of this, discussed in sec. B4.2 of (Johnstone 2002,I p.431), is that classifying toposes for [[geometric theories]] over $\mathcal{S}$ exist precisely if the object classifier $\mathcal{S}[\mathbb{O}]$ exists.

### An alternative characterization

+-- {: .num_prop}
###### Proposition

The classifying topos $[FinSet, Set]$ is [[equivalence of categories|equivalent]] to the category of finitary [[endofunctors]] on [[Set]] (those that commute with [[filtered colimits]]):

$$
  [FinSet, Set] \simeq End_f(Set)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because every [[set]] is the [[filtered colimit]] over its finite [[subsets]].

Constructively we should take a little care over what is meant by "[[finite set]]". A set is the filtered colimit of its _Kuratowski_ finite subsets, but a Kuratowski finite set is the image of some finite cardinal $\{0,\ldots, n-1\}$. The issue is that, unless the superset has decidable equality, we are not necessarily able to eliminate duplicates from the list of elements in the Kuratowski finite subset.
We find that the set is still a filtered colimit of finite cardinals, though not necessarily subsets. The category $FinSet$ can be taken to have the natural numbers as its objects, with morphisms being functions between the corresponding finite cardinals.

=--

### The monoidal point of view

Since the category $End_f(Set) \hookrightarrow End(Set)$ of [[finitary functors]] is naturally a [[monoidal category]] under composition, this induces the structure of a (non-cartesian) [[monoidal category]] also on the [[classifying topos]] $[FinSet, Set]$ and hence makes it a [[monoidal topos]]. A [[monoid]] with respect to this monoidal structure is equivalently a [[finitary monad]]. 

A related point of view is that $FinSet^{op}$ is the [[free construction|free]] [[cartesian monoidal category]] generated by an object (or by the terminal category), and its [[free cocompletion]] $[FinSet, Set]$ is the free [[cartesian monoidal category|cartesian]] [[monoidally cocomplete category]] generated by an object. Thus $[FinSet, Set]$ plays the role of a cartesian analogue to $[\mathbb{P}^{op}, Set]$, the free [[symmetric monoidal category|symmetric]] [[monoidally cocomplete category]] on an object, where $\mathbb{P} = Core(FinSet)$ is the [[core]] of [[FinSet]], the [[permutation groupoid]]. And in the same way that $[\mathbb{P}^{op}, Set]$ is a [[monoidal topos]] whose monoids are symmetric or permutative [[operads]] (as discussed at _[operad -- a detailed conceptual treatment](operad#Conceptual)_), so $[FinSet, Set]$ is seen as a monoidal topos whose monoids are cartesian operads, aka [[Lawvere theories]]. Some material on this can be found at _[[toddtrimble:Towards a doctrine of operads]]_.

### The functorial point of view

Consider the forgetful [[2-functor]] $U:GrTop^{op}\to Cat$ from the opposite of the 2-category $GrTop$ of Grothendieck toposes and geometric morphisms that maps a topos to its underlying category and a geometric morphism to its [[inverse image functor]]. The object classifier $\mathcal{S}[\mathbb{O}]$ is a [[representing object]] for $U$.

For more on this functorial approach to geometric theories see at [[geometric theory#FunctorialDefinition]] or Johnstone ([2002, vol.1 pp.424ff](#JT02)).

### The generalized space point of view

The universal property says that maps (geometric morphisms) from a Grothendieck topos $\mathcal{E}$ to $\mathcal{S}[\mathbb{O}]$ are equivalent to the objects of $\mathcal{E}$, the sheaves over the generalized space of whatever $\mathcal{E}$ classifies. But $\mathcal{S}[\mathbb{O}]$ is the generalized space of "sets", so sheaves should be understood as continuous set-valued maps.
This is seen most clearly when $\mathcal{E}$ is sheaves over an [[point-free topology|ungeneralized space]] $X$. The sheaf is equivalent to a local homeomorphism to $X$, and the set-valued map takes points of $X$ to the stalks, the fibres of the local homeomorphism.

So what are the sheaves over $\mathcal{S}[\mathbb{O}]$, i.e. its objects? They are continuous maps $F$ from the space of sets to itself. All continuous maps (geometric morphisms) preserve filtered colimits of points, and it follows that $F$ is determined by its action on finite cardinals. Hence $\mathcal{S}[\mathbb{O}]$ is - at least - a subcategory of $[FinSet, Set]$.

### The object classifier and exponentiability

Recall that a [[locale]] $X$ is  called _exponentiable_ (in the category of locales) if the [[exponential object|exponential]] $Y^X$ exists for all locales $Y$. Interestingly, exponentiability of $X$ hinges on the existence of the single exponential $S^X$ where $S$ is the [[Sierpinski space]]: $Y^X$ exists for all $Y$ iff $S^X$ exists.

In the 2-category $GrTop$ the object classifier $\mathcal{S}[\mathbb{O}]$ takes over the role of the Sierpinski space and we have the following

+-- {: .num_prop}
###### Proposition
A [[Grothendieck topos]] $\mathcal{E}$ is [[exponentiable topos|exponentiable]] iff the exponential $\mathcal{S}[\mathbb{O}]^\mathcal{E}$ exists.

=--

This result is due to Johnstone-Joyal ([1982, p.257](#JJ82)) and occurs as theorem 4.3.1 of Johnstone ([2002, vol.1 p.433](#J02)).


## The pointed object classifier

[[pointed object|Pointed objects]] are important in [[homotopy theory]]. Similarly to objects, they arise as models of a geometric theory and this [[theory of objects|theory of pointed objects]] $\mathbb{O}_\ast$  is, of course, classified by a topos, namely, the presheaf topos $[FinSet_\ast, Set]$ on the opposite $FinSet_\ast^{op}$ of the category of finite [[pointed sets]] whose skeleton is [[Segal's category]], hence $[FinSet_\ast, Set]$ is equivalent to the topos of "$\Gamma$-sets": cf. [[Gamma-space]] and for the role as a classifying space the following MO-discussion: [link](http://mathoverflow.net/questions/85600/what-do-gamma-sets-classify) .[^classi]

[^classi]: More generally, classifying toposes for [[Horn theory|universal Horn theories]] $\mathbb{T}$ correspond to the respective toposes of covariant set-valued functors on the category of finitely presentable models of $\mathbb{T}$ (Blass&Scedrov (1983)).

Since the theory $\mathbb{O}_\ast$ is an extension of $\mathbb{O}$, it can be treated relatively as an internal theory in $\mathcal{S}[\mathbb{O}]$. There it is just the theory of elements of the generic set $G$, in other words the propositional theory for the discrete space of $G$. Discrete spaces are always got as slice toposes, so $\mathcal{S}[\mathbb{O}_\ast]$ is equivalent to

$$[FinSet, Set]/G\simeq [(\underset{FinSet^{op}}{\int} G)^{op},Set]\;.$$

$G$ is the inclusion functor $FinSet \to Set$, mapping each natural number $n$ to its finite cardinal $\{0,\ldots,n-1\}$.

The forgetful map (geometric morphism) from $\mathcal{S}[\mathbb{O}_\ast]$ to $\mathcal{S}[\mathbb{O}]$, forgetting the point, is the generic local homeomorphism. Every local homeomorphism is a bipullback of it.

## Related entries

* [[theory of objects]]

* [[classifying topos]]

* [[geometric theory]]

* [[exponentiable topos]]

* [[Sierpinski space]]

## References

* [[Peter Johnstone|P. T. Johnstone]], _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). (sec. 6.3)

* {#JT02}[[Peter Johnstone]], _[[Sketches of an Elephant]]_ , Oxford UP 2002. (sections B4.2 pp.424-432, D3.2 pp.901-910)

* {#JJ82}[[Peter Johnstone]], [[André Joyal]], _Continuous categories and exponentiable toposes_ ,  JPAA **25** (1982) pp.255-296.

* [[Peter Johnstone]], [[Gavin Wraith]], _Algebraic Theories in a Topos_ , pp.141-242 in LNM **661** Springer Heidelberg 1978. (ch. IV, pp.175ff)

* [[Saunders Mac Lane]], [[Ieke Moerdijk]]: _[[Sheaves in Geometry and Logic]]_, Springer Heidelberg 1994. (sec.VIII.4)

* [[Andreas Blass]], _Classifying topoi and the axiom of infinity_ , Algebra Universalis **26** (1989) pp.341-345. {#blass}

* [[Andreas Blass]], Andrej Scedrov, _Classifying topoi and finite forcing_ , JPAA **28** (1983) pp.111-140.

* [[Marta Bunge]], [[Jonathon Funk]], _Singular Coverings of Toposes_ , Springer LNM **1890** Heidelberg 2006.

* [[Richard Garner]], _Lawvere theories, finitary monads and Cauchy-completion_ , JPAA **218** no.11 (2014) pp.1973&#8211;1988. ([preprint](http://comp.mq.edu.au/~rgarner/Papers/FSet.pdf))
 {#Garner13}

* [[Gavin Wraith]], _Topos El&#233;mentaire et Arithm&#233;tique_ , Cah. Top. G&#233;om. Diff. Cat. **XIV-2** (1973) pp.217-218. ([proceedings colloque Amiens 1973](http://archive.numdam.org/article/CTGDC_1973__14_2_153_0.pdf), 3.92 MB)

[[!redirects classifying topos for the theory of objects]]
[[!redirects classifying topos for the theory of pointed objects]]