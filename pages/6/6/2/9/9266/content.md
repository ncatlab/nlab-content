
> under construction


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

## Idea

### General

We discuss aspects of the [[extended geometric quantization]] of one of the simplest and yet interesting examples of [[schreiber:∞-Chern-Simons theory]], namely [[2d Chern-Simons theory]] and here specifically the case induced by a binary and non-degenerate [[invariant polynomial]], namely the [[Lie integration|Lie integrated]] version of the [[Poisson sigma-model]].

It turns out that several aspects of the [[extended geometric quantization]] of this 2d [[theory (physics)|theory]] turn out to be known in the literature already, albeit in disguise: the [[2-plectic geometry|2-plectic]] [[moduli stack]] of [[field (physics)|fields]] is equivalently what in the literature is known as a _[[symplectic groupoid]]_ and its [[higher geometric quantization]] is essentially what is known as the _[[geometric quantization of symplectic groupoids]]_.

To some extent in the following we simply review the traditional [[geometric quantization of symplectic groupoids]] but we show at the same time how its ingredients are (more) naturally interpreted in [[higher symplectic geometry]]. This makes quantization of symplectic groupoids a good test case against which to check notions of [[higher geometric quantization]].

Specifically, we discuss what should be the first nontrivial case of the Chern-Simons-type _[[holographic principle]]_ realized in [[higher geometric quantization]]: The [[moduli stack]] of the [[2d Chern-Simons theory]] is the [[Lie integration]] of the [[Poisson Lie algebroid]] associated to a [[Poisson manifold]]. The latter we may think of as defining a [[quantum mechanical system]], hence a $(2-1) = 1$-dimensional [[quantum field theory]]. The higher geometric quantization of the 2-d theory yields a [[2-vector space]] [[space of states|of quantum 2-states]] (assigned to the point n codimension 2). Under the identification of [[2-vector spaces]] with [[categories of modules]] over an [[associative algebra]], this space of quantum 2-states identifies (the [[Morita equivalence]]-class of) an algebra. Suitably re-interpreting traditional results about the quantization of symplectic groupods shows that this algebra is the [[strict deformation quantization]] of that [[Poisson manifold]].

Notice that at the level of just infinitesimal ("formal") [[deformation quantization]] a similar [[holographic principle|holographic]] relation between quantization of a Poisson manifold and of its associated 2d [[sigma-model]] QFT has famously been shown by [[Cattaneo]] and [[Felder]] to underly [[Kontsevich]]'s construction of deformation quantization (see at _[[Poisson sigma-model]]_). We suggest that the discussion here provides the refinement of this relation to [[strict deformation quantization]].

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



## The setup

Let $(X, \pi)$ be a [[Poisson manifold]], which we tend to think of as defining a _[[quantum mechanical system]]_. This canonically induces the structure of [[Lie algebroid]] over $X$, the _[[Poisson Lie algebroid]]_ $(\mathfrak{P}, \mathbf{\omega})$ over $X$. This is a [[symplectic Lie n-algebroid|symplectic Lie algebroid]], with graded symplectic form (binary [[invariant polynomial]]) $\mathbf{\omega}$ which is in [[transgression]] with the Poisson tensor $\pi$, regarded as a [[Lie algebroid cohomology|Lie algebroid cocycle]]. The transgression is witnessed by a [[Chern-Simons element]] $cs_\pi$. By the general construction of [[schreiber:infinity-Chern-Simons theory]] this means that there is a universal differential characteristic map

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

This is the [[extended Lagrangian]] of a [[2d Chern-Simons theory]] ([[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models|FRS]]). Infinitesimally this yields the [[Poisson sigma-model]].

We discuss here the [[higher geometric quantization]] of this [[theory (physics)|theory]] defined by $\mathbf{L}$.


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

Generally, given a [[prequantum line 2-bundle]] the corresponding (local) [[prequantum n-states]] are the (local) [[sections]] of this [[line 2-bundle]], and these in turn are equivalently the [[twisted unitary bundles]] (maybe best known for the [[WZW model]] where these are the [[Chan-Paton gauge fields]]). These 2-sections/twisted bundles form a [[2-vector space]] of prequantum 2-states. This is equivalently a [[category of modules]] over some [[associative algebra]], well defined up to [[Morita equivalence]]. A canonical way of constructing this algebra is as follows: present the [[line 2-bundle]] as a [[bundle 2-gerbe]], hence as a multiplicative [[line bundle]] over the morphisms of a [[Lie groupoid]], then the algebra is the [[groupoid algebra]] of sections of this line bundle. A module over this is manifestly a [[bundle gerbe module]], which in turn is equivalently a unitary bundle twisted by the line 2-bundle.


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


