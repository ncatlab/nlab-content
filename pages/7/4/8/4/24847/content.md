
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
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

In [[quantum computation]] the term "dynamic lifting" (mostly used in the *[[Quipper]]*-community, starting around [Green et al (2013), p. 5](#GLRSV13)) refers to the outcome of [[quantum measurement]]-results --- which can be known only during runtime (ie. "dynamically"), due to the intrinsic stochastic nature of [[quantum physics]]  --- being turned into (ie. "lifted" back to) [[variables]] on which subsequent classical [[computation]] may be conditioned, which may then in turn [[controlled quantum gate|control]] further [[quantum circuits]], etc.:

\begin{imagefromfile}
    "file_name": "SQRAMschema-WithDynLifting.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "SQRAM model adapted from [Nagarajan, Papanikolaou & Williams 2007, Fig 1](#NagarajanPapanikolaouWilliams07)"
\end{imagefromfile}

Dynamic lifting is thought (eg. [Rand (2018),p. 52](#Rand18)) to be optional in cases like the [[quantum teleportation protocol]] but necessary for applications like 

* [[quantum error correction]] (e.g. [Paler, Herr & Devitt (2019), §4.1](quantum+error+correction#PalerHerrDevitt19)), where error correction steps are conditioned on [[quantum measurement]] of syndrome [[qbits]];

* [[repeat-until-success computing]], where a quantum circuit is re-run on its input data until a failure syndrome measurement indicates success.

There have been several (partial) proposals for the precise [[categorical semantics]] of this idea, see the references [below](#ReferencesCategoricalSemantics).
Another formalization, via [[monadic effects]] of [potentiality modalities](necessity+and+possibility#RelationToPotentiality) in [[dependent linear type theory]], is discussed at *[[quantum circuits via dependent linear types]]* ([CQTS 2022](#CQTS22), see [there](quantum+circuits+via+dependent+linear+types#QuantumMeasurement)).


## References

### General

The general but informal idea of quantum computation with classical control that may itself be conditioned on quantum measurement results (see also at *[Quantum Computation -- Classical control and quantum data](quantum+computation#ClassicalControlQuantumData)*) may be argued to be implicit already in [Knill (1996)](quantum+computation#Knill96). 

Explicit discussion includes:

* {#NagarajanPapanikolaouWilliams07} Rajagopal Nagarajan, Nikolaos Papanikolaou, David Williams, *Simulating and Compiling Code for the Sequential Quantum Random Access Machine*, Electronic Notes in Theoretical Computer Science Volume 170, 6 March 2007, Pages 101-124 &lbrack;[doi:10.1016/j.entcs.2006.12.014](https://doi.org/10.1016/j.entcs.2006.12.014)&rbrack;


The term "dynamic lifting" is mainly used in discussion of the [[quantum programming language]] *[[Quipper]]*.  Its first (brief) appearance might be that in:

* {#GLRSV13} [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], p.5 of: _Quipper: A Scalable Quantum Programming Language_, ACM SIGPLAN Notices **48** 6 (2013) 333-342 &lbrack;[arXiv:1304.3390](https://arxiv.org/abs/1304.3390), [doi:10.1145/2499370.2462177](https://doi.org/10.1145/2499370.2462177)&rbrack;

More in-depth discussion of "dynamic lifting" is in:

* {#Rand18} [[Robert Rand]], pp. 40 of: *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

### Categorical semantics
 {#ReferencesCategoricalSemantics}

Proposals for [[categorical semantics]] of "dynamic lifting", mostly following along the lines of some [[dependent linear type theory]], such as found in [[Quipper]]:

* [[Mathys Rennela]], [[Sam Staton]], *Classical Control, Quantum Circuits and Linear Logic in Enriched Category Theory*, Logical Methods in Computer Science **16** (2020) lmcs:6192 &lbrack;[arXiv:1711.05159](https://arxiv.org/abs/1711.05159), <a href="https://doi.org/10.23638/LMCS-16(1:30)2020">doi:10.23638/LMCS-16(1:30)2020</a>&rbrack;

  > (cf. *[[EWIRE]]*)


* [[Dongho Lee]], Sebastien Bardin, [[Valentin Perrelle]], [[Benoît Valiron]], *Formalization of a Programming Language for Quantum Circuits with Measurement and Classical Control*, talk at *[Journées Informatique Quantique 2019](https://quantcert.github.io/GT-IQ'19/)* (Nov 2019) &lbrack;[pdf](https://quantcert.github.io/GT-IQ%2719/slides/Lee.pdf), [[LBPV_QCWithClassicalControl.pdf:file]]&rbrack;

* [[Dongho Lee]], [[Valentin Perrelle]], [[Benoît Valiron]], Zhaowei Xu, *Concrete Categorical Model of a Quantum Circuit Description Language with Measurement*, Leibniz International Proceedings in Informatics **213** (2021) 51:1-51:20 &lbrack;[arXiv:2110.02691](https://arxiv.org/abs/2110.02691), [doi:10.4230/LIPIcs.FSTTCS.2021.51](https://doi.org/10.4230/LIPIcs.FSTTCS.2021.51)&rbrack;


* [[Andrea Colledan]], [[Ugo Dal Lago]], *On Dynamic Lifting and Effect Typing in Circuit Description Languages*, talk at *TYPES Workshop*, Nantes (2022)  &lbrack;[arXiv:2202.07636](https://arxiv.org/abs/2202.07636), [pdf](https://types22.inria.fr/files/2022/06/TYPES_2022_slides_13.pdf), [[ColledanLago-DynamicsLifting.pdf:file]]&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *A biset-enriched categorical model for Proto-Quipper with dynamic lifting*, in proceedings of *[Quantum Physics and Logic 2022](https://www.qplconference.org/)* &lbrack;[arXiv:2204.13039](https://arxiv.org/abs/2204.13039)&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *Proto-Quipper with dynamic lifting*, in proceedings of *[Quantum Physics and Logic 2022](https://www.qplconference.org/)* &lbrack;[arXiv:2204.13041](https://arxiv.org/abs/2204.13041)&rbrack;

* {#CQTS22} [[Urs Schreiber]], *[Quantum Data Types via Linear HoTT](https://ncatlab.org/schreiber/show/QDataInLHoTT#QTML2022)* (Nov 2022)

* [[Dongho Lee]], *Formal Methods for Quantum Programming Languages*, Paris Saclay (Dec 2022) &lbrack;[hal:tel-03895847](https://hal.science/LMF/tel-03895847)&rbrack;

* [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:The Quantum Monadology|The Quantum Monadology]]* &lbrack;[arXiv:2310.15735](https://arxiv.org/abs/2310.15735)&rbrack;

