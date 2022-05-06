
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

We discuss tesults on the [[rational homotopy type]] of [[spaces of maps]] inti an [[n-sphere]], hence [[rational Cohomotopy]] [[cocycle]] spaces.

+-- {: .num_prop}
###### Proposition     

Let $n \in \mathbb{N}$ be a [[natural number]] and $f\colon S^n \to S^n$ a [[continuous function]] from the [[n-sphere]] to itself. Then the [[connected component]] $Maps_f\big( S^n, S^n\big)$ of the [[mapping space]] which contains this map has the following [[rational homotopy theory|rational]] [[homotopy type]]:

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
  \mathbb{Q}\big[ e_{n - D}, a_{2n - D - 1} \big] 
  \,.
$$  

=--

([Kallel-Sjerve 99, Prop. 4.10](#KallelSjerve99))

## Related concepts

[[!include Sullivan models -- examples]]



## References


### General
 {#ReferencesSullivanModelsForMappingSpaces}

Discussion of [[Sullivan models]] and models via [[L-∞ algebra]] for [[spaces of maps]]:

* {#CohenVoronov05} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))

* [[Urtzi Buijs]], [[Aniceto Murillo]], _Basic constructions in rational homotopy theory of function spaces_,  Annales de l'Institut Fourier, Volume 56 (2006) no. 3, p. 815-838 ([doi:10.5802/aif.2201](https://doi.org/10.5802/aif.2201))

* [[Urtzi Buijs]], [[Aniceto Murillo]], _The rational homotopy Lie algebra of function spaces_, Comment. Math. Helv. 83 (2008), 723–739 ([pdf](https://pdfs.semanticscholar.org/d404/657ccc24b0c06434086485d3e528e0316e26.pdf))

* [[Alexander Berglund]], _Rational homotopy theory of mapping spaces via Lie theory for $L_\infty$ algebras_,  Homology, Homotopy and Applications, Volume 17 (2015) Number 2 ([arXiv:1110.6145](https://arxiv.org/abs/1110.6145), [doi:10.4310/HHA.2015.v17.n2.a16]( http://dx.doi.org/10.4310/HHA.2015.v17.n2.a16))

* {#BuijsFelixMurillo12} [[Urtzi Buijs]], [[Yves Félix]], [[Aniceto Murillo]], _$L_\infty$-rational homotopy of mapping spaces_,  published as _$L_\infty$-models of based mapping spaces_,  J. Math. Soc. Japan Volume 63, Number 2 (2011), 503-524 ([arXiv:1209.4756](https://arxiv.org/abs/1209.4756), [doi:10.2969/jmsj/06320503](https://doi.org/10.2969/jmsj/06320503))

### Rational Cohomotopy cocycle spaces
 {#ReferencesRationalCohomotopy}

Discussion of [[rational Cohomotopy]] [[cocycle spaces]]:

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242](https://www.jstor.org/stable/2000242)) 


### Rational cohomology of mapping spaces

On [[rational cohomology]] of [[iterated loop spaces]] of [[n-spheres]]:

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structur eof Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])


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

