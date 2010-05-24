#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A *computad* is a formal device (due to [[Ross Street]], 1976) for describing "generators" of [[higher category theory|higher categories]], and in particular for $n$-[[n-category|categories]].  They generalize [[directed graph]]s, which describe generators of ordinary (1-)[[categories]].  In a sense, $n$-computads are the "most general" structure from which one can generate a free $n$-category; they allow the free adjoining of $k$-cells whose [[source]] and [[target]] are arbitrary [[composites]] of previously adjoined $(k-1)$-cells.

Originally the $n$-categories under consideration were [[strict n-category|strict]], but more recently the concept of $n$-computad has been expanded to take into account weak $n$-categories and other higher-categorical structures.  The notion is tied to [[algebraic definition of higher category|algebraic]] senses of higher categories, but computads can also be used as the input for [[geometric definition of higher category|geometric]] senses as well, and may aid in a comparison between the two approaches.

Computads are also called *polygraphs*, following Burroni; this term is especially used in parts of the literature related to [[rewriting]] theory.

## Definition ##

Each type of higher-categorical structure comes with its own notion of computad.  Thus there are computads for strict $n$-categories, computads for weak $n$-categories, computads for [[double categories]], and so on.  Here we will define computads relative to an arbitrary [[globular operad]] $P$.  This reproduces the original strict situation when $P$ is the terminal globular operad, whose algebras are [[strict omega-categories]], but it also applies to operads $P$ whose algebras are [[Batinin weak omega-categories]].  The generalization to the weak case is originally due to Batanin; the following simpler reformulation of it is due to Richard Garner.

Let $P$ be a [[globular operad]] and let $P Alg$ denote the category of $P$-algebras and strict morphisms.  Thus if $P$ is terminal, then $P Alg = Str \omega Cat$.  We denote by $U_P$ the forgetful functor $P Alg \to GSet$ and by $F_P$ its left adjoint, where $GSet$ denotes the category of [[globular sets]].  Let $2_n$ denote the $n$-[[globe]] and $\partial_n$ its boundary (which is the pushout of two $(n-1)$-globes along their boundaries).  These are globular sets and thus they generate free $P$-algebras $F_P 2_n$ and $F_P \partial_n$.

We now define, recursively in $n$, the category $n Cptd_P$ of **$n$-computads** relative to $P$, together with an adjunction
$$ n Cptd_P \underoverset{U_n}{F_n}{\leftrightarrows} P Alg .$$

* When $n=-1$, the category $(-1) Cptd_P$ is the [[terminal category]] $*$, $U_{-1}\colon P Alg \to *$ is the unique functor, and $F_{-1}$ is its left adjoint, which picks out the initial $P$-algebra.  Thus there is exactly one $(-1)$-computad, and the free $P$-algebra on it is the initial one.

* If $n\ge 0$, an **n-computad** consists of an $(n-1)$-computad $C$, a set $X$, and a function
  $$x\colon X\to P Alg(F_P \partial_n, F_{n-1} C) = GSet(\partial_n, U_P F_{n-1} C).$$
  We call $X$ the set of **n-cells**.  Note that $x$ simply equips each $n$-cell with a pair of parallel $(n-1)$-cells in $F_{n-1} C$.  In fancy language, the category $n Cptd_P$ is the [[comma category]] $Set / B_n$, where $B_n = P Alg(F_P \partial_n, F_{n-1} -)$.

* The functor $U_n\colon P Alg \to n Cptd_P$ sends a $P$-algebra $A$ to the $n$-computad defined by the $(n-1)$-computad $U_{n-1} A$ together with $X$ and $x$ defined by the following pullback square in [[Set]]:
  $$\array{X & \overset{}{\to} & P Alg(F_P 2_n, A)\\
  ^x \downarrow && \downarrow\\
  P Alg(F_P \partial_n, F_{n-1} U_{n-1} A) & \underset{}{\to} & P Alg(F_P \partial_n, A)}$$
  Here the bottom map is induced by the counit of the adjunction $F_{n-1}\dashv U_{n-1}$, while the right-hand map is induced by the inclusion $\partial_n \hookrightarrow 2_n$.

