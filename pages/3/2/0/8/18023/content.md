
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

By the [[stable Dold-Kan correspondence]], the ([[stable homotopy theory|stable]]) [[homotopy theory]] of _[[rationalization|rationalized]] [[spectra]]_, namely of $H \mathbb{Q}$-[[module spectra]] is [[equivalence of (infinity,1)-categories|equivalent]] to that of [[chain complexes]] of [[modules]]/[[vector space]] over the [[rational numbers]] ([Schwede-Shipley 03, theorem 5.1.6](#SchwedeShipley03)):

$$
  H \mathbb{Q} ModSpectra
   \;\simeq\;
  Ch_\bullet(\mathbb{Q})
  \,.
$$

(Observe that, just as a $\mathbb{Q}$-[[module]] structure on an [[abelian group]] is unique if it exists, so an $H \mathbb{Q}$-[[module spectrum]] structure on a [[spectrum]] is essentially unique if it exists, due to the fact that the multiplication map $H \mathbb{Q} \wedge H \mathbb{Q} \to H \mathbb{Q}$ is an [[equivalence in an (infinity,1)-category|equivalence]].)

This statement parallels that of classical [[rational homotopy theory]], which identifies the [[homotopy theory]] of [[nilpotent topological space|nilpotent]] [[rational topological spaces]] of [[finite type]] with that of cochain [[dgc-algebras]] over $\mathbb{Q}$ in non-negative degree

$$
  \infty Grpd_{\mathbb{Q}, nil,fin}
    \;\simeq\;
  dgcAlg^{\geq 0}_{\mathbb{Q},nil,fin}
$$

in the precise sense that under these two identifications, then the [[stabilization]] [[adjunction]]

$$
  Spectra
    \underoverset
      {\underset{\Omega^\infty}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {\bot}
  \infty Grpd^{\ast/}
$$

is modeled by the [[derived functor|derived]] [[adjunction]] whose [[left adjoint]] sends an [[augmented algebra|augmented]] [[dgc-algebra]] to the underlying [[chain complex]] of its [[augmentation ideal]]

$$
  (dgcAlg^{\geq 2}_{\mathbb{Q}})_{/\mathbb{Q}[0]}
    \underoverset
      {\underset{U \circ ker(\epsilon_{(-)})}{\longrightarrow}}
      {\overset{Sym \circ cn_2}{\longleftarrow}}
      {\bot}
  Ch^{\bullet}(\mathbb{Q})
$$

> add proof

## Related concepts

* [[rational homotopy theory]]

* [[rational parameterized stable homotopy theory]]

* [[rational equivariant homotopy theory]]

* [[rational equivariant stable homotopy theory]]

## References

* {#SchwedeShipley03} [[Stefan Schwede]], [[Brooke Shipley]], _Stable model categories are categories of modules_ , Topology 42 (2003), 103-153 ([pdf](http://www.math.uic.edu/~bshipley/classTopFinal.pdf))


[[!redirects stable rational homotopy theory]]


