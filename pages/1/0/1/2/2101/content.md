
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Monadic adjunctions
* table of contents
{: toc}


## Idea

One can turn [[monads]] into [[adjunctions]] and adjunctions into monads, but one doesn\'t always return where one started.  Every monad comes from an adjunction, but only a _monadic adjunction_ comes from a monad via a [[monadic functor]].  (To be fair, there are two ways to turn a monad into an adjunction, given by the [[Kleisli category]] and the [[Eilenberg–Moore category]]; we are talking about the latter here.)


## Definition

We give the definitions in [[Cat]] and leave it to future readers and writers to generalise.  See for instance ([Riehl-Verity 13](#RiehlVerity13)).

Let $(C,D,\ell,r,\iota,\epsilon)$ be an adjunction in $Cat$; that is, $\ell: C \to D$ and $r: D \to C$ are [[adjoint functors]] with $\ell \dashv r$, where $\iota$ and $\epsilon$ are the unit and counit.  Let $T$ be $r \circ \ell$; $T$ has the structure of a monad on $C$, so consider the [[Eilenberg–Moore category]] $C^T$ of [[module for a monad|modules (algebras)]] for $T$.  Then $r \circ \epsilon: T \circ r \to r$ endows $r: D \to C$ with a $T$-algebra structure, hence defines a [[functor]] $k: D \to C^T$.

The adjunction $\ell \dashv r$ is __monadic__ if this functor $k$ is an [[equivalence of categories]].  


## Beck's monadicity theorem

__Beck's Monadicity Theorem__ gives a necessary and sufficient condition for an adjunction to be monadic.  Namely, the adjunction $(C,D,\ell,r,\iota,\epsilon)$ is monadic iff:

*  $r$ reflects isomorphisms; and
   
*  $D$ has coequalizers of $r$-split coequalizer pairs, and $r$ preserves those coequalizers.

See [[monadicity theorem]] for more details and variants.


## Algebraic categories

The typical categories studied in [[algebra]], such as [[Grp]], [[Ring]], etc, all come equipped with monadic adjunctions from [[Set]].  Specifically, the [[right adjoint]] is the [[forgetful functor]] from algebras to sets, and the [[left adjoint]] maps each set to the [[free object|free]] algebra on that set.  Their composite (a monad on $Set$) may be thought of as mapping a set $A$ to the set of words with alphabet taken from $A$ and the connections between letters taken from the appropriate algebraic operations, with two words identified if they can be proved equal by the appropriate algebraic axioms.

Abstractly, one may *define* an [[algebraic category]] to be a category equipped with a monadic adjunction from $Set$.  However, there are now more examples than the ones from algebra; the best known of these is the category of [[compact Hausdorff spaces]], which corresponds to the [[ultrafilter]] monad.  (This result relies on the [[ultrafilter principle]], regardless of whether one interprets 'space' here as referring to [[topological spaces]] or [[locales]].)


## Semantics-structure adjunction

The relationship between monads and adjunctions itself constitutes an adjunction called the **semantics-structure adjunction**. Explicitly, for a category $C$ there exist contravariant functors $Str:Cat_{/C}^*\to Mon(C):Sem$ with $Str\dashv Sem$ where $Cat_{/C}^*$ denotes the full subcategory of $Cat_{/C}$ consisting of functors admitting a codensity monad; $Str$ sends a functor to its corresponding codensity monad and $Sem$ sends a monad to the forgetful functor from its E-M category to $C$. Intuitively speaking we may think of a monad as a kind of structure with which the objects of $\mathcal{C}$ can be equipped presented in a syntax-independent way, and we may think of the E-M category of a monad (viewed as a syntax independent presentation of an equational theory) as the category of models of this theory, which is often referred to by logicians as the semantics of the theory. For more on this, see for instance section 5 of ([Schäppi 2009](#DanielSchäppi1)).


## Examples

1. [[Eilenberg-Moore categories]] are obviously all examples, and up to equivalence, the only examples.
2. If the categories are pre-orders, then a monadic adjunction is a [[Galois connection]] where the right adjoint reflects ordering and dually a comonadic adjunction is a Galois connection where the left adjoint reflects ordering.
3. More generally an [[idempotent adjunction]] is monadic if and only if the right adjoint is [[fully faithful]], i.e. essentially a [[reflective subcategory]] inclusion. Dually, a comonadic idempotent adjunction is essentially a [[coreflective]] subcategory inclusion.

## Related pages

* [[monadic functor]]
* [[monadic decomposition]]
* [[nuclear adjunction]]

## References

* [[Michael Barr]] and [[Charles Wells]], _Toposes, Triples and Theories_ ([online](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html))

Discussion for [[quasi-categories]] is around definition 6.1.15 and definition 7.1.6 in

* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))


* {#DanielSchäppi1} Daniel Schäppi, _Tannaka duality for comonoids in cosmoi_ ([arXiv:0911.0977](https://arxiv.org/abs/0911.0977))


* Alec Rhea ([MO user page](https://mathoverflow.net/users/92164/alec-rhea)), _Semantics-structure adjunction_, URL (version: 2019-01-13): <https://mathoverflow.net/q/320698>


[[!redirects semantics-structure adjunction]]
[[!redirects structure-semantics adjunction]]


[[!redirects monadic adjunctions]]