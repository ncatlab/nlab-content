
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

### Sullivan models

Discussion of [[rational cohomology]] and of [[Sullivan models]] for [[cocycle spaces]] in rational Cohomotopy.



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


[[!include flavours of cohomotopy -- table]]

See also

* [[rational cohomology]]


## References

### Cocycle spaces

Discussion of [[cocycle spaces]] in [[rational Cohomotopy]] (see also at _[[rational model for mapping spaces]]_):

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structure of Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])



* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242](https://www.jstor.org/stable/2000242)) 

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



