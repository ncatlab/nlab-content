# Coslice (under) categories
* tic
{: toc}


## Definition

Given a [[category]] $C$ and an [[object]] $c \in C$, the __under category__ (also called __coslice category__) $c \downarrow C$ (also written $c/C$ and sometimes, confusingly, $c\backslash C$) is the category whose

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

The under category $c\downarrow C$ is a kind of [[comma category]]; it is the strict pullback 

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

* $I$ is the [[interval category]] $\{0 \to 1\}$;

* $[I,C]$ is the [[closed monoidal category|internal hom]] in [[Cat]], which here is the [[arrow category]] $Arr(C)$;

* the functor $d_0$ is evaluation at the left end of the interval;

* $pt$, the point, is the terminal category, the 0th [[oriental]], the 0-globe;

* the right vertical morphism maps the single object of the point to the object $c$.

The left vertical morphism $c \downarrow C \to C$ is the forgetful morphism which forgets the tip of the triangles mentioned above.

The [[duality|dual]] notion is an [[over category]].


##Examples#

* $Set_*$, the category of [[pointed set]]s, is the undercategory $pt\downarrow Set$, where $pt \simeq \{\bullet\}$ is [[generalized the|the]] singleton set.

* The category of commutative algebras over a field $F$ is the category $F \downarrow$[[Ring]] of commutative rings under $F$.

On this last example we had some blog discussion at

* John Baez, [A Quick Algebra Quiz](http://golem.ph.utexas.edu/category/2008/12/a_quick_algebra_quiz.html)


##Discussion#

_[[Eric Forgy|Eric]] says_: I thought this sounded familiar. Is an under category the same thing as what Urs calls a <a href="http://golem.ph.utexas.edu/category/2007/07/tangent_categories.html">tangent category</a>?

_[[Eric Forgy|Eric]] says_: Found it, but I'll leave my question here in case it inspires anything that can be included. I see on <a href="http://www.math.uni-hamburg.de/home/schreiber/tangcat.pdf">page 3</a> Urs says that a tangent category is a co-slice category.


[[!redirects coslice category]]
[[!redirects under-category]]
[[!redirects undercategory]]
[[!redirects coslice categories]]
[[!redirects under-categories]]
[[!redirects undercategories]]
[[!redirects under categories]]