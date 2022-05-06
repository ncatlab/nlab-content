
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Complex algebraic [[K3-surfaces]] admit the [[mathematical structure|structure]] of [[elliptic fibrations]] over the [[Riemann sphere]] $\mathbb{C}P^1$. Equipped with such, they are also called _elliptic K3-surfaces_.


## Properties

### Singular points
 {#SingularPoints}

Counted with multiplicity, these elliptic fibrations have 24 singular points (where the [[elliptic curve]]-fiber degenerates, to a [[nodal curve]] or [[cuspidal curve]]).

(review in [Huybrechts 16, Section 2-2.4](#Huybrechts16), [Propp 18, p. 4](K3-spectrum#Propp18)).

This number 24 of singularities-with-multiplicities is identified with the [[Euler number]] of the [[topological space]] underlying the (complex analytic) [[K3-surface]] (e.g. [Shimada 00, p. 432 (10 of 24)](#Shimada00), [Schütt-Shioda 09, Section 6.7, Theorem 6.10](#SchuttShioda09), [Huybrechts 16, Chapter 11, Remark 1.12](#Huybrechts16), review includes [Marquart 02, Section A.3.3, p. 59](#Marquart02)).

### Classification
 {#Classification}

Up to [[isomorphism]], there are a [[finite number]] of possible such elliptic fibrations.

([Nikulin 10](#Nikulin10),  [Lecacheux 19](#Lecacheux19))


## In F-theory

Elliptically fibered [[Calabi-Yau manifolds]] play a central role in [[F-theory]]:

In passing from [[M-theory]] to [[type IIA string theory]], the locus of any [[Kaluza-Klein monopole]] in 11d becomes the locus of [[D6-branes]] in 10d. The locus of the [[Kaluza-Klein monopole]] in turn (as discussed there) is the locus where the $S^1_A$-circle fibration degenerates. Hence in [[F-theory]] this is the locus where the fiber of the $S^1_A \times S^1_B$-[[elliptic fibration]] degenerates to the [[nodal curve]]. Since the [[T-duality|T-dual]] of [[D6-branes]] are [[D7-branes]], it follows that [[D7-branes]] in F-theory "are" the singular locus of the elliptic fibration.

Now an [[elliptic fibration|elliptically fibered]] complex [[K3-surface]] 

$$
  \array{
    T &\longrightarrow& K3
    \\
    && \downarrow
    \\
    && \mathbb{C}\mathbb{P}^1
  }
$$

may be parameterized via the [[Weierstrass elliptic function]] as the solution locus of the equation

$$
  y^2 = x^3 + f(z) x + g(z)
$$

for $x,y,z \in \mathbb{C}\mathbb{P}^1$, with $f$ a [[polynomial]] of degree 8 and $g$ of degree twelve. The [[j-invariant]] of the complex [[elliptic curve]] which this parameterizes for given $z$ is

$$
  j(\tau(z)) = \frac{4 (24 f)^3}{27 g^2 + 4 f^3} 
  \,.
$$

The [[poles]] $j\to \infty$ of the [[j-invariant]] correspond to the [[nodal curve]], and hence it is at these poles that the [[D7-branes]] are located. 

Since the order of the poles is 24 (the polynomial degree of the [[discriminant]] $\Delta = 27 g^2 + 4 f^3$) there are necessarily _24 D7-branes_ ([Sen 96, page 5](F-theory#Sen96), [Sen 97b](F-theory#Sen97b), see also [Morrison 04, sections 8 and 17](F-theory#Morrison04), [Denef 08, around (3.41)](F-theory#Denef08), [Douglas-Park-Schnell 14](duality+between+M%2FF-theory+and+heterotic+string+theory#DouglasParkSchnell14)).

Under [[T-duality]] this translates to 24 [[D6-branes]] in [[type IIA string theory]] on [[K3]] ([Vafa 96, Footnote 2 on p. 6](#Vafa96)).

Notice that the _net charge_ of these 24 D7-branes is supposed to vanish, due to [[S-duality]] effects (e.g. [Denef 08, below (3.41)](F-theory#Denef08)).

## Related concepts

* [[F/M-theory on elliptically fibered Calabi-Yau 2-folds|F-theory on CY2]]


## References

Basics:

* {#FriedmanMorgan94} [[Robert Friedman]], [[John Morgan]], _Smooth Four-Manifolds and Complex Surfaces_, Ergebnisse der Mathematik und ihrer Grenzgebiete. 3. Folge / A Series of Modern Surveys in Mathematics (1994) ([doi:10.1007/978-3-662-03028-8](https://www.springer.com/gp/book/9783540570585))

* {#Shimada00} [[Ichiro Shimada]], _On elliptic K3 surfaces_, Michigan Math. J. Volume 47, Issue 3 (2000), 423-446 ([euclid:mmj/1030132587](https://projecteuclid.org/euclid.mmj/1030132587))

* {#SchuttShioda09} Matthias Schütt, Tetsuji Shioda, Section 12 of: _Elliptic surfaces_, Adv. Stud. Pure Math. Algebraic Geometry in East Asia — Seoul 2008, J. H. Keum, S. Kondō, K. Konno and K. Oguiso, eds. (Tokyo: Mathematical Society of Japan, 2010), 51 - 160 ([arXiv:0907.0298](https://arxiv.org/abs/0907.0298), [euclid:aspm/1543085637](https://projecteuclid.org/euclid.aspm/1543085637))


* {#Huybrechts16} [[Daniel Huybrechts]], Chapter 11 of: _Lectures on K3-surfaces_,  Cambridge University Press  2016 ([pdf](http://www.math.uni-bonn.de/people/huybrech/K3Global.pdf), [[HuybrechtsLecturesOnK3.pdf:file]], [doi:10.1017/CBO9781316594193](https://doi.org/10.1017/CBO9781316594193))



Further review:

* [[Tristan Hübsch]], Section 6.2 of: _Calabi-Yau Manifolds -- A Bestiary for Physicists_, World Scientific 1992 ([doi:10.1142/1410](https://doi.org/10.1142/1410))

* {#Marquart02} [[Monika Marquart]], Section A.3 of: _Applications of Dualities in String Theory_, 2002 ([sundoc:02/02H150](https://sundoc.bibliothek.uni-halle.de/diss-online/02/02H150), [pdf](https://sundoc.bibliothek.uni-halle.de/diss-online/02/02H150/prom.pdf))



Classification:

* {#Nikulin10} Viacheslav Nikulin, _Elliptic fibrations on K3 surfaces_, Proceedings of the Edinburgh Mathematical Society, Volume 57 Issue 1 ([arXiv:1010.3904](http://arxiv.org/abs/1010.3904), [doi:10.1017/S0013091513000953](https://doi.org/10.1017/S0013091513000953))


* {#Lecacheux19} O. Lecacheux, _Weierstrass Equations for the Elliptic Fibrations of a K3 Surface_ In: Balakrishnan J., Folsom A., Lalín M., Manes M. (eds.) _Research Directions in Number Theory Association for Women in Mathematics Series, vol 19. Springer (2019) ([doi:10.1007/978-3-030-19478-9_4](https://doi.org/10.1007/978-3-030-19478-9_4))

* Marie Bertin, _Elliptic Fibrations on K3 surfaces_, 2013 ([pdf](https://webusers.imj-prg.fr/~marie-jose.bertin/WINEurope13.pdf))


Discussion in the context of [[K3-spectra]]:

* {#Propp18} Oron Y. Propp, _Constructing explicit K3-spectra_ ([arXiv:1810.08953](https://arxiv.org/abs/1810.08953))

[[!redirects elliptically fibered K3-surfaces]]


[[!redirects elliptic fibration of a K3-surface]]
[[!redirects elliptic fibrations of a K3-surface]]


[[!redirects elliptically fibered complex K3-surface]]
[[!redirects elliptically fibered complex K3-surfaces]]



