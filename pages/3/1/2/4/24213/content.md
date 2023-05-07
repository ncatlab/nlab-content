Note: This page is an update of a page initially posted on the wiki of the special year on Univalent Foundations at IAS in 2012-13.

One interesting open problem (considered by [[Vladimir Voevodsky]] and others): define _[[semi-simplicial object|semi-simplicial]]_ types in Homotopy Type Theory.

Classically, a _[[semi-simplicial object]]_ in a category is like a simplicial object, but without degeneracy maps; i.e. a contravariant functor from the category $\Delta_i$, of finite nonempty ordinals and just injections between them.

Can we define these internally to type theory, that is as a functor from $\Delta_i$ to types in Homotopy Type Theory?

The initial idea, proposed at IAS, was to represent semi-simplicial types not as a contravariant functor but, iterating the correspondence between fibrations and families, as a family of families, what could be called an "indexed", or iterated-dependent, presentation of semi-simplicial types.

## Semi-simplicial types as families of families of n-semi-simplices

To illustrate the idea of semi-simplicial types as families of families of $n$-semi-simplices, let us consider the finite-dimensional parts of such semi-simplicial type:

A 0-semi-simplicial type is just a type $X_0\,:\,Type$.

A 1-semi-simplicial type: $X_0\,:\,Type$, and $X_1\,:\,X_0 \rightarrow X_0 \rightarrow Type$.

A 2-semi-simplicial type:

  $X_0\,:\,Type$;  
  $X_1\,:\, X_0 \rightarrow X_0 \rightarrow Type$;  
  $X_2\,:\,forall\:(x y z\,:\,X_0)\:(f\,:\,X_1 x y)\:(g\,:\,X_1 y z)\:(h\,:\,X_1 x z), Type$

A 3-semi-simplicial type:

  $(X_0,X_1,X_2)$ as before; and  
  $X_3:\,forall (\text{tetrahedral configurations from} X_0 \ldots X_2), Type$

And so on.

Each of these can be tupled up as a single type.

* Can we define a function "$\text{Semi-simplicial}\,:\,nat \rightarrow Type$", such that for $n = 0,1,2,3$, $\text{Semi-simplicial}~n$ is (equivalent to) the objects explicitly defined here?

* Can we define a type of semi-simplicial types (i.e. infinity-semi-simplicial types) with $n$-simplices for all $n$?

