
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

Poisson manifolds are a mathematical setup for [[classical mechanics]] with finitely many degrees of freedom. 

## Definition

A __[[Poisson algebra]]__ is a commutative unital [[associative algebra]] $A$, in this case over the field of [[real number|real]] or [[complex numbers]], equipped with a Lie bracket $\{,\}:A\otimes A\to A$ such that, for any $f\in A$, $\{ f,-\}:A\to A$ is a [[derivation]] of $A$ as an associative algebra.

A __Poisson manifold__ is a real [[smooth manifold]] $M$ equipped with a __Poisson structure__. A Poisson structure is a Lie algebra bracket $\{,\}:C^\infty(M)\times C^\infty(M)\to C^\infty(M)$ on the vector space of smooth functions on $M$ which together with the pointwise multiplication of functions makes it a Poisson algebra. As derivations of $C^\infty(M)$ correspond to smooth [[tangent vector fields]], for each $f\in C^\infty(M)$ there is a vector $X_f$ given by $X_f(g)=\{f,g\}$ and called the __Hamiltonian vector field__ corresponding to the function $f$, which is viewed as a classical hamiltonian function.  

Alternatively a Poisson structure on a manifold is given by a choice of smooth antisymmetric bivector called a __Poisson bivector__ $P\in\Lambda^2 T M$; then $\{f,g\}:=\langle d f\otimes d g, P\rangle$. 

This induces and is equivalently encoded by the structure of a [[Poisson Lie algebroid]].


A morphism $h:M\to N$ of Poisson manifolds is a morphism of smooth manifolds such that, for all $f,g\in C^\infty(N)$, $\{f\circ h, g\circ h\}_M = \{f,g\}_N$. 


## Examples

### Various

+-- {: .num_example}
###### Example

Every manifold admits the _trivial Poisson structure_ for which the [[Poisson bracket]] simply vanishes on all elements.

=--


+-- {: .num_example}
###### Example

Every [[symplectic manifold]] carries a natural Poisson structure see [below](PresymplecticManifolds) for more; however, such Poisson manifolds are very special. It is a basic theorem that Poisson structures on a manifold are equivalent to the smooth [[foliations]] of the underlying manifold such that each leaf is a symplectic manifold.

=--

+-- {: .num_example}
###### Example


The dual to a finite-dimensional [[Lie algebra]] has a natural structure of a Poisson manifold, the _[[Lie-Poisson structure]]_. Its leaves are called [[coadjoint orbits]].

=--

+-- {: .num_example}
###### Example

Given a [[symplectic manifold]] $(X,\omega)$ and given a [[Hamiltonian]] [[function]] $H \colon X \longrightarrow \mathbb{R}$, there is a Poisson bracket on the functions on the [[smooth space|smooth]] [[path space]] $[I,X]$ (the "space of histories" or "space of [[trajectories]]"), for $I = [0,1]$ the closed [[interval]], which is such that its [[symplectic leaves]] are each a copy of $X$, but regarded as the space of initial conditions for evolution with respect to $H$ with a [[source]] term added. For more on this see at _[[off-shell Poisson bracket]]_.

=--

+-- {: .num_example}
###### Example

