
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
  \frac{1}{6} p_2 : B String \to B^8 \mathbb{Z}
$$ 

in the [[(∞,1)-topos]] [[∞Grpd]] $\simeq$ [[Top]] has a refinement to $\mathbf{H} = $ [[Smooth∞Grpd]] of the form 

$$
  \frac{1}{6}\mathbf{p}_2 : \mathbf{B}String \to \mathbf{B}^3 U(1)
$$ 

-- the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth second fractional Pontryagin class</a>.

The induced morphism on [[cocycle]] [[∞-groupoid]]s

$$
  \frac{1}{6}\mathbf{p}_2
  :
  \mathbf{H}(X,\mathbf{B} String)
  \stackrel{}{\to}
  \mathbf{H}(X,\mathbf{B}^3 U(1))
$$

sends a [[string 2-group]]-[[principal 2-bundle]] $P$ to its corresponding [[Chern-Simons circle 7-bundle]] $\frac{1}{6}\mathbf{p}_2(P)$.
 
A choice of trivialization of $\frac{1}{6}p_2(P)$ is a [[fivebrane structure]]. The [[n-groupoid|6-groupoid]] of smooth fivebrane structures is the [[homotopy fiber]] of $\frac{1}{6}\mathbf{p}_2$ over the trivial [[circle n-bundle with connection|circle 7-bundle]].

By [[Chern-Weil theory in Smooth∞Grpd]] this morphism may be further refined to a [[differential characteristic class]] $\frac{1}{6}\hat \mathbf{p}_2$ that lands in the [[ordinary differential cohomology]] 
$\mathbf{H}_{diff}(X, \mathbf{B}^7 U(1))$, 
classifying [[circle n-bundle with connection|circle 7-bundles with connection]]

$$
  \frac{1}{6}\hat \mathbf{p}_2
  :
  \mathbf{H}_{conn}(X,\mathbf{B} String)
  \stackrel{}{\to}
  \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
$$

The [[n-groupoid|7-groupoid]] of **differential fivebrane structures** is the [[homotopy fiber]] of this refinement $\frac{1}{6}\hat \mathbf{p}_2$ over the [[circle n-bundle with connection|trivial circle 7-bundle with trivial connection]] or more generally over the trivial circle 7-bundles with possibly non-trivial connection.

Such a differential fivebrane structure over a [[smooth manifold]] $X$ is characterized by a tuple consisting of

1. a [[connection on a 2-bundle|2-connection]] $\nabla$ on a [[string 2-group|String]]-[[principal 2-bundle]] on $X$;

1. a choice of trivial [[circle n-bundle with connection|circle 7-bundle]] with connection $(0, H_7)$, hence a differential 7-form $H_7 \in \Omega^7(X)$;

1. a choice of [[equivalence in an (∞,1)-category|equivalence]] $\lambda$ of the [[Chern-Simons circle 7-bundle]] with connection $\frac{1}{6}\hat\mathbf{p}_2(\nabla)$ of $\nabla$ with this chosen 7-bundle

  $$
    \lambda : \frac{1}{6}\hat \mathbf{p}_2(\nabla) \stackrel{\simeq}{\to}
    (0,H_7)
    \,.
  $$

More generally, one can consider the [[homotopy fiber]]s of $\frac{1}{6}\hat \mathbf{p}_2$ over arbitrary circle 7-bundles with connection $\hat \mathcal{G}_8 \in \mathbf{H}_{diff}^8(X, \mathbf{B}^3 U(1))$ and hence replace $(0,H_7)$ in the above with $\hat \mathcal{G}_8$. According to the general notion of [[twisted cohomology]], these may be thought of as **twisted differential string structures**, where the class $[\mathcal{G}_8] \in H^8_{diff}(X)$ is the twist.


## Definition {#Definition}

We will assume that the reader is familiar with basics of the discussion at [[Smooth∞Grpd]]. We often write $\mathbf{H} := Smooth \infty Grpd$ for short.

