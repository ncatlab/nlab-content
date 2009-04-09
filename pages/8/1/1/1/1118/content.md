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

# Examples #
* A group object in [[Set]] is a [[group]].
* A group object in [[Top]] is a [[topological group]].
* A group object in [[Diff]] is a [[Lie group]].
* A group object in [[Grp]] is an [[abelian group]] (using the [[Eckmann-Hilton argument]]).
* A group object in [[Ab]] is an abelian group again.
* A group object in [[Cat]] is a strict [[2-group]].
* A group object in [[Grpd]] is a strict $2$-group again.

# Theory #

The basic results of elementary group theory apply to group objects in any category with finite products.  (Arguably, it is precisely the *elementary* results that apply in any such category.)

The theory of group objects is an example of a [[Lawvere theory]].