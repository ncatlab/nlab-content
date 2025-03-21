
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Classical mechanics is that part of [[classical physics]] dealing with the deterministic physics of point [[particle|particles]] and rigid bodies; often the systems with the infinitely many degrees of freedom are also included (like infinite arrays of particles and their continuous limits like classical mechanics of strings, membranes, elastic media and of classical fields). For the continuous systems, the equations of motion can often be explained by the partial differential equations, describing classical [[physical field|physical fields]] of quantities (typically smooth possibly vector valued functions on manifolds), including background fields like metric; the latter (sub)area is the [[classical field theory]], but it is often studied separately from the classical mechanics of the finite systems of particles; especially if non-classical features or interpretations are involved (e.g. supersymmetry, or unusual case of non-variational  equations of motion etc.). In Hamiltonian reduction, due to conservation laws, many systems with infinitely many degrees of freedom, reduce to the finite ones. 

Nondissipative systems with finitely many degrees of freedom may be described geometrically using [[symplectic manifolds]], or more generally [[Poisson manifolds]]; the later may also sometimes appear as reductions of the systems with infinitely many degrees of freedom. 

Classical mechanics of a system of point particles and rigid bodies is usually divided into statics, kinematics and dynamics. __Statics__ studies the balance of forces in a system which does not move, or in a stationary flow. __Kinematics__ studies the relation between position, velocity and acceleration of bodies in a mechanical system, without reference to the causes of motion. __Dynamics__ studies motion with reference to the causes of motion and interaction between bodies and its manifestation via (quantified) [[force|forces]], energy and mass assigned to bodies in motion and interaction.

For a theoretical classical mechanics one often starts with a concrete system of bodies with pulleys, strings, spins, external and internal forces, and dissipative sinks and sources (e.g. friction forces), which are then analysed to get the configuration or phase space of the system, the equations of motion and possibly to determine some special [[observable|observables]] of interest. Once abstracted that way, the rest of the study is a rather special case of the theory of [[dynamical system|dynamical systems]], which itself studies general (either deterministic or stochastic) spatially-parametrized systems in a (discrete or continuous) time evolution. 

