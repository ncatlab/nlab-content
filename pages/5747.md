
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

# Semi-simplicial sets
* table of contents
{:toc}

## Idea

A *semi-simplicial set* is like a [[simplicial set]], but without degeneracy maps: it is a sequence $\{X_n\}_{n \in \mathbb{N}}$ of [[sets]] together with [[functions]] called _face maps_ between them which encode that an element in $X_{n+1}$ has $(n+1)$ "faces" (boundary segments) which are elements in $X_{n}$.

The semi-simplicial set version of a [[simplicial complex]] is also called a _[[Delta set]]_.

## Definition

Let $\Delta$ denote the [[simplex category]], which is a [[skeleton]] of the [[category]] of [[inhabited set|inhabited]] [[finite set|finite]] [[totally ordered sets]].   Let $\Delta_+$ denote the [[wide subcategory]] of $\Delta$ containing only the [[injective functions]].   Thus, $\Delta_+$ is equivalent to the category of inhabited finite totally ordered sets and order-preserving injections.  

Recall that a [[simplicial set]] is a [[presheaf]] $X\colon \Delta^{op}\to Set$.  Similarly, a **semi-simplicial set** is a presheaf $X\colon \Delta_+^{op} \to Set$.

More generally, for $\mathcal{C}$ any other category, a functor $\Delta_+^{op} \to \mathcal{C}$ is a _[[semi-simplicial object]]_ in $\mathcal{C}$.


## Properties

### Relation to nerves of semi-categories

The [[nerve]] of a [[semicategory]] is a semi-simplicial set (satisfying the [[Segal conditions]]) just as the nerve of a [[category]] is a [[simplicial set]]. 

### Model category structure

There is a _[[model structure on semi-simplicial sets]]_, [[transferred model structure|transferred]] along the [[right adjoint]] of the [[forgetful functor]] from the [[model structure on simplicial sets]]. 

## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

  * [[simplicial object in an (∞,1)-category]]

* [[semi-simplicial object]]

* [[semicategory]]

* [[semi-Segal space]]

## Historical and terminological remarks
 {#History}

The original paper

* Eilenberg and Zilber, "Semi-Simplicial Complexes and Singular Homology", *Annals of Mathematics* vol. 51 no. 3 (1950), 499--513

defined both (what we now call) semi-simplicial sets, under the name *semi-simplicial complexes*, and (what we now call) simplicial sets, under the name *complete semi-simplicial complexes*.  The motivation for the name "semi-simplicial" was that a semi-simplicial set is like a [[simplicial complex]], but lacks the property that a [[simplex]] is uniquely determined by its vertices.  Then they added the degeneracies and a corresponding adjective "complete."

Over time it became clear that "complete semi-simplicial complexes" were much more important and useful than the non-complete ones.  This seems to have led first to the omission of the adjective "complete," and then the omission of the prefix "semi" (and at some point the replacement of "complex" by "set"), resulting in the current name [[simplicial sets]].

+--{: .query}
Anyone more knowledgable about the history, please correct/improve the preceding paragraph.
=--

The concept is essentially the same as that of $\Delta$-set, as used by Rourke and Sanderson. Their motivation was from geometric topology.

On the other hand, in other contexts the prefix "semi-" is used to denote absence of identities (such as a [[semigroup]] (which is, admittedly, missing more than identities relative to a group) or a [[semicategory]]),  thus if we start from the modern name "simplicial sets" it makes independent sense to refer to their degeneracy-less variant as "semi-simplicial sets."  This is coincidentally in line with the original terminology of Eilenberg and Zilber, but not of course with the intermediate usage of "semi-simplicial set" for what we now call a "simplicial set."


## References

*  C. P. Rourke,  and  B. J. Sanderson, _&#916;-Sets I: Homotopy Theory_. The Quarterly Journal of Mathematics 22: 321&#8211;338 (1971) ([PDF](http://www.maths.ed.ac.uk/~aar/papers/deltars.pdf))

* S. Buoncristiano, C.P. Rourke, and B. J. Sanderson, _A geometric approach to Homology Theory_, LMS Lect. Notes 18, (1976)

* [[Peter Hilton]], _On a generalization of nilpotency to semi-simplicial complexes_ ([pdf](http://plms.oxfordjournals.org/content/s3-10/1/604.full.pdf))

* [[Alex Heller]], _Homotopy resolutions of semi-simplicial complexes_, Transactions of the American Mathematical Society Vol. 80, No. 2 (Nov., 1955), pp. 299-344 ([JSTOR](http://www.jstor.org/stable/1992992))

* James E. McClure, On semisimplicial sets satisfying the Kan condition ([ArXiv](http://arxiv.org/abs/1210.5650)).

Discussion of a [[model structure on semi-simplicial sets]]:

* [[Benno van den Berg]], _A note on semisimplicial sets_, 2013 ([[vandenBerg_SemisimplicialSets.pdf:file]])


See also the references at _[[semi-simplicial object]]_.

and 

* Wikipedia, _[Delta sets](http://en.wikipedia.org/wiki/Delta_set)_

* MO, _[Semi-simplicial versus simplicial sets (and simplicial categories)](http://mathoverflow.net/questions/75094/semi-simplicial-versus-simplicial-sets-and-simplicial-categories)_
    _[Degeneracies for semi-simplicial Kan complexes](http://mathoverflow.net/questions/57653/degeneracies-for-semi-simplicial-kan-complexes/)_

[[!redirects semi-simplicial sets]]
[[!redirects semisimplicial set]]
[[!redirects semisimplicial sets]]


[[!redirects Delta set]]
[[!redirects Delta sets]]
