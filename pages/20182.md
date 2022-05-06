
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

### Mapping spaces between spheres

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

## Related concepts

[[!include Sullivan models -- examples]]



## References

### Sullivan models for mapping spaces
 {#ReferencesSullivanModelsForMappingSpaces}

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242](https://www.jstor.org/stable/2000242)) 

* {#CohenVoronov05} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))

* {#BuijsFelixMurillo12} [[Urtzi Buijs]], [[Yves Félix]], [[Aniceto Murillo]], _$L_\infty$-rational homotopy of mapping spaces_,  published as _$L_\infty$-models of based mapping spaces_,  J. Math. Soc. Japan Volume 63, Number 2 (2011), 503-524 ([arXiv:1209.4756](https://arxiv.org/abs/1209.4756), [doi:10.2969/jmsj/06320503](https://doi.org/10.2969/jmsj/06320503))

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

