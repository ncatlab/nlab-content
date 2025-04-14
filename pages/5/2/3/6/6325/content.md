
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### AQFT and operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

The _Stone--von Neumann theorem_ --- due to [Stone 1930](#Stone1930), [von Neumann 1931](vonNeumann1931)/[32](vonNeumann1932) ---  says that there is, up to [[isomorphism]], a *unique* [[irreducible representation|irreducible]] [[unitary representation]] of the [[Heisenberg group]] on [[finite set|finitely]] many generators, equivalently: of the [[Weyl algebra]], the [[Weyl relations]], the [[canonical commutation relations]].

This was originally motivated from and has special impact in [[quantum mechanics]], where it says that [[phase spaces]] which are [[symplectic vector spaces]], hence of the form $\mathbb{R}^{2n}$ equipped with their canonical [[symplectic form]] (such as describe for instance [[non-relativistic particles]] propagating on [[Euclidean space]] $\mathbb{R}^n$), have an essentially unique [[quantization]] (disregarding the choice of [[quantization]] of further [[observables]] such as [[Hamiltonians]]), namely with half of the [[canonical coordinates]] on $\mathbb{R}^{2n}$ represented as multiplication operators and the remaining [[canonical momenta]] represented as [[partial derivatives]] on [[square integrable functions]].

Curiously, the analogous uniqueness statement does _not_ hold for infinitely many generators as they generically appear in [[quantum field theory]]: this is the statement of _[[Haag's theorem]]_.

It was observed by [Mackey 1949](#Mackey1949) that the Stone-von Neumann theorem naturally generalizes from the usual [[Heisenberg groups]] based on the additive group of [[real numbers]] to analogous Heisenberg groups based on any [[locally compact topological group|locally compact]] [[abelian group]], whence some authors speak of the *Stone-von Neumann-Mackey theorem* (e.g. [Prasad 2011](#Prasad11)). 

For instance, the [[phase space]] of [[abelian Chern-Simons theory]] (a [[quantum field theory]], but "[[TQFT|topological]]", expected to describe [[fractional quantum Hall systems]] at certain filling fractions) over the [[torus]] has as [[algebra of observables]] the *[[integer Heisenberg group]]* which is based on the [[discrete group|discrete]] [[integer]] [[subgroup]] $\mathbb{Z} \hookrightarrow \mathbb{R}$. In this case, Mackey's generalization of the Stone-von Neumann theorem applies and characterizes the [[finite dimensional Hilbert space]] of [states of the theory](abelian+Chern-Simons+theory#SpaceOfQuantumStates) (cf. [Gelca & Uribe 2010 Thm 2.4](#GelcaUribe10), [Gelca & Hamilton 2012](#GelcaHamilton12)/[15](#GelcaHamilton15)).


## Statement

The form of the theorem closest to traditional discussion in [[quantum mechanics]] textbooks is in terms of representations of the [[Lie algebra]] or [[Weyl algebra]] of "[[canonical commutation relations]]"

* *[For canonical commutation remations](#ForCanonicalCommutationRelations)*

But mathematically the theorem has been and is most naturally expressed in terms of the corresponding "exponentiated" operators representing a [[Heisenberg group]].

In this form it is natural to generalize the underlying abelian group $\mathbb{R}$ to any [[locally compact topological group|locally compact]] [[abelian group]]:

* *[For general Heisenberg groups](#ForGeneralHeisenbergGroupsOfAbelianGroups)*

\linebreak

### For canonical commutation relations
 {#ForCanonicalCommutationRelations}


The [[canonical commutation relations]] on two generators ([[canonical coordinate]] $q$ and [[canonical momentum]] $p$) in the form 

$$
  [q,p] = \mathrm{i} \hbar
$$

may be represented as [[unbounded operators]] on the [[Hilbert space]] of [[square integrable functions]] $L^2(\mathbb{R})$ on the [[real line]] by defining them on the [[dense subspace]] of [[smooth functions]] $\psi \colon \mathbb{R} \to \mathbb{C}$ as

$$
  (q \psi)(x) 
    \;\coloneqq\; 
  x \psi(x)
  \phantom{AAAA}
  (p \psi)(x) 
    \;\coloneqq\; 
  -\mathrm{i} \hbar 
  \frac{\partial}{\partial x} \psi(x)
  \,,
$$

where on the right we have the [[partial derivative]] along the canonical [[coordinate function]] on $\mathbb{R}$.

This is often called the _Schrödinger representation_, after [[Erwin Schrödinger]], cf. eg. [Redei](#Redei)

> (to be distinguished from "[[Schrödinger picture]]" which is a related but different concept)


\linebreak


### For general Heisenberg groups of abelian groups
 {#ForGeneralHeisenbergGroupsOfAbelianGroups}

Consider 

* $A$ a [[locally compact topological group|locally compact]] [[topological group|topological]] [[abelian group]],

* $\mathbb{R}/\mathbb{Z}$ the [[circle group]],

* $\widehat A$ the [[Pontrjagin dual group]] of [[continuous map|continuous]] [[group homomorphisms]] $A \xrightarrow{\;} \mathbb{R}/\mathbb{Z}$.

\begin{definition}**(Generalized Heisenberg group)**
\label{GeneralizedHeisenbergGroup}
\linebreak
  The *[[Heisenberg group]]* $H(A)$ is that generated by

* $W_{(a,b)}$ for $a \in A$, $b \in \widehat{A}$

* $\zeta^t$ for $t \in \mathbb{R}/\mathbb{Z}$

subject to the [[group commutator]] relations

$$
  \big[W_{(a,0))},\, W_{(a',0)}\big]
    \;=\; 
  \mathrm{e}
  \,,
  \;\;\;\;
  \big[W_{(0,b)},\, W_{(0,b')} \big]
    \;=\; 
  \mathrm{e}
  \,,
  \;\;\;\;
  [\zeta^t, -] = \mathrm{e}
$$
and
$$
  W_{(0,b)} 
  W_{(a,0)} 
    \;=\; 
  e^{2 \pi \mathrm{i} b(a)}
  \,
  W_{(a,0)} 
  W_{(0,b)} 
  \,.
$$
\end{definition}

\begin{theorem}
\label{MackeyGeneralizationOfStoneVonNeumann}
**(Mackey's generalization of Stone-vonNeumann)**
\linebreak
  On the [[Hilbert space]] $L^2(A)$ of [[square integrable functions]] (with values in [[complex numbers|$\mathbb{C}$]]) over $A$,
the following formulas define a [[unitary representation|unitary]] [[linear representation]] of $H(A)$ (Def. \ref{GeneralizedHeisenbergGroup}):
$$
  \begin{array}{ccccccl}
    H(A) 
      &\xrightarrow{\phantom{---}}& 
    \mathrm{U}\big(L^2(A)\big)
    \\
    W_{(0,b)} 
      &\mapsto& 
    \widehat{W}_{(0,b)} 
        &\colon& 
      f &\mapsto& 
        \big(
          x \mapsto e^{2 \pi \mathrm{i} b(x) }\, f(x)   
        \big)
    \\
    W_{(a,0)}
      &\mapsto&  
    \widehat{W}_{(a,0)}
        &\colon&
      f &\mapsto& 
        \big(
          x \mapsto f( x - a )
        \big)
     \\
     \zeta^t
       &\mapsto&
     \widehat{\zeta}^t
         &\colon&
       f &\mapsto&
         \big(
           x \mapsto e^{2\pi \mathrm{i} t} \, f(x)
         \big)
  \end{array}
$$
which is [[irreducible representation|irreducible]] in that $L^2(A)$ does not have a [[closed subspace|closed]] [[linear subspace|linear]] proper [[subspace]] [[invariant]] under this action. 

Moreover, every other [[continuous map|continuous]] [[unitary representation]] $\widehat{(-)} \colon H(A) \xrightarrow{\;} \mathscr{H}$ on some [[separable Hilbert space|separable]] [[complex number|complex]] [[Hilbert space]] $\mathscr{H}$,  for which $\widehat{\zeta}^t \,=\, e^{2 \pi \mathrm{i}t}\, \mathrm{id}$, is [[isomorphism|isomorphic]] to an [[orthogonality|orthogonal]] [[direct sum]] of copies of this representation. 
\end{theorem}
([Prasad 2011 §4.1](#Prasad11))


## Related concepts

* [[Weyl relation]], [[Weyl algebra]]

* [[canonical commutation relation]]

* For the Schrödinger representation obtained via [[geometric quantization]] see [there](geometric+quantization#ExamplesSchroedingerRepresentation).



## References

### General

The original articles:

* {#Stone1930} [[Marshall H. Stone]]: *Linear transformations in Hilbert space. III. Operational methods and group theory*, Proceedings of the National Academy of Sciences of the United States of America, **16** (1930) 172–175 &lbrack;[jstor:85485](https://www.jstor.org/stable/85485), [doi:10.1073/pnas.16.2.172](https://doi.org/10.1073/pnas.16.2.172)&rbrack;

* {#vonNeumann1931} [[John von Neumann]], *Die Eindeutigkeit der Schrödingerschen Operatoren*, Mathematische Annalen **104**  (1931) 570–578 &lbrack;[doi:10.1007/BF01457956](https://doi.org/10.1007/BF01457956)&rbrack;
 
* {#vonNeumannNeu1932} [[John von Neumann]], _Über Einen Satz Von Herrn M. H. Stone_, Annals of Mathematics, Second Series **33** 3 (1932) 567-573 &lbrack;[doi:10.2307/1968535](https://doi.org/10.2307/1968535), [jstor:1968535](https://www.jstor.org/stable/1968535)&rbrack;

The original generalization to Heisenberg groups of locally compact abelian groups:

* {#Mackey1949} [[George W. Mackey]]: *A theorem of Stone and von Neumann*, Duke Mathematical Journal, **16** (1949) 313–326 &lbrack;[doi:10.1215/S0012-7094-49-01631-2](https://projecteuclid.org/journals/duke-mathematical-journal/volume-16/issue-2/A-theorem-of-Stone-and-von-Neumann/10.1215/S0012-7094-49-01631-2.short)&rbrack;

* [[Marc Rieffel]], _On the uniqueness of the Heisenberg commutation relations_, Duke Math. J. **39**  4 (1972) 745-752 &lbrack;[doi:10.1215/S0012-7094-72-03982-8](https://projecteuclid.org/journals/duke-mathematical-journal/volume-39/issue-4/On-the-uniqueness-of-the-Heisenberg-commutation-relations/10.1215/S0012-7094-72-03982-8.short)&rbrack;


Review:

* {#Prasad11} [[Amritanshu Prasad]]: *An easy proof of the Stone-von Neumann-Mackey theorem*, Expositiones Mathematicae **29** (2011) 110-118 &lbrack;[arXiv:0912.0574](https://arxiv.org/abs/0912.0574), [doi:10.1016/j.exmath.2010.06.001](https://doi.org/10.1016/j.exmath.2010.06.001)&rbrack;

* {#Redei} [[Miklós Rédei]]: _Von Neumann's proof of Uniqueness of Schrödinger representation of Heisenberg's commutation relation_ &lbrack;[[RedeiCCRRepUniqueness.pdf:file]]&rbrack;


See also:

* Wikipedia, _[Stone-von Neumann theorem](https://en.wikipedia.org/wiki/Stone%E2%80%93von_Neumann_theorem)_


### For the integer Heisenberg group

Discussion for the [[integer Heisenberg group]] in view of [[abelian Chern-Simons theory]]:

* {#GelcaUribe10} [[Răzvan Gelca]], [[Alejandro Uribe]], Thm. 2.4 in: *From classical theta functions to topological quantum field theory*, in: *The Influence of Solomon Lefschetz in Geometry and Topology: 50 Years of Mathematics at CINVESTAV*, Contemporary Mathematics **621**, AMS (2014) 35-68 &lbrack;[arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [doi;10.1090/conm/621](https://doi.org/10.1090/conm/621), [ams:conm-621](https://bookstore.ams.org/conm-621), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf), [[GelcaUribe-ThetaFunctionsTQFT.pdf:file]]&rbrack;

* {#GelcaHamilton12} [[Răzvan Gelca]], [[Alastair Hamilton]]: *Classical theta functions from a quantum group perspective*, New York J. Math. **21** (2015) 93–127 &lbrack;[arXiv:1209.1135](http://arxiv.org/abs/1209.1135), [nyjm:j/2015/21-4](https://nyjm.albany.edu/j/2015/21-4.html)&rbrack;

* {#GelcaHamilton15} [[Răzvan Gelca]], [[Alastair Hamilton]]: *The topological quantum field theory of Riemann’s theta functions*, Journal of Geometry and Physics **98** (2015) 242-261 &lbrack;[doi:10.1016/j.geomphys.2015.08.008](https://doi.org/10.1016/j.geomphys.2015.08.008), [arXiv:1406.4269](https://arxiv.org/abs/1406.4269)&rbrack;



[[!redirects Stone von Neumann theorem]]
[[!redirects Stone-von Neumann theorem]]
[[!redirects Stone–von Neumann theorem]]
[[!redirects Stone--von Neumann theorem]]

[[!redirects Schrödinger representation]]
[[!redirects Schrödinger representations]]

[[!redirects Schroedinger representation]]
[[!redirects Schroedinger representations]]

