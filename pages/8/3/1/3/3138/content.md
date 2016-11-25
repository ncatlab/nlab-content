
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What [Simons-Sullivan 08](#SimonsSullivan08) call a _structured bundle_ is a certain [[equivalence class]] of [[vector bundles]] with [[connection on a bundle|connection]], such that the corresponding [[Grothendieck group]] is a model for [[differential K-theory]].

The [[equivalence relation]] divided out is relation by a [[concordance]] such that the corresponding [[Chern-Simons form]] is exact.


## Details

Let $V \to X$ be a [[complex vector bundle]] with [[connection on a bundle|connection]] $\nabla$ and [[curvature]] 2-form

$$
  F = F_\nabla \in \Omega^2(X,End(V))
  \,.
$$

**Definition**

The **[[Chern character]]** of $\nabla$ is the inhomogenous [[curvature characteristic form]] 

$$
 ch(\nabla) := \sum_{j \in \mathbb{N}}
   k_j
   tr( F_\nabla \wedge \cdots \wedge F_\nabla)
  \;\;
  \in \Omega^{2 \bullet}(X)
  \,,
$$

where on the right we have $j$ wedge factors of the [[curvature]] .

**Definition**

Let $(V,\nabla)$ and $(V',\nabla')$ be two complex
vector bundles with connection.

A [[Chern-Simons form]] for this pair is a differential form

$$
  CS(\nabla,\nabla') + d \omega \in
  \Omega^{2 \bullet + 1}(X)
$$

obtained from the [[concordance]] bundle $\bar V \to X \times [0,1]$ given by [[pullback]] along $X \times [0,1] \to X$ equipped with a connection $\bar \nabla$ such that ..., by

$$
  CS(\nabla,\nabla') =
  \int_0^1 \psi_t^* (\iota_{\partial/\partial t} ch(\bar \nabla))
  + d (...)
  \,.
$$

**Proposition** This is indeed well defined in that it is independent of the chosen [[concordance]], up to an exact term.

**Definition**

A **structured bundle** in the sense of the Simons-Sullivan model is a complex vector bundle $V$ equipped with the equivalence class $[\nabla]$ of a connection under the equivalence relation that identifies two connections $\nabla$ and $\nabla'$ if their Chern-Simons form $CS(\nabla,\nabla')$ is exact.

Two structured bundles are isomorphic if there is a vector bundle isomorphism under which the two equivalence classes of connections are identified.

**Definition** 

Let $Struc(X)$ be the set of [[isomorphism]] classes of structured bundles on $X$. 

Under [[direct sum]] and [[tensor product]] of vector bundles, this becomes a commutatve [[rig]].

Let 
$$
  \hat K(X) := K(Struct(X))
$$

be the additive [[group completion]] of this rig as usual in [[K-theory]].

So as an additive group $\hat K(X)$ is the quotient of the [[monoid]] induced by [[direct sum]] on pairs $(V,W)$ of isomorphism classes in $Struc(X)$, modulo the sub-monoid consisting of pairs $(V,V)$.

Hence the pair $(V,0)$ is the additive inverse to $(0,V)$ and $(V,W)$ may be written as $V - W$.

**Theorem**

$\hat K(X)$ is indeed a [[differential cohomology]] refinement of ordinary K-theory $K(X)$ of $X$ (i.e. of the 0th [[cohomology group]] of [[K-theory spectrum|K-cohomology]]).

Moreover...






## Refereces

* {#SimonsSullivan08} [[James Simons]], [[Dennis Sullivan]], _Structured vector bundles define differential K-theory_ ([arXiv:0810.4935](http://arxiv.org/abs/0810.4935))



[[!redirects Simons-Sullivan structured bundles]]
