## Idea ##

A pure type system is an explicitly typed lambda calculus
using dependent product as the type of lambda expressions:
the basic idea is that
$$\Gamma, x:A \vdash B:C$$
implies
$$\Gamma \vdash (\lambda x:A . B) : (\prod x:A . C).$$

## Definition ##

A _pure type system_ is defined by
* a set $S$ of _sorts_, all of which are constants,
* a set $A$ of _axioms_ of the form $c : s$ with $c$ a constant and $s$ a sort,
* a set $R$ of _relations_: triples $(s_{1}, s_{2}, s_{3})$ of sorts.
  Relations $(s_{1}, s_{2}, s_{2})$ are abbreviated as $(s_{1}, s_{2})$.

The _terms_ of a pure type system are the following (recursive definition):
* variables and constants
* $(\lambda x : A . B)$ (abstraction)
* $(\prod x : A . B)$ (product)
* $A B$ (application)

Here $x$ is a variable and $A$, $B$ are terms.
The operators $\lambda$ and $\prod$ bind the variable $x$.

The typing of terms is inductvely defined by the following rules.
A typing is of the form
$$x_{1} : A_{1}, \dots, x_{n} : A_{n} \vdash A : B$$
meaning that the types of the variables declared on the left
induces the term $A$ has type $B$.
Note that types are also terms.
The order of variable  declarations is significant:
the declaration $x_{i} : A_{i}$ may depend on declarations to its left.

name          | rule                                                                                                                      | condition                         |
--------------|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
(axioms)      | $\Gamma \vdash c : s$                                                                                                     | if $(c : s)$ is an axiom;         |
(start)       | $\frac{\Gamma \vdash A:s}{\Gamma, x : A \vdash \Gamma x : A}$                                                             | if $x \notin \Gamma$              |
(weakening)   | $\frac{\Gamma \vdash A:B; \quad \Gamma \vdash C:s}{\Gamma, x : C \vdash A : B}$                                           | if $x \notin \Gamma$              |
(product)     | $\frac{\Gamma \vdash A : s_{1}; \quad \Gamma x:A \vdash B : s_{2}}{\Gamma \vdash (\prod x:A . B) : s_{3}}$                | if $(s_{1}, s_{2}. s_{3}) \in R$; |
(application) | $\frac{\Gamma \vdash F : (\prod x:A . B); \quad \Gamma \vdash a : A}{\Gamma \vdash Fa : B [x := a]}$                      |                                   |
(abstraction) | $\frac{\Gamma, x:A \vdash b : B; \quad \Gamma \vdash (\prod x:A . B) : s}{\Gamma \vdash (\lambda x:A:b) : (\prod x:A:B)}$ |                                   |
(conversion)  | $\frac{\Gamma \vdash A : B; \quad \Gamma B' : s; B =_{\beta} B'}{\Gamma \vdash A : B'}$                                   |                                   |

In the above $s$ ranges over sorts and $x$ ranges over variables.

## Examples ##

### Strongly normalizing systems ###

#### Intuitionistic (higher-order) logic ####

#### Lambda cube #### 

The lambda cube consists of eight systems arranged in a cube.
The most expressive is

| symbol | actual value
|--------|-------------
| S      | $\ast$, $\square$
| A      | $\ast : \square$
| R      | $(\ast, \ast)$, $(\ast, \square)$, $(\square, \ast)$, $(\square, \square)$ 

The other systems omit some of the last three relations.
Some specific systems:

name                                                  | $(\ast, \ast)$ | $(\ast, \square)$ | $(\square, \ast)$ | $(\square, \square)$ | 
------------------------------------------------------|----------------|-------------------|-------------------|----------------------|
$\lambda\rightarrow$ [[simply typed lambda calculus]] | yes            |                   |                   |                      |
$\lambda2$ [[system F]]                               | yes            | yes               |                   |                      |
[[LF]]                                                | yes            |                   | yes               |                      |
[[calculus of constructors]]                          | yes            | yes               | yes               | yes                  |

### Inconsistent systems ### 

The most permissive pure type system:

| symbol | actual value
|--------|-------------
| S      | $\ast$
| A      | $\ast : \ast$
| R      | $(\ast, \ast)$

But there is an example with even non-circular system of axioms:

| symbol | actual value
|--------|-------------
| S      | $\ast$, $\square$, $\triangle$
| A      | $\ast : \square$, $\square : \triangle$
| R      | $(\ast, \ast)$, $(\square, \ast)$, $(\square, \square)$, $(\triangle, \square)$

## References ##

Henk Barendregt (Catholic University Nijmegen),
[[Lambda calculi with types]],
To appear in
Handbook of Logic in Computer Science, Volume II,
Edited by
S. Abramsky, D.M. Gabbay and T.S.E. Maibaum
Oxford University Press
