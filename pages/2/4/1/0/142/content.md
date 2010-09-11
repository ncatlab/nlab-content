
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

* [[sheaf]]

* [[2-sheaf]] / **stack**

* [[(∞,1)-sheaf]] / [[∞-stack]]


***


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _stack_ is the one-step [[vertical categorification]] of a [[sheaf]]: it is a [[2-sheaf]].

Or rather, it is the half-categorification of a sheaf where the _codomain_ is categorified (from [[Set]] to [[Cat]] or [[Grpd]]). If also the domain (the [[site]]) is categorified, one speaks of a [[derived stack]].

Since the full $\infty$-categorification of "[[sheaf]]" is [[∞-stack]], a stack is conversely an [[∞-stack]] which happens to be 1-truncated.

From this $\infty$-point of view it seems a bit pointless to say "stack" instead of "2-sheaf" and accordingly for instance in [[Higher Topos Theory|HTT]] the term [[(infinity,1)-sheaf|∞-sheaf]] is used instead of $\infty$-stack.

More concretely this means that a stack on a [[site]] $S$ is 

* a ([[pseudofunctor|pseudo]]-)[[functor]] from  $S^{op}$ to the 2-category [[Cat]] of categories or [[Grpd]] of groupoids;

* that satisfies [[descent]].

In the latter case, the stack is sometimes referred to as a stack of groupoids. This is the more commonly occurring case so the term 'stack' has come to mean 'stack of groupoids' in much of the literature. 

In some circles the notion of a stack as a generalized groupoid is almost more familiar than the notion of sheaf as a [[space and quantity|generalized space]]. For instance [[differentiable stacks]] have attracted much attention in the study of [[Lie groupoids]] and [[orbifolds]], while [[diffeological space]]s are only beginning to be investigated more in [[Lie theory]]. 


## Provisional discussion

The following is "provisional" material on stacks that [[Todd Trimble]] wrote in the course of a discussion with [[Urs Schreiber|Urs]]. Somebody should turn this here into a coherent entry on stacks.

***

(Todd speaking.) I don't really speak "stacks", but in an effort to build a bridge between sheaves and stacks, I'll write down what I thought I understood, and ask someone such as Urs to come in and check. (Warning: I'm treating this edit box almost as a sandbox, in that what I say below is all a bit provisional until we get some discussion going.) 

+--{.query}
 Hi Todd, thanks for this. I started making some remarks on the relation between descent $\infty$-categories and pseudofunctors from [[covers]] regarded as [[sieves]] (hence as presheaves) at [[descent and codescent]] in the section titled _Descent in terms of pseudo-functors_.
=--

At the simplest level, let $C$ be a category. As we know, a presheaf on $C$ is just a functor $X: C^{op} \to Set$. 

Now let's categorify just once: regard a category $C$ as a bicategory whose local hom-categories are discrete. What I'll call a "pre-stack" is then a homomorphism of bicategories $X: C^{op} \to Cat$. Here I'm following Street's terminology: a homomorphism of bicategories is the "pseudo" version of a weak map of bicategories, as opposed to the "lax" version. So, we have given coherent isomorphisms $X(f)X(g) \to X(f g)$, and so on.  

Now suppose that $C$ also comes equipped with a topology $J$, and let $F$ be a $J$-covering sieve for $c$, so that in particular it's a subfunctor $i: F \hookrightarrow \hom(-, c)$. We want to build a (truncated) simplicial object out of this, and to this end I'll use some yoga which was basically developed in my Cafe post [on the bar construction](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html) [perhaps this may go partway to addressing your most recent [query](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html#c021027) there, Urs]. 

Namely, there is a canonical way of presenting $F$ as a colimit of representables. Officially, it's given by a coend formula, but it's probably more illuminating to think of it in terms of tensor products over $C$: 

$$\hom_C(-, -) \otimes_C F(-) \cong F(-)$$ 

In the long-winded version, this says that $F$ is the coequalizer of a diagram having the form 

$$\sum_{c, d} \hom_C(-, c) \times \hom_C(c, d) \times F(d) \stackrel{\to}{\to} \sum_c \hom_C(-, c) \times F(c) \to F(-)$$ 

where the more visible one of the two parallel arrows involves the contravariant action of $C$ on $F$: 

$$\hom(c, d) \times F(d) \to F(c)$$ 

and the less visible one uses $C$ acting on itself: 

$$\hom(-, c) \times \hom(c, d) \times F(d) \to hom(-, d) \times F(d)$$ 

The point now is that this coequalizer diagram represents the tail end of a simplicial object (with $F(-)$ appearing in dimension -1), which in the notation of the bar construction one could call $B(C, C, F)$. Let me explain this last bit. 

The point is that any category $C$ can be regarded as a monad in the bicategory of spans. The underlying span is of course 

$$C_0 \stackrel{dom}{\leftarrow} C_1 \stackrel{cod}{\to} C_0$$ 

and a presheaf $F$ on $C$, as a discrete op-fibration, has an underlying span 

$$C_0 \leftarrow F \to 1$$ 

and is precisely an algebra over the monad $C$. Then, given the data of a monad and an algebra over that monad, one proceeds to build the bar construction as a simplicial object, and I think this is probably the simplicial thingy we want to base the category of descent data on (given a pre-stack $X$). 

In fact, if memory serves the category of descent data can be efficiently expressed in bicategorical language as follows. The covering sieve $F$ becomes a homomorphism of bicategories by changing base from $Set$ to $Cat$: 

$$C^{op} \stackrel{F}{\to} Set \stackrel{discrete}{\to} Cat$$ 

and, abbreviating $discrete$ to $d$, it turns out that 

$$Desc_F(X) \simeq Nat(d F, X)$$ 

where the thing on the right side is the category of strong (i.e., pseudo) natural transformations between the indicated bicategory homomorphisms. 

In that case, the stack condition on $X$ becomes the statement that the canonical functor 

$$X(c) \stackrel{Yoneda}{\cong} Nat(d \hom(-, c), X) \to Nat(d F, X)$$ 

(where the first equivalence comes from the bicategorical Yoneda lemma, and the second functor is induced from the subfunctor $i: F \to \hom(-, c)$) is an equivalence for all $J$-covering sieves $F$. This formulation connects up nicely, that is, is a straight categorification of what was put down in the entry [[sheaf]]. 

## Related concepts

Special kinds of stacks include

* [[geometric stack]]s;

* [[gerbe]]s.

## References

Introductory material is

* [[Jochen Heinloth]], _Some notes on differentiable stacks_ ([pdf](http://www.uni-due.de/~hm0002/stacks.pdf))

* [[Ieke Moerdijk]], _Introduction to the language of stacks and gerbes_ ([arXiv](http://arxiv.org/abs/math/0212266))

The article

 * [[Angelo Vistoli]], _Notes on Grothendieck topologies, fibered categories and descent theory_ ([arXiv](http://arxiv.org/abs/math/0412512))

discusses stacks focussing on their dual incarnation as [[Grothendieck fibration]]s.

A [[model category]] presentation of stacks that mimics the way the [[model structure on simplicial presheaves]] models [[∞-stack]]s is discussed in

* [[Sharon Hollander]], _A homotopy theory for stacks_ ([arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247))

[[!redirects stack*]]
[[!redirects stacks]]