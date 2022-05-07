
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _strict model 2-category_ is a [[strict 2-category]] $C$ -- hence a [[category]] [[enriched category|enriched over]] [[Cat]] -- whose underlying [[category]] $C_1$ is equipped with the structure of a [[model category]] which is compatible, in some sense, with the [[folk model structure]] on the enrichment category [[Cat]].

The compatibility is such that in particular the notion of [[homotopy limit]] and of [[strict 2-limit|pseudo-limit]] coincide in such model 2-category.

To state the definition of a strict model 2-category, we need the following notation:

## Notation

For $C$ a [[enriched category|category enriched over]] [[Cat]] and for
$$
  u : X \to Y
$$
$$
  v : V \to W
$$
two morphisms in $C$, let 

$$
  [u,v] : C(Y,V) \to C(Y,W) \times_{C(X,W)} C(X,V)
$$
be the unique morphism induced from the commutativity of the diagram
$$
  \array{
    C(Y,V) &\stackrel{C(u,V)}{\to}& C(X,V)
    \\
    \downarrow^{C(Y,v)} && \downarrow^{C(X,v)}
    \\
    C(Y,W) &\stackrel{C(u,W)}{\to}& C(X,W)
  }
  \,.
$$

## Definition

The structure of a **model 2-category** on a [[strict 2-category]] $C$ with finite limits and colimits is

* a [[model category]] structure on the underlying 1-category $C_1$;

* such that

  * if $u : X \to Y$ is a cofibration and $v : V \to W$ is a fibration in $C_1$ then the functor $[u,v]$ defined above is an [[isofibration]] in [[Cat]];

  * and $[u,v]$ is a weak equivalence (in the [[folk model structure]] on [[Cat]], i.e. an [[equivalence of categories]]) if either of $u$ or $v$ is.

This is just the usual notion of an [[enriched model category]] specialized to enrichment over the [[monoidal model category]] $Cat$.


## Examples 

* Every suitably complete and cocomplete 2-category admits a "trivial" or "natural" model 2-category structure in which the weak equivalences are the categorical equivalences and the fibrations are the internal [[isofibration]]s.  By duality, there also is a second such model structure; in Cat both coincide with the [[folk model structure]].

* The 2-category $T Alg_s$ of algebras and _strict_ morphisms for a suitably well-behaved (strict) [[2-monad]] $T$ inherits a model structure where the weak equivalences are those that become weak equivalences in the underlying category.  These are precisely the morphisms that are equivalences in the 2-category $T Alg$ of $T$-algebras and _pseudo_ morphisms, so $T Alg$ is the "homotopy 2-category" of $T Alg_s$. Cofibrant replacements in this model structure can also be identified with [[flexible algebra|flexible]] replacements in the theory of 2-monads.

* The 2-category $[C,K]$ of diagrams in any 2-category $K$ also inherits two different, but Quillen equivalent, model structures, called the "projective" and "injective" model structures.


## Remarks

* Every model 2-category has a [[homotopy 2-cateory|homotopy (weak) 2-category]] which can be constructed by formally making the weak equivalences into categorical equivalences.  It can alternately be described using fibrant and cofibrant replacements, just like the ordinary homotopy category of a model category.

* In a strict model 2-category with a _natural_ model structure, the notions of 2-categorical [[strict 2-limit|pseudo-limit]] and (one canonical construction of) [[model category|model theoretic]] [[homotopy limit]]s coincide.  For a general model 2-category, homotopy limits can be construed as representatives of [[2-limit]]s in its homotopy 2-category.

## Related concepts

* [[homotopy 2-category]]

## References

The original reference, which constructs the natural model structure and its lifting to 2-monads, is:

* [[Steve Lack]], _Homotopy theoretic aspects of 2-monads_, Journal of Homotopy and Related Structures, Vol. 2(2007), No. 2, pp. 229-260 ([math.CT/0607646](http://www.arxiv.org/abs/math.CT/0607646))

The projective and injective model structures on diagrams, and the relation between pseudo-limits and homotopy limits, are discussed in the following (especially section 6).

* [[Nicola Gambino]], _Homotopy limits for 2-categories_, Mathematical Proceedings of the Cambridge Philosophical Society 145 (2008) 43-63 ([pdf](http://www1.maths.leeds.ac.uk/~pmtng/Publications/homotopy.pdf))
