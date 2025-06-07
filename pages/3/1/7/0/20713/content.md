[[!redirects rational Cohomotopy]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Rational Cohomotopy theory_ $\pi^\bullet_{\mathbb{Q}}$ is the approximation in [[rational homotopy theory]] of [[Cohomotopy cohomology theory]], i.e. the ([[non-abelian cohomology|non-abelian]]) [[generalized cohomology theory]] whose [[cocycle spaces]] are [[rationalizations]] of the [[cocycle spaces]] of plain [[Cohomotopy cohomology theory]], hence which are [[spaces of maps]] into [[rational n-spheres]] $S^n_{\mathbb{Q}}$:

$$
  \pi^n_{\mathbb{Q}}(-)
  \;=\;
  \pi_0 Maps\big(-, S^n\big)_{\mathbb{Q}}
  \;\simeq\;
  \pi_0 Maps\big(-, S^n_{\mathbb{Q}}\big)
  \;.
$$

## Properties

### Sullivan models for cocycle spaces

Discussion of [[rational cohomology]] and of [[Sullivan models]] for [[cocycle spaces]] in rational Cohomotopy.
+-- {: .num_prop #RationalHomotopyTypeOfMapsNSphereToNsphere}
###### Proposition     
**([[rational homotopy type]] of [[space of maps]] from [[n-sphere]] to itself)**

Let $n \in \mathbb{N}$ be a [[natural number]] and $f\colon S^n \to S^n$ a [[continuous function]] from the [[n-sphere]] to itself. Then the [[connected component]] $Maps_f\big( S^n, S^n\big)$ of the [[space of maps]] which contains this map has the following [[rational homotopy theory|rational]] [[homotopy type]]:

\[
  \label{RationalHomotopyTypeOfMappingSpacesSnToSn}
  Maps_f\big( S^n, S^n\big)
  \;\simeq_{\mathbb{Q}}\;
  \left\{
    \array{
      S^n \times S^{n-1} &\vert& n\,\text{even}\,, deg(f) = 0
      \\
      S^{2n-1} &\vert& n \, \text{even}\,, deg(f) \neq 0
      \\
      S^n &\vert& n\, \text{odd}
    }
  \right.
\]

where $deg(f)$ is the [[degree of a continuous function|degree]] of $f$.

Moreover, under the canonical morphism expressing the canonical [[action]] of  the [[special orthogonal group]] $SO(n+1)$ on $S^n = S\big( \mathbb{R}^{n+1}\big)$ (regarded as the [[unit sphere]] in $(n+1)$-[[dimension|dimensional]] [[Cartesian space]]) we have that on [[ordinary homology]]

$$
  \array{
    H_\bullet\Big( 
      SO\big( n+ 1 \big)
    \Big)
    &\longrightarrow&
    H_\bullet\Big( 
      Maps_{f = id}\big( S^n, S^n  \big) 
    \Big)
  }
$$

the generator in $\left\{ \array{ H_{2n+1}\big( SO(n+1), \mathbb{Q} \big) \simeq \mathbb{Q} &\vert& n\, \text{even} \\ H_{n}\big( SO(n+1), \mathbb{Q} \big) \simeq \mathbb{Q} &\vert& n\, \text{odd}   }  \right.$ maps to the [[fundamental class]] of the respective [[spheres]] in (eq:RationalHomotopyTypeOfMappingSpacesSnToSn), all other generators mapping to [[zero]].

=--

([Møller-Raussen 85, Example 2.5](#MollerRaussen85), [Cohen-Voronov 05, Lemma 5.3.5](#CohenVoronov05))

See at _[[Sullivan model of a spherical fibration]]_ for more on this.

+-- {: .num_prop #RationalCohomologyOfIteratedLoopSpaceOf2kSphere}
###### Proposition     
**([[rational cohomology]] of [[iterated loop space]] of the [[n-sphere|2k-sphere]])**

Let 

$$
  1 \leq D \lt n = 2k \in \mathbb{N}

$$ 

(hence two [[positive number|positive]] [[natural numbers]], one of them required to be [[even number|even]] and the other required to be smaller than the first) and consider the [[iterated loop space|D-fold loop space]] $\Omega^D S^n$ of the [[n-sphere]]. 

Its [[rational cohomology|rational]] [[cohomology ring]] is the [[free construction|free]] [[graded-commutative algebra]] over $\mathbb{Q}$ on one [[generators and relations|generator]] $e_{n-D}$ of degree $n - D$ and one generator $a_{2n - D - 1}$ of degree $2n - D - 1$:

$$
  H^\bullet
  \big(
    \Omega^D S^n
    ,
    \mathbb{Q}
  \big)
  \;\simeq\;
  \mathbb{Q}\big[ \omega_{n - D}, \omega_{2n - 1 - D} \big] 
  \,.
$$  

=--

(by [this Prop.](Sullivan+model+of+free+loop+space#SullivanModelsOfMapsFromSkToSnFornLargerk) at _[[Sullivan model of based loop space]]_; see also  [Kallel-Sjerve 99, Prop. 4.10](#KallelSjerve99))

For the edge case $\Omega^D S^D$ the above formula does not apply, since $\Omega^{D-1} S^D$ is not [[simply connected topological space|simply connected]] (its [[fundamental group]] is $\pi_1\big( \Omega^{D-1}S^D \big) = \pi_0 \big(\Omega^D S^D\big) = \pi_D(S^D) = \mathbb{Z}$, the 0th [[stable homotopy group of spheres]]). 

But:

+-- {: .num_example #RationalModelsForBasedMappingSpaceSDToSD}
###### Example   

The rational model for $\Omega^D S^D$ follows from Prop. \ref{RationalHomotopyTypeOfMapsNSphereToNsphere} by realizing the pointed mapping space as the [[homotopy fiber]] of the [[evaluation map]] from the free mapping space:

$$
  \array{
    \mathllap{
      \Omega^D S^D
      \simeq
    \;}
    Maps^{\ast/\!}\big( S^D, S^D\big)
    \\
    \big\downarrow^{\mathrlap{fib(ev_\ast)}}
    \\
    Maps(S^D, S^D)
    \\
    \big\downarrow^{\mathrlap{ev_\ast}}
    \\
    S^D
  }
$$

This yields for instance the following examples.

In odd dimensions:

\begin{xymatrix}
    \mathrm{Maps}^{\ast/\!}
    \big(
      S^3, S^3
    \big)
    \ar[d]^-{ \mathrm{fib}_{(\mathrm{ev}_\ast)} }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n \in \mathbb{Z}
    }{\sqcup}
    \ast
    \ar@{^{(}->}[d]
    \\
    \mathrm{Maps}
    \big(
      S^3, S^3
    \big)
    \ar[d]^-{ \mathrm{ev}_\ast }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n  \in \mathbb{Z}
    }{\sqcup}
    S^3
    \ar[d]^-{ (\mathrm{id}_{S^3})_{n \in \mathbb{N}} }
    \\
    S^3
    \ar@{=}[r]
    &
    S^3
\end{xymatrix}

In even dimensions:

(In the following $h_{\mathbb{K}}$ denotes the [[Hopf fibration]] of the [[division algebra]] $\mathbb{K}$, hence $h_{\mathbb{C}}$ denotes the [[complex Hopf fibration]] and $h_{\mathbb{H}}$ the [[quaternionic Hopf fibration]].)

\begin{xymatrix}
    \mathrm{Maps}^{\ast/\!}
    \big(
      S^2, S^2
    \big)
    \ar[d]^-{ \mathrm{fib}_{(\mathrm{ev}_\ast)} }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n \in \mathbb{Z}
    }{\sqcup}
    S^1
    \ar@{^{(}->}[d]
    \\
    \mathrm{Maps}
    \big(
      S^2, S^2
    \big)
    \ar[d]^-{ \mathrm{ev}_\ast }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \big(
      S^2 \times S^1
    \big)
    \sqcup
    \big(
      \underset{
        n \neq 0  \in \mathbb{Z}
      }{\sqcup}
      S^3
    \big)
    \ar[d]^-{
      \big(
        p_1, (h_{\mathbb{C}})_{n \neq 0 \in \mathbb{N}}
      \big)
    }
    \\
    S^2
    \ar@{=}[r]
    &
    S^2
\end{xymatrix}


\begin{xymatrix}
    \mathrm{Maps}^{\ast/\!}
    \big(
      S^4, S^4
    \big)
    \ar[d]^-{ \mathrm{fib}_{(\mathrm{ev}_\ast)} }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n \in \mathbb{Z}
    }{\sqcup}
    S^3
    \ar@{^{(}->}[d]
    \\
    \mathrm{Maps}
    \big(
      S^4, S^4
    \big)
    \ar[d]^-{ \mathrm{ev}_\ast }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \big(
      S^4 \times S^3
    \big)
    \sqcup
    \big(
      \underset{
        n \neq 0  \in \mathbb{Z}
      }{\sqcup}
      S^7
    \big)
    \ar[d]^-{ 
      \big(
        p_1, (h_{\mathbb{H}})_{n \neq 0 \in \mathbb{N}} 
      \big)
    }
    \\
    S^4
    \ar@{=}[r]
    &
    S^4
\end{xymatrix}



=--


## Examples

We discuss examples of cocycle spaces for rational 4-Cohomotopy, hence with [[coefficients]] in the [[rational n-sphere|rational]] [[4-sphere]], whose [[Sullivan model]] is


$$
  CE
  \big( 
    S^4
  \big)
  \;=\;
  \left(
  \begin{aligned}
  d\,g_4 & = 0
  \\
  d\,g_7 & = -\tfrac{1}{2} g_4 \wedge g_4
  \end{aligned}
  \right)
  \,.
$$


### The cocycle space for $\pi^4\big( S^1\big)_{\mathbb{Q}}$

The [[Sullivan model]] for the [[space of maps]] $Maps(S^1, S^4)$ from the [[1-sphere]] to the [[4-sphere]] is

$$
  CE
  \Big(
    \mathfrak{l}
    Maps
    \big( 
      S^1, S^4
    \big)
  \Big)
  \;=\;
  \left(
  \begin{aligned}
    d\,h_3 & = 0
    \\
    d\, \omega_4 & = 0
    \\
    d\, \omega_6 & = h_3 \wedge \omega_4
    \\
    d\, h_7 & = -\tfrac{1}{2} \omega_4 \wedge \omega_4
    \\
  \end{aligned}
  \right)
$$

By [this Prop.](#Sullivan+model+of+free+loop+space#SullivanModelForTheFreeLoopSpace), see [FSS 16, Section 3](#FSS16).


### The cocycle space for $\pi^4\big( S^3\big)_{\mathbb{Q}}$

The [[Sullivan model]] for the [[space of maps]] $Maps(S^3, S^4)$ from the [[3-sphere]] to the [[4-sphere]] is

$$
  CE
  \Big( 
    \mathfrak{l}
    Maps
    \big(
      S^3, S^4
    \big)
  \Big)
  \;=\;
  \left(
  \begin{aligned}
    d\, b_1 & = 0
    \\
    d\, \omega_4 & = 0
    \\
    d\, v_{{}_{4}} & = \omega_4 \wedge b_1
    \\
    d\, \omega_7 & = - \tfrac{1}{2} \, \omega_4 \wedge \omega_4
  \end{aligned}
  \right)
$$

By [Møller-Raussen 85, Prop. 2.3](#MollerRaussen85).

## Related concepts


[[!include flavours of cohomotopy -- table]]

See also

* [[rational cohomology]]


## References

### Cocycle spaces

Discussion of [[cocycle spaces]] in [[rational Cohomotopy]] (see also at _[[rational model for mapping spaces]]_):

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structure of Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])


* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242](https://www.jstor.org/stable/2000242)) 

* J.-B. Gatsinzi, _Rational Gottlieb Group of Function Spacesof Maps into an Even Sphere_, International Journal of Algebra, Vol. 6, 2012, no. 9, 427 - 432 ([pdf](http://www.m-hikari.com/ija/ija-2012/ija-9-12-2012/gatsinziIJA9-12-2012.pdf))


### On super-spaces

The observation that the [[equations of motion]] of the [[supergravity C-field]] and its dual in [[D=11 N=1 supergravity]] characterize it as a [[cocycle]] in rational 4-Cohomotopy:

* {#Sati13} [[Hisham Sati]], Section 2.5 of: _Framed M-branes, corners, and topological invariants_, J. Math. Phys. 59 (2018), 062304 ([arXiv:1310.1060](http://arxiv.org/abs/1310.1060))


Rational Cohomotopy of [[super-spaces]] (see also at _[[geometry of physics -- fundamental super p-branes]]_):

* {#FSS16} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: _[[schreiber:Rational sphere valued supercocycles in M-theory|Rational sphere valued supercocycles in M-theory and type IIA string theory]]_, Journal of Geometry and Physics, Volume 114, Pages 91-108 (2017) ([arXiv:1606.03206](https://arxiv.org/abs/1606.03206))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: _[[schreiber:The WZW term of the M5-brane|The WZW term of the M5-brane and differential cohomotopy]]_, J. Math. Phys. 56, 102301 (2015) ([arXiv:1506.07557](https://arxiv.org/abs/1506.07557))

  (**[arXiv:1506.07557](http://arxiv.org/abs/1506.07557)**)

Review in:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: _[[schreiber:The rational higher structure of M-theory]]_, in: _Proceedings of the [LMS-EPSRC Durham Symposium](http://www.maths.dur.ac.uk/lms/):_ _[Higher Structures in M-Theory](http://www.maths.dur.ac.uk/lms/109/index.html), August 2018_m Fortschritte der Physik, 2019 ([arXiv:1903.02834](https://arxiv.org/abs/1903.02834))

### Rational equivariant Cohomotopy

Discussion of [[rational equivariant homotopy theory|rational]] [[equivariant Cohomotopy]]:

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, Comm. Math. Phys. 2019 ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

### Rational twisted Cohomotopy

Discussion of rational [[twisted Cohomotopy]]:

* {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3 of _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization|Twisted Cohomotopy implies level quantization of the full 6d Wess-Zumino-term of the M5-brane]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

[[!redirects rational Cohomotopy theory]]
[[!redirects rational Cohomotopy cohomology theory]]

[[!redirects rational cohomotopy]]
[[!redirects rational cohomotopy theory]]
[[!redirects rational cohomotopy cohomology theory]]



