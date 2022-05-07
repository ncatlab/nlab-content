

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
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

For $\mathcal{V}_X$ a [[complex vector bundle]] of complex [[rank]] $n$, the highest degree [[Chern class]] that may generally be non-vanishing is $c_n$. This is hence often called the _[[top Chern class]]_ of the vector bundle.

## Properties

### Relation to Euler- and Thom-class

\begin{prop}
  The [[top Chern class]] of a [[complex vector bundle]] $\mathcal{V}_X$ equals the [[Euler class]] $e$ of the underlying [[real vector bundle]] $\mathcal{V}^{\mathbb{R}}_X$:

$$
  \mathcal{V}_X
  \;
  \text{has complex rank}\;n
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;   
  c_n
  \big(
    \mathcal{V}_X
  \big)
  \;\;
    =
  \;\;
  e
  \big(
    \mathcal{V}^{\mathbb{R}}_X
  \big)
  \;\;\;\;
  \in
  H^{2n}
  \big(
   X; 
   \,
   \mathbb{Z} 
  \big)
  \,.
$$
\end{prop}

(e.g. [Bott-Tu 82 (20.10.6)](#BottTu82))

\begin{prop}
  The [[top Chern class]] of a [[complex vector bundle]] $\mathcal{V}_X$ equals the [[pullback in cohomology|pullback]] of any [[Thom class]] 
$th \;\in\; H^{2n}\big( \mathcal{V}_X; \mathbb{Z} \big)$ on $\mathcal{V}_X$ along the [[zero-section]]:

$$
  \mathcal{V}_X
  \;
  \text{has complex rank}\;n
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;   
  c_n
  \big(
    \mathcal{V}_X
  \big)
  \;\;\;  
    =
  \;\;\;
  (0_X)^\ast
  (th)
  \;\;
  \in
  \;
  H^{2n}
  \big(
    X ;
    \,
    \mathbb{Z}
  \big)
$$
\end{prop}

(e.g. [Bott-Tu 82, Prop. 12.4](#BottTu82))

\begin{remark}
  This relation to [[Thom classes]] generalizes to [[Conner-Floyd-Chern classes]] in [[complex oriented cohomology|complex oriented]] [[Whitehead-generalized cohomology]]. See at _[[universal complex orientation on MU]]_.
\end{remark}


## Related concepts

* [[first Chern class]]

* [[Euler class]], [[Thom class]]

## References

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))

For more references see at _[[Chern class]]_ and at _[[characteristic class]]_.

[[!redirects top Chern classes]]
