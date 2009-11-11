

<div class="rightHandSide toc">

[[!include higher algebra - contents]]

</div>


>**Abstract** This entry attempts to give an outline of a proof of Lurie's main theorem.


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


###Reduction###

**Claim.** To prove the theorem it is enough to show

1. $O_{1,1} = \pi_0 O' \to \pi_0 O$ is an isomorphism;

1. For $n$ odd, the sheaf $\pi_n O =0$.

_Proof._  Suppose (1) and (2) hold.  Let $f: \mathrm{Spec} R \to M_{1,1}$ be etale for $R$ discrete.  We must show that $O (\mathrm{Spec} R)$ is an elliptic cohomology theory associated to $f$. Condition (1) ensures $\pi_0 A \simeq R$, (2) guarantees evenness and from above we have weakly periodic.  We must show that $\mathrm{Spf} A^{0} (\mathbb{C}P^\infty ) \simeq \hat E_f$ which follows from having an orientation.


###Reducing to a Local Calculation###
We wish to show that $\pi_n O = 0$ for $n$ odd.  From above, it suffices to show that

$$ f_k : \pi_{n+2k} O' \otimes \omega^{-k} \to \pi_n O $$

is zero for all $k$. Note that $\mathrm{im} (f_k )$ is a quotient of $\pi_{n+2k} O' \to \mathrm{im} (f_k )$ which is coherent.  Suppose $p$ is an etale cover of $M_{1,1}$ then
$\mathrm{im} (f_k ) = 0$ iff $p^{i} \mathrm{im} (f_k )=0$. We can find an etale cover by a disjoint union of level 3 and level 4 modular forms denoted $\mathrm{Spec} R$.

That $M:= p^{i} \mathrm{im} (f_k ) =0$ is equivalent to $M \otimes_R R/m$ for all $m \in R$.  It is not difficult to show that all residue fields $R/m$ are finite in this case. 

Now it is enough to show condition (2) formally locally as $\hat R_m /m \simeq R_m / m$.


