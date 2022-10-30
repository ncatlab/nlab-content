
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# $M$-complete and $E$-cocomplete categories
* table of contents
{:toc}

## Idea

A [[category]] is $M$-complete or $E$-cocomplete if has certain [[limits]] or [[colimits]] of [[morphisms]] in a given class $M$ or $E$.

Not to be confused with an [[M-category]].


## Definitions

Let $C$ be a [[category]] and let $M$ be a class of [[monomorphisms]] in $C$.  (Often, $M$ will be the right class in an [[orthogonal factorization system]].)  We say that $C$ is **$M$-complete** if it admits all (even [[large category|large]]) [[intersections]] of $M$-[[subobjects]].  This means that it admits all (even large) [[wide pullbacks]] of families of $M$-morphisms, and such pullbacks are again in $M$.  (If $M$ is the right class of an OFS, then any intersection of $M$-morphisms which exists is automatically in $M$.)

If $M$ is the class of all monomorphisms, we may say **mono-complete** for $M$-complete.

Dually, if $E$ is a class of [[epimorphisms]], we say $C$ is **$E$-cocomplete** if it admits all [[cointersection]]s of $E$-morphisms, and **epi-cocomplete** if $E$ is the class of all epimorphisms.


## Examples

* If $C$ is $M$-[[well-powered category|well-powered]], then no large limits are required in the definition of $M$-completeness.  Therefore, if $C$ is well-powered and [[complete category|complete]], it is $M$-complete whenever $M$ is the right class in an OFS.  Dually, if $C$ is well-copowered and cocomplete, it is $E$-cocomplete whenever $E$ is the left class in an OFS.

* For similar reasons, the category [[FinSet]] is mono-complete and epi-cocomplete---although it is not complete or cocomplete, it is [[finitely complete category|finitely complete]] and [[finitely cocomplete category|cocomplete]], and its subobject lattices and quotient lattices are likewise [[essentially finite category|essentially finite]].

* If $C$ is a [[topological concrete category]] over a category $D$ which is mono-complete or epi-complete, then $C$ is also mono-complete or epi-complete.  For the faithful forgetful functor $U\colon C\to D$ preserves and reflects monos and epis, and so the [[weak structure|initial]] $C$-structure on an [[intersection]] of underlying monos in $D$ gives an intersection in $C$ and the [[strong structure|final]] $C$-structure on a [[cointersection]] of underlying epis in $D$ gives a cointersection in $C$.


## Construction of factorization systems

$M$-completeness is useful for constructing [[orthogonal factorization systems]].  The following is Lemma 3.1 in [CHK](#CHK).

+-- {: .num_theorem #ConstructingOFS}
###### Theorem
Let $M$ be a class of maps in a category $C$, and assume that

1. $M$ consists of monomorphisms,
2. $M$ is closed under [[composition]],
3. all [[pullbacks]] of $M$-morphisms exist in $C$ and are again in $M$, and
4. $C$ is $M$-complete.

Then there is an orthogonal factorization system $(E,M)$, with $E = {}^\perp M$.
=--
+-- {: .proof}
###### Proof
Given $f\colon A\to B$, let $m$ be the intersection of all $M$-morphisms $n\colon X \to B$ through which $f$ factors.  Then by the universal property of this intersection, we have $f = m e$ for some $e$; thus it suffices to show $e\in E$.  Suppose given a commutative square
$$\array{ A & \overset{g}{\to} & Z \\
  ^e \downarrow & & \downarrow^p \\
  Y & \underset{h}{\to} & W} $$
with $p\in M$.  By pulling $p$ back to $Y$ (since pullbacks of $M$-morphisms exist), we may assume that $Y=W$ and $h$ is the identity.  But now the composite $m p$ is an $M$-morphism through which $f$ factors, so by definition, $m$ factors through it.  Thus $p$ is an isomorphism and so the lifting problem can be solved.
=--

In fact, it is easy to see that the same proof constructs a [[factorization structure for sinks]].

Note that if $M$ is already part of a [[prefactorization system]], then any composite, pullback, or intersection of $M$-morphisms which exists is automatically also in $M$, since $M = E^\perp$.

+-- {: .num_cor}
###### Corollary
Let $(E,M)$ be a [[prefactorization system]] on a category $C$, and assume that

1. $M$ consists of monomorphisms,
2. All pullbacks of $M$-morphisms exist in $C$, and
3. $C$ is $M$-complete.

Then $(E,M)$ is an orthogonal factorization system.
=--

The following is a slight generalization of Theorem 3.3 of [CHK](#CHK).  There it is stated only for the case $M=$ [[strong monomorphisms]], in which case a finitely complete and $M$-complete category is called **finitely well-complete**.

+-- {: .num_theorem #OFSFromAdjunction}
###### Theorem
Let $S : A \rightleftarrows C : T$ be an [[adjunction]], and assume that $A$ is finitely complete and $M$-complete for some OFS $(E,M)$, where $M$ consists of monomorphisms and contains the split monics.  Define $E_S$ to be the class of maps inverted by $S$, and $M_S = (E_S)^\perp$; then $(E_S,M_S)$ is an OFS on $A$.
=--
+-- {: .proof}
###### Proof
First of all, since $M_S$ belongs to a prefactorization system, it is closed under composites, pullbacks, and any intersections which exist.  Therefore, if we define $M' \coloneqq M \cap M_S$, then $M'$ satisfies the hypotheses of Theorem \ref{ConstructingOFS}, and so we have an OFS $(E',M')$.

Now suppose given $f\colon A\to B$; we want to construct an $(E_S,M_S)$-factorization.  Let $v$ be the pullback of $T S f$ along the [[unit of an adjunction|unit]] $\eta_B \colon B \to T S B$.  The naturality square for $\eta$ at $f$ shows that $f$ factors through $v$, say $f = v w$.  Since $T S f$ is evidently in $M_S$, so is $v$; thus it suffices to find an $(E_S,M_S)$-factorization of $w$.

Let $w = n g$ be the $(E',M')$-factorization of $w$.  Since $M' \subseteq M_S$, it suffices to show that $g\in E_S$.  Note also that since $w$ is a first factor of the unit $\eta_A$, by passing to adjuncts we find that $S w$ is [[split monic]]; hence so also is $S g$.  But $T S g$ is then also split monic, hence belongs to $M$ and thus also to $M'$.  Therefore, since $g\in E'$, the naturality square for $\eta$ at $g$ contains a lift.  Passing to adjuncts again, we find that $S g$ is also [[split epic]], hence an isomorphism; thus $g\in E_S$ as desired.
=--

This is useful in the construction of [[reflective factorization systems]].


## Related concepts

* [[complete category]]


## References

* Cassidy and H&#233;bert and [[Max Kelly|Kelly]], "Reflective subcategories, localizations, and factorization systems".  *J. Austral. Math Soc. (Series A)* 38 (1985), 287--329
 {#CHK}


[[!redirects M-complete category]]
[[!redirects M-complete categories]]

[[!redirects mono-complete category]]
[[!redirects mono-complete categories]]

[[!redirects E-cocomplete category]]
[[!redirects E-cocomplete categories]]

[[!redirects epi-cocomplete category]]
[[!redirects epi-cocomplete categories]]

[[!redirects finitely well-complete category]]
[[!redirects finitely well-complete categories]]
