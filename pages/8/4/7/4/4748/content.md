
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

#Contents#
* table of contents
{:toc}

## Idea

A [[connection on a bundle]] induces a notion of [[parallel transport]] over _paths_ . A [[connection on a 2-bundle]] induces a generalization of this to a notion of parallel transport over _surfaces_ . Similarly a [[connection on a 3-bundle]] induces a notion of parallel transport over 3-dimensional volumes.

Generally, a [[connection on an ∞-bundle]] induces a notion of parallel transport in arbitrary dimension.

## Definition


Let $A$ be an [[∞-Lie groupoid]] such that morphisms $X \to A$ in [[?LieGrpd]] classify the $A$-[[principal ∞-bundle]]s under consideration. Write $A_{conn}$ for the differential refinement described at [[∞-Lie algebra valued form]], such that lifts

$$
  \array{
     && A_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow & \downarrow
     \\
     X &\stackrel{g}{\to}& A
  }
$$

describe [[connections on ∞-bundles]].

+-- {: .un_defn}
###### Definition

For $n \in \mathbb{N}$ say that $\nabla$ **admits parallel $n$-transport** if for all [[smooth manifold]]s $\Sigma$ of [[dimension]] $n$ and all morphisms 

$$
  \phi : \Sigma \to X
$$

we have that the pullback of $\nabla$ to $\Sigma$

$$
  \phi^* \nabla : \Sigma \stackrel{\phi}{\to} X \stackrel{\nabla}{\to} A_{conn}
$$

**flat** in that it factors through the canonical inclusion $\mathbf{\flat}A \to A_{conn}$.

In other words: if all the lower [[curvature]] $k$-forms, $1 \leq k \leq n$ of $\phi^* \nabla$ vanish (the higher ones vanish automatically for dimensional reasons).

=--

Here $\mathbf{\flat}A = [\mathbf{\Pi}(-),A]$ is the coefficient for [[schreiber:path ∞-groupoid|flat differential A-cohomology]].


+-- {: .un_defn}
###### Remark

This condition is automatically satisfied for ordinary [[connections on bundles]], hence for $A = \mathbf{B}G$ with $G$ an ordinary [[Lie group]]: because in that case there is only a single curvature form, namely the ordinary [[curvature]] 2-form.

But for a [[principal 2-bundle]] with connection there is in general a 2-form curvature and a 3-form curvature. A 2-connection therefore admits parallel transport only if its 2-form curvature is constrained to vanish. 

Notice however that if the coefficient object $A$ happens to be $(n-1)$-[[connected]] -- for instance if it is an [[Eilenberg-MacLane object]] in degree $n$, then there is no extra condition and _every_ connection admits parallel transport. This is notably the case for [[circle n-bundles with connection]].
 
=--


+-- {: .un_defn}
###### Definition

For $\nabla : X \to A_{conn}$ an $\infty$-connection that admits parallel $n$-transport, this is for each $\phi : \Sigma \to X$ the morphism

$$
  \mathbf{\Pi}(\Sigma) \to A
$$

that corresponds to $\phi^* \nabla$ under the equivalence

$$
  \mathbf{H}(\Sigma, \mathbf{\flat}A ) \simeq \mathbf{H}(\mathbf{\Pi}(\Sigma), A)
  \,.
$$

=--

+-- {: .un_defn}
###### Remark


The objects of the [[schreiber:path ∞-groupoid]] $\mathbf{\Pi}(\Sigma)$ are points in $\Sigma$, the morphisms are paths in there, the 2-morphisms surves between these paths, and so on. Hence a morphism $\mathbf{\Pi}(\Sigma) \to A$ assigns fibers in $A$ to points in $X$, and equivalences between these fibers to paths in $\Sigma$, and so on.

=--


## Higher holonomy

We now define thee higher analog of [[holonomy]] for the case that $\Sigma$ is closed.

+-- {: .un_defn}
###### Definition

Let $\nabla : X \to A_{conn}$ be a connection with parallel $n$-transport and $\phi : \Sigma \to X$ a morphism from a _closed_ $n$-[[manifold]].

Then the **$n$-holonomy** of $\nabla$ over $\Sigma$ is the image $[\phi^* \nabla]$ of

$$
  \phi^* \nabla : \Pi(\Sigma) \to \Gamma(A)
$$

in the [[homotopy category]]

$$
  [\phi^* \nabla] \in [\Pi(\Sigma), \Gamma(A)] 
$$

=--


## In terms of parallel transport $n$-functors on $n$-paths

