
#Contents#
* table of contents
{:toc}

## Idea

Certain [[Grothendieck topologies]] on a category with an [[initial object]] can be presented by a very simple structure called a _cd-structure_.
[[sheaves|Sheaves]] with respect to such topologies can be described by an [[excision]] property.

## Definition

+-- {: .num_defn}
###### Definition
A *cd-structure* $\chi$ on a [[category]] $C$ with an [[initial object]] is a class of [[commutative squares]] which is stable by isomorphism.
We will call its elements **$\chi$-distinguished squares**.
=--

## Properties

Any cd-structure gives rise in a canonical way to a [[Grothendieck topology]] on $C$.

+-- {: .num_defn}
###### Definition
Let $\chi$ be a cd-structure on $C$.  The associated [[Grothendieck pretopology]] on $C$ is defined by the coverings:

* the empty covering of $\emptyset_C$, the initial object of $C$;
* the coverings $\{ b \to d, c \to d \}$ for all $\chi$-distinguished squares
$$
\begin{matrix}
  a& \to & b \\
  \downarrow& &\, \downarrow p\\
  c &\underset{j}{\to} & d
\end{matrix}
$$
=--

One checks that this is indeed a well-defined [[Grothendieck pretopology]].  We will denote it by $\tau_\chi$, and by abuse of notation we will also write $\tau_\chi$ for the associated [[Grothendieck topology]].

+-- {: .num_defn}
###### Definition
A cd-structure $\chi$ is called **complete** if every [[morphism]] whose target is an [[initial object]] of $C$ is an isomorphism, and if it is stable by [[base change]] along arbitrary morphisms of $C$.
=--

+-- {: .num_defn}
###### Definition
A cd-structure $\chi$ is called **regular** if (i) each $\chi$-distinguished square $Q$ is [[cartesian square|cartesian]], (ii) the lower horizontal morphism $j : c \to d$ is a [[monomorphism]], and (iii) for each $Q \in \chi$, the induced commutative square
$$
\begin{matrix}
  a& \to & c \\
  \downarrow& &\, \downarrow\\
  a \times_b a &\to & c \times_d c
\end{matrix}
$$
belongs to $\chi$.
=--

+-- {: .num_prop}
###### Proposition
Let $\chi$ be a complete cd-structure.  If $F$ is a [[presheaf]] on $C$ that maps initial objects of $C$ to terminal objects, and sends $\chi$-distinguished squares to [[cartesian squares]], then $F$ is a $\tau_\chi$-sheaf.

If $\chi$ is further regular, then the converse is also true.
=--

## Examples

There are various interesting cd-structures on the category of [[schemes]] over a base $S$, which give rise to [[Grothendieck topologies]] like the [[Zariski topology|Zariski]], [[Nisnevich topology|Nisnevich]] and [[cdh topology|cdh]] topologies.

## See also

* [[Grothendieck topology]]
* [[Nisnevich topology]]
* [[cdh topology]]

## References

* [[Vladimir Voevodsky]], _Homotopy theory of simplicial presheaves in completely decomposable topologies_, 2000, [K-theory archive](http://www.math.uiuc.edu/K-theory/443/), [arXiv:0805.4578](http://arxiv.org/abs/0805.4578v1).

* Brad Drew, _Descente : Nisnevich et cdh_, Groupe de travail at Universit&#233; Paris 13, Spring 2010, [pdf](http://www.math.univ-paris13.fr/~kelly/GdT/exposeVII.pdf).

[[!redirects cd-structures]]
[[!redirects cd structure]]
[[!redirects cd structures]]
[[!redirects cd-topology]]
[[!redirects cd-topologies]]
[[!redirects cd topology]]
[[!redirects cd topologies]]