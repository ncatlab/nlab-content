

<div class="rightHandSide toc">


[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]


***

[[!include cohomology - contents]]

</div>


>**Abstract** 

+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

=--

Here are the entries on the previous sessions:


* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

* [[A Survey of Elliptic Cohomology - elliptic curves]]

* [[A Survey of Elliptic Cohomology - equivariant cohomology]]

 
* [[A Survey of Elliptic Cohomology - derived group schemes and (pre-)orientations]]

* [[A Survey of Elliptic Cohomology - A-equivariant cohomology]]

* [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves]]

***


# Towards a proof #
* automatic table of contents goes here
{:toc}

Recall the main theorem.

+-- {: .un_theorem }
###### Theorem
**(J. Lurie)**

For

* $A$ any [[E-∞ ring]]

* and $E(A)$ is the space of oriented [[derived elliptic curve]]s over $A$ (the realization of the topological category of elliptic curves over $A$).

There exists a derived Deligne-Mumford stack $M^{Der} = (M, O^{Der})$ such that we have an equivalence

$$
  Hom(Spec A, M^{Der})  
  \simeq
  E(A)
$$

natural in $A$.

And $O^{Der}$ provides the lift of Goerss-Hopkins-Miller.

=--

##Preliminaries##

Recall that for $A$ an $E_\infty$-ring a [[derived elliptic curve]] $F$ is a commutative [[derived group scheme]] over $A$ such that $F_0$ over $\pi_0 A$ is an elliptic curve.  

Denote by $E' (A)$ the space of preoriented (derived) elliptic curves (so equipped with a map $\mathbb{C} P^\infty \to F ( \mathrm{Spec} A )$. And $E(A)$ the space of oriented elliptic curves.

Note that a map $\mathrm{Spec} A \to M^{Der}$ is a map
$\mathrm{Spec} \pi_0 A \to M_{1,1}$ and a map of rings
$O (\mathrm{Spec} \pi_0 A) \to A$.

##Representability##

In his thesis, Lurie proves the following.

**Proposition.** Let $F$ be a functor from connective $E_\infty$-ring spectra to spaces s.t.

1. The restriction of $F$ to discrete rings is represented by a (classical) DM-stack $X$, i.e. $F(R) \simeq \mathrm{Nerv} X(R)$;

1. $F$ is a sheaf with respect to the etale topology;

1. $F$ has a good deformation theory.

Then there exists a derived DM-stack $(X , \hat O )$ representing $F$ s.t. $\hat O (U)$ is connective for $U$ affine.


**Examples.**

