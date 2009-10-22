The concept of Cauchy completeness, ordinarily thought of as applying to [[metric space]]s, was vastly generalized by Bill Lawvere in his influential paper "Metric spaces, generalized logic, and closed categories". It is now seen by category theorists as a concept of [[enriched category]] theory, with close ties to the concept of [[Morita equivalence]] in the theory of modules. 

The basic idea is that the Cauchy completion of a category is the closure of a category under what are called "absolute limits", i.e., limits that are preserved by any functor whatsoever. Equivalently, the Cauchy completion is the closure with respect to absolute colimits. If $C$ is small, the Cauchy completion $\bar{C}$ of $C$ lies between $C$ and its "[[free cocompletion]]", aka [[presheaf]] category

$$C \hookrightarrow \bar{C} \hookrightarrow Set^{C^{op}}$$ 

(see the entry at [[presheaf]] for "free cocompletion"), and consists of those presheaves $F$ dubbed [[tiny object|tiny]] by Lawvere, meaning those presheaves which are connected and projective: the functor 

$$hom_{Set^{C^{op}}}(F, -): Set^{C^{op}} \to Set$$ 

preserves small coproducts and coequalizers. All of these concepts generalize straightforwardly to the context of general $V$-[[enriched category theory|enriched categories]], where $V$ is a complete, cocomplete, symmetric [[monoidal closed category]]. 

Lawvere defines a **point** of the Cauchy completion of a small $V$-category $C$ to be a $V$-enriched [[bimodule]] $p: \mathbf{1} \to C$ (in other words, a $V$-functor $\mathbf{1} \to V^{C^{op}}$) for which there is a bimodule $q: C \to \mathbf{1}$ right adjoint to $p$ (in the bicategory of enriched bimodules), where $\mathbf{1}$ is the unit $V$-category. Thus points of the Cauchy completion are certain $V$-enriched presheaves $p: C^{op} \to V$, and together form a $V$-category whose homs are the presheaf homs. We work through a few examples in the following section. 

## Examples 

#### Example of metric spaces 

We consider first the classical case of [[metric space]]s, but as redefined by Lawvere to mean a category enriched in the [[poset]] $V = ([0, \infty], \geq)$, with tensor product given by addition. So, to say $X$ is a Lawvere metric space means that with the set $X$ there is a distance function 

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

Recall now that $Id_X: X \to X$ in the bicategory of modules is the unit bimodule $y_X: X \to V^{X^{op}}$ given by the enriched Yoneda embedding, or in different words, $hom_X = d_X: X^{op} \times X \to [0, \infty]$. Recall also that module composition is defined by a coend formula for a tensor product. If one now tracks through the definitions, keeping in mind that we are in the very simple case of enrichment in a poset, the unit of the adjunction $p \dashv q$ boils down to having the property 

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

To be filled in... 

## Discussion 

_Todd_: I envision starting with the example $V = [0, \infty]$ before treating other bases $V$ such as $Set$ and $Ab$.

_Toby_: Although the term comes from $[0,\infty]$, readers might find it easier to understand in $\Set$, where we usually study limits first. That said, you should write whichever you want, and people will add to it.

_Todd_: Um, I _think_ I understand how the wiki works, Toby, so I while I appreciate your giving me permission to write however I please, I wasn't actually asking for any. I was just stating some intent. That said, some things are easier for the $Set$ case, and some are easier for the case $[0, \infty]$. I'll get back to this in a bit. Thanks. 

_Toby_: Sorry, I interpreted it more broadly as a suggestion for future development rather than individual intent. (That is, 'I envision that we should start with ...' rather than 'I envision that I shall start with ...'.) So I added my own suggestion; but then it sounded like I might be telling you what to do, so I disclaimed that. In other words, of course you don\'t need my permission, but I didn\'t want to leave you with the impression that I was trying to stop you either.

_Todd_: Okay, that makes sense. It would have been clearer had I said "I plan to...": in a sense I was both thinking to myself and also letting people know what I was thinking. Anyway, thanks for clarifying, and I promise to try to add some more intellectual content to this so far scintillating conversation we're having. ;-) 

_Toby_:  I just read this again after a couple of months, and I think that I was just completely stupid.  Of course one should start with $[0, \infty]$!

_David_: Concerning the result that on Set the terminal F-coalgebra is the Cauchy completion of the initial F-algebra, for certain F, I wonder if we have to factor completions through the metric space completion, as Barr does in <a href="ftp://ftp.math.mcgill.ca/pub/barr/pdffiles/trmclg.pdf">Terminal coalgebras for endofunctors on sets</a>. Perhaps Adamek's work on <a href="http://citeseer.ist.psu.edu/cache/papers/cs/21985/http:zSzzSzwww.iti.cs.tu-bs.dezSzTI-INFOzSzadamekzSzPaper2000-4.pdf/final-coalgebras-are-ideal.pdf">Final Algebras are Ideal Completions of Initial Algebras</a> is more natural.

Does this all tie in with the [[ideal completion]] as <a href="http://golem.ph.utexas.edu/category/2009/08/chasing_around_the_triangle.html">discussed</a> by Awodey where you sum types/sets in a topos into a universal object?

[[!redirects Cauchy complete categories]]
[[!redirects Cauchy completion]]
