
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

> This entry explains the [[J-homomorphism]], states how its image is the first ([[chromatic layer|chromatic]]) layer of the [[sphere spectrum]]; and then  motivated by this explains some basic notions of [[chromatic homotopy theory]], notably the origin of the general $E$-[[Adams spectral sequence]].



#Contents#
* table of contents
{:toc}


## **I)** The J-homomorphism

The _[[J-homomorphism]]_ is a map from the [[homotopy groups]] of the [[stable orthogonal group]] (which are completely understood) to the [[stable homotopy groups of spheres]] (which in their totality are hard to compute). 

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
the **[[J-homomorphism]]**.

=--


### On classifying spaces

+-- {: .num_remark #DeloopedJ}
###### Remark

Since the maps of def. \ref{OrthogonalActionOnSphereOnHomotopyGroups}
are [[∞-group]] [[homomorphisms]], there exists their [[delooping]]

$$
  B J \;\colon\; B O \longrightarrow B GL_1(\mathbb{S}) = B H
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

Here $GL_1(\mathbb{S})$ is the [[∞-group of units]] of the [[sphere spectrum]].

=--

This map $B J$ is the [[universal characteristic class]] of stable [[vector bundles]] with values in [[spherical fibrations]]:

+-- {: .num_defn #SphereBundleOfVectorBundle}
###### Definition

For $V \to X$ a [[vector bundle]], write $S^V$ for its [[fiber]]-wise [[one-point compactification]]. This is a [[sphere bundle]], a [[spherical fibration]]. Write $\mathbb{S}^V$ for the $X$-[[parameterized spectrum]] which is fiberwise the [[suspension spectrum]] of $S^V$.

=--

It is immediate that:

+-- {: .num_prop}
###### Proposition

For $V \to X$ a [[vector bundle]] classified by a map $X \to B O$, 
the corresponding [[spherical fibration]] $\mathbb{S}^V$, def. \ref{SphereBundleOfVectorBundle}, is classified by $X \to B O \stackrel{B J}{\longrightarrow} B GL_1(\mathbb{S})$, def. \ref{DeloopedJ}.

=--


## **II)** The image of the J-homomorphism

Since the [[J-homomorphism]] maps from something well-understood to something hard to understand, it is of interst to characterize its [[image]], "the [[image of J]]".

### Explicit description

The following characterization of the [[image]] of the J-homomorphism on [[homotopy groups]] derives from a statement that was first conjectured in ([Adams 66](Adams+spectrals+sequence#Adams66)) -- and since called the _[[Adams conjecture]]_ -- and then proven in ([Quillen 71](Adams+spectrals+sequence#Quillen71), [Sullivan 74](Adams+spectrals+sequence#Sullivan74)).

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

The characterization of this image is due to ([Adams 66](Adams+spectrals+sequence#Adams66), [Quillen 71](Adams+spectrals+sequence#Quillen71), [Sullivan 74](Adams+spectrals+sequence#Sullivan74)). 
Specifically the identification of $J(\pi_{4n-1}(S O))$ is ([Adams 65a, theorem 3.7](Adams+spectrals+sequence#Adams65a) and the direct summand property is ([Adams 66, theorems 1.1-1.6.](Adams+spectrals+sequence#Adams66)).
That the image is a direct summand of the codomain is proven for instance in ([Switzer 75, end of chapter 19](Adams+spectrals+sequence#Switzer75)). 

A modern version of the proof, using methods from [[chromatic homotopy theory]], is surveyed in some detail in ([Lorman 13](#Lorman13)).

The statement of the theorem is recalled for instance as ([Ravenel, chapter 1, theorem 1.1.13](#Ravenel)). 
Another computation of the image of $J$ is in ([Ravenel, chapter 5, section 3](#Ravenel)).

+-- {: .num_remark}
###### Remark

The order of $J(\pi_{4k-1} O)$ in theorem \ref{AdamsQuillenTheorem} 
is for low $k$ given by the following table

| k | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| $\vert J(\pi_{4k-1}(O))\vert$ | 24 | 240 | 504 | 480 | 264 | 65,520 | 24 | 16,320 | 28,728 | 13,200 |

=--

See for instance ([Ravenel, Chapt. 1,  p. 5](#Ravenel)).


+-- {: .num_remark}
###### Remark

Therefore we have in low degree the following situation

[[!include image of J -- table]]

=--


+-- {: .num_example #TableOfPPrincipalComponentsInHomotopyGroups}
###### Example

The following tables show the [[p-primary components]] of the [[stable homotopy groups of spheres]] for low values, the image of J appears as the bottom row. 

Here the horizontal index is the degree $n$ of the stable homotopy group $\pi_n$. The appearance of a string of $k$ connected dots vertically above index $n$ means that there is a [[direct sum|direct summand]] [[primary group]] of [[order of a group|order]] $p^k$. See example \ref{InterpretTable} below for illustration. (These tables are taken from ([Hatcher](homotopy+groups+of+spheres#Hatcher)), where in turn they were generated based on ([Ravenel 86](#Ravenel))).


**$p = 2$-primary component** (e.g. [Ravenel 86, theorem 3.2.11, figure 4.4.46](#Ravenel))

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D2pic.gif" alt="stable homotopy groups of spheres at 2" />

**$p = 3$-primary component**

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D3pic.gif" alt="stable homotopy groups of spheres at 3" />

**$p = 5$-primary component**

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D5pic.gif" alt="stable homotopy groups of spheres at 5" />

=--

We illustrate how to read these tables:

+-- {: .num_example #InterpretTable}
###### Example


The [[finite abelian group]] $\pi_3(\mathbb{S}) \simeq \mathbb{Z}_{24}$ decomposes into [[primary groups]] as $\simeq \mathbb{Z}_8 \oplus \mathbb{Z}_3$. Here $8 = 2^3$ corresponds to the three dots above $n = 3$ in the first table, and $3 = 3^1$ to the single dot over $n = 3$ in the second.

The [[finite abelian group]] $\pi_7(\mathbb{S}) \simeq \mathbb{Z}_{240}$ decomposes into [[primary groups]] as $\simeq \mathbb{Z}_{16} \oplus \mathbb{Z}_3 \oplus \mathbb{Z}_5$. Here $16 = 2^4$ corresponds to the four dots above $n = 7$ in the first table, and $3 = 3^1$ to the single dot over $n = 7$ in the second and $5 = 5^1$ to the single dot over $n = 7$ in the third table.

The [[finite abelian group]] $\pi_11(\mathbb{S}) \simeq \mathbb{Z}_{504}$ has [[primary group]]-decomposition $\cdots \simeq \mathbb{Z}_{2^3} \oplus \mathbb{Z}_{3^2} \oplus \mathbb{Z}_7$ and so this corresponds to the three connected dots over $n = 11$ in the first table and the two connected dots over $n = 11$ in the second (and there will be one dot over $n = 11$ in the fourth table for $p = 7$ not shown here). 

The groups $\pi_1(\mathbb{S}) \simeq \pi_2(\mathbb{S}) \simeq \pi_6(\mathbb{S}) \simeq \pi_{10}(\mathbb{S}) \simeq \mathbb{Z}_2$ correspond to the single dots over $n = 1,2,6,10$ in the first table, respectively.

The group $\pi_8(\mathbb{S}) \simeq \mathbb{Z}_2 \oplus \mathbb{Z}_2$ corresponds to the two _unconnected_ dots over $n = 8$ in the first table.

Similarly the group $\pi_9(\mathbb{S}) \simeq \mathbb{Z}_2 \oplus \mathbb{Z}_2 \oplus \mathbb{Z}_2$ corresponds to the three unconnected dots above $n = 9$ in the first table.

=--

### Chromatic formulation

The above tables, example \ref{TableOfPPrincipalComponentsInHomotopyGroups}, suggest that the [[image of the J-homomorphism]] is 
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
       \mathbb{Z}_{p^{k+1}} & if\; n+1 = (p-1)p^k m \;with\; m \neq 0\;mod\;p
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

To say what all this means, we recall now [[Bousfield localization of spectra]] and then indicate the tower of localizations at the [[Morava E-theory]] spectra,  the "[[chromatic filtration]]".

### Bousfield localization of spectra


+-- {: .num_defn #AcyclicAndLocal}
###### Definition

Let $E \in Spec$ be a [[spectrum]]. 

Say that another spectrum
$X \in Spec$ is an **$E$-acyclic spectrum** if the [[smash product]]
is [[zero object|zero]], $E \wedge X \simeq 0$.

Say that $X$ is an **$E$-local spectrum** if every [[morphism]]
$Y \longrightarrow X$ out of an $E$-acyclic spectrum $Y$ is homotopic to the [[zero morphism]]. 

Say that a morphism $f \colon X \to Y$ is an **$E$-equivalence** if it becomes an [[equivalence]] after [[smash product]] with $E$.

=--

(e.g. [Lurie, Lecture 20, example 4](#LurieLecture))

+-- {: .num_prop #LocalizationCofiber}
###### Proposition

For $E$ a [[spectrum]], every other spectrum sits in an essentially unique [[homotopy cofiber sequence]]

$$
  G_E(X) \to X \to L_E(X)
  \,,
$$

where $G_E(X)$ is $E$-acyclic, and $L_E(X)$ is $E$-local, def. \ref{AcyclicAndLocal}.

Here $X \to L_E (X)$ is characterized by two properties

1. $L_E(X)$ is $E$-local;

1. $X \to L_E(X)$ is an $E$-equivalence

according to def. \ref{AcyclicAndLocal}.

=--

(e.g. [Lurie, Lecture 20, example 4](#LurieLecture))

+-- {: .num_defn}
###### Definition

Given $E \in Spec$, 
the [[natural transformation|natural morphisms]] $X \longrightarrow L_E X$
in prop. \ref{LocalizationCofiber} exhibit the [[localization of an (infinity,1)-category]] called **Bousfield localization** at $E$.

=--

+-- {: .num_example #EModulesAreELocal}
###### Example

For $E$ an [[E-∞ ring]], every [[∞-module]] $X$ over $E$ is $E$-local, def. \ref{AcyclicAndLocal}.

=--

(e.g. [Lurie, Lecture 20, example 5](#LurieLecture))

+-- {: .num_example}
###### Example

For $E$ an [[E-∞ algebra]] over an [[E-∞ ring]] $S$ and for $X$ an $S$-[[∞-module]], consider the dual [[Cech nerve]] [[cosimplicial object]]

$$
  E^{\wedge_S^{\bullet+1}}\wedge_S X \;\colon\; \Delta \longrightarrow Spectra
  \,.
$$

By example \ref{EModulesAreELocal} each term is $E$-local, so that the map  to the  [[totalization]]

$$
  X \longrightarrow \underset{\leftarrow}{\lim} E^{\wedge_S^{\bullet+1}} \wedge_S X
$$

factors through the $E$-localization of $X$

$$
  X \longrightarrow 
  L_E X
  \longrightarrow
  \underset{\leftarrow}{\lim} E^{\wedge_S^{\bullet+1}} \wedge_S X
  \,.
$$

Under suitable condition the second map here is indeed an [[equivalence]], in which case the [[totalization]] of the dual [[Cech nerve]] exhibits the $E$-localization. This happens for instance in the discussion of the [[Adams spectral sequence]], see the examples given there.

=--

+-- {: .num_example}
###### Example

For $p \in \mathbb{N}$ a [[prime number]], let 

$$
  E \coloneqq H \mathbb{Z}/p\mathbb{Z}
$$ 

be the corresponding [[Eilenberg-MacLane spectrum]]. Then a spectrum which corresponds to a [[chain complex]] under the [stable Dold-Kan corespondence](module+spectrum#StableDoldKanCorrespondence) is $E$-local, def. \ref{AcyclicAndLocal}, if that chain complex has [[chain homology]] groups being $\mathbb{Z}[p^{-1}]$-modules.

The $E$-localization of a spectrum in this case is called _[[p-localization]]_.

=--

(e.g. [Lurie, Lecture 20, example 8](#LurieLecture))



### Chromatic layers

Let

* $k$ be a [[perfect field]] of [[characteristic]] $p$;

* $f$ be a [[formal group]] of [[height of a formal group|height]] $n$ over $k$.


+-- {: .num_defn}
###### Definition

Write $W(k)$ for the [[ring of Witt vectors]]. Write 

$$
  R \coloneqq W(k)[ [ v_1, \cdots, v_{n-1} ] ]
$$

for the ring of [[formal power series]] over this ring, in $n-1$ [[variables]]; called the _[[Lubin-Tate ring]]_.

=--


+-- {: .num_theorem}
###### Theorem

The [[Lubin-Tate formal group]] $\overline{f}$ is the [[universal property|universal]] deformation of $f$ in that for every [[infinitesimal object|infinitesimal thickening]] $A$ of $k$, $\overline{f}$ induces a [[bijection]]

$$
  Hom_{/k}(R,A) \stackrel{\simeq}{\longrightarrow} Def(A)
$$

between the $k$-[[associative algebra|algebra]]-[[homomorphisms]] from $R$ into $A$ and the [[deformations]] of $A$.

=--

(e.g. [Lurie 10, lect 21, theorem 5](#LurieLecture))


By the discussion there, this is [[Landweber exactness|Landweber exact]], hence defines a [[cohomology theory]]. Therefore by the [[Landweber exact functor theorem]] there is an [[even periodic cohomology theory]] $E(n)^\bullet$ [[Brown representability theorem|represented by]] a [[spectrum]] $E(n)$ with the property that its [[homotopy groups]] are

$$
  \pi_\bullet(E(n))
  \simeq
  W(k)[ [v_1, \cdots, v_{n-1} ] ] [ \beta^{\pm 1} ]
$$

for $\beta$ of degree 2. This is called alternatively $n$th _[[Morava E-theory]]_, or _[[Lubin-Tate theory]]_ or _[[Johnson-Wilson theory]]_.

(e.g. [Lurie, lect 22](#LurieLecture))

For each [[prime]] $p \in \mathbb{N}$ and for each [[natural number]]  $n \in \mathbb{N}$ there is a [[Bousfield localization of spectra]]

$$
  L_n \coloneqq L_{E(n)}
  \,,
$$

where $E(n)$ is the $n$th [[Morava E-theory]] (for the given [[prime]] $p$), called the $n$th _[[chromatic localization]]_. These arrange into the _[[chromatic tower]]_ which for each spectrum $X$ is of the form

$$  
  X \to \cdots \to L_n X \to L_{n-1} X \to \cdots \to L_0 X
  \,.
$$

The [[homotopy fibers]] of each stage of the tower

$$
  M_n(X) \coloneqq fib(L_{E(n)}X \longrightarrow L_{E(n-1)}(X))
$$

is called the $n$th _[[monochromatic layer]]_ of $X$.


[[!include chromatic tower examples - table]]


## **IV)** Adams spectral sequence for $E$-local homotopy groups

Summing up the above, we need a means to compute [[homotopy groups]] of $E$-[[Bousfield localization of spectra|localized]] [[spectra]].
In ([Lurie, Higher Algebra, section 1.2.2](#LurieHigherAlgebra)) is given a general [[spectral sequence of a filtered stable homotopy type]] which computes homotopy groups of [[spectra]], and in ([Lurie 10, lectures 8 and 9](#LurieLecture)) is discussed that the [[totalization]] of the [[coskeleton]] filtration on the dual [[Cech nerve]] of an [[E-∞ algebra]] yields the $E$-localization. Taken together this is just what we need... and this is the general _$E$-[[Adams spectral sequence]]_. We follow the nice exposition in ([Wilson 13](#Wilson13)).

First we recall

* [Spectral sequences computing homotopy groups of filtered objects](#SpectralSequencesForHomotopyGroupsOfFilteredObjects)

for the general case of filtered objects in suitable [[stable (∞,1)-categories]]. Then we consider the specialization of that to the

* [Canonical cosimplicial resolutions of E-∞ algebras](#CanonicalCosimplicialResolutionOfEInfinityAlgebras).

In conclusion this yields for each suitable [[E-∞ algebra]] $E$ over $S$  and $S$-[[∞-module]] $X$ a [[spectral sequence]] converging to the [[homotopy groups]] of the $E$-[[Bousfield localization of spectra|localization]] of $X$, and this is

* [The E-Adams-Novikov spectral sequence](#TheEAdamsSpectralSequence).


### Spectral sequences for homotopy groups of filtered spectra
 {#SpectralSequencesForHomotopyGroupsOfFilteredObjects}

We discuss the [[spectral sequence of a filtered stable homotopy type]].

Let throughout $\mathcal{C}$ be a [[stable (∞,1)-category]], $\mathcal{A}$ an [[abelian category]], and $\pi \;\colon\; \mathcal{C}\longrightarrow \mathcal{A}$ a [[homological functor]] on $\mathcal{C}$, i.e., a functor that transforms every [[cofiber sequence]]

$$ X\to Y\to Z\to \Sigma X $$

in $\mathcal{C}$ into a long exact sequence

$$ \dots \to \pi(X)\to \pi(Y)\to \pi(Z)\to \pi(\Sigma X) \to \dots $$

in $\mathcal{A}$. We write $\pi_n=\pi\circ \Sigma^{-n}$.

+-- {: .num_example}
###### Example

* $\mathcal{C}$ is arbitrary, $\mathcal{A}$ is the category of [[abelian groups]] and $\pi$ is taking the 0th [[homotopy group]] $\pi_0 \mathcal{C}(S,-)$ of the [[mapping spectrum]] out of some [[object]] $S\in\mathcal{C}$

* $\mathcal{C}$ is equipped with a [[t-structure]], $\mathcal{A}$ is the [[heart of a stable (∞,1)-category|heart]] of the t-structure, and $\pi$ is the canonical functor.

* $\mathcal{C} = D(\mathcal{A})$ is the [[derived category]] of the abelian category $\mathcal{A}$ and $\pi=H_0$ is the degree-0  [[chain homology]] functor.

* Any of the above with $\mathcal{C}$ and $\mathcal{A}$ replaced by their [[opposite categories]].

=--

+-- {: .num_defn #GeneralizedFilteredObject}
###### Definition

A _[[filtered object in an (∞,1)-category]]_ in $\mathcal{C}$ is
simply a [[sequential diagram]] $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n-1} \to X_n \to X_{n+1} \to \cdots
  \,.
$$

=--

This appears as ([[Higher Algebra|Higher Algebra, def. 1.2.2.9]]).

We will take the view that the object being filtered is the [[homotopy limit]]

$$
  X \coloneqq \underset{\leftarrow}{\lim}_n X_n.
$$

We could also consider the sequential diagram as a filtering of its [[homotopy colimit]], but this is really an equivalent point of view since we can replace $\mathcal{C}$ by $\mathcal{C}^{op}$.


+-- {: .num_defn #ChainComplexInStableInfinityCategory}
###### Definition

Let $I$ be a [[linearly ordered set]]. An $I$-chain complex in a [[stable (∞,1)-category]] $\mathcal{C}$ is an [[(∞,1)-functor]]

$$
  F \;\colon\; I^{\Delta[1]} \longrightarrow \mathcal{C}
$$

such that 

1. for each $n \in I$, $F(n,n) \simeq 0$ is the [[zero object]];

1. for all $i \leq j \leq k$ the induced [[diagram]]

   $$
     \array{
        F(i,j) &\longrightarrow& F(i,k)
        \\
        \downarrow && \downarrow
        \\
        F(j,j) &\longrightarrow& F(j,k)
     }
   $$

   is a [[homotopy pullback]] square.

=--

This is [[Higher Algebra|Higher Algebra, def. 1.2.2.2]].


+-- {: .num_remark }
###### Remark

Given a $\mathbb{Z}$-chain complex $F$ in $\mathcal{C}$ as in def. \ref{ChainComplexInStableInfinityCategory}, 
setting

$$
  C_n \coloneqq \Sigma^{-n} F(n,n+1)
$$

and defining a [[differential]] induced from the [[connecting homomorphisms]] of the defining [[homotopy fiber sequences]]

$$
  F(n-1,n) \to F(n-1, n+1) \to F(n,n+1)
$$

yields an ordinary [[chain complex]] $C_\bullet$ in the [[homotopy category of an (∞,1)-category|homotopy category]].

=--

([[Higher Algebra|Higher Algebra, remark 1.2.2.3]])

+-- {: .num_prop #ChainComplexesFromFilteredObjects}
###### Proposition

Consider the inclusion of [[posets]]

$$
  (\mathbb{Z}, \leq)
  \to 
  (\mathbb{Z}\cup \{\infty\}, \leq)^{\Delta[1]} 
$$

given by

$$
  n \mapsto (n,\infty)
  \,.
$$

The induced [[(∞,1)-functor]]

$$
  Func((\mathbb{Z}\cup \{\infty\}, \leq)^{\Delta[1]} , \mathcal{C})
  \longrightarrow
  Func((\mathbb{Z}, \leq), \mathcal{C})
$$

restricts to an [[equivalence of (∞,1)-categories|equivalence]] between the (∞,1)-category of $\mathbb{Z}\cup \{\infty\}$-chain complexes in $\mathcal{C}$ (def. \ref{ChainComplexInStableInfinityCategory}) and that of generalized filtered objects in $\mathcal{C}$ (def. \ref{GeneralizedFilteredObject}).


=--

This is [[Higher Algebra|Higher Algebra, lemma 1.2.2.4]]. The inverse functor can be described informally as follows: given a filtered object $X_\bullet$, the associated chain complex $X(\bullet,\bullet)$ is given by

$$ X(n, n+r) = \operatorname{fib}(X_n\to X_{n+r}). $$

+-- {: .num_defn }
###### Definition

Let $X_\bullet$ be a filtered object in the sense of def. \ref{GeneralizedFilteredObject}. Write $X(\bullet,\bullet)$ for the corresponding chain complex, according to prop. \ref{ChainComplexesFromFilteredObjects}.

Then for all $i \leq j \leq k$ there is a [[long exact sequence of homotopy groups]] in $\mathcal{A}$ of the form

$$
  \cdots \to 
  \pi_n X(i,j) 
  \to 
  \pi_n X(i,k)
  \to 
  \pi_n X(j,k)
  \to
  \pi_{n-1}X(i,j)
  \to \cdots
  \,.
$$

Define then for $p,q \in \mathbb{Z}$ and $r \geq 1$ the object $E^r_{p,q}$ by the canonical [epi-mono factorization](abelian+category#FactorizationOfMorphisms)

$$
    \pi_{p} X(q-r+1,q+1)
    \twoheadrightarrow
    E^r_{p,q}
    \hookrightarrow
    \pi_{p} X(q, q+r)
$$

in the abelian category $\mathcal{A}$, and define the [[differential]]

$$
  d^r \;\colon\; E_{p,q}^r \to E_{p-1, q-r}^r
$$

to be the restriction of the [[connecting homomorphism]]

$$
 \pi_{p} X(q,q+r) \to \pi_{p-1} X(q-r, q)
$$

from the above long exact sequence (with $i=q-r$, $j=q$, and $k=q+r$).


=--


([[Higher Algebra|Higher Algebra, construction 1.2.2.6]])


+-- {: .num_prop}
###### Proposition

$d^r\circ d^r = 0$ and there are natural (in $X_\bullet$) isomorphisms

$$
E^{r+1}\cong \operatorname{ker}(d^r)/\operatorname{im}(d^r).
$$

Thus, $\{E^r_{*,*}\}_{r\geq 1}$ is a bigraded [[spectral sequence]]  in the [[abelian category]] $\mathcal{A}$, functorial in the filtered object $X_\bullet$, with

$$ E^1_{p,q} = \pi_p \operatorname{fib}(X_q\to X_{q+1}), \qquad d^r: E^r_{p,q}\to E^r_{p-1,q-r}. $$

=--

([[Higher Algebra|Higher Algebra, prop. 1.2.2.7]])

If [[sequential limits]] and [[sequential colimits]] exist in $\mathcal{A}$, we can form the limiting term $E^\infty_{*,*}$ of this spectral sequence.

On the other hand, the [[graded object]] $\pi_\bullet (X)$ admits a [[filtered object|filtration]] by

$$ F_q \pi_p (X) = \operatorname{ker}(\pi_p (X)\to \pi_p(X_q)) $$

and we would like to compare $E^\infty_{*,*}$ with the [[associated graded]] of this filtration. We say that 

+-- {: .num_defn #WeakAndStrongConvergence}
###### Definition

The spectral sequence **converges weakly** if there is a canonical isomorphism

$$ E^\infty_{p,q} \cong F_q\pi_p(X)/ F_{q-1}\pi_p(X) $$

for every $p,q\in\mathbb{Z}$. 

We say that the spectral sequence **converges strongly** if it converges weakly and if, in addition, the filtration $F_\bullet\pi_p(X)$ is complete on both sides.


=--

+-- {: .num_remark}
###### Remark

The meaning of the word *canonical* in def. \ref{WeakAndStrongConvergence} is somewhat subtle since, in general, there is no map from one side to the other. However, there always exists a canonical *[[relation]]* between the two, and we ask that this relation be an isomorphism (see [Hilton-Stammbach, VIII.7](#HiltonStammbach)).

=--


+-- {: .num_prop #FiltrationSpectralSequence}
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]] and let $\pi:\mathcal{C}\to\mathcal{A}$ be a homological functor where $\mathcal{A}$ is an [[abelian category]] which admits [[sequential limits]]. Let $X_\bullet$ be a filtered object in $\mathcal{C}$ such that $\underset{\leftarrow}{\lim} X_\bullet$ exists. Suppose further that:

1. For every $n$, the diagram $r\mapsto \operatorname{fib}(X_{n-r}\to X_n)$ has a limit in $\mathcal{C}$ and that limit is preserved by $\pi$.
2. For every $n$, $\pi_n(X_r)=0$ for $r\gg 0$.

Then the [[spectral sequence]] $\{E^r_{*,*}\}_{r\geq 1}$ in $\mathcal{A}$ converges strongly (def. \ref{WeakAndStrongConvergence}). We write:

$$
  E_{p,q}^1
  =
  \pi_{p} \operatorname{fib}(X_q\to X_{q+1})
  \Rightarrow
  \pi_{p} (\underset{\leftarrow}{\lim} X_\bullet) 
$$

=--

There is also a dual statement in which limits are replaced by colimits, but it is in fact a special case of the proposition with $\pi$ replaced by $\pi^{op}$. A proof of this proposition (in dual form) is given in ([[Higher Algebra|Higher Algebra, prop. 1.2.2.14]]). Review is in ([Wilson 13, theorem 1.2.1](#Wilson13)).

For the traditional statement in the [[category of chain complexes]] see at _[[spectral sequence of a filtered complex]]_.

Plenty of types of [[spectral sequences]] turn out to be special cases of this general construction.

[[!include Lurie spectral sequences -- table]]









### Canonical cosimplicial resolution of $E_\infty$-algebras
 {#CanonicalCosimplicialResolutionOfEInfinityAlgebras}

We discuss now the special case of coskeletally filtered 
totalizations coming from the canonical cosimplicial objects
induced from [[E-∞ algebras]] (dual [[Cech nerves]]/[[Sweedler corings]]/[[Amitsur complexes]]).

In this form this appears as ([Lurie 10, theorem 2](#LurieLecture)). A review is in ([Wilson 13, 1.3](#Wilson13)). For the analog of this in the traditional formulation see ([Ravenel, ch. 3, prop. 3.1.2](#Ravenel)).


+-- {: .num_defn #FiltrationOfTotalizationByTotalizationOfCoskeleta}
###### Definition

Given an [[cosimplicial object in an (∞,1)-category]]  with [[(∞,1)-colimits]]

$$
  Y \;\colon\; \Delta  \longrightarrow \mathcal{C}
$$

its [[totalization]] $Tot Y \simeq \underset{\leftarrow}{\lim}_n Y_n$
is [[filtered object in an (infinity,1)-category|filtered]], def. \ref{GeneralizedFilteredObject}, by the 
totalizations of its [[coskeleta]]

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

+-- {: .num_defn #SpectralSequenceOfSimplicialStableHomotopyType}
###### Definition

The [[spectral sequence of a filtered stable homotopy type|filtration spectral sequence]], prop. \ref{FiltrationSpectralSequence},
applied to the filtration of a [[totalization]] by [[coskeleton|coskeleta]] as in def. \ref{FiltrationOfTotalizationByTotalizationOfCoskeleta}, we call the _[[spectral sequence of a simplicial stable homotopy type]]_.

=--

([[Higher Algebra|Higher Algebra, prop. 1.2.4.5]])

+-- {: .num_prop #E2PageByMooreComplex}
###### Proposition

The [[spectral sequence of a simplicial stable homotopy type]] has as first page/$E_1$-term the [[cohomology groups]] of the [[Moore complex]] associated with the [[cosimplicial objects]] of [[homotopy groups]]

$$
  E_2^{p,q}
  = 
  H^p(\pi_q(Tot (cosk_\bullet(Y))))
  \Rightarrow
  \pi_{p-q} Tot(Y)
  \,.
$$

=--

By the discussion at _[[∞-Dold-Kan correspondence]]_ and _[[spectral sequence of a filtered stable homotopy type]]_. This appears as ([[Higher Algebra|Higher Algebra, remark 1.2.4.4]]). Review is around  ([Wilson 13, theorem 1.2.4](#Wilson13)).




+-- {: .num_defn}
###### Definition

Let $S$ be an [[E-∞ ring]] and let $E$ be an [[E-∞ algebra]] over $S$, hence an [[E-∞ ring]] equipped with a [[homomorphism]]

$$
  S \longrightarrow E
  \,.
$$

The _canonical [[cosimplicial object]]_ 
associated to this (the $\infty$-[[Cech nerve]]/[[Sweedler coring]]/[[Amitsur complex]]) is that given by the iterated [[smash product]]/[[tensor product]] over $S$:

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

Reviewed for instance as ([Wilson 13, prop. 1.3.1](#Wilson13)).

+-- {: .num_remark}
###### Remark

This makes $(E_\bullet, E_\bullet(E))$ be 
the [[commutative Hopf algebroid]]
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

Under good conditions (...), $\pi_\bullet$ of the canonical [[cosimplicial object]] provides a [[resolution]] of [[comodule]] [[tensor product]] and hence computes the [[Ext]]-groups over the [[commutative Hopf algebroid]]:

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

([Lurie 10, lecture 30, prop. 1](LurieLecture))


We consider now conditions for this morphism to be an [[equivalence]].

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


([Bousfield 79](Bousfield+localization+of+spectra#Bousfield79), [Lurie 10, lecture 30, prop. 3](LurieLecture), [Lurie 10, lecture 31, ](LurieLecture)).


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

converging to the [[homotopy groups]] of the  $ c \pi_0(E)$-[[Bousfield localization of spectra|localization]] of $X$. If moreover the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ is [[flat module|flat]] as a [[module]] over $E_\bullet$, then, by prop. \ref{E2PageByMooreComplex} and remark \ref{ExtGroupsByMooreComplex}, the $E_1$-term of this spectral sequence is given by the [[Ext]]-groups over the $E$-[[Steenrod algebra|Steenrod]] [[commutative Hopf algebroid|Hopf algebroid]].

$$
  E^{p,q}_\bullet
  =
  Ext^p_{E_\bullet(E)}(\Sigma^q E_\bullet, E_\bullet X)
  \,.
$$


=--



## References

An introduction to the chromatic perspective on the homotopy groups of spheres and the image of $J$ is in:

* [[Mark Mahowald]], [[Doug Ravenel]], _Towards  a Global Understanding of the Homotopy Groups of Spheres_, 1998 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/global.pdf))

The bulk of the basic constructions is in

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, lecture notes (2010)
 {#LurieLecture}

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#LurieHigherAlgebra}


Recent surveys of the modern picture are in

* [Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/events/talbot/), _[2013 Pre-Talbot Seminar Chromatic homotopy theoy](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php?pageID=links)_

and of relevance for the above discussion are particularly the following contributions there

* [[Mark Behrens]], section 1 of Introduction talk at _[Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/events/talbot/index.php?year=2013&sub=talks)_ ([pdf](http://math.mit.edu/events/talbot/2013/1-Behrens-intro.pdf), [pdf](http://math.mit.edu/events/talbot/2013/Behrens-Introduction-chromatic-homotopy-thy-4-22-13.pdf))
 {#Behrens13}


* [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the
Spectrum of the Category of Spectra_ lecture at _[2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php)_ ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}

* Ben Knudsen, _First chromatic layer of the sphere spectrum = homotopy of the $K(1)$-local sphere_, talk at _[2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php)_ ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-04-04-Rob-Legg-K1-local-sphere.pdf))
 {#Knudsen13}

* [[Vitaly Lorman]], _Chromatic homotopy theory at height 1 and the
image of $J$_, talk at _[Talbot 2013: Chromatic Homotopy Theory](https://math.mit.edu/events/talbot/index.php?year=2013&sub=talks)_ ([pdf](https://math.mit.edu/events/talbot/2013/Image%20of%20J-1.pdf))
 {#Lorman13}

Loads of details for computations in the Adams spectral sequence are in

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986
 {#Ravenel}