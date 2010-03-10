
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

## Example: Causal Nets of Operator Algebras
We will lay down a specific set of axioms knowing that this set is not _the set_ of Haag-Kastler axioms, but one specific choice. This will allow us to state and prove important general properties. It is possible to construct examples that fulfill the axioms, to show that they are not empty, but we will not engage in this task here, at least not now. Note however that up to now there was no success in the task to construct systems in 4 dimensions with interactions, which has led to some doubts about the usefulness of this approach in the physics community: It has yet to be shown if the approach does or does not capture the essential features that makes possible the tremendous success of the standard model of particle physics.

###Notation

####The Minkowski Spacetime
We talk about 4-dimensional Minkowski spacetime $\mathcal{Min}$ only, i.e. $\mathcal{Min}$ is the vector space $\R^{4} = \R \times \R^{3}$ equipped with the scalar product $\lt x, y \gt := x_0 y_0 - (\vec x, \vec y)$ with $( \cdot , \cdot  )$ being the Euclidean scalar product on $\R^{3}$.
Open bounded subsets of $\mathcal{Min}$ will be denoted by $\mathcal{O}$.

####The Poincar&#233; Group
...notation will be explained here...

####Operator Algebras
Von Neumann algebras $\mathcal{M}$ will always be concrete operator algebras acting on a given Hilbert space $\mathcal{H}$, as is the rule in the literature. The commutant of $\mathcal{M}$ will be denoted by $\mathcal{M}'$, the positive cone by $\mathcal{M}^+$. The minimal von Neumann algebra that contains two given ones $\mathcal{M}_1$ and $\mathcal{M}_2$ will be denoted by:
$$
      \mathcal{M}_1 \vee \mathcal{M}_2 :=  {(\mathcal{M}_1 \cup \mathcal{M}_2)}''
$$

###Definition of Vacuum Representations
...will be placed here

###Classical Theorems 
...will be cited here

## References 

... should go here. See also [[AQFT]].

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