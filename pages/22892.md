
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

For $\mathcal{C}$ a [[model category]], there is canonically induced a model category structure on the corresponding [[category of pointed objects]] $\mathcal{C}^{\ast/}$, namely the [[coslice model structure]] under "the point", i.e. under the [[terminal object]] $\ast \in \mathcal{C}$.

## Definition

As a special case of the general discussion at *[[coslice model structures]]*, we have:

\begin{prop}\label{ModelStructureOnSliceCategory}
  Let $\mathcal{C}$ be a [[model category]] with [[terminal object]] dented $\ast \in \mathcal{C}$. Then there is a model category structure on its [[category of pointed objects]] $\mathcal{C}^{\ast/}$, hence on the [[coslice category|category under]] $\ast$, whose classes of morphisms ([[weak equivalences]], [[fibrations]], [[cofibrations]]) are those created by the [[forgetful functor]] $\mathcal{C}^{\ast/} \to \mathcal{C}$.
\end{prop}

(e.g. [Hovey 99, Prop. 1.1.8](#Hovey99))

## Examples

+-- {: .num_example #ClassicalPointedHomotopyCategory}
###### Example
**([[classical model structure on pointed topological spaces]])**

For $\mathcal{C} = Top_{Qu}$, the [[classical model structure on topological spaces]], then the model structure on [[pointed topological spaces]] induced via prop. \ref{ModelStructureOnSliceCategory} we call the _[[classical model structure on pointed topological spaces]]_ $Top_{Qu}^{\ast/}$. Its [[homotopy category of a model category]] is the _classical pointed homotopy theory_ $Ho(Top^{\ast/})$.

=--

## Properties

+-- {: .num_remark #NonDegenerateBasepointAsCofibrantObjects}
###### Remark

The [[fibrant objects]] in the pointed model structure $\mathcal{C}^{\ast/}$, prop. \ref{ModelStructureOnSliceCategory}, are those that are fibrant as objects of $\mathcal{C}$.

But the [[cofibrant objects]] in $\mathcal{C}^{\ast}$ are now those for which the basepoint inclusion is a [[cofibration]] in $X$.

For $\mathcal{C}^{\ast/} = Top^{\ast/}_{Qu}$ (Ex. \ref{ClassicalPointedHomotopyCategory}), the cofibrant pointed topological spaces are typically referred to as spaces _with non-degenerate basepoints_. Notice that the point itself is cofibrant in $Top_{Qu}$, so that cofibrant pointed topological spaces are in particular cofibrant topological spaces.

=--


+-- {: .num_example #HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}
###### Example

For $\mathcal{C}$ any [[model category]], with $\mathcal{C}^{\ast/}$ its [[slice model structure|pointed model structure]] according to Prop. \ref{ModelStructureOnSliceCategory}, then corresponding [[homotopy category of a model category|homotopy category]] is, (by [this Remark](pointed+object#PointedObjectsHaveZeroObject)), canonically [[enriched category|enriched]] in [[pointed sets]], in that its [[hom-functor]] is of the form

$$
  [-,-]_\ast
  \;\colon\;
  Ho(\mathcal{C}^{\ast/})^\op
  \times
  Ho(\mathcal{C}^{\ast/})
  \longrightarrow
  Set^{\ast/}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

If $\mathcal{C}$ is a [[monoidal model category]] with cofibrant [[tensor unit]], then the pointed model structure on  $\mathcal{C}^{\ast/}$ (Prop. \ref{ModelStructureOnSliceCategory}) is also a [[monoidal model category]], and the [[smash product]]$\dashv$[[mapping space]] adjunction of prop. \ref{SmashProductLeftAdjointToPointedMappingSpace} is a [[Quillen adjunction]]

$$
  \big(
    X \wedge (-)
    \;\dashv\;
    (-)^X
  \big)
  \;\;\colon\;\;
  \mathcal{C}^{\ast/}
  \leftrightarrow
  \mathcal{C}^{\ast/}
  \,.
$$

=--

## References

Textbook accounts:

* {#Hovey99} [[Mark Hovey]], Prop. 1.1.8 in: _[[Model Categories]]_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

[[!redirects model category of pointed objects]]
[[!redirects model categories of pointed objects]]

