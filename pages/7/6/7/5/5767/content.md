
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

# The tropical semiring
* table of contents
{: toc}


## Definitions

The __tropical semiring__ is a [[semiring]] $(\mathbb{R}\cup \{\infty\},\oplus,\otimes)$ with addition $x\oplus y = min(x,y)$  and multiplication $x\otimes y = x+y$. (This is semiring in the sense of [[rig]], hence sometimes the __tropical rig__.) 

[[tropical geometry|Tropical geometry]] is often thought as the algebraic geometry over the tropical semiring.


## Terminology

The tropical rig is also called the [[min-plus algebra]]. There is a related, in fact isomorphic rig called the [[max-plus algebra]]. (Some authors use the term 'tropical algebra' for the max-plus rather than the min-plus algebra.  The theories, of course, run in parallel, as each is the negative of the other.) 

In his survey article, cited below, Pin uses the term for a wide range of similar idempotent semirings. For instance $\mathcal{M} = (\mathbb{N} \cup{\infty}, min, +)$ is a tropical semiring introduced by [[Imre Simon]] in 1978.


## Properties

* The tropical semiring is an example of an [[additively idempotent semiring|idempotent semiring]], since for all elements $x$, we have $x\oplus x=x$.


## Examples
 {#Examples}

In the min-plus algebra we have, for instance:

$$
  \begin{aligned}
    (5\oplus 6)\otimes 7 
    &
    = min(5,6) + 7
    \\
    & = 
    5 + 7
    \\
    & = 
    12
    \,.
  \end{aligned}
$$



## Applications

Apart from applications in [[tropical geometry]], the min-plus and max-plus algebras have extensive use in providing algebraic models for simple [[discrete event system]]s related to timed [[Petri nets]].


## References

The use of the tropical algebra in [[discrete event systems]] is handled in many sources, e.g

* [[Jean-Eric Pin]], _Tropical semirings_, Publ. Newton Inst. 11 (1998) 50--69 &lbrack;[hal:00113779](), [pdf](https://hal.archives-ouvertes.fr/hal-00113779/file/Tropical.pdf)&rbrack;

* [[Stéphane Gaubert]], of INRIA Saclay (1999) &lbrack;[pdf](http://amadeus.inria.fr/gaubert/PAPERS/POLY12-02-1999.pdf)&rbrack;
 
Book collection of articles on idempotent semirings:

* J. Gunawardena (ed.), *Idempotency*, Cambridge University Press, 2001, 

An original source:

* [[Imre Simon]], (1978), _Limited Subsets of a Free Monoid_, in Proc. 19th Annual Symposium on Foundations of Computer Science, Piscataway, N.J., Institute of Electrical and Electronics Engineers, 143--150 ([doi:10.1109/SFCS.1978.21](https://doi.org/10.1109/SFCS.1978.21))

See also:

* Wikipedia, *[Tropical semiring](https://en.wikipedia.org/wiki/Tropical_semiring)*

and the first few pages of:

* {#Lawvere92} [[William Lawvere]], *Introduction to Linear Categories and Applications*, course lecture notes (1992) &lbrack;[pdf](https://github.com/mattearnshaw/lawvere/blob/192dac273e8bf352f307f87b9ec4fe8ef7dc85b9/pdfs/1992-introduction-to-linear-categories-and-applications.pdf), [[Lawvere-LinearCategories.pdf:file]]&rbrack;

Iterated sums and [[iterated integral]]s over semirings, where the case of tropical semiring is a central, with applications (including in [[machine learning]]),

* Joscha Diehl, [[Kurusch Ebrahimi-Fard]], Nikolas Tapia, _Tropical time series, iterated-sums signatures, and quasisymmetric functions_, SIAM Journal on Applied Algebra and Geometry __6__:4 (2022) [arxiv:2009.08443](https://arxiv.org/abs/2009.08443) [doi](https://doi.org/10.1137/20M1380041)


[[!redirects tropical semirings]]


[[!redirects tropical rig]]
[[!redirects tropical rigs]]



