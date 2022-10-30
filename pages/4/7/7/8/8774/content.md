
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
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

A variant of [[Yang-Mills theory]] in which the [[field strength]]/[[curvature]] 2-form of the [[Yang-Mills field]] is constrained to be self-dual.

## Definition

### Via an action functional
 {#ViaActionFunctional}

Let $(X, g)$ be a ([[pseudo-Riemannian manifold|pseudo]]) [[Riemannian manifold]] of [[dimension]] 4. Write $\star \colon \Omega^2(X) \to \Omega^2(X)$ for the corresponding [[Hodge star operator]]. Its square is $\star^2 = -1$ for Euclidean [[signature of a quadratic form|signature]] and $\star^2 = +1$ for Lorentzian signature. Decompose (possibly after [[complexification]])

$$
  \Omega^2(X) \simeq \Omega^2(X)_+ \oplus \Omega^2(X)_-
$$

into the [[direct sum]] of [[eigenspaces]] of $\star$, the _self-dual_ and the _anti-self-dual forms_. 

Let $G$ be a [[Lie group]]. Write $\mathfrak{g}$ for the corresponding [[Lie algebra]]. Let $\langle -,-\rangle$ be a binary [[invariant polynomial]] on the Lie algebra.

Accordingly we have

$$
  \Omega^2(X, \mathfrak{g}) \simeq \Omega^2(X, \mathfrak{g})_+ \oplus \Omega^2(X, \mathfrak{g})_-
  \,.
$$

The configuration space of self-dual Yang-Mills theory on $(X,g)$ is that of pairs $(\nabla, \mathcal{G})$ with 

* $\nabla \in \mathbf{H}^1_{conn}(X,G)$ is a $G$-[[principal connection]] over $X$;

* $\mathcal{G} \in \Omega^2(X, \mathfrak{g})_-$ is an anti-self-dual 2-form. 

The [[action functional]] of the theory is

$$
  (\nabla, \mathcal{G})
  \mapsto
  \int_X
  \langle 
    (F_\nabla)_- \wedge \mathcal{G}
  \rangle
  dvol_g
  \,.
$$

### Via BV-complexes
 {#ViaBVComplexes}
 
Let $X$ be an oriented [[smooth manifold]] of [[dimension]] 4 equipped with a [[conformal structure]] with [[Hodge star]] operator $\star_g$. Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$. 

Let $P \to X$ be a $G$-[[principal bundle]] and write $\mathfrak{g}_P \coloneqq P \times_G \mathfrak{g}$ for the [[associated bundle]] via the [[adjoint action]] of the group on its Lie algebra. Fix a $G$-[[principal connection]] $\nabla_0$ on $P$ with self dual curvature $F_{\nabla_0} = 0 \in \Omega_-^2(X, \mathfrak{g}_P)$.

Consider then the [[chain complex]]

$$
  \array{
    &
    \Omega^0(X, \mathfrak{g}_P)
    &\stackrel{d_{\nabla_0}}{\to}&
    \Omega^1(X, \mathfrak{g}_P)        
    &\stackrel{P_- \circ d_{\nabla_0}}{\to}&
    \Omega^2_-(X, \mathfrak{g}_P)    
    \\
    \\
    deg =  & 1 & & 0 && -1
  }
  \,,
$$

where 

* $d_\nabla$ is the [[de Rham differential]] coupled to the connection, hence the [[covariant derivative]] of $\nabla$;

* $P_-$ is the [[projection]] onto anti-self dual 2-forms.

This is a [[derived L-infinity algebroid]]  model for perturbations of self-dual connections about $\nabla_0$: 

a [[field (physics)|field configuration]] is an element in degree 0, hence a differential 1-form $A \in \Omega^1(X, \mathfrak{g}_P)$, which is in the kernel of the differential, hence of self-dual curvature. A [[gauge transformation]] of this is an element $\lambda \Omega^1(X, \mathfrak{g}_P)$ transforming 

$$
  A \mapsto A + d_{\nabla_0} \lambda 
  \,.
$$

Consider then the [[action functional]] on this complex of fields which is simply zero. Then the corresponding local [[BV-complex]] (with local [[antibracket]] taking values in the [[densities]] on $X$) is

$$
  \array{
    &
    \Omega^0(X, \mathfrak{g}_P)
      &\stackrel{d_{\nabla_0}}{\to}&
    \Omega^1(X, \mathfrak{g}_P)        
      &\stackrel{P_- \circ d_{\nabla_0}}{\to}&
    \Omega^2_-(X, \mathfrak{g}_P)    
    \\
    & && \oplus && \oplus
    \\
    & && \Omega^2_-(X, \mathfrak{g}_P)
     &\to&
     \Omega^3(X, \mathfrak{g}_P)
    &\to&
      \Omega^4(X, \mathfrak{g}_P)
    \\
    \\
    deg =  & 1 & & 0 && -1 && -2
  }
  \,,
$$

This formulaton of self-dual Yang-Mills theory is considered in 
([Costello-Gwilliam, section 4.12.3](#CostelloGwilliam)). There the grading is such that the Lie algebra of gauge transformations $\Omega^1(X,\mathfrak{g}_P)$ is in degree 0, whereas what is displayed above is the "delooped deived $L_\infty$-algebra". 

## Properties

### Of the action functional

If one changes the action functional of self-dual Yang-Mills theory by adding a term

$$
 \cdots +  \epsilon \int_X \langle \mathcal{G} \wedge \mathcal{G}\rangle
$$


for some non-vanishing $\epsilon \in \mathbb{R}$, then it becomes equivalent to that of ordinary [[Yang-Mills theory]] in the form

$$
  \nabla \mapsto \frac{1}{\epsilon}
  \int_X
  \left(
    \langle F_\nabla \wedge \star F_\nabla \rangle
    -
    \langle F_\nabla \wedge F_\nabla \rangle
  \right)
  dvol_g
  \,.
$$


### Via the Penrose-Ward twistor transform

Solutions to the [[equations of motion]] of self-dual Yang-Mills theory are naturally produced by seding cohomology classes on [[twistor space]] through the [[Penrose-Ward twistor transform]]. See there for more details.

## Related concepts

* [[self-dual higher gauge theory]]

## References

### Via action functional

The action functional [above](#ViaActionFunctional) is due to 

* Gordon Chalmers, Warren Siegel, _T-Dual Formulation of Yang-Mills Theory_, (1997) ([arXiv:hep-th/9712191](http://arxiv.org/abs/hep-th/9712191))

briefly reviewed at the beginning of

* M.V. Movshev, _A note on self-dual Yang-Mills theory_, [arXiv:0812.0224](http://arxiv.org/abs/0812.0224)

* [[Nigel Hitchin|N.J. Hitchin]], _The self-duality equations on a Riemann surface_, Proc. London Math. Soc. (3) 55 (1987), no. 1, 59&#8211;126, [MR887284](http://www.ams.org/mathscinet-getitem?mr=887284) [doi](http://dx.doi.org/10.1112/plms/s3-55.1.59)

For self-dual [[super Yang-Mills theory]] a discusion is in 

* E. Sokatchev, _An action for $N=4$ supersymmetric self-dual Yang-Mills theory_ ([arXiv:hep-th/9509099](http://arxiv.org/abs/hep-th/9509099))

See also

* H. J. de Vega, _Nonlinear multiplane wave solutions of self-dual Yang-Mills theory_ ([EUCLID](http://projecteuclid.org/euclid.cmp/1104161520))

### Via BV complex

The description via [[BV-complexes]] is amplified in the context of [[factorization algebras of observables]] in section 4.12.3 of

* [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html), early/partial draft [pdf](http://math.northwestern.edu/~gwilliam/factorization.pdf))
 {#CostelloGwilliam}


[[!redirects self-dual Yang-Mills equation]]