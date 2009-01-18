#Internal Categories and Groupoids#

The notion of a [[category]] can be formulated [[internalization|internal]] to any other category with enough [[pullback|pullbacks]]. By regarding [[group|groups]] as one-object [[groupoid|groupoids]], this generalizes the familiar way in which, for instance

 * topological groups are groups _internal to topological spaces_
 
 * Lie groups are groups _internal to (smooth) manifolds_.

#Definition#

Let $A$ be any category. A _category internal to $A$_ is 

 * a collection of morphisms in $A$ of the form
  $$
    C_1 \stackrel{s,t}{\to} C_0 \stackrel{i}{\to} C_1
  $$
  such that the composites $s\cdot i$ and $t\cdot i$ are the identity morphisms on $C_0$, and such that the pullback 
  $$
    \array{
      C_1 \times_{t,s} C_1 &\to& C_1
      \\
      \downarrow && \downarrow^{t}
      \\
      C_1 &\stackrel{s}{\to}& C_0
    }
  $$
  exists;

 * and a morphism
  $$
     C_1 \times_{t,s} C_1 \stackrel{comp}{\to} C_1
  $$
  "respecting $s$ and $t$";

 * such that the _composition_ $comp$ is associative
   and unital with respect to $i$ "in the obvious way".

A [[groupoid]] internal to $A$ is all of the above 

 * such that the cartesian product $C_1 \times C_1$ exists

 * and a morphism
  $$
     C_1 \stackrel{s}{\to} C_1
  $$


 * such that
   $$
     \array{
        C_1 &\stackrel{diag}{\to}& C_1 \times C_1
        \\
        \downarrow^s && \;\;\;\;\;\;\;
           \downarrow^{comp \;\; (Id \times s)}
        \\
        C_0 &\stackrel{i}{\to}& C_1
     }
     \,.
   $$


#Terminology#

 * $C_0$ is the "object of objects"; $C_1$ is the "object of morphisms", for instance for $A = Top$ $C_0$ is the "space of objects" and $C_1$ the "space of morphisms".

#Examples#

* A [[small category]] is a category internal to [[Set]].

In this case, $C_0$ is a set of objects and $C_1$ is a set of morphisms and the pullback is Cartesian product.

* A small [[cocategory]] is a category internal to $Set^{op}$.
* A [[double category]] is a category internal to [[Cat]]. 
* A [[double bicategory]] is a category internal to [[Bicat]] (in a suitably weak sense).
* A [[crossed module]] is equivalent to a category internal to [[Grp]].
* A [[Baez-Crans 2-vector space]] is a category internal to [[Vect]].
* Historically, the motivating example was (apparently) the notion of [[Lie groupoid|Lie groupoids]]: groupoids internal to the category [[Diff]] of manifolds. 

#Functors#

Functors between internal categories are defined in a similar fashion. See [[functor]].  But if the ambient category does not satisfy the [[axiom of choice]] it is often better to use [[anafunctor|anafunctors]] instead.

#Literature#

[...]

Jean Pradines, _In [Ehresmann](http://en.wikipedia.org/wiki/Charles_Ehresmann)'s footsteps: from Group Geometries to Groupoid Geometries_ [	arXiv:0711.1608](http://arxiv.org/abs/0711.1608)

Baez & Crans, _[Higher-Dimensional Algebra VI: Lie 2-Algebras](http://arxiv.org/abs/math/0307263)_

[...]

#Discussion#

Question: I've looked at the definition of category in $A$ for a while and still haven't been able to absorb it. Could we walk through an explicit example, e.g. "This is exactly what $C_0$ is, this is exactly what $C_1$ is, this is exactly what $s,t,i$ are, and this is how it relates to the more familiar context"? For example, an [[algebra]] is a monoid in $Vect$. I'll try to step through it myself, but it will probably need some correcting. - [[Eric Forgy|Eric]]

Eric, one example to ponder is: how is an internal category in [[Grp]] the "same" as a [[crossed module]]? As a partial hint, try to convince yourself that given a internal category, part of whose data is $(C_1, C_0, s, t)$, the group $C_1$ of arrows can be expressed as a semidirect product with $C_0$ acting on $\ker(s)$. The full details of this exercise may take some doing, but it might also be enjoyable; if you get stuck, you can look at [Forrester-Barker](http://arxiv.org/PS_cache/math/pdf/0212/0212065v1.pdf). - [[Todd Trimble|Todd]]

_[[Urs Schreiber|Urs]]_: I don't know, but maybe Eric should first convince himself of what Todd may find too obvious: how the above definition of an internal category reproduces the ordinary one when one works internal to [[Set]]. Eric, is that clear? If not, let us know where you get stuck!

_[[Tim Porter|Tim]]_: I have just had a go at [[2-group]] and looked at the relationship between 2-groups and crossed modules in a little more detail, in the hope it will unbug the definition for those who have not yet 'groked' it.

_[[Eric Forgy|Eric]]_: Oh thanks guys. I will try to understand how a small category is a category internal to Set first and then move on to category in Grp and the stuff Tim wrote. I'm sure this is all obvious, but don't underestimate my ability to not understand the obvious :)

_[[Eric Forgy|Eric]]_: Ok. Duh. It is pretty obvious for Set EXCEPT for pullback. Pullbacks in Set are obvious, but what about other cases? Why is that important and what is an example where there are not pullbacks?  In other words, is there an a example of something that is ALMOST a category in some other category except it doesn't have pullbacks, so is not? 