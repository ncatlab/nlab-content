+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Continuous algebras

* automatic table of contents goes here
{:toc}

## Definition

Let $T$ be a [[lax-idempotent 2-monad]] or pseudo 2-monad, and $A$ a pseudo $T$-algebra witnessed by a [[left adjoint]] $a : T A \to A$ to the unit $\eta_A : A \to T A$.  We say that $A$ is a **continuous $T$-algebra** if $a : T A \to A$ has a further left adjoint, forming an [[adjoint triple]].

Note that every free $T$-algebra $T B$ is continuous: it is a property of lax-idempotent 2-monads that the multiplication $\mu_B:T T B \to T B$ has left adjoint $T\eta_B$.

For the rest of this page we will say "$T$-algebra" to mean "pseudo $T$-algebra".

## Examples

* If $T A = Ind(A)$ is the [[ind-completion]] monad on [[Cat]], whose algebras are categories with [[filtered colimits]], then a continuous $T$-algebra is precisely a [[continuous category]].  This is the origin of the name.

* Specializing the previous example, if $T A = Idl(A)$ is the [[ideal]] completion monad on [[Poset]], whose algebras are posets with [[directed joins]], then a continuous $T$-algebra is a [[continuous poset]].

Note also that if an [[adjoint functor theorem]] applies (such as if $A$ and $T A$ are [[complete lattices]], or [[locally presentable categories]]), then $A$ is continuous if and only if $T A \to A$ is a [[continuous functor]].  This provides another justification for the name.

* For instance, if $T$ is the downset monad on [[Poset]], whose algebras are [[suplattices]], then continuous algebras are called [[constructive completely distributive lattices]].  Assuming the [[axiom of choice]], these are equivalent to [[completely distributive lattices]].  See ([WoodFawcett](#WoodFawcett)).

* If $T$ is the free small-cocompletion monad on $Cat$, whose algebras are [[cocomplete categories]], then continuous algebras are in particular [[completely distributive categories]].  The converse only holds if an adjoint functor theorem applies.

* If $T$ is the [[presheaf category]] "monad", whose "algebras" are [[total categories]], then the "continuous algebras" are [[totally distributive categories]].  The scare quotes are because this example is not really a monad for size reasons.

* If $T$ is the [[free cocompletion]] monad under coproducts, then continuous algebras are "locally connected" in a sense: the extra left adjoint $A \to T A$ decomposes every object as a coproduct of connected ones.

## Characterizations

+--{: .num_theorem #Retract}
###### Theorem
Consider the following conditions on a $T$-algebra $A$:

1. $A$ is a continuous algebra.
1. $A$ is a [[coreflective subcategory|coreflective]] sub-$T$-algebra of a free $T$-algebra.
1. $A$ is a retract (up to isomorphism) of a free $T$-algebra.

Then (1) $\Rightarrow$ (2) $\Rightarrow$ (3), and both converses hold if idempotent 2-cells split in the underlying 2-category.
=--
+--{: .proof}
###### Proof
This is B1.1.15 in the [[Elephant]].  If the algebra structure $a : T A \to A$ has a left adjoint $\ell$, then $\ell \dashv a$ is an adjunction in the 2-category of $T$-algebras (since any left adjoint between $T$-algebras is a $T$-morphism).  And since the counit of $a\dashv \eta_A$ is an isomorphism, the unit of $\ell \dashv a$ is an isomorphism, by the theorem on [fully faithful adjoint triples](adjoint+triple#FullyFaithFulAdjointTriples).  This shows (1) $\Rightarrow$ (2), and (2) $\Rightarrow$ (3) is obvious.  For the converse, see the [[Elephant]].
=--

+--{: .num_theorem #Comonadicity}
###### Theorem
(?) Let $G$ be the pseudo [[2-comonad]] on the 2-category $T Alg$ of $T$-algebras induced by the free-forgetful adjunction.  Then $G$ is lax-idempotent, and a $T$-algebra $A$ is continuous if and only if it is a $G$-coalgebra.
=--

This is proven in ([Kock](#Kock)) in the special case when the base 2-category is a [[(1,2)-category]] (the result is due to [[Bart Jacobs]]).  It seems  probably true in general, but perhaps no one has checked the details.


## Related pages

* [[lax-idempotent 2-monad]]
* [[adjoint triple]]

## References

* [[Richard Wood]] and Barry Fawcett, "Constructive complete distributivity. I". Math. Proc. Camb. Phil. Soc. (1990), 107, 81
 {#WoodFawcett}

* [[Anders Kock]], "Monads for which structures are adjoint to units", JPAA 104 (1992).
 {#Kock}

[[!redirects continuous algebras]]
