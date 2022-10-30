
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

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


## Examples

* $Set_*$, the category of [[pointed set]]s, is the undercategory $pt\downarrow Set$, where $pt \simeq \{\bullet\}$ is [[generalized the|the]] singleton set.

* The category of commutative algebras over a field $F$ is the category $F \downarrow$[[CRing]] of commutative rings under $F$.


## Related concepts

* [[over-category]] 

  * [[slice category]] 

  * **under category** 

  * [[over topos]]


* [[over (∞,1)-category]],

  * [[model structure on an over category]] 

  * [[over-(∞,1)-topos]]



[[!redirects under category]]
[[!redirects under-category]]
[[!redirects undercategory]]
[[!redirects coslice category]]
[[!redirects co-slice category]]
[[!redirects under categories]]
[[!redirects under-categories]]
[[!redirects undercategories]]
[[!redirects coslice categories]]
[[!redirects co-slice categories]]