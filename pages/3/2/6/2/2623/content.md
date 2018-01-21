
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Effective field theory and renormalization
+--{: .hide}
[[!include renormalization - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The construction of a [[perturbative quantum field theory]] from a given [[local Lagrangian density]] (rigorously via [[causal perturbation theory]]) involves ambiguities associated with the detailed nature of the quantum processes at point interactions. What is called _renormalization_ is making a choice of fixing these ambiguities to produce a [[perturbative quantum field theory]] ([Wightman et al. 76](#Wightman76)).

In [[causal perturbation theory]] the renormalization ambiguities are understood as the freedom of extending the [[time-ordered product]] of [[operator-valued distributions]] to the interaction points, in the sense of [[extension of distributions]]. The notorious "infinities that plague quantum field theory" arise only if this extension is not handled correctly and has to be fixed. Hence what historically is called "renormalization" could from a mathematical point of view just be called "normalization" (a point made vividly for instance in [[Finite Quantum Electrodynamics -- The Causal Approach|Scharf 95]], [[Quantum Gauge Theories -- A True Ghost Story|Scharf 01]]).

The _[[main theorem of perturbative renormalization theory]]_ states that any two choices of such (re-)normalizations are uniquely related by a re-definition of the [[interaction]] [[Lagrangian density]] which introduces further point interactions of higher order ("counter terms"),

The [[extension of distributions]] of the [[time-ordered product]] may naturally be organized via [[graphs]], the _[[Feynman graphs]]_ ([Garcia-Bondia & Lazzarini 00](#GarciaBondiaLazzarini00), [Keller 10, chapter IV](#Keller10)), and hence the renormalized perturbative [[S-matrix]] defining the [[perturbative quantum field theory]] is expressed as a [[formal power series]] in renormalized [[Feynman graphs]], the _[[Feynman perturbation series]]_ ([Keller 10 (IV.12)](#Keller10)).

Historically the [[Feynman perturbation series]] was motivated from intuition about the would-be [[path integral]], and this is still a popular point of view, albeit its lack of rigorous formulation. One may understand the axiomatics on the [[S-matrix]] in [[causal perturbation theory]] as defining the result of the path integral without actually doing an integration over field configurations.

But while [[path integral quantization]] for [[perturbative quantum field theory]] remains elusive, it has been shown that the (re-)normalized [[perturbative quantum field theory]] thus constructed via [[causal perturbation theory]] is, at least under favorable circumstances, equivalently the ([[Fedosov deformation quantization|Fedosov]]) [[formal deformation quantization]] of the [[covariant phase space]] induced by the given interacting [[Lagrangian density]] ([Collini 16](#Collini16)). This identifies the (re-)normalization freedom with the usual freedom in choosing [[formal deformation quantization]].

This also suggest that the construction of the full [[non-perturbative quantum field theory]] ought to be given by a [[strict deformation quantization]] of the [[covariant phase space]]. But presently no example of such for non-trivial interaction in [[spacetime]] [[dimension]] $\geq 4$ is known.
In particular the [[phenomenology|phenomenologically]] interesting case of a complete construction of interacting field theories on 4-dimensional spacetimes is presently unknown. For the case of [[Yang-Mills theory]] this open problem is one of the "Millenium Problems" (see at _[[quantization of Yang-Mills theory]]_).


## Definitions

There are different procedures of renormalization

1. [In causal perturbation theory (SBEG-renormalization)](#SBEG Renormalization)

1. [BPHZ and Hopf-Algebraic renormalization](#BPHZRenormalization)

1. [Of theories in BV-CS form](#OfTheoriesInBVForm)

### In causal perturbation theory (SBEG-renormalization)
 {#SBEG Renormalization}

> under construction

Based on [St&#252;ckelberg-Peterman-53](#StueckelbergPetermann53), [Bogoliubov-Shirkov 76](#BogoliubovShirkov76), developed by [Epstein-Glaser 73](#EpsteinGlaser73). Generalized to [[quantum field theory on curved spacetimes]] in [Brunetti-Fredenhagen 99](#BrunettiFredenhagen99).

See at _[[causal perturbation theory]]_
and _[[locally covariant perturbative quantum field theory]]_.

[[!include Feynman diagrams in causal perturbation theory -- summary]]

#### Free field vacua
 {#FreeFieldVacua}


In considering [[perturbative QFT]], we are considering [[perturbation theory]] in formal [[deformation]] parameters around a fixed [[free field theory|free]]
[[Lagrangian field theory|Lagrangian]] [[quantum field theory]] in a chosen [[Hadamard vacuum state]].

For convenient referencing we collect all the structure and notation that goes into this in the following definitions:

+-- {: .num_defn #VacuumFree}
###### Definition
**([[free field theory|free]] [[relativistic field theory|relativistic]] [[Lagrangian field theory|Lagrangian]] [[quantum field theory|quantum field]] [[vacuum]])**

Let

1. $\Sigma$ be a [[spacetime]] (e.g. [[Minkowski spacetime]]);

1. $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)), with [[field bundle]] $E \overset{fb}{\to} \Sigma$;

1. $\mathcal{G} \overset{fb}{\to} \Sigma$ a [[gauge parameter bundle]] for $(E,\mathbf{L})$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeParameters)), with induced [[BRST-complex|BRST]]-[[reduced phase space|reduced]] [[Lagrangian field theory]] $\left( E \times_\Sigma \mathcal{G}[1], \mathbf{L} - \mathbf{L}_{BRST}\right)$ ([this example](A+first+idea+of+quantum+field+theory#LocalOffShellBRSTComplex));

1. $(E_{\text{BV-BRST}}, \mathbf{L}' - \mathbf{L}'_{BRST})$ a [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) with [[graded manifold|graded]] [[BV-BRST formalism|BV-BRST]] [[field bundle]] $E_{\text{BV-BRST}} = T^\ast_{\Sigma}[-1]\left( E\times_\Sigma \mathcal{G}[1] \times_\Sigma A \times_\Sigma A[-1]\right)$ ([this remark](A+first+idea+of+quantum+field+theory#FieldBundleBVBRST));

1. $\Delta_H \in \Gamma'( E_{\text{BV-BRST}} \boxtimes E_{\text{BV-BRST}} )$ a [[Wightman propagator]] $\Delta_H = \tfrac{i}{2} \Delta + H$ compatible with the [[causal propagator]] $\Delta$ which corresponds to the [[Green hyperbolic partial differential equation|Green hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] induced by the [[gauge fixing|gauge-fixed]] [[Lagrangian density]] $\mathbf{L}'$.

Given this, we write

$$
  \left(
    {\, \atop \,}
    PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar] ] \;,\;
   \star_H
   {\, \atop \,}
  \right)
$$

for the corresponding [[Wick algebra]]-[[structure]] on [[formal power series]] in $\hbar$ ([[Planck's constant]]) of [[microcausal polynomial observables]]. This is a [[star algebra]] with respect to ([[coefficient]]-wise) [[complex conjugation]].

Write

$$
  \label{HadamardVacuumStateForFreeFieldTheory}
  \array{
    PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar] ]
     &\overset{\langle - \rangle}{\longrightarrow}&
    \mathbb{C}[ [\hbar] ]
    \\
    A &\mapsto& A(\Phi = 0)
  }
$$

for the induced [[Hadamard vacuum state]] ([this prop.](Wick+algebra#WickAlgebraCanonicalState)), hence the [[state on a star-algebra|state]] whose [[distribution|distributional]] [[2-point function]] is the chosen [[Wightman propagator]]:

$$
  \left\langle \mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y)\right\rangle
  \;=\;
  \hbar \, \Delta_H^{a b}(x,y)
  \,.
$$

Given any [[microcausal polynomial observable]] $A \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]$ then its value in this state is called its _free [[vacuum expectation value]]_

$$
  \left\langle
    A
  \right\rangle
  \;\in\;
  \mathbb{C}[ [ \hbar, g, j] ]
  \,.
$$

Write

$$
  \label{NormalOrderingLocalObservables}
  \array{
    LocObs(E_{\text{BV-BRST}})
      &\overset{\phantom{A}:(-):\phantom{A}}{\hookrightarrow}&
    PolyObs(E_{\text{BV-BRST}})_{mc}
    \\
    A &\mapsto& :A:
  }
$$

for the inclusion of [[local observables]] into [[microcausal polynomial observables]] ([this example](A+first+idea+of+quantum+field+theory#PointwiseProductsOfFieldObservablesAdiabaticallySwitchedIsMicrocausal)), thought of as forming [[normal-ordered products]] in the [[Wick algebra]] (by [this def.](A+first+idea+of+quantum+field+theory#NormalOrderedProductNotation)).

We denote the [[Wick algebra]]-product (the [[star product]] $\star_H$ induced by the [[Wightman propagator]] $\Delta_H$) by juxtaposition ([this def.](A+first+idea+of+quantum+field+theory#NormalOrderedProductNotation))

$$
  A_1 A_2 \;\coloneqq\; A_1 \star_H A_2
  \,.
$$

If an element $A \in PolyObs(E_{\text{BV-BRST}})$ has an [[inverse]] with respect to this product, we denote that by
$A^{-1}$:

$$
  A^{-1} A = 1
  \,.
$$

Finally, for $A \in LocObs(E_{\text{BV-BRST}})$ we write $supp(A) \subset \Sigma$ for its spacetime support ([this def.](A+first+idea+of+quantum+field+theory#SpacetimeSupport)).
For $S_1, S_2 \subset \Sigma$ two [[subsets]] of [[spacetime]] we write

$$
  S_1 {\vee\!\!\!\wedge} S_2
  \phantom{AAA}
  \left\{
    \array{
      "S_1 \, \text{does not intersect the past of} \, S_2"
      \\
      \Updownarrow
      \\
      "S_2 \, \text{does not intersect the future of} \, S_1"
    }
  \right.
$$

for the  [[causal ordering]]-[[relation]] and


$$
  S_1 {\gt\!\!\!\!\lt} S_2
  \phantom{AAA}
  \text{for}
  \phantom{AAA}
  \array{
    S_1 {\vee\!\!\!\wedge} S_2
    \\
    \text{and}
    \\
    S_2 {\vee\!\!\!\wedge} A_1
  }
$$

for _[[spacelike]] separation_.

=--

+-- {: .num_remark}
###### Remark

For the purposes of constructing or defining the Wick algebra, the conditions on $\Delta_H$ or $H$ could be relaxed. Requiring $\Delta_H$ to be an honest [[Wightman propagator]] means that it is a distribution satisfying the [[Hadamard distribution|Hadamard wavefront condition]], as well as addition positivity and normalization requirements. Dropping the positivity and some of the normalization requirements, $\Delta_H$ is then only a _Hadamard parametrix_ for the Wightman propagator. The construction of the Wick algebra with respect to $\Delta_H$ still makes sense, but $:(-):$ can no longer be interpreted as normal ordering with respect to a fixed vacuum state. In fact, in [[locally covariant pAQFT]], the property for $\Delta_H$ to be the Wightman propagator for a state is in conflict with local covariance. On the other hand, there is no problem with selecting a locally covariant Hadamard parametrix $\Delta_H$, which allows the construction or definition of the Wick algebra to be locally covariant.

=--


#### Inductive construction


+-- {: .num_prop #RenormalizationIsInductivelyExtensionToDiagonal}
###### Proposition
**([[renormalization|("re"-)normalization]] is [[induction|inductive]] [[extension of distributions]] to the [[diagonal]])**


Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}.

Assume that for $n \in \mathbb{N}$, [[time-ordered products]]
$\{T_{k}\}_{k \leq n}$ of arity $k \leq n$ have been constructed
in the sense of [this def.](S-matrix#TimeOrderedProduct).
Then the time-ordered product $T_{n+1}$ of arity $n+1$ is uniquely fixed on the [[complement]]

$$
  \Sigma^{n+1} \setminus diag(n)
  \;=\;
  \left\{
     (x_i \in \Sigma)_{i = 1}^n
     \;\vert\;
     \underset{i,j}{\exists} (x_i \neq x_j)
  \right\}
$$

of the [[image]] of the [[diagonal]] inclusion $\Sigma \overset{diag}{\longrightarrow} \Sigma^{n}$
(where we regarded $T_{n+1}$ as a [[generalized function]] on $\Sigma^{n+1}$ according to [this remark](S-matrix#NotationForTimeOrderedProductsAsGeneralizedFunctions)).

=--

This statement appears in ([Popineau-Stora 82](#PopineauStora82)), with (unpublished) details in ([Stora 93](#Stora93)), following personal communicatin by [[Henri Epstein]] (according to [Dütsch 18, footnote 57](#Duetsch18)). Following this, statement and detailed proof appeared in ([Brunetti-Fredenhagen 99](#BrunettiFredenhagen99)).


+-- {: .proof}
###### Proof

We will construct an [[open cover]] of $\Sigma^{n+1} \setminus \Sigma$ by subsets $\mathcal{C}_I \subset \Sigma^{n+1}$ which are [[disjoint unions]]
of [[inhabited set|non-empty]] sets that are in [[causal order]], so that by [[causal factorization]] the 
time-ordered products $T_{n+1}$ on these subsets are uniquely given by $T_{k}(-) \star_H T_{n-k}(-)$.
Then we show that these unique products on these special subsets do coincide on [[intersections]].
This yields the claim by a [[partition of unity]].

We now say this in detail:

For $I \subset \{1, \cdots, n+1\}$  write $\overline{I} \coloneqq \{1, \cdots, n+1\} \setminus I$.
For $I, \overline{I} \neq \emptyset$, define the subset

$$
  \mathcal{C}_I
  \;\coloneqq\;
  \left\{
    (x_i)_{i \in \{1, \cdots, n+1\}} \in \Sigma^{n+1}
    \;\vert\;
    \{x_i\}_{i \in I} {\vee\!\!\!\wedge} \{x_j\}_{j \in \{1, \cdots, n+1\} \setminus I}
  \right\}
  \;\subset\;
  \Sigma^{n+1}
  \,.
$$

Since the [[causal order]]-relation involves the [[closed future cones]]/[[closed past cones]], respectively, it is clear that these are [[open subsets]]. Moreover it is immediate that they form an [[open cover]] of the [[complement]] of the [[diagonal]]:

$$
  \underset{ { I \subset \{1, \cdots, n+1\} \atop { I, \overline{I} \neq \emptyset } }   }{\cup}
  \mathcal{C}_I
  \;=\;
  \Sigma^{n+1} \setminus diag(\Sigma)
  \,.
$$

(Because any two distinct points in the [[globally hyperbolic spacetime]] $\Sigma$ may be causally separated by a [[Cauchy surface]],
and any such may be deformed a little such as not to intersect any of a given finite set of points. )

Hence the condition of [[causal factorization]] on $T_{n+1}$ implies that 
[[restriction of distributions|restricted]] to any $\mathcal{C}_{I}$ these have to be given (in the condensed [[generalized function]]-notation from [this remark](S-matrix#NotationForTimeOrderedProductsAsGeneralizedFunctions)) on 
any unordered tuple $\mathbf{X} = \{x_1, \cdots, x_{n+1}\} \in \mathcal{C}_I$ with corresponding induced tuples
$\mathbf{I} \coloneqq \{x_i\}_{i \in I}$ and $\overline{\mathbf{I}} \coloneqq \{x_i\}_{i \in \overline{I}}$ by

$$
  \label{InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal}
  T_{n+1}( \mathbf{X} )
  \;=\;
  T(\mathbf{I}) T(\overline{\mathbf{I}})
  \phantom{AA}
  \text{for}
  \phantom{A}
  \mathcal{X} \in \mathcal{C}_I
  \,.
$$

This shows that $T_{n+1}$ is unique on $\Sigma^{n+1} \setminus diag(\Sigma)$ if it exists at all,
hence if these local identifications glue to a global definition of $T_{n+1}$. To see that this is the case, 
we have to consider any two such subsets

$$
  I_1, I_2 
  \subset
  \{1, \cdots, n+1\}
  \,,
  \phantom{AA}
  I_1, I_2, \overline{I_1}, \overline{I_2} \neq \emptyset
  \,.
$$

By definition this implies that for

$$
  \mathbf{X} \in \mathcal{C}_{I_1} \cap \mathcal{C}_{I_2}
$$

a tuple of spacetime points which decomposes into causal order with respect to both these subsets,
the corresponding mixed intersections of tuples  are spacelike separated:

$$
  \mathbf{I}_1 \cap \overline{\mathbf{I}_2}
    \;
    {\gt\!\!\!\!\lt}
    \;
  \overline{\mathbf{I}_1} \cap \mathbf{I}_2
  \,.
$$

By the assumption that the $\{T_k\}_{k \neq n}$ satisfy causal factorization, this implies that the corresponding
time-ordered products commute:

$$
  \label{TimeOrderedProductsOfMixedIntersectionsCommute}
  T(\mathbf{I}_1 \cap \overline{\mathbf{I}_2})
  \,
  T(\overline{\mathbf{I}_1} \cap \mathbf{I}_2)
  \;=\;
  T(\overline{\mathbf{I}_1} \cap \mathbf{I}_2)
  \,
  T(\mathbf{I}_1 \cap \overline{\mathbf{I}_2})
  \,.
$$

Using this we find that the identifications of $T_{n+1}$
on $\mathcal{C}_{I_1}$ and on $\mathcal{C}_{I_2}$, accrding to (eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal),
agree on the intersection: in that for $  \mathbf{X}  \in \mathcal{C}_{I_1} \cap \mathcal{C}_{I_2}$ we have

$$
  \begin{aligned}
    T( \mathbf{I}_1 ) T( \overline{\mathbf{I}_1} )
    & =
    T( \mathbf{I}_1 \cap \mathbf{I}_2 )
    T( \mathbf{I}_1 \cap \overline{\mathbf{I}_2} )
    \,
    T( \overline{\mathbf{I}_1} \cap \mathbf{I}_2 )
    T( \overline{\mathbf{I}_1} \cap \overline{\mathbf{I}_2} )
    \\
    & = 
    T( \mathbf{I}_1 \cap \mathbf{I}_2 )
    \underbrace{
    T( \overline{\mathbf{I}_1} \cap \mathbf{I}_2 )
    T( \mathbf{I}_1 \cap \overline{\mathbf{I}_2} )
    }
    T( \overline{\mathbf{I}_1} \cap \overline{\mathbf{I}_2} )
    \\
    & = 
    T( \mathbf{I}_2 )
    T( \overline{\mathbf{I}_2} )
  \end{aligned} 
$$

Here in the first step we expanded out the two factors using (eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal) for $I_2$,
then under the brace we used (eq:TimeOrderedProductsOfMixedIntersectionsCommute) and in the last step we used again
(eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal), but now for $I_1$.

To conclude, let

$$
  \left(
    \chi_I
    \in  
    C^\infty_{cp}(\Sigma^{n+1})    
  \right)_{ { I \subset \{1, \cdots, n+1\} } \atop { I, \overline{I} \neq \emptyset } }
$$

be a [[partition of unity]] subordinate to the [[open cover]] formed by the $\mathcal{C}_I$. Then the above implies that
setting for any $\mathbf{X} \in \Sigma^{n+1} \setminus diag(\Sigma)$

$$
  T_{n+1}(\mathbf{X})
  \;\coloneqq\;
  \underset{
    { I \in \{1, \cdots, n+1\} }
    \atop
    { I, \overline{I} \neq \emptyset }
  }{\sum}
  \chi_i(\mathbf{X}) T( \mathbf{I} ) T( \overline{\mathbf{I}} )
$$

is well defined and satisfies causal factorization.




=--



#### Main theorem of perturbative renormalization

* [[main theorem of perturbative renormalization theory]]


### BPHZ and Hopf-algebraic renormalization
 {#BPHZRenormalization}

#### The phenomenon

In the study of [[perturbative quantum field theory]] one is concerned with functions -- called _amplitudes_ -- that take a collection of graphs -- called [[Feynman graph]]s -- to [[Laurent polynomial]]s in a complex variable $z$ -- called the **(dimensional) [[regularization (physics)|regularization]] parameter** --

$$
  Amplitude : CertainGraphs \to LaurentPolynomials
$$

and wishes to extract a "meaningful" finite component when evaluated at vanishing regularization parameter $z = 0$.

A prescription -- called **renormalization scheme** -- for adding to a given amplitude in a certain recursive fashion further terms -- called **counterterms** -- such that the resulting modified amplitude -- called the **renormalized amplitude** -- is finite at $z=0$ was once given by physicists  and is called the **BPHZ-procedure** .

This procedure justifies itself mainly through the remarkable fact that the numbers obtained from it match certain numbers measured in particle accelerators to fantastic accuracy.

#### Its combinatorial Hopf-algebraic interpretation

The combinatorial Hopf algebraic approach to perturbative quantum field theory, see for instance

* Hector Figueroa, [[Jose Gracia-Bondia]], _Combinatorial Hopf algebras in quantum field theory I_ ([arXiv](http://arxiv.org/abs/hep-th/0408145)),

starts with the observation that the BPHZ-procedure can be understood

* by noticing that there is secretly a natural [[group]] structure on the collection of amplitudes;

* which is induced from the fact that there is secretly a natural [[Hopf algebra]] structure on the vector space whose basis consists of graphs;

* and with respect to which the BPHZ-procedure is simply the [[Birkhoff decomposition]] of group valued functions on the circle into a divergent and a finite part.

The Hopf algebra structure on the vector space whose basis consists of graphs can be understood most conceptually in terms of [[pre-Lie algebra|pre-Lie algebras]].

#### The Connes-Kreimer theorem

A [[Birkhoff decomposition]] of a loop $\phi : S^1 \to G$ in a complex group $G$ is a continuation of the loop to

* a [[holomorphic function]] $\phi_+$ on the standard disk inside the circle;

* a holomorphic function $\phi_-$ on the complement of this disk in the projective [[complex plane]]

* such that on the unit circle the original loop is reproduced as

  $$
    \phi = \phi_+ \cdot (\phi_-)^{-1}
    \,,
  $$

  with the product and the inverse on the right taken in the group $G$.

  Notice that by the assumption of holomorphicity $\phi_+(0)$ is a well defined element of $G$.



+-- {: .num_theorem}
###### Theorem
**(Connes-Kreimer)**

1. If $G$ is the group of [[character]]s on any graded connected commutative [[Hopf algebra]] $H$

   $$
    G = Hom(H,\mathbb{C})
   $$

   then the Birkhoff decomposition always exists and is given by the formula

   $$
    \phi_- :  (X \in H) \mapsto Counit(X)
          -
        PolePartOf(
             Product(\phi_- \otimes \phi)
            \circ (1 \otimes (1 - Counit))
         \circ Coproduct (X)
        )
    \,.
   $$

1. There is naturally the structure of a [[Hopf algebra]], $H = Graphs$, on the graphs considered in [[quantum field theory]]. As an algebra this is the free commutative algebra on the "1-particle irreducible graphs". Hence QFT amplitudes can be regarded as characters on this Hopf algebra.



1. The BPHZ renormalization-procedure for amplitudes is nothing but the first item applied to the special case of the second item.

=--

+-- {: .proof}
###### Proof

The proof is given in

* [[Alain Connes]], [[Dirk Kreimer]], _Renormalization in quantum field theory I_ ([arXiv](http://arxiv.org/abs/hep-th/9912092))

=--



#### The Hopf-algebra perspective on QFT

This result first of all makes [[Hopf algebra]] an organizational principle for (re-)expressing familiar operations in [[quantum field theory]].

Computing the renormalization $\phi_+$ of an amplitude $\phi$ amounts to using the above formula to compute the counterterm $\phi_-$ and then evaluating the right hand side of

$$
  \underbrace{\phi_+}_{renormalized amplitude} = \underbrace{\phi}_{amplitude} \underbrace{\cdot}_{convolution product} \underbrace{\phi_-}_{counterterm}
  \,,
$$

where the product is the group product on characters, hence the [[convolution product]] of characters.

Every elegant reformulation has in it the potential of going beyond mere reformulation by allowing to see structures invisible in a less natural formulation. For instance [[Dirk Kreimer]] [claims](http://golem.ph.utexas.edu/category/2007/03/recent_developments_in_quantum.html#c010903) that the Hopf algebra language allows him to see patterns in perturbative quantum gravity previously missed.

#### Gauge theory and BV-BRST with Hopf algebra

Walter von Suijlekom is thinking about the Hopf-algebraic formulation of [[BV theory|BRST-BV methods]] in nonabelian [[gauge theory]]

In his nicely readable

* [[Walter von Suijlekom]], _Renormalization of gauge fields using Hopf algebra_, ([arXiv](http://arxiv.org/abs/0801.3170))

he reviews the central idea: the [[BRST]] formulation of [[Yang-Mills theory]] manifests itself at the level of the resulting _bare_ i.e. unnormalized amplitudes in certain relations satisfied by these, the **Slavnov-Taylor identities** .

Renormalization of gauge theories is consistent only if these relations are still respected by renormalized amplitudes, too. We can reformulate this in terms of Hopf algebra now:

the relations between amplitudes to be preserved under renormalization must define a [[Hopf ideal]] in the Hopf algebra of graphs.

Walter von Suijlekom proves this to be the case for Slavnov-Taylor in his [theorem 9 on p. 12](http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3170v1.pdf#page=12)

As a payoff, he obtains a very transparent way to prove the generalization of **Dyson's formula** to nonabelian gauge theory, which expresses renormalized Green's functions in terms of unrenormalized Green's functions "at bare coupling". This is his [corollary 12 on p. 13](http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3170v1.pdf#page=12).

In the context of [[BV theory|BRST-BV quantization]] these statements are subsumed, he says, by the structure encoded in the Hopf ideal which corresponds to imposing the BV-master equation.  See also ([Suijlekom](#Suijlekom)).


### Lattice renormalization

* [[lattice renormalization]]

### Of theories in BV-CS form
 {#OfTheoriesInBVForm}

In ([Costello 07](#Costello)) a comparatively simple renormalization procedure is given that applies to [[theory (physics)|theories]] that are given by [[action functionals]] which can be given in the form

$$
  S(\phi)
  =
  \langle \phi , Q \phi \rangle
  +
  I(\phi)
$$

where

1. the [[field (physics)|fields]] $\phi$ are sections of a graded [[field bundle]] $E$ on which $Q$ is a [[differential]], $\langle -,-\rangle$ a compatible [[antibracket]] pairing such that $(E,Q, \langle \rangle)$ is a [[free field theory]] (as discussed there) in [[BV-BRST formalism]];

1. $I$ is an [[interaction]] that is at least cubic.

These are action functionals that are well adapted to [[BV-BRST formalism]] and for which there is a [[quantization]] to a [[factorization algebra of observables]].

Most of the fundamental [[theory (physics)|theories]] in [[physics]] are of this form, notably [[Yang-Mills theory]]. In particular also all theories of [[schreiber:infinity-Chern-Simons theory]]-type coming from binary [[invariant polynomials]] are perturbatively of this form, notably ordinary 3d [[Chern-Simons theory]].

For a discussion of just the simple special case of 3d CS see ([Costello 11, chapter 5.4 and 5.14](#Costello11)).

For comparison of the following with other renormalization schemes, see at ([Costello 07, section 1.7](#Costello)).

1. [The setup](#TheSetup)

1. [Operator (heat) kernels and propagators](#OperatorKernelsAndPropagators)

1. [The renormalization group operator](#TheRenormalizationGroupOperator)

1. [The path integral](#ThePathIntegral)

1. [Renormalized action](#RenormalizedAction)

1. [Renormalization](#Renormalization)

#### The setup
 {#TheSetup}

+-- {: .num_defn }
###### Definition

A **[[free field theory]]** $(E, \langle, -,-\rangle. Q)$:

**[[kinematics]]**:

* A [[smooth manifold]] $X$ ("[[spacetime]]"/"[[worldvolume]]");

* a $\mathbb{Z}$-[[graded object|graded]] [[complex numbers|complex]] [[vector bundle]] $E \to X$ (the "[[field bundle]]" containing also in general [[antifields]] and [[ghosts]]);

* equipped with a [[bundle]] [[homomorphism]] (the "[[antibracket]] [[density]]")

  $$
    \langle -,-\rangle_{loc} \;\colon\; E \times E \to Dens_X
  $$

  from the fiberwise [[tensor product]] of $E$ with itself to the compex [[density bundle]] which is fiberwise

  * non-degenerate

  * anti-symmetric

  * of degree -1

Write $\mathcal{E}_c \coloneqq \Gamma_{cp}(E)$ for the space of [[sections]] of the [[field bundle]] of [[compact support]]. Write

$$
  \langle -,-\rangle
  \;\colon\;
  \mathcal{E}_c
  \otimes
  \mathcal{E}_c
  \to
  \mathbb{C}
$$

for the induced pairing on sections

$$
  \langle \phi, \psi\rangle
  =
  \int_{x \in X} \langle \phi(x), \psi(x)\rangle_{loc}
  \,.
$$

The paring being non-degenerate means that we have an [[isomorphism]] $E \stackrel{\simeq}{\to} E^* \otimes Dens_X$ and we write

$$
  E^! \coloneqq E^* \otimes Dens_X
  \,.
$$

**[[dynamics]]**

* A [[differential operator]] on sections of the [[field bundle]]

  $$
    Q \;\colon\; \mathcal{E} \to \mathcal{C}
  $$

  of degree 1 such that

  1. $(\mathcal{E}, Q)$ is an [[elliptic complex]];

  1. $Q$ is [[self-adjoint operator|self-adjoint]] with respect to $\langle -,-\rangle$ in that for all [[field (physics)|fields]] $\phi,\psi \in \mathcal{E}_c$ of homogeneous degree we have $\langle \phi , Q \psi\rangle = (-1)^{{\vert \phi\vert}} \langle Q \phi, \psi\rangle$.

From this data we obtain:

* The [[action functional]] $S \colon \mathcal{E}_c \to \mathbb{C}$ of this corresponding free field theory is

  $$
    S \;\colon\; \phi \mapsto \int_X \langle \phi, Q \phi\rangle
    \,.
  $$

* The [[classical BV-complex]] is the [[symmetric algebra]] $Sym  \mathcal{E}^!$ of sections of $E^!$ equipped with the induced action of the differential $Q$ and the pairing

  $$
    \{\alpha,\beta\} \coloneqq  \int_{x \in X} \langle \alpha(x), \beta(x)\rangle
    \,.
  $$


=--

+-- {: .num_defn }
###### Definition

An **[[interaction]]** term $I \in \cdots$

(...)

=--

+-- {: .num_defn #LaplaceOperatorFromGaugeFixing}
###### Definition

A **[[gauge fixing operator]]** $Q^{GF}$ such that

$$
  H \coloneqq [Q, Q^{GF}]
$$

is a [[generalized Laplace operator]].

=--

#### Operator (heat) kernels and propagators
 {#OperatorKernelsAndPropagators}

+-- {: .num_defn #ConvolutionOfOperatorKernel}
###### Definition

For $K = \sum K' \otimes K'' \in \mathcal{E} \otimes \mathcal{E}$ the corresponding **convolution operator** $K \star \colon \mathcal{E} \to \mathcal{E}$ is

$$
  K \star e  = (-1)^{\vert e\vert} \sum K' \otimes \langle K'', e\rangle
  \,.
$$

=--

+-- {: .num_defn #HeatKernel}
###### Definition


For $H \colon \mathcal{E} \to \mathcal{E}$ a [[linear operator]], a **[[heat kernel]]** for it is a [[function]] $K_{(-)} \colon \mathbb{R}_{\gt 0} \to \mathcal{E}\otimes \mathcal{E}$ such that for each $t \in \mathbb{R}_{\gt 0}$ the convolution with $K_t$, def. \ref{ConvolutionOfOperatorKernel}, reproduces the exponential of $t\cdotH$:

$$
  K_t \star = \exp(-t H) \;\;\;\;\; \forall t \in \mathbb{R}_{\gt 0}
  \,.
$$

=--

+-- {: .num_prop #UniquenessOfHeatKernel}
###### Proposition

For $H$ a [[generalized Laplace operator]] such as the $[Q,Q^{GF}]$ of def. \ref{LaplaceOperatorFromGaugeFixing} there is a unique [[heat kernel]] which is moreover a [[smooth function]] of $t$.

=--

+-- {: .num_defn #DifferentialOperatorByKernel}
###### Definition

For $\phi =  \sum \phi' \otimes \phi'' \in Sym^2 \mathcal{E}$ write

$$
  \partial_{\phi}
  \coloneqq
  \frac{1}{2}
  \sum \partial_{\phi''} \partial_{\phi'}
  \,.
$$

=--

This is ([Costello 07, p. 32](#Costello)).

+-- {: .num_prop }
###### Proposition

$$
  [\partial_\phi, Q] = \partial_{Q \phi}
  \,.
$$

=--

#### The renormalization group operator
 {#TheRenormalizationGroupOperator}

+-- {: .num_defn}
###### Definition

For $Q^{GF}$ the [[gauge fixing operator]] of def. \ref{LaplaceOperatorFromGaugeFixing}, and $K_t$ the [[heat kernel]] of the corresponding [[generalized Laplace operator]] $H = [Q, Q^{GF}]$ by prop. \ref{UniquenessOfHeatKernel}, write for $\epsilon, T \in \mathbb{R}_{\gt 0}$

$$
  P(\epsilon, T)
  \coloneqq
  \int_{\epsilon}^T
  (Q^{GF} \otimes 1)
  K_t \; d t
  \;\;\;\;\;
  \in \mathcal{E} \otimes \mathcal{E}\,.
$$

=--

([Costello 07, p. 33](#Costello))

+-- {: .num_defn #RenormalizationOperator}
###### Definition

Write

$$
  \Gamma(P(\epsilon,T), S)
  \coloneqq
  \hbar log
  \left(
   \exp\left(\hbar \partial_{P(\epsilon,T)}\right)
   \exp\left(I/\hbar\right)
  \right)
  \;\;
  \in \mathcal{O}(\mathcal{E}, \mathbb{C}[ [ \hbar ] ])
  \,,
$$

where $\partial_{\cdots}$ is given by def. \ref{DifferentialOperatorByKernel}.

=--

([Costello 07, def. 6.6.1](#Costello))

#### The path integral
 {#ThePathIntegral}

+-- {: .num_prop #PathIntegralByLimitInDimension0}
###### Proposition

If $X = *$ is the [[point]], then the [[path integral]] over the [[action functional]] exists as an ordinary [[integral]] and is equal to

$$
  \hbar log
  \int_{x \in (Im Q^{GF})_{\mathbb{R}}}
  \exp\left(
    \tfrac{1}{2} \langle x, Q x\rangle
    +
    I(x + a) d \mu
  \right)
  =
  \Gamma(P(0,\infty), I)(a)
$$

=--

This is ([Costello 07, lemma 6.6.2](#Costello)).

+-- {: .num_remark}
###### Remark

For $X$ of positive [[dimension]], the [[limit]]


$$
  \underset{\epsilon \to 0}{\lim}
  \Gamma(P(\epsilon,\infty), I)(a)
$$

does not in general exist. Renormalization is the process of adding $\hbar$-corrections to the action -- the [[counterterms]] -- such as to make it exist after all. In this case we may regard the limit, by prop. \ref{PathIntegralByLimitInDimension0}, as the _definition_ of the [[path integral]].

=--

#### Renormalized action
 {#RenormalizedAction}

+-- {: .num_defn #RenormalizedActionAndCounterterms}
###### Definition

Given the [[action functional]] $S \colon \phi \mapsto \frac{1}{2}\langle \phi, Q phi\rangle + I(\phi)$, a **renormalization** is a [[power series]]

$$
  I^R(\hbar, \epsilon)
  =
  I(\hbar)
  -
  \underset{{i \gt 0} \atop  { k \geq k}}{\sum}
  \hbar^i I^{CT}_{i,k}(\epsilon)
$$

such that the [[limit]]

$$
  \underset{\epsilon \to 0}{\lim}
  \Gamma(P(\epsilon,T), I^R(\epsilon))
  \,,
$$

by def. \ref{RenormalizationOperator}, exists.

=--

The $I^{CT}_{i,k}$ are called the _[[counterterms]]_.

#### Renormalization
 {#Renormalization}

+-- {: .num_defn #RenormalizationScheme}
###### Definition

A [[renormalization scheme]] is a decomposition of functions $\mathcal{A}$ on $(0,1)$, as a [[vector space]], into a [[direct sum]]

$$
  \mathcal{A} \simeq \mathcal{A}_{\geq 0} \oplus \mathcal{A}_{\gt 0}
$$

such that the functions $f \in \mathcal{A}_{\geq 0}$ are non-singular in that $\underset{\epsilon \to 0}{\lim} f(\epsilon)$ exists.

=--

Hence this is a choice of picking the [[singularities]] in functions that are not necessarily defined at $\epsilon = 0$.

+-- {: .num_theorem}
###### Theorem

Given any choice of [[renormalization scheme]], def. \ref{RenormalizationScheme}, there exists a unique choice of [[counterterms]] $\{I^{CT}_{k,i}\}$, def. \ref{RenormalizedActionAndCounterterms} such that

* each counterterm is in the chosen $\mathcal{A}_{\gt 0}$ as a function of $\epsilon$;

* for $k \gt 0$ the [[germ]] of a counterterm at $x \in X$ depends only on the [[germ]] of the given field theory data $(E, Q, Q^{GF})$ at that point.

=--

This is ([Costello 07, theorem B, p. 38](#Costello)).

+-- {: .num_defn}
###### Definition

Given a renormalization $I^{R}$, write for all $T \in \mathbb{R}_{\ht 0}$

$$
  \Gamma^R(P(0,T), I)
  \coloneqq
  \underset{\epsilon \to 0}{\to}
  \Gamma(P(\epsilon, R), I - I^{CT}(\epsilon))
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

We think of $\Gamma^R(P(0,T), I)$ as the renormalized [[effective action]] of the original action at [[scale]] $T$.

=--

+-- {: .num_prop}
###### Proposition

The [[renormalization group flow]]

$$
  \Gamma^R(P(0,T'), I)
  =
  \Gamma(P(T,T'), \; \Gamma^R(P(0,T), I ))
$$

holds.

=--

([Costello 07, lemma 9.0.6](#Costellon)).




## Related concepts

* [[renormalization group]], [[renormalization group flow]]

* [[renormalization scheme]]

* [[renormalon]]

* [[regularization (physics)]]

* [[perturbation theory]]

* [[BV quantization]]

* [[gauge fixing]], [[Gribov ambiguity]]

* [[cosmic Galois group]]



## References
 {#References}

After the original informal suggestions by [[Schwinger-Tomonaga-Feynman-Dyson]]

* {#Dyson49} [[Freeman Dyson]], _The raditation theories of Tomonaga, Schwinger and Feynman_, Phys. Rev. 75, 486, 1949 ([pdf](http://web.ihep.su/dbserv/compas/src/dyson49b/eng.pdf))

the mathematics of renormalization was finally understood and summarized in the 1975 Erice Majorana School:

* {#Wightman76} G. Velo and [[Arthur Wightman]] (eds.) _Renormalization Theory_ Proceedings of the 1975 Erice summer school, NATO ASI Series C 23, D. Reidel, Dordrecht, 1976

which included [[causal perturbation theory]], [[BPHZ renormalization]], proof of the [[forest formula]] and the [[BRST complex]] method for [[gauge theory]].

Little advancement happened until the identification of [[Hopf algebra]] structure in the [[forest formula]] due to

* {#Kreimer97} [[Dirk Kreimer]], _On the Hopf algebra structure of perturbative quantum field theories_, Adv. Theor. Math. Phys. 2 , 303 (1998) ([q-alg/9707029](https://arxiv.org/abs/q-alg/9707029))

This finally triggered the formulation of [[causal perturbation theory]] in terms of [[Feynman diagrams]] in

* {#GarciaBondiaLazzarini00} [[Jose Gracia-Bondia]], S. Lazzarini, _Connes-Kreimer-Epstein-Glaser Renormalization_ ([arXiv:hep-th/0006106](https://arxiv.org/abs/hep-th/0006106))

* {#Keller10} [[Kai Keller]], chapter IV of _Dimensional Regularization in Position Space and a Forest Formula for Regularized Epstein-Glaser Renormalization_, PhD thesis ([arXxiv:1006.2148](https://arxiv.org/abs/1006.2148))

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], [[Kai Keller]], [[Katarzyna Rejzner]], _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy.
55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))

Thus the original "dark art" of the construction of [[perturbative quantum field theory]] via renormalization finds a complete rigorous formulation.

In

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

it is shown that (at least under favorable circumstances) the construction of [[perturbative quantum field theory]] via [[causal perturbation theory]] is equivalently [[Fedosov deformation quantization]] of the given interacting [[Lagrangian density]], thus identifying the renormalization freedom with the Freedom in choosing a [[deformation quantization]].


### Review
 {#General}

A textbook account of [[renormalization|("re"-)normalization]] in [[causal perturbation theory]] is in

* {#Duetsch18} [[Michael Dütsch]], chapters 3 and 4 of _[[From classical field theory to perturbative quantum field theory]]_, 2018

Informal introductions include

* G. Peter Lepage, _What is Renormalization?_, talk 1989 ([arXiv:hep-ph/0506330](http://arxiv.org/abs/hep-ph/0506330))

* {#Weinberg09} [[Steven Weinberg]], _Effective Field Theory, Past and Future_ ([arXiv:0908.1964](http://arxiv.org/abs/0908.1964))

* [[R. E. Borcherds]], _Renormalization and quantum field theory_, ([arxiv/1008.0129](http://arxiv.org/abs/1008.0129))

* [[Arnold Neumaier]], _Renormalizatin without infinities -- an elementary tutorial_ ([pdf](http://www.mat.univie.ac.at/~neum/ms/ren.pdf))


### In causal perturbation theory

The concept of renormalization in [[causal perturbation theory]] via [[splittig of distributions]] was establied in

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211.

following precursors in

* {#StueckelbergPetermann53} [[Ernst Stückelberg]], A. Peterman, , _La normalisation des constants dans la theorie des quanta_ Helv. Phys. Acta 26, 499 (1953); and earlier references therein

  (see also _[[Stückelberg-Petermann renormalization group]]_)

* {#BogoliubovShirkov76} Bogoliubov, N. N., and Shirkov, D. V., _Introduction to the Theory of Quantized Fiels_, New York: John Wiley and Sons, 1976, 3rd edition

Further observations made in

* {#PopineauStora82} G. Popineau and [[Raymond Stora]], _A pedagogical remark on the main theorem of perturbative renormalization theory_, Nucl. Phys. B 912 (2016), 70–78, preprint: LAPP–TH, Lyon (1982).

* {#Stora93} [[Raymond Stora]], _Differential algebras in Lagrangean field theory_, Lectures at ETH, Zürich, 1993, unpublished

led to the equivalent formulation in [[pAQFT]] in terms of [[extension of distributions]] due to

* {#BrunettiFredenhagen99} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_  Commun.Math.Phys.208:623-661 (2000) ([arXiv](http://arxiv.org/abs/math-ph/9903028))

* [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_ Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))

Exposition includes

* [[Arnold Neumaier]], _Renormalization without infinities -- a tutorial_ ([pdf](http://www.mat.univie.ac.at/~neum/ms/ren.pdf))

* {#Brouder10} [[Christian Brouder]], _Multiplication of distributions_, 2010 ([[BrouderProductOfDistributions.pdf:file]])

For more see at _[perturbation theory -- In AQFT](perturbation+theory#ReferencesInAQFT)_.


Applications to the renoamrliaztion of [[Yang-Mills theory]] on curved [[background field|background]] [[spacetimes]] is accomplished in

* {#Hollands07} [[Stefan Hollands]], _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev.Math.Phys.20:1033-1172,2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))


### BPHZ Renormalization

BPHZ renormalization was introduced in particular in

* [[Klaus Hepp]], _Th&#233;orie de la Renormalisation_ Lect. Notes in Phys. Springer (1969)


Review includes

* Klaus Sibold, _Bogoliubov-Parasiuk-Hepp-Zimmermann renormalization scheme_, Scholarpedia, 5(5):7306. [doi:10.4249/scholarpedia.7306](http://dx.doi.org/10.4249/scholarpedia.7306)

* [[Alain Connes]], [[Matilde Marcolli]] _[[Noncommutative Geometry, Quantum Fields and Motives]]_

The original articles on this are

* [[Alain Connes]], [[Dirk Kreimer]], _Renormalization in quantum field theory and the Riemann-Hilbert problem. I. The Hopf algebra structure of graphs and the main theorem_, Comm. Math. Phys. __210__ (2000), no. 1, 249&#8211;273, [hep-th/9912092](http://arxiv.org/abs/hep-th/9912092), [MR2002f:81070](http://www.ams.org/mathscinet-getitem?mr=1748177), [doi](http://dx.doi.org/10.1007/s002200050779), _II. The $\beta$-function, diffeomorphisms and the renormalization group_, Comm. Math. Phys. __216__ (2001), no. 1, 215--241; [hep-th/0003188](http://arxiv.org/abs/hep-th/0003188), [MR2002f:81071](http://www.ams.org/mathscinet-getitem?mr=1748177), [doi](http://dx.doi.org/10.1007/PL00005547)

An introduction and review to the Hopf-algebraic description of renormalization is in

* Christian Brouder, _Quantum field theory meets Hopf algebra_ ([arxiv:hep-th/0611153](http://de.arxiv.org/abs/hep-th/0611153))

A textbook treatment is

* [[Dirk Kreimer]], _Knots and Fenyman diagrams_ , Cambridge Lecture Notes in Physics. 13. Cambridge: Cambridge University Press.
* Joseph C. Varilly, _The interface of noncommutative geometry and physics_, [hep-th/0206007](http://arxiv.org/abs/hep-th/0206007)

Some heavywheight automated computations using this formalism are discussed in

* D. J. Broadhurst, [[Dirk Kreimer]], _Renormalization automated by Hopf algebra_ ([arXiv:hep-th/9810087](http://arxiv.org/abs/hep-th/9810087))

See also

* W. van Suijlekom, _Representing Feynman graphs on BV-algebras_ , ([arXiv](http://arxiv.org/abs/0807.0999))
 {#Suijlekom}

* [[Dirk Kreimer]], Karen Yeats, _Diffeomorphisms of quantum fields_, [arxiv/1610.01837](https://arxiv.org/abs/1610.01837)


### In BV formalism
 {#ReferencesInBVFormalism}

Discussion of renormalization in the context of [[BV-BRST formalism]] is for [[relativistic field theory]] in the rigorous framework of [[causal perturbation theory]]/[[perturbative AQFT]] due to

* {#FredenhagenRejzner11a} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_, Commun. Math. Phys. 314(1), 93&#8211;127 (2012) ([arXiv:1101.5112](https://arxiv.org/abs/1101.5112))

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))

* {#Rejzner11} [[Katarzyna Rejzner]], _Batalin-Vilkovisky formalism in locally covariant field theory_ ([arXiv:1111.5130](https://arxiv.org/abs/1111.5130))

* {#Rejzner13} [[Katarzyna Rejzner]], _Remarks on local symmetry invariance in perturbative algebraic quantum field theory_ ([arXiv:1301.7037](https://arxiv.org/abs/1301.7037))

and surveyed in

* {#Rejzner16} [[Kasia Rejzner]], section 7 of _Perturbative algebraic quantum field theory_ Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

Discussion for [[Euclidean field theory]] is in

* {#Costello11} [[Kevin Costello]], _[[Renormalization and Effective Field Theory]]_ AMS (2011) ([publisher webpage](http://www.ams.org/publications/authors/books/postpub/surv-170))

building on

* {#Costello} [[Kevin Costello]], _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv:0706.1533](http://arxiv.org/abs/0706.1533))


See also at _[[factorization algebra of observables]]_.

A vaguely related approach earlier appeared in

* {#Tamarkin} [[Dmitry Tamarkin]], _A formalism for the renormalization procedure_ ([arXiv:math/0312219](http://arxiv.org/abs/math/0312219))





### Operadic description

* [[Jean-Louis Loday]], Nikolay M. Nikolov, _Operadic construction of the renormalization group_ ([arXiv:1202.1206](http://arxiv.org/abs/1202.1206))

### Relations to motives, polylogarithms, positivity

* [[Alexander Goncharov]], Marcus Spradlin, C. Vergu, Anastasia Volovich, _Classical polylogarithms for amplitudes and Wilson loops_,  Phys.Rev.Lett.105:151605,2010 [arxiv/1006.5703](http://arxiv.org/abs/1006.5703)

* [[Nima Arkani-Hamed]], Jacob L. Bourjaily, Freddy Cachazo, [[Alexander Goncharov]], Alexander Postnikov, Jaroslav Trnka, _Scattering amplitudes and the positive Grassmannian_, [arxiv/1212.5605](http://arxiv.org/abs/1212.5605)

* [[Spencer Bloch]], [[Hélène Esnault]], [[Dirk Kreimer]], _On motives associated to graph polynomials_, Commun.Math.Phys. __267__ (2006) 181-225 [math.AG/0510011](http://arxiv.org/abs/math/0510011) [doi](http:&&dx.doi.org/10.1007/s00220-006-0040-2)


[[!redirects renormalizable]]
[[!redirects renormalizable theory]]

[[!redirects BPHZ renormalization]]

[[!redirects Hopf-algebraic renormalization]]

[[!redirects Hopf algebra renormalization]] 