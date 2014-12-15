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

The notion of __Cartan connection__ is a special case of that of _[[connection on a bundle]]_ which is more general than the notion of _[[affine connection]]_ , but more special than the notion of _[[principal connection]]_ , in general: 

it is an $G$-[[principal connection]] subject to the constraint that the connection 1-form linearly identifies each [[tangent space]] of the base space with a quotient $\mathfrak{g}/\mathfrak{h}$ of the [[Lie algebra]] $\mathfrak{g}$ of $G$ by a sub-Lie algebra $\mathfrak{h}$.

The [[fiber]] of the [[bundle]] underlying a  Cartan connection is a [[homogeneous space]]. This notion is closely related to [[Klein geometry|Klein geometries]]. 

Cartan connections are also just called _[[Cartan geometries]]_ . See there for more.


## Definition

### Traditional

Let $G$ be a [[Lie group]] and $H \hookrightarrow G$  a sub-Lie group. (So that we may think of the [[coset space]] $G/H$ as a [[Klein geometry]].) Write $\mathfrak{h} \hookrightarrow \mathfrak{g}$ for the corresponding [[Lie algebras]]. 

There are various equivalent forms of the definition of Cartan connections. The following one characterizes it as a $G$-[[principal connection]] equipped with extra [[stuff, structure and property|structure and property]].

