
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
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

   1. the "[[collapse of the wavefunction|collapse]]" of the [[quantum state]] being measured by [[orthogonal linear basis|orthogonal]] [[projection operator|projection]] to the [[linear span]] of the $b$th basis state.

      $$
        \array{
          P_b 
            &\colon&
          \mathscr{H} 
            &\xrightarrow{\phantom{---}}&
          \mathscr{H}_b \hookrightarrow \mathscr{H}
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

\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumModalUnits-221110.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

|  |  |
|--|--|
| quantum measurement | [[quantum state preparation]] |
| [[quantum superposition]] | [[quantum parallelism]] |


## Properties

* [[collapse of the wavefunction]]

* [[deferred measurement principle]]

\linebreak

## The "measurement problem"

In the context of _[[interpretation of quantum mechanics]]_ it is common to speak of the "measurement problem" when referring to the tension between regarding [[quantum physics]] as a [[probability theory|probabilistic]] theory and the idea of realism.

Namely -- by the [above](#Definition) -- a quantum measurement is formally reflected in a change of [[probabilities]]. But since in any given [[measurement]] [[experiment]] one definite outcome is observed, one may wonder how that particular outcome was actually chosen, given that the theory only gives its probability.

(...)

## Related concepts

* [[deferred measurement principle]]

* [[Bell's inequality]]

* [[no-cloning theorem]]

* [[quantum reader monad]]

* [[quantum state preparation]]

* [[quantum fluctuation]]

* [[decoherence]]


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

### Formalization

Brief mentioning of [[type|typing]] and [[categorical semantics]] of quantum measurement in the [[quantum programming language]] [[QPL]]/[[Quipper]]:

* {#Selinger04} [[Peter Selinger]], p. 39 of: *Towards a quantum programming language*, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 &lbrack;[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)&rbrack;


Discussion of quantum measurements in terms of [[finite quantum mechanics in terms of dagger-compact categories]] via [[Frobenius algebra]]-structures and the [[quantum reader monad]]:

* {#CoeckePavlović08} [[Bob Coecke]], [[Duško Pavlović]], *Quantum measurements without sums*, in [[Louis Kauffman]], [[Samuel Lomonaco]] (eds.), *Mathematics of Quantum Computation and Quantum Technology*, Taylor & Francis (2008) 559-596 &lbrack;[arXiv:quant-ph/0608035](https://arxiv.org/abs/quant-ph/0608035), [doi:10.1201/9781584889007](https://doi.org/10.1201/9781584889007)&rbrack;

* [[Bob Coecke]], [[Eric Oliver Paquette]], *POVMs and Naimark's theorem without sums*, Electronic Notes in Theoretical Computer Science **210** (2008) 15-31 &lbrack;[arXiv:quant-ph/0608072](https://arxiv.org/abs/quant-ph/0608072), [doi:10.1016/j.entcs.2008.04.015](https://doi.org/10.1016/j.entcs.2008.04.015)&rbrack;

* [[Bob Coecke]], [[Eric Paquette]], [[Dusko Pavlovic]], *Classical and quantum structures* (2008) &lbrack;[pdf](http://www.comlab.ox.ac.uk/files/627/RR-08-02.pdf), [[Coecke-Paquette-Pavlovic-CQS.pdf:file]]&rbrack;


* [[Bob Coecke]], [[Duško Pavlović]], [[Jamie Vicary]],  *A new description of orthogonal bases*, Mathematical Structures in Computer Science **23** 3 (2012) 555- 567 &lbrack;[arXiv:0810.0812](https://arxiv.org/abs/0810.0812), [doi:10.1017/S0960129512000047](https://doi.org/10.1017/S0960129512000047)&rbrack;

Textbook account in:

* {#HeunenVicary19} [[Chris Heunen]], [[Jamie Vicary]], *Categories for Quantum Theory*, Oxford University Press 2019 ([ISBN:9780198739616](https://global.oup.com/academic/product/categories-for-quantum-theory-9780198739616))

Generalization to [[Hilbert bundles]]:

* [[Chris Heunen]], [[Manuel L. Reyes]], *Frobenius Structures Over Hilbert $C^\ast$-Modules*, Commun. Math. Phys. **361** (2018) 787–824 &lbrack;[doi:10.1007/s00220-018-3166-0](https://doi.org/10.1007/s00220-018-3166-0), [arXiv:1704.05725](https://arxiv.org/abs/1704.05725)&rbrack;


### The Measurement Problem
 
The article

* [[Klaas Landsman]], Robin Reuvers, _A Flea on Schr&#246;dinger's Cat_,  Found. Phys. 43, 373-407 (2013) ([arXiv:1210.2353](http://arxiv.org/abs/1210.2353), [pdf](http://www.math.ru.nl/~landsman/Catresubmission.pdf))

points out that for symmetric systems with a symmetric [[ground state]], already a tiny perturbation mixing the ground state with the first [[excited state]] causes [[spontaneous symmetry breaking]] in a suitable limit, and suggests that this already resolves the measurement problem.

See also 

* {#Wallace07} [[David Wallace]], _The Quantum Measurement Problem: State of Play_ ([arXiv:0712.0149](http://arxiv.org/abs/0712.0149))



[[!redirects quantum measurements]]

[[!redirects quantum measurement]]
[[!redirects measurement problem]]


