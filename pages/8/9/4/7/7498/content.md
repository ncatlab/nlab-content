
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
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

# Contents
* table of contents
{: toc}

## Idea

For $G$ a [[topological group]] [[action|acting]] on a [[topological space]] $X$, its _Borel construction_ or _Borel space_ is another topological space $X \times_G E G$, also known as the [[homotopy quotient]]. In many cases, its ordinary [[cohomology]] is the $G$-[[equivariant cohomology]] of $X$.

## Definition

For $X$ a [[topological space]], $G$ a [[topological group]] and $\rho\colon G \times X \to X$ a [[continuous map|continuous]] $G$-[[action]], the **Borel construction** of $\rho$ is [[generalized the|the]] [[topological space]] $X \times_G E G$, hence [[quotient]] of the [[product]] of $X$ with the total space of [[generalized the|the]] $G$-[[universal principal bundle]] $E G$ by the [[diagonal]] [[action]] of $G$ on both.



## Properties

### As the realization of the action groupoid

This Borel construction is naturally understood as being the [[geometric realization of simplicial topological spaces|geometric realization]] of the [[topological groupoid|topological]] [[action groupoid]] $X // G$ of the [[action]] of $G$ on $X$:

the [[nerve]] of this topological groupoid is the [[simplicial topological space]]

$$
  (X // G)_\bullet =
  \left(
 \cdots X \times G \times G \stackrel{\to}{\stackrel{\to}{\to}} X \times G \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to}} X
  \right)
  \,.
$$ 

Observing that $E G = G//G$ itself as a groupoid has the nerve

$$
  (E G)_\bullet
   = 
   \left(
   \cdots 
   G \times G \times G 
     \stackrel{\to}{\stackrel{\to}{\to}}
   G \times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G
  \right)
$$

(where "$\cdot$" denotes the multiplication action of $G$ on itself) and regarding $X$ and $G$ as topological 0-groupoids ($G$ as a group object in topological 0-groupoids), hence with simplicially constant nerves, we have an [[isomorphism]] of simplicial topological spaces

$$
  (X //G)_\bullet 
    \simeq_{iso}
  X \times_G (E G)_\bullet
  \,.
$$

If this is set up in a sufficiently nice category of topological spaces, then, by the discussion at [[geometric realization of simplicial topological spaces]], the geometric realization ${\vert{-}\vert}\colon Top^{\Delta^{op}} \to Top$ manifestly takes this to the Borel construction (since, by the discussion there, it preserves the product and the quotient).

### As a homotopy colimit over the category associated to $G$

If $G$ is the topological category associated to the group $G$, then a $G$-space is precisely a Top-enriched functor $G\to Top$ in a similar fashion to the fact that an  R-module is an Ab-enriched functor. If $X$ is a $G$-space, the ordinary quotient $X/G$ is the colimit of the diagram associated to $X$ and the Borel construction is (a model of) the homotopy colimit of that diagram. This is a reason for calling the Borel construction homotopy quotient in some contexts.

### In rational homotopy theory

The image of the Borel construction in [[rational homotopy theory]] is the [[Weil model]] for [[equivariant de Rham cohomology]]. See there for more.

\begin{xymatrix}
  &
  X \times E G \ar@(ul,ur)^G
  \ar[d]^-{ q }
  &
  \Omega^\bullet( X )
  \otimes 
  W(g)
  \ar@(ur,ul)_{ g }
  \ar@{<-^{)}}[d]^-{ q^\ast }
  \\
  \;
  X // G
  \ar@{}[r]|-{
    \simeq_{\mathrm{whe}}
  }
  &  
  \big(
    X \times E G 
  \big)/G
  &
  \big(
    \Omega^\bullet( X )
    \otimes 
    W(g)
  \big)_{\mathrm{basic}} 
  \ar@{<-}[r]^-{ :\exp\big( t^a \iota_a\big): }_-{\simeq}
  &
  \big(
    \Omega^\bullet( X )\big[ r^a \big]
  \big)^G
  \\
  &
  \mbox{Borel construction}
  &
  \mbox{Weil model}
  &
  \mbox{Cartan model}
\end{xymatrix}



## Related concepts

* [[Borel equivariant cohomology]]

  * [[equivariant ordinary cohomology]]

  * [[equivariant de Rham cohomology]]



## References

Lecture notes in classical [[topology]]:

* Stephen A. Mitchell, _Notes on principal bundles and classifying spaces_, 2011 ([pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]])

General statement in [[simplicial homotopy theory]] of [[simplicial presheaves]]:

* [[J. F. Jardine]], _Stacks and the homotopy theory of simplicial sheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0450/stacks3.pdf))


* {#NSS12b} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Prop. 3.73 in: _Principal $\infty$-bundles -- Presentations_,  Journal of Homotopy and Related Structures, Volume 10, Issue 3 (2015), pages 565-622 ([arXiv:1207.0249](http://arxiv.org/abs/1207.0249), [doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4))


The nature of the Borel construction as the geometric realization of the action groupoid is mentioned for instance in 

* [[Alejandro Adem]], Michele Klaus, _Lectures on orbifolds and group cohomology_ ([pdf](http://www.math.ubc.ca/~adem/hangzhou.pdf))


[[!redirects Borel construction]]
[[!redirects Borel constructions]]

[[!redirects Borel space]]
[[!redirects Borel spaces]]
