
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

But the [[cofibrant objects]] in $\mathcal{C}^{\ast/}$ are those for which the basepoint inclusion is a [[cofibration]] in $X$.

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


\begin{prop}\label{InducedQuilleAdjunctionsOnModelCategoriesOfPointedObjects}
**(induced [[Quillen adjunction]] on [[model categories of pointed objects]])** \linebreak
Given a [[Quillen adjunction]] between [[model categories]]
$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}
  \,,
$$
there is induced a [[Quillen adjunction]] between the corresponding [[model categories of pointed objects]]
$$
  \mathcal{D}^{\ast\!/}
    \underoverset
      {\underset{R^{\ast\!/}}{\longrightarrow}}
      {\overset{L^{\ast\!/}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{\ast\!/}
  \,,
$$
where 

* the [[right adjoint]] acts directly as $R$ on the triangular [[commuting diagrams]] in $\mathcal{C}$ that define the morphisms in $\mathcal{C}^{\ast\!/}$;

* the [[left adjoint]] is the [[composition|composite]] of the corresponding direct application of $L$ followed by [[pushout]] along the [[adjunction counit]] $L(\ast) \simeq L \circ R(\ast) \xrightarrow{ \;\epsilon_\ast \; } \ast$ (using that $R(\ast) \simeq \ast$ since [[right adjoints preserve limits]] and hence [[terminal objects]]):

  $$
    L^{\ast\!/}
    \;\colon\;
    \mathcal{C}^{\ast\!/}
    \xrightarrow{ \;\; L  \;\; }
    \mathcal{D}^{L(\ast)\!/}
    \;\simeq\;
    \mathcal{D}^{L\circ R(\ast)\!/}
    \xrightarrow{ \;\; (-) \sqcup \epsilon_\ast \;\; }
    \mathcal{D}^{\ast\!/}
    \,.
  $$

\end{prop}
\begin{proof}
  It is fairly straightforward to check this directly (e.g. [Hovey 1999, Prop. 1.3.5](#Hovey99)), but it is also a special case of [this general prop.](slice+model+structure#SlicedQuillenAdjunction) about [[slice model categories]] --- to make this explicit, notice that passing to [[opposite categories]] with their [[opposite model structures]] turns the original Quillen adjunction into the [[opposite Quillen adjunction]]:

$$
  \mathcal{D}^{op}
    \underoverset
      {\underset{L^{op}}{\longrightarrow}}
      {\overset{R^{op}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{op}
  \,.
$$

Now the passage to [[pointed objects]] corresponds to [[slice category|slicing]] (instead of [[coslice category|co-slicing]]), since

\[
  \label{PointedObjectsIsOppositeOfCopointedObjectsInOpposite}
  \mathcal{C}^{\ast\!/}
  \;\;
  \simeq
  \big(
    \mathcal{C}^{op}_{/\ast}
  \big)^{op}
  \,,
  \;\;\;\;\;\;\;
  \text{similarly}
  \;\;\;
  \mathcal{D}^{\ast\!/}
  \;\;
  \simeq
  \big(
    \mathcal{D}^{op}_{/R(\ast)}
  \big)^{op}
  \,,
\]

whence item (1) in [that Prop.](slice+model+structure#SlicedQuillenAdjunction) says that there is a Quillen adjunction of the form

$$
  \mathcal{D}^{op}_{/R(\ast)}
    \underoverset
      {\underset{L^{op}_{/\ast}}{\longrightarrow}}
      {\overset{R^{op}_{/\ast}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{op}_{/\ast}
  \,,
$$

hence with [[opposite Quillen adjunction]] of the required form

$$
  \mathcal{D}^{\ast\!/}  
  \simeq
  \big(\mathcal{D}^{op}_{/R(\ast)}\big)^{op}
    \underoverset
      {\underset{ 
        R^{\ast\!/} \,\coloneqq\, \big( R^{op}_{/\ast} \big)^{op}
      }{\longrightarrow}}
      {\overset{
        L^{\ast\!/} \,\coloneqq\, \big( L^{op}_{/\ast} \big)^{op}
      }{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \big(\mathcal{C}^{op}_{/\ast}\big)^{op}
  \simeq
  \mathcal{C}^{\ast\!/}
  \,,
$$


with $R^{op}$ acting directly as $R$ on underlying diagrams, and with $L^{op}$ acting as the composite of $L$ following by [[pullback]] -- in $\mathcal{C}^{op}$ -- along the [[adjunction unit]] of $(R^{op} \dashv L^{op})$. Since the component morphism of the [[adjunction unit|unit]] of the [[opposite adjunction]] $(R^{op} \dashv L^{op})$ is that of the adjunction unit of $(L \dashv R)$, and since [[pullback]] in an [[opposite category]] is [[pushout]] in the original category, this implies the claim. 
\end{proof}


## References

Textbook accounts:

* {#Hovey99} [[Mark Hovey]], Prop. 1.1.8 in: _[[Model Categories]]_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

[[!redirects model category of pointed objects]]
[[!redirects model categories of pointed objects]]

