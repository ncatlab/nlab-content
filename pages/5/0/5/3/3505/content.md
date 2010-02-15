<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The [[model category]] structure on the [[category]] of [[category with weak equivalences|categories with weak equivalences]] is a model for the [[(∞,1)-category of (∞,1)-categories]].

Every [[category with weak equivalences]] $C$ presents under Dwyer-Kan [[simplicial localization]] a [[simplicially enriched category]] or alternatively under [[Charles Rezk]]'s _simplicial nerve_ a [[complete Segal space|Segal space]], both of which are incarnations of a corresponding [[(∞,1)-category]] $\mathbf{C}$ with the same objects of $C$, at least the 1-morphisms of $C$ and such that every weak equivalence in $C$ becomes a true equivalence ([[homotopy equivalence]]) in $\mathbf{C}$.

## Details

For the purposes of the present entry, we understand under a [[category with weak equivalences]] the absolute minimum structure that may deserve to go by that name, namely a **relative category**:

**Definition** A **relative category** $(C,W)$ is a [[category]] $C$ equipped with a choice of [[wide subcategory]] $W$.

A morphism in $W$ are called a **weak equivalence** in $C$. Notice that we do not require here that these weak equivalence satisfy [[category with weak equivalences|2-out-of-3]], nor even that they contain all [[isomorphism]]s. 

A morphism $(C_1,W_1) \to (C_2,W_2)$ of relative catgeories is a [[functor]] $C_1 \to C_2$ that preserves weak equivalences.

Write $RelCat$ for the [[category]] of relative categories and such morphisms between them.

### Model category structure

The model category structure on $RelCat$ is obtained from that on [[bisimplicial set]]s modelling [[complete Segal space]]s in section 6.1  of

* [[Clark Barwick]] and [[Dan Kan]], _Relative categories; another model for the homotopy theory of homotopy theories -- Part I: the model structure_ ([pdf](http://www.math.harvard.edu/~clarkbar/barwick-kan.pdf))


### Nerve functors

The compatibility of the various nerve and simplicial localization functors is in section 1.11 of 

* [[Clark Barwick]] and [[Dan Kan]], _Relative categories; another model for the homotopy theory of homotopy theories -- Part II: the weak equivalences_ ([pdf](http://www.math.harvard.edu/~clarkbar/bar-kan-we.pdf))

## References

* [[Clark Barwick]] and [[Dan Kan]], 

  * _Relative categories; another model for the homotopy theory of homotopy theories -- Part I: the model structure_ ([pdf](http://www.math.harvard.edu/~clarkbar/barwick-kan.pdf))

  * _Relative categories; another model for the homotopy theory of homotopy theories -- Part II: the weak equivalences_ ([pdf](http://www.math.harvard.edu/~clarkbar/bar-kan-we.pdf))

  * Partial model categories and their simplicial nerves, a relative Yoneda embedding, and a Quillen theorem $B_n$ for homotopy pullbacks ([pdf](http://www.math.harvard.edu/~clarkbar/partmodcat.pdf))