+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Conceptual completeness

**Conceptual completeness** refers to the result of [Makkai and Reyes '77](#MakRey) that the [[enriched hom-functor|hom-2-functor]] ${\mathbf{Pretop}}(-,{Set}) : \mathbf{Pretop}^{op} \to \mathbf{CAT}$, for the [[2-category]] $\mathbf{Pretop}$ of ([[small category|small]]) [[pretopos|pretoposes]], reflects [[equivalences]]. More explicitly:

\begin{theorem}\label{thm:conc-compl-pretoposes}**(Conceptual completeness for pretoposes)**

Let $F : P_1 \to P_2$ be a pretopos morphism between small pretoposes. If the precomposition functor
\[  F^* : {\mathbf{Pretop}}(P_2, {Set}) \to {\mathbf{Pretop}}(P_1,{Set}) \]
is an equivalence of categories, then so is $F$. 
\end{theorem}

From a logical point of view, recall that pretoposes can be identified with  ([[syntactic categories]] of) [[coherent logic|coherent theories]] up to [[elimination of imaginaries]], so that a pretopos morphism $P_1 \to P_2$ corresponds to an [[interpretation]] of the theory $P_1$ into the theory $P_2$, or equivalently to a model of the theory $P_1$ inside the category $P_2$; in particular, a pretopos morphism into [[Set]] is therefore a [[model]] of the source theory. In these terms, conceptual completeness states that if an interpretation $T_1 \to T_2$ between two coherent theories induces an equivalence $\operatorname{Mod}(T_2) \to \operatorname{Mod}(T_1)$ between the categories of models, then $T_1$ and $T_2$ are bi-interpretable up to elimination of imaginaries, that is, $T_1^{eq}$ and $T_2^{eq}$ are bi-interpretable.

\begin{remark}
The above theorem can also be interpreted as a "semantic" characterization of pretoposes among coherent categories, instead of their "syntactic" characterization as (syntactic categories of) coherent theories admitting elimination of imaginaries.   First note that, as stated in [Theorem 7.1.8, Makkai and Reyes '77](#MakRey), the theorem above holds also if the target category is merely a coherent category: that is, if $F \colon P \to C$ is a coherent functor from a pretopos $P$ to a coherent category $C$ such that $-\circ F \colon \operatorname{Mod}(C) \to \operatorname{Mod}(P)$ is an equivalence of categories, then $F$ is an equivalence itself. Call now a coherent functor $C \to C'$ an _extension_ of $C$. An extension $I \colon C \to C'$ of a coherent category $C$ is:

1. _tight_ (or _strongly conservative_ in [Makkai and Reyes](#MakRey)) if $I^* \colon \operatorname{Mod}(C') \to \operatorname{Mod}(C)$ is an equivalence of categories;

2. _significant_ if $I \colon C \to C'$ is _not_ an equivalence of categories.

We then say that a coherent category $C$ is _conceptually complete_ if every tight extension of $C$ is not significant. As the embedding of a coherent category into its [[pretopos completion]] is a tight extension, conceptually complete categories are pretoposes; conversely, the conceptual completeness theorem can be rephrased by saying that pretoposes are conceptually complete, thus characterizing pretoposes as the conceptually complete (coherent) categories. Intuitively, this corresponds to the fact that pretoposes admit all the coherently-definable structure that coherent categories may lack but which coherent functors automatically preserve: that is, finite (disjunct) coproducts and quotients of definable equivalence relations. 
\end{remark}


The conceptual completeness theorem is proved in [Makkai and Reyes '77](#MakRey) via model-theoretical techniques, such as the compactness theorem, and "syntactical" arguments, exploiting the identification between coherent categories and coherent theories. In [Pitts '86](#Pitts86), Pitts provided a new, constructive, and purely categorical proof rephrasing the theorem in terms of an interpolation property for [[comma object|cocomma squares]] in $\mathbf{Pretop}$, which he employed in [Pitts '89](#Pitts89) to prove a conceptual completeness theorem for [[intuitionistic logic|intuitionistic first-order logic]] by considering _Heyting pretoposes_.

\begin{theorem}**(Pitts' interpolation theorem for pretoposes)**

Consider a cocomma square in $\mathbf{Pretop}$ 
\begin{tikzcd}
	R & T \\
	S & P
	\arrow["J", from=1-1, to=1-2]
	\arrow["I"', from=1-1, to=2-1]
	\arrow["N", from=1-2, to=2-2]
	\arrow["h", Rightarrow, from=2-1, to=1-2]
	\arrow["M"', from=2-1, to=2-2]
\end{tikzcd}
and let $r \in R$. Consider subobjects $s \rightarrowtail I(r)$ in $S$ and $t \rightarrowtail J(r)$ in $T$ such that $\exists_{h_r} ( M(s) ) \leq N(t)$ as subobjects of $NJ(r)$. Then, there exists a subobject $r' \rightarrowtail r$ in $R$ such that $s \leq I(r')$ as subobjects of $I(r)$ and $J(r') \leq t$ as subobjects of $J(r)$.
\end{theorem}


##Strong conceptual completeness

[[ultracategory|Ultracategories]], introduced by [Makkai '87](#Makkai87), allow for a stronger form of theorem \ref{thm:conc-compl-pretoposes}, known as **strong conceptual completeness**. Intuitively, the category of models $\operatorname{Mod}(P)= \mathbf{Pretop}(P, Set)$ of a (small) pretopos $P$ can be endowed with the structure of an ultracategory by considering the usual notion of ultraproducts of models; this way, the pretopos $P$ can be reconstructed up to equivalence by considering _ultrafunctors_ $\operatorname{Mod}(P) \to Set$, that is, functors which preserve ultraproducts in a suitable sense.

\begin{theorem}\label{thm:strong-conc-compl}**(Strong conceptual completeness for pretoposes)**

For every small pretopos $P$, the evaluation functor
\[ 
  ev 
    \colon 
  P \to \mathbf{Ult}\big( \operatorname{Mod}(P) , Set \big) 
\]
is an equivalence of categories, where $\mathbf{Ult}$ is the [[2-category]] of ultracategories, ultrafunctors, and transformations thereof.
\end{theorem}

In other words, $Set$ is a [[dualizing object]] for a [[dual adjunction|dual 2-adjunction]], known as [[Makkai duality]]:
\begin{tikzcd}
	{\mathbf{Pretop}^{op}} && {\mathbf{Ult}}
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\mathbf{Pretop}(-, Set)}"', bend right=25, from=1-1, to=1-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\mathbf{Ult}(-, Set)}"', bend right=25, from=1-3, to=1-1]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=1, to=0]
\end{tikzcd} 
The counit of this [[2-adjunction]], at a pretopos $P$, is given by the evaluation functor $ev \colon P \to  \mathbf{Ult}\big( \operatorname{Mod}(P) , Set \big) $: as it is an equivalence, the hom-2-functor ${\mathbf{Pretop}}(-,{Set}) : \mathbf{Pretop}^{op} \to \mathbf{Ult}$ is a [[fully faithful 2-functor|2-fully-faithful]] embedding. 

\begin{remark}
More precisely, as $Set$ is not a small pretopos, the previous 2-adjunction should be considered between $\mathbf{Ult}$ and $\mathbf{PRETOP}$, the 2-category of (potentially not small) pretoposes. As expressed in [Theorem 8.2, Makkai](#Makkai87), this 2-adjunction is then a _reflection in the small_, meaning that the counit $ev : P \to \mathbf{Ult} ( \operatorname{Mod}(P), Set )$ is an equivalence for each _small_ pretopos $P$.
\end{remark}

###Remarks
In his AMS monograph on duality and definability in first-order logic, Makkai refined the above reconstruction result to work with just the (ultra) [[core]] of the ultracategory of models of $T$. Awodey and his students replaced the ultracategory structure on this groupoid with a related topology instead; this is the "spectral groupoid" which forms the basis of the [[logical scheme]] approach.


### Related concepts

- [[ultraproduct]]
- [[Makkai duality]]
- [[Stone duality]]

##References

* {#MakRey} [[Michael Makkai]] and [[Gonzalo Reyes]], _First order categorical logic: Model-theoretical methods in the theory of topoi and related categories_, Springer-Verlag, 1977.

* {#Makkai87} [[Mihaly Makkai]], _Stone duality for first-order logic_, Adv. Math. __65__ 2 (1987) 97--170 &lbrack;<a href="https://doi.org/10.1016/0001-8708(87)90020-X">doi:10.1016/0001-8708(87)90020-X</a>,  [MR89h:03067](http://www.ams.org/mathscinet-getitem?mr=900266)&rbrack;

* {#Pitts86} [[Andrew Pitts]], _Interpolation and Conceptual Completeness for Pretoposes via Category Theory_, Mathematical Logic and Theoretical Computer Science, **106** (1987), pp. 301-327.

* [[Michael Makkai]], _Strong Conceptual Completeness for First-Order Logic_ , APAL **40** (1988) pp.167-215.  (freely available online)

* {#Pitts89} [[Andrew Pitts]], _Conceptual completeness for first-order Intuitionistic logic: an application of categorical logic_, APAL, **41** (1987), pp. 38-81.

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. II_ , Oxford UP 2002. (sec. D3.5, pp.931-939)

* Victor Harnik, _Model theory vs. categorical logic: two approaches to pretopos completion (a.k.a. $T^{eq}$)_, in: Models, logics, and higher-dimensional categories, 79&#8211;106 (Makkai volume), CRM Proc. Lecture Notes __53__, Amer. Math. Soc. 2011; [gBooks](http://books.google.fr/books?id=-PZpEXuvvm4C&lpg=PA79&ots=uB-pruKFx8&dq=Victor%20Harnik%20pretopos%20completion&pg=PA79#v=onepage&q=Victor%20Harnik%20pretopos%20completion&f=false) 

* {#Lurie} [[Jacob Lurie]], _Ultracategories_, ([pdf](http://www.math.harvard.edu/~lurie/papers/Conceptual.pdf))


An approach which reframes conceptual completeness in terms of [[logical schemes]] is adopted in section 4.4 of

* [[Spencer Breiner]], _Scheme representation for first-order logic_, ([arXiv:1402.2600](http://arxiv.org/abs/1402.2600))

For the $(\infty, 1)$-analog of conceptual completeness, see section A.9 of 

* [[Jacob Lurie]], [[Spectral Algebraic Geometry]]

[[!redirects strong conceptual completeness]]
