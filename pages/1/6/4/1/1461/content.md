#Idea#

A _strict morphism_ is a [[morphism]] for which the notion of [[image]] and [[coimage]] coincide.

#Definition#

## in a category with limits and colimits ##

Let $C$ be a category with finite [[limit]]s and [[colimit]]s. Let $f : c \to d$ be a [[morphism]] in $C$.

Recall that the [[image]] of $f$ is the [[limit]] 

$$
  Im f \simeq lim( d \stackrel{\to}{\to} d \sqcup_c d )
  \,,
$$

i.e. the [[kernel pair]] of $d \to d \sqcup_c d$,

while the [[coimage]] is the [[colimit]]

$$
  Coim f \simeq colim( c \times_d c \stackrel{\to}{\to} c)
  \,.
$$

By the various universal properties, there is a unique morphism 

$$
  u : Coim f \to Im f
$$

such that

$$
  \array{
      c &\stackrel{f}{\to}& d
      \\
      \downarrow && \downarrow
      \\
      Coim f &\stackrel{u}{\to}& Im f
  }
  \,.  
$$

The morphism $f$ is called a **strict morphism** if $u$ is an [[isomorphism]].

#Remarks#

* Compare with [[strict epimorphism]].

#Examples#

* Examples of categories in which every morphism is strict are

  * [[Set]]

  * the  category $Mod(R)$ of [[module]]s over a [[ring]] $R$;

  * the category $PSh(C) = [C^{op},Set]$ of [[presheaf|presheaves]] on any [[small category]] $C$.