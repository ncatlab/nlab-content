
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Enveloping von Neumann algebras
* table of contents
{: toc}

## Definitions

Let $A$ be a $C^*$-[[C-star algebra|algebra]].  We may define its _enveloping [[von Neumann algebra]]_ in a few different but equivalent ways.

+-- {: .num_defn #adjunction}
###### Definition

The __enveloping von Neumann algebra__ $E(A)$ of $A$ is the [[free object|free]] von Neumann algebra on $A$.  That is, we have an [[adjoint functors|adjunction]]
$$ W^* Alg \overset{E}\underset{U}\leftrightharpoons C^* Alg ,$$
where $W^* Alg$ is the category of von Neumann algebras (which are $C^*$-algebras with [[preduals]]) and von Neumann algebra [[homomorphisms]] (which are $C^*$-algebra homomorphisms with preduals), $C^* Alg$ is the category of $C^*$-algebras and $C^*$-algebra homomorphisms, $U$ is the [[forgetful functor]] or [[inclusion functor]], and $E$ is the [[functor]] that we wish to define.
=--

Definition \ref{adjunction} defines [[the]] functor $E$ up to unique [[natural isomorphism]], if it exists.  We may prove that it exists by the [[adjoint functor theorem]] or by proving that one of the explicit constructions below satisfies the relevant [[universal property]].

+-- {: .num_defn #concrete}
###### Definition

Consider the [[direct sum]] of the the [[GNS representation]]s of the [[positive functional|positive]] linear functionals on $A$; this is a [[Hilbert space]] $H$ and [[representation]] $\pi : A \to B(H)$, the a [[universal representation of a C-star algebra|universal representation]] of $A$.  The [[image]] $\pi(A)$ is a [[linear subspace|subspace]] of $B(H)$; consider its [[double commutant]] (or equivalently its [[topological closure|closure]] in the [[weak operator topology]]) $A''$.  Ignoring the representation of $A''$ on $H$, $A''$ is a von Neumann algebra, the __enveloping von Neumann algebra__ of $A$.
=--

To obtain an [[adjoint functors|adjunction]] from Definition \ref{concrete}, we need also the [[unit of the adjunction]], which is the map
$$ A \to \pi(A) \to Cl_{wk^*}(\pi(A)) = A'' .$$

+-- {: .num_defn #doubledual}
###### Definition

Think of $A$ as a [[Banach space]], and consider its [[double dual]] $A^{**}$.  We have (as with any Banach space) a [[short linear map]] $i\colon A \to A^{**}$, so that $i(A)$ has the structure of a $C^*$-algebra.  Since $i(A)$ is weak-$*$-[[dense subspace|dense]] in $A^{**}$ and the $C^*$-algebraic operations are [[continuous map|continuous]], they extend to $A^{**}$. These extensions turn $A^{**}$ into a [[Banach algebra]]; the $C^*$ identity also extends, making $A^{**}$ into $C^*$-algebra.  Since $A^{**}$ has $A^*$ as a [[predual]], it is a von Neumann algebra, the __enveloping von Neumann algebra__ of $A$.
=--

Here, the [[unit of the adjunction]] is simply $i$.
The counit of the adjunction is given by a similar procedure: for every $W^*$-algebra $M$ with predual $M_{*}$ we can combine the bidual of the canonical embedding $M_{*} \to (M_{*})^{**}$ with the isomorphism $(M_{*})^{*} \to M$ to provide a norm 1 projection $M^{**} \to M$.
This can be shown to be a unital normal $*$-homomorphism.

The claim that the definitions above are all equivalent is the __Sherman&#8211;Takeda theorem__, due (naturally enough) to [Sherman (1950)](#Sherman1950) and [Takeda (1954)](#Takeda1954).


## Properties

A $C^*$-algebra and its enveloping von Neumann algebra rarely have the same [[spectrum]]. For example, consider the $C^*$-algebra $A=C_{0}(\mathbb{N})$, where $\mathbb{N}$ is given the discrete topology. Then, the von Neumann enveloping algebra of $A$ is the set of all bounded sequences, whose spectrum is homeomorphic to the Stone-Čech compactification of $\mathbb{N}$.

The [[functional calculus]] on a $C^*$-algebra (which treats [[continuous functions]]) extends to the functional calculus on its enveloping von Neumann algebra (which treats [[measurable functions]]).  In particular, we can apply a measurable function to an element of a $C^*$-algebra to obtain an element of its enveloping von Neumann algebra.


## Applications

Some abstract treatments of [[quantum mechanics]] use $C^*$-algebras, while others use von Neumann algebras.  If a [[physical system]] is described by a $C^*$-algebra in the first case, then it may described by its enveloping von Neumann algebra in the second case.


## References

* S. Sherman (1950). The second adjoint of a C* algebra. _Proceedings of the International Congress of Mathematicians_ 1950 (1): 470. American Mathematical Society.
  {#Sherman1950}

* Zir&#244; Takeda (1954). Conjugate spaces of operator algebras. _Proceedings of the Japan Academy_ 30 (2): 90&#8211;95.
  {#Takeda1954}

* Wikipedia (English): [Enveloping von Neumann algebra](http://en.wikipedia.org/wiki/Enveloping_von_Neumann_algebra), [Sherman&#8211;Takeda theorem](https://en.wikipedia.org/wiki/Sherman%E2%80%93Takeda_theorem)


category: operator algebras

[[!redirects enveloping von Neumann algebra]]
[[!redirects enveloping von Neumann algebras]]
[[!redirects enveloping W-star-algebra]]
[[!redirects enveloping W-star-algebras]]
[[!redirects enveloping W-*-algebra]]
[[!redirects enveloping W-*-algebras]]
[[!redirects enveloping W*-algebra]]
[[!redirects enveloping W*-algebras]]

[[!redirects Sherman-Takeda theorem]]
[[!redirects Sherman–Takeda theorem]]
[[!redirects Sherman--Takeda theorem]]
