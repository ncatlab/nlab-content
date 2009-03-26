#Definition#

An **equalizer** is a [[limit]] over a [[diagram]] of the shape 
$$
  \left\lbrace
      a \stackrel{\to}{\to} b
  \right\rbrace
  \,.
$$

This means that for $f : c \to d$ and $g : c \to d$ two [[parallel morphisms]] in a [[category]] $C$, their equalizer is, if it exists

* an object $Eq(f,g) \in C$;

* a morphism $Eq(f,g) \to c$

* such that 

  * pulled back to $Eq(f,g)$ both morphisms become [[equality|equal]]: $ (Eq(f,g) \to c \stackrel{f}{\to} d) = (Eq(f,g) \to c \stackrel{g}{\to} d) $
  * and $Eq(f,g)$ is the universal object with this property.

#Examples#

* In $C =$ [[Set]] the equalizer of two functions of sets is the subset of elements of $c$ on which both functions coincide.
$$
  Eq(f,g)
  = 
  \left\{
     s \in c | 
     f(s) = g(s)
  \right\}
  \,.
$$

* For $C$ a category with [[zero object]] the equalizer of a morphism $f : c \to d$ with the corresponding [[zero morphism]] is the [[kernel]] of $f$.