## Feynman diagrams
 {#FeynmanDiagrams}

So far we considered only the [[axioms]] on a consistent perturbative S-matrix /[[time-ordered products]]
and its formal consequences. Now we discuss the actual construction of [[time-ordered products]],
hence of perturbative S-matrices, by the process called _[[renormalization]] of [[Feynman diagrams]]_.

We first discuss how [[time-ordered product]], and hence the perturbative S-matrix [above](#PerturbativeSMatrixAndTimeOrderedProducts),
is uniquely determined away from the locus where interaction points coincide (prop. \ref{TimeOrderedProductAwayFromDiagonal} below).
Moreover, we discuss how on that locus the time-ordered product is naturally expressed as a sum
of [[products of distributions]] of [[Feynman propagators]] that are labeled by [[Feynman diagrams]]: the _[[Feynman perturbation series]]_ (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} below).

This means that the full  [[time-ordered product]] is an [[extension of distributions]] of these
_[[scattering amplitudes]]- to the locus of coinciding vertices. The space of possible such
extensions turns out to be finite-dimensional in each order of $g/\hbar, j/\hbar$, parameterizing the choice of
[[point-supported distributions]] at the interaction points whose [[degree of a distribution|scaling degree]]
is bounded by the given Feynman propagators.

+-- {: .num_defn #TuplesOfCompactlySupportedPolynomialLocalFunctionalsWithPairwiseDisjointSupport}
###### Definition

For $k \in \mathbb{N}$, write

$$
  \left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}_{pds}
  \hookrightarrow
  \left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}
$$

for the subspace of the $k$-fold [[tensor product]] of the space of compactly supported polynomial
local densities (def. \ref{CompactlySupportedPolynomialLocalDensities}) on those [[tuples]]
which have pairwise disjoint spacetime [[support]].

=--

+-- {: .num_prop #TimeOrderedProductAwayFromDiagonal}
###### Proposition
**([[time-ordered product]] away from the diagonal)**

Restricted to $\left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}_{pds}$
(def. \ref{TuplesOfCompactlySupportedPolynomialLocalFunctionalsWithPairwiseDisjointSupport})
there is a unique [[time-ordered product]] (def. \ref{TimeOrderedProduct}),
given by the [[star product]] that is induced by the [[Feynman propagator]] $\omega_F$

$$
  F \star_{\omega_F} G
  \;\coloneqq\;
  prod \circ
  \exp\left(
   \hbar
   \left\langle
     \omega_F , \frac{\delta}{\delta \phi} \otimes \frac{\delta}{\delta \phi}
   \right\rangle
  \right)
  (F \otimes G)
$$

in that

$$
  T( L_1 \cdots L_k )
  =
  L_1 \star_{\omega_F} L_2 \star_{\omega_F} \cdots \star_{\omega_F} L_k
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since the [[singular support]] of the [[Feynman propagator]] is on the [[diagonal]],
and since the support of elements in $\left(\mathcal{F}_{loc}\langle g,j\rangle\right)^{\otimes^k}_{pds}$
is by definition in the complement of the diagonal, the star product $\star_{\omega_F}$ is well defined.
By construction it satisfies the axioms "peturbation" and "normalization" in def. \ref{TimeOrderedProduct}.
The only non-trivial point to check is that it indeed satisfies "[[causal factorization]]":

Unwinding the definition of the [[Hadamard state]] $\omega$ and the [[Feynman propagator]] $\omega_F$, we have

$$
  \begin{aligned}
    \omega & = \tfrac{i}{2}( \Delta_R - \Delta_A ) + H
    \\
    \omega_F & = \tfrac{i}{2}( \Delta_R + \Delta_A ) + H
  \end{aligned}
$$

where the propagators on the right have, in particular, the following properties:

1. the [[advanced propagator]] vanishes when its first argument is not in the causal past of its second argument:

   $$
     (supp(F) \geq supp(G))
     \;\Rightarrow\;
     \left(
       \left\langle \Delta_A , \frac{\delta F}{\delta \phi} \otimes \frac{\delta G}{\delta \phi}  \right\rangle = 0
     \right)
     \,.
   $$

