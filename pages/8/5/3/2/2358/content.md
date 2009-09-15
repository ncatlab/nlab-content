<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]


</div>



+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

This entry disscusses basics of [[formal group law]]s arising from [[periodic cohomology theory|periodic]] [[multiplicative cohomology theory|multiplicative]] [[cohomology theory|cohomology theories]]

=--

Previous:

* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]


## rough notes from a talk##

>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention, meaning: **somebody should go through this and polish**




We will talk about a lifting problem that will lead to the formulation of [[tmf]]. This requires [[E-infinity ring]]s and [[derived algebraic geometry]].

**Definition**

An $\Omega$-[[spectrum]] is a sequence of pointed [[topological space]]s $\{E_n\}$ and base-point preserving maps $\{\sigma_n : E_n \to \Omega E_{n+1}\}$ that are [[weak homotopy equivalence]]s.

($\Omega E_n$ is the [[loop space]] of $E_n$).

if $\{E_n\}$ is an $\Omega$-spectrum, define $h^{-n}(X) := [X, E_n]$ ([[homotopy]] classes of continuous maps). Then this $h$ is a [[generalized (Eilenberg-Steenrod) cohomology theory]].

It should be noted that all our spaces are based and $h$ is a reduced cohomology theory. Define $\pi_n(E) := [S^0, E_n]$. $\pi_*(E)$ are the coefficients (i.e. the cohomology over the point of the corresponding unreduced theory) of $E$.

**Brown's representability theory**: Any [[reduced cohomology theory]] on [[CW-complex]]es is [[representable functor|represented]] by an $\Omega$-[[spectrum]].

**examples** 

1. [[singular cohomology]] with coefficients in $A$: the [[Eilenberg-MacLane spectrum]] $H A$.

1. complex [[K-theory]]: $K_n = \mathbb{Z} \times BU$ for $n$ even and $\cdots = U$ otherwise

Le $M_{1,1}$ be the [[moduli stack]] of all [[elliptic curve]]s, then $Hom(Spec R, M_{1,1}) = \{elliptic curves over Spec R\}$.

(we will construct this more rigorously later)

If $\phi : Spec R \to M_{1,1}$ is a map that is a [[flat morphism]], then we obtain an [[elliptic cohomology]] theory called $A_{\phi}$.

This assignment is a [[presheaf]] of [[cohomology theory|cohomology theories]].

To get a single [[cohomology theory]] from that we want to take global sections, but there is no good way to say what a global section of a cohomology-theoy valued functor would be. One reason is that there is not a good notion to say what a _sheaf_ of [[cohomology theory]]s is. 

But if we had an [[(infinity,1)-category]] valued functor, then [[Higher Topos Theory]] would provide all that technology. So that's what we try to get now.

**goal** find lift

$$
  \array{
    && Spectra
    \\
    & {}^{?}\nearrow & \;\;\;\downarrow^{represent}
    \\
    \{\phi : Spec R \to M_{1,1}\}
    &\to&
    CohomologyTheories
  }
  \,.
$$


**Hopkins-Miller**: use the multiplicative nature of cohomology theories to solve this, i.e. instead look for a more refined lift

$$
  \array{
    && CommRingSpectra
    \\
    & {}^{O_{M^{der}}}\nearrow & \downarrow
    \\
    \{\phi : Spec R \to M_{1,1}\}
    &\to&
    MultiplicativeCohomologyTheories
  }
  \,.
$$

**theorem** There exists a [[symmetric monoidal category|symmetric monoidal]] [[model category]] $StTop$ of [[spectrum|spectra]] such that the  [[homotopy category]] is the [[stable homotopy category]] as a symmetric monoidal category.

This and the following is described in more detail at [[symmetric monoidal smash product of spectra]].

**Definition** An [[A-infinity ring]] is an ordinary [[monoid]] in $StTop$ and an [[E-infinity ring]] is an ordinray commutative monoid there.


So an $E_\infty$-ring is an honest [[monoid]] with respect to the funny smash product that makes spectra a symmetric monoidal category, but it is just a monoid up to homotopy with respect to the ordinary product of spaces.

For more on this see (for the time being) the literature referenced at [[stable homotopy theory]].

**proposition**

Let $A$ be an [[A-infinity ring]] [[spectrum]].

1. the $\infty$-monoidal structure on the spectrum induces a [[multiplicative cohomology theory]].

1. $\pi_0(A)$ is a commutative ring

1. $\pi_n(A)$ is a [[module]] over $\pi_0(A)$.

**Definition** For $A$ an [[E-infinity ring]], $M$ with a map $A \wedge M \to M$ such that the obvious diagrams commute is a [[module]] for that [[E-infinity ring]].

**Proposition** $\pi_*(M)$ is a graded [[module]] over $\pi_*(A)$.

**Definition** for $A$ an [[E-infinity ring]] and $M$ an $A$-module, we have that $M$ is **flat module** if

1. $\pi_0(M)$ is flat over $\pi_0(A)$ in the ordinary sense

1. $\forall n : \pi_n(A) \otimes_{\pi_0(A)} \pi_0(M) \to \pi_n(M)$ is an isomorphism of $\pi_0(M)$-modules

**definition** a morphism $f : A \to B$ of [[E-infinity ring]]s is flat if $B$ regarded as an $A$-module using this morphism is flat. 

**Theorem (Goerss-Hopkins-Miller)**: 

A lift $O_{M_{1,1}, der}$ as indicated in the GOAL above (multiplicative version) does exists and is unique up to homotopy equivalence.


The [[tmf]]-[[spectrum]] is the global sections of this: 

   $$
     tmf[\Delta^{-1}] = \Gamma(O_{M_{1,1}, der})
   $$

   this is not elliptic (its not even nor has period 2), but is a multiplicative spectrum and hence defines a cohomology theory.

The [[spectrum]] [[tmf]] is obtained in the same manner by replacing $M_{1,1}$ by its [[Deligne-Mumford compactification]].