##Key Ingredients##
In the previous section we had a moduli stack preoriented elliptic curves $(M,O')$.  The structure sheaf of $O'$ took values in _connected_ $E_\infty$-rings.  We had a refinement $(M, O)$ which was a moduli stack for oriented elliptic curves.  From the orientation condition we deduced that the structure sheaf took values in _weakly periodic_ $E_\infty$-rings.

Further, we showed how to reduce the main theorem to a (formal) local computation.  That is, we only need to consider $\hat R_m$, the completion of a ring localized at a maximal ideal.

We delay the completion of the proof until later, but now we introduce the key technical tool: $p$-divisible groups.

###$p$-divisible Groups###
Let $R$ be a complete, local ring (e.g. the $p$-adic integers $\mathbb{Z}_p$) and $E_0$ an [[elliptic curve]] over $R_0 := R/M = \mathbf{F}_q$.  What do we need in order to lift $E_0$ to an elliptic curve over $R$?

Let $p$ be a prime (say the characteristic of $\mathbf{F}_q$) and $E$ an [[elliptic curve]] over $R$.  Using the _multiplication by_ $p$ map $p^n \colon E \to E$ we can define a sheaf of Abelian groups
$$ E[p^\infty] := \mathrm{colim} \; E[p^n],$$
where $E[p^n]$ is the kernel of the map $p^n$.  That is, $E[p^n]$ corresponds to the $p$-torsion points of $E$.

**Definition.** A $p$-divisible group $\mathfrak{I}$ over $R$ is a sheaf of Abelian groups on the flat site of schemes over $R$ such that

1. $p^n : \mathfrak{I} \to \mathfrak{I}$ is surjective;

1. $\mathfrak{I} = \mathrm{colim} \; \mathfrak{I} [p^n]$ where $\mathfrak{I} = \mathrm{ker} \; (p^n \colon \mathfrak{I} \to \mathfrak{I})$.

1. $\mathfrak{I}[p^n]$ is a finite, flat, commutative $R$-group scheme.  Note that finite means that $\mathfrak{I}$ is affine and whose global sections is a finite $R$-module.

For instance, the constant sheaf $\underline{\mathbb{Z}_p}$ is a $p$-divisible group.

###Serre-Tate Theory###

Now let $R$, in addition to above, be Noetherian with residue field $\mathbf{F}_q$ for $q=p^n$.

**Theorem (Serre-Tate).**
Let $\overline{E}$ be an elliptic curve over $\mathbf{F}_q$, then there is an equivalence of categories between elliptic curves over $R$ that restrict to $\overline{E}$ and the category of $p$-divisible groups $\mathfrak{I}$ over $R$ such that the restriction of $\mathfrak{I}$ to $\mathbf{F}_q$ is $\overline{E} [p^\infty ]$.

The theorem is somewhat surprising as, _a priori_, the latter category sees only torsion phenomena of the elliptic curves.

###Derived Serre-Tate Theory###

**Definition.** Let $A$ be an $E_\infty$-ring.  A functor $\mathfrak{I}$ from commutative $A$-algebras to topological Abelian groups is a $p$-divisible group if

1. $B \mapsto \mathfrak{I} (B)$ is a sheaf;

1. $p^n : \mathfrak{I} \to \mathfrak{I}$ is surjective;

1. $(\mathrm{ho})\mathrm{colim} \; \mathfrak{I} [p^n] \simeq \mathfrak{I}$, where as above $\mathfrak{I} [p^n] := (\mathrm{ho}) \mathrm{ker} \; p^n$;

1. $\mathfrak{I}[p^n]$ is a derived commutative group scheme over $A$ which is finite and flat.

If $\mathfrak{I}$ is a $p$-divisible group over $\mathbf{F}_q$, then $\mathfrak{I} [p]$ is a finite $\mathbf{F}_q$-module of dimension $r$ called the _rank_ of $\mathfrak{I}$.

**Proposition.** If $\mathfrak{I} = E [p^\infty]$, for $E$ an elliptic curve, then $\mathfrak{I}$ has rank 2.

One can verify the proposition over $\mathbb{C}$ pretty easily; it is more subtle over a finite field.  We have a derived version of the Serre-Tate theorem.


**Theorem (Serre-Tate).** Let $A$ be an $E_\infty$-ring such that $\pi_0 A$ is a complete, local, Noetherian ring and $\pi_i A$ are finitely generated $\pi_0 A$-modules.  Let $E_0$ be a (derived) elliptic curve over $\pi_0 A / M$, then there is an equivalence of $\infty$-categories: elliptic curves over $A$ that restrict to $E_0$ and $p$-divisible groups over $A$ that restrict to $E_0 [p^\infty]$.

###Proof of the Classical Theorem###
We give a proof of the classical result, however the proof is quite formal and should carry over to the derived setting.

Let $R$ be a ring as in the theorem such that $N \cdot R =0$ for some $N \in \mathbb{N}$ and let $I \subset R$ be a nilpotent ideal, so $I^{r+1} =0$, and set $R_0 = R/I$.  Let $\mathfrak{I} \colon R-\mathrm{alg} \to \mathrm{Ab}$ and
$$ \mathfrak{I}_I (A) := \mathrm{ker} \; ( \mathfrak{I} (A) \to \mathfrak{I} (A / I \cdot A ) .$$
Further, define
$$ \overline{\mathfrak{I}} (A) := \mathrm{ker} \; (\mathfrak{I}(A) \to \mathfrak{I} (A / \mathrm{nil}R \cdot A)) \subset \mathfrak{I}_I (A) .$$

**Lemma.** If $\mathfrak{I}$ is a formal group over $R$, then $\mathfrak{I}_I$ is annihilated by $N^r$.


**Proposition.** Let $\mathfrak{I}$, $\mathfrak{H}$ be elliptic curves or $p$-divisible groups over $R$ and let $N=p^n$.  Denote by $\mathfrak{I}_0$ and $\mathfrak{H}_0$ the restriction of $\mathfrak{I}$ and $\mathfrak{H}$ to $R_0$-algebras.  Then

1. $\mathrm{Hom}_{R-grp} (\mathfrak{I}, \mathfrak{H})$ and $\mathrm{Hom}_{R_0-grp} (\mathfrak{I}_0 , \mathfrak{H}_0 )$ have no $N$-torsion;

1. $\mathrm{Hom} (\mathfrak{I} , \mathfrak{H}) \to \mathrm{Hom} (\mathfrak{I}_0 , \mathfrak{H}_0 )$ is injective;

1. For $f_0 \colon \mathfrak{I}_0 \to \mathfrak{H}_0$ there is a unique homomorphism $N^r f \colon \mathfrak{I} \to \mathfrak{H}$ which lifts $N^r \cdot f_0$;

1. $f_0 \colon \mathfrak{I}_0 \to \mathfrak{H}_0$ lifts to $f \colon \mathfrak{I} \to \mathfrak{H}$ if and only if $N^r f$ annihilates $\mathfrak{I}[N^r] \subset \mathfrak{I}$.

Note that if $E$ is an elliptic curve over $R$ then the $E_0$ above is given by
$$E_0 = E \times_{\mathrm{Spec} \; R} \mathrm{Spec} \; R/I .$$

Using the previous results one can prove the following alternate version of the Serre-Tate theorem.

**Theorem (alternative Serre-Tate).**
Let $R$ be a ring with $p$ nilpotent and $I \subset R$ a nilpotent ideal.  Let $R_0 = R/I$.  We have a categorical equivalence: elliptic curves over $R$ and the category of triples $\{ (E, E_0 [p^\infty] , \epsilon )\}$; where $E$ is an elliptic curve over $R_0$, $E_0 [p^\infty]$ is a $p$-divisble group over $R$, and $\epsilon \colon E_0 [p^\infty] \to E[p^\infty]_0$ is a natural isomorphism.

###Adding in Completions###
We really want to consider elliptic curves over $R$ completed by an ideal $m$, this is the $\hat{R}_m$ from far above.  We can reduce this problem to that of elliptic curves over $R$ and a system of $p$-divisible groups over $R/m^n$ by combining the Serre-Tate theorem and the following theorem of Grothendieck.

**Theorem (Formal GAGA).** Let $X, Y$ be exceedingly nice schemes over $R$ and $\hat X$, $\hat Y$ be their formal completions, then there is a bijection
$$\mathrm{Hom}_{R} (X,Y) \leftrightarrow \mathrm{Hom}_{\hat R} (\hat X, \hat Y).$$


