# Lax $\mathcal{F}$-adjunctions

* table of contents
{: toc}

## Idea

The notion of [[adjunction]] or [[2-adjunction]] can be "laxified" in many ways; as discussed at [[lax 2-adjunction]], one can make the triangle identities hold only up to a noninvertible cell, make the unit and counit only lax natural, and even consider making the functors only lax.  Of these, lax naturality of the unit and counit is problematic because lax natural transformations do not satisfy a Yoneda lemma.  However, this becomes less of a problem if the lax transformations restrict to pseudo ones on certain well-behaved subcategories.  An abstract context to define this is that of [[F-categories]].

## Definition

Let $K,L$ be [[F-categories]] (strict for simplicity).  A **lax $\mathcal{F}$-adjunction** between them consists of:

* $\mathcal{F}$-functors $F:K\to L$ and $G:L\to K$ (strict for simplicity).
* [[pseudo/lax F-natural transformations]] $\eta : Id_K \to G F$ and $\epsilon : F G \to Id_L$.
* The triangle identities for $\eta,\epsilon$ hold up to isomorphism (which can be made coherent).

If $\epsilon$ is fully pseudo, we call it a **right semi-lax $\mathcal{F}$-adjunction**.  Dually, we have left semi-lax, right semi-oplax, left semi-oplax, and so on.  (We could also consider allowing the triangle identities or functors to be lax, but we will not.)

## Properties

The following theorem seems to fail for 2-adjunctions involving lax transformations; the fact that it holds for lax $\mathcal{F}$-adjunctions thus means that they are significantly better-behaved and more interesting.  It was first observed (without the terminology of $\mathcal{F}$-categories) by [Johnstone](#JohnstonePP).

+-- {: .un_theorem}
###### Theorem
If $F:K\to L$ is an $\mathcal{F}$-functor and $G,G'$ are two lax right $\mathcal{F}$-adjoints for it, then $G\simeq G'$.
=--
+-- {: .proof}
###### Proof
As usual, we consider the composites
$$ G \xrightarrow{\eta' G} G' F G \xrightarrow{G' \epsilon} G' \qquad G' \xrightarrow{\eta G'} G F G' \xrightarrow{G \epsilon'} G. $$
The usual proof of uniqueness of adjoints applies to show that these are pseudo-inverses, but we do need the fact that these unit and counit are pseudo/lax rather than merely lax.  For the proof requires using naturality squares to commute units and counits past each other, and since their components are tight and they are all pseudo-natural on tight morphisms these naturality squares commute up to isomorphism; if they only commuted laxly then the proof would fail.

Note that *a priori* these composites are themselves also only pseudo/lax $\mathcal{F}$-natural.  However, any lax natural transformation that is (pseudo) invertible is actually pseudo natural, so in fact these composites are a pseudo/pseudo $\mathcal{F}-$natural equivalence $G\simeq G'$.
=--

## Examples

### Fibrations in a 2-category

In [Johnstone](#JohnstonePP) it is shown that a [[fibration in a 2-category]] $K$ can equivalently be defined as a morphism $p:E\to B$ with the following property.  Let $K\swarrow B$ denote the [[oplax slice 2-category]], whose objects are morphisms $f:A\to B$ and whose morphisms are pairs $(g:A\to A', \alpha : f' g \Rightarrow f)$.  We make $K\swarrow B$ into an $\mathcal{F}$-category by declaring $(g,\alpha)$ to be tight if $\alpha$ is an isomorphism.

Now, composing with $p:E\to B$ induces an $\mathcal{F}$-functor $\Sigma_p : K\swarrow E \to K\swarrow B$.

+-- {: .un_theorem}
###### Theorem
$p$ is a [[fibration in a 2-category|fibration]] (in the [[Street fibration|pseudo sense]]) if and only if $\Sigma_p$ has a right semi-lax $\mathcal{F}$-adjoint.
=--

## References

* [[Peter Johnstone]], *Fibrations and partial products in a 2-category*
 {#JohnstonePP}

[[!redirects lax F-adjunction]]
[[!redirects oplax F-adjunction]]
[[!redirects colax F-adjunction]]
[[!redirects lax F-adjunctions]]
[[!redirects oplax F-adjunctions]]
[[!redirects colax F-adjunctions]]

[[!redirects semi-lax F-adjunction]]
[[!redirects semi-oplax F-adjunction]]
[[!redirects semi-colax F-adjunction]]
[[!redirects semi-lax F-adjunctions]]
[[!redirects semi-oplax F-adjunctions]]
[[!redirects semi-colax F-adjunctions]]

[[!redirects right semi-lax F-adjunction]]
[[!redirects right semi-oplax F-adjunction]]
[[!redirects right semi-colax F-adjunction]]
[[!redirects right semi-lax F-adjunctions]]
[[!redirects right semi-oplax F-adjunctions]]
[[!redirects right semi-colax F-adjunctions]]

[[!redirects left semi-lax F-adjunction]]
[[!redirects left semi-oplax F-adjunction]]
[[!redirects left semi-colax F-adjunction]]
[[!redirects left semi-lax F-adjunctions]]
[[!redirects left semi-oplax F-adjunctions]]
[[!redirects left semi-colax F-adjunctions]]
