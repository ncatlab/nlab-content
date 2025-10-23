
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
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

The _Polyakov action functional_ or _energy functional_ is a standard [[kinetic action|kinetic]] [[action functional]] for [[sigma models]] with [[worldvolume]] $(\Sigma,g)$ and [[target spacetime]] $(X,\mu)$ ([[pseudo-Riemannian manifold|pseudo]])[[Riemannian manifolds]]. Its [[critical points]] are the [[harmonic maps]] from $\Sigma$ to $X$

With a suitable "[[worldvolume]] [[cosmological constant]]" added and with the worldvolume metric "integrated out", then the Polyakov action is [[classical field theory|classically]] equivalent to the [[Nambu-Goto action]] functional, which is simply the "proper volume" function for images of $\Sigma$ in $Y$. But as opposed to the Nambu-Goto action the Polyakov action is quadratic in derivatives. Therefore it lends itself better to [[perturbation theory]] of [[scattering amplitudes]] -- where the kinetic contributions have to be [[Gaussian integrals]] -- such as in [[worldline formalism]] for [[quantum field theory]] as well as in [[perturbative string theory]].

On the other hand, the [[Nambu-Goto action]] lends itself better to generalizations such as the [[Dirac-Born-Infeld action]] for [[D-branes]].

## Definition

Let 

* $p \in \mathbb{N}$ (for [[p-brane]] dynamics),

* $(X,\mu)$ a [[pseudo-Riemannian manifold]] ([[target spacetime]]),

* $\Sigma$ a [[compact topological space|compact]] [[smooth manifold]] ([[manifold with boundary|with boundary]]) of dimension $(p+1)$ ([[worldvolume]]),

* $[\Sigma,X]$ the [[diffeological space]] of [[smooth functions]] $\Sigma \to X$,

* $Met(\Sigma)$ the [[moduli space]] of ([[pseudo-Riemannian metrics|pseudo]])[[Riemannian metrics]] $g$ on $\Sigma$.

The Polyakov action is the [[smooth function]]

$$
  S_{Pol}
  \;\colon\;
  [\Sigma,X]\times Met(\Sigma)
  \longrightarrow
  \mathbb{R}
$$

which on a map $\phi \colon \Sigma \to X$ and a metric $g$ on $\Sigma$ is given by the [[integral]]

$$
  S_{Pol}(\phi,g)
  \coloneqq
  \int_\Sigma
    \Vert d\phi\Vert^2    
  dvol_g
$$

where the [[derivative]] $d \phi \in \Gamma(T^\ast \Sigma\otimes \phi^\ast T X)$, and where the [[norm]] $\Vert - \Vert$ is given jointly by the metrics $g$ and $\mu$ of $\Sigma$ and $X$.

When both $\Sigma$ and $X$ are covered by single [[coordinate charts]] $(\sigma^a)_{a = 0}^p$ and $(x^\mu)$, then this reads

$$
  S_{Pol}(\phi,g)
  =
  \int_{\Sigma}
  \sqrt{det g}
  \left(
     g^{a b} \eta_{\mu \nu} (\partial_a \phi^\mu) (\partial_b \phi^\nu)
  \right)
  d \sigma^0 \cdots d \sigma^p
$$

with a sum over repeated indices understood. Here $det g$ denotes the [[absolute value]] of the [[determinant]] of $(g_{a b})$ (often written $-det g$ in the pseudo-Riemannian case.)

## Properties

