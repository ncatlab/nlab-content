[[!redirects Higman's Theorem]]
[[!redirects Higman's theorem]]
[[!redirects Higman embedding theorem]]
[[!redirects Higman's Embedding Theorem]]

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
In 1961 G. Higman proved an important result in [[group theory]] that brings together in an intriguing way concepts from [[computability theory]] and [[finitely presentable object|finite presentability]].

## The result

**Higman's embedding theorem.** _A finitely generated group can be embedded in a finitely presented group iff it has a presentation (with a finite generating set) for which the set of defining relations is a recursively enumerable set of words._

**Theorem.** _There is a finitely presented group which contains an isomorphic copy of every finitely presented group._

## Lawvere on Higman's embedding theorem

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

## Related pages

* [[combinatorial group theory]]

* [[Boone conjecture]]

## Link

* [Wikipedia entry](https://en.wikipedia.org/wiki/Higman%27s_embedding_theorem)

## References

* G. Higman, _Subgroups of finitely presented groups_ , Proc. Royal. Soc. London Ser. A (1961) pp.455-475.

* W. Craig, R. L. Vaught, _Finite axiomatizability using additional predicates_ , JSL **23** (1958) pp.289-308.

* L. Dediu , _Higman's Embedding theorem - An Elementary Proof_ , Report CDMCTS-010 (1995).  ([pdf](https://www.cs.auckland.ac.nz/research/groups/CDMTCS/researchreports/010luminita.pdf))

* M. H&#233;bert, _Finitely presentable morphisms in exact sequences_ , TAC **24** no.9 (2010) pp.209-220.([pdf](http://www.tac.mta.ca/tac/volumes/24/9/24-09.pdf))

* {#Lawvere02}[[William Lawvere|W. F. Lawvere]], _On the [[effective topos]] - message to catlist_, January 2002. ([link](http://facultypages.ecc.edu/alsani/ct02%281-2%29/msg00016.html))