* The left adjoint $F_n$ of $U_n$ is defined by taking an $n$-computad $D = (C,X,x)$ to the following pushout in $P Alg$:
  $$\array{X\cdot F_P \partial_n & \overset{\overline{x}}{\to} & F_{n-1} C\\
  \downarrow && \downarrow\\
  X \cdot F_P 2_n & \underset{}{\to} & F_n D}$$
  Here $\cdot$ denotes a [[copower]] by a set, the top map $\overline{x}$ is the [[adjunct]] of $x$, and the left-hand map is again induced by the inclusion $\partial_n \hookrightarrow 2_n$.  Adjointness is easy to verify using the universal properties of pullbacks and pushouts.

Finally, the category $\omega Cptd_P$ of $\omega$-computads is the [[limit]] of the diagram
$$ \dots \to 2 Cptd_P \to 1 Cptd_P \to 0 Cptd_P \to (-1) Cptd_P $$
consisting of the functors $n Cptd_P \to (n-1)Cptd_P$ taking $(C,X,x)$ to $C$.  The functors $U_n$ form a [[cone]] over this diagram and thus induce a functor $U_\omega\colon P Alg \to \omega Cptd_P$, which is easily seen to have a left adjoint which takes an object $(C_n)$ of $\omega Cptd_P$ to the [[colimit]]
$$ F_{-1} C_{-1} \to F_0 C_0 \to F_1 C_1 \to F_2 C_2 \to \dots.$$


## Examples ##

* As in the definition, there is exactly one $(-1)$-computad, and the free $P$-algebra on it is the initial one.

* A 0-computad is a set.

* The free [[0-category]] on a 0-computad is just itself.

* A 1-computad is just a [[directed graph]].

* The free 1-category on a 1-computad is the usual free category on a graph.  That is, its objects are the vertices of the graph and its morphisms are finite composable strings of edges in the graph.

* A 2-computad is given by a directed graph together with a set $C_2$ of 2-cells, each equipped with a source and a target which are composable strings of edges in the graph.  For example, if the directed graph is a square
  $$\array{\bullet & \overset{f}{\to} & \bullet \\
  ^h\downarrow && \downarrow^k\\
  \bullet& \underset{g}{\to} & \bullet}$$
  then the free category it generates is the free noncommutative square, having two diagonals $k f$ and $g h$.  We can then make a 2-computad by adding one 2-cell $\alpha$ with source $k f$ and target $g h$.  The free 2-category on this 2-computad can then be drawn pictorially as
  $$\array{\bullet & \overset{f}{\to} & \bullet\\
  ^h\downarrow & \swarrow_\alpha & \downarrow^k\\
  \bullet & \underset{g}{\to} & \bullet}$$

* Any $n$-[[globular set]] can be considered as an $n$-computad where for each $n$, the functions $s, t: C_n \rightrightarrows F_{n-1}(\mathcal{C})_{n-1}$ land inside $C_{n-1}$.  The free $n$-category on this $n$-computad will then agree with the free $n$-category on the $n$-globular set we started with.

* Every [[oriental]] can be presented by a computad.


## Computads, presheaves and opetopes ##

The category of computads is "almost" a [[presheaf]] category.  At first glance, it may look as though it should *be* a presheaf category, say $Set^{Ctp^{op}}$ where $Ctp$ is the category of "computopes."  A "computope" is, intuitively, one possible "[[geometric shapes for higher structures|shape]]" for an $n$-cell in an $n$-category.  For example, every "[[globe]]" is a computope, as is every [[simplex]]/[[oriental]], every [[cube]], and so on.  It may feel at first as though a computad should be specified by giving a set of cells of each "shape" (i.e. for each computope) related by "face maps," generalizing [[globular set]]s, [[simplicial set]]s, [[cubical set]]s, and so on.

