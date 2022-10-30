
# Contents 
* table of contents 
{: toc} 

## Introduction 

This article is about structure on a closed interval of real numbers, generally taken to be $I = [0, 1]$, that is derivable from a [[coalgebra of an endofunctor|coalgebraic]] perspective. This topic was introduced by [[Peter Freyd]]. 


## Coalgebraic description of $I$ 

For the moment we work [[classical mathematics|classically]], over the [[category of sets]]. A _bipointed set_ is a set equipped with two elements, that is a [[cospan]] of the form 

$$\array{
1 & & & & 1 \\
 & ^\mathllap{x_0} \searrow & & \swarrow^\mathrlap{x_1} & \\
 & & X & & 
}$$ 

where $x_0$ and $x_1$ might coincide. There is a [[monoidal category|monoidal product]] on $Cospan(1, 1)$ given by cospan composition (formed by taking [[pushouts]]); this monoidal product is denoted $\vee$. (Explicitly, $(X,x_0,x_1) \vee (Y,y_0,y_1)$ is $((X \uplus Y)/(x_1 \sim y_0), x_0, y_1)$.)  The monoidal unit is a $1$-element set with its unique bipointed structure. The category of such cospans or bipointed sets is denoted $Cos$. 

Inside $Cos$ is the full subcategory of _two-pointed_ sets, where $x_0$ and $x_1$ are distinct. Let $Twop$ be the category of two-pointed sets. The monoidal product $\vee$ restricts to a functor 

$$\vee \colon Twop \times Twop \to Twop$$ 

and one can define the square 

$$sq = (Twop \stackrel{\Delta}{\to} Twop \times Twop \stackrel{\vee}{\to} Twop)$$ 

A **$sq$-coalgebra** is a two-pointed set $X$ together with a map $\xi: X \to X \vee X$. An example is given by $I = [0, 1]$, where $I \vee I$ is identified with the interval $[0, 2]$ and the coalgebra structure $I \to I \vee I$ is identified with multiplication by $2$, $[0, 1] \to [0, 2]$. This map will be denoted $\alpha$. 

+-- {: .un_theorem} 
###### Theorem (Freyd) 
$(I, \alpha)$ is terminal in the category of $sq$-coalgebras. 
=-- 


## Corecursively defined operations on $I$ 

We now define a number of operations on $I$. For $0 \leq x \leq 1$, define ${x \uparrow} \coloneqq \min(2 x, 1)$ and ${x \downarrow} \coloneqq \max(2 x - 1, 0)$. These give unary operations on $I$ which can also be defined as maps in $Cos$ using the coalgebra structure $\alpha$: 

$$I \stackrel{{(-) \uparrow}}{\to} I = (I \stackrel{\alpha}{\to} I \vee I \stackrel{I \vee !}{\to} I \vee 1 \cong I)$$ 

$$\,$$ 

$$I \stackrel{{(-) \downarrow}}{\to} I  = (I \stackrel{\alpha}{\to} I \vee I \stackrel{! \vee I}{\to} 1 \vee I \cong I)$$ 

We similarly define unary operations ${(-)\uparrow}$, ${(-) \downarrow}$ for any $sq$-coalgebra $(X, \xi)$. For any coalgebra $X$ and $x \in X$, either ${x \downarrow} = x_0$ or ${x \uparrow} = x_1$. Moreover, if $i_0 \colon X \to X \vee X$ and $i_1 \colon X \to X \vee X$ are the evident pushout inclusions, we have $\xi(x) = i_0({x \uparrow})$ if ${x \downarrow} = x_0$, and $\xi(x) = i_1({x \downarrow})$ if ${x \uparrow} = x_1$. This means that coalgebra structures can be recovered from algebraic structures consisting of two constants $x_0, x_1$ and two unary operations $\uparrow$, $\downarrow$, although we must consider a coherent but non-algebraic axiom 

$$\vdash {x \uparrow} = x_1 or {x \downarrow} = x_0$$ 


### Order-theoretic operations 

Next, we define meet and join operations on $I$, making it a lattice, by exploiting corecursion. A slick corecursive definition of the order $\leq$ is that $x \leq y$ 

* if ${x \downarrow} = 0$ and ${x \uparrow} \leq {y \uparrow}$, or 

* if ${y \uparrow} = 1$ and ${x \downarrow} \leq {y \downarrow}$. 

If one prefers to work with operations, one could define the meet operation $\wedge \colon I \times I \to I$ by putting a suitable coalgebra structure on $I \times I$ and using terminality of the coalgebra $I$ to define $\wedge$ as a coalgebra map. A coalgebra structure 

$$\xi \colon I \times I \to (I \times I) \vee (I \times I)$$ 

which works is 

* $\xi(x, y) = i_0({x \uparrow}, {y \uparrow})$ if ${x \downarrow} = 0$ or ${y \downarrow} = 0$; 

