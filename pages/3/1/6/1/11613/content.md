
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _[[domain specific programming language]]_ is one designed for  a specialized kind ("domain") of applications. A _domain specific embedded programming language_ (DSEL) is a domain specific language realized "inside" a general-purpose high level ([[type theory|typed]]) [[programming language]].

## {#RelationToSyntheticMathematics} Relation to synthetic mathematics
 
 
There is at least some similarity between DSELs and [[synthetic mathematics]], see for instance ([Hudak 98, section 3.2](#Hudak98)). In ([Hudak 98, figure 2](#Hudak98)) this shows aspects of a real-world DSL for "geometric region analysis" embedded in [[Haskell]] which under the [[relation between type theory and category theory]]/[[computational trinitarianism]] one immediately recognizes as a fragment of [[synthetic geometry]].

## Examples
 {#Examples}

### Quantum programming

Many existing [[quantum programming languages]] are actually domain-specific languages for the description of [[quantum circuits]], and as such many are embedded in ambient [[type theories]].


For instace:

* *[[Quipper]]* is embedded into into [[Haskell]];

* [[QWIRE]] has been embedded into [[Coq]] ([Rand, Paykin & Zdancewic (2018)](QWIRE#RandPaykinZdancewic18)) and [[homotopy type theory]] ([Paykin & Zdancewic (2019)](QWIRE#PaykinZdancewic19)).

See also [Rennela & Staton (2020)](#RennelaStaton17) for more general discussion.

## References

* {#Hudak98} [[Paul Hudak]], _Modular Domain Specific Languages and Tools_, in: _Proceedings of Fifth International Conference on Software Reuse_, IEEE Computer Society Press  (1998)  &lbrack;[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=685738), [doi:10.5555/551789.853532](https://dl.acm.org/doi/10.5555/551789.853532)&rbrack;

Discussion for embedding in [[Haskell]]:

* HaskellWiki, _[Embedded domain specific language](http://www.haskell.org/haskellwiki/Embedded_domain_specific_language)_

A list of literature is at 

* Haskell Wiki, _[Research papers/Domain specific languages](http://www.haskell.org/haskellwiki/Research_papers/Domain_specific_languages)_

Discussion specifically of [[quantum programming languages]] for [[quantum circuits]] as domain specific embedded languages:

* {#RennelaStaton17} [[Mathys Rennela]], [[Sam Staton]], *Classical Control, Quantum Circuits and Linear Logic in Enriched Category Theory*, Logical Methods in Computer Science **16** 1 (2020) &lbrack;[arXiv:1711.05159](https://arxiv.org/abs/1711.05159), <a href="https://doi.org/10.23638/LMCS-16(1:30)2020">doi:10.23638/LMCS-16(1:30)2020</a>&rbrack;



[[!redirects domain specific embedded programming languages]]

[[!redirects domain specific embedded language]]
[[!redirects domain specific embedded languages]]

[[!redirects embedded domain specific language]]
[[!redirects embedded domain specific languages]]

[[!redirects embedded domain specific programming language]]
[[!redirects embedded domain specific programming languages]]


[[!redirects DSEL]]
[[!redirects EDSL]]