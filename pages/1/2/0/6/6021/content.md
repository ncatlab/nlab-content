
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For manifolds

For $X$ a [[connected]] [[orientation|oriented]] [[boundary|closed]] [[manifold]], its integral [[homology]] group in degree the [[dimension]] of $X$ is [[isomorphic]] to the [[integer]]s

$$
  H_{dim X}(X, \mathbb{Z}) \simeq \mathbb{Z}
  \,.
$$

The generator of this corresponding to the choice of [[orientation]] is called the **fundamental class** of $X$. 

### For $(n-1)$-connected spaces

If a [[topological space]] $X$ is $(n-1)$-[[n-connected space|connected]] for $n\geq2,$ then by the [[Hurewicz theorem]] there is an isomorphism $h\colon\pi_n(X)\to H_n(X)$. By the [[universal coefficient theorem]], we have $H^n(X;\pi_n(X))=\hom(H_n(X),\pi_n(X))$. Hence $h^{-1}$ represents an element of $H^n(X;\pi_n(X))$ called the fundamental class of $X$. In particular, the [[Eilenberg-MacLane space]] $K(G,n)$ has a fundamental class $\iota$ which represents the identity map $1\in [K(G,n),K(G,n)]\cong H^n(K(G,n);G).$ This is the universal cohomology class, in the sense that all cohomology classes are pullbacks of this one by classifying maps. ref Mosher and Tangora.

### Virtual fundamental class

(...)

* [[virtual fundamental class]].

## Related concepts

* [[Poincaré duality complex]]

* [[Poincaré duality algebra]]

* [[intersection theory]]

* [[wrapped brane]]

* [[Steenrod representability]]


[[!redirects fundamental classes]]