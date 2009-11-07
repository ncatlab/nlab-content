A _regular category_ is a [[finitely complete category]] which admits a good notion of [[image]] factorization. A primary _raison d'etre_ behind regular categories $C$ is to have a decently behaved _calculus of [[relation]]s_ in $C$.  Regular categories are also the natural setting for [[internal logic|regular logic]].

## Definition

A category $C$ is **regular** if 

* It is finitely complete; 

* The [[kernel pair]] $p_1, p_2: e \,\rightrightarrows\, d$ of any $f: d \to c$ admits a [[coequalizer]];  and

* The pullback of a regular epi along any map is a regular epi.

Here the "kernel pair" is the parallel pair of projection maps coming out of a pullback $e$ of the diagram 

$$d \stackrel{f}{\to} c \stackrel{f}{\leftarrow} d$$

The kernel pair is always an [[congruence]] on $d$ in $C$; informally, $\ker(f)$ is the subobject of $d \times d$ consisting of pairs of elements which have the same value under $f$ (sometimes called the 'kernel' of a function in $\Set$). The coequalizer above is supposed to be the "object of equivalence classes" of $\ker(f)$ as an internal [[equivalence relation]].

A map which is the coequalizer of a parallel pair of morphisms is called a _[[regular epimorphism]]_. In fact, in any category satisfying the first two conditions above, every coequalizer is the coequalizer of its kernel pair. (See for instance Lemma 5.6.6 in _[[Practical Foundations]]_.)

The last condition may equivalently be stated in the form "coequalizers of kernel pairs are stable under pullback". However, it is not generally true in a regular category that the pullback of a general coequalizer diagram 

$$e \stackrel{\to}{\to} d \to c$$ 

along a morphism $c' \to c$ is again a coequalizer diagram. 

To form the image factorization of a map $f: d \to c$, let $q: d \to k$ be the coequalizer of the kernel pair of $f$. Since $f$ coequalizes its kernel pair, there is a unique map $i: k \to c$ such that $f = i q$. It may be shown from the regular category axioms that $i$ is monic and in fact represents the [[image]] of $f$, i.e., the smallest subobject through which $f$ factors.  Moreover, the classes of regular epis and of (all) monomorphisms form a [[orthogonal factorization system|factorization system]].

In fact, a regular category can alternately be defined as a finitely complete category with pullback-stable [[image]] factorizations.  See [[familial regularity and exactness]] for a generalization of this approach to include [[coherent category|coherent]] categories as well.


## Examples

* [[Set]] is a regular category. In fact, any [[topos]] is regular. More generally, a locally cartesian closed category with coequalizers is regular, and so any quasitopos is regular. 

* The category of models of any finitary algebraic theory (i.e., [[Lawvere theory]]) $T$ is regular. This applies in particular to the category [[Ab]] of abelian groups. 

* Any [[abelian category]] is regular. 

* If $C$ is regular, then so is $C^D$ for any category $D$. 

Examples of categories which are _not_ regular include [[Cat]], [[Pos]], and [[Top]]. 


## Remarks

1. As exactness properties go, the ones possessed by general regular categories are fairly moderate; the main condition is of course stability of regular epis under pullback. In the first place, the focus is just on certain coequalizers; finite coproducts aren't even mentioned. Some of that imbalance is redressed by the notion of l[[extensive category]], where coproducts are also stable under pullback (and are also disjoint). 

Further desirable exactness properties can be phrased in the language of [[Galois connection]]s. For each object $d$, consider the following relation $coeq$ between the class of parallel pairs $f, g: e \stackrel{\to}{\to} d$) and maps $h: d \to c$: 

$$\langle (f, g); h \rangle \in coeq \qquad iff \qquad h f = h g$$

[to be continued...]


## Making categories regular

Any category $C$ with [[finite limits]] has a **reg/lex completion** $C_{reg/lex}$ with the following properties:

* There is a [[full and faithful functor]] $C\hookrightarrow C_{reg/lex}$
* Each object of $C$ becomes [[projective object|projective]] in $C_{reg/lex}$
* Each left-exact functor $C\to D$, where $D$ is regular, extends to an essentially unique regular functor $C_{reg/lex}\to D$.

In particular, the reg/lex completion is a left adjoint to the [[forgetful functor]] from regular categories to lex categories (categories with finite limits).  The reg/lex completion can be obtained by "formally adding images" for all morphisms in $C$, or by "closing up" $C$ under images in its [[presheaf category]] $[C^{op},Set]$.  In general, even if $C$ is regular, $C_{reg/lex}$ is larger than $C$ (that is, it is a [[free cocompletion]] rather than merely a [[completion]]), although if $C$ satisfies the [[axiom of choice]] (in the sense that all [[regular epimorphisms]] are split), then $C\simeq C_{reg/lex}$.

See [[regular and exact completions]].

+-- {: .query}
H\'m, so what is $Set_{reg/lex}$ like if the axiom of choice fails in $Set$?  Some category like $Set$, but larger, in which every set becomes projective (but perhaps not every object in the larger category).  Of course, I\'d have to check that the statements above that this conclusion relies don\'t themselves use the axiom of choice in $Set$!  ---Toby

