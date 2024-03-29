
> under construction, notes related to material that appears in detail elsewhere, see the [References](#References).


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Local 2d prequantum boundary field theory and KK-Quantization

### **1)** Local 2d prequantum field theory

ambient [[(∞,1)-topos]] $\mathbf{H} = $ [[Smooth∞Grpd]]. 

We use in there mostly just the [[full sub-(∞,1)-category]]

$$
  DiffStack \hookrightarrow SmoothGrpd \hookrightarrow Smooth \infty Grpd
$$

of [[differentiable stacks]], i.e. the full subcategory on object that are presented by [[Lie groupoids]] but as [[coefficients]] at least we also need [[smooth infinity-groupoid|smooth 2-groupoids]].

In particular, write $\mathbf{B}^2 U(1)$ for the [[smooth 2-groupoid]] which is the [[circle 3-group]]. 

For $\mathbf{Fields} \in \mathbf{H}$ a [[moduli stack]] of [[field (physics)|fields]], we say that a map

$$
  \array{
    \mathbf{Fields}
    \\
    \downarrow^{\mathrlap{exp(i S)}}
    \\
    \mathbf{B}^2 U(1)
  }
$$

is a [[local action functional]]. 

(More generally we consider [[smooth super ∞-groupoids]] and replace $\mathbf{B}^2 U(1)$ by the moduli stack of [[super 2-line bundles]].)

Since this is necessarily a [[dualizable objects]] in the [[(∞,2)-category]] of [[(∞,n)-category of correspondences|correspondences]] $Corr_2(\mathbf{H}, \mathbf{B}^2 U(1))$ it induces by the [[cobordism theorem]] a **[[local prequantum field theory]]** given by a [[monoidal (∞,n)-functor|monoidal (∞,2)-functor]]

$$
  \array{      
    && Corr_2(\mathbf{H},\mathbf{B}^2 U(1)) &\to& Corr_2(\mathbf{H}, KU Mod)
    \\
    & {}^{\mathllap{\exp(i S)}}\nearrow&  \downarrow
    \\
    Bord_n &\stackrel{\mathbf{Fields}}{\to}& Corr_2(\mathbf{H})
  }
$$

Here we postcomposed with [[geometric realization]]

$$
  \mathbf{B}^2 U(1)
  \to
  {\vert \mathbf{B}^2 U(1)\vert}
  \simeq
  K(\mathbb{Z},3)
  \to
  B gl_1(KU)
  \to
  KU Mod
  \,.
$$

### **2)** Local boundary 2d prequantum field theory

Considering one marked boundary condition we have [[boundary field theory]] defined in addition to the data of $\exp(i S) \colon \mathbf{Fields} \to KU Mod$ by a morphisms in $Corr_2(\mathbf{H}, KU Mod)$ which as a [[diagram]] in $\mathbf{H}$ is of the form

$$
  \array{
    && Q
    \\
    & \swarrow && \searrow^{\mathrlap{i}}
    \\
    \ast && \swArrow_{\mathrlap{\xi}} && \mathbf{Fields}
    \\
    & {}_{\mathllap{\mathbb{I}}}\searrow
    &&
    \swarrow_{\mathrlap{\exp(i S)}}
  }
  \,.
$$

This is the _[[boundary condition]]_.


### **3)** Quantization in KK-Theory
 {#QuantizationInKKTheory}

We [[quantization|quantize]] by interpreting the [[path integral]] as [[push-forward in generalized cohomology]] in [[complex topological K-theory]] $KU$.

Specifically we quantize a correspondence as above by applying the following procedure

1. Decompose the correspondence explicitly as

   $$
     \array{
       && Q
       \\
       & \swarrow && \searrow^{\mathrlap{i}}
       \\
       \ast &\swArrow_{\mathrlap{\xi}}& \downarrow^{\mathrlap{i^\ast \chi}}  && \mathbf{Fields}
       \\
       & {}_{\mathllap{\mathbb{I}}}\searrow
       &&
       \swarrow_{\mathrlap{\chi}}
       \\
       && KU Mod
     }
     \,.
   $$


1. Form [[twisted groupoid convolution algebras]] to produce a [[co-span]] of [[Hilbert bimodules]]


   $$
     \mathbb{C} \stackrel{\xi}{\to}
     C_{i^\ast \chi}(Q)
     \stackrel{i^\ast}{\leftarrow}
     C_\chi(X)
     \,.
   $$

   Regard this as a cospan in [[KK-theory]].

1. Assume that the middle and right objects are [[dualizable objects]]. Choose a map in [[KK-theory]]

   $$
     Th(Q)
     \colon
     \left(C_{i^\ast \chi}\left(Q\right)\right)
     \to
    \left(C_{i^\ast \chi}\left(Q\right)\right)^{\vee}
   $$

   to the dual [[C*-algebra]]. (If this is an KK-[[equivalence]] then this is the [[Thom isomorphism]] in this context.)

1. Consider the [[dual morphism]] to $i^\ast$, to be denoted

   $$
     i_! \;\colon\; 
     \left(C_{i^\ast}\left(Q\right)\right)^{\vee}
     \to
     \left(C_\chi\left(X\right)\right)^\vee
   $$

   and then turn the above cospan into the following consecutive composite in [[KK-theory]]

   $$
     i_! Th\left(Q_{i^\ast \chi}\right) \xi
     \colon
     \mathbb{C}
     \stackrel{\xi}{\to}
     C_{i^\ast \chi}(Q)
     \stackrel{Th}{\to}
     (C_{i^\ast \chi}(Q))^\vee
     \stackrel{i_!}{\to}
     (C_{\chi}(X))^\vee
     \,.
   $$

   This we regard as the quantization of the boundary correspondence.

(...)
 

## 2d Poisson Chern-Simons theory -- Idea

### General

We discuss aspects of the [[extended geometric quantization]] of one of the simplest and yet interesting examples of [[schreiber:∞-Chern-Simons theory]], namely [[2d Chern-Simons theory]] and here specifically the case induced by a binary and non-degenerate [[invariant polynomial]], namely the [[Lie integration|Lie integrated]] version of the [[Poisson sigma-model]].

It turns out that several aspects of the [[extended geometric quantization]] of this 2d [[theory (physics)|theory]] are known in the literature already, albeit in disguise: the [[2-plectic geometry|2-plectic]] [[moduli stack]] of [[field (physics)|fields]] is equivalently what in the literature is known as a _[[symplectic groupoid]]_ and its [[higher geometric quantization]] is essentially what is known as the _[[geometric quantization of symplectic groupoids]]_.

The suggestion that there should be such a relation is contained already in ([Cattaneo-Felder 01](symplectic%20groupoid#CattaneoFelder01)), but at the time of that writing the [[geometric quantization of symplectic groupoids]] had not been performed yet.

To some extent in the following we review the traditional [[geometric quantization of symplectic groupoids]] while showing at the same time how its ingredients are (more) naturally interpreted in [[higher symplectic geometry]]. This makes quantization of symplectic groupoids a good test case against which to check notions of [[higher geometric quantization]].

Specifically, we discuss what should be the first nontrivial case of the Chern-Simons-type _[[holographic principle]]_ realized in [[higher geometric quantization]]: The [[moduli stack]] of the [[2d Chern-Simons theory]] is the [[Lie integration]] of the [[Poisson Lie algebroid]] associated to a [[Poisson manifold]]. The latter we may think of as defining a [[quantum mechanical system]], hence a $(2-1) = 1$-dimensional [[quantum field theory]]. The higher geometric quantization of the 2-d theory yields a [[2-vector space]] [[space of states|of quantum 2-states]] (assigned to the point n codimension 2). Under the identification of [[2-vector spaces]] with [[categories of modules]] over an [[associative algebra]], this space of quantum 2-states identifies (the [[Morita equivalence]]-class of) an algebra. Suitably re-interpreting traditional results about the quantization of symplectic groupods shows that this algebra serves as a kind of [[strict deformation quantization]] of that [[Poisson manifold]] &lbrack;[Hawkins (2008)](#Hawkins08)&rbrack;.

Notice that at the level of just infinitesimal ("formal") [[deformation quantization]] a similar [[holographic principle|holographic]] relation between quantization of a Poisson manifold and of its associated 2d [[sigma-model]] QFT has famously been shown by [[Alberto Cattaneo]] and [[Giovanni Felder]] to underly [[Kontsevich]]'s construction of deformation quantization (see at _[[Poisson sigma-model]]_). We suggest that the discussion here provides the refinement of this relation to [[strict deformation quantization]].

All of this should be a blueprint for an analogous situaton in one dimension higher, where the analogous procedure should reproduce the famous holographic quantization of the [[2d Wess-Zumino-Witten theory]] in terms of that of a [[3d Chern-Simons theory]].

### Identifying "symplectic groupoids" as 2-plectic groupoids

We briefly indicate the basis for re-interpreting traditional [[symplectic groupoid]]-theory in terms of [[higher symplectic geometry]].

The identification of the traditional notion of "[[symplectic groupoid]]" as really a [[2-plectic geometry|2-plectic]] structure is evident as soon as one translates the traditional definition of a [[symplectic groupoid]] to more intrinsic language of [[smooth infinity-groupoid|higher differential geometry]]. We discuss this in detail below, but in brief it works as follows: 

A [[symplectic groupoid]] $(\mathbf{X},\omega)$ is traditionally defined to be a [[Lie groupoid]] $\mathbf{X}$ which is equipped with a (non-degenerate) [[differential 2-form]] $\omega \in \Omega^2(\mathbf{X}_1)$ on its [[smooth manifold]] of [[morphisms]], such that it is annihilated by the [[de Rham differential]] as well as by 
the operator $\delta$ that sums the [[pullback of differential forms|pullback]] of $\omega$ to the space $\mathbf{X}_2$ of composable morphisms along the [[source]] and [[target]] maps and minus that along the [[composition]] map.
But together this just means that regarded as a triple $(0, \omega, 0) \in \underset{k = 0,1,2}{\oplus} \Omega^{3-k}(\mathbf{X}_k)$ the symplectic form is a  [[cocycle]] in the [[simplicial de Rham complex]] over the [[simplicial manifold]] which is the [[nerve]] of the Lie groupoid. And this finally means fully intrinsically that $\omega$ is a degree-3 [[cocycle]] in the [intrinsic de Rham cohomology](cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology) [of smooth ∞-groupoids](smooth+infinity-groupoid+--+structures#deRhamCoefficientsInBnU1) over $\mathbf{X}$, which we denote by

$$
  \omega \;\colon\; \mathbf{X} \to \flat_{dR} \mathbf{B}^3 U(1)
  \,.
$$

This simple observation shows that [[symplectic groupoids]], which in traditional literature are treated as a topic in [[symplectic geometry]], are really objects in [[higher symplectic geometry]], namely in [[2-plectic geometry]]. 

More specifically, if $(X,\pi)$ is a [[Poisson manifold]], there is canonically associated with it a [[Lie algebroid]] $\mathfrak{P}$, the _[[Poisson Lie algebroid]]_. This is an example of a [[symplectic Lie n-algebroid]] and as such it carries a canonical binary [[invariant polynomial]]. Together this serves as the [[target space]] and [[background gauge field]] of what is called the [[Poisson sigma-model]]. But moreover, the [[Lie integration]] of this data is the [[extended Lagrangian]] of an [[schreiber:∞-Chern-Simons theory]], namely a map

$$
  \mathbf{L}
  \;\colon\;
  \tau_1\exp(\mathfrak{P})_{conn}
  \to 
  \mathbf{B}^2 (\mathbb{R}/\Gamma)_{conn}
$$

from the [[moduli stack]] of [[field (physics)|fields]] of the [[2d Chern-Simons theory]] to that of [[circle 2-bundles with connection]].

If we [[concretify]] the moduli stack by forgetting the connection data here and just consider the underlying [[instanton sectors]], then this is precisely the symplectic groupoid data above

$$
  \array{
    \tau_1\exp(\mathfrak{P})_{conn}
    &\stackrel{\mathbf{L}}{\to}& 
    \mathbf{B}^2 (\mathbb{R}/\Gamma)_{conn}
    \\
    {}^{\mathllap{concretify}}\downarrow && \downarrow
    \\
    \mathbf{X} &\stackrel{\omega}{\to}& \flat_{dR} \mathbf{B}^3 U(1)
  }
  \,.
$$

It is in this way that we may identify the [[symplectic groupoid]] of a Poisson manifold

$$
  \mathbf{X} \simeq \tau_1 \exp(\mathfrak{P})
$$

as the [[moduli stack]] of the [[extended prequantum field theory|extended prequantum]] [[2d Chern-Simons theory]] which refines the [[Poisson sigma-model]].

Hence we identify the [[geometric quantization]] of $(\mathbf{X}, \omega)$ as the extended geometric quantization of the [[2d Chern-Simons theory]]. But traditional literature shows (and this was motivation for introducing [[symplectic groupoids]] in the first place) that this encodes the [[quantization]] of the [[Poisson manifold]] $(X, \pi)$ itself, regarded as a [[quantum mechanical system]]. This is the traditional topic of _[[geometric quantization of symplectic groupoids]]_.

Taken together this says: the [[extended geometric quantization]] of the [[extended prequantum field theory|extended prequantum]] [[Poisson sigma-model]] computes the ordinary [[geometric quantization]] of the underlying Poisson manifold.

This statement we recognize as a geometric quantization analog of a famous relation in [[algebraic deformation quantization]]. As discussed there, the construction by [[Kontsevich]] of the algebraic deformation quantization of any Poisson manifold was identified by [[Cattaneo]] and [[Felder]] as a limiting case of the  [[n-point function|3-point function]] in the [[perturbation theory|perturbative quantization]] of the corresponding 2d Poisson $\sigma$-model.

These relations to traditional theory we use in the following to explore aspects of the [[extended geometric quantization]] of [[2d Chern-Simons theory]].

### Summary and survey

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## General theory

We use the general tools for formulating notions in [[physics]] in terms of [[higher differential geometry]] as discussed at _[[geometry of physics]]_. Here we just collect some of the main ingredients needed below.

+-- {: .num_defn}
###### Definition

We write

$$
  DL
  \;\colon\;
  [CartSp^{op}, Ch_\bullet(Ab)]
  \stackrel{\simeq}{\to}
  [CartSp^{op}, Ab^{\Delta^{op}}]
  \stackrel{forget}{\to}
  [CartSp^{op}, KanCplx]
  \stackrel{}{\to}
  L_{lhe} 
  [CartSp^{op}, KanCplx]
  \simeq
  Smooth\infty Grpd  
$$

where the first equivalence is the [[Dold-Kan correspondence]] and the last map is the map to the [[simplicial localization]].

=--

+-- {: .num_defn}
###### Definition

For $k,n \in \mathbb{N}$, $k \leq n$ we write

$$
  \mathbf{B}^n U(1)_{conn^k}
  \coloneqq
  DK\left[
    \underline{U}(1)
    \stackrel{\mathbf{d}}{\to}
    \Omega^1 
    \stackrel{\mathbf{d}}{\to}
    \cdots
    \stackrel{\mathbf{d}}{\to}
    \Omega^k
    \stackrel{}{\to}
    0
    \stackrel{}{\to}
    \cdots
    \stackrel{}{\to}
    0
  \right]
$$

with $\Omega^k$ in degree $(n-k)$ (hence with $(n-k)$ vanishing entries on the right). 

In particular

* $\mathbf{B}^n U(1) \simeq \mathbf{B}^n U(1)_{conn^0}$

* $\mathbf{B}^n U(1)_{conn} \simeq \mathbf{B}^n U(1)_{conn^n}$.

=--


+-- {: .num_example}
###### Example

For $n,k \in \mathbb{N}$, $k \lt n$ we have

1. $\Omega (\mathbf{B} U(1)_{conn}) \simeq \flat \mathbf{B}^{n-1}$

1. $\Omega (\mathbf{B}^n U(1)_{conn}^k) \simeq \mathbf{B}^{n-1} U(1)_{conn}^k$.

=--

(...)

$$  
  \array{
    field space
    &&
    \tau_n \exp(\mathfrak{a})_{conn}
    &\to&
    \mathbf{B}^n U(1)_{conn}
    \\
    && \downarrow && \downarrow
    \\
    delooped phase space && \tau_n \exp(\mathfrak{a})
    &\to&
    \mathbf{B}^n U(1)_{conn^{n-1}}
  }
$$

$$
  \array{
    C_0 &\to& *
    \\
    \downarrow && \downarrow 
    \\
    \tau_n \exp(\mathfrak{a}) &\to& \mathbf{B}^n U(1)_{conn^{n-1}} 
    \\
    \uparrow && \uparrow 
    \\
    C_1 &\to& *
  }
$$

under [[homotopy fiber product]] this yields the phase space prequantum bundle

$$
  Phase(C_0, C_1) \to \mathbf{B}^{n-1}U(1)_{conn}
  \,.
$$

(...)

## The setup

Let $(X, \pi)$ be a [[Poisson manifold]], which we tend to think of as defining a _[[quantum mechanical system]]_. This canonically induces the structure of [[Lie algebroid]] over $X$, the _[[Poisson Lie algebroid]]_ $(\mathfrak{P}, \mathbf{\omega})$ over $X$. This is a [[symplectic Lie n-algebroid|symplectic Lie algebroid]], with graded symplectic form (binary [[invariant polynomial]]) $\mathbf{\omega}$ which is in [[transgression]] with the Poisson tensor $\pi$, regarded as a [[Lie algebroid cohomology|Lie algebroid cocycle]]. The transgression is witnessed by a [[Chern-Simons element]] $cs_\pi$. 

### Moduli stack of fields

By the general construction of [[schreiber:infinity-Chern-Simons theory]] this means that there is a universal differential characteristic map

$$
  \mathbf{L}
  \;\colon\;
  \exp(\mathfrak{P})_{conn}
  \to 
  \mathbf{B}^2 \mathbb{R}_{conn}
$$

and its truncation ([[Lie integration]])


$$
  \mathbf{L}
  \;\colon\;
  \tau_1 \exp(\mathfrak{P})_{conn}
  \to 
  \mathbf{B}^2 (\mathbb{R}/\Gamma)_{conn}
  \,.
$$

Here $\tau_1 \exp(\mathfrak{P})_{conn}$ is the [[smooth groupoid|smooth]] [[moduli stack]] of fields of the 2d Poisson-Chern-Simons theory and
$\mathbf{H}$ is the [[extended Lagrangian]] of a [[2d Chern-Simons theory]] ([[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models|FRS]]). Infinitesimally this yields the [[Poisson sigma-model]].

We discuss here the [[higher geometric quantization]] of this [[theory (physics)|theory]] defined by $\mathbf{L}$.

### The Phase space stack
 {#ThePhaseSpaceStack}

There is the canonical universal forgetful map

$$
  \tau_1 \exp(\mathfrak{P})_{conn}
  \to
  \tau_1 \exp(\mathfrak{P})
$$

which forgets the conection data of fields and only retains their "[[instanton sector]]". The [[smooth groupoid]] $\tau_1 \exp(\mathfrak{P})$ is the [[symplectic groupoid]] which is the [[Lie integration]] of the [[Poisson Lie algebroid]] $\mathfrak{P}$. (In the traditional literature this is called the symplectic groupoid only if it happens to be representable by a [[Lie groupoid]], hence if $\mathfrak{P}$ is integrable in the traditional sense of Lie groupoid theory.)

Notice that this is equivalently [[differential concretification]] over the point: $\tau_1 \exp(\mathfrak{P})$ may be understood as the [[smooth groupoid|smooth]] [[moduli stack]] of $\mathfrak{P}$-[[Lie algebroid valued differential forms|valued]] forms on the point.

But moreover, we may think of $\tau_1 \exp(\mathfrak{P})$ as being the [[phase space]] of the [[open string]] 2d Poisson-Chern-Simons [[sigma-model]] for the space-filling [[D-brane]] boundary condition: in this interpretation the [[objects]] of $\tau_1 \exp(\mathfrak{P})$ are the endpoints of open strings, the [[morphisms]] are solutions to the [[Euler-Lagrange equations]] of motion along an interval (an initial spatial slice of string) and [[composition]] is string concatenation. 

This is the point of view suggested in ([Cattaneo-Felder 01](symplectic%20groupoid#CattaneoFelder01)), there argued for by the observation that the space of [[morphisms]] of $\tau_1 \exp(\mathfrak{P})$ is naturally the [[symplectic reduction]] of (in our language) of that of $\tau_1 \exp(\mathfrak{P})$ for the [[moment map]] that characterizes the [[equations of motion]] and [[gauge symmetries]] of the [[Poisson sigma-model]].

### D-branes
 {#DBranes}

Let $\mathfrak{C}_0, \mathfrak{C}_1 \hookrightarrow \mathfrak{P}$ be two [[Lagrangian dg-submanifold|Lagrangian]] sub-[[Lie algebroids]] of the given [[Poisson Lie algebroid]]. These correspond to [[coisotropic submanifolds]] of the underlying [[Poisson manifold]]. 

Accoring to ([Cattaneo-Felder 03](coisotropic+submanifold#CattaneoFelder03)) we are two think of these as being two [[D-brane]] inclusions for the [[open string]] Poisson-Chern-Simons model.

Their [[Lie integration]] induces two Lagrangian sub-groupoids of the [[symplectic groupoid]]

$$
  tau_1 \exp(\mathfrak{C}_0)
  \to
  \tau_1 \exp(\mathfrak{P})
  \leftarrow
  \tau_1 \exp(\mathfrak{C}_1)
  \,.
$$

This means that the [[moduli stack]] of [[open strings]] with endpoints restricted to these two [[D-branes]] is the [[homotopy fiber product]] of [[smooth groupoids]]

$$
  \array{
    & & \mathbf{Fields}_{\mathfrak{C}_0, \mathfrak{C}_1}
    \\
    & \swarrow && \searrow
    \\
    \tau_1 \exp(\mathfrak{C}_0) && && \tau_1 \exp(\mathfrak{C}_1)
    \\
    & \searrow && \swarrow
    \\
    && \tau_1 \exp(\mathfrak{P})
  }
  \,.
$$

One finds that this [[homotopy pullback]] is equivalently the [[symplectic reduction]] considered in ([Cattaneo-Felder 03, page 6, 7](coisotropic+submanifold#CattaneoFelder03)).

That for space-filling branes $\mathfrak{C}_0, \mathfrak{C}_1 \coloneqq \mathfrak{P}$ one recovers the original moduli stack

$$
  \mathbf{Fields}_{\mathfrak{P}, \mathfrak{P}}
  \simeq
  \tau_1 \exp(\mathfrak{P})
$$

is just the statement that the homotopy pullback of an equivalence is an equivalence.

## Constructions

### Moduli of 2d CS fields and symplectic groupoids

We discuss how the [[moduli stack]] of the [[2d Chern-Simons theory]] obtained by [[Lie integration]] of the [[Poisson sigma-model]] is a [[symplectic groupoid]].

Let $\mathfrak{P}$ be the [[Poisson Lie algebroid]] corresponding to a [[Poisson manifold]] that comes from a [[symplectic manifold]] $(X,\omega)$.

The [[symplectic groupoid]] associated to this is (by the discussion there) supposed to be the [[fundamental groupoid]] 
$\Pi_1(X)$ of $X$ equipped on its space of morphisms with the differential form $p_1^* \omega - p_2^* \omega$, where $p_1,p_2$ are the two endpoint projections from paths in $X$ to $X$.

We demonstrate in the following how this is indeed the result of applying the [[∞-Chern-Weil homomorphism]] to this situation.

For simplicity we shall start with the simple situation where $(X,\omega)$ has a global [[Darboux coordinate chart]] $\{x^i\}$. Write $\{\omega_{i j}\}$ for the components of the [[symplectic form]] in these coordinates, and $\{\omega^{i j}\}$ for the components of the [[inverse]].


Then the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{P})$ is generated from $\{x^i\}$ in degree 0 and $\{\partial_i\}$ in degree 1, with differential given by

$$
  d_{CE} x^i = - \omega^{i j} \partial_j
$$

$$
  d_{CE} \partial_i = \frac{\partial \pi^{j k}}{\partial x^i} \partial_j \wedge \partial_k = 0
  \,.
$$

The differential in the corresponding [[Weil algebra]] is hence

$$
  d_{W} x^i = - \omega^{i j} \partial_j + \mathbf{d}x^i
$$

$$
  d_{W} \partial_i = \mathbf{d} \partial_i
  \,.
$$


By the discussion at [[Poisson Lie algebroid]], the symplectic [[invariant polynomial]] is

$$
  \mathbf{\omega} = \mathbf{d} x^i \wedge \mathbf{d} \partial_i \in W(\mathfrak{P})
  \,.
$$

Clearly it is useful to introduce a new basis of generators with

$$
  \partial^i := -\omega^{i j} \partial_j
  \,.
$$

In this new basis we have a manifest isomorphism

$$
  CE(\mathfrak{P}) = CE(\mathfrak{T}X)
$$

with the [[Chevalley-Eilenberg algebra]] of the [[tangent Lie algebroid]] of $X$. 

Therefore the [[Lie integration]] of $\mathfrak{P}$ is the [[fundamental groupoid]] of $X$, which, since we have assumed global Darboux oordinates and hence [[contractible]] $X$, is just the [[pair groupoid]]:

$$
  \tau_1 \exp(\mathfrak{P}) = \Pi_1(X) = (X \times X \stackrel{\overset{p_2}{\to}}{\underset{p_1}{\to}} X)
  \,.
$$

It remains to show that the symplectic form on $\mathfrak{P}$ makes this a [[symplectic groupoid]].

Notice that in the new basis the invariant polynomial reads

$$
  \begin{aligned}
    \mathbf{\omega} 
      &= 
     - \omega_{i j} \mathbf{d}x^i \wedge \mathbf{d} \partial^j 
     \\
      & = \mathbf{d}( \omega_{i j} \partial^i \wedge \mathbf{d}x^j)
   \end{aligned}
$$

and that we may regard this as a morphism of $L_\infty$-algebroids

$$
  \mathbf{\omega}
   : 
  \mathfrak{T}\mathfrak{P} \to \mathfrak{T}b^3 \mathbb{R}
$$

The corresponding [[infinity-Chern-Weil theory|infinity-Chern-Weil homomorphism]] that we need to compute is given by the [[∞-anafunctor]]

$$
  \array{
    \exp(\mathfrak{P})_{diff}
     &\stackrel{\exp(\mathbf{\omega})}{\to}&
    \exp(b \mathbb{R})_{dR}
    &\stackrel{\int_{\Delta^\bullet}}{\to}&
    \mathbf{\flat}_{dR}\mathbf{B}^3 \mathbb{R} 
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{P})
  }
  \,.
$$


Over a test space $U$ in degree 1 an element in $\exp(\mathfrak{P})_{diff}$ is a pair
$(X^i, \eta^i)$

$$
  X^i \in C^\infty(U \times \Delta^1)
$$

$$
  \eta^i \in \Omega^1_{vert}(U \times \Delta^1)
$$

subject to the verticality constraint, which says that along $\Delta^1$ we have

$$
  d_{\Delta^1} X^i + \eta^i_{\Delta^1} = 0
  \,.
$$

The vertical morphism $\exp(\mathfrak{P})_{diff} \to \exp(\mathfrak{P})$ has in fact a [[section]] whose image is given by those pairs for which $\eta^i$ has no leg along $U$. We therefore find the desired form on $\exp(\mathfrak{P})$ by evaluating the top morphism on pairs of this form. 

Such a pair is taken by the top morphism to

$$
  \begin{aligned}
    (X^i, \eta^j) 
     & \mapsto 
   \int_{\Delta^1}
    \omega_{i j} F_{X^i} \wedge F_{\partial^j}
   \\
    & =
  \int_{\Delta^1}
    \omega_{i j} (d_{dR} X^i + \eta^i) \wedge d_{dR} \eta^j
  \in 
  \Omega^3(U)
  \end{aligned}
  \,.
$$

Using the above verticality constraint and the condition that $\eta^i$ has no leg along $U$, this becomes

$$
  \cdots = 
  \int_{\Delta^1}
  \omega_{i j}
    d_U X^i 
  \wedge
    d_U d_{\Delta^1} X^j 
  \,.
$$

By the [[Stokes theorem]] the integration over $\Delta^1$ yields

$$
  \cdots 
    =
  \omega_{i j} d_{dR} x^i \wedge \eta^j|_{0}
   -
  \omega_{i j} d_{dR} x^i \wedge \eta^j|_{1}
  \,.
$$

This completes the proof.

$$
  \array{
    X &\to& *
    \\
    \downarrow && \downarrow
    \\
    \tau_1 \exp(\mathfrak{P})
    &\stackrel{\omega}{\to}&
    \flat_{dR} \mathbf{B}^3 U(1)
  }
  \,.
$$

### Prequantum 2-states

Generally, given a [[prequantum line 2-bundle]] the corresponding (local) [[prequantum n-states]] are the (local) [[sections]] of this [[line 2-bundle]], and these in turn are equivalently the [[twisted unitary bundles]] (maybe best known for the [[WZW model]] where these are the [[Chan-Paton gauge fields]]). These 2-sections/twisted bundles form a [[2-vector space]] of prequantum 2-states. This is equivalently a [[category of modules]] over some [[associative algebra]], well defined up to [[Morita equivalence]]. 

A canonical way of constructing this algebra is as follows: present the [[line 2-bundle]] as a [[bundle 2-gerbe]], hence as a multiplicative [[line bundle]] over the morphisms of a [[Lie groupoid]], then the algebra is the [[groupoid algebra]] (see there for details) of sections of this line bundle. A module over this is manifestly a [[bundle gerbe module]], which in turn is equivalently a unitary bundle twisted by the line 2-bundle.


More in detail:

Let $\mathbf{X}$ be a smooth groupoid and $\mathbf{X} \to \mathbf{B}^2 U(1)$ the map modulating a [[circle 2-group]]-[[principal 2-bundle]] $P \to \mathbf{X}$.

Let $(\coprod_n \mathbf{B}U(n))//\mathbf{B}U(1) \to \mathbf{B}^2 U(1)$ the canonical [[infinity-action|2-representation]], the sections of the [[associated infinity-bundle|associated 2-bundle]] are unitary [[twisted bundles]] equivariant on $\mathbf{X}$.

If we present the 2-bundle by a [[bundle gerbe]] exhibited as a multiplicative [[line bundle]] over the space of morphisms $\mathbf{X}_1$, then there is the [[groupoid algebra|convolution algabra]] $\mathcal{A}$ of sections of this line bundle. Twisted unitary vector bundles are equivalently projective [[modules]] over this algebra. 

This means that under the identification 

$$
  \phi \colon Alg_k \stackrel{\simeq}{\to} 2 Vect_k
$$

of the [[2-category]] of [[2-vector spaces]] with that of [[algebras]], [[bimodules]] and intertwiners (see at _[[n-vector space]]_), the convolution algebra $\mathcal{A}$ _is_ the 2-vector space of sections

$$
  \phi\left(\mathcal{A}\right) 
   \simeq 
  \Gamma_{\mathbf{X}}\left(P \times_{\mathbf{B}U\left(1\right)} \coprod_n \mathbf{B}U\left(n\right) \right)
  \,.
$$



### Polarizations and branes

The full generalization of the notion of _[[polarization]]_ from traditional [[geometric quantization]] to [[higher geometric quantization]] may need more thinking, but in the case of 2d Chern-Simons theory we can apply the following plausible shortcut.

A [[Poisson Lie algebroid]] $(\mathfrak{P}, \mathbf{\omega})$ is a [[symplectic Lie n-algebroid]] for $n = 1$. This means that if we regard it as a [[dg-manifold]] (the dg-manifold whose [[dg-algebra]] of functions is the [[Chevalley-Eilenberg algebra]] $(CE(\mathfrak{P})$) then the [[invariant polynomial]] $\mathbf{\omega}$ constitutes a graded [[symplectic form]] on $\mathfrak{P}$. Since a [[real polarization]] of an ordinary [[symplectic manifold]] is equivalently a [[foliation]] by [[Lagrangian submanifolds]], it hence makes sense to take a [[real polarization]] of $(\mathfrak{P}, \mathbf{\omega})$ to consist of [[Lagrangian dg-submanifolds]]. As discussed there, for the [[Poisson Lie algebroid]] these corespond to the [[coisotropic submanifolds]] of the underlying [[Poisson manifold]] $(X, \pi)$. The same definition of polarization has been used/obtained in the study of [[geometric quantization of symplectic groupoids]] (see there).

The [[branes]] of the [[2d Chern-Simons theory]] should be those leaves of the foliation which satisfy an extra [[BS-leaf|intrability condition]].

Indeed, according to [[branes]] of the [[Poisson sigma-model]] are supposed to be coisotropic submanifolds, see at [Poisson sigma-model -- Properties -- Branes](Poisson+sigma-model#Branes).

### Quantum 2-states

Summing up, the convolution subalgebra $\mathcal{A}_q \hookrightarrow \mathcal{A}$ of polarized sections is under $\phi$ the actual 2-vector space of states.

In _[[geometric quantization of symplectic groupoids]]_ it is show that this is the algebra of observables of the [[quantum mechanical system]] of the underlying [[Poisson manifold]] (its [[strict deformation quantization]]).


In fact we have to quantize the whole [[atlas]] of the [[symplectic groupoid]]

$$
  X \to \tau_1 \exp(\mathfrak{P})
  \,.
$$

By the discussion at [[groupoid convolution algebra]] this yields a [[bimodule]]

#### Symplectic case

Consider the simple case where $(X,\omega)$ is a [[symplectic manifold]] and in fact a [[symplectic vector space]]. 

Here the [[symplectic groupoid]] is the [[pair groupoid]] $Pair(X)_\bullet$ carrying the trivial twist. The [[atlas]] is the object inclusion

$$
  X \to Pair(X)
  ,.
$$

Notice that this is equivalent ([[Morita equivalence|Morita equivalent]]) to just the terminal map

$$
  X \to *
  \,.
$$

Accordingly, the [[groupoid convolution algebra]] of $Pair(X)_\bullet$ is the [[C-star-algebra]] of [[compact operators]] $\mathcal{K}(X)$. A [[Morita equivalence]] [[bimodule]] from there to the ground field is (...)

The [[groupoid-principal bundle|groupoid-principal]]-[[bibundle]] corresponding to this atlas regarded as a [[Morita morphism]] is just the [[projection]] $X \times X \stackrel{p_1}{\to} X$. Hence the $C^\ast$-bimodule here is that generated from [[integral kernels]].

In conclusion, up to equivalence the bimodule is $L^2(X)$ regarded as a $C(X)-\mathbb{C}$-bimodule.

(...)



## References
 {#References}

The above discussion was inspired by

* {#Hawkins08} [[Eli Hawkins]], *A Groupoid Approach to Quantization*, J. Symplectic Geom. **6** 1  (2008) 61-125 &lbrack;[arXiv:math/0612363](https://arxiv.org/abs/math/0612363), [euclid](https://projecteuclid.org/journals/journal-of-symplectic-geometry/volume-6/issue-1/A-groupoid-approach-to-quantization/jsg/1215032733.full)&rbrack;

and details have been written out in these two theses:

* {#Bongers} Stefan Bongers, _[[schreiber:master thesis Bongers|Geometric quantization of symplectic and Poisson manifolds]]_, master thesis, Utrecht (2013)

* {#Nuiten13} [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis, Utrecht (2013)

Here section 4 of [Bongers (2013)](#Bongers) recalls and makes explicit relevant details in the construction of the [[symplectic groupoid]], and section 5.2.2 of [Nuiten (2013)](#Nuiten13) essentially provides a re-casting of the quantization construction in [Hawkins (2008)](#Hawkins08) which gives it an invariant home and brings out the above holographic picture more explicitly. 

This reveals a general abstract nature of the construction which was meant to be further brought out in:

* [[Urs Schreiber]], *[[schreiber:Quantization via Linear homotopy types]]* &lbrack;[arXiv:1402.7041](https://arxiv.org/abs/1402.7041)&rbrack;

where the above situation corresponds to "running example a)", Example 7.3 ([p. 70](https://arxiv.org/pdf/1402.7041.pdf#page=70)).


[[!redirects 2d Poisson-Chern-Simons theory]]
[[!redirects 2d Poisson-Chern-Simons theories]]
