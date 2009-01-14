Given a [[category]] $C$ and an [[object]] $c \in C$, the _under category_ $c \downarrow C$ is the category whose

* objects are morphisms in $C$ starting at $c$; $c \to d$

* morphisms are commuting triangles 
$
 \array{
    && c
    \\
    & \swarrow && \searrow
    \\
    d_1 &&\to && d_2
  }
  \,.
$

The under category $c\downarrow C$ is the strict pullback 

$$
 \array{
  c\downarrow C
  &\to&
  pt
  \\
  \downarrow
  &&
  \;\;\downarrow^{pt \mapsto c}
  \\
  [I,C]
  &\stackrel{d_0}{\to}&
  C
 } 
$$
in [[Cat]], where

* $I$ is the interval category $I = \{a \to b\}$, which is the first [[oriental]], the 1-[[globe]], the canonical [[interval object]] in [[Cat]];

* $[I,C]$ is the [[closed monoidal category|internal hom]] in [[Cat]], which here is the [[arrow category]] $Arr(C)$;

* the functor $d_0$ is evaluation at the left end of the interval;

* $pt$, the point, is the terminal category, the 0th [[oriental]], the 0-globe;

* the right vertical morphism maps the single object of the point to the object $c$.

The left vertical morphism $c \downarrow C \to C$ is the forgetful morphism which forgets the tip of the triangles mentioned above.

#Examples#

* $Set_*$, the category of [[pointed set]]s, is the undercategory $pt\downarrow Set$, where $pt \simeq \{\bullet\}$ is [[generalized the|the]] singleton set.

* The category of commutative algebras over a field $F$ is the category $F \downarrow$[[Ring]] of commutative rings under $F$.

On this last example we had some blog discussion at

* John Baez, [A Quick Algebra Quiz](http://golem.ph.utexas.edu/category/2008/12/a_quick_algebra_quiz.html)