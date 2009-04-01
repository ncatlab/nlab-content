A **group object** in a category $C$ with binary products and a terminal object $*$ is an object $G$ in $C$ and arrows
$$
1:* \to G
$$
the unit map
$$
(-)^{-1}:G\to G
$$
the inverse map and
$$
m:G\times G \to G
$$
the multiplication map,
such that the following diagrams commute

$$
\array{
G\times G\times G & \stackrel{id\times m}{\to} & G\times G\\
 m\times id\downarrow && \downarrow m \\
 G\times G & \stackrel{m}{\to} &G
}
$$
expressing the fact multiplication is associative,
$$
\array{
G & \stackrel{(1,id)}{\to} & G\times G\\
 (\id,1)\downarrow &\underset{=}{\searrow}& \downarrow m \\
 G\times G & \stackrel{m}{\to} &G
}
$$
telling us that the unit map picks out an element that is a left and right identity, and
$$
\array{
G & \stackrel{(id,(-)^{-1})}{\to} & G\times G\\
 ((-)^{-1},id)\downarrow & \underset{1}{\searrow}& \downarrow m \\
 G\times G & \stackrel{m}{\to} &G
}
$$
Telling us that the inverse map really is an inverse.

Here we have let $1: G \to G$ denote the composite $G \to * \stackrel{1}{\to} G$.