1. the [[retarded propagator]] equals the [[advanced propagator]] with arguments switched:

   $$
     \left\langle \Delta_R , \frac{\delta F}{\delta \phi} \otimes \frac{\delta G}{\delta \phi} \right\rangle
       =
     \left\langle \Delta_A , \frac{\delta G}{\delta \phi} \otimes \frac{\delta F}{\delta \phi} \right\rangle
   $$

1. $H$ is symmetric:

   $$
     \left\langle H, \frac{\delta F}{\delta \phi} \otimes \frac{\delta G}{\delta \phi} \right\rangle
     =
     \left\langle H, \frac{\delta G}{\delta \phi} \otimes \frac{\delta F}{\delta \phi} \right\rangle
   $$

It follows for causal ordering $supp(F) \geq supp(G)$ (def. \ref{CausalOrdering}) that

$$
  \begin{aligned}
    F \star_{\omega_F} G
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \omega_F , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}( \Delta_R + \Delta_A ) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}\Delta_R + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}( \Delta_R - \Delta_A ) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ
    \exp\left(
      \hbar
      \left\langle  \omega , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    F \star_{\omega} G
  \end{aligned}
$$

and for $supp(G) \geq supp(F)$ that

$$
  \begin{aligned}
    F \star_{\omega_F} G
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \omega_F , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2}( \Delta_R + \Delta_A ) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2} \Delta_A + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( F \otimes G )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2} \Delta_R + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( G \otimes F )
    \\
    & =
    prod \circ \exp\left(
      \hbar
      \left\langle  \tfrac{i}{2} (\Delta_R - \Delta_A) + H  , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle
    \right)
    ( G \otimes F )
    \\
    & =
    G \star_{\omega} F
    \,.
  \end{aligned}
$$

This shows that $\star_F$ is a consistent time-ordered product on the subspace of functionals
with disjoint support. It is immediate from the above that it is the unique solution on this subspace.

=--

+-- {: .num_remark #TimeOrderedProductAssociative}
###### Remark
**([[time-ordered product]] is [[associativity|assocativative]])**

Prop. \ref{TimeOrderedProductAwayFromDiagonal} implies in particular that the
time-ordered product is [[associativity|associative]], in that

$$
  T( T(V_1 \cdots V_{k_1}) \cdots T(V_{k_{n-1}+1} \cdots V_{k_n} ) )
  =
  T( V_1 \cdots V_{k_1} \cdots V_{k_{n-1}+1} \cdots V_{n_n} )
  \,.
$$

=--

It follows that the problem of constructing time-ordered products, and hence (by prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix}) the
perturbative S-matrix, consists of finding compatible [[extension of distributions|extension]]
of the distribution
$ prod \circ \exp\left( \left\langle  \omega_F , \frac{\delta }{\delta \phi} \otimes \frac{\delta}{\delta \phi}  \right\rangle \right)$ to the diagonal.

Moreover, by the nature of the exponential expression, this means in each order to
extend [[product of distributions|products]] of Feynman propagators labeled by
[[graphs]] whose [[vertices]] correspond to the polynomial factors in $F$ and $G$ and whose
[[edges]] indicate over which variables the Feynman propagators are to be multiplied.


