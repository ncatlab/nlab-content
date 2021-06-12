

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


[Metamath](http://us.metamath.org/) is a [[proof assistant]] for creating databases of formally verified [[proofs]].  The proof language is extremely parsimonious using textual [[substitution]] as its only [[rule of inference]] (augmented by distinct [[variable]] constraints so that unfortunate variable captures can be prohibited).

One disadvantage of this philosophy is that [[definitions]], [[syntax]] and [[axioms]] are all [[axioms]]. In particular, the user is responsible for ensuring that no ambiguities or contradictions are inadvertently introduced.

Metamath proof verifiers can be very small and simple, so many have been implemented in a wide variety of computer languages. Perhaps the most interesting was created by Stephen O'Rear using a language that makes Turing machines optimised for few states. This was used to [reduce the bound of the smallest Busy Beaver Number that ZFC cannot prove to exist](https://www.scottaaronson.com/blog/?p=2725). A side effect was a small turing machine that [halts iff the Riemann Hypothesis is False](https://www.scottaaronson.com/blog/?p=2741) (and gives the smallest counterexample)

## Related entries

[[!include proof assistants and formalization projects -- list]]

## References

Metamath was originally designed by Norman Megill, but many people have contributed over the years.

* [Metamath home page](http://us.metamath.org/)

There are several Metamath databases on the Metamath website.  The most developed covers classical ZFC set theory, but there is a very nice NF set theory database and a couple of other less well developed ones.

See also

* Wikipedia, _[Metamath](https://en.wikipedia.org/wiki/Metamath)_
* Mario Carneiro's paper _[Metamath Zero: The Cartesian Theorem Prover](https://arxiv.org/abs/1910.10703)_ discusses a metamath variant that _bootstraps_ ie proves it's own correctness.








