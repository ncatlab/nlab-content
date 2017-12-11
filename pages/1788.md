
+-- {: .num_defn #StarAlgebra}
###### Definition
**([[star algebra]])**

A _[[star ring]]_ is a [[ring]] $R$ equipped with 

* a [[linear map]]

  $(-)^\ast \;\colon\; R \longrightarrow R$

such that

* ([[involution]]) $((-)^\ast)^\ast = id$;

* ([[antihomomorphism]])

  1. $(a b)^\ast = b^\ast a^\ast$ for all $a,b \in R$

  1. $1^\ast = 1$.

A [[homomorphism]] of star-rings

$$
  f \;\colon\; (R_1, (-)^\ast) \longrightarrow (R_2, (-)^\dagger)
$$

is a [[homomorphism]] of the underlying [[rings]]

$$
  f \;\colon\; R_1 \longrightarrow R_2
$$

which respects the star-[[involutions]] in that 

$$ 
  f \circ (-)^\ast \;=\; (-)^\dagger \circ f
  \,.
$$

A _[[star algebra]]_ $\mathcal{A}$ over a [[commutative ring|commutative]] star-ring $R$ in an [[associative algebra]] $\mathcal{A}$ over $R$ such that the inclusion

$$
  R \hookrightarrow \mathcal{A}
$$

is a star-homomorphism.

=--

+-- {: .num_examples #StarAlgebraOfObservables}
###### Examples
**([[complex number]]-valued [[observables]] are [[star-algebra]] under pointwise product and pointwise [[complex conjugation]])**

The [[complex numbers]] $\mathbb{C}$ carry the [[structure]] of a [[star-ring]] (def. \ref{StarAlgebra}) with star-operation given by [[complex conjugation]].

Given any space $X$, then the [[algebra of functions]] on $X$ with values in the [[complex numbers]] carries the [[structure]] of a [[star-algebra]] over the star-ring $\mathbb{C}$ (def. \ref{StarAlgebra}) with star-operation given by pointwise [[complex conjugation]] in the [[complex numbers]].

In particular for $(E,\mathbf{L})$ a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) then its [[on-shell]] [[observables]] $Obs(E,\mathbf{L})$ (def. \ref{Observable}) carry the structure of a [[star-algebra]] this way.


=--

+-- {: .num_defn #StateOnAStarAlgebra}
###### Definition
**([[state on a star-algebra]])**

Given a [[star algebra]] $(\mathcal{A}, (-)^\ast)$ (def. \ref{StarAlgebra})
over the star-ring of [[complex numbers]] (def. \ref{StarAlgebraOfObservables}) a _[[state on a star-algebra|state]]_ is a [[function]] to the [[complex numbers]]

$$
  \langle -\rangle
  \;\colon\;
  Obs_\Sigma \longrightarrow \mathbb{C}
$$

such that

1. (linearity) this is a complex-[[linear map]]:

   $$
     \left\langle 
       c_1 A_1 + c_2 A_2
     \right\rangle
     \;=\;
     c_1 \langle A_1 \rangle + c_2 \langle A_2 \rangle
   $$

1. (positivity) for all $A \in Obs$ we have that 

   $$
     \langle A^\ast A \rangle \geq 0 \;\in\; \mathbb{R}
   $$

   where on the left $A^\ast$ is the [[star-algebra|star-operation]] from

1. (normalization)

   $$
     \langle 1 \rangle \;=\; 1
     \,.
   $$

=--

(e.g. [Bordemann-Waldmann 96](state+on+a+star-algebra#BordemannWaldmann96), [Fredenhagen-Rejzner 12, def. 2.4](state+on+a+star-algebra#FredenhagenRejzner12), [Khavkine-Moretti 15, def. 6](state+on+a+star-algebra#KhavkineMoretti15))

+-- {: .num_remark #ProbabilityTheoreticInterpretationOfStateOnAStarAlgebra}
###### Remark
**([[probability theory|probability theoretic]] interpretation of [[state on a star-algebra]])**

A [[star algebra]] $\mathcal{A}$ (def. \ref{StarAlgebra}) equipped with a [[state on a star-algebra|state]] $\mathcal{A} \overset{\langle -\rangle}{\longrightarrow} \mathbb{C}$ (def. \ref{States}) is also called a _[[quantum probability space]]_, at least when $\mathcal{A}$ is in fact a [[von Neumann algebra]]. 

For this interpretation we think of each element $A \in \mathcal{A}$ as an [[observable]] as in example \ref{StarAlgebraOfObservables} and of the state as assigning _[[expectation values]]_.

=--




+-- {: .num_remark #StatesFormAConvexSet}
###### Remark
**([[state on a star-algebra|states]] form a [[convex set]])**

For $\mathcal{A}$ a unital [[star-algebra]] (def. \ref{StarAlgebra}), the [[set]] of [[state on a star-algebra|states]] on $\mathcal{A}$ according to def. \ref{StateOnAStarAlgebra} is naturally a [[convex set]]: For $\langle (-)\rangle_1, \langle - \rangle_2 \colon \mathcal{A} \to \mathbb{C}$ two [[state on a star-algebra|states]] then for every $p \in [0,1] \subset \mathbb{R}$ also the [[linear combination]]

$$
  \array{
    \mathcal{A}
     &\overset{p \langle (-)\rangle_1 + (1-p) \langle (-)\rangle_2}{\longrightarrow}&
    \mathbb{C}
    \\
    A &\mapsto& p \langle A \rangle_1 + (1-p) \langle A \rangle_2
  }
$$
 

is a [[state on a star-algebra|state]].

=--

+-- {: .num_defn #PureStateOnAStarAlgebra}
###### Definition
**([[pure state]])**

A [[state on a star-algebra|state]] $\rho \colon \mathcal{A} \to \mathbb{C}$ on a unital [[star-algebra]] (def. \ref{StateOnAStarAlgebra}) is called a _[[pure state]]_ if it is extremal in the [[convex set]] of all states (remark \ref{StatesFormAConvexSet}) in that an identification

$$
  \langle (- )\rangle = p \langle (-)\rangle_1 + (1-p) \langle (-)\rangle_2
$$

for $p \in (0,1)$ implies that $\langle (-) \rangle_1 = \langle (-)\rangle_2$ (hence $= \langle (-)\rangle$).

=--


+-- {: .num_prop #ClassicalProbabilityMeasureAsStateOnMeasurableFunctions}
###### Proposition
**(classical [[probability measure]] as state on [[measurable functions]])**

For $\Omega$ classical [[probability space]], hence a [[measure space]] which normalized total measure $\int_\Omega d\mu = 1$, let $\mathcal{A} \cloneqq L^1(\Omega)$ be the algebra of Lebesgue [[measurable functions]] with values in the [[complex numbers]], regarded as a [[star algebra]] (def. \ref{StarAlgebra}) by pointwise [[complex conjugation]] as in example \ref{StarAlgebraOfObservables}. Then forming the [[expectation value]] with respect to $\mu$ defines a [[state on a star-algebra|state]] (def. \ref{StateOnAStarAlgebra}):

$$
  \array{
    L^1(\Omega) 
      &\overset{\langle (-)\rangle_\mu}{\longrightarrow}& 
    \mathbb{C}
    \\
    A &\mapsto& \int_\Omega A d\mu
  }
$$


=--

+-- {: .num_example #ElementsOfHilbertSpaceAsPureStates}
###### Example
**(elements of a [[Hilbert space]] as [[pure states]] on [[bounded operators]])**

Let $\mathcal{H}$ be a [[complex numbers|complex]] [[separable Hilbert space|separable]] [[Hilbert space]] with [[inner product]] $\langle -,-\rangle$ and let $\mathcal{A} \coloneqq \mathcal{B}(\mathcal{H})$ be the algebra of [[bounded operators]], regarded as a [[star algebra]] (def. \ref{StarAlgebra}) under forming [[adjoint operators]]. Then for every element $\psi \in \mathcal{H}$ of unit [[norm]] $\langle \psi,\psi\rangle = 1$ there is the [[state on a star-algebra|state]] (def. \ref{StateOnAStarAlgebra}) given by

$$
  \array{
    \mathcal{B}(\mathcal{H})
      &\overset{\langle (-)\rangle_\psi}{\longrightarrow}&
     \mathbb{C}
     \\
     A &\mapsto& \langle \psi \vert\, A \, \vert \psi \rangle &\coloneqq& \langle \psi, A \psi \rangle
  }
$$

These are [[pure states]] (def. \ref{PureStateOnAStarAlgebra}).

More general states in this case are given by [[density matrices]].

=--

+-- {: .num_theorem #GNSConstruction}
###### Theorem
**([[GNS construction]])**

Given 

1. a [[star-algebra]], $\mathcal{A}$ (def. \ref{StarAlgebra});

1. a [[state on a star-algbra|state]], $\langle (-)\rangle \;\colon\; \mathcal{A} \to \mathbb{C}$ (def. \ref{StateOnAStarAlgebra})

there exists 

1. a [[star-representation]]

   $$
     \pi 
     \;\colon\;
     \mathcal{A}
      \longrightarrow
      End(\mathcal{H})
   $$

   of $\mathcal{A}$ on some [[Hilbert space]] $\mathcal{H}$

1. a [[cyclic vector]] $\psi \in \mathcal{H}$ 

such that $\langle (-)\rangle$ is the state corresponding to $\psi$ via example \ref{ElementsOfHilbertSpaceAsPureStates}, in that

$$
  \begin{aligned}
    \langle A \rangle
      & = \langle \psi \vert\, A \, \vert \psi \rangle
      \\
      & \coloneqq
      \langle \psi , \pi(A) \psi \rangle
  \end{aligned}
$$

for all $A \in \mathcal{A}$.

=--

([Khavkine-Moretti 15, theorem 1](GNS+construction#KhavkineMoretti15))



+-- {: .num_defn #ClassicalState}
###### Definition
**(classical state)**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) then a _classical state_ is a [[state on a star-algebra|state on the star algebra]] (def. \ref{StateOnAStarAlgebra}) of [[on-shell]] [[observables]] (example \ref{StarAlgebraOfObservables}):

$$
  \langle -\rangle
  \;\colon\;
  Obs(E,\mathbf{L})
   \longrightarrow
  \mathbb{C}
  \,.
$$


=--



Below we consider _[[quantum states]]_. These are defined formally in just the same way, only that now the algebra of observables is equipped with another product, which changes the meaning of
the product expression $A^\ast A$.
