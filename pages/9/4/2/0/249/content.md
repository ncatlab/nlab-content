A functor $F: C \to D$ is __pseudomonic__ if

1. it is [[faithful functor|faithful]]; that is, for any pair of objects
   $x,y\in C$ the function $F: C(x,y) \to D(F x,F y)$ is injective,
   and
2. it is _full on isomorphisms_, meaning that for  any pair of objects
   $x,y\in C$ the function $F: Iso_C(x,y) \to Iso_D(F x, F y)$ is
   surjective (hence bijective), where $Iso_C(x,y)$ means the set of
   [[isomorphism|isomorphisms]] from $x$ to $y$ in $C$.

Every [[full functor|full]] and faithful functor is pseudomonic.  A
functor $F: C \to D$ is pseudomonic if and only if the square

$$
  \array{ 
    C &\stackrel{Id}{\to}& C
    \\
    \downarrow^{Id}
    &&
    \downarrow^F
    \\
    C &\stackrel{F}{\to}& D
  }
$$

is a [[2-categorical limit|bicategorical pullback]] in [[Cat]].
