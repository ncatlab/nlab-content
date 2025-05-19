
\tableofcontents

## Idea 

The *free-living structure* or *free-standing structure* is an archetypal model of the [[mathematical structure]], and usually refers to a *[[free construction|free]]* or *[[initial object|initial]]* form of such a kind of structure. 

## Terminology

Around the nLab and elsewhere, one occasionally sees an expression "the walking _____" where the blank is some mathematical concept. This is a colloquial way of referring to the free-living concept or type. 

Pronunciation is just as in 'John is a walking almanac' or 'Eugene Levy is a walking pair of eyebrows'. The term is [believed](http://golem.ph.utexas.edu/category/2010/01/f_and_the_shibboleth.html#c031066) to have been introduced by [[James Dolan]]. 

## Definition

The idea is probably easier to apprehend through examples rather than through a formal definition, but for the record: 

If $X$ is a type of [[mathematical structure]] that can be defined in a [[category]], [[higher category]], or category with some [[extra structure]], then the *free-living X* refers to the *[[free construction|free]] category (resp. higher category, category with suitable structure) containing an $X$.

More precisely, if $StructCat$ denotes some (higher) category of categories with an appropriate type of structure, then the **free-living X** is an object $[X] \in StructCat$ together with a [[natural transformation|natural]] [[equivalence]]
$$ 
  StructCat([X],C) 
  \;\simeq\; 
  \big\{Xs \; in \; C\}
$$
between the [[hom-set]]/[[hom-category|category]]/[[hom-space|space]] from $[X]$ to $C$, for any $C\in StructCat$, and the set/category/space of all Xs in $C$. 

+-- {: .num_remark} 
###### Remark 
In other words, the structured category $[X]$ equipped with its canonical type $X$ is [[initial object|initial]] among such structured categories that come equipped with such types $X$. A fancier expression is that $[X]$ 'coclassifies' such types: this is analogous to how a [[classifying space]] $B G$ for a [[topological group]] $G$ classifies $G$-[[bundles]], in that every $G$-bundle $p: E \to X$ over a suitable space $X$ has a classifying map $\chi_p: X \to B G$ (unique up to homotopy) such that pulling back the canonical $G$-bundle type $\pi: E G \to B G$ along $\chi_p$ reproduces the type $p$. Only here we say 'coclassifies' (as for example in this [comment](http://nforum.mathforge.org/discussion/1529/walking-structures/#Item_5)), since here we instead "push forward" the canonical type $X$ of $[X]$ along a structured-category morphism $[X] \to C$ to obtain a given type of $C$. 
=-- 



## Examples

* The [[interval category]] is the *free-living morphism*.

* The [[interval groupoid]] is the *free-living isomorphism*. 

* [[equivalence|Equivalences]] in a [[2-category]] are represented by the [[walking equivalence]].

* The [[2-category]] [[Adj]] is the [[walking adjunction]].

* The [[walking 2-isomorphism with trivial boundary]] is a 2-groupoid model for the 2-truncation of the [[2-sphere]].

* The augmented/algebraist's [[simplex category]] is "the *free-living [[monoid]]*" (in a [[monoidal category]]). That is to say: the simplex category is initial (in a 2-categorical sense) among monoidal categories equipped with a monoid object. Intuitively, it is [[the]] monoidal category that results if all one need be told about it is that it has a monoid object -- all the morphisms of the category are obtainable from the monoid structure by applying the operations of a monoidal category, and they are subject to no further relations beyond those implied by the monoid axioms. 

* Similarly, the [[Lawvere theory]] of groups can be described as "the *free-living [[group object|group]]*" (qua [[cartesian monoidal categories]]). This gives a good intuitive description: this Lawvere theory can be understood as the category (with finite products) that results if all one need be told about it is that it has a [[group object]]; the rest of the structure of this category can be deduced from this one fact. 

The last two examples indicate the need for a little care: the [[doctrine]] or type of structured category in which the '$X$' of "the free-living $X$" lives should either be specified or clear from context. For example, if one simply says "the free-living monoid", this means the simplex category if the surrounding context is the doctrine of monoidal categories -- but means something else (the Lawvere theory of monoids) if the ambient context is the doctrine of categories with finite products, and it means the category opposite to that of finitely presentable monoids if we are in the doctrine of [[finitely complete categories]]. 

If the doctrine is not specified, then a reasonable default is a 'minimal' doctrine in which the concept makes sense; for example, to make sense of monoids, one doesn't need more than monoidal categories. See also [[microcosm principle]]. 

Thus, more generally, 

* The [[syntactic category]] of a [[theory]] $T$ in some [[doctrine]] $D$ is the "free-living $T$-model" (in a $D$-category).  In particular, the [[classifying topos]] of a [[geometric theory]] $T$ is "the *free-living $T$-model*" *qua* [[Grothendieck toposes]] (where the morphisms are the left-adjoint parts of [[geometric morphisms]]).

## Relation to initial objects

The free-living X is, of course, not the same as the [[initial object|initial]] X.

Consider for example the case when X is a pointed monoid (a monoid equipped with an element).  The initial pointed monoid (in $Set$) is the [[natural numbers]] equipped with $1\in \mathbb{N}$.  Whereas the free-living pointed monoid (qua category with finite products, say) is a category $C_M$ with finite products containing a [[monoid object]] $M\in C_M$ and an "[[generalized element|element]]" $e:1\to M$.  They have different types and different universal properties: $\mathbb{N}$ has a universal property mapping into other pointed monoids in $Set$, while $C_M$ has a universal property mapping into other categories with products equipped with pointed monoids.

Nevertheless, the first sits inside the second!  Specifically, for any category $C$ with products, the "underlying set" functor $C(1,-):C\to Set$ is product-preserving and hence carries monoid objects to monoid objects, and in the case of the free-living pointed monoid we have $C_M(1,M) \cong \mathbb{N}$.

This is true rather generally: *the initial X is the underlying X of the free-living X*.  One general theorem of this sort is the following:

+--{: .un_theorem}
###### Theorem
Let $K$ be a [[2-category]] containing an object $S$, and suppose that:

1. The domain projection $K\sslash S \to K$ from the [[lax slice 2-category]] has a section.  Explicitly, for every object $X$ we have a map $s_X : X\to S$ and for every morphism $f:X\to Y$ we have a 2-cell $\sigma_f : s_X \to s_Y f$, such that for every 2-cell $\alpha :f\to g$ we have $\sigma_g . s_Y\alpha = \sigma_f$, and these vary functorially.
2. We have $s_S \cong 1_S$, and for any $X$ the composite $s_X \xrightarrow{\sigma_{s_X}} s_S s_X \cong s_X$ is the identity.

Then for any $X$, the morphism $s_X:X\to S$ is the initial object of the hom-category $K(X,S)$.
=--
+--{: .proof}
###### Proof
We will use the characterization of initial objects via [cones over the identity](/nlab/show/initial+object#ConesOverTheIdentity).  Thus, we must construct a natural transformation from the constant functor $\Delta_{s_X} : K(X,S) \to K(X,S)$ to the identity, which is the identity at $s_X$.  However, given any $f:X\to S$, we have the 2-cell $s_X \xrightarrow{\sigma_f} s_S f \cong f$, and the assumption $\sigma_g . s_Y\alpha = \sigma_f$ makes this a natural transformation; and the final assumption says exactly that this is the identity at $s_X$.
=--

To see how this theorem implies that the initial X is the underlying X of the free-living X, consider again the case of pointed monoids.  Let $K$ be the 2-category of categories with products and product-preserving functors, let $S=Set$, and let $s_C : C \to Set$ be $C(1,-)$.  The hypotheses are easy to verify; thus the theorem tells us that $C(1,-)$ is the initial functor $C\to Set$ for any $C$.

Now take $C$ to be the free-living pointed monoid $C_M$ above.  Then its universal property tells us that functors $F:C_M\to Set$ are equivalent to pointed monoids $F(M)$ in $Set$; so we see that $C(1,M)$ is the initial pointed monoid in $Set$, i.e. $\mathbb{N}$.

A similar argument applies whenever we have a "$Set$-like" object of a 2-category with "underlying set" morphisms to it.  For instance, in place of categories with finite products we could consider categories with finite limits.  However, in other cases, such as monoidal categories, there is a disconnect: the natural "underlying set" functor for a monoidal category $C$ is $C(I,-)$, where $I$ is the unit object; but in general this is only *lax* monoidal, whereas the universal property of a "free-living X qua monoidal category" is relative to *strong* monoidal functors.

It does often happen that this disconnect can be bridged.  For instance, suppose X is something that can be defined in any [[multicategory]] (like a pointed monoid).  Then we can apply the above argument to the 2-category of multicategories, as the free-living X qua multicategory has a universal property relative to functors of multicategories, even though such functors correspond to *lax* functors between monoidal categories.  It follows that the underlying set functor $C_M(;-) : C_M\to Set$ of the free-living X qua multicategory corresponds to the initial X in $Set$.

Moreover, we can deduce from this that the underlying pointed monoid of the free-living X qua monoidal category is also the initial X in $Set$.  This is because the free-living X qua monoidal category is the monoidal category freely generated by the free-living X qua multicategory, and a multicategory embeds fully-faithfully in the monoidal category that it freely generates.  In terms of the [[type theory]] that generates free-living Xs, the latter fact can be seen as a sort of [[canonicity]] for the tensor-product constructor.

Similar arguments apply in other cases.  For instance, in the 2-category of [[double categories]] we can take $S$ to be the double category [[Span]]; this has the same problem as that of monoidal categories, but we can solve it similarly by considering [[virtual double categories]] instead.

On the other hand, there are also cases where this argument does not apply.  For instance, X could be something that can be defined in a monoidal category but *not* in a multicategory, such as a [[Frobenius monoid]].  In this case the claim doesn't even make sense: the functor $C(I,-)$, being only lax monoidal in general, need not preserve Frobenius monoids.  It seems that in most cases where an "underlying set" functor $C(I,-)$ preserves Xs, there is a kind of [[generalized multicategory]] in which Xs can be defined and this argument carried through, but I do not know of a general theory suggesting this.


## References

* {#FoltzLairKelly80} [[François Foltz]], [[Christian Lair]], [[G. M. Kelly]], *Algebraic categories with few monoidal biclosed structures or none*, Journal of Pure and Applied Algebra **17** 2 (1980) 171-177 &lbrack;[pdf](https://core.ac.uk/download/pdf/82322397.pdf), <a href="https://doi.org/10.1016/0022-4049(80)90082-1">doi:10.1016/0022-4049(80)90082-1</a>&rbrack;

The terminology "walking" appears in:

* A [Café post](http://golem.ph.utexas.edu/category/2010/01/f_and_the_shibboleth.html) essentially about walking objects (among other things), including a [comment](http://golem.ph.utexas.edu/category/2010/01/f_and_the_shibboleth.html#c031066) that explains the terminology.

[[!redirects free-living]]
[[!redirects free-living structure]]
[[!redirects free-living structures]]
[[!redirects free-living object]]
[[!redirects free-living objects]]

[[!redirects walking]]
[[!redirects walking structure]]
[[!redirects walking structures]]
[[!redirects walking object]]
[[!redirects walking objects]]
