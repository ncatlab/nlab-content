
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

The first fractional [[Pontryagin class]] $\frac{1}{2} p_1 : \mathcal{B}Spin \to \mathcal{B}^4 \mathbb{Z}$ in the [[(∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]] $\simeq$ [[Top]] has a refinement to $\mathbf{H} = $ [[?LieGrpd]] of the form $\frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)$ -- the [[smooth first fractional Pontryagin class]].

For $P \to X$ a [[spin group]]-[[principal bundle]], a trivialization of its underlying topological class $\frac{1}{2}p_1(P)$ is called a [[string structure]]. The 2-groupoid of smooth string structures is the [[homotopy fiber]] of

$$
  \frac{1}{2}\mathbf{p}_1
  :
  \mathbf{H}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}(X,\mathbf{B}^3 U(1))
  \,.
$$

This morphism may be refined to land in [[ordinary differential cohomology]] $\mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$. The 2-groupoid of **differential string structures** is a homotopy fiber of

$$
  \frac{1}{2}\hat \mathbf{p}_1
  :
  \mathbf{H}_{conn}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
$$

over some [[circle n-bundle with connection|circle 3-bundle with connection]] whose underlying circle 3-bundle is trivial. Such a differential string structure is represented by a tuple consisting of

* a [[connection on a bundle|connection]] $\nabla$ on a $Spin$-[[principal bundle]];

* a choice of trivial [[circle n-bundle with connection|circle 3-bundle]] with connection $(0, C)$;

* a choice of equivalence of the [[Chern-Simons circle 3-bundle]] with connection of $\nabla$ with this chosen 3-bundle

  $$
    \lambda : \frac{1}{2}\hat \mathbf{p}_1(\nabla) \stackrel{\simeq}{\to}
    (0,C)
    \,.
  $$

More generally, one can consider the [[homotopy fiber]]s of $\frac{1}{2}\hat \mathbf{p}_1$ over arbitrary circle 3-bundles with connection. According to the general notion of [[twisted cohomology]], these may be thought of as **twisted differential string structures**, where the twist is the class of of cocycle over which one computes the homotopy fiber.


## In $\infty$-Chern-Weil theory

We discuss differential string structures in the context of [[∞-Chern-Weil theory]].


Let 

$$
  \frac{1}{2}\hat p_1 : 
  \mathbf{H}_{conn}(-,\mathbf{B}Spin)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^3 U(1))
$$

be the differential refinement of the first fractional Pontryagin class discussed [above](#StringStructure).

+-- {: .un_def }
###### Definition

For $X \in \mathbf{H} =$ [[nLab:?LieGrpd]], the $\infty$-groupoid  of **differential string-structures** $String_{diff}(X)$ is the [[nLab:homotopy fiber]] of    $\frac{1}{2}p_1(X) : \mathbf{H}(X,\mathbf{B}Spin) \to \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$.

More generally, the $\infty$-groupoid of **twisted differential string structures** is the [[nLab:(∞,1)-pullback]] $String_{diff,tw}(X)$ in

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
  \,.
$$

=--

In terms of just the underlying $\infty$-Lie algebra valued local connection data, i.e. before Lie integration in the above sense, this has been considered in <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a>. 

For the case where the twist is given just by globally defined 3-forms, i.e. by  trivial 2-gerbes with connection, essentially this definition, explicitly modeled on [[nLab:bundle gerbe]]s, has been given in ([Waldorf09](http://arxiv.org/PS_cache/arxiv/pdf/0906/0906.0117v1.pdf)).

We describe now the Lie integration of the $\infty$-Lie algebraic model in <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a> to a model of the above homotopy pullback.

In order to compute the homotopy pullback as an ordinary pullback, we want to model the morphism     
$\mathbf{H}_{conn}(X,\mathbf{B}Spin) \stackrel{\frac{1}{2}\hat p_1}{\to} \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))$ in $\infty Lie Grpd$ by a fibration in $[CartSp^{op}, sSet]_{proj,cov}$. To that end, we replace the Lie algebra $\mathfrak{g}$ by an equivalent Lie 3-algebra

+-- {: .un_def }
###### Definition

Let $\hat \mathfrak{g}$ be the $\infty$-Lie algebra defined by the fact that its [[nLab:Chevalley-Eilenberg algebra]] is

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

obtained by projecting out onto the 3-forms induced by the generator $c$ and then integrating is another model for $\frac{1}{2}p_1$, with the special property that the top morphism is a fibration in $[CartSp^{op}, sSet]_{proj}$.

=--

With this observation we can read off the cocycles in $String_{diff,tw}(X)$ from the diagrams of dg-algebras in SSSIII.


## References

A discussion of differential string structures in terms of [[bundle 2-gerbe]]s is given in

* [[Konrad Waldorf]], _String Connections and Chern-Simons Theory_ ([arXiv:0906.0117](http://arxiv.org/abs/0906.0117))

The [[∞-Lie algebra cohomology]]-data for the description of twisted differential string structures in terms of [[∞-Chern-Weil homomorphism]] is in 

* Sati, S., Stasheff, _Twisted differential string and fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#SSSIII">web</a>)

