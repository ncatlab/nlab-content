#Internal Categories and Groupoids#

The notion of a [[category]] can be formulated _internal_ to any other category with enough [[pullback|pullbacks]]. By regarding [[group|groups]] as one-object [[groupoid|groupoids]], this generalizes the familiar way in which, for instance

 * topological groups are groups _internal to topological spaces_
 
 * Lie groups are groups _internal to manifolds_.



#Definition#

Let $A$ be any category. A _category internal to $A$_ is 

 * a collection of morphisms in $A$ of the form
  $$
    C_1 \stackrel{s,t}{\to} C_0 \stackrel{i}{\to} C_1
  $$
  such that the pullback 
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

A _groupoid_ internal to $A$ is all of the above 

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

+--{.query}

Question: I've looked at the definition of category in $A$ for a while and still haven't been able to absorb it. Could we walk through an explicit example, e.g. "This is exactly what $C_0$ is, this is exactly what $C_1$ is, this is exactly what $s,t,i$ are, and this is how it relates to the more familiar context"? For example, an [[algebra]] is a monoid in $Vect$. I'll try to step through it myself, but it will probably need some correcting. - [[Eric Forgy|Eric]]

Question: In many cases it seems that a monoid internal to $A$ is the same as a monoid enriched over $(A,\otimes)$. Is that a coincidence? - [[Eric Forgy|Eric]]

=--

#Terminology#

 * $C_0$ is the "object of objects"; $C_1$ is the "object of morphisms", for instance for $A = Top$ $C_0$ is the "space of objects" and $C_1$ the "space of morphisms".

#Examples#

* A [[ring]] is a [[monoid]] internal to [[Ab]]. 

Explicitly, in the case of a ring, $C_0$ is the abelian group of objects and $C_1$ is the abelian group of morphisms. 

...

* An [[algebra]] is a [[monoid]] internal to [[Vect]]. 
* A [[Baez-Crans 2-vector space]] is a category internal to [[Vect]].
* A [[double category]] is a category internal to [[Cat]]. 
* A [[double bicategory]] is a category internal to [[Bicat]].
* A _small category_ is a category internal to $Sets$.
* Historically, the motivating exmaple for was (apparently) the notion of [[Lie groupoid|Lie groupoids]]: groupoids internal to the category [[Diff]] of manifolds. 

#Remarks#

Functors between internal categories are defined in a similar fashion. See [[functor]]. But in general it is better to use [[anafunctor|anafunctors]] instead.

#Literature#

[...]

Jean Pradines, _In [Ehresmann](http://en.wikipedia.org/wiki/Charles_Ehresmann)'s footsteps: from Group Geometries to Groupoid Geometries_ [	arXiv:0711.1608](http://arxiv.org/abs/0711.1608)

Baez & Crans, _[Higher-Dimensional Algebra VI: Lie 2-Algebras](http://arxiv.org/abs/math/0307263)_

[...]