A first [sketch of definition](https://ncatlab.org/ufias2012/files/semisimplicial.v) was proposed by [[Vladimir Voevodsky]] in Coq, suggesting that defining such families requires to define restrictions, then to prove that restrictions of restrictions commute, but then also to prove higher-dimensional coherence conditions on restrictions.

Hugo Herbelin worked on a formalization in Coq based on the presentation of $\Delta_i$ with face maps $d_i$. On 3/20/2013, he made available a [note](https://ncatlab.org/ufias2012/files/semi-simplicial.pdf) describing the construction in Coq extended with the principle of [[Uniqueness of Identity Proofs|uniqueness of identity proofs]] (UIP). UIP was used to cut down the need for higher-dimensional coherence, so morally, it meant that types were actually [[h-sets]]. The outcome of the formalization was however to precisely describe how to define an alternative "indexed", or "dependently-typed", presentation of semi-simplicial sets.

To cut the need for higher-dimensional coherences, several extensions of type theory were considered:
* Vladimir Voevodsky proposed Homotopy Type Theory (HTT), an extensional type theory with non-fibrant types and two equalities;
* Fedor Part and Zhaohui Luo proposed a "Logic-enriched Homotopy Type Theory", in particular, they formalized a construction of semi-simplicial types in this logic using the Plastic proof assistant;
* Thorsten Altenkirch, Paolo Capriotti and Nicolai Kraus proposed a two-level type theory generalizing HTT, leading to 2LTT by Dannil Annenkov, Paolo Capriotti, Nicolai Kraus and Christian Sattler, providing another construction of semi-simplicial types in an extended type theory;
* According to Nicolai Kraus 2018, semi-simplicial types can also be constructed in Angiuli-Harper-Wilson's computational higher-dimensional type theory. 

## Other approaches

The "indexed" approach as families of families with iterated dependencies is only one possible approach! Other approaches to the problem are also possible, and may be better.

An alternative idea is something like "in the simplicial model, or more generally in other homotopy-theoretic model, they should be equivalent to coherent (possibly: Reedy-fibrant) semi-simplicial objects".

Why not imitate the classical definition, using internal functors from the internally-defined category $\Delta{}_i$? Giving a reasonable definition of $\Delta{}_i$ is not too hard: the objects [n] are very well-behaved. But defining functors out of it is problematic, because there are coherence issues. One would have to specify the functoriality laws using equations, i.e. inhabitants of equality types, which homotopically we treat as paths. But specified paths in homotopy theory have to be coherent to define a useful notion of functor; thus we need equations between our equations (associativity pentagons, etc), then higher equations between those, and so on forever. Thus we end up with the same problem we had before of specifying infinitely much data using a finite description in type theory.

If one restricts the types involved to h-sets, then this problem go away; but then one has again only defined semi-simplicial h-sets, which are (presumably) strictly less general.

Another approach is to extend type theory with streams typed by streams of types as in a HoTTEST talk by Kolomatskaia.

## Why semi-simplicial, not simplicial?

With semi-simplicial sets, the “iterated dependency” approach gives us at least a candidate approach for tackling coherence issues. With simplicial sets, it’s hard to see how one might tackle or avoid them. (Comparing it to the semi-simplicial approach, one requires degeneracy maps and equations between them, which lets loose the spectre of coherence again.) Furthermore, reasoning about Kan simplicial sets seems to insist on classical logic. For example, the classical result stating the homotopy equivalence of fibers of a Kan fibration cannot be proved constructively ([pdf](https://ncatlab.org/ufias2012/files/countermodel.pdf)).

In homotopy-theoretic terms, this is because $\Delta{}_i$ is a [[direct category]], while $\Delta$ is not. 

## About the original page on the wiki of the Univalent Foundations year

The original page about semi-simplicial types on the wiki of the Univalent Foundations year contained also material related to semi-simplicial set in general though not to semi-simplicial types properly speaking. It is kept here for historical reasons.

**Update 4/12**: [A note on semisimplicial sets](https://ncatlab.org/ufias2012/files/semisimplicialsets.pdf) by Benno van den Berg.

**Update 4/15**: [A note on a presheaf model for simplicial sets](https://ncatlab.org/ufias2012/files/countermodel.pdf) by Marc Bezem and Thierry Coquand.

**Update 6/24**: Accompanying files to Update 4/15:

* [CL.pl](https://ncatlab.org/ufias2012/files/CL.pl), the prover for coherent logic (requires [SWI-Prolog](http://www.swi-prolog.org/))
* [X.in](https://ncatlab.org/ufias2012/files/X.in), a formalization of the model in coherent logic
* [X.model](https://ncatlab.org/ufias2012/files/X.model), the edges, fill1 and fill2, day by day, generated by the prover from input X.in.
* [X.v](https://ncatlab.org/ufias2012/files/X.v), a Coq script verifying the proof that no homotopy equivalence between the fibers can exist in the model.

## See also

* [[open problems in homotopy type theory]]

## References

* [Semi-simplicial Types in Logic-enriched Homotopy Type Theory, Fedor Part, Zhaohui Luo](http://arxiv.org/abs/1506.04998 ) (Submitted on 16 Jun 2015) 

* [Extending Homotopy Type Theory with Strict Equality, Thorsten Altenkirch, Paolo Capriotti, and Nicolai Kraus](https://arxiv.org/abs/1604.03799) (Submitted on Apr 2016)

* [Two-Level Type Theory and Applications
Danil Annenkov, Paolo Capriotti, Nicolai Kraus, Christian Sattler](https://arxiv.org/abs/1705.03307) (Submitted on May 2017)

* [Space-valued diagrams, type-theoretically (extended abstract), Nicolai Kraus, Christian Sattler](https://arxiv.org/abs/1704.04543) (Submitted on Apr 2017)

* [On the Role of Semisimplicial Types, Nicolai Kraus, 2018](https://www.cs.nott.ac.uk/~psznk/docs/on_semisimplicial_types.pdf)