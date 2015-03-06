
> This entry is gouing to contain one chapter of _[[geometry of physics]]_.

> previous chapters: _[flat connections](geometry+of+physics#FlatConnections)_

> next chapter: _[principal connections](geometry+of+physics#PrincipalConnections)_ 

***

## De Rham coefficients

### Model Layer

#### Lie-algebra valued differential 1-forms

+-- {: .num_defn #SheafOfLieAlgebraValuedForms}
###### Definition

Let $G$ be a [[Lie group]], and write $\mathfrak{g}$ for its [[Lie algebra]]. The set of [[Lie algebra valued differential 1-forms]] is the [[tensor product]]

$$
  \Omega^1(U,\mathfrak{g}) = \Omega^1(U) \otimes_{\mathbb{R}} \mathfrak{g}
  \,.
$$

flat forms:

$$
  \Omega^1_{flat}(U, \mathfrak{g}) = 
  \left\{
    \omega \in \Omega^1(U,\mathfrak{g}) |
    F_\omega = \mathbf{d} \omega + [\omega, \omega] = 0
  \right\}

  \,.
$$

=--

(...)

This is a [[smooth space]]

$$
  \Omega^1_{flat}(-,\mathfrak{g}) \in Smooth 0 Type
$$

For $\mathfrak{g} = Lie(\mathbb{R})$ we have

$$
  \Omega^1(-,Lie(\mathbb{R})) = \Omega^1
$$

and we write

$$
  \Omega^1_{flat}(-,Lie(\mathbb{R})) = \Omega^1_{cl}
$$


Below we see

$$
  \flat_{dR}\mathbf{B}G \simeq \Omega^1_{flat}(-,\mathfrak{g})
$$

#### The de Rham complex

* [[de Rham complex]]

* [[de Rham cohomology]]

* [[de Rham theorem]]

Below we see that 

$$
  \flat_{dR}\mathbf{B}^n \mathbb{R} 
    \simeq
  \flat_{dR}\mathbf{B}^n U(1)
   \simeq
  DK[ \Omega^1(-) \stackrel{\mathbf{d}}{\to} \Omega^2(-) \stackrel{\mathbf{d}}{\to}\cdots \stackrel{\mathbf{d}}{\to} \Omega^n_{cl}(-)]
 \,.
$$

### Semantic Layer

#### De Rham coefficient objects

+-- {: .num_defn #deRhamCoefficientObject}
###### Definition


For $G \in Gpr(\mathbf{H})$, its **de Rham coefficient object**
is the [[homotopy pullback]]

$$
  \flat_{dR} \mathbf{B}G \coloneqq \flat \mathbf{B}G \times_{\mathbf{B}G} * 
$$

in

$$
  \array{
     \flat_{dR} \mathbf{B}G &\stackrel{UnderlyingConnection}{\to}& \flat \mathbf{B}G
     \\
     \downarrow &pb& \downarrow^{\mathrlap{UnderlyingBundle}}
     \\
     * &\to& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This pullback diagram expresses that [[generalized element|elements]] of $\flat_{dR}\mathbf{B}G$ are flat $G$-connections $\nabla \colon X \to \flat \mathbf{B}G$, def. \ref{FlatCohesiveConnection} equipped with a trivialization of their underlying $G$-principal bundle, def. \ref{UnderlyingBundleOfFlatConnection}.

=--


#### Recovering smooth differential forms from cohesive de Rham coefficients
 {#OrdinaryDifferentialFormsFromSmoothCohesion}

Let $\mathbf{H} = $ [[Smooth∞Grpd]]. All [[smooth manifolds]] and sheaves on smooth manifolds etc. in the following are canonically regarded as objects in this $\mathbf{H} = Sh_\infty(CartSp)$.

+-- {: .num_prop #DeRhamCoefficientsOfLieGroup}
###### Proposition

For $G$ a [[Lie group]], the de Rham coefficient object $\flat_{dR}\mathbf{B}G$, def. \ref{deRhamCoefficientObject} of its [[delooping]] is given by the [[sheaf]] of flat [[Lie algebra valued differential 1-forms]] $\Omega^1_{flat}(-,\mathfrak{g})$, def. \ref{SheafOfLieAlgebraValuedForms}, for $\mathfrak{g}$ the [[Lie algebra]] of $G$:

$$
  \flat_{dR}\mathbf{B}G \simeq \Omega^1_{flat}(-,\mathfrak{g})
  \,.
$$

=--

This is discussed at _[smooth ∞-groupoid - structures - de Rham coefficients for BG with G a Lie group](smooth+infinity-groupoid+--+structures#deRhamWithCoefficientsInBOfLieGroup)_.

Write $U(1)$ for the [[circle group]] regared as a [[Lie group]] in the standard way.

+-- {: .num_prop}
###### Proposition

For $n \in \mathbb{N}$, the de Rham coefficient object $\flat_{dR}\mathbf{B}^n U(1)$, def. \ref{deRhamCoefficientObject}, of the $n$-fold [[delooping]] of $U(1)$ is given by the image under the [[Dold-Kan correspondence]] 

$$
  DK \colon : Sh(CartSp, Ch_\bullet) \to Sh(CartSp, sSet)
  \to L_{lwhe} Sh(CartSp, sSet) \simeq \mathbf{H}
$$ 

of the truncated [[de Rham complex]] of sheaves of differential forms, 

$$
  \begin{aligned}
   \flat_{dR}\mathbf{B}^n U(1)
   &\simeq
   \flat_{dR} \mathbf{B}^n \mathbb{R}
   \\
   & \simeq
   DK[\Omega^1(-) \stackrel{\mathbf{d}}{\to} \cdots \stackrel{\mathbf{d}}{\to} \Omega^n_{cl}(-)]
    \\ 
   & \simeq DK[\Omega^1_{cl}(-) \to 0 \to  \cdots \to 0]
  \end{aligned}
  \,.
$$

=--

This is discussed at _[smooth ∞-groupoid - structures - de Rham coefficients for the circle n-groups](smooth+infinity-groupoid+--+structures#deRhamCoefficientsInBnU1)_.

### Syntactic Layer

$$
  \begin{aligned}
    \flat_{dR}(\mathbf{B}G \colon Type)\; \colon & Type
    \\
    \coloneqq & 
     \;\;
    \sum_{\nabla \colon \flat \mathbf{B}G}
    (  UnderlyingBundle(\nabla) = * )
  \end{aligned}
$$

## **Maurer-Cartan forms**
 {#MaurerCartanForms}


### Model Layer
 {#MaurerCartanLayerMod}


#### Maurer-Cartan form on a Lie group
 {#MaurerCartanFormOnLieGroup}


* [[Maurer-Cartan form]]

$$
  \theta_G \colon G \to \Omega^1_{flat}(-,\mathfrak{g})
$$


Consider

$$
  \flat_{dR} \mathbf{B}\mathbb{R}  = \Omega^1_{cl}
$$

the Maurer-Cartan form on $\mathbb{R}$ is the [[de Rham differential]]

$$
  \theta_{\mathbb{R}} = \mathbf{d} \colon \mathbb{R} \to \Omega^1_{cl} \hookrightarrow \Omega^1
  \,.
$$






### Semantic Layer

#### Maurer-Cartan form on a cohesive $\infty$-group

Let $\mathbf{H}$ be a [[cohesive (infinity,1)-topos]] $(\mathbf{\Pi} \dashv \flat \dashv \sharp)$. We discuss a general formulation of [[Maurer-Cartan forms]] on cohesive [[infinity-groups]]


Let $G \in Grp(\mathbf{H})$ be a [[group object in an (infinity,1)-category|group object]]. 

Use the [[pasting law]] together with the fact that $\flat$ is
[[right adjoint]] and hence preserves [[limits]] to get $\theta$ in

$$
  \array{
    G &\to& *
    \\
    \downarrow^{\mathrlap{\theta}} & pb & \downarrow
    \\
    \flat_{dR} \mathbf{B}G &\to& \flat \mathbf{B}G
    \\
    \downarrow &pb& \downarrow
    \\
    * &\to& \mathbf{B}G
  }
$$

+-- {: .num_defn #GeneralAbstractMaurerCartanForm}
###### Definition

This is the **[[Maurer-Cartan form]]** on $G$

$$
  \theta \;\colon\; G \to \flat_{dR} \mathbf{B}G
  \,.
$$

=--

+-- {: .num_defn #DifferentiationOfInfinityGroupValuedFunction}
###### Definition

For $S \;\colon\; X \to G$ a morphism, write

$$
  S^{-1} \mathbf{d} S 
  \coloneqq S^* \theta_G
  \;\colon\;
  X \stackrel{S}{\to}
  G
  \stackrel{\theta_G}{\to}
  \flat_{dR}\mathbf{B}G
$$

for its composite with the map of def. \ref{GeneralAbstractMaurerCartanForm}, hence the **pullback of the Maurer-Cartan form along $S$**. We also call this the **[[de Rham differential]]** of $S$.

=--

#### Maurer-Cartan forms on smooth $\infty$-groups

+-- {: .num_prop}
###### Proposition

For $G$ a [[Lie group]] canonically regarded  in $\mathbf{H} = $[[Smooth∞Grpd]] the general abstract morphism

$$
  \theta_G \colon G \to \flat_{dR}\mathbf{B}G
$$

is identified, via the identification $\flat_{dR}\mathbf{B}G \simeq \Omega^1_{flat}(-,\mathfrak{g})$  of prop. \ref{DeRhamCoefficientsOfLieGroup} and the [[Yoneda lemma]], with the traditional [[Maurer-Cartan form]] 


$$
  \theta_G \in \Omega^1_{flat}(G, \mathfrak{g})
  \,.
$$

=--

#### Cohesive differentiation 
 {#CohesiveDifferentiation}

The Maurer-Cartan form on the [[line object]]

$$
  \theta_{\mathbb{R}} \colon \mathbb{R} \to \Omega^1_{cl}(-,\mathbb{R})
$$

is the [[de Rham differential]], 

$$
  \mathbf{d} = \theta_{\mathbb{R}}
  \,.
$$

#### Universal curvature characteristic forms

For $G = \mathbf{B}^n U(1)$

$$
  curv \colon \mathbf{B}^n U(1) \to \flat_{dR} \mathbf{B}^{n+1}U(1)
$$

sends a circle $n$-bundle to the curvature of a pseudo-connection on it.

### Syntactic Layer

(...)