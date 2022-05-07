
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Given two [[topological spaces]] $X$, $Y$ one may ask for the [[rational homotopy theory|rational homotopy type]] of their [[mapping space]] $Maps(X,Y)$. Under good conditions this is a [[nilpotent space]] of [[finite type]] and hence admits a [[Sullivan model]] from which its rationalized [[homotopy groups]] and its rational [[cohomology groups]] may be read off.

## Examples

### Free loop spaces

See at _[[Sullivan model of free loop space]]_.

### Rational Cohomotopy spaces

We discuss results on the [[rational homotopy type]] of [[spaces of maps]] into an [[n-sphere]], hence [[rational Cohomotopy]] [[cocycle spaces]].

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


## Related concepts

[[!include Sullivan models -- examples]]



## References


### General
 {#ReferencesSullivanModelsForMappingSpaces}

Discussion of [[Sullivan models]] and models via [[L-∞ algebra]] for [[spaces of maps]]:

* Samuel Bruce Smith, _Rational evaluation subgroups_, Math Z (1996) 221: 387 ([doi:10.1007/BF02622121](https://doi.org/10.1007/BF02622121))

* Gregory Lupton, Samuel Bruce Smith, _Rationalized Evaluation Subgroups of a Map and the Rationalized G-Sequence_ ([arXiv:math/0309432](https://arxiv.org/abs/math/0309432))

* {#CohenVoronov05} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))

* [[Urtzi Buijs]], [[Aniceto Murillo]], _Basic constructions in rational homotopy theory of function spaces_,  Annales de l'Institut Fourier, Volume 56 (2006) no. 3, p. 815-838 ([doi:10.5802/aif.2201](https://doi.org/10.5802/aif.2201))

* [[Micheline Vigué-Poirrier]], _Rational formality of function spaces_, Journal of Homotopy and Related Structures 2.1 (2007): 99-108 ([arXiv:0706.2977](https://arxiv.org/abs/0706.2977))

* Gregory Lupton, Samuel Bruce Smithm, _Rationalized evaluation subgroups of a map I: Sullivan models, derivations and $G$-sequences_, Journal of Pure and Applied Algebra, Volume 209, Issue 1, April 2007, Pages 159-171 ([doi:10.1016/j.jpaa.2006.05.018](https://doi.org/10.1016/j.jpaa.2006.05.018))

* [[Urtzi Buijs]], [[Aniceto Murillo]], _The rational homotopy Lie algebra of function spaces_, Comment. Math. Helv. 83 (2008), 723–739 ([pdf](https://pdfs.semanticscholar.org/d404/657ccc24b0c06434086485d3e528e0316e26.pdf))

* Gregory Lupton, Samuel Bruce Smith, _Whitehead products in function spaces: Quillen model formulae_, J. Math. Soc. Japan, Volume 62, Number 1 (2010), 49-81. ([arXiv:0812.1829](https://arxiv.org/abs/0812.1829), [euclid:jmsj/1265380424](https://projecteuclid.org/euclid.jmsj/1265380424))


* [[Andrey Lazarev]], *Maurer-Cartan moduli and models for function spaces*, Advances in Mathematics Volume 235, 1 March 2013, Pages 296-320 ([arxiv:1109.3715](http://arxiv.org/abs/1109.3715), [doi:10.1016/j.aim.2012.11.009](https://doi.org/10.1016/j.aim.2012.11.009))


* J.-B. Gatsinzi, _A model for function spaces_, Topology and its Applications, Volume 168, 15 May 2014, Pages 153-158 ([doi:10.1016/j.topol.2014.02.021](https://doi.org/10.1016/j.topol.2014.02.021))

* J.-B. Gatsinzi, _Rational Gottlieb Group of Function Spacesof Maps into an Even Sphere_, International Journal of Algebra, Vol. 6, 2012, no. 9, 427 - 432 ([pdf](http://www.m-hikari.com/ija/ija-2012/ija-9-12-2012/gatsinziIJA9-12-2012.pdf))

* [[Alexander Berglund]], _Rational homotopy theory of mapping spaces via Lie theory for $L_\infty$ algebras_,  Homology, Homotopy and Applications, Volume 17 (2015) Number 2 ([arXiv:1110.6145](https://arxiv.org/abs/1110.6145), [doi:10.4310/HHA.2015.v17.n2.a16]( http://dx.doi.org/10.4310/HHA.2015.v17.n2.a16))

* {#BuijsFelixMurillo12} [[Urtzi Buijs]], [[Yves Félix]], [[Aniceto Murillo]], _$L_\infty$-rational homotopy of mapping spaces_,  published as _$L_\infty$-models of based mapping spaces_,  J. Math. Soc. Japan Volume 63, Number 2 (2011), 503-524 ([arXiv:1209.4756](https://arxiv.org/abs/1209.4756), [doi:10.2969/jmsj/06320503](https://doi.org/10.2969/jmsj/06320503))

### Rational Cohomotopy cocycle spaces
 {#ReferencesRationalCohomotopy}

Discussion of [[rational Cohomotopy]] [[cocycle spaces]]:

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242](https://www.jstor.org/stable/2000242)) 

* J.-B. Gatsinzi, _Rational Gottlieb Group of Function Spacesof Maps into an Even Sphere_, International Journal of Algebra, Vol. 6, 2012, no. 9, 427 - 432 ([pdf](http://www.m-hikari.com/ija/ija-2012/ija-9-12-2012/gatsinziIJA9-12-2012.pdf))

On the [[rational cohomology]] of [[iterated loop spaces]] of [[n-spheres]]:

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structure of Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])


### Spectral sequence for rational homotopy of mapping spaces

A [[spectral sequence]] computing the [[rational homotopy theory|rational homotopy]] of [[mapping spaces]]:

* {#Smith97} Samuel B. Smith, _A based Federer spectral sequence and the rational homotopy of function spaces_, Manuscripta Math (1997) 93: 59 ([doi:10.1007/BF02677458](https://doi.org/10.1007/BF02677458))

based on 

* {#Federer56} Herbert Federer, _A Study of Function Spaces by Spectral Sequences_,  Transactions of the American Mathematical Society Vol. 82, No. 2 (Jul., 1956), pp. 340-361 ([jstor:1993052](https://www.jstor.org/stable/1993052))

[[!redirects rational models of mapping spac]]

[[!redirects rational model of mapping spaces]]
[[!redirects rational models of mapping spaces]]

[[!redirects Sullivan model of mapping space]]
[[!redirects Sullivan models of mapping space]]
[[!redirects Sullivan models of mapping spaces]]

[[!redirects rational model of mapping space]]
[[!redirects rational models of mapping space]]
[[!redirects rational models of mapping spaces]]

[[!redirects Sullivan model mapping space]]
[[!redirects Sullivan model of mapping spaces]]

[[!redirects Sullivan model of a mapping space]]



[[!redirects rational model for mapping space]]
[[!redirects rational model for mapping spaces]]
[[!redirects rational models for mapping spaces]]

[[!redirects Sullivan model for mapping space]]
[[!redirects Sullivan models for mapping space]]
[[!redirects Sullivan models for mapping spaces]]

[[!redirects rational model for mapping space]]
[[!redirects rational models for mapping space]]
[[!redirects rational models for mapping spaces]]

[[!redirects Sullivan model for mapping spaces]]

[[!redirects Sullivan model for a mapping space]]


