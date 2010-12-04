
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Where a [[fivebrane structure]] is a trivialization of a class in [[integral cohomology]], a _differential fivebrane structure_ is the trivialization of this class refined to [[ordinary differential cohomology]]:

the second fractional [[Pontryagin class]] 

$$
  \frac{1}{6} p_2 : \mathcal{B}String \to \mathcal{B}^8 \mathbb{Z}
$$ 

in the [[(∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]] $\simeq$ [[Top]] has a refinement to $\mathbf{H} = $ [[?LieGrpd]] of the form 

$$
  \frac{1}{6}\mathbf{p}_2 : \mathbf{B}String \to \mathbf{B}^7 U(1)
$$ 

where $String$ denotes the smooth [[string 2-group]]

-- the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth second fractional Pontryagin class</a>.

The induced morphism

$$
  \frac{1}{6}\mathbf{p}_2
  :
  \mathbf{H}(X,\mathbf{B} String)
  \stackrel{}{\to}
  \mathbf{H}(X,\mathbf{B}^7 U(1))
$$

sends a [[string 2-group]]-[[principal 2-bundle]] $P$ to its corresponding [[Chern-Simons circle 7-bundle]] $\frac{1}{6}\mathbf{p}_2(P)$.
 
A choice of trivialization of $\frac{1}{6}p_2(P)$ is a [[fivebrane structure]]. The 6-groupoid of smooth fivebrane structures is the [[homotopy fiber]] of $\frac{1}{6}\mathbf{p}_2$.

By [[∞-Chern-Weil theory]] this morphism may be further refined to land in [[ordinary differential cohomology]] $\mathbf{H}_{diff}(X, \mathbf{B}^7 U(1))$, classifying [[circle n-bundle with connection|circle 7-bundles with connection]]. The [[n-groupoid|6-groupoid]] of **differential fivebrane structures** is the [[homotopy fiber]] of this refinement

$$
  \frac{1}{6}\hat \mathbf{p}_2
  :
  \mathbf{H}_{conn}(X,\mathbf{B} String)
  \stackrel{}{\to}
  \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
$$

Such a differential fivebrane structure is represented by a tuple consisting of

* a [[connection on a 2-bundle|2-connection]] $\nabla$ on a $String$-[[principal 2-bundle]];

* a choice of trivial [[circle n-bundle with connection|circle 7-bundle]] with connection $(0, C)$;

* a choice of equivalence $\lambda$ of the [[Chern-Simons circle 7-bundle]] with connection $\frac{1}{6}\hat\mathbf{p}_2(\nabla)$ of $\nabla$ with this chosen 7-bundle

  $$
    \lambda : \frac{1}{6}\hat \mathbf{p}_2(\nabla) \stackrel{\simeq}{\to}
    (0,C)
    \,.
  $$

More generally, one can consider the [[homotopy fiber]]s of $\frac{1}{6}\hat \mathbf{p}_2$ over arbitrary circle 7-bundles with connection. According to the general notion of [[twisted cohomology]], these may be thought of as **twisted differential fivebrane structures**, where the twist is the class of cocycle over which one computes the homotopy fiber.


## Definition {#Definition}

Let 

$$
  \frac{1}{6}\hat p_2 : 
  \mathbf{H}_{conn}(-,\mathbf{B}String)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^7 U(1))
$$

be the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth second fractional Pontryagin class</a>.


+-- {: .un_def }
###### Definition

For any $X \in \mathbf{H} :=$ [[nLab:?LieGrpd]], the [[n-groupoid|6-groupoid]]  of **differential fivebrane-structures** $Fivebrane_{diff}(X)$ is the [[nLab:homotopy fiber]] of  $\frac{1}{6}\mathbf{p}_2(X)$ over the trivial differential cocycle.

More generally, following the general definition of [[twisted cohomology]] -- the 6-groupoid of **twisted differential fivebrane structures** is the [[(∞,1)-pullback]] $Fivebrane_{diff,tw}(X)$ in

$$
  \array{
    String_{diff,tw}(X) &\to& H_{diff}(X,\mathbf{B}^7 U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{conn}(X,\mathbf{B}String)
    &\stackrel{\frac{1}{6}\hat \mathbf{p}_2}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
  }
  \,,
$$

where $H_{diff}(X,\mathbf{B}^7 U(1))$ is the set of connected components of $\mathbf{H}_{diff}(X, \mathbf{B}^7 U(1))$ and where the right vertical morphism picks one object in each connected component.

=--

+-- {: .un_remark }
###### Remark

In terms of just the underlying $\infty$-Lie algebra valued local connection data, i.e. before Lie integration as discussed [below](#ChernWeilTheory), this has been considered in ([SSSIII](#SSSIII)).

=--



## Related concepts

[[Whitehead tower]] of the [[orthogonal group]]

* [[orientation]] 
 
* [[spin structure]]

* [[string structure]],  **differential string structure**

* [[fivebrane structure]], [[differential fivebrane structure]]

## References


The [[∞-Lie algebra cohomology]]-data for the description of twisted differential string structures in terms of [[∞-Chern-Weil homomorphism]] is in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential string and fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#SSSIII">web</a>)
{#SSSIII}

The full cocycles are described in 

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cocycles for differential characteristic classes_ ([web](http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+%28%E2%88%9E%2C1%29-topos+--+references#FSS))

[[!redirects differential fivebrane structures]]