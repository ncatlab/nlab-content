
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _proof assistant_ or _proof management system_ is a kind of software designed to help with [[proofs]] in formalized [[mathematics]]. Many proof assistants resemble and/or include a [[programming language]].

There are arguably two threads of current development in proof systems, which may be called "foundational" and "coverage".

The "foundational" work tries to find the best foundational theory to formalize mathematics (see also at _[[foundations of mathematics]]_). Out of that work first came [[dependent type theory|dependent types]] ([[Automath]], in the late 60s), then the [[calculus of constructions]] (early [[Coq]]), and the [[calculus of inductive constructions]] (current [[Coq]]). More recently a new wave of such work is being done in [[homotopy type theory]] as another step in this direction. Coq's library is not that large, except in the area of [[group theory]] where the results of the work on [[Feit-Thompson theorem]] has produced something larger.

The "coverage" work tries to formalize as much as possible of mathematics in existing theories.  For instance, for decades people have been building [[Mizar]]'s library (Mizar is based on [[Tarski–Grothendieck set theory]] rather than [[type theory]]). Its library is a couple of orders of magnitude larger than anyone else's. On the other hand, despite this quantity, it remains an issue to attack problems of contemporary research interest in these systems, see also at _[Mizar -- problem of pertinence](Mizar#ProblemOfPertinence)_.

Similar to Mizar is [[NuPRL]], [[HOL light]] and [[Isabelle]], which all have decently sized libraries.  (Isabelle can be used with either [[material set theory]], like Mizar, or [[higher-order type theory]], like the others.)


## Examples

[[!include proof assistants and formalization projects -- list]]


## References

Gentle exposition:

* [[Théo Winterhalter]], §1 of: *Formalisation and Meta-Theory of Type Theory*, Nantes (2020) &lbrack;[pdf](https://github.com/TheoWinterhalter/phd-thesis/releases/download/v1.2.1/TheoWinterhalter-PhD-v1.2.1.pdf), [github](https://github.com/TheoWinterhalter/phd-thesis)&rbrack;

Further exposition:

* {#Avigad12} [[Jeremy Avigad]], _Interactive Theorem Proving, Automated Reasoning, and Mathematical Computation_, (2012) [pdf slides](http://www.andrew.cmu.edu/user/avigad/Talks/icerm.pdf)

Exposition in relation to developments in [[machine learning]]:

* [[Terence Tao]]: *Machine-Assisted Proof*, Notices of the AMS **72** 1 (2024) &lbrack;[pdf](https://www.ams.org/journals/notices/202501/rnoti-p6.pdf), [doi:10.1090/noti3041](https://doi.org/10.1090/noti3041), full issue:[pdf](https://www.ams.org/notices/202501/202501FullIssue.pdf)&rbrack;


On computer assisted proofs in [[analysis]]:

* [[Oscar E. Lanford]], *Computer assisted proofs*, in: *Computational Methods in Field Theory*, Lecture Notes in Physics, **409**, Springer (1992) &lbrack;[doi:10.1007/3-540-55997-3_30](https://doi.org/10.1007/3-540-55997-3_30)&rbrack;

   
See also:

* Wikipedia, _[Proof assistant](https://en.wikipedia.org/wiki/Proof_assistant)_

List of web resources:

* [[Freek Wiedijk]], _Digital math by alphabet_ ([web](http://www.cs.ru.nl/~freek/digimath/index.html))





See also



* _[Conference Series on Intelligent Computer Mathematics](http://www.cicm-conference.org/)_

  ([2014](http://cicm-conference.org/2014/cicm.php))

* Conference series on Interactive theorem proving

  ([2014](http://www.cs.uwyo.edu/~ruben/itp-2014/))

Parts of the above text are taken from [this MO comment](http://mathoverflow.net/questions/133572/at-which-level-is-it-currently-possible-to-write-formal-proofs/134009#134009) by [[Jacques Carette]].

Proof assistants specifically for [[homotopy type theory]]:

* [HoTT wiki](https://ncatlab.org/homotopytypetheory/show/HomePage), *[[homotopytypetheory:Proof Assistants]]*

See also 

* [[Kevin Buzzard]], _[Xena project](https://xenaproject.wordpress.com/2018/10/07/what-is-the-xena-project/)_

  on [[formal proof]] and proof assistants in undergraduate mathematics.

[[!redirects proof assistant]]
[[!redirects proof assistants]]

[[!redirects proof management system]]
[[!redirects proof management systems]]

[[!redirects computer proof assistant]]
[[!redirects computer proof assistants]]

[[!redirects theorem prover]]
