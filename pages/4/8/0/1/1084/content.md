<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The _mapping cone_ of a [[morphism]] $f : X \to Y$ is a particular [[model category]] representative of the [[homotopy fiber|homotopy cofiber]] of $f$, also called the homotopy cokernel of $f$ or _[[weak quotient]]_ of $Y$ by the [[image]] of $X$ in $Y$ under $f$. 


#Definition#

In an [[(∞,1)-category]] the [[homotopy fiber|homotopy cofiber]] of a [[morphism]] $f : X \to Y$ is the homotopy pushout

$$
  \array{
     X &\stackrel{}{\to}& {*}
     \\
     \downarrow^f && \downarrow
     \\
     Y &\to& coker(f)
  }
  \,.
$$

When the [[(∞,1)-category]] is [[presentable (∞,1)-category|presented]] by a [[model category]] and when all objects involved are cofibrant in this model structurem then this may be computed by the ordinary [[colimit]] 

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{i_1} && \downarrow
    \\
    X &\stackrel{i_0}{\to}& Cyl(X)
    \\
    \downarrow && && \downarrow
    \\
    {*} &\to& &\to& coker(f) 
  }
$$

using a [[cylinder object]] $Cyl(X)$ for $X$, that models the [[left homotopy]] filling the original homotopy pushout diagram. This colimit, in turn, may be computed in two stages by two consecutive [[pushout]]s as

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{i_1} && \downarrow
    \\
    X &\stackrel{i_0}{\to}& Cyl(X)
    \\
    \downarrow && \downarrow 
    \\
    {*} &\to& cone(X) &\to& coker(f) 
  }
  \,.
$$

The first [[pushout]] here 

$$
  \array{
     X &\stackrel{i_0}{\to}& Cyl(X)
     \\
     \downarrow && \downarrow
     \\
     {*} &\to& cone(X)
  }
$$

is  the **cone** over $X$: the result of taking the [[cylinder object|cylinder]] over $X$ and identifying one $X$-shaped end with the [[point]].

The remaining [[pushout]]

$$
  \array{
    X &\stackrel{f}{\to}& Y
    \\
    \downarrow && \downarrow
    \\
    cone(X) &\to& coker(f) & =: cone(f)
  }
$$

is the **mapping cone** of $f$:

this is the result of taking that _other_ remaining end of the cyclinder and gluing that to $Y$, using the identification given by $f$.

The geometric intuition behind this is best seen in the archetypical example of the [[model category]] [[Top]]. See the examples below.


#Examples#

## Suspension ##

The mapping cone of the morphism $X \to {*}$ to the [[terminal object]] is the [[suspension object]] $\Sigma X$ of an object $X$. The dual notion of the [[loop space object]] of $X$.

##In Top##

The construction is geometrically most obvious in the category [[Top]] of [[topological space]]s.

Here for $I = [0,1]$ the standard [[interval object]] we may take the [[cylinder object]] to be $Cyl(X) = X \times I$, literally the cylinder over $X$. 

Given a continuous map $f:X\to Y$, the 
[[topological space]] $cone(f)$ is

$$
  X\times I \cup_{f} Y
$$

(here for all $x\in X$, $(x,1)$ is identified with $f(x)$) modulo the contraction of $X\times \{0\}$ to a point. 

When 

Singular chain complex functor from [[Top]] to the 
[[category of chain complexes]] of abelian groups sends the mapping cone to a mapping cone in the sense of chain complexes (up to conventions on the orientation of the interval and vector order in the definition of mapping cone of chain complexes). 


##In additive categories with translation##

Let $C$ be an [[additive category]] [[category with translation|with translation]] $T=[1] : C \to C$. Let $X$ and $Y$ be two [[differential object]]s in $(C,T)$ and $f : X \to Y$ any [[morphism]] in $C$. 

The **mapping cone** $Cone(f)$ of $f$ is the [[differential object]] whose underlying object is the [[direct sum]] $T X \oplus Y$ and whose differential $d_{cone f} : T X \oplus X \to T T X \oplus T X$ is given in [[matrix calculus]] notation by

$$
  d_{cone f} :=
  \left(
   \array{
    d_{T X} & 0
    \\
    T(f) & d_Y
   }
  \right)
  =
  \left(
   \array{
    - T(d_X) & 0
    \\
    T(f) & d_Y
   }
  \right)
  \,.
$$

Notice the minus sign here, coming from the definition of a [[differential object|shifted differential object]].


## Distinguished triangles from mapping cones ##

A [[homotopy category]] of the [[category of chain complexes]] (with respect to chain [[homotopy equivalence]]s) has a natural structure of a [[triangulated category]] where the distinguished triangles are the triangles isomorphic to **mapping cone triangle**s

$$
  A \stackrel{f}{\to}
  B
  \stackrel{
    \left(
      \array{
          0 
          \\
          Id_B
      }
    \right)
  }{\to}
   Cone(f)
  \stackrel{
    \left(
      \array{
         Id_{A[1]} & 0
      }
    \right)
  }{\to}
  A[1]
  \,.
$$

For every map of [[chain complex]]es $f:A\to B$, the cylinder $Cyl(f)$ is quasi-isomorphic to $B$, and moreover in the [[homotopy category]] of chain complexes, every distinguished triangle is quasi-isomorphic to a distinguished triangle of the form 

$$ A\to Cyl(u)\to Cone(u)\to A[1]$$

for some $u:A\to B$ where all the morphisms in the triangle are appropriatedly induced by $u$. 