+-- {: .num_defn #ScalarFieldFeynmanDiagram}
###### Definition
**([[scalar field]] [[Feynman diagram]])**

A _[[scalar field]] [[Feynman diagram]]_ $\Gamma$ is

1. a [[natural number]] $v \in \mathcal{N}$ (number of [[vertices]]);

1. a $v$-[[tuple]] of elements $(V_r \in \mathcal{F}_{loc} \langle g,j\rangle)_{r \in \{1, \cdots, v\}}$ (the interaction and external field vertices)

1. for each $a \lt b \in \{1, \cdots, v\}$ a natural number $e_{a,b} \in \mathbb{N}$ ("of [[edges]] from the $a$th to the $b$th vertex").

For a given [[tuple]] $(V_j)$ of interaction vertices we write

$$
  FDiag_{(V_j)}
$$

for set of scalar field Feynman diagrams with that tuple of vertices.

=--

+-- {: .num_prop #FeynmanPerturbationSeriesAwayFromCoincidingPoints}
###### Proposition
**([[Feynman perturbation series]] away from coinciding vertices)**


For $v \in \mathbb{N}$ the $v$-fold
[[time-ordered product]] away from the diagonal,
given by prop. \ref{TimeOrderedProductAwayFromDiagonal}

$$
  T_v
    \;\colon\;
  \left(\mathcal{F}_{loc}\langle g,j\rangle\right)_{pds}^{\otimes^{v}}
    \longrightarrow
  \mathcal{W}[ [ g/\hbar, j/\hbar] ]
$$

is equal to

$$
  T_k(V_1 \cdots V_v)
    \;=\;
  prod
    \circ
  \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
  \underset{ r \lt s \in \{1, \cdots, v\} }{\prod}
  \tfrac{1}{e_{r,s}!}
  \left\langle
      \hbar \omega_F
      \,,\,
      \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
      \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
  \right\rangle
  (V_1 \otimes \cdots \otimes V_v)
  \,,
$$

where the edge numbers $e_{r,s} = e_{r,s}(\Gamma)$ are those of the given Feynman diagram $\Gamma$.

=--

([Keller 10, IV.1](Feynman+diagram#Keller10))

+-- {: .proof}
###### Proof

We proceed by [[induction]] over the number of [[vertices]].
The statement is trivially true for a single vertex.
Assume it is true for $v \geq 1$ vertices. It follows that

$$
  \begin{aligned}
    T(V_1 \cdots V_v V_{v+1})
    & =
    T( T(V_1 \cdots V_v) V_{v+1} )
    \\
    &=
    prod \circ
    \exp\left(
      \left\langle
         \hbar \omega_F, \frac{\delta}{\delta \phi} \otimes \frac{\delta}{\delta \phi}
      \right\rangle
    \right)
    \left(
      prod
        \circ
      \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
      \underset{ r \gt s \in \{1, \cdots, v\} }{\prod}
      \frac{1}{e_{r,s}!}
      \left\langle
          \hbar \omega_F
          \,,\,
          \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
          \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
      \right\rangle
      (V_1 \otimes \cdots \otimes V_v)
    \right)
    \;\otimes\;
    V_{v+1}
    \\
    & =
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
      \underset{ r \gt s \in \{1, \cdots, v\} }{\prod}
      \tfrac{1}{e_{r,s}!}
    \left\langle
        \hbar \omega_F
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
    \right\rangle
    \left(
    \underset{e_{1,{v+1}}, \cdots e_{v,v+1} \in \mathbb{N}}{\sum}
      \underset{t \in \{1, \cdots v\}}{\prod}
      \tfrac{1}{e_{t,v+1} !}
    \left(
      \frac{\delta^{e_{1,v+1}} V_1 }{\delta \phi_{1}^{e_{1,v+1}}}
        \otimes
        \cdots
        \otimes
      \frac{ \delta^{e_{v,v+1}} V_v}{ \delta \phi_{v}^{e_{v,v+1}} }
    \right)
    \;\otimes\;
    \frac{\delta^{e_{1,v+1} + \cdots + e_{v,v+1}} V_{v+1}}{\delta \phi_{v-1}^{e_{1,v+1} + \cdots + e_{v,v+1}}}
    \right)
    \\
    &=
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v+1}}}{\sum}
    \underset{ r \lt s \in \{1, \cdots, v+1\} }{\prod}
    \tfrac{1}{e_{r,s}!}
    \left\langle
        \hbar \omega_F
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \phi_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{ \delta \phi_s^{e_{r,s}} }
    \right\rangle
    (V_1 \otimes \cdots \otimes V_{v+1})
  \end{aligned}
$$

Here in the first step we use the [[associativity]] of the time-ordered product
(remark \ref{TimeOrderedProductAssociative}), in the second step we use the induction assumption,
in the third we pass the outer functional derivatives through the pointwise product
using the [[product rule]], and in the fourth step we recognize that this amounts to summing
in addition over all possible choices of sets of edges from the first $v$ vertices to the new $v+1$st vertex,
which yield in total the sum over all diagrams with $v+1$ vertices.

=--


+-- {: .num_remark}
###### Remark
**([[loop order]] and powers of [[Planck's constant]])**

From prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} one deduces that the
order in [[Planck's constant]] that a ([[planar graph|planar]]) [[Feynman diagram]] contributes to the
S-matrix is given (up to a possible offset due to external vertices) by the "number of loops" in the diagram.


In the computation of [[scattering amplitudes]] for [[field (physics)|fields]]/[[particles]] via [[perturbative quantum field theory]] the [[scattering matrix]] ([[Feynman perturbation series]]) is a [[formal power series]] in (the [[coupling constant]] and) [[Planck's constant]] $\hbar$ whose contributions may be labeled by [[Feynman diagrams]]. Each Feynman diagram $\Gamma$ is a finite labeled [[graph]], and the order in $\hbar$ to which this graph contributes is

$$
  \hbar^{ E(\Gamma) - V(\Gamma) }
$$

where

1. $V(\Gamma) \in \mathbb{N}$ is the number of [[vertices]] of the graph

1. $E(\Gamma) \in \mathbb{N}$ is the number of [[edges]] in the graph.

This comes about, according to the above, because

1. the explicit $\hbar$-dependence of the [[S-matrix]] is

   $$
     S\left(\tfrac{g}{\hbar} L_{int} \right)
     =
     \underset{k \in \mathbb{N}}{\sum} \frac{g^k}{\hbar^k k!} T( \underset{k \, \text{factors}}{\underbrace{L_{int} \cdots L_{int}}} )
   $$

1. the further $\hbar$-dependence of the [[time-ordered product]] $T(\cdots)$ is

   $$
     T(L_{int} L_{int}) = prod \circ \exp\left( \hbar \int \omega_{F}(x,y) \frac{\delta}{\delta \phi(x)} \otimes \frac{\delta}{\delta \phi(y)}  \right) ( L_{int} \otimes L_{int} )
     \,,
   $$

where $\omega_F$ denotes the [[Feynman propagator]] and $\phi(x)$ the field observable at point $x$ (where we are notationally suppressing the internal degrees of freedom of the fields for simplicity, writing them as [[scalar fields]], because this is all that affects the counting of the $\hbar$ powers).

The resulting terms of the S-matrix series are thus labeled by

1. the number of factors of the [[interaction]] $L_{int}$, these are the [[vertices]] of the corresponding Feynman diagram and hence each contibute with $\hbar^{-1}$

1. the number of integrals over the Feynman propagator $\omega_F$, which correspond to the edges of the Feynman diagram, and each contribute with $\hbar^1$.

Now the formula for the [[Euler characteristic of planar graphs]] says that the number of regions in a plane that are encircled by edges, the _faces_ here thought of as the number of "loops", is

$$
  L(\Gamma) =  1 + E(\Gamma) - V(\Gamma)
  \,.
$$

Hence a planar Feynman diagram $\Gamma$ contributes with

$$
  \hbar^{L(\Gamma)-1}
  \,.
$$

So far this is the discussion for internal edges. An actual scattering matrix element is of the form

$$
  \langle \psi_{out} \vert S\left(\tfrac{g}{\hbar} L_{int} \right)
  \vert \psi_{in} \rangle
  \,,
$$

where

$$
  \vert \psi_{in}\rangle
    \propto
  \tfrac{1}{\sqrt{\hbar^{n_{in}}}}
  \phi^\dagger(k_1) \cdots \phi^\dagger(k_{n_{in}}) \vert vac \rangle
$$

is a state of $n_{in}$ free field quanta and similarly

$$
  \vert \psi_{out}\rangle
    \propto
  \tfrac{1}{\sqrt{\hbar^{n_{out}}}}
  \phi^\dagger(k_1) \cdots \phi^\dagger(k_{n_{out}}) \vert vac \rangle
$$

is a state of $n_{out}$ field quanta. The normalization of these states, in view of the commutation relation $[\phi(k), \phi^\dagger(q)] \propto \hbar$, yields the given powers of $\hbar$.

This means that an actual [[scattering amplitude]] given by a [[Feynman diagram]] $\Gamma$ with $E_{ext}(\Gamma)$ external vertices scales as

$$
  \hbar^{L(\Gamma) - 1 + E_{ext}(\Gamma)/2 }
  \,.
$$

(For the analogous discussion of the dependence on the actual [[quantum observables]] on $\hbar$ given by [[Bogoliubov's formula]], see [there](Bogoliubov's+formula#PowersInPlancksConstant).)



=--
