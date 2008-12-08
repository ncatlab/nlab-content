#Internal Categories and Groupoids#

The notion of a [[category]] can be formulated _internal_ to any other category with enough [[pullbacks]]. By regarding [[group|groups]] as one-object [[groupoid|groupoids]], this generalizes the familiar way in which, for instance

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

#Terminology#

 * $C_0$ is the "object of objects"; $C_1$ is the "object of morphisms", for instance for $A = Top$ $C_0$ is the "space of objects" and $C_1$ the "space of morphisms".

#Examples#

* A _small category_ is a category internal to $Sets$.

* Historically, the motivating exmaple for was (apparently) the notion of [[Lie groupoid]]s: groupoids internal to the category of manifolds. 


#Literature#

[...]

Jean Pradines, _In [Ehresmann](http://en.wikipedia.org/wiki/Charles_Ehresmann)'s footsteps: from Group Geometries to Groupoid Geometries_ [	arXiv:0711.1608](http://arxiv.org/abs/0711.1608)

[...]