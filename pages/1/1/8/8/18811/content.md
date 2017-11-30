

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _evolutionary derivative_ or "[[Fréchet derivative]] of a [[tuple]] of differential functions" ([Olver 93, def. 5.24](#Olver93))) is the [[derivative]] of a [[section]] of some [[vector bundle]] $V$ depending on [[jets]] of a "[[field bundle]]" $E$ (def. \ref{FieldDependentSections} below) along the prolongation of an [[evolutionary vector field]] on $E$. Equivalently this is a jet-dependent [[differential operator]] on the [[vertical tangent bundle]] of $E$ and as such is usefully related to the [[Euler-Lagrange derivative]] on $E$ (example \ref{DifferentialOperatorDerivativeOfLagrangianFunction} and prop. \ref{EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives} below).

## Definition

In the following _[[fiber bundles]]_ are considered in [[differential geometry]] and in particular _[[vector bundle]]_ means _[[smooth vector bundle]]_.

+-- {: .num_defn #FieldDependentSections}
###### Definition
**([[field (physics)|field]]-dependent [[sections]])**

For

$$
  E \overset{fb}{\longrightarrow} \Sigma
$$

a [[fiber bundle]], regarded as a [[field bundle]], and for 

$$
  E' \overset{fb'}{\longrightarrow} \Sigma
$$

any other [[fiber bundle]] over the same base space ([[spacetime]]), we write

$$
  \Gamma_{J^\infty_\Sigma(E)}(E')
  \;\coloneqq\;
  \Gamma_{J^\infty_\Sigma(E)}( jb^\ast E' )
  \;=\;
  Hom_\Sigma(J^\infty_\Sigma(E), E')
  \;\simeq\; 
  DiffOp(E,E')
$$

for the [[space of sections]] of the [[pullback of bundles]] of $E'$ to the [[jet bundle]] $J^\infty_\Sigma(E) \overset{jb}{\longrightarrow} \Sigma$  along $jb$.

$$
  \Gamma_{J^\infty_\Sigma(E)}(E')
  \;=\;
  \left\{
    \array{
       && E'
       \\
       & {}^{\mathllap{}}\nearrow & \downarrow \mathrlap{fb'} 
       \\
       J^\infty_\Sigma(E)
       &\underset{jb}{\longrightarrow}&
       \Sigma
    }
    \phantom{A}\,\,
  \right\}
  \,.
$$

(Equivalently this is the space of [[differential operators]] from sections of $E$ to sections of $E'$. )

=--

In ([Olver 93, section 5.1, p. 288](#Olver93)) the field dependent sections of def. \ref{FieldDependentSections}, considered in [[local coordinates]], are referred to as [[tuples]] of _differential functions_.

+-- {: .num_example #EvolutionaryVectorFieldsAsFieldDependentSections}
###### Example
**([[source forms]] and [[evolutionary vector fields]] are field-dependent sections)**

For $E \overset{fb}{\to} \Sigma$ a [[field bundle]], write $T_\Sigma E$ for its [[vertical tangent bundle]] and $T_\Sigma^\ast E$ for its [[dual vector bundle]], the [[vertical cotangent bundle]].

Then the field-dependent sections of these bundles according to def. \ref{FieldDependentSections} are identified as follows:
 
* the space $\Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)$ contains the space of [[evolutionary vector fields]] $v$ as those bundle morphism which respect not just the projection to $\Sigma$ but also its factorization through $E$:

  $$
    \left(
      \array{
        && T_\Sigma E
        \\
        & {}^{\mathllap{v}}\nearrow & \downarrow^{\mathrlap{tb_\Sigma}}
        \\
        J^\infty_\Sigma(E) &\underset{jb_{\infty,0}}{\longrightarrow}& E & \overset{fb}{\longrightarrow}& \Sigma
      }
    \right)
    \;\in\;
    \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)
  $$

* $\Gamma_{J^\infty_\Sigma(E)}( T^\ast_\Sigma E) \otimes \wedge^{p+1}_\Sigma(T^\ast \Sigma)$ contains the space of [[source forms]] $E$ as those bundle morphisms which respect not just the projection to $\Sigma$ but also its factorization through $E$:

  $$
    \left(
      \array{
        && T^\ast_\Sigma E
        \\
        & {}^{E}\nearrow & \downarrow^{\mathrlap{ctb_\Sigma}}
        \\
        J^\infty_\Sigma(E) &\underset{jb_{\infty,0}}{\longrightarrow}& E & \overset{fb}{\longrightarrow}& \Sigma
      }
    \right)
    \;\in\;
    \Gamma_{J^\infty_\Sigma(E)}(T^\ast_\Sigma E)
  $$


This makes manifest the duality pairing between [[source forms]] and [[evolutionary vector fields]]

$$
  \array{
    \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)
    \otimes
    \Gamma_{J^\infty_\Sigma(E)}(T^\ast_\Sigma E)
    &\longrightarrow&
    C^\infty(J^\infty_\Sigma(E))
  } 
$$

which in local coordinates is given by

$$
  (v^a \partial_{\phi^a} \,,\, \omega_a \delta \phi^a)
  \mapsto
  v^a \omega_a
$$

for $v^a, \omega_a \in C^\infty(J^\infty_\Sigma(E))$ [[smooth functions]] on the [[jet bundle]].

=--

+-- {: .num_defn #FieldDependentDifferentialOperatorDerivative}
###### Definition
**([[evolutionary derivative of field-dependent section]])**

Let 

$$
  E \overset{fb}{\to} \Sigma
$$ 

be a [[fiber bundle]] regarded as a [[field bundle]] and let

$$
  V \overset{vb}{\to} \Sigma
$$

be a [[vector bundle]]. Then for

$$
  P \in \Gamma_{J^\infty_\Sigma(E)}(V)
$$

a field-dependent section of $E$ accoring to def. \ref{FieldDependentSections}, its _evolutionary derivative_ is the morphism

$$
  \array{
    \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)
      & \overset{  \mathrm{D}P }{\longrightarrow} &
    \Gamma_{J^\infty_\Sigma(E)}(V)
    \\
    v &\mapsto& \hat v(P) 
  }
$$

which, under the identification of example \ref{EvolutionaryVectorFieldsAsFieldDependentSections}, sense an [[evolutionary vector field]] $v$ to the [[derivative]] of $P$ along the prolongation [[tangent vector field]] $\hat v $ of $v$.


In the case that $E$ and $V$ are [[trivial vector bundles]] over [[Minkowski spacetime]] with coordinates $((x^\mu), (\phi^a))$ and $((x^\mu),  (\rho^b))$, respectively, then this is given by

$$
  ((\mathrm{D}P)(v))^b
   \;=\;
  \left(
     v^a \frac{\partial P^b}{\partial \phi^a}
     +
     \frac{d v^a}{d x^\mu}  
     \frac{\partial P^b}{\partial \phi^a_{,\mu}}
     +
      \frac{d^2 v^a}{d x^\mu d x^\nu}
      \frac{\partial  P^b}{\partial \phi^a_{,\mu \nu}}
      +
     \cdots
  \right)
$$

This makes manifest that $\mathrm{D}P$ may equivalently be regarded as a $J^\infty_\Sigma(E)$-dependent [[differential operator]] from the [[vertical tangent bundle]] $T_\Sigma E$ to $V$, namely a morphism of the form

$$
  \mathrm{D}_P
  \;\colon\;
  J^\infty_\Sigma(E) \times_\Sigma J^\infty_\Sigma T_\Sigma E
  \longrightarrow
  V   
$$

in that

$$
  \label{FrechetDerivativeAsDifferentialOperatorEquality}
  \mathrm{D}_P(-,v)
  =
  \mathrm{D}P(v)
  = 
  \hat v (P)
  \,.
$$

=--

([Olver 93, def. 5.24](#Olver93))


## Examples


+-- {: .num_example #DifferentialOperatorDerivativeOfLagrangianFunction}
###### Example
**([[evolutionary derivative]] of [[Lagrangian function]])**

Over a ([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian manifold]] $\Sigma$, let $\mathbf{L} = L dvol \in \Omega^{p,0}_\Sigma(E)$ be a [[Lagrangian density]], with coefficient function regarded as a field-dependent section (def. \ref{FieldDependentSections}) of the [[trivial bundle|trivial]] [[real line bundle]]:

$$
  L \;\in \; \Gamma_{J^\infty_\Sigma}(E)(\Sigma \times \mathbb{R})
  \,,
$$

Then the [[formally adjoint differential operator]]  

$$
  (\mathrm{D}_L)^\ast
    \;\colon\;
  J^\infty_\Sigma(E)\times_\Sigma (\Sigma \times \mathbb{R})^\ast
  \longrightarrow
  T_\Sigma^\ast E
$$


of its [[evolutionary derivative]], def. \ref{FieldDependentDifferentialOperatorDerivative}, regarded as a $J^\infty_\Sigma(E)$-dependent differential operator $\mathrm{D}_P$ from $T_\Sigma$ to $V$ and applied to the constant section 

$$
  1 \in \Gamma_\Sigma(\Sigma \times \mathbb{R}^\ast)
$$

is the [[Euler-Lagrange derivative]]

$$
  \delta_{EL}\mathbf{L}
  \;=\;
  \left(\mathrm{D}_{L}\right)^\ast(1)
  \;\in\;
  \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma^\ast)
   \simeq
   \Omega^{p+1,1}_\Sigma(E)_{source}
$$

via the identification from example \ref{EvolutionaryVectorFieldsAsFieldDependentSections}.

=--

([Olver 93, above (5.80)](#Olver93))


## Properties

+-- {: .num_prop #EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives}
###### Proposition
**([[Euler-Lagrange derivative]] is [[derivation]] via [[evolutionary derivatives]])**

Let $V \overset{vb}{\to} \Sigma$ be a [[vector bundle]] and write $V^\ast \overset{}{\to} \Sigma$ for its [[dual vector bundle]]. 

For field-dependent sections (def. \ref{FieldDependentSections})

$$
  \alpha \in \Gamma_{J^\infty_\Sigma(E)}(V)
$$ 

and 

$$
  \beta^\ast \in \Gamma_{J^\infty_\Sigma(E)}(V^\ast)
$$ 

we have that the [[Euler-Lagrange derivative]] of their canonical pairing to a [[smooth function]] on the [[jet bundle]] is the sum of the derivative of either one via the [[formally adjoint differential operator]] of the [[evolutionary derivative]] (def. \ref{FieldDependentDifferentialOperatorDerivative}) of the other:

$$
  \delta_{EL}( \alpha \cdot \beta^\ast )
  \;=\;
  (\mathrm{D}_\alpha)^\ast(\beta^\ast)
  + 
  (\mathrm{D}_{\beta^\ast})^\ast(\alpha)
$$

=--

([Olver 93 (5.80)](#Olver93))

+-- {: .proof}
###### Proof

It is sufficient to check this in [[local coordinates]]. By the [[product law]] for [[differentiation]] we have

$$
  \begin{aligned}
    \frac{
      \delta_{EL} \left(\alpha \cdot \beta^\ast \right)
    }
    {
      \delta \phi^a
    }
    & =
    \frac{\partial \left(\alpha \cdot \beta^\ast \right)}{\partial \phi^a}
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \left( \alpha \cdot \beta^\ast \right)}{\partial \phi^a_{,\mu}}
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \left( \alpha \cdot \beta^\ast \right) }{\partial \phi^a_{,\mu \nu}}
    \right)  
    -
    \cdots
    \\
    & =
    \phantom{+}
    \frac{\partial \alpha }{\partial \phi^a}
    \cdot \beta^\ast
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \alpha }{\partial \phi^a_{,\mu}}
       \cdot 
       \beta^\ast
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \alpha  }{\partial \phi^a_{,\mu \nu}}
       \cdot 
       \beta^\ast
    \right)  
    -
    \cdots
    \\
    & \phantom{=}
    +
    \frac{\partial \beta^\ast }{\partial \phi^a}
    \cdot \alpha
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \beta^\ast }{\partial \phi^a_{,\mu}}
       \cdot 
       \alpha
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \beta^\ast  }{\partial \phi^a_{,\mu \nu}}
       \cdot 
       \alpha
    \right)  
    -
    \cdots
    \\
    & =
    (\mathrm{D}_\alpha)^\ast(\beta^\ast)
    + 
    (\mathrm{D}_{\beta^\ast})^\ast(\alpha)
  \end{aligned}
$$

=--


## References

* {#Olver93} [[Peter Olver]], _Applications of Lie groups to Differential equations_, Graduate Texts in Mathematics, Springer 1993

* [[Igor Khavkine]], starting with p. 45 of _Characteristics, Conal Geometry and Causality in Locally Covariant Field Theory_ ([arXiv:1211.1914](https://arxiv.org/abs/1211.1914))

[[!redirects evolutionary derivatives]]

[[!redirects evolutionary derivative of field-dependent section]]
[[!redirects evoolutionary derivatives of field-dependent sections]]
