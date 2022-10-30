
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A *computad* is a formal device (due to [[Ross Street]], 1976) for describing "generators" of [[higher category theory|higher categories]], and in particular for $n$-[[n-category|categories]].  They generalize [[quivers]] ([[directed graphs]]), which describe generators of ordinary (1-)[[categories]].  In a sense, $n$-computads are the "most general" structure from which one can generate a free $n$-category; they allow the free adjoining of $k$-cells whose [[source]] and [[target]] are arbitrary [[composites]] of previously adjoined $(k-1)$-cells.

Originally the $n$-categories under consideration were [[strict n-category|strict]], but more recently the concept of $n$-computad has been expanded to take into account weak $n$-categories and other higher-categorical structures.  The notion is tied to [[algebraic definition of higher category|algebraic]] senses of higher categories, but computads can also be used as the input for [[geometric definition of higher category|geometric]] senses as well, and may aid in a comparison between the two approaches.

Computads are also called [[polygraphs]], following [[Burroni]]; this term is especially used in parts of the literature related to [[rewriting]] theory.

## Definition ##

Each type of higher-categorical structure comes with its own notion of computad.  Thus there are computads for strict $n$-categories, computads for weak $n$-categories, computads for [[double categories]], and so on.  Here we will define computads relative to an arbitrary [[globular operad]] $P$.  This reproduces the original strict situation when $P$ is the terminal globular operad, whose algebras are [[strict ∞-categories]], but it also applies to operads $P$ whose algebras are [[Batanin weak ∞-categories]].  The generalization to the weak case is originally due to Batanin; the following simpler reformulation of it is due to Richard Garner.

Let $P$ be a [[globular operad]] and let $P Alg$ denote the category of $P$-algebras and strict morphisms.  Thus if $P$ is terminal, then $P Alg = Str \omega Cat$.  We denote by $U_P$ the forgetful functor $P Alg \to GSet$ and by $F_P$ its left adjoint, where $GSet$ denotes the category of [[globular sets]].  Let $2_n$ denote the $n$-[[globe]] and $\partial_n$ its boundary (which is the pushout of two $(n-1)$-globes along their boundaries).  These are globular sets and thus they generate free $P$-algebras $F_P 2_n$ and $F_P \partial_n$.

We now define, recursively in $n$, the category $n Cptd_P$ of **$n$-computads** relative to $P$, together with an adjunction
$$ n Cptd_P \underoverset{U_n}{F_n}{\rightleftarrows} P Alg .$$

* When $n=0$, the category $(-1) Cptd_P$ is [[Set]], $U_0\colon P Alg \to Set$ picks out the set of objects, and $F_0$ is its left adjoint, which constructs the free $P$-algebra on a set (considered as a globular set concentrated in degree 0).

* If $n\gt 0$, an **n-computad** consists of an $(n-1)$-computad $C$, a set $X$, and a function
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

For simplicity, let $P$ be the terminal globular operad, such that $P$-algebras are [[strict ∞-categories]].

* As in the definition, a 0-computad is just a set, and the free [[0-category]] on a 0-computad is just itself, considered as a discrete $\omega$-category.

* A 1-computad consists of 0-computad $C$ (i.e. a set) together with another set $X$ and a function $X\to GSet(\partial_1, U_P F_0 C)$.  Now $\partial_1$ is just a pair of objects, so this means that each element of $X$ is equipped with a pair of elements of $C$, which we call its [[source]] and [[target]].  Thus a 1-computad is just a [[quiver]].

* The free 1-category on a 1-computad is the usual free category on a quiver.  That is, its objects are the vertices of the graph and its morphisms are finite composable strings of edges in the quiver.

* A 2-computad is given by a quiver together with a set $C_2$ of 2-cells, each equipped with a source and a target which are composable strings of edges in the graph.  For example, if the given quiver is a square
  $$\array{\bullet & \overset{f}{\to} & \bullet \\
  ^h\downarrow && \downarrow^k\\
  \bullet& \underset{g}{\to} & \bullet}$$
  then the free category it generates is the free noncommutative square, having two diagonals $k f$ and $g h$.  We can then make a 2-computad by adding one 2-cell $\alpha$ with source $k f$ and target $g h$.  The free 2-category on this 2-computad can then be drawn pictorially as
  $$\array{\bullet & \overset{f}{\to} & \bullet\\
  ^h\downarrow & \swarrow_\alpha & \downarrow^k\\
  \bullet & \underset{g}{\to} & \bullet}$$

