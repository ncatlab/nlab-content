
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

The _$J$-homomorphism_ is traditionally a family of [[group]] homomorphisms

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

Since the process of [[one-point compactification]] is a [[functor]] on [[proper maps]], hence on [[homeomorphisms]], via def. \ref{SphereAsCompactification}, the $n$-sphere inherits from the canonical [[action]] of the [[orthogonal group]] $O(n)$ on $\mathbb{R}^n$ an [[action]] 

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

By construction, the homomorphism of remark \ref{OrthogonalActionOnSphereOnHomotopyGroups} are compatible with  [[suspension]] in that for all $n \in \mathbb{N}$ the [[diagrams]]

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


spring

$$
  KO^0(X) \longrightarrow Sph(X)
$$

[[topological K-theory]] to [[spherical fibrations]]

## Properties

### Image of the J-homomorphism
 {#Image}

The following characterization of the [[image]] of the J-homomorphism on [[homotopy groups]] was first conjectured in ([Adams 66](#Adams66)) (since called the _Adams conjecture_) and then proven in ([Quillen 71](#Quillen71)).

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

+-- {: .num_theorem #AdamsQuillenTheorem}
###### Theorem

The [[stable homotopy groups of spheres]] $\pi_n(\mathbb{S})$ are the [[direct sum]] of the ([[cyclic group|cyclic]]) [[image]] of the J-homomorphism, def. \ref{JHom}, and the [[kernel]] of the [[Adams e-invariant]].

Moreover,

* for $n = 0 \;mod \;$ and $n = 1 \;mod \; 8$ and $n$ positive the J-homomorphism is [[injection|injective]], hence its image is $\mathbb{Z}_2$, 

* for $n = 3\; mod\; 8$ and $n = 7 \; mod \; 8$ hence for $n = 4 k -1$, the [[order of a group|order]] of the image is equal to the [[denominator]] of $B_{2k}/4k$, where $B_{2k}$ is the [[Bernoulli number]]

* for all other cases the image is necessarily zero.

=--

The characterization of the image is due to ([Adams 66](#Adams66), [Quillen 71](#Quillen71)). That it is a direct summand of the codomain is proven for instance in ([Switzer 75, end of chapter 19](#Switzer75)). The theorem is recalled for instance as ([Ravenel, theorem 1.1.13](#Ravenel)).

+-- {: .num_remark}
###### Remark

The order of $J(\pi_{4k-1} O)$ in theorem \ref{AdamsQuillenTheorem} 
is for low $k$ given by the following table

| k | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| $\vert J(\pi_{4k-1}(O))\vert$ | 24 | 240 | 504 | 480 | 264 | 65,520 | 24 | 16,320 | 28,728 | 13,200 |

=--

See for instance ([Ravenel, p. 5](#Ravenel)).

## Related concepts

* [[orientation in generalized cohomology]]

## References

### General

The J-homomorphism was introduced in 

* [[George Whitehead]], _On the homotopy groups of spheres and rotation groups_, Annals of Mathematics. Second Series 43 (4): 634&#8211;640 (1942), ([JSTOR](http://www.jstor.org/stable/1968956)).

The analysis of its image is due to 

* [[John Adams]], _On the groups $J(X)$ IV_, Topology 5: 21,(1966)  _Correction_, Topology 7 (3): 331 (1968)
 {#Adams66}

* [[Daniel Quillen]], _The Adams conjecture_, Topology. an International Journal of Mathematics 10: 67&#8211;80 (1971)
 {#Quillen71}

* [[Robert Switzer]], _Algebraic topology&#8211;homotopy and homology_, Springer-Verlag, New York, 1975.
 {#Switzer75}

This is reviewed for instance in 

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, chapter I, _An introduction to the homotopy groups of spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel1.pdf))
 {#Ravenel}

see there also theorem 3.4.16.

Other revies include

* [[Johannes Ebert]], _The Adams conjecture after Edgar Brown_, ([pdf](http://www.math.uni-muenster.de/u/jeber_02/talks/adams.pdf))

See also 

* [[Victor Snaith]], _Infinite loop maps and the complex $J$-homomorphism_, Bull. Amer. Math. Soc. Volume 82, Number 3 (1976), 508-510. ([Euclid](http://projecteuclid.org/euclid.bams/1183537922))

Lecture notes include

* [[Akhil Mathew]], _Notes on the J-homomorphism_ ([pdf](http://people.fas.harvard.edu/~amathew/j.pdf))

Discussion in the modern perspective of [[higher algebra]] is for instance in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_ ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))

### The image of the J-homomorphism

* [[Jacob Lurie]], _The image of $J$_, lecture 35 in _[[Chromatic Homotopy Theory]]_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture35.pdf))
 {#Lurie}


* [[Mark Mahowald]], _The Image of J in the EHP Sequence_, Annals of Mathematics   Second Series, Vol. 116, No. ([JSTOR](http://www.jstor.org/stable/2007048))


[[!redirects J-homomorphisms]]

[[!redirects Adams conjecture]]
[[!redirects Adams' conjecture]]