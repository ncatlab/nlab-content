#Contents#
* automatic table of contents goes here
{:toc}


#Idea and definition#

The concept of Cauchy completeness, ordinarily thought of as applying to [[metric space]]s, was vastly generalized by [[Bill Lawvere]] in his influential paper "Metric spaces, generalized logic, and closed categories". It is now seen by [[category|theory|category theorist]s as a concept of [[enriched category theory]], with close ties to the concept of [[Morita equivalence]] in the theory of [[module]]s. 

The basic idea is that the Cauchy completion of a [[category]] is the closure of a category under what are called "absolute limits", i.e., [[limit]]s that are preserved by any [[functor]] whatsoever. Equivalently, the Cauchy completion is the closure with respect to absolute [[colimit]]s. If $C$ is [[small category|small]], the Cauchy completion $\bar{C}$ of $C$ lies between $C$ and its "[[free cocompletion]]", aka [[presheaf]] category

$$C \hookrightarrow \bar{C} \hookrightarrow Set^{C^{op}}$$ 

(see the entry at [[presheaf]] for "free cocompletion"), and consists of those presheaves $F$ dubbed [[tiny object|tiny]] by Lawvere, meaning those presheaves which are [[connected object|connected]] and [[projective object|projective]]: the functor 

$$hom_{Set^{C^{op}}}(F, -): Set^{C^{op}} \to Set$$ 

preserves small coproducts and coequalizers. All of these concepts generalize straightforwardly to the context of general $V$-[[enriched category theory|enriched categories]], where $V$ is a [[complete category|complete]], [[cocomplete category|cocomplete]], [[symmetric monoidal category|symmetric]] [[monoidal closed category]]. 

Lawvere defines a **point** of the Cauchy completion of a small $V$-category $C$ to be a $V$-enriched [[bimodule]] $p: \mathbf{1} \to C$ (in other words, a $V$-functor $\mathbf{1} \to V^{C^{op}}$) for which there is a bimodule $q: C \to \mathbf{1}$ right adjoint to $p$ (in the [[bicategory]] of enriched bimodules (see [[profunctor]])), where $\mathbf{1}$ is the unit $V$-category. Thus points of the Cauchy completion are certain $V$-enriched presheaves $p: C^{op} \to V$, and together form a $V$-category called the **Cauchy completion** whose [[hom-object|hom]]s are the presheaf homs. It is denoted $\bar{C}$. 

As we will explain in more detail below, representables belong to the Cauchy completion, and so the Yoneda embedding of $C$ factors through a full embedding 

$$i: C \to \bar{C}$$ 

and we say the $V$-category $C$ is **Cauchy-complete** if this emebedding is an equivalence. We work through a few examples in the following section. 

## Examples 

#### Example of metric spaces 

We consider first the classical case of [[metric space]]s, but as redefined by Lawvere to mean a category enriched in the [[poset]] $V = ([0, \infty], \geq)$, with [[tensor product]] given by addition. So, to say $X$ is a Lawvere metric space means that with the set $X$ there is a distance function 

$$d_X = hom_X: X \times X \to [0, \infty]$$ 

such that 

$$d(x, y) + d(y, z) \geq d(x, z), \qquad 0 \geq d(x, x)$$ 

for all $x, y, z$ in $X$. (The associativity and identity axioms are here superfluous since $V$ is a poset.) A $V$-enriched functor $f: X \to Y$ here just means a function from $X$ to $Y$ such that 

$$d_X(x, y) \geq d_Y(f(x), f(y))$$ 

for all $x, y$ in $X$ (again, preservation of composition and of identities is superfluous here), so that $V$-functors are contractive maps between vector spaces (Lipschitz maps with constant 1). Finally, a $V$-enriched transformation $f \to g: X \to Y$ in this case boils down to an instance of a property: that 

$$0 \geq d_Y(f(x), g(x))$$ 

for all $x$ in $X$. If $f, g$ are valued in $[0, \infty]$, this just means $f(x) \geq g(x)$ for all $x$. 

A point of the Cauchy completion is an $X$-module $p: \mathbf{1} \to X$, i.e., an enriched functor or contractive map 

$$p: X^{op} \to [0, \infty]$$ 

for which there is an $X$-module $q: X \to \mathbf{1}$ on the other side, an enriched functor 

$$q: X \to [0, \infty]$$ 

that is right adjoint to $p$ in the sense of modules. This means there is a unit of the adjunction in the bicategory of modules: 

$$(Id: \mathbf{1} \to \mathbf{1}) \to (\mathbf{1} \overset{p}{\to} X \overset{q}{\to} \mathbf{1})$$ 

and a counit: 

$$(X \overset{q}{\to} \mathbf{1} \overset{p}{\to} X) \to (Id: X \to X)$$ 

Recall now that $Id_X: X \to X$ in the bicategory of modules is the unit bimodule $y_X: X \to V^{X^{op}}$ given by the enriched [[Yoneda embedding]], or in different words, $hom_X = d_X: X^{op} \times X \to [0, \infty]$. Recall also that module composition is defined by a coend formula for a tensor product. If one now tracks through the definitions, keeping in mind that we are in the very simple case of enrichment in a poset, the unit of the [[adjunction]] $p \dashv q$ boils down to having the property 

$$0 \geq \int^{x \in X} q(x) + p(x) = \inf_{x \in X} q(x) + p(x)$$ 

and the counit boils down to having the property 

$$p(x) + q(y) \geq d_X(x, y)$$ 

To better appreciate what these conditions mean, we point out that $p(x)$ should be thought of as the distance $d_{\bar{X}}(x, p)$ between $x$ and the "ideal point" $p$ in the Cauchy completion $\bar{X}$, and $q(x)$ should be thought of as the companion distance $d_{\bar{X}}(p, x)$. Thus the unit condition above would come down to saying that for every $\varepsilon \gt 0$ there exists $x \in X$ such that 

$$d_{\bar{X}}(p, x) \lt \varepsilon, \, d_{\bar{X}}(x, p) \lt \varepsilon$$ 

and the counit condition imposes a necessary triangle inequality constraint on the distance functions $p$ and $q$, in order that we get an actual metric space $\bar{X}$. If $p, p'$ are two points of the Cauchy completion thus defined, then their distance is defined by the usual formula for enriched presheaves: 

$$d(p, p') = \int_{x \in X} \hom_{[0, \infty]}(p(x), p'(x)) = \sup_{x \in X} \max\{0, p'(x) - p(x)\}$$ 

It should be noted that even under the classical definitions where we impose symmetry ($d(x, y) = d(y, x)$) and separation ($d(x, y) = 0$ implies $x = y$), this provides an elegant alternative definition of Cauchy completion. In essence, all it is doing is taking the metric closure $\bar{X}$ of the embedding of $X$ into the already complete space of contractive maps:  

$$y_X: X \to [0, \infty]^{X^{op}}: x \mapsto d_X(-, x)$$ 

The presheaf-hom definition of the distance formula for $\bar{X}$, being manifestly non-symmetric, is not the usual definition of distance in the classical symmetric case. However, if we first symmetrize the distance in $[0, \infty]$: 

$$\sigma d(r, s) = d(r, s) + d(s, r) = \max\{0, s-r\} + \max\{0, r-s\} = |r - s|$$ 

then we would retrieve the classical formula 

$$d(p, p') = \int_{x \in X} \sigma d(p(x), p'(x)) = \sup_{x \in X} |p(x) - p'(x)|$$ 

#### Example of ordinary (Set-enriched) categories

The analysis of Cauchy complete Lawvere metric spaces contains some of the seeds of what happens in other enriched category contexts; the case of ordinary small categories, where the enrichment is no longer in a mere poset but in $Set$, reflects still more of the phenomena generally associated with Cauchy completions. 

Let $C$ be a small category and let the module $p: \mathbf{1} \to C$ be a point of $\bar{C}$, with module $q: C \to \mathbf{1}$ as its right adjoint in the bicategory of modules. As functors, 

$$p: C^{op} \to Set, \, q: C \to Set$$ 

and the structure of the adjunction is given by unit and counit maps:  

$$\eta: 1 \to \int^{c \in Ob(C)} q(c) \times p(c), \qquad \varepsilon_{c, d}: p(c) \times q(d) \to C(c, d)$$ 

As we said in the case of metric spaces, $p(c)$ and $q(c)$ measure "distances" = homs: 

$$p(c) \cong Set^{C^{op}}(C(-, c), p), \qquad q(c) \cong Set^{C^{op}}(p, C(-, c))$$ 

The first isomorphism is an instance of the Yoneda lemma, and the second can be seen as follows. The set $q(c)$ is the bimodule composite 

$$(\mathbf{1} \overset{c}{\to} C \overset{q}{\to} \mathbf{1})$$ 

where $c$ is shorthand for the module $C(-, c): C^{op} \to Set$; this is just an instance of the Yoneda lemma: 

$$q \circ_C C(-, c) \overset{def}{=} \int^{d \in C} q(d) \times C(d, c) \overset{Yoneda}{\cong} q(c).$$ 

Now using the adjunction $p \dashv q$, there are, for any set $S$, natural bijections 

$$\frac{\frac{S \to q(c)}{S \to q \circ_C C(-, c)}}{\frac{p \circ_{\mathbf{1}} S \to C(-, c)}{p(-) \times S \to C(-, c)}}$$

and maps in the bottom line are in bijection with maps $S \to Set^{C^{op}}(p, C(-, c))$. Therefore we have a natural bijection 

$$\frac{S \to q(c)}{S \to Set^{C^{op}}}$$ 

and this proves $q(c) \cong Set^{C^{op}}(p, C(-, c))$. 

With these identifications of $q(c)$ and $p(c)$, the unit of the adjunction $p \dashv q$ takes the form 

$$\eta: 1 \to \int^{c} Set^{C^{op}}(p, C(-, c)) \times Set^{C^{op}}(C(-, c), p)$$ 

The coend above is a quotient of 

$$\sum_c Set^{C^{op}}(p, C(-, c)) \times Set^{C^{op}}(C(-, c), p)$$ 

and hence the unit element $\eta$ is represented by a pair of transformations 

$$i: p \to C(-, c), \qquad \pi: C(-, c) \to p$$ 

for some $c$. 

Given that, it is now not hard -- in fact it is fairly tautological -- to verify that on the basis of the triangular equation of the adjunction which says 

$$(p \overset{p \circ \eta}{\to} p \circ q \circ p \overset{\varepsilon}{\to} p) = 1_p,$$ 

that 

$$(p \overset{i}{\to} C(-, c) \overset{\pi}{\to} p) = 1_p$$ 

and so a point $p$ in the Cauchy completion $\bar{C}$ must be a retract of a representable $C(-, c)$. Spelling this out a little more: the composite 

$$C(-, c) \overset{\pi}{\to} p \overset{i}{\to} C(-, c)$$ 

is an idempotent represented by a morphism $e: c \to c$ in $C$ (by the Yoneda lemma), and this factorization through $p$ splits the idempotent $C(-, e)$ in $Set^{C^{op}}$. 

Indeed, the claim is that modules $p: C^{op} \to Set$ in the Cauchy completion are precisely those presheaves on $C$ which arise as retracts of representables in $Set^{C^{op}}$, or in other words may be identified with objects of the idempotent-splitting completion of $C$ (aka the _Karoubi envelope_ of $C$). Therefore, in the $Set$-enriched case, the Cauchy completion _is_ the idempotent-splitting completion. In particular, representables themselves are points of the Cauchy completion. 

Notice that in a finitely complete category (such as $Set$ or a presheaf category), idempotents $e: c \to c$ split automatically: just take the equalizer of the pair 

$$c \stackrel{\overset{e}{\to}}{\underset{1}{\to}} c$$ 

For that matter, in any finitely cocomplete category, taking the coequalizer of the above pair would also split the idempotent. Indeed, we can say that idempotents split in a category iff all equalizers of such pairs exist, iff all coequalizers of such pairs exist. 

Notice that if $C$ and $D$ are categories, then any functor $F: C \to D$ preserves retracts and therefore splittings of idempotents. Thus, the equalizers above are the sort of limits which are preserved by _any_ functor $F$ whatsoever. They are called **absolute limits** for that reason. For the same reason, the coequalizers above are **absolute colimits**: they are precisely the colimits preserved by any functor whatsoever. 

Pursuing this a bit further: if $F: C^{op} \to Set$ is any functor, then (because idempotents split in $Set$) there is a unique extension $\bar{F}: \bar{C}^{op} \to Set$ of $F$. Therefore we have an equivalence 

$$Set^{C^{op}} \simeq Set^{\bar{C}^{op}}$$ 

and we say that $C$ and $\bar{C}$ are **Morita equivalent**. 

## Discussion 

_David_: Concerning the result that on Set the terminal F-coalgebra is the Cauchy completion of the initial F-algebra, for certain F, I wonder if we have to factor completions through the metric space completion, as Barr does in <a href="ftp://ftp.math.mcgill.ca/pub/barr/pdffiles/trmclg.pdf">Terminal coalgebras for endofunctors on sets</a>. Perhaps Adamek's work on <a href="http://citeseer.ist.psu.edu/cache/papers/cs/21985/http:zSzzSzwww.iti.cs.tu-bs.dezSzTI-INFOzSzadamekzSzPaper2000-4.pdf/final-coalgebras-are-ideal.pdf">Final Algebras are Ideal Completions of Initial Algebras</a> is more natural.

Does this all tie in with the [[ideal completion]] as <a href="http://golem.ph.utexas.edu/category/2009/08/chasing_around_the_triangle.html">discussed</a> by Awodey where you sum types/sets in a topos into a universal object?

[[!redirects Cauchy complete categories]]
[[!redirects Cauchy completion]]
