
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Due to [[Paul Taylor]], Abstract Stone Duality (ASD) is a re-[[axiom|axiomatisation]] of the notions of *[[topological space]]* and *[[continuous function]]* in [[general topology]] in terms of a [[lambda calculus|lambda-calculus]] of [[computable function|computable]] [[continuous functions]] and [[predicates]].

Abstract Stone duality is both [[constructive mathematics|constructive]] and [[computable mathematics|computable]], thus being one approach to [[synthetic topology]].

The topology on a space is treated not as a discrete [[lattice]], but as an [[exponential object]] of the same [[category]] as the original space, with an associated &#955;-calculus (which includes an [[internalization|internal]] lattice structure). Every expression in the &#955;-calculus denotes both a continuous function and a program. ASD does not use the [[Set|category of sets]] (or any [[topos]]), but the [[full subcategory]] of [[overt space|overt]] [[discrete space|discrete]] objects plays this role (an overt object is the dual to a [[compact space|compact]] object), forming an [[arithmetic pretopos]] (a [[pretopos]] with [[lists]]) with general [[recursion]]; an optional 'underlying set' axiom (which is not [[predicative mathematics|predicative]]) will make this a topos.

The classical (but not constructive) theory of [[locally compact space|locally compact]] [[sober space|sober]] [[topological space]]s is a model of ASD, as is the theory of locally compact [[locale]]s over any topos (even constructively).  In "Beyond Local Compactness" on the ASD website, Taylor removes the restriction of local compactness.

## Related concepts

* [[Stone duality]]


## References

*  [[Paul Taylor]], *Abstract Stone Duality* ([www.paultaylor.eu/ASD](http://www.paultaylor.eu/ASD))

* [[Paul Taylor]], *Review of Abstract Stone Duality* (2004) &lbrack;[pdf](https://cdc.ioc.ee/appsem04/webproc/short/taylor.pdf)&rbrack;
 
On [[Dedekind real numbers]] via abstract Stone duality:


*  [[Paul Taylor]], *[Dedekind cuts](http://www.paultaylor.eu/ASD/dedras/classical)* (2007-2009?)

* [[Andrej Bauer]], [[Paul Taylor]], *The Dedekind reals in abstract Stone duality*, Mathematical Structures in Computer Science **19** 4 (2009) 757-838 &lbrack;[doi:10.1017/S0960129509007695](https://doi.org/10.1017/S0960129509007695)&rbrack;

review in:

* [[Andrej Bauer]], *Efficient Computation with Dedekind Reals*, talk at *[Computability and complexity in analysis 2008](https://math.andrej.com/2008/08/24/efficient-computation-with-dedekind-reals/)* and at *[Mathematics, Algorithms and Proofs 2008](http://cdsagenda5.ictp.trieste.it/full_display.php?smr=0&ida=a07167)* (2008) &lbrack;[web](https://math.andrej.com/2008/08/24/efficient-computation-with-dedekind-reals/), slides: [pdf](https://math.andrej.com/wp-content/uploads/2008/08/slides-map2008.pdf), extended abstract: [pdf](https://math.andrej.com/wp-content/uploads/2008/08/abstract-cca2008.pdf)&rbrack;


See also:

*  [Caf&#233; discussion](http://golem.ph.utexas.edu/category/2009/01/abstract_stone_duality.html)



[[!redirects Abstract Stone Duality]]
[[!redirects abstract stone duality]]
[[!redirects ASD]]