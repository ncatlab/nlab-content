+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **lax-idempotent 2-monad**, also called a **Kock--Z&#246;berlein** or **KZ** monad, encodes a certain kind of [[stuff, structure, property|property-like structure]] that a [[category]], or more generally an [[object]] of a [[2-category]], can carry.

The archetypal examples are given by [[2-monads]] $T$ on [[Cat]] that take a [[category]] $C$ to the [[free cocompletion]] $T C$ of $C$ under a given class of [[colimits]] -- then an [[algebra of a monad|algebra]] $T C \to C$ is a category $C$ with all such colimits, which are of course essentially unique.  Moreover, given thus-cocomplete categories $C$ and $D$, a functor $F \colon C \to D$, and a diagram $S$ in $C$, there is a unique arrow $colim T F S \to F(colim S)$ given by the universal property of the colimit.  It is this property that lax-idempotence generalizes.


## Definition

A [[2-monad]] $T$ on a [[2-category]] $K$ is called **lax-idempotent** if given any two (strict) $T$-algebras $a \colon T A \to A$, $b \colon T B \to B$ and a morphism $f \colon A \to B$, there exists a unique 2-cell $\bar f \colon b \circ T f \Rightarrow f \circ a$ making $(f,\bar f)$ a lax morphism of $T$-algebras:
\[
\array{
T A & \overset{T f}{\to} & T B \\
a \downarrow & \swArrow \bar f & \downarrow b \\
A & \underset{f}{\to} & B
}
\]

Dually, a 2-monad $T$ is called **colax-idempotent** if $f \colon A \to B$ gives rise to a colax $T$-morphism $(f,\tilde f)$:
\[
\array{
T A & \overset{T f}{\to} & T B \\
a \downarrow & \neArrow \tilde f & \downarrow b \\
A & \underset{f}{\to} & B
}
\]


### Equivalent conditions

