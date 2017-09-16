#Idea#

The _mapping cone_ of a [[morphism]] $f : X \to Y$ is a _weak quotient_ of $Y$ by the image of $X$.

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

A [[category of chain complexes]] naturally becomes a [[triangulated category]] where the distinguished triangles are the **mapping cone triangle**s

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

#In Top#

...