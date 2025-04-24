
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
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


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

A [[functor]] $U \,\colon\, D\to C$ is _monadic_ iff it has a [[left adjoint]] $F \,\colon\, C\to D$ such that -- under the [relation between adjunctions and monads](monad#RelationBetweenAdjunctionsAndMonads) -- the [[adjoint functor|adjunction]] $F\dashv U$ is that induced by the [[monad]] which it induces -- in which case it is called a *[[monadic adjunction]]*.

In this situation $U$ is identified with the [[forgetful functor]] from the [[Eilenberg-Moore category]] $EM(U \circ F)$ of the monad $(U \circ F, \eta, U\epsilon_F)$ on $C$, and hence shares the properties of these [[forgetful functors]].

\begin{tikzcd}
  \mathcal{C}
  \ar[
    from=r,
    "{ U }"{description}
  ]
  \ar[
    r,
    shift left=16pt,
    "{ F }"
  ]
  \ar[
    r,
    shift left=9.5pt,
    phantom,
    "{ \scalebox{.62}{$\bot$} }"
  ]
  &
  \mathcal{D}
  \simeq
  \mathrm{EM}(\mathrm{ U \circ F })
\end{tikzcd}


The *[[monadicity theorem]]* characterizes monadic functors and makes these 'nice properties' precise.

Monadic functors are sometimes called *functors of effective descent (type)*. See the page on *[[monadic descent]]* for more on this aspect.


## Definition

Given a [[adjoint pair|pair]] of [[adjoint functors]] $F \colon C \to D :U$, $F \dashv U$, with [[unit of an adjunction|unit]] $\eta: Id_C \to U \circ F$ and counit $\epsilon: F \circ U \to Id_D$, one constructs a [[monad]] $\mathbf{T}=(T,\mu,\eta)$ setting $T = U \circ F: C \to C$, $\mu = U \epsilon F: T T = U F U F \to U F = T$. 

Consider the [[Eilenberg-Moore category]] $C^{\mathbf{T}}$ of $T$-algebras ($T$-modules) in $C$. Clearly $U (\epsilon_M): T U M = U F U M \to U M$ is a $T$-action. In fact there is a canonical *[[comparison functor]]* $K^{\mathbf{T}} \colon D \to C^{\mathbf{T}}$ given on objects by $K(M) \coloneqq \big(U M, U (\epsilon_M) \big)$.  We then say that we have a (resp. strictly) [[monadic adjunction]] iff $K$ is an equivalence (resp. isomorphism) of categories.

\begin{definition}\label{MonadicFunctor}
**(monadic functor)**
\linebreak
A [[functor]] $U \colon D \to C$ is *monadic* (resp. *strictly monadic*) if it has a [[left adjoint]] $F \colon C\to D$ and the [[comparison functor]] $K^{\mathbf{T}} \colon D \to C^{\mathbf{T}}$ is an [[equivalence of categories]] (resp. an [[isomorphism]] of [[strict categories]]).  
\end{definition}

In other words, up to [[equivalence of categories|equivalence]], monadic functors are precisely the [[forgetful functors]] defined on [[Eilenberg-Moore categories]] for [[monads]], and strictly monadic functors are the same as these forgetful functors up to [[isomorphism]] of [[strict categories]]. 

* If the [[comparison functor]] is only [[fully faithful]], a functor is sometimes called *[[premonadic functor|premonadic]]* or said to be *of [[descent type]]*.


\begin{definition}
A *category* $D$ is called *monadic* over a category $C$ if there is any functor $U \colon D \to C$ which is monadic (Def. \ref{MonadicFunctor}).
\end{definition}



## Properties

### Basic properties

Every monadic functor is 

1. [[faithful functor|faithful]] (by the definition of [[Eilenberg-Moore category]]) 

1. [[conservative]] (by [Beck's monadicity theorem](monadicity+theorem#statement)).  

Moreover:

\begin{proposition}\label{MonadicFunctorsCreateLimits}
**([[monadic functors]] [[created limit|create limits]])**
A [[monadic functor]] 

1. [[created limit|creates]] all [[limits]] that exist in its [[codomain]];

1. creates all [[colimits]] that exist in its codomain and are preserved by the corresponding monad (or, equivalently, by the monadic functor itself).  

\end{proposition}
(e.g. [MacLane 71, Exercise IV.2.2 (p. 138)](#MacLane71))


\begin{remark}
Beware that the [[class]] of monadic functors is *not* generally closed under [[composition]]. 

For a specific **[[counter-example]]**: the category of [[reflexive graphs]] is monadic over [[Set]] via the functor $RefGph \to Set$ sending a graph to its set of [[edges]], and the [[category of categories]] is monadic over [[reflexive graphs]] via the [[forgetful functor]] $Cat \to RefGph$, but $Cat$ is not monadic over $Set$ (via any functor whatsoever, since monadic categories over [[Set]] are [[regular categories]] which [[Cat]] is not).

This is an instance of a general phenomenon: Let $\mathcal{C}$ be a [[reflective subcategory]] of a [[presheaf category]] $\widehat{A}$ (e.g. any [[locally presentable category]] is of this form). Then the [[adjoint functor|adjunction]] between $\mathcal{C}$ and $\widehat{A}$ is monadic, and the [[adjoint functor|adjunction]] between $\widehat{A}$ and $\mathrm{Set}^{\mathrm{Ob} A}$ is also monadic. But the composite adjunction between $\mathcal{C}$ and $\mathrm{Set}^{\mathrm{Ob} A}$ is often not monadic. For instance, if it is monadic, then $\mathcal{C}$ must be a [[Barr-exact category]].
\end{remark}

However, it is possible to characterise when the composite of two functors is monadic. The following characterisation is Theorem 6.5 of [Arkor and McDermott 2025](#AM23b).

\begin{theorem}
  Let $U : A \to B$ and $U' : B \to C$ be functors, and suppose that $U'$ is monadic (and in particular has a left adjoint $F'$). Then $U' U$ is monadic if and only if $U$ is [[relative monad|monadic relative to]] $F'$.
\end{theorem}

Monadic functors have the following cancellation property:
\begin{proposition}\label{Cancellation}
Consider a pair of [[adjoint functors|adjunctions]]:
\begin{tikzcd}
	A & B & C
	\arrow[""{name=0, anchor=center, inner sep=0}, "U", shift left=2, from=1-1, to=1-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{U'}", shift left=2, from=1-2, to=1-3]
	\arrow[""{name=2, anchor=center, inner sep=0}, "{F'}", shift left=2, from=1-3, to=1-2]
	\arrow[""{name=3, anchor=center, inner sep=0}, "F", shift left=2, from=1-2, to=1-1]
	\arrow["\dashv"{anchor=center, rotate=90}, draw=none, from=2, to=1]
	\arrow["\dashv"{anchor=center, rotate=90}, draw=none, from=3, to=0]
\end{tikzcd}
If here $U' U$ is monadic, then $U$ is of [[descent type]] and the [[comparison functor]] has a [[adjoint functor|left adjoint]]. If $U'$ is furthermore [[conservative]] (and in particular if it is monadic), then $U$ is monadic.
\end{proposition}

This is Propositions 4 and 5 of [Bourn](#Bourn).

\begin{proposition}
A monadic functor is *strictly monadic* if and only if it is also an [[amnestic functor|amnestic]] [[isofibration]].
\end{proposition}
\begin{proof}
Clearly, a strictly monadic functor is an amnestic isofibration; and if a monadic functor $U$ is amnestic, then the [[comparison functor]] $K$ is also [[amnestic functor|amnestic]], and if $U$ is a monadic isofibration, so is $K$; therefore in this case $K$ must be an isomorphism of categories. 
\end{proof}

### Monadicity theorem

Various versions of Beck's [[monadicity theorem]] (also: "tripleability theorem" in older literature) give sufficient, and sometimes necessary, conditions for a given functor to be monadic. There are also dual, [[comonadic functor|comonadic versions]].

### Monadic functors to Set

Monadic functors to the category [[Set]] have additional properties.  For example: 

* Every monadic functor $U \,\colon\, D \to \mathrm{Set}$ is a [[solid functor]].  

* A category is monadic over $\mathrm{Set}$ (i.e. it admits a monadic functor to $\mathrm{Set}$) if and only if is [[exact category|Barr exact]], [[cocomplete category|cocomplete]], and has a [[projective object|projective]] [[separator|generator]].

&lbrack;[Vitale (1994)](#Vitale94)&rbrack;

## Examples
 {#Examples}

\begin{example}
  \label{ReflectiveSubcategoryInclusion}
  Every [[reflective subcategory]]-inclusion is a [[monadic functor]]. See also [there](reflective+subcategory#ReflectiveSubcategoryInclusionIsMonadic).
\end{example}

A proof is spelled out for instance in [Borceux 1994, vol 2, cor. 4.2.4](reflective+subcategory#Borceux94b). A [[formal proof]] in [[cubical Agda]] is given in [1Lab](reflective+subcategory#1Lab). See also at _[idempotent monad -- Properties -- Algebras for an idempotent monad and localization](idempotent+monad#AlgebrasForAnIdempotentMonad)_.



## Related concepts

* [[monadic adjunction]], [[structure-semantics adjunction]]

* [[comonadic functor]], [[monadicity theorem]]

* [[monadic decomposition]]


## References

* {#MacLane71} [[Saunders Mac Lane]], Section VI in: _[[Categories for the Working Mathematician]]_, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


* [[Francis Borceux]], Def. 4.4.1 in: *[[Handbook of Categorical Algebra]]*,   Vol. 2: *Categories and Structures*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)&rbrack;

* [[Emily Riehl]], §5.3 in: _[[Category Theory in Context]]_, Dover Publications (2017) &lbrack;[pdf](http://www.math.jhu.edu/~eriehl/context.pdf)&rbrack;

* {#Bourn} [[Dominique Bourn]]. _Low dimensional geometry of the notion of choice_. Category Theory 1991, CMS Conf. Proc. Vol. 13. 1992.

* {#Vitale94} [[Enrico Vitale]], *On the characterization of monadic categories over $SET$*, Cahiers de topologie et géométrie différentielle catégoriques **35** 4 (1994) 351-358.  &lbrack;[numdam:CTGDC_1994__35_4_351_0](http://www.numdam.org/item/?id=CTGDC_1994__35_4_351_0), [pdf](http://www.numdam.org/article/CTGDC_1994__35_4_351_0.pdf)&rbrack;

* {#AM23b} [[Nathanael Arkor]], [[Dylan McDermott]], _Relative monadicity_, Journal of Algebra 663 (2025), [DOI](https://doi.org/10.1016/j.jalgebra.2024.08.040) &lbrack;[arXiv:2305.10405](https://arxiv.org/abs/2305.10405)&rbrack;

[[!redirects monadic]]
[[!redirects monadic category]]
[[!redirects monadic functors]]

[[!redirects comonadic]]
[[!redirects co-monadic]]

[[!redirects comonadic functor]]
[[!redirects co-monadic functor]]
[[!redirects comonadic functors]]
[[!redirects co-monadic functors]]

[[!redirects effective descent type]]
[[!redirects functor of effective descent type]]
[[!redirects functors of effective descent type]]

