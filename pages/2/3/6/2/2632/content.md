

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

While [[classical mechanics]] considers deterministic evolution of particles and fields, quantum physics follows nondeterministic evolution where the probability of various outcomes of [[measurement]] may be predicted from the state in a Hilbert space representing the possible reality: that state undergoes a unitary evolution, what means that the generator of the evolution is $\sqrt{-1}$ times a Hermitean operator called the *quantum Hamiltonian* or the [[Hamiltonian operator]] of the system. The theoretical framework for describing this precisely is the __quantum mechanics__. It involves a constant of nature, Planck constant $h$; some quantum systems with spatial interpretation in the limit $h\to 0$ lead to classical mechanical systems (not all: some phenomena including non-integer spin are purely quantum mechanical, but the properties depending on their existence survive in the "classical" limit); in limited generality, one can motivate and find the *nonfunctorial* procedure to single out a [[right inverse]] to taking this *classical limit* under the name [[quantization]]. 

While quantum mechanics may be formulated for a wide range of physical systems, interpreted as particles, extended particles and fields, the quantum mechanics of fields is often called the [[quantum field theory]] and the quantum mechanics of systems of a fixed finite number of particles is often viewed as the quantum mechanics in a narrow sense. 

##### nPOV

Mathematically, despite the basic formalism of quantum mechanics which is sound and clear, there are two big areas which are yet not clear. One is to understand quantization, in all cases -- of particles, fields, strings and so on. The second and possibly more central to nLab is a problem how to define rigorously a wide range of quantum field theories and some related quantum mechanical systems like the hypothetical [[superstring theory]]. Regarding that this is a central goal, we also put emphasis on the [[interpretation of quantum mechanics]] via the picture which is a special case of a FQFT, and where the time evolution functorially leads to evolution operators. 

## Definition

We discuss some basic notions of quantum mechanics.

### Quantum mechanical systems

Recall the notion of a _[[classical mechanical system]]_: the formal dual of a real _commutative_ [[Poisson algebra]]. 

