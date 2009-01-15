In 1999, [[Todd Trimble]] introduced a definition of weak $n$-category in a lecture at Cambridge University. This definition was introduced in order to give an algebraic notion of fundamental $n$-groupoid, and has since been taken up in a number of directions by Tom Leinster and Eugenia Cheng, who compare it with globular approaches (e.g., Batanin's) and give a weak $\omega$-category extension. 

The original idea was to use an $A_{\infty}$ cocategory structure on the topological interval $I$, in the form of an topological operad $T$ which is used to control all ways of weakly composing arrows. Then one proceeds to define weak $n$-categories by induction, defining at each stage a fundamental $n$-groupoid functor 

$$\Pi_n: Top \to nCat$$ 

and then defining an $(n+1)$-category as a category "weakly enriched" in $nCat$, meaning roughly speaking a structure of $\Pi_n(T)$-algebra in the category of $nCat$-graphs. 

## The original idea

Trimble never published this material himself (in effect leaving it to others present at the Cambridge lecture to develop their own accounts, which has been a good thing), but it may be of at least historical interest to have Trimble's original account available. We will then pick out the highlights and streamline the approach, following subsequent work by Leinster and Cheng. 

It will be helpful to review the fundamental (1-)groupoid of a space first, doing it in such a way that we will see how to inductively define the fundamental $n$-groupoid. 

Let $X$ be a space, and let $X_0$ denote its underlying set, viewed as a discrete category. If $V$ is a category, then a _$V$-graph_ over $X_0$ is just a functor 

$$X_0 \times X_0 \to V.$$ 

There is an obvious category of $V$-graphs. A basic example for our purposes is the "graph of paths" in a space $X$: define 

$$X^\tilde : X_0 \times X_0 \to Top \qquad (1)$$ 

by letting $X^{\tilde}(x, y)$ be the space of paths from $x$ to $y$. Two paths from $x$ to $y$ are homotopic if they lie in the same connected component of $X^\tilde(x, y)$, so by applying the connected components functor, 

$$X_0 \times X_0 \stackrel{X^\tilde}{\to} Top \stackrel{\Pi_0}{\to} Set$$ 

we get the graph of homotopy classes of paths. What we want is to put a category structure on this $Set$-graph, so as to obtain the fundamental groupoid $\Pi_1(X)$. 

The $Top$-graph (1) can also be thought of as a topological span from the discrete space $X_0$ to itself, and this is obviously closely related to the span 

$$X^1 \stackrel{X^{i_0}}{\leftarrow} X^I \stackrel{X^{i_1}}{\to} X^1 \qquad (2)$$ 

where $i_0, i_1: 1 \to I$ are the endpoint inclusions. Indeed, we get (1) from (2) by first precomposing with a span from $X_0$ to $X$, 

$$X_0 \leftarrow X_0 \to X,$$

(both arrows being identity functions), followed by postcomposing with the opposite span. This pre- and post-composition gives a functor 

$$TopSpan(X, X) \to TopSpan(X_0, X_0) = TopGraph_{X_0} \qquad (3)$$ 

to which we return later, but for the time being we work with the span (2). 

As a functor in $X$, the span (2) is obtained by homming out of the _interval cospan_ 

$$1 \stackrel{i_0}{\to} I \stackrel{i_1}{\leftarrow} 1$$

and the fundamental groupoid structure on the span (1) ultimately comes about by homming out of an H-cogroupoid structure on the interval cospan, just as the fundamental group of a based space is obtained by homming out of the pointed circle, seen as an H-cogroup. 

Let us describe the H-cocategory structure on the interval cospan. A cospan from a point to itself is a bipointed space, and the composite of two such cospans $X$, $Y$ is obtained by identifying the second point of $X$ with the first point of $Y$, resulting in a new bipointed space we denote by $X \vee Y$. In particular, 

$$I \vee I = [0, 1] \vee [0, 1] \cong [0, 2]$$ 

and the co-composition for the H-cocategory structure on $I$, which is a cospan map $I \to I \vee I$, is essentially just multiplication by 2: 

$$[0, 1] \to [0, 2]$$ 

This co-operation $I \to I \vee I$ is not strictly coassociative, but is coassociative up to homotopy. As a matter of fact, it follows straight away from the _convexity_ of the $n$-fold cospan composite $I^{\vee n} \cong [0, n]$ that the space of cospan maps $\hom(I, I^{\vee n})$ is _contractible_: the convexity actually gives a way of defining coherent homotopies (the pentagon, etc.) all the way up the "$A_{\infty}$-ladder". In other words, the cospan $I$ carries an $A_{\infty}$-cocategory structure. 

But we don't actually need the $A_{\infty}$-jargon: all we will need are two basic facts: 

* There is a tautological topological operad $T$ where the component $T_n$ is the space $\hom(I, I^{\vee n})$ of cospan maps; 

* Each component $T_n$ is contractible. 

The operad structure on $T$ is derived from pure abstract nonsense: if $A$ is an object in a monoidal category, then the objects $\hom(A, A^{\otimes n})$ are the components of an operad, just as are the objects $\hom(A^{\otimes n}, A)$ the components of the familiar tautological endomorphism operad. This applies in particular to the cospan $I$, seen as an object in the monoidal category of cospans from a point to itself. 

Now we just hom out of the cospan co-operations encapsulated in the operad $T$ to get span operations on the topological span above. That is, we use the facts that 

* $\hom(-, X)$ takes the $n$-fold cospan composite $I^{\vee n}$ to the $n$-fold span composite of $X \leftarrow X^I \to X$, so 

* Each co-operation $\theta \in T_n = \hom(I, I^{\vee n})$ induces a span operation 
$$\hom(\theta, X): \hom(I^{\vee n}, X) \to \hom(I, X)$$
from the $n$-fold span composite to the span itself. 

Again, we could express this by saying we derive an $A_\infty$-category structure on the topological span (2), but it is perhaps much less fancy just to say that the composition map 

$$\hom(I, I^{\vee n}) \times \hom(I^{\vee n}, X) \to \hom(I, X)$$ 

gives a $T$-algebra structure on the topological span: 

$$T_n \times (X \leftarrow X^I \to X)^{\otimes n} \to (X \leftarrow X^I \to X) \qquad (4)$$ 

where $\otimes$ indicates span composite. 

* **Remark**: $T$ is an operad in $Top$, not in the monoidal category $TopSpan(X, X)$. But we can make it an operad there by applying an evident change-of-base $Top \to TopSpan(X, X)$, sending a space $Y$ in $Top$ to the span 
$$X \stackrel{\pi}{\leftarrow} X \times Y \stackrel{\pi}{\to} X$$
This change of base is (strong) monoidal. As a matter of fact, this change of base factors through the center of the monoidal category $TopSpan$, which we actually need because one needs symmetries in order to express the notion of an operad internal to a monoidal category. 

We get a similar $T$-algebra structure on the $Top$-graph $X^\tilde: X_0 \times X_0 \to Top$ we started with. Indeed, the functor 

$$TopSpan(X, X) \to TopSpan(X_0, X_0) \cong TopGraph_{X_0} \qquad (3)$$ 

is a lax monoidal functor, and hence takes $T$-algebras in $TopSpan(X, X)$ (as in (4)) to $T$-algebras in $TopGraph_{X_0}$. This gives a $T$-algebra structure 

$$T_n \times (X^\tilde)^{\otimes n} \to X^\tilde \qquad (5)$$ 

in the monoidal category of $Top$-graphs. Considered geometrically, this is almost pure tautology, but **(5) is the crucial input datum in Trimble's machine**. 

We may as well make some of this explicit. In general, if $V$ is a monoidal category with coproducts, such that the tensor $u \otimes v$ preserves coproducts in each of its separate arguments $u$ and $v$, then the category of $V$-graphs also carries a monoidal structure, where for two $V$-graphs $G, H$ we define 

$$(G \otimes H)(x, z) = \sum_y G(x, y) \otimes H(y, z)$$ 

Hence, in the case $V = Top$, (5) takes the more explicit form 

$$T_n \times \sum_{y_1, \ldots, y_{n-1}} X^\tilde(x, y_1) \times X^\tilde(y_1, y_2) \times \ldots \times X^\tilde(y_{n-1}, z) \to X^{\tilde}(x, z) \qquad (6)$$ 

Now apply the functor $\Pi_0: Top \to Set$ (which preserves products and incidentally sums as well) to (6). This makes the $Set$-graph $\Pi_0 X^\tilde$ an algebra over the operad $\Pi_0 T$. But a $Set$-graph equipped with a $\Pi_0 T$-algebra structure is just a category, since $\Pi_0 T_n$ consists of just a point. 

This category is precisely the fundamental groupoid $\Pi_1(X)$. It is pretty clear from this description that $\Pi_1(X)$ is functorial in $X$. Indeed, if $f: X \to Y$ is a continuous map, we can pull back the $Top$-graph $Y^\tilde$ over $Y_0$ to a $Top$-graph over $X_0$, 

$$X_0 \times X_0 \stackrel{f_0 \times f_0}{\to} Y_0 \times Y_0 \stackrel{Y^\tilde}{\to} Top,$$ 

which we call $f_0^{-1} Y^\tilde$. The continuous map $f: X \to Y$ induces a comparison map of $T$-algebras in $TopGraph_{X_0}$, 

$$ f^*: X^\tilde \to f_0^{-1} Y^\tilde: X_0 \times X_0 \to Top $$ 

and again by composing with $\Pi_0: Top \to Set$, we get a map $ \Pi_0 f^*: \Pi_1(X) \to \Pi_1(Y) $, i.e., a functor between the fundamental groupoids. 

Thus, by a long series of small tautological steps, we have bootstrapped our way up from $\Pi_0$ to $\Pi_1$. This same procedure suggests a way to bootstrap from $\Pi_1$ to a definition of $\Pi_2$, and so on up an $n$-categorical ladder. Here are the general inductive definitions: 

* A (flabby) 0-category is a set. The fundamental 0-groupoid $Top \to Flabby(0)Cat$ is the connected components functor $\Pi_0: Top \to Set$. 

* For $n \geq 0$, a **flabby $(n+1)$-category** consists of a set $X_0$ and a $Flabby(n)Cat$-graph 
$$X: X_0 \times X_0 \to Flabby(n)Cat$$ 
equipped with a structure of algebra over the operad $\Pi_n T$ (a priori an operad in the cartesian monoidal category $Flabby(n)Cat$, but made into an operad in $Flabby(n)CatGraph_{X_0}$ by an obvious change of base; cf. the remark above). 

* A **morphism** of flabby $(n+1)$-categories $(X_0, X) \to (Y_0, Y)$ consists of of a function $f_0: X_0 \to Y_0$ together with a _strict_ $\Pi_n T$-algebra map $f: X \to f_0^{-1} Y$. The category $Flabby(n+1)Cat$ admits finite products and arbitrary sums over which products distribute. 

* The **fundamental flabby $(n+1)$-category functor** 
$$\Pi_{n+1}: Top \to Flabby(n+1)Cat$$ 
sends a space $X$ to the pair $(X_0, \Pi_n X^\tilde)$, seen as a $\Pi_n T$-algebra by applying the product-preserving functor $\Pi_n$ to the tautological $T$-algebra $X^\tilde$. 

* **Theorem**: $\Pi_{n+1}$ preserves finite products and arbitrary coproducts. 

And that's it. As Cheng put it, this inductive definition is disarmingly straightforward, and yet it codes up all the essential structure one expects to see in weak $n$-categories. For example, an associator for 2-categories is coded up as a 1-cell in $\Pi_1 T_3$, i.e., as a homotopy class of paths between two points in $\hom(I, I \vee I \vee I)$: 

$$(\delta \vee 1)\delta, (1 \vee \delta)\delta: [0, 1] \to [0, 3]$$ 

where $\delta: [0, 1] \to [0, 2]$ is a co-composition. The pentagonator is similarly coded up as a 2-cell in $\Pi_2 T_4$. And so on. 

To be continued...