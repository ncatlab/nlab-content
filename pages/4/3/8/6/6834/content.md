
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An ordinary [[gauge field]] (such as the [[electromagnetic field]] or the fields that induce the [[nuclear force]]) is a [[field (physics)|field (in the sense of physics)]] which is locally represented by a [[differential 1-form]] (the "[[gauge potential]]") and whose [[field strength]] is locally a [[differential 2-form]]. For instance, in the case of the [[electromagnetic field]] this [[differential 2-form]] is the _[[Faraday tensor]]_. 

Roughly speaking, a _higher gauge field_ is similarly a field which is locally represented by [[differential forms]] of higher degree.

An explanation as to why an ordinary [[gauge field]] has a [[gauge potential]] given locally by a [[differential 1-form]] $A$ is that the [[trajectory]] of a [[charged particle]] is a 1-dimensional [[curve]] in [[spacetime]] $X$, its _[[worldline]]_, hence a [[smooth function]] $\gamma \colon \Sigma_1 \to X$, and the canonical way to produce an [[action functional]] on the [[mapping space]] of such curves is the [[integration of differential forms|integration of 1-forms]] over curves:

$$
  \exp(\tfrac{i}{\hbar} S_{gauge})
  \;\colon\;
  \gamma
  \mapsto
  P \exp\left(
    \int_{\Sigma_1} \gamma^\ast A
  \right)
  \,.
$$

This is the _[[parallel transport]]_ map or the _[[holonomy]]_ map, if $\Sigma_1$ is a [[closed manifold|closed manifold]]. The contribution to the [[Euler-Lagrange equation]] of the particle obtained from the [[variational calculus|variation]] of this [[action functional]] is the _[[Lorentz force]]_ which is exerted by the [[background field|background]] [[gauge field]] on the particle.

When one generalizes in this picture from 0-dimensional [[particles]] with 1-dimensional [[worldlines]] to $p$-dimensional particles (often called "[[p-branes]]") with $(p+1)$-dimensional [[worldvolumes]] $\gamma_{p+1} \colon \Sigma_{p+1} \to X$, then one needs, locally, a [[differential n-form|differential (p+1)-form]] $A_{p+1}$ on [[spacetime]] $X$ 

$$
  \exp(\tfrac{i}{\hbar} S_{higher\,gauge})
  \;\colon\;
  \gamma
  \mapsto
  P \exp\left(
    \int_{\Sigma_{p+1}} \gamma_{p+1}^\ast A_{p+1}
  \right)
  \,.
$$

The [[field strength]] or _[[flux]]_ of such a higher gauge field is, accordingly, locally the $(p+2)$-form $F_{p+2}$.

The archetypical example of such a higher gauge field is the (hypothetical) _[[Kalb-Ramond field]]_ or _[[B-field]]_ (a precursor of the [[axion]] field under [[KK-compactification]]) to which the charged 1-brane, the "[[string]]", couples. This is locally a [[differential 2-form]] $B_2$, and the gauge-coupling term in the [[action functional]] for the string is accordingly, locally, of the form

$$
  \exp(\tfrac{i}{\hbar} S_{stringy\,gauge})
  \;\colon\;
  \gamma
  \mapsto
  P \exp\left(
    \int_{\Sigma_{2}} \gamma_2^\ast B_2
  \right)
  \,.
$$

This continues: next one may consider "2-branes", i.e. _[[membranes]]_, and these will couple to a 3-form gauge field. For instance, the membrane which gives the name to _[[M-theory]]_ (the [[M2-brane]]) couples to a 3-form field called the _[[supergravity C-field]]_.

But there is an important further aspect to higher gauge fields which makes this simple picture of higher degree differential forms drastically more rich: 

Where an ordinary [[gauge field]] has [[gauge transformations]] $A_1 \mapsto A'_1$ given locally by smooth functions (0-forms) $\lambda_0$ via the [[de Rham differential]] $d_{dR}$

$$
  A'_1 = A_1 + d_{dR} \lambda_0
$$

so a higher gauge field has [[higher gauge transformations]] given locally by $p$-forms $\lambda_p$:

$$
  A'_{p+1} = A_{p+1} + d_{dR} \lambda_{p}
  \,.
$$

But for $p \geq 0$ then a crucial new effect appears: these gauge transformations, being higher differential forms themselves, have "[[higher gauge transformation|gauge-of-gauge transformations]]" between them, given by lower degree forms.

This phenomenon implies that higher gauge fields have a rich _global_ ("topological") structure, witnessed by the higher analog of their [[instanton sectors]]. Namely, while a higher gauge field to which a [[p-brane]] may couple is _locally_ given by a $(p+1)$-form $A_{p+1}$, as one moves across [[coordinate charts]] this form gauge transforms by a $p$-form, which then itself, as one passes along two charts, transforms by a $(p-1)$-form, and so on.

The global structure for higher gauge fields obtained by carrying out this globalization via [[higher gauge transformations]] is the higher analog of that of a [[fiber bundle]] with [[connection on a bundle]] in [[higher differential geometry]]. This is sometimes known as a _[[gerbe]]_ or, more generally, a _[[principal infinity-bundle]]_.

