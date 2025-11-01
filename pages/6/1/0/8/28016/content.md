
## Idea

[[Jordan algebras]] were invented to axiomatize some properties of the Jordan product $a \circ b = (a b + b a)/2$ of self-adjoint complex matrices, which serve as [[observables]] in quantum mechanics.  As work proceeded, some researchers found it convenient to focus on another binary operation on self-adjoint matrices, $U_a (b) = a b a$.  Axiomatizing the properties of this led to the definition of a [[quadratic Jordan algebra]].   However, it is often convenient to replace this operation $U_a(b)$ by a trilinear operation, obtained by [[polarization identity|polarization]] as follows:

$$  \{a,b,c\} = U_{a+c}(b) - U_a(b) - U_c(b) = a b c + c b a $$

A **Jordan triple system** axiomatizes the properties of this triple product of self-adjoint complex matrices.  

Later it was discovered that there are close relations between Jordan triple systems and [[Lie triple systems]]. Just as Lie triple systems naturally give $\mathbb{Z}/2$-graded [[Lie algebras]], Jordan triple systems naturally give a certain class of so-called **3-graded Lie algebras**, which are $\mathbb{Z}$-graded Lie algebras concentrated in degrees $-1,0$ and $1$.   And just as the tangent space of any point in a [[symmetric space]] is naturally a Lie triple system, the tangent space of any point in a [[hermitian]] symmetric space is naturally a Jordan triple system.

## Definition

A **Jordan triple system** is a vector space $V$ equipped with a trilinear map $\{\cdot, \cdots, \cdot \} \colon V \times V \times V \to V$ obeying two axioms:

$$ \{a,b,c\} = \{c,b,a\}$$

$$\{a,b,\{c,d,e\}\} - \{c,d,\{a,b,e\}\} = \{\{a,b,c\},d,e\} - \{c,\{b,a,d\},e\} 
$$

Any subspace of an associative algebra closed under the operation $\{a,b,c\} = a b c + c b a$ obeys these axioms, and the first axiom captures the symmetry of this operation under switching the first and last arguments.  The second, subtler axiom implies that the operations $L_{a,b} \colon V \to V$ given by $L_{a,b}(c) = \{a,b,c\}$  form a Lie algebra under commutators.

## Jordan triple systems from Jordan algebras

Any Jordan algebra gives a Jordan triple system by

$$ \{a,b,c\} = a \circ (b \circ c) + (a \circ b) \circ c - b \circ (a \circ c).$$

There are however other Jordan triple systems.  For example, let $M(m,n)$ be the space of $m \times n$ matrices with entries in a field, and given $a \in M(m,n)$ let $a^T \in M(n,m)$ be its transpose.  We can make $M(m,n)$ into a Jordan triple system by defining

$$ {a,b,c} = a b^t c - c b^t a .$$

## Lie triple systems from Jordan triple systems

Any Jordan triple system gives a Lie triple system with Lie triple product given by

$$ [x,y,z] = \{x,y,z\} - \{y,x,z\} .$$


## References

* {#Loos71} Ottmar Loos, _Jordan triple systems, R-spaces, and bounded symmetric domains_, Bulletin of the American Mathematical Society __77__ (1971) 558–561. [pdf](https://www.ams.org/journals/bull/1971-77-04/S0002-9904-1971-12753-2/S0002-9904-1971-12753-2.pdf)

* {#Jacobson49} [[Nathan Jacobson]]: _Lie and Jordan triple systems_, American Journal of Mathematics __71__ (1949) 149–170 &lbrack;[jstor:2372102](https://www.jstor.org/stable/2372102)&rbrack; also in: *Nathan Jacobson, Collected Mathematical Papers*, Contemporary Mathematicians. Birkhäuser Boston (1989) &lbrack;[doi:10.1007/978-1-4612-3694-8_2](https://doi.org/10.1007/978-1-4612-3694-8_2)&rbrack;

