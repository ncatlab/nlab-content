#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The Haag--Kastler axioms (sometimes also called Araki--Haag--Kastler axioms) try to define in a mathematically precise way the notion of [[quantum field theory]] (QFT), by axiomatizing how its local _algebras of observables_ should behave. 

The approch to quantum field theory based on these axioms is often called [[AQFT]]: _algebraic quantum field theory_ .

Although they are called axioms, one should keep in mind that the Haag--Kastler approach to QFT has not reached its final state, so that different versions of the axioms are used by practitioners of the field.

From the [[nPOV]], the Haag-Kastler axioms descibe a coflabby [[copresheaf|presheaf]] of algebras. This kind of structure is similar to the notion of a [[factorization algebra]], which plays a role in other approaches to formalize local algebras of observables.


## Definition

1. Axiom A: 

   To every "allowed" (e.g. bounded open) region $O$ in spacetime there is associated a [[C*-algebra]]; this association fulfils isotony.
The basic assumption of the Haag--Kastler approach is that everything that can be measured in certain regions of spacetime $O$ (like temperature or particle count) is described by an algebra $A(O)$, so that the theory consists of a [[net]] of [[operator algebras]] and a [[state]] $p$ that describes the physical system. There are different approaches to define what regions are "allowed", one common approach is to take all [[bounded space|bounded]] [[open subspace|open]] subsets of [[Minkowski space|Minkowski]] [[spacetime]].

1. Axiom B: locality

   Locality Algebras assigned to regions that are spacelike separated commute. 

1. Axiom C:  Transformation Properties

   The geometric symmetry operations map the algebra of a region onto the algebra of the transformed region.

   In Minkowski spacetime the geometric symmetry group is usually be taken to be the [[Poincaré group]], but note that some authors consider subgroups of the full Poincar&#233; group, like the subgroup of translations (Borchers: "Translation group and particle representations in quantum field theory").

1. Axiom D: Positivity of Energy

   An axiom is needed to ensure that only nonnegative energies occur -- one possibility is the "spectrum condition", which says that the spectrum (to be more precise: the support of the [[spectral measure]]) of the operator associated with a translation is contained in the closed forward light cone, for all translations. 

## Remarks

Unlike the [[Wightman axioms]], the Haag--Kastler axioms do not need the notion of "[[physical field|field]]": the fields in the Wightman axioms are -- from the Haag--Kastler point of view -- only necessary to describe how the algebras of observables are constructed; any way to consistently construct the net of algebras would suffice.

## Example: Causal Nets of Operator Algebras on Minkowski Spacetime
We will lay down a specific set of axioms knowing that this set is not _the set_ of Haag-Kastler axioms, but one specific choice. This will allow us to state and prove important general properties. It is possible to construct examples that fulfill the axioms, to show that they are not empty, but we will not engage in this task here, at least not now. Note however that up to now there was no success in the task to construct systems in 4 dimensions with interactions, which has led to some doubts about the usefulness of this approach in the physics community: It has yet to be shown if the approach does or does not capture the essential features that makes possible the tremendous success of the standard model of particle physics.

###Notation

####The Minkowski Spacetime
We talk about 4-dimensional Minkowski spacetime $\mathcal{Min}$ only, i.e. $\mathcal{Min}$ is the vector space $\R^{4} = \R \times \R^{3}$ equipped with the scalar product $\lt x, y \gt := x_0 y_0 - (\vec x, \vec y)$ with $( \cdot , \cdot  )$ being the Euclidean scalar product on $\R^{3}$.
Open bounded subsets of $\mathcal{Min}$ will be denoted by $\mathcal{O}$. The union of these $\mathcal{O}$ form an index set $\mathcal{J}$, that is partially ordered by inclusion. 

If two sets are spacelike seperated, this will be denoted by $\mathcal{O}_1 \perp \mathcal{O}_2$.

We denote the open forward cone at x by $V_+(x)$, similar $V_-(x)$ is the open backward cone at $x$, if $x=0$ we simply write $V_+$ and $V_-$.

####The Poincar&#233; Group
The universal covering $SL(2, \C) \ltimes \R^4$ of the restriced Poincar&#233; group $\mathcal{P}^{\dagger}_+$ will be denoted by $\mathcal{P}$, the abelian subgroup of all translations by $\mathcal{T}$.

####Operator Algebras
Von Neumann algebras $\mathcal{M}$ will always be concrete operator algebras acting on a given Hilbert space $\mathcal{H}$, as is the rule in the literature (see also [[von Neumann algebra]] here on the nLab). The commutant of $\mathcal{M}$ will be denoted by $\mathcal{M}'$, the positive cone by $\mathcal{M}^+$. The minimal von Neumann algebra that contains two given ones $\mathcal{M}_1$ and $\mathcal{M}_2$ will be denoted by:
$$
      \mathcal{M}_1 \vee \mathcal{M}_2 :=  {(\mathcal{M}_1 \cup \mathcal{M}_2)}''
$$

