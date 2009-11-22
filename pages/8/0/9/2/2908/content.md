An __algebraic category__, according to one well-established definition, is a [[category]] $A$ equipped with a [[monadic adjunction]] from [[Set]].


## Details

In more detail, let $A$ be a [[locally small category]], let $F\: Set \to A$ and $U\: A \to Set$ be [[functors]], and let $\epsilon\: F \circ U \to id_A$ be a [[natural transformation]].  Then $F, U, \epsilon$ give $A$ the structure of an __algebraic category__ if the following conditions hold:

*  $F \vdash U$ are [[adjoint functors]] with counit $\epsilon$.  More explicitly: for each $h\colon F(x) \to y$ in $A$, there is a unique $g\colon x \to U(y)$ in $Set$ such that $\epsilon(y) \circ F(g) = h$.
*  $U \circ \epsilon$ is an [[equivalence of categories]] from $C$ to the [[Eilenberg–Moore category]] of $U \circ F$.  More explicitly: ...


## Examples

The typical categories studied in [[algebra]], such as [[Grp]], [[Ring]], etc, are all algebraic categories.  Specifically, the [[right adjoint]] is the [[forgetful functor]] from algebras to sets, and the [[left adjoint]] maps each set to the [[free object|free]] algebra on that set.  Their composite (a monad on $Set$) may be thought of as mapping a set $A$ to the set of words with alphabet taken from $A$ and the connections between letters taken from the appropriate algebraic operations, with two words identified if they can be proved equal by the appropriate algebraic axioms.

There are more examples than the ones from algebra; the best known of these is the category of [[compact Hausdorff spaces]], which corresponds to the [[ultrafilter]] monad.  (This result relies on the [[ultrafilter principle]], regardless of whether one interprets 'space' here as referring to [[topological spaces]] or [[locales]].)