However, the presence of identities in the notion of free $n$-category prevents this from quite working, for sort of the same reason that [[strict n-categories]] are insufficient for $n\gt 2$.  For instance, there is a 2-computad with one 0-cell $x$, *no* 1-cells, and two 2-cells $\alpha$ and $\beta$.  The source and target of $\alpha$ and $\beta$ must then both be the identity 1-cell $id_x$ of $x$.  Now in the free 2-category generated by this 2-computad, we have $\beta\alpha = \alpha\beta$, by the [[Eckmann-Hilton argument]].  If we define a 3-computad on top of this 2-computad with a 3-cell $\mu$ whose source (say) is $\beta\alpha = \alpha\beta$, then there can be no "face" maps from the computope-shape of $\mu$ to the computope-shape of $\beta$ and $\alpha$, since there is no way to distinguish $\alpha$ from $\beta$ (i.e. neither one is the "first" or the "second").

This argument only kicks in for $n\ge 3$, so the categories of 0-computads, 1-computads, and 2-computads are presheaf categories.  (For 0 and 1, this is obvious.)

If we restrict the notion slightly, however, we can obtain presheaf categories.  For instance, if we consider only "many-to-one" computads in which the target of each $n$-cell consists of exactly one $(n-1)$-cell (rather than a free composite of such), we obtain a presheaf category, which is in fact equivalent to the category of [[opetopic set]]s.

+--{: .query}
[[Mike Shulman]]: Do the non-strict versions of computads get around this problem?

Daniel Sch ppi: Batanin has a paper on this:
[Computads and slices of operads](http://arxiv.org/abs/math.CA/0209035)

If you take any finitary monad $A$ on the category of globular sets, you can use the truncation functor to get monads $A_n$ on the category of $n$-globular sets, and then you can inductively define the notion of an $A$-computad. If you take $A=T$ the free strict $\omega$-category monad, then this notion agrees with Streets definition of an ordinary computad. Batanin gives a condition which ensures that the category of $n$-computads of $A$ is a presheaf category, in terms of slices of the monad $A$.

The $k$-slice of $A$ is defined as follows: the full subcategory of $A_n-\mathbf{Alg}$ consisting of those algebras whose underlying globular set is $(n-1)$-terminal is monadic over the category of sets, and the $k$-slice of $A$ is given by this monad. In the above paper, Theorem 5.2 Batanin shows that the category of $n$-computads of a Batanin-operad $A$ is a presheaf category if the $k$-slices of $A$ are strongly regular theories for $0\leq k \leq n-1$. This applies in particular to the case where $A$ is the operad for Batanin weak $\omega$-categories.
=--

## Computads as cofibrant resolutions ##

With respect to the [[canonical model structure]] on [[strict omega-category|strict  -categories]]

* Yves Lafont, Francois M&#233;tayer, Krzysztof Worytkiewicz, _A folk model structure on omega-cat_ ([arXiv](http://arxiv.org/abs/0712.0617))

the $\omega$-categories that are (freely generated by) computads are precisely the cofibrant objects

This is discussed in 

* F. M&#233;tayer, _Cofibrant complexes are free_ ([arXiv](http://arxiv.org/abs/math.CT/0701746))

* F. M&#233;tayer, _Resolutions by polygraphs_ ([tac](http://www.tac.mta.ca/tac/volumes/11/7/11-07.pdf))

This says in particular that _every_ [[strict  -category]] is equivalent as an $\omega$-category to one that is a computad. (Notice that these articles say "polygraph" for "computad", following Burroni).

The cofibrant resolution $(-)_{cof} \to Id : \omega Cat \to \omega Cat$ given by M&#233;tayer in these articles is the one counit of the [[adjunction]] $\omega Comp  \to \omega Cat$. 


> We had some blog discussion about this at [Freely generated omega-categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html).

## References

* [[Albert Burroni]], _Higher dimensional word problems with applications to equational logic_ ([pdf](http://people.math.jussieu.fr/~burroni/mapage/highwordpb.pdf))
