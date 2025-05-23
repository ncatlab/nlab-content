+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

An **enhanced 2-category** (or **$\mathcal{F}$-category**) is like a [[2-category]], but with two types of [[1-morphisms]], one of which we think of as "stricter" than the other.  The stricter morphisms are called **tight** and the less strict ones are called **loose**.

## Definition

### Strict $\mathcal{F}$-categories

Let $\mathcal{F}$ denote the category whose [[objects]] are [[functors]] that are [[fully faithful functors|fully faithful]] and injective on objects, and whose [[morphisms]] are [[commutative squares]] (a [[full subcategory]] of the [[arrow category]] of [[Cat]]).  We call the objects of $\mathcal{F}$, for the nonce, _full embeddings_.  Then $\mathcal{F}$ is [[cartesian closed category|cartesian closed]], [[complete category|complete]] and [[cocomplete category|cocomplete]], hence a [[Benabou cosmos]].

A **strict $\mathcal{F}$-category** is a [[enriched category|category enriched over]] $\mathcal{F}$.  Therefore, between every two objects, an $\mathcal{F}$-category $K$ has an object $K(x,y)\in \mathcal{F}$, hence a full embedding $K(x,y)_\tau \to K(x,y)_\lambda$.  The objects of $K(x,y)_\tau$ are called **tight morphisms** $x\to y$, and the objects of $K(x,y)_\lambda$ are called **loose morphisms** $x\rightsquigarrow y$.

Since full embeddings are injective on objects, "being tight" is a [[stuff, structure, property|property]] of a loose morphism.  (This would still be true in the "up to unique isomorphism" sense even if we did not ask for injectivity on objects, but when dealing with strict things, it is easier to keep them as strict as possible.)  And since full embeddings are fully faithful, the 2-cells between two tight morphisms are the same whether we regard them as tight or as loose.

For any $\mathcal{F}$-category $K$, the objects, tight morphisms, and 2-cells form a strict 2-category $K_\tau$, and the objects, loose morphisms, and 2-cells form a strict 2-category $K_\lambda$.  There is an obvious strict 2-functor
$$J_K : K_\tau \to K_\lambda$$
which is the identity on objects, strictly [[faithful functor|faithful]] on 1-morphisms, and [[locally fully faithful 2-functor|locally fully faithful]].  Since $K$ can be recovered from this 2-functor, an equivalent definition of a strict $\mathcal{F}$-category is as a strict 2-functor with these properties.

Strict $\mathcal{F}$-categories are equivalent to strict [[double categories]] with a functorial choice of [[companions]], and for which the assignment of tight morphisms to loose morphisms is injective.

### Weak $\mathcal{F}$-categories

Probably the best "fully weak" version of $\mathcal{F}$-categories is obtained by redefining $\mathcal{F}$ to consist of fully faithful functors, with squares that commute up to specified isomorphism, and then by considering $\mathcal{F}$-[[enriched bicategories]] rather than enriched categories.  Such a thing would be equivalent to an identity-on-objects and locally-fully-faithful pseudofunctor between bicategories.

One could consider semi-strict versions as well, in which (for example) the tight morphisms form a strict 2-category.

## Examples

* Any [[proarrow equipment]] is an $\mathcal{F}$-category (perhaps weak, perhaps semi-strict).

* An example of a semi-strict $\mathcal{F}$-category is the [[localization]] 2-functor $Cat(S) \to Cat(S)[W^{-1}]$ for a class of [[weak equivalences]] $W$.

* For any ([[strict 2-monad|strict]]) [[2-monad]] $T$, there are strict $\mathcal{F}$-categories of $T$-algebras whose tight and loose morphisms are, respectively:

  1. strict and pseudo $T$-morphisms
  1. strict and [[lax morphism|lax]] $T$-morphisms
  1. strict and colax $T$-morphisms
  1. pseudo and lax $T$-morphisms
  1. pseudo and colax $T$-morphisms

  In fact, this can be generalized to any $\mathcal{F}$-monad on an $\mathcal{F}$-category.

* Any 2-category gives rise to two $\mathcal{F}$-categories:

  * In a **chordate** $\mathcal{F}$-category, all morphisms are tight.
  * In an **inchordate** $\mathcal{F}$-category, only identities are tight.

* The [[lax slice 2-category]] is an $\mathcal{F}$-category whose tight 2-category is the (pseudo) slice 2-category.  This $\mathcal{F}$-category allows a definition of [[fibration in a 2-category|fibrations]] using [[lax F-adjunctions]].

