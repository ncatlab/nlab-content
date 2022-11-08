
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

Dynamic lifting is thought (eg. [Rand (2018),p. 52](#Rand18)) to be optional in cases like the [[quantum teleportation protocol]] but necessary for applications like [[quantum error correction]] (e.g. [Paler, Herr & Devitt (2019), §4.1](quantum+error+correction#PalerHerrDevitt19)), where error correction steps are conditioned on [[quantum measurement]] of syndrome [[qbits]].

There have been several (partial) proposals for the precise [[categorical semantics]] of this idea, see the references [below](#ReferencesCategoricalSemantics).



## References

### General

The general but informal idea of quantum computation with classical control that may itself be conditioned on quantum measurement results (see also at *[Quantum Computation -- Classical control and quantum data](quantum+computation#ClassicalControlQuantumData)*) may be argued to be implicit already in [Knill (1996)](quantum+computation#Knill96). 

Explicit discussion includes:

* {#NagarajanPapanikolaouWilliams07} Rajagopal Nagarajan, Nikolaos Papanikolaou, David Williams, *Simulating and Compiling Code for the Sequential Quantum Random Access Machine*, Electronic Notes in Theoretical Computer Science Volume 170, 6 March 2007, Pages 101-124 &lbrack;[doi:10.1016/j.entcs.2006.12.014](https://doi.org/10.1016/j.entcs.2006.12.014)&rbrack;


The term "dynamic lifting" is mainly used in discussion of the [[quantum programming language]] *[[Quipper]]*.  Its first (brief) appearance might be that in:

* {#GLRSV13} [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], p.5 of: _Quipper: A Scalable Quantum Programming Language_, ACM SIGPLAN Notices **48** 6 (2013) 333-342 &lbrack;[arXiv:1304.3390](https://arxiv.org/abs/1304.3390), [doi:10.1145/2499370.2462177](https://doi.org/10.1145/2499370.2462177)&rbrack;

More in-depth discussion of "dynamic lifting" is in:

* {#Rand18} [[Robert Rand]], *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

### Categorical semantics
 {#ReferencesCategoricalSemantics}

Proposals for [[categorical semantics]] of "dynamic lifting", mostly following along the lines of some [[dependent linear type theory]]:

* Dongho Lee, Valentin Perrelle, Benoît Valiron, Zhaowei Xu, *Concrete Categorical Model of a Quantum Circuit Description Language with Measurement*, Leibniz International Proceedings in Informatics **213** (2021) 51:1-51:20 &lbrack;[arXiv:2110.02691](https://arxiv.org/abs/2110.02691), [doi:10.4230/LIPIcs.FSTTCS.2021.51](https://doi.org/10.4230/LIPIcs.FSTTCS.2021.51)&rbrack;

* Andrea Colledan, [[Ugo Dal Lago]], *On Dynamic Lifting and Effect Typing in Circuit Description Languages* &lbrack;[arXiv:2202.07636](https://arxiv.org/abs/2202.07636)&rbrack;

* Andrea Colledan, [[Ugo Dal Lago]], *On Dynamic Lifting
and Effect Typing in Circuit Description Languages*, talk at *TYPES Workshop*, Nantes (2022)  &lbrack;[pdf](https://types22.inria.fr/files/2022/06/TYPES_2022_slides_13.pdf), [[ColledanLago-DynamicsLifting.pdf:file]]&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *A biset-enriched categorical model for Proto-Quipper with dynamic lifting*, in proceedings of *[Quantum Physics and Logic 2022](https://www.qplconference.org/)* &lbrack;[arXiv:2204.13039](https://arxiv.org/abs/2204.13039)&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *Proto-Quipper with dynamic lifting*, in proceedings of *[Quantum Physics and Logic 2022](https://www.qplconference.org/)* &lbrack;[arXiv:2204.13041](https://arxiv.org/abs/2204.13041)&rbrack;



