
> This entry is about [[M-theory]]/[[F-theory]] [[KK-compactification|compactified]] on [[K3-surfaces]]. For [[M-theory]] on [[MO9]]-planes see instead at _[[Hořava-Witten theory]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[duality in string theory]]. The [[non-perturbative effect|non-perturbative]] enhancement of [[duality between heterotic and type II string theory]]:

[[F-theory]]$\,$ "[[KK-compactification|KK-compactified]]" on an [[elliptic fibration|elliptically fibered]] [[K3]] with a [[section]] is supposed to be equivalent to [[heterotic string theory]] [[KK-compactification|KK-compactified]] on a [[2-torus]]. 

More generally, [[F-theory]] on a [[complex manifold|complex]] $n$-dimensional $X$ fibered $X\to B$ with elliptic [[K3]]-[[fibers]] is supposed to be equivalent to [[heterotic string theory]] on an [[elliptic fibration|elliptically fibered]] [[Calabi-Yau manifold]] $Z \to B$ of [[complex manifold|complex]] [[dimension]] $(n-1)$.

A detailed discussion of the [[equivalence]] of the respective [[moduli spaces]] is originally due to ([Friedman-Morgan-Witten 97](#FriedmanMorganWitten97)). A review of this is in ([Donagi 98](#Donagi98)).


From the abstract of ([Donagi 98](#Donagi98)).

> The [[heterotic string theory|heterotic string]] [[KK-compactification|compactified]] on an $(n-1)$-[[dimension|dimensional]] [[elliptic fibration|elliptically fibered]] [[Calabi-Yau variety|Calabi-Yau]] $Z \to B$ is conjectured to be [[duality in string theory|dual]] to [[F-theory]] [[KK-compactification|compactified]] on an $n$-dimensional [[Calabi-Yau variety|Calabi-Yau]] $X \to B$, fibered over the same base with [[elliptic fibration|elliptic]] [[K3]] fibers. In particular, the [[moduli]] of the two theories should be [[isomorphism|isomorphic]]. The cases most relevant to the physics are $n=2$, $3$, $4$, i.e. the [[KK-compactification|compactification]] is to [[dimensions]] $d=8$, $6$ or $4$ respectively. Mathematically, the richest picture seems to emerge for $n=3$, where the [[moduli space]] involves an analytically [[integrable system]] whose fibers admit rather different descriptions in the two theories.



## Aspects

### Singular locus of the elliptic fibration and 24 D7-branes
 {#SingularLocusAndD7Branes}

In passing from [[M-theory]] to [[type IIA string theory]], the locus of any [[Kaluza-Klein monopole]] in 11d becomes the locus of [[D6-branes]] in 10d. The locus of the [[Kaluza-Klein monopole]] in turn (as discussed there) is the locus where the $S^1_A$-circle fibration degenerates. Hence in F-theory this is the locus where the fiber of the $S^1_A \times S^1_B$-[[elliptic fibration]] degenerates to the [[nodal curve]]. Since the [[T-duality|T-dual]] of [[D6-branes]] are [[D7-branes]], it follows that [[D7-branes]] in F-theory "are" the singular locus of the elliptic fibration.

Now an [[elliptically fibered complex K3-surface]] 

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

\begin{imagefromfile}
        "file_name": "K3CobordismBetween24ThreeSpheres.jpg",
        "web": "nlab",
        "width": 260,
        "unit": "px",
        "float": "right",
        "margin": {
            "top": -40,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting the homotopy Whitehead integral",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

Since the order of the poles is 24 (the polynomial degree of the [[discriminant]] $\Delta = 27 g^2 + 4 f^3$, see at _[[elliptically fibered K3-surface]]  -- [singular points](elliptic+fibration+of+a+K3-surface#SingularPoints)_) there are necessarily _24 D7-branes_ ([Sen 96, page 5](#Sen96), [Sen 97b](#Sen97b), see also [Morrison 04, sections 8 and 17](#Morrison04), [Denef 08, around (3.41)](#Denef08), [Douglas-Park-Schnell 14](duality+between+M%2FF-theory+and+heterotic+string+theory#DouglasParkSchnell14)).

Under [[T-duality]] this translates to 24 [[D6-branes]] in [[type IIA string theory]] on [[K3]] ([Vafa 96, Footnote 2 on p. 6](#Vafa96)).

Notice that the _net charge_ of these 24 D7-branes is supposed to vanish, due to [[S-duality]] effects (e.g. [Denef 08, below (3.41)](#Denef08)).

(This reminds one of the situation for the [[third stable homotopy group of spheres]]...)

For analogous discussion of 24 NS5-branes in [[heterotic string theory]] on [[K3]] see [Schwarz 97, around p. 50](duality+in+string+theory#Schwarz97).

For more see at _[[24 branes transverse to K3]]_.


### From M-branes to F-branes to heterotic strings and NS5-branes

[[!include F-branes -- table]]

### Non-reducible heterotic $E_8$-gauge backgrounds
 {#NonReducibleHeteroticGaugeBackgrounds}

There are some [[F-theory]] backgrounds whose supposed dual in [[heterotic string theory]] involves an [[E8]]-[[principal connection]] which is not [[reduction of the structure group|reducible]] to [[SemiSpin(16)]] ([Distler-Sharpe 10, section 5](#DistlerSharpe10)), while in fact the traditional construction of the heterotic [[worldsheet]] theory only covers this case. In ([Distler-Sharpe 10, section 7-8](#DistlerSharpe10)) it is argued that therefore a more general formulation of [[heterotic string theory]] needs to involve [[parameterized WZW models]]. See also at _[heterotic string -- Properties -- General gauge backgrounds and parameterized WZW models](http://ncatlab.org/nlab/show/heterotic+string+theory#GeneralGaugeBackgroundsAndParameterizedWZWModels)_.


## Related concepts

* [[24 branes transverse to K3]]

\linebreak

[[!include F-theory compactifications -- table]]

\linebreak

[[!include KK-compactifications of M-theory -- table]]


## References

### For type IIA and M-theory

The conjectured duality between [[type IIA string theory]] [[KK-compactification|KK-compactified]] on [[K3]] times an [[n-torus]] and [[heterotic string theory]] on the $(n+2)$-torus is originally due to

* [[Chris Hull]], [[Paul Townsend]], section 6 of: _Unity of Superstring Dualities_, Nucl. Phys. B438:109-137, 1995 ([arXiv:hep-th/9410167](http://arxiv.org/abs/hep-th/9410167))

* {#Witten95} [[Edward Witten]], section 4 of: _[[String Theory Dynamics In Various Dimensions]]_, Nucl. Phys. B443:85-126, 1995 ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))


* {#Lerche99} [[Wolfgang Lerche]], _On the Heterotic/F-Theory Duality in Eight Dimensions_, In: Baulieu L., Green M., Picco M., Windey P. (eds.) _Progress in String Theory and M-Theory_, NATO Science Series (Series C: Mathematical and Physical Sciences), vol 564. Springer 2001 ([arXiv:hep-th/9910207](https://arxiv.org/abs/hep-th/9910207), [doi:10.1007/978-94-010-0852-5_2](https://doi.org/10.1007/978-94-010-0852-5_2))


Review:

* [[Paul Aspinwall]], [[David Morrison]], _String Theory on K3 Surfaces_, in [[Brian Greene]], [[Shing-Tung Yau]] (eds.), _Mirror Symmetry II_, International Press, Cambridge, 1997, pp. 703-716 ([arXiv:hep-th/9404151](https://arxiv.org/abs/hep-th/9404151))


* {#Aspinwall96} [[Paul Aspinwall]], _K3 Surfaces and String Duality_, in  [[Shing-Tung Yau]] (ed.): _Differential geometry inspired by string theory_ 1-95 ([arXiv:9611137](https://arxiv.org/abs/hep-th/9611137) [spire:426102](http://inspirehep.net/record/426102))

Further discussion:

* [[Paul Aspinwall]], _Enhanced Gauge Symmetries and K3 Surfaces_, Phys.Lett. B357 (1995) 329-334 ([arXiv:hep-th/9507012](http://arxiv.org/abs/hep-th/9507012))

* [[Eric Bergshoeff]], C. Condeescu, G. Pradisi, F. Riccioni, _Heterotic-Type II duality and wrapping rules_, JHEP12(2013)057 ([arXiv:1311.3578](https://arxiv.org/abs/1311.3578))




Specifically in relation to the putative [[K-theory]]-classification of [[D-brane charge]]:

* {#GarciaUranga05} Inaki Garcia-Etxebarria, [[Angel Uranga]], _From F/M-theory to K-theory and back_, JHEP 0602:008,2006 ([arXiv:hep-th/0510073](https://arxiv.org/abs/hep-th/0510073))


Specifically in [[M-theory on G2-manifolds]]:

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] section 6.4 of _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

* [[Bobby Acharya]], Alex Kinsella, [[David Morrison]], *Non-Perturbative Heterotic Duals of M-Theory on $G_2$ Orbifolds* ([arXiv:2106.03886](https://arxiv.org/abs/2106.03886))

Specifically in relation to [[Moonshine]]:

* [[Miranda Cheng]], Sarah M. Harrison, Roberto Volpato, Max Zimet, _K3 String Theory, Lattices and Moonshine_ ([arXiv:1612.04404](https://arxiv.org/abs/1612.04404))


### For F-theory

Discussion for [[F-theory]] includes

* {#MorrisonVafa96a} [[David Morrison]], [[Cumrun Vafa]], _Compactifications of F-Theory on Calabi--Yau Threefolds -- I_, Nucl. Phys. B473 (1996) 74-92 ([arXiv:hep-th/9602114](http://arxiv.org/abs/hep-th/9602114))

* {#MorrisonVafa96b} [[David Morrison]], [[Cumrun Vafa]], _Compactifications of F-Theory on Calabi--Yau Threefolds -- II_, Nucl. Phys. B476:437-469, 1996 ([arXiv:hep-th/9603161](http://arxiv.org/abs/hep-th/9603161))

* {#Sen96} [[Ashoke Sen]], _F-theory and Orientifolds_ ([arXiv:hep-th/9605150](http://arxiv.org/abs/hep-th/9605150))

* {#FriedmanMorganWitten97} Robert Friedman, [[John Morgan]], [[Edward Witten]], _Vector Bundles And F Theory_, Commun.Math.Phys.187:679-743, 1997 ([arXiv:hep-th/9701162](http://arxiv.org/abs/hep-th/9701162))

* {#Aspinwall97} [[Paul Aspinwall]], _M-Theory Versus F-Theory Pictures of the Heterotic String_, Adv.Theor.Math.Phys.1:127-147, 1998 ([arXiv:hep-th/9707014](http://arxiv.org/abs/hep-th/9707014))

Review of ([Friedman-Morgan-Witten 97](#FriedmanMorganWitten97)) is in

* {#Donagi98} [[Ron Donagi]], _ICMP lecture on heterotic/F-theory duality_ ([arXiv:hep-th/9802093](http://arxiv.org/abs/hep-th/9802093))

* Bj&#246;rn Andreas, _$N=1$ Heterotic/F-theory duality_, PhD thesis ([pdf](http://edoc.hu-berlin.de/dissertationen/physik/andreas-bjoern/PDF/Andreas.pdf))

with more details in 

* {#DonagiMarkman95} [[Ron Donagi]], [[Eyal Markman]], _Spectral curves, algebraically completely integrable Hamiltonian systems, and moduli of bundles_ ([arXiv:alg-geom/9507017](http://arxiv.org/abs/alg-geom/9507017))

The issue with non-reducible $E_8$-gauge connections is highligted in 

* {#DistlerSharpe10} [[Jacques Distler]], [[Eric Sharpe]], section 5 of _Heterotic compactifications with principal bundles for general groups and general levels_, Adv. Theor. Math. Phys. 14:335-398, 2010 ([arXiv:hep-th/0701244](http://arxiv.org/abs/hep-th/0701244))

On a subtlety in the application of the [[Narasimhan-Seshadri theorem]] in the duality:

* Herbert Clemens, Stuart Raby, _Heterotic/F-theory Duality and Narasimhan-Seshadri Equivalence_ ([arxiv:1906.07238](https://arxiv.org/abs/1906.07238))

See also

* {#DouglasParkSchnell14} [[Michael Douglas]], Daniel S. Park, Christian Schnell, _The Cremmer-Scherk Mechanism in F-theory Compactifications on K3 Manifolds_, JHEP05 (2014) 135 ([arXiv:1403.1595](https://arxiv.org/abs/1403.1595))

### For both

* Yusuke Kimura, _New perspectives in the duality of M-theory, heterotic strings, and F-theory_ ([arXiv:2103.03088](https://arxiv.org/abs/2103.03088))






[[!redirects duality between F-theory and heterotic string theory]]

[[!redirects F/M-theory on elliptically fibered Calabi-Yau 2-folds]]

[[!redirects duality between heterotic string theory and M/F-theory]]

[[!redirects duality between heterotic string theory and F-theory]]

[[!redirects F-theory on K3]]
