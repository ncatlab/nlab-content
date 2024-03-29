
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


# Contents 
* table of contents 
{: toc} 

## Definition 

Let $k$ be a [[field]]. A _conic section_ over $k$ is the [[zero locus|zero set]] of a degree 2 [[polynomial]] $p(x, y) \in k[x, y]$ in the [[affine space|affine plane]] $\mathbb{A}^2(k)$, or better yet the zero set of a [[homogeneous polynomial]] $p(x, y, z)$ of degree 2 in the [[projective space|projective plane]] $\mathbb{P}^2(k)$. 

## Over the real numbers 

In the classical case $k = \mathbb{R}$ of [[real numbers]], conic sections may be pictured in terms of [[intersections]] of a standard [[cone]] $x^2 + y^2 - z^2 = 0$ in affine 3-space with various affine hyperplanes (hence the name, "conic section"). In this picture, _nonsingular_ conic sections are classified (up to [[automorphisms]] of the affine plane) by the sign of the [[discriminant]] of $p$. In other words, if we write $p(x, y) = a x^2 + b x y + c y^2 + \lambda(x, y)$ where $deg(\lambda) = 1$ and put $D = b^2 - 4 a c$, then an isomorphism class is one of three types: ellipses (when $D \lt 0$), parabolas ($D = 0$), and hyperbolas ($D \gt 0$). Of course when we admit possibly singular conic sections, we get further isomorphism classes involving some degree of degeneracy (e.g., two lines, a double line, etc.). 

The distinctions between [[ellipse]], [[parabola]], and [[hyperbola]] are artifacts of affine geometry: if we instead consider conic sections as projective [[algebraic variety|subvarieties]] of $\mathbb{P}^2(\mathbb{R})$, then considered up to projective transformations (automorphisms of the projective plane), these distinctions evaporate and there is really only one kind of nonsingular conic section. Put differently: if we fix a representation $\mathbb{P}^2(\mathbb{R}) = \mathbb{A}^2(\mathbb{R}) \sqcup L$ where $L$ is a chosen "line at infinity", then in the original classification up to affine transformations, i.e., the subgroup of projective transformations which take $L$ to itself, ellipses are those conic sections which do not intersect $L$, parabolas are those which intersect $L$ in a double point, and hyperbolas are those which intersect $L$ in two points. By enlarging to the group of all projective transformations, we can move $L$ to a line which *does* intersect an "ellipse" in two points, making it a "hyperbola" with respect to the new coordinate system, etc. 

## Stereographic projection 

Considered in terms of projective geometry, all *pointed*[^1] nonsingular conic sections $C \subset \mathbb{P}^2(k)$ are isomorphic and can be identified explicitly with a projective line $\mathbb{P}^1(k)$ by means of a [[stereographic projection]]. 

Geometrically, if $p$ is the chosen basepoint of $C$ and $L \subset \mathbb{P}^2(k)$ is a line not incident to $p$, then for any other point $q$ of $C$ the unique line $L(p, q)$ incident to $p$ and $q$ intersects $L$ in exactly one point, denoted $\phi(q)$. (Here $\phi(p)$ to be the intersection of the _tangent_ to $p$ at $C$ with $L$; this can be considered the basepoint of $L$.) In the opposite direction, to each point $x$ of $L$, the line $L(p, x)$ intersects $C$ in $p$ and (since a quadratic with one root will also have another root) another point $q$ (which might be the same as $p$; this happens precisely when $L(p, x)$ is the tangent at $p$); this gives the inverse $\phi^{-1}(x) = q$. In this way we obtain an isomorphism $\phi: C \to L$ of subvarieties. 

Working over an [[algebraically closed field]] $k$, where every nonsingular conic $C$ has a point, we may conclude that $C$ is isomorphic (as a projective variety) to $\mathbb{P}^1(k)$. Hence $C$ is a curve of [[genus]] $0$. 

[^1]: We took care to say *pointed*: note that depending on the field $k$, there might not even be a solution point on the conic $C$, even if $C$ is by all rights nonsingular. For example, consider $p(x, y) = x^2 + y^2 + 1$ over $\mathbb{R}$. Of course we can relax again if $k$ is algebraically closed. 

## Projective duality 

Working over an [[algebraically closed field]] $k$ (let us assume the [[characteristic]] is not $2$), all nondegenerate [[quadratic forms]] on a vector space $V$ are isomorphic and we may fix one as standard. For example, for $V = k^3$, we may fix attention on the quadratic form $q(x, y, z) = x^2 + y^2 + z^2$, which determines a conic section $C \subset \mathbb{P}^2(k)$ and an accompanying nondegenerate symmetric [[bilinear form]] $\langle-, -\rangle_q: V \times V \to k$. 

Projective duality relative to $C$ is the projectivization of linear duality with respect to $\langle -, - \rangle$, which takes a linear subspace $L$ to its [[orthogonality|orthogonal dual]] $L^\perp = \{v \in V: (\forall w \in L)\; \langle v, w \rangle = 0\}$. We note that the orthogonal dual is an involution that takes joins of subspaces to meets and vice-versa. This construction descends through the quotient $k^3 \backslash \{0\} \to \mathbb{P}^2(k)$ to give an operation that takes points in $\mathbb{P}^2(k)$ (lines in $k^3$) to lines in $\mathbb{P}^2(k)$ (hyperplanes in $k^3$), and vice-versa, and moreover takes a join of two distinct points (the line incident to them) to the meet of their dual lines (the point of their intersection). 

This duality may be visualized thus: given a nondegenerate conic $C$ and a point $p$ off of $C$, draw the two lines incident to $p$ that are tangent to $C$, and pass to the line incident to the tangent points. (This is easier to visualize by imagining $k = \mathbb{R}$ and considering a point $p$ exterior to say an ellipse $C$.) This defines the line that is projectively dual to $p$ (dual with respect to the conic $C$); if $p$ is *on* $C$, then the same procedure works by considering the two tangent points as infinitesimally close to $C$, so that the line between them is the tangent line at $p$: the projective dual of $p$ on $C$ is its tangent line (this is the case where the line in $k^3$ corresponding to $p$ is isotropic with respect to the bilinear form). 

The entire procedure can be reversed and gives an anti-[[involution]] on the [[poset]] of flats of $\mathbb{P}^2(k)$, interchanging points and lines and interchanging meets and joins. 

More generally, projective duality can be described in terms of an orthogonality map $\mathbb{P}(V) \to \mathbb{P}(V^\ast)$, where $V^\ast$ is the linear dual of $V$, which maps a subvariety to a corresponding dual "envelope" subvariety. This is explored in [GKZ](#GKZ). The role of the conic section (or generally a conic hypersurface) is simply to set up an explicit self-duality $\mathbb{P}(V^\ast) \cong \mathbb{P}(V)$. 

## Pascal's "mystic hexagon" 

(...) 

## References 

* I.M. Gel'fand, M. Kapranov, A. Zelevinsky, _Discriminants, Resultants, and Multidimensional Determinants_, Birkh&#228;user 2008 (paperback edition). 
 {#GKZ} 

[[!redirects conic sections]] 
[[!redirects conic]] 
[[!redirects conics]] 
