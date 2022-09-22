+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Pseudo-preorders are to [[preorders]] as [[pseudo-equivalence relations]] are to [[equivalence relations]]. A set with a pseudo-preorder is then a pseudo-preordered set or a pseudo-proset. 

Pseudo-prosets are important because they are the basic structure out of which many other structures like [[categories]] and [[setoids]] are built out of. 

## Definition

### With a family of sets

...

### With one set

A **pseudo-preorder** on a set $A$ is a set $E$ of **morphisms** and functions $s:E \to V$, $t:E \to V$ (a loop [[directed pseudograph]]), with with functions $\mathrm{id}:V \to E$ and  
$$\mathrm{comp}:\{(f,g) \in E \times E \vert t(f) =_V s(g)\} \to E$$ 
such that 

* for every $a \in V$, $s(\mathrm{id}(a)) =_E a$
* for every $a \in V$, $t(\mathrm{id}(a)) =_E a$
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $s(\mathrm{comp}(f,g)) =_E s(f)$ 
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $t(\mathrm{comp}(f,g)) =_E t(g)$

A **pseudo-preordered set** or **pseudo-proset** $A$ consists of a set $Ob(A)$ with a pseudo-preorder $Mor_A, \mathrm{id}, \mathrm{comp}$. 

## Examples

A [[category]] is a pseudo-proset $A$ which additionally satisfies

* for every object $a \in Ob(A)$, $b \in Ob(A)$, $c \in Ob(A)$, and $d \in Ob(A)$ and edge $f \in Mor_A(a, b)$, $g \in Mor_A(b, c)$, and $h \in Mor_A(c, d)$
$$\mathrm{comp}(a, b, d)(f, \mathrm{comp}(b, c, d)(g, h)) = \mathrm{comp}(a, c, d)(\mathrm{comp}(a, b, c)(f, g), h)$$

* for every vertex $a \in Ob(A)$, $b \in Ob(A)$ and edge $f \in Mor_A(a, b)$
$$\mathrm{comp}(a, b, b)(f, \mathrm{id}(b)) = f$$

* for every vertex $a \in Ob(A)$, $b \in Ob(A)$ and edge $f \in Mor_A(a, b)$
$$\mathrm{comp}(a, a, b)(\mathrm{id}(a), f) = f$$

## See also

* [[preorder]]
* [[setoid]]
* [[category]]

[[!redirects pseudo-prosets]]
[[!redirects pseudo-preorder]]
[[!redirects pseudo-preorders]]
[[!redirects pseudo-preordered set]]
[[!redirects pseudo-preordered sets]]