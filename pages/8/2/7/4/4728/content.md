
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **surface** is a [[space]] of [[dimension]] 2, usually understood to be [[connected topological space|connected]].

In [[differential topology|differential]] [[topology]]/[[differential geometry]] this means a 2-[[dimension of a manifold|dimensional]] ([[differentiable manifold|differentiable]]/[[smooth manifold|smooth]]) [[manifold]].

In [[complex analytic geometry]] this usually means a [[complex manifold]] of _complex_ dimension 2 (hence real dimension 4).

Similarly and more generally, in [[algebraic geometry]] an _[[algebraic surface]]_ is a [[variety]] of algebraic dimension 2. 

## Properties

### Classification
 {#Classification}

The [[real manifold|real]] [[closed manifold|closed]] [[orientation|oriented]] surfaces are classified, up to [[isomorphism]] by a [[natural number]] $g \in \mathbb{N}$ called the *[[genus of a surface|genus]]*, which is its "number of holes":

| [[genus of a surface|genus]] | [[surface]] | 
|------------------------------|-------------|
| $0$ | [[2-sphere]] |
| $1$ | [[2-torus]]  |
| $2$ | [[double torus]] |


### Homotopy
 {#Homotopy}

The [[fundamental group]] of the [[real manifold|real]] [[closed manifold|closed]] [[orientation|oriented]] surface $\Sigma^2_g$ of [[genus of a surface|genus]] $g \in \mathbb{N}$ (see [above](#Classification)) is the [[quotient group]] of the [[free group]] on $2g$ generators $(a_1, \cdots, a_g, \, b_1, \cdots, b_g)$ by the group product of the [[group commutators]] $[a_i, b_i]$ of the sequence of [[pairs]] of generators:

$$
  \pi_1\big(
    \Sigma^2_g
  \big)
  \;\simeq\;
  \big\langle
    a_1, \cdots a_g
    ,\,
    b_1, \cdots b_g
  \big\rangle
  \big/
  \Big(
    \textstyle{\prod_i}
    [a_i, b_i]
  \Big)
  \,.
$$

(cf. [Actipes 2013, Thm. 6.3](#Actipes13))


## Examples

* [[plane]]

* [[sphere]]

* [[torus]]

* [[Klein bottle]]


## Related concepts

* [[punctured]] surface

* [[differential geometry of curves and surfaces]]

* analog for dimension 1: [[curve]], [[algebraic curve]]

* [[genus of a surface]]

* [[area]]

* [[moduli space of curves]]

* [[complex surface]]

* [[surface knot]]

* [[hypersurface]]

* [[minimal surface]]

[[!include low dimensional manifolds -- table]]


## References

See also:

* Wikipedia: *<a href="https://en.wikipedia.org/wiki/Surface_(topology)">Surface (topology)</a>*

* Wikipedia: *[Genus g surface](https://en.wikipedia.org/wiki/Genus_g_surface)*

* [[Manifold Atlas]], _[2-manifolds](www.map.mpim-bonn.mpg.de/2-manifolds)_

Review of the classification of surfaces by fundamental [[polygons]]:

* E. C. Zeeman: *An Introduction to Topology -- The Classification theorem for Surfaces* &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/surgery/zeeman.pdf), [pdf](https://www.maths.ed.ac.uk/~v1ranick/surgery/ecztop.pdf), [[Zeeman-ClassificationOfSurfaces.pdf:file]]&rbrack;

* Chen Hui George Teo: *Classification of Surfaces*, REU notes (2011) &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Teo.pdf), [[CHGT-ClassificationOfSurfaces.pdf:file]]&rbrack;

* Thomas George: *The Classification of Surfaces with Boundary*, REU notes (2001) &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/George.pdf), [[George-SurfacesWithBoundary.pdf:file]]&rbrack;

* Ana da Silva Rodrigues: *Classification of Surfaces*, BSc thesis, ETH (2023) &lbrack;[pdf](https://people.math.ethz.ch/~acannas/Student_Papers/BSc_Theses/2023_bsc_da_silva_classification_of_surfaces.pdf), [[Rodrigues-ClassificationOfSurfaces.pdf:file]]&rbrack;

See also:

* Wikipedia: *[Fundamental polygon](https://en.wikipedia.org/wiki/Fundamental_polygon)*

Review of the computation of the [[fundamental group]] of surfaces:

* {#Actipes13} Matthew Actipes: *On the fundamntal group of surfaces*, REU notes (2013) &lbrack;[pdf](http://math.uchicago.edu/~may/REU2013/REUPapers/Actipes.pdf), [[Actipes-FundamentalGroupOfSurfaces.pdf:file]]&rbrack;

Discussion of [[de Rham cohomology]] of surfaces:

* [[William Fulton]], §18 of: *Algebraic Topology -- A First Course*, Graduate Texts in Mathematics **153**, Springer (1995) \[<a href="https://doi.org/10.1007/978-1-4612-4180-5">doi:10.1007/978-1-4612-4180-5</a>\] 



[[!redirects surface]]
[[!redirects surfaces]]

[[!redirects 2-manifold]]
[[!redirects 2-manifolds]]