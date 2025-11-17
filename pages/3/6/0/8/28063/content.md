[[!redirects quadratic Jordan algebras]]


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

[[Jordan algebras]] were invented to axiomatize some properties of the Jordan product $a \circ b = (a b + b a)/2$ of self-adjoint complex matrices, which serve as [[observables]] in quantum mechanics.  As work proceeded, some researchers found it convenient to focus on another binary operation on self-adjoint matrices, 

$$ U_a (b) = 2 a \circ (a \circ b) - (a \circ a) \circ b = a b a \, . $$

Axiomatizing the properties of this operation led to the definition of a **quadratic Jordan algebra**.   Later work led to the definitions of [[Jordan triple system]] and [[Jordan pair]].

## Definition 

A **quadratic Jordan algebra** consists of a vector space $V$ with a distinguished element $1 \in V$ and a map 

$$ U \colon V \to \mathrm{End}(V) $$

such that:

* $U$ is **quadratic**, meaning that $U(\lambda v) = \lambda^2 U(v)$ for all $v \in V$ and $\lambda$ in the ground field, and $U(u + w) - U(u) - U(w)$ is bilinear in $u$ and $w$,
* $U(1) = 1_V$,
* the **fundamental identity** holds: $U(U(v) w) = U(v) U(w) U(v)$ for all $v,w \in V$,
* if we polarize $U$, defining the **Jordan triple product** by $\{u,v,w\} = \bigl(U(u+w) - U(u) - U(w)\bigr)(v)$, and then define $V(u,v)(w) = \{u,v,w\}$, then the **commuting formula** holds: $U(u)V(v,u) = V(u,v)U(u)$ for all $u,v \in V$.

## Related concepts

* [[Jordan algebra]]

* [[Jordan triple system]]

* [[Jordan pair]]

* [[Jordan superalgebra]]

* [[exceptional Jordan algebra]]/[[Albert algebra]]

## References 

Starting on page 7 of this book, there is a short introduction to quadratic Jordan algebras:

* {#McCrimmon} Kevin McCrimmon: _A Taste of Jordan Algebras_, Springer (2006) &lbrack;[pdf](http://math.nsc.ru/LBRT/a1/files/mccrimmon.pdf)&rbrack;

and they are used throughout.

[[!redirects quadratic Jordan algebras]]