### Relation to Nambu-Goto action
  {#RelationToNambuGotoAction}

The Polyakov action with a suitable worldvolume cosmological constant term added is classically equivalent to the [[Nambu-Goto action]] (e.g. [Nieto 01, section 2](#Nieto01)).

This [[shell|on-shell]] equivalence is exhibited by the smooth function 

$$
  \tilde S
  \;\colon\;
  [\Sigma,X] \times Met(\Sigma)\times \Gamma(T \Sigma \otimes T \Sigma \otimes Dens \Sigma)
  \longrightarrow \mathbb{R}
$$

which on a triple $(\phi,g,\Lambda)$ is given by 

$$
  \tilde S(\phi,g,\Lambda)
  \coloneqq
  \int_\Sigma
  \left(
    dvol(g) + \Lambda( \vert d \phi \vert^2 - g)
  \right)
  \,,
$$

where now $\vert d\phi \vert^2$ denotes the square norm only with respect to the metric on $X$. 

Because, on the one hand, the [[equations of motion]] induced by $\tilde S$ for variation of $\Lambda$ are

$$
  \vert d \phi \vert^2 - g = 0
$$

and substituting that constraint back into $\tilde S$ gives the [[Nambu-Goto action]]. On the other hand, the equations of motion induced by $\tilde S$ for variation of $g$ are

$$
  \tfrac{1}{2}g^{-1}dvol(g) - \Lambda = 0
$$

and substituting that back into $\tilde S$ gives 

$$
  \tfrac{1}{2}\int_\Sigma 
  \left(
    \Vert d \phi\Vert^2
    +
    (p-1)
  \right)
  dvol(g)
$$

which is the Polyakov action with "[[cosmological constant]]" $(p-1)$.

(So the case where this cosmological constant correction disappears is $p = 1$ corresponding to the [[string]].)

## Related concepts

* [[minimal surface]]

* [[bosonic string]]

* [[Liouville theory]]

* [[Nambu-Goto action]]

## References

The Polyakov action  is named after

* [[Alexander Polyakov]], *Quantum geometry of bosonic strings*, Phys. Lett. B **103** (1981) 207-210 &lbrack;<a href="https://doi.org/10.1016/0370-2693(81)90743-7">doi:10.1016/0370-2693(81)90743-7</a>, [pdf](http://qft.itp.ac.ru/polyakov-2.pdf)&rbrack;

where it is discussed for the [[bosonic string]] and related to [[Liouville theory]], and

* [[Alexander Polyakov]], *Quantum geometry of fermionic strings*, Physics Letters B **103** 3 (1981) 211-213 &lbrack;<a href="https://doi.org/10.1016/0370-2693(81)90744-9">doi:10.1016/0370-2693(81)90744-9</a>&rbrack;

where it is generalized to the [[superstring]], but in fact (cf. [Polyakov (2008), p. 3](Alexander+Polyakov#Polyakov08)) it originates already in discussion of the [[spinning string]] in:

* [[Stanley Deser]], [[Bruno Zumino]], *A complete action for the spinning string*, Physics Letters B **65** 4 (1976) 369-373 &lbrack;<a href="https://doi.org/10.1016/0370-2693(76)90245-8">doi:10.1016/0370-2693(76)90245-8</a>[pdf](http://cdsweb.cern.ch/record/201648/files/CM-P00061857.pdf?version=1)&rbrack;

* [[Lars Brink]], [[Paolo Di Vecchia]], [[Paul Howe]], _A locally supersymmetric and reparametrization invariant action for the spinning string_ , Physics Letters B **65** Issue 5, 20 (1976) 471-474 &lbrack;<a href="https://doi.org/10.1016/0370-2693(76)90445-7">doi:10.1016/0370-2693(76)90445-7</a>&rbrack;
 

Further early discussion of the Polyakov action:

* [[Jean-Loup Gervais]], [[André Neveu]], *The dual string spectrum in Polyakov's quantization (I)*, Nuclear Physics B **199** 1 (1982) 59-76 &lbrack;<a href="https://doi.org/10.1016/0550-3213(82)90566-1">doi:10.1016/0550-3213(82)90566-1</a>&rbrack;

* [[Jean-Loup Gervais]], [[André Neveu]], *Dual string spectrum in Polyakov's quantization (II). Mode separation*, Nuclear Physics B **209** 1 (1982) 125-145 &lbrack;<a href="https://doi.org/10.1016/0550-3213(82)90105-5">doi:10.1016/0550-3213(82)90105-5</a>&rbrack;

* {#Nag96} Subhashis Nag, *Mathematics in and out of String Theory*, Topology and Teichmüller Spaces (1996) 187-220 &lbrack;[arXiv:alg-geom/9512010](https://arxiv.org/abs/alg-geom/9512010), [doi:10.1142/9789814503921_0011](https://doi.org/10.1142/9789814503921_0011)&rbrack;


and further discussion of the related [[Liouville theory]]:

* [[Colin Guillarmou]], [[Rémi Rhodes]], [[Vincent Vargas]], *Polyakov's formulation of 2d bosonic string theory*, Publ. Math. IHES **130** (2019) 111–185 &lbrack;[arXiv:1607.08467](https://arxiv.org/abs/1607.08467), [doi:10.1007/s10240-019-00109-6](https://doi.org/10.1007/s10240-019-00109-6)&rbrack;


Detailed discussion of the relation to the [[Nambu-Goto action]] and the [[Dirac-Born-Infeld action]]

* {#Nieto01} J. A. Nieto, _Remarks on Weyl invariant p-branes and Dp-branes_ ([arXiv:hep-th/0110227](http://arxiv.org/abs/hep-th/0110227))

Review:

* [[Igor Dolgachev]], pp, 43, 51 in: *Introduction to string theory for mathematicians*, lecture at *[1999 Summer on Algebraic Geometry and Physics](https://people.sissa.it/~bruzzo/sagp99/sagp.html)* (1999) &lbrack;[pdf](https://dept.math.lsa.umich.edu/~idolga/stringy.pdf), [[Dolgachev-IntroductionStringTheory.pdf:file]]&rbrack;

and mathematical details:

* [[Jürgen Jost]], *Bosonic Strings: A Mathematical Treatment*, AMS/IP Stud. Adv. Math. **21** (2001) &lbrack;[ISBBN:978-0-8218-4336-9](https://bookstore.ams.org/view?ProductCode=AMSIP/21.S.B), [spire:1388134](https://inspirehep.net/literature/1388134)&rbrack;

See also 

* Wikipedia, _[Polyakov action](https://en.wikipedia.org/wiki/Polyakov_action)_


Discussion of the Polyakov action and [[Nambu-Goto action]] on [[worldsheets]] with [[manifold with boundary|boundary]] (i.e. in the generality of [[open strings]]) and cast in [[BV-BRST formalism]]:

* {#MartinoliSchiavina22} S. Martinoli, [[Michele Schiavina]], *BV analysis of Polyakov and Nambu–Goto theories with boundary*,  Lett. Math. Phys. **112** 35 (2022) &lbrack;[doi:10.1007/s11005-022-01526-1](https://doi.org/10.1007/s11005-022-01526-1), [arXiv:2106.02983](https://arxiv.org/abs/2106.02983)&rbrack;


On the Polyakov model as the continuum limit of a sequence of particles coupled by [[harmonic oscillator|harmonic]] nearest neighbour interaction:

* [[Leonard Susskind]]: (24) ff in: *Structure of Hadrons Implied by Duality*, Phys. Rev. D **1** (1970) 1182 &lbrack;[doi:10.1103/PhysRevD.1.1182](https://doi.org/10.1103/PhysRevD.1.1182)&rbrack;

  > (often credited as one of the origins of [[string theory]])

* [[Igor Klebanov]], [[Leonard Susskind]]: *Continuum Strings From Discrete Field Theories*, Nucl. Phys. B **309** (1988) 175-187 &lbrack;<a href="10.1016/0550-3213(88)90237-4">doi:10.1016/0550-3213(88)90237-4</a>&rbrack;


* Renann Lipinski Jusinskas: *Strings as particle arrays* &lbrack;[arXiv:2407.08638](https://arxiv.org/abs/2407.08638)&rbrack;



[[!redirects Polyakov action functional]]

[[!redirects energy functional]]