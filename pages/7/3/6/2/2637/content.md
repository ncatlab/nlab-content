

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In contexts related to [[quantum mechanics]] and [[quantum field theory]], by the "canonical commutation relations" (CCR) one refers to the [[commutator]] relations in [[Weyl algebras]], i.e. [[associative algebras]] generated from elements $\{a_k, a^\ast_k\}_{k \in K}$ subject to the "canonical" expressions for the [[commutators]] $[a,b] \coloneqq a \cdot b - b \cdot a$

$$
  \underset{i,j \in K}{\forall} \left(  [a_i, a_j] = 0 = [a^\ast_i, a^\ast_j] \right)
$$

$$
  \underset{i,j \in K}{\forall}\left( [a_i, a^\ast_j] = diag((a_k))_{i, j} \right)
  \,,
$$

where $diag((a_k))$ is some [[diagonal matrix]] with entries $(a_k)_{k \in K}$.

The archetypical example is the [[deformation quantization]] of the simple [[phase space]] which is the [[symplectic vector space]] $\mathbb{R}^2$ equipped with the [[symplectic form]] $\omega = \left( \array{ 0 & -1 \\ 1 & 0 } \right)$. 

The resulting algebra is equivalently the [[quotient]] of the [[universal enveloping algebra]] of the [[Heisenberg Lie algebra]] $h_2$ which identifies the [[center|central element]] with a multiple of the 1 (the multiplicative neutral element, see at _[[polynomial Poisson algebra]]_ for more).

More concretely, in the [[quantization]] of a single particle propagating on the [[real line]] the [[Hilbert space]] of [[quantum states]] is identified with the the space of [[square integrable functions]] $L^2(\mathbb{R})$. On this the operators

$$
  a \coloneqq \tfrac{1}{\sqrt{2}}\left(x + i \hbar \frac{\partial}{\partial x} \right)
  \phantom{AAAAA}
  a^\ast \coloneqq \tfrac{1}{\sqrt{2}}\left(x - i \hbar \frac{\partial}{\partial x}\right)
$$

act (where "$x$" denotes the operator that multiplies a function with the canonical coordinate function, and $\frac{\partial}{\partial x}$ is the operator that forms the [[derivative]] with respect to this coordinate).

These operators satisfy the canonical commutation relations with 

$$  
  [a, a^\ast] = i \hbar
$$

If the particle being quantized here is equipped with [[Hamiltonian]] that represents the [[energy]] of a [[harmonic oscillator]], then one may show that the operator $a$ has the interpretation of removing one quantum of energy from the oscillator, while $a^\ast$ has the interpretation of adding one quantum.

(Accordingly the CCR relations in this case have been argued to be related to the [[combinatorics]] of placing a ball into a box and removing a ball from a box.)

More generally, in the [[quantum field theory]] of the [[free fields|free]] [[scalar field]] on [[Minkowski spacetime]] of [[dimension]] $d+1 \in \mathbb{N}$, each [[Fourier transform|Fourier mode]] [[amplitude]] $a_k$ of the field behaves independently like a [[harmonic oscillator]] and hence the [[Wick algebra]] of [[quantum observables]] of this free field is a [[Weyl algebra]] with a [[countable set]] $\{a_k, a^\ast_k\}_{k \in \mathbb{Z}^d}$ of generator, subject to the "canonical commutation relations"

$$
  [a_k, a^\ast_{k'}] = i \hbar \delta_{k, k'}
$$

(where on the right we have the [[Kronecker delta]]). Now $a_k$ is interpreted as having the effect of "annihilating" a paticle/quantum in mode $k$, while $a_k^\ast$ has the effect of "creating" one. 

Therefore operators satisfying the "canonical commutation relations" are often referred to as (particle) _creation and annihilation operators_.

One a curved [[spacetime]] these relations become more complicated, see at _[[Wick algebra]]_ for more.

If the field in question is not a [[bosonic field]] but a [[fermionic field]] then all of the above has to be understood in [[superalgebra]] with the fermionic variabled in off super-degree. This yields [[anti-commutator]] relations as above, hence often called "canonical anti-commutation relations".

Under passing to [[exponentials]] the canomical commutation relations are also called the _[[Weyl relations]]_.

## Properties

* The [[Stone-von Neumann theorem]] says that for finitely many generators the canonical commutation relations (in the form of the [[Weyl relations]]) have, up to [[isomorphism]], a unique [[irreducible representation|irreducible]] [[unitary representation]]: the _[[Schrödinger representation]]_.

  [[Haag's theorem]] says that this uniqueness fails for infinitely many generators.

## Related concepts

* [[Weyl relation]], [[Weyl algebra]]

* [[Heisenberg algebra]]

* [[Stone-von Neumann theorem]]

* [[Wick algebra]]

* [[singleton representation]]

## References

Original discussion:

* {#Weyl27} [[Hermann Weyl]], (36) in: *Quantenmechanik und Gruppentheorie*, Zeitschrift für Physik **46** (1927) 1–46 &lbrack;[doi:10.1007/BF02055756](https://doi.org/10.1007/BF02055756)&rbrack;


More on the history of the notion:

* [[Severino C. Coutinho]], Introduction to: *A primer of algebraic D-modules*, London Math. Soc. Stud. Texts **33**, Cambridge University Press (1995) &lbrack;[doi:10.1017/CBO9780511623653](https://doi.org/10.1017/CBO9780511623653)&rbrack;

* [[Severino C. Coutinho]], *The Many Avatars of a Simple Algebra*, The American Mathematical Monthly **104** 7 (1997) 593-604 &lbrack;[doi:10.2307/2975052](https://doi.org/10.2307/2975052), [jstor:2975052](https://www.jstor.org/stable/2975052)&rbrack;

Review:

* Jan Dereziński: _Introduction to Representations of the Canonical Commutation and Anticommutation Relations_, in: _Large Coulomb Systems --- QED_, Lecture Notes in Physics **695**, Springer (2006) 63-143 &lbrack;[doi:10.1007/3-540-32579-4_3](https://doi.org/10.1007/3-540-32579-4_3), [arXiv:math-ph/0511030](https://arxiv.org/abs/math-ph/0511030)&rbrack;

Monograph on [[commutators]] in [[operator algebra]]:

* [[Calvin R. Putnam]], *Commutation Properties of Hilbert Space Operators and Related Topics*, Ergebnisse der Mathematik und ihrer Grenzgebiete **36**, Springer (1967) &lbrack;[doi:10.1007/978-3-642-85938-0](https://doi.org/10.1007/978-3-642-85938-0)&rbrack;

See also:

* [[Elisa Ercolessi]], [[Giuseppe Marmo]], Giuseppe Morandi, *From the Equations of Motion to the Canonical Commutation Relations*, Riv. Nuovo Cim. **33** (2010) 401-590 &lbrack;[arXiv:1005.1164](https://arxiv.org/abs/1005.1164), [doi:10.1393/ncr/i2010-10057-x](https://doi.org/10.1393/ncr/i2010-10057-x)&rbrack;


[[!redirects canonical commutation relations]]

[[!redirects canonical anti-commutation relation]]
[[!redirects canonical anti-commutation relations]]

[[!redirects creation and annihilation operators]]

[[!redirects CCR]]
