Trimble's definition of weak $n$-category is an example of a notion of [[weak omega-category]] which is based on using an [[operad]] induced by all the possible compositions of an [[interval object]] with itself for describing weak composition of 1-morphisms. The higher cells and their composition are then obtained iteratively.


## History ##

In 1999, [[Todd Trimble]] introduced a definition of weak $n$-category in a lecture at Cambridge University. This definition was introduced in order to give an algebraic notion of fundamental $n$-groupoid, and has since been taken up in a number of directions by Tom Leinster and Eugenia Cheng, who compare it with globular approaches (e.g., Batanin's) and give a weak $\omega$-category extension. 

Trimble never published this material himself (in effect leaving it to others present at the Cambridge lecture to develop their own accounts, which has been a good thing), but it may be of at least historical interest to have Trimble's original account available. We will then pick out the highlights and streamline the approach, following subsequent work by Leinster and Cheng. 





## The original idea


The original idea was to use an $A_\infty$-[[A-infinity-cocategory|cocategory]] structure on the topological interval $I$, in the form of an topological operad $T$ which is used to control all ways of weakly composing arrows. Then one proceeds to define weak $n$-categories by induction, defining at each stage a fundamental $n$-groupoid functor 

$$\Pi_n: Top \to nCat$$ 

and then defining an $(n+1)$-category as a category "weakly enriched" in $nCat$, meaning roughly speaking a structure of $\Pi_n(T)$-algebra in the category of $nCat$-graphs. 


It will be helpful to review the fundamental (1-)groupoid of a space first, doing it in such a way that we will see how to inductively define the fundamental $n$-groupoid. 

Let $X$ be a space, and let $X_0$ denote its underlying set, viewed as a discrete category. If $V$ is a category, then a _$V$-graph_ over $X_0$ is just a functor 

$$X_0 \times X_0 \to V$$ 

(which here amounts to a function $X_0 \times X_0 \to Ob(V)$).


There is an obvious category of $V$-graphs. A basic example for our purposes is the "graph of paths" in a space $X$: define 

$$X^\sim : X_0 \times X_0 \to Top \qquad (1)$$ 

by letting $X^\sim(x, y)$ be the space of paths from $x$ to $y$. Two paths from $x$ to $y$ are homotopic if they lie in the same connected component of $X^\sim(x, y)$, so by applying the connected components functor, 

$$X_0 \times X_0 \stackrel{X^\sim}{\to} Top \stackrel{\Pi_0}{\to} Set$$ 

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

* Each cospan co-operation $\theta \in T_n = \hom(I, I^{\vee n})$ induces a span operation 
$$\hom(\theta, X): \hom(I^{\vee n}, X) \to \hom(I, X)$$
from the $n$-fold span composite to the span itself. 

Again, we could express this by saying we derive an $A_\infty$-[[A-infinity-category|category]] structure on the topological span (2), but in less fancy terms, the composition map 

$$\hom(I, I^{\vee n}) \times \hom(I^{\vee n}, X) \to \hom(I, X)$$ 

gives a $T$-algebra structure on the topological span: 

$$T_n \times (X \leftarrow X^I \to X)^{\otimes n} \to (X \leftarrow X^I \to X) \qquad (4)$$ 

where $\otimes$ indicates span composite. 

* **Remark**: $T$ is an operad in $Top$, not in the monoidal category $TopSpan(X, X)$. But we can make it an operad there by applying an evident change-of-base $Top \to TopSpan(X, X)$, sending a space $Y$ in $Top$ to the span 
$$X \stackrel{\pi}{\leftarrow} X \times Y \stackrel{\pi}{\to} X$$
This change of base is (strong) monoidal. As a matter of fact, this change of base factors through the center of the monoidal category $TopSpan$, which we actually need because one needs symmetries in order to express the notion of even a nonpermutative operad internal to a monoidal category. 

We get a similar $T$-algebra structure on the $Top$-graph $X^\sim: X_0 \times X_0 \to Top$ we started with. Indeed, the functor 

$$TopSpan(X, X) \to TopSpan(X_0, X_0) \cong TopGraph_{X_0} \qquad (3)$$ 

is a lax monoidal functor, and hence takes $T$-algebras in $TopSpan(X, X)$ (as in (4)) to $T$-algebras in $TopGraph_{X_0}$. This gives a $T$-algebra structure 

$$T_n \times (X^\sim)^{\otimes n} \to X^\sim \qquad (5)$$ 

in the monoidal category of $Top$-graphs. Considered geometrically, this is almost pure tautology, but **(5) is the crucial topological input in Trimble's machine**. 

Let us make this more explicit. In general, if $V$ is a monoidal category with coproducts, such that the tensor $u \otimes v$ preserves coproducts in each of its separate arguments $u$ and $v$, then the category of $V$-graphs also carries a monoidal structure, where for two $V$-graphs $G, H$ we define 

$$(G \otimes H)(x, z) = \sum_y G(x, y) \otimes H(y, z)$$ 

Hence, in the case $V = Top$, (5) takes the more explicit form 

$$T_n \times \sum_{y_1, \ldots, y_{n-1}} X^\sim(x, y_1) \times X^\sim(y_1, y_2) \times \ldots \times X^\sim(y_{n-1}, z) \to X^{\sim}(x, z) \qquad (6)$$ 

Now apply the functor $\Pi_0: Top \to Set$ (which preserves products and incidentally sums as well) to (6). This makes the $Set$-graph $\Pi_0 X^\sim$ an algebra over the operad $\Pi_0 T$. But a $Set$-graph equipped with a $\Pi_0 T$-algebra structure is just a category, since $\Pi_0 T_n$ consists of just a point, i.e., is the operad whose algebras are monoids, and a category is a monoid in a category of graphs. 

This category is precisely the fundamental groupoid $\Pi_1(X)$. It is pretty clear from this description that $\Pi_1(X)$ is functorial in $X$. Indeed, if $f: X \to Y$ is a continuous map, we can pull back the $Top$-graph $Y^\sim$ over $Y_0$ to a $Top$-graph over $X_0$, 

$$X_0 \times X_0 \stackrel{f_0 \times f_0}{\to} Y_0 \times Y_0 \stackrel{Y^\sim}{\to} Top,$$ 

which we call $f_0^{-1} Y^\sim$. The continuous map $f: X \to Y$ induces a comparison map of $T$-algebras in $TopGraph_{X_0}$, 

$$ f^*: X^\sim \to f_0^{-1} Y^\sim: X_0 \times X_0 \to Top $$ 

and again by composing with $\Pi_0: Top \to Set$, we get a map $ \Pi_0 f^*: \Pi_1(X) \to \Pi_1(Y) $, i.e., a functor between the fundamental groupoids. 

Thus, after a series of small tautological steps, we have bootstrapped our way up from $\Pi_0$ to $\Pi_1$. This same procedure suggests a way to bootstrap from $\Pi_1$ to a definition of $\Pi_2$, and so on up an $n$-categorical ladder. Here are the general inductive definitions: 

* A (flabby) 0-category is a set. The fundamental 0-groupoid $Top \to Flabby(0)Cat$ is the connected components functor $\Pi_0: Top \to Set$. 

* For $n \geq 0$, a **flabby $(n+1)$-category** consists of a set $X_0$ and a $Flabby(n)Cat$-graph 
$$X: X_0 \times X_0 \to Flabby(n)Cat$$ 
equipped with a structure of algebra over the operad $\Pi_n T$ (a priori an operad in the cartesian monoidal category $Flabby(n)Cat$, but made into an operad in $Flabby(n)CatGraph_{X_0}$ by an obvious change of base; cf. the remark above). 

* A **morphism** of flabby $(n+1)$-categories $(X_0, X) \to (Y_0, Y)$ consists of of a function $f_0: X_0 \to Y_0$ together with a _strict_ $\Pi_n T$-algebra map $f: X \to f_0^{-1} Y$. The category $Flabby(n+1)Cat$ admits finite products and arbitrary sums over which products distribute. 

* The **fundamental $(n+1)$-groupoid functor** 
$$\Pi_{n+1}: Top \to Flabby(n+1)Cat$$ 
sends a space $X$ to the pair $(X_0, \Pi_n X^\sim)$, seen as a $\Pi_n T$-algebra by applying the product-preserving functor $\Pi_n$ to the tautological $T$-algebra $X^\sim$. 

* **Theorem**: $\Pi_{n+1}$ preserves finite products and arbitrary coproducts. (This theorem is needed to push the induction through.)

And that's it. Notice this approach is in essence globular, that is we have an underlying functor 

$$U_n: Flabby(n)Cat \to (n)GlobularSet$$ 

to $n$-globular sets. This is defined by induction: the underlying $(n+1)$-globular set of a flabby $(n+1)$-category $(X_0, X)$ is given by 

$$X_0 \times X_0 \to Flabby(n)Cat \stackrel{U_n}{\to} (n)GlobularSet$$ 

using the fact that an $(n+1)$-globular set is naturally an $n$-globular graph over its set of 0-cells. In fact, Cheng has shown that flabby $n$-categories (and related structures; see the next section) are the algebras of a Batanin operad, that is a globular operad satisfying a contractibility condition. 

As Cheng put it, Trimble's inductive definition is disarmingly straightforward, and yet it codes up all the essential structure one expects to see in weak $n$-categories. For example, an associator for 2-categories is coded up as a 1-cell in $\Pi_1 T_3$, i.e., as a homotopy class of paths between two points in $\hom(I, I \vee I \vee I)$: 

$$(\delta \vee 1)\delta, (1 \vee \delta)\delta: [0, 1] \to [0, 3]$$ 

where $\delta: [0, 1] \to [0, 2]$ is a co-composition. The pentagonator is similarly coded up as a 2-cell in $\Pi_2 T_4$. And so on. 

To be continued...

+--{.query}
[[Urs Schreiber|Urs]]: Thanks, Todd, this is great. If I may, let me try, also to check if I am following, to see how much of this we can do while abstracting away from Top and the concrete interval object in there.

It seems that we need:

* a closed monoidal homotopical category $V$ (not your $V$ above, but I'll call it $V$ nevertheless);

* an object $I \in V$ fitting in an internal co-graph $pt \stackrel{\sigma, \tau}{\to} I$ such that

  * all the end-to-end pushouts $I^{\vee n}$ exist in $V$;
 
  * all the $V$-internal hom-objects $[I, I^{\vee n}]$ are weakly equivalent to the point (the terminal object) $[I, I^{\vee n}] \stackrel{\sim}{\to} pt$;

  * equipped with the structure of a co-operad internal to $V$ on $\{[I,I^{\vee n}]\}$, $n \in \mathbb{N}$.

Then

  * for $C$ any $V$-enriched homotopical category (I want to use now that $C$ is powered over $V$) we get &#8211; now let me see... &#8211; a functor
$$\Pi_{\omega}: C \to Trimble-\omega-Cat.$$

Hm, let me just let it stand this way for you to either erase all of this or maybe comment on it for the moment...

[[Todd Trimble|Todd]]: Yes, that's more or less right. But there is a god-given nonpermutative operad (not co-operad) structure on the graded $V$-object $\{[I, I^{\vee n}]\}$, and that's what I'm using here. If you know how the "endomorphism operad" works (as in the entry [[operad]]), then the operad here works the same way, mutatis mutandis. 

As for the last part: in the original definition, I didn't know how to pass to the full-fledged $\omega$-categorical definition; I just had $n$-categories, one for each $n$. But Tom and Eugenia figured out how to make "Trimble-like" $\omega$-categories work by using coalgebraic methods. I haven't thought about whether that allows a $\Pi_\omega$... But aside from these technicalities: yes, you seem to understand what this is all about. 

There were some comments to this effect after I gave that lecture; someone asked what you really need to do this definition very generally. Martin Hyland cried, "Not much!"

_[[Urs Schreiber]]:_ Okay, thanks. I tried now to formalize this at [[interval object]].

=--

+--{.query}
_[[Toby Bartels|Toby]]_ says:

This is interesting. I never looked at this definition before, and I need to give it some thought. Has it been extedned to $\infty$-categories?

Also, what is the proper name for these things? 'Trimble\'s notion of weak $n$-category' is a mouthful, but 'Trimble $n$-category' would work. Or 'flabby $n$-category', if that is unambiguous. (One might move this page, too, ... but only if it\'s clear where to move it!)

_[[Urs Schreiber|Urs]]:_ I am not enthusiastic about "flabby". "Trimble $\omega$-category" sounds good to me, though. $Trimble\omega Cat$.

_[[Todd Trimble|Todd]]_: The extension to $\infty$-categories was accomplished not too long ago by Tom Leinster and Eugenia Cheng, using coalgebra theory: 

[Terminal coalgebras](http://www-lmpa.univ-littoral.fr/CT08/slides/Cheng.pdf)

It's actually quite ingenious: as motivation, they start with Simpson's (Alex? Carlos?) observation that for the endofunctor $(-)-Cat: SymMonCat \to SymMonCat$ mapping $V \mapsto V-Cat$, the terminal coalgebra is (strict) $\omega$-Cat. Then they explain how this idea can be extended to produce Trimble-like weak $\omega$-categories (starting around page 57 of 124). 

As far as terminology goes: "flabby" was meant to accomplish several purposes: first to distinguish itself from "weak" (since at the time I wasn't convinced that these structures were truly weak enough, owing to the fact that we use strict maps of algebras along the way); second to recall the word "flab" as used by Frank Adams in his Infinite Loop Spaces book: there is rather a lot of topological flab in my original definition; third out of modesty. But I don't like it much now either (I think it partially violates my 'cutesy' rule). 

For now I'm okay with "Trimble $\omega$-Cat" or the like, but I'd very much welcome something new and snappy that conveys something of the spirit of this idea. 
=--

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

* $V_{n+1} = (V_n, P_n)-Cat$ 

for some series of operads $P_n$ valued in $V_n$. The operads $P_n$ in his definition came from one master operad $T$, by applying a product-preserving functor 

$$\Pi_n: Top \to V_n$$

to $T$. But other operads are possible; for the purposes of $n$-category theory, it is preferable to choose such operads that are contractible in some sense. 

#References#

* Eugenia Cheng, _Comparing operadic theories of $n$-category_ ([arXiv](http://arxiv.org/abs/0809.2070))

  * section 1.1: Trimble's original definition

  * section 1.2: A more general version of Trimble's definition