* Any $n$-[[globular set]] can be considered as an $n$-computad where for each $n$, the functions $s, t: C_n \rightrightarrows F_{n-1}(\mathcal{C})_{n-1}$ land inside $C_{n-1}$.  The free $n$-category on this $n$-computad will then agree with the free $n$-category on the $n$-globular set we started with.


* Every [[oriental]] can be presented by a computad, as can every [[opetope]], [[cube]], as can most other [[geometric shapes for higher structures]].


## Computads, presheaves and opetopes ##

The category of computads relative to a globular operad $P$ is sometimes a [[presheaf category]], and when it isn't, it "almost is."  At first glance, it may look as though it should always be a presheaf category, say $Set^{Ctp^{op}}$ where $Ctp$ is the category of "computopes."  A "computope" is, intuitively, one possible "[[geometric shapes for higher structures|shape]]" for an $n$-cell in an $n$-category (i.e. a $P$-algebra).  For example, every "[[globe]]" is a computope, as is every [[simplex]]/[[oriental]], every [[cube]], and so on.  It may feel at first as though a computad should be specified by giving a set of cells of each "shape" (i.e. for each computope) related by "face maps," generalizing [[globular set]]s, [[simplicial set]]s, [[cubical set]]s, and so on.

However, when $P$ is the terminal globular operad whose algebras are *strict* $\omega$-categories, the presence of identities in the notion of free $n$-category prevents this from quite working, for sort of the same reason that [[strict n-categories]] are insufficient for $n\gt 2$.  For instance, there is a 2-computad with one 0-cell $x$, *no* 1-cells, and two 2-cells $\alpha$ and $\beta$.  The source and target of $\alpha$ and $\beta$ must then both be the identity 1-cell $id_x$ of $x$.  Now in the free 2-category generated by this 2-computad, we have $\beta\alpha = \alpha\beta$, by the [[Eckmann-Hilton argument]].  If we define a 3-computad on top of this 2-computad with a 3-cell $\mu$ whose source (say) is $\beta\alpha = \alpha\beta$, then there can be no "face" maps from the computope-shape of $\mu$ to the computope-shape of $\beta$ and $\alpha$, since there is no way to distinguish $\alpha$ from $\beta$ (i.e. neither one is the "first" or the "second").

