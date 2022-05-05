
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A [[functor]] $F\colon C \to D$ from a [[category]] $C$ to a category $D$ is called _full_ if for each pair of [[objects]] $x, y \in C$, the [[function]]
$$F\colon C(x,y) \to D(F(x), F(y))$$
between [[hom sets]] is [[surjective]].  

More abstractly, we may say a functor is full if it is [[k-surjective functor|1-surjective]] -- or, in simple terms, 'surjective on morphisms between given objects'.  (Note that a functor may be full without being surjective on morphisms, overall, since $F$ is allowed to not hit morphisms between objects that are not in the image of $F$.)

Fullness is most important for functors which are also [[faithful functor|faithful]], and full and faithful functors are often called _[[fully faithful functor|fully faithful]]_.  For ordinary functors this may sound odd, because there is no real sense in which "full" modifies "faithful."  However, in some contexts (such as for morphisms in a general [[2-category]]), there is a good notion of "full-and-faithful" or "fully faithful," but the right notion of "full" alone is not so clear.  "Fully faithful" is also sometimes abbreviated to "ff"; see also [[bo-ff factorization system]].

A [[subcategory]] is called a _[[full subcategory]]_ if its inclusion functor (which is automatically faithful) is also full, and any full and faithful functor exhibits an equivalence of its domain with a full subcategory of its codomain.

## Examples


+-- {: .num_prop}
###### Proposition

Given a pair of [[adjoint functors]]

$$
  \mathcal{C}
    \underoverset
     {\underset{R}{\longrightarrow}}
     {\overset{L}{\longleftarrow}}
     { \phantom{AA} \bot \phantom{AA} }
  \mathcal{D}
$$

* the [[right adjoint]] $R$ is a [[full functor]] precisely if the component of the [[unit of an adjunction|counit]] over every object $x$ is a [[split monomorphism]] $L R x \stackrel{}{\to} x $;

* the [[left adjoint]] $L$ is a [[full functor]] precisely if the component of the [[unit of an adjunction|unit]] over every object $x$ is a [[split epimorphism]] $x \to R L x $.

=--

For [[proof]] see [this Prop](adjoint+functor#FullyFaithfulAndInvertibleAdjoints) at _[[adjoint functor]]_.

## Related concepts

* [[essentially surjective functor]]

* [[faithful functor]]

* [[full and faithful functor]]

* [[equivalence of categories]]


[[!redirects full functor]]
[[!redirects full functors]]

[[!redirects full]]
