+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

Problems of [[set theory]] arise by the unjustified [[recursion]] of the naive notion of a 'collection of things.' If 'Col' is one notion of collections (such as '[[set|Set]]' or '[[class|Class]]'), then the notion 'Col of all Cols' is in general problematic, as it is subject to the construction of [[Russell's paradox|Russell-style]] [[paradoxes]] (although it is not the only source of such paradoxes).

One way out is to consider a hierarchy of notions of collections: Postulate that the collection of all 'Col's is not a 'Col' itself but instead is another notion of collection, 'Col+'. We may thus speak of the 'Col+ of all Cols.' Similarly, the collection of all 'Col+'-type collections may be taken to be 'Col++,' and so on.

One formalization of this idea is that of a _Grothendieck universe_. This is defined to be a [[set]] $U$ that behaves like a 'set+ of all small sets' in that all the standard operations of set theory (union, power set, etc.) can be performed on its elements.

Although developed for application to [[category theory]], the definition is usually given in a form that only makes sense in a [[material set theory|membership-based set theory]]. On this page, we consider only that version; for a form that makes sense in [[structural set theory]] see instead at *[[universe in a topos]]*.



## Definition

\begin{definition}
\label{GrothendieckUniverse}
A **Grothendieck universe** is a [[pure set]] $ U $ such that:

1. (transitivity) for all $ u \in U $ and $t\in u$, we have $ t \in U $;

1. ([[power set]]) for all $ u \in U $, we have $ \mathcal{P}(u) \in U $;

1. ([[empty set]]) $ \varnothing \in U $;

1. ([[unions]]) for all $ I \in U $ and functions $ u: I \to U $, we have $\underset{i \in I}{\bigcup} u_{i} \in U $.

\end{definition}

\begin{remark}
**(variant definitions)**
\linebreak
Some authors leave out (3), which allows the empty set $ \varnothing $ itself to be a Grothendieck universe.  Other authors use the set $ \mathbb{N} $ of [[natural numbers]] in place of $ \empty $ in (3), which prevents the [[countable set]] $ V_{\omega} $ of [[hereditarily finite sets]] from being a Grothendieck universe.
\end{remark}


\begin{remark}
**(terminology)**
Given a universe $U$, an element of $U$ is called a **$U$-small set**, while a [[subset]] of $U$ is called **$U$-moderate**. Every $U$-small set is $U$-moderate by requirement (1) of def. \ref{GrothendieckUniverse}. If the universe $U$ is understood, we may simply say **small** and **moderate**.

The term **$ U $-large** is ambiguous; it sometimes means 'not small' but sometimes means the same as 'moderate' (or 'moderate but not small'). The reason is that language that distinguishes 'small' from 'large' in terms of sets and [[proper class|proper classes]] translates fairly directly into terms of $ U $-small and $ U $-moderate sets. To be precise, if we redefine 'set' to mean '$ U $-small set,' then every proper class in this new world of sets will be represented by a $ U $-moderate set (a subset of $ U $). Those sets that are not even $ U $-moderate are 'too large' to be translated into language of proper classes.

(Note, though, that not all $ U $-moderate sets represent proper classes in the language of set theory relative to the world of $ U $-small sets, only those that are _first-order definable_ from $ U $-small sets. In fact, if $ \kappa $ is the [[cardinal number|cardinality]] of the universe $ U $, then there are only $ \kappa $ proper classes relative to $ U $, but there are $ 2^{\kappa} $-many $ U $-moderate sets.)

As defined above in def. \ref{GrothendieckUniverse}, these concepts violate the [[principle of equivalence]], as two sets may be [[isomorphism|isomorphic]] yet have different properties with respect to $ U $. However, a set which is isomorphic to a $ U $-small or $ U $-moderate set is called **essentially** $ U $-small or $ U $-moderate; these respect the [[principle of equivalence]].
\end{remark}



## Consequences

From the definition above, one can prove additional closure properties of a universe $ U $, including the usual codings in pure set theory of [[function sets]] and [[cartesian products]] and [[disjoint unions]] of sets, using the following lemmata:

+-- {: .num_lemma}
###### Lemma
If $ t $ is a [[subset]] of $ u $ and $ u \in U $, then $ t \in U $.
=--
+-- {: .proof}
###### Proof
By (2), $ \mathcal{P}(u) \in U $. Then as $ t \in \mathcal{P}(u) $, we have $ t \in U $ by (1).
=--

+-- {: .num_lemma}
###### Lemma
If $ u, v \in U $, then $ u \cup v \in U $.
=--
+-- {: .proof}
###### Proof
As $ \empty \in U $ by (3), so are $ \star \stackrel{\text{df}}{=} \mathcal{P}(\empty) $ and $ TV \stackrel{\text{df}}{=} \mathcal{P}(\star) $ by (2). Even in [[constructive mathematics]], $ 2 = \{ \bot,\top \} $ is a subset of $ TV $, so $ 2 \in U $ by Lemma 1. Then $ (\bot \mapsto u,\top \mapsto v) $ is a function from $ 2 \to U $, so the union $ u \cup v $ in $ U $ by (4).
=--

Then using their usual encodings in set theory:

* the nullary cartesian product $ \star $ is $ \mathcal{P}(\varnothing) $ as in the previous proof;
* the binary cartesian product $ u \times v $ is a subset of $ \mathcal{P}(\mathcal{P}(u \cup v)) $;
* the general cartesian product $ \displaystyle \prod_{i \in I} u_{i} $ is a subset of $ \displaystyle \mathcal{P} \left( I \times \bigcup_{i \in I} u_{i} \right) $;
* the nullary disjoint union is $ \varnothing $;
* the binary disjoint union $ u \uplus v $ is a subset of $ 2 \times (u \cup v) $;
* the general disjoint union $ \displaystyle \biguplus_{i \in I} u_{i} $ is a subset of $ \displaystyle I \times \bigcup_{i \in I} u_{i} $;
* the set of functions $ u \to v $ is a subset of $ \mathcal{P}(u \times v) $.



## Axiom of Universes

If $ U $ is a Grothendieck universe, then it is easy to show that $ U $ is itself a model of [[ZFC]] (minus the axiom of infinity unless you modify (3) to rule out countable universes). Therefore, one cannot prove in ZFC the existence of a Grothendieck universe containing $ \mathbb{N} $, and so we need extra set-theoretic axioms to ensure that uncountable universes exist. Grothendieck's original proposal was to add the following **axiom of universes** to the usual axioms of set theory:

* For every set $ s $, there exists a universe $ U $ that contains $ s $, i.e., $ s \in U $.

In this way, whenever any operation leads one outside of a given Grothendieck universe (see applications below), there is guaranteed to be a bigger Grothendieck universe in which one lands. In other words, every set is small if your universe is large enough!

Later, Mac Lane pointed out that often, it suffices to assume the existence of *one* uncountable universe. In particular, any discussion of 'small' and 'large' that can be stated in terms of sets and proper classes can also be stated in terms of a single universe $ U $ (with 'large' meaning '$ U $-moderate but not $ U $-small').


## Large cardinals

If $ U $ is a Grothendieck universe, then one can prove in ZFC that it must be of the form $ V_{\kappa} $, where $ \kappa $ is a (strongly) [[inaccessible cardinal]] ([Williams](#Williams)). Here, $ V_{\kappa} $ is the $ \kappa $-th set in the [[von Neumann hierarchy]] of pure sets. Conversely, every such $ V_{\kappa} $ is a Grothendieck universe. Thus, the existence of Grothendieck universes is equivalent to the existence of inaccessible cardinals, and so the axiom of universes is equivalent to the 'large cardinal axiom' that 'there exist arbitrarily large inaccessible cardinals.'

It is worth noting, for those with foundational worries, that the axiom of universes is much, much weaker than many large cardinal axioms which are routinely used, and believed to be consistent, by modern set theorists. Of course, one cannot _prove_ the consistency of any large cardinal axiom (if it really is consistent) except by invoking a stronger one.


## Structural Version

An equivalent concept (at least for the purposes of category theory) can also be defined in structural set theories (like [[ETCS]]). Please see [[universe in a topos]].


## Examples

The set $ V_{\omega} $ of [[hereditarily finite sets]] (finite sets of finite sets of...) is a Grothendieck universe, unless you phrase axiom (3) in the definition to specifically rule it out. In this way, the axiom of infinity can be seen as a simple universe axiom (stating that at least one universe exists), and Mac Lane's axiom that an uncountable universe exists is merely one step further.

If you refrain from using the axiom of universes (except perhaps once, to get $ \mathbb{N} $ as above), then the set of all sets (or cardinal numbers) that you can actually construct is a Grothendieck universe. Of course, you cannot possibly have proved that this universe exists, but the intuition that you ought be able to form the collection of 'everything that we've used so far' is the justification for the axiom of universes.

Similarly, if you use the axiom of universes at most $ n $ times, then the set of all sets that you can construct with this restriction is a Grothendieck universe. Thus, we can find a sequence $ U_{1} \in U_{2} \in U_{3} \in \ldots $ of universes. The [[axiom of replacement]] then allows us to form the union (a directed [[colimit]]) $ \bigcup_{n \lt \omega} U_{n} $. This will not be a universe (it violates (4), by definition), but we can use the axiom of universes again to show that it is in some universe $ U_{\omega} $. Proceeding in this way, we can construct a tower of universes indexed by the [[ordinal numbers]].

The set of all sets that can be constructed using the axioms of ZFC together with the axiom of universes is, if it exists, again a universe which contains all the $ U_{\alpha} $ constructed above. Of course, it cannot be shown to exist using only ZFC and the axiom of universes; the axiom of universes is not the final word on large cardinal axioms by any means.


## Applications

Let $ U Set $ be the [[category]] of $ U $-small sets, a [[full subcategory]] of [[Set]]. It is common, especially when $ U $ is understood, to redefine $ Set $ to mean $ U Set $; here we keep the distinction for clarity. However, when $ Set $ means $ U Set $, sometimes $ SET $ is used to mean the category of _all_ sets.

A category whose set of morphisms is (essentially) $ U $-small may be called a $ U $-[[small category]]; it can also be thought of as an [[internal category]] in $ U Set $. A category whose [[hom-sets]] are all (essentially) $ U $-small may be called [[locally small category|locally]] $ U $-small; it can also be thought of as an [[enriched category]] over $ U Set $. Every $ U $-small category is locally $ U $-small.

A category whose set of morphisms is $ U $-moderate may be called a $ U $-[[large category|moderate category]]; again '$ U $-large' may mean 'not $ U $-small,' '$ U $-moderate,' or both. In practice, most $ U $-moderate categories are locally $ U $-small and vice versa, but there is no theorem that this must be true. Note that $ U Set $ itself is $ U $-moderate and locally $ U $-small but not $ U $-small.

All notions of category theory that reference size, such as [[complete category|completeness]] and [[locally presentable category|local presentability]], must then be relativized to $ U $. In order to move from a category defined in one universe to another, we need a procedure of [[universe enlargement]].


### Presheaf Categories

Let $ C $ be a $ U $-small category. Then the category of $ U $-[[presheaf|presheaves]] on $ C $ (the [[functor category]] $ [C^{op},U Set] $) is also $ U $-moderate and locally $ U $-small but not $ U $-small unless $ C $ is empty. ($ U Set $ itself is the special case of this where $ C $ is the [[point]].) These arguments go as follows:

* $ U PSh(C) $ is $ U $-moderate: An upper bound for the size of $ [C^{op},U Set] $, hence of the set $ Obj([C^{op},U Set]) $ is the size of $ \{ F: Obj(C) \times Mor(C) \to U \} $, where both $ Obj(C) $ and $ Mor(C) $ are in $ U Set $. Hence, we are looking at the cardinal number $ |U|^{|u| \times |v|} $, where $ u = Obj(C) $ and $ v = Mor(C) $. Use the fact that any Grothendieck universe must be infinite (since it has $ \varnothing $, $ \mathcal{P}(\varnothing) $, etc.), and the result follows from cardinal arithmetic that $ \kappa^{\lambda} = \kappa $ if $ \lambda \lt \kappa $ and $ \kappa $ is infinite.

* $ U PSh(C) $ is locally $ U $-small: An upper bound for the size of the set of morphisms between two functors $ F,G: C^{op} \to U Set $ is the disjoint union indexed by the objects $ c $ of $ C $ over the $ U $-sets $ G(c)^{F(c)} $. Now $ G(c)^{F(c)} \in U $ as it is a function set and $ \displaystyle \bigcup_{c \in Obj(C)} G(c)^{F(c)} $ by the assumption that unions stay in $ U $.

Now let $ C $ be a $ U $-moderate category (and not small). Then the category of $ U $-presheaves on $ C $ is not even locally $ U $-small, nor is it even $ U $-moderate (it is 'too large'). However, it is locally $ U $-moderate. Also, it is quite possible, if $ C $ is a $ U $-[[large site|moderate site]], that the category of $ U $-[[sheaf|sheaves]] on $ C $ is $ U $-moderate and locally $ U $-small.

+-- {: .standout}
*Note:* Here we are considering presheaves on $ C $ with values in $ U $-small sets. In many cases, a more appropriate notion of '$ U $-small presheaf' is that discussed at [[small presheaf]], namely a presheaf that is a $ U $-small colimit of representables.
=--


## Alternative Approaches

* A different, potentially much more elegant and natural proposal for solving the problem to be solved by Grothendieck universes is that described at [[michaelshulman:category of all sets|category of all sets]]. Don't get your hopes up too high, though; even if it works, it isn't quite the category theory you're used to.

## Related concepts

* [[Tarski-Grothendieck set theory]]


## References
 {#References}

As a solution to foundational problems of [[category theory]] the concept was apparently brought up by Grothendieck (cf. [below](#Kroemer06), p.149) in the context of 1958 Bourbaki discussions. It makes a sketchy appearance in [[SGA1]] in exposé VI on [[fibered category|fibered categories]].

Fuller early accounts are

* [[Pierre Gabriel]], *[[Des Categories Abeliennes]]*, Bulletin de la Société Mathématique de France **90** (1962) 323-448 &lbrack;[numdam:BSMF_1962__90__323_0](http://www.numdam.org/item?id=BSMF_1962__90__323_0)&rbrack;

* [[Johann Sonner]], *On the formal definition of categories*, Math. Zeitschr. **80** (1962) 163-176 &lbrack;[eudml:170093](https://eudml.org/doc/170093), [[Sonner-FormalDefCategories.pdf:file]]&rbrack;

The "official" account is then:

* [[Nicolas Bourbaki]], _Univers_, Appendix to Expose I in [[SGA 4]] (1963-64)

Further early discussion:

* [[Saunders MacLane]], *One universe as a foundation for category theory*,  In: *Reports of the Midwest Category Seminar III*, Lecture Notes in Mathematics **106**, Springer (1969) 192-200 &lbrack;[doi:10.1007/BFb0059147](https://doi.org/10.1007/BFb0059147)&rbrack;

Comprehensive historical review with further references:

* [[Ralf Krömer]], §6.4.4 in: *Tool and object: A history and philosophy of category theory*, Science Networks. Historical Studies **32**, Springer (2007) &lbrack;[doi:10.1007/978-3-7643-7524-9](https://doi.org/10.1007/978-3-7643-7524-9)&rbrack;

* {#Kroemer06}[[Ralf Krömer]], _La « machine de Grothendieck », se fonde-t-elle seulement sur des vocables métamathématiques? Bourbaki et les catégories au cours des années cinquante_, Revue d’Histoire des Mathématiques **12** 111–154 ([Numdam](http://www.numdam.org/item/RHM_2006__12_1_119_0/))

For more information on the origin of the terminology consult:

* [[Colin McLarty]], _Authorship of Grothendieck universes_ [Mathoverflow](https://mathoverflow.net/questions/117517/authorship-of-grothendieck-universes)

Most texts on [[category theory]] and related topics mention the topic of Grothendieck universes without providing details. Exceptions are:

* {#Isbell66} [[John Isbell]], *Structure of categories*, Bulletin of the American Mathematical Society **72** (1966), 619-655. &lbrack;[euclid:1183528163](http://projecteuclid.org/euclid.bams/1183528163), [ams:1966-72-04/S0002-9904-1966-11541-0](https://www.ams.org/journals/bull/1966-72-04/S0002-9904-1966-11541-0/)&rbrack;

* [[Horst Schubert]], §3.2 in: *Categories*, Springer (1972) &lbrack;[doi:10.1007/978-3-642-65364-3](https://doi.org/10.1007/978-3-642-65364-3)&rbrack;

Discussions spelling out more details:

* [[Mike Shulman]], _Set theory for category theory_ &lbrack;[arXiv:0810.1279](http://arxiv.org/abs/0810.1279)&rbrack;

* {#Murfet06} [[Daniel Murfet]], _Foundations for category theory_ (2006) &lbrack;[pdf](http://therisingsea.org/notes/FoundationsForCategoryTheory.pdf), [[Murfet-GrothendieckUniverses.pdf:file]]&rbrack;

* [[Zhen Lin Low]], _Universes for category theory_ &lbrack;[arxiv/1304.5227](http://arxiv.org/abs/1304.5227)&rbrack;

* [[Paul Blain Levy]], _Formulating Categorical Concepts using Classes_ &lbrack;[arXiv:1801.08528](https://arxiv.org/abs/1801.08528)&rbrack;



The proof that a Grothendieck universe is equivalently a set of $ \kappa $-small sets for $ \kappa $ an [[inaccessible cardinal]] is in 

* {#Williams} N. H. Williams, _On Grothendieck universes_, Compositio Mathematica, tome 21 no 1 (1969) ([numdam]( http://www.numdam.org/item?id=CM_1969__21_1_1_0))
 

SGA uses universes and much of modern results in algebraic geometry use general results from SGA, including Wiles proof of Fermat's theorem. Colin McLarty discusses how to remove the need for universes in Wiles' proof in

* [[Colin McLarty]], _What does it take to prove Fermat's last theorem? -- Grothendieck and the logic of number theory_, [pdf](http://www.cwru.edu/artsci/phil/Proving_FLT.pdf)


category: foundational axiom

[[!redirects Grothendieck universe]]
[[!redirects Grothendieck universes]]

[[!redirects axiom of Grothendieck universes]]
[[!redirects axiom of universes]]