* $\xi(x, y) = i_1({x \downarrow}, {y \downarrow})$ if ${x \uparrow} = 1 = {y \uparrow}$. 


### Midpoint operations 

The general midpoint operation is not as easy to construct as one might think, but to start with we do have operations which take the midpoint between a given point and an endpoint. Namely, the left midpoint operation is the unary operation defined by 

$$l = (I \stackrel{i_0}{\to} I \vee I \stackrel{\alpha^{-1}}{\to} I)$$ 

and the right midpoint operation is defined by 

$$r = (I \stackrel{i_1}{\to} I \vee I \stackrel{\alpha^{-1}}{\to} I).$$


## Constructive aspects

There are two versions of this construction, classically equivalent, in [[constructive mathematics]], one of which produces the unit interval of [[MacNeille real numbers]], the other of which produces the unit interval of [[located Dedekind real numbers]].  Both start with $Cos$ (which is straightforward) but define $Twop$ differently, and the monoidal product $\vee$ is subtler.

For the MacNeille real numbers, define $Twop_M$ in the most obvious way,
$$ \neg\; x_0 = x_1 .$$
For the Dedekind real numbers, define $Two_D$ by requiring
$$ \forall x,\; \neg\; x = x_0 \;\vee\; \neg\; x = x_1 .$$
(The two statements are equivalent assuming the classical [[de Morgan law]] $\neg(p \wedge q) \Rightarrow \neg{p} \vee \neg{q}$, but the latter is stronger in [[intuitionistic logic]].)

In $Cos$, let $X \vee Y$ be a [[subset]] of $X \times Y$, with $(x,y) \in X \vee Y$ iff
$$ (\neg\; x = x_1 \;\Rightarrow\; y = y_0) \;\wedge\; (\neg\; y = y_0 \;\Rightarrow\; x = x_1) .$$
(A pushout can be constructed using $x = x_1 \;\vee\; y = y_0$ instead; this is stronger in intuitionistic logic but equivalent assuming [[excluded middle]].  If equality happens to be [[stable proposition|stable]] in $X$ and $Y$, then only the classical de Morgan law is needed to make this a pushout.)

As in the classical case, this makes $Twop_M$ and $Twop_D$ into "[[semigroup]]al" categories ([[monoidal categories]] but without the monoidal unit), since the unit object (which exists in $Cos$ as the [[singleton]]) does not exist in $Twop_M$ or in $Twop_D$, but we can still define $sq_M$ and $sq_D$ and consider their coalgebras.  As stated above, $[0,1]_M$ is the final coalgebra of $sq_M$, and $[0,1] = [0,1]_D$ is the final coalgebra of $sq_D$; both are equipped with $0$ and $1$.

Another approach to the Dedekind real interval looks simpler from the perspective of [[constructive analysis]].  Start with $Set_\#$, the category of $T_0$ [[point–point apartness spaces]] and [[strongly extensional functions]] between them.  (A point--point apartness space is a set equipped with an [[apartness relation]], that is a binary relation $\#$ satisfying properties [[de Morgan duality|dual]] to those of an equivalence relation; it is $T_0$ iff the apartness relation is [[tight relation|tight]]; and a function between such spaces is strongly extensional iff it reflects $#$.)  On $Cos_\#$, let $X \vee Y$ be the subset of $X \times Y$ satisfying
$$ (x \# x_1 \;\Rightarrow\; y = y_0) \;\wedge\; (y \# y_0 \;\Rightarrow\; x = x_1) .$$
Define $Twop_\#$ by
$$ x \# x_0 \;\vee\; x \# x_1 .$$
Now defining $sq_\#$ on $Twop_\#$, its final coalgebra is again the Dedekind unit interval (equipped with its endpoints).


## Computational aspects

... explain how the classical version corresponds to computation with (unsigned) binary digits ... the constructive (Dedekind) version corresponds to computation with signed binary digits ...


## References 

The original development by Freyd is

* [[Peter Freyd]], _Real coalgebra_, post to the categories list, December 22, 1999 ([web](http://facultypages.ecc.edu/alsani/ct99-00%288-12%29/msg00039.html))

The constructive version is also due to Freyd:

* [[Peter Freyd]], _Reality Check_, post to the categories list, July 31, 2000 ([web](http://facultypages.ecc.edu/alsani/ct99-00%288-12%29/msg00200.html)) 

Freyd published 8 years later:

* [[Peter Freyd]], _Real Algebraic Analysis_, TAC **20** no.10 (2008) pp. 215--306. ([web](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

There is also a complete development in the [[Elephant]]:

* [[Peter Johnstone]], _Sketches of an Elephant_, following 4.7.14.


[[!redirects real coalgebra]]
[[!redirects coalgebra of the real interval]]
[[!redirects coalgebra of the real numbers]]
[[!redirects coalgebra of real numbers]]
