[[!redirects empty 155]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
####Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}


## Idea
A [[Higman's embedding theorem|famous result by G. Higman]] in group theory says that a finitely generated group can be embedded in a finitely presented group precisely if it has a presentation whose defining relations are a recursively enumerable set of words. It has been conjectured by the group theorist W. Boone that the same result holds more generally for every single-sorted algebraic theory.

## Statement

...

## Lawvere on the Boone conjecture

>There is an issue involving recursivity that categorists should settle:
How general is Higman's theorem? In group theory the [[word problem]] (whether
a given finitely generated group is recursively related) is equivalent to
the purely algebraic one of whether the given group can be embedded as a
subgroup of a finitely presentable one. 
For which other algebraic categories is the same statement true? or
is it possibly true for the category of single-sorted [[algebraic theory|algebraic theories]]?
The latter problem was posed by Bill Boone, but as far as I know, is 
not yet resolved.

>For the category of [[predicate logic|first-order]] [[theory|theories]], a theorem analogous to Higman's
was proved by Craig and Vaught; for that case, they gave a kind of
intuitive argument: using a few additional predicates one can express
enough of number theory to encode a fragmentary satisfaction relation and
any given recursive set of axioms, so that one can then add the one
additional axiom that says "all those axioms are true".
Of course, it is non-trivial that this argument actually works.  ([Lawvere 2002](#Lawvere02))

## Partial results and failure of the conjecture for all single-sorted algebraic theories 

A category of models of an algebraic theory is said to satisfy the Higman property whenever any recursively presentable model embeds into a finitely presented model. The Higman property has been shown to hold for models of several algebraic theories such as rings, semigroups, inverse semigroups and Lie algebras, see ([Kukin 1989](#Kukin89)) for rings and references therein for the others. 

However, there are single-sorted algebraic theories whose models do not have the Higman property as remarked in the introduction of ([Kukin 1989](#Kukin89)). This is because having the Higman property implies an undecidable word problem under suitable conditions (see connection 2.8. in ([Kharlampovich 1995](#Kharlampovich95))) but for instance (non-associative) commutative algebras over a fixed field have a decidable word-problem ([Shirshov 2009](#Shirshov09)). 


## Related entries

* [[Higman's embedding theorem]]

* [[Lawvere theory]]

## References

* W. Craig, R. L. Vaught, _Finite axiomatizability using additional predicates_ , JSL **23** (1958) pp.289-308.

* M. H&#233;bert, _Finitely presentable morphisms in exact sequences_ , TAC **24** no.9 (2010) pp.209-220.([pdf](http://www.tac.mta.ca/tac/volumes/24/9/24-09.pdf))

* G. Higman, _Subgroups of finitely presented groups_ , Proc. Royal. Soc. London Ser. A (1961) pp.455-475.

* {#Kharlampovich95}O. G. Kharlampovich, &  M. V. Sapir, _Algorithmic problems in varieties._ International Journal of Algebra and Computation 5(04n05) (1995) pp.379-602.

* {#Kukin89}G. Kukin, _The variety of all rings has Higman's property._ 
Third Siberian School: Algebra and Analysis (1989); American Mathematical Society translations. Series 2 v. **163** (1995) pp.91-101.

* {#Lawvere02}[[William Lawvere|W. F. Lawvere]], _On the [[effective topos]] - message to catlist_, January 2002. ([link](http://facultypages.ecc.edu/alsani/ct02%281-2%29/msg00016.html))

* {#Shirshov09}Shirshov, Anatolii Illarionovich. _Some algorithmic problems for ε-algebras._ Selected Works of AI Shirshov. Birkhäuser Basel (2009) pp. 119-124.