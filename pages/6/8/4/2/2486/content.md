#Contents#
* automatic table of contents
{:toc}


## Idea

A PRO, an abbreviation for "product category", is similar to a [[PROP]] but more general, being merely a monoidal category but not necessarily symmetric monoidal. They may be used to describe theories for finitary algebraic and coalgebraic structures which make sense in any monoidal category, for example monoids and comonoids. 

## Definitions 

A **PRO** is a strict monoidal category $T$ in which every object is of the form 

$$x^{\otimes n} = x \otimes \ldots \otimes x \qquad (product of n copies of x)$$

for some $n \geq 0$. Somewhat more precisely, a PRO is a strict monoidal category for which the unique strict monoidal functor 

$$(\mathbb{N}, +, 0) \to (T, \otimes, I)$$ 

is an isomorphism on objects. 

Morphisms $x^{\otimes m} \to x^{\otimes n}$ in a PRO are often thought of as operations which accept $m$ inputs and produce $n$ outputs, hence PROs are like nonpermutative operads but for the multiple outputs, which make them more general. 

Let $C$ be a monoidal category. A **$T$-model** in $C$ (or a $C$-representation of $T$) is a strong monoidal functor $F: T \to C$; the _underlying object_ of the $T$-model is the value $F(x)$. A $T$-model is thus an object $c$ of $C$ equipped with operations 

$$\theta_c: c^{\otimes m} \to c^{\otimes n},$$ 

one for each morphism $x^{\otimes m} \to x^{\otimes n}$, reflecting the monoidal category structure of $T$. A **homomorphism** $F \to G$ of $T$-models $F, G: T \to C$ is a monoidal transformation between $F$ and $G$; it may be equivalently expressed as a morphism $\phi: F(x) \to G(x)$ in $C$ which respects the modelings of the $T$-operations $\theta$. 

## Examples 

The [[simplex]] category $\Delta$ is a PRO whose models are [[monoid]]s in monoidal categories. Similarly, $\Delta^{op}$ is a PRO whose models are [[comonoid]]s. 

The [[cube]] category is a PRO whose models are objects $X$ equipped with "elements" $x_0, x_1: I \to X$ and a projection $p: X \to I$ which is a retraction of both $x_0$ and $x_1$, where $I$ denotes the monoidal unit. 

The monoidal category of planar thickened 1d tangles (is this the right vocabulary?) is a PRO whose models are noncommutative Frobenius objects in monoidal categories. 

## Variations 

Just as the notion of [[PROP]] is a symmetric monoidal analogue of PRO, there is a braided monoidal analogue called a **PROB**. The cartesian monoidal analogue is known as a [[Lawvere theory]]. 

More generally, given any [[doctrine]] $D$, let $I(D)$ be an initial algebra of the doctrine. A PRO-D can then be defined as an algebra $T$ such that the algebra map $I(D) \to T$ induces an isomorphism on objects. This is clearly an [[evil]] notion, and yet a useful and general one in practice. 