* $\mathcal{F}$ itself becomes an $\mathcal{F}$-category in the usual way.  Its tight morphisms are just the morphisms in the underlying ordinary category $\mathcal{F}$, while its loose morphisms are simply functors between the loose parts (the codomains of the full embeddings).

## $\mathcal{F}$-functors and $\mathcal{F}$-transformations

\begin{definition}
An **$\mathcal{F}$-functor** $F:\mathbb{A} \to \mathbb{B}$ is a [[2-functor]] $F_\lambda:\mathcal{A}_\lambda \to \mathcal{B}_\lambda$ sends tight 1-cells to tight 1-cells, i.e. such that it co/restrcts to a 2-functor $F_\tau:\mathcal{A}_\tau \to \mathcal{B}_\tau$.
\end{definition}

\begin{definition}
An **$\mathcal{F}$-natural transformation** $\alpha:F \to G$ is a [[2-natural transformation]] $F_\tau \to G_\tau$, i.e. a 2-natural transformation $F \to G$ whose components are all tight.
\end{definition}

## $\mathcal{F}$-weighted limits

The general machinery of [[enriched category]] theory applied to $\mathcal{F}$ gives us a notion of [[weighted limit]].  Note first that an $\mathcal{F}$-enriched *diagram* in an $\mathcal{F}$-category is a diagram of morphisms in which some are required to be tight, and others are not (but could "accidentally" be tight).

