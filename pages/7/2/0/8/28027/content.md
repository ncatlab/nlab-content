
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


\tableofcontents


## Idea

As a further development of the concept of [[Jordan algebra]], a [[Jordan triple system]] axiomatizes the properties of the Jordan triple product

$$  
  \{a,b,c\} 
    \;=\; a b c + c b a 
  \,.
$$

of self-adjoint complex matrices.  However, this triple product also makes sense when $a$ and $c$ are of a different type than $b$. For example, it makes sense when $a$ and $c$ are $m \times n$ matrices and $b$ is an $n \times m$ matrix, or vice versa.  Thus, it turns out to be useful to generalize Jordan triple systems to **Jordan pairs**.  The theory of bounded symmetric domains has been developed by Ottmar Loos using Jordan pairs ([Loos77](#Loos77)).

## Definition

A **Jordan pair** is a pair of vector spaces $V_+$ and $V_-$ together with a pair of trilinear maps

$$ \{\cdot,\cdot,\cdot\}_+ \colon V_+ \times V_- \times V_+ \to V_+ \, , $$
$$  \{\cdot,\cdot,\cdot\}_- \colon V_- \times V_+ \times V_- \to V_- \, . $$

obeying two symmetry axioms

$$ \{u,v,w\}_\pm = \{w,v,u\}_\pm $$

and two Jacobi-like axioms

$$
  \big\{a,b,\{c,d,e\}_\pm \big\}_\pm - \big\{c,d,\{a,b,e\}_\pm \big\}_\pm 
    \;=\; 
  \big\{\{a,b,c\}_\pm ,d,e\big\}_\pm - \big\{c,\{b,a,d\}_\mp,e\big\}_\pm
  \,.
$$

This definition works well over any field or even commutative ring that is not of characteristic 2 or 3.

## Advantages 

Jordan pairs are more general than Jordan algebras.  Further, the connection between Jordan structures, 3-graded Lie algebras and bounded symmetric domains is arguably clearer in terms of Jordan pairs than using Jordan algebras or Jordan triple systems ([Loos77](#Loos77)). 

Unlike for Jordan algebras and Jordan triple systems, there is a natural way to define inner automorphisms of Jordan pairs 
([Loos75](#Loos75)).   (See below for inner derivations.)

Furthermore, Jordan pairs always contain sufficiently many idempotents (which generalize the [[projection operators]] familiar in the case of self-adjoint complex matrices) ([Loos75](#Loos75)).  It may happen even in a finite-dimensional simple Jordan algebra that the unit element cannot be written as the sum of orthogonal division idempotents (the algebra need not have "capacity").  In a Jordan triple system the relevant generalization of an idempotent is a **tripotent**, an element $p$ with $\{p,p,p\} = p$, but if we make $\mathbb{R}$ into a Jordan triple system with $\{a,b,c\} = -(a b c + c b a)$ it has no nonzero tripotents.  In the case of a Jordan pair $(V^+, V^-)$, we define an **idempotent** to be a pair of elements $p_+ \in V^+, p_- \in V^-$ such that 

$$  \{p_\pm, p_\mp, p_\pm\}_\pm = p_{\pm} \, . $$

## Relation to 3-graded Lie algebras

A **3-graded Lie algebra** is a $\mathbb{Z}$-graded Lie algebra that vanishes except in grades -1, 0 and 1, say

$$ \mathfrak{g} = \mathfrak{g}_{-1} \oplus \mathfrak{g}_0\oplus \mathfrak{g}_1 \, .$$

Given any 3-graded Lie algebra, the pair of vector spaces $(\mathfrak{g}_{1}, \mathfrak{g}_{-1})$ becomes a Jordan pair with brackets

$$ \{a,b,c\}_\pm = [[a,b],c] $$

for $a,c \in \mathfrak{g}_{\pm 1}$ and $b \in \mathfrak{g}_{\mp 1}$.  

Conversely, there is a functorial way to build a 3-graded Lie algebra from a Jordan pair.  Start with a Jordan pair $(V^+, V^-)$.  We construct a 3-graded Lie algebra $\mathfrak{g} = \mathfrak{g}_{-1} \oplus \mathfrak{g}_0 \oplus \mathfrak{g}_1$ 
as follows.  First, set

$$ \mathfrak{g}_1 = V^+, \qquad \mathfrak{g}_{-1} = V^- $$

and let $\mathfrak{g}_0$ consist of the **inner derivations** of the Jordan pair.  These are linear maps $D \colon V^+ \oplus V^- \to V^+ \oplus V^-$ of the form  

$$D(x, y) = (\{x, y, \cdot\}, -\{y, x, \cdot\})$$

for $x \in V^+, y \in V^-$.  We write $D(x,y) = (D^+(x,y), D^-(x,y))$. 

Next, define a Lie bracket on $\mathfrak{g}$ as follows:

1) **$[\mathfrak{g}_1, \mathfrak{g}_{-1}] \to \mathfrak{g}_0$**: For $x \in V^+, y \in V^-$, set

$$[x, y] = D(x, y) = (Q(x, y, \cdot), -Q(y, x, \cdot))$$

2) **$[\mathfrak{g}_0, \mathfrak{g}_{\pm 1}] \to \mathfrak{g}_{\pm 1}$**: For $D = (D^+, D^-) \in \mathfrak{g}_0$, set

$$[D, x] = D^+(x) \; \text{ for } \; x \in V^+, \qquad [D, y] = D^-(y) \; \text{ for } \; y \in V^-$$

3) **$[\mathfrak{g}_0, \mathfrak{g}_0] \to \mathfrak{g}_0$**: Here we use the usual commutator of linear operators:

$$[(D^+, D^-), (E^+, E^-)] = ([D^+, E^+], [D^-, E^-]) \, .$$

4) **$[\mathfrak{g}_i, \mathfrak{g}_j] = 0$** when $|i + j| \gt 1$.

## Related concepts

* [[Jordan algebra]]

* [[Jordan triple system]]

* [[Jordan-Lie-Banach algebra]]

* [[JBW-algebra]], [[JBW-algebraic quantum mechanics]]

* [[Kantor-Koecher-Tits construction]]

* [[order-theoretic structure in quantum mechanics]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[W-algebra]]

* [[Jordan superalgebra]]

* [[exceptional Jordan algebra]]/[[Albert algebra]]

## References

* {#Loos75} [[Ottmar Loos]]: _Jordan Pairs_, Lecture Notes in Mathematics **460** Springer (1975) &lbrack;ISBN:978-3-540-37499-2, [doi:10.1007/BFb0080843](https://doi.org/10.1007/BFb0080843), [ark:/13960/t9774fs7f ](https://archive.org/details/jordanpairs0000loos)&rbrack;

* {#Loos77} [[Ottmar Loos]]: _Bounded Symmetric Domains and Jordan Pairs_, Lecture notes, University of California (1977)


[[!redirects Jordan pairs]]


