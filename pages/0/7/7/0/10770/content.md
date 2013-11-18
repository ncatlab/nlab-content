
> This entry explains the [[J-homomorphism]], states how its image is the first ([[chromatic layer|chromatic]]) layer of the [[sphere spectrum]]; and then  motivated by this explains some basic notions of [[chromatic homotopy theory]], notably the origin of the general $E$-[[Adams spectral sequence]].

#Contents#
* table of contents
{:toc}


## **I)** The J-homomorphism

### On groups
 {#OnGroups}


+-- {: .num_defn #SphereAsCompactification}
###### Definition

For $n \in \mathbb{N}$ regard the $n$-[[sphere]] (as a [[topological space]]) as the [[one-point compactification]] of the [[Cartesian space]] $\mathbb{R}^n$

$$
  S^n \simeq (\mathbb{R}^n)^\ast
  \,.
$$

=--

+-- {: .num_remark #ActionOfOrthogonalOnSphere}
###### Remark

Since the process of [[one-point compactification]] is a [[functor]] on [[proper maps]], hence on [[homeomorphisms]], via def. \ref{SphereAsCompactification} the $n$-sphere inherits from the canonical [[action]] of the [[orthogonal group]] $O(n)$ on $\mathbb{R}^n$ an [[action]] 

$$
  O(n) \times S^n \longrightarrow S^n
$$

(by [[continuous maps]]) which preserves the base point (the "point at infinity").

=--

For definiteness we distinguish in the following notationally between 

1. the $n$-[[sphere]] $S^n \in Top$ regarded as a [[topological space]];

1. its [[homotopy type]] $\Pi(S^n) \in L_{whe} Top \simeq$ [[∞Grpd]] given by its [[fundamental ∞-groupoid]].

Similarly we write $\Pi(O(n))$ for the [[homotopy type]] of the [[orthogonal group]], regarded as a [[group object in an (∞,1)-category]] in [[∞Grpd]] (using that the [[shape modality]] $\Pi$ preserves [[finite products]]).

+-- {: .num_defn #AutoequivalencesOfnSphere}
###### Definition

For $n \in \mathbb{N}$ write $H(n)$ for the [[automorphism ∞-group]] of homotopy self-equivalences $S^n \longrightarrow S^n$, hence

$$
  H(n) \coloneqq Aut_{\infty Grpd^{\ast/}}(\Pi(S^n))
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

The [[∞-group]] $H(n)$, def. \ref{AutoequivalencesOfnSphere}, constitutes the two [[connected components]] of the $n$-fold based [[loop space]] $\Omega^n S^n$ corresponding to  the [[homotopy groups]] $\pm 1 \in \pi_n(S^n)$.

=--

+-- {: .num_defn #OrthogonalActionOnSphereOnHomotopyGroups}
###### Definition

Via the presentation of [[∞Grpd]] by the [[cartesian closed model structure|cartesian closed]] [[model structure on topological spaces|model structure on compactly generated topological spaces]] (and using that $S^n$ and $O(n)$ and hence their product are [[compact topological spaces|compact]]) we have that for $n \in \mathbb{N}$ the [[continuous function|continuous]] [[action]] of $O(n)$ on $S^n$
of remark \ref{ActionOfOrthogonalOnSphere}, which by [[cartesian closed category|cartesian closure]] is equivalently a homomorphism of [[topological groups]] of the form

$$
  O(n) \longrightarrow Aut_{Top^{\ast/}}(S^n)
  \,,
$$

induces a homomorphism of [[∞-groups]] of the form

$$
  \Pi(O(n)) \longrightarrow Aut_{\infty Grpd^{\ast/}}(\Pi(S^n))
  \,.
$$

This in turn induces for each $i \in \mathbb{N}$ homomorphisms of [[homotopy groups]] of the form

$$
  \pi_i(O(n)) \longrightarrow \pi_i(\Omega^n S^n) \simeq \pi_{n+i}(S^n)
  \,.
$$


=--

+-- {: .num_remark #OrthogonalActionOnSphereOnHomotopyGroups}
###### Remark

By construction, the homomorphisms of remark \ref{OrthogonalActionOnSphereOnHomotopyGroups} are compatible with  [[suspension]] in that for all $n \in \mathbb{N}$ the [[diagrams]]

$$
  \array{
    O(n) &\longrightarrow& Aut_{Top^{\ast/}}(S^n)
    \\
    \downarrow && \downarrow
    \\
    O(n+1) &\longrightarrow& Aut_{Top^{\ast/}}(S^{n+1})
  }
$$

in $Grp(Top)$ commute, and hence so do the diagrams

$$
  \array{
    \Pi(O(n)) &\longrightarrow& Aut_{\infty Grpd^{\ast/}}(\Pi(S^n))
    \\
    \downarrow && \downarrow
    \\
    \Pi(O(n+1)) &\longrightarrow& Aut_{\infty Grpd^{\ast/}}(\Pi(S^{n+1}))
  }
$$

in $Grp(\infty Grpd)$, up to [[homotopy]].

=--

Therefore one can take the [[direct limit]] over $n$:


+-- {: .num_defn #JHom}
###### Definition

By remark \ref{OrthogonalActionOnSphereOnHomotopyGroups}
there is induced a homomorphism 

$$
  J_i \;\colon\; \pi_\bullet(O) \longrightarrow \pi_\bullet(\mathbb{S})
$$

from the [[homotopy groups]] of the [[stable orthogonal group]]
to the [[stable homotopy groups of spheres]]. This is called
the **J-homomorphism**.

=--


### On classifying spaces

+-- {: .num_remark #DeloopedJ}
###### Remark

Since the mas of def. \ref{OrthogonalActionOnSphereOnHomotopyGroups}
are [[∞-group]] [[homomorphisms]], there exists their [[delooping]]

$$
  B J \;\colon\; B O \longrightarrow B GL_1(\mathbb{S}) = B H
  \,.
$$

=--

Here $GL_1(\mathbb{S})$ is the [[∞-group of units]] of the [[sphere spectrum]].

This map $B J$ is the [[universal characteristic class]] of stable [[vector bundles]] with values in [[spherical fibrations]]:

+-- {: .num_defn #SphereBundleOfVectorBundle}
###### Definition

For $V \to X$ a [[vector bundle]], write $S^V$ for its [[fiber]]-wise [[one-point compactification]]. This is a [[spherical fibration]]. Write $\mathbb{S}^V$ for the $X$-[[parameterized spectrum]] which is fiberwise the [[suspension spectrum]] of $S^V$.

=--

It is immediate that:

+-- {: .num_prop}
###### Proposition

For $V \to X$ a [[vector bundle]] classified by a map $X \to B O$, 
the corresponding [[spherical fibration]] $\mathbb{S}^V$, def. \ref{SphereBundleOfVectorBundle}, is classified by $X \to B O \stackrel{B J}{\longrightarrow}$, def. \ref{DeloopedJ}.

=--


## **II)** The image of the J-homomorphism


### Explicit description

The following characterization of the [[image]] of the J-homomorphism on [[homotopy groups]] derives from a statement that was first conjectured in ([Adams 66](#Adams66)) -- and since called the _[[Adams conjecture]]_ -- and then proven in ([Quillen 71](#Quillen71), [Sullivan 74](#Sullivan74)).

+-- {: .num_remark}
###### Remark

By the discussion at _[orthogonal group -- homotopy groups](orthogonal%20group#HomotopyGroups)_ we have that the [[homotopy groups]] of the [[stable orthogonal group]] are 

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| $\pi_n(O)$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ |0 | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ |

Because all groups appearing here and in the following are [[cyclic groups]], we instead write down the [[order of a group|order]]

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| ${\vert\pi_n(O)\vert}$ | 2 | 2 | 1 | $\infty$ | 1 | 1 | 1 | $\infty$ |

=--

For the following statement it is convenient to restrict to J-homomorphism to the stable [[special orthogonal group]] $S O$, which removes the lowest degree homotopy group in the above

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| $\pi_n(S O)$ | 0 | $\mathbb{Z}_2$ |0 | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ |

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| ${\vert\pi_n(S O)\vert}$ | 1 | 2 | 1 | $\infty$ | 1 | 1 | 1 | $\infty$ |


+-- {: .num_theorem #AdamsQuillenTheorem}
###### Theorem

The [[stable homotopy groups of spheres]] $\pi_n(\mathbb{S})$ are the [[direct sum]] of the ([[cyclic group|cyclic]]) [[image]] 
$im(J|_{SO})$ of the J-homomorphism, def. \ref{JHom}, applied to the [[special orthogonal group]] and the [[kernel]] of the [[Adams e-invariant]].

Moreover,

* for $n = 0 \;mod \;$ and $n = 1 \;mod \; 8$ and $n$ positive the J-homomorphism $\pi_n(J) \colon \pi_n(S O) \to \pi_n(\mathbb{S})$ is [[injection|injective]], hence its image is $\mathbb{Z}_2$, 

* for $n = 3\; mod\; 8$ and $n = 7 \; mod \; 8$ hence for $n = 4 k -1$, the [[order of a group|order]] of the image is equal to the [[denominator]] of $B_{2k}/4k$ in its reduced form, where $B_{2k}$ is the [[Bernoulli number]]

* for all other cases the image is necessarily zero.

=--

The characterization of the image is due to ([Adams 66](#Adams66), [Quillen 71](#Quillen71), [Sullivan 74](#Sullivan74)). 
Specifically the identification of $J(\pi_{4n-1}(S O))$ is ([Adams 65a, theorem 3.7](#Adams65a) and the diract summand property is ([Adams 66, theorems 1.1-1.6.](#Adams66)).
That the image is a direct summand of the codomain is proven for instance in ([Switzer 75, end of chapter 19](#Switzer75)). 

A modern version of the proof, using methods from [[chromatic homotopy theory]], is surveyed in some detail in ([Lorman 13](#Lorman13)).

The statement of the theorem is recalled for instance as ([Ravenel, chapter 1, theorem 1.1.13](#RavenelCh1)). 
Another computation of the image of $J$ is in ([Ravenel, chapter 5, section 3](#RavenelChapter5)).

+-- {: .num_remark}
###### Remark

The order of $J(\pi_{4k-1} O)$ in theorem \ref{AdamsQuillenTheorem} 
is for low $k$ given by the following table

| k | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| $\vert J(\pi_{4k-1}(O))\vert$ | 24 | 240 | 504 | 480 | 264 | 65,520 | 24 | 16,320 | 28,728 | 13,200 |

=--

See for instance ([Ravenel, Chapt. 1,  p. 5](#RavenelCh1)).


+-- {: .num_remark}
###### Remark

Therefore we have in low degree the following situation

[[!include image of J -- table]]

=--

The following tables show the [[p-primary components]] of the [[stable homotopy groups of spheres]] for low values, the image of J appears as the bottom row. 

Here the horizontal index is the degree $n$ of the stable homotopy group $\pi_n$. The appearance of a string of $k$ connected dots vertically above index $n$ means that there is a [[direct sum|direct summand]] [[primary group]] of [[order of a group|order]] $p^k$. See example \ref{InterpretTable} below for illustration.

(The tables are taken from ([Hatcher](#Hatcher)), where in turn were they were generated based on ([Ravenel 86](#RavenelCh1)).


**at $p = 2$**

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D2pic.gif" alt="stable homotopy groups of spheres at 2" />

**at $p = 3$**

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D3pic.gif" alt="stable homotopy groups of spheres at 3" />

**at $p = 5$**


<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D5pic.gif" alt="stable homotopy groups of spheres at 5" />

+-- {: .num_example #InterpretTable}
###### Example


The [[finite abelian group]] $\pi_3(\mathbb{S}) \simeq \mathbb{Z}_{24}$ decomposes into [[primary groups]] as $\simeq \mathbb{Z}_8 \oplus \mathbb{Z}_3$. Here $8 = 2^3$ corresponds to the three dots above $n = 3$ in the first table, and $3 = 3^1$ to the single dot over $n = 3$ in the second.

The [[finite abelian group]] $\pi_7(\mathbb{S}) \simeq \mathbb{Z}_{24}$ decomposes into [[primary groups]] as $\simeq \mathbb{Z}_{16} \oplus \mathbb{Z}_3 \oplus \mathbb{Z}_5$. Here $16 = 2^4$ corresponds to the four dots above $n = 7$ in the first table, and $3 = 3^1$ to the single dot over $n = 7$ in the second and $5 = 5^1$ to the single dot over $n = 7$ in the third table.


=--

### Chromatic formulation

The above tables suggest that the image of the J-homomorphism is 
in some sense the "lowest order layer" of the [[stable homotopy groups of spheres]]. This is made precise by the following characterization of the image in [[stable homotopy theory]]. We bluntly state this here and give all the relevant definitions [below](#ELocalStableHomotopyTheory).

$\,$

Write $E(1)$ for the first [[Morava E-theory]] [[spectrum]] at given [[prime number]] $p$. Write
$L_{E(1)}\mathbb{S}$ for the [[Bousfield localization of spectra]] of the [[sphere spectrum]] at $E(1)$.

+-- {: .num_theorem }
###### Theorem

The [[homotopy groups]] of the $E(1)$-localized sphere spectrum are

$$
  \pi_n L_{E(1)} \mathbb{S}
  \simeq
  \left\{
    \array{
      \mathbb{Z} & if\; n = 0
       \\
       \mathbb{Q}_p/\mathbb{Z}_p & if\; n= -2
       \\
       \mathbb{Z}/p^{k+1}\mathbb{Z} & if\; n+1 = (p-1)p^k m \;with\; m \neq 0\;mod\;p
        \\
        0 & otherwise
    }
  \right.
  \,.
$$

=--

This appears as ([Lurie 10, theorem 6](#LurieLecture))


+-- {: .num_defn }
###### Definition

Write $\mathbb{S}_p$ for the [[p-localization]] of the [[sphere spectrum]].
For $n \in \mathbb{Z}$, write $im(J)_n$ for the [[image]] of the $p$-localized J-homomorphism 

$$
  J \;\colon\; \pi_n(O) \longrightarrow \pi_n(\mathbb{S}) \longrightarrow \pi_n(\mathbb{S}_{(p)})
  \,.
$$

=--

+-- {: .num_theorem }
###### Theorem

For $n \in \mathbb{N}$, the further [[Bousfield localization]] at [[Morava E-theory|Morava E(1)-theory]]  $\mathbb{S}_{(p)} \longrightarrow L_{E(1)}\mathbb{S}$ induces a [[isomorphism]]

$$
  im(J)_n \stackrel{\simeq}{\longrightarrow} \pi_n (L_{E(1)} \mathbb{S})
$$

between the image of the $J$-homomorphism and the $E(1)$-local [[stable homotopy groups of spheres]].

=--

In this form this appears as ([Lurie 10, theorem 7](#LurieLecture)). See also ([Behrens 13, section 1](#Behrens13)).

+-- {: .num_cor }
###### Corollary

The $E(1)$-[[Bousfield localization of spectra|localization map]] is surjective on non-negative homotopy groups:

$$
  \pi_n(\mathbb{S}_{(p)}) \longrightarrow \pi_n(L_{E(1)} \mathbb{S})
  \,.
$$

=--


For review see also ([Lorman 13](#Lorman13)). That $J$ factors through $L_{K(1)}\mathbb{S}$ is in ([Lorman 13, p. 4](#Lorman13))

+-- {: .num_remark }
###### Remark

Hence: the image of $J$ is essentially the first [[chromatic layer]] of the [[sphere spectrum]].

=--



## **III)** $E$-Local stable homotopy theory
 {#ELocalStableHomotopyTheory}


### Bousfield localization of spectra

_Bousfield localization of spectra_ refers generally to [[localization of an (∞,1)-category|localizations]] of the [[stable (∞,1)-category of spectra]] or else to its presentation by  [[Bousfield localization of model categories|Bousfield localization]] of the [[stable model category]] of [[spectra]]. 

Specifically, for $E \in Spec$ a [[spectrum]], the _Bousfield localization at $E$_ of another [[spectrum]] $X$ is the [[universal property|universal map]]

$$
  X \longrightarrow L_E X
$$

to the _$E$-local spectrum_ $L_E X$, with the property that for $Y$ any $E$-acyclic spectrum in that $Y \wedge E \simeq 0$, every morphism $Y \longrightarrow L_E X$ is null-homotopic (a [[zero morphism]] in the [[stable (∞,1)-category of spectra]]). (see for instance [Lurie 10, Example 4](#LurieLecture))

For $E = H \mathbb{Z}_p$ the [[Eilenberg-MacLane spectrum]] of the [[cyclic group]] $\mathbb{Z}_p \coloneqq \mathbb{Z}/p\mathbb{Z}$ for some [[prime number]] $p$, this $E$-localization is _[[p-localization]]_. (see for instance [Lurie 10, Examples 7 and 8](#LurieLecture))

Example:

For $p$ a [[prime number]], a **$p$-local** [[topological space]] or rather  [[homotopy type]] or [[spectrum]] $X$ is one whose [[homotopy groups]] 

* admit the [[structure]] of [[modules]] over the $p$-[[localization of a ring|localized ring]] of [[integers]]  $\mathbb{Z}[p^{-1}]$;

equivalently:

* are such that the [[tensor product]] with the $p$-[[cyclic group]] vanishes: $\pi_\bullet(X) \otimes \mathbb{Z}/p\mathbb{Z} \simeq 0$.

The _$p$-localization_ is the [[localization]] that makes the $p$-local homotopy types/spectra be the [[local objects]]. 

Specifically for [[spectra]] this is the [[Bousfield localization of spectra]] at the [[Eilenberg-MacLane spectrum]] $H \mathbb{Z}_p$ for the [[cyclic group]].

### Chromatic layers

Choose

* $k$ be a [[perfect field]] of [[characteristic]] $p$;

* $f$ be a [[formal group]] of [[height of a formal group|height]] $n$ over $k$.

Write

$$
  R \coloneqq W(k)[ [ v_1, \cdots, v_{n-1} ] ]
$$

for the [[Lubin-Tate ring]] of $f$, classifying its universal deformation.

By the discussion there, this is [[Landweber exactness|Landweber exact]], hence defines a [[cohomology theory]]. Therefore by the [[Landweber exact functor theorem]] there is an [[even periodic cohomology theory]] $E(n)^\bullet$ [[Brown representability theorem|represented by]] a [[spectrum]] $E(n)$ with the property that its [[homotopy groups]] are

$$
  \pi_\bullet(E(n))
  \simeq
  W(k)[ [v_1, \cdots, v_{n-1} ] ] [ \beta^{\pm 1} ]
$$

for $\beta$ of degree 2. This is called alternatively $n$th _Morava E-theory_, or _[[Lubin-Tate theory]]_ or _[[Johnson-Wilson theory]]_.

(e.g. [Lurie, lect 22](#LurieLect22))

For each [[prime]] $p \in \mathbb{N}$ and for each [[natural number]]  $n \in \mathbb{N}$ there is a [[Bousfield localization of spectra]]

$$
  L_n \coloneqq L_{E(n)}
  \,,
$$

where $E(n)$ is the $n$th [[Morava E-theory]] (for the given [[prime]] $p$). These arrange into the _chromatic tower_ which for each spectrum $X$ is of the form

$$  
  X \to \cdots \to L_n X \to L_{n-1} X \to \cdots \to L_0 X
  \,.
$$

The [[homotopy fibers]] of each stage of the tower

$$
  M_n(X) \coloneqq fib(L_{E(n)}X \longrightarrow L_{E(n-1)}(X))
$$

is called the $n$th _monochromatic layer_ of $X$.



## **IV)** Adams spectral sequence for $E$-local homotopy groups

We discuss the general definition of $E$-[[Adams-Novikov spectral sequences]] for suitable [[E-∞ rings]] $E$ expressed in [[higher algebra]], as in ([Lurie, Higher Algebra](#LurieHigherAlgebra)). We follow the nice exposition in ([Wilson 13](#Wilson13)).

First we recall

* [Spectral sequences computing homotopy groups of filtered objects](#SpectralSequencesForHomotopyGroupsOfFilteredObjects)

for the general case of filtered objects in suitable [[stable (∞,1)-categories]]. Then we consider the specialization of that to the

* [Homotopy groups of cosimplicial totalizations filtered by coskeleta](#HomotopyGroupsOfOfTotalizationsFilteredByCoskeleta).

Finally we consider specifically the examples of such given by

* [Canonical cosimplicial resolutions of E-∞ algebras](#CanonicalCosimplicialResolutionOfEInfinityAlgebras).

In conclusion this yields for each suitable [[E-∞ algebra]] $E$ over $S$  and $S$-[[∞-module]] $X$ a [[spectral sequence]] converging to the [[homotopy groups]] of the $E$-[[Bousfield localization of spectra|localization]] of $X$, and this is

* [The E-Adams-Novikov spectral sequence](#TheEAdamsSpectralSequence).


### Spectral sequences computing homotopy groups of filtered objects
 {#SpectralSequencesForHomotopyGroupsOfFilteredObjects}

Let thoughout $\mathcal{C}$ be a [[stable (∞,1)-category]] equipped with a [[t-structure]] such that its [[heart of a stable (∞,1)-category|heart]] is an [[abelian category]]. 

+-- {: .num_example}
###### Example

For instance 

* $\mathcal{C} = Spec$  the [[stable (∞,1)-category of spectra]]. 

=--

+-- {: .num_defn #GeneralizedFilteredObject}
###### Definition

A _generalized [[filtered object]]_ in $\mathcal{C}$ is
simply a sequential diagram $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n+1} \to X_n \to X_{n-1} \to \cdots
  \,.
$$

Or rather, the object being filtered is the [[homotopy limit]]

$$
  X \coloneqq \underset{\leftarrow}{\lim}_n X_n
$$

and the sequential diagram exhibits the filtering.

=--

This appears as ([[Higher Algebra|Higher Algebra, def. 1.2.2.9]]).


+-- {: .num_defn #ExactCoupleForFilteredObject}
###### Definition

For a generalized filtered object $X_\bullet$, def. \ref{GeneralizedFilteredObject}, write 

$$
  F_n \coloneqq fib(X_n \to X_{n+1})
$$

for the [[homotopy fiber]] of the $n$th structure map, for all $n \in \mathbb{Z}$, and define an [[exact couple]]

$$
  \array{
    && \pi_\bullet(F_\bullet)
    \\
    & \swarrow && \nwarrow
    \\
    \pi_\bullet(X_\bullet)
    && 
       \stackrel{}{\longrightarrow}
    && 
    \pi_\bullet(X_\bullet)
  }
$$

where the maps are given by the [[long exact sequences of homotopy groups]]

$$
  \cdots
  \to
  \pi_\bullet(X_{n+1})
  \to 
  \pi_\bullet(F_n) \to  \pi_\bullet(X_n) \to \pi_\bullet(X_{n+1}) \to \pi_{\bullet+1}(F_n) \to \cdots
$$

=--

We now have the [[spectral sequence of a filtered stable homotopy type]].

+-- {: .num_prop #FiltrationSpectralSequence}
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]] equipped with a [[t-structure]] such that its [[heart of a stable (∞,1)-category|heart]] is an [[abelian category]]. 

If $\mathcal{C}$ has [[sequential limits]] and if  $X_n \simeq 0$ for all $n \gt n_0$ then the [[spectral sequence]] induced by the [[exact couple]]
of def. \ref{ExactCoupleForFilteredObject} converges to the [[homotopy groups]] of the [[homotopy limit]] $\underset{\leftarrow}{\lim}_n X_n$ of the generalized filted object:

$$
  E^{p,q}_1
  =
  \pi_{p+q} F_{p-1}
  \Rightarrow
  \pi_{p+q} (\underset{\leftarrow}{\lim} X_\bullet) 
$$

=--

This is due to ([[Higher Algebra|Higher Algebra, prop. 1.2.2.14]]). Review is in [Wilson 13, theorem 1.2.1](#Wilson13).

For the traditional statement in the [[category of chain complexes]] see at _[[spectral sequence of a filtered complex]]_.


### Homotopy groups of cosimplicial totalizations filtered by coskeleta
 {#HomotopyGroupsOfOfTotalizationsFilteredByCoskeleta}

+-- {: .num_defn #FiltrationOfTotalizationByTotalizationOfCoskeleta}
###### Definition

Given an [[cosimplicial object]] 

$$
  Y \;\colon\; \Delta  \longrightarrow \mathcal{C}
$$

its [[totalization]] $Tot Y \simeq \underset{\leftarrow}{\lim}_n Y_n$
is filtered, def. \ref{GeneralizedFilteredObject}, by the 
totalizations of its [[coskeleton|coskeleta]]

$$
  Tot Y 
  \to 
  \cdots 
  \to 
  Tot (cosk_2 Y) 
  \to
  Tot (cosk_1 Y) 
  \to
  Tot (cosk_0 Y) 
  \to 0
  \,.
$$

=--

+-- {: .num_prop #E2PageByMooreComplex}
###### Proposition

The filtration spectral sequence, prop. \ref{FiltrationSpectralSequence},
applied to the filtration of a [[totalization]] by [[coskeleton|coskeleta]] as in def. \ref{FiltrationOfTotalizationByTotalizationOfCoskeleta}, has as $E_2$-term the [[cohomology groups]] of the [[Moore complex]] associated with the cosimplicial object

$$
  E_2^{p,q}
  = 
  H^p(\pi_q(Tot (cosk_\bullet(Y))))
  \Rightarrow
  \pi_{p-q} Tot(Y)
  \,.
$$


=--

This is ([[Higher Algebra|Higher Algebra, remark 1.2.4.4]]). Review is around  ([Wilson 13, theorem 1.2.4](#Wilson13)).



### Canonical cosimplicial resolution of $E_\infty$-algebras
 {#CanonicalCosimplicialResolutionOfEInfinityAlgebras}

We discuss now the special case of coskeletally filtered 
totalizations coming from the canonical cosimplicial objects
induced from [[E-∞ algebras]] ("[[Sweedler corings]]").

In this form this appears as ([Lurie 10, theorem 2](#LurieLecture)). A review is in ([Wilson 13, 1.3](#Wilson13)). For the analog of this in the traditional formulation see ([Ravenel, ch. 3, prop. 3.1.2](#Ravenel)).



+-- {: .num_defn}
###### Definition

Let $S$ be an [[E-∞ ring]] and let $E$ be an [[E-∞ algebra]] over $S$, hence an [[E-∞ ring]] equipped with a [[homomorphism]]

$$
  S \longrightarrow E
  \,.
$$

The _canonical [[cosimplicial object]]_ 
associated to this (the "$\infty$-[[Sweedler coring]]") is that given by the iterated [[smash product]]/[[tensor product]] over $S$:

$$
  E^{\wedge^{\bullet+1}_S} \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

More generally, for $X$ an $S$-[[∞-module]], the canonical [[cosimplicial object]] is

$$
  E^{\wedge^{\bullet+1}_S}\wedge_S X \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

=--

+-- {: .num_prop #FlatnessCondition}
###### Proposition

If $E$ is such that the self-[[generalized homology]] 
$E_\bullet(E) \coloneqq \pi_\bullet(E \wedge_S E)$ (the dual $E$-[[Steenrod operations]]) is such that as a [[module]] over $E_\bullet \coloneqq \pi_\bullet(E)$ it is a [[flat module]], then there is a [[natural equivalence]]

$$
  \pi_\bullet
  \left(
    E^{\wedge^{n+1}_S}
    \wedge_S 
    X
  \right)
  \simeq
  E_\bullet(E^{\wedge^n_S})
  \otimes_{E_\bullet}
  E_\bullet(X)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This makes $(E_\bullet, E_\bullet(E))$ be the [[Hopf algebroid]]
formed by the  $E$-[[Steenrod algebra]]. See there for more on this.

=--

+-- {: .num_example}
###### Example

The condition in prop. \ref{FlatnessCondition} is
satisfied for 

* $E = H \mathbb{F}_p$ an [[Eilenberg-MacLane spectrum]] with $mod\;p$ [[coefficients]];

* $E = B P$ the [[Brown-Peterson spectrum]];

* $E = MU$ the [[complex cobordism cohomology theory|complec cobordism spectrum]].

It is NOT satisfied for

* $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]] for [[integer|integers]] [[coefficients]];

* $E = M S U$.

=--

+-- {: .num_remark #ExtGroupsByMooreComplex}
###### Remark

Under good conditions (...), $\pi_\bullet$ of the canonical [[cosimplicial object]] provides a [[resolution]] of [[comodule]] [[tensor product]] and hence computes the [[Ext]]-groups over the [[Hopf algebroid]]:

$$
  H^p(\pi_q(Tot(cosk_\bullet(E^{\wedge^{\bullet+1}_S } \wedge_S X))))
  \simeq
  Ext^p_{E_\bullet(E)}(\Sigma^q E_\bullet, E_\bullet(X))
  \,.
$$

(...)

=--


+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

There is a canonical map

$$
  L_E X \stackrel{}{\longrightarrow} \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the [[totalization]].


=--

We consider now condition for this morphism to be an [[equivalence]].

+-- {: .num_defn #CoreOfARing}
###### Definition

For $R$ a [[ring]], its _core_ $c R$ is the [[equalizer]] in

$$
  c R 
    \longrightarrow 
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,.
$$

=--

+-- {: .num_prop #SufficientConditionsForTotalizationToBeELocalization}
###### Proposition

Let $E$ be a [[connective spectrum|connective]] [[E-∞ ring]] such that the core or $\pi_0(E)$, def. \ref{CoreOfARing} is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \matbb{Z}[J^{-1}]$;

* $\mathbb{Z}_n$ for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X \stackrel{\simeq}{\longrightarrow} 
  \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
  \,.
$$

=--


([Bousfield 79](#Bousfield79)).


### The $E$-Adams-Novikov spectral sequence
 {#TheEAdamsSpectralSequence}

Summing this up yields the general $E$-Adams(-Novikov) spectral sequence

+-- {: .num_cor}
###### Corollary

Let $E$ a [[connective spectrum|connective]] [[E-∞ ring]] 
that satisfies the conditions of prop. \ref{SufficientConditionsForTotalizationToBeELocalization}. 
Then by prop. \ref{FiltrationSpectralSequence} and prop. \ref{SufficientConditionsForTotalizationToBeELocalization} there is a strongly convergent multiplicative
[[spectral sequence]]

$$
  E^{p,q}_\bullet \Rightarrow \pi_{q-p} L_{c \pi_0 E} X
$$

converging to the [[homotopy groups]] of the  $ c \pi_0(E)$-[[Bousfield localization of spectra|localization]] of $X$. If moreover the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ is [[flat module|flat]] as a [[module]] over $E_\bullet$, then, by prop. \ref{E2PageByMooreComplex} and remark \ref{ExtGroupsByMooreComplex}, the $E_2$-term of this spectral sequence is given by the [[Ext]]-groups over the $E$-[[Steenrod algebra|Steenrod]] [[Hopf algebra]].

$$
  E^{p,q}_\bullet
  =
  Ext^p_{E_\bullet(E)}(\Sigma^q E_\bullet, E_\bullet X)
  \,.
$$


=--



## References

An introduction to the chromatic perspective on the homotopy groups of spheres and the image of $J$ is in:

* [[Mark Mahowald]], [[Doug Ravenel]], _Towards  a Global Understanding of the Homotopy Groups of Spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/global.pdf))

The bulk of the basic constructions is in

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, lecture notes (2010)
 {#LurieLecture}

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#LurieHigherAlgebra}


Recent surveys of the modern picture are in

* [Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/conferences/talbot/), _[2013 Pre-Talbot Seminar Chromatic homotopy theoy](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php?pageID=links)_

  * [[Mark Behrens]], section 1 of Introduction talk at _[Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/conferences/talbot/index.php?year=2013&sub=talks)_ ([pdf](http://math.mit.edu/conferences/talbot/2013/1-Behrens-intro.pdf), [pdf](http://math.mit.edu/conferences/talbot/2013/Behrens-Introduction-chromatic-homotopy-thy-4-22-13.pdf))
 {#Behrens13}


  * [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the
Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php) ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}
  * Ben Knudsen, _First chromatic layer of the sphere spectrum = homotopy of the $K(1)$-local sphere_, talk at _[2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php)_ ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-04-04-Rob-Legg-K1-local-sphere.pdf))
 {#Knudsen13}

  * [[Vitaly Lorman]], _Chromatic homotopy theory at height 1 and the
image of $J$_, talk at _[Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/conferences/talbot/index.php?year=2013&sub=talks)_ ([pdf](http://math.mit.edu/conferences/talbot/2013/Image%20of%20J-1.pdf))
 {#Lorman13}

Loads of details for computations in the Adams spectral sequence are in

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_