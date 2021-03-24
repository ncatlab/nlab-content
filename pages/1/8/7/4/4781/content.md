
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### Vertical vector fields

Let $\pi : P \to X$ be a [[bundle]] in the [[category]] [[Diff]] of [[smooth manifolds]]. A [[vector field]] $v \in \Gamma(T P)$ is _vertical_ with respect to this bundle if it is in the [[kernel]] of the [[derivative]] $d \pi \colon T P \to T X$.

### Vertical tangent bundle
 {#VerticalTangentBundle}

The collection of vertical vectors forms the _vertical tangent bjundle_ inside the full [[tangent bundle]], typically denoted $T_\pi P$.

If $\pi$ is a [[smooth function|smooth]] [[surjective submersion]] between [[compact topological space|compact]] [[smooth manifolds]] then its vertical tangent bundle is the [[fiber]]-wise [[kernel]] of $d \pi$, as shown in the following diagram (recalled e.g. in [Berglund 20, p. 16](#Berglund20)):

\begin{tikzcd}[column sep=normal, row sep=small]
  T_{\pi} P
  \ar[
   r,
   "
    \mathrm{ker}(d \pi)
   "
  ]
  &
  T P 
  \ar[
    r,
    dashed,
    "d \pi"
  ]
  \ar[ddr]
  &
  \pi^\ast
  \big(
    T B 
  \big)
  \ar[
    r
  ]
  \ar[
    ddr,
    phantom,
    "
      \mbox{\tiny\rm(pb)}
    "{
      description
    }
  ]
  \ar[dd]  
  &
  T B
  \ar[
    dd
  ]
  \\
  \\
  &
  &
  P
  \ar[
    r,
    "\pi"{
      below
    }
  ]
  &
  B
\end{tikzcd}

### Horizontal differential forms

A [[differential form]] on $P$ is a [[horizontal differential form]] with respect to $P \to X$ it it _vanishes_ on vertical vector fields.

## Properties

\begin{proposition}
  If $P \overset{\pi}{\longrightarrow} X$ is a [[smooth manifold|smooth]] [[fiber bundle]], then the full [[tangent bundle]] of its total space $P$ is [[isomorphism|isomorphic]] to the [[direct sum of vector bundles|direct sum]] of the vertical tangent bundle ([above](#VerticalTangentBundle)) with the [[pullback bundle|pullback]] of the [[tangent bundle]] of the base space:

$$
  T P
  \;\simeq\;
  \big(
    \pi^\ast T B
  \big)
  \oplus_P
  \big(
    T_\pi P
  \big)
$$

 
\end{proposition}


## Related concepts

* [[evolutionary vector field]]

* [[parameterized index theorem]]

## References

See also

* [[Manifold Atlas]], _<a href="http://www.map.mpim-bonn.mpg.de/Tangent_bundles_of_bundles_(Ex)">Tangent bundles of bundles</a>_

* {#Berglund20} Alexander Berglund, _Characteristic classes for families of bundles_ ([arXiv:2012.12170](https://arxiv.org/abs/2012.12170))

[[!redirects vertical vector fields]]

[[!redirects vertical vector]]
[[!redirects vertical vectors]]

[[!redirects vertical tangent bundle]]
[[!redirects vertical tangent bundles]]

[[!redirects vertical vector bundle]]
[[!redirects vertical vector bundles]]

[[!redirects vertical cotangent bundle]]
[[!redirects vertical cotangent bundles]]

