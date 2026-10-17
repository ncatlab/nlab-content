
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


\tableofcontents


##Idea

The notion of _abelian category_ is an abstraction of basic properties of the category [[Ab]] of [[abelian groups]], more generally of the category $R$[[Mod]] of [[modules]] over some [[ring]], and still more generally of categories of [[sheaves]] of abelian groups and of modules. It is such that much of the [[homological algebra]] of [[chain complexes]] can be developed inside every abelian category.

The concept of abelian categories is one in a sequence of notions of [[additive and abelian categories]].  

While additive categories differ significantly from [[toposes]], there is an intimate relation between abelian categories and toposes. See _[[AT category]]_ for more on that.

##Definition

Recall the following fact about [[pre-abelian categories]] from [this proposition](pre-abelian+category#DecompositionOfMorphisms), discussed there:

+-- {: .num_prop #DecompositionOfMorphisms}
###### Proposition

Every [[morphism]] $f \colon A\to B$ in a [[pre-abelian category]] has a canonical de-[[composition]]

\[
  \label{PreImageFactorization}
  A
  \overset{\; p \;}{\twoheadrightarrow}
  \coker\big(\ker f\big)
  \xrightarrow{\; \overline{f} \;}
  \ker\big(\coker f\big)
  \xhookrightarrow{\; i \;}  
  B
\]

where: 

* $p$ is a [[cokernel]], hence  an [[epimorphism]], 

* $i$ is a [[kernel]], hence a [[monomorphism]].

=--


+-- {: .num_defn #AbelianCategory}
###### Definition

An **abelian category** is a [[pre-abelian category]] satisfying the following equivalent conditions.

1. For every [[morphism]] $f$, the canonical morphism $\bar{f} \colon coker(ker(f)) \to ker(coker(f))$ (eq:PreImageFactorization) from prop. \ref{DecompositionOfMorphisms} is an [[isomorphism]] (hence providing an [[image]] factorization $A \twoheadrightarrow im(f) \hookrightarrow B$).

1. Every [[monomorphism]] is a [[kernel]] and every [[epimorphism]] is a [[cokernel]].

=--

+-- {: .num_prop}
###### Proposition

These two conditions are indeed equivalent.

=--

+-- {: .proof}
###### Proof

The first condition implies that if $f$ is a [[monomorphism]] then $f \cong \ker(\coker(f))$ (in the category of objects over $B$) so $f$ is a kernel. Dually if $f$ is an [[epimorphism]] it follows that $f \cong coker(ker(f))$. So (1) implies (2).

The converse can be found in, among other places, Chapter VIII of ([MacLane](#MacLane)).

=--


## Properties

### General
 {#PropertiesGeneral}

+-- {: .num_remark}
###### Remark

The notion of abelian category is self-dual: [[opposite category|opposite]] of any abelian category is abelian. 

=--

+-- {: .num_remark #RegularEpisAndMonos}
###### Remark

By the second formulation of the definition \ref{AbelianCategory},  in an abelian category

* every [[monomorphism]] is a [[regular monomorphism]];

* every [[epimorphism]] is a [[regular epimorphism]].

It follows that every abelian category is a _[[balanced category]]_.

=--

\begin{prop}\label{PullbackPreservesEpimorphisms}
  In an [[abelian category]], [[pullback]] preserves [[epimorphisms]] and [[pushout]] preserves [[monomorphisms]].
\end{prop}
Because every abelian category is a [[regular category]]. For an explicit proof see, e.g., [Selick, Prop. 1.3.13](#Selick).




### Factorization of morphisms
 {#FactorizationOfMorphisms}

+-- {: .num_prop}
###### Proposition

In an abelian category every morphism decomposes [[generalized the|uniquely up to a unique isomorphism]] into the composition of an [[epimorphism]] and a [[monomorphism]], via prop \ref{DecompositionOfMorphisms} combined with def. \ref{AbelianCategory}.  

Since by remark \ref{RegularEpisAndMonos} every monic is [[regular monomorphism|regular]], hence [[strong monomorphism|strong]], it follows that $(epi, mono)$ is an [[orthogonal factorization system]] in an abelian category; see at _[[(epi, mono) factorization system]]_.

=--

+-- {: .num_remark}
###### Remark

Some references claim that this property characterizes abelian categories among pre-abelian ones, but it is not clear to the authors of this page why this should be so, although we do not currently have a counterexample; see [this discussion](http://nforum.mathforge.org/discussion/4094/?Focus=33415#Comment_33415).

=--

### Canonical $Ab$-enrichment
 {#CanonicalAbEnrichment}

The [[Ab]]-[[enriched category|enrichment]] of an abelian category need not be specified a priori, this is Prop. \ref{UniquenessOfAbEnrichment} below.

However, in most examples, the $Ab$-enrichment is evident from the start and does not need to be constructed in this way. A similar statement is true for [[additive categories]], although the most natural result in that case gives only enrichment over [[commutative monoids]]., cf. at *[[semiadditive category]]*.

The last point is of relevance in particular for [[infinity-category|higher categorical]] generalizations of additive categories. See for instance [remark 2.14, p. 5](http://www.math.harvard.edu/~lurie/papers/DAG-I.pdf#page=5) of [[Jacob Lurie]]'s *[[Stable Infinity-Categories]]*.


\begin{proposition}
\label{UniquenessOfAbEnrichment}
If a (not necessarily [[pre-additive category|pre-additive]]) [[category]] $C$ has 

1. a [[zero object]], 

1. binary [[Cartesian product|products]] or binary [[coproducts]], 

1. all [[kernels]] and [[cokernels]],

1. the property that every [[monomorphism]] is a [[kernel]] and every [[epimorphism]] is a [[cokernel]] 

   (so that all monos and epis are [[normal monomorphism|normal]]), 

then there is a unique [[Ab]]-[[enriched category|enrichment]] of $C$ and with it $C$ is abelian.

\end{proposition} 
(cf. [Freyd & Scedrov 1990 §1.598](#FreydScedrov1990), and [[Lean]] formalization in [Mathlib.CategoryTheory.Abelian.NonPreadditive](https://leanprover-community.github.io/mathlib4_docs/Mathlib/CategoryTheory/Abelian/NonPreadditive.html))
\begin{proof}
We give a streamlined version of the argument in [Freyd & Scedrov 1990 §1.597-§1.598](#FreydScedrov1990), which proceeds via the notion of *[[exact categories]]* (where the analog of Step 3 (iii) is immediate). The construction of the subtraction morphism $\sigma_B$ (Step 4) and of the addition from it (Step 6) is that of loc. cit. §1.597 (beware of misprints in the proof on p. 93 [there](#FreydScedrov1990): "$x \colon C \to \mathrm{Cok}(\theta)$" should be "$z \colon \cdots$", "$y$ is monic" should be "$y$ is epic", and "forces $y$ to be an isomorphism" should be "forces $\theta$ to be an isomorphism"). 

We write $0$ also for the [[zero morphisms]] $A \to 0 \to B$; these form a two-sided ideal under composition. For [[Cartesian product|binary products]] we write $p_1, p_2$ for the projections, $\langle f, g \rangle$ for the pairing of morphisms, $\Delta_B \coloneqq \langle \mathrm{id}_B, \mathrm{id}_B \rangle \colon B \to B \times B$ for the [[diagonal morphism]], and

$$
  \iota_1 \coloneqq \langle \mathrm{id}_A, 0 \rangle \colon A \longrightarrow A \times B
  \,,
  \;\;\;\;\;\;
  \iota_2 \coloneqq \langle 0, \mathrm{id}_B \rangle \colon B \longrightarrow A \times B
  \,.
$$

**Step 0 (reduction to binary products).** All hypotheses except the second are invariant under passage to the [[opposite category]], while the second turns binary products into binary coproducts and vice versa. The conclusion is invariant as well: $Ab$-enrichments of $C$ are the same as those of $C^{op}$, and $C$ is abelian iff $C^{op}$ is (see [below](#Properties)). Hence it suffices to consider the case that $C$ has binary products, which we assume from now on.

**Step 1 (normal monos and epis).**

(i) If $m$ is the kernel of some morphism $g$, then $m$ is the kernel of its own cokernel $c \coloneqq \mathrm{coker}(m)$: Since $g \circ m = 0$, we have $g = g' \circ c$ for some $g'$, so that $c \circ z = 0$ implies $g \circ z = 0$, whence $z$ factors uniquely through $m$. Dually, every epimorphism, being a cokernel by assumption, is the cokernel of its kernel.

(ii) Every [[split monomorphism]] is a monomorphism, hence by assumption a kernel, hence by (i) the kernel of its cokernel. Dually for split epimorphisms. This applies in particular to $\Delta_B$ and $\iota_1$ (split by $p_1$), to $\iota_2$ (split by $p_2$), and to $p_1$, $p_2$ (split by $\iota_1$, $\iota_2$, respectively).

**Step 2.** The morphism $\iota_1 \colon A \to A \times B$ is a kernel of $p_2$, and $p_2$ is a cokernel of $\iota_1$:
First, $p_2 \circ \iota_1 = 0$, and if $p_2 \circ z = 0$ then $z = \langle p_1 \circ z, 0 \rangle = \iota_1 \circ p_1 \circ z$, uniquely so since $\iota_1$ is mono. Hence $\iota_1 = \mathrm{ker}(p_2)$, and so $p_2 = \mathrm{coker}(\iota_1)$ by Step 1. Symmetrically, $\iota_2 = \mathrm{ker}(p_1)$ and $p_1 = \mathrm{coker}(\iota_2)$.

**Step 3 (equalizers, and a criterion for isomorphisms).**

(i) $C$ has [[equalizers]]: For $f, g \colon A \to B$ let $e \coloneqq \mathrm{ker}\big( \mathrm{coker}(\Delta_B) \circ \langle f, g \rangle \big)$. Since $\Delta_B = \mathrm{ker}\big(\mathrm{coker}(\Delta_B)\big)$ by Step 1, a morphism $z$ into $A$ factors (necessarily uniquely) through $e$ iff $\langle f \circ z, g \circ z \rangle$ factors through $\Delta_B$, hence iff $f \circ z = g \circ z$. So $e$ is an equalizer of $f$ and $g$.

(ii) If $f \colon A \to B$ has vanishing kernel, in that $f \circ z = 0$ implies $z = 0$, then $f$ is a monomorphism:
Let $k \colon P \to A \times A$ be the equalizer of $f \circ p_1$ and $f \circ p_2$ (the [[kernel pair]] of $f$), and write $q_i \coloneqq p_i \circ k$. Since $f \circ p_1 \circ \Delta_A = f \circ p_2 \circ \Delta_A$, there is $s \colon A \to P$ with $k \circ s = \Delta_A$, hence with $q_1 \circ s = \mathrm{id}_A = q_2 \circ s$. Now if $q_1 \circ z = 0$, then $f \circ q_2 \circ z = f \circ q_1 \circ z = 0$, hence $q_2 \circ z = 0$, hence $k \circ z = \langle q_1 \circ z, q_2 \circ z \rangle = 0$, hence $z = 0$, since $k$ is mono. Thus the kernel of the split epimorphism $q_1$ is $0 \to P$, so that, by Step 1, $q_1$ is a cokernel of $0 \to P$, hence an isomorphism, with inverse $s$. Therefore $q_2 = q_2 \circ s \circ q_1 = q_1$. Finally, if $f \circ x = f \circ y$ then $\langle x, y \rangle = k \circ u$ for some $u$, and so $x = q_1 \circ u = q_2 \circ u = y$.

(iii) If $f \colon A \to B$ has vanishing kernel and vanishing cokernel (in that also $t \circ f = 0$ implies $t = 0$), then $f$ is an isomorphism:
By (ii), $f$ is mono, hence by Step 1 a kernel of $\mathrm{coker}(f)$. But $\mathrm{coker}(f) = 0$, and the kernel of a zero morphism out of $B$ is $\mathrm{id}_B$. Since kernels are unique up to unique isomorphism, $f$ is an isomorphism.

**Step 4 (the subtraction morphism).** For any object $B$, let $q \colon B \times B \to Q$ be a cokernel of $\Delta_B$, and consider

$$
  r \coloneqq q \circ \iota_1 \;\colon\; B \longrightarrow Q
  \,.
$$

* $r$ has vanishing kernel: If $r \circ z = 0$, then $\iota_1 \circ z$ factors through $\Delta_B = \mathrm{ker}(q)$ (by Step 1), say as $\iota_1 \circ z = \Delta_B \circ w$. Applying $p_2$ to this equation gives $0 = w$, and then applying $p_1$ gives $z = w = 0$.

* $r$ has vanishing cokernel: If $t \circ r = 0$, then $t \circ q$ vanishes on $\iota_1$ and hence factors through $p_2 = \mathrm{coker}(\iota_1)$ (by Step 2), say as $t \circ q = s \circ p_2$. Then $s = s \circ p_2 \circ \Delta_B = t \circ q \circ \Delta_B = 0$, so that $t \circ q = 0$, and hence $t = 0$, since $q$ is epi.

By Step 3 (iii), $r$ is an isomorphism, and we set

$$
  \sigma_B
  \;\coloneqq\;
  r^{-1} \circ q
  \;\colon\;
  B \times B \longrightarrow B
  \,.
$$

This is a cokernel of $\Delta_B$ which satisfies

$$
  \sigma_B \circ \Delta_B = 0
  \,,
  \;\;\;\;\;\;
  \sigma_B \circ \iota_1 = \mathrm{id}_B
  \,.
$$

(For $C = $ [[Ab]] this is the map $(b_1, b_2) \mapsto b_1 - b_2$.) Moreover, $\sigma$ is natural: For $f \colon A \to B$ we have $\sigma_B \circ (f \times f) = f \circ \sigma_A$. Namely, $\sigma_B \circ (f \times f) \circ \Delta_A = \sigma_B \circ \Delta_B \circ f = 0$, so that $\sigma_B \circ (f \times f) = f' \circ \sigma_A$ for some $f'$, and then

$$
  f'
  = f' \circ \sigma_A \circ \iota_1
  = \sigma_B \circ (f \times f) \circ \iota_1
  = \sigma_B \circ \iota_1 \circ f
  = f
  \,.
$$

**Step 5 (properties of subtraction).** For $x, y \colon A \to B$ define

$$
  x - y
  \;\coloneqq\;
  \sigma_B \circ \langle x, y \rangle
  \;\colon\;
  A \longrightarrow B
$$

(the notation is justified by Step 6). Then, for all composable morphisms $x, y, z, w$:

1. $x - 0 = x$, since $\langle x, 0 \rangle = \iota_1 \circ x$;

1. $x - x = 0$, since $\langle x, x \rangle = \Delta_B \circ x$;

1. $z \circ (x - y) = z \circ x - z \circ y$, by naturality of $\sigma$ (Step 4) and since $(z \times z) \circ \langle x, y \rangle = \langle z \circ x, z \circ y \rangle$;

1. $(x - y) \circ w = x \circ w - y \circ w$, since $\langle x, y \rangle \circ w = \langle x \circ w, y \circ w \rangle$.

From this follows the *middle-two interchange law*: For $u, v, x, y \colon A \to B$ we have

$$
  (u - v) - (x - y)
  \;=\;
  (u - x) - (v - y)
  \,.
$$

To see this, observe first that for $a, b \colon A \to D$ and $c, d \colon D \to B$, items 3 and 4 give

$$
  \begin{aligned}
    (c \circ a - d \circ a) - (c \circ b - d \circ b)
    & =
    (c - d) \circ a - (c - d) \circ b
    \\
    & =
    (c - d) \circ (a - b)
    \\
    & =
    c \circ (a - b) - d \circ (a - b)
    \\
    & =
    (c \circ a - c \circ b) - (d \circ a - d \circ b)
    \,,
  \end{aligned}
$$

and then specialize to $D = B \times B$, $a = \langle u, v \rangle$, $b = \langle x, y \rangle$, $c = p_1$, $d = p_2$.

**Step 6 (the abelian group structure).** Define

$$
  x + y
  \;\coloneqq\;
  x - (0 - y)
  \,.
$$

Then $x + 0 = x - 0 = x$, by items 2 and 1 of Step 5, and

$$
  0 + x
  \;=\;
  0 - (0 - x)
  \;=\;
  (x - x) - (0 - x)
  \;=\;
  (x - 0) - (x - x)
  \;=\;
  x - 0
  \;=\;
  x
  \,,
$$

by items 1, 2 and the interchange law. Applying the interchange law three times gives

$$
  \begin{aligned}
    (u + v) + (x + y)
    & =
    \big( u - (0 - v) \big) - \Big( 0 - \big( x - (0 - y) \big) \Big)
    \\
    & =
    (u - 0) - \Big( (0 - v) - \big( x - (0 - y) \big) \Big)
    \\
    & =
    (u - 0) - \Big( (0 - x) - \big( v - (0 - y) \big) \Big)
    \\
    & =
    \big( u - (0 - x) \big) - \Big( 0 - \big( v - (0 - y) \big) \Big)
    \\
    & =
    (u + x) + (v + y)
    \,.
  \end{aligned}
$$

Setting here $u = y = 0$ shows that $+$ is commutative, and setting $v = 0$ shows that it is associative (this is the [[Eckmann-Hilton argument]]). Moreover, $(0 - x) + x = (0 - x) - (0 - x) = 0$, so that every $x$ has the inverse $-x \coloneqq 0 - x$ (and $x + (-y) = x - y$, by the formula for $0 + x$ above). Hence each hom-set $C(A,B)$ is an [[abelian group]], whose neutral element is the zero morphism. Finally, composition is bilinear, since by items 3 and 4 of Step 5

$$
  z \circ (x + y)
  \;=\;
  z \circ x - \big( z \circ 0 - z \circ y \big)
  \;=\;
  z \circ x - \big( 0 - z \circ y \big)
  \;=\;
  z \circ x + z \circ y
  \,,
$$

and similarly $(x + y) \circ w = x \circ w + y \circ w$. This is an $Ab$-enrichment of $C$.

**Step 7 (abelianness).** With respect to this enrichment, $\iota_1 \circ p_1 + \iota_2 \circ p_2 = \mathrm{id}_{A \times B}$, as seen by composing with $p_1$ and with $p_2$. Together with $p_1 \circ \iota_1 = \mathrm{id}_A$, $p_2 \circ \iota_2 = \mathrm{id}_B$ and $p_2 \circ \iota_1 = 0$, $p_1 \circ \iota_2 = 0$, this means that binary products are [[biproducts]], so that $C$ is an [[additive category]], hence (having kernels and cokernels) a [[pre-abelian category]] in which, by assumption, every monomorphism is a kernel and every epimorphism is a cokernel. Therefore $C$ is abelian, by the second condition in the definition [above](#Definition).

**Step 8 (uniqueness).** Let $+'$ be any $Ab$-enrichment of $C$. Its neutral elements are the zero morphisms, because $C(A,0)$ is a singleton, so that $A \to 0$ is neutral, and composition is bilinear. Consider

$$
  \nabla \coloneqq p_1 + p_2
  \,,
  \;\;\;\;\;\;
  \nabla' \coloneqq p_1 +' p_2
  \;\;\;
  \colon
  \;
  B \times B \longrightarrow B
  \,.
$$

By bilinearity of composition we have, for $x, y \colon A \to B$,

$$
  x + y = \nabla \circ \langle x, y \rangle
  \,,
  \;\;\;\;\;\;
  x +' y = \nabla' \circ \langle x, y \rangle
  \,,
$$

as well as $\nabla' \circ \iota_1 = \mathrm{id}_B +' 0 = \mathrm{id}_B$ and similarly $\nabla' \circ \iota_2 = \mathrm{id}_B$. Hence, using Step 7,

$$
  \nabla'
  \;=\;
  \nabla' \circ \big( \iota_1 \circ p_1 + \iota_2 \circ p_2 \big)
  \;=\;
  \nabla' \circ \iota_1 \circ p_1 + \nabla' \circ \iota_2 \circ p_2
  \;=\;
  p_1 + p_2
  \;=\;
  \nabla
  \,,
$$

and therefore $x +' y = x + y$.
\end{proof}



### Relation to exactness properties of toposes
 {#RelationToToposes}

The [[exactness properties]] of abelian categories have many features in common with exactness properties of [[toposes]] or of [[pretoposes]]. 

[Freyd (1999)](AT+category#Freyd99) gave a sharp description of the properties shared by these categories, introducing a new concept called _[[AT categories]]_ (for "abelian-topos"), and showing convincingly that the difference between the A and the T can be concentrated precisely in the difference of the behavior of the initial object. 

### Embedding theorems
 {#EmbeddingTheorems}

Not every [[abelian category]] is a [[concrete category]] such as [[Ab]] or $R$[[Mod]]. But for many proofs in [[homological algebra]] it is very convenient to have a concrete abelian category, for that allows one to check the behaviour of morphisms on actual _elements_ of the sets underlying the [[objects]].

The following _embedding theorems_, however, show that under good conditions an abelian category can be _embedded_ into [[Ab]] as a [[full subcategory]] by an [[exact functor]], and generally can be embedded this way into $R Mod$, for some ring $R$. This is the celebrated _[[Freyd-Mitchell embedding theorem]]_  discussed [below](#FreydMitchellEmbedding).

This implies for instance that proofs about [[exact sequence|exactness of sequences]] in an abelian category can always be obtained by a naive argument on elements -- called a "[[diagram chasing|diagram chase]]" -- because that does hold true after such an embedding, and the exactness of the embedding means that the notion of exact sequences is preserved by it.

Alternatively, one can reason with [[generalized elements]] in an abelian category, without explicitly embedding it into a larger concrete category, see at _[[element in an abelian category]]_. But under suitable conditions this comes down to working subject to an embedding into $Ab$, see the discussion at _[Embedding into Ab](#EmbeddingIntoAb)_ below.

#### Counterexamples

First of all, it's easy to see that not every abelian category is equivalent to $R$[[Mod]] for some ring $R$.  The reason is that $R Mod$ has all [[small category]] [[limits]] and [[colimits]].  For a [[Noetherian ring]] $R$ the category of [[finitely generated module|finitely generated]] $R$-modules is an abelian category that lacks these properties.


#### Embedding into $Ab$
 {#EmbeddingIntoAb}

(...)

([Bergman 1974](#Bergman))

(...)

#### Freyd-Mitchell embedding into $R Mod$
 {#FreydMitchellEmbedding}

+-- {: .num_thm}
###### Mitchell's Embedding Theorem

Every small abelian category admits a [[full functor|full]], [[faithful functor|faithful]] and [[exact functor|exact]] functor to the category $R Mod$ for some ring $R$.

=--

+-- {: .proof}
###### Proof
This result can be found as Theorem 7.34 on page 150 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=176).  His terminology is a bit outdated, in that he calls an abelian category "fully abelian" if admits a full and faithful exact functor to a category of $R$-modules.  See also the [Wikipedia article](http://en.wikipedia.org/wiki/Mitchell%27s_embedding_theorem) for the idea of the proof.
=--

For more see at _[[Freyd-Mitchell embedding theorem]]_.

We can also characterize which abelian categories _are_ equivalent to a category of $R$-modules:

+-- {: .num_theorem}
###### Theorem
Let $C$ be an abelian category.  If $C$ has all [[small category|small]] [[coproducts]] and has a [[compact object|compact]] [[projective object|projective]] [[generator]], then $C \simeq R Mod$ for some ring $R$.  In fact, in this situation we can take $R = C(x,x)^{op}$ where $x$ is any compact projective generator.   Conversely, if $C \simeq R Mod$, then $C$ has all small coproducts and $x = R$ is a compact projective generator.
=--

+-- {: .proof}
###### Proof
This theorem, minus the explicit description of $R$, can be found as Exercise F on page 103 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=132).
The first part of this theorem can also be found as Prop. 2.1.7. of Victor Ginzburg's [Lectures on noncommutative geometry](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=4).  Conversely, it is easy to see that $R$ is a compact projective generator of $R Mod$. 
=--

One can characterize functors between categories of $R$-modules that are either (isomorphic) to functors of the form $B \otimes_R -$ where $B$ is a bimodule or those which look as Hom-modules. For the characterization of the tensoring functors see [[Eilenberg-Watts theorem]]. 

Going still further one should be able to obtain a nice theorem describing the image of the embedding of the weak 2-category of

* rings
* bimodules
* bimodule homomorphisms

into the strict 2-category of 

* abelian categories
* right exact functors
* natural transformations.

For more discussion see the [$n$-Cafe](http://golem.ph.utexas.edu/category/2007/08/questions_about_modules.html).

## Examples

* Of course, [[Ab]] is abelian, 

* the [[category of modules|category $R$Mod of (left) modules]] over any [[ring]] $R$ is abelian

* Therefore in particular the category [[Vect]] of vector spaces over any field is an abelian category

* The full subcategory of $R$Mod whose objects are the Noetherian left $R$-modules is abelian, since it contains any submodule or quotient module of any of its objects (see Theorem 2.3.8 p.103 of Berrick and Keating in the textbook references below).

* Similarly, the full subcategory of $R$Mod whose objects are the Artinian left $R$-modules is abelian, since it contains any submodule or quotient module of any of its objects (loc. cit.).

* Also similarly, the full subcategory of $R$Mod whose objects are the Artinian semisimple modules is abelian, since it contains any submodule or quotient module of any of its objects (loc. cit.) . 

* as is the [[category of representations]] of a [[group]] (e.g. [here](https://unapologetic.wordpress.com/2008/12/15/the-category-of-representations-is-abelian/))

* The [[category of sheaves|category of]] [[sheaves of abelian groups]] on any [[site]] is abelian.


Counter-examples:

* The category of [[torsion subgroup|torsion-free]] abelian groups is pre-abelian, but not abelian: the monomorphism $2:\mathbb{Z}\to\mathbb{Z}$ is not a kernel.


## Related concepts

* [[additive and abelian categories]]

* [[abelian subcategory]]

* [[Deligne tensor product of abelian categories]]

* [[Grothendieck category]]

* [[pseudo-abelian category]]

* [[quasi-abelian category]]

* [[semi-abelian category]]

* [[length of an object]]

## References

Possibly the first reference on abelian categories, then still called _exact categories_: 

* D. A. Buchsbaum: _Exact categories and duality_, Transactions of the American Mathematical Society **80** 1 (1955) 1--34 &lbrack;[jstor:1993003](http://www.jstor.org/stable/1993003)&rbrack;

Further foundations of the theory were then laid in 

* [[Alexander Grothendieck]]: _[[Tohoku|Sur quelques points d'algèbre homologique]], T&#244;hoku Math. J. **9** 2--3 (1957)

Other classic references:

* [[Pierre Gabriel]], *[[Des Catégories Abéliennes]]*, Bulletin de la Société Mathématique de France **90** (1962) 323-448 &lbrack;[numdam:BSMF_1962__90__323_0](http://www.numdam.org/item?id=BSMF_1962__90__323_0)&rbrack;

* {#Freyd64} [[Peter Freyd]]: _Abelian Categories -- An Introduction to the theory of functors_, Harper and Row, New York (1964), Reprints in Theory and Applications of Categories **3** (2003)  &lbrack;[tac:tr3](http://www.emis.de/journals/TAC/reprints/articles/3/tr3abs.html), [pdf](https://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf)&rbrack;
  

Textbook accounts:

* [[Nicolae Popescu]], _[[Abelian categories with applications to rings and modules]]_, London Math. Soc. Monographs __3__, Academic Press (1973) &lbrack;[MR0340375](http://www.ams.org/mathscinet-getitem?mr=0340375)&rbrack;

* [[Saunders MacLane]], Chapter VIII of: _[[Categories for the Working Mathematician]]_ (1978)

* {#FreydScedrov1990} [[Peter Freyd]], [[Andre Scedrov]]: *Categories*, chapter one of: *[[Categories, Allegories]]*, Mathematical Library **39**, North-Holland (1990) &lbrack;[ISBN 978-0-444-70368-2](https://www.elsevier.com/books/categories-allegories/freyd/978-0-444-70368-2), [math-library:vol/39/suppl/C](https://www.sciencedirect.com/bookseries/north-holland-mathematical-library/vol/39/suppl/C), [ark:/13960/s2mnkcjwggx](https://archive.org/details/categoriesallego0000frey)&rbrack;



* A. J. Berrick and M. E. Keating, *Categories and Modules, with K-theory in View*, Cambridge Studies in Advanced Mathematics **67**, Cambridge University Press (2000)

* [[Masaki Kashiwara]], [[Pierre Schapira]], Section 8 of: *[[Categories and Sheaves]]*, Grundlehren der Mathematischen Wissenschaften **332**, Springer (2006) &lbrack;[doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)&rbrack;

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], Chapter 1 of: *Tensor Categories*, AMS Mathematical Surveys and Monographs **205** (2015) &lbrack;[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)&rbrack;

Further review:

* Rankey Datta, _An introduction to abelian categories_  (2010) ([pdf](http://www-bcf.usc.edu/~lauda/teaching/rankeya.pdf))

* {#Selick} Paul Selick, *Homological Algebra Notes* ([pdf](www.math.toronto.edu/selick/mat1352/1350notes.pdf),[[Selick_HomologicalAlgebra.pdf:file]])


On [[diagram chasing]] and [[elements in an abelian category]]:

* {#Bergman} [[George Bergman]], _A note on abelian categories -- translating element-chasing proofs, and exact embedding in abelian groups_ (1974) &lbrack;[pdf](http://math.berkeley.edu/~gbergman/papers/unpub/elem-chase.pdf), [[Bergman-ElementChasing.pdf:file]]&rbrack;
 

For more discussion of the _[[Freyd-Mitchell embedding theorem]]_ see there.

A proof that $R Mod$ is an abelian category: 

* Rankeya Datta, _The category of modules over a commutative ring and abelian categories_ ([pdf](http://www.math.columbia.edu/~ums/pdf/Rankeya_R-mod_and_Abelian_Categories.pdf))

A [[2-monad|2-monadic]] characterization of abelian categories:

* [[Martin Markl]], Dominik Trnka: *Lax Distributivity and a Characterization of Abelian Categories* &lbrack;[arXiv:2607.25740](https://arxiv.org/abs/2607.25740)&rbrack;


A discussion about to which extent abelian categories are a general context for [[homological algebra]] is archived at nForum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2052&Focus=17680#Comment_17680).

See also the [catlist 1999 discussion](http://www.mta.ca/~cat-dist/catlist/1999/atcat) on comparison between abelian categories and topoi ([[AT categories]]).

Formalization of abelian categories as [[univalent categories]] in [[univalent foundations of mathematics]] ([[homotopy type theory]]):

* [[unimath]], *Abelian Categories* &lbrack;[UniMath.CategoryTheory.Abelian](https://unimath.github.io/doc/UniMath/4dd5c17/UniMath.CategoryTheory.Abelian.html)&rbrack;

Generalization of abelian categories to [[(n,1)-categories]]:

* Nao Mochizuki, _Higher-dimensional generalization of abelian categories via DG Categories_ &lbrack;[arXiv:2501.06955](https://arxiv.org/abs/2501.06955)&rbrack;

[[!redirects abelian categories]]
[[!redirects Abelian category]]
