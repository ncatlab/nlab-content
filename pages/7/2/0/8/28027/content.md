
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

of self-adjoint complex matrices.  However, this triple product also makes sense when $a$ and $c$ are of a different type than $b$. For example, it makes sense when $a$ and $c$ are $m \times n$ matrices and $b$ is an $n \times m$ matrix, or vice versa.  Thus, it turned out to be useful to generalize Jordan triple systems to **Jordan pairs**.

## Definition

A Jordan pair is a pair of vector spaces $V_+$ and $V_-$ together with a pair of trilinear maps

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

## Relation to 3-graded Lie algebras

A **3-graded Lie algebra** is a $\mathbb{Z}$-graded Lie algebra that vanishes except in grades -1, 0 and 1, say

$$ \mathfrak{g} = \mathfrak{g}_{-1} \oplus \mathfrak{g}_0\oplus \mathfrak{g}_1 \, .$$

Given any 3-graded Lie algebra, the pair of vector spaces $(\mathfrak{g}_{1}, \mathfrak{g}_{-1})$ becomes a Jordan pair with brackets

$$ \{a,b,c\}_\pm = [[a,b],c] $$

for $a,c \in \mathfrak{g}_{\pm 1}$ and $b \in \mathfrak{g}_{\mp 1}$.  Conversely there is a functorial way to build a 3-graded Lie algebra from a Jordan pair.

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

* Ottmar Loos, _Jordan Pairs_, Lecture Notes in Mathematics, vol. 460, Springer, 1975, ISBN 978-3-540-37499-2.


