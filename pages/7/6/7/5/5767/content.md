
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# The tropical semiring
* table of contents
{: toc}


## Definitions

The __tropical rig__  is a [[rig]] $(\mathbb{R}\cup \{\infty\}, \oplus,\otimes)$ with addition $x\oplus y = min(x,y)$  and multiplication $x\otimes y = x+y$. This

The __tropical semiring__ is a [[semiring]] $(\mathbb{R},\oplus,\otimes)$ with addition $x\oplus y = min(x,y)$  and multiplication $x\otimes y = x+y$.

[[tropical geometry|Tropical geometry]] is often thought as the algebraic geometry over the tropical semiring.


## Terminology

The tropical rig is also called the [[min-plus algebra]]. There is a related, in fact isomorphic rig called the [[max-plus algebra]]. (Some authors use the term 'tropical algebra' for the max-plus rather than the min-plus algebra.  The theories, of course, run in parallel, as each is the negative of the other.) 

In his survey article, cited below, Pin uses the term for a wide range of similar idempotent semirings. For instance $\mathcal{M} = (\mathbb{N} \cup{\infty}, min, +)$ is a tropical semiring introduced by Imre Simon in 1978.


## Elementary properties

The tropical semiring is an example of an [[idempotent semiring]], since for all elements $x$, we have $x\oplus x=x$.


## Elementary example

$$(5\oplus 6)\otimes 7 = 12$$


## Applications

Apart from applications in [[tropical geometry]], the min-plus and max-plus algebras have extensive use in providing algebraic models for simple [[discrete event system]]s related to timed [[Petri nets]].


## References

*  The use of the tropical algebra in [[discrete event systems]] is handled in many sources. A slightly old set of notes (in French) for an introductory  course by St&#233;phane Gaubert, of INRIA Rocquencourt.  They can be found [here](http://amadeus.inria.fr/gaubert/PAPERS/POLY12-02-1999.pdf).

* [[Jean-Eric Pin]], _Tropical semirings_, [Hal preprint, hal-00113779](https://hal.archives-ouvertes.fr/hal-00113779/file/Tropical.pdf), and in the next reference,  pp.50-69, 1998, Publ. Newton Inst. 11. 

Book collection of articles on idempotent semirings:

* J. Gunawadena (ed.), *Idempotency*, Cambridge University Press, 2001, 

An original source:

* [[Imre Simon]], (1978), _Limited Subsets of a Free Monoid_, in Proc. 19th Annual Symposium on Foundations of Computer Science, Piscataway, N.J., Institute of Electrical and Electronics Engineers, 143–150 ([doi:10.1109/SFCS.1978.21](https://doi.org/10.1109/SFCS.1978.21))

See also:

* Wikipedia, *[Tropical semiring](https://en.wikipedia.org/wiki/Tropical_semiring)*

[[!redirects tropical semirings]]


[[!redirects tropical rig]]
[[!redirects tropical rigs]]