1. The functor $E'$: observe that every classical elliptic curve over a discrete $R$ has a unique preorientation.  Hence $E'$ is represented by DM-stack $(M, O' )$.

1. The functor $E$: the theorem doesn't apply as a discrete ring cannot be weakly periodic.


**Claim.** $(M, O')$ represents $E'$ for all $E_\infty$-rings, so we dropped connectivity.

_Proof._ Recall the map $A \to \tau_{\ge 0} A$ to the connected cover.

1. Let $A$ be an $E_\infty$-ring, then we have an equivalence

$$\mathrm{Hom} (O' (\mathrm{Spec} \pi_0 \tau_{\ge 0} A) , \tau_{\ge 0} A ) \to \mathrm{Hom} (O' (\mathrm{Spec} \pi_0 A) , A).$$

1. $E' ( \tau_{\ge 0} A \simeq E' (A)$ since every elliptic curve is by definition flat.

We need the following to prove the claim.

**Proposition.** The functor $M \mapsto M \otimes_{\tau_{\ge 0} A} A,$ from flat modules over $\tau_{\ge 0} A$ to flat modules over $A$ is an equivalence.

_Proof of proposition (sketch)._
Let $M,N$ be $A$-modules then there is a spectral sequence

$$\mathrm{Tor}_{p}^{\pi_* A} (\pi_* M, \pi_* N )_q \Rightarrow \pi_{p+q} (M \otimes_A N ) .$$

Suppose $M$ is flat, then

$$\mathrm{Tor}_{p}^{\pi_* A} (\pi_* M , \pi_* N) = \pi_* N \otimes_{\pi_0 A} \pi_0 M$$

if $p=0$ and 0 otherwise.  Thus,

$$\pi_* (M \otimes_A N ) \simeq \pi_* N \otimes_{\pi_0 A} \pi_0 M .$$

So we have

$$ F: \mathrm{Mod}^{flat} (\tau_{\ge 0} A ) \leftrightarrow \mathrm{Mod}^{flat} (A) : G .$$

This is an equivalence and $F$ respects the monoidal structure, hence the equivalence extends to the categories of algebras and the proposition (and hence claim) is proved.



We need to know that $\pi_i O'$ are coherent sheaves over $M_{1,1}$, where a [[coherent sheaf]] is an assignment $\mathrm{Spec} R \to M_{1,1}$ which behaves well under finite limits.  Let $\omega$ be the line bundle of invariant differentials on $M_{1,1}$ so that is

$$ \omega = e^* \Omega_{F |_{\mathrm{Spec} R}}. $$

Recall that a preorientation determines a map $\beta : \omega \to \pi_2 (O' )$.  So define a sheaf of $E_\infty$-rings $O$ as $O' [ \beta^{-1} ]$ which is characterized (maybe) by 

$$ \pi_n O = \lim ( \pi_{n+2k} O' \otimes_{O_{1,1}} \omega^{-k} ) .$$

**Remark.**

* This formula comes from a much simpler situation...Let $R$ be (an honest to God) ring, $x \in R$ then

$$ R[x^{-1}] \simeq \lim (R \stackrel{x}{\to} R  \stackrel{x}{\to} \dots )$$

* Suppose $U \to M_{1,1}$ with $U$ affine, $\omega$ restricted to $U$ is trivialized then $O' (U) =A$ and $\beta \in \pi_2 A$.  Hence, $O' [\beta^{-1} ] (U) = A [ \beta^{-1} ]$ and we get the formula above $\pi_i (A [ \beta^{-1} ]) = (\pi_i A) [\beta^{-1} ]$.

More generally, for $U \to M_{1,1}$ we have that $O(U)$ is weakly periodic, so

$$ \pi_2 O (U) \otimes_{\pi_0 O(U)} \pi_n O(U) \to \pi_{n+2} O (U) $$

is an equivalence.

*  $(M, O)$ classifies oriented elliptic curve.  Let $F$ over $U = \mathrm{Spec} B$ be a preoriented elliptic curve over $B$, so we have the classifying map $f: O' (U) = A \to B$ and this is an orientation iff 

$$ \pi_n B \otimes_{\pi_0 B} \omega \to \pi_{n+2} B $$

is an isomorphism.  This map can be identified with $\times \beta$, so the preorientation is an orientation iff there is a unique factorization through $O(U) = A [ \beta^{-1} ]$.


##Reduction##

**Claim.** To prove the theorem it is enough to show

1. $O_{1,1} = \pi_0 O' \to \pi_0 O$ is an isomorphism;

1. For $n$ odd, the sheaf $\pi_n O =0$.

_Proof._  Suppose (1) and (2) hold.  Let $f: \mathrm{Spec} R \to M_{1,1}$ be etale for $R$ discrete.  We must show that $O (\mathrm{Spec} R)$ is an elliptic cohomology theory associated to $f$. Condition (1) ensures $\pi_0 A \simeq R$, (2) guarantees evenness and from above we have weakly periodic.  We must show that $\mathrm{Spf} A^{0} (\mathbb{C}P^\infty ) \simeq \hat E_f$ which follows from having an orientation.


##Reducing to a Local Calculation##
We wish to show that $\pi_n O = 0$ for $n$ odd.  From above, it suffices to show that

$$ f_k : \pi_{n+2k} O' \otimes \omega^{-k} \to \pi_n O $$

is zero for all $k$. Note that $\mathrm{im} (f_k )$ is a quotient of $\pi_{n+2k} O' \to \mathrm{im} (f_k )$ which is coherent.  Suppose $p$ is an etale cover of $M_{1,1}$ then
$\mathrm{im} (f_k ) = 0$ iff $p^{i} \mathrm{im} (f_k )=0$. We can find an etale cover by a disjoint union of level 3 and level 4 modular forms denoted $\mathrm{Spec} R$.

That $M:= p^{i} \mathrm{im} (f_k ) =0$ is equivalent to $M \otimes_R R/m$ for all $m \in R$.  It is not difficult to show that all residue fields $R/m$ are finite in this case. 

Now it is enough to show condition (2) formally locally as $\hat R_m /m \simeq R_m / m$.