+-- {: .num_defn #QuantumSystem}
###### Definition

A **quantum mechanical system** is a [[star algebra]] $(A, (-)^\ast)$ over the [[complex number]]s. The [[category]] of of quantum mechanical systems is the [[opposite category]] of $\ast$-algebras:

$$
  QuantMechSys := {\ast}Alg_{\mathbb{C}}^{op}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

It makes sense to think of this as a deformed version of a real [[Poisson algebra]] as follows:

* the Poisson-[[Lie algebra|Lie bracket]] of a [[Poisson algebra]] corresponds to the [[commutator]] of the $\ast$-algebra:

  $$
    [a,b] := a b - b a
    \,,
  $$

* the commutative algebra structure of the Poisson algebra coresponds to the [[Jordan algebra]] structure of the $\ast$-algebra, with commutative (but non-associative!) product

  $$
    (a,b) := a b + b a
    \,.
  $$

With this interpretation the [[derivation]]-property of the Poisson bracket over the other product is preserved: for all $a,b,c \in A$ we have

$$
  [a,(b,c)] = ([a,b],c) + (b,[a,c])
  \,.
$$

We thus may regard a non-commutative star-algebra as a _[[nonassociative algebra|non-associative]] [[Poisson algebra]]_ : a [[Jordan-Lie algebra]]. See there for more details.

=--




### Observables and states

+-- {: .num_defn}
###### Definition

Given a quantum mechanical system in terms of a [[star algebra]] $A$, we say

* an **[[observable]]** is an element $a \in A$ such that $a^\ast = a$;

* a **[[state]]** is a [[linear function]] $\rho : A \to \mathbb{C}$ which is _positive_ in the sense that for all $a \in A$ we have $\rho(a a^\ast) \geq 0 \in \mathbb{R} \hookrightarrow \mathbb{C}$.

=--

+-- {: .num_remark}
###### Remark

One can formalize the idea that a quantum mechanical system is like a deformed [[classical mechanical system]] as follows:

To every ${}^\ast$-algebra $A$ is associated its [[poset of commutative subalgebras]] $Com(A)$. Then the corresponding quantum mechanical system is a [[classical mechanical system]] [[internalization|internal]] to the [[sheaf topos]] $Sh(Com(A))$:

* The $\ast$-algebra canonically induces a commuative algebra $\underline A \in Sh(Com(A))$;

* the (classical) [[state]]s of $\underline{A}$ in $Sh(Com(A))$ are in natural bijection with the quantum states externally on $A$;

* the (classical) [[observable]]s of $\underline{A}$ in $Sh(Com(A))$ correspond to the external quantum observables on $A$.

(...details...)

=--

One also says that the internal classical mechanical system $(Sh(Com(A)), \underline{A})$ is the "[[Bohrification]]" of the external quantum system $A$. See there for more details.


### Spaces of states

Given a $\ast$-algebra $A$ together with a [[state]] $\rho$ on it, the [[GNS construction]] provides an [[inner product space]] $H_\rho$ together with an [[action]] of $A$ on $H_\rho$ and a [[vector]] $\Omega = \sqrt(\rho)$ -- the [[vacuum vector]]  -- such that for all $a \in A$ the value of the state $\rho : A \to \mathbb{C}$ is obtained by applying $a$ to $\sqrt{\rho}$ and then taking the inner product with $\sqrt \rho$:

$$
  \rho(A) = \langle \sqrt\rho, a \sqrt \rho\rangle
  \,.
$$

If the [[star algebra]] $A$ happens to be a [[C-star algebra]], then this inner product space is naturally a [[Hilbert space]].

Historically and still often in the literature, such a Hilbert space is taken as a fundamental input of the definition of quantum systems.

Traditionally, [[Dirac]]'s "bra-ket" notation is used to represent vectors in such Hilbert spaces of states, where $|\psi\rangle$ represents a state and $\langle\psi|$ represents its linear adjoint. State evolutions are expressed as unitary maps. Self-adjoint operators represent physical quantities such as position and [[momentum]] and are called [[observables]]. [[measurements|Measurements]] are expressed as sets of [[projectors]] onto the eigenvectors of an observable.

In [[mixed state]] quantum mechanics, physical states are represented as [[density operators]] $\rho$, state evolution as maps of the form $\rho \mapsto U^\dagger \rho U$ for unitary maps $U$, and [[measurements]] are positive operator-valued measures (POVM's). There is a natural embedding of pure states into the space of density matrices: $|\psi\rangle \mapsto |\psi\rangle\langle\psi|$. So, one way to think of mixed states is a probabilistic mixture of pure states.

\[ \rho = \sum_i a_i |\psi_i\rangle\langle\psi_i| \]

Composite systems are formed by taking the tensor product of Hilbert spaces. If a [[pure state]] $|\Psi\rangle \in H_1 \otimes H_2$ can be written as $|\psi_1\rangle \otimes |\psi_2\rangle$ for $|\psi_i\rangle \in H_i$ it is said to be _[[separable]]_. If no such $|\psi_i\rangle$ exist, $|\Psi\rangle$ is said to be _[[entangled]]_. If a mixed state is separable if it is the sum of separable pure states. Otherwise, it is entangled.


### Flows and time evolution

As for classical mechanics, 1-parameter families of flows in a quantum mechanical system are induced from observables $a \in A$ by

$$
  \frac{d}{d \lambda} b_\lambda = \frac{1}{i \hbar}[b_\lambda, a]
  \,.
$$

In a non-relativistic system one specifies an observable $H$ -- called the [[Hamiltonian]] -- whose flow represents the time evolution of the system. (This is the [[Heisenberg picture]].)

We comment on how to interpret this from the point of view of [[FQFT]]:

Quantum mechanics of point particles may be understood as a special case of the formalism of [[quantum field theory]]. It is interpreted as the quantum analog of the [[classical mechanics]] of point particles. Of course, we can take a configuration space of a system of particles looking like the configuration space of a single particle in a higher dimensional manifold. 

Remark: related query on the relation between QFT and quantum mechanics (of particles and in general) can be found [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2573&Focus=22060#Comment_22060). 

One may usefully think of the quantum mechanics of a point particle propagating on a [[manifold]] $X$ as being $(0+1)$-dimensional [[quantum field theory]]:

the fields of this system are maps $\Sigma \to X$ where $\Sigma \in Riem Bord_1$ are 1-dimensional [[Riemannian manifold]] [[cobordism]]s. These are the _trajectories_ of the particle. 

After [[quantization]] this yields a 1-dimensional [[FQFT]] given by a [[functor]]

$$
  U(-) : Riem Bord_1 \to Hilb
$$

from [[cobordism]]s to [[Hilbert space]]s (or some other flavor of [[vector space]]s) that assigns

* to the point the _space of states_ $\mathcal{H}$, typically the space of $L_2$-sections (with respect to a [[Riemannian metric]] on $X$) of the background [[gauge field]] on $X$ under which the particle in question is charged 

* to the cobordism of Riemannian length $t$ the operator

  $$
    U(t) := \exp\left(\frac{t}{i \hbar } H \right)
    : \mathcal{H} \to \mathcal{H}
    \,,
  $$

  where $H$ is the [[Hamiltonian operator]], typically of the form $H = \nabla^\dagger \circ \nabla $ for $\nabla$ the [[covariant derivative]] of the given background [[gauge field]].

Such a setup describes the quantum mechanics of a particle that feels forces of backgound [[gravity]] encoded in the [[Riemannian metric]] on $X$ and forces of background gauge fields (such as the [[electromagnetic field]]) encoded in the covariant derivative $\nabla$.

(This is the [[Schrödinger picture]].)

### Quantum subsystems 
 {#Subsystems}

+-- {: .num_defn}
###### Definition

For $\mathcal{A}$ an algebra describing a quantum system, def. \ref{QuantumSystem}, a **subsystem** is a subalgebra (a [[subobject]]) $B \hookrightarrow \mathcal{A}$.

Two subsystems $B_1, B_2 \hookrightarrow \mathcal{A}$ are called **independent subsystems** if the [[linear map]]

$$
  B_1 \otimes B_2 \to \mathcal{A}
$$

$$  
  (b_1, b_2) \mapsto b_1 \cdot b_2
$$

from the [[tensor product]] of algebras (the [[composite system]]) factors as an [[isomorphism]]

$$
  B_1 \otimes B_2 \stackrel{\simeq}{\to} B_1 \vee B_2 \hookrightarrow \mathcal{A}
$$

through the algebra $B_1 \vee B_2$ that is generated by $B_1$ and $B_2$ inside $\mathcal{A}$ (the smallest subalgebra containing both).

=--

See for instance ([BrunettiFredenhagen, section 5.2.2](#BrunettiFredenhagen)).

+-- {: .num_defn}
###### Definition

Given two independent subsystems $B_1, B_2 \hookrightarrow \mathcal{A}$, and two [[states]] $\rho_1 : B_1 \to \mathbb{C}$ and $\rho_2 : B_2 \to \mathbb{C}$, then the corresponding **product state** $\rho_1 \otimes \rho_2$ on $B_1 \vee B_2$ is defined to be

$$
  (\rho_1 \otimes \rho_2) : 
  (b_1 , b_2) \mapsto \rho_1(b_1) \rho_2(b_2)
  \,.
$$

=--


+-- {: .num_defn}
###### Definition

There exist states on $B_1 \vee B_2$ that are not (convex combinations of) product states. This phenomenon is called [[entanglement]].

=--

## Quantum physics in general 

More generally, _quantum physics_ is all the known physics not including [[classical physics]] in wider sense; it includes relativistic and nonrelativistic phenomena. Quantum mechanics is the standard formalism with the Hilbert space, unitary evolution etc. which explains theoretically phenomena of quantum physics: in this generality of the formalism a la von Neumann, it includes the quantum field theory. Quantum statistical mechanics in fact uses some additional assumptions not in exact quantum mechanics, which are believed to be derivable eventually (like quantum ergodicity etc.). Thus quantum statistical mechanics may or may not be included within quantum mechanics. 

Remark: Another way to look at quantum processes is via [[quantum channels]] which are completely positive trace-preserving maps.

For a previous query about quantum physics (includes experimental phenomena) and quantum mechanics (formalism for such, sometimes with or without statistical principles) see [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2573&Focus=22059#Comment_22059).

## Formulations and formalization

### Order-theoretic structure in quantum mechanics

See _[[order-theoretic structure in quantum mechanics]]_.

### Quantum mechanics in terms of $\dagger$-compact categories

Many aspects of quantum mechanics and [[quantum computation]] depend only on the abstract properties of [[Hilb]] characterized by the fact that it is a [[†-compact category]]. 

For more on this see

* [[quantum mechanics in terms of †-compact categories]].

## Foundational theorems of quantum mechanics

The following circle of [[theorems]]

* [[Kochen-Specker theorem]]

* [[Gleason's theorem]]

* [[Alfsen-Shultz theorem]]

* [[Harding-Döring-Hamhalter theorem]]

all revolve around the phenomenon that the "[[phase space]]" in quantum mechanics and hence the [[space of quantum states]] are all determined by the [[Jordan algebra]] structure on the [[algebra of observables]], which in turn is determined by the [[poset of commutative subalgebras]] of the algebra of observables. See at _[[order-theoretic structure in quantum mechanics]]_ for more on this.

There is also 

* [[Wigner's theorem]]

which says roughly that linear maps between [[spaces of quantum states]] are [[unitary operators]] (or anti-unitary) already when they preserve [[norm]], hence preserve [[probability]].


## Applications of quantum mechanics

Quantum mechanics, as opposed to [[classical mechanics]], is necessary for an accurate description of reality whenever the characteristic scale is sufficiently small. For instance

* In [[chemistry]] ("[[quantum chemistry]]") the properties of [[atoms]] and [[molecules]] are derived from quantum mechanics.

* In [[solid state physics]] the properties of [[metals]] etc. are described by quantum mechanics of electron gases.

* In [[particle physics]] of course, [[quantum field theory]] is the appropriate description.

## Examples

* [[harmonic oscillator]]

* [[hydrogen atom]]

* [[quantum lattice system]]

## Related concepts

* [[classical mechanics]]

  * [[semiclassical approximation]]

* [[quantization]]

  * [[deformation quantization]], [[geometric quantization]]

* **quantum mechanics**

  * [[Planck's constant]]

  * [[Schrödinger picture]], [[Heisenberg picture]], [[Dirac picture]]

  * [[quantum probability]]

  * [[propagator]]

  * [[quantum superposition]], [[quantum fluctuation]], [[quantum entanglement]]

  * [[quantum measurement]]

    * [[positive-operator valued probability measure]]

  * [[hidden variable theory]], 

    * [[EPR paradox]], [[Bell's inequalities]]

    * [[Kochen-Specker theorem]]

  * [[no-cloning theorem]]
 
  * [[Born-Oppenheimer approximation]]

  * [[quantum tunneling]]

  * [[supersymmetric quantum mechanics]]

  * [[quantum logic]], [[quantum computing]]

    * [[linear logic]], [[linear type theory]]

  * [[finite quantum mechanics in terms of dagger-compact categories]]

  * [[JBW-algebraic quantum mechanics]]

  * [[interpretation of quantum mechanics]]

  * [[quaternionic quantum mechanics]]

* [[quantum field theory]]

  * [[FQFT]], [[AQFT]]

* [[quantum chemistry]]

* [[quantum biology]]

## References

### Historical origins

* [[Werner Heisenberg]], *Über quantentheoretische Umdeutung kinematischer und mechanischer Beziehungen*, Zeitschrift für Physik **33** (1925) 879–893 &lbrack;[doi:10.1007/BF01328377]( https://doi.org/10.1007/BF01328377), [Engl. pdf](http://users.mat.unimi.it/users/galgani/arch/heis25ajp.pdf)&rbrack;

* [[Max Born]], [[Pascual Jordan]], *Zur Quantenmechanik*, Zeitschrift für Physik **34** (1925) 858–888 &lbrack;[doi:10.1007/BF01328531](https://doi.org/10.1007/BF01328531)&rbrack;

* [[Paul A. M. Dirac]], *On the theory of quantum mechanics*, Proceedings of the Royal Society **112** 762 (1926) &lbrack;[doi:10.1098/rspa.1926.0133](https://doi.org/10.1098/rspa.1926.0133)&rbrack;

Equivalence of the [[Heisenberg picture]] and the [[Schrödinger picture]]:

* [[Erwin Schrödinger]], *Über das Verhältnis der Heisenberg-Born-Jordanschen Quantenmechanik zu der meinen*, Annalen der Physil **384** 8 (1926) 734-756 &lbrack;[doi:10.1002/andp.19263840804]( https://doi.org/10.1002/andp.19263840804)&rbrack;

* [[Carl Eckart]], *Operator Calculus and the Solution of the Equations of Quantum Dynamics*, Phys. Rev. **28** 4  (1926) 711-726 &lbrack;[doi:10.1103/PhysRev.28.711](https://doi.org/10.1103/PhysRev.28.711)&rbrack;

Introducing the tool of [[group theory]] to quantum physics:

* [[Eugene P. Wigner]], *Group theory: And its application to the quantum mechanics of atomic spectra*, 5, Academic
Press (1959) &lbrack;[doi:978-0-12-750550-3](https://www.elsevier.com/books/group-theory/wigner/978-0-12-750550-3)&rbrack;



### General

Classical textbooks (on the [[Hilbert space]] description) include

* [[John von Neumann]], _Mathematische Grundlagen der Quantenmechanik_.
(German) Mathematical Foundations of Quantum Mechanics. Berlin,
Germany: Springer Verlag, 1932.

* [[George Mackey]], _The Mathematical Foundations of Quamtum Mechanics_ A
Lecture-note Volume, ser. The mathematical physics monograph series.
Princeton university, 1963

* E. Prugovecki, _Quantum mechanics in Hilbert Space_. Academic Press,
1971.


* {#Dirac78} [[Paul Dirac]], _[[The Principles of Quantum Mechanics]]_, International series of monographs on physics, Oxford University Press, 1978
  
* Anthony Sudbery, Quantum mechanics and the particles of nature: an outline for mathematicians 

Modern textbooks:

* [[Mikio Nakahara]], Chapter 1 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)



Lecture notes include

* Uni Bonn, _[Lecture scripts and Online courses -- Quantum mechanics](http://www-cip.physik.uni-bonn.de/~baehren/scripts/quantum.html)_

* [[Valter Moretti]], _Mathematical Foundations of Quantum Mechanics: An Advanced Short Course_ ([arXiv:1508.06951](http://arxiv.org/abs/1508.06951))

Some standard references include

* Glimm and Jaffe, [[Glimm-Jaffe|Quantum physics - a functional integral point of view]] 

* Movshev's course has mathematically nice references: [link](http://www.math.sunysb.edu/~mmovshev/MAT570Spring2008/syllabusfinal.html); and [here](http://www.math.columbia.edu/~woit/qftnotes1.pdf) is a link to Woit's list of more physical tradition references. 

* [[Klaas Landsman]], _[[Mathematical Topics Between Classical and Quantum Mechanics]]_

* {#Landsman17} [[Klaas Landsman]], _Foundations of quantum theory -- From classical concepts to Operator algebras_, Springer Open 2017 ([doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf))

* P. Cartier, C. DeWitt-Morette, _Functional integration: action and symmetries_, Cambridge Monographs on Mathematical Physics, 2006.

* Leon Takhtajan, _[[Quantum mechanics for mathematicians]]_ , Amer. Math. Soc. 2008. 

* {#BatesWeinstein} Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)
 
* F. Strocchi, _An introduction to the mathematical structure of quantum mechanics_ 

* [[Valter Moretti]], _Spectral Theory and Quantum Mechanics_ 2nd edition  Springer 2018

* [[Valter Moretti]], _Fundamental Mathematical Structures of Quantum Theory_  Springer 2019

Dicussion of quantum measurement is in

* Jan Perina, Z. Hradil, [[Branislav Jurčo]], _[[Quantum optics and fundamentals of physics]]_, Kluwer 1994


Introduction to mathematical foundations of quantum physics in [[quantum probability]], [[operator algebra]]:

* {#Gleason09} Jonathan Gleason, _The $C^*$-algebraic formalism of quantum mechanics_, 2009 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/Gleason.pdf), [[GleasonAlgebraic.pdf:file]])

* {#FroehlichSchubnel15} [[Jürg Fröhlich]],  B. Schubnel, _Quantum Probability Theory and the Foundations of Quantum Mechanics_. In: Blanchard P., Fröhlich J. (eds.) _The Message of Quantum Science_. Lecture Notes in Physics, vol 899. Springer 2015 ([arXiv:1310.1484](https://arxiv.org/abs/1310.1484), [doi:10.1007/978-3-662-46422-9_7](https://doi.org/10.1007/978-3-662-46422-9_7))

* {#Froehlich} [[Jürg Fröhlich]], _The structure of quantum theory_, Chapter 6 in _The quest for laws and structure_, EMS 2016  ([doi](https://www.researchgate.net/publication/308595814_The_Quest_for_Laws_and_Structure), [doi:10.4171/164-1/8](https://www.ems-ph.org/books/show_abstract.php?proj_nr=207&vol=1&rank=8))

* {#Landsman17} [[Klaas Landsman]], _Foundations of quantum theory -- From classical concepts to Operator algebras_, Springer Open 2017 ([pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf))

see also

* {#Hardy01} [[Lucien Hardy]], _Quantum Theory From Five Reasonable Axioms_ ([arXiv:quant-ph/0101012](https://arxiv.org/abs/quant-ph/0101012))


Generalization of the algebraic perspective to [[quantum field theory]] is discussed in 

* [[Rudolf Haag]], _[[Local Quantum Physics -- Fields, Particles, Algebras]]_ 

for more on this see at _[[AQFT]]_ and at _[[perturbative AQFT]]_  

Different incarnations of this [[C*-algebra|C*-algebraic]] locality condition are discussed in section 3 of 

* Sander Wolters, _Quantum toposophy_, 

relating it to the [[topos theory|topos-theoretic]] formulation in 

* [[Joost Nuiten]], _[[schreiber:bachelor thesis Nuiten|Bohrification of local nets of observables]]_



Aspects of quantum mechanics in [[category theory]] and [[topos theory]] are discussed in 

* [[Hans Halvorson]] (ed.) _Deep Beauty -- Understanding the quantum world through mathematical innovation_ Cambridge (2011) ([pdf](http://www.tacron.com/uploads/Deep_Beauty_-_Understg_the_Quantum_World_Through_Mathem._Innov._-_H._Halvorson__Cambridge__2011__WW.pdf))

This discusses for instance [[higher category theory and physics]] and the [[Bohr topos]] of a quantum system.

[[!redirects quantum physics]]
[[!redirects quantum theory]]

[[!redirects quantum mechanical system]]
[[!redirects quantum mechanical systems]]