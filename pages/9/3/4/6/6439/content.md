
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyiscs
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--




> This is a sub-entry of [[sigma-model]]. See there for further background and context.

***

#Contents#
* table of contents
{:toc}


## Exposition of a general abstract formulation

We give a leisurely exposition of a general abstract formulation $\sigma$-models, aimed at readers with a background in [[category theory]] but trying to assume no other prerequisites.

What is called an _$n$-dimensional $\sigma$-model_ is first of all an instance of an $n$-dimensional [[quantum field theory]] (to be explained). The distinctive feature of those quantum field theories that are $\sigma$-models is that 

1. these arise from a simpler kind of field theory -- called a [[classical field theory]] -- by a process called [[quantization]] 

1. moreover, this simpler kind of field theory encoded by[[geometry|geometric data]] in a nice way: it describes physical [[configuration space]]s that are [[mapping space]]s into a [[geometry|geometric]] [[space]] equipped with some [[synthetic differential geometry|differential geometric]] [[structure]].

We give expositions of these items step-by-step:

1. [Quantum field theory](#ExpositionQuantumFieldTheory)

1. [Classical field theory](#ExpositionClassicalFieldTheory)

1. [Quantization](#ExpositionQuantization)

1. [Classical sigma-models](#ExpositionClassicalSigmaModels)

1. [Quantum sigma-models](#ExpositionQuantumSigmaModels)

We draw from ([FHLT, section 3](#FHLT)).



### Quantum field theory
 {#ExpositionQuantumFieldTheory}

#### Definition

For our purposes here, a [[quantum field theory]] of [[dimension]] $n$ is a [[symmetric monoidal functor]]

$$
  Z : Bord_n^S \to \mathcal{C}
  \,,
$$

where

* $Bord_n^S$ is a [[cobordism category|category of n-dimensional cobordisms]] that are equipped with some [[structure]] $S$; 

  * its [[object]]s are $(n-1)$-[[dimension]]al [[topological manifold]]s;

  * its [[morphism]]s are [[isomorphism class]]es of $n$-[[dimension]]al [[cobordism]]s between such manifolds

  * and all manifolds are equipped with _$S$-[[structure]]_ . For instance $S$ could be _[[Riemannian structure]]_ . Then we would call $Z$ a [[Euclidean quantum field theory]] (confusingly). If $S$ is "no structure" then we call $Z$ a [[topological quantum field theory]].

  * the [[monoidal category]]-structure is given by [[disjoint union]] of manifolds

    $$
      \Sigma_1 \otimes \Sigma_2 := \Sigma_1 \coprod \Sigma_2    
      \,;
    $$

* $\mathcal{C}$ is some [[symmetric monoidal category]].

We think of data as follows:

* $Bord_n^S$ is a model for _being_ and _becoming_ in [[physics]] (following [[Bill Lawvere]]'s terminology): the objects of $Bord_n^S$ are archetypes of _physical spaces that are_ and the morphisms are _physical spaces that evolve_ ;

* the [[object]] $Z(\Sigma)$ that $Z$ assigns to any $(n-1)$-manifold $\Sigma$ is to be thought of as the _[[space]] of all possible [[state]]s_ over the space $\Sigma$ of a the physical system to be modeled;

* so $\mathcal{C}$ is the category of [[n-vector space]]s among which the _spaces of [[state]]s_ of the quantum theory can be picked;

* the [[morphism]] $Z(\hat \Sigma) : Z(\Sigma_{in}) \to Z(\Sigma_{out})$ that $\Sigma$ assigns to any [[cobordism]] $\hat \Sigma$ with incoming [[boundary]] $\Sigma_{in}$ and outgoing boundary $\Sigma_{out}$ is the [[propagator]] along $\hat \Sigma$: it maps every state $\psi \in Z(\Sigma_{in})$ of the system over $\Sigma_{in}$ to the state $Z(\Psi) \in \Sigma_{out}$ that is the result of the evolution of $\psi$ along $\hat \Sigma$ by the _dynamics_ of the system. Or conversely: the action of $Z$ encodes what this dynamics is supposed to be.

Notice that since $Z$ is required to be a symmetric monoidal functor it sends disjoint unions of manifolds to [[tensor product]]s

$$
  F(\Sigma_1 \coprod \Sigma_2) \simeq Z(\Sigma_1) \otimes Z(\Sigma_2)
  \,.
$$

Moreover, for $\hat \Sigma$ a closed [[cobordism]], hence a morphism $\emptyset \stackrel{\hat \Sigma}{\to} \emptyset$ from the [[empty set|empty]] manifold to itself, we have that

* $Z(\emptyset) = \mathbf{1}$ is the tensor unit of $\mathcal{C}$;

* $Z(\hat \Sigma)  \in End(\mathbb{1})$ is an [[endomorphism]] of this tensor unit, a _number_ as seen internal to $\mathcal{C}$ -- this is the _invariant_ associated to $\hat \Sigma$ by $Z$, called the [[partition function]] of $Z$ over $\hat \Sigma$. We can think of $Z$ as being a rule for computing such invariants by building them up from smaller pieces. This is the _locaity_ of quantum field theory.

#### Examples
 {#ExpositionQFTExamples}

* A simple but archetypical example is this: let $S := Riem$ be [[Riemannian manifold|Riemannian structure]]. Then the category $Bord_1^{Riem}$ of 1-dimensional cobordisms equipped with Riemannian structure is generated (as a [[symmetric monoidal category]]) from [[interval]]s 

  $$
    \bullet \stackrel{t}{\to} \bullet
  $$

  equipped with a [[length]] $t \in \mathbb{R}_+$. Composition is given by addition of lengths

  $$
    (\bullet \stackrel{t_1}{\to} \bullet \stackrel{t_2}{\to})
    = 
    (\bullet \stackrel{t_1 + t_2}{\to} \bullet)
    \,.
  $$

  Therefore a 1-dimensional [[Euclidean quantum field theory]]

  $$
    Z : Bord_1^{Riem} \to Vect
  $$

  is specified by
  
  * a [[vector space]] $\mathcal{H}$ ("of [[state]]s") assigned to the point;

  * for each $t \in \mathbb{R}_+$ a linear endomorphism

    $$
      U(t) : \mathcal{H} \to \mathcal{H}
    $$

    such that 

    $$  
      U(t_1 + t_2) = U(t_2) \circ U(t_1)
      \,.
    $$

  This is just a system of [[quantum mechanics]]. If we demand that $Z$ respects the [[smooth structure]] on the space of morphisms in $Bord_1^{Riem}$ then there will be a linear map $i H : \mathcal{H} \to \mathcal{H}$ such that

   $$
     U(t) = \exp(i H t)
     \,.
   $$

   This $H$ is called the [[Hamilton operator]] of the system.
   
   (We are glossing here over some technical fine print in the definition of $Bord_1^{Riem}$. Done right we have that $\mathcal{H}$ may indeed be an infinite-dimensional vector space. See [[(1,1)-dimensional Euclidean field theories and K-theory]])


### Classical field theory
 {#ExpositionClassicalFieldTheory}

A special class of examples of $n$-dimensional quantum field theories, as discussed [above](#ExpositionQuantumFieldTheory), arise as [[deformation quantization|deformations]] or _[[path integral|averages]]_ of similar, but simpler structure: _[[classical field theories]]_ . The process that constructs a quantum field theory out of a classical field theory is called _[[quantization]]_ . This is discussed [below](#ExpositionQuantization). Here we describe what a classical field theory is. We shall inevitably oversimplify the situation such as to still count as a leisurely exposition. The kind of examples that the following discussion applies to strictly are field theories <a href="http://nlab.mathforge.org/schreiber/show/infinity-Chern-Simons+theory#DiscreteTargets">of Dijkgraaf-Witten type</a>. But despite its simplicity, this case accurately reflects most of the general abstract properties of the general theory.

For our purposes here, a [[classical field theory]] of dimension $n$ is

* a [[symmetric monoidal functor]]

  $$
    \exp(i S(-)) : Bord_n^S \to Span(Grpd, \mathcal{C})
    \,,
  $$

  where

  * $Bord_n^S$ is the same [[category of cobordisms]] as before;

  * $Span(Grpd, \mathcal{C})$ is the [[category of spans]] of [[groupoid]]s over $\mathcal{C}$:

    * [[object]]s are [[groupoid]]s $K$ equipped with [[functor]]s $\phi : K \to \mathcal{C}$;

    * [[morphism]]s $(K_1, \phi_1) \to (K_2, \phi_2)$ are [[diagram]]s

      $$
        \array{
           && \hat K
           \\
           & \swarrow && \searrow
           \\
           K_1 &&\swArrow&& K_2
           \\
           & \searrow && \swarrow
           \\
           && \mathcal{C}
        }
        \,,
      $$

      where in the middle we have a [[natural transformation]];

    * [[composition]] of morphism is by forming [[2-pullback]]s:

      $$
        (\hat K_2 \circ \hat K_1) = \hat K_1 \prod_{K_2} \hat K_2
        \,.
      $$


Let $\hat \Sigma : \Sigma_1 \to \Sigma_2$ be a [[cobordism]] and

$$
  \exp(i S(-))_{\Sigma} =
  \left(
        \array{
           && Conf_{\hat \Sigma}
           \\
           & {}^{\mathllap{(-)|_{in}}}\swarrow && \searrow^{\mathrlap{(-)|_{out}}}
           \\
           Conf_{\Sigma_1} &&\swArrow_{\exp(i S(-)_{\hat \Sigma})}&& Conf_{\Sigma_2}
           \\
           & {}_{V_{\Sigma_1}}\searrow && \swarrow_{\mathrlap{V_{\Sigma_2}}}
           \\
           && \mathcal{C}
        }
  \right)
$$

the value of a classical field theory on $\hat \Sigma$.
We interpret this data as follows:

* $Conf_{\Sigma_1}$ is the [[configuration space]] of a [[classical field theory]] over $\Sigma_1$: [[object]]s are "field configurations" on $\Sigma_1$ and [[morphism]]s are [[gauge transformation]]s between these. Similarly for $Conf_{\Sigma_2}$.

  Here a "physical field" can be something like the [[electromagnetic field]]. But it can also be something very different. For the special case of $\sigma$-models that we are eventually getting at, a "field configuration" here will instead be a way of an particle of shape $\Sigma_1$ sitting in some [[target space]].

* $Conf_{\hat \Sigma}$ is similarly the groupoid of field configurations on the whole cobordism, $\hat \Sigma$. If we think of an object in $Conf_{\hat \Sigma}$ of a way of a [[brane]] of shape $\Sigma_1$ sitting in some [[target space]], then an object in $Conf_{\hat Sigma}$ is a _trajectory_ of that brane in that target space, along which it evolves from shape $\Sigma_1$ to shape $\Sigma_2$.

* $V_{\Sigma_i} : Conf_{\Sigma_i} \to \mathcal{C}$ is the [[classifying space|classifying map]] of a kind of [[vector bundle]] over configuration space: a [[state]] $\psi \in Z(\Sigma_1)$ of the [[quantum field theory]] that will be associated to this [[classical field theory]] by [[quantization]] will be a [[section]] of this vector bundle. Such a section is to be thought of as a generalization of a 
[[probability distribution]] on the space of classical field configurations. The [[generalized element]]s of a [[fiber]] $V_{c}$ of $V_{\Sigma_1}$ over a configuration $c \in Conf_{\Sigma_1}$ may be thought of as an _internal state_ of the brane of shape $\Sigma_1$ sitting in target space. 

* $\exp(i S(-))_{\hat \Sigma}$ is the [[action functional]] that defines the classical field theory: the component

  $$
   \exp(i S(\gamma))_{\hat \Sigma} 
    : 
    V_{\gamma|_{in}}
    \to
    V_{\gamma|_{out}}
  $$

 of this [[natural transformation]] on a trajectory $\gamma \in Conf_{\hat \Sigma}$ going from a configuration $\gamma|_{in}$ to a configuration $\gamma|_{out}$ is a morphism in $\mathcal{C}$ that maps the internal states of the ingoing configuration $\gamma|_{\Sigma_1}$ to the internal states of the outgoing configuration $\gamma|_{\Sigma_2}$. This evolution of internal states encodes the _classical dynamics_ of the system.
 
Notice that this way a classical field theory is taken to be a special case of a [quantum field theory](#ExpositionQuantumFieldTheory), where the codomain of the symmetric monoidal functor is of the special form $Span(Grpd, \mathcal{C})$. For more on this see [[classical field theory as quantum field theory]].


### Quantization
 {#ExpositionQuantization}

We assume now that $\mathcal{C}$ has [[colimit]]s and in fact [[biproduct]]s.

Then for every [[functor]] $\phi : K \to \mathcal{C}$ the [[colimit]] 

$$
  \int^{K} \phi \in \mathcal{C}
$$

exists, and (using the existence of [[biproduct]]s) this construction extends to a [[functor]]

$$
  \int : Span(Grpd, \mathcal{C}) \to \mathcal{C}
  \,.
$$

We call this the _[[path integral]]_ functor.

For

$$
  \exp(i S(-)) : Bord_n^S \to Span(Grpd, \mathcal{C})
$$

a [classical field theory](#ExpositionClassicalFieldTheory), we get this way a [quantum field theory](#ExpositionQuantumFieldTheory) by forming the composite functor

$$
  Z 
    := 
  \int \circ \exp(i S(-)) 
   : 
  Bord_n^S 
    \stackrel{\exp(i S(-))}{\to}
  Span(Grpd, \mathcal{C})
    \stackrel{\int}{\to}
  \mathcal{C}
  \,.
$$

This $Z$ we call the _[[quantization]]_ of $\exp(i S(-))$.

It acts

* on [[object]]s by sending

  $$
    \begin{aligned}
      \Sigma_{in} & \mapsto (V_{\Sigma_{in}} : Conf_{\Sigma_{in}} \to \mathcal{C}) 
      \\
      & \mapsto \mathcal{H}_{\Sigma_{in}} := \int^K V_{\Sigma_{in}}
    \end{aligned}
  $$

  the vector bundle on the [[configuration space]] over some boundary $\Sigma_{in}$ of [[worldvolume]] to its space $\mathcal{H}_{\Sigma_{in}}$ of [[gauge transformation|gauge invariant]] [[section]]s. In typical situations this $\mathcal{H}_{\Sigma_{in}}$ is the famous [[Hilbert space]] of [[state]]s in [[quantum mechanics]], only that here it is allowed to be any object in $\mathcal{C}$;

* on [[morphism]]s by sending a [[natural transformation]]

  $$
    \begin{aligned}   
      \hat \Sigma & \mapsto 
       (\exp(i S(-))_{\hat \Sigma} : \gamma \mapsto 
       V_{\gamma|_{in}} \to V_{\gamma|_{out}})
       \\   
       & \mapsto
       (\int^K \exp(i S(-))_{\hat \Sigma} 
        : 
        \mathcal{H}_{\Sigma_1} \to \mathcal{H}_{\Sigma_2}
       )
    \end{aligned}
  $$

  to the [[integral transform]] that it defines, weighted by the [[groupoid cardinality]] of $Conf_{\hat \Sigma}$ : the _[[path integral]]_ .


### Classical $\sigma$-models
 {#ExpositionClassicalSigmaModels}


A _classical $\sigma$-model_ is a [classical field theory](#ExpositionClassicalFieldTheory) such that

* the [[configuration space]]s $Conf_{\Sigma}$ are [[mapping spaces]] $\mathbf{H}(\Sigma,X)$ in some suitable category -- some [[cohesive (infinity,1)-topos|higher topos]] in fact -- , for $X$ some fixed [[object]] of that category called _[[target space]]_ ;
 
* the bundles $V_{\Sigma} : Conf_{\Sigma} \to \mathcal{C}$ "of internal states" over these mapping spaces are 

  * the [[transgression]] to these [[mapping space]]s...

  * ...of an [[associated infinity-bundle|associated higher bundle]]... 

  * ...asscociated to a [[circle n-bundle with connection]] on [[target space]]...

  * ...encoded by a classifying morphism

    $$
      \alpha : X \to \mathbf{B}^{n} U(1)
    $$

    into the [[circle n-group]] in $\mathbf{H}$; equipped with an [[connection on an infinity-bundle|n-connection]] $\nabla$...

  * ...where the [[associated bundle|association]] is via a [[representation]]

    $$
      \rho : \mathbf{B}^{n+1} U(1) \to (n+1) Vect
    $$

    on [[n-vector spaces]], which is usually taken to be the canonical 1-dimensional one.

  One calls $(\alpha,\nabla)$ the [[background gauge field]] of the $\sigma$-model.

* The [[action functional]]s $\exp(i S(-))_{\hat \Sigma}$ are given by the [[higher parallel transport]] of $\nabla$ over $\hat \Sigma$.

So an $n$-dimensional $\sigma$-model is a classical field theory that is [[representable functor|represented]], in a sense, by a [[circle n-bundle with connection]] on some [[target space]].

More specifically and more simply, in cases where $X$ is just a [[discrete ∞-groupoid]]  -- the case of  <a href="http://nlab.mathforge.org/schreiber/show/infinity-Chern-Simons%20theory#DiscreteTargets">sigma-models of Dijkgraaf-Witten type</a>, every [[principal ∞-bundle]] on $X$ is necessarily <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos%20--%20structures#FlatDifferentialCohomology">flat</a>, hence the [[background gauge field]] is given just by the morphism

$$
  \alpha : X \to \mathbf{B}^{n} U(1)
  \,.
$$

Then for $\hat \Sigma$ a closed $n$-dimensional manifold, the [[action functional]] of the sigma-model on $\Sigma$ on a field configuration $\gamma : \hat \Sigma \to X$ has the value

$$
  \exp(i S(\gamma))_{\hat \Sigma}
  = 
  \int_{\hat \Sigma} [\alpha]
$$

being the evaluation of $[\alpha]$ regarded as a class in [[ordinary cohomology]] $H^n(\hat \Sigma, U(1))$ evaluated on the [[fundamental class]] of $X$. 

One says that $[\alpha]$ is the [[Lagrangian]] of the theory.


### Quantum $\sigma$-models
 {#ExpositionQuantumSigmaModels} 

(...)

## References

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_, A celebration of the mathematical legacy of Raoul Bott, 367--403, Amer. Math. Soc. 2010 ([arXiv:0905.0731](https://arxiv.org/abs/0905.0731))
 {#FHLT}