In fact the situation that there is just one [[gauge potential]] of degree $(p+1)$ with [[field strength]] of degree $(p+2)$ is just the simplest case, the "ordinary" case.  More abstractly one says that such higher gauge fields are [[cocycles]] in _[[ordinary differential cohomology]]_.

More generally it may happen in [[higher gauge theory]] that the gauge potential is a [[formal linear combination]] of differential forms in various degrees.

The canonical example of this phenomenon is the [[RR-field]] in [[string theory]]. This has, locally, a gauge potential which is a differential form in every even degree, or every odd degree. If one is careful about the [[higher gauge transformations]] in this situation to find the correct global structure (the "[[instanton sector]]") of the higher gauge field, then one finds that this now is a [[cocycle]] in a [[differential cohomology|differential]] _[[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]]_, namely, in what is called [[differential K-theory|differential]] [[topological K-theory]]. This may be understood as a higher and generalized form of the famous [[Dirac charge quantization]] condition for the [[electromagnetic field]], see [Freed 00](#Freed00). A lot of the fine detail of the [[anomaly cancellation]] in [[type II string theory]] depends on being careful about the global nature of this [[K-theory|K-theoretic]] higher gauge [[RR-field]] ([Distler-Freed-Moore 09](#DistlerFreedMoore09))


## Examples
 {#Examples}

Among ordinary [[gauge theories]] there is

1. "metric" gauge theory:

   1. [[Maxwell theory]],

   1. [[Yang-Mills theory]]

1. [[topological field theory|topological]] gauge theory:

   * [[Chern-Simons theory]]

(as well as mixed cases, such as the [[ABJM model]]).

While the [[field (physics)|fields]] of these theories are [[gauge fields]] of the same kind in all cases (modeled by [[connection on a bundle|connections]] on [[principal bundles]]), the nature of these theories is different, not the least because the first class depends on (couples to) a [[background field|background]] ([[pseudo-Riemannian metric|pseudo]]) [[Riemannian metric]] ([[gravity]]) while the second does not (is a [[topological field theory]]).

Moreover, even though [[Maxwell theory]] ([[electromagnetism]]) may be understood as the special case of [[Yang-Mills theory]] for [[gauge group]] specialized to the [[circle group]] $U(1)$, this makes a crucial difference for the nature of these theories and their higher generalizations.

Some example of higher gauge fields...

1. ...of higher Maxwell type:

   the fields appearing in higher-dimensional [[supergravity]] theories:

   * [[Kalb-Ramond field]] ([[B-field]])

   * [[RR-field]]

   * [[supergravity C-field]]

1. ...of higher Chern-Simons type:

   * [[AKSZ sigma-models]]

   * [[string field theory|string field]]



### Higher gauge theories of Maxwell type
 {#HigherGaugeTheoryOfMaxwellType}

Consider

* $D = 1 + d \in \mathbb{N}_{\geq 2}$ the [[spacetime]] dimension,

* $X^D$ a $D$-dimensional [[spacetime]] [[smooth manifold|manifold]],

* with [[Hodge star]]-operator on [[differential forms]]

  $$
    \star \,\colon\,
    \Omega^p_{dR}(X^D) \to \Omega^{D-p}_{dR}(X^D)
  $$

  satisfying (see [there](Hodge+star+operator#eq:HodgeSquareOnRiemannian))

  $$
    \star \, \star = - (-1)^{p(D-p)}
    \,,
  $$

* $I \,\in\, Set$ an [[index set]] of flux species 

  (subsuming both electric fluxes and magnetic fluxes, both now allowed of further different species),

* $\big( deg_i \,\in\, \mathbb{N}_{\geq 1} \big)_{i \in I}$ an [[indexed set]] of degrees,

* $\vec F \,\equiv\,\big( F^{(i)} \,\in\, \Omega^{deg_i}_{dR}(X^D) \big)_{i \in I}$ an [[indexed set]] of [[flux densities]]

* $\vec P = \big( P^{(i)}  \big)_{i \in I}$ an [[indexed set]] of graded-symmetric [[polynomials]] in $I$ [[variables]],

* $\vec \mu$ an [[invertible matrix|invertible]] $I \times I$-[[matrix]] 

then the corresponding **higher Maxwell-type equations** on these [[differential forms]]/[[flux densities]] are, in [[duality-symmetric higher gauge theory|duality-symmetric form]] (cf. [SS23](#SS23)): 

1. the system of [[Bianchi identity]] [[differential equations]] (cf. at *[[Gauss law]]*)

   \[
     \label{HigherBianchiIdentities}
     \mathrm{d}\,\vec F 
     \,=\,
     \vec P\big(
       \vec F
     \big)
   \]

1. the self-[[Hodge duality]] condition

   \[
     \label{HigherSelfDuality}
     \star \, \vec F
     \,=\,
     \vec \mu\big(\vec F\big)
     \,.
   \]

The full field content of a higher gauge theory with these flux densities is to involve *[[gauge potentials]]* for these flux densities. A systematic way to get hold of these is to choose a [[flux quantization law]] for the given flux densities, defining a ([[nonabelian cohomology|nonabelian]]) [[generalized cohomology theory]]. Then a full higher gauge field is a [[cocycle]] in the corresponding ([[nonabelian differential cohomology|nonabelian]]) [[differential cohomology]].


### Higher gauge theories of Chern-Simons type

See at *[[schreiber:infinity-Chern-Simons theory]]*



## Related entries

* [[differential nonabelian cohomology]]

* [[Wilson surface]]

* [[local prequantum field theory]]

* [[higher category theory and physics]]

* [[adjusted Weil algebra]]


## References

### General

Introduction and exposition:

* {#BaezHuerta10} [[John Baez]], [[John Huerta]], _An invitation to higher gauge theory_, General Relativity and Gravitation 43 (2011), 2335-2392 ([arXiv:1003.4485](https://arxiv.org/abs/1003.4485))

* [[Luigi Alfonsi]], §2 in: *Higher geometry in physics*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2312.07308](https://arxiv.org/abs/2312.07308)&rbrack;

* [[Leron Borsten]], [[Mehran Jalali Farahani]], [[Branislav Jurčo]], [[Hyungrok Kim]], [[Jiří Nárožný]], [[Dominik Rist]], [[Christian Saemann]], [[Martin Wolf]], *Higher Gauge Theory*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2401.05275](https://arxiv.org/abs/2401.05275)&rbrack;


* PhysicsForums-Insights _[Why higher category theory in physics?](https://www.physicsforums.com/insights/higher-category-theory-physics/)_


* _[[geometry of physics]]_

* _[[twisted smooth cohomology in string theory]]_

* _[Examples of prequantum field theories II: Higher gauge fields](https://www.physicsforums.com/insights/examples-prequantum-field-theories-ii-higher-gauge-fields/)

For technical introduction to the [[RR-field]] as a higher gauge field (for more see at *[[Dirac charge quantization]]*):

* {#Freed00} [[Daniel Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_, Surveys in Differential Geometry, Int. Press, Somerville, MA, 2000, pp. 129&#8211;194 ([arxiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))

* {#DistlerFreedMoore09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))

Deriving [[higher gauge symmetries]] through the [[variational bicomplex]]:

* [[Igor Khavkine]], *Topology, rigid cosymmetries and linearization instability in higher gauge theories*, Annales Henri Poincaré **16** (2015) 255–288, &lbrack;[arXiv:1303.2406](https://arxiv.org/abs/1303.2406), [doi:10.1007/s00023-014-0321-9](https://doi.org/10.1007/s00023-014-0321-9)&rbrack;

The aspect of [[flux quantization laws]]:

* {#SS23} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Flux Quantization on Phase Space]]* &lbrack;[arXiv:2312.12517](https://arxiv.org/abs/2312.12517)&rbrack;


Foundations of higher [[prequantum field theory]]:

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_

For foundations of higher gauge theory formalized in [[homotopy type theory]] see

* [[Urs Schreiber]], [[Mike Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]

On higher gauge theory in [[condensed matter physics]]:

* [[Chenchang Zhu]], Tian Lan, [[Xiao-Gang Wen]], _Topological non-linear σ-model, higher gauge theory, and a realization of all 3+1D topological orders for boson systems_ &lbrack;[arXiv:1808.09394](https://arxiv.org/abs/1808.09394)&rbrack;

* J.P. Ang, Abhishodh Prakash, _Higher categorical groups and the classification of topological defects and textures_, ([ arXiv:1810.12965](https://arxiv.org/abs/1810.12965))

Specifically on [[topological phases of matter]] via higher  [[lattice gauge theory]]:

* [[Joe Huxford]], *The higher lattice gauge theory model for topological phases of matter*, PhD thesis, Oxford (2022) &lbrack;[uuid:e789bf29-179b-4b79-9168-605bf8c035ba](https://ora.ox.ac.uk/objects/uuid:e789bf29-179b-4b79-9168-605bf8c035ba), [pdf](https://ora.ox.ac.uk/objects/uuid:e789bf29-179b-4b79-9168-605bf8c035ba/files/ddj52w5202)&rbrack;

* [[Joe Huxford]], [[Steven H. Simon]], *Excitations in the Higher Lattice Gauge Theory Model for Topological Phases I: Overview* &lbrack;[arXiv:2202.08294](https://arxiv.org/abs/2202.08294)&rbrack;

Further on higher [[lattice gauge theory]]:

* [[Juan Orendain]], [[José A. Zapata]], *Higher homotopy and lattice gauge fields* &lbrack;[arXiv:2311.02363](https://arxiv.org/abs/2311.02363)&rbrack;




[[!include higher gauge theory of the Green-Schwarz mechanism -- references]]



[[!redirects higher gauge fields]]

[[!redirects higher gauge theory]]
[[!redirects higher gauge theories]]

[[!redirects higher gauge symmetry]]
[[!redirects higher gauge symmetries]]

