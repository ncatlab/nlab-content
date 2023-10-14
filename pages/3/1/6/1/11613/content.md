
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

## Relation to synthetic mathematics
 {#RelationToSyntheticMathematics}
 
There is at least some similarity between DSELs and [[synthetic mathematics]], see for instance ([Hudak 98, section 3.2](#Hudak98)). In ([Hudak 98, figure 2](#Hudak98)) this shows aspects of a real-world DSL for "geometric region analysis" embedded in [[Haskell]] which under the [[relation between type theory and category theory]]/[[computational trinitarianism]] one immediately recognizes as a fragment of [[synthetic geometry]].


## Relation to monadic effects
 {#RelationToMonadicEffects}

There is a close relation between embedding a domain-specific language and declaring [do-notation](monad+in+computer+science#DoNotation) for [[monadic effects]], see [Benton, Hughes & Moggi 2002, §5.3](#BentonHughesMoggi02) who write:

> Every time a functional programmer designs a combinator library, then, we might as well say that he or she designs a domain specific programming language &lbrack;...&rbrack;. This is a useful perspective, since it encourages programmers to produce a modular design, with a clean separation between the semantics of the DSL and the program that uses it, rather than mixing combinators and 'raw' semantics willy-nilly. And since monads appear so often in programming language semantics, it is hardly surprising that they appear often
in combinator libraries also!

## Examples
 {#Examples}

### Quantum programming
 {#QuantumProgramming}

Many existing [[quantum programming languages]] are actually domain-specific languages for the description of [[quantum circuits]], and as such many are embedded in ambient [[type theories]].


For instance:

* *[[Quipper]]* is embedded into into [[Haskell]] &lbrack;[Green, Lumsdaine, Ross, Selinger & Valiron (2013)](Quipper#GLRSV13)&rbrack;;

* *[[QWIRE]]* has been embedded into [[Coq]] ([Rand, Paykin & Zdancewic (2018)](QWIRE#RandPaykinZdancewic18)) and [[homotopy type theory]] &lbrack;[Paykin & Zdancewic (2019)](QWIRE#PaykinZdancewic19)&rbrack;.

* [[CoqQ]] is another quantum programming language embedded in [[Coq]] &lbrack;Ying et al. (2022)&rbrack;

See also [Rennela & Staton (2020)](#RennelaStaton17) for more general discussion.

## References

* [[Paul Hudak]], *Building Domain-Specific Embedded Languages*, ACM Computing Surveys **28** 4e (1996) 196–es &lbrack;[doi:10.1145/242224.242477](https://doi.org/10.1145/242224.242477), [web](https://dl.acm.org/doi/fullHtml/10.1145/242224.242477)&rbrack;

* {#Hudak98} [[Paul Hudak]], _Modular Domain Specific Languages and Tools_, in: _Proceedings of Fifth International Conference on Software Reuse_, IEEE Computer Society Press  (1998)  &lbrack;[pdf](http://staff.um.edu.mt/afra1/seminar/ModularDSL.pdf), [doi:10.5555/551789.853532](https://dl.acm.org/doi/10.5555/551789.853532)&rbrack;

With emphasis on the relation to [[monads in computer science]]:

* {#BentonHughesMoggi02} [[Nick Benton]], [[John Hughes]], [[Eugenio Moggi]], §5.3 in: *Monads and Effects*, in: *Applied Semantics*, Lecture Notes in Computer Science **2395**, Springer (2002) 42-122 &lbrack;[doi:10.1007/3-540-45699-6_2](https://doi.org/10.1007/3-540-45699-6_2)&rbrack;

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

[[!redirects embedded programming language]]
[[!redirects embedded programming languages]]