Let $String(n) \in $ [Smooth∞Grpd]] be the smooth [[String 2-group]], for some $n \in \mathbb{N}$, regarded as a [[Lie 2-group]] and thus canonically as an [[∞-group]] object in [[Smooth∞Grpd]]. We shall notationally suppress the $n$ in the following. Write $\mathbf{B}String$ for its [[delooping]] of $Spin$ in [[Smooth∞Grpd]]. (See the discussion <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#StrictLie2Groups">here</a>). 
Let moreover $\mathbf{B}^6 U(1) \in Smooth \infty Grpd$ be the <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">circle Lie 7-group</a> and $\mathbf{B}^7 U(1)$ its [[delooping]].

At [[Chern-Weil theory in Smooth∞Grpd]] the following statement is proven ([FSS](#FSS)).

+-- {: .un_prop }
###### Proposition

The image under [[Lie integration]] of the canonical [[Lie algebra cohomology|Lie algebra 7-cocycle]]

$$
  \mu = \langle -,[-,-], [-,-], [-,-]\rangle : \mathfrak{so} \to b^6 \mathbb{R}
$$

on the [[semisimple Lie algebra]] $\mathfrak{so}$ of the [[Spin group]] -- the [[special orthogonal Lie algebra]] -- is a morphism in [[Smooth∞Grpd]] of the form

$$
  \frac{1}{6} \mathbf{p}_2 : 
  \mathbf{B}String
    \to
  \mathbf{B}^7 U(1)
$$

whose image under the <a href="http://nlab.mathforge.org/nlab/show/Euclidean-topological%20infinity-groupoid#GeometricHomotopy">the fundamental ∞-groupoid (∞,1)-functor/ geometric realization</a> $\Pi : Smooth \infty Grpd \to $ [[∞Grpd]] is the ordinary second fractional [[Pontryagin class]]

$$
  \frac{1}{6}p_2 : B String \to B^8 \mathbb{Z}
$$

in [[Top]]. Moreover, the corresponding <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#ChernWeilTheory">refined differential characteristic class</a> 

$$
  \frac{1}{6}\hat \mathbf{p}_2 : 
  \mathbf{H}_{conn}(-,\mathbf{B}String)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^7 U(1))
$$

is in [[cohomology]] the corresponding refined [[Chern-Weil homomorphism]]

$$
  [\frac{1}{6}\hat \mathbf{p}_String] : 
  H^1_{Smooth}(X,String) \to H_{diff}^8(X)
$$

with values in [[ordinary differential cohomology]] that corresponds to the second [[Killing form]] [[invariant polynomial]] $\langle - , - ,-,-\rangle $ on $\mathfrak{so}$.


=--

+-- {: .un_def #DifferentialStringStructure}
###### Definition

For any $X \in $ [[Smooth∞Grpd]], the [[n-groupoid|6-groupoid]]  of **differential fivebrane-structures** on $X$ -- $Fivebrane_{diff}(X)$ -- is the [[homotopy fiber]] of  $\frac{1}{6}\hat \mathbf{p}_2(X)$ over the trivial differential cocycle.

More generally (see [[twisted cohomology]]) the 6-groupoid of **twisted differential fivebrane structures** is the [[(∞,1)-pullback]] $Fivebrane_{diff,tw}(X)$ in

$$
  \array{
    Fivebrane_{diff,tw}(X) &\to& H_{diff}^8(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{conn}(X,\mathbf{B}String)
      &\stackrel{\frac{1}{6}\hat \mathbf{p}_2}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
  }
  \,,
$$

where the right vertical morphism is a choice of (any) one point in each [[connected component]] (differential cohomology class) of the [[cocycle]] [[∞-groupoid]] $\mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))$ (the [[homotopy type]] of the [[(∞,1)-pullback]] is independent of this choice).

=--


+-- {: .un_remark }
###### Remark

In terms of local [[∞-Lie algebra valued differential forms]] data this has been considered in ([SSSIII](#SSSIII)), as we shall discuss [below](#ChernWeilTheory).

=--


## Construction in terms of $L_\infty$-Cech cocycles 
  {#ChernWeilTheory}

We use the [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-topos]] [[Smooth∞Grpd]] (as described there) by the local [[model structure on simplicial presheaves]] $[CartSp_{smooth}^{op}, sSet]_{proj,loc}$ to give an explicit construction of twisted differential fivebrane structures in terms of [[Cech cohomology|Cech]]-cocycles with coefficients in [[∞-Lie algebra valued differential forms]].

Recall the following fact from [[Chern-Weil theory in Smooth∞Grpd]] ([FSS](#FSS)).

+-- {: .un_prop }
###### Proposition

The differential second fractional Pontryagin class $\frac{1}{6} \hat \mathbf{p}_2$ is presented in $[CartSp_{smooth}^{op}, sSet]_{proj}$ by the top morphism of simplicial presheaves in

$$
  \array{
    \mathbf{cosk}_7\exp(\mathfrak{so})_{ChW,smp}
     &\stackrel{\exp(\mu, cs)}{\to}&
    \mathbf{B}^7 \mathbb{R}/\mathbb{Z}_{ChW,smp}     
    \\
    \downarrow && \downarrow
    \\
    \mathbf{cosk}_7\exp(\mathfrak{so})_{diff,smp}
     &\stackrel{\exp(\mu, cs)}{\to}&
    \mathbf{B}^7 \mathbb{R}/\mathbb{Z}_{smp} 
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}String_{c}
  }
  \,.
$$

=--

Here the middle morphism is the direct [[Lie integration]] of the [[infinity-Lie algebra cohomology|L-∞ algebra cocycle]] while the top morphisms is its restriction to coefficients for [[connection on an ∞-bundle|∞-connections]].

In order to compute the [[homotopy fiber]]s of 
$\frac{1}{6}\hat \mathbf{p}_2$ we now find a [[resolution]] of this morphism $\exp(\mu,cs)$ by a fibration in $[CartSp_{smooth}^{op}, sSet]_{proj}$. By the fact that this is a [[simplicial model category]] then also the hom of any cofibrant object into this morphism, computing the cocycle $\infty$-groupoids, is a fibration, and therefore, by the general discussion at [[homotopy pullback]], we obtain the [[homotopy fiber]]s as the ordinary [[fiber]]s of this fibration.


### Presentation of the differential class by a fibration

(...)

The discussion is analogous to that at [[differential string structure]]. To be filled in 

(...)



## Related concepts

[[Whitehead tower]] of the [[orthogonal group]]

* [[orientation]] 
 
* [[spin structure]]

* [[string structure]],  [[differential string structure]]

* [[fivebrane structure]], **differential fivebrane structure**

## References

The local data for the [[∞-Lie algebra valued differential forms]] for the description of twisted differential fivebrane structures as above was given in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential string and fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#SSSIII">web</a>)
{#SSSIII}

The full Cech-Deligne cocycles induced by this (but not yet the homotopy fibers over them) were discussed in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cocycles for differential characteristic classes_ (
<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+%28%E2%88%9E%2C1%29-topos+--+references#FSS">web</a>)
{#FSS}

A comprehensive discussion is at

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

in section 4.2.



[[!redirects differential fivebrane structures]]

[[!redirects twisted differential fivebrane structure]]
[[!redirects twisted differential fivebrane structures]]
