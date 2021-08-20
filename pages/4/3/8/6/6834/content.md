
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

* [[Kalb-Ramond field]]

* [[RR-field]]

* [[supergravity C-field]]

* [[string field theory|string field]]

* [[AKSZ sigma-model]]

## Related entries

* [[Wilson surface]]

* [[local prequantum field theory]]

* [[higher category theory and physics]]

## References

### General

Introduction and exposition includes

* {#BaezHuerta10} [[John Baez]], [[John Huerta]], _An invitation to higher gauge theory_, General Relativity and Gravitation 43 (2011), 2335-2392 ([arXiv:1003.4485](https://arxiv.org/abs/1003.4485))

* PhysicsForums-Insights _[Why higher category theory in physics?](https://www.physicsforums.com/insights/higher-category-theory-physics/)_

* _[[geometry of physics]]_

* _[[twisted smooth cohomology in string theory]]_

* _[Examples of prequantum field theories II: Higher gauge fields](https://www.physicsforums.com/insights/examples-prequantum-field-theories-ii-higher-gauge-fields/)

For technical introduction to the [[RR-field]] as a higher gauge field (for more see at *[[Dirac charge quantization]]*):

* {#Freed00} [[Daniel Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_, Surveys in Differential Geometry, Int. Press, Somerville, MA, 2000, pp. 129&#8211;194 ([arxiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))

* {#DistlerFreedMoore09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))


For foundations of higher [[prequantum field theory]] see 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_

For foundations of higher gauge theory formalized in [[homotopy type theory]] see

* [[Urs Schreiber]], [[Mike Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]

For higher gauge theory in [[condensed matter physics]] see

* Chenchang Zhu, Tian Lan, Xiao-Gang Wen, _Topological non-linear σ-model, higher gauge theory, and a realization of all 3+1D topological orders for boson systems_, ([arXiv:1808.09394](https://arxiv.org/abs/1808.09394))

* J.P. Ang, Abhishodh Prakash, _Higher categorical groups and the classification of topological defects and textures_, ([ arXiv:1810.12965](https://arxiv.org/abs/1810.12965))



[[!include higher gauge theory of the Green-Schwarz mechanism -- references]]



[[!redirects higher gauge fields]]

[[!redirects higher gauge theory]]
[[!redirects higher gauge theories]]

[[!redirects higher gauge symmetry]]
[[!redirects higher gauge symmetries]]

