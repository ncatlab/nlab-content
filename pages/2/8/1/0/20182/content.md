
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--




\tableofcontents

## Idea

Given two [[topological spaces]] $X$, $Y$ one may ask for the [[rational homotopy theory|rational homotopy type]] of their [[mapping space]] $Maps(X,Y)$. Under good conditions this is a [[nilpotent space]] of [[finite type]] and hence admits a [[Sullivan model]] from which its rationalized [[homotopy groups]] and its rational [[cohomology groups]] may be read off.


## General formula
 {#GeneralFormula}

\begin{proposition}
\label{GeneralModelOfRationalizedMappingSpace}
For $X, \mathcal{A}$ a [[pair]] of [[connected topological space|connected]] [[nilpotent topological space|nilpotent]] [[topological spaces]] of [[rational cohomology|rational]] [[finite type]], the [[mapping space]] from $X$ into the [[rationalization]] $L^{\mathbb{Q}} \mathcal{A}$ has a ([[simplicial weak equivalence|simplicial]]) [[weak homotopy equivalence]] 

$$
  Map\big(
    X, 
    L^{\mathbb{Q}}\mathcal{A}
  \big)
  \,\simeq\,
  \Omega^1_{cl}\big(
    X \times \Delta^\bullet;
    \mathfrak{l}\mathcal{A}
    \big)
  \mathrlap{\,,}
$$

where we denote by

* $\mathfrak{l}(-)$ the rational [[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]],

* $\Omega^1_{cl}(-;\mathfrak{g}) \coloneqq Hom_{dgcAlg}\big(CE(\mathfrak{g}), \Omega^\bullet_{PL}(-)\big)$ the set of [[closed L-infinity algebra valued differential forms|closed $L_\infty$-algebra valued differential forms]], where

  * $\Omega^\bullet_{PL}\big(X \times \Delta^n\big)$ is the [[polynomial de Rham complex]] of the [[product space]] of $X$ with the [[n-simplex]],

  * $CE(-)$ the [[Chevalley-Eilenberg algebra]], so that $CE\big(\mathfrak{l}(-)\big)$ gives the [[minimal Sullivan model]],

and we understand the [[topological space]] on the left as its [[homotopy type]] incarnated by its [[singular simplicial complex]].

\end{proposition}

(This is, in paraphrase, [Berglund 2015 Thm. 1.4](#Berglund2015).)

Over the [[real numbers]] and in the case that $X$ is a [[smooth manifold]], there is a quick re-proof of Prop. \ref{GeneralModelOfRationalizedMappingSpace} using [[cohesive (infinity,1)-topos|cohesive homotopy theory]]:


\begin{proposition}
\label{RationalModelViaCohesion}
For 

* $X$ a [[smooth manifold]],

* $\mathcal{A}$ a [[connected topological space|connected]] [[nilpotent topological space|nilpotent]] [[topological space]] of [[rational cohomology|rational]] [[finite type]],

there is an [[equivalence in an (infinity,1)-category|equivalence]]

$$
  \mathbf{Map}\big(
    X,
    L^{\mathbb{R}}
    \mathcal{A}
  \big)
  \simeq
  \esh
  \mathbf{\Omega}^1_{cl}\big(X; \mathfrak{l}\mathcal{A}\big)
  \,,
$$

of ([[discrete object|geometrically discrete]]) [[smooth infinity-groupoid|smooth $\infty$-groupoids]], where we denote by

* $\mathbf{Map}(-,-)$ the [[mapping stack]] ([[internal hom]]),

* $L^{\mathbb{R}}(-)$ the [[real homotopy theory|$\mathbb{R}$-rationalization]] ([[rationalization]] followed by [[derived functor|derived]] [[extension of scalars]]),

* $\mathbf{\Omega}^1_{cl}\big(X; \mathfrak{g}\big) \,\colon\, U \mapsto Hom_{dgcAlg}\big( CE(\mathfrak{g}), \Omega^\bullet_{dR}(U \times X) \big)$ the [[moduli space|moduli]] [[smooth set]] of [[closed L-infinity algebra valued differential forms|closed $L_\infty$-algebra valued differential forms]],

* $\esh$ the [[shape modality]].

\end{proposition}
\begin{proof}
This follows readily as:
$$
  \begin{aligned}
    \esh
    \mathbf{\Omega}^1_{cl}\big(
      X; \mathfrak{l}\mathcal{A}
    \big)
    & \simeq
    \esh
    \mathbf{Map}\Big(
      X,
      \mathbf{\Omega}^1_{cl}\big(
        \ast; \mathfrak{l}\mathcal{A}
      \big)
    \Big) 
    \\
    & \simeq
    \mathbf{Map}\Big(
      X,
      \esh
      \mathbf{\Omega}^1_{cl}\big(
        \ast; \mathfrak{l}\mathcal{A}
      \big)
    \Big) 
    \\
    & =
    \mathbf{Map}\Big(
      X,
      L^{\mathbb{R}} \mathcal{A}
    \Big) 
    \mathrlap{\,,}
  \end{aligned}
$$
where we used, in order of appearance:

1. the formula for the plots of [[mapping stacks]] (cf. [here](closed+monoidal+structure+on+presheaves#CartesianClosedMonoidalnessOfCategoriesOfPresheaves)),

1. the [smooth Oka principle](shape+via+cohesive+path+∞-groupoid#ConsequenceSmoothOkaPrinciple) to pass the [[shape modality]] into the mapping stack,

1. the formula for [[shape via cohesive path ∞-groupoids]] to identify

   $$
     \esh \mathbf{\Omega}^1_{cl}(\ast; \mathfrak{g})
     \simeq
     Dsc\, \Omega^1_{cl}\big(\mathbf{\Delta}^\bullet; \mathfrak{g}\big)
     \mathrlap{\,,}
   $$

   together with the [[fundamental theorem of dg-algebraic rational homotopy theory]]:

   $$
     L^{\mathbb{R}}\mathcal{A}
     \simeq
     \Omega^1_{cl}\big(\mathbf{\Delta}^\bullet; \mathfrak{l}\mathcal{A}\big)
     \mathrlap{\,,}
   $$ 

   here implemented not with [[polynomial de Rham complex|piecewise linear]] but with [[smooth differential forms]] on [[smooth manifolds]] and extended simplices $\mathbf{\Delta}^n$ (which still satisfy the relevant [[extension lemma for differential forms]], see [there](extension+lemma+for+differential+forms#ExtensionLemmaForPiecewiseSmoothForms)).

\end{proof}

The global model of Prop. \ref{GeneralModelOfRationalizedMappingSpace} induces analog models for each of the [[connected components]] of the mapping space:

\begin{proposition}
Consider:

* $X, \mathcal{A}$ a [[pair]] of [[connected topological space|connected]] [[nilpotent topological space|nilpotent]] [[CW-complexes]] of [[rational cohomology|rational]] [[finite type]],
 
  with $X$ a [[finite CW complex]] or $\mathcal{A}$ having a finite [[Postnikov tower]],

* $\phi \colon X \to \mathcal{A}$ a [[continuous map]].

Then a [[dg-Lie algebra]] model for the [[rational homotopy type]] of the [[mapping space]] $Map\big(X; \mathcal{A}\big)$ in the [[connected component]] of $\phi$ is given by the twisted [[tensor product]]

$$
  \big(
    \Omega^\bullet_{PL}(X) 
      \textstyle{
        \otimes_{\mathbb{Q}}
      }
    \mathfrak{l} \mathcal{A}
  \big)^{\xi_\phi}
  \langle 0 \rangle
$$ 

where :

* $\Omega^\bullet_{PL}(-)$ denotes the [[PL de Rham complex|PL de Rham]] [[dgc-algebra]],

* $\mathfrak{l}(-)$ denotes the [[dg-Lie algebra]] model.

* $\xi_\phi \in MC\big( \Omega^\bullet_{PL}(X) \otimes \mathfrak{l}\mathcal{A}\big)$ is the [[Maurer-Cartan element]] corresponding to the [[pullback of differential forms]]

  $$
    \phi^\ast 
      \,\colon\,
    CE(\mathfrak{l}\mathcal{A})
      \longrightarrow
    \Omega^\bullet_{PL}(X) 
    \mathrlap{\,,}
  $$

* $(-)^{\xi_\phi}$ means that the [[differential]] of the tensor [[dg-Lie algebra]] is twisted as

  $$
    d^{\mathfrak{l}\phi}(-)
    \coloneqq
    \mathrm{d}(-)
    +
    \big[\xi_\phi, -\big]
    \mathrlap{\,,}
  $$

* $(-)\langle-\rangle$ denotes the [[connective cover]] (discarding negative degrees and restricting to [[cycles]] in degree=0).

\end{proposition}

([Lazarev 2013 Thm. 8.1](#Lazarev2013), cf. [Berglund 2015 Thm. 1.5](#Berglund2015), [Buijs, Felix & Murillo 2012 Thm. 3.1](#BuijsFelixMurillo12))



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

* [[Edgar H. Brown, Jr.]], [[Robert H. Szczarba]]: *On the Rational Homotopy Type of Function Spaces*, Transactions of the American Mathematical Society **349** 12 (1997) 4931-4951 &lbrack;[jstor:2155493](https://www.jstor.org/stable/2155493)&rbrack;

* Gregory Lupton, Samuel Bruce Smith, _Rationalized Evaluation Subgroups of a Map and the Rationalized G-Sequence_ ([arXiv:math/0309432](https://arxiv.org/abs/math/0309432))

* {#CohenVoronov05} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))

* [[Urtzi Buijs]], [[Aniceto Murillo]], _Basic constructions in rational homotopy theory of function spaces_,  Annales de l'Institut Fourier, Volume 56 (2006) no. 3, p. 815-838 ([doi:10.5802/aif.2201](https://doi.org/10.5802/aif.2201))

* [[Micheline Vigué-Poirrier]], _Rational formality of function spaces_, Journal of Homotopy and Related Structures 2.1 (2007): 99-108 ([arXiv:0706.2977](https://arxiv.org/abs/0706.2977))

* Gregory Lupton, Samuel Bruce Smithm, _Rationalized evaluation subgroups of a map I: Sullivan models, derivations and $G$-sequences_, Journal of Pure and Applied Algebra, Volume 209, Issue 1, April 2007, Pages 159-171 ([doi:10.1016/j.jpaa.2006.05.018](https://doi.org/10.1016/j.jpaa.2006.05.018))

* [[Urtzi Buijs]], [[Aniceto Murillo]], _The rational homotopy Lie algebra of function spaces_, Comment. Math. Helv. 83 (2008), 723–739 ([pdf](https://pdfs.semanticscholar.org/d404/657ccc24b0c06434086485d3e528e0316e26.pdf))

* Gregory Lupton, Samuel Bruce Smith, _Whitehead products in function spaces: Quillen model formulae_, J. Math. Soc. Japan, Volume 62, Number 1 (2010), 49-81. ([arXiv:0812.1829](https://arxiv.org/abs/0812.1829), [euclid:jmsj/1265380424](https://projecteuclid.org/euclid.jmsj/1265380424))


* {#Lazarev2013} [[Andrey Lazarev]]: *Maurer-Cartan moduli and models for function spaces*, Advances in Mathematics **235** (2013) 296--320 &lbrack;[arxiv:1109.3715 math.AT](http://arxiv.org/abs/1109.3715), [doi:10.1016/j.aim.2012.11.009](https://doi.org/10.1016/j.aim.2012.11.009)&rbrack;


* J.-B. Gatsinzi, _A model for function spaces_, Topology and its Applications, Volume 168, 15 May 2014, Pages 153-158 ([doi:10.1016/j.topol.2014.02.021](https://doi.org/10.1016/j.topol.2014.02.021))

* J.-B. Gatsinzi, _Rational Gottlieb Group of Function Spacesof Maps into an Even Sphere_, International Journal of Algebra, Vol. 6, 2012, no. 9, 427 - 432 ([pdf](http://www.m-hikari.com/ija/ija-2012/ija-9-12-2012/gatsinziIJA9-12-2012.pdf))

* {#Berglund2015} [[Alexander Berglund]]: _Rational homotopy theory of mapping spaces via Lie theory for $L_\infty$ algebras_, Homology, Homotopy and Applications **17** 2 (2015) &lbrack;[arXiv:1110.6145 math.AT](https://arxiv.org/abs/1110.6145), [doi:10.4310/HHA.2015.v17.n2.a16](http://dx.doi.org/10.4310/HHA.2015.v17.n2.a16)&rbrack;

* {#BuijsFelixMurillo12} [[Urtzi Buijs]], [[Yves Félix]], [[Aniceto Murillo]]: _$L_\infty$-rational homotopy of mapping spaces_,  published as: _$L_\infty$-models of based mapping spaces_, J. Math. Soc. Japan **63** 2 (2011) 503--524 &lbrack;[arXiv:1209.4756 math.AT](https://arxiv.org/abs/1209.4756), [doi:10.2969/jmsj/06320503](https://doi.org/10.2969/jmsj/06320503)&rbrack;

* {#SatiVoronov24} [[Hisham Sati]], [[Alexander A. Voronov]]: Section 2 of: *Mysterious Triality and the Exceptional Symmetry of Loop Spaces* &lbrack;[arXiv:2408.13337](https://arxiv.org/abs/2408.13337)&rbrack;


### Rational Cohomotopy cocycle spaces
 {#ReferencesRationalCohomotopy}

Discussion of [[rational Cohomotopy]] [[cocycle spaces]]:

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242](https://www.jstor.org/stable/2000242)) 

* J.-B. Gatsinzi, _Rational Gottlieb Group of Function Spacesof Maps into an Even Sphere_, International Journal of Algebra, Vol. 6, 2012, no. 9, 427 - 432 ([pdf](http://www.m-hikari.com/ija/ija-2012/ija-9-12-2012/gatsinziIJA9-12-2012.pdf))

On the [[rational cohomology]] of [[iterated loop spaces]] of [[n-spheres]]:

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structure of Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])

Also

* [Sati & Voronov 2024, Section 2](#SatiVoronov24)


### Spectral sequence for rational homotopy of mapping spaces

A [[spectral sequence]] computing the [[rational homotopy theory|rational homotopy]] of [[mapping spaces]]:

* {#Smith97} Samuel B. Smith, _A based Federer spectral sequence and the rational homotopy of function spaces_, Manuscripta Math (1997) 93: 59 ([doi:10.1007/BF02677458](https://doi.org/10.1007/BF02677458))

based on 

* {#Federer56} Herbert Federer, _A Study of Function Spaces by Spectral Sequences_,  Transactions of the American Mathematical Society Vol. 82, No. 2 (Jul., 1956), pp. 340-361 ([jstor:1993052](https://www.jstor.org/stable/1993052))

[[!redirects rational models of mapping spac]]

[[!redirects rational model of mapping spaces]]
[[!redirects rational models of mapping space]]
[[!redirects rational models of mapping spaces]]

[[!redirects Sullivan model of mapping space]]
[[!redirects Sullivan models of mapping space]]
[[!redirects Sullivan models of mapping spaces]]


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