[[Mike Shulman]]: I believe that $Set_{reg/lex}$ admits the following simple description: it is the category of [[setoids]] $(X,\equiv)$ where a morphism $(X,\equiv_X)\to (Y,\equiv_Y)$ is a function $f\colon X\to Y$ such that $x\equiv x'$ implies $f(x)\equiv f(x')$, and two such morphisms $f$ and $g$ are set equal if $f(x)\equiv g(x)$ for all $x\in X$.  In this case $Set_{reg/lex}$ is already exact, and therefore it is the same as $Set_{ex/lex}$.  The monics in $Set_{reg/lex}$ are morphisms $f$ such that $f(x)\equiv f(x')$ implies $x\equiv x'$, and the regular epics are the morphisms $f\colon (X,\equiv_X)\to (Y,\equiv_Y)$ such that there exists a function $g\colon Y\to X$ such that $f(g(y))\equiv y$ for all $y\in Y$.  Evidently every set, considered as a setoid in the obvious way, is then regular projective.  And of course, if $Set$ satisfies AC, then every setoid is isomorphic to a set in $Set_{reg/lex}$.

_Toby_:  This is very interesting!  I should check that your construction satisfies the universal property, but for the moment I\'ll just believe it.  Then this construction mimics the construction of sets as presets with equivalence relations.  If you adopt the axiom of choice, then that construction stabilises; but otherwise, it seems that you can continue it over and over again!  (Perhaps we can get a family of weaker and weaker versions of AC by postulating that the construction stabilises at some point.)

[[Mike Shulman]]: Yes, your question started me thinking in that direction too.  This category $Set_{ex/lex}$ of setoids is interesting in some other ways.  It's not only exact, I'm pretty sure that it's a [[Π-pretopos]] (assuming that $Set$ is).  However, there's no reason for it to be a topos even if $Set$ is; in fact it may not even be well-powered (relative to $Set$)!  In general the subobject lattice $Sub_{Set_{ex/lex}}(X)$ of a set (considered as a setoid) is the preorder reflection of $Set/X$.  If $Set$ satisfies AC, then of course any $Y\to X$ is isomorphic in this poset reflection to its [[image]], but in the complete absence of AC I don't see any reason for this preordered class to be small.  So "$Set_{ex/lex}$ is a topos" would also be an interesting weaker form of AC.

Additionally, in $Set_{ex/lex}$ the terminal object $1$ is a [[generator]] which is nondegenerate, projective, and indecomposable, but *not* (in general) a *strong* generator.  Thus, it is not [[well-pointed topos|well-pointed]] in the correct sense for a pretopos.  In fact, I believe saying that $1$ is a strong generator in $Set_{ex/lex}$ is equivalent to AC in $Set$.

Maybe we should move this discussion to a page like [[exact completion of Set]].

[[Mike Shulman]]: Hmm, I think I made a mistake.  The category I described above is $Set_{reg/lex}$, but it is not exact and thus not also $Set_{ex/lex}$.  However, $Set_{ex/lex}$ also has an interesting description: it is the category of [[bicategories]] in which any two parallel 2-cells are equal and invertible, any two parallel 1-cells are (uniquely) isomorphic, and any 1-cell is an equivalence.  The morphisms are pseudonatural equivalence classes of 2-functors.  That is, $Set_{reg/lex}$ is the category of 1-groupoids that are weakly equivalent to discrete ones, and $Set_{ex/lex}$ is the category of 2-groupoids that are weakly equivalent to discrete ones (both with non-ana functors, otherwise you'd just get $Set$ back again).  The obvious question is then: what about $n$-categories that are weakly equivalent to discrete ones?  Possibly that would have something to do with iterating the completions, although the latter looks more directly related to n-fold categories.
=--

Regular categories of the form $C_{reg/lex}$ for a lex category $C$ can be characterized as those regular categories in which every object admits both a regular epi from a projective object and a monomorphism into a projective object, and the projective objects are closed under finite limits.  In this case $C$ can be recovered as the subcategory of projective objects.  In fact, the construction of $C_{reg/lex}$ can be extended to categories having only [[weak finite limits]], and the regular categories of the form $C_{reg/lex}$ for a "weakly lex" category $C$ are those satisfying the first two conditions but not the third.

When the reg/lex completion is followed by the [[ex/reg completion]] which completes a regular category into an [[exact category|exact one]], the result is unsurprisingly the [[ex/lex completion]].


## Related Articles

Regular categories were introduced by Barr in
_Exact categories_, by M. Barr, Lecture Notes in Mathematics, Springer-Verlag 1971
and by Grillet in the same volume of Lecture Notes in Mathematics.

Some of the history is provided in 
_Topos Theory_, by P. Johnstone, 1977.

An application of the regularity condition is found in the paper
_Tensor envelopes of regular categories_, by F. Knop.   [arXiv:math/0610552v2](http://arxiv.org/abs/math/0610552)

Knop's condition for regularity is slightly different from that presented here; he works with categories that when augmented by an absolutely initial object are regular in the terminology here.  In the paper, Knop generalizes a construction of Deligne by showing how to construct a symmetric pseudo-abelian [[tensor category]] out of a regular category through the calculus of relations.

[[!redirects regular categories]]
