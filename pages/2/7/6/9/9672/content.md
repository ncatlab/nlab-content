
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Formal reasoning is critical for building truly secure and reliable software, and one of the key techniques for establishing properties of software systems is that of logical relations ([Reynolds 83](#Reynolds83)). Logical relations can be used to prove i) properties of [[programs]], e.g., that they perform no illegal operations, satisfy certain security criteria, or are observationally equivalent to their compiled forms; ii) whole-language properties, e.g., that [[programming language|languages]] satisfy [[parametricity]], enforce information flow policies, or guarantee privacy; and iii) properties of implementations, e.g., compiler correctness. (from [Johann-Ghani](#JohannGhani)).

## Related concepts

* [[programming language]], [[computer science]]

## References

Logical relationn have maybe been introduced in 

* J. C. Reynolds, _Types, Abstraction and Parametric Polymorphism_ Information Processing 83(1) (1983), pp. 513-523.
  {#Reynolds83}

See also 

* Patricia Johann, [[Neil Ghani]], _Logical Relations for Program Verification_, research proposal ([pdf](https://personal.cis.strath.ac.uk/neil.ghani/lrpv.pdf))
  {#JohannGhani}


* [[Thierry Coquand]], from slide 63 on in _Equality and dependent type theory_ ([pdf](http://www.cse.chalmers.se/~coquand/equality.pdf))

* Florian Rabe, Kristina Sojakova, _Logical Relations for a Logical Framework_ ([pdf](http://kwarc.info/frabe/Research/RS_logrels_12.pdf))

* Carsten Sch&#252;rmann, Jeffrey Sarnat, _Strctural logical relations_ ([pdf](http://www.twelf.org/slr/slr.pdf))

[[!redirects logical relations]]
