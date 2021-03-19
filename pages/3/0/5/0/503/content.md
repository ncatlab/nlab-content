
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The concept of _[[Cauchy-complete space|Cauchy completeness]]_, ordinarily thought of as applying to [[metric spaces]], was vastly generalized by [[Bill Lawvere]] in his influential paper _[Metric spaces, generalized logic, and closed categories](#Lawvere)_. It is now seen by [[category theory|category theorists]] as a concept of [[enriched category theory]], with close ties to the concept of [[Morita equivalence]] in the theory of [[modules]]. In category theory one also speaks of _[[idempotent completion|idempotent completeness]]_.

The basic idea is that the Cauchy [[completion]] of a [[category]] is the closure of a category under what are called "[[absolute limit]]s", i.e., those [[limit]]s that are preserved by any [[functor]] whatsoever. Equivalently, the Cauchy completion is the closure with respect to [[absolute colimit]]s. If $C$ is [[small category|small]], the Cauchy completion $\bar{C}$ of $C$ lies between $C$ and its "[[free cocompletion]]", aka [[presheaf category]]

$$C \hookrightarrow \bar{C} \hookrightarrow Set^{C^{op}}$$ 

and consists of the presheaves $F$ dubbed [[tiny object|tiny]] by Lawvere, meaning those presheaves which are [[connected object|connected]] and [[projective object|projective]]: the functor 

$$hom_{Set^{C^{op}}}(F, -): Set^{C^{op}} \to Set$$ 

preserves small [[coproducts]] and [[coequalizers]]. All of these concepts generalize straightforwardly to the context of general $V$-[[enriched category theory|enriched categories]], where $V$ is a [[complete category|complete]], [[cocomplete category|cocomplete]], [[symmetric monoidal category|symmetric]] [[monoidal closed category]]. 

Lawvere defines a **point** of the Cauchy completion of a small $V$-category $C$ to be a $V$-enriched [[bimodule]] $p: \mathbf{1} \to C$ (in other words, a $V$-functor $\mathbf{1} \to V^{C^{op}}$) for which there is a bimodule $q: C \to \mathbf{1}$ right adjoint to $p$ (in the [[bicategory]] of enriched bimodules, see [[profunctor]]), where $\mathbf{1}$ is the unit $V$-category. Thus points of the Cauchy completion are certain $V$-enriched presheaves $p: C^{op} \to V$, and together form a $V$-category called the **Cauchy completion** whose [[hom-object|hom]]s are the presheaf homs. It is denoted $\bar{C}$. 

As we will explain in more detail below, [[representable functor|representable presheaves]] belong to the Cauchy completion, and so the [[Yoneda embedding]] of $C$ factors through a full embedding 

$$i: C \to \bar{C}$$ 

and we say the $V$-category $C$ is **Cauchy-complete** if this embedding is an equivalence. We work through a few examples in the following section. 


## In ordinary category theory
 {#InOrdinaryCategoryTheory}

### In terms of splitting of idempotents

+-- {: .num_defn #CauchyCompletionByRetractsOfRepresentablePresheaves}
###### Definition

For $C$ a [[small category]] write 

$$
  \overline{C} \hookrightarrow [C^{op}, Set]
$$

for the [[full subcategory]] of the [[category of presheaves]] on $C$ on the 
[[retract]]s of [[representable functor]].

This $\overline{C}$ is called the **Cauchy completion** of $C$.

=--

For instance ([BorceuxDejean, below theorem 1](#BorceuxDejean)).

+-- {: .num_theorem}
###### Theorem

The Cauchy completion $\overline{C}$ satisfies the following properties

1. $\overline{C}$ is a [[small category]];

1. $C$ is a [[full subcategory]] $C \hookrightarrow \overline{C}$;

1. every [[idempotent]] in $\overline{C}$ [[split idempotent|splits]];

1. the inclusion $C \hookrightarrow \overline{C}$ is an [[equivalence of categories]] precisely if already every [[idempotent]] in $C$ splits;

1. there is an [[equivalence of categories]]

   $$
     [C^{op}, Set] \simeq [\overline{C}^{op}, Set]
     \,.
   $$

=--

This appears for instance as ([BorceuxDejean, theorem 1](#BorceuxDejean)).

+-- {: .proof}
###### Proof

$\overline{C}$ is small because $[C^{op}, Set]$ is a [[well-powered category]]. It contains $C$ as a [[full subcategory]] because the [[Yoneda embedding]] is a [[full and faithful functor]]. Every idempotent splits in $\overline{C}$ because it does so in $[C^{op}, Set]$ and because the composite of two retractions is a retraction.

A retract of a representable $y(c) \in [C^{op}, Set]$ induces an idempotent on $y(c)$ and hence by the [[Yoneda lemma]] an idempotent on $c \in C$. If $C$ is already idempotent complete, this splits and produces a retraction of $c$ in $C$ and hence of $y(C)$ in $[C^{op}, Set]$. Since this is necessarily isomorphic to the original retraction, we find that every retract of the representable $y(c)$ is itself representable, therefore $C \simeq \overline{C}$ in this case.

=--

### In terms of tiny objects
 {#InTermsOfTinyObjects}

+-- {: .num_prop #CauchyComplIsFullSubcatOnTinyObjects}
###### Proposition

The Cauchy completion $\overline{C}$ is equivalently the [[full subcategory]] of $[C^{op}, Set]$ on the [[tiny object]]s ("small projective objects"). 

=--

This appears for instance as ([BorceuxDejean, prop. 2](#BorceuxDejean)).

### In terms of absolute colimits
 {#InTermsOfAbsoluteColimits}

+-- {: .num_prop}
###### Proposition

The following conditions are equivalent for a [[small category]] $C$.

1. $C$ is Cauchy complete;

1. $C$ has all small [[absolute colimit]]s.

=--


### In terms of profunctors
 {#InOrdinaryCatTheoryByProfunctors}

We discuss Cauchy completion of [[small categories]] in terms of [[profunctor]]s.

Write $*$ for the terminal category (single object, single morphism). Let $C$ be a [[small category]]

+-- {: .num_remark}
###### Remark

The category $C$ is equivalent to the [[functor category]] out of the point

$$
  C \simeq Func(*,C)
  \,.
$$

Its [[category of presheaves]] is equivalent to the profunctor category

$$
  [C^{op}, Set] \simeq Profunc(*, C)
  \,.
$$

In these terms the [[Yoneda embedding]] $C \hookrightarrow [C^{op}, Set]$ is the canonical inclusion

$$
  Func(*,C) \hookrightarrow Profunc(*,C)
  \,.
$$

Accordingly the Cauchy completion, def. \ref{CauchyCompletionByRetractsOfRepresentablePresheaves} is a 
[[full subcategory]] of the profunctor category

$$
  \overline{C} \hookrightarrow Profunc(*,C)
  \,.
$$

=--

+-- {: .num_prop #CuachyCompByLeftAdjointProfunctor}
###### Proposition

A [[profunctor]] $F : * &#8696; C$ belongs to $\overline{C}$ precisely if it has a [[right adjoint]] in [[Prof]].

=--

This appears for instance as ([BorceuxDejean, prop. 4](#BorceuxDejean)).

+-- {: .num_theorem}
###### Theorem

For a [[small category]] $C$, the following are equivalent

1. $C$ is Cauchy complete;

1. a profunctor $* &#8696; C$ has a [[right adjoint]] precisely if it is a functor;

1. for every [[small category]] $A$ a profunctor $A &#8696; C$ has a [[right adjoint]] precisely if it is a functor;

=--

This appears for instance as ([BorceuxDejean, theorem 2](#BorceuxDejean)).


### In terms of essential geometric morphisms
 {#InOrdinaryCatTheoryByEssGeomMorphisms}

In the context of [[topos theory]] we say, for $C$ [[small category]], that an [[adjoint triple]] of [[functor]]s 

$$
  Set \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
  [C,Set]
$$

is an [[essential geometric morphism]] of [[topos]]es $f : Set \to [C,Set]$; or an **[[point of a topos|essential point]]** of $[C,Set]$.

By the [[adjoint functor theorem]] this is equivalently simply a single functor $f^* : [C, Set] \to Set$ that preserves all small [[limit]]s and [[colimit]]s. Write

$$
  Topos_{ess}(Set,[C,Set]) 
   \simeq 
  LRFunc([C,Set], Set)
   \subset 
  Func([C,Set], Set)
$$

for the [[full subcategory]] of the [[functor category]] on functors that have a [[left adjoint]] and a [[right adjoint]].

+-- {: .num_prop #CauchyCompletionByEssentialPoints}
###### Proposition

For $C$ a [[small category]] there is an [[equivalence of categories]]

$$
  \overline{C} \simeq Topos_{ess}(Set, [C,Set])^{op}
$$

of its Cauchy completion, def. \ref{CauchyCompletionByRetractsOfRepresentablePresheaves}, with the category of essential points of $[C,Set]$.

=--

+-- {: .proof}
###### Proof

We first exhibit a [[full subcategory|full inclusion]] $Topos_{ess}(Set,[C,Set])^{op} \hookrightarrow \overline{C}$.

So let $Set \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}} [C,Set]$ be an [[essential geometric morphism]]. Then because $f_!$ is [[left adjoint]] and thus preserves all small [[colimits]] and because every [[set]] $S \in Set$ is the colimit over itself of the singleton set we have that

$$
  f_! S \simeq \coprod_{s \in S} f_!(*)
$$

is fixed by a choice of [[copresheaf]]

$$
  F := f_!(*) \in [C, Set]
  \,.
$$

The $(f_! \dashv f^*)$-[[adjunction]] [[isomorphism]] then implies that for all $H \in [C,Set]$ we have

$$
  f^* H \simeq Set(*, f^* H) \simeq [C,Set](f_! *, H)
  \simeq [C,Set](F,H)
  \,.
$$

naturally in $H$, and hence that

$$
  f^*(-) \simeq [C,Set](F,-) : Set \to [C,Set]
  \,.
$$

By assumption this has a further right adjoint $f_\ast$ and hence preserves all [[colimits]]. By the discussion at [[tiny object]] it follows that $F \in [C,Set]$ is a tiny object. By prop. \ref{CauchyComplIsFullSubcatOnTinyObjects} this means that $F$ belongs to $\overline{C} \subset [C,Set]$.

A morphism $f \Rightarrow g$ between [[geometric morphisms]] $f,g : Set \to [C,Set]$ is a [[geometric transformation]], which is a [[natural transformation]] $f^* \Rightarrow g^*$, hence by the above a natural transformation $[C,Set](F,-) \Rightarrow [C,Set](G,-)$. By the [[Yoneda lemma]] these are in bijection with morphisms $G \to H$ in $[C,Set]$. This gives the full inclusion $Topos_{ess}(Set,[C,Set])^{op} \subset \overline{C}$.

The converse inclusion is now immediate by the same arguments: since the objects in $\overline{C}$ are precisely the [[tiny object]]s $F \in [C,Set]$ each of them corresponds to a functor $[C,Set](F,-) : [C,Set] \to Set$ that has a [[right adjoint]]. Since this generally also has a left adjoint, it is the [[inverse image]] of an essential geometric morphism $f : Set \to [C,Set]$.

=--

Write $Cat_{Cauchy} \hookrightarrow$ [[Cat]] for the [[full sub-2-category]]
of [[Cat]] on the Cauchy-complete categories.

+-- {: .num_prop}
###### Proposition

The 2-category of Cauchy complete categories is a 
[[coreflective subcategory|coreflective]] [[full sub-2-category]] of [[Topos]] with essential geometric morphisms

$$
  Cat_{Cauchy} \hookrightarrow Topos_{ess}
$$

exhibited by the [[2-adjunction]]

$$
  ([-,Set]
  \dashv
  Topos_{ess}(Set,-)
  )

  :
  Topos_{ess}
   \stackrel{\overset{Cat_{Cauchy}(-,Set)}{\hookleftarrow}}{\underset{Topos_{ess}(Set,-)}{\to}}
  Cat_{Cauchy}
  \,.
$$

=--

+-- {: .proof}
###### Proof

We first claim that when working with all categories
instead of just the Cauchy-complete categories 
there is a [[2-adjunction]]

$$
  ([-,Set]
  \dashv
  Topos_{ess}(Set,-)
  )
  :
  Topos_{ess}
   \stackrel{\overset{[-,Set]}{\leftarrow}}{\underset{Topos_{ess}(Set,-)}{\to}}
  Cat
  \,.
$$

This is exhibited by the following [[equivalence of categories|equivalence]]
of [[hom-categories]]

$$
  \begin{aligned}
    Func(C, Topos_{ess}(Set, E))
     & \simeq
    Func(C, LRFunc(E, Set))
    \\
     & \simeq
    LRFunc(E, Func(C,Set)) =: LRFunc(E, [C,Set])
    \\
     & \simeq
    Topos_{ess}([C,Set], E)
  \end{aligned}
$$

[[natural equivalence|natural]] in $C \in Cat$ and $E \in Topos$. Here

* the first equivalence is by definition of [[essential geometric morphism]];

* the second equivalence follows by observing that limits and colimits in presheaf categories are computed objectwise;

* the third equivalence is again the definition of essential geometric morphisms.

Now by prop. \ref{CauchyCompletionByEssentialPoints} we have that the components of the
[[unit of an adjunction|unit]] of this adjunction

$$
  C \to Topos_{ess}(Set,[C,Set])
$$

are [[equivalence of categories|equivalences]] precisely if $C$ is 
Cauchy-complete. This means that restricted along 
$Cat_{Cauchy} \hookrightarrow Cat$ the adjunction exhibits a coreflective embedding.

=--


## In enriched category theory
 {#InEnrichedCategoryTheory}

We discuss Cauchy completion in $\mathcal{V}$-[[enriched category]] theory, for $\mathcal{V}$ a [[closed category|closed]] [[symmetric monoidal category]] with all [[limits]] and [[colimits]]. The discussion in ordinary category theory [above](InOrdinaryCategoryTheory) is the special case where $\mathcal{V} := $ [[Set]].

The key to the enriched version is the reformulation of ordinary Cauchy completion in terms of [[profunctors]] as discussed [above](InOrdinaryCatTheoryByProfunctors). These have an immediate generalization to enriched category theory, and so one takes this formulation as the definition.

As before, we have

+-- {: .num_remark}
###### Remark

Every small $\mathcal{V}$-category $C$ is equivalent to the $\mathcal{V}$-[[enriched functor category]] 

$$
  C \simeq \mathcal{V}Func(I,C)
  \,,
$$

where $I$ is the $\mathcal{V}$-category with a single [[object]] $*$ and $I(*,*) = I_{\mathcal{V}}$, the tensor unit in $\mathcal{V}$.

Also, 

$$
  [C^{op}, \mathcal{V}] \simeq \mathcal{V}Profunc(I, C)
$$

and the canonical $\mathcal{V}$-[[enriched functor]]

$$
  \mathcal{V}Func(I,C) \hookrightarrow \mathcal{V}Profunc(I,C)
$$

is the enriched [[Yoneda embedding]].

=--

+-- {: .num_defn}
###### Definition

For $C$ a small $\mathcal{V}$-[[enriched category]], the **Cauchy completion** of $C$ is the full $\mathcal{V}$-subcategory 

$$
  \overline{C} \hookrightarrow \mathcal{V}Profunc(I,C)
$$

on those [[profunctor]]s with a [[right adjoint]] in $\mathcal{V}$[[Prof]].

=--


## Examples 

* When $\mathcal{V} = \mathbf{Set}$, a $\mathcal{V}$-category is an ordinary category. The Cauchy completion of an ordinary category is its _idempotent completion_, or [[Karoubi envelope]]. This also holds when $\mathcal{V} = \mathbf{Cat}$ or $\mathcal{V} = \mathbf{sSet}$, or more generally whenever $\mathcal{V}$ is a cartesian [[cosmos]] where the terminal object is [[tiny]].

* When $\mathcal{V} = [0,\infty]$ is the extended nonnegative reals ordered by $\geq$ and with $+$ as monoidal product, $\mathcal{V}$-categories are generalized metric spaces. The Cauchy completion is the usual completion under _Cauchy sequences_.

* When $\mathcal{V} = \mathbf{Ab}$ is abelian groups, a $\mathcal{V}$-category is a [[pre-additive category]]. The Cauchy completion is the completion under _finite direct sums and idempotent splitting_. Notice that there is also a "sub-Cauchy completion" given by completing just under finite direct sums, which turns a pre-additive category into an [[additive category]].

* When $\mathcal{V} = \mathbf{Ch}$ is [[chain complexes]], a $\mathcal{V}$-category is a [[dg-category]].  Cauchy complete dg-categories are characterized by [Nikolić, Street, and Tendas](#NST2020).

* When $\mathcal{V} = \mathbf{Slat}$ is the category of sup-lattices, a $\mathcal{V}$-category is a locally posetal, [[locally cocomplete bicategory]], i.e. a [[quantaloid]]. The Cauchy completion is some sort of completion under _arbitrary_ sums: it is large even if the original quantaloid is small, and its existence depends on the precise definition we choose of Cauchy completion.

* In the $\infty$-categorical context, we can consider enrichment in the $\infty$-category of [[spectra]]. The Cauchy completion of an $\infty$-category enriched in spectra is its completion under _all finite colimits_.

* Generalizing to bicategorical enrichment, we can construct from a [[site]] $(\mathcal{C}, J)$ a certain bicategory $\mathcal{W}$ such that the Cauchy-complete, symmetric, skeletal $\mathcal{W}$-categories are just the sheaves on $(\mathcal{C}, J)$. Variations on this theme can yield $\mathcal{C}$-indexed categories, stacks, prestacks, or presheaves as Cauchy completions or sub-Cauchy completions for categories enriched in certain bicategories.

Now we look at two examples in more detail: metric spaces and ordinary categories.

### Metric spaces 

We consider first the classical case of [[metric space]]s, but as redefined by Lawvere to mean a category enriched in the [[poset]] $V = ([0, \infty], \geq)$, with [[tensor product]] given by addition. So, to say $X$ is a [[Lawvere metric space]] means that with the set $X$ there is a distance function 

$$d_X = hom_X: X \times X \to [0, \infty]$$ 

such that 

$$d(x, y) + d(y, z) \geq d(x, z), \qquad 0 \geq d(x, x)$$ 

for all $x, y, z$ in $X$. (The associativity and identity axioms are here superfluous since $V$ is a poset.) A $V$-enriched functor $f: X \to Y$ here just means a function from $X$ to $Y$ such that 

$$d_X(x, y) \geq d_Y(f(x), f(y))$$ 

for all $x, y$ in $X$ (again, preservation of composition and of identities is superfluous here), so that $V$-functors are [[short maps]] between metric spaces (Lipschitz maps with constant at most $1$). Finally, a $V$-enriched transformation $f \to g: X \to Y$ in this case boils down to an instance of a property: that 

$$0 \geq d_Y(f(x), g(x))$$ 

for all $x$ in $X$. If $f, g$ are valued in $[0, \infty]$, this just means $f(x) \geq g(x)$ for all $x$. 

A point of the Cauchy completion is an $X$-module $p: \mathbf{1} \to X$, i.e., an enriched functor or short map 

$$p: X^{op} \to [0, \infty]$$ 

for which there is an $X$-module $q: X \to \mathbf{1}$ on the other side, an enriched functor 

$$q: X \to [0, \infty]$$ 

that is [[right adjoint]] to $p$ in the sense of modules. This means there is a unit of the adjunction in the bicategory of modules: 

$$(Id: \mathbf{1} \to \mathbf{1}) \to (\mathbf{1} \overset{p}{\to} X \overset{q}{\to} \mathbf{1})$$ 

and a counit: 

$$(X \overset{q}{\to} \mathbf{1} \overset{p}{\to} X) \to (Id: X \to X)$$ 

Recall now that $Id_X: X \to X$ in the bicategory of modules is the unit bimodule $y_X: X \to V^{X^{op}}$ given by the enriched [[Yoneda embedding]], or in different words, $hom_X = d_X: X^{op} \times X \to [0, \infty]$. Recall also that module composition is defined by a [[coend]] formula for a tensor product. If one now tracks through the definitions, keeping in mind that we are in the very simple case of enrichment in a poset, the unit of the [[adjunction]] $p \dashv q$ boils down to having the property 

$$0 \geq \int^{x \in X} q(x) + p(x) = \inf_{x \in X} q(x) + p(x)$$ 

and the counit boils down to having the property 

$$p(x) + q(y) \geq d_X(x, y)$$ 

To better appreciate what these conditions mean, we point out that $p(x)$ should be thought of as the distance $d_{\bar{X}}(x, p)$ between $x$ and the "ideal point" $p$ in the Cauchy completion $\bar{X}$, and $q(x)$ should be thought of as the companion distance $d_{\bar{X}}(p, x)$. Thus the unit condition above would come down to saying that for every $\varepsilon \gt 0$ there exists $x \in X$ such that 

$$d_{\bar{X}}(p, x) \lt \varepsilon, \, d_{\bar{X}}(x, p) \lt \varepsilon$$ 

and the counit condition imposes a necessary triangle inequality constraint on the distance functions $p$ and $q$, in order that we get an actual Lawvere metric space $\bar{X}$. If $p, p'$ are two points of the Cauchy completion thus defined, then their distance is defined by the usual formula for enriched presheaves: 

$$d(p, p') = \int_{x \in X} \hom_{[0, \infty]}(p(x), p'(x)) = \sup_{x \in X} \max\{0, p'(x) - p(x)\}$$ 

It should be noted that even under the classical definition (where we impose symmetry $d(x, y) = d(y, x)$, separation $d(x, y) \gt 0$ for $x \neq y$, and finiteness $d(x,y) \lt \infty$), this provides an elegant alternative definition of Cauchy completion. In essence, all it is doing is taking the metric closure $\bar{X}$ of the embedding of $X$ into the already complete space of short maps:  

$$y_X: X \to [0, \infty]^{X^{op}}: x \mapsto d_X(-, x)$$ 

The presheaf-hom definition of the distance formula for $\bar{X}$, being manifestly non-symmetric, is not the usual definition of distance in the classical symmetric case. However, if we first symmetrize the distance in $[0, \infty]$: 

$$\sigma d(r, s) = d(r, s) + d(s, r) = \max\{0, s-r\} + \max\{0, r-s\} = |r - s|$$ 

or equivalently

$$\sigma d(r, s) = d(r, s) + d(s, r) = \max(\max\{0, s-r\}, \max\{0, r-s\}) = |r - s|$$ 

then we do retrieve the classical formula 

$$d(p, p') = \int_{x \in X} \sigma d(p(x), p'(x)) = \sup_{x \in X} |p(x) - p'(x)|$$ 

In other words, the completion $\bar{X}$ of a symmetric metric space $X$ as a general (Lawvere) metric space is not necessarily the same as its completion $\sigma\bar{X}$ as a symmetric metric space, but $\sigma\bar{X}$ is the symmetrisation of $\bar{X}$.

### Ordinary ($Set$-enriched) categories 

The analysis of Cauchy complete Lawvere metric spaces contains some of the seeds of what happens in other [[enriched category]] contexts; the case of ordinary [[small category|small categories]], where the enrichment is no longer in a mere [[poset]] but in [[Set]], reflects still more of the phenomena generally associated with Cauchy completions. 

Let $C$ be a [[small category]] and let the [[module]] $p: \mathbf{1} \to C$ be a point of $\bar{C}$, with module $q: C \to \mathbf{1}$ as its [[right adjoint]] in the [[bicategory]] of modules. As [[functor]]s, 

$$p: C^{op} \to Set, \, q: C \to Set$$ 

and the structure of the [[adjunction]] is given by unit and counit maps:  

$$\eta: 1 \to \int^{c \in Ob(C)} q(c) \times p(c), \qquad \varepsilon_{c, d}: p(c) \times q(d) \to C(c, d)$$ 

As we said in the case of metric spaces, $p(c)$ and $q(c)$ measure "distances" = homs: 

$$p(c) \cong Set^{C^{op}}(C(-, c), p), \qquad q(c) \cong Set^{C^{op}}(p, C(-, c))$$ 

The first [[isomorphism]] is an instance of the [[Yoneda lemma]], and the second can be seen as follows. The set $q(c)$ is the [[bimodule]] composite 

$$(\mathbf{1} \overset{c}{\to} C \overset{q}{\to} \mathbf{1})$$ 

where $c$ is shorthand for the module $C(-, c): C^{op} \to Set$; this is just an instance of the [[Yoneda lemma]]: 

$$q \circ_C C(-, c) \overset{def}{=} \int^{d \in C} q(d) \times C(d, c) \overset{Yoneda}{\cong} q(c).$$ 

Now using the adjunction $p \dashv q$, there are, for any set $S$, natural bijections 

$$\frac{\frac{S \to q(c)}{S \to q \circ_C C(-, c)}}{\frac{p \circ_{\mathbf{1}} S \to C(-, c)}{p(-) \times S \to C(-, c)}}$$

and maps in the bottom line are in bijection with maps $S \to Set^{C^{op}}(p, C(-, c))$. Therefore we have a natural bijection 

$$\frac{S \to q(c)}{S \to Set^{C^{op}}(p, C(-, c))}$$ 

and this proves $q(c) \cong Set^{C^{op}}(p, C(-, c))$. 

With these identifications of $q(c)$ and $p(c)$, the unit of the adjunction $p \dashv q$ takes the form 

$$\eta: 1 \to \int^{c} Set^{C^{op}}(p, C(-, c)) \times Set^{C^{op}}(C(-, c), p)$$ 

The [[coend]] above is a quotient of 

$$\sum_c Set^{C^{op}}(p, C(-, c)) \times Set^{C^{op}}(C(-, c), p)$$ 

and hence the unit element $\eta$ is represented by a pair of [[natural transformation|transformation]]s 

$$i: p \to C(-, c), \qquad \pi: C(-, c) \to p$$ 

for some $c$. 

Given that, it is now not hard -- in fact it is fairly tautological -- to verify that on the basis of the triangular equation of the adjunction which says 

$$(p \overset{p \circ \eta}{\to} p \circ q \circ p \overset{\varepsilon}{\to} p) = 1_p,$$ 

that 

$$(p \overset{i}{\to} C(-, c) \overset{\pi}{\to} p) = 1_p$$ 

and so a point $p$ in the Cauchy completion $\bar{C}$ must be a [[retract]] of a [[representable functor|representable]] $C(-, c)$. Spelling this out a little more: the composite 

$$C(-, c) \overset{\pi}{\to} p \overset{i}{\to} C(-, c)$$ 

is an [[idempotent]] represented by a morphism $e: c \to c$ in $C$ (by the Yoneda lemma), and this factorization through $p$ [[split idempotent|splits]] the idempotent $C(-, e)$ in $Set^{C^{op}}$. 

Indeed, the claim is that modules $p: C^{op} \to Set$ in the Cauchy completion are precisely those presheaves on $C$ which arise as [[retract]]s of [[representable functor|representable]]s in $Set^{C^{op}}$, or in other words may be identified with objects of the [[split idempotent|idempotent-splitting]] completion of $C$ (aka the _[[Karoubi envelope]]_ of $C$). Therefore, in the $Set$-enriched case, the Cauchy completion _is_ the idempotent-splitting completion. In particular, representables themselves are points of the Cauchy completion. 

Notice that in a finitely complete category (such as $Set$ or a [[presheaf]] category), idempotents $e: c \to c$ split automatically: just take the equalizer of the pair 

$$c \stackrel{\overset{e}{\to}}{\underset{1}{\to}} c$$ 

For that matter, in any finitely cocomplete category, taking the [[coequalizer]] of the above pair would also split the idempotent. Indeed, we can say that idempotents split in a category iff all equalizers of such pairs exist, iff all coequalizers of such pairs exist. 

Notice that if $C$ and $D$ are categories, then any functor $F: C \to D$ preserves [[retract]]s and therefore splittings of idempotents. Thus, the equalizers above are the sort of limits which are preserved by _any_ functor $F$ whatsoever. They are called **absolute limits** for that reason. For the same reason, the coequalizers above are **absolute colimits**: they are precisely the colimits preserved by any functor whatsoever. 

Pursuing this a bit further: if $F: C^{op} \to Set$ is any functor, then (because idempotents split in $Set$) there is a unique extension $\bar{F}: \bar{C}^{op} \to Set$ of $F$. Therefore we have an equivalence 

$$Set^{C^{op}} \simeq Set^{\bar{C}^{op}}$$ 

and we say that $C$ and $\bar{C}$ are **Morita equivalent**. 


### Of prosets

Every ordinary [[poset]] clearly is Cauchy complete, since the only idempotents are the [[identity morphism]]s. The [[internalization]] of this statement requires some extra assumptions:

+-- {: .num_prop}
###### Proposition

[[internalization|Internal]] to any [[regular category]] every [[poset]]
is Cauchy complete.

=--

This appears as ([Rosolini, prop. 2.1](#Rosolini)).

+-- {: .num_prop}
###### Proposition

[[internalization|Internal to]] any [[exact category]] the Cauchy completion of any [[preorder]] exists and is its [[poset reflection]].

=--

This appears as ([Rosolini, corollary. 2.3](#Rosolini)).

Moreover, the characterization of Cauchy completion by left adjoint profunctors requires the internal [[axiom of choice]]:

+-- {: .num_prop}
###### Proposition

In a given ambient context, the following are equivalent:

1. the [[axiom of choice]] holds;

1. every [[profunctor]] $F : A &#8696; C$ between [[posets]] is an ordinary functor when it has a [[right adjoint]].

=--

For instance ([BorceuxDejean, prop. 5](#BorceuxDejean)).


## Discussion 

_David_: Concerning the result that on Set the terminal F-coalgebra is the Cauchy completion of the initial F-algebra, for certain F, I wonder if we have to factor completions through the metric space completion, as Barr does in <a href="ftp://ftp.math.mcgill.ca/pub/barr/pdffiles/trmclg.pdf">Terminal coalgebras for endofunctors on sets</a>. Perhaps Adamek's work on <a href="http://citeseer.ist.psu.edu/cache/papers/cs/21985/http:zSzzSzwww.iti.cs.tu-bs.dezSzTI-INFOzSzadamekzSzPaper2000-4.pdf/final-coalgebras-are-ideal.pdf">Final Algebras are Ideal Completions of Initial Algebras</a> is more natural.

Does this all tie in with the [[ideal completion]] as <a href="http://golem.ph.utexas.edu/category/2009/08/chasing_around_the_triangle.html">discussed</a> by Awodey where you sum types/sets in a topos into a universal object?

How many kinds of completion are there for an enriched category? I see some may coincide in certain cases. 

If two categories can be Morita equivalent, should this be reflected in the page [[Morita equivalence]]?

## Related concepts

* [[split idempotent]]

* [[Karoubi envelope]]

* [[idempotent complete (infinity,1)-category]]

## References

The notion of Cauchy complete categories was introduced in

* [[Bill Lawvere]], _Metric spaces, generalized logic and closed categories_ Rend. Sem. Mat. Fis. Milano, 43:135&#8211;166 (1973)

  Reprints in Theory and Applications of Categories, No. 1 (2002) pp 1-37 ([tac](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html))
 {#Lawvere}

Surveys are in 

* [[Francis Borceux]] and D. Dejean, _Cauchy completion in category theory_  Cahiers Topologie G&eacute;om. Diff&eacute;rentielle Cat&eacute;goriques, 27:133&#8211;146, (1986) ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_2_133_0))
  {#BorceuxDejean}

* A. Carboni and [[Ross Street]], _Order ideal in categories_ Pacific J. Math., 124:275&#8211;288, 1986.
 {#CarboniStreet}

Further references include for instance

* S. R. Johnson, _Small Cauchy Completions_ , JPAA **62** (1989) pp.35-45.

* R. Walters, _Sheaves and Cauchy complete categories_ , Cahiers Top. Geom. Diff. Cat. 22 no. 3 (1981) 283-286 ([numdam](http://www.numdam.org/item?id=CTGDC_1981__22_3_283_0))

* R. Walters, _Sheaves on sites as Cauchy-complete categories, J. Pure Appl. Algebra 24 (1982) 95-102

* {#NST2020} Branko Nikolić, [[Ross Street]], Giacomo Tendas, _Cauchy completeness for DG-categories_, [arxiv](https://arxiv.org/abs/2012.10157), 2020

Cauchy completion of [[internalization|internal]] [[prosets]] is discussed in 

* G. Rosolini, _A note on Cauchy completeness for preorders_ ([pdf](http://www.disi.unige.it/person/RosoliniG/notccp.pdf))
 {#Rosolini}


[[!redirects Cauchy complete category]]
[[!redirects Cauchy complete categories]]
[[!redirects Cauchy-complete category]]
[[!redirects Cauchy-complete categories]]

[[!redirects Cauchy complete]]
[[!redirects Cauchy-complete]]
[[!redirects Cauchy completeness]]
[[!redirects Cauchy-completeness]]

[[!redirects Cauchy completion]]
[[!redirects Cauchy completions]]
[[!redirects Cauchy-completion]]
[[!redirects Cauchy-completions]]

[[!redirects idempotent complete category]]
[[!redirects idempotent complete categories]]
[[!redirects idempotent-complete category]]
[[!redirects idempotent-complete categories]]
