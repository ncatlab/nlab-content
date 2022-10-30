

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
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

The notion of _connection on a 2-bundle_ generalizes the notion of [[connection on a bundle]] from [[principal bundle]]s to [[principal 2-bundle]]s.

It comes with a notion of [[higher parallel transport|2-dimensional parallel transport]].

For an exposition of the concepts here see also at _[[infinity-Chern-Weil theory introduction]]_ the section _[Connections on principal 2-bundles](http://ncatlab.org/nlab/show/infinity-Chern-Weil%20theory%20introduction#ConnectionOn2Bundle)_ .

## Definition

For $G$ a [[Lie 2-group]], a _connection_ on a $G$-[[principal 2-bundle]] coming from a [[cocycle]] $g : X \to \mathbf{B}G$ is a lift of the cocycle to the  [[2-groupoid of Lie 2-algebra valued forms]] $\mathbf{B}G_{conn}$

$$
  \array{
     && \mathbf{B}G_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow & \downarrow
     \\
     X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

## Properties

### Differential &#268;ech cocycle data

We spell out the data of a connection on a 2-bundle over a [[smooth manifold]] $X$ with respect to a given [[open cover]] $\{U_i \to X\}$, following ...

## Examples

* A [[differential string structure]] (untwisted) is a 2-connection with coefficients in the [[string 2-group]] / [[string Lie 2-algebra]].

* The [[worldvolume]] theory of the [[fivebrane]] is expected to support a [[self-dual higher gauge theory]] whose fields are 2-connections (see _[Self-dual 2-connections](http://ncatlab.org/nlab/show/NS5-brane#SelfDual2Connections)_ there).

## Related concepts

* [[connection on a bundle]]

* **connection on a 2-bundle** / [[connection on a gerbe]] / [[connection on a bundle gerbe]]

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* [[connection on an ∞-bundle]]




## References

Connections on 2-bundles with vanishing 2-form curvature defined in terms of their [[higher parallel transport]] are discussed in

* [[Urs Schreiber]],  [[Konrad Waldorf]], _Connections on non-abelian gerbes and their holonomy_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">web</a>)

expanding on

* [[John Baez]], [[Urs Schreiber]], _Higher gauge theory_ ([arXiv:math/0511710](http://arxiv.org/abs/math/0511710)) ([web](http://ncatlab.org/schreiber/show/differential+cohomology+in+a+cohesive+topos+--+references/#BaezSchreiber))

Examples of 2-connections with vanishing 2-form curvature obtained from [[geometric quantization]] are discusssed in

* Olivier Brahic, _On the infinitesimal Gauge Symmetries of closed forms_ ([arXiv](http://arxiv.org/abs/1010.2189))

The [[cocycle]] data for 2-connections with coeffcients in [[automorphism 2-group]]s but without restrictions on the 2-form curvature  have been proposed in 

* [[Lawrence Breen]], [[William Messing]], _Differential Geometry of Gerbes _ ([arXiv:math/0106083](http://arxiv.org/abs/math/0106083))

* [[Lawrence Breen]], _Differential Geometry of Gerbes and Differential Forms_ ([arXiv:0802.1833](http://arxiv.org/abs/0802.1833))

and 

* Paolo Aschieri, Luigi Cantini, [[Branislav Jurco]], _Nonabelian Bundle Gerbes, their Differential Geometry and Gauge Theory_ ([arXiv:hep-th/0312154](http://arxiv.org/abs/hep-th/0312154)).

A discussion of fully general 2-connections is in section xy of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

See also [[connection on an infinity-bundle]] for the general theory.

[[!redirects connections on a 2-bundle]]
[[!redirects connections on 2-bundles]]
