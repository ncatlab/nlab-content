
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

\begin{defn}\label{TwistedNormalFraming}
Consider a [[differentiable manifold|differentiable]]/[[smooth manifold]] $M^D$ of [[dimension]] $D$ and equipped with a [[real vector bundle]] 

\[
  \label{TwistingVectorBundle}
  \mathcal{V} \to M^d
  \;\;\;\;
  \in
  VectorBundles_{\mathbb{R}}(M)
\]

of [[rank]] $n \leq D$, with [[classifying map]] to be denoted $\tau \;\colon\; M \longrightarrow B \mathrm{O}(n)$.

Then a _$\tau$-twisted normal framing_ on a [[submanifold]] $\Sigma^d \hookrightarrow M$ is an [[isomorphism]] of [[real vector bundles]]

$$
  N\Sigma \overset{\simeq}{\longrightarrow} \mathcal{V}_{\vert \Sigma}
$$ 

between the [[normal bundle]] of the submanifold and the [[pullback bundle]] of $\mathcal{V}$ along its inclusion.
\end{defn}

(e.g. [Cruickshank 99, Def. 6.0.7](#Cruickshank 99) [Cruickshank 03, Def. 5.1](#Cruickshank03))

For this to exist it is necessary that

$$
  n \;=\; D - d
$$

is the [[codimension]] of $\Sigma^d \hookrightarrow M^D$.

\begin{example}
In the special case that $\mathcal{V}$ (eq:TwistingVectorBundle) is the [[trivial bundle|trivial]] real vector bundle $n$, the notion of twisted normal framing (Def. \ref{TwistedNormalFraming}) reduces to that of _[[normal framing]]_.

\end{example}

## Properties

### Twisted Pntrjagin theorem

The [[twisted Pontrjagin theorem]] identifies [[cobordism classes]] of twisted-framed submanifolds in $M^D$ (Def. \ref{TwistedNormalFraming}) with the [[twisted Cohomotopy]] of $M^d$.

## References

* {#Cruickshank99} [[James Cruickshank]], _Twisted  Cobordism and its Relationship to Equivariant Homotopy Theory_, 1999 ([pdf](http://www.collectionscanada.gc.ca/obj/s4/f2/dsk1/tape9/PQDD_0030/NQ46823.pdf), [[Cruickshank99.pdf:file]])

* {#Cruickshank03} [[James Cruickshank]], _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">doi:10.1016/S0166-8641(02)00183-9</a>)

[[!redirects normal twisted framings]]

[[!redirects normal twisted-framing]]
[[!redirects normal twisted-framings]]

[[!redirects normally twisted-framed submanifold]]
[[!redirects normally twisted-framed submanifolds]]


