
<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

_Differential K-theoiry_ is the refinement of the [[generalized (Eilenberg-Steenrod) cohomology]] theory [[K-theory]] to [[differential cohomology]].

In as far as we can think of cocycles in [[K-theory]] as represented by [[vector bundle]]s or [[vectorial bundle]]s, cocycles in differential K-theory may be represented by [[vector bundle]]s [[connection on a bundle|with connection]].

There are various different models that differ in the concrete realization of these cocycles and in their extra properties.

## The Simons-Sullivan model 

This section discusses the model presented in

* [[James Simon]], [[Dennis Sullivan]], _Structured vector bundles define differential K-theory_ ([arXiv](http://arxiv.org/abs/0810.4935?context=math.DG))

More details will eventually be at

* [[Simons-Sullivan structured bundle]].

### Idea 

In the Simons-Sullivan model cocycles in differential K-theory are represented by ordinary [[vector bundle]]s [[connection on a bundle|with connection]]. The crucial ingredient is that two connections on a vector bundle are taken to be the same representative of a differential K-cocycle if they are related by a [[concordance]] such that the corresponding [[Chern-Simons form]] is exact.

### Details

Let $V \to X$ be a complex [[vector bundle]] with [[connection on a bundle|connection]] $\nabla$ and [[curvature]] 2-form

$$
  F = F_\nabla \in \Omega^2(X,End(V))
  \,.
$$

**Definition**

The **[[Chern character]]** of $\nabla$ is the inhomogeneous differential form

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
vector bundles with conneciton.

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



## The Bunke-Schick model 

### Idea

[[Uli Bunke]] and [[Thomas Schick]] developed in a series of articles a differential-geometric cocycle model of differential K-theory where cocycles are given by smooth families of [[Dirac operator]]s.

### References

The basic article is

* [[Ulrich Bunke]], [[Thomas Schick]], _Smooth K-Theory_ ([arXiv:0707.0046](http://arxiv.org/abs/0707.0046))

Re survey talk is

* [[Ulrich Bunke]], _Differential cohomology in geometry and analysis_ ([pdf slides](http://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/Vortrag-Erlangen.pdf))

The [[equivariant cohomology]] version of this is in

* [[Ulrich Bunke]], [[Thomas Schick]], _Differential orbifold $K$-Theory_ ([arXiv:0905.4181](http://arxiv.org/abs/0905.4181))

A construction of [[differential cobordism cohomology]] theory in terms of explicit geoimetric cocycles is in

* [[Ulrich Bunke]], [[Thomas Schick]], Ingo Schroeder, Moritz Wiethaup _Landweber exact formal group laws and smooth cohomology theories_ ([arXiv:0711.1134](http://arxiv.org/abs/0711.1134))

By tensoring this with the suitable ring, this also gives a model for differential K-theory, as well as for [[differential elliptic cohomology]].




## Examples 

* In [[gauge theory]] gauge fields are modeled by cocycles in [[differential cohomology]]. The field modeled by differential K-theory is the [[RR-field]]. 