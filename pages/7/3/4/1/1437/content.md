[[!redirects terminal coalgebra of an endofunctor]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--




# Terminal coalgebras
* table of contents
{: toc}

## Introduction

A __terminal coalgebra__, also called __final coalgebra__, for an [[endofunctor]] $F$ on a category $C$ is a [[terminal object]] in the category of [[coalgebra for an endofunctor|coalgebras]] of $F$.

If $F$ has a terminal coalgebra $\alpha\colon X \to F(X)$, then $X$ is isomorphic to $F(X)$ (see below); in this sense, $X$ is a fixed point of $F$.  Being terminal, $X$ is the largest fixed point of $F$ in that there is a map to $X$ to any other fixed point (indeed, any other coalgebra), and this map is an [[injection]] if $C$ is [[Set]].

The dual concept is [[initial algebra]]. Just as initial algebras allow for [[induction]] and [[recursion]], so terminal coalgebras allow for [[coinduction]] and [[corecursion]].


## Details

Given two coalgebras $(x, \eta: x \to F x)$, $(y, \theta: y \to F y)$, a coalgebra map is a morphism $f: x \to y$ which respects the coalgebra structures: 

$$\theta \circ f = F(f) \circ \eta$$

A **terminal coalgebra** (usually called a _final coalgebra_ in the literature) is of course a terminal object in the category of coalgebras. Many data structures can be expressed as terminal coalgebras of suitable endofunctors; a simple but useful theorem says that terminal coalgebras $x$ are "fixed points" of their endofunctors, in that $F x \cong x$. This is the dual form of a theorem discovered long ago by Lambek: 

+-- {: .num_theorem}
###### Theorem

If $(x, \theta: x \to F x)$ is a terminal object in the category of $F$-coalgebras, then $\theta$ is an isomorphism. 
=--

+-- {: .proof}
###### Proof

Define a coalgebra structure on $F x$ by $F\theta: F x \to F F x$. By terminality of $x$, there is a unique coalgebra map $f: F x \to x$. We claim this is inverse to $\theta$. Indeed, by how we defined the coalgebra structure on $F x$, it is tautological that $\theta$ is a coalgebra map. By terminality of $x$ again, this gives an equation of coalgebra maps:

$$f \circ \theta = 1_x.$$

On the other hand, 

$$\theta \circ f = F(f) \circ F(\theta) = F(f \circ \theta) = F(1_x) = 1_{F x}$$

where the first equation holds because $f$ is a coalgebra map. This completes the proof.
=--

To construct terminal coalgebras, the following result is useful and practical. See [[Adámek's theorem on terminal coalgebras]] for an extension of this result. 

+-- {: .num_theorem}
###### Theorem (Ad&#225;mek)

If $C$ has a terminal object $1$ and the limit $L$ of the diagram 

$$\ldots F^3 1 \stackrel{F^2 !}{\to} F^2 1 \stackrel{F !}{\to} F 1 \stackrel{!}{\to} 1 \qquad (1)$$ 

exists in $C$ and $F$ preserves this limit, then the limit 
carries a structure of terminal coalgebra. 
=--

+-- {: .proof}
###### Proof

Let $\pi_n: L \to F^n 1$ be the $n^{th}$ projection of the limiting cone. Then we have a cone from $F L$ to the diagram (1) whose components are 

$$F L \stackrel{F\pi_n}{\to} F^{n+1} 1 \stackrel{F^n !}{\to} F^n 1$$ 

and the induced map $F L \to L$ to the limit is invertible by hypothesis; let $\theta: L \to F L$ be the inverse. We claim the coalgebra $(L, \theta)$ is terminal. 

Indeed, suppose $(x, \eta: x \to F x)$ is any coalgebra. We recursively define maps $f_n: x \to F^n 1$: let $f_0: x \to 1$ be the unique map, and 

$$f_{n+1} = F(f_n) \circ \eta$$ 

It is easily checked by induction that we have a commutative diagram 

$$\array{
F^{n+1}1 & \stackrel{F^n !}{\to} & F^n 1 \\
 ^\mathllap{F f_n} \uparrow & \nwarrow  ^\mathrlap{f_{n+1}} & \uparrow ^\mathrlap{f_n} \\
F x & \underset{\eta}{\leftarrow} & x
}$$ 

defining a cone from $x$ to the diagram (1), and inducing a map $f: x \to L$ such that the following diagram commutes: 

$$\array{
F L & \stackrel{\theta^{-1}}{\to} & L \\
 ^\mathllap{F f} \uparrow & & \uparrow  ^\mathrlap{f} \\
F x & \underset{\eta}{\leftarrow} & x
}$$ 

This diagram gives the fact that $f$ is a coalgebra map. Moreover, any coalgebra map $f: x \to L$ leads to a sequence $f_n = \pi_n \circ f$ that satisfies $f_{n+1} = F(f_n) \circ \eta$, by gluing the second diagram to the commutative diagram 

$$\array{
F^{n+1}1 & \stackrel{F^n!}{\to} & F^n 1 \\
 ^\mathllap{F \pi_n} \uparrow & \nwarrow  ^\mathrlap{\pi_{n+1}} & \uparrow  ^\mathrlap{\pi_n} \\
F L & \underset{\theta^{-1}}{\to} & L
}$$ 

so that we were forced to define the $f_n$ by recursion as we did, and the coalgebra map $f: x \to L$ is therefore uniquely determined. 
=-- 


## Examples 

### Unit interval in the real line
 {#UnitInterval}

As first observed by [[Peter Freyd]], the [[unit interval]] $[0, 1] \hookrightarrow \mathbb{R}$ inside the [[real line]] can be characterized as a suitable terminal coalgebra. There are various ways of realizing this; we give one (but see remarks below). 

Consider the [[category]] of [[intervals]] $Int$, i.e., linearly ordered sets with separate [[top]] and [[bottom]] elements $1$ and $0$, and let 

$$F\colon Int \to Int$$ 

be the endofunctor which takes an interval $X$ to $X \vee X$, the linear order obtained by taking two copies of $X$ and gluing the top element of the first copy to the bottom element of the second. The real interval $[0, 1]$ becomes a coalgebra if we identify $[0, 1] \vee [0, 1]$ with $[0, 2]$ and consider the multiplication-by-2 map $[0, 1] \to [0, 2]$ as giving a coalgebra structure. 

+-- {: .num_theorem} 
######Theorem 
The interval $[0, 1]$ is terminal in the category of coalgebras. 
=-- 

+-- {: .proof} 
######Proof (sketch) 
Given any coalgebra structure $f: X \to X \vee X$, any value $f(x)$ lands either in the "lower" half (the first $X$ in $X \vee X$), the "upper" half (the second $X$ in $X \vee X$), or at the precise spot between them, where the top element in the first copy is glued to the bottom element of the second. Intuitively, one could think of a coalgebra structure $\theta: X \to X \vee X$ as giving an automaton where on input $x_0$ there is output of the form $(x_1, h_1)$, where $h_1$ is either "upper", "lower", or "between". By iteration, this generates a behavior stream $(x_n, h_n)$. Interpreting upper as 1 and lower as 0, the $h_n$ form a binary expansion to give a number between 0 and 1, and therefore we have an interval map $X \to [0, 1]$ which sends $x_0$ to that number. Of course, should we ever hit $(x_n, between)$, we have a choice to resolve it as either $(bottom_X, upper)$ or $(top_X, lower)$ and continue the stream, but these streams are identified, and this corresponds to the identification of binary expansions 

$$.h_1... h_{n-1} 100000... = .h_1... h_{n-1}011111...$$ 

as real numbers. In this way, we produce a unique well-defined interval map $X \to [0, 1]$, so that $[0, 1]$ is the terminal coalgebra. 
=-- 

+-- {: .num_remark}
###### Remarks 
(More material can be found at [[coalgebra of the real interval]].) 

1. The same proof shows that we could have considered instead the category of [[poset|posets]] with separate top and bottom, or even the category of sets with separate top and bottom, with an analogous endofunctor. The reason we chose the category of intervals is (besides the availability of the succinct term 'interval') to indicate that choice of interval $[0, 1]$, 
as the model which classifies the [[geometric realization]] functor, can be justified on the grounds of a universal property, as shown by this theorem. 

1. Freyd, in his original [post](#Freyd) on this result, was inspired by a similar theorem due to [Pavlovic and Pratt](#PP), that the half-open interval $[0, \infty)$ can be described as the terminal coalgebra for the endofunctor that sends a linearly ordered set $X$ to $\omega \times X$ with the dictionary order. 

1. The theorem holds in an arbitrary topos (with $[0, 1]$ being the interval of [[real number object|Dedekind reals]]), provided that the word "separate" is interpreted correctly: 
$$\forall p\colon P\; (\neg(0 = p) \vee \neg(1 = p))$$ 
and provided that the process of gluing endpoints is given correctly. See Johnstone's [[Elephant]], section D.4.7, for an extended discussion. 

=--

### Categorified example: Trees 

The notion of terminal coalgebra may be categorified. For example, given a 2-category $C$ and a (pseudo) functor $F: C \to C$, one may speak of a 2-terminal (pseudo) coalgebra. 

A theoretically important example is the [[tree|category of trees]], seen as a 2-terminal coalgebra for the endofunctor on $Cat$ which takes a locally small category $C$ to its small-coproduct cocompletion. Further discussion of this point is given at [[pure set]]. 

The small-coproduct cocompletion of $C$ is given by a comma category construction: objects are pairs $(X, F: X_d \to C)$ where $X$ is a set and $F$ is a functor whose domain is the discrete category on $X$, denoted $X_d$. A morphism from $(X, F)$ to $(Y, G)$ is a pair $(f, \Phi)$ where $f: X \to Y$ is a function and $\Phi: F \to G \circ f_d$ is a natural transformation. This category is denoted $Set \wr C$; it is called a "[[categorical wreath product]]" (see also the discussion at [[club]]). 

Ad&#225;mek's theorem may be adapted to this 2-categorical situation. The iterated [[categorical wreath product|wreath product]] $(Set \wr)^n 1$ may be identified with the category of $n$-stage trees: 

$$(Set \wr)^n 1 = Set^{[n]^{op}}$$ 

where $[n]$ is the linear order $1 \leq 2 \leq \ldots \leq n$. Or, what is the same, the category of presheaves $T: [n+1]^{op} \to Set$ with the condition that $T(0) = 1$ is terminal; the element of $T(0)$ is considered to be the root of the tree. 

Indeed, we realize an explicit equivalence 

$$\Sigma: Set \wr Set^{[n]^{op}} \simeq Set^{[n+1]^{op}}$$ 

by defining $\Sigma(X, F: X \to Set^{[n]^{op}})$ to be the functor $T: [n+1]^{op} \to Set$ that on the object level takes $1$ to $X$, and $i+1$ to 

$$\sum_{x \in X} F(x)(i).$$ 

On the morphism level, $T(i+1 \to i)$ is the coproduct of morphisms 

$$\sum_{x \in X} F(x)(i \to i-1)$$ 

(and this makes sense for all $1 \leq i \leq n$ under the convention $F(x)(0) = 1$). 

The morphism 

$$(Set \wr)^n !: (Set \wr)^n Set \to (Set \wr)^n 1$$ 

used in Ad&#225;mek's theorem is identified with the restriction functor 

$$Set^{[n+1]^{op}} \to Set^{[n]^{op}}$$ 

which restricts presheaves along the inclusion $[n] \hookrightarrow [n+1]$. 

The 2-limit of the diagram in Ad&#225;mek's theorem is then 

$$Set^{\omega^{op}},$$ 

aka the [[tree|category of trees]], where $\omega$ is the colimit of the finite ordinals $[n]$. The statement that the category of trees is equivalent to its small-coproduct cocompletion says that the category of trees is equivalent to the category of forests. 

## Related concepts

Terminal coalgebras are the [[categorical semantics]] of [[coinductive types]], for instance [[M-types]].

## References 

* [[Peter Freyd]], _Real coalgebra_ Mailing to the categories list, Dec. 22, 1999. ([link](http://www.mta.ca/~cat-dist/catlist/1999/realcoalg))
{#Freyd}

* [[Dusko Pavlovic]], [[Vaughan Pratt]], _On coalgebra of real numbers_, 1999. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.47.5204))
{#PP}

Cross-relations between algebraic and coalgebraic aspects of real numbers may be found in this article: 

* [[Peter Freyd]], _Algebraic Real Analysis, Theor._ Appl. Cat., vol. 20, no. 10 (2008), 215-308. ([link](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))


[[!redirects terminal coalgebra]]
[[!redirects terminal coalgebras]]
[[!redirects final coalgebra]]
[[!redirects final coalgebras]]

[[!redirects terminal coalgebra of an endofunctor]]
[[!redirects terminal coalgebras of an endofunctor]]

[[!redirects terminal coalgebra]]