In general, a weighted limit of such a diagram in a (strict) $\mathcal{F}$-category is a weighted (strict) [[2-limit]] in its 2-category of loose morphisms, with the property that certain specified projections from the limit object are tight and "jointly detect tightness", in the sense that a morphism into the limit is tight if and only if its composites with all of the specified projections are tight.  Details and examples can be found in ([LS](#LS)).

One of the most important things about $\mathcal{F}$-categories is that they allow us to define the classes of [[rigged limits]], which are the $\mathcal{F}$-weighted limits that are [[created limit|created]] by the forgetful functors from the various $\mathcal{F}$-categories of algebras and strict/pseudo/lax/colax morphisms over a 2-monad (or an $\mathcal{F}$-monad).

### Characterization

Let $\mathbb{F}$ be $\mathcal{F}$ considered as self-enriched.
In ([LS](#LS)) (where all that follows is taken from), it is shown that an $\mathcal{F}$-weight $\Phi:\mathbb{D} \to \mathbb{F}$ is given by the following data:

1. [[2-functors]] $\Phi_\tau : \mathcal{D}_\tau \to \mathbf{Cat}$ and $\Phi_\lambda : \mathcal{D}_\lambda \to \mathbf{Cat}$,
2. a [[2-natural transformation]] $\varphi : \Phi_\tau \to \Phi_\lambda J_{\mathbb{D}}$ whose components are full embeddings (i.e. [[injective-on-objects]], [[fully faithful]] functors)

\begin{tikzcd}
	{\mathcal{D}_\tau} \\
	&& {\mathbf{Cat}} \\
	{\mathcal{D}_\lambda}
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\Phi_\tau}", from=1-1, to=2-3]
	\arrow["{J_{\mathbb{D}}}"', from=1-1, to=3-1]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\Phi_\lambda}"', from=3-1, to=2-3]
	\arrow["\phi"', shift right=4, shorten <=7pt, shorten >=7pt, Rightarrow, from=0, to=1]
\end{tikzcd}

Here $J_\mathbb{D}$ denotes the [[identity-on-objects]], [[faithful]] and [[locally]] [[fully faithful]] inclusion of the tight 2-category associated to $\mathbb{D}$ into its loose 2-category.

Representable weights are easily constructed. Let $S:\mathbb{D} \to \mathbb{A}$ be an $\mathcal{F}$-diagram, i.e. an $\mathcal{F}$-functor.
Any chosen $A \in \mathbb{A}$ induces an $\mathcal{F}$-weight on $\mathbb{D}$ given by

\begin{tikzcd}
	{\mathcal{D}_\tau} & {\mathcal{A}_\tau} \\
	&&& {\mathbf{Cat}} \\
	{\mathcal{D}_\lambda} & {\mathcal{A}_\lambda}
	\arrow["{S_\tau}", from=1-1, to=1-2]
	\arrow["{J_{\mathbb{D}}}"', from=1-1, to=3-1]
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\mathcal{A}_\tau(A,-)}", from=1-2, to=2-4]
	\arrow["{J_{\mathbb{A}}}"{description}, from=1-2, to=3-2]
	\arrow["{S_\lambda}"', from=3-1, to=3-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\mathcal{A}_\lambda(A,-)}"', from=3-2, to=2-4]
	\arrow["{j_\mathbb{A}}"', shift right=4, shorten <=4pt, shorten >=4pt, Rightarrow, from=0, to=1]
\end{tikzcd}

Now a $\Phi$-[[weighted limit]] for $S$, $\lim^\Phi S$, is characterized by the isomorphism
$$\mathbb{A}(A, {\lim}^\Phi S) \cong [\mathbb{D},\mathbb{F}](\Phi, \mathbb{A}(A,S))$$
One can prove (by an easy characterization of the $\mathcal{F}$-category on the right) this amounts to three conditions:

1. $\lim^\Phi S$ is a [[2-limit]] in the 2-category $\mathcal{A}_\lambda$,
2. for any $w \in \Phi_\tau(D)$, the projection $p_D^w : \lim^\Phi S \to S(D)$ is tight,
3. for any $h:A \to \lim^\Phi S$, $h$ is tight as soon as for each $w \in \Phi_\tau(D)$, $p_D^w h$ is tight.

The third condition is succinctly expressed by saying the family $\{p_D^w\}_{D \in \mathbb{D}, w \in \Phi_\tau(D)}$ **jointly detects tightness**.

This characterization of $\mathcal{F}$-weighted limits is Proposition 3.6 in ([LS](#LS)).

## Properties of $\mathcal{F}$

As mentioned above, the [[base of enrichment]] $\mathcal{F}$ is well behaved. For instance, it is [[cartesian closed]] and [[locally finitely presentable category|locally finitely presentable]] (hence [[complete category|complete]] and [[cocomplete category|cocomplete]]). Cartesian closure is proven in [Lack and Shulman](#LS); we establish local finite presentability below.

\begin{proposition}
	$\mathcal{F}$ is locally finitely presentable.
\end{proposition}

\begin{proof}
	Since $\mathbb{CAT}^\to$ is locally finitely presentable, to show that $\mathcal{F}$ is locally finitely presentable, it suffices by Theorem 1.39 of [[Locally Presentable and Accessible Categories]] to show that $\mathcal{F}$ is a [[orthogonal subcategory problem|finite orthogonality class]] in $\mathbb{CAT}^\to$. First, note that, for any category $\mathbb{C}$, a morphism $m \colon X \to Y$ is orthogonal in $\mathbb{C}$ to a morphism $e \colon A \to B$ if and only if $m$ is orthogonal, as an object in $\mathbb{C}^\to$, to the following square.
	\begin{tikzcd}
		A & B \\
		B & B
		\arrow["e", from=1-1, to=1-2]
		\arrow["e"', from=1-1, to=2-1]
		\arrow["{1_B}", from=1-2, to=2-2]
		\arrow["{1_B}"', from=2-1, to=2-2]
	\end{tikzcd}
	It remains to observe that injectivity-on-objects and full faithfulness are both properties of functors captured by orthogonality in $\mathbb{CAT}$.
    - A functor is injective-on-objects if and only if it is orthogonal to the unique functor $\{ * \quad *' \} \to \{ * \}$.
    - A functor is fully faithful if and only if it is orthogonal to the unique identity-on-objects functor $\{ * \quad *' \} \to \{ * \to *' \}$.
\end{proof}

## Related pages

* [[rigged limit]]

* [[F-functor]]

* [[lax F-natural transformation]]

* [[lax F-adjunction]]

The [[1-category]]-theoretic version:

* [[M-categories]] (cf. [[relative categories]]$\;$[as enriched categories](relative+category#AsEnrichedCategories))

## References

$\mathcal{F}$-categories were introduced in the following, where they were called **enhanced 2-categories**:

* {#LS} [[Stephen Lack]] and [[Mike Shulman]], "Enhanced 2-categories and limits for lax morphisms", [arXiv](http://arxiv.org/abs/1104.2111).
 

[[!redirects F-category]]
[[!redirects F-categories]]
[[!redirects strict F-category]]
[[!redirects strict F-categories]]
[[!redirects enhanced 2-categories]]
