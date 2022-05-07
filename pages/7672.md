
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _$J$-homomorphism_ is traditionally a family of [[group]] [[homomorphisms]]

$$
  J_i \;\colon\; \pi_i(O(n)) \longrightarrow \pi_{n+i}(S^n)
$$

from the [[homotopy groups]] of (the [[topological space]] underlying) the [[orthogonal group]] to the [[homotopy groups of spheres]].
This refines to a morphism of [[∞-groups]]

$$
  J \;\colon\; O \longrightarrow GL_1(\mathbb{S})
$$

from the [[stable orthogonal group]] (regarded as a [[group object in an (∞,1)-category|group object]] in $L_{whe} Top \simeq$ [[∞Grpd]])
to the [[∞-group of units]] of the [[sphere spectrum]], regarded as an [[E-∞ ring spectrum]].

By postcomposition, the [[delooping]] of the J-homomorphism  

$$
  B J \;\colon\; B O \to B GL_1(\mathbb{S}) 
$$ 

sends real [[vector bundles]] to [[sphere bundles]], namely to [[(∞,1)-line bundles]] with typical [[fiber]] the [[sphere spectrum]] $\mathbb{S}$. See also at _[[Thom space]]_ for more on this.

The description of the image of the $J$-homomorphism in the [[stable homotopy groups of spheres]] was an important precursor to the development of [[chromatic homotopy theory]], which is used to explain the periodicities seen in the image of the J-homomorphism (see also [Lurie 10, remark 8](#Lurie)). See also at _[[periodicity theorem]]_.

## Definition

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

The [[∞-group]] $H(n)$, def. \ref{AutoequivalencesOfnSphere}, constitutes the two [[connected components]] of the $n$-fold based [[loop space]] $\Omega^n S^n$ corresponding to the [[homotopy classes]] $\pm 1 \in \pi_n(S^n)$.

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


### Delooped: On classifying spaces and K-theory classes

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

For $V \to X$ a [[vector bundle]], write $S^V$ for its [[fiber]]-wise [[one-point compactification]]. This is a [[sphere bundle]]/[[spherical fibration]]. Write $\mathbb{S}^V$ for the $X$-[[parameterized spectrum]] which is fiberwise the [[suspension spectrum]] of $S^V$.

=--

It is immediate that:

+-- {: .num_prop #SphericalFibrationsOfVectorBundlesClassifiedViaJ}
###### Proposition
**([[spherical fibrations]] of [[vector bundles]] classified via J-homomorphism)**

For $V \to X$ a [[vector bundle]] classified by a map $X \to B O$, 
the corresponding [[spherical fibration]] $\mathbb{S}^V$, def. \ref{SphereBundleOfVectorBundle}, is classified by $X \to B O \stackrel{B J}{\longrightarrow} B GL_1(\mathbb{S})$, def. \ref{DeloopedJ}.

=--

This construction descends to a map

$$
  KO^0(X) \longrightarrow Sph(X)
$$

from [[topological K-theory]] to [[spherical fibrations]]

(e.g. [Clausen 11, Section 2](#Clausen11), [Westerland 14, slide 5](#Westerland14), [MO discussion](http://mathoverflow.net/a/156369/381))



## Properties
 {#Properties}

### Image of the J-homomorphism
 {#Image}

#### Traditional formulation
 {#ImageOfJTradtionalFormulation}


##### Description of the image

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

* for $n = 0 \;mod \;8$ and $n = 1 \;mod \; 8$ and $n$ positive the J-homomorphism $\pi_n(J) \colon \pi_n(S O) \to \pi_n(\mathbb{S})$ is [[injection|injective]], hence its image is $\mathbb{Z}_2$, 

* for $n = 3\; mod\; 8$ and $n = 7 \; mod \; 8$ hence for $n = 4 k -1$, the [[order of a group|order]] of the image is equal to the [[denominator]] of $B_{2k}/4k$ in its reduced form, where $B_{2k}$ is the [[Bernoulli number]]

* for all other cases the image is necessarily zero.

=--

This characterization of the image of $J$ is due to ([Adams 66](#Adams66), [Quillen 71](#Quillen71), [Sullivan 74](#Sullivan74)). 
Specifically the identification of $J(\pi_{4n-1}(S O))$ is ([Adams 65a, theorem 3.7](#Adams65a) and the direct summand property is ([Adams 66, theorems 1.1-1.6.](#Adams66)).
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



##### Characterization via the Adams operations

(...)

We indicate how the [[Adams conjecture]]/Adams-Quillen-Sullivan theorem serves to identify the image of the J-homomorphism. We follow the modern account as reviewed in ([Lorman 13](#Lorman13)).

(...)

Write $\psi^k$ for the $k$th [[Adams operation]] on [[complex K-theory]].

Let $p$ be a [[prime]]. Consider $k$ coprime to $p$.


The [[Adams conjecture]] implies that completed at $p$, the 
J-homomorphism factors through the [[homotopy fiber]] of $1 - \psi^k$.

proof:

We have a homotopy-commuting diagram

$$
  \array{
    B U_p &\stackrel{1 - \psi^k}{\longrightarrow}& B U_p
    \\
    \downarrow &\swArrow_\simeq& \downarrow
    \\
    \ast &\stackrel{0}{\longrightarrow}& B H_p
  }
  \,.
$$

The [[pasting]] composite with the [[homotopy pullback]] that witnesses the [[homotopy fiber]] of $1 - \psi^k$ induces via the [[universal property]] of the [[loop space object]] a canonical map $fib(1-\psi^k) \longrightarrow H_p$:

$$
  \array{
    fib(1-\psi^k) &\longrightarrow& \ast
    \\
    \downarrow &&  \downarrow
    \\
    B U_p &\stackrel{1 - \psi^k}{\longrightarrow}& B U_p
    \\
    \downarrow &\swArrow_\simeq& \downarrow
    \\
    \ast &\stackrel{0}{\longrightarrow}& B H_p
  }
  \;\;\;
  \simeq 
  \;\;\;
  \array{
    fib(1-\psi^k) &\longrightarrow& \ast
    \\
    \downarrow &&  \downarrow
    \\
    H_p &\stackrel{}{\longrightarrow}& \ast
    \\
    \downarrow &\swArrow_\simeq& \downarrow
    \\
    \ast &\stackrel{0}{\longrightarrow}& B H_p
  }   
  \,.
$$

(...)


##### The J-spectrum

The [[J-spectrum]] is a [[spectrum]] whose [[homotopy groups]] are close to being the image of the J-homomorphism.

(...)


#### Formulation in chromatic homotopy theory
 {#ImageOfJInChromotopy}

In terms of [[chromatic homotopy theory]] the nature of the image of the J-homomorphism can be formulated more succinctly as follows.


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
       \mathbb{Z}/p^{k+1}\mathbb{Z} & if\; n+1 = 2(p-1)p^k m \;with\; m \neq 0\;mod\;p
        \\
        0 & otherwise
    }
  \right.
  \,.
$$

=--

This appears as ([Lurie 10, theorem 6](#Lurie)) (note that there are two typos: first, the theorem is stated with $L_{K(1)} \mathbb{S}$ rather than $L_{E(1)} \mathbb{S}$, and second, it should be $n+1 = 2(p-1)p^k m$ but the $2$ is missing.)


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

In this form this appears as ([Lurie 10, theorem 7](#Lurie)). See also ([Behrens 13, section 1](#Behrens13)).

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


## Related concepts

* [[e-invariant]]

* [[Thom spectra]], [[MO]]

* [[orientation in generalized cohomology]]

* [[J-homomorphism and chromatic homotopy]]

* [[scanning map equivalence]]

* [[twisted cohomotopy]]

\linebreak


## References

### General

The J-homomorphism was introduced in 

* {#Whitehead42} [[George Whitehead]], _On the homotopy groups of spheres and rotation groups_, Annals of Mathematics. Second Series 43 (4): 634&#8211;640 (1942) ([jstor:1968956](http://www.jstor.org/stable/1968956)).

Textbook accounts:

* {#Kosinski93} [[Antoni Kosinski]], chapter IX 6.3 of: _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf), [ISBN:978-0-12-421850-5](https://www.sciencedirect.com/bookseries/pure-and-applied-mathematics/vol/138/suppl/C))

* [[Dai Tamaki]], [[Akira Kono]], Section 4.4 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))


Lecture notes:

* [[Akhil Mathew]], _The Adams conjecture I_ ([web](http://amathew.wordpress.com/2013/01/23/the-adams-conjecture-i/))

* [[Akhil Mathew]], _Notes on the J-homomorphism_, 2012 ([pdf](http://math.uchicago.edu/~amathew/j.pdf), [[MathewJHomomorphism.pdf:file]])

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lecture 13 in: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])

* [[Arpon Raksit]], _Vector fields and the J-homomorphism_, 2014 ([pdf](http://stanford.edu/~arpon/math/files/vfields.pdf), [[Raksit_JHomomorphism.pdf:file]])

* {#Westerland14} [[Craig Westerland]], _Views on the J-homomorphism_, MSRI talk, 2014 ([recording](https://mathinstitutes.org/videos/videos/1464), [pdf](https://docs.google.com/viewer?url=https://www.msri.org/workshops/685/schedules/17895/documents/1978/assets/20102), [[WesterlandJHomomorphism.pdf:file]])

* [[Gereon Quick]], _The $e$-invariant and the $J$-homomorphism_, lecture notes in: _[Advanced algebraic topology](https://folk.ntnu.no/gereonq/Math231br.html)_, 2014 ([[QuickEInvariantAndJHomomorphism.pdf:file]])

Discussion in [[higher algebra]] in term of [[(∞,1)-module bundles]] is in

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_ ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))

and in higher [[chromatic homotopy theory]]:

* [[Craig Westerland]], _A higher chromatic analogue of the image of J_, Geometry & Topology 21 (2017) 1033–1093 ([doi:10.2140/gt.2017.21.1033](https://doi.org/10.2140/gt.2017.21.1033))

Discussion in [[p-adic geometry]]:

* {#Clausen11} Dustin Clausen, _$p$-adic J-homomorphisms and a product formula_ ([arXiv:1110.5851](https://arxiv.org/abs/1110.5851))



The [[complex geometry|complex]] J-homomorphism is discussed in 

* [[Victor Snaith]], _The complex J-homomorphism_, Proc. London Math. Soc. (1977) s3-34 (2): 269-302 ([journal](http://plms.oxfordjournals.org/content/s3-34/2/269.full.pdf+html))

* [[Victor Snaith]], _Infinite loop maps and the complex $J$-homomorphism_, Bull. Amer. Math. Soc. Volume 82, Number 3 (1976), 508-510. ([Euclid](http://projecteuclid.org/euclid.bams/1183537922))

A [[p-adic number|p-adic]] J-homomorphism is described in 

* Dustin Clausen, _p-adic J-homomorphisms and a product formula_ ([arXiv:1110.5851](http://arxiv.org/abs/1110.5851))


### The image of J


The analysis of the image of $J$ is due to 

* [[John Adams]], _On the groups $J(X)$ I_, Topology 2 (3) (1963) ([pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/J-I.pdf))

* {#Adams65a} [[John Adams]], _On the groups $J(X)$ II_, Topology 3 (2) (1965) ([pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/J-II.pdf))
 

* {#Adams65b} [[John Adams]], _On the groups $J(X)$ III_, Topology 3 (3) (1965) ([pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/J-III.pdf))
 

* {#Adams66} [[John Adams]], _On the groups $J(X)$ IV_, Topology 5: 21,(1966)  _Correction_, Topology 7 (3): 331 (1968) ([pdf](http://math.unice.fr/~cazanave/Gdt/ImJ/J-IV.pdf))
 


* {#Quillen71} [[Daniel Quillen]], _The Adams conjecture_, Topology. an International Journal of Mathematics 10: 67&#8211;80 (1971) ([pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/Quillen.pdf))
 


* {#Sullivan74} [[Dennis Sullivan]], _Genetics of homotopy theory and the Adams conjecture_, Ann. of Math. 100 (1974), 1&#8211;79.
 

* {#Switzer75} [[Robert Switzer]], _Algebraic topology&#8211;homotopy and homology_, Springer-Verlag, New York, 1975.
 

The statement of the theorem about the characterization of the image is reviewed in 

* {#RavenelCh1} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, chapter 1, _An introduction to the homotopy groups of spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel1.pdf))
 

see there also around theorem 3.4.16.

The details of the proof are surveyed in 

* {#RavenelChapter5} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, chapter 5, _The chromatic spectral sequence_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel5.pdf))
 


Tables showing the image of $J$ at low primes are in 

* {#Hatcher} [[Allen Hatcher]], _Stable homotopy groups of spheres_ ([html](http://www.math.cornell.edu/~hatcher/stemfigs/stems.html))
 


Other reviews include

* [[Mark Mahowald]], _The Image of J in the EHP Sequence_, Annals of Mathematics   Second Series, Vol. 116, No. ([JSTOR](http://www.jstor.org/stable/2007048))

* [[Johannes Ebert]], _The Adams conjecture after Edgar Brown_, ([pdf](http://www.math.uni-muenster.de/u/jeber_02/talks/adams.pdf))


Discussion from the point of view of [[chromatic homotopy theory]] is in 

* {#Lurie} [[Jacob Lurie]], _The image of $J$_, lecture 35 in _[[Chromatic Homotopy Theory]]_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture35.pdf))

* {#Behrens13} [[Mark Behrens]], section 1 of Introduction talk at _[Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/conferences/talbot/index.php?year=2013&sub=talks)_ ([pdf](http://math.mit.edu/conferences/talbot/2013/1-Behrens-intro.pdf), [pdf](http://math.mit.edu/conferences/talbot/2013/Behrens-Introduction-chromatic-homotopy-thy-4-22-13.pdf)) 

* {#Knudsen13} [[Ben Knudsen]], _First chromatic layer of the sphere spectrum = homotopy of the $K(1)$-local sphere_, talk at _[2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php)_ ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-04-04-Rob-Legg-K1-local-sphere.pdf))
 


* {#Lorman13} [[Vitaly Lorman]], _Chromatic homotopy theory at height 1 and the image of $J$_, talk at _[Talbot 2013: Chromatic Homotopy Theory](http://math.mit.edu/conferences/talbot/index.php?year=2013&sub=talks)_ ([pdf](https://math.mit.edu/events/talbot/2013/Image%20of%20J-1.pdf))
 
Generalization to [[equivariant cohomology]] ([[equivariant K-theory]]) is discussed in
 
* Z. Fiedorowicz, H. Hauschild, [[Peter May]], theorem 0.4 of _Equivariant algebraic K-theory_, _Equivariant algebraic K-theory_, Algebraic K-Theory. Springer, Berlin, Heidelberg, 1982. 23-80 ([pdf](http://math.uchicago.edu/~may/PAPERS/40.pdf))

* Henning Hauschild, [[Stefan Waner]], theorem 0.1 of _The equivariant Dold theorem mod $k$ and the Adams conjecture_, Illinois J. Math. Volume 27, Issue 1 (1983), 52-66. ([euclid:1256065410](https://projecteuclid.org/euclid.ijm/1256065410))

* Kuzuhisa Shimakawa, _Note on the equivariant $K$-theory spectrum_, Publ. RIMS, Kyoto Univ. **29** (1993), 449-453 ([pdf](http://www.ems-ph.org/journals/show_pdf.php?issn=0034-5318&vol=29&iss=3&rank=5), [doi](https://doi.org/10.2977/prims/1195167052))

* Christopher French, theorem 2.4 in _The equivariant $J$–homomorphism for finite groups at certain primes_, Algebr. Geom. Topol. Volume 9, Number 4 (2009), 1885-1949 ([euclid:1513797069](https://projecteuclid.org/euclid.agt/1513797069))

### Equivariant enhancement

The generalization to [[equivariant cohomology]] ([[equivariant K-theory]] and the [[equivariant Adams conjecture]]) is discussed in

* [[Tammo tom Dieck]], theorem 11.3.8 in _[[Transformation Groups and Representation Theory]]_ Lecture Notes in Mathematics 766 Springer 1979

* Z. Fiedorowicz, H. Hauschild, [[Peter May]], theorem 0.4 of _Equivariant algebraic K-theory_, _Equivariant algebraic K-theory_, Algebraic K-Theory. Springer, Berlin, Heidelberg, 1982. 23-80 ([pdf](http://math.uchicago.edu/~may/PAPERS/40.pdf))

* Henning Hauschild, [[Stefan Waner]], theorem 0.1 of _The equivariant Dold theorem mod $k$ and the Adams conjecture_, Illinois J. Math. Volume 27, Issue 1 (1983), 52-66. ([euclid:1256065410](https://projecteuclid.org/euclid.ijm/1256065410))

* Kuzuhisa Shimakawa, _Note on the equivariant $K$-theory spectrum_, Publ. RIMS, Kyoto Univ. **29** (1993), 449-453 ([pdf](http://www.ems-ph.org/journals/show_pdf.php?issn=0034-5318&vol=29&iss=3&rank=5), [doi](https://doi.org/10.2977/prims/1195167052))

* Christopher French, theorem 2.4 in _The equivariant $J$–homomorphism for finite groups at certain primes_, Algebr. Geom. Topol. Volume 9, Number 4 (2009), 1885-1949 ([euclid:1513797069](https://projecteuclid.org/euclid.agt/1513797069))


### Relation to $O$-action on general spectra

Similarly there is a canonical $O(n)$-[[∞-action]] on an [[n-fold loop space]], not just on the [[sphere spectrum]]. But the general case is closely related to the J-homomorphism. Discussion includes

* {#GaudensMenichi07} Gerald Gaudens, [[Luc Menichi]],  section 5 of _Batalin-Vilkovisky algebras and the $J$-homomorphism_, Topology and its Applications Volume 156, Issue 2, 1 December 2008, Pages 365&#8211;374 ([arXiv:0707.3103](http://arxiv.org/abs/0707.3103))

and in the context of the [[cobordism hypothesis]]:

* {#Lurie} [[Jacob Lurie]], example 2.4.15 of _[[On the Classification of Topological Field Theories]]_, Current Developments in Mathematics Volume 2008 (2009), 129-280 ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))



[[!redirects J-homomorphisms]]


[[!redirects image of J]]
[[!redirects image of J-homomorphism]]
[[!redirects image of the J-homomorphism]]

[[!redirects equivariant J-homomorphism]]
[[!redirects equivariant J-homomorphisms]]
