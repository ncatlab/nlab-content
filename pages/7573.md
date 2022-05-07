+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


This is a subentry of _[[sheaf]]_ about the _plus-construction on presheaves_. For other constructions called _[[plus construction]]_, see there.

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The _plus construction_ $(-)^+ : PSh(C) \to PSh(C)$ on presheaves over a [[site]] $C$ is an operation that makes a presheaf "closer" to being a sheaf.

For ordinary sheaves of sets, the plus construction replaces a [[presheaf]] first by a [[separated presheaf]] and then by a [[sheaf]].

$$
  PSh(C) \stackrel{(-)^+}{\to} SepPSh(C)
  \stackrel{(-)^+}{\to} Sh(C)
  \,.
$$

(The first of these steps, however, is not a [[reflective subcategory|reflection]] into $SepPsh(C)$.)  Notice that in terms of [[n-truncated]] morphisms, a presheaf is

* separated precisely if every comparison map $A(U) \to Desc(A,U)$ to the set of [[descent data]] is [[(-1)-truncated]], namely a [[monomorphism]];

* a sheaf precisely if every such comparison map is [[(-2)-truncated]], namely an [[equivalence]].

More generally, in [[(n,1)-topos]] theory, the plus-construction is applied $(n+1)$-times in a row to an [[(n,1)-presheaf]] (a presheaf of $(n-1)$-groupoids), at each step decreasing the truncatedness of the comparison map until at the last step it becomes an actual [[(n,1)-sheaf]], a.k.a. stack; see [Anel and Leena Subramaniam, 2020](#ALS).  When $n=\infty$, even a countable sequence of applications does not suffice, but a transfinite one does; see [Lurie, section 6.5.3](#Lurie).

## Definition


+-- {: .num_defn #PlusConstruction}
###### Definition

Let $C$ be a small site equipped with a [[Grothendieck topology]] $J$, let $A:C^{op}\to Set$ be a functor. Then the __plus construction__ is a functor $(-)^+ : PSh(C) \to PSh(C)$ defined by the following equivalent descriptions:

1. $A^+(U) = colim_{(R\hookrightarrow  y U)\in J(U)} Hom_{Psh(C)}(R,A)$ where $J(U)$ can be defined in any of the following equivalent ways:
   * The poset of covering [[sieves]] on $U$ for the topology.  (It is important here that we use covering *sieves*, or at least families closed under composition and identities.)
   * The class of [[dense monomorphisms]] with [[representable functor|representable]] codomain $y U$.
   * The class of monomorphisms with codomain $y U$ that are inverted by the [[sheafification]] functor.  (Of course, this definition is not available unless we have shown that sheafification exists in some other way.)

1. For $U\in C^{op}$ we define $A^+(U)$ to be the set of [[equivalence classes]] of pairs $(R,s)$ where $R\in J(U)$ and $s=(s_f\in A(dom f)|f\in R)$ is a [[matching family|compatible family]] of elements of $A$ relative to $R$, and $(R,s)\sim (R', s')$ iff there is a $J$-covering sieve $R'' \subseteq R \cap R'$ on which the restrictions of $s$ and $s'$ agree.

1. In the [[internal language]] of the presheaf topos $PSh(C)$, we can define $ A^+ = \{ K \subseteq A \,|\, j(K\,\text{ is a singleton}) \}/{\sim}$, where $\sim$ is the equivalence relation given by $K \sim L$ if and only if $j(K = L)$ and $j$ is the [[Lawvere-Tierney topology]].

1. $A^+ = Lan_{r^{op}} Ran_{s^{op}} A$, where $r : J \to C$ is the [[Grothendieck construction]] of the functor $Cov : C^{op} \to Pos$ sending each $U$ to its set of covering [[sieves]], and $s:C\to J$ sends each $U\in C$ to its maximal sieve $M_U$ (the set of all morphisms with codomain $U$).
=--

The first and last of these definitions also work for higher sheaves on higher sites, i.e. when $C$ is an [[(infinity,1)-site]] and $A:C^{op} \to \infty Gpd$ is an [[(infinity,1)-presheaf]], as long as limits, colimits, and Kan extensions are interpreted in the $(\infty,1)$-categorical sense.

## Construction of sheafification

The basic property of the plus-construction is that we can construct [[sheafification]] (a.k.a. stack completion, in the higher-categorical case) by iterating it.  For ordinary presheaves of sets, two iterations suffice: for any presheaf $A$, $A^+$ is separated, while if $A$ is separated then $A^+$ is a sheaf; thus $A^{++}$ is the sheafification of any presheaf $A$.

+-- {: .num_remark}
###### Remark
Note, though, that $(-)^+ : PSh(C) \to SepPSh(C)$ is not left adjoint to the inclusion $\iota : SepPSh(C) \hookrightarrow PSh(C)$ of the full subcategory of separated presheaves. If it were, it would be a [[reflector]] and therefore satisfy $(-)^+ \circ \iota \cong Id$. But this is false, since the plus construction applied to separated presheaves yields their sheafification. See [this MathOverflow question](http://mathoverflow.net/questions/49486/the-single-plus-construction-is-not-the-left-adjoint-of-the-inclusion-of-separat) for details.
=--

More generally, when working with presheaves of $n$-groupoids for some finite $n$, it takes $n+2$ iterations for the plus-construction to converge to a sheaf/stack.  In the case $n=\infty$, no finite number of iterations suffices, and not even a countable number, but a transfinite number does.

We now sketch a proof of these facts, using the [[implicit infinity-category convention]] so that our results apply to higher sheaves/stacks as well as ordinary ones.

We use the fourth definition above $A^+ = Lan_{r^{op}} Ran_{s^{op}} A$, which we will write more shortly as $A^+ = r_! s_* A$.  There is a canonical map $A\to A^+$, which we can more easily construct and study with the following observation:

\begin{lemma}\label{AnAdjointQuadruple}
  $s:C\to J$ is right adjoint to $r:J\to C$.  Therefore, we have an adjunction $r^* : Psh(C) \rightleftarrows Psh(J) : s^*$, and hence an [[adjoint quadruple]]:
  $$ r_! \dashv r^* \dashv s^* \dashv s_*. $$
  Moreover, $r^*$ and $s_*$ are [[fully faithful]] and $r_!$ preserves finite limits, so $Psh(J)$ is [[cohesive topos|cohesive]] and even [[totally connected topos|totally connected]] over $Psh(C)$.
\end{lemma}
\begin{proof}
  Since the maximal sieve $M_U$ is the terminal object of the fiber of $r$, the functor $s$ picks out a fiberwise terminal object in the fibration $r$; thus it is right adjoint to $r$.  This implies the existence of the adjoint quadruple as discussed [[adjoint quadruple#KanExtensionOfAdjointPairIsAdjointQuadruple|here]].  Since $r s = 1_C$, we have that $s$ is fully faithful, and hence so are $s_*$ and $s_! \cong r^*$.  Finally, the fibers of $r^{op}$ are filtered since covering sieves are closed under intersections, so $r_!$ preserves finite limits since finite limits commute with filtered colimits.
\end{proof}

Thus, we can identify $Psh(C)$ with either the [[discrete objects]] or [[codiscrete objects]] in $Psh(J)$, via the fully faithful functors $r^*$ or $s_*$.  If we regard $A\in Psh(C)$ as the discrete object $r^*A$, then the plus-construction is similarly identified with $r^* r_! s_* s^* r^* A$.  Thus $r^*(A^+)$ can be written as $&#643; \sharp r^* A$, where $&#643; = r^* r_!$ is the reflector into the discrete objects and $\sharp = s_* s^*$ is the reflector into the codiscrete objects.

The rest of the proof can actually be carried out "synthetically" in the [[internal logic|internal]] [[homotopy type theory]] of the cohesive topos $Psh(J)$.  This argument is formalized [in the HoTT/Coq library](#HoTTplus).  But here we formulate the argument externally and categorically.

\begin{lemma}\label{PlusWellPointed}
The plus-construction is a [[well-pointed endofunctor]].  That is, we have a natural transformation $\eta : A \to A^+$ and a homotopy (an equality in the case $n=0$) $\theta : \eta_{A^+} \sim (\eta_A)^+$.  Moreover, the whiskered homotopy $\theta \eta_A$ is homotopic to the naturality square $\eta_{A^+} \circ \eta_A \sim (\eta_A)^+ \circ \eta_A$.
\end{lemma}
\begin{proof}
This follows fairly formally from its identification with $&#643; \sharp$, the composite of two reflectors.
\end{proof}

\begin{lemma}
The plus-construction preserves finite limits.
\end{lemma}
\begin{proof}
Both functors $r_!$ and $s_*$ preserve finite limits.
\end{proof}

\begin{lemma}
For $A\in Psh(C)$, the following are equivalent:

1. $A$ is a sheaf.
1. The canonical map $r^* A \to s_* A$ is an equivalence.
1. $r^* A$ is codiscrete.
1. $\eta_A : A \to A^+$ is an equivalence.
1. $\eta_A : A \to A^+$ has a retraction.

\end{lemma}
\begin{proof}
To see that the first two are equivalent, note that for a covering sieve $R$ of $U$ we have $(r^* A)(R) = A(U)$ while $(s_* A)(R)$ is the space of descent data for $R$.  Now we have $s_* A \cong s_* s^* r^* A = \sharp r^* A$, so the second and third statements are equivalent.

For the fourth, if $r^*A $ is codiscrete, then it is equivalent to $\sharp r^* A$; hence the latter is also discrete, and thus equivalent to $&#643; \sharp r^* A$.  Of course if $\eta_A$ is an equivalence, it has a retraction.  Finally, if it has a retraction, then the composite $\sharp r^* A \to &#643; \sharp r^* A = r^* A^+$ is a retraction for $r^* A \to \sharp r^* A$, so that $r^*A$ is codiscrete.
\end{proof}

\begin{theorem}
If some (perhaps transfinite) iteration of the plus-construction on $A\in Psh(C)$ stabilizes, it is a sheaf and the sheafification of $A$.
\end{theorem}
\begin{proof}
This follows formally from the fact that the plus-construction is a well-pointed endofunctor whose fixed points are the sheaves.
\end{proof}

Now since the plus-construction is an accessible endofunctor of a locally presentable category, its iteration always converges at some transfinite stage.  It follows that sheafification exists.  (Roughly this argument appears in [Lurie, section 6.5.3](#Lurie).)

We now want to prove that if $A$ is a presheaf of $n$-groupoids for some finite $n$, the iteration in fact converges already after $n+2$ steps.  Though long expected, it seems that this was first actually proven by [Anel and Leena Subramaniam, 2020](#ALS); what follows is inspired by their proof.  We will actually prove something slightly more general.

\begin{definition}
A presheaf $A\in Psh(C)$ is **$n$-separated** if the map $\eta_A : A\to A^+$ is [[n-truncated]].
\end{definition}

Thus $A$ is a sheaf if and only if it is $(-2)$-separated.  Moreover, since the plus-construction preserves finite limits, it preserves truncated objects; thus if $A$ is $n$-truncated (i.e. a presheaf of $n$-groupoids) then so is $A^+$ and hence so is $\eta_A$.  Thus, any $n$-truncated presheaf is $n$-separated.

We will prove that if $A$ is $n$-separated, then its plus-construction converges after $n+2$ steps.  The central auxiliary definition is:

\begin{definition}
A map $f:A\to B$ in $Psh(C)$ is **plus-connected** if there is a lift in its $\eta$-naturality square.  That is, there is a map $h:B \to A^+$ and homotopies $f^+ h \sim \eta_B$ and $h f \sim \eta_A$ that paste to the naturality square $f^+ \eta_A \sim \eta_B f$.
\end{definition}

\begin{lemma}
For any $A\in Psh(C)$, the map $\eta_A : A\to A^+$ is plus-connected.
\end{lemma}
\begin{proof}
Lemma \ref{PlusWellPointed} says precisely that $1_{A^+}$ is a lift in the $\eta$-naturality square for $\eta_A$.
\end{proof}

\begin{lemma}
If $f:A\to B$ is plus-connected, so is its diagonal $\triangle f : A \to A\times_B A$.
\end{lemma}
\begin{proof}
Since the plus-construction preserves finite limits, it suffices to observe that if a given commutative square has a lift, so does the induced square between its diagonals.
\end{proof}

So far everything has been very formal.  The concrete input from the fact that we are talking about a Grothendieck topology comes here:

\begin{lemma}\label{Composing}
If $f:A\to B$ is a [[monomorphism in an (infinity,1)-category|monomorphism]] that is plus-connected, then $f^+ : A^+ \to B^+$ is an equivalence.
\end{lemma}
\begin{proof}
Since the plus-construction preserves finite limits, it preserves monomorphisms; thus it suffices to show that $f^+$ is surjective.  An object $x\in B^+(U)$ is determined by a matching family over a covering sieve $R\hookrightarrow y U$, consisting of $x_V \in B(V)$ for all $V\to U$ in $R$.  Since $f$ is plus-connected, we have a map $h:B\to A^+$ assigning to each $x_V$ an object $h(x_V) \in A^+(V)$, determined by a matching family over a covering sieve $S_V \hookrightarrow y V$.  Now we can compose the sieves $S_V$ and $R$ to obtain a covering sieve $T$ on $U$, such that the restriction of $x$ to $T$ (which is equal to $x$) is in the image of $f^+$.
\end{proof}

\begin{lemma}
For $n\ge -1$, if $f:A\to B$ is $n$-truncated and plus-connected, then $f^+ : A^+ \to B^+$ is $(n-1)$-truncated.
\end{lemma}
\begin{proof}
By induction.  The base case $n=-1$ is the previous lemma.  For the inductive step, $f$ is $(n+1)$-truncated and plus-connected, then its diagonal $\triangle f$ is $n$-truncated and plus-connected.  Thus, by induction $(\triangle f)^+$ is $(n-1)$-truncated.  But since the plus-construction preserves finite limits, $(\triangle f)^+$ is equivalent to $\triangle (f^+)$, so $f^+$ is $n$-truncated.
\end{proof}

\begin{theorem}
If $A$ is $n$-separated, then its plus-construction converges after $n+2$ steps.
\end{theorem}
\begin{proof}
If $A$ is $n$-separated, then by definition $\eta_A : A\to A^+$ is $n$-truncated, and we have shown it is always plus-connected.  Thus, $(\eta_A)^+$ is $(n-1)$-truncated.  Hence so is $\eta_{A^+}$, in other words $A^+$ is $(n-1)$-separated.

Thus, by induction, if $A$ is $n$-separated, the $(n+2)$-th iteration of the plus-construction is $(n-(n+2))$-separated, i.e. $(-2)$-separated, i.e. a sheaf.
\end{proof}

\begin{remark}
Note that we do not need to know that the category $J$ is obtained as the category of covering sieves for a topology on $C$.  We only need that there is a projection $r:J\to C$ that is a fibration with cofiltered fibers and a fully faithful right adjoint, plus the result of Lemma \ref{Composing}.  In particular, $J$ could be a "mono-saturated lex modulator" in the sense of [ALS](#ALS), generating a non-topological localization of $Psh(C)$.
\end{remark}

\begin{remark}
We can also construct left exact localizations of non-presheaf toposes in this way.  If $E$ is a topos that is itself a left exact localization of some presheaf topos $Psh(C)$, then a lex modulator on $E$ induces a $J$ as above, and by composing the reflectors $&#643;$ and $\sharp$ with the reflection into $E$ we can make the same argument work to construct a left exact localization of $E$.
\end{remark}

## Related concepts

* [[sheafification]]

* [[(∞,1)-sheafification]] / [[∞-stackification]] 



## References 

Related entries: [[sheafification]]

A standard textbook reference in the context of 1-[[topos theory]] is:

* [[Peter Johnstone]], _[[Sketches of an elephant]] - a topos theory compendium_, Section C.2.2, proof of proposition 2.2.6, p.551

Remarks on the plus-construction in [[(infinity,1)-topos theory]] is in section 6.5.3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

The plus-construction for presheaves in values in abelian categories is also called the Heller-Rowe construction:

* [[Alex Heller]], K. A. Rowe, _On the category of sheaves_
Amer. J. Math. 84 1962 205&#8211;216, [MR144341](http://www.ams.org/mathscinet-getitem?mr=144341), [doi](http://dx.doi.org/10.2307/2372759)

The plus-construction is studied for higher sheaves, and shown to converge after $n+2$ steps for $n$-presheaves, in

* {#ALS} [[Mathieu Anel]], Chaitanya Leena Subramaniam.  _Small object arguments, plus-construction, and left-exact localizations_.  [arxiv:2004.00731](https://arxiv.org/abs/2004.00731), 2020.

The above argument is formalized in the internal logic of $Psh(J)$ here:

* {#HoTTplus} Canonical binary meets of subuniverses, <https://github.com/HoTT/HoTT/blob/master/theories/Modalities/Meet.v>

[[!redirects plus-construction on presheaves]]
[[!redirects plus constructions on presheaves]]
[[!redirects plus-constructions on presheaves]]
