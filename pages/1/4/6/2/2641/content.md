+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

The [[Poincaré group]] is the group of rigid [[spacetime]] symmetries of [[Minkowski spacetime]]. It is a [[topological group]] and as such has [[unitary representation]]s on infinite-dimensional [[Hilbert space]]s. For any [[quantum field theory]] in [[Minkowski space]] its [[space of states]] therefore decomposes into [[irreducible representation]]s of the [[Poincaré group]]. As was first observed by [[Hermann Weyl]], these irreducible representations encode the [[particle]] spectrum of the QFT.

We are interested in the **[[unitary representations]]** of a [[topological group]] $G$, i.e., the continuous [[group homomorphisms]]
$$U\colon G \to U(H)$$
into the [[unitary group]] of a [[Hilbert space]] $H$, especially those that are [[irreducible representation|irreducible]] in the usual sense of [[representation theory]]. The topology on $U(H)$ here is understood to be the [[operator topology|strong operator topology]]. 

In this and related articles, we study such representations in the case where 

$$G = SL_2(\mathbb{C}) \ltimes \mathbb{R}^4$$ 

is the [[universal cover]] of the [[connected]] component of the identity of the [[Poincaré group]], which is important in the study of [[quantum field theory]]. A more physical name for such a representation is "[[elementary particle]]", and we will often use that term in this article. (NB: "elementary particle" will always refer to the formal mathematical representation it refers to.)

A full rounded account could become large; see the [blog discussion](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html), which despite its size was left in a still-nascent state. However, in a nutshell, the basic theorem is that (elementary) particles are classified up to isomorphism according to their [[mass]] and [[helicity]]; mass is a continuous parameter and helicity is a discrete parameter. 

This theorem in commonly ascribed to [[Eugene Wigner]] and often referred to as the _[[Wigner classification]]_. 

Wigner classified all irreducible unitary representations of the restricted Poincare group, including the unphysical ones. The latter cannot be used to define a [[free quantum field theory]] satisfying the [[Wightman axioms]]. Those that can are the physical ones and are characterized by a nonnegative real mass and a nonnegative half-integral spin; the zero component of the momentum has a nonnegative spectrum. 
Many of these are realized by particles occurring in Nature, though not as 'elementary particles' but as bound states (in a suitable approximation, e.g., [[QCD]]). From the point of view of representation theory, the center of mass of a bound state behaves just like an elementary particle. Thus elementary is meant in this generalized sense.


## Related entries

Relevant topics in a full account will include 

* [[spectral theorem|Spectral theorem]]

* [[rigged Hilbert space|Rigged Hilbert spaces]] and [[direct integral|direct integrals]]

* [[induced representations]]

* [[helicity]], [[spin]]

* [[Klein-Gordon equation]] 

* [[Dirac equation]] 

* [[spin-statistics theorem]]

* [[Maxwell equation]] 

* [[Stone's theorem]] 

* [[Mackey theory]]



## Tentative notes, to be expanded on... 

In the first place, physicists tend to be a little carefree with the mathematics, so this account is written from the point of view of a 'stupid' mathematician (for the moment Todd Trimble) who wants to get details straight and precise. 

For example, physicists tend to talk about "eigenstates" as if they were elements of the Hilbert space, and other states as linear combinations of eigenstates, whereas really we are dealing with some more complicated technology like rigged Hilbert spaces or direct integrals instead of direct sums. Failure to mention such details places hurdles of communication between physicists and mathematicians. In addition, there are stylistic differences in presentation, where a physicist will happily deal with formulas replete with lots of subscripts and superscripts, whereas many mathematicians prefer dealing with more conceptual, less notation-heavy explanations. 

There seem to be at least three ways of dealing with spectral theory of (unbounded) self-adjoint operators on a Hilbert space: 

* The usual Stone theory

* Direct integrals of Hilbert spaces

* Rigged Hilbert spaces


### Rigged Hilbert spaces 

A rigged Hilbert space 


## Induced representations 

Simultaneous diagonalization. 

Fact that Poincar&#233; group is a [[semidirect product group]]. 


Let $\vec p \in \mathbb{R}^{d-1,1}$ be a given vector in [[Minkowski spacetime]]. Write 

$$
  Stab_{Iso(\mathbb{R}^{d-1,1}))}(\vec p)
    \hookrightarrow
  Iso(\mathbb{R}^{d-1,1})
$$ 

for its [[stabilizer subgroup]] (often called _the little group_ in this context, going back to Wigner). Every unitary irrep of $Iso(\mathbb{R}^{d-1,1})$ of mass $p$ is an [[induced representation]] of a finite dimensional representation of the "little group" $Stab_{Iso(\mathbb{R}^{d-1,1}))}(\vec p)$. (recalled concisely e.g. in [Dragon 16, p. 2](#Dragon16)).


## Related concepts

* [[Wigner classification]]

* [[twistor]]

* [[unitary representation of the super Poincaré group]]

* [[Doplicher-Roberts reconstruction theorem]]

* [[finite-dimensional representation of the Poincaré group]]

* unitary representations of the [[anti de Sitter group]],

  [[singleton representation]]

## References

The observation that the irreps of the Poincar&#233; group correspond to [[fundamental particles]] ([[Wigner classification]]) is due to

* [[Eugene Wigner]], _On unitary representations of the inhomogeneous Lorentz group_ , Ann. Math. **40:1** (1939), 149–204.

Review includes

* [[Rudolf Haag]], section I.3.1  of _[[Local Quantum Physics -- Fields, Particles, Algebras]]_

* {#Schroer96} [[Bert Schroer]], _Wigner Representation Theory of the Poincar&#233;
Group, Localization, Statistics and the S-Matrix_, 1996  ([pdf](http://cds.cern.ch/record/308785/files/9608092.pdf))

* Eberhard Freitag, _Unitary representations of the Poincar&#233; group_ ([pdf](http://www.rzuser.uni-heidelberg.de/~t91/skripten/unitdarst.pdf))

* [[Xavier Bekaert]], Nicolas Boulanger, _The unitary representations of the Poincare group in any spacetime dimension_ ([arXiv:hep-th/0611263](http://arxiv.org/abs/hep-th/0611263))

* {#Dragon16} [[Norbert Dragon]], _Currents for Arbitrary Helicity_ ([arXiv:1601.07825](http://arxiv.org/abs/1601.07825))


[[!redirects unitary irrep of the Poincare group]]
[[!redirects unitary irreps of the Poincare group]]
[[!redirects unitary irrep of the Poincaré group]]
[[!redirects unitary irreps of the Poincaré group]]

[[!redirects unitary representation of the Poincare group]]
[[!redirects unitary representations of the Poincare group]]
[[!redirects unitary representation of the Poincaré group]]
[[!redirects unitary representations of the Poincaré group]]

[[!redirects irreducible representation of the Poincare group]]
[[!redirects irreducible representation of the Poincaré group]]
[[!redirects irreducible representations of the Poincare group]]
[[!redirects irreducible representations of the Poincaré group]]
