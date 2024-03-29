
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Symplectomorphisms are the [[homomorphisms]] of [[symplectic manifolds]].

In the context of [[mechanics]] where symplectic manifolds model [[phase spaces]], symplectomorphisms are essentially what are called _[[canonical transformations]]_.


## Definition

### Symplectomorphisms

A **symplectomorphism** or **symplectic diffeomorphism** from a [[symplectic manifold]] $(X_1,\omega_1)$ to a symplectic manifold $(X_2,\omega_2)$ is a [[diffeomorphism]] $\phi : X_1 \to X_2$ preserving the [[symplectic form]], i.e. such that 

$$
  \phi^* \omega_2 = \omega_1
  \,.
$$ 

### Auto-symplectomorphisms
 {#AutoSymplectomorphisms}

The symplectomorphisms from a [[symplectic manifold]] $(X, \omega)$ to itself form an infinite-dimensional [[Lie group]] that is a [[subgroup]] of the [[diffeomorphism group]] of $X$, the _[[symplectomorphism group]]_:

$$
  Sympl(X, \omega) 
  \hookrightarrow
  Diff(X)
  \,.
$$ 

Its [[Lie algebra]] 

$$
  \mathfrak{SymplVect}(X, \omega) \hookrightarrow \mathfrak{Vect}(X)
$$

is that of [[symplectic vector fields]]: those [[vector fields]] 
$v \in  \mathfrak{Vect}(X)$ such that their [[Lie derivative]] annihilates the [[symplectic form]]

$$
  \mathcal{L}_v \omega = 0
  \,.
$$

The further [[subgroup]] corresponding to those symplectic vector fields which are [[flows]] of [[Hamiltonian vector fields]] coming from a smooth family of [[Hamiltonians]]

$$
  \mathfrak{HamVect}(X, \omega) \hookrightarrow \mathfrak{SymplVect}(X, \omega) \hookrightarrow \mathfrak{Vect}(X)
$$

is the group of **Hamiltonian symplectomorphisms** or **Hamiltonian diffeomorphisms**.

$$
  HamSympl(X,\omega) \hookrightarrow Sympl(X, \omega) \hookrightarrow Diff(X)
  \,.
$$

### $n$-Plectomorphisms

In the generalization to [[n-plectic geometry]] there are accordingly _$n$-plectomorphisms_. See at _[[higher symplectic geometry]]_.

## Properties

### Preservation of volume

Inasmuch as a symplectic manifold $(M, \omega)$ carries a canonical [[volume form]] $\omega^{\wedge n}$, it is clear that a symplectomorphism is locally volume-preserving. 

### Relation to Poisson brackets

The [[Lie algebra]] given by the [[Poisson bracket]] of a [[symplectic manifold]] $(X, \omega)$ is that of a [[central extension]] of the group of Hamiltonian symplectomorphisms. (It [[Lie integration|integrates]] to the [[quantomorphism group]].)

The central extension results form the fact that the Hamiltonian associated with every [[Hamiltonian vector field]] is well defined only up to the addition of a constant function.

If $(X, \omega)$ is a [[symplectic vector space]] then there is corresponding to it a [[Heisenberg Lie algebra]]. This sits inside the Poisson bracket algebra, and accordingly the [[Heisenberg group]] is a subgroup of the group of (necessarily Hamiltonian) symplectomorphisms of the symplectic vector space, regarded as a symplectic manifold.

### Relation to Lagrangian correspondences

A symplectomorphisms $\phi \;\colon\; (X_1, \omega_1) \longrightarrow (X_2, \omega_2)$ canonically induces a [[Lagrangian correspondence]] between $(X_1, \omega_1)$ and $(X_2,\omega_2)$, given by its [[graph]]. 

### Extensions under geometric quantization

[[!include geometric quantization extensions - table]]


## Examples

### Linear symplectomorphisms

Given a [[symplectic vector space]] $(V,\omega)$ regarded as a [[symplectic manifold]], then those symplectomorphisms which are [[linear maps]] on $V$ form, under composition, the [[symplectic group]] $Sp(V,\omega)$.

The linear Hamiltonian symplectomorphisms are also known as the _[[Hamiltonian matrices]]_.

### A curious example: volumes of balls 

The following example, due to Andreas Blass and Stephen Schanuel, is a [[categorification|categorified]] way to calculate [[volumes]] of even-dimensional [[balls]]. 

In any dimension $n$, the volume of the unit ball in $\mathbb{R}^n$ (with respect to the [[Lebesgue measure]]) is 

$$
  vol(B_n) = \frac{\pi^{n/2}}{\Gamma(\frac{n}{2} + 1)}
$$ 

where $\Gamma$ is the Euler [[Gamma function]]. In dimension $2 n$, this gives 

$$
  vol(B_{2 n}) = \frac{\pi^n}{n!}
$$ 

Meanwhile, we may regard $\pi^n$ as the volume of the $n$-dimensional complex [[polydisc]], viz. the $n^{th}$ cartesian power of the complex 1-disc $B_{2} = \{z: {|z|} \leq 1\}$, on which the [[symmetric group]] $S_n$ acts by [[permutation|permuting]] [[coordinates]]. The volume of the orbit space $B_2^n/S_n$ is clearly $\pi^n/n!$. 

+-- {: .un_thm}
###### Theorem (Blass-Schanuel)
Given $(z_1, \ldots, z_n) \in \mathbb{C}^n$, write coordinates $z_j$ in polar coordinate form $z_j = r_j e^{i \theta_j}$, and define an $S_n$-invariant map $\phi \colon B_2^n \to B_{2 n}$ by first permuting the $z_j$ so that $r_1 \geq r_2 \geq \ldots \geq r_n$ and then mapping $(z_1, \ldots, z_n)$ to 
$$(\sqrt{r_1^2 - r_2^2}e^{i\theta_1}, \sqrt{r_2^2 - r_3^2}e^{i(\theta_1 + \theta_2)}, \ldots, \sqrt{r_{n-1}^2-r_n^2}e^{i(\theta_1 + \theta_2 + \ldots + \theta_{n-1})}, r_n e^{i(\theta_1 + \theta_2 + \ldots + \theta_n)})$$ 
Then $\phi$ induces a continuous well-defined map $B_2^n/S_n \to B_{2 n}$. Furthermore, when restricted to the set $P_n$ of $(z_1, \ldots, z_n)$ for which the $r_j$ are all distinct, $\phi$ induces a smooth symplectic isomorphism mapping $P_n/S_n$ onto the set $Q_n$ of $(w_1, \ldots, w_n) \in B_{2 n}$ for which $w_j \neq 0$ for $1 \leq j \leq n-1$. 
=--  

In other words, writing $z_j = x_j + i y_j$ the symplectic 2-form 

$$\sum_{j=1}^n d x_j \wedge d y_j = \sum_{j=1}^n r_j d r_j \wedge d\theta_j$$ 

is preserved by pulling back along $\phi \colon P_n/S_n \to Q_n$. Since symplectic maps are locally volume-preserving, and since $P_n$ and $Q_n$ are almost all of $B_2^n$ and $B_{2 n}$ respectively, this gives a proof that the volume of $B_{2 n}$ is $\pi^n/n!$ (alternate to standard purely computational proofs). 

## Related concepts

* [[canonical transformation]]

* [[Hamilton's equations]]

* [[symplectic integrator]]

## References 

Lecture notes include

* Augustin Banyaga, _Introduction to the geometry of hamiltonian diffeomorphisms_ ([pdf](https://www.personal.psu.edu/auw4/dakar.pdf))

The example of volumes of balls is discussed in 

* Andreas Blass, Stephen Schanuel, On the volumes of balls ([ps](http://www.math.lsa.umich.edu/~ablass/vol.ps)).  

[[!redirects symplectomorphisms]]

[[!redirects Hamiltonian symplectomorphism]]
[[!redirects Hamiltonian symplectomorphisms]]
[[!redirects hamiltonian symplectomorphism]]
[[!redirects hamiltonian symplectomorphisms]]

[[!redirects n-plectomorphism]]
[[!redirects n-plectomorphisms]]
[[!redirects Hamiltonian n-plectomorphism]]
[[!redirects Hamiltonian n-plectomorphisms]]

[[!redirects symplectic diffeomorphism]]
[[!redirects symplectic diffeomorphisms]]
[[!redirects Hamiltonian diffeomorphism]]
[[!redirects Hamiltonian diffeomorphisms]]


