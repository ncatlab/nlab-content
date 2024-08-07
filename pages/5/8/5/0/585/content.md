
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Content#
* automatic table of contents goes here
{:toc}

[[Todd Trimble]]'s definition of weak $n$-[[n-category|category]] is an example of a notion of weak $n$-category which is based on using an [[operad]] induced by all the possible compositions of an [[interval object]] with itself for describing weak composition of 1-morphisms. The higher cells and their composition are then obtained iteratively.

Trimble originally called these *flabby* $n$-categories, which was intended to distinguish them from "weak" $n$-categories (since at the time he wasn't convinced that they were truly weak enough, owing to the fact that we use strict maps of algebras along the way), and also to recall the word "flab" as used by [[Frank Adams]] in his Infinite Loop Spaces book (since there is rather a lot of topological flab in the definition).  

## Basic idea

An [[morphism|arrow]] looks like an  [[interval object|interval]]. So, the [[category theory|theory of categories]] and even [[higher category theory|n-categories]] should have a lot to do with the [[interval object|interval]] &#8212; especially when it comes to applications to [[topology]]!

In a [[category]] we can glue [[morphism|arrows]] together, 'composing' them. But an [[interval object|interval]] can be chopped apart or 'decomposed' into a bunch of intervals. So, there should be a [[cocategory]] or something like that lurking around here.

In fact the closed unit interval gives an [[A-infinity category|A-infinity]]-[[cocategory]]: a [[cocategory]] where the laws hold up to [[homotopy]], where the homotopies satisfy nice laws up to homotopy, [[homotopy coherent category theory|ad infinitum]].

The space of maps out of an $A_\infty$-cocategory into something should form an [[A-infinity category]]. So, the space of maps out of an interval into a space forms an $A_\infty$-category. And this is an important first step in how [[Todd Trimble]] constructs the [[fundamental infinity-groupoid|fundamental n-groupoid ]] of a space!

But the really cool part is how this construction goes hand in hand with his definition of $n$-categories, in an inductive kind of way.


## History 

In 1999, [[Todd Trimble]] introduced a definition of weak $n$-category in a lecture at Cambridge University. This definition was introduced in order to give an algebraic notion of fundamental $n$-groupoid, and has since been taken up in a number of directions by [[Tom Leinster]] and [[Eugenia Cheng]], who compare it with globular approaches (e.g., [[Michael Batanin|Batanin]]'s) and give a weak $\omega$-category extension. 

Trimble never published this material himself (in effect leaving it to others present at the Cambridge lecture to develop their own accounts, which has been a good thing), but it may be of at least historical interest to have Trimble's original account available. We will then pick out the highlights and streamline the approach, following subsequent work by Leinster and Cheng. 

## The original idea

The original idea was to use an $A_\infty$-[[A-infinity-cocategory|cocategory]] structure on the topological [[interval object|interval]] $I$, in the form of an [[Top|topological]] [[operad]] $T$ which is used to control all ways of weakly composing arrows. Then one proceeds to define [[n-category|weak n-categories]] by induction, defining at each stage a [[fundamental groupoid|fundamental]] [[n-groupoid]] [[functor]] 

$$\Pi_n: Top \to n Cat$$ 

and then defining an $(n+1)$-category as a category "weakly [[enriched category|enriched]]" in $nCat$, meaning roughly speaking a structure of $\Pi_n(T)$-[[algebra over an operad|algebra]] in the category of $n Cat$-[[graph]]s. 


It will be helpful to review the [[fundamental groupoid|fundamental (1-)groupoid]] of a space first, doing it in such a way that we will see how to inductively define the fundamental $n$-groupoid. 

Let $X$ be a [[topological space]], and let $X_0$ denote its underlying set, viewed as a [[discrete category]]. If $V$ is a category, then a _$V$-graph_ over $X_0$ is just a functor 

$$X_0 \times X_0 \to V$$ 

(which here amounts to a function $X_0 \times X_0 \to Ob(V)$).There is an obvious category of $V$-graphs over $X_0$. 

* We can also consider a more general category **$V$-Graph**, where a morphism $(C_0, C(-, -)) \to (D_0, D(-, -))$ consists of a function $f_0: C_0 \to D_0$ together with a collection $C(c, c') \to D(f_0 c, f_0 c')$ of morphisms in $D$.  

A basic example of $V$-graph for our purposes is the "graph of paths" for a space $X$: define 

\[\label{Trimble1}
X^\sim : X_0 \times X_0 \to Top
\]

by letting $X^\sim(x, y)$ be the [[topological space|space]] of paths from $x$ to $y$. Two paths from $x$ to $y$ are homotopic if they lie in the same connected component of $X^\sim(x, y)$, so by applying the connected components functor, 

$$X_0 \times X_0 \stackrel{X^\sim}{\to} Top \stackrel{\Pi_0}{\to} Set$$ 

we get the graph of [[homotopy (as a transformation)|homotopy classes]] of paths. What we want is to put a category structure on this $Set$-graph, so as to obtain the [[fundamental groupoid]] $\Pi_1(X)$. 

The $Top$-graph (eq:Trimble1) can also be thought of as a topological [[span]] from the discrete space $X_0$ to itself, and this is obviously closely related to the span 

\[\label{Trimble2}
X^1 \stackrel{X^{i_0}}{\leftarrow} X^I \stackrel{X^{i_1}}{\to} X^1
\] 

where $i_0, i_1: 1 \to I$ are the endpoint inclusions. Indeed, we get (eq:Trimble1) from (eq:Trimble2) by first precomposing with a span from $X_0$ to $X$, 

$$X_0 \leftarrow X_0 \to X,$$

(both arrows being identity functions), followed by postcomposing with the opposite span. This pre- and post-composition gives a functor 

\[\label{Trimble3}
TopSpan(X, X) \to TopSpan(X_0, X_0) = TopGraph_{X_0}
\] 

to which we return later, but for the time being we work with the span (eq:Trimble2). 

As a functor in $X$, the span (eq:Trimble2) is obtained by homming out of the _interval cospan_ 

$$1 \stackrel{i_0}{\to} I \stackrel{i_1}{\leftarrow} 1$$

and the fundamental groupoid structure on the span (eq:Trimble1) ultimately comes about by homming out of an H-cogroupoid structure on the interval cospan, just as the [[fundamental group]] of a based space is obtained by homming out of the pointed circle, seen as an H-[[cogroup]]. 

Let us describe the H-[[cocategory]] structure on the interval [[cospan]]. A cospan from a point to itself is a bi[[pointed object|pointed]] space, and the composite of two such cospans $X$, $Y$ is obtained by identifying the second point of $X$ with the first point of $Y$, resulting in a new bipointed space we denote by $X \vee Y$. In particular, 

$$I \vee I = [0, 1] \vee [0, 1] \cong [0, 2]$$ 

and the co-composition for the H-cocategory structure on $I$, which is a cospan map $I \to I \vee I$, is essentially just multiplication by 2: 

$$[0, 1] \to [0, 2]$$ 

This co-operation $I \to I \vee I$ is not strictly coassociative, but is coassociative up to [[homotopy (as a transformation)|homotopy]]. As a matter of fact, it follows straight away from the _[[convex space|convexity]]_ of the $n$-fold cospan composite $I^{\vee n} \cong [0, n]$ that the space of cospan maps $\hom(I, I^{\vee n})$ is _contractible_: the convexity actually gives a way of defining coherent homotopies (the pentagon, etc.) all the way up the "$A_{\infty}$-ladder". In other words, the cospan $I$ carries an $A_{\infty}$-cocategory structure. 

But we don't actually need the $A_{\infty}$-jargon: all we will need are two basic facts: 

* There is a 'tautological' topological operad $T$ where the component $T_n$ is the space $\hom(I, I^{\vee n})$ of cospan maps; 

* Each component $T_n$ is contractible. 

The operad structure on $T$ is derived from pure abstract nonsense: if $A$ is an object in a monoidal category, then the objects $\hom(A, A^{\otimes n})$ are the components of an operad, just as are the objects $\hom(A^{\otimes n}, A)$ the components of the familiar tautological endomorphism operad. This applies in particular to the cospan $I$, seen as an object in the monoidal category of cospans from a point to itself; in analogy, we call $T$ 'tautological' as well.

Now we just hom out of the cospan co-operations encapsulated in the operad $T$ to get span operations on the topological span above. That is, we use the facts that 

* $\hom(-, X)$ takes the $n$-fold cospan composite $I^{\vee n}$ to the $n$-fold span composite of $X \leftarrow X^I \to X$, so 

* Each cospan co-operation $\theta \in T_n = \hom(I, I^{\vee n})$ induces a span operation 
$$\hom(\theta, X): \hom(I^{\vee n}, X) \to \hom(I, X)$$
from the $n$-fold span composite to the span itself. 

Again, we could express this by saying we derive an $A_\infty$-[[A-infinity-category|category]] structure on the topological span (eq:Trimble2), but in less fancy terms, the composition map 

$$\hom(I, I^{\vee n}) \times \hom(I^{\vee n}, X) \to \hom(I, X)$$ 

gives a $T$-algebra structure on the topological span: 

\[\label{Trimble4}
T_n \times (X \leftarrow X^I \to X)^{\otimes n} \to (X \leftarrow X^I \to X)
\] 

where $\otimes$ indicates span composite. 

* **Remark**: $T$ is an operad in $Top$, not in the monoidal category $TopSpan(X, X)$. But we can make it an operad there by applying an evident change-of-base $Top \to TopSpan(X, X)$, sending a space $Y$ in $Top$ to the span 
$$X \stackrel{\pi}{\leftarrow} X \times Y \stackrel{\pi}{\to} X$$
This change of base is (strong) monoidal. As a matter of fact, this change of base factors through the center of the monoidal category $TopSpan$, which we actually need because one needs symmetries in order to express the notion of even a nonpermutative operad internal to a monoidal category. 

We get a similar $T$-algebra structure on the $Top$-graph $X^\sim: X_0 \times X_0 \to Top$ we started with. Indeed, the functor 

\[\label{Trimble3}
TopSpan(X, X) \to TopSpan(X_0, X_0) \cong TopGraph_{X_0}
\]

is a lax monoidal functor, and hence takes $T$-algebras in $TopSpan(X, X)$ (as in (eq:Trimble4)) to $T$-algebras in $TopGraph_{X_0}$. This gives a $T$-algebra structure 

\[\label{Trimble5}
T_n \times (X^\sim)^{\otimes n} \to X^\sim
\] 

in the monoidal category of $Top$-graphs. Considered geometrically, this is almost pure tautology, but **(eq:Trimble5) is the crucial topological input in Trimble's machine**. 

Let us make this more explicit. In general, if $V$ is a monoidal category with coproducts, such that the tensor $u \otimes v$ preserves coproducts in each of its separate arguments $u$ and $v$, then the category of $V$-graphs also carries a monoidal structure, where for two $V$-graphs $G, H$ we define 

$$(G \otimes H)(x, z) = \sum_y G(x, y) \otimes H(y, z)$$ 

Hence, in the case $V = Top$, (eq:Trimble5) takes the more explicit form 

\[\label{Trimble6}
T_n \times \sum_{y_1, \ldots, y_{n-1}} X^\sim(x, y_1) \times X^\sim(y_1, y_2) \times \ldots \times X^\sim(y_{n-1}, z) \to X^{\sim}(x, z)
\]

Now apply the functor $\Pi_0: Top \to Set$ (which preserves products and incidentally sums as well) to (eq:Trimble6). This makes the $Set$-graph $\Pi_0 X^\sim$ an algebra over the operad $\Pi_0 T$. But a $Set$-graph equipped with a $\Pi_0 T$-algebra structure is just a category, since $\Pi_0 T_n$ consists of just a point, i.e., is the [[associative operad]]  whose algebras are monoids, and a category is a monoid in a category of graphs. 

This category is precisely the fundamental groupoid $\Pi_1(X)$. It is pretty clear from this description that $\Pi_1(X)$ is functorial in $X$. Indeed, if $f: X \to Y$ is a continuous map, we can pull back the $Top$-graph $Y^\sim$ over $Y_0$ to a $Top$-graph over $X_0$, 

$$X_0 \times X_0 \stackrel{f_0 \times f_0}{\to} Y_0 \times Y_0 \stackrel{Y^\sim}{\to} Top,$$ 

which we call $f_0^{-1} Y^\sim$. The continuous map $f: X \to Y$ induces a comparison map of $T$-algebras in $TopGraph_{X_0}$, 

$$ f^*: X^\sim \to f_0^{-1} Y^\sim: X_0 \times X_0 \to Top $$ 

and again by composing with $\Pi_0: Top \to Set$, we get a map $ \Pi_0 f^*: \Pi_1(X) \to \Pi_1(Y) $, i.e., a functor between the fundamental groupoids. 

Thus, after a series of small tautological steps, we have bootstrapped our way up from $\Pi_0$ to $\Pi_1$. This same procedure suggests a way to bootstrap from $\Pi_1$ to a definition of $\Pi_2$, and so on up an $n$-categorical ladder. Here are the general inductive definitions: 

* A (Trimble) 0-category is a set. The fundamental 0-groupoid $Top \to 0 Cat$ is the connected components functor $\Pi_0: Top \to Set$. 

* For $n \geq 0$, a **Trimble $(n+1)$-category** consists of a set $X_0$ and a $n Cat$-graph 
$$X: X_0 \times X_0 \to n Cat$$ 
equipped with a structure of algebra over the operad $\Pi_n T$ (a priori an operad in the cartesian monoidal category $n Cat$, but made into an operad in $n Cat Graph_{X_0}$ by an obvious change of base; cf. the remark above). 

* A **morphism** of Trimble $(n+1)$-categories $(X_0, X) \to (Y_0, Y)$ consists of of a function $f_0: X_0 \to Y_0$ together with a _strict_ $\Pi_n T$-algebra map $f: X \to f_0^{-1} Y$. The category $(n+1)Cat$ admits finite products and arbitrary sums over which products distribute. 

* The **fundamental $(n+1)$-groupoid functor** 
$$\Pi_{n+1}: Top \to (n+1)Cat$$ 
sends a space $X$ to the pair $(X_0, \Pi_n X^\sim)$, seen as a $\Pi_n T$-algebra by applying the product-preserving functor $\Pi_n$ to the tautological $T$-algebra $X^\sim$. 

* **Theorem**: $\Pi_{n+1}$ preserves finite products and arbitrary coproducts. (This theorem is needed to push the induction through.)

And that's it. Notice this approach is in essence globular, that is we have an underlying functor 

$$U_n: n Cat \to (n)GlobularSet$$ 

to $n$-globular sets. This is defined by induction: the underlying $(n+1)$-globular set of an $(n+1)$-category $(X_0, X)$ is given by 

$$X_0 \times X_0 \to (n)Cat \stackrel{U_n}{\to} (n)GlobularSet$$ 

using the fact that an $(n+1)$-globular set is naturally an $n$-globular graph over its set of 0-cells. In fact, Cheng has shown that Trimble $n$-categories (and related structures; see the next section) are the algebras of a Batanin operad, that is a globular operad satisfying a contractibility condition. 

As Cheng put it, Trimble's inductive definition is disarmingly straightforward, and yet it codes up all the essential structure one expects to see in weak $n$-categories. For example, an associator for 2-categories is coded up as a 1-cell in $\Pi_1 T_3$, i.e., as a homotopy class of paths between two points in $\hom(I, I \vee I \vee I)$: 

$$(\delta \vee 1)\delta, (1 \vee \delta)\delta: [0, 1] \to [0, 3]$$ 

where $\delta: [0, 1] \to [0, 2]$ is a co-composition. The pentagonator is similarly coded up as a 2-cell in $\Pi_2 T_4$. And so on. 

To be continued...

## Comparison to classical notions of $n$-category in low degree

A Trimble $n$-category has composition and unit which are associative and unital up to $n-1$-equivalence, but the notion of a morphism of Trimble $n$-categories is strict; for example, a morphism of bicategories regarded as Trimble 2-categories is precisely a strict pseudofunctor (one whose lax composition constraint and lax unit constraint are identity 2-cells).

In comparison with classical concrete definitions of higher category, a bicategory is precisely a Trimble 2-category, but a Trimble 3-category is a tricategory satisfying a strict interchange law for composition. [[Simpson's conjecture]] implies that every tricategory should be equivalent to one with a strict interchange law for composition: this is proven for tricategories with a single object. A different, proven, coherence theorem for tricategories states that every tricategory is equivalent to a [[Gray-category|Gray category]], which is a tricategory strict in every respect *except* for the interchange law.

## Iterative operadic enrichment

The account above was given in a traditional language of operads, but subsequent analysis by Leinster and Cheng led to the following notion, involving a hybrid between algebras over an [[operad]] and [[enriched category theory|enriched categories]]. 

Fix a symmetric monoidal category $V$, and let $P$ be an operad valued in $V$. A **$(V, P)$-category** consists of 

* A set of objects $X_0$, 

* A $V$-graph $X(-, -): X_0 \times X_0 \to V$; 

* Maps $P_n \otimes X(x_0, x_1) \otimes \ldots X(x_{n-1}, x_n) \to X(x_0, x_n)$ parametrized over all choices $x_0, x_1, \ldots, x_n$

subject to axioms similar to the usual axioms for algebras over an operad. 

* Example: For $V = (Top, \times)$ and $P$ the operad $T = \{\hom_{cospan}(I, I^{\vee n})\}$ discussed above, we constructed a $(V, P)$-category $(X_0, X^\sim)$ out of any space $X$.

Trimble's definition above amounts to an inductive definition of weak $n$-Cat (call it $V_n$) where 

* 0-Cat = Set; 

* $V_{n+1} = (V_n, P_n)$-Cat 

for some series of operads $P_n$ valued in $V_n$. The operads $P_n$ in his definition came from one master operad $T$, by applying a product-preserving functor 

$$\Pi_n: Top \to V_n$$

to $T$. But other operads are possible.  For the purposes of $n$-category theory, we should choose operads that are contractible in some sense (which the $\Pi_n(T)$ should be), but even in the realm of contractible operads there are many possible choices which may be convenient for different purposes.


## Extension to $\infty$-categories {#InftyCats}

Using some theory of terminal coalgebras, Leinster and Cheng described a viable notion of Trimble $\infty$-category.

* [Terminal coalgebras](http://www-lmpa.univ-littoral.fr/CT08/slides/Cheng.pdf)

There are several equivalent ways to describe this construction.

### As an inverse limit

This approach starts from the observation that the category $Str \infty Cat$ of strict $\infty$-categories is the inverse limit in $CAT$ of the sequence

$$\dots \to Str3Cat \to Str2Cat \to Cat \to Set$$

where each functor is "truncation," i.e. discard all top-dimensional cells.  We would like to imitate this, but the problem is that if we discard the $(n+1)$-cells in a (Trimble) weak $(n+1)$-category, we don't get a weak $n$-category; for that we would have to also *identify* $n$-cells that are connected by some $(n+1)$-cell.

We can see this going on at the operad level as well.  Consider the basic shape of the fundamental $n$-groupoid $\Pi_n(X)$ as a globular set: in dimensions $j \lt n$, the $j$-cells are just continuous maps $D^j \to X$, but the dimension $j = n$ is exceptional: the putative $\infty$-groupoid $\Pi_\omega(X)$ is "truncated" to a fundamental $n$-groupoid $\Pi_n(X)$ by forcing all $j$-cells in dimensions $j \gt n$ to be identity cells, that is by taking the quotient of the set of $n$-cells $D^n \to X$ with respect to homotopy-equivalence rel boundary $\partial D^n$.  Thinking of homotopy-equivalence classes in terms of applying a path-components functor $\Pi_0$ to a suitable function space, one sees after some reflection that this globular "truncation", which is a sort of enforcement of coherence at the level of top-dimensional cells, is really the result of beginning the iterative enrichment with the path-components functor 

$$\Pi_0: Top \to Set$$ 

in the first place. 

In slightly different words: this form of "truncation" from a higher-dimensional category to a lower one is iterated "decategorification", going from isomorphisms between $n$-cells to isomorphism classes of $n$-cells: again the effect of applying a connected components functor $\Pi_0$. To take weak $\omega$-categories seriously is to eliminate all vestiges of such decategorification: there are no coherence _equations_ to impose at the top level; there are only higher and higher coherence data all the way up the dimensional chain, which one could elect to chop off past a certain point (instead of modding out by).

So in order to perform the inverse limit construction successfully, we should *not* perform any identifications at all, merely truncation.  Precisely, if instead of starting out the iterative enrichment with $\Pi_0$, one could start by replacing it with the *underlying set functor*

$$U: Top \to Set$$

and again set the machine in motion.  In this way we obtain an "incoherent Trimble 1-category" as a graph equipped with a structure of algebra over the operad $D_0 = U T$, an "incoherent Trimble 2-category" as a graph enriched in incoherent 1-categories and with a structure of algebra over the operad $D_1 = D_0 T$, and so on. Again, one proves that $D_n$ preserves coproducts and finite products by induction, starting with the base observation that the underlying set functor $U$ preserves coproducts and finite products.  Thus by induction we have a category of incoherent $n$-categories, $n iCat$.

As a result, we have actual truncation functors 

$$\ldots (n+1)iCat \to n iCat \to \ldots ... \to Set$$

where one just saws off the $(n+1)$-cells at each step, and one may define the category of Trimble $\omega$-categories as the inverse limit of this sequence.

### As a terminal coalgebra

This approach begins with the observation of Simpson that $Str$-$\omega$-$Cat$ is a fixed point of the ordinary enrichment process

$$E: V \mapsto V-Cat$$ 

taking a (complete, cocomplete) closed symmetric monoidal $V$ to the (complete, cocomplete) closed symmetric monoidal category of small $V$-categories.  In fact, it is more than a fixed point; it is a [[terminal coalgebra]] for the functor $E$.  This is the same as the previous observation that $Str \omega Cat$ is the inverse limit of the sequence

$$\ldots \to Strict(n+1)Cat \overset{E^n !}{\to} Strict(n)Cat \to \ldots Set \overset{!}{\to} 1$$ 

because of Adamek's theorem that the limit

$$ \dots \to E^n 1 \to \dots \to E^2 1 \to E 1 \to 1 $$

always produces a terminal $E$-coalgebra whenever the functor $E$ preserves limits of sequences of this form.   In our case, $E^n !$ works out to be the usual globular truncation from $(n+1)$-categories to $n$-categories.  We now observe that the same principle applies to the weak enrichment process, as long as we carry along the information of the fundamental $n$-groupoid functor, i.e. we consider the functor

$$E: \langle V, \Pi \rangle \mapsto \langle (V, \Pi)-Cat, \Pi^+ \rangle$$ 

where $\Pi: Top \to V$ preserves finite products (and coproducts), where $(V, \Pi)$-$Cat$ is the category of $(V,\Pi(T))$-categories, and where $\Pi^+$ takes a space $X$ to $\Pi(X^\sim)$ as a $(V,\Pi(T))$-category.
This time $E^n !$ works out to be precisely the globular truncation

$$Dec(n+1)Cat \to Dec(n)Cat$$ 

and so the terminal $E$-coalgebra is the category $Trimble(\omega)Cat$ as described above, equipped with the fundamental $\omega$-groupoid functor 

$$\Pi_\omega: Top \to Trimble(\omega)Cat$$ 

### As a coinductive definition {#Coinductive}

It is often convenient to reason about terminal coalgebras using [[coinduction]] and [[corecursion]].  In this spirit, it is possible to reformulate the definition of Trimble $\omega$-categories coinductively.  Namely, we define a category $\omega Cat = Trimble \omega Cat$ and a functor $\Pi\colon Top \to \omega Cat$, which preserves coproducts and finite products, by mutual coinduction, as follows.

* An object of $\omega Cat$ (that is, a Trimble $\omega$-category) is an $(\omega Cat,\Pi(T))$-category, i.e. an $\omega Cat$-enriched graph $X$ with composition operations $\Pi(T)_n \times X(x_0, x_1) \times \ldots X(x_{n-1}, x_n) \to X(x_0, x_n)$ satisfying the evident axioms.
* Similarly, a morphism in $\omega Cat$ is a (strict) $(\omega Cat,\Pi(T))$-functor, i.e. a map of $\omega Cat$-enriched graphs which respects the $\Pi(T)$-structure.
* The functor $\Pi$ takes a space $X$ to the $\omega$-category $\Pi(X^\sim)$, whose objects are the points of $X$, whose hom-$\omega$-category from $x$ to $y$ is $\Pi(X^\sim(x,y))$, and whose $\Pi(T)$-structure is given by composing paths.

This sort of coinductive definition is that used in the [[calculus of coinductive constructions]], which when rephrased in terms of a terminal coalgebra reduces to the definitions given above.


## Category theory for Trimble $n$-categories {#CatTheory}


+-- {: .query}

[[Urs Schreiber|Urs]]:

suppose I wanted to serious apply the Trimble $n$-category tool to some class of problems. It would be helpful to have an idea about some of the following points. 

The main reason why [[quasi-category|quasi-categories]]
and other models for 
[[(infinity,1)-category|(infinity,1)-categories]] 
are popular is that Joyal and Lurie showed that beyond
just having a definition, one can _do category theory_
with them. I would like to understand to which extent
we know how to "do category theory" with Trimble $n$-categories.

I understand that much of this will remain to be worked out, but probably in particular [[Todd Trimble|Todd]] has many ideas about how one should go about approaching this. I'd be interested in whatever idea or tentative suggestion there is.

So:

What can be said about 

* [[universal construction]]s

  * definition of [[weak limit]]/weak colimit, of [[adjunction]]s and [[Kan extension]] 
43
in Trimble $n$-catgeories? 

For instance for what I am doing
I'd need in particular weak pullbacks and the resulting
[[fibration sequence]]s in a Trimble $n$-category.
What are the chances to get hold of these notions in this context?

What is known about the reflection of Trimble $n$-categories on themselves

* Is there a definition of Trimble $(n+1)$-categorry of all Trimble $n$-categories?

* A Trimble $\infty$-category of all Trimble $\infty$-categories?


What is the relation to 

* [[simplicial model for weak omega-categories|simplicial models for weak omega categories]],

  * do we have a notion of [[nerve]] of a Trimble $n$-category? 

  * can we characterize the nerves of Trimble $n$-categories?

Probably we want to define the cosimplicial Trimble $\infty$-category that sends $[n]$ to the fundamental Trimble $\infty$-path category of the topological $n$-simplex and induce a notion of nerve of that. But the naive version of that will give just $\infty$-groupoidal nerve. What is generally needed is probably a notion of [[directed space|directed]] Trimble path $n$-category.

What can be said about [[(n,r)-category]]-cases of Trimble $n$-categories. How do we say "Trimble $n$-groupoid"?


What about monoidal structures? Is there a good guess for what it would mean to have a

* monoidal Trimble $n$-category

* symmetric (i.e. stably) monoidal Trimble $n$-category?

=--

## References

The first appearance in print of the definition was in 

* [[Tom Leinster]], _A Survey of Definitions of $n$-Category_ ([arXiv](http://arxiv.org/abs/math.CT/0107188)), [p. 54](http://arxiv.org/PS_cache/math/pdf/0107/0107188v1.pdf#page=54) 

Later the definition was applied tentatively for the construction of weak $n$-cateories of cobordisms in

* [[Eugenia Cheng]] and [[Nick Gurski]], _Towards an $n$-category of cobordisms_, Theory and Applications of Categories, Vol. 18, 2007, No. 10, pp 274-302. ([tac](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html))

This article first reviews the original definition

* section 2, _Trimble's definition_ recalls the original definition, 

and then generalizes it 

* section 4 _Generalised Trimble definition_ proposes a generalization

A comparison of Trimble's definition with that of a [[Batanin omega-category]] is in

* [[Eugenia Cheng]], _Comparing operadic theories of $n$-category_ ([arXiv](http://arxiv.org/abs/0809.2070))

Weak ω-category construction via terminal coalgebras

* [[Eugenia Cheng]] and [[Tom Leinster]], _Weak ω-categories via terminal coalgebras_ ([arXiv](https://arxiv.org/abs/1212.5853)), published as _Weak $\infty$-categories via terminal coalgebras_, Theory and Applications of Categories,  Vol. 34, 2019, No. 34, pp 1073-1133. ([tac](http://www.tac.mta.ca/tac/volumes/34/34/34-34abs.html))

[[!redirects Trimble's notion of weak n-category]]
[[!redirects Trimble's notion of weak n-category]]
[[!redirects flabby n-category]]
[[!redirects flabby n-categories]]

[[!redirects Trimble omega-category]]
[[!redirects Trimble ∞-category]]
[[!redirects Trimble omega-catgeories]]
[[!redirects Trimble ∞-categories]]