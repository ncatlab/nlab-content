
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _Chaitin incompleteness theorem_ is a kind of [[incompleteness theorem]] in the context of [[complexity theory]]. It says roughly that within any sufficiently strong [[formal logic|formal system]] $S$, there is an upper bound on provable complexity: a [[natural number]] $L$ such that for no given string of data is there is a [[formal proof]] in $S$ that its [[Kolmogorov complexity]] exceeds $L$.

Note that $L$ is not an upper bound on complexity; on the contrary, there are only finitely many strings with complexity $L$ or less, and all of the infinitely many others must have complexity larger than $L$.  The system $S$ may even be capable of proving this, but it still cannot prove any particular example.


## References

* [[Gregory Chaitin]], _Algorithmic Information Theory_, 2003. (first edition 1987) ([pdf](http://www.umcs.maine.edu/~chaitin/cup.pdf))

* [[Gregory Chaitin]], _The Limits of Mathematics_, 1994 ([arXiv:chao-dyn/9407003](http://arxiv.org/abs/chao-dyn/9407003))

Expositions and surveys include 

* Wikipedia, _[Chaitin's incompleteness theorem](http://en.wikipedia.org/wiki/Kolmogorov_complexity#Chaitin.27s_incompleteness_theorem)_

* [[John Baez]], _[Surprises in logic](http://math.ucr.edu/home/baez/surprises.html)_, 2011


[[!redirects Chaitin incompletenss theorem]]
[[!redirects Chaitin incompleteness theorem]]
[[!redirects Chaitin's incompleteness theorem]]
[[!redirects Chaitin's incompleteness theorem]]
[[!redirects Chaitin\'s incompleteness theorem]]
