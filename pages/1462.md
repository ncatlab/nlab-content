#Idea#

The coimage of a morphism is the notion [[duality|dual]] to its [[image]].

#Definition#

The **coimage** of a [[morphism]] $f : c \to d$ in a [[category]] $C$ is the [[image]] of the corresponding morphism in the [[opposite category]] $C^{op}$.

## In terms of colimits ##

If $C$ has finite [[limit]]s and [[colimit]]s, then the coimage of a morphism $f : c \to d$ is
$$
  Coim f \simeq colim ( c \times_d c \stackrel{\to}{\to} c)
  \,,
$$
that is the [[coequalizer]] of its [[kernel pair]].

This is isomorphic to the [[pushout]] $c \sqcup_{c\times_d c} c$

$$
  coim f \simeq c \sqcup_{c\times_d c} c
  \,.
$$

So in

$$
  \array{
    c \times_d c &&\to&& c
    \\
     &&& \swarrow
    \\
    \downarrow^f && coim f && \downarrow^f
    \\
    & \nearrow && \searrow
    \\
    C && \stackrel{f}{\to} && d
  }
$$

the outer square is a [[pullback]] square while the inner is a [[pushout]].

Notice that being a coequalizer, the morphism

$$
  c \to coim f
$$

is an [[epimorphism]]. 


#Remarks#

* Morphisms for which image and coimage coincide (in a certain sense) are [[strict morphism]]s.