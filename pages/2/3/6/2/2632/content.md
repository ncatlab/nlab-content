

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

* The $\ast$-algebra canonically induces a commutative algebra $\underline A \in Sh(Com(A))$;

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

  * [[geometrical formulation of quantum mechanics]]

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
 {#References}

### Historical origins

Historical review:

* Eren Volkan Küçük: *The Birth of Quantum Mechanics: A Historical Study Through the Canonical Papers* &lbrack;[arXiv:2503.13630](https://arxiv.org/abs/2503.13630)&rbrack;

The seed of quantum mechanics was sown in 

* [[Max Planck]] (transl. M. Martius) *The Theory of Heat Radiation* (1914) &lbrack;[pdf](https://www.gutenberg.org/files/40030/40030-pdf.pdf)&rbrack;

with the recognition of a quantum of "action": [[Planck's constant]] ([p. 164](https://www.gutenberg.org/files/40030/40030-pdf.pdf#page=178))

Quantum mechanics as such originates with:

* [[Werner Heisenberg]], *Über quantentheoretische Umdeutung kinematischer und mechanischer Beziehungen*, Zeitschrift für Physik **33** (1925) 879–893 &lbrack;[doi:10.1007/BF01328377]( https://doi.org/10.1007/BF01328377), [Engl. pdf](http://users.mat.unimi.it/users/galgani/arch/heis25ajp.pdf)&rbrack;

* [[Max Born]], [[Pascual Jordan]], *Zur Quantenmechanik*, Zeitschrift für Physik **34** (1925) 858–888 &lbrack;[doi:10.1007/BF01328531](https://doi.org/10.1007/BF01328531)&rbrack;

* [[Paul A. M. Dirac]], *On the theory of quantum mechanics*, Proceedings of the Royal Society **112** 762 (1926) &lbrack;[doi:10.1098/rspa.1926.0133](https://doi.org/10.1098/rspa.1926.0133)&rbrack;

*  [[Paul A. M. Dirac]], *The physical interpretation of the quantum dynamics*, Proceedings of the Royal Society of London **113** 765 (1927) &lbrack;[doi:10.1098/rspa.1927.0012](https://doi.org/10.1098/rspa.1927.0012)&rbrack;

* {#HilbertvonNeumannNordheim} [[David Hilbert]], [[John von Neumann]], [[Lothar W. Nordheim]], *Über die Grundlagen der Quantenmechanik*,  Math. Ann. **98** (1928) 1–30 &lbrack;[doi:10.1007/BF01451579](https://doi.org/10.1007/BF01451579)&rbrack;

Formulating the [[Born rule]]:

* {#Born26a} [[Max Born]], *Zur Quantenmechanik der Stoßvorgänge*, Zeitschrift für Physik **37** (1926) 863–867 &lbrack;[doi:10.1007/BF01397477](https://doi.org/10.1007/BF01397477)&rbrack;

* {#Born26b} [[Max Born]], *Quantenmechanik der Stoßvorgänge*, Zeitschrift für Physik **38** (1926) 803–827 &lbrack;[doi:10.1007/BF01397184](https://doi.org/10.1007/BF01397184)&rbrack;

* {#Born72} [[Max Born]], *Das Adiabatenprinzip in der Quantenmechanik*, Zeitschrift für Physik **40** (1927) 167–192 &lbrack;[doi:10.1007/BF01400360](https://doi.org/10.1007/BF01400360)&rbrack;

* [[Pascual Jordan]], *Über eine neue Begründung der Quantenmechanik*, Zeitschrift für Physik **40** (1927) 809–838 &lbrack;[doi:10.1007/BF01390903](https://doi.org/10.1007/BF01390903)&rbrack;

Introducing the [[Hilbert space]]-formulation (and the [[projection postulate]]):

* Von Neumann's 1927 Trilogy on the Foundations of Quantum Mechanics (annotated translations by Anthony Duncan) &lbrack;[arXiv:2406.02149](https://arxiv.org/abs/2406.02149)&rbrack;

* [[John von Neumann]]: 

  *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

but see (on [[John von Neumann|von Neumann]]'s further reasoning regarding [[quantum logic]] and then of [[von Neumann algebra factors]]):

* [[Miklos Rédei]], *Why John von Neumann did not Like the Hilbert Space formalism of quantum mechanics (and what he liked instead)*, Studies in History and Philosophy of Modern Physics **27** 4 (1996) 493-510 &lbrack;<a href="https://doi.org/10.1016/S1355-2198(96)00017-2">doi:10.1016/S1355-2198(96)00017-2</a>&rbrack;


Equivalence of the [[Heisenberg picture]] and the [[Schrödinger picture]]:

* [[Erwin Schrödinger]], *Über das Verhältnis der Heisenberg-Born-Jordanschen Quantenmechanik zu der meinen*, Annalen der Physil **384** 8 (1926) 734-756 &lbrack;[doi:10.1002/andp.19263840804]( https://doi.org/10.1002/andp.19263840804)&rbrack;

* [[Carl Eckart]], *Operator Calculus and the Solution of the Equations of Quantum Dynamics*, Phys. Rev. **28** 4  (1926) 711-726 &lbrack;[doi:10.1103/PhysRev.28.711](https://doi.org/10.1103/PhysRev.28.711)&rbrack;

Introducing the tool of [[group theory]] to quantum physics (cf. *[[Gruppenpest]]*):

* [[Hermann Weyl]], *Quantenmechanik und Gruppentheorie*, Zeitschrift für Physik **46** (1927) 1–46 &lbrack;[doi:10.1007/BF02055756](https://doi.org/10.1007/BF02055756)&rbrack;

* [[Hermann Weyl]], *Gruppentheorie und Quantenmechanik*, S. Hirzel, Leipzig, (1931), translated by H. P. Robertson: *The Theory of Groups and Quantum Mechanics* Dover (1950) &lbrack;[ISBN:0486602699](https://store.doverpublications.com/0486602699.html), [ark:/13960/t1kh1w36w](https://archive.org/details/ost-chemistry-quantumtheoryofa029235mbp/page/n15/mode/2up)&rbrack;

* {#Wigner31} [[Eugene P. Wigner]]: *Gruppentheorie und ihre Anwendung auf die Quantenmechanik der Atomspektren*, Springer (1931) &lbrack;[doi:10.1007/978-3-663-02555-9](https://doi.org/10.1007/978-3-663-02555-9), [pdf](https://digbib.ubka.uni-karlsruhe.de/volltexte/wasbleibt/33355459/33355459.pdf)&rbrack;

* [[Eugene P. Wigner]]: *Group theory: And its application to the quantum mechanics of atomic spectra*, 5, Academic
Press (1959) &lbrack;[doi:978-0-12-750550-3](https://www.elsevier.com/books/group-theory/wigner/978-0-12-750550-3)&rbrack;

Early discussion of [[composite quantum systems]] and their [[quantum entanglement]]:

* [[Erwin Schrödinger]], *Discussion of Probability Relations between Separated Systems*, Mathematical Proceedings of the Cambridge Philosophical Society, **31** 4 (1935) 555-563 &lbrack;[doi:10.1017/S0305004100013554](https://doi.org/10.1017/S0305004100013554)&rbrack;

On the historical origin of the [[canonical commutation relations]]:

* [[Severino C. Coutinho]], *The Many Avatars of a Simple Algebra*, The American Mathematical Monthly **104** 7 (1997) 593-604 &lbrack;[doi:10.2307/2975052](https://doi.org/10.2307/2975052), [jstor:2975052](https://www.jstor.org/stable/2975052)&rbrack;



### General
 {#ReferencesGeneral}

Classical textbook accounts: 

* {#Dirac78} [[Paul Dirac]], *[[The Principles of Quantum Mechanics]]*, International series of monographs on physics, Oxford University Press (1930, 1935, 1947) &lbrack;[ISBN:9780198520115](https://global.oup.com/academic/product/the-principles-of-quantum-mechanics-9780198520115)&rbrack;

* {#Mackey63} [[George Mackey]], *The Mathematical Foundations of Quantum Mechanics: a Lecture-note Volume*, Mathematical physics monograph series, Benjamin (1963), Dover (2004) &lbrack;[google books](https://books.google.de/books?id=qlpb2mWYmfYC&printsec=frontcover&hl=de&source=gbs_ge_summary_r&cad=0#v=onepage&q&f=false)&rbrack;
  > (including an influential proposal for [[quantum logic]])

* [[James D. Bjorken]], [[Sidney D. Drell]]: *Relativistic Quantum Mechanics*, McGrawHill (1964) &lbrack;[ark:/13960/t5fc2v05h](https://archive.org/details/relativisticquan0000bjor/page/n1/mode/2up), [pdf](https://emineter.wordpress.com/wp-content/uploads/2018/10/james-d-bjorken-sidney-d-drell-relativistic-quantum-mechanics-1964.pdf), [pdf](http://www.mmmut.ac.in/News_content/14331tpnews_11122020.pdf)&rbrack;
 > (focus on [[relativistic particles]]: [[Klein-Gordon equation]], [[Dirac equation]] towards [[perturbative quantum field theory]])

* Eduard Prugovecki, _Quantum mechanics in Hilbert Space_. Academic Press (1971) &lbrack;[ISBN: 9780080874081](https://www.elsevier.com/books/quantum-mechanics-in-hilbert-space/prugovecki/978-0-12-566060-0)&rbrack;

* {#Scheibe73} [[Erhard Scheibe]], _The logical analysis of quantum mechanics_, Pergamon Press Oxford (1973)
  > (focus on the [[interpretation of quantum mechanics]])

* {#BratteliRobinson79} [[Ola Bratteli]], [[Derek W. Robinson]], *Operator Algebras and Quantum Statistical Mechanics* -- vol 1: *$C^\ast$- and $W^\ast$-Algebras. Symmetry Groups. Decomposition of States.*, Springer (1979, 1987, 2002) &lbrack;[doi:10.1007/978-3-662-02520-8](https://doi.org/10.1007/978-3-662-02520-8)&rbrack;
  > ([[AQFT|algebraic]] [[quantum statistical mechanics]])


* [[James Glimm]], [[Arthur Jaffe]], *[[Glimm-Jaffe|Quantum physics: a functional integral point of view]]*, Springer (1981, 1987) &lbrack;[doi:10.1007/978-1-4612-4728-9](https://doi.org/10.1007/978-1-4612-4728-9)&rbrack;
  > (focus on the [[path integral]] in [[constructive quantum field theory]])

* [[Hans Primas]], *Chemistry, Quantum Mechanics and Reductionism*, Springer (1983) &lbrack;[doi:10.1007/978-3-642-69365-6](https://doi.org/10.1007/978-3-642-69365-6)&rbrack;
  > (with an eye towards [[quantum chemistry]] and [[interpretation of quantum mechanics]])
  
* [[Anthony Sudbery]], *Quantum mechanics and the particles of nature: an outline for mathematicians*, Cambridge University Press (1986) &lbrack;[pdf](http://users.uoa.gr/~navidcon/sudbery.pdf), [spire:240835](https://inspirehep.net/literature/240835)&rbrack;

* {#Kraus} [[Karl Kraus]], *States, Effects, and Operations -- Fundamental Notions of Quantum Theory*, Lecture Notes in Physics **190** Springer (1983) &lbrack;[doi:10.1007/3-540-12732-1](https://doi.org/10.1007/3-540-12732-1)&rbrack;
  > (emphasis on [[effect algebras]] and [[quantum operations]])

* [[Jun John Sakurai]], Jim Napolitano, *Modern Quantum Mechanics*, Cambridge University Press (1985, 2020) &lbrack;[doi:10.1017/9781108587280](https://doi.org/10.1017/9781108587280), [Wikipedia](https://en.wikipedia.org/wiki/Modern_Quantum_Mechanics)&rbrack;


More recent textbook accounts:

* [[Paul Busch]], Marian Grabowski, [[Pekka J. Lahti]], *Operational Quantum Physics*, Lecture Notes in Physics Monographs **31**, Springer (1995) &lbrack;[doi:10.1007/978-3-540-49239-9](https://doi.org/10.1007/978-3-540-49239-9)&rbrack;
  > (perspective of [[quantum probability theory]] via [[POVMs]])

* [[Chris Isham]], *Lectures on Quantum Theory -- Mathematical and Structural Foundations*, World Scientific (1995) &lbrack;[doi:10.1142/p001](https://doi.org/10.1142/p001), [ark:/13960/t4xh7cs99](https://archive.org/details/lecturesonquantu0000isha)&rbrack;

* [[Klaas Landsman]], *[[Mathematical Topics Between Classical and Quantum Mechanics]]*, Springer (1998) &lbrack;[doi:10.1007/978-1-4612-1680-3](https://doi.org/10.1007/978-1-4612-1680-3)&rbrack;

* [[Robert B. Griffiths]], *Consistent Quantum Theory*, Cambridge University Press (2002) &lbrack;[doi:10.1017/CBO9780511606052](https://doi.org/10.1017/CBO9780511606052), [webpage](https://quantum.phys.cmu.edu/CQT)&rbrack;

* [[Mikio Nakahara]], Chapter 1 of: _[[Geometry, Topology and Physics]]_, IOP (2003) &lbrack;[doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>&rbrack;

* [[Serge Haroche]], [[Jean-Michel Raimond]], *Exploring the Quantum: Atoms, Cavities, and Photons*, Oxford University Press (2006) &lbrack;[doi:10.1093/acprof:oso/9780198509141.001.0001](https://doi.org/10.1093/acprof:oso/9780198509141.001.0001)&rbrack;
 
* [[Ingemar Bengtsson]], [[Karol Życzkowski]], *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048)&rbrack;
  > (focus on the [[geometry]] of [[quantum state spaces]] and culminating in a chapter on [[quantum entanglement]])

* [[Heinz-Peter Breuer]], [[Francesco Petruccione]], *The Theory of Open Quantum Systems*, Oxford University Press (2007) &lbrack;[doi:10.1093/acprof:oso/9780199213900.001.0001](https://doi.org/10.1093/acprof:oso/9780199213900.001.0001)&rbrack;
  > (focus on [[open quantum systems]])

* [[Teiko Heinosaari]], [[Mário Ziman]], *The Mathematical Language of Quantum Theory -- From Uncertainty to Entanglement*, Cambridge University Press  (2011) &lbrack;[doi:10.1017/CBO9781139031103]( https://doi.org/10.1017/CBO9781139031103)&rbrack;

* [[Nik Weaver]], *Mathematical Quantization*, Routledge (2011) &lbrack;[ISBN 9781584880011](https://www.routledge.com/Mathematical-Quantization/Weaver/p/book/9781584880011)&rbrack;


* [[Thomas L. Curtright]], [[David B. Fairlie]], [[Cosmas K. Zachos]], *A Concise Treatise on Quantum Mechanics in Phase Space*, World Scientific (2014) &lbrack;[doi:10.1142/8870](https://doi.org/10.1142/8870)&rbrack;
  > (in [[Weyl quantization]])


* [[Paul Busch]], [[Pekka J. Lahti]], Juha-Pekka Pellonpää, Kari Ylinen, *Quantum Measurement*, Springer (2016) &lbrack;[doi:10.1007/978-3-319-43389-9](https://doi.org/10.1007/978-3-319-43389-9)&rbrack;
  > (perspective of [[quantum probability]] via [[POVMs]])


* {#Landsman17} [[Klaas Landsman]], *Foundations of quantum theory -- From classical concepts to Operator algebras*, Springer Open (2017) &lbrack;[doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf)&rbrack;
  > With a focus on the relationship between quantum mechanics and [[representation theory]]

* [[Peter Woit]], *Quantum Theory, Groups and Representations: An Introduction*, Springer (2017) &lbrack;[doi:10.1007/978-3-319-64612-1](https://doi.org/10.1007/978-3-319-64612-1), ISBN:978-3-319-64610-7&rbrack;

On the [[interpretation of quantum mechanics]]:

* [[Roland Omnès]], *[[The Interpretation of Quantum Mechanics]]*, Princeton University Press (1994) &lbrack;[ISBN:9780691036694](http://press.princeton.edu/titles/5525.html)&rbrack;

Lecture notes:

* [[Robert Geroch]], *Geometrical Quantum Mechanics*, University of Chicago (1974) &lbrack;[pdf](http://strangebeautiful.com/other-texts/geroch-geom-qm.pdf), [[Geroch-GeometricalQuantumMechanics.pdf:file]]&rbrack;

* Uni Bonn, _[Lecture scripts and Online courses -- Quantum mechanics](https://web.archive.org/web/20001101031920/http://www-cip.physik.uni-bonn.de/~baehren/scripts/quantum.html)_

* [[Valter Moretti]], *Mathematical Foundations of Quantum Mechanics: An Advanced Short Course*, Int. J. Geom. Methods Mod. Phys. **13** Supp. 1 (2016) 1630011 &lbrack;[arXiv:1508.06951](http://arxiv.org/abs/1508.06951), [doi:10.1142/S0219887816300117](https://doi.org/10.1142/S0219887816300117)&rbrack;


* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;

  > (with an eye towards [[quantum probability]] and [[quantum computation]])

* [[Stéphane Attal]], *Quantum Mechanics*, Lecture 5 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Quantum_Mechanics.pdf), [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;

  > (with an eye towards [[quantum probability]] and [[quantum noise]])


Further references:

* {#BatesWeinstein} Sean Bates, [[Alan Weinstein]], _[[Lectures on the geometry of quantization]]_ AMS (1997) &lbrack;[pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)&rbrack;
  > (on [[geometric quantization]])


* [[Pierre Cartier]], [[Cécile DeWitt-Morette]], _Functional integration: action and symmetries_, Cambridge Monographs on Mathematical Physics (2006) &lbrack;[ISBN:9780521143578](https://www.cambridge.org/ae/academic/subjects/physics/theoretical-physics-and-mathematical-physics/functional-integration-action-and-symmetries?format=PB#contentsTabAnchor)&rbrack;
  > (on rigorous [[path integrals]])

* [[Leon A. Takhtajan]]: _[[Quantum mechanics for mathematicians]]_, Amer. Math. Soc. (2008) &lbrack;[ISBN:978-0-8218-4630-8](https://bookstore.ams.org/gsm-95)&rbrack;

* Michael Movshev, *Concepts of Quantum Mechanics* (2008) &lbrack;[web](http://www.math.sunysb.edu/~mmovshev/MAT570Spring2008/syllabusfinal.html)&rbrack; 

* [[Franco Strocchi]], *An introduction to the mathematical structure of quantum mechanics*, Advanced Series in Mathematical Physics **28**, World Scientific (2008) &lbrack;[doi:10.1142/7038](https://doi.org/10.1142/7038)&rbrack;

* [[Steven Weinberg]], *Lectures on Quantum Mechanics*, Cambridge University Press (2015) &lbrack;[doi:10.1017/CBO9781316276105](https://doi.org/10.1017/CBO9781316276105)&rbrack;

* [[Valter Moretti]], _Spectral Theory and Quantum Mechanics -- Mathematical Foundations of Quantum Theories, Symmetries and Introduction to the Algebraic Formulation_, Springer (2017) &lbrack;[doi:10.1007/978-3-319-70706-8](https://doi.org/10.1007/978-3-319-70706-8)&rbrack;

* [[Valter Moretti]], *Fundamental Mathematical Structures of Quantum Theory* -- *Spectral Theory, Foundational Issues, Symmetries, Algebraic Formulation*, Springer (2020) &lbrack;[doi:10.1007/978-3-030-18346-2](https://doi.org/10.1007/978-3-030-18346-2)&rbrack; 

* Jan Perina, Z. Hradil, [[Branislav Jurčo]], _[[Quantum optics and fundamentals of physics]]_, Kluwer 1994


Introduction to mathematical foundations of quantum physics in [[quantum probability]], [[operator algebra]]:

* {#Gleason09} [[Jonathan Gleason]], *The $C^*$-algebraic formalism of quantum mechanics* (2009) &lbrack;[[Gleason09.pdf:file]], [[GleasonAlgebraic.pdf:file]]&rbrack;

* {#Gleason11} [[Jonathan Gleason]], *From Classical to Quantum: The $F^\ast$-Algebraic Approach*, contribution to *[VIGRE REU 2011](http://www.math.uchicago.edu/~may/VIGRE/VIGREREU2011.html)*, Chicago (2011) &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Gleason.pdf), [[GleasonFAlgebraic.pdf:file]]&rbrack;

* {#FroehlichSchubnel15} [[Jürg Fröhlich]],  B. Schubnel, _Quantum Probability Theory and the Foundations of Quantum Mechanics_. In: Blanchard P., Fröhlich J. (eds.) _The Message of Quantum Science_. Lecture Notes in Physics, vol 899. Springer 2015 ([arXiv:1310.1484](https://arxiv.org/abs/1310.1484), [doi:10.1007/978-3-662-46422-9_7](https://doi.org/10.1007/978-3-662-46422-9_7))

* {#Froehlich} [[Jürg Fröhlich]], _The structure of quantum theory_, Chapter 6 in _The quest for laws and structure_, EMS 2016  ([doi](https://www.researchgate.net/publication/308595814_The_Quest_for_Laws_and_Structure), [doi:10.4171/164-1/8](https://www.ems-ph.org/books/show_abstract.php?proj_nr=207&vol=1&rank=8)).

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




[[!include quantum observables as groupoid convolution -- references]]





[[!include quantum information theory via string diagrams -- references]]




[[!redirects quantum physics]]
[[!redirects quantum theory]]

[[!redirects quantum mechanical system]]
[[!redirects quantum mechanical systems]]