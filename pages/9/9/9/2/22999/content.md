
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

In [[equivariant cohomology|equivariant]] generalization of how the [[universal principal bundle]] with [[structure group]] the [[projective unitary group]] $PU(\mathcal{H})$ on a [[separable Hilbert space]] $\mathcal{H}$ classifies the [[twisted cohomology|3-twist]] of [[twisted K-theory|twisted]] [[KU]]-[[cohomology theory]], so the the
[[universal equivariant principal bundle]] with this [[structure group]] $PU(\mathcal{H})$ serves to classify the [[twisted cohomology|3-twists]] of [[twisted equivariant K-theory|equivariant]] [[KU]]-[[cohomology theory]].

## Details

For [[finite group|finite]] [[equivariance group]] $G$ and
in specialization of the [Murayama-Shimakawa construction](equivariant+bundle#calBGammaForDiscreteG), the base space of the universal $G$-equivariant $PU(\mathcal{H})$-principal bundle is 

\[
  \label{TheEquivariantClassifyingSpace}
  \mathcal{B} PU(\mathcal{H})
  \;\;
    =
  \;\;
  TopGrpds
  \big(
    G \times G \rightrightarrows G
    ,\,
    PU(\mathcal{H}) \rightrightarrows \ast
  \big)
  \;\;\;
  \in
  \;
  \in G Actions(TopSpaces)
  \,,
\]

where $G$ [[group action|acts]] by right multiplication on the arguments.


This space is considered in [BEJU 2014, Thm. 3.5](#BEJU14) (without reference to [Murayama & Shimakawa 1995](equivariant+bundle#MurayamaShimakawa95)) as the equivariant classifying space for the 3-twist of [[twisted equivariant K-theory]].

For [[subgroups]] $H \subset G$ the $H$-[[fixed locus]] of this space is the [[Borel construction]]

$$
  \big( 
    \mathcal{B} PU(\mathcal{H})  
  \big)^H
  \;\;
    =
  \;\;
  Grps\big(H, PU(\mathcal{H})\big) \sslash_{\!ad} PU(\mathcal{H})
$$

of the [[adjoint action]] of $PU(\mathcal{H})$ on the space of [[group homomorphisms]] from $H$.

## Properties

### Equivariant homotopy groups
 {#EquivariantHomotopyGroups}

\begin{proposition}\label{EquivariantHomotopyGroupsOfBaseSpace}
  For $H \subset G$ any [[subgroup]], the higher [[homotopy groups]]
  of the $H$-[[fixed locus]] of the equivariant classifying space (eq:TheEquivariantClassifyingSpace) are concentrated on the [[integers]] in degree 3 and the [[Pontrjagin dual]] of $K$ in degree 1:
  $$
    \pi_{k \gt 0}
    \Big(
      \big(
        \mathcal{B} PU(\mathcal{H})
      \big)^H
    \Big)
    \;\;
    =
    \;\;
    \left\{
    \begin{array}{cll}
      0 &\vert& k \geq 4
      \\
      \mathbb{Z} &\vert& k = 3
      \\
      0 &\vert& k = 2
      \\
      Grps(H,S^1) &\vert& k = 1
    \end{array}
    \right.
  $$
\end{proposition}
([BEJU 2014, around Cor. 1.11](#BEJU14))


## Related concepts

* [[U(ℋ)|$U(\mathcal{H})$]]


## References

* {#BEJU14} [[Noé Bárcenas Torres|Noé Bárcenas]], [[Jesús Francisco Espinoza Fierro|Jesús Espinoza]], [[Michael Joachim]], [[Bernardo Uribe]], _Universal twist in Equivariant K-theory for proper and discrete actions_, Proceedings of the London Mathematical Society, Volume 108, Issue 5 (2013) ([arXiv:1202.1880](https://arxiv.org/abs/1202.1880), [doi:10.1112/plms/pdt061](https://doi.org/10.1112/plms/pdt061))

* [[Noé Bárcenas Torres|Noé Bárcenas]], [[Jesús Francisco Espinoza Fierro|Jesús Espinoza]], [[Bernardo Uribe]], [[Mario Velasquez]], Section 3.2 of: _Segal's spectral sequence in twisted equivariant K-theory for proper and discrete actions_, Proceedings of the Edinburgh Mathematical Society **61** 1 (2018) ([arXiv:1307.1003](https://arxiv.org/abs/1307.1003), [doi:10.1017/S0013091517000281](https://doi.org/10.1017/S0013091517000281))

* [[Jesus Espinoza]], [[Bernardo Uribe]], *Topological properties of spaces of projective unitary representations*, Rev. Acad. Colombiana Cienc. Exact. Fís. Natur. 40 (2016), no. 155, 337-352 ([arXiv:1511.06785](https://arxiv.org/abs/1511.06785), [scielo:S0370-39082016000200013](http://www.scielo.org.co/scielo.php?script=sci_arttext&pid=S0370-39082016000200013), [doi:10.18257/raccefyn.317](https://doi.org/10.18257/raccefyn.317))


[[!redirects universal equivariant PU-bundle]]
[[!redirects universal equivariant PUH-bundle]]

[[!redirects universal equivariant PU(ℋ)-bundle]]
