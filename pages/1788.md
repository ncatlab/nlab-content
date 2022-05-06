
**Cohomotopy theory and Microscopic brane physics**

As reviewed in H. Sati's talk, assuming that the C-field is charge-quantized in the generalized cohomology theory called J-twisted Cohomotopy  ("Hypothesis H") implies a list of M-theoretic anomaly cancellation conditions, such a shifted flux quantization, DMW anomaly cancellation and C-field tadpole cancellation on 8-manifolds. In this talk I review the further geometric refinement of the cohomology theory to equivariant Cohomotoy theory and to differential Cohomotopy theory. Now we find that Hypothesis H implies also the Witten mechanism of multiple M5-branes on MO5 ADE-orientifolds, hence RR-field tadpole cancellation in IIA, as well as a multitude of effects associated with Dp/D(p+2)-brane intersections: Chan-Paton factors, BMN matrix model fuzzy funnel states and BLG 3-algebras, the Hanany-Witten rules, AdS3-gravity observables, supersymmetric indices of Coulomb branches as well as gauge/gravity duality between all these.
This suggest that Hypothesis H is a correct assumption about the elusive mathematical fomulation of M-theory.
This is joint work with H. Sati (arxiv.org/abs/1909.12277, arxiv.org/abs/1912.10425 )

## Definition
 {#Definition}

+-- {: .num_defn}
###### Definition

Where $K\subset \mathbb{R}^d$ is compact, $\{T_L\}_{L\leq N \in \mathbb{N}}$ a finite set of affine maps such that $T_L(x) = \langle W_L,x\rangle + b_L$ where $W_L$ is the $L^{th}$ layer weight matrix and $b_L$ the $L^{th}$ layer bias, $g:\mathbb{R}\to\mathbb{R}$ a non-linear activation function, a **neural network**  is a function $f:K\subset \mathbb{R}^d \to \mathbb{R}^m$, such that on input $x$, computes the composition:

$$f(x) = (T_L\circ g \circ T_{L-1}\circ g \circ \dots \circ T_1)(x)$$

where $g$ is applied component-wise. 
=--

Duality is duality.

Let $\mathfrak{g} = \mathfrak{su}(2)$ and consider complex representations.

Then $\mathfrak{g}$-weight system are 

1. observables on CS/RW theory;

1. states of BMN matrix model.

In the second case, chord diagrams are the observables.

| | [[anti de Sitter spacetime|AdS]] [[3d gravity]] | [[BMN matrix model]] | 
|--|--|--|
| [[observables]] | [[weight systems]] <br/> commutative/classical | [[chord diagrams]] <br/> non-commutative/quantum | 
| [[states]] |  |  [[weight systems]]  | 



For $n \in \mathbb{N}$ write 

\[
  \label{OrderedConfigurationSpaceofnPointsinC}
  \underset{{}^{\{1,\cdots,n\}}}{Conf}(\mathbb{R}^2)
  \;\coloneqq\;
  (\mathbb{R}^2)^n \backslash FatDiagonal
\]

for the [[ordered configuration space of n points]] in the [[plane]], regarded as a [[smooth manifold]].

Identifying this with the [[complex plane]] $\mathbb{C}$, we have canonical [[coordinate functions]]

\[
  \label{CoordinateFunctionsOnConfC}
  (z_1, \cdots, z_n)
  \;\colon\;
  \underset{{}^{\{1,\cdots,n\}}}{Conf}(\mathbb{R}^2)
  \longrightarrow
  \mathbb{C}^n
  \,.
\]


Write moreover

$$
  \mathcal{A}^{{}^{pb}}_{n}
  \;\coloneqq\;
  Span\big(\mathcal{D}^{{}^{pb}}\big)/4T
$$

for the [[quotient vector space]] of the [[linear span]] of [[horizontal chord diagrams]] on $n$ strands by the [[4t relations]] ([[infinitesimal braid relations]]), regarded as an [[associative algebra]] under [[concatenation]] of strands ([here](horizontal+chord+diagram#AlgebraOfHorizontalChordDiagrams)).

Then the _[[Knizhnik-Zamolodchikov form]]_ is the [[horizontal chord diagram]]-[[Lie algebra valued differential form|algebra valued differential form]] on the [[configuration space of points]]  (eq:OrderedConfigurationSpaceofnPointsinC)$ 