+-- {: .num_defn #Traditional}
###### Definition

A $(H \hookrightarrow G)$-Cartan connection over a [[smooth manifold]] $X$ is;

* a $G$-[[principal connection]] $\nabla$ on $X$;

* such that 

  1. there is a [[reduction of structure groups]] along $H \hookrightarrow G$;

  1. for each point $x \in X$ the canonical composite (for any local trivialization)

     $$
       T_x X \stackrel{\nabla}{\to} \mathfrak{g} \to \mathfrak{g}/\mathfrak{h}
     $$

     is an [[isomorphism]].

=--

+-- {: .num_remark #TraditionalReferences}
###### Remark
**(References)**

In terms of [[Cech cohomology|Cech]] [[cocycle]]-data definition \ref{Traditional} is ([Sharpe, section 5.1, def. 1.3](#Sharpe)).  The equivalent formulation as an $H$-[[principal bundle]] equipped with $\mathfrak{g}$-[[Lie algebra valued differential form]] data on its total space is in ([Sharpe, section 5.3, def. 3.1](#Sharpe)), and the equivalent formulation as a $G$-[[principal bundle]] equipped with an [[Ehresmann connection]] on its total space, subject to a constraint, is in ([Sharpe, appendix A, prop. 3.1](#Sharpe)). 

Hence ([Sharpe](#Sharpe)) gives closely related equivalent definitions, but never quite says it fullly explicitly in the form of def. \ref{Traditional}. More explicit statements as above are in [Wikipedia -- Cartan connection -- As principal connectoions](http://en.wikipedia.org/wiki/Cartan_connection#Cartan_connections_as_principal_connections).

=--

+-- {: .num_remark}
###### Remark

The last clause in def. \ref{Traditional} says that the [[tangent space]] of $X$ at any point $x$ is being identified with the tangent space of the [[homogeneous space]] $G/H$ at the base point $e H$. This may be visualized by imagining that $X$ "tangentially touches" $G/H$ at $x\in X$ and $e H \in G/H$.

But by homogeneity, all the tangent spaces of $G/H$ are [[isomorphism|isomorphic]], and canonically so by [[invariant differential form|left translation]]. Hence by the path-lifting property of [[principal connections]], one may visualize the Cartan connection as describing how the $G/H$ touching $X$ at $x$  "rolls" along paths (infinitesimal paths, vectors) through $x$. This picture of "rolling" is particularly vivid for the case that $(H \hookrightarrow G) = (O(n)\hookrightarrow O(n+1))$ is the inclusion of [[orthogonal groups]], which gives that $G/H = S^n$ is the [[n-sphere]] (for more on this see at _[[conformal connection]]_).

This picture of model spaces rolling along was influential in the historical development of the concept of Cartan geometry in the spirit of [[Klein geometry]].

=--

+-- {: .num_remark #ExamplesOfGlobalCartanPatches}
###### Remark

In many important examples the spaces $X$ carrying a Cartan connection are not just tangentially identified with $G/H$, but are locally modeled on all of $G/H$. This is notably the case for all Cartan connections appearing in [[gravity]] and [[supergravity]]. Here $G$ is a [[Euclidean group]] or [[Poincaré group]] or [[super Poincaré group]], $H \hookrightarrow G$is the [[rotation group]] or [[Lorentz group]] and $G/H$ is [[Cartesian space]] or [[Minkowski space]] or [[super Minkowski space]], respectively. Given a manifold ([[spacetime]]) $X$ then a Cartan connection encodes a [[vielbein field]] with compatible "[[spin connection]]" and the manifold is locally diffeomorphic to copies of $G/H$.

=--

### Synthetically in terms of differential cohesion
 {#InTermsOfSmoothModuliStacks}

We discuss a [[synthetic mathematics|synthetic]] formulation of Cartan connections in terms of [[differential cohesion]].

> under construction

Write

* $\Omega^1(-,\mathfrak{g})$ for the [[sheaf]] (on the [[site]] of [[formal manifold|formal]] [[smooth manifolds]]) of [[Lie algebra valued differential forms]], regarded as the [[smooth set|smooth]] [[moduli space]] of $\mathfrak{g}$-differential forms (as explained at _[[geometry of physics]]_ in the chapter _[[geometry of physics -- differential forms|on differential forms]]_)

* $\mathbf{B} G_{conn} \simeq \Omega^1(-,\mathfrak{g})//G$ for the universal [[moduli stack of connections]], which is equivalently the [[homotopy quotient]] of $\Omega^1(-,\mathfrak{g})$ by the [[action]] of $G$ (regarded as a [[smooth group]]) by [[gauge transformations]];

* $\Omega^1(-,\mathfrak{g})//H$ for the [[homotopy quotient]] by just the [[subgroup]] $H \hookrightarrow G$;

* $\mathbf{J} \;\colon\;\Omega^1(-,\mathfrak{g})//H \longrightarrow \Omega^1(-,\mathfrak{g})//G\simeq \mathbf{B}G_{conn}$ for the canonical morphism.

+-- {: .num_prop #MCFormAsFiberOfDifferentialModuli}
###### Proposition

There is a [[homotopy fiber sequence]] of [[smooth groupoids]]

$$
  \array{
     G/H &\stackrel{\theta/H}{\longrightarrow}& \Omega^1(-,\mathfrak{g})//H
     \\
     && \downarrow^{\mathrlap{\mathbf{J}}}
     \\
     && \mathbf{B}G_{conn}
  }
  \,,
$$

where $\theta/H$ is the $G$-[[Maurer-Cartan form]] modulo $H$.

=--

+-- {: .proof}
###### Proof

A detailed proof for the statement as given is spelled out at _[this proposition](orbit+method#ThetaAsHomotopyFiberOfJ)_.

But this statement holds generally in [[cohesive (∞,1)-toposes]] and an argument at this generality proceeds as follows: via the discussion at _[[∞-action]]_ the action of $G$ on $\Omega^1(-,\mathfrak{g})$ is exhibited by the forgetful map $\mathbf{B}G_{conn}\to \mathbf{B}G$ and since the action of $H$ on $\Omega^1(-,\mathfrak{g})$ is the restricted action, the square on the right of 

$$
  \array{
     G/H &\stackrel{\theta/H}{\longrightarrow}& \Omega^1(-,\mathfrak{g})//H
     &\longrightarrow& \mathbf{B}H
     \\
     \downarrow && \downarrow^{\mathrlap{\mathbf{J}}} && \downarrow
     \\
     \ast &\longrightarrow& \mathbf{B}G_{conn} &\longrightarrow& \mathbf{B}G
  }
$$

is a [[homotopy pullback]]. From this the [[pasting law]] implies that in the top left corner we have indeed $G/H$, this being the [[homotopy fiber]] of $\mathbf{B}H \to \mathbf{B}G$. Similar considerations show that the top left map is the abstractly defined [[Maurer-Cartan form]].

=--

+-- {: .num_example}
###### Example


For $G$ a [[semisimple Lie group|semisimple]] [[compact Lie group|compact]] [[Lie group]] and $H = T\hookrightarrow G$ a [[maximal torus]], then prop. \ref{MCFormAsFiberOfDifferentialModuli} plays a central role in the stacky formulation of the [[orbit method]]. See there at _[this proposition](orbit+method#ThetaAsHomotopyFiberOfJ)_.

=--

We need this and one more ingredient for synthetically formalizing Cartan connections:

+-- {: .num_remark #FactorizationOfConnection}
###### Remark

Let $\mathbb{D}^d_x \hookrightarrow X$ be the first-oder [[infinitesimal neighbourhood]] of a point in a manifold $X$. This being first order means that every [[differential p-form]] for $p \geq 2$ vanishes on $\mathbb{D}^d$. In particular therefore every [[principal connection]] restricted to $\mathbb{D}^d$ becomes a [[flat connection]] and hence is indeed gauge equivalent to the trivial connection. In particular every map

$$
  \mathbb{D}^d_x \longrightarrow \Omega^1(-,\mathfrak{g})//H \to \mathbf{B}G_{conn}
$$

has a null-homotopy, hence fits into a square of the form

$$
  \array{
    \mathbb{D}^d_x 
      &\stackrel{\nabla_H}{\longrightarrow}& 
    \Omega^1(-,\mathfrak{g})//H
    \\
    \downarrow &\swArrow_{\mathrlap{\simeq}}& \downarrow^{\mathrlap{\mathbf{J}}} 
    \\
    \ast &\longrightarrow& \mathbf{B}G_{conn}
  }
  \,.
$$

It follows by prop. \ref{MCFormAsFiberOfDifferentialModuli} that $\nabla_H$ here factors through the [[Maurer-Cartan form]]

$$
  \nabla_H|_{\mathbb{D}^d_x}
  \;\colon\;
  \mathbb{D}^d_x 
     \stackrel{}{\longrightarrow} 
  G/H 
     \stackrel{\theta/H}{\longrightarrow}
  \Omega^1(-,\mathfrak{g})//H
  \,.
$$

=--

The following is a synthetic formulation of Cartan connections, def. \ref{Traditional}. 

+-- {: .num_defn #CartanConnectionSynthetically}
###### Definition

Let $X$ be a [[smooth set]]. Then an _$(H \hookrightarrow G)$-Cartan connection_ on $X$ is

1. a $G$-[[principal connection]] 

   $$
     \nabla \colon X \longrightarrow \mathbf{B}G_{conn}
   $$

1. equipped with a [[reduction of structure groups]] given by a lift through $\mathbf{J}$ in prop. \ref{MCFormAsFiberOfDifferentialModuli}

   $$
     \array{
        && \Omega^1(-,\mathfrak{g})//H
        \\
        & {}^{\mathllap{\nabla^H}}\nearrow & \downarrow^{\mathrlap{\mathbf{J}}}
        \\
        X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}G_{conn}
     }
   $$

1. such that over each first-order [[infinitesimal neighbourhood]] $\mathbb{D}^d_x \hookrightarrow X$ any induced factorization, via remark \ref{FactorizationOfConnection},

   $$
     \mathbb{D}^d_x \stackrel{}{\longrightarrow} G/H
   $$

   is [[formally étale morphism|formally étale]].

=--


## Properties

### As encoding "rolling without sliding"

It is useful to decompose the definition of Cartan connection into two states:

1. the [[reduction of structure groups|reduction]] of the underlying principal bundles along $H \hookrightarrow G$;

1. the compatible connection data.

In the synthetic formulation [above](#InTermsOfSmoothModuliStacks) these two stages are reflected by the [[pasting law]] applied to the pullback pasting diagram of prop. \ref{MCFormAsFiberOfDifferentialModuli}: the lift

$$
  \array{
     && G/H &\stackrel{\theta/H}{\longrightarrow}& \Omega^1(-,\mathfrak{g})//H
     &\longrightarrow& \mathbf{B}H
     \\
     &{}^{\mathllap{\nabla_H}}\nearrow& \downarrow && \downarrow^{\mathrlap{\mathbf{J}}} && \downarrow
     \\
     X &\stackrel{\nabla}{\longrightarrow}& \ast &\longrightarrow& \mathbf{B}G_{conn} &\longrightarrow& \mathbf{B}G
  }
$$

may be thought of as being first of all a lift in

$$
  \array{
     && \mathbf{B}H 
    \\
     & \nearrow & \downarrow
    \\
    X &\longrightarrow& \mathbf{B}G
  }
  \,.
$$

Now the [[homotopy fiber sequence]]

$$
  \array{
     G/H &\longrightarrow& \mathbf{B}H
     \\
     && \downarrow
     \\
     && \mathbf{B}H
  }
$$

exhibits $\mathbf{B}H \to \mathbf{B}G$ as the universal $G/H$-[[fiber bundle]] [[associated bundle|associated]] to the $G$-[[universal principal bundle]], and exhibits this lift as a [[section]] of the $G/H$-[[fiber bundle]] $P \underset{G}{\times} G/H$ associated with the given $G$-[[principal bundle]] on $X$:

$$
  \array{
     && P \underset{G}{\times} G/H &\longrightarrow& \mathbf{B}H 
    \\
    &\nearrow & \downarrow && \downarrow
    \\
    X &=& X &\longrightarrow& \mathbf{B}G
  }
  \,.
$$

This section is what identifies each point of $X$ with a point in $G/H$, modulo $G$-action. More in detail, given any [[cover]] $U \to X$ equipped with a trivialization of $U \to X \to \mathbf{B}G$ then the induced map $U \to G/H$ identifies each point of this cover with a point in $G/H$.

One could at this point just demand that there is such a cover and trivialization such that this induced map $U \to G/H$ is [[formally étale morphism|formally étale]] (a [[local diffeomorphism]]). This would already serve the purpose of identifying each [[tangent space]] $T_x X$ with the tangent space $T_{e H} (G/H)$.

The full definition of Cartan connection demands that this identification is carried along by a compatible parallel transport. (...)


## Examples

### (pseudo-)Riemannian geometry

Let $G = Iso(d,1)$ be the [[Poincare group]] and $H \subset G$ the [[orthogonal group]] $O(d,1)$. Then the quotient

$$
  \mathfrak{iso}(d,1)/\mathfrak{so}(d,1) \simeq
  \mathbb{R}^{d+1}
$$

is [[Lorentzian spacetime]]. Therefore an $(O(d,1)\hookrightarrow Iso(d,1))$-Cartan connection is equivalently an $O(d,1)$-connection on a manifold whose [[tangent space]]s look like [[Minkowski spacetime]]: this is  equivalently a [[pseudo-Riemannian manifold]] from the perspective discussed at [[first-order formulation of gravity]]:

the $\mathbb{R}^{d+1}$-valued part of the connection is the [[vielbein]]. 

## Related concepts

* [[connection on a bundle]]

  * [[parallel transport]], [[holonomy]]

* [[principal connection]]

  * [[affine connection]], [[Levi-Civita connection]], **Cartan connection**

* [[connection on a 2-bundle]]

* [[connection on an ∞-bundle]]

  * [[higher Cartan geometry|∞-Cartan connection]]

  * [[higher parallel transport]]

[[!include local and global geometry - table]]


## References

[[Élie Cartan]] has introduced Cartan connections in his work on the Cartan's "method of moving frames" (cf. [[Cartan geometry]]).

A standard textbook reference is

* R. Sharpe, _Differential Geometry -- Cartan's Generalization of Klein's Erlagen program_ Springer (1997)
 {#Sharpe}


Further discussion of Cartan connections as models for the [[first order formulation of gravity]] is in 

* [[Derek Wise]], _MacDowell-Mansouri gravity and Cartan geometry_, Class.Quant.Grav.27:155010,2010 ([arXiv:gr-qc/0611154](http://arxiv.org/abs/gr-qc/0611154/))

* [[Gabriel Catren]], _Geometrical Foundations of Cartan Gauge Gravity_ ([arXiv:1407.7814](http://arxiv.org/abs/1407.7814))

See also

* wikipedia [Cartan connection](http://en.wikipedia.org/wiki/Cartan_connection)


[[!redirects Cartan connections]]