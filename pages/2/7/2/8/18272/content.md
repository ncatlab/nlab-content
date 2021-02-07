
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Introduction 

There is a battery of little [[set theory|set-theoretic]] [[lemmas]] which inevitably recur when laying the [[foundations]] of core [[mathematics]], as when teaching the standard curriculum that includes basic [[topology]], real [[analysis]], [[algebra]], and so forth. In this article we collect some of those core results having to do with the properties of [[image]] and [[pre-image]] operators, especially regarding their preservation (or not) of set-theoretic operations like [[unions]] and [[intersections]]. 

The attitude and approach of the mathematics professor toward such routine bread-and-butter issues is a matter of some interest. A professional, upon being presented with any one of these "naive set theory" [[propositions]], will probably be able to verify it on the spot using ordinary follow-your-nose logic, driven by the definitions. While being able to produce such verifications is part of basic training in mathematics, it is not quite the same as giving an *explanation*, and in fact even good mathematicians trained this way may struggle to remember "now which is it that direct images preserve, unions or intersections?"[^1] 

[^1]: There is a famous story of how [[Mikhail Yakovlevich Suslin|Suslin]] discovered an error in an argument of [[Lebesgue]], concerning just this type of routine set-theoretic detail (that Lebesgue perhaps just misremembered). In response, [[Mikhail Yakovlevich Suslin|Suslin]] was led to develop some of the basics of [[descriptive set theory]]. Details of the story have been told by Dave Renfro, [here](http://mathforum.org/kb/message.jspa?messageID=4966721) and [here](http://mathforum.org/kb/message.jspa?messageID=4967733)

A strong pedagogy would not only instill this sort of basic training, but make the battery of routine results more memorable by concentrating their essence in one or two basic principles that provide an explanatory basis for the rest. According to [Lawvere 69](#Lawvere69), [Lawvere 05](#Lawvere05), logic is an interlocking system of certain types of [[adjoint functors]], and we believe putting those [[adjunction|adjoint]] relationships front and center and seeing how the rest flows from them is an effective way to arrange the facts. 

## Statements

+-- {: .num_prop #PreservationOfUnionsAndIntersectionsOfSets}
###### Proposition
**([[images]] preserve [[unions]] but not in general [[intersections]])**

Let $f \colon X \longrightarrow Y$ be a [[function]] between [[sets]]. Let $\{S_i \subset X\}_{i \in I}$ be a set of [[subsets]] of $X$. Then 

1. $im_f\left( \underset{i \in I}{\cup}  S_i\right) = \left(\underset{i \in I}{\cup} im_f(S_i)\right)$ (the [[image]] under $f$ of a [[union]] of subsets is the union of the images)

1. $im_f\left( \underset{i \in I}{\cap}  S_i\right) \subset \left(\underset{i \in I}{\cap} im_f(S_i)\right)$ (the [[image]] under $f$ of the [[intersection]] of the subsets is contained in the intersection of the images).

The [[injective function|injection]] in the second item is in general proper. If $f$ is an [[injective function]] then this is a [[bijection]]:

* $(f\,\text{injective}) \Rightarrow \left(im_f\left( \underset{i \in I}{\cap}  S_i\right) = \left(\underset{i \in I}{\cap} im_f(S_i)\right)\right)$ 

*provided* that $I$ is [[inhabited set|inhabited]]. 

=-- 

+-- {: .num_prop #PreImagePreservesUnionsAndIntersections} 
###### Proposition 
**(pre-images preserve unions and intersections)** 

Let $f \colon X \longrightarrow Y$ be a [[function]] between [[sets]]. Let $\{T_i \subset Y\}_{i \in I}$ be a set of [[subsets]] of $Y$. Then 

1. $f^{-1}\left( \underset{i \in I}{\cup}  T_i\right) = \left(\underset{i \in I}{\cup} f^{-1}(T_i)\right)$ (the [[pre-image]] under $f$ of a [[union]] of subsets is the union of the pre-images), 

1. $f^{-1}\left( \underset{i \in I}{\cap}  T_i\right) = \left(\underset{i \in I}{\cap} f^{-1}(T_i)\right)$ (the [[pre-image]] under $f$ of the [[intersection]] of the subsets is the intersection of the pre-images).
=-- 

+-- {: .num_prop} 
###### Proposition 
**(projection formula)** 
Let $f: X \longrightarrow Y$ be a [[function]] between [[sets]]. Let $S \subset X$ be a [[subset]] of $X$, and $T \subseteq Y$ be a subset of $Y$. Then 

$$f(S) \cap T = f(S \cap f^{-1}(T)).$$ 
=--

## Proofs via adjoints 

The properties 1., 2. of Proposition \ref{PreservationOfUnionsAndIntersectionsOfSets} may be proved by appeal to fundamental relationships between [[direct image]] and [[inverse image]] and the like, which [[category theory|category theorists]] call [[adjunctions]] (similar in form to adjoints in linear algebra). The advantage of this type of proof is that, despite its utter simplicity, it generalizes to much wider contexts (beyond elementary classical set theory). 

### Direct images preserve unions, inverse images preserve intersections 

The first such relationship is that, for all subsets $S \subseteq X$ and $T \subseteq Y$, we have 

$$f(S) \subseteq T \qquad iff \qquad S \subseteq f^{-1}(T)$$ 

One says in this situation that the direct image mapping $f(-)$ is *[[left adjoint]]* to the inverse image mapping $f^{-1}(-)$, or that inverse image is *[[right adjoint]]* to direct image. This terminology is guided by the formally similar usage in linear algebra where linear mappings $A$ and $B$ are adjoint if one has an equation 

$$\langle A x, y \rangle = \langle x, B y \rangle$$ 

for all $x, y$ in suitable [[inner product spaces]] (and in fact the analogy is not idle; see for instance [Baez](#JB97)). 

In that case, we have the following elementary inferences: 

$$\array{
\bigcup_{i \in I} f(S_i) \subseteq T & iff & (\forall_{i \in I})\; f(S_i) \subseteq T \\ 
 & iff & (\forall_{i \in I})\; S_i \subseteq f^{-1}(T) \\ 
 & iff & \bigcup_{i \in I} S_i \subseteq f^{-1}(T) \\ 
 & iff & f\left(\bigcup_{i \in I} S_i\right) \subseteq T
}$$ 

where the first and third lines use the defining [[universal property|property]] of unions. Then, putting $T = \bigcup_{i \in I} f(S_i)$ and reasoning forward, we get $f\left(\bigcup_{i \in I} S_i\right) \subseteq \bigcup_{i \in I} f(S_i)$. On the other hand, putting $T = f\left(\bigcup_{i \in I} S_i\right)$ and reasoning backward, we get $\bigcup_{i \in I} f(S_i) \subseteq f\left(\bigcup_{i \in I} S_i\right)$. These two inclusions together give $\bigcup_{i \in I} f(S_i) = f\left(\bigcup_{i \in I} S_i\right)$. 

The [[duality|dual]] of this proof immediately gives the fact that inverse images preserve arbitrary intersections, but let us spell it out directly: 

$$\array{
S \subseteq \bigcap_{i \in I} f^{-1}(T_i) & iff & (\forall_{i \in I})\; S \subseteq f^{-1}(T_i) \\ 
 & iff & (\forall_{i \in I})\; f(S) \subseteq T_i \\ 
 & iff & f(S) \subseteq \bigcap_{i \in I} T_i \\ 
 & iff & S \subseteq f^{-1}\left(\bigcap_{i \in I} T_i \right)
}$$ 

and again by using the reasoning forward/backward trick, we infer $\bigcap_{i \in I} f^{-1}(T_i) = f^{-1}\left(\bigcap_{i \in I} T_i\right)$. 

+-- {: .num_remark} 
###### Remark 
The "reasoning forward/backward trick" may be summarized by saying that in a [[poset]], we have $A = B$ iff ($A \leq T \Leftrightarrow B \leq T$), or dually that $A = B$ iff ($S \leq A \Leftrightarrow S \leq B$). This trick is vastly extrapolated by the [[Yoneda lemma]]. 
=-- 

+-- {: .num_remark #Lawvere} 
###### Remark 
People who work with categorial forms of logic denote direct images $f(S)$ by $\exists_f(S)$. The suggestion is to view [[existential quantifier|existential quantification]] as corresponding to taking of a [[direct image]]. For example, given a property $P$ of pairs $(x, y)$, i.e. a subset $P \subseteq X \times Y$ where we write $P(x, y)$ to say $(x, y) \in P$ holds, the set of $y$ such that $(\exists_{x \in X})\; P(x, y)$ holds is exactly the direct image $\pi_2(P)$ under the [[projection map]] $\pi_2: X \times Y \to Y$. This suggests furthermore a useful extended meaning of existential quantification, by considering direct images along more general maps, not just projection maps.  With this in mind, category theorists often denote $f(S) = \{y \in Y: (\exists_{x: f(x) = y})\; x \in S\}$ by $\exists_f(S)$, giving an operator $\exists_f: P(X) \to P(Y)$ between [[power sets]]. This is [[left adjoint]] to the taking of [[inverse images]] $T \mapsto f^{-1}(T)$ as an operator $f^{-1}: P(Y) \to P(X)$, also denoted by $f^\ast: P(Y) \to P(X)$. The adjointness relationship between direct image and inverse image, denoted by $\exists_f \dashv f^\ast$, is an example of a famous slogan due to [[Lawvere]]: "Logical quantification is adjoint to substitution" (with resonances far beyond the purview of logic as ordinarily conceived; see Remark \ref{MoreJargon}). 
=-- 

As for direct images and intersections, we have 

$$f\left(\bigcap_{i \in I} S_i\right) \subseteq \bigcap_{i \in I} f(S_i)$$ 

because this is equivalent to $(\forall_{i \in I})\; f\left(\bigcap_{i \in I} S_i\right) \subseteq f(S_i)$, which is obvious because for all $i \in I$, we have $\bigcap_{i \in I} S_i \subseteq S_i$, and $f(A) \subseteq f(B)$ if $A \subseteq B$. 

This inclusion is not usually an equality. For example, in the [[cartesian space]] $\mathbb{R}^2$ with $x y$-coordinates, the [[projection]] $(x, y) \mapsto x$ does not preserve the intersection of the lines $y = 1$ and $y = 2$. 

However, if $f: X \to Y$ is injective, then the direct image operator $S \mapsto f(S)$ *does* preserve intersections of subsets $(S_i)_{i \in I}$ indexed over *nonempty* sets $I$. This is not difficult to check once we verify that 

* For any map $f: X \to Y$ (not necessarily injective) and any subset $T \subseteq Y$, we have $f(X) \cap T = f(f^{-1}(T))$. 

* If $f$ is injective, then for any subset $S \subseteq X$ we have $S = f^{-1}(f(S))$. 

For then, if $T = \bigcap_{i \in I} f(S_i)$ and $I$ is inhabited, we have for some $i$ that $T \subseteq f(S_i) \subseteq f(X)$, and then 

$$\array{
T = f(X) \cap T & = & f(f^{-1}(T)) \\ 
 & = & f(f^{-1}(\bigcap_i f(S_i))) \\ 
 & = & f\left(\bigcap_{i \in I} f^{-1}(f(S_i))\right) \\ 
 & = & f\left(\bigcap_{i \in I} S_i\right)
}$$ 

which was to be shown. 

### Inverse images preserve unions, codirect images preserve intersections 

As for the statement that inverse images of unions are unions of inverse images, it turns out this follows from a second fundamental logical adjunction. For a function $f: X \to Y$ and a subset $U \subseteq X$, define 

$$\forall_f(U) = \{y \in Y: (\forall_{x: f(x) = y})\; x \in U\}$$ 

which is analogous to the formula $\exists_f(S) = f(S) = \{y \in Y: (\exists_{x: f(x) = y})\; x \in S\}$ in Remark \ref{Lawvere}. (Alternatively, in [[classical logic]] where the [[negation]] operator $\neg$ on power sets means complementation, we have $\forall_f = \neg \exists_f \neg$.) Then it is easy to verify a second adjunction 

$$f^{-1}(T) \subseteq U \qquad iff \qquad T \subseteq \forall_f (U)$$ 

The same adjointness proof as used to prove property 1., then shows that the left adjoint part which here is the inverse image operator $f^{-1} = f^\ast: P(Y) \to P(X)$ preserves unions, and that right adjoint part which here is the "codirect image" operator $\forall_f: P(X) \to P(Y)$ preserves intersections. 

+-- {: .num_remark #MoreJargon}
###### Remark

In terms of some more [[category theory]] jargon the above situation may be phrased as follows:

Subsets of some set $S$ are the [[(-1)-truncated objects]] in the [[slice category]] $Set_{/S}$ of [[Set]] over $S$. Since [[Set]] is a [[topos]], every [[morphism]], i.e. [[function]] $X \longrightarrow Y$ induces a [[base change]] [[adjoint triple]]

$$
  Set_{/X}
     \underoverset
       {\underset{f^\ast}{\longrightarrow}}
       {\overset{f_!}{\longrightarrow}}
       {\overset{f_\ast}{\longleftarrow}}
  Set_{/Y}
  \,.
$$

Here in the language of [[type theory]]

1. the [[left adjoint]] $f_!$ is also called the [[dependent sum]] 

1. the middle morphism is also called [[context extension]]

1. the [[right adjoint]] $f_\ast$ is also called the [[dependent product]].

All this restricts to the (-1)-truncated objects by composing the left adjoint with [[(-1)-truncation]]. Then one also says that we are looking at a morphism in a [[hyperdoctrine]] and (under "[[propositions as types]]") may think of

1. the left adjoint $f_!$ as the [[existential quantifier]] $\exists_f$

1. the right adjoint $f_\ast$ as the [[universal quantifier]] $\forall_f$.

Now the fact that [[left adjoint]] $\exists_f$ preserves [[unions]] is the fact that [[left adjoints preserve colimits]], and the fact that the left- and [[right adjoint]] $f^\ast$ preserves unions and intersections is that in addition [[right adjoints preserve limits]].

=--

## Projection formula 

Another useful formula for interactions between images and pre-images and intersections is the projection formula: 

+-- {: .num_prop} 
###### Proposition 
Let $f: X \to Y$ be a function, and let $S \subseteq X, T \subseteq Y$ be subsets. Then $f(S) \cap T = f(S \cap f^{-1}(T))$. 
=-- 

+-- {: .proof} 
###### Proof 
The easy direction is the inclusion $f(S \cap f^{-1}(T)) \subseteq f(S) \cap T$: by the [[universal property|defining property]] of intersections, it suffices to show $f(S \cap f^{-1}(T)) \subseteq f(S)$ and $f(S \cap f^{-1}(T)) \subset T$. The first is clear since $S \cap f^{-1}(T) \subseteq S$, and $A \subseteq B$ implies $f(A) \subseteq f(B)$. Similarly, $f(S \cap f^{-1}(T)) \subseteq f(f^{-1}(T))$, and $f(f^{-1}(T)) \subseteq T$ since this is equivalent to $f^{-1}(T) \subseteq f^{-1}(T)$ by the adjunction between direct and inverse image. 

To be continued. 

=--




## Related statements

* [[countable unions of countable sets are countable]]

* [[limits and colimits by example]] 

## References 

The slogan of Lawvere on logic and adjoint functors appears in 

* {#Lawvere05} [[F. William Lawvere]], _An elementary theory of the category of sets_, Proceedings of the National Academy of Science of the U.S.A 52 (1965), 1506-1511. Reprinted in an expanded version, with commentary by Colin McLarty and by Lawvere, in Reprints in Theory and Applications of Categories, No. 11 (2005), pp. 1-35. ([link](http://www.tac.mta.ca/tac/reprints/articles/11/tr11abs.html)) 

based on

* {#Lawvere69} [[William Lawvere]], _[[Adjointness in Foundations]]_, ([TAC](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

The story of Lebesgue's slip that projections commute with intersections, in attempting to prove that [[projections]] of [[Borel sets]] are Borel, is well explained here: 

* Dave L. Renfro, *Mikhail Y. Suslin and Lebesgue's error*, two Mathforum posts dated July 29, 2006 (first post [here](http://mathforum.org/kb/message.jspa?messageID=4966721)). 

The analogy between adjoint functors and adjoints in linear algebra becomes very strong when jacking up from Hilbert spaces to [[2-Hilbert spaces]]. See 

* {#JB97} [[John C. Baez]], *Higher-Dimensional Algebra II. 2-Hilbert Spaces*, Advances in Mathematics, Volume 127 Issue 2 (10 May 1997), 125-189. [https://doi.org/10.1006/aima.1997.1617](https://doi.org/10.1006/aima.1997.1617) ([Elsevier link](http://www.sciencedirect.com/science/article/pii/S0001870897916170)) 


[[!redirects images preserve unions]]

[[!redirects the image of an intersection is contained in the intersection of the images]]
[[!redirects images of unions are unions of images]]
