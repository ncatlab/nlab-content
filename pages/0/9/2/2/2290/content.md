
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _elliptic cohomology theory_ is a type of _[[generalized (Eilenberg-Steenrod) cohomology]]_ theory associated with the datum of an [[elliptic curve]].

Even ([[weakly periodic cohomology theory|weakly]]) [[periodic cohomology theory|periodic]] [[multiplicative cohomology theory|multiplicative]] [[generalized (Eilenberg-Steenrod) cohomology]] theories $A$ are characterized by the [[formal group]] whose ring of functions $A(\mathbb{C}P^\infty)$ is the [[cohomology ring]] of $A$ evaluated on the [[complex projective space]] $\mathbb{C}P^\infty$ and whose group product is induced from the canonical morphism $\mathbb{C}P^\infty \times \mathbb{C}P^\infty \to \mathbb{C}P^\infty$ that describes the tensor product of complex [[line bundle]]s under the identification $\mathbb{C}P^\infty \simeq \mathcal{B} U(1)$.

There are precisely three types of 1-dimensional such [[formal group laws]]:

* the simple additive group structure -- this corresponds to  integral [[ordinary cohomology]] given by the [[Eilenberg-MacLane spectrum]];

* the multiplicative group that corresponds to complex [[topological K-theory]]

* the formal group law on an [[elliptic curve]].

An **elliptic cohomology** theory is an even [[periodic cohomology theory|periodic]] [[multiplicative cohomology theory|multiplicative]] [[generalized (Eilenberg-Steenrod) cohomology]] theory whose corresponding formal group is an elliptic curve, hence which is [[Brown representability theorem|represented]] by an [[elliptic spectrum]].

