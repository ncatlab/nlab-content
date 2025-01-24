+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

An **exponentiable functor**, also called a **Conduch&#233; functor** or **Conduch&#233; fibration**, is a [[functor]] which is an [[exponentiable morphism]] in [[Cat]].  (In accordance with [[Stigler's law of eponymy]], the notion was actually defined in [Giraud 64](#Giraud64) before [Conduch&#233; 72](#Conduche72).)  This turns out to be equivalent to a certain "factorization lifting" property which includes both [[Grothendieck fibrations]] and opfibrations.

So, roughly speaking, a functor $p\colon E\to B$ is a **strict Conduch&#233; functor** if given any morphism $\alpha$ in $E$, and any way of factoring its image in $B$, we can lift that factorization back up to a factorization of $\alpha$, in a way that is unique up to isomorphism.   There is also a weak version of this idea.

## Failure of local cartesian closedness in Cat

As is evident from the fact that such functors have a name, not every functor is exponentiable in [[Cat]].  In particular, although $Cat$ is [[cartesian closed category|cartesian closed]], it is not [[locally cartesian closed category|locally cartesian closed]].

It is easy to write down examples of [[colimits]] in $Cat$ that are not preserved by [[pullback]] (as they would be if pullback had a [[right adjoint]]).  For instance, let $\mathbf{2}$ denote the [[walking arrow]], i.e. the [[ordinal]] $2$ regarded as a [[category]], $1$ the [[terminal category]], and $\mathbf{3} = \mathbf{2} \sqcup_1 \mathbf{2}$ the ordinal $3 = (a \to b \to c)$ regarded as a category.  Then the [[pushout]] square
$$\array{1 & \overset{}{\to} & \mathbf{2}\\
  \downarrow && \downarrow\\
  \mathbf{2}& \underset{}{\to} & \mathbf{3}}$$
in the [[slice category]] $Cat/\mathbf{3}$ pulls back along the inclusion $\mathbf{2}\to \mathbf{3}$ of the arrow $(a\to c)$ to the square
$$\array{0 & \overset{}{\to} & 1\\
  \downarrow && \downarrow\\
  1& \underset{}{\to} & \mathbf{2}}$$
which is certainly not a pushout.

One way to describe the problem is that the pushout has "created new morphisms" that didn't exist before.  But another way to describe the problem is that the inclusion $\mathbf{2}\to\mathbf{3}$ fails to notice that the morphism $(a\to c)$ acquires a new factorization in $\mathbf{3}$ which it didn't have in $\mathbf{2}$.  Conduch&#233;'s observation was that this latter failure is really the only problem that can prevent a functor from being exponentiable.

## Definition

A [[functor]] $p\colon E\to B$ is a **strict Conduch&#233; functor**, if for any [[morphism]] $\alpha\colon a\to b$ in $E$ and any factorization $p a \overset{\beta}{\to} c \overset{\gamma}{\to} p b$ of $p \alpha$ in $B$, we have:

1. there exists a factorization $a \overset{\tilde{\beta}}{\to} d \overset{\tilde{\gamma}}{\to} b$ of $\alpha$ in $E$ such that $p \tilde{\beta} = \beta$ and $p \tilde{\gamma} = \gamma$, and

1. any two such factorizations in $E$ are connected by a [[zigzag]] of commuting morphisms which map to $id_c$ in $B$.

