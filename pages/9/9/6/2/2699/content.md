
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--




+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

This entry contains a basic introduction to getting equivariant cohomology from [[derived group scheme]]s.


=--

Previous:

* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

* [[A Survey of Elliptic Cohomology - elliptic curves]]

* [[A Survey of Elliptic Cohomology - equivariant cohomology]]

* [[A Survey of Elliptic Cohomology - derived group schemes and (pre-)orientations]]

Next:

* [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves]]

> the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention, meaning: **somebody should go through this and polish** See also at _[[equivariant elliptic cohomology]]_.


***

#Contents#

* toc
{:toc}


#Derived Elliptic Curves#

**Definition** A [[derived elliptic curve]] over an (affine) [[derived scheme]] $\mathrm{Spec} A$ is a commutative [[derived group scheme]] (CDGS) $E /A$ such that $\overline{E} \to \mathrm{Spec} \pi_0 A$ is an [[elliptic curve]].

Let $A$ be an $E_\infty$-ring.  Let $E(A)$ denote the $\infty$-groupoid of oriented elliptic curves over $\mathrm{Spec} A$.  Note that $E(A)$ is in particular a space (we will return to this point later).

The point is to prove the following due to Lurie.

**Theorem** The functor $A \mapsto E(A)$ is representable by a derived Deligne-Mumford stack $\mathcal{M}^{Der} = (\mathcal{M} , O_\mathcal{M} )$.  Further, $\mathcal{M}$ is equivalent to the topos underlying $\mathcal{M}_{1,1}$ and $\pi_0 O_\mathcal{M} = O_{\mathcal{M}_{1,1}}$.  Also, restricting to discrete rings, $O_\mathcal{M}$ provides a lift in sense of Hopkins and Miller. 

#$\mathbf{G}$-Equivariant $A$-cohomology
{#equivariant}

##The Strategy##
1. Define $A_{S^1 } (*)$;

1. Extend to $A_{S^1} (X)$ where $X$ is a trivial $S^1$-space;

1. Define $A_T (X)$ where $T$ is a compact abelian Lie group where $X$ is again a trivial $T$-space;

1. Extend to $A_T (X)$ for any (finite enough) $T$-space;

1. Define $A_G (X)$ for $G$ any compact Lie group.

##$S^1$-equivariance##

To accomplish (1) we need a map
$$\sigma : \mathrm{Spf} A^{\mathbb{C} P^\infty} \to \mathbf{G}$$
over $\mathrm{Spec} A$.  Then we can define $A_{S^1} (*) = O (\mathbf{G})$.  Such a map arises from a completion map
$$A_{S^1} \to A^{\mathbb{C}P^\infty}$$ 
which we may interpret as a preorientation $\sigma \in \mathrm{Map} (BS^1 , \mathbf{G} (A))$.  Recall that such a map $\sigma$ is an orientation if the induced map to the formal completion of $\mathbf{G}$ is an isomorphism.

Recall two facts:

1. There is a bijection $\{ BS^1 \to \mathbf{G} (A) \} \leftrightarrow \{ \mathrm{Spf} A^{BS^1} \to \mathbf{G} \}$;

1. Orientations of the multiplicative group $\mathbf{G}_m$ associated to $A$ are in bijection with maps of $E_\infty$-rings $\{ K \to A\}$, where $K$ is the K-theory spectrum.

**Theorem** We can define equivariant $A$-cohomology using $\mathbf{G}_m$ if and only if $A$ is a $K$-algebra.

##The Abelian Lie Group Case for a Point##

Fix $\mathbf{G}/A$ oriented. Now let $T$ be a compact abelian Lie group.  We construct a commutative [[derived group scheme]] $M_T$ over $A$ whose global sections give $A_T$ which is equipped with an appropriate completion map.

**Definition** Define the Pontryagin dual, $\hat T$ of $T$ by $\hat T := \mathrm{Hom}_\mathrm{Lie} (T, S^1)$.

**Examples**

1. $T=T^n$, the $n$-fold torus.  Then $\hat T = \mathbb{Z}^n$ as 
$$\hat T \ni ( \theta_1 , \dots , \theta_n ) \mapsto (k_1 \theta_1 , \dots , k_n \theta_n ).$$

1. If $T = \{ e \}$, then $\hat T = T$.

**Pontryagin Duality** If $T$ is an abelian, locally compact topological group then $\hat \hat T \simeq T$.

**Definition** Let $B$ be an $A$-algebra.  Define $M_T$ by
$$M_T (B) := \mathrm{Hom}_\mathrm{AbTop} (\hat T , \mathbf{G} (B)).$$

Further, $M_T$ is representable.

**Examples**

1. $M_{S^1} (B) = \mathrm{Hom} ( \mathbb{Z} , \mathbf{G} (B)) = \mathbf{G} (B).$

1. $M_{T^n} = \mathbf{G} \times_{\mathrm{Spec} A} \dots \times_{\mathrm{Spec} A} \mathbf{G}.$

1. $M_{\mathbb{Z}/n} = \mathrm{hker} (\times n: \mathbf{G}\to \mathbf{G}).$ 

1. $M_{\{e\}} (B) = \mathrm{Hom} ( \{e \} , \mathbf{G} (B) = \{e\}$, so $M_{\{e\}}$ is final over $\mathrm{Spec} A$, hence it is isomorphic to $\mathrm{Spec} A$.

How do we get a completion map $\sigma_T : BT \to M_T (A)$ for all $T$ given an orientation $\sigma_{S^1} : BS^1 \to \mathbf{G} (A)$?  By a composition: define
$$ Bev: BT \to \mathrm{Hom}(\hat T , BS^1), \; p \mapsto (f \mapsto Bf(p))$$
then define
$$\sigma_T := \sigma_{S^1} \circ Bev.$$

**Proposition**
There exists a map $\hat M$ such that the assignment $T \mapsto M_T$ factors as $T \mapsto \hat M (BT)$. That is the functor $M$ factors through the category of classifying spaces of compact Abelian Lie groups $B(CALG)$ (considered as orbifolds). Further, such factorizations are in bijection with the preorientations of $\mathbf{G}$.

_Proof._ That such a factorization exists defines $\hat M$ on objects.  Now by choosing a base point in $BT'$ we have

$$ \mathrm{Hom} (BT , BT' ) \simeq BT' \times \mathrm{Hom} (T, T') $$

as spaces.  Now we need a map
$$BT' \to \mathrm{Hom} (M_T , M_{T'}) .$$
Because this map must be functorial in $T$ and $T'$ we can restrict to the universal case where $T$ is trivial and then
$$BT' \to \mathrm{Hom} ( M_{\{e\}} , M_{T'} ) = M_{T'} (A)$$
is just a preorientation $\sigma_{T'}$.

##The Abelian Case for General Spaces##
We will see that $A_T (X)$ is the global sections of a quasi-coherent sheaf on $M_T$.

**Theorem** Let $\mathbf{G}$ be preoriented and $X$ a finite $T$-CW complex.  There exist a unique family of functors $\{ F_T \} $ from finite $T$-spaces to the category of quasi-coherent sheaves on $M_T$ such that

1. $F_T$ maps $T$-equivariant (weak) homotopy equivalences to equivalence of quasi-coherent sheaves;

1. $F_T$ maps finite homotopy colimits to finite homotopy limits of quasi-coherent sheaves;

1. $F_T (*) = O (M_\mathbf{G})$;

1. If $T \subset T'$ and $X' = (X \times T' )/T$ then $F_{T'} (X') \simeq f_* (F_T (X))$, where $f: M_T \to M_{T'}$ is the induced map;

1. The $F_T$ are compatible under finite chains of inclusions of subgroups $T \subset T' \subset T'' \dots$.

_Proof._ Use (2) to reduce to the case where $X$ is a $T$-equivariant cell, i.e. $X = T/ T_0 \times D^k$ for some subgroup $T_0 \subset T$.  Use (1) to reduce to the case where $X = T/T_0$. Use (3) to conclude that $F_T (T/T_0) = f_* F_{T_0} (*)$.  Finally, (4) implies that $F_{T_0} (*) = \hat M (*/T_0 )$, where $\hat M$ is specified by the preorientation.

>For trivial actions there is no dependence on the preorientation.

**Remark** 

1. $F_T (X)$ is actually a sheaf of algebras.

1. If $X,Y$ are $T$-spaces then we have maps
$$F_T (X) \to F_T (X \times Y) \leftarrow F_T (Y)$$
and
$$F_T (X) \otimes F_T (Y) \to F_T (X \times Y).$$

1. Define relative version for $X_0 \subset X$ by
$$F_T (X, X_0 ) = hker (F_T (X) \to F_T (X_0 ))$$
and for all $T$-spaces $Y$ we have a map
$$F_T (X, X_0 ) \otimes_{A} F_T (Y) \to F_T (X \times Y , X_0 \times Y).$$

**Definition** $A_T (X) = \Gamma (F_T (X))$ as an $E_\infty$-ring (algebra).

We now verify loop maps on $A_T$.

Recall that in the classical setting $A^n (X)$ is represented by a space $Z_n$ and we have suspension maps $Z_0 \to (S^n \to Z_n)$.  Now we need to consider all possible $T$-equivariant deloopings, that is $T$-maps from $S^n \to Z_n$.

**Theorem** Let $\mathbf{G}$ be oriented, $V$ a finite dimensional unitary representation of $T$.  Denote by $SV \subset BV$ the unit sphere inside of the unit ball.  Define $L_V = F_T (BV, SV)$.  Then

1. $L_V$ is a line bundle on $M_T$, i.e. invertible;

1. For all (finite) $T$-spaces $X$ the map

$$L_V \otimes F_T (X) \to F_T (X \times BV, X \times SV)$$
is an isomorphism.

_Proof for $T = S^1 = U(1)$ and $V = \mathbb{C}$._  Then 

$$L_V = hker ( F_T (BV) \to F_T (SV)) .$$

As $BV$ is contractible $F_T (BV) = O (\mathbf{G})$ and by property (3) above $F_T (SV) = f_* (O (\mathrm{Spec} A))$ for $f: \mathrm{Spec} A \to \mathbf{G}$ is the identity section.  As $\mathbf{G}$ is oriented, $\pi_0 \mathbf{G} / \pi_0 \mathrm{Spec} A$ is smooth of relative dimension 1, so $L_V$ can be though of as the invertible sheaf of ideals defining the identity section of $\mathbf{G}$.

Suppose $V$ and $V'$ are representations of $T$ then $L_V \otimes L_{V'} \to L_{V \oplus V'}$ is an equivalence.  So if $W$ is a virtual representation (i.e. $W = U - U'$) then
$L_W = L_U \otimes (L_{U'} )^{-1} .$

**Definition** Let $V$ be a virtual representation of $T$ and define
$$A_T^V (X) = \pi_0 \Gamma (F_T (X) \otimes L_V^{-1}) .$$

>The point is that in order to define equivariant cohomology requires functors $A_G^W$ for all representations of $G$, not just the trivial ones.  In the derived setting we obtain this once we have an orientation of $\mathbf{G}$.


##The Non-Abelian Lie Group Case##
Let $A$ be an $E_\infty$-ring, $\mathbf{G}$ an orientated commutative [[derived group scheme]] over $\mathrm{Spec} A$, and $T$ a (not necessarily Abelian) compact Lie group.

**Theorem** There exists a functor $A_T$ from (finite?) $T$-spaces to Spectra which is uniquely characterized by the following.

1. $A_T$ preserves equivalence;

1. For $T_0 \subset T$, $A_{T_0} (X) = A_T ((X \times G) / T_0 )$;

1. $A_T$ maps homotopy colimits to homotopy limits;

1. If $T$ is Abelian, then $A_T$ is defined as above;

1. For all spaces $X$ the map

$$ A_T (X) \to A_T (X \times E^{ab} T) $$
where $E^{ab} T$ is a $T$-space characterized by the requirement that for all Abelian subgroups $T_0 \subset T$, $(E^{ab} T )^{T_0}$ is contractible and empty for $T_0$ not Abelian.
Further, for Borel equivariant cohomology we require

1. If $T = \{e \}$, then $A_T(X) = A(X) = A^X$;

1. $A_T (X) \to A_T (X \times ET)$ is an isomorphism.

_Proof._ In the case of ordinary equivariant cohomology we can use property (5) to reduce to the case where $X$ has only Abelian stabilizer groups.  Then via (3) we reduce to $X$ being a colimit of $T$-equivariant cells $D^k \times T/T_0$ for $T_0$ Abelian. Via homotopy equivalence (1) we reduce to $X = T / T_0$.  Using property (2) we see $A_T (X) = A_{T_0} (*)$, so (4) yields $A_{T_0} (*) = \hat M (*/T_0 )$




