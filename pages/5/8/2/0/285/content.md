Given [[object|objects]] $x$ and $y$ in a [[locally small category]], the __hom-set__ $hom(x,y)$ is the collection of all morphisms from $x$ to $y$.  

## Remarks ##

* We say a category is [[locally small category|locally small]] if this collection is always actually a set instead of a proper class, or in the context of a [[Grothendieck universe]]: if this set is a $U$-small set.  This holds for many examples, but not for all. For example, if $C$ and $D$ are not [[small category|small categories]], then the [[functor category]] $C^D$ (whose objects are [[natural transformation]]s) will not be locally small.



#for enriched categories#

For a category $C$ [[enriched category theory|enriched over]] a category $V$, the "hom-set" $C(x,y)$ is an object of $V$, the [[hom-object]].

#for internal categories#

For $C = (C_0, C_1, s,t,e, comp)$ a [[internal category|category internal to]] a category with a [[terminal object|terminal]] [[generator]] $*$, we may identitfy morphisms $x,y * \to C_0$ with objects of $C$ and the corresponding "hom-thing" is the [[pullback]] $C(x,y)$ in

$$
  \array{
    C(x,y) &\to& C_1
    \\
    \downarrow && \downarrow^{s \times t}
    \\
    * &\stackrel{x \times y}{\to}&
    C_0 \times C_0
  }
$$


