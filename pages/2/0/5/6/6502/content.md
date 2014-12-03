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

Cartan connections are also just called _[[Cartan geometries]]_ . 



## Definition

### Traditional

Let $G$ be a [[Lie group]] and $H \hookrightarrow G$  a sub-Lie group. (So that we may think of the [[coset space]] $G/H$ as a [[Klein geometry]].) Write $\mathfrak{h} \hookrightarrow \mathfrak{g}$ for the corresponding [[Lie algebras]]. 

+-- {: .num_defn}
###### Definition

A $(H \hookrightarrow G)$-Cartan connection over a [[smooth manifold]] $X$ is;

* a $G$-[[affine connection]] $\nabla$ on $X$;

* such that 

  1. there is a [[reduction of structure groups]] along $H \hookrightarrow G$;

  1. for each point $x \in X$ the canonical composite (for any local trivialization)

     $$
       T_x X \stackrel{\nabla}{\to} \mathfrak{g} \to \mathfrak{g}/\mathfrak{h}
     $$

     is an [[isomorphism]].

=--

This appears for instance as ([Sharpe, section 5.1](#Sharpe)).

### In terms of smooth moduli stacks
 {#InTermsOfSmoothModuliStacks}

In terms of [[smooth stacks]] the definition of Cartan connections has the following equivalent form.

Write

* $\Omega^1(-,\mathfrak{g})$ for the [[sheaf]] (on the [[site]] of [[smooth manifolds]]) of [[Lie algebra valued differential forms]], regarded as the [[smooth set|smooth]] [[moduli space]] of $\mathfrak{g}$-differential forms (as explained at _[[geometry of physics]]_ in the chapter _[[geometry of physics -- differential forms|on differential forms]]_)

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

is a [[homotopy pullback]]. From this the [[pasting law]] implies that in the top left coner we have indeed $G/H$, this being the [[homotopy fiber]] of $\mathbf{B}H \to \mathbf{B}G$. Similar considerations show that the top left map is the abstractly defined [[Maurer-Cartan form]].

=--

+-- {: .num_example}
###### Example

For $G$ a [[semisimple Lie group|semisimple]] [[compact Lie group|compact]] [[Lie group]] and $H = T\hookrightarrow G$ a [[maximal torus]], then prop. \ref{MCFormAsFiberOfDifferentialModuli} plays a central role in the stacky formulation of the [[orbit method]]. See there at _[this proposition](orbit+method#ThetaAsHomotopyFiberOfJ)_.

=--

+-- {: .num_defn}
###### Definition

Let $X$ be a [[smooth set]]. Then an _$(H \hookrightarrow G)$-Cartan connection_ on $X$ is

1. a $G$-[[principal connection]] 

   $$
     \nabla \colon X \longrightarrow \mathbf{B}G_{conn}
   $$

1. equipped with a [[reduction of the structure group]] given by a lift through $\mathbf{J}$ in prop. \ref{MCFormAsFiberOfDifferentialModuli}

   $$
     \array{
        && \Omega^1(-,\mathfrak{g})//H
        \\
        & {}^{\mathllap{\nabla^H}}\nearrow & \downarrow^{\mathrlap{\mathbf{J}}}
        \\
        X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}G_{conn}
     }
   $$

1. such that there exists an [&#233;tale atlas](differential+cohesion#CohesivemanifoldsSeparated) $p \colon \coprod_i G/H \to X$ over which the underlying $G$-[[principal bundle]] has a trivialization  and such that the morphism $\phi$ which is universally induced from this trivialization via prop. \ref{MCFormAsFiberOfDifferentialModuli}  is the [[codiagonal]] of an [[equivalence]]:


   $$
     \array{
       && G/H &\stackrel{\theta/H}{\longrightarrow}& \Omega^1(-,\mathfrak{g})/H
       \\
       & {}^{\mathllap{\phi}}_{\mathrlap{\coprod_i \simeq}}\nearrow && \swArrow_{\simeq} & \downarrow^{\mathrlap{\mathbf{J}}}
       \\
       \coprod_i G/H
       &\stackrel{p}{\longrightarrow}&
       X
       &\stackrel{\nabla}{\longrightarrow}&
       \mathbf{B}G_{conn}
     }
   $$

.

=--



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


See also

* [[Gabriel Catren]], _Geometrical Foundations of Cartan Gauge Gravity_ ([arXiv:1407.7814](http://arxiv.org/abs/1407.7814))

* wikipedia [Cartan connection](http://en.wikipedia.org/wiki/Cartan_connection)

[[!redirects Cartan connections]]