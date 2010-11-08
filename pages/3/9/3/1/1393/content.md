
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A constant [[∞-stack]]/[[(∞,1)-sheaf]] is the [[∞-stackification]] of a [[(∞,1)-presheaf]] which is constant as an [[(∞,1)-functor]].


With the [[global section]] [[(∞,1)-functor]] the constant $\infty$-stack functor $LConst$ forms the [[terminal object|terminal]] [[(∞,1)-geometric morphism]]

$$
  (LConst \dashv \Gamma)
  :
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
  \,.
$$


## On $Top$

Notice that in the special case of [[∞-stack]]s on [[Top]], hence of [[topological ∞-groupoid]], which may be thought of as [[Top]]-valued presheaves on [[Top]](!), there are _two different_ obvious ways to regard a topological space $X$ as an [[∞-stack]] on [[Top]]:

* there is the [[∞-stack]] $\bar const_X$ _constant_ on $X$, meaning constant on the [[Kan complex]] that is  the [[fundamental ∞-groupoid]] $Sing X = \Pi(X)$ of $X$;

* there is the [[Yoneda embedding]] $Y(X)$ of $X$ into [[∞-stack]].

The first regards $X$ really as an [[∞-groupoid]], forgetting its topology, the second regards $X$ as a [[locale]], not caring about the homotopies that are inside.



For any [[(∞,1)-category]] $S$, there is the obvious embedding of [[∞-groupoid]]s into [[(∞,1)-presheaf|(∞,1)-presheaves]] on $S$

$$
  const : \infty Grpd \to [S^{op}, \infty Grpd]
$$

where of course

$$
  const_K : U \mapsto K
$$

for all $U$.

This is all very obvious, but deserves maybe a special remark in the case that [[∞-groupoid]]s are modeled as (compactly generated and weakly Hausdorff) [[topological space]]s: in particular in the case that $S = Top$ itself, there are then two different ways to regard a topological space as an $\infty$-stack, and they have very different meaning.


In particular, with $X$ a [[topological space]], the $\infty$-stack _constant_ on $X$ has the property that its [[loop space object]] $\Lambda X$ is indeed the $\infty$-stack constant on the free loop space of $X$, while the [[loop space object]] of $X$ regarded as a representable $\infty$-stack is just $X$ itself again. 

This is because 

* the $\infty$-stack represented by $X$ regards $X$ as a [[discrete category|categorically discrete]] topological groupoid;

* while the $\infty$-stack constant on $X$ regards $X$ as a topologically discrete groupoid which however may have nontrivial morphisms.


## Pattern

* A [[locally constant function]] is a section of a [[constant sheaf]];

* a [[locally constant sheaf]] is a section of a [[constant stack]];

* a [[locally constant stack]] is a section of (... and so on...)

* a [[locally constant ∞-stack]] is a section of a **constant $\infty$-stack**.

A locally constant sheaf / $\infty$-stack is also called a [[local system]].



[[!redirects constant infinity-stacks]]
[[!redirects constant ∞-stack]]
[[!redirects constant ∞-stacks]]

[[!redirects constant (∞,1)-sheaf]]
[[!redirects constant (∞,1)-sheaves]]