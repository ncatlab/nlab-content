

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


## Definition

### On symplectic manifolds
 {#OnSymplecticManifolds}

+-- {: .num_defn}
###### Definition

For $(X,\omega)$ a [[symplectic manifold]], a [[vector field]] $v \in \Gamma(T X)$ is called a **Hamiltonian vector field** if is contraction with the 2-form $\omega$ is exact: there is $\alpha \in C^\infty(X)$ such that

$$
  \iota_v \omega = d \alpha
  \,.
$$

In this case $\alpha$ is called a [[Hamiltonian]] for $v$.

=--

### On $n$-plectic manifolds

+-- {: .num_defn}
###### Definition

For $(X,\omega)$ an [[n-plectic manifold]], a [[vector field]] $v \in \Gamma(T X)$ is called a **Hamiltonian vector field** if is contraction with the $(n+1)$-form $\omega$ is exact: there is $\alpha \in \Omega^{n-1}(X)$ such that

$$
  \iota_v \omega = d \alpha
  \,.
$$

In this case $\alpha$ is called a [[Hamiltonian form|Hamiltonian (n-1)-form]] for $v$.

=--

### On $n$-plectic smooth $\infty$-groupoids
 {#OnNPlecticInfinityGroupoids}

Let $X$ be a [[smooth ∞-groupoid]] and
$\omega : X \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}$
a closed differential $(n+1)$-form on $X$.

For instance $X$ might be a [[symplectic ∞-groupoid]].

Assume that this is _prequantizable_ in that there exists a [[prequantum line bundle|prequantum]] 
[[circle n-bundle with connection]] for $\omega$,

$$
  \nabla : X \to \mathbf{B}^n U(1)_{conn}
$$

(one whose [[curvature]] $n+1$-form is $\omega$).


+-- {: .num_defn #HamiltonianDiffeomorphismsOnInfinityGroupoid}
###### Definition

A **Hamiltonian diffeomorphism** $(\phi, \alpha)$ 
on $(X, \omega)$ is, for any choice of of 
prequantum circle $n$-bundle $\nabla$ for $\omega$, 
a diagram

$$
  \array{
    X &&\underoverset{\simeq}{\phi}{\to}&& X
    \\
    & {}_{\mathllap{\nabla}}\searrow 
    &
      \swArrow_{\alpha}
    & 
    \swarrow_{\mathrlap{\nabla}}
    \\
    && \mathbf{B}^n U(1)_{conn}
  }
$$

in [[Smooth∞Grpd]]. 

Hamiltonian diffeomorphisms naturally form a [[smooth ∞-group]]. We say that a **Hamiltonian vector field** on $(X, \omega)$ is an element in the [[∞-Lie algebra]] of this $\infty$-group.

=--

+-- {: .num_prop}
###### Proposition

For $n = 1$ and $(X, \omega)$ an ordinary
prequantizable [[symplectic manifold]] regarded as a smooth $\infty$-groupoid, 
this definition reproduces the ordinary definition 
of Hamiltonian vector fields [above](#OnSymplecticManifolds).

In particular it is independent of the choice of [[prequantum line bundle]].

=--

+-- {: .proof}
###### Proof

To compute the Lie algebra of this, 
we need to consider smooth 1-parameter families of 
Hamiltonian diffeomorphisms and differentiate them. 

Assume first that the [[prequantum line bundle]] is
trivial as a bundle, with the connection 1-form of $\nabla$ 
given by a globally defined 
$A \in \Omega^1(X)$ with $d A = \omega$. Then the 
existence of the diagram in def. \ref{HamiltonianDiffeomorphismsOnInfinityGroupoid}
is equivalent to the condition

$$
  (\phi(t)^* A - A) = d \alpha(t)
  \,,
$$

where $\alpha(t) \in C^\infty(X)$. Differentiating this at 0 yields the 
[[Lie derivative]]

$$
  \mathcal{L}_v A = d \alpha'
  \,,
$$

where $v$ is the [[vector field]] of which $t \mapsto \phi(t)$ is the 
[[flow]] and where $\alpha' := \frac{d}{dt} \alpha$.

By [[Cartan calculus]] this is equivalently

$$
  d_{\mathrm{dR}} \iota_v A + \iota_v d_{dR} A  = d \alpha'
$$

and using that $A$ is the connection on a prequantum circle bundle
for $\omega$

$$
  \iota_v \omega = d (\alpha' - \iota_v A)
  \,.
$$

This says that for $v$ to be Hamiltonian, 
its contraction with $\omega$ must be exact. This is precisely the definition of Hamiltonian vector fields. 
The corresponding Hamiltonian function here is 

$$
  h := \alpha'-\iota_v A
  \,.
$$

In the general case that the prequantum bundle is not trivial, we can present it by a [[Cech cohomology|Cech cocycle]] on the [[Cech nerve]] 
$C(P_* X \to X)$ of the based [[path space]] 
[[surjective submersion]] (regarding $P_* X$ as a 
[[diffeological space]] and choosing one base point per connected component, 
or else assuming without restriction that $X$ is connected).

Any [[diffeomorphism]] $\phi = \exp(v) : X \to X$ lifts to a 
diffeomorphism $ P_*\phi : P_* X \to P_* X$ by setting $P_* \phi(\gamma) : (t \in [0,1]) \mapsto \exp(t v)(\gamma(t))$. This way the Hamiltonian diffeomorphism
is presented in the [[model structure on simplicial presheaves]] by a diagram 

$$
  \array{
    C(P_*X \to X) &&\underoverset{\simeq}{\phi}{\to}&& C(P_*X \to X)
    \\
    & {}_{\mathllap{\nabla}}\searrow 
    &
      \swArrow_{\alpha}
    & 
    \swarrow_{\mathrlap{\nabla}}
    \\
    && \mathbf{B}^n U(1)_{conn}
  }
$$

of [[simplicial presheaves]]. 

Now the same argument as above applies for $P_* X$.

=--

## Properties

### Hamiltonian actions and moment maps

An [[action]] of a [[Lie algebra]] by (flows of) 
Hamiltonian vector fields that can be lifted to a [[Hamiltonian action]] is equivalently given by a _[[moment map]]_. See there for details.

### Relation to symplectic vector fields
 {#RelationToSymplectic}

Every Hamiltonian vector field is in particular a [[symplectic vector field]]. Where a symplectic vector field only preserves the [[symplectic form]], a Hamiltonian vector field also preserves the connection on its [[prequantum line bundle]].



+-- {: .num_prop}
###### Proposition

For $(X, \omega)$ a finite dimensional [[symplectic manifold]], 
there is an [[exact sequence]]


$$
  0 \to HamVect(X, \omega) \to SympVect(X, \omega) \to H^1(X, \mathbb{R}) 
  \to 0
  \,.
$$


=--

This appears as ([Brylinski, 2.3.3](#Brylinski)).


### Relation to functions and Poisson brackets
 {#RelationToFunctions}

+-- {: .num_prop}
###### Proposition

Let $(X, \omega)$ be a connected [[symplectic manifold]]. Then there is a [[central extension]] of [[Lie algebras]]

$$
  0 \to \mathbb{R} \to (C^\infty(X),\{-,-\}) \to HamVect(X,\omega) \to 0
  \,. 
$$

=--

This is a special case of what is called the **Kostant-Souriau central extension**. See around ([Brylinski, prop. 2.3.9](#Brylinski)).

[[!include geometric quantization extensions - table]]

### Group of Hamiltonian symplectomorphisms

The auto-[[symplectomorphisms]] on a [[symplectic manifold]] form a [[group]], of which the [[symplectic vector fields]] generate the connected component. The Hamiltonian vector fields among the symplectic ones generate the group of [[Hamiltonian symplectomorphisms]].

(...) 

## Related concepts

The Hamiltonian vector field of a given function may also be called its _[[symplectic gradient]]_.

* [[Hamiltonian action]]

## References

A textbook reference is section II.3 in 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_, Birkh&#228;user.
 {#Brylinski}

For more references on the ordinary notion of Hamiltonian vector fields see the references at _[[symplectic geometry]]_ and _[[geometric quantization]]_.

The notion of Hamiltonian vector field in [[n-plectic geometry]] is discussed in 

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))

The notion of Hamiltonian vector field for $n$-plectic cohesive $\infty$-groupoids is discussed in section 4.8.1 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

See also at _[[higher geometric quantization]]_.

[[!redirects Hamiltonian vector fields]]

[[!redirects hamiltonian vector field]]
[[!redirects hamiltonian vector fields]]