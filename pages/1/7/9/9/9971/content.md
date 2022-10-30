
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Quipper_ is a [[functional programming language|functional]] [[quantum programming language]]

## Related concepts

* [[QML]]

* [[QPL]]

## References

### General

Resources:

* [[Peter Selinger]], _The Quipper Language_ ([web](http://www.mathstat.dal.ca/~selinger/quipper/))




Original articles:

* {#Selinger04} [[Peter Selinger]], _Towards a quantum programming language_, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 &lbrack;[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)&rbrack;


* {#GLRSV13} [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _Quipper: A Scalable Quantum Programming Language_, ACM SIGPLAN Notices 48(6):333-342, 2013 ([arXiv:1304.3390](https://arxiv.org/abs/1304.3390))

* [[Jonathan Smith]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _Quipper: Concrete Resource Estimation in Quantum Algorithms_, QAPL 2014 ([arXiv:1412.0625](https://arxiv.org/abs/1412.0625))

Review:

* [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _An Introduction to Quantum Programming in Quipper_, Lecture Notes in Computer Science 7948:110-124, Springer, 2013 ([arXiv:1304.5485](https://arxiv.org/abs/1304.5485))

On quantum [[software verification]] for/with Quipper:

* Linda Anticoli, Carla Piazza, Leonardo Taglialegne, Paolo Zuliani, _Towards Quantum Programs Verification: From Quipper Circuits to QPMC_, In: Devitt S., Lanese I. (eds) Reversible Computation. RC 2016. Lecture Notes in Computer Science, vol 9720. Springer, Cham ([doi:10.1007/978-3-319-40578-0_16](https://doi.org/10.1007/978-3-319-40578-0_16))

### Dependent linear types and categorical semantics
 {#ReferencesDependentLinearTypesAndCategoricalSemantics}

Discussion of some [[dependent linear type theory]] and [[categorical semantics]] for [[Quipper]]:

* Francisco Rios, [[Peter Selinger]], *A Categorical Model for a Quantum Circuit Description Language*, EPTCS **266** (2018) 164-178 &lbrack;[arXiv:1706.02630](https://arxiv.org/abs/1706.02630), [doi:10.4204/EPTCS.266.11](https://doi.org/10.4204/EPTCS.266.11)&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil Ross]], [[Peter Selinger]],  _A Tutorial Introduction to Quantum Circuit Programming in Dependently Typed Proto-Quipper_, in I. Lanese, M. Rawski  (eds.) _Reversible Computation_ RC 2020. Lecture Notes in Computer Science, vol 12227 &lbrack;[arXiv:2005.08396](https://arxiv.org/abs/2005.08396), [doi:10.1007/978-3-030-52482-1_9](https://doi.org/10.1007/978-3-030-52482-1_9)&rbrack;

{#ReferencesDynamicLifting} The issue of "dynamic lifting" (of "bits" resulting from [[quantum measurement]] back into the "[[context]]"):

* Dongho Lee, Valentin Perrelle, Benoît Valiron, Zhaowei Xu, *Concrete Categorical Model of a Quantum Circuit Description Language with Measurement*, Leibniz International Proceedings in Informatics **213** (2021) 51:1-51:20 &lbrack;[arXiv:2110.02691](https://arxiv.org/abs/2110.02691), [doi:10.4230/LIPIcs.FSTTCS.2021.51](https://doi.org/10.4230/LIPIcs.FSTTCS.2021.51)&rbrack;

* Andrea Colledan, [[Ugo Dal Lago]], *On Dynamic Lifting and Effect Typing in Circuit Description Languages* &lbrack;[arXiv:2202.07636](https://arxiv.org/abs/2202.07636)&rbrack;

* Andrea Colledan, [[Ugo Dal Lago]], *On Dynamic Lifting
and Effect Typing in Circuit Description Languages*, talk at *TYPES Workshop*, Nantes (2022)  &lbrack;[pdf](https://types22.inria.fr/files/2022/06/TYPES_2022_slides_13.pdf), [[ColledanLago-DynamicsLifting.pdf:file]]&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *A biset-enriched categorical model for Proto-Quipper with dynamic lifting* &lbrack;[arXiv:2204.13039](https://arxiv.org/abs/2204.13039)&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *Proto-Quipper with dynamic lifting* &lbrack;[arXiv:2204.13041](https://arxiv.org/abs/2204.13041)&rbrack;


[[!redirects QPL]]