At least in low categorical dimension one has the definition of the [[path n-groupoid]] $\mathbf{P}_n(X)$ of a smooth manifold, whose $n$-morphisms are [[thin homotopy]]-classes of smooth functions $[0,1]^n \to X$. Parallel $n$-transport with only the $(n+1)$-curvature form possibly nontrivial and all the lower curvature degree 1- to $n$-forms nontrivial may be expressed in terms of smooth $n$-functors out of $\mathbf{P}_n$ ([SWI](#SWI), [SWII](#SWII), [MartinsPickenI](#MartinsPickenI), [MartinsPickenII](#MartinsPickenII)).

### 2-Transport

We work now concretely in the category $2DiffeoGrpd$ of [[2-groupoid]]s [[internalization|internal to]] the category of [[diffeological space]]s.

Let $X$ be a [[smooth manifold]] and write $\mathbf{P}_2(X) \in 2DiffeoGrpd$ for its [[path 2-groupoid]]. Let $G$ be a [[Lie 2-group]] and $\mathbf{B}G \in 2DiffeoGrpd$ its [[delooping]] 1-object 2-groupoid. Write $\mathfrak{g}$ for the corresponding [[Lie 2-algebra]].

Assume now first that $G$ is a [[strict 2-group]] given by a [[crossed module]] $(G_1 \to G_0)$. Corresponding to this is a [[differential crossed module]] $(\mathfrak{g}_1 \to \mathfrak{g}_0)$.

We describe now how smooth 2-functors

$$
  tra : \mathbf{P}_2(X) \to \mathbf{B}G
$$

i.e. morphisms in $2DiffeoGrpd$ are characterized by [[Lie 2-algebra valued differential forms]] on $X$.

+-- {: .un_defn}
###### Definition

Given a morphism $F : \mathbf{P}_2(X) \to \mathbf{B}G$ we construct a $\mathfrak{g}_1$-valued 2-form  $B_F \in \Omega^2(X, \mathfrak{g}_1)$ as follows.

To find the value of $B_F$ on two vectors $v_1, v_2 \in T_p X$ at some point, _choose_ any smooth function

$$
  \Gamma : \mathbb{R}^2 \to X
$$

with

* $\Gamma(0,0) = p$

* $\frac{d}{d s}|_{s = 0} \Gamma(s,0) = v_1$

* $\frac{d}{d t}|_{t = 0} \Gamma(0,t) = v_2$.

Notice that there is a canonical 2-parameter family

$$
  \Sigma_{\mathbb{R}} : \mathbb{R}^2 \to 2Mor \mathbf{P}_2(\mathbb{R}^2)
$$

of classes of bigons on the plane, given by sending $(s,t) \in \mathbb{R}^2$ to the class represented by any bigon (with sitting instants) with straight edges filling the square

$$
  \Sigma_{\mathbb{R}}(s,t) = 
  \left(
    \array{
      (0,0) &\to& (0,t)
      \\
      \downarrow && \downarrow
      \\
      (s,0) &\to& (s,t)
    }
  \right)
  \,.
$$

Using this we obtain a smooth function

$$
  F_\Gamma : 
  \mathbb{R}^2 \stackrel{\Sigma_{\mathbb{R}}}{\to}
  2Mor \mathbf{P}_2(\mathbb{R}^2)
  \stackrel{\Gamma_*}{\to}
  2Mor \mathbf{P}_2(X)
  \stackrel{F}{\to}
  G_0 \times G_1
  \stackrel{p_2}{\to}
  G_1
  \,.
$$

Then set

$$
  B_F(v_1, w_1) := 
   \frac{\partial^2 F_\Gamma}{\partial x \partial y}|_{(0,0)}
  \,.
$$
 
=--

+-- {: .un_prop}
###### Proposition

This is well defined, in that $B_F(v_1,v_2)$ does not depend on the choices made. Moreover, the 2-form defines this way is smooth.

=--

+-- {: .proof}
###### Proof

To see that the definition does not depend on the choice of $\Gamma$, proceed as follows.

For given vectors $v_1,v_2 \in \T_X X$ let $\Gamma, \Gamma' : \mathbb{R}^2 \to X$ be two choices of smooth maps as in the defnition.  By restricting, if necessary, to a neighbourhood of the origin of $\mathbb{R}^2$, we may assume without restriction that these maps land in a single coordinate patch in $X$. Using the vector space structure of $\mathbb{R}^n$ defined by such a patch, define a smooth homotopy

$$
  \tau : [0,1]^3 \to X : (x,y,z) \mapsto (1-z)\Gamma(x,y) + z \Gamma'(x,y)
$$

Let 

$$
  Z = \{(x,y,w) \in [0,1]^3 | 0 \leq w \leq \frac{1}{2}(x^2 + y^2) \}
$$

and consider the map $f : [0,1]^3 \to Z$ given by

$$
  f : (x,y,z) \mapsto (x,y, \frac{1}{2}(x^2 + y^2) z)
$$

and the map $g : Z \to X$ given away from $(x^2 + y^2) = 0$ by

$$
  g : (x,y,w) \mapsto \tau(x,y, 2 \frac{w}{x^2 + y^2})
  \,.
$$

Using [[Hadamard's lemma]] and the fact that by constructon $\tau$ has vanishing 0th and 1st order differentials at the origin it follows that this is indeed a [[smooth function]].

We want to similarly factor the smooth family of bigons $[0,1]^3 \to 2Mor(\mathbf{P}_2(X))$ given by

$$
  [0,1]^3 \times [0,1]^2 \to X
$$

$$
  ((x,y,z),(s,t)) \mapsto \tau(s x, t y, z)
$$

as $[0,1]^3 \times [0,1]^2 \to Z \times [0,1]^2 \to Z \to X$

$$
  ((x,y,z),(s,t)) 
    \mapsto
  ((x, y, \frac{1}{2}(x^2 + y^2)), (s,t))
    \mapsto
  (s x , t y, \frac{1}{2}((s x)^2 + (t y)^2)z)
    \mapsto
  \tau(s x, s y, z)
  \,.
$$

As before using Hadamard's lemma this is a sequence of smooth functions. Under the hom-adjunction it corresponds to a factorization of $G_\Gamma : [0,1]^3 \to 2 Mor(\mathbf{P}_2(X))$ into

$$
 G_\Gamma :  [0,1]^3 \stackrel{f}{\to} Z \to 2 Mor(\mathbf{P}_2(X))
  \,.
$$

By the above construction we have the the push-forwards

$$
  f_* : \frac{\partial}{\partial x}(x=0,y=0,z)  
    \mapsto
    \frac{\partial}{\partial x}(x= 0, y = 0, w = 0)
$$

and similarly for $\frac{\partial}{\partial y}$ are indendent of $z$. It follows by the [[chain rule]] that also 

$$
  \frac{\partial^2 G_\Gamma}{\partial x \partial y}|_{(x=0,y=0)} 
$$

is independent of $z$. But at $z = 0$ this equals $\frac{\partial^2 F_\Gamma}{\partial x \partial y}|_{(x=0,y=0)}$, while at $z = 1$ it equals $\frac{\partial^2 F_{\Gamma'}}{\partial x \partial y}|_{(x=0,y=0)}$. Therefore these two are equal.

=--




## Examples

### For trivial circle $n$-bundles / for $n$-forms

The simplest example is the parallel transport in a [[circle n-bundle with connection]] over a [[smooth manifold]] $X$ whose underlying $\mathbf{B}^{n-1}U(1)$-bundle is trivial. This is equivalently given by a degree $n$-[[differential form]] $A \in \Omega^n(X)$. For $\phi : \Sigma_n \to X$ any [[smooth function]] from an $n$-dimensional manifold $\Sigma$, the corresponding parallel transport is simply the [[integral]] of $A$ over $\Sigma$:

$$
  \tra_A(\Sigma) = \exp(i \int_\Sigma \phi^* A)
  \;\;\; \in \;\; U(1)
  \,.
$$

One can understand higher parallel transport therefore as a generalization of integration of diifferential $n$-forms to the case where

* the $n$-form is not globally defined;

* the $n$-form takes values not in $\mathbb{R}$ but more generally is an [[∞-Lie algebroid valued differential form]].

### For circle $n$-bundles with connection

We show how the $n$-holonomy of [[circle n-bundles with connection]] is reproduced from the above.

Let $\phi^* \nabla : \mathbf{\Pi}(\Sigma) \to \mathbf{B}^n U(1)$ be the parallel transport for a [[circle n-bundle with connection]] over a $\phi : \Sigma \to X$.

This is equivalent to a morphism

$$
  \Pi(\Sigma) \to \mathcal{B}^n U(1)
  ,.
$$

We may map this further to its $(n-dim \Sigma)$-[[nLab:truncated|truncation]]

$$
  :\infty Grpd(\Pi(\Sigma), \mathcal{B}^n U(1)) 
  \to
  \tau_{n-dim \Sigma} \infty Grpd(\Pi(X), \mathcal{B}^n U(1))
  \,.
$$

+-- {: .un_theorem}
###### Theorem

We have

$$
  \tau_{n-dim\Sigma} \infty Grpd(\Pi(\Sigma), \mathcal{B}^n U(1))
  \simeq
  \mathbf{B}^{n-dim \Sigma} U(1)
  \,.
$$

=--

(This is due to an observation by [[nLab:Domenico Fiorenza]].)

+-- {: .proof}
###### Proof

By general abstract reasoning (recalled at [[nLab:cohomology]] and [[nLab:fiber sequence]]) we have for the [[nLab:homotopy group]]s that

\[
  \pi_i \infty Grpd(\Pi(\Sigma),\mathcal{B}^n U(1))
  \simeq 
  H^{n-i}(\Sigma, U(1))
  \,.
\]

Now use the [[nLab:universal coefficient theorem]], which asserts that we have an [[nLab:exact sequence]]

\[
  0
  \to 
  Ext^1(H_{n-i-1}(\Sigma,\mathbb{Z}),U(1))
  \to 
  H^{n-i}(\Sigma,U(1))
  \to 
  Hom(H_{n-i}(\Sigma,\mathbb{Z}),U(1))
  \to 0
  \,.
\]

Since $U(1)$ is an [[nLab:injective object|injective]] $\mathbb{Z}$-[[nLab:module]] we have 

$$
  Ext^1(-,U(1))=0
  \,.
$$  

This means that we have an [[nLab:isomorphism]]

\[
  H^{n-i}(\Sigma,U(1))
  \simeq 
  Hom_{Ab}(H_{n-i}(\Sigma,\mathbb{Z}),U(1))
\]

that identifies the [[nLab:cohomology group]] in question with the [[nLab:internal hom]] in [[nLab:Ab]] from the integral [[nLab:homology]] group of $\Sigma$ to $U(1)$.

For $i\lt (n-dim \Sigma)$, the right hand is zero, so that 

$$
  \pi_i \infty Grpd(\Pi(\Sigma),\mathbf{B}^n U(1)) =0 \;\;\;\;
  for i\lt (n-dim \Sigma)
  \,. 
$$ 

For $i=(n-dim \Sigma)$, instead, $H_{n-i}(\Sigma,\mathbb{Z})\simeq \mathbb{Z}$, since $\Sigma$ is a closed $dim \Sigma$-manifold and so 

$$
  \pi_{(n-dim\Sigma)} \infty Grpd(\Pi(\Sigma),\mathcal{B}^n U(1))\simeq U(1)
  \,.
$$


=--


+-- {: .un_def}
###### Definition 

The resulting morphism

$$
  \mathbf{H}(\Sigma, A_{conn})
  \stackrel{\exp(i S(-))}{\to}
  \mathbf{B}^{n-dim\Sigma} U(1)
$$

in [[nLab:∞Grpd]] we call the **$\infty$-Chern-Simons action** on $\Sigma$.

=--

Here in the language of [[nLab:quantum field theory]]

* the [[nLab:object]]s of $\mathbf{H}(\Sigma,A_{conn})$ are the [[nLab:gauge field]] on $\Sigma$;

* the [[nLab:morphism]]s in $\mathbf{H}(\Sigma, A_{conn})$ are the [[nLab:gauge transformation]]s;.








## Applications

### In physics

In [[physics]] various [[action functional]]s for [[quantum field theories]] are nothing but higher parallel transport.

* The gauge interaction part of the action functional for the particle charged under a background [[electromagnetic field]], which is a [[circle n-bundle with connection|circle bundle with connection]] $\nabla$, is the parallel 1-transport of $\nabla$.

* The gauge interaction part of the action functional for the string charged under a background [[Kalb-Ramond field]], which is a [[circle n-bundle with connection|circle 2-bundle with connection]] $\nabla$, is the parallel 2-transport of $\nabla$.

* The gauge interaction part of the action functional for the membrane charged under a background [[supergravity C-field]], which is a [[circle n-bundle with connection|circle 3-bundle with connection]] $\nabla$, is the parallel 3-transport of $\nabla$.

* The action functional of [[Chern-Simons theory]] is the parallel 3-transport of a [[Chern-Simons circle 3-bundle]].



## References

For references on parallel 2-transport in bundle gerbes see [[connection on a bundle gerbe]].

The description of parallel $n$-transport in terms of $n$-functors on the [[path n-groupoid]] is in 

* [[Urs Schreiber]], [[Konrad Waldorf]], _Smooth functors vs. differential forms_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">SWII</a>)
{#SWII}

* [[João Faria Martins]], [[Roger Picken]], _On 2-dimensional holonomy_ ([arXiv](http://arxiv.org/abs/0710.4310))
{#MartinsPickenI}

* [[João Faria Martins]], [[Roger Picken]], _The fundamental Gray 3-groupoid of a smooth manifold and local 3-dimensional holonomy based on a 2-crossed module_ ([arXiv](http://arxiv.org/abs/0907.2566))
{#MartinsPickenII}

The description of [[connections on a 2-bundle]] in terms of such parallel 2-transoort 

* U.S. [[Konrad Waldorf]] _Nonabelian gerbes and their holonomy_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">web</a>)
{#SWIII}
