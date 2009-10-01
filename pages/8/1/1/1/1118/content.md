
#Contents#
* automatic table of contents goes here
{:toc}

A group object in a [[category]] $C$ is a [[group]] [[internalization|interal]] to $C$.

# Definition #

A **group object** in a category $C$ with binary [[product]]s and a [[terminal object]] $*$ is an object $G$ in $C$ and arrows
$$
1:* \to G
$$
(the unit map)
$$
(-)^{-1}:G\to G
$$
(the inverse map) and
$$
m:G\times G \to G
$$
(the multiplication map),
such that the following diagrams commute:
$$
\array{
G\times G\times G & \stackrel{id\times m}{\to} & G\times G\\
 m\times id\downarrow && \downarrow m \\
 G\times G & \stackrel{m}{\to} &G
}
$$
(expressing the fact multiplication is associative),
$$
\array{
G & \stackrel{(1,id)}{\to} & G\times G\\
 (\id,1)\downarrow &\underset{=}{\searrow}& \downarrow m \\
 G\times G & \stackrel{m}{\to} &G
}
$$
(telling us that the unit map picks out an element that is a left and right identity), and
$$
\array{
G & \stackrel{(id,(-)^{-1})}{\to} & G\times G\\
 ((-)^{-1},id)\downarrow & \underset{1}{\searrow}& \downarrow m \\
 G\times G & \stackrel{m}{\to} &G
}
$$
(telling us that the inverse map really does take an inverse), where we have let $1: G \to G$ denote the composite $G \to * \stackrel{1}{\to} G$.

Even if $C$ doesn\'t have *all* binary products, as long as products with $G$ (and the terminal object $*$) exist, then one can still speak of a group object $G$ in $C$.

## in terms of generalized group elements ##

One useful way to characterize [[group object]]s $G$ in a [[cartesian monoidal category]] $C$ is by first sending 
$G$ with the [[Yoneda embedding]] to a [[presheaf]] on $C$
and then imposing a lift of $Y(G) : C^{op} \to Set$
through the [[forgetful functor]] [[Grp]] $\to$ [[Set]]
that sends a (ordinary) [[group]] to its underlying [[set]].

So a group object structure on $G$ is a diagram

$$
  \array{
    && Grp
    \\
    & {}^{(G,\cdot)}\nearrow & \downarrow
    \\
    C^{op} &\stackrel{Y(G)}{\to}& Set
  }
  \,.
$$

This gives for each object $S \in C$ an ordinary group 
$(G(S), \cdot)$, so in particular a product operation

$$
  \cdot_S : G(S) \times G(S) \to G(S)
  \,.
$$

Moreover, since morphisms in $Grp$ are group homomorphisms, it follows
that for every morphism $f : S \to T$ of [[supermanifold]]s we get a 
commuting diagram

$$
  \array{
    G(S) \times G(S) &\stackrel{\cdot_S}{\to}& G(S)
    \\
    \uparrow^{G(f)\times G(f)}  && \uparrow^{G(f)}
    \\
    G(T) \times G(T) &\stackrel{\cdot_T}{\to}& G(T)     
  } 
$$

Taken together this means that there is a morphism

$$
  Y(G \times G)  \to Y(G)
$$

of representable presheaves. By the [[Yoneda lemma]], this uniquely
comes from a morphism $\cdot : G \times G \to G$, which is the 
product of the group structure on the object $G$ that we are after.

etc.  



# Examples #
* A group object in [[Set]] is a [[group]].
* A group object in [[Top]] is a [[topological group]].
* A group object in [[Diff]] is a [[Lie group]].
* A group object in [[SDiff]] is a [[supergroup|super Lie group]].
* A group object in [[Grp]] is an [[abelian group]] (using the [[Eckmann-Hilton argument]]).
* A group object in [[Ab]] is an abelian group again.
* A group object in [[Cat]] is a strict [[2-group]].
* A group object in [[Grpd]] is a strict $2$-group again.
* A group object in [[CRing]]$^{op}$ is a commutative [[Hopf algebra]].

# Theory #

The basic results of elementary group theory apply to group objects in any category with finite products.  (Arguably, it is precisely the *elementary* results that apply in any such category.)

The theory of group objects is an example of a [[Lawvere theory]].