This argument only kicks in for $n\ge 3$, so the categories of 0-computads, 1-computads, and 2-computads are presheaf categories.  Moreover, the problem can also be avoided if $P$ is "suitably weak."  To define what this means, one considers the "slices" of the operad $P$.  By truncation, any such $P$ induces a monad $P_k$ on the category of $k$-globular sets.  Now the full subcategory of $P_n Alg$ on the objects whose underlying globular set is $(n-1)$-terminal (i.e. terminal in degrees $\lt n$) is [[monadic functor|monadic]] over the category of sets; the resulting monad on [[Set]] is called the **$k$-slice** of $P$.  In Theorem 5.2 of [Computads and slices of operads](http://arxiv.org/abs/math.CA/0209035), Batanin shows that the category of $n$-computads of a Batanin-operad $P$ is a presheaf category if the $k$-slices of $P$ are [[strongly regular theory|strongly regular theories]] for all $0\leq k \leq n-1$.  This applies in particular to the case where $P$ is an operad for Batanin weak $\omega$-categories.

On the other hand, even in the strict case we can obtain presheaf categories of suitably restricted computads.  For instance, if we consider only "many-to-one" computads in which the target of each $n$-cell consists of exactly one $(n-1)$-cell (rather than a free composite of such), we obtain a presheaf category, which is in fact equivalent to the category of [[opetopic set]]s.

## Monadicity

The adjunction $n Cptd \rightleftarrows n Cat$ should be [[monadic adjunction|monadic]], at least in good cases.  However, it is not clear to the author of this page whether or where a correct proof of this fact appears in the literature for any value of $n\gt 1$.

## Computads as cofibrant resolutions ##

Quite generally, computads can be used to describe [[cofibrant object|cofibrant replacements]].  Specifically, the $\omega$-categories freely generated by computads are precisely the cofibrant objects in the [[canonical model structure]] on [[strict ∞-categories]].  This is discussed in 

* F. M&#233;tayer, _Cofibrant complexes are free_ ([arXiv](http://arxiv.org/abs/math.CT/0701746))

* F. M&#233;tayer, _Resolutions by polygraphs_ ([tac](http://www.tac.mta.ca/tac/volumes/11/7/11-07.pdf))

The cofibrant resolution $(-)_{cof} \to Id : \omega Cat \to \omega Cat$ given by M&#233;tayer in these articles is the one counit of the [[adjunction]] $\omega Cptd  \to \omega Cat$.  In particular, this implies that _every_ [[strict ∞-category]] is equivalent as an $\omega$-category to one that is freely generated by a computad.  (Notice that these articles say "polygraph" for "computad", following Burroni).

It is to be expected that similar results are true for Batanin weak $\omega$-categories, defined as algebras for some other "contractible" globular operad $P$.

Moreover, for any globular operad $P$, one can show that the "cofibrant replacement" obtained as above from the adjunction $\omega Cptd_P \rightleftarrows P Alg$ is the same as the "canonical" cofibrant replacement [[comonad]] obtained from the [[algebraic weak factorization system]] on $P Alg$ generated by the boundary inclusions $F_P \partial_n \to F_P 2_n$.  This is proven in

* [[Richard Garner]], [Homomorphisms of higher categories](http://arxiv.org/abs/0810.4450).

In particular, the [[Kleisli category]] of this comonad is a good candidate for the category of *weak functors* between Batanin weak $\omega$-categories.

## Related concepts

* [[syzygy]]


## References

2-computads were originally defined by Ross Street in the paper

* [[Ross Street]], _Limits indexed by category-valued 2-functors_.

The goal there was to describe which 2-categories are "finitely presented" (the presentation being given by a 2-computad) in order to describe the correct notion of "finite [[2-limit]]".

I don't know the first use of "$n$-computads," but [[Michael Makkai]] has studied them as a way to define [[opetopic sets]], and shown that they are "almost" but not quite a presheaf category:

* Makkai, Harnik, and Zawadowski, _Multitopic sets are the same as many-to-one computads_, [link](http://www.math.mcgill.ca/makkai/m_1_comp/).

* Makkai, _The word problem for computads_, [link](http://www.math.mcgill.ca/makkai/computad.zip).

* Makkai, _All Vedic Maths Tricks for computads_, [link](http://mental-maths-trick.blogspot.com/2011/10/do-super-quick-maths-calculation-using.html).

Computads were studied by [[Burroni]] under the name "polygraph" in the framework of [[rewriting]]:

* [[Albert Burroni]], _Higher dimensional word problems with applications to equational logic_ ([pdf](http://people.math.jussieu.fr/~burroni/mapage/highwordpb.pdf))

The following more recent papers are referred to above:

* [[Michael Batanin]], [Computads and slices of operads](http://arxiv.org/abs/math.CA/0209035)

* [[Richard Garner]], [Homomorphisms of higher categories](http://arxiv.org/abs/0810.4450).

One should beware that there are some erroneous claims in some of Batanin's papers; in particular the claim that computads relative to a globular operad are *always* a presheaf category.  This was explicitly shown to be false in

* Michael Makkai and Marek Zawadowski, _The category of 3-computads is not cartesian closed_, [MR](http://www.ams.org/mathscinet-getitem?mr=2440266).

* Eugenia Cheng, [A direct proof that the category of 3-computads is not cartesian closed](http://arxiv.org/abs/1209.0414)

Finally, we had some blog discussion about this at 

* [Freely generated &#969;-categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html).

[[!redirects computads]]
[[!redirects n-computad]]
[[!redirects n-computads]]
[[!redirects ∞-computad]]
[[!redirects ∞-computads]]
[[!redirects 2-computad]]
[[!redirects 2-computads]]
[[!redirects polygraph]]
[[!redirects polygraphs]]