Every [[local action functional]] which admits a [[Green's function]] for its [[equations of motion]] defines the [[Peierls bracket]] on [[covariant phase space]] (where in fact it is symplectic) and also "[[off-shell Poisson bracket|off-shell]]" on all of configuration space, where it is a genuine Poisson bracket, the canonocal Poisson bracket of the corresponding [[prequantum field theory]].

=--

### Pre-symplectic manifolds and infinitesimal quantomorphisms
 {#PresymplecticManifolds}

We discuss the traditional definition of the [[Poisson bracket]] of a ([[presymplectic manifold|pre-]])[[symplectic manifold]] $(X,\omega)$, and then show how it may equivalently be understood as the algebra of infinitesimal symmetries of any of the [[prequantizations]] of $(X,\omega)$. For more on this see at _[[Poisson bracket Lie n-algebra]]_ and at _[[geometry of physics -- prequantum geometry]]_.

+-- {: .num_defn #PresymplecticManifold}
###### Definition

Let $X$ be a [[smooth manifold]]. A closed [[differential 2-form]] $\omega \in \Omega_{cl}^2(X)$ is a _[[symplectic form]]_ if it is non-degenerate in that the [[kernel]] of the operation of contracting with [[vector fields]]

$$
  \iota_{(-)}\omega \colon Vect(X) \longrightarrow \Omega^1(X)
$$

is trivial: $ker(\iota_{(-)}\omega) = 0$.

If $\omega$ is just closed with possibly non-trivial kernel, we call it a [[presymplectic form]]. (We do not require here the dimension of the kernel restricted to each tangent space to be constant.)

=--


+-- {: .num_defn #HamiltonianVectorField}
###### Definition

Given a [[presymplectic manifold]] $(X, \omega)$, then a _[[Hamiltonian]]_ for a [[vector field]] $v \in Vect(X)$ is a [[smooth function]] $H \in C^\infty(X)$ such that

$$
  \iota_{v} \omega + d H = 0
  \,.
$$

If $v \in Vect(X)$ is such that there _exists_ at least one Hamiltonian for it then it is called a _[[Hamiltonian vector field]]_. Write

$$
  HamVect(X,\omega) \hookrightarrow Vect(X)
$$

for the $\mathbb{R}$-[[linear subspace]] of Hamiltonian vector fields among all [[vector fields]]

=--

+-- {: .num_remark}
###### Remark

When $\omega$ is symplectic then, evidently, there is a unique Hamiltonian vector field, def. \ref{HamiltonianVectorField}, associated with every Hamiltonian, i.e. every smooth function is then the Hamiltonian of precisely one Hamiltonian vector field (but two different Hamiltonians may still have the same Hamiltonian vector field uniquely associated with them). As far as [[prequantum geometry]] is concerned, this is all that the non-degeneracy condition that makes a closed 2-form be symplectic is for. But we will see that the definitions of [[Poisson brackets]] and of [[quantomorphism groups]] directly generalize also to the presymplectic situation, simply by considering not just Hamiltonian fuctions but pairs of a Hamiltonian vector field and a compatible Hamiltonian.

=--


+-- {: .num_defn #PoissonBracket}
###### Definition

Let $(X,\omega)$ be a [[presymplectic manifold]]. Write 

$$
  Ham(X,\omega) \hookrightarrow HamVect(X,\omega) \oplus C^\infty(X)
$$

for the [[linear subspace]] of the [[direct sum]] of [[Hamiltonian vector fields]], def. \ref{HamiltonianVectorField}, and [[smooth functions]] on those pairs $(v,H)$ for which $H$ is a [[Hamiltonian]] for $v$ 

$$
  Ham(X,\omega)
  \coloneqq
  \left\{
    (v,H) | \iota_v \omega + d H  = 0
  \right\}
  \,.
$$


Define a [[bilinear map]] 

$$
  [-,-] \;\colon\;
  Ham(X,\omega) \otimes Ham(X,\omega)
  \longrightarrow
  Ham(X,\omega)
$$

by

$$
 [(v_1,H_1), (v_2,H_2)] \coloneqq ([v_1,v_2], \iota_{v_2}\iota_{v_1} \omega)
 \,,
$$

called the _[[Poisson bracket]]_, where $[v_1,v_2]$ is the standard Lie bracket on [[vector fields]]. Write

$$
  \mathfrak{Pois}(X,\omega)
  \coloneqq
  (Ham(X,\omega),[-,-])
$$

for the resulting [[Lie algebra]]. In the case that $\omega$ is symplectic, then $Ham(X,\omega) \simeq C^\infty(X)$ and hence in this case

$$
  \mathfrak{Pois}(X,\omega)
  \simeq
  (C^\infty(X),[-,-])
  \,.
$$

=--

+-- {: .num_example #HeisenbergAlgebraOfSymplecticVectorSpace}
###### Example

Let $X = \mathbb{R}^{2n}$ and let $\omega = \sum_{i = 1}^n d p_i \wedge d q^i$ for $\{q^i\}_{i = 1}^n$ the [[canonical coordinates]] on one copy of $\mathbb{R}^n$ and $\{p_i\}_{i = 1}^n$ that on the other ("[[canonical momenta]]"). Hence let $(X,\omega)$ be a [[symplectic vector space]] of dimension $2n$, regarded as a [[symplectic manifold]].

Then $Vect(X)$ is [[linear span|spanned]] over $C^\infty(X)$ by the canonical bases vector fields $\{\partial_{q^i}, \partial_{p^i}\}$. These basis vector fields are manifestly [[Hamiltonian vector fields]] via

$$
  \iota_{\partial_{q^i}} \omega = - d p_i
$$

$$
  \iota_{\partial_{p_i}} \omega = + d q^i
  \,.  
$$

Moreover, since $X$ is [[connected topological space|connected]], these Hamiltonians are unique up to a choice of constant function. Write $\mathbf{i} \in C^\infty(X)$ for the unit constant function, then the nontrivial Poisson brackets between the basis vector fields are 

$$
  [q^i, p_j]
  \coloneqq
  [(-\partial_{p_i}, q^i), (\partial_{q^j}, p_j)]
  =
  -
  \delta_j^i
  (0, \mathbf{i})
  =
  -
  \delta_j^i
  \mathbf{i}
  \,.
$$

This is called the [[Heisenberg algebra]].

More generally, the [[Hamiltonian vector fields]] corresponding to [[quadratic Hamiltonians]], i.e. degree-2 [[polynomials]] in the $\{q^i\}$ and $\{p_i\}$, generate the [[affine symplectic group]] of $(X,\omega)$. The freedom to add constant terms to Hamiltonians gives the [[extended affine symplectic group]].

=--

Example \ref{HeisenbergAlgebraOfSymplecticVectorSpace} serves to motivate a more conceptual origin of the definition of the Poisson bracket in def. \ref{PoissonBracket}.

+-- {: .num_example }
###### Example

Write

$$
  \theta \coloneqq \sum_{i = 1}^n p_i d q_i \in \Omega^1(\mathbb{R}^{2n})
$$

for the canonical choice of [[differential 1-form]] satisfying 

$$
  d \theta = \omega
  \,.
$$

If we regard $\mathbb{R}^{2n} \simeq T^\ast \mathbb{R}^n$ as the [[cotangent bundle]] of the [[Cartesian space]] $\mathbb{R}^n$, then this is what is known as the [[Liouville-Poincaré 1-form]].

Since $\mathbb{R}^{2n}$ is [[contractible topological space|contractible]] as a [[topological space]], every [[circle bundle]] over it is necessarily trivial, and hence any choice of 1-form such as $\theta$ may canonically be thought of as being a [[connection on a bundle|connection]] on the trivial $U(1)$-[[principal bundle]]. As such this $\theta$ is a [[prequantization]] of $(\mathbb{R}^{2n}, \sum_{i=1}^n d p_i \wedge d q^i)$.

Being thus a [[circle bundle with connection]], $\theta$ has more symmetry than its [[curvature]] $\omega$ has: for $\alpha \in C^\infty(\mathbb{R}^{2n}, U(1))$ any smooth function, then 

$$
  \theta \mapsto \theta + d\alpha
$$

is the [[gauge transformation]] of $\theta$, leading to a different but equivalent [[prequantization]] of $\omega$.

Hence while a [[vector field]] $v$ is said to preserve $\omega$ (is a [[symplectic vector field]]) if the [[Lie derivative]] of $\omega$ along $v$ vanishes

$$
  \mathcal{L}_v \omega = 0 
$$

in the presence of a choice for $\theta$ the right condition to ask for is that there is $\alpha$ such that

$$
  \mathcal{L}_v \theta = d \alpha
  \,.
$$

=--

For more on this see also at _[[prequantized Lagrangian correspondence]]_.

Notice then the following basic but important fact.

+-- {: .num_prop}
###### Proposition

For $(X,\omega)$ a [[presymplectic manifold]] and $\theta \in \Omega^1(X)$ a 1-form such that $d \theta = \omega$ then for $(v,\alpha) \in Vect(X)\oplus C^\infty(X)$ the condition

$$
  \mathcal{L}_v \theta = d \alpha
$$

is equivalent to the condition that makes $H \coloneqq \iota_v \theta - \alpha $ a [[Hamiltonian]] for $v$ according to def. \ref{HamiltonianVectorField}:

$$
  \iota_v \omega + d (\iota_v \theta - \alpha  ) = 0
  \,.
$$

Moreover, the [[Poisson bracket]], def. \ref{PoissonBracket}, between two such Hamiltonian pairs $(v_i, \alpha_i -\iota_v \theta)$ is equivalently given by the skew-symmetric [[Lie derivative]] of the corresponding vector fields on the $\alpha_i$:

\[
  \label{EquationForLieHomomorphism}
  \iota_{[v_1,v_2]} \theta
  -
  \iota_{v_2}\iota_{v_1}\omega 
  = 
  \mathcal{L}_{v_1} \alpha_2 - \mathcal{L}_{v_2} \alpha_1
\]

=--

+-- {: .proof}
###### Proof

Using [[Cartan's magic formula]] and by the prequantization condition $d \theta = \omega$ the we have

$$
  \begin{aligned}
    \mathcal{L}_v \theta &= \iota_v d\theta + d \iota_v \theta
    \\
    & =  \iota_v\omega + d \iota_v \theta
  \end{aligned}
  \,.
$$

This gives the first statement. For the second we first use the formula for the [[de Rham differential]] and then again the definition of the $\alpha_i$

$$
  \begin{aligned}
    \iota_{v_2}\iota_{v_1} \omega
    & =
    \iota_{v_2}\iota_{v_1} d\theta
    \\
    & =
    \iota_{v_1} d \iota_{v_2} \theta
    -
    \iota_{v_2} d \iota_{v_1} \theta
    -
    \iota_{[v_1,v_2]} \theta
    \\
     & = 
    \iota_{v_1} d \alpha_2 - \iota_{v_1} \iota_{v_2}\omega
    - \iota_{v_2} d \alpha_1 + \iota_{v_2} \iota_{v_1}\omega 
    -
    \iota_{[v_1,v_2]} \theta
    \\
     & = 
    2 \iota_{v_2} \iota_{v_1}\omega 
    + \mathcal{L}_{v_1} \alpha_2
     -\mathcal{L}_{v_2} \alpha_1
    -
    \iota_{[v_1,v_2]} \theta
 \end{aligned}
  \,.
$$

=--

+-- {: .num_cor #EquivalenceBetweenPoissonBracketAndInfinQuantomorphism}
###### Corollary

For $(X,\omega)$ a [[presymplectic manifold]] with $\theta \in \Omega^1(X)$ such that $d \theta = \omega$, consider the [[Lie algebra]]

$$
  \mathfrak{QuantMorph}(X,\theta)
  =
  \left\{
    (v,\alpha) | \mathcal{L}_v \theta = d \alpha
  \right\}
  \subset
  Vect(X) \oplus C^\infty(X)
$$

with Lie bracket

$$
  [(v_1,\alpha_1), (v_2,\alpha_2)] = ([v_1,v_2], \mathcal{L}_{v_1}\alpha_2 - \mathcal{L}_{v_2}\alpha_1)
  \,.
$$

Then by (eq:EquationForLieHomomorphism) the linear map

$$
  (v,H) \mapsto (v, \iota_v \theta - H)
$$

is an [[isomorphism]] of [[Lie algebras]]

$$
  \mathfrak{Pois}(X,\omega) 
    \stackrel{\simeq}{\longrightarrow}
  \mathfrak{QuantMorph}(X,\theta)
$$

from the [[Poisson bracket Lie algebra]], def. \ref{PoissonBracket}.

=--

This shows that for exact pre-symplectic forms the Poisson bracket Lie algebra is secretly the Lie algebra of infinitesimal symmetries of any of its [[prequantizations]]. In fact this holds true also when the pre-symplectic form is not exact:

+-- {: .num_defn #CechDelignePrequantizationAnditsInfinitesimalAutomorpisms}
###### Definition

For $(X,\omega)$ a [[presymplectic manifold]], a [[Cech cohomology|Cech]]-[[Deligne cohomology|Deligne]] [[cocycle]] $(X,\{U_i\},\{g_{i j}, \theta_i\})$ for a  _[[prequantization]]_ of $(X,\omega)$ is

1. an [[open cover]] $\{U_i \to X\}_i$;

1. 1-forms $\{\theta_i \in \Omega^1(U_i)\}$;

1. smooth function $\{g_{i j} \in C^\infty(U_{i j}, U(1))\}$

such that

1. $d \theta_i = \omega|_{U_i}$ on all $U_i$;

1. $\theta_j = \theta_i + d log g_{ij}$ on all $U_{i j}$;

1. $g_{i j} g_{j k} = g_{i k}$ on all $U_{i j k}$.

The _quantomorphism Lie algebra_ of this is 

$$
  \mathfrak{QuantMorph}(X,\{U_i\},\{g_{i j}, \theta_i\})
  =
  \left\{
    (v, \{\alpha_i\})
    |
    \mathcal{L}_v log g_{i j} = \alpha_j - \alpha_i
    \,,
    \mathcal{L}_v \theta_i = d \alpha_i
  \right\}
  \subset
  Vect(X) \oplus \left(\underset{i}{\bigoplus} C^\infty(U_i)\right)
$$

with bracket

$$
  [(v_1, \{(\alpha_1)_i\}), (v_2, \{(\alpha_2)_i\})]
  \coloneqq
  ([v_1,v_2], \{\mathcal{L}_{v_1}(\alpha_2)_i - \mathcal{L}_{v_2} (\alpha_1)_i\})
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $(X,\omega)$ a [[presymplectic manifold]] and 
$(X,\{U_i\},\{g_{i j}, \theta_i\})$ a [[prequantization]],
def. \ref{CechDelignePrequantizationAnditsInfinitesimalAutomorpisms}, the linear map

$$
  (v,H) \mapsto (v,  \{\iota_v \theta_i - H|_{U_i}\})
$$

constitutes an [[isomorphism]] of [[Lie algebras]]

$$
  \mathfrak{Pois}(X,\omega)
  \stackrel{\simeq}{\longrightarrow}
  \mathfrak{QuantMorph}(X,\{U_i\},\{g_{i j}, \theta_i\})
  \,.
$$

=--

+-- {: .proof}
###### Proof

The condition $\mathcal{L}_v log g_{i j} = \alpha_j - \alpha_i$
on the infinitesimal quantomorphisms, togther with the Cech-Deligne cocycle condition $d log g_{i j} = \theta_j - \theta_i$ says that on $U_{i j}$

$$
  \iota_v \theta_j - \alpha_j = \iota_v \theta_i - \alpha_i
$$

and hence that there is a globally defined function $H \in C^\infty(X)$ such that $\iota_v \theta_i - \alpha_i = H|_{U_i}$. This shows that the map is an isomrophism of vector spaces.

Now over each $U_i$ the the situation for the brackets is just that of corollary
\ref{EquivalenceBetweenPoissonBracketAndInfinQuantomorphism} implied by (eq:EquationForLieHomomorphism), hence the morphism is a Lie homomorphism.

=--


## Properties

### Deformation quantization

[[Kontsevich formality]] implies that every Poisson manifold has a family of [[deformation quantizations]], parameterized by the [[Grothendieck-Teichmüller group]].


## Related concepts

* [[Poisson tensor]]

* [[Poisson geometry]]

* [[Poisson cohomology]]

* [[Poisson reduction]]

* [[isotropic submanifold]], [[coisotropic submanifold]]

* [[symplectic leaf]]

* [[symplectic realization]]

* [[symplectic dual pair]]

* [[Poisson Lie algebroid]]


* [[deformation quantization]]

  * [[Moyal quantization]]

* [[higher Poisson structure]]

  * [[Nambu bracket]]

  * [[Poisson n-algebra]]

  * [[Poisson bracket Lie n-algebra]]


[[!include Isbell duality - table]]

[[!include infinitesimal and local - table]]


[[!redirects Poisson Lie algebra]]

[[!redirects Poisson manifolds]]

[[!redirects Poisson bracket]]
[[!redirects Poisson brackets]]


[[!redirects Poisson structure]]
[[!redirects Poisson structures]]

[[!redirects Poisson Lie algebra]]
[[!redirects Poisson Lie algebras]]

[[!redirects Poisson bracket Lie algebra]]
[[!redirects Poisson bracket Lie algebras]]

