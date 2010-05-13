## Idea

A lax-idempotent 2-monad encodes a certain kind of [[stuff, structure, property|property-like structure]] that a category, or more generally an object of a 2-category, can carry.

The archetypal examples are given by 2-monads $T$ on $Cat$ that take a category $C$ to the free cocompletion $T C$ of $C$ under a given class of colimits -- then an algebra $T C \to C$ is a category $C$ with all such colimits, which are of course essentially unique.  Moreover, given thus-cocomplete categories $C$ and $D$, a functor $F \colon C \to D$, and a diagram $S$ in $C$, there is a unique arrow $colim T F S \to F(colim S)$ given by the universal property of the colimit.  It is this property that lax-idempotence generalizes.


## Definition

A [[2-monad]] $T$ on a [[2-category]] $K$ is called **lax-idempotent** if given any two (strict) $T$-algebras $a \colon T A \to A$, $b \colon T B \to B$ and a morphism $f \colon A \to B$, there exists a unique 2-cell $\bar f \colon b \circ T f \Rightarrow f \circ a$ making $(f,\bar f)$ a lax morphism of $T$-algebras.

Lax-idempotent monads are also referred to as **Kock--Z&#246;berlein** or **KZ** monads.

### Equivalent conditions

A 2-monad $T$ as above is lax-idempotent iff

* for any $T$-algebra $a \colon T A \to A$ there is a 2-cell $\theta \colon 1 \Rightarrow \eta A \circ a$ such that $(\theta,1_{1_A})$ are the unit and counit of an [[adjunction]] $a \dashv \eta A$.

  Indeed, $\mu_A \colon T^2 A \to T A$ is a $T$-algebra on $T A$, and $\eta_A \colon A \to T A$ is a morphism from the underlying object of $a$ to that of $\mu_A$.  So there is a unique $\bar\eta_A \colon \mu_A \circ T \eta_A = 1_{T A} \Rightarrow \eta_A \circ a$ making $\eta_A$ into a lax $T$-morphism.  The [[adjunction|triangle equalities]] then require that:

  1.  $a \bar\eta_A \colon a \Rightarrow a \circ \eta_A \circ a = a$ is equal to $1_a$.  The composite $a \circ \bar\eta_A$ makes $a \circ \eta_A$ a lax $T$-morphism from $a$ to $a$ (paste $\bar\eta_A$ with the identity square $a \circ \mu_A = a \circ T a$).  But $a \circ \eta_A = 1_A$, and $1_a$ also makes this into a lax $T$-morphism, so by uniqueness $a \bar\eta_A = 1_a$.

  2. $\bar\eta_A \eta_A \colon \eta_A \Rightarrow \eta_A \circ a \circ \eta_A = \eta_A$ is equal to $1_{\eta_A}$.  But this follows directly from the unit coherence condition for the lax $T$-morphism $\bar\eta_A$.

* Since $T$'s multiplication $\mu$ makes $T$ itself into a (generalized) $T$-algebra, the above implies (and in fact is implied by) the requirement that there exist a [[modification]] $\ell \colon 1_{T^2} \to \eta T \circ \mu$ making $(\ell,1_{1_T}) \colon \mu \dashv \eta T$.

  Given an algebra $a \colon T A \to A$, the 2-cell $\theta$ is given by $T a \circ \ell_A \circ T \eta_A$.

* There is a modification $d \colon T \eta \to \eta T$ such that $d \eta = 1$ and $\mu d = 1$.

  Given $\ell$ as above, $d$ is given by $\ell \circ T \eta$.


## Examples

As mentioned above, the standard examples of lax-idempotent 2-monads are those on $Cat$ whose algebras are categories with all colimits of a specified class.

A converse is given by Power _et. al._, who show that a 2-monad is a monad for free cocompletions if and only if it is lax-idempotent and the unit $\eta$ is dense (plus a coherence condition).

## References

* Kelly--Lack, _On property-like structures_, TAC 3(9), 1997.
* Kock, _Monads for which structures are adjoint to units_, JPAA 104:41--59, 1995.
* Power--Cattani--Winskel, _A representation result for free cocompletions_, JPAA 151:273--286, 2000.

[[!redirects KZ monad]]
[[!redirects KZ doctrine]]

[[!redirects lax-idempotent monad]]