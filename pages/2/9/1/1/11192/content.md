
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _T-duality 2-group_ is a [[smooth 2-group]] (or rather a class of such) which controls [[T-duality]] and [[T-folds]]. It is the [[string 2-group]] for the [[cup product]] [[universal characteristic class]] on [[fiber products]] of [[torus]]-[[fiber bundles]] with their dual [[torus]]-[[principal bundles]].

## Definition

For $T$ a [[torus]] and $\tilde T$ its dual torus, there is the [[cup product]] [[universal characteristic class]]

$$
  \langle -\cup -\rangle \;\colon\;B T \times B \tilde T \longrightarrow K(\mathbb{Z}, 4)
  \,.
$$

This has a smooth refinement to morphism of [[smooth groupoids]]/[[moduli stacks]]

$$
  \langle -\cup -\rangle \;\colon\;\mathbf{B} T \times \mathbf{B} \tilde T \longrightarrow \mathbf{B}^3 U(1)
  \,.
$$

In fact it has furthermore a differential refinement to a [[universal Chern-Simons circle 3-bundle with connection]]

$$
  \langle -\cup -\rangle_{conn} \;\colon\;(\mathbf{B} T \times \mathbf{B} \tilde T)_{conn} \longrightarrow \mathbf{B}^3 U(1)_{conn}
$$

of which the above is obtained by forgetting the connections ([FSS 12, section 3.2.1](#FSS12))

As such this is the [[local Lagrangian]] of abelian [[Chern-Simons theory]] with two abelian gauge field species (the [[diagonal]] is 3d abelian CS theory itself).

This universal class is suitably equivariant under the action of the integral T-duality group $O(n,n,\mathbb{Z})$, so that one may consider ([Nikolaus 14](#Nikolaus14))

$$
  \langle -\cup -\rangle \;\colon\;\mathbf{B} T \times \mathbf{B} \tilde T // O(n,n,\mathbb{Z}) \longrightarrow \mathbf{B}^3 U(1)
  \,.
$$

As for the [[string 2-group]], this defines an [[infinity-group extension]] (the looping of the [[homotopy fiber]] of this map) and this one may call the _T-duality 2-group_ as it controls T-duality pairs by the discussion at _[[T-Duality and Differential K-Theory]]_. Indeed, according to ([Nikolaus 14](#Nikolaus14)) the [[principal 2-bundles]] for this 2-group are the correct formalization of the concept of _[[T-folds]]_.

## Related concepts

* [[T-duality]], [[topological T-duality]]

* [[string 2-group]]

## References

* {#FSS12} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_, Journal of Geometry and Physics, Volume 74, 2013, Pages 130&#8211;163 ([arXiv:1207.5449](http://arxiv.org/abs/1207.5449))

* {#Nikolaus14} [[Thomas Nikolaus]], _[[T-Duality in K-theory and Elliptic Cohomology]]_, talk at _String Geometry Network Meeting_, Feb 2014, ESI Vienna ([website](http://www.ingvet.kau.se/juerfuch/conf/esi14/esi14_34.html))

* {#NikolausWaldorf18} [[Thomas Nikolaus]], [[Konrad Waldorf]], _Higher geometry for non-geometric T-duals_ ([arXiv:1804.00677](https://arxiv.org/abs/1804.00677))

See also:

* [[Nora Ganter]], _Categorical Tori_, SIGMA 14 (2018), 014, 18 ([arXiv:1406.7046](https://arxiv.org/abs/1406.7046))



[[!redirects T-duality Lie 2-group]]
[[!redirects T-duality Lie 2-algebra]]