An automorphismus of an algebra $\alpha \mathcal{M} \rightarrow \mathcal{M}$ is called an **inner** automorphismus if there is an invertible element $u \in \mathcal{M}$ such that $\alpha$ is given by conjugation with $u: \alpha(m) = u \quad m \quad u^{-1} \qquad \forall m\in \mathcal{M}$ (note that our convention here differs from that used by [Wikipedia] (http://en.wikipedia.org/wiki/Inner_automorphism)).

###Definition of Vacuum Representations
A net of von Neumann algebras $\mathcal{M}(\mathcal{O})$ on a common Hilbert space $(\mathcal{H})$, indexed by $\mathcal{O} \in \mathcal{J}$, is called a **vacuum respresentation** (on the 4-dimensional Minkowski spacetime) if it satisfies the following axioms:

+-- {: .num_theorem #isotony}
* (V1) **isotony**: $\mathcal{O}_1 \subset \mathcal{O}_2 implies \mathcal{M}(\mathcal{O}_1) \subseteq \mathcal{M}(\mathcal{O}_2)$
=--

+-- {: .num_theorem #additivity}
* (V2) **additivity**: $\mathcal{O} = \bigcup_j \mathcal{O}_j$ implies  $\mathcal{M}(\mathcal{O}) = ( \bigcup_j \mathcal{M}(\mathcal{O}_j) )'' $ 
=--

+-- {: .num_theorem #locality}
* (V3) **locality**, see [[local net]]: $\mathcal{O}_1 \perp \mathcal{O}_2 implies \mathcal{M}(\mathcal{O}_1) \subseteq  (\mathcal{M}(\mathcal{O}_2))' $
=--

+-- {: .num_theorem #covariance}
* (V4) **covariance**: There is a strongly continuous unitary representation $\mathcal{U}(\mathcal{P})$ of $\mathcal{P}$ such that for each $g \in \mathcal{P}$ the following holds: $\mathcal{M}(g\mathcal{O}) = \mathcal{U}(g) \mathcal{M}(\mathcal{O}) \mathcal{U}(g)^{-1}$
=--

+-- {: .num_theorem #spectrum_condition}
* (V5) **spectrum condition**: $spec\mathcal{U}(\mathcal{T}) \subseteq clo \mathcal{V}_+$
=--

Note: $\mathcal{T}$ is the abelian subgroup of translations, and $\mathcal{V}_+$ is the (open) forward cone at 0, see above. For the definiton of the spectrum of the representation $\mathcal{U}(\mathcal{T})$ see [[spectral measure]].

+-- {: .num_theorem #existence_of_vacuum_vector}
* (V6) **existence of a vacuum vector**: There exists a vector $\Omega \in \mathcal{H}, \|\Omega\| = 1$, such that $( \bigcup_{\mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O} ) \Omega$ is dense in $\mathcal{H}$ and $\mathcal{U}(g)\Omega = \Omega$ for all $g \in \mathcal{P}$
=--

Note: The _uniqueness_ is sometimes part of the axioms, but not here. Instead we will cite theorems that will specify necessary and sufficient conditions to ensure that there is a _unique_ vacuum vector. 

###Additional Notations and Notions of Vacuum Representations
A short hand notation for vacuum representations will be $\mathcal{M}(\mathcal{J})$ in the following.

The algebras $\mathcal{M}(\mathcal{O})$ are sometimes called **local algebras**.

The $C^*-$algebra $\mathcal{A} := clo_{\| \cdot \|} ( \bigcup_{\mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O}) $ is called **quasilocal algebra**, the smallest von Neuman algebra that contains $\mathcal{A}$ is called the **global algebra** and denoted by $\mathcal{R}$. 

A vacuum representation is called **irreducible** if $\mathcal{R} = \mathcal{L}(\mathcal{H})$ (the global algebra is the whole algebra of all bounded linear operators on the given Hilbert space), it is called **factorial** if $\mathcal{R}$ is a factor.

* Wikipedia on [factors] (http://en.wikipedia.org/wiki/Von_Neumann_algebra#Factors) of von Neumann algebras.

The subspace of $\mathcal{H}$ that is invariant under the action of the translation group $\mathcal{T}$ is not trivial due to the axiom \ref{existence_of_vacuum_vector}. If it is one-dimensional, we will say that the vacuum representation has a **unique vacuum vector** (the space is then necessarily the subspace $\C\Omega$).

###Classical Theorems 
...will be cited here, default reference for this section is

* Hellmut Baumg&#228;rtel: Operatoralgebraic Methods in Quantum Field Theory, see [[AQFT]].

* **Theorem 1 (Borchers)**: The representatives of the translations are elements of the global algebra $\mathcal{R}$, i.e. they are inner automorphisms of $\mathcal{R}$: $\mathcal{U}(\mathcal{T}) \subseteq \mathcal{R}$.

* **Theorem**: Every factorial vacuum representation is irreducible. A vacuum representation is irreducible iff it has an unique vacuum vector.

* **Reeh-Schlieder Theorem**: The vacuum vector is cyclic and separating for all local algebras.

Let $x, y \in \R^4$ and define $[x, y] := \{\lambda x + \mu y | \lambda, \mu \geqq 0, \lambda + \mu = 1\} $.
Define
$$
           \mathcal{M}[x, y] := \cap_{[x, y] \subset \mathcal{O}} \mathcal{M}(\mathcal{O})
$$
* **Triviality of algebras of spacelike segments**: If the segment $[x, x + b]$ is spacelike, i.e. $\langle b, b \rangle \lt 0$, and the vacuum respresentation has a unique vacuum vector, then $\mathcal{M}[x, x + b] = \mathbb{C} \mathbb{1}$, i.e. the algebra associated with the segment is trivial.

* **Triviality of algebras of points**: The conclusion of the preceding statement holds if we put $b = 0$, i.e. if we consider the algebra associated with one point.

The preceding theorem is sometimes summarized as _there are no non-trivial observables at the point_. There are two possible ways to interpret this result: The pragmatic approach says that, since no detector can be built that measures observables precisley at one point of spacetime, there is no need of a theory to support the concept of observables localized at a point. The philosophical approach takes this one step further and states that our relativistic quantum theory tells us that the concepts of points and observables localized at points are an idealization with no relevance to nature.

## Generalization of the Haag-Kastler Axioms to Curved Spacetimes
It is possible to generalize the Haag-Kastler approach to general (Lorentzian) spacetimes.

### Idea
From the physical point of view there are two different reasons to consider the Haag-Kastler approach on more general manifolds than the Minkowski spacetime:

* It is expected that such a theory, while not solving the problem to construct a theory of quantum gravity, would still have a wide range of validity.

* From a conceptual viewpoint abandoning the special situation of the Minkowski spacetime could lead to the development of new ideas and tools that turn out to be helpful to understand the concept of a quantum field theorie better.

The first point deserves some elaboration: The curved manifolds under consideration are supposed to be solutions to the field equations of General Relativity, i.e. physically realistic spacetimes, so that gravity is modelled classically by the curvature of spacetime. A quantum field theory on such a spacetime should be able to model the situation of elementary particles that feel the effects of gravity while neglecting the effect that the particles themselves have on spacetime (the notion of "particle" is highly nontrivial and nonproblematic in this setting and is to be understood in a methaphorical sense in the given context). Example: If you let an electron drop from your hand to the ground, that would be a situation that should be handled by the theory.
While a full theory of quantum gravity still eludes us, a theory of quantum fields on curved spacetimes could be useful as a kind of interpolation. In a certain sense this is already the case, since the [laws of black hole thermodynamics] (http://en.wikipedia.org/wiki/Black_hole_thermodynamics) were first discovered with the help of this setting.

## References 

See also [[AQFT]]. 

### References for the physical aspects of the Haag-Kastler approach on Minkowski spacetime

Since on that page there are already some references to sources that stress the mathematical aspects, we will cite some that are more oriented to the physical interpretations:

The classic references are of course:

* Rudolf Haag: Local quantum physics. Fields, particles, algebras. 2nd., rev. and enlarged ed. Springer 1996 [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0857.46057&format=complete).

and:

* Huzihiro Araki: Mathematical theory of quantum fields. Oxford University Press 1999 [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0998.81501&format=complete). 

An online reference page by is here:

* Stephen J. Summers: [AQFT online] (http://www.math.ufl.edu/~sjs/aqft.html)

### References for the generalization of the Haag-Kastler approach to curved spacetimes

A classic reference is this:

* Wald, Robert M.: Quantum field theory in curved spacetime and black hole thermodynamics. Univ. of Chicago Press 1994 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0842.53052&format=complete)).

Recently published review papers:

* Romeo Brunetti, Klaus Fredenhagen: [Quantum Field Theory on Curved Backgrounds] (http://xxx.uni-augsburg.de/abs/0901.2063)

* Robert M. Wald: [The Formulation of Quantum Field Theory in Curved Spacetime] (http://de.arxiv.org/abs/0907.0416)

* Robert M. Wald: [The History and Present Status of Quantum Field Theory in Curved Spacetime] (http://lanl.arxiv.org/abs/gr-qc/0608018v1)

+-- {: .query}
[[Tim van Beek]]: I have not done an extensive search for pages that I could link to, so there may be some missing (but not on purpose!). Also the links on the [[AQFT]] site could equally well be placed here... 
=--


[[!redirects Haag-Kastler axioms]]
[[!redirects Haag-Kastler axiom]]
[[!redirects Haag–Kastler axioms]]
[[!redirects Haag–Kastler axiom]]
[[!redirects Haag--Kastler axioms]]
[[!redirects Haag--Kastler axiom]]
[[!redirects Araki-Haag-Kastler axioms]]
[[!redirects Araki-Haag-Kastler axiom]]
[[!redirects Araki–Haag–Kastler axioms]]
[[!redirects Araki–Haag–Kastler axiom]]
[[!redirects Araki--Haag--Kastler axioms]]
[[!redirects Araki--Haag--Kastler axiom]]