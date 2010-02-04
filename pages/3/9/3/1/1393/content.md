
#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A constant [[∞-stack]] or [[(∞,1)-sheaf]] is the [[∞-stackification]] of a [[(∞,1)-presheaf]] which is constant as an [[(∞,1)-functor]].

This is the [[vertical categorification|categorification]] of the notion of [[constant sheaf]]

A section of the $\infty$-stack constant on $Core(Fin \infty Grpd) \in $ [[∞Grpd]] is a [[locally constant ∞-stack]].

## Remarks on constant $\infty$-stacks on Top

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


[[!redirects constant infinity-stacks]]
[[!redirects constant ∞-stack]]
[[!redirects constant ∞-stacks]]