(e.g. [Lurie, def. 1.2](#Lurie)).

The [[Goerss-Hopkins-Miller-Lurie theorem]] shows that the assignment of [[generalized (Eilenberg-Steenrod) cohomology]] theories to [[elliptic curves]] lifts to an assignment of representing [[spectrum|spectra]] in a structure-preserving way. 

The [[homotopy limit]] of this assignment functor, i.e. the "gluing" of all spectra representing all elliptic cohomology theories is the [[spectrum]] that represents the cohomology theory called [[tmf]].

## Properties

### Genera, the elliptic genus and relation to string theory

> A properly developed theory of [[elliptic cohomology]] is likely to shed some light on what [[string theory]] really means. ([Witten 87, very last sentence](#Witten87))


The following is **rough material** originating from notes taken live (and long ago), to be polished. See also at _[[elliptic genus]]_ and _[[Witten genus]]_ 



Some topological invariants of [[manifolds]] that are of interest:

we restricted attention to [[closed manifold|closed]] connected  [[smooth manifolds]] $X$

* the [[Euler characteristic]] $e(X) \in \mathbb{Z}$

  * takes all values in $\mathbb{Z}$

  * is the obstruction to the existence of a nowhere vanishing [[vector field]] on $X$:

    $$
      (e(X)= 0)
      \Leftrightarrow
      (\exists  v \in \Gamma(T X) : \forall x \in X : v(x) \neq 0)
    $$  


* [[signature]] $sgn(X)$

  this is the obstruction to $X$ being cobordant to a fiber bundle over the circle:

  $X$ is [[bordant manifold|bordant]] to a [[fiber bundle]] over $S^1$ precisely if $sgn(X) = 0$

* when $X$ has a [[spin structure]]

  the index of the [[Dirac operator]] $D$: 

  $$
    ind D_X \in \mathbb{Z} 
  $$

  $$
    \alpha(D) \in 
    \left\{
      \array{
           \mathbb{Z} & dim X = 0 mod 4
           \\
           \mathbb{Z}_2 & dim X = 1, 2 mod 8
           \\
           0 & otherwise
      }
    \right.
  $$

  **theorem** (Gromov-Lawson / [[Stephan Stolz|Stolz]]) let $dim X \geq 5$ and

  then $X$ admits a [[Riemannian metric]] of positive [[scalar curvature]] precisely when $\alpha(X) = 0$

These invariants share the following properties:

* they are additive under [[disjoint union]] of [[manifold]]s

* they are multiplicative under [[cartesian product]] of manifolds

* $e(X) mod 2, sgn(X), ind(D_X)$ all vanish when $X$ is a boundary, $\exists W : X = \partial W$, which means that $X$ is [[cobordant manifold|cobordant]] to the empty manifold $\emptyset$.

  in other words, these invariants are [[genus|genera]], namely [[ring]] homomorphisms 

  $$
    \Omega \to R
  $$
  
  form the [[cobordism ring]] $\Omega$ to some commutative [[ring]] $R$

* good [[genus|genera]] are those which reflect geometric properties of $X$.

* now for $X$ a [[topological space]] consider the [[cobordism ring]] _over $X$_:

  $$
    \Omega(X) := \{(M,f)| f : M \stackrel{cont}{\to X}\}/_{bordism}
  $$

  where addition and multiplication are again given by disjoint union and cartesian product.

  this assignment of rings to topological spaces is a [[generalized homology]] theory: [[cobordism homology theory]]

  **question** given a [[genus]] $\Omega \to R$, can we find a [[homology theory]] $R(-)$ with $R  = R(pt)$ its [[homology ring]] over the point and such that it all fits into a natural diagram

  $$
    \array{
     \Omega &\to& R
     \\
     \uparrow && \uparrow
     \\
     \Omega(X) &\stackrel{\rho}{\to}& R(X)
    }
  $$

  This would be a _parameterized extension_ $\rho = R(-)$ of $R$ .

  Now let $X$ be a closed manifold. 
  
  consider $u_X : X \to K(\pi_1(X),1)$ (on the right an [[Eilenberg-MacLane space]]) which is the classifying map for the [[universal cover]]

  $$
    u_* \pi_1(X) \stackrel{\simeq_{canon}}{\to}
    \pi_1(K(\pi_1(X), 1))
  $$

  then consider

  $$
    \rho_X[X, u_X] \in R(K(\pi_1(X),1))
  $$

  **theorem (Julia Weber)** 

  take the [[Euler characteristic]]  mod 2, $Eu(X)$

  $$
    \array{
      \Omega^0 &\stackrel{Eu(M)\cdot t^{dim M}}{\to}& \mathbb{Z}_2[t]
      \\
      \uparrow && \uparrow
      \\
      \Omega^0(X) &\to& Eu(X) &
      \simeq H_\bullet(X; \mathbb{Z}_2[t])
    }
  $$

  for $X$ smooth we have then:

  $$
    Eu_X[X, id] = Poincare\; dual\;  of\; total\; Stiefel-Whitney\; class 
  $$

  **theorem** (Minalta)

  something analogous for [[signature genus]]

  $$
    \array{
      \Omega_\bullet^{SO}
      &\to&
      Sig_\bullet(X)
    }
  $$

  $sign_X[X,u] \in sig_\bullet(K) \otimes \mathbb{Q}$

  this is the Novikov higher signature 

  now the same for the $\alpha$-genus

  $$
    \array{
      \Omega_{X}^{Spin} &\stackrel{\alpha}{\to}&
      KO_\bullet(pt)
      \\
      \uparrow && \uparrow
      \\
      \Omega_\bullet^{Spin}
      &\to&
      KO_\bullet(X)
    }
  $$  


now towards elliptic genera: recall the notion of [[string structure]] of a [[manifold]] $X$: a lift of the structure map $X \to \mathcal{B}O(n)$ through the 4th connected universal cover $\mathcal{B}String(n) := \mathcal{B}O(n)\langle 4\rangle \to \mathcal{B} O$:

so consider [[string structure|String manifold]]s and the bordism ring $\Omega_\bullet^{String}$ of String manifold, let $M_\bullet$ be the ring of integral [[modular form]]s, then there is a [[genus]] -- the [[Witten genus]] $W$--

$$
  \array{
    \Omega_\bullet^{String} &\stackrel{W}{\to}& M_\bullet
    \\
    \uparrow && \uparrow
    \\
    \Omega_\bullet^{String}(X)
    &\to&
    M_\bullet(X)
    \\
    &\searrow&
    \\
    && tmf_\bullet(X) 
  }
$$
  
where $\Omega_\bullet^{String}(pt) \to tmf_\bullet(pt)$ is surjective

**conjecture ([[Stolz conjecture]])**

If a String manifold $Y$ has a positive [[Ricci curvature]] [[Riemannian metric|metric]], then the [[Witten genus]] vanishes.

The attempted "Proof" of this is the motivation for the [[Stephan Stolz|Stolz]]-[[Peter Teichner|Teichner]]-program for [[geometric models for elliptic cohomology]]:

**"Proof"** If $Y$ is String, then the [[loop space]] $L Y$ is has [[spin structure]], so if $Y$ has positive [[Ricci curvature]] the $L Y$ has positive [[scalar curvature]] which implies by the above that $ind^{S^1} D_{L Y} = 0$ which by the index formula is the [[Witten genus]].

### Equivariant elliptic cohomology and loop group representations

The analog of the [[orbit method]] with [[equivariant K-theory]]
replaced by [[equivariant elliptic cohomology]] yields (aspects of) the [[representation theory]] of [[loop groups]]. ([Ganter 12](#Ganter12))

### Chromatic filtration

[[!include chromatic tower examples - table]]



## Related concepts

* [[elliptic spectrum]]

* [[elliptic genus]], [[equivariant elliptic genus]]

* [[SO orientation of elliptic cohomology]], [[spin orientation of elliptic cohomology]]

* [[elliptic Chern character]]

* [[equivariant elliptic cohomology]]

* [[sigma-orientation]]

* [[tmf]]

[[!include moduli of higher lines -- table]]


## References

[[!include elliptic cohomology -- references]]


[[!redirects elliptic cohomologies]]

[[!redirects elliptic cohomology theory]]
[[!redirects elliptic cohomology theories]]

[[!redirects elliptic generalized cohomology theory]]
[[!redirects elliptic generalized cohomology theories]]