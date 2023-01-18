
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computing
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

*Hoare logic* &lbrack;[Hoare (1969)](#Hoare69)&rbrack; is a form of [[formal program verification]].

> &lbrack;[from Streicher (1993, p.1-2):](#Streicher93)&rbrack; In theoretical computer science the issue of *correctness of programs* has become more and more important over the years. Early approaches to establishing correctness  were *program verification logics* such as Hoare calculi for verifying [[imperative programs]] and the method of *algebraic specification* for specifying modules in functional languages.

> Program logics as e.g. the Hoare calculus are oriented towards state-oriented programming languages and provide calculi for deriving correct "Hoare triples", i.e. expressions of the form $\{P\}S\{Q\}$ with the intuitive meaning that whenever the initial state of a program satisfies [[proposition]] $P$ then the execution of the program $S$ [[termination|terminates]] and results in a state satisfying proposition $Q$. 

> Although this method works  quite well for "pidgin" programs (i.e. using only `assignment`, `if_then_else` and `while` over a *single* [[data type]]) there are big problems with dealing with procedures, modules and general user defined data types. In general a main drawback is that the world of programs and the world of specifications are conceptually quite different. Of course, this problem is typical for all state-oriented imperative programming languages.

> This conceptual gap between programs and their specification has been overcome by the appearance and development of [[functional programming languages]]. &lbrack;...&rbrack; for languages supporting the construction and verification of large modular systems the concept of [[dependent type]] is inevitable.

## Related concepts

* [[separation logic]]

## References

The original article:

* {#Hoare69} [[C. A. R. Hoare]], *An axiomatic basis for computer programming*, Communications of the ACM **12** 10 (1969) 576–580 &lbrack;[doi:10.1145/363235.363259](https://doi.org/10.1145/363235.363259)&rbrack;

See also:

* Wikipedia, *[Hoare logic](https://en.wikipedia.org/wiki/Hoare_logic)*

The above quote is from:

* {#Streicher93} [[Thomas Streicher]], p. 1-2 of: *Investigations into Intensional Type Theory*, Habilitation Thesis, Darmstadt (1993) &lbrack;[pdf](https://www2.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf), [[Streicher-IntensionalTT.pdf:file]]&rbrack;

which otherwise is about [[intensional type theory|intensional]] [[dependent type theory]]/


[[!redirects Hoare logics]]

[[!redirects Hoare calculus]]
[[!redirects Hoare calculi]]

