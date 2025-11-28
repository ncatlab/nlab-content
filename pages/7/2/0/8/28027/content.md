
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

The trilinear maps are often reformulated as quadratic maps 

$$ Q_+ \colon V_+ \to \text{Hom}(V_-, V_+) $$
$$ Q_- \colon V_- \to \text{Hom}(V_+, V_-) .$$

For a simple example of a Jordan pair, let $V_+$ be a finite-dimensional vector space and $V_-$ the dual of that vector space, with the quadratic maps given by

$$ Q_+(v)(f) = f(v) \,v $$
$$ Q_-(f)(v) = f(v) \, f. $$

for $v \in V_+, f \in V_-$.

## Advantages 

Jordan pairs are more general than Jordan algebras.  Further, the connection between Jordan structures, 3-graded Lie algebras and bounded symmetric domains is arguably clearer in terms of Jordan pairs than using Jordan algebras or Jordan triple systems ([Loos77](#Loos77)). 

Isomorphisms of Jordan pairs are more general than isomorphisms of Jordan algebras or Jordan triple systems: they generalize the so-called "isotopies" of these.  An **isotopy** $f \colon V \to V'$ of Jordan triple systems is a pair of bijective linear maps $f_+, f_- \colon V \to V'$ such that

$$ f_+(\{u,v,w\}) = \{f_+(u), f_-(v), f^+(w) \} $$

for all $u,v,w \in V$.  The use of two separate linear maps is somewhat odd here, but natural for Jordan pairs.   An **isomorphism** from a Jordan pair $V_\pm$ to a Jordan pair $V'_\pm$ is a pair of bijective linear maps $f_\pm \colon V_\pm \to V'_\pm$ such that

$$ f_\pm\bigl(\{u,v,w\}_\pm\bigr) = \{f_\pm(u), f_\mp(v), f_\pm(w)\}_\pm  $$

for all $u,w \in V_\pm, v \in V_\mp$.

Unlike for Jordan algebras and Jordan triple systems, there is a natural way to define inner automorphisms of Jordan pairs ([Loos75](#Loos75)).   (See below for inner derivations.)

Furthermore, Jordan pairs always contain sufficiently many idempotents (which generalize the [[projection operators]] familiar in the case of self-adjoint complex matrices) ([Loos75](#Loos75)).  It may happen even in a finite-dimensional simple Jordan algebra that the unit element cannot be written as the sum of orthogonal division idempotents (the algebra need not have "capacity").  In a Jordan triple system the relevant generalization of an idempotent is a **tripotent**, an element $p$ with $\{p,p,p\} = p$, but if we make $\mathbb{R}$ into a Jordan triple system with $\{a,b,c\} = -(a b c + c b a)$ it has no nonzero tripotents.  In the case of a Jordan pair $(V_+, V_-)$, we define an **idempotent** to be a pair of elements $p_+ \in V_+, p_- \in V_-$ such that 

$$  \{p_\pm, p_\mp, p_\pm\}_\pm = p_{\pm} \, . $$

## Relation to 3-graded Lie algebras

A **3-graded Lie algebra** is a $\mathbb{Z}$-graded Lie algebra that vanishes except in grades -1, 0 and 1, say

$$ \mathfrak{g} = \mathfrak{g}_{-1} \oplus \mathfrak{g}_0\oplus \mathfrak{g}_1 \, .$$

Given any 3-graded Lie algebra, the pair of vector spaces $(\mathfrak{g}_{1}, \mathfrak{g}_{-1})$ becomes a Jordan pair with brackets

$$ \{a,b,c\}_\pm = [[a,b],c] $$

for $a,c \in \mathfrak{g}_{\pm 1}$ and $b \in \mathfrak{g}_{\mp 1}$.  

Conversely, there is a functorial way to build a 3-graded Lie algebra from a Jordan pair.  Start with a Jordan pair $(V_+, V_-)$.  We construct a 3-graded Lie algebra $\mathfrak{g} = \mathfrak{g}_{-1} \oplus \mathfrak{g}_0 \oplus \mathfrak{g}_1$ 
as follows.  First, set

$$ \mathfrak{g}_1 = V_+, \qquad \mathfrak{g}_{-1} = V_- $$

and let $\mathfrak{g}_0$ consist of the **inner derivations** of the Jordan pair.  These are linear maps $D \colon V_+ \oplus V_- \to V_+ \oplus V_-$ that are linear combinations of those of the form  

$$D(x, y) = (\{x, y, \cdot\}_+, -\{y, x, \cdot\}_-)$$

for $x \in V_+, y \in V_-$.  We write $D(x,y) = (D_+(x,y), D_-(x,y))$. 

Next, define a Lie bracket on $\mathfrak{g}$ as follows:

1) **$[\mathfrak{g}_1, \mathfrak{g}_{-1}] \to \mathfrak{g}_0$**: For $x \in V_+, y \in V_-$, set

$$[x, y] = D(x, y) = (Q(x, y, \cdot), -Q(y, x, \cdot))$$

2) **$[\mathfrak{g}_0, \mathfrak{g}_{\pm 1}] \to \mathfrak{g}_{\pm 1}$**: For $D = (D_+, D_-) \in \mathfrak{g}_0$, set

$$[D, x] = D_+(x) \; \text{ for } \; x \in V_+, \qquad [D, y] = D_-(y) \; \text{ for } \; y \in V_-$$

3) **$[\mathfrak{g}_0, \mathfrak{g}_0] \to \mathfrak{g}_0$**: Here we use the usual commutator of linear operators:

$$[(D_+, D_-), (E_+, E_-)] = ([D_+, E_+], [D_-, E_-]) \, .$$

4) **$[\mathfrak{g}_i, \mathfrak{g}_j] = 0$** when $|i + j| \gt 1$.

## Relation to Jordan triple systems

There is a way to see a [[Jordan triple system]] as a Jordan pair with extra structure, and vice versa ([McCrimmon78](#McCrimmon78)).  This suggests that there are adjoint functors between the category of Jordan triple systems and the category of Jordan pairs.

### Jordan triple systems as Jordan pairs with involutions

Define a **Jordan pair with involution** to be a Jordan pair $(V_\pm, \{\cdot, \cdot, \cdot\}_\pm)$ with a vector space isomorphism $\alpha \colon V_+ \to V_-$ such that 

$$ Q_-(\alpha(v)) = \alpha \circ Q_+(v) \alpha $$

for all $v \in V_+$, where $Q_\pm$ are the quadratic maps mentioned above.

The category of [[Jordan triple systems]] is equivalent to the category of Jordan pairs with involution ([Loos75](#Loos75)).  In this equivalence, a Jordan pair with involution gives a Jordan triple system $(V, \{\cdot,\cdot,\cdot\})$ with $V = V_+$ and 

$$ \{u,v,w\} = \{u,\alpha(v),w\}_+ \, . $$
 
Conversely, a Jordan triple system $(V, \{\cdot, \cdot, \cdot \})$ gives a Jordan pair $(V_\pm, \{\cdot, \cdot, \cdot\}_\pm)$ with $V_+ = V_- = V$ and 

$$ \{u,v,w\}_+ = \{u,v,w\}  \qquad for \; all \; u,w \in V_+, v \in V_- $$

$$ \{u,v,w\}_- = \{u,v,w\}  \qquad for \; all \; u,w \in V_-, v \in V_- \, . $$

This has an involution given by $\alpha = 1_V$.

### Jordan pairs as polarized Jordan triple systems

Define a **polarized Jordan triple system** to be a [[Jordan triple system]] $(V, \{\cdot, \cdot, \cdot\})$ together with a direct sum decomposition $V = V_+ \oplus V_-$ such that 

$$ \{u,v,w\}_\pm \in V_\pm $$

for all $u,w \in V_\pm, v \in V_\mp$ and 

$$ \{u,v,w\}_\pm = 0 $$

for all other possibilities, i.e. for all $u, v \in V_\pm$, $w \in V_\mp$, all $v, w \in V_\pm$, $u \in V_\mp$, and all $u, v, w \in V_\pm$.

The category of Jordan pairs is equivalent to the category of polarized Jordan triple systems ([Loos75](#Loos75)). 

## Related concepts

* [[Jordan algebra]]

* [[quadratic Jordan algebra]]

* [[Jordan triple system]]

* [[exceptional Jordan algebra]]/[[Albert algebra]]

## References

* {#Loos75} [[Ottmar Loos]]: _Jordan Pairs_, Lecture Notes in Mathematics **460** Springer (1975) &lbrack;ISBN:978-3-540-37499-2, [doi:10.1007/BFb0080843](https://doi.org/10.1007/BFb0080843), [ark:/13960/t9774fs7f ](https://archive.org/details/jordanpairs0000loos)&rbrack;

* {#Loos77} [[Ottmar Loos]]: _Bounded Symmetric Domains and Jordan Pairs_, Lecture notes, University of California (1977)

* {#McCrimmon78} Kevin McCrimmon, _Review: Ottmar Loos, Jordan pairs_, Bull. Amer. Math. Soc. **84** 4 (1978) 685-690 &lbrack;[euclid](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-84/issue-4/Review-Ottmar-Loos-Jordan-pairs/bams/1183540942.full)&rbrack;

[[!redirects Jordan pairs]]


