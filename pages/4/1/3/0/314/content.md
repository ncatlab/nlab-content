#Idea#

In [[category theory]] a limit of a [[diagram]] $F : D \to C$ in a [[category]] $C$ is an [[object]] $lim F$ of $C$ equipped with morphisms to the objects $F(d)$ for all $d \in D$, such that everything in sight commutes. Moreover, the limit $lim F$ is the _universal_ object with this property, i.e. the "most optimized solution" to the problem of finding such an object.

The limit construction has a wealth of applications throughout category theory and mathematics in general. On heuristic grounds it is possibly best thought of in the context of [[representable functor]]s as a **classifying space** for maps into a diagram. So in some sense the limit object $lim F$ "subsumes" the entire diagram $F(D)$ into a single object.

In some cases the category theoretic notion of limit does reproduce notions of limit as known from analysis. See the examples below.

# Warning on terminology #

Another equivalent term for limit is [[projective limit]]. Texts that say projective limit instead of just limit will use the symbol $\stackrel{lim}{\leftarrow}$ instead of just $lim$. Correspondingly, these text will write [[inductive limit]] for [[colimit]]. 

# Definition in terms of representable functors #

...

# Definition in terms of universal cones #

A **limit** of some [[diagram]] $F$ is a [[universal construction|universal]] [[cone]] to $F$. In more detail, it is a cone $\theta$ from an object denoted $lim F$ to $F$, such that given any cone $\gamma: \Delta c \to F$, there exists a unique morphism $f: c \to lim F$ such that 

$$
  (\Delta c
    \stackrel{\gamma}{\to}
   F
   )
    = 
  (
  \Delta c 
    \stackrel{\Delta f}{\to} 
  \Delta lim F 
    \stackrel{\theta}{\to} 
  F
  )
$$ 

(Given $f: c \to d$, $\Delta f: \Delta c \to \Delta d$ is the evident natural transformation whose component at each object $j$ of $J$ is $f: c \to d$.) 

[To be continued...]


# Definition in terms of adjoint of the constant diagram functor #

For $D$ a [[small category]] and $C$ a category the [[functor category]] $[D,C]$ is the category of $D$-[[diagram]]s in $C$.  Pullback along the functor $D \to pt$ to the [[terminal object|terminal]] category $pt = \{\bullet\}$ induces a functor
$$
  const :  C \to [D,C]
$$
which sends every object of $C$ to the diagram functor constant on this object.

The [[left adjoint]]
$$
  colim_D : [D,C] \to C
$$
of this functor is, if it exists, the functor
which sends every diagram to its [[colimit]] and the [[right adjoint]] is, if it exists, the functor
$$
  lim_D : [D,C] \to C
$$
which sends every diagram to its [[limit]]. The Hom-isomorphisms of these [[adjunction]]s state precisely the universal property of [[limit]] and [[colimit]] given above.




#Examples#

## Types of shapes of limit cones ##

Here are some important examples of limits, classified by the shape of the diagram:

* A limit of the [[empty set|empty diagram]] is a [[terminal object]].
* A limit of a diagram consisting of two (or more) objects and no nontrivial morphisms is their [[product]].
* A limit of a [[cospan]] is a [[pullback]].
* A limit of a pair (or more) of [[parallel morphisms]] is an [[equalizer]].
* Another important "shape" of limits are those that give rise to [[end]]s.

## Familiar concepts that are secretly examples of limits ##

* A limit over a [[subcategory|sub-poset]] $F : D \hookrightarrow C$ of a [[poset]] is, if it exists, the **supremum** of $D$ in $C$. Similarly, the limit over $F^{op} : D^{op} \to C^{op}$ is, if it exists, the **infimum** of $D$ in $C$.

