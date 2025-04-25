
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

A [[strict functor]] is _amnestic_ if its [[domain]] has no more duplication of [[isomorphic]] [[objects]] than its [[codomain]].  

As ‘amnestic’ is basically a fancy synonym of ‘forgetful’, the idea is to identify a property that one would like in a [[forgetful functor]].

For example, the notion of amnestic functors formalizes the sense in which the [[concrete category]] $Met_cont$ of [[metric spaces]] and [[continuous maps]] is often better thought of as the category $Met Top$ of [[metrizable topological spaces]] (and [[continuous maps]]), by identifying a property that the [[forgetful functor]]  $Met Top \to Set$ has but $Met_cont \to Set$ does not.  

There is a corresponding notion of _amnesticization_ of a functor (called the _amnestic modification_ in _[[The Joy of Cats]]_), which replaces the domain with an [[equivalent category]], relative to which the functor becomes amnestic.  Applying this to $Met_cont \to Set$ produces a category [[isomorphic category|isomorphic]] to $Met Top$.  Although not needed in this case, we need the [[axiom of choice]] (AC) in general to prove that every functor has an amnesticization.  Without AC, we can use amnestic [[anafunctors]] to make everything work out, although much of the convenience is lost.

Amnesticity is really a property of [[strict functors]] (or anafunctors) between [[strict category|strict]] [[groupoids]].  Groupoids, because the non-isic [[morphisms]] play no role in the definition; only the categories\' [[cores]] matter, and a functor is amnestic iff its core is amnestic.  Strict, because the definition requires us to state (in two places) that some isomorphic objects are equal; weakening the definition to follow the [[principle of equivalence]] leads to a trivial property that every functor satisfies.  (That is, up to [[equivalence of categories|equivalence]], every functor is amnestic, which is because every functor is equivalent to its amnesticization.)


## Definitions

+-- {: .num_defn}
###### Definition

Let $C$ and $D$ be two [[strict categories]], and let $U$ be a [[strict functor]] from $D$ to $C$.  We say that $U$ is __amnestic__ if its [[groupoid core]] reflects [[identity morphisms]].  

Explicitly, $U$ is amnestic iff, for every [[isomorphism]] $f \colon a \to b$ in $D$ that $U$ takes to an [[identity morphism]] $U(f) = id_{U(a)} = id_{U(b)}$, then already $f$ itself is an [[identity morphism]].

In other words, a functor is amnestic if its strict [[fibers]] are [[gaunt category|gaunt]].

=--

Observe that this is similar to a [[conservative functor]], which reflects isomorphisms rather than identities.

