
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Semi-simplicial sets
* table of contents
{:toc}

## Idea

A *semi-simplicial set* is like a [[simplicial set]], but without the degeneracy maps: it is a sequence $\{X_n\}_{n \in \mathbb{N}}$ of [[sets]] together with [[functions]] called _face maps_ between them which encode that an element in $X_{n+1}$ has $(n+1)$ "faces" (boundary segments) which are elements in $X_{n}$.

The semi-simplicial set version of a [[simplicial complex]] is also called a _[[Delta set]]_.

## Definition

Let $\Delta$ denote the [[simplex category]], which is a [[skeleton]] of the [[category]] of [[inhabited set|inhabited]] [[finite set|finite]] [[totally ordered sets]].   Let $\Delta_+$ denote the [[wide subcategory]] of $\Delta$ containing only the [[injective functions]].   Thus, $\Delta_+$ is equivalent to the category of inhabited finite totally ordered sets and order-preserving injections.  

Recall that a [[simplicial set]] is a [[presheaf]] $X\colon \Delta^{op}\to Set$.  Similarly, a **semi-simplicial set** is a presheaf $X\colon \Delta_+^{op} \to Set$.

More generally, for $\mathcal{C}$ any other category, a functor $\Delta_+^{op} \to \mathcal{C}$ is a _[[semi-simplicial object]]_ in $\mathcal{C}$.


## Properties

