
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

Where a [[string structure]] is a trivialization of a class in [[integral cohomology]], a _differential string structure_ is the trivialization of this class refined to [[ordinary differential cohomology]]:

the first fractional [[Pontryagin class]] 

$$
  \frac{1}{2} p_1 : \mathcal{B}Spin \to \mathcal{B}^4 \mathbb{Z}
$$ 

in the [[(∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]] $\simeq$ [[Top]] has a refinement to $\mathbf{H} = $ [[?LieGrpd]] of the form 

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)
$$ 

-- the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>.

The induced morphism

$$
  \frac{1}{2}\mathbf{p}_1
  :
  \mathbf{H}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}(X,\mathbf{B}^3 U(1))
$$

sends a [[spin group]]-[[principal bundle]] $P$ to its corresponding [[Chern-Simons circle 3-bundle]] $\frac{1}{2}\mathbf{p}_1(P)$.
 
A choice of trivialization of $\frac{1}{2}p_1(P)$ is a [[string structure]]. The 2-groupoid of smooth string structures is the [[homotopy fiber]] of $\frac{1}{2}\mathbf{p}_1$.

By [[Chern-Weil theory]] this morphism may be further refined to land in [[ordinary differential cohomology]] $\mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$, classifying [[circle n-bundle with connection|circle 3-bundles with connection]]. The [[2-groupoid]] of **differential string structures** is the homotopy fiber of this refinement

$$
  \frac{1}{2}\hat \mathbf{p}_1
  :
  \mathbf{H}_{conn}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
$$

Such a differential string structure is represented by a tuple consisting of

* a [[connection on a bundle|connection]] $\nabla$ on a $Spin$-[[principal bundle]];

* a choice of trivial [[circle n-bundle with connection|circle 3-bundle]] with connection $(0, C)$;

* a choice of equivalence $\lambda$ of the [[Chern-Simons circle 3-bundle]] with connection $\frac{1}{2}\hat\mathbf{p}_1(\nabla)$ of $\nabla$ with this chosen 3-bundle

  $$
    \lambda : \frac{1}{2}\hat \mathbf{p}_1(\nabla) \stackrel{\simeq}{\to}
    (0,C)
    \,.
  $$

More generally, one can consider the [[homotopy fiber]]s of $\frac{1}{2}\hat \mathbf{p}_1$ over arbitrary circle 3-bundles with connection. According to the general notion of [[twisted cohomology]], these may be thought of as **twisted differential string structures**, where the twist is the class of cocycle over which one computes the homotopy fiber.


## Definition {#Definition}

Let 

$$
  \frac{1}{2}\hat p_1 : 
  \mathbf{H}_{conn}(-,\mathbf{B}Spin)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^3 U(1))
$$

be the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>.


+-- {: .un_def }
###### Definition

For any $X \in \mathbf{H} :=$ [[nLab:?LieGrpd]], the [[2-groupoid]]  of **differential string-structures** $String_{diff}(X)$ is the [[nLab:homotopy fiber]] of  $\frac{1}{2}\mathbf{p}_1(X)$ over the trivial differential cocycle.

More generally, following the general definition of [[twisted cohomology]] -- the 2-groupoid of **twisted differential string structures** is the [[(∞,1)-pullback]] $String_{diff,tw}(X)$ in

$$
  \array{
    String_{diff,tw}(X) &\to& H_{diff}(X,\mathbf{B}^3 U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{conn}(X,\mathbf{B}Spin)
    &\stackrel{\frac{1}{2}\hat p_1}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
  }
  \,,
$$

where $H_{diff}(X,\mathbf{B}^3 U(1))$ is the set of connected components of $\mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$ and where the right vertical morphism picks one object in each connected component.

=--

+-- {: .un_remark }
###### Remark

In terms of just the underlying $\infty$-Lie algebra valued local connection data, i.e. before Lie integration as discussed [below](#ChernWeilTheory), this has been considered in ([SSSIII](#SSSIII)).

For the case where the twist is given just by globally defined 3-forms, i.e. by  trivial 2-gerbes with connection, essentially this definition, explicitly modeled on [[bundle 2-gerbe]]s, has been given in ([Waldorf](#Waldorf)).

=--


## In $\infty$-Chern-Weil theory {#ChernWeilTheory}

We discuss here an explicit computation of the homotopy fibers in the [above definition](#Definition) using tools described at [[∞-Chern-Weil theory]]. That is we describe a model for $\frac{1}{2}\mathbf{p}_1$ in terms of [[Lie integration]] of a morphism in [[∞-Lie algebra cohomology]] (following [SSSIII](#SSSIII)).

In order to compute the [[homotopy pullback]] (see there) as an ordinary [[pullback]], we want to model $\frac{1}{2}\mathbf{p}_1$  by a _fibration_ in the [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj,cov}$. To that end, we replace the [[Lie algebra]] $\mathfrak{g}$ by an equivalent [[∞-Lie algebra|Lie 3-algebra]]

+-- {: .un_def }
###### Definition

Let $\hat \mathfrak{g}$ be the $\infty$-Lie algebra defined by the fact that its [[Chevalley-Eilenberg algebra]] is

$$
  CE(\hat \mathfrak{g}) = 
  (\wedge^\bullet(  \mathfrak{g}^* \oplus \langle b\rangle \oplus \langle c \rangle ), d)
  \,,
$$

with $b$ a generator in degree 2, and $c$ a generator in degree 3, and with differential

$$
  d|_{\mathfrak{g}^*} = [-,-]^*
  \,; 
$$

$$
  d : b \mapsto \langle - , [-,-]\rangle + c
$$

$$
  d : c \mapsto 0
  \,.
$$

=--

+-- {: .un_prop }
###### Proposition

The canonical correspondence

$$
  \array{
    \mathbf{cosk}_3\exp(\hat \mathfrak{g})
    &\to&
    \mathbf{B}^3 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}G
  }
$$

obtained by projecting out onto the 3-forms induced by the generator $c$ and then integrating is another model for $\frac{1}{2}\mathbf{p}_1$, with the special property that the top morphism is a fibration in $[CartSp^{op}, sSet]_{proj}$.

=--

With this observation we can read off the cocycles in $String_{diff,tw}(X)$ from the diagrams of dg-algebras in SSSIII.

(...)

## References

A discussion of differential string structures in terms of [[bundle 2-gerbe]]s is given in

* [[Konrad Waldorf]], _String Connections and Chern-Simons Theory_ ([arXiv:0906.0117](http://arxiv.org/abs/0906.0117))
{#Waldorf}

The [[∞-Lie algebra cohomology]]-data for the description of twisted differential string structures in terms of [[∞-Chern-Weil homomorphism]] is in 

* H. Sati, U. Schreiber, J. Stasheff, _Twisted differential string and fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#SSSIII">web</a>)
{#SSSIII}
