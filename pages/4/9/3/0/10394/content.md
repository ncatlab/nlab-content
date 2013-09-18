
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

## Interpretation in higher geometry
 {#InterpretationInHigherGeometry}

+-- {: .num_remark #nExtendedHamiltonEquationAsLInfinityRelation}
###### Remark

By the discussion at [[n-plectic geometry]], a (pre-)[[n-plectic manifold]] $(X,\omega)$ induces a [[Poisson bracket Lie n-algebra]] $\mathfrak{pois}(X,\omega)$, given as follows:

* in possitive degree $k$ it has the degree $(n-k)$-[[differential forms]] on $X$

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

* and whose unary Lie bracket is given by the [[de Rham differential]].

This means that the $n$-extended Hamilton equation of def. \ref{ExtendedHamiltonEquations} reads in terms of the [[Poisson bracket Lie n-algebra]] equivalently thus ([hgp 13, remark 2.5.10](#hgp13)):

$$
  [v_1, \cdots, v_n] = [H]
  \,.
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

More in detai: the [[Lie integration]] of $\mathfrak{pois}(X,\omgea)$ is a [[simplicial object]] which in simplicial degree $n$ has as elements the [[Maurer-Cartan elements]] of $\Omega^\bullet(\Sigma_n)\otimes \mathfrak{pois}(X,\omgea)$, where $\Sigma_n = \Delta^n$ is the $n$-dimensional [[simplex]], regarded as a [[smooth manifold]] (with boundaries and corners).

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


## Related concepts

* [[de Donder-Weyl formalism]]


## References

The specific condition of def. \ref{ExtendedHamiltonEquations} appears as equation (4) in 

* [[Frédéric Hélein]], _Hamiltonian formalisms for multidimensional calculus of variations and perturbation theory_ ([arXiv:math-ph/0212036](http://arxiv.org/abs/math-ph/0212036))
  {#Helein02}

Remark \ref{nExtendedHamiltonEquationAsLInfinityRelation} appears in remark 2.5.10 of 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
  {#hgp13}


[[!redirects Hamiltonian n-vector fields]]

[[!redirects Hamiltonian multivector field]]
[[!redirects Hamiltonian multivector fields]]

[[!redirects Hamiltonian multi-vector field]]
[[!redirects Hamiltonian multi-vector fields]]