(Here, 'commuting morphism' means a morphism $d \to d'$ in $E$ such that the pair of triangles in 

$$\array{
 & & d & \stackrel{\tilde{\gamma}}{\to} & b \\
 & ^\mathllap{\tilde{\beta}} \nearrow & \downarrow & \nearrow^\mathrlap{\tilde{\gamma}'} & \\
a & \underset{\tilde{\beta}'}{\to} & d' & & 
}$$

[[commuting diagram|commute]].) 

The theorem is then that the following are equivalent:

* $p$ is a strict Conduch&#233; functor.
* $p$ is [[exponentiable morphism|exponentiable]] in the 1-category $Cat$.
* $p$ is exponentiable in the [[strict 2-category]] $Cat$.

By "exponentiable in the strict 2-category $Cat$" we mean that pullback along $p$ has a strict right 2-adjoint (i.e.&#160;a $Cat$-enriched right adjoint).  Of course, this implies ordinary exponentiability in the 1-category $Cat$, while the converse follows via an argument involving [[cotensors]] with $\mathbf{2}$ in $Cat$.

For exponentiability in the weak [[2-category]] $Cat$, in the sense of pullback having a weak/pseudo 2-adjoint, we can simply weaken the condition.  We say that $p\colon E\to B$ is a **(weak) Conduch&#233; functor** if for any morphism $\alpha\colon a\to b$ in $E$ and any factorization $p a \overset{\beta}{\to} c \overset{\gamma}{\to} p b$ of $p \alpha$ in $B$, we have:

1. there exists a factorization $a \overset{\tilde{\beta}}{\to} d \overset{\tilde{\gamma}}{\to} b$ of $\alpha$ in $E$, and an isomorphism $p d \cong c$, such that modulo this isomorphism $p \tilde{\beta} = \beta$ and $p \tilde{\gamma} = \gamma$, and

1. any two such factorizations in $E$ are connected by a zigzag of commuting morphisms which map to isomorphisms in $B$.

A functor can then be shown to be a weak Conduch&#233; functor if and only if it is exponentiable in the weak sense in $Cat$.

A Conduch&#233; functor is **discrete** if each factorisation is unique (equivalently, if it reflects identities). Discrete Conduch&#233; functors generalise [[discrete fibrations]] and [[discrete opfibrations]].

Discrete Conduch&#233; functors are said to satisfy the **unique lifting of factorisations**. Discrete Conduch&#233; functors are therefore sometimes called **ULF** functors.

### Properties

* ULF functors form the right class of an [[orthogonal factorisation system]] on [[Cat]].

## Conduch&#233; functors and 2-functors to Prof

The Conduch&#233; criterion can be reformulated in a more conceptual way by analogy with [[Grothendieck fibrations]].  We first observe that to give a functor $p\colon E\to B$ is essentially the same as to give a [[normal lax functor|normal]] [[lax 2-functor]] $B\to Prof$ from $B$ to [[Prof]], the 2-category of [[profunctors]].  The latter is also known as a [[displayed category]]; see there for more on this correspondence.

Specifically, given a functor $p$, we define $B\to Prof$ as follows.  Each object $b\in B$ is sent to the fiber category $p^{-1}(b)$ of objects lying over $b$ and morphism lying over $1_b$.  And each morphism $f\colon a\to b$ in $B$ to the profunctor $H_f\colon p^{-1}(a) &#8696; p^{-1}(b)$ for which $H_f(x,y)$ is the set of arrows $x\to y$ in $E$ lying over $f$.  The lax structure maps $H_f \otimes H_g \to H_{g f}$ are given by composition in $E$.  The converse construction of a functor $p$ from a normal lax 2-functor into $Prof$ is an evident generalization of the [[Grothendieck construction]].  Now we can say that:

* $p$ is a fibration iff the corresponding functor $B\to Prof$ factors through a pseudo 2-functor landing in $Cat^{op}$, via the contravariant inclusion $Cat^{op}\to Prof$.
* Similarly, $p$ is an opfibration iff $B\to Prof$ factors through a pseudo 2-functor landing in $Cat$ via the covariant inclusion $Cat \to Prof$.
* The functor $B\to Prof$ factors through a *lax* 2-functor landing in $Cat^{op}$ iff $p$ admits all "weakly cartesian" liftings, and dually.
* Finally, $p$ is a (strict) Conduch&#233; functor iff the functor $B\to Prof$ is itself a pseudo 2-functor (though it may not land in $Cat$ or $Cat^{op}$).  This can be seen by comparing the definition of the tensor product of profunctors with the explicit description in terms of unique factorizations above.

Thus Conduch&#233; functors into $B$ correspond to pseudofunctors from $B$, regarded as a locally discrete bicategory, to the bicategory $Prof$.  However, morphisms between Conduch&#233; functors over $B$ do not correspond to pseudonatural transformations between such pseudofunctors.  To get the correct transformations, we must instead regard $B$ as a vertically discrete [[double category]], and $Prof$ as a pseudo double category with profunctors horizontally and functors vertically; then pseudo double functors $B\to Prof$ again correspond to Conduch&#233; functors into $B$, and *vertical* double transformations between them correspond to functors between Conduch&#233; functors into $B$.

More generally, the slice category $Cat/B$ is equivalent to the hom-category $Dbl_{normal,lax}(B,Prof)$, with its full subcategory consisting of Conduch&#233; functors corresponding to the pseudo double functors.

## Higher-categorical versions

Non-strict Conduch&#233; functors and [[Street fibrations]] may be equivalently characterized by an "up-to-iso" version of the above constructions using [[essential fibers]].

[Ayala and Francis](#AyalaFrancis) prove an analogous characterization of exponentiable [[(∞,1)-functors]].  The [[(∞,1)-category theory|(∞,1)-categorical context]] eliminates the "level-shifting" in the characterization via $Prof$ (i.e. the presence of a [[bicategory]] [[Prof]] when discussing only exponentiable 1-functors).  Thus, there is an [[(∞,1)-category]] [[(∞,1)Prof]] such that exponentiable $(\infty,1)$-functors into an $(\infty,1)$-category $B$ correspond to $(\infty,1)$-functors $B\to (\infty,1)Prof$.

As in the 1-categorical case, ordinary $(\infty,1)$-transformations between functors $B\to (\infty,1)Prof$ do not give the correct maps between exponentiable $(\infty,1)$-functors over $B$; we need to instead regard $(\infty,1)Prof$ as a sort of "$(\infty,1)$-double category".  Ayala and Francis consider only the vertically-invertible fragment of this $(\infty,1)$-double category, which can be represented as a functor from an $\infty$-groupoid to an $(\infty,1)$-category (a sort of [[proarrow equipment]] with all 2-cells and all 1-cells in the domain invertible); this is what they call a "flagged" $(\infty,1)$-category and is also what is represented by a non-complete [[Segal space]].  Of course, restricting to the vertically-invertible fragment of $(\infty,1)Prof$ also restricts what it classifies to the $\infty$-groupoid of exponentiable $(\infty,1)$-functors over $B$ rather than the whole $(\infty,1)$-category thereof.,

## In a double category - completeness
Functors satisfying a Conduch&#233;-like condition are central to completeness/cocompleteness in [[pseudo-double categories]]. In short, in 1-category theory, $A$ is complete iff for any small $M$ and locally small $C$, $K: M\to C$ a functor, $T : A\to M$, $T$ has a pointwise right Kan extension along $K$; in pseudo double categories, this is too strong, and we must restrict to double functors $K: M\to C$ satisfying a Conduch&#233; condition.

A pseudo-double category is *unitary* if the vertical identity arrows are strict identities, so $1_A\circ f = f = f\circ 1_B$ on-the-nose. We here assume all double categories are unitary; this is not a severe restriction in practice.

Call a lax functor $F: \mathbb{A}\to\mathbb{B}$ between pseudo-double categories *unitary* if it it preserves identity vertical arrows on-the-nose and the comparison map $1_{FA}\to F(1_A)$ is the identity; therefore it is only really lax from the point of view of composition. A unitary lax functor $1\to\mathbb{A}$ is automatically strict, as $1$ has no nontrivial compositions, whereas a lax functor $1\to\mathbb{A}$ is an object endowed with a vertical monad.

Note that if we are working in a 2-category of lax functors, and we want to define the limit of a functor $F : \mathbb{A}\to\mathbb{B}$ as the right Kan extension of $F$ along $!_{\mathbb{A}}:\mathbb{A}\to 1$, we probably want to consider the initial extension $1\to \mathbb{B}$ along unitary lax functors rather than lax functors, so that our answer is just an object of $\mathbb{B}$ and a cocone rather than a vertical monad in $\mathbb{B}$. Thus we will here consider unitary Kan extensions.

The correct definition of "complete" for a pseudo-double category $\mathbb{A}$ is that it admits pointwise unitary lax right Kan extensions of any lax double functor $S: \mathbb{I}\to\mathbb{A}$ ($\mathbb{I}$ small) along all lax double functor along a lax double functor $R: \mathbb{I}\to\mathbb{J}$, where $R$ satisfies the "right Conduch&#233; condition: that the laxity 2-cell for vertical composition in $R$,
\begin{centre}
\begin{tikzcd}
	{\mathbb{I}_a\times_{\mathbb{I}_o}\mathbb{I}_a} & {\mathbb{J}_a\times_{\mathbb{J}_o}\mathbb{J}_a} \\
	{\mathbb{I}_a} & {\mathbb{J}_a}
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\circ_\mathbb{I}}"', from=1-1, to=2-1]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\circ_\mathbb{J}}", from=1-2, to=2-2]
	\arrow["{R\times R}", from=1-1, to=1-2]
	\arrow["R"', from=2-1, to=2-2]
	\arrow["\alpha", shorten <=9pt, shorten >=9pt, Rightarrow, from=1, to=0]
\end{tikzcd}
\end{centre}
is [[exact square|exact]].
Here, $\mathbb{I}_o$ is the category of objects and horizontal morphisms of $\mathbb{I}$, and $\mathbb{I}_a$ is the category of arrows and 2-cells.

The situation for cocompleteness is dual, replacing lax by colax everywhere.

For more on this see [Grandis and Paré](#GrandisParé07), Theorem 5.2.

## Examples

* The above considerations show that any Grothendieck fibration *or* opfibration is a (strict) Conduch&#233; functor, while any [[Street fibration]] or opfibration is a non-strict Conduch&#233; functor.

* If $\mathbf{2}$ denotes the [[interval category]], then any [[normal lax functor]] out of $\mathbf{2}$ is necessarily pseudo, since there are no composable pairs of nonidentity arrows in $\mathbf{2}$.  It follows that, as pointed out by Jean Benabou, *any* functor with codomain $\mathbf{2}$ is a Conduch&#233; functor.  Note that functors with codomain $\mathbf{2}$ can also be identified with [[profunctors]], the two fiber categories being the source and target of the corresponding profunctor.

* As with [[exponentiable morphisms]] in any category, Conduch&#233; functors are closed under composition.

## References

That Conduché functors are exactly the exponentiable ones is Theorem 4.4 (pages 40-45) of

* {#Giraud64} [[J. Giraud]], _M&#233;thode de la descente_, Bull. Math. Soc. M&#233;moire **2** (1964). ([numdam](http://www.numdam.org/numdam-bin/item?id=MSMF_1964__2__R3_0))

See also,

* {#Conduche72} [[F. Conduché]], _Au sujet de l'existence d'adjoints &#224; droite aux foncteurs 'image reciproque' dans la cat&#233;gorie des cat&#233;gories_ , C. R. Acad. Sci. Paris **275** S&#233;rie A (1972) pp.891-894. ([gallica](http://gallica.bnf.fr/ark:/12148/bpt6k56191352/f19.image#))

* {#GrandisParé07} [[Marco Grandis]], [[Robert Paré]] _Lax Kan extensions for double categories (on weak double categories, part IV)_ , Cahiers de topologie et géométrie différentielle catégoriques, tome 48, no 3 (2007), p. 163-199

Some of definitions and proofs of the above theorems, along with the 2-categorical generalization (Conduch&#233; considered only the 1-categorical case) can also be found in (e.g. see Lemma 6.1 for a proof that Conduch&#233; implies exponentiability):

* [[Peter Johnstone]], "Fibrations and partial products in a 2-category", *Appl. Categ. Structures* 1 (1993), 141--179

A description of the characterization in terms of lax normal functors can be found in

* [[Ross Street]], \'Powerful functors\', [pdf](http://www.math.mq.edu.au/~street/Pow.fun.pdf)

Discrete Conduch&#233; functors are considered in

* {#BN00}[[Marta Bunge|M. Bunge]], [[Susan Niefield|S. Niefield]], _Exponentiability and single universes_ , JPAA **148** (2000) pp.217-250.

* [[Peter Johnstone]], _A Note on Discrete Conduch&#233; Fibrations_ , TAC **5** no.1 (1999) pp.1-11. ([pdf](http://www.tac.mta.ca/tac/volumes/1999/n1/n1.pdf))

An analogue of Conduch&#233; functors for [[∞-categories]], classified by maps into an ∞-category version of [[Prof]], is studied in

* {#AyalaFrancis} [[David Ayala]] and [[John Francis]], _Fibrations of ∞-categories_, [arxiv](https://arxiv.org/abs/1702.02681)

A discussion of ULF functors (including the fact they form a factorisation system) is contained in:

* [Pullback-homomorphisms](https://golem.ph.utexas.edu/category/2010/08/pullbackhomomorphisms.html), n-Category Café (2010)

* [[Tom Leinster]], _Notions of Möbius inversion_, Bulletin of the Belgian Mathematical Society-Simon Stevin 19.5 (2012): 909-933.

[[!redirects Conduché fibration]]
[[!redirects Conduchè fibration]]
[[!redirects Conduche fibration]]

[[!redirects Conduché functor]]
[[!redirects Conduchè functor]]
[[!redirects Conduche functor]]

[[!redirects Conduché functors]]
[[!redirects Conduchè functors]]
[[!redirects Conduche functors]]

[[!redirects exponentiable functors]]

[[!redirects strict Conduche functor]]
[[!redirects strict Conduche functors]]
[[!redirects strict Conduché functor]]
[[!redirects strict Conduché functors]]

[[!redirects strictly exponentiable functor]]
[[!redirects strictly exponentiable functors]]
[[!redirects powerful functor]]
[[!redirects powerful functors]]
[[!redirects strictly powerful functor]]
[[!redirects strictly powerful functors]]

[[!redirects Conduché ∞-fibration]]
[[!redirects Conduche ∞-fibration]]
[[!redirects Conduche ∞-functor]]
[[!redirects Conduche ∞-functors]]
[[!redirects Conduché ∞-functor]]
[[!redirects Conduché ∞-functors]]
[[!redirects exponentiable ∞-functor]]
[[!redirects exponentiable ∞-functors]]
[[!redirects Conduché infinity-fibration]]
[[!redirects Conduche infinity-fibration]]
[[!redirects Conduche infinity-functor]]
[[!redirects Conduche infinity-functors]]
[[!redirects Conduché infinity-functor]]
[[!redirects Conduché infinity-functors]]
[[!redirects exponentiable infinity-functor]]
[[!redirects exponentiable infinity-functors]]

[[!redirects discrete Conduché functor]]
[[!redirects discrete Conduché functors]]
[[!redirects discrete exponentiable functor]]
[[!redirects discrete exponentiable functors]]

[[!redirects ULF]]
[[!redirects ULF functor]]
[[!redirects ULF functors]]
