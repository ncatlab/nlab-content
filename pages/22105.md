
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Several classes of [[string theory vacua]] require the presence of exactly 24 [[branes]] of [[codimension]] 4 transverse to a [[K3-surface]]-[[fiber]]; this happens notably:

* in [[F-theory]] on an [[elliptically fibered K3-surface]], which requires/implies the presence of 24 [[D7-branes]] ([Sen 96, p. 5](#Sen96)),

* in [[HET-theory]] [[KK-compactification|KK-compactified]] on a [[K3-surface]] with vanishing [[gauge field]] [[instanton number]], which requires/implies the presence of 24 [[NS5-branes]] ([Schwarz 96, p. 50](#Schwarz96)). 

In both cases the condition arises as a kind of [[tadpole cancellation]]-condition, where the charge of the 24 branes in the [[compact topological space|compact]] [[K3]]-fiber space, which naively would be 24 in natural units, cancels out to zero, due to some subtle effect.

Despite the superficial similarity, this subtle effect is, at the face of it, rather different in the two cases:

* for [[F-theory]] it results from the [[Kodeira classification]] of [[elliptic fibrations]], which implies that an [[elliptically fibered K3]] has exactly 24 singular points, counted with multiplicity,

* for [[HET-theory]] it results, via the [[Green-Schwarz mechanism]], from the [[Euler characteristic]] of a [[K3-surface]] being 24, and hence vanishing, via the [[Poincare-Hopf theorem]], after the locus of 24 [[NS5-brane]] loci are cut out.

An argument that these two different-looking mechanisms are in fact equivalent, under suitable [[duality in string theory]], is given in [Braun-Brodie-Lukas-Ruehle 18, Sec. III](#BraunBrodieLukasRuehle18), following detailed analysis due to [Aspinwall-Morrison 97](#AspinwallMorrison97).


### In F-theory on K3
 {#InFTheoryOnK3}


In passing from [[M-theory]] to [[type IIA string theory]], the locus of any [[Kaluza-Klein monopole]] in 11d becomes the locus of [[D6-branes]] in 10d. The locus of the [[Kaluza-Klein monopole]] in turn (as discussed there) is the locus where the $S^1_A$-circle fibration degenerates. Hence in F-theory this is the locus where the fiber of the $S^1_A \times S^1_B$-[[elliptic fibration]] degenerates to the [[nodal curve]]. Since the [[T-duality|T-dual]] of [[D6-branes]] are [[D7-branes]], it follows that [[D7-branes]] in F-theory "are" the singular locus of the elliptic fibration.

Now, considering [[F-theory on K3]], an [[elliptically fibered complex K3-surface]] 

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

Since the order of the poles is 24 (the polynomial degree of the [[discriminant]] $\Delta = 27 g^2 + 4 f^3$, see at _[[elliptically fibered K3-surface]]  -- [singular points](elliptic+fibration+of+a+K3-surface#SingularPoints)_) there are necessarily _24 D7-branes_ ([Sen 96, page 5](#Sen96), [Lerche 99, p. 6](#Lerche99) , see also [Morrison 04, sections 8 and 17](#Morrison04), [Denef 08, around (3.41)](#Denef08), [Douglas-Park-Schnell 14](duality+between+M%2FF-theory+and+heterotic+string+theory#DouglasParkSchnell14)).


Notice that the _net charge_ of these 24 D7-branes is supposed to vanish, due to [[S-duality]] effects (e.g. [Denef 08, below (3.41)](#Denef08)).

### In IIA-theory on K3

Under [[T-duality]] the [above](#InFTheoryOnK3) discussion in [[F-theory]] translates to 24 [[D6-branes]] in [[type IIA string theory]] on [[K3]] ([Vafa 96, Footnote 2 on p. 6](#Vafa96)).

### In HET-theory on K3

In [[heterotic string theory]] [[KK-compactification|KK-compactified]] on [[K3]] with vanishing [[gauge fields]]-[[instanton number]], the existence of exactly 24 [[NS5-branes]] is implied by the [[Green-Schwarz mechanism]]: This requires that the 3-flux density $H_3$ measuring the [[NS5-brane]] charge satisfies $ d H_3 = \trac{1}{2} p_1(\nabla)$; and using that on [[K3]] we have $\int_{K3} \tfrac{1}{2} p_1(\nabla)  = \int_{K3} \chi_4(\nabla) = \chi_4[K3] = 24$ this implies, with [[Stokes' theorem]], that the $H_3$-flux through the [[3-spheres]] around transversal [[NS5-brane]]-punctures of the K3 equals 24
(e.g. [Schwarz 96, around p. 50](duality+in+string+theory#Schwarz97), [Aspinwall-Morrison 97, Sec. 4-5](#AspinwallMorrison97), [Johnson 98, p. 30](#Johnson98), [Braun-Brodie-Lukas-Ruehle 18, Section III.A](#BraunBrodieLukasRuehle18), [Choi-Kobayashi 19, Sec. 1.1](#ChoiKobayashi19)).


The [[duality in string theory|duality]] of this HET-phenomenon with that in F-theory [above](#InFTheoryOnK3) is discussed in [Braun-Brodie-Lukas-Ruehle 18, Section III](#BraunBrodieLukasRuehle18).

### Under Hypothesis H

The vanishing of the [[Euler characteristic]] of K3 after cutting out the [[complement]] of 24 points is precisely the mechanism which witnesses the [[order of a group|order]] 24 of the [[third stable homotopy group of spheres]], seen under [[Pontryagin's theorem]] as the existence of a [[framed manifold|framed]] [[cobordism]] $K3 \setminus 24 \cdot D^4$ between 24 [[3-spheres]]:

\begin{imagefromfile}
    "web": "schreiber",
    "file_name": "24BranesTransversalToK3ViaHypothesisH-20210207.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/M-Theory+as+Mf-Theory)"
\end{imagefromfile}

This relates the number of 24 branes transverse on K3 to [[schreiber:Hypothesis H]]:

\begin{imagefromfile}
    "web": "schreiber",
    "file_name": "KKOn24PuncturedK3ViaHypothesisH-20210207.jpg",
    "width": 760,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/M-Theory+as+Mf-Theory)"
\end{imagefromfile}


## Related concepts

* [[duality between M/F-theory and heterotic string theory]]


## References

### In F-theory

Discussion in [[F-theory]] via the [[Kodeira classification]] of [[elliptically fibered K3s]]:

* {#Sen96} [[Ashoke Sen]], _F-theory and Orientifolds_, Nucl. Phys. B475:562-578, 1996 ([arXiv:hep-th/9605150](http://arxiv.org/abs/hep-th/9605150))

* {#Lerche99} [[Wolfgang Lerche]], [p. 6](https://arxiv.org/pdf/hep-th/9910207.pdf#page=6) of: _On the Heterotic/F-Theory Duality in Eight Dimensions_, In: Baulieu L., Green M., Picco M., Windey P. (eds.) _Progress in String Theory and M-Theory_, NATO Science Series (Series C: Mathematical and Physical Sciences), vol 564. Springer 2001 ([arXiv:hep-th/9910207](https://arxiv.org/abs/hep-th/9910207), [doi:10.1007/978-94-010-0852-5_2](https://doi.org/10.1007/978-94-010-0852-5_2))

* {#Morrison04} [[David Morrison]], _TASI Lectures on Compactification and Duality_ ([arXiv:hep-th/0411120](http://arxiv.org/abs/hep-th/0411120))

* {#Denef08} [[Frederik Denef]], [p. 34](https://arxiv.org/pdf/0803.1194.pdf#page=34) of: _Les Houches Lectures on Constructing String Vacua_, in: _[[String theory and the real world]]_ ([arXiv:0803.1194](http://arxiv.org/abs/0803.1194), [spire:780946](https://inspirehep.net/literature/780946))




* {#DouglasParkSchnell14} [[Michael Douglas]], Daniel S. Park, Christian Schnell, _The Cremmer-Scherk Mechanism in F-theory Compactifications on K3 Manifolds_, JHEP05 (2014) 135 ([arXiv:1403.1595](https://arxiv.org/abs/1403.1595))

### In HET-theory

Discussion in [[heterotic string theory]] via the [[Green-Schwarz mechanism]] on K3 (see also at _[[small instantons]]_):

* {#Schwarz96} [[John Schwarz]], around [p. 50](https://arxiv.org/pdf/hep-th/9607201.pdf#page=51) of: _Lectures on Superstring and M Theory Dualities_, Nucl. Phys. Proc. Suppl. 55B:1-32, 1997 ([arXiv:hep-th/9607201](https://arxiv.org/abs/hep-th/9607201))

* {#Johnson98} [[Clifford Johnson]], _Études on D-Branes_, in: [[Mike Duff]] et. al. (eds.) _Nonperturbative aspects of strings, branes and supersymmetry_, Proceedings, Trieste, Italy, March 23-April 3, 1998 ([arXiv:hep-th/9812196](https://arxiv.org/abs/hep-th/9812196), [spire:481393](https://inspirehep.net/literature/481393))

* {#ChoiKobayashi19} Kang-Sin Choi, Tatsuo Kobayashi, _Transitions of Orbifold Vacua_,   JHEP07 (2019) 111 ([arXiv:1901.11194](https://arxiv.org/abs/1901.11194))


### In F- and HET-theory

Joint discussion in F- and [[duality in string theory|dual]] HET-theory:

* {#AspinwallMorrison97} [[Paul Aspinwall]], [[David Morrison]], _Point-like Instantons on K3 Orbifolds_, Nucl. Phys. B503 (1997) 533-564 ([arXiv:hep-th/9705104](https://arxiv.org/abs/hep-th/9705104), <a href="https://doi.org/10.1016/S0550-3213(97)00516-6">doi:10.1016/S0550-3213(97)00516-6</a>)


* {#BraunBrodieLukasRuehle18} [[Andreas Braun]], Callum Brodie, [[Andre Lukas]], [[Fabian Ruehle]], _NS5-Branes and Line Bundles in Heterotic/F-Theory Duality_, Phys. Rev. D 98, 126004 (2018) ([arXiv:1803.06190](https://arxiv.org/abs/1803.06190), [doi:10.1103/PhysRevD.98.126004](https://doi.org/10.1103/PhysRevD.98.126004))

  > (in the context of [[heterotic line bundles]])

