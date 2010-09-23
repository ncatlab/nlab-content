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

* [[Chern-Simons circle 3-bundle]]

* **Chern-Simons circle 7-bundle**

***

#Contents#
* table of contents
{:toc}

## Idea

A _Chern-Simons circle 7-bundle_ is the [[circle n-bundle with connection|circle 7-bundle with connection]]  classified by the cocycle in degree-8 [[ordinary differential cohomology]] that is canonically associated to a [[string group]]-[[principal 2-bundle]] with [[connection on a 2-bundle|connection]].

The [[characteristic class]] called the second fractional [[Pontryagin class]] $\frac{1}{6}p_2 : \mathcal{B}String \to \mathcal{B}^8 \mathbb{Z}$ in [[Top]] on the [[classifying space]] of the [[string group]] has a smooth lift to the <a href="http://ncatlab.org/nlab/edit/Lie+infinity-groupoid#SmoothSecondPontryagin">smooth second fractional Pontryagin class</a>

$$
  \frac{1}{6} \mathbf{p}_2 : \mathbf{B}String \to \mathbf{B}^7 U(1)
$$

in $\mathbf{H} :=$ [[?LieGrpd]], mapping from the [[delooping]] [[∞-Lie groupoid]] of the [[string Lie 2-group]] to that of the  <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle Lie 7-group</a>. This is the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">Lie integration</a>  of the degree 7 [[∞-Lie algebra cocycle]] $\mu_7 : \mathfrak{string} \to b^6 \mathbb{R}$ on the [[string Lie 2-algebra]] which classified the [[fivebrane Lie 6-algebra]].

Therefore, by [[∞-Chern-Weil theory]], there is a refinement of this morphism to [[connection on an ∞-bundle|∞-bundles with connection]]

$$
  \frac{1}{6}\hat \mathbf{p} : \mathbf{B}String_{conn} \to 
  \mathbf{B}^7 U(1)_{conn}
$$

hence on [[cocycle]] [[∞-groupoid]]s

$$
  \frac{1}{6} \hat \mathbf{p} : \mathbf{H}_{conn}(X,\mathbf{B}String) 
  \to \mathbf{H}_{diff}^8(X)
$$


a map from [[string Lie 2-group]]-[[principal 2-bundle]]s with [[connection on a 2-bundle|connection]] to [[circle n-bundle with connection|circle 7-bundles with connection]], hence degree 8 [[ordinary differential cohomology]]. 

For $(P,\nabla)$ a String-principal 2-bundle, we call the image $\frac{1}{6}\hat\mathbf{p}(\nabla) \in \mathbf{H}_{diff}(X,\mathbf{B}^z U(1))$ its **Chern-Simons circle 7-bundle with connection**.

This is a differential refinement of the [[twisted cohomology|obstruction]] to lifting $P$ to a [[fivebrane Lie 6-group]]-bundle.


By construction, the [[curvature]] 8-form of $\hat \mathbf{c}(\nabla)$ is the [[curvature characteristic form]] $\langle F_\nabla \wedge F_\nabla \wedge F_\nabla \wedge F_\nabla\rangle$ of $\nabla$ and accordingly the 7-form connection on $\hat \mathbf{c}(\nabla)$ is locally a [[Chern-Simons form]] $CS(\nabla)$ of $\nabla$.

Therefore the [[higher parallel transport]] induced by $\frac{1}{6}\hat \mathbf{p}_2(\nabla)$ over 7-dimensional volumes $\phi : \Sigma \to X$ is the [[action functional]] of degree-7 [[∞-Chern-Simons theory]].  This is the analog of the way the [[Chern-Simons circle 3-bundle]] arises from Spin-principal bundles.



## Construction

Using the discusson at [[∞-Chern-Weil theory]] and in direct analogy to the constructin of the [[Chern-Simons circle 3-bundle]] we can model the [[(∞,1)-functor]]

$$
  \mathbf{H}_{conn}(X, \mathbf{B}String)
  \to 
  \mathbf{H}_{conn}(X, \mathbf{B}^7 U(1))
$$

by postcomposition with the [[∞-anafunctor]]

$$
  \array{
    \exp(\mathfrak{string})_{conn} 
    &\stackrel{\exp(\mu_7)_{conn}}{\to}&
    \exp(b^6 \mathbb{R})_{conn}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{cosk}_7 \exp(\mathfrak{string})_{conn}
    &\to&
    \mathbf{B}^7 U(1)_{conn}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}String_{conn}
  }
$$

where $\mu_7 : \mathfrak{string} \to b^6 \mathbb{R}$ is the 7-cocycle that classifies the [[fivebrane Lie 6-algebra]].

For 

$$
  \array{
     C(U) &\stackrel{g}{\to}& \mathbf{B}String_{conn}
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
$$

an [[∞-anafunctor]] modelling a [[cocycle]] for a [[string 2-group]]-[[principal 2-bundle]] with [[connection on a 2-bundle]] the $\infty$-anafunctor composition

$$
  \array{
    && \exp(\mathfrak{string})_{conn} 
    &\stackrel{\exp(\mu_7)_{conn}}{\to}&
    \exp(b^6 \mathbb{R})_{conn}
    \\
    && \downarrow && \downarrow
    \\
    C(V)
    &\stackrel{\hat g}{\to}&
    \mathbf{cosk}_7 \exp(\mathfrak{string})_{conn}
    &\to&
    \mathbf{B}^7 U(1)_{conn}
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}String_{conn}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

produces a lift of the transition functions $g$ to $\mathbf{cosk}_7 \exp(\mathfrak{string})$. The string-cocycle is itself in first degree a collection of paths in $G$, in second a collection of surfaces with labels in $U(1)$. That lift corresponds to further resolving this to families

$$
  U_{i_1} \cap \cdots U_{i_k} \times \Delta^k \to G
$$ 

up to $k = 7$. That this is indeed always possible is the statement about [[Lie integration]] that $\mathbf{cosk}_7  \exp(\mathfrak{string}) \stackrel{\simeq}{\to} \mathbf{B}String$ is a weak equivalence, which in turn is due to the fact that the next nonvanishing [[homotopy group]] of $G = SO(n)$ after $\pi_3$ is $\pi_7$.

The above composite [[∞-anafunctor]] is manifestly a degree 8-cocycle in [[Cech cohomology|Cech]]-[[Deligne cohomology]] given by

$$
  \left(
     CS_7(\sigma_i^* A)
     \,,\,
     \int_{\Delta^1} g_{i j}^*CS_7(A) 
     \,,\,
     \int_{\Delta^2} g_{i j k}^*CS_7(A) 
     \,,\,
     \int_{\Delta^3} \hat g_{i j k l}^*CS_7(A) 
     \,,\,
     \int_{\Delta^5} \hat g_{i j k l m}^*CS_7(A) 
     \,,\,
     \int_{\Delta^6} \hat g_{i j k l m n}^*CS_7(A) 
     \,,\,
     \int_{\Delta^7} \hat g_{i j k l m n o}^* \mu(A)
  \right)
  \,,
$$

where $A$ is a connection form on the total space of the $Spin(n)$-[[principal bundle]] that the string bundle itself is lifted from and $CS_7$ is the [[Chern-Simons element]] in degree 7 defining the [[fivebrane Lie 6-algebra]].

(...)


## Applications

* [[differential fivebrane structure]]

* [[dual heterotic string theory]]

[[!redirects Chern-Simons circle 7-bundle]]