A terminological and scope discussion is archived [here](https://nforum.ncatlab.org/comments.php?DiscussionID=2807&Focus=23543#Comment_23543).

## Traditional formulation

The fundamental distinction is between open and closed mechanical systems. Open systems have exchange of energy with the rest of universe, that is with the energy sources or sinks which are not described by the mechanical system: for example the energy can be absorbed through forces from external bodies not belonging to the system but accounted in terms of such forces, or the energy can be lost by heating (described by friction force and alike). Closed systems are conservative in energetic sense. The terminology open/closed is wider than conservative/nonconservative, as it pertains also to statistical and quantum systems. 

The standard formalisms for classical mechanics are Newtonian mechanics, Lagrangean formalism, and the Hamiltonian formalism which can be studied in the generality of symplectic manifolds and more general (allowing degeneracies) formalism of Poisson manifolds; Poisson manifolds can generalize to he study of somewhat nonclassically to (the opposite of) more general Poisson algebras. 

### Newtonian formalism

...

### Lagrangean formalism

...

### Hamiltonian formalism and symplectic manifolds

(...) [[symplectic manifold]], [[Hamiltonian]]  (...)

###  Mechanical systems based on Poisson algebras

We set up some basic notions of classical mechanics. 

+-- {: .num_defn}
###### Definition

A _real [[Poisson algebra]]_ is a unital (commutative) [[associative algebra]] $(A, \dot)$ over the [[real number|real numbers]] that is equipped with with an additional bilinear operation

$$
  [-,-] : A \otimes_{\mathbb{R}} A \to A 
$$

that makes $A$ into a [[Lie algebra]] such that for each element $a \in A$ the operation $[a,-] : A \to A$ is a [[derivation]] of the product $\cdot : A \otimes A \to A$.

This definition readily generalized to symmetric monoidal categories. For example, a real _super Poisson algebra_ is a graded-commutative [[superalgebra]] equipped with the compatible structure of a [[super Lie algebra]].

A _[[homomorphism]]_ $(A, \dot, [-,-]) \to (B, \cdot, [-,-])$ of (super) Poisson algebras is a [[linear function]] $A \to B$ that respects both the associative product and the Lie bracket.

Write [[Poiss]] for the resulting category of 
(super) Poisson algebras. 

=--

The standard setup of conservative classical mechanical system is a Poisson manifold. 

+-- {: .num_defn #PoissonManifoldExample}
###### Definition - principal example

A [[Poisson manifold]] is a smooth real manifold $M$ equipped with a Poisson structure (that is the Poisson bracket) on the commutative algebra $C^\infty(M)$ of smooth real valued functions on $M$. 
=--

Recall that every [[symplectic manifold]] provides an example of a Poisson manifold. Possibly infinite-dimensional generalization of this example is called a [[phase space]]. Hence commutative Poisson algebras should be viewed as formal opposites to phase spaces in a generalized sense. 


+-- {: .num_defn #ClassMechSys}
###### Definition

The [[opposite category]] of that of commutative real (super) Poisson algebras we call the category of **classical mechanical systems**

$$
  ClassMechSys \coloneqq CPoiss^{op}
  \,.
$$ 

=--

+-- {: .num_remark }
###### Remark

Poisson superalgebras describe systems with [[fermion|fermions]]. Systems without fermions may be described by plain Poisson algebras.

=--

+-- {: .num_remark }
###### Remark

This definition captures most notions of "mechanical systems". Exceptions contain 
[[open system|open systems]] for which there is no conservation laws (examples: externally-driven 
and [[dissipative system|dissipative systems]]). In real worlds, physicists believe that such systems may be realized only as parts of larger systems (eventually, the universe) which are conservative; hence either describable by a Poisson algebra or it entails energy types which can not be described using classical mechanics. 

=--

+-- {: .num_remark}
###### Remark

For $(A, \cdot, \{-,-\})$ a Poisson algebra, $A$ together with its [[module]] $\Omega^1(A)$ of [[Kähler differential|Kähler differentials]] naturally form a [[Lie-Rinehart pair]], with bracket given by

$$
  [d a, d b ] \coloneqq d \{a,b\}
  \,.
$$

If the Poisson algebra comes from a [[Poisson manifold]] $X$, then this Lie-Rinehart pair is the [[Chevalley-Eilenberg algebra]] of the given [[Poisson Lie algebroid]] over $X$. We can therefore identify classical mechanical systems over a phase space manifold also with Poisson Lie algebroids. 

=--


### Observables and states

+-- {: .num_defn}
###### Definition

Given $S \coloneqq (A,\cdot, \{-,-\})$ a classical mechanical system, we say

* an **[[observable]]** of $S$ is an element $a \in A$, hence we call $A$ the **algebra of observables**;

* a **[[classical state]]** of $S$ is 

  * a [[linear function]] $\rho : A \to \mathbb{R}$;

    * which is **positive** in that for all $a \in A$ we have that

      $\rho(a \cdot a) \geq 0$;

    * and which is **normalized** in that $\rho(1) = 1$.

* a **[[pure state]]** of $S$ is a state that is not only a linear map, but even an [[associative algebra]] [[homomorphism]] $\rho : A \to \mathbb{R}$.

Write $States((A, \cdot))$ for the set of states of $A$. 

For $\rho \in States$ and $a \in A$ we say that $\rho(a)$ is the **value of the observable $a$ on the system in state $\rho$**.

=--

+-- {: .num_remark}
###### Remark

If the classical mechanical system comes from a [[Poisson manifold]] $(X, \{-,-\})$ by 
example \ref{PoissonManifoldExample}, then the pure states correspond precisely to the points of the manifold $X$. So each point of $X$ is one _specific_ (= "pure") state that the mechanical system defined by $(X, \{-,-\})$ can be in, whereas a general state $\rho : A \to \mathbb{R}$ is a distribution of such specific states.

=--

### Flows and evolution

Let $M$ be a [[Poisson manifold]], possibly infinite-dimensional with $A = C^\infty(M)$. More generally, $A$ can be a Poisson algebra with a good notion of weak topology and corresponding notion of a derivative. 

+-- {: .num_remark}
###### Remark

For any observable $a \in A$ we say that a **1-parameter flow induced by the observable** is, if it exists, an [[action]] of the [[real number|real numbers]] on the observables

$$
  F_a : \mathbb{R} \times A \to A
$$

which is [[differentiation|differentiable]] in $\mathbb{R}$ and satisfies for all $b \in A$ the [[differential equation]]

$$
  \frac{d}{d t} F_a(b) (t) = \{a,b\}
  \,.
$$

with initial value $F_a(b)(0) = b$. The differentiation is understood pointwise on $M$ (pointwise we get to differentiate a function $\mathbb{R}\to\mathbb{R}$). 

=--

In non-relativistic classical mechanics every system comes up with a choice of one element $H \in A$ and declare that the corresponding flow is the _time evolution_ of observables of the system. One calls this $H$ the **[[Hamiltonian]]** or *energy observable* of the system. The physical meaning, however, does not change if $H$ is changed by an overall constant. 

### Quantization

+-- {: .num_defn}
###### Definition

Write $StarAlg_{\mathbb{C}}$ for the category of [[star-algebra|star-algebras]] over the [[complex number|complex numbers]]. 

The [[opposite category]]

$$
  QuantMechSys \coloneqq StarAlg^{op}
$$

we call the category of **[[quantum mechanical systems]]**.

=--

+-- {: .num_defn}
###### Definition

For $(A, \cdot, \{-,-\})$ a classical mechanical system, 
def. \ref{ClassMechSys}, a **[[quantization]]** of it is -- if it exists --

* a 1-parameter [[field of star-algebras]] $\{A_\hbar\}_{\hbar \in [0,\infty)}$;

* such that in the limit $\hbar \to 0$ we have

  1. $A_\hbar \to A_0 \coloneqq A \otimes_{\mathbb{R}}\mathbb{C}$;

  1. for all $a,b \in A_{\hbar}$: $\frac{1}{i \hbar } [a,b] = \{a,b\}$.

Conversely, given a quantum mechanical system $(A, \ast)$ and a field of star-algebras such that $A = A_1$, then we call the clasical system $A_0$ its (or rather: a)**[[classical limit]]**.

=--

## Formulation in higher geometry by local prequantum field theory

Traditional classical mechanics ([[Hamiltonian mechanics]], [[Lagrangian mechanics]], [[Hamilton-Jacobi theory]]) is naturally understood as a special case of -- and in fact as deriving from -- [[local prequantum field theory]] formulated in the [[higher differential geometry]] over $\mathbf{B}U(1)_{conn}$. This is discussed in some detail at

* _[[prequantized Lagrangian correspondence]]_.


## Particular classical systems

* [[Hamiltonian dynamics on Lie groups]]

  * [[rigid body dynamics]]

## Related concepts

* [[mechanics]], [[Poisson manifold]], [[symplectic manifold]], [[contact manifold]]

* [[continuum mechanics]]

* [[semiclassical approximation]]

* [[classical anomaly]]

* [[quantization]]: [[deformation quantization]], [[geometric quantization]]

* [[quantum mechanics]], [[supersymmetric quantum mechanics]]

* [[quantum field theory]]: [[FQFT]], [[AQFT]]

* [[generating function in classical mechanics]], 


## References

The origin of [[Newton's laws of motion]]:

* {#Newton1687} [[Isaac Newton]], *[[Philosophiæ naturalis principia mathematica]]* (1687)


Classical textbooks:

* [[Tom W. B. Kibble]], [[Frank Berkshire]], *Classical mechanics*, McGraw-Hill (1966, 1973, 2004) &lbrack;[pdf](https://physicaeducator.files.wordpress.com/2018/02/classical-mechanics-by-kibble-and-berkshire.pdf), <a href="https://en.wikipedia.org/wiki/Classical_Mechanics_(Kibble_and_Berkshire)">Wikipedia entry</a>&rbrack;

* [[Vladimir Arnol'd]], _[[Mathematical methods of classical mechanics]]_, Graduate Texts in Mathematics **60**, Springer (1978) &lbrack;[doi:10.1007/978-1-4757-1693-1](https://doi.org/10.1007/978-1-4757-1693-1)&rbrack;

* [[Ralph Abraham]], [[Jerrold E. Marsden]]: _[[Foundations of Mechanics]]_, Second Edition, Addison-Wesley (1978) &lbrack;ISBN:978-0-8218-4438-0, [pdf](http://authors.library.caltech.edu/25029/1/FoM2.pdf)&rbrack;  Reprinted: Chelsea Publishing **364**, AMS (1978)  &lbrack;[doi:10.1090/chel/364](https://doi.org/10.1090/chel/364)&rbrack;
* [[Lev Landau]], [[Evgeny Lifshitz]], _Classical mechanics_, vol. I of the *[[Course of Theoretical Physics]]*

* [[Michael Spivak]], _Elementary mechanics from a mathematician's viewpoint_ ([pdf](http://alpha.math.uga.edu/~shifrin/Spivak_physics.pdf))

See also:

* {#Warner09} [[Garth Warner]]: *Lagrangian Mechanics*, EPrint Collection, University of Washington (2009) &lbrack;[hdl:1773/4606](http://hdl.handle.net/1773/4606), [pdf](https://sites.math.washington.edu//~warner/LM_Warner.pdf), [[WarnerLagrangianMechanics.pdf:file]]&rbrack;


Detailed exposition with emphasis on the [[principle of extremal action]]:



* [[Douglas Cline]], *Variational Principles in Classical Mechanics*, University of Rochester (2021) &lbrack;[pdf](http://classicalmechanics.lib.rochester.edu/pdf/Variational_Principles_in_Classical_Mechanics_3e_final_fbcover.pdf), <a href="https://phys.libretexts.org/Bookshelves/Classical_Mechanics/Variational_Principles_in_Classical_Mechanics_(Cline)">online version</a>&rbrack;


Discussion with an eye also towards [[quantum mechanics]] is in

* [[Klaas Landsman]], _[[Mathematical Topics Between Classical and Quantum Mechanics]]_

See also 

* {#MacLane68} [[Saunders MacLane]], _Geometrical Mechanics_, Lectures 1968 ([web](https://harrydole.com/wp/2017/09/10/saunders-mac-lane-geometrical-mechanics/))

* [[Valter Moretti]], *Analytical Mechanics* -- *Classical, Lagrangian and Hamiltonian Mechanics, Stability Theory, Special Relativity*, Springer (2023) &lbrack;[doi:10.1007/978-3-031-27612-5](https://doi.org/10.1007/978-3-031-27612-5)&rbrack; 


[[!redirects classical mechanical system]]
[[!redirects classical mechanical systems]]
[[!redirects system of classical mechanics]]

[[!redirects Newtonian mechanics]]