### Adjunction with simplicial sets
 {#AdjunctionWithSimplicialSets}

The [[forgetful functor]] from [[SimplicialSets]] to the [[category]] of semi-simplicial sets is given by precomposition with the [[opposite functor]] of the non-[[full subcategory|full]] [[wide subcategory]] inclusion

$$
  \Delta_{inj} \xrightarrow{\;j\;} \Delta
$$

into the [[simplex category]] and hence has both a [[left adjoint]] as well as a [[right adjoint]] given by left/right [[Kan extension]], respectively:

\begin{tikzcd}[column sep=small]
  \mathrm{SemiSimplSets}
  \ar[
    rr,
    shift left=18pt,
    "j_!"{above}
  ]
  \ar[
    rr,
    shift right=18pt,
    "j_\ast"{below}
  ]
  &&
  \mathrm{SimplSets}
  \ar[
    ll,
    "j^\ast"{description}
  ]
  \ar[ll, shift left=10pt, phantom, "\scalebox{.7}{$\bot$}" ]
  \ar[ll, shift right=10pt, phantom, "\scalebox{.7}{$\bot$}" ]
\end{tikzcd}

The [[adjunction unit]] of the left [[adjoint pair]]

$$
  X \xrightarrow{ \;\eta_X\; } j^\ast j_! X
$$

is a [[weak homotopy equivalence]] in the sense that its [[geometric realization]] is so ([Rourke & Sanderson 71, Rem. 5.8](#RourkeSanderson71)).

Notice that 

1. for $X \in $ [[SimplicialSets]], the [[geometric realization]] of the underlying semi-simplicial set $j^\ast X$ is the *[[fat geometric realization]]* of $X$ (see [there](geometric+realization+of+simplicial+topological+spaces#FatGeometricRealization)):

   $$
     \left\Vert X \right\Vert
     \;\coloneqq\;  
     \left\vert j^\ast X \right \vert
   $$

1. There is (by [this Prop.](https://ncatlab.org/nlab/source/geometric+realization+of+simplicial+topological+spaces#FatRealizationOfGoodSimplicialSpaces)) a natural [[weak homotopy equivalence]] from the fat to the ordinay geometric realization of a simplicial set (which is always "[[good simplicial topological space|good]]" when regarded as a simplicial space):

   $$
     \left\vert j^\ast X \right \vert
     \;\simeq_{whe}\;
     \left\vert X \right \vert
     \,.
   $$

It follows (see also [MO:a/75101](https://mathoverflow.net/a/75101/381)) that also the [[adjunction counit]]

$$
  j_! j^\ast X \xrightarrow{\; \epsilon_X \;} X
$$

is a [[simplicial weak equivalence]].

### Relation to semi-categories

The [[nerve]] of a [[semicategory]] is a semi-simplicial set (satisfying the [[Segal conditions]]) just as the nerve of a [[category]] is a [[simplicial set]]. 

### Model category structure

There is a _[[model structure on semi-simplicial sets]]_, [[transferred model structure|transferred]] along the [[right adjoint]] to the [[forgetful functor]] from the [[model structure on simplicial sets]]. 

## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

  * [[simplicial object in an (∞,1)-category]]

* [[semi-simplicial object]]

* [[semicategory]]

* [[semi-Segal space]]

## Historical and terminological remarks
 {#History}

The original paper [Eilenberg & Zilber 50](#EilenbergZilber50) defined both (what we now call) semi-simplicial sets, under the name *semi-simplicial complexes*, and (what we now call) simplicial sets, under the name *complete semi-simplicial complexes*.  The motivation for the name "semi-simplicial" was that a semi-simplicial set is like a [[simplicial complex]], but lacks the property that a [[simplex]] is uniquely determined by its vertices.  Then they added the degeneracies and a corresponding adjective "complete."

Over time it became clear that "complete semi-simplicial complexes" were much more important and useful than the non-complete ones.  This seems to have led first to the omission of the adjective "complete," and then the omission of the prefix "semi" (and at some point the replacement of "complex" by "set"), resulting in the current name [[simplicial sets]].

The concept is essentially the same as that of $\Delta$-set, as used by [Rourke & Sanderson 71](#RourkeSanderson71). Their motivation was from geometric topology.

On the other hand, in other contexts the prefix "semi-" is used to denote absence of identities (such as a [[semigroup]] (which is, admittedly, missing more than identities relative to a group) or a [[semicategory]]),  thus if we start from the modern name "simplicial sets" it makes independent sense to refer to their degeneracy-less variant as "semi-simplicial sets."  This is coincidentally in line with the original terminology of Eilenberg and Zilber, but not of course with the intermediate usage of "semi-simplicial set" for what we now call a "simplicial set."

## Related concepts

* [[semi-simplicial object]]

* [[semi-simplicial topological space]]

## References

* {#EilenbergZilber50} [[Samuel Eilenberg]], [[Joseph Zilber]], *Semi-Simplicial Complexes and Singular Homology*, *Annals of Mathematics* vol. 51 no. 3 (1950), 499--513 ([jstor:1969364](https://www.jstor.org/stable/1969364))

* [[Daniel Kan]], *Is an ss complex a css complex?*, Advances in Mathematics
Volume 4, Issue 2, April 1970, Pages 170-171 (<a href="https://doi.org/10.1016/0001-8708(70)90021-6">doi:10.1016/0001-8708(70)90021-6</a>)

*  {#RourkeSanderson71} [[Colin Rourke]],  [[Brian Sanderson]], _&#916;-Sets I: Homotopy Theory_. The Quarterly Journal of Mathematics 22: 321&#8211;338 (1971) ([doi:10.1093/qmath/22.3.321](https://doi.org/10.1093/qmath/22.3.321), [pdf](http://www.maths.ed.ac.uk/~aar/papers/deltars.pdf))

* S. Buoncristiano, [[Colin Rourke]], [[Brian Sanderson]], _A geometric approach to Homology Theory_, LMS Lect. Notes 18, (1976)

* [[Peter Hilton]], _On a generalization of nilpotency to semi-simplicial complexes_ ([pdf](http://plms.oxfordjournals.org/content/s3-10/1/604.full.pdf))

* [[Alex Heller]], _Homotopy resolutions of semi-simplicial complexes_, Transactions of the American Mathematical Society Vol. 80, No. 2 (Nov., 1955), pp. 299-344 ([JSTOR](http://www.jstor.org/stable/1992992))

* [[James McClure]], On semisimplicial sets satisfying the Kan condition ([arXiv:1210.5650](http://arxiv.org/abs/1210.5650)).

See also the references at _[[semi-simplicial object]]_ and:

* Wikipedia, _[Delta sets](http://en.wikipedia.org/wiki/Delta_set)_

* MO, _[Semi-simplicial versus simplicial sets (and simplicial categories)](http://mathoverflow.net/questions/75094/semi-simplicial-versus-simplicial-sets-and-simplicial-categories)_
    _[Degeneracies for semi-simplicial Kan complexes](http://mathoverflow.net/questions/57653/degeneracies-for-semi-simplicial-kan-complexes/)_


On the [[model structure on semi-simplicial sets]]:

* [[Benno van den Berg]], _A note on semisimplicial sets_, 2013 ([[vandenBerg_SemisimplicialSets.pdf:file]])


[[!redirects semi-simplicial sets]]
[[!redirects semisimplicial set]]
[[!redirects semisimplicial sets]]


[[!redirects Delta set]]
[[!redirects Delta sets]]
