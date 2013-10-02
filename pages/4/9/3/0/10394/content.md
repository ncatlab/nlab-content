
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Symplectic geometry
+-- {: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _Hamiltonian $n$-vector field_ is the $n$-dimensional analog of a [[Hamiltonian vector field]] as one passes from [[symplectic geometry]] to [[multisymplectic geometry]]/[[n-plectic geometry]]. Roughly, the [[transgression]] of a Hamiltonian $n$-vector field to [[mapping spaces]] out of an $(n-1)$-manifold yields an ordinary [[Hamiltonian vector field]].

## Definition

+-- {: .num_defn #ExtendedHamiltonEquations}
###### Definition

Let $X$ be a [[smooth manifold]] equipped with a degree $(n+1)$ [[differential form]] $\omega \in \Omega^{n+1}(X)$ for $n \in \mathbb{N}$, with the pair $(X,\omega)$ regarded as a [[multisymplectic manifold]]/[[n-plectic manifold]].


Let moreover $H \;\colon\; X \longrightarrow \mathbb{R}$ be a [[smooth function]], to be regarded as an extended [[Hamiltonian function]], hence a [[de Donder-Weyl Hamiltonian]].

Then a _Hamiltonian $n$-vector field_ on $X$ is an $n$-[[multivector field]] $\mathbf{v} \in \Gamma(\wedge^{n} T X)$ satisfying the analog of [[Hamilton's equations]], namely the [[differential equation]] of [[differential 1-forms]] on $X$

$$
  \iota_{\mathbf{v}} \omega = \mathbf{d} H 
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $\Sigma$ be a [[manifold]] to be regarded as a [[spacetime]]/[[worldvolume]] and let $E \to \Sigma$ be a [[vector bundle]], to be regarded as a [[field bundle]]. Assume for simplicity of notation that both $\Sigma$ and $E$ are in fact [[Cartesian spaces]] (which is always true locally). Write $j^1 E$ for the corresponding jet bundle]], equipped with the canonical "kinetic" [[n-plectic form]] which in local coordinates reads

$$
  \omega 
    \coloneqq 
  \mathbf{d}_v\phi^a_{,i} \wedge \mathbf{d}_v q^a \wedge (\iota_{\partial_i} vol_\Sigma) 
$$

as discussed at [[multisymplectic geometry]]. 

Then for $\phi^a$ and $\phi^a_{,i}$ smooth functions on $\Sigma$ and for vector fields

$$
  v_i 
  \coloneqq 
  \frac{\partial}{\partial \sigma^i}
  + 
  \frac{\partial \phi^a}{\partial \sigma^i}
  +
  \frac{\partial \phi^a_{,j}}{\partial \sigma^j}
  \frac{\partial}{\partial \phi^a_{,i}}
$$

the equation 

$$
  \iota_{v_1 \cdots v_n} \omega = \pm \mathbf{d}H
$$

is equivalent to the [[de Donder-Weyl equations]]

$$
  \frac{\partial \phi^a}{\partial \sigma^i}
  =
  \frac{\partial H}{\partial p^i_a}
  \;\;\;\;
  \frac{\partial p^i_a}{\partial \sigma^i}
  = 
  \frac{\partial H}{\partial \phi^a}
  \,.
$$

=--

+-- {: .proof}
###### Proof

We have

$$
  \mathbf{d}_v \phi^a = \mathbf{d}\phi^a - \phi^a_{,i}\mathbf{d}\sigma^i
$$

and

$$
  \mathbf{d}_v \phi^a_{,i} 
    =
  \mathbf{d}\phi^a_{,i}
  - 
  \phi^a_{,i j} \mathbf{d}\sigma^j
  \,.
$$

The claimed equation comes from contracting in $\mathbf{d}\phi^a_{,i} \wedge \mathbf{d}\phi^a \wedge (\iota_{\partial_i}vol_\Sigma)$ all but the $i$th vector with the contracted volume form. The remaining contractions are then

$$
  \frac{\partial \phi^a}{\partial \sigma^i \partial \sigma^{[j}}
  \frac{\partial \phi_a}{\partial \sigma^{i]}}
  \mathbf{d}\sigma^j
$$

and these cancel against the horizontal derivative contributions form above.

=--

## Interpretation in higher geometry
 {#InterpretationInHigherGeometry}

We discuss here how Hamiltonian $n$-vector fields are equivalently homorphisms from an $n$-dimensional surface into the [[Poisson bracket Lie n-algebra]] associated with the given [[n-plectic geometry]].


+-- {: .num_remark #nExtendedHamiltonEquationAsLInfinityRelation}
###### Remark

By the discussion at [[n-plectic geometry]], a (pre-)[[n-plectic manifold]] $(X,\omega)$ induces a [[Poisson bracket Lie n-algebra]] $\mathfrak{pois}(X,\omega)$, given as follows:

* in positive degree $k$ it has the degree $(n-k)$-[[differential forms]] on $X$

* in degree 0 it has pairs $(v,A)$ of [[Hamiltonian n-forms]] $A$ with their [[Hamiltonian vector fields]] $v$ (such that $\mathbf{d}A = \iota_v \omega$)

and

* whose [[L-infinity algebra|n-ary Lie bracket]] for $n \geq 2$ is non-trivial only on $n$-tuples of degree-0 elements, where it is given by

  $$
    [(v_1, A_1), \cdots, (v_n,A_n)]
    =
    \pm
    \iota_{v_n}\cdots \iota_{v_1} \omega
    \;\;\;
    \in
    \Omega^1(X)    
    \,,
  $$

* and whose unary Lie bracket is given by the [[de Rham differential]], $\{-\} = \mathbf{d}$.

This means that the $n$-extended Hamilton equation of def. \ref{ExtendedHamiltonEquations} reads in terms of the [[Poisson bracket Lie n-algebra]] equivalently thus ([hgp 13, remark 2.5.10](#hgp13)):

$$
  \{v_1, \cdots, v_n\} = \pm\{H\}
  \,.
$$

=--

Let now $\Sigma$ be a [[manifold]] to be regarded as a [[spacetime]]/[[worldvolume]] and let $E \to \Sigma$ be a [[vector bundle]], to be regarded as a [[field bundle]]. Assume for simplicity of notation that both $\Sigma$ and $E$ are in fact [[Cartesian spaces]] (which is always true locally). Write $(j^1 E)^\ast$ for the coreresponding dual [[jet bundle]], equipped with the canonical "kinetic" [[n-plectic form]] which in local coordinates reads

$$
  \omega 
    \coloneqq 
  \mathbf{d}p^i_a \wedge \mathbf{d}q^a \wedge (\iota_{\partial_i} vol_\Sigma) 
$$

as discussed at [[multisymplectic geometry]]. 
Write $\mathfrak{pois}(X,\omega)$ for the corresponding [[Poisson bracket Lie n-algebra]].


+-- {: .num_prop }
###### Proposition

The [[L-∞ algebra]] [[homomorphisms]]

$$
  \mathbb{R}^n \longrightarrow \mathfrak{pois}((j^1 E)^\ast, \omega)
$$

which induce the canonical map under the projection to vector fields on $\Sigma$ are [[equivalence|equivalently]] [[tuples]] consisting of 

* a [[smooth function]] $H$;

* $n$ [[vector fields]] $v_i$

on $(j^1 E)^\ast$, such that the $(v_i)$ satisfy the [[de Donder-Weyl equation]] for [[Hamiltonian]] $H$

$$
  \iota_{v_1 \cdots v_n} \omega = \pm \mathbf{d}H
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion at _[[Maurer-Cartan element]]_, a homomorphism as indicated is equivalently an element

$$
  \mathcal{J}
  \in
  \wedge^\bullet(\mathbb{R}^n) \otimes \mathfrak{pois}(X,\omega)
$$

of total degree 1, which satifies the [[Maurer-Cartan equation]]

$$
  \sum_k \frac{1}{k!}\{\underbrace{\mathcal{J}\wedge \cdots \wedge \mathcal{J}}_{k\; factors}\}
  = 0
  \,.
$$

If we suggestively write $\mathbf{d}\sigma^i$ for the generators of the [[Grassmann algebra]] $\wedge^\bullet(\mathbb{R}^n)$, then, by remark \ref{nExtendedHamiltonEquationAsLInfinityRelation}, $\mathcal{J}$ is of the form

$$
  \mathcal{J}
  =
  \mathbf{d}\sigma^i \otimes (v_i, J_i)
  +
  \mathbf{d}\sigma^{i_1} \wedge \mathbf{d}\sigma^{i_2}
  \otimes J_{i_1 i_2}
  + 
  \cdots
  + 
  \mathbf{d}\sigma^1 \wedge \cdots \wedge \mathbf{d}\sigma^n
  \otimes
  H
  \,,
$$

where the $v_i$ are vector fields on the extended phase space,

$$
  J_{i_1 \cdots i_k} \in \Omega^{n-k}((j^1 E)^\ast)
$$

and $H$ is a smooth function. Again by remark \ref{nExtendedHamiltonEquationAsLInfinityRelation}, the [[Maurer-Cartan equation]] on this element is equivalent to

$$
  \iota_{v_{i_1}} \cdots \iota_{v_{i_k}} \omega
  = 
  \pm
  \mathbf{d} J_{i_1 \cdots i_k}
$$

for all $1 \leq k \leq n-1$ and all $\{i_j\}_{j = 1}^k$, and

$$
  \iota_{v_{1}} \cdots \iota_{v_{n}} \omega
  = 
  \pm
  \mathbf{d} H
  \,.
$$

The condition on the projection means that 

$$
  v_i = \frac{\partial}{\partial\sigma^i}
  +
  \frac{\partial \phi^a}{\partial \sigma^i}
  \frac{\partial }{\partial \phi^a}
  + 
  \frac{\partial \phi^a_{,j}}{\partial \sigma^i}
  \frac{\partial }{\partial \phi^a_{,j}}
  \,.
$$

This way the last equation is the [[de Donder-Weyl equation]]. But then

$$
  J_{i_1 \cdots i_k}
  \coloneqq
  \pm H \iota_{\partial_{i_1} \cdots \partial_{i_k}} vol_\Sigma  
$$

=--

We can further interpret this in [[local prequantum field theory]] as follows:

+-- {: .num_remark }
###### Remark

By ([hgp 13](#hgp13)) the [[Poisson bracket Lie n-algebra]] is the [[Lie differentiation]] of the smooth [[automorphism n-group]]
of any [[prequantization]] of $(X,\omega)$ by a  [[prequantum n-bundle]] $\nabla$:

$$
  \array{
    X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}^n U(1)_{conn}
    \\
    & {}_{\mathllap{\omega}}\searrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    && \mathbf{\Omega}^n_{cl}
  }
$$

regarded as an object in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}$ of that [[cohesive (∞,1)-topos]] $\mathbf{H}$ of [[smooth ∞-groupoids]], hence of the [[quantomorphism n-group]])

$$
  QuantMorph(X,\nabla) = \mathbf{Aut}_{\mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}}(\nabla)
  \,.
$$


In terms of this [[Lie integration|Lie integrated]] perspective, remark \ref{nExtendedHamiltonEquationAsLInfinityRelation} says that $H$-Hamitlonian $n$-vector fields are the infinitesimal [[n-morphisms]] in $\left(\mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}\right)^{\Box_n}$ whose faces carry trivial labels.

Here for instance for $n = 2$ a [[2-morphism]] in $\left(\mathbf{H}_{/\mathbf{B}^2 U(1)_{conn}}\right)^{\Box_2}$ looks, "viewed from the top", like a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    X && \stackrel{}{\longrightarrow} && X
    \\
    & {}_{\mathllap{\nabla}}\searrow && \swarrow_{\mathrlap{\nabla}}
    \\
    \downarrow && \mathbf{B}^2 U(1)_{conn} && \downarrow
    \\
    &  {}^{\mathllap{\nabla}}\nearrow && \nwarrow^{\mathrlap{\nabla}}
    \\
    X && \underset{}{\longrightarrow} && X
  }
$$

with a big 3-[[homotopy]] filling this pyramid.

The equation of remark \ref{nExtendedHamiltonEquationAsLInfinityRelation} is the [[Maurer-Cartan equation]] exhibiting an infinitesimal such situation.

More in detai: the [[Lie integration]] of $\mathfrak{pois}(X,\omega)$ is a [[simplicial object]] which in simplicial degree $n$ has as elements the [[Maurer-Cartan elements]] of $\Omega^\bullet(\Sigma_n)\otimes \mathfrak{pois}(X,\omgea)$, where $\Sigma_n = \Delta^n$ is the $n$-dimensional [[simplex]], regarded as a [[smooth manifold]] (with boundaries and corners).

Write then $\mathbf{d}\sigma^i$ for the canonical [[basis]] of 1-forms on $\Sigma_n$, then consider an element in there is of the form

$$
  A 
  = 
  \mathbf{d}\sigma^i \otimes v_i
  + 
  vol \otimes H
 \,.
$$

This satisfying the [[Maurer-Cartan equation]]

$$
  \mathbf{d}A + [A] +  [A \wedge A] + [A\wedge A \wedge A] + \cdots = 0
$$

then is equivalent to

$$
  [\mathbf{d}\sigma^1 \otimes v_1 \wedge \cdots \wedge \mathbf{d}\sigma^1 \otimes v_1]
  + 
  \underbrace{
    \mathbf{d}\sigma^1 \wedge \cdots \wedge \mathbf{d}\sigma^n
  }_{= vol}
  \otimes [H]
  = 0
$$

which is again the de Donder-Weyl-Hamilton equation of motion.

=--


+-- {: .num_prop #HDWAsMaurerCartan}
###### Proposition

For $(X,\omega)$ a pre-[[n-plectic manifold]] and $\mathfrak{poiss}(X,\omega)$ the corresponding [[Poisson bracket Lie n-algebra]] then 
[[L-∞ algebra]] [[homomorphisms]] of the form

$$
  \mathbb{R}^k \longrightarrow \mathfrak{pois}(X,\omega)
$$

are in bijection to tuples consisting of $k$ [[vector fields]] $(v_1, \cdots, v_k)$ on $X$ and differential forms $\{J_{i_1 \cdots i_l}\}$ and a smooth function $H$ on $X$ such that

$$
  \iota_{v_{1_1} \cdots v_{i_l}} \omega = \pm \mathbf{d} J_{i_1 \cdots i_l}
$$

$$
  \iota_{v_{1_1} \cdots v_{i_n}} \omega = \pm \mathbf{d} H
$$

holds. 

=--

The following is the higher/local analog of the [[symplectic Noether theorem]].

For $(X,\omega)$ a pre-[[n-plectic manifold]], (...)

let 
$H \in C^\infty(X)$ be a [[smooth function]] to be regarded
as a [[de Donder-Weyl Hamiltonian]] and let $(v_1, \cdots, v_n)$
be a Hamiltonian $n$-vector field, hence a solution to the 
Hamilton-de Donder-Weyl equation of motion. By 
prop. \ref{kTuplesOfCommutingDWFlows} this corresponds to an
[[L-∞ algebra]] map of the form

$$
  ((v_1, \cdots, v_n), H) 
     \;\colon\; 
  \mathbb{R}[n-1] \longrightarrow \mathfrak{pois}(X,\omega)
  \,.
$$


+-- {: .num_prop }
###### Proposition
**(higher symplectic Noether theorem)**

The extension of $((v_1, \cdots, v_n), H)$
to a homomorphism of the form

$$
  ((v_1, \cdots, v_n, v_0), H, J, \{K_i\}) 
    \;\colon\; 
  \mathbb{R}[n-1]\oplus \mathbb{R} 
    \longrightarrow 
  \mathfrak{pois}(X,\omega)
$$

is equivalently the choice of a vector field $v_0$ on $X$ such that

$$
  \iota_{v_0} \mathbf{d}H
  =
  
$$



$$
  \iota_{v_0} \omega = \pm \mathbf{d}J
$$

$$
  \iota_{v_1 \cdots v_n} \omega = \pm \mathbf{d}H
$$

$$
  \iota_{v_1 \cdots v_{i-1} v_{i+1} \cdots v_n v_0} \omega
  =
  \mathbf{d} K^i
$$

=--



## Related concepts


* [[de Donder-Weyl formalism]]



## References

The specific condition of def. \ref{ExtendedHamiltonEquations} appears as equation (4) in 

* [[Frédéric Hélein]], _Hamiltonian formalisms for multidimensional calculus of variations and perturbation theory_ ([arXiv:math-ph/0212036](http://arxiv.org/abs/math-ph/0212036))
  {#Helein02}

Remark \ref{nExtendedHamiltonEquationAsLInfinityRelation} appears in remark 2.5.10 of 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
  {#hgp13}



[[!redirects Hamiltonian n-vector field]]
[[!redirects Hamiltonian n-vector fields]]
[[!redirects Hamiltonian n-vecotr field]]

[[!redirects Hamiltonian multivector field]]
[[!redirects Hamiltonian multivector fields]]

[[!redirects Hamiltonian multi-vector field]]
[[!redirects Hamiltonian multi-vector fields]]