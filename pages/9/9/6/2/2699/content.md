<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher algebra - contents]]


</div>



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


>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention, meaning: **somebody should go through this and polish**


***

#Contents#

* toc
{:toc}


#Derived Elliptic Curves#

**Definition** A [[derived elliptic curve]] over an (affine) [[derived scheme]] $\mathrm{Spec} A$ is a commutative [[derived group scheme]] (CDGS) $E /A$ such that $\overline{E} \to \mathrm{Spec} \pi_0 A$ is an [[elliptic curve]].

Let $A$ be an $E_\infty$-ring.  Let $E(A)$ denote the $\infty$-groupoid of oriented elliptic curves over $\mathrm{Spec} A$.  Note that $E(A)$ is in particular a space (we will return to this point later).

The point is to prove the following due to Lurie.

**Theorem** The functor $A \mapsto E(A)$ is representable by a derived Deligne-Mumford stack $\mathcal{M}^{Der} = (\mathcal{M} , O_\mathcal{M} )$.  Further, $\mathcal{M}$ is equivalent to the topos underlying $\mathcal{M}_{1,1}$ and $\pi_0 O_\mathcal{M} = O_{\mathcal{M}_{1,1}}$.  Also, restricting to discrete rings, $O_\mathcal{M}$ provides a lift in sense of Hopkins and Miller. 

#$\mathbf{G}$-Equivariant $A$-cohomology#

##The Strategy##
1. Define $A_{S^1} (*}$;

1. Extend to $A_{S^1} (X)$ where $X$ is a trivial $S^1$-space;

1. Define $A_T (X)$ where $T$ is a compact abelian Lie group where $X$ is again a trivial $T$-space;

1. Extend to $A_T (X)$ for any (finite enough) $T$-space;

1. Define $A_G (X)$ for $G$ any compact Lie group.

##$S^1$-equivariance##

To accomplish (1) we need a map
$$\sigma : \mathrm{Spf} A^{\mathbb{C} P^\infty} \to \mathbf{G}$$
over $\mathrm{Spec} A$.  Then we can define $A_{S^1} (*) = \Gamma (\mathbf{G})$.  Such a map arises from a completion map
$$A_{S^1} \to A^{\mathbb{C}P^\infty}$$ 
which we may interpret as a preorientation $\sigma \in \mathrm{Map} (BS^1 , \mathbf{G} (A))$.  Recall that such a map $\sigma$ is an orientation if the induced map to the formal completion of $\mathbf{G}$ is an isomorphism.

Recall two facts:

1. There is a bijection $\{ BS^1 \to \mathbf{G} (A) \} \leftrightarrow \{ \mathrm{Spf} A^{BS^1} \to \mathbf{G} \}$;

1. Orientations of the multiplicative group $\mathbf{G}_m$ associated to $A$ are in bijection with maps of $E_\infty$-rings $\{ K \to A\}$, where $K$ is the K-theory spectrum.

**Theorem** We can define equivariant $A$-cohomology using $\mathbf{G}_m$ if and only if $A$ is a $K$-algebra.

##The Abelian Lie Group Case##

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

1. $M_{\{e\}} (B) = \mathrm{Hom} ( \{e \} , \mathbf{G} (B) = \{e\}$, so $M_{\{e\}}$ is final over $\mathrm{Spec} A$, hence it is isomorphic to $\mathrm{Spec} A$.

How do we get a completion map $\sigma_T : BT \to M_T (A)$ for all $T$ given an orientation $\sigma_{S^1} : BS^1 \to \mathbf{G} (A)$?  By a composition: define
$$ Bev: BT \to \mathrm{Hom}(\hat T , BS^1), \; p \mapsto (f \mapsto Bf(p))$$
then define
$$\sigma_T := \sigma_{S^1} \circ Bev.$$

**Proposition**
There exists a map $\hat M$ such that the assignment $T \mapsto M_T$ factors as $T \mapsto \hat M (BT)$.

_Proof._ That such a factorization exists defines $\hat M$ on objects.  Now by choosing a base point in $BT'$ we have

$$ \mathrm{Hom} (BT , BT' ) \simeq BT' \times \mathrm{Hom} (T, T') $$

as spaces.  Now we need a map
$$BT' \to \mathrm{Hom} (M_T , M_{T'}) .$$
Because this map must be functorial in $T$ and $T'$ we can restrict to the universal case where $T$ is trivial and then
$$BT' \to \mathrm{Hom} ( M_{\{e\}} , M_{T'} ) = M_{T'} (A)$$
is just a preorientation $\sigma_{T'}$.