If we follow the [[principle of equivalence]] and refuse to state [[equalities]] between objects, then we must modify the hypothesis to say that $U(a)$ and $U(b)$ are *[[isomorphic]]* in $C$ (say via $g\colon U(a) \to U b$) and $U(f)$ is the identity *relative to* this isomorphism (so $U(f) = \id_{U(b)} \circ g \circ \id_{U(a)}$; since we can simply let $g$ be $U(f)$, this is trivial (beyond the initial isomorphism $f\colon a \to b$).  Similarly, we must modify the conclusion to say that $a$ and $b$ are *isomorphic* (say via $h\colon a \to b$) and $f$ is the identity *relative to* this isomorphism (so $f = \id_b \circ h \circ \id_a$); since we can simply let $h$ be $f$, this is also trivial.  Thus up to [[equivalence of categories|equivalence]], this property is trivial; on the other hand, it is preserved by [[isomorphism of categories|isomorphism]].

+-- {: .num_defn #anafunctor}
###### Definition

Now let $C$ and $D$ be two [[strict categories]], and let $U$ be an [[anafunctor]] from $D$ to $C$.  We again say that $U$ is __amnestic__ if its [[core]] reflects [[identity morphisms]].  Explicitly, now $U$ is amnestic iff, whenever $a$ and $b$ are [[objects]] of $D$, $f$ is an [[isomorphism]] in $D$ from $a$ to $b$, $\alpha$ is a specification of $a$ for the anafunctor $U$, $\beta$ is a specification of $b$ for the anafunctor $U$, $U_\alpha(a)$ and $U_\beta(b)$ are equal objects in $C$, and $U_{\alpha,\beta}(f)$ is the [[identity morphism]] on this object in $C$, then $a$ and $b$ are equal objects in $D$, and $f$ is the identity morphism on this object in $D$.
=--

We might also demand that $\alpha = \beta$; this is automatic if $U$ is saturated.


## Properties

* An amnestic [[full and faithful functor]] is automatically an [[isocofibration]], i.e. injective on objects: if $U D' = U D$, then there is some _isomorphism_ $f : D' \to D$ in $\mathcal{D}$ such that $U f = id_{U D}$, but then we must have $f = id_{U D'} = id_{U D}$, so $D' = D$.

* An amnestic [[isofibration]] has the following lifting property: for any object $D$ in $\mathcal{D}$ and any isomorphism $f : C \to U D$ in $\mathcal{C}$, there is a _unique_ isomorphism $\tilde{f} : \tilde{C} \to D$ such that $U \tilde{f} = f$. Indeed, if $\tilde{f}' : \tilde{C}' \to D$ were any other isomorphism such that $U \tilde{f}' = f$, then $U (\tilde{f}^{-1} \circ \tilde{f}') = id_C$, so we must have $\tilde{f} = \tilde{f}'$. Amnestic isofibrations are occasionally called **discrete isofibrations**, but this term may be misleading, because they are not [[isofibrations]] with discrete fibres.

* If the [[composite]] $U \circ K$ is an amnestic functor, then $K$ is also amnestic.


## Examples

* Most famous [[forgetful functors]] are amnestic, such as $Grp \to Set$, $Top \to Set$, $Top Grp \to Grp$, and $Top Grp \to Top$.  Even $Met \to Set$ is amnestic, since the morphisms in [[Met]] are [[short maps]].  However, $Met_cont \to Set$, where the morphisms are [[continuous maps]], is *not* amnestic, as is shown by any set with two different but topologically equivalent metrics (such as $\mathbb{R}^2$ with the $l^1$ and $l^\infty$ metrics).

* The forgetful functor from a groupoid of [[structured sets]] is amnestic.  The examples above may all be defined by starting from such a groupoid and specifying which functions preserve the structure (and so are morphisms in the category of structured sets).  So long as this produces no additional isomorphisms, the forgetful functor will be amnestic.  But in the case of $Met_cont$, any non-isometric homeomorphism will be an isomorphism that was not in the original groupoid (consisting only of surjective isometries), and so this forgetful functor is not amnestic.

* Any strictly [[monadic functor]] is amnestic. Conversely, any monadic functor that is also an amnestic isofibration is necessarily strictly monadic.


## Related concepts

* [[conservative functor]]
* [[concrete category]]
* [[structure]]
* [[stuff, structure, property]]


## References

* J. Ad&#225;mek, H. Herrlich and G.E. Strecker: [[The Joy of Cats]], Chapter I, Definition 3.27.

* G. Preu&#223;: Theory of Topological Structures: An Approach to Categorical Topology. D. Reidel Publishing Company. Mathematics and Its Applications, Dordrecht, Holland 1988.  p. 178, footnote 31


[[!redirects amnestic functor]]
[[!redirects amnestic functors]]
[[!redirects amnestic anafunctor]]
[[!redirects amnestic anafunctors]]

[[!redirects amnesticization]]
[[!redirects amnesticizations]]
[[!redirects amnesticisation]]
[[!redirects amnesticisations]]
[[!redirects amnestic modification]]
[[!redirects amnestic modifications]]

[[!redirects amnestic isofibration]]
[[!redirects amnestic isofibrations]]
[[!redirects discrete isofibration]]
[[!redirects discrete isofibrations]]
