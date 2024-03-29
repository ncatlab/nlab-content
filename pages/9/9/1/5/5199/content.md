### Idea

A **framed link** is a link where the circles forming the components are viewed as having a thickness, albeit an arbitrarily small thickness.
That is to say, instead of the components of the links being embedded circles, they are embedded solid tori.

The thickening can be considered in one direction only which gives embedded ribbons.  This is an equivalent definition which can be useful as it makes the distinction clearer between an embedding and the same embedding composed with, say, a [[Dehn twist]].

A [[link diagram]] can be made into a diagram of a framed links by giving it the **blackboard framing**: this views each segment of the link diagram as a ribbon lying on the "blackboard".

Two diagrams represent the same link diagram if and only if they can be related by a modified version of the [[Reidemeister moves]] in which the first move is replaced by the following move.

[[!include modified Reidemeister move 1 - SVG]]

## Definition 

The precise notion of a framing on a link is perhaps most naturally given in terms of smooth structures on manifolds. We'll start from there and later give other versions. 

Let $M$ be an oriented 3-manifold, for example $S^3$. The tangent bundle $p: T M \to M$ is a bundle with structure group $GL(3) = GL(\mathbb{R}^3)$ which in fact admits a reduction to $GL_+(3)$ (invertible linear transformations with positive determinant) since $M$ is oriented. A further reduction to the structure group $SO(3)$ can be effected by a number of means, e.g., by equipping $M$ with a Riemannian metric. 

Now let 

$$L: S^1 \sqcup \ldots \sqcup S^1 \hookrightarrow M$$ 

be a smoothly embedded link (of oriented circles). The normal bundle of $L$ is the cokernel of the bundle inclusion 

$$T(S^1 \sqcup \ldots \sqcup S^1) \to L^\ast T M$$ 

(as bundles over $S^1 \sqcup \ldots \sqcup S^1$); it is naturally associated with a principal $SO(2)$-bundle. A *framing* of $L$ is simply a choice of section $\sigma$ of this principal $SO(2)$-bundle. It can be thought of as a smooth choice of unit normal vectors along points of the embedded link, and can be visualized as "ribbons", one for each component $S^1$, with one edge of the ribbon being that component. 

The $SO(2)$-bundle or circle bundle over each component $S^1$ can be seen as an embedded [[torus]] in $M$. The framing itself induces a diffeomorphism on this torus which takes an element $(\xi, p)$ over $p \in S^1$ to $(\sigma(p)\xi, p)$. 

However, it is often convenient to consider such framings, or rather their associated torus diffeomorphisms, only up to isotopy. For each component $S^1$, the isotopy class is specified by an integer which gives the number of 360 degree clockwise rotations of the unit normal or clockwise twists of the ribbon as one traverses the component in the direction of its orientation. Thus a shortcut is to say a framing of an oriented link is given by assigning an integer to each link component. 

[[!redirects framed links]]
[[!redirects Framed link]]
[[!redirects Framed links]]
[[!redirects framed knot]]
[[!redirects framed knots]]
[[!redirects Framed knot]]
[[!redirects Framed knots]]
