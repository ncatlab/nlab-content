<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher category theory - contents]]


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



## contents

* [part 1](#part1)

* [part 2](#part2)

## part 1 {#part1}


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



## part 2 {#part2}



recall that we want global sections of the [[presheaf]]

$$
  \{Spec R \to M_{1,1}\} \to CohomologyTheories
$$

(on the left we have something like the etale [[site]] of the moduli stack $M_{1,1}$ )

but there is no good notion of gluing in CohomologyTheories (lack of colimits) hence no good notion of sheaves with values in cohomology theories. $CohomologyTheories$ is the [[homotopy category]] of some other category, to be identified, and passage to homotopy categories may destroy existence of useful colimits. The category of CohomologyTheories "is" the stable homotopy category.

A simple example:

in the [[(infinity,1)-category]] [[Top]] we have the homotopy pushout

$$
  \array{
    S^1 &\to& D^2
    \\
    \downarrow && \downarrow
    \\
     D^2 &\to& S^2
  }
$$

but in the [[homotopy category]] the pushout is instead

$$
  \array{
    S^1 &\to& D^2
    \\
    \downarrow && \downarrow
    \\
     D^2 &\to& *
  }
$$

The result is not even homotopy equivalent. In the homotopy category the pushout does not exist.

So we want to refine $CohomologyTheories$ to the cateory of [[spectrum|spectra]] that they come from by the [[Brown representability theorem]].

In fact, we want to lift $MultiplicativeCohomologyTheories$ to that of [[E-infinity ring]]-spectra. 

The map

$$
  E_\infty Rings \to MultiplicativeCohomologyTheories
$$

should be that of taking the [[homotopy category of an (infinity,1)-category]].

**Approach A** (modern but traditional [[stable homotopy theory]]) choose a [[symmetric monoidal category|symmetric monoidal]] [[simplicial model category]] whose [[homotopy category]] is the [[stable homotopy category]] and whose [[tensor product]] is the [[smash product of spectra]]. For instance use the [[symmetric monoidal smash product of spectra]].

Then define [[E-infinity ring]] spectra to be ordinary [[monoid]] objects in this symmetric monoidal model category of spectra.

**Approach B** ([[Jacob Lurie]]: be serious about working with [[(infinity,1)-category]] instead of just [[model category]] theory) .

1. define [[(infinity,1)-category]] ([[Higher Topos Theory|chapter 1 of HTT]])

   in this framework we'll have a [[stable (infinity,1)-category of spectra]], let's call that $Sp$

2. show that $Sp$ is a [[symmetric monoidal (infinity,1)-category]]

3. show that the [[homotopy category of an (infinity,1)-category]] of $Sp$ is the [[stable homotopy category]], where the tensor product goes to the [[smash product of spectra]]

4. define an [[E-infinity ring]] to be a [[commutative monoid in an (infinity,1)-category]] in $Sp$.



These two approaches are equivalent is a suitable sense. See [[Noncommutative Algebra]], page 129 and [[Commutative Algebra]], 0.0.2 and paragraph 4.3.

[[derived algebraic geometry]] categorifies [[algebraic geometry]]

[[E-infinity ring]] categoriefies commutative [[ring]]

[[(infinity,1)-category]] catgeorifies [[category]]





**Definition** An [[(infinity,1)-category]] is (for instance modeled by) 

* a [[Top]]-[[enriched category]] (essentially [[simplicially enriched category]])

* a [[quasi-category]]

  (see there for details). In fact, see [[Higher Topos Theory]] for lots of details.

use [[homotopy coherent nerve]] to go from a [[simplicially enriched category]] to its corresponding [[quasi-category]] 

**definition** [[homotopy category of an (infinity,1)-category]] (see there)

**definition** morphism of [[(infinity,1)-category|(infinity,1)-categories]] is, when regarded as a [[quasi-category]], just a morphism of [[simplicial set]]s.: this is an [[(infinity,1)-functor]].

There is an [[(infinity,1)-category of (infinity,1)-functors]] between two [[(infinity,1)-categories]]




**why simplicial sets?**

because they provide a convenient calculus for doing [[homotopy coherent category theory]].

suppose some [[(infinity,1)-category]] $C$ and its homotopy category $C \to h C$.

A commutative-up-to-homotopy diagram in $C$ is a functor $I \to h C$

$$
  \array{
     && C
     \\
     && \downarrow
     \\
     I &\to& h C
  }
$$

for $I$ some diagram category.

to get a **homotopy coherent** diagram instead take the [[nerve]] $N(I)$ of $I$ and then map $N(I) \to C$.

The nerve automatically encodes the homotopy coherence. See [[Higher Topos Theory]] pages 37, 38 (but the general idea is well known from [[simplicial model category]] theory).

Now let $C$ be an [[(infinity,1)-category]]. Suppose that it has a [[zero object]] $0 \in C$, i.e. an object that is both an [[initial object]] and a [[terminal object]].

Assume that $C$ admits [[kernel]]s and [[cokernel]]s, i.e. all [[homotopy pullback]]s and pushouts with $0$ in one corner.

Then from this we get [[loop space object]]s $\Omega X$ and [[delooping]] objects $B X$ in $C$ (called suspension objects $\Sigma X$ in this context).

$$
  \array{
     X &\stackrel{f}{\to}& Y
     \\
     \downarrow &\Downarrow& \downarrow
     \\
     0 &\to& coker f
  }
  \;\;\;\;
    \array{
     ker(g) &\stackrel{}{\to}& X
     \\
     \downarrow &\Downarrow& \downarrow^g
     \\
     0 &\to& Y
  }
$$

in particular a [[loop space object]] $\Omega Y$ is the kernel of the 0-map,while the suspension $\Sigma X$ is the cokernel

$$
  \array{
     X &\stackrel{f}{\to}& 0
     \\
     \downarrow &\Downarrow& \downarrow
     \\
     0 &\to& \Sigma X
  }
  \;\;\;\;
    \array{
     \Omega Y &\stackrel{}{\to}& 0
     \\
     \downarrow &\Downarrow& \downarrow^g
     \\
     0 &\to& Y
  }
$$


One example of this is the [[(infinity,1)-category]] of [[pointed object|pointed]] [[topological space]]s.

**definition** a [[prespectrum object]] in an [[(infinity,1)-category]] $C$ with the properties as above is a [[(infinity,1)-functor]]

$$
  X : N(\mathbb{Z} \times \mathbb{Z}) \to C
$$

such that $X(i,j)$ for $i \neq j$ is  [[zero object]] 0.

$$
  \array{
     X(n,n) &\stackrel{}{\to}& X(n,n+1) \simeq 0
     \\
     \downarrow &\searrow& \downarrow^g
     \\
     X(n+1,n) \simeq 0 &\to& X(n+1,n+1)
  }
$$

(everything filled with 2-cells aka homotopies)



since we have cokernels we get maps from the universal property

$$
  \array{
     X(n,n) &\stackrel{}{\to}& X(n,n+1) \simeq 0
     \\
     \downarrow &\searrow& \downarrow^g
     \\
     0 &\to& \Sigma X(n,n)
     \\
     &&& \searrow^{\alpha_n}
     \\
     &&&& X(n+1,n+1)
  }
$$

and analogously maps $\beta_n : X(n,n) \to \Omega X(n+1, n+1)$

now $X$ is a **spectrum object** if the $\beta_n$ are equivalences, for all $n$. (We don't require $\alpha_n$ to be equivalences.)



so to each [[(infinity,1)-category]] $C$ we get another [[(infinity,1)-category]] $Sp(C)$, the full subcategory $Fun(N(\mathbb{Z}\times \mathbb{Z}), C)$ on the [[spectrum object]]s.

In particular, we set 

$$
  Sp := Sp(Top)
$$

the [[stable (infinity,1)-category of spectra]] is the stabilization of the [[(infinity,1)-category]] [[Top]] of [[topological space]]s.

**Fact**: $Sp$ has an essentially unique structure of a [[symmetric monoidal (infinity,1)-category]].

This monoidal structure $\otimes$ is uniquely characterized by the following two properties:

1. $\otimes$ preserves limits and colimits.

1. the [[sphere spectrum]] is the [[monoidal unit]]/[[tensor unit]] wrt $\otimes$.

**definition** A [[symmetric monoidal (infinity,1)-category]] structure on an [[(infinity,1)-category]] $C$ is given by the following data:

1. another [[(infinity,1)-category]] $C^\otimes$ with an [[(infinity,1)-functor]] $C^\otimes \to N(\Gamma)$ that is a [[coCartesian fibration]]

  where $\Gamma$ is [[Segal's category]] with objects finite [[pointed object|pointed]] [[set]]s and morphisms basepoint preserving [[function]]s between sets.

  such that $C^\otimes_{\langle 1\rangle} \simeq C$

  where $C^\otimes_{\langle 1\rangle}$ is the fiber 
  over $\langle 1\rangle = \{*,1\}$, i.e. the pullback

  $$
    \array{
      C^\otimes_{\langle 1\rangle} &\to& C^\otimes
      \\
      \downarrow &pullback& \downarrow
      \\
      \{\langle 1\rangle\} &\to& N(\Gamma)
    }
  $$

>here should go some pictures that illustarte this. But see the first few pages of [[Noncommutative Algebra]] for the intuition and motivation.

so let $C$ now be a [[symmetric monoidal (infinity,1)-category]]. 

**definition** A [[commutative monoid in an (infinity,1)-category|commutative monoid in]] $C$ is a [[section]] $s$ of the structure map mentioned above $C^\otimes \to N(\Gamma) \stackrel{s}{\to} C^\otimes$.

The monoid object itself is the image of $\langle 1 \rangle$ under $s$, $A = s(\langle 1 \rangle)$.

> There is one more condition on $s$, though.

**definition** an [[E-infinity ring]] spectrum is a [[commutative monoid in an (infinity,1)-category]] in the [[stable (infinity,1)-category of spectra]] $Sp$.

$E_\infty$-rings themselves form an [[(infinity,1)-category]]. And this has all [[limit]]s and [[colimit]]s (see DAG III 2.1, 2.7), so we can talk about sheaves of $E_\infty$ rings!

