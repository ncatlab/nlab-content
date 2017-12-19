# Phase semantics

* table of contents
{: toc}

## Idea

Girard's *phase semantics* is a way of building [[star-autonomous category|star-autonomous]] [[posets]] with [[exponential modalities]], hence models of classical [[linear logic]].

## Definition

Let $M$ be a commutative [[monoid]], and $\bot\subseteq M$ a specified subset.  ($M$ equipped with $\bot$ is sometimes called a *phase space*.)  Then $P M$, the [[powerset]] of $M$, is a commutative [[quantale]], with tensor product

$$ X\otimes Y = \{ m n \mid m\in X \wedge n \in Y \}$$

and internal-hom

$$ X\multimap Y = \{ m \mid \forall n \in X, m n \in Y \}. $$

Indeed, if we regard $M$ as a discrete [[poset]], hence as a category enriched over $\mathbf{2} = \{0\le 1\}$, then $P M$ is its $\mathbf{2}$-enriched [[presheaf category]], and this is its [[Day convolution]] monoidal structure.

Now $\bot$ is an object of $P M$, hence induces a contravariant self-[[adjunction]] $(-\multimap\bot) \dashv (-\multimap \bot)$ of $P M$, which is [[idempotent adjunction|idempotent]] since $P M$ is a poset.  We define a **fact** to be a [[fixed point of an adjunction|fixed point]] of this adjunction, i.e. a subset $X\in P M$ of the form $Y\multimap \bot$, or equivalently such that $X = (X\multimap\bot)\multimap\bot$.

+-- {: .un_theorem}
###### Theorem
The poset of facts is [[star-autonomous category|star-autonomous]].
=--
+-- {: .proof}
###### Proof
It is closed under $\multimap$, since $(X\multimap (Y\multimap\bot)) = (X\otimes Y\multimap \bot)$.  And it is reflective, with reflector $(-\multimap\bot)\multimap\bot$.  Thus, it is closed symmetric monoidal with tensor product $((X\otimes Y)\multimap\bot)\multimap\bot$.  By construction, it is therefore star-autonomous.
=--

The poset of facts is also, of course, a [[complete lattice]], since it a reflective sub-poset of the complete lattice $P M$.  In addition, it admits [[exponential modalities]] $!$ and $?$.  There are different ways to obtain these, but perhaps the simplest (see [here](#GirardSS)) is to take

$$ !X = ((X \cap Idem \cap 1)\multimap\bot)\multimap\bot $$

where $Idem= \{ m \mid m m = m \}$ is the set of idempotents in $M$, and $1 = (\{1\}\multimap\bot)\multimap\bot$ is the unit object of the monoidal category of facts.

## Properties

Phase semantics is complete for provability in linear logic, i.e. if a sequent of linear logic is valid in the phase semantics for all choices of $M$ and $\bot$, then it is provable.  This follows from a construction of a particular $M$ and $\bot$ out of the syntax: let $M$ be the free commutative monoid on the formulas of linear logic subject to the relation that formulas of the form $?A$ are idempotent, and let $\bot$ be the set of $\Gamma\in M$ that are provable when regarded as one-sided sequents $\vdash\Gamma$, and interpret a formula $A$ by the set of $\Gamma\in M$ such that $\vdash \Gamma,A$ is provable.  See [Girard](#Girard) for details.

## Generalizations

When phrased categorically as above, there is an obvious generalization to the case when $M$ is a commutative monoidal *poset*, with $P M$ replaced by its $\mathbf{2}$-enriched presheaf category, i.e. the poset $D M$ of downsets in $M$.  We can also generalize to other enrichments, although in that case the idempotence of the adjunction $(-\multimap\bot) \dashv (-\multimap \bot)$ is no longer automatic but has to be assumed.

If $M$ is assumed only to be a [[promonoidal category|promonoidal]] $\mathbf{2}$-enriched category, i.e. equipped with a suitable [[relation]] $M\times M   &#8696; M$, then it is a [[ternary frame]].  This can be used to construct models of more general [[substructural logics]].

## References

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard}

* [[Jean-Yves Girard]], _Linear logic, its syntax and semantics_ ([pdf](http://www.cs.brandeis.edu/~cs112/2006-cs112/docs/girard-intro.pdf))
 {#GirardSS}

[[!redirects phase space semantics for linear logic]]
[[!redirects linear logic phase space]]
[[!redirects linear logic phase spaces]]
[[!redirects phase space for linear logic]]
[[!redirects phase spaces for linear logic]]
[[!redirects Girard phase space]]
[[!redirects Girard phase spaces]]
