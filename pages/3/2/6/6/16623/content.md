
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

Membrane [[instantons]] are constituted by [[supermembranes]] ([[M2-branes]])  [[wrapped brane|wrapped]] on [[spacelike]] (and [[supersymmetric cycle|supersymmetric]]) [[cycles]]. Also known as _[[SM2-branes]]_.

These appear as [[non-perturvative effects]] in [[M-theory]] [[model (physics)|model building]]. For instance they generate the [[hierarchy problem|gauge hierarchy]] in constructions of [[M-theory on G₂-manifolds]] such as the [[G₂-MSSM]].

Basically the effect is that the [[action functional]] of the given [[11-dimensional supergravity]] is multiplied by the exponentiated [[Nambu-Goto action]] of the [[wrapped brane|wrapping]] membrane configurations $\phi \colon \Sigma \to X$. These are of the form (e.g. [Harvey-Moore 99, (4.13)](#HarveyMoore99), [Atiyah-Witten 01 (4.17)](#AtiyahWitten01), [Curio 02, (2.15)](#Curio02))

$$
  \exp\left(
    \int_{\Sigma} 
    \left(
      \ell_P^{-3} vol(\phi^\ast g) + i \phi^\ast C 
    \right)
  \right)
  \,,
$$

where $\ell_P$ is the [[Planck length]] of [[11-dimensional supergravity]], $T = 1/\ell^3$ is the membrane [[tension]], $C$ is the [[background field|background]] [[supergravity C-field]], $g$ the background [[metric]] and $vol$ its [[volume form]], .  

## Properties

### Relation to worldsheet and D-brane instantons

Under the [[duality between M-theory and type IIA string theory]], membrane instantons become string [[worldsheet instantons]] or [[D-brane]] instantons, depending on whether they [[wrapped brane]] wrape the M-theory circle fiber or not. See at _[[non-perturbative effect]]_ the section _[Worldsheet and brane instantons](https://ncatlab.org/nlab/show/non-perturbative+effect#WorldsheetAndBraneInstantons)_ for more.

### Relation to complex volume

When here $(\Sigma, \phi^\ast g)$ is a [[hyperbolic 3-manifold]] and $\phi^\ast C = CS(\omega)$ is the [[Chern-Simons form|Chern-Simons invariant]] then this is the exponentiated "[[complex volume]]" of $\Sigma$[^footnote].



## Related concepts

* [[hierarchy problem]]

* [[non-perturbative effect]]

* [[complex volume]]

* [[associative submanifold]]

* [[D3-brane instanton]]

* [[M5-brane instanton]]

[[!include table of branes]]

## References

* [[Katrin Becker]], [[Melanie Becker]], [[Andrew Strominger]], section 2.1 of _Five-branes, membranes and nonperturbative string theory_, Nucl. Phys. B 456, 130 (1995) ([hep-th/9507158](http://arxiv.org/abs/hep-th/9507158))

* {#HarveyMoore99} [[Jeff Harvey]], [[Greg Moore]], _Superpotentials and Membrane Instantons_ ([arXiv:hep-th/9907026](http://arxiv.org/abs/hep-th/9907026), [spire:503172](http://inspirehep.net/record/503172))

Discussion specifically for [[M-theory on G₂-manifolds]] includes

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]], around (4.17) of _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

* {#Curio02} [[Gottfried Curio]], _Superpotentials for M-theory on a $G_2$ holonomy manifold and Triality symmetry_, JHEP 0303:024,2003 ([arXiv:hep-th/0212211](http://arxiv.org/abs/hep-th/0212211))

Discussion related to the [[cosmological constant]] in models of [[M-theory on G₂-manifolds]] includes

* {#CarlosLukasMorris04} Beatriz de Carlos, Andre Lukas, Stephen Morris, _Non-perturbative vacua for M-theory on $G_2$ manifolds_, JHEP 0412:018, 2004 ([arxiv:hep-th/0409255](https://arxiv.org/abs/hep-th/0409255))

which concludes that with taking [[non-perturbative effects]] from membrane instantons into account one gets 4d vacua with vanishing and negative [[cosmological constant]] ([[Minkowski spacetime]] and [[anti-de Sitter spacetime]]) but not with positive [[cosmological constant]] ([[de Sitter spacetime]]). They close by speculating that [[M5-brane]] instantons might yield [[de Sitter spacetime]].


[^footnote]: This relation was pointed out by [[Hisham Sati]].

[[!redirects membrane instantons]]

[[!redirects M2-instanton]]
[[!redirects M2-instantons]]

[[!redirects M2-brane instanton]]
[[!redirects M2-brane instantons]]
