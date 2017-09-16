#Idea#

The _mapping cone_ of a [[morphism]] $f : X \to Y$ is a _[[weak quotient]]_ of $Y$ by the image of $X$.

#In additive categories with translation#

Let $C$ be an [[additive category]] [[category with translation|with translation]] $T : C \to C$. Let $X$ and $Y$ be two [[differential object]]s in $(C,T)$ and $f : X \to Y$ any [[morphism]] in $C$. 

The **mapping cone** $cone(f)$ of $f$ is the [[differential object]] whose underlying object is the [[direct sum]] $T X \oplus Y$ and whose differential $d_{cone f} : T X \oplus X \to T T X \oplus T X$ is given in [[matrix calculus]] notation by

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

A homotopy category of the [[category of chain complexes]] (with respect to chain homotopy equivalences) has a natural structure of a [[triangulated category]] where the distinguished triangles are the triangles isomorphic to **mapping cone triangle**s

$$
  X \stackrel{f}{\to}
  Y
  \stackrel{
    \left(
      \array{
          0 
          \\
          Id_Y
      }
    \right)
  }{\to}
   cone(f)
  \stackrel{
    \left(
      \array{
         Id_{T X} & 0
      }
    \right)
  }{\to}
  T X
  \,.
$$

For every map of chain complexes $f:A^\bullet\to B^\bullet$, the cylinder $Cyl(f)$ is quasi-isomorphic to $B^\bullet$, and moreover in the homotopy category of chain complexes, every distinguished triangle is quasi-isomorphic to a distinguished triangle of the form 

$$ A\to Cyl{u}\to Cone(u}\to A[1]$$

for some $u:A\to B$ where all the morphisms in the triangle are appropriatedly induced by $u$. 

#In Top#

Given a continuous map $f:X\to Y$, define the topological space $Cone(f)$ as the mapping cylinder which is the amalgamated sum $X \cup_{(f,0)} Y\times I$
(here each $x\in X$ is identified with $(f(x),0)$) modulo the contraction of $Y\times \{1\}$ to a point. 

Singular chain complex functor from $Top$ to the category of chain complexes of abelian groups sends the mapping cone to a mapping cone in the sense of chain complexes (up to conventions on the orientation of the interval and vector order in the definition of mapping cone of chain complexes). 
