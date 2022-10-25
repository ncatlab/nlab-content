
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

# Quantum measurement
* table of contents
{: toc}

## Idea
 {#Idea}

Quantum measurement is [[measurement]] in [[quantum mechanics]]. 

The "[[projection postulate]]" of [[quantum physics]] asserts ([von Neumann 1932](#vonNeumann32); [Lüders 1951](#Lüders51)) that:

1. measurement of [[quantum states]] is *with respect* to a choice of [[orthonormal linear basis]] $\big\{\vert \psi_b \rangle \big\}_{b : B}$ of the given [[Hilbert space]] $\mathscr{H}$ [[space of quantum states|of]] [[pure quantum states]];

1. the result of measurement on [[pure quantum states]] $\vert \psi \rangle \;\in\; \mathscr{H}$ is 

   1. a random value $b \in B$;

   1. the "[[collapse of the wavefunction|collapse]]" of the [[quantum state]] being measured by [[orthogonal linear basis|orthogonal]] [[projection operator|projection]] to the the [[linear span]] of the $b$th basis state.

      $$
        \array{
          P_b 
            &\colon&
          \mathscr{H} 
            &\xrightarrow{\phantom{---}}&
          \mathscr{H}_B \hookrightarrow \mathscr{H}
          \\
          &&
          \vert \psi \rangle
          &\mapsto&
          P_b \vert \psi \rangle
          \mathrlap{
            =
            \vert \psi_b \rangle
            \langle \psi_b \vert \psi \rangle
          }
        }
      $$ 
     

In terms of [[mixed quantum states]] represented by [[density matrices]], this prescription translates into a [[quantum operation]] which is given by a [[positive-operator valued measure]] (this is what [Lüders (1951)](#Lüders51) first wrote down).


There are different ways to *[[type theory|type]]* the quantum measurement, taking into account the non-deterministic nature of its outcome: 

1. Regarding the [[direct sum]] $\bigoplus_{b \colon B} \mathscr{H}$ of [[Hilbert spaces]] as the [[logical disjunction]] ("or") of [[quantum logic]], one may regard measurement as being the [[linear map]] into the direct sum whose $b$th component is $P_b$.

   > This choice of typing appears (briefly) in [Selinger 2004](#Selinger04), [p. 39](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf#page=39), in a precursor discussion that led to the formulation of the [[quantum programming language]] *[[Quipper]]*.

1. Regarding the measurement outcome $b \in B$ as the observed [[context]] of the actual quantum collapse, one may regard the collapse projection as [[dependent type theory|dependently typed]].

   > Getting from previous option back to this one is known in the the [[Quipper]]-community as *[dynamic lifting](Quipper#ReferencesDynamicLifting)* (namely "of the measured bits back into the context")

\begin{imagefromfile}
    "file_name": "PossibleTypingsOfQuantumMeasurement-221025.jpg",
    "width": "560",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Both of these options naturally emerge and are naturally unified in the "[Quantum Modal Logic](necessity+and+possibility#ModalQuantumLogic)" inherent to [[dependent linear type theory]]: This is discussed at *[[quantum circuits via dependent linear types]]*.

\linebreak

## The "measurement problem"

In the context of _[[interpretation of quantum mechanics]]_ it is common to speak of the "measurement problem" when referring to the tension between regarding [[quantum physics]] as a [[probability theory|probabilistic]] theory and the idea of realism.

Namely -- by the [above](#Definition) -- a quantum measurement is formally reflected in a change of [[probabilities]]. But since in any given [[measurement]] [[experiment]] one definite outcome is observed, one may wonder how that particular outcome was actually chosen, given that the theory only gives its probability.

(...)

## Related concepts

* [[quantum state preparation]]

* [[quantum fluctuation]]

* [[decoherence]]

* [[Bell's inequality]]

* [[quantum probability]]

* [[interpretation of quantum mechanics]]

## References

### General

The original axiomatization of quantum measurement via the *projection postulate*:

* {#vonNeumann32} [[John von Neumann]], §III.3 and §VI of: 

  *Mathematische Grundlagen der Quantenmechanik* (German) (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

* {#Lüders51} [[Gerhart Lüders]]:

  *Über die Zustandsänderung durch den Meßprozeß*, Ann. Phys. **8** (1951) 322–328  &lbrack;[doi:10.1002/andp.19504430510](https://doi.org/10.1002/andp.19504430510)&rbrack;

  *Concerning the state-change due to the measurement process*, Ann. Phys. **15** 9 (2006) 663-670 &lbrack;[pdf](http://myweb.rz.uni-augsburg.de/~eckern/adp/history/historic-papers/2006_518_663-670.pdf), [[Lueders-StateChange.pdf:file]]&rbrack;

Review and discussion:

* [[Roland Omnès]], §8 of: *[[The Interpretation of Quantum Mechanics]]*, Princeton University Press (1994) &lbrack;[ISBN:9780691036694](http://press.princeton.edu/titles/5525.html)&rbrack;

* {#Landsman17} [[Klaas Landsman]], Section 11: of _Foundations of quantum theory -- From classical concepts to Operator algebras_, Springer Open 2017 ([doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf))

Brief mentioning of [[type|typing]] and [[categorical semantics]] of quantum measurement in the [[quantum programming language]] [[QPL]]/[[Quipper]]:

* {#Selinger04} [[Peter Selinger]], p. 39 of: *Towards a quantum programming language*, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 &lbrack;[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)&rbrack;


### The Measurement Problems
 
The article

* [[Klaas Landsman]], Robin Reuvers, _A Flea on Schr&#246;dinger's Cat_,  Found. Phys. 43, 373-407 (2013) ([arXiv:1210.2353](http://arxiv.org/abs/1210.2353), [pdf](http://www.math.ru.nl/~landsman/Catresubmission.pdf))

points out that for symmetric systems with a symmetric [[ground state]], already a tiny perturbation mixing the ground state with the first [[excited state]] causes [[spontaneous symmetry breaking]] in a suitable limit, and suggests that this already resolves the measurement problem.

See also 

* {#Wallace07} [[David Wallace]], _The Quantum Measurement Problem: State of Play_ ([arXiv:0712.0149](http://arxiv.org/abs/0712.0149))



[[!redirects quantum measurements]]

[[!redirects quantum measurement]]
[[!redirects measurement problem]]