+-- {: .num_theorem #AlgebraAdjoint}
###### Theorem
A 2-monad $T$ as above, with unit $\eta: 1 \to T$, is lax-idempotent if and only if for any $T$-algebra $a \colon T A \to A$ there is a 2-cell $\theta_a \colon 1 \Rightarrow \eta_A \circ a$ such that $(\theta_a ,1_{1_A})$ are the unit and counit of an [[adjunction]] $a \dashv \eta_A$.
=--

+-- { .proof}
###### Proof
**(Adapted from Kelly--Lack)**.  The multiplication $\mu_A \colon T^2 A \to T A$ is a $T$-algebra on $T A$, and $\eta_A \colon A \to T A$ is a morphism from the underlying object of $a$ to that of $\mu_A$.  So there is a unique $\bar\eta_A \colon \mu_A \circ T \eta_A = 1_{T A} \Rightarrow \eta_A \circ a$ making $\eta_A$ into a lax $T$-morphism.  Set $\theta_a = \bar\eta_A$.  The [[adjunction|triangle equalities]] then require that:

  1.  $a \bar\eta_A \colon a \Rightarrow a \circ \eta_A \circ a = a$       is equal to $1_a$.  The composite $a \circ \bar\eta_A$ makes $a \circ \eta_A$ a lax $T$-morphism from $a$ to $a$ (paste $\bar\eta_A$ with the identity square $a \circ \mu_A = a \circ T a$).  But $a \circ \eta_A = 1_A$, and $1_a$ also makes this into a lax $T$-morphism, so by uniqueness $a \bar\eta_A = 1_a$.

  2. $\bar\eta_A \eta_A \colon \eta_A \Rightarrow \eta_A \circ a \circ \eta_A = \eta_A$ is equal to $1_{\eta_A}$.  But this follows directly from the unit coherence condition for the lax $T$-morphism $\bar\eta_A$.

Conversely, suppose $\theta_a$, algebras $a,b$ on $A,B$ and $f \colon A \to B$ are given.  Take $\bar f$ to be the [[mate]] of $1_f \colon b \circ T f \circ \eta A = f \Rightarrow f$ with respect to the adjunctions $a \dashv \eta_A$ and $1 \dashv 1$, which is given in this case by pasting with $\theta_a$, so we have that $\bar f = b \circ T f \circ \theta_a$.  The mate of $\bar f$ in turn is given by $\bar f \circ \eta_A$, which because mates correspond bijectively is equal to $1_f$.  So $\bar f$ satisfies the unit condition.

Consider the diagrams expressing the multiplication condition: because $a \circ \mu_A = a \circ T a$ (and the same for $b$), their boundaries are equal, so we have 2-cells $\alpha, \beta \colon b \circ T b \circ T^2 f \Rightarrow f \circ a \circ T a$.  Their mates under the adjunction $(T\theta_a, 1) \colon T a \dashv T\eta_A$ are given by pasting with $T \eta_A$.  One is $\bar f$ pasted with $T \bar f \circ T \eta_A = T(f \circ \eta_A) = T 1_f = 1_{T f}$, and the other is given by composing $T \eta_A$ with the identity $\mu_B \circ T^2 f = T f \circ \mu_A$ (and then pasting with $\bar f$), but because $\mu_A \circ T \eta_A = 1_{T A}$ this is also equal to $1_{T f}$.  The two original 2-cells are hence equal, because their mates are equal, and so $\bar f$ is indeed a lax $T$-morphism.
=--

Since $T$'s multiplication $\mu$ makes $T$ itself into a (generalized) $T$-algebra, the above implies (and in fact is implied by) the requirement that there exist a [[modification]] $\ell \colon 1_{T^2} \to \eta T \circ \mu$ making $(\ell,1) \colon \mu \dashv \eta T$.  Conversely, given an algebra $a \colon T A \to A$, the 2-cell $\theta_a$ is given by $T a \circ \ell_A \circ T \eta_A$.

A different but equivalent condition is that there be a modification $d \colon T \eta \to \eta T$ such that $d \eta = 1$ and $\mu d = 1$; and given $\ell$ as above, $d$ is given by $\ell \circ T \eta$.

These various conditions can also be regarded as ways to say that the [[Eilenberg-Moore category|Eilenberg-Moore adjunction]] for $T$ is a [[lax-idempotent 2-adjunction]].  Thus, $T$ is a lax-idempotent 2-monad exactly when this 2-adjunction is lax-idempotent, and therefore also just when it is the 2-monad induced by *some* lax-idempotent 2-adjunction.

Dually, for $T$ to be colax-idempotent, it is necessary and sufficient that any of the following hold.

* For any $T$-algebra $a \colon T A \to A$ there is a 2-cell $\zeta_a \colon \eta_A \circ a \Rightarrow 1$ such that $(1,\zeta_a) \colon \eta_A \dashv a$.

* There is a modification $m \colon \mu \circ \eta T \to 1$ making $(1,m) \colon \eta T \dashv \mu$.

* There is a modification $e \colon \eta T \to T\eta$ such that $e\eta = 1$ and $\mu e = 1$.

## Algebras

Theorem \ref{AlgebraAdjoint} gives a necessary condition for an object $A$ to admit a $T$-algebra structure, namely that $\eta_A : A \to T A$ admit a left adjoint with identity counit.  In the case of pseudo algebras, this necessary condition is also sufficient.

+--{: .num_theorem #PseudoAlgebras}
###### Theorem
To give a pseudo $T$-algebra structure on an object $A$ is equivalently to give a left adjoint to $\eta_A : A\to T A$ with invertible counit.
=--

In particular, an object admits at most one pseudo $T$-algebra structure, up to unique isomorphism.  Thus, $T$-algebra structure is [[property-like structure]].

In many cases it is interesting to consider the pseudo $T$-algebras for which the algebra structure $T A \to A$ has a further left adjoint, forming an [[adjoint triple]].  Algebras of this sort are sometimes called [[continuous algebras]].

## Examples

As mentioned above, the standard examples of lax-idempotent 2-monads are those on $Cat$ whose algebras are categories with all colimits of a specified class.  In this case, the 2-monad is a [[free cocompletion]] operation.  Dually, there are colax-idempotent 2-monads which adjoin limits of a specified class.  A converse is given by ([PowerCattaniWinskel](#PowerCattaniWinskel)), who show that a 2-monad is a monad for free cocompletions if and only if it is lax-idempotent and the unit $\eta$ is dense (plus a coherence condition).

Another important example of a colax-idempotent monad is the monad on $Cat/B$ that takes $p \colon E \to B$ to the projection $B/p \to p$ out of the [[comma category]].  The algebras for this monad are [[Grothendieck fibrations]] over $B$; see also [[fibration in a 2-category]].  The monad $p \mapsto p/B$ is lax-idempotent, and its algebras are opfibrations.

This latter is actually a special case of a general situation.  If $T$ is a (2-)monad relative to which one can define [[generalized multicategories]], then often it induces a lax-idempotent 2-monad $\tilde{T}$ on the 2-category of such generalized multicategories (aka "virtual $T$-algebras"), such that (pseudo) $\tilde{T}$-algebras are equivalent to (pseudo) $T$-algebras.  When $T$ is the 2-monad whose algebras are strict 2-functors $B\to Cat$ and whose pseudo algebras are pseudofunctors $B\to Cat$, then a virtual $T$-algebra is a category over $B$, and it is a pseudo $\tilde{T}$-algebra just when it is an opfibration.  Similarly, there is a lax-idempotent 2-monad on the 2-category of [[multicategories]] whose pseudo algebras are [[monoidal categories]], and so on.

## Properties

* [[pseudo-distributive laws]] involving lax-idempotent 2-monads have an especially nice form; see [(Marmolejo)](#MarmolejoDL) and [(Walker)](#WalkerDL).

* For ordinary 1-monads there exists a presentation due to Manes as "Kleisli triples" with primary data a family of unit morphisms and lifts avoiding the iteration of the endofunctor. A similar presentation exists for lax-idempotent 2-monads as shown in Marmolejo-Wood ([2012](#MW12)). It is shown then in Walker [(2017)](#WalkerYS) that provided the units of this presentation are fully faithful (a reflection of the fully-faithfulness of the Yoneda embedding) (almost) all the axioms of a [[Yoneda structure]] are satisfied. In cases where size plays no role like e.g. the ideal completion of posets the two concepts coincide. For further details see at [[Yoneda structure]] or Walker [(2017)](#WalkerYS).

## Related concepts

* [[idempotent monad]]
* [[2-monad]]
* [[stuff, structure, property]]
* [[property-like structure]]
* [[continuous algebra]]
* [[free cocompletion]]
* [[lax-idempotent 2-adjunction]]

## References

Classical references are

* [[Max Kelly]], [[Steve Lack]], _On property-like structures_, TAC 3(9), 1997. ([abstract](http://www.tac.mta.ca/tac/volumes/1997/n9/3-09abs.html))

* [[Anders Kock]], _Monads for which structures are adjoint to units_ , Aarhus Preprint 1972/73 No. 35. ([pdf](http://home.imf.au.dk/kock/msau1.PDF))

* [[Anders Kock]], _Monads for which structures are adjoint to units_, JPAA 104:41--59, 1995.

* [[Ross Street]], _Fibrations in Bicategories_ , Cah. Top. Géom. Diff. **XXI** no.2 (1980). ([numdam](http://www.numdam.org/item?id=CTGDC_1980__21_2_111_0))

* Volker Zöberlein, _Doctrines on 2-categories_ , Math. Zeitschrift **148** (1976) pp.267-279. ([gdz](https://gdz.sub.uni-goettingen.de/id/PPN266833020_0148?tify={%22pages%22:[273],%22view%22:%22info%22}))

"Textbook" accounts of the concept can be found in

* [[Peter Johnstone]], _Sketches of an elephant vol.1_ , Oxford UP 2004. (B1.1.11, pp.250-54)

* [[Marta Bunge]], [[Jonathon Funk]], _Singular coverings of Toposes_ , Springer Heidelberg 2006. (pp.79ff)

Special facets of the concept are studied in

* [[Marta Bunge]], _Tightly Bounded Completions_ , TAC **28** no.8 (2013) pp.213-240. ([abstract](http://tac.mta.ca/tac/volumes/28/8/28-8abs.html))

* {#BF99} [[Marta Bunge]], [[Jonathon Funk]], _On a bicomma object condition for KZ-doctrines_ , JPAA **143** (1999) pp.69-105.

* A. J. Power, G. L. Cattani, G. Winskel, _A representation result for free cocompletions_, JPAA 151:273--286, 2000 {#PowerCattaniWinskel} <a href="        http://dx.doi.org/10.1016/S0022-4049(99)00063-8">doi</a>

Their distributive laws come into focus in

* Francisco Marmolejo, *Distributive laws for pseudomonads*, [TAC](http://tac.mta.ca/tac/volumes/1999/n5/5-05abs.html)
 {#MarmolejoDL}

* {#MW12} Francisco Marmolejo, [[Richard J. Wood]], _Kan extensions and lax idempotent pseudomonads_ , TAC **26** no.1 (2012) pp.1-19. ([abstract](http://www.tac.mta.ca/tac/volumes/26/1/26-01abs.html))

* Charles Walker, *Distributive Laws via Admissibility*, [arXiv](https://arxiv.org/abs/1706.09575)
 {#WalkerDL}

The relation to Yoneda structures is due to

* Charles Walker, *Yoneda Structures and KZ Doctrines*, [arxiv](https://arxiv.org/abs/1703.08693)
 {#WalkerYS}

The logical-syntactical side is examined in

*  [[Jiri Adamek]], Lurdes Sousa, *KZ-monadic categories and their logic*, [tac](http://tac.mta.ca/tac/volumes/32/10/32-10abs.html)


[[!redirects KZ monad]]
[[!redirects KZ-monad]]
[[!redirects KZ doctrine]]
[[!redirects KZ-doctrine]]

[[!redirects KZ monads]]
[[!redirects KZ-monads]]
[[!redirects KZ doctrines]]
[[!redirects KZ-doctrines]]

[[!redirects lax-idempotent 2-monad]]
[[!redirects lax-idempotent 2-monads]]
[[!redirects lax-idempotent monad]]
[[!redirects lax-idempotent monads]]

[[!redirects colax-idempotent 2-monad]]
[[!redirects colax-idempotent 2-monads]]
[[!redirects colax-idempotent monad]]
[[!redirects colax-idempotent monads]]

[[!redirects lax-idempotent]]
[[!redirects lax-idempotence]]
[[!redirects colax-idempotent]]
[[!redirects colax-idempotence]]

[[!redirects lax idempotent 2-monad]]
[[!redirects lax idempotent 2-monads]]
[[!redirects lax idempotent monad]]
[[!redirects lax idempotent monads]]

[[!redirects colax idempotent 2-monad]]
[[!redirects colax idempotent 2-monads]]
[[!redirects colax idempotent monad]]
[[!redirects colax idempotent monads]]

[[!redirects lax idempotent]]
[[!redirects lax idempotence]]
[[!redirects colax idempotent]]
[[!redirects colax idempotence]]