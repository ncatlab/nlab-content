A **covering space** is a [[bundle]] $p: E \to B$ in [[Top]] which is locally trivial and with [[discrete space|discrete]] fiber. That is, a map $p: E \to B$ is a covering space over $B$ if for each point $x \in B$, there exists an open neighborhood $U$ of $x$ **evenly covered** by $p$: the [[pullback]] of $p$ over $U$ is isomorphic to a product bundle with discrete fiber $E_x = p^{-1}(x)$: 

$$\array{
U \times E_x & \cong & p^{-1}(U) & \to & E\\
& \pi \searrow & \downarrow & & \downarrow p\\
& & U & \hookrightarrow & B
}$$

(the square is a pullback and the isomorphism maps $(x, e \in E_x) \mapsto e$). 

Covering spaces over $B$ form an evident [[full subcategory]] $Cov/B \hookrightarrow Top/B$. These can be put together to form a full subcategory $Cov$ of $Top$, so that $Cov/B$ is an [[over category]], just as the notation suggests.

## Remarks ##

* Different points in $B$ may have non-isomorphic fibers. However, if open sets $U$ and $V$ are evenly covered by $p: E \to B$ and have nonempty intersection, then there are canonical identifications 
$$E_x \cong E_z \cong E_y$$ 
between typical fibers over $x \in U$, $y \in V$, and $z \in U \cap V$. If $B$ is path-connected, then all the fibers match up to isomorphism (by the unique path-lifting lemma; see below). 

* Fibers may be empty. Some authors choose to forbid that, adding the condition that $p$ be a surjection, but the resulting category of covering projections over a space $B$ is not as nice as it would be without that condition. 

* The terms "covering space" and "covering projection", while traditional, are certainly not optimal: they mislead by being too close to (open) "[[cover|coverings]]". [[James Dolan]] has suggested "wrapping space" as an alternative (as in the image of thread wrapping around a spool, to evoke the archetypal example of a covering projection, $p: \mathbb{R} \to S^1: x \mapsto \exp(i x)$). 

## Fundamental theorem of covering spaces ## 

The connection between covering spaces over $B$ and the [[fundamental group]] $\pi_1(B)$ (for $B$ a [[connected space]]) is very old and runs very deep. An updated account involves shifting attention to representations of the [[fundamental groupoid]] $\Pi_1(B)$ (regardless of connectedness); we give a brief outline of the theory here. 

Under some technical topological assumptions on the space $B$, the fundamental theorem can be stated thus: 

+-- {: .un_thm}
###### Theorem

The category of covering spaces $Cov/B$ is equivalent to the category of functors $\Pi_1(B) \to Set$. 

More precisely, the equivalence $Cov/B \to Set^{\Pi_1(B)}$ sends a covering space $p: E \to B$ to the functor which maps the object $b \in \Pi_1(B)$ to the fiber $p^{-1}(b)$. 
=--

...

The key construction underlying this is the _[[universal covering space]]_ of $B$. Let $|B|$ be $B$ retopologized with the discrete topology, and consider the pullback in $Top$ 

$$\array{
Path(B) & \to & B^I & \\
\downarrow & & \downarrow & \langle ev_0, ev_1 \rangle\\
|B| \times B & \overset{id \times id}{\to} & B \times B & 
}$$ 

... 

+-- {: .query}
[[David Roberts]]: My personal favourite way of doing this is to topologise the fundamental groupoid, then form the following strict pullback of topological groupoids 
$$
\array{
\widetilde{B} & \to & T_b\Pi_1(B) \\
downarrow && \downarrow\\
B & \to \Pi_1(B)
}
$$
where $b\in B$ is a chosen basepoint and $T_b\Pi(B)$ is the tangent groupoid at the object $b$. This links the ideas that the tangent groupoid is the contractible cover of a groupoid, that the fundamental groupoid is the 1-type of a space and the Whitehead construction of connected covers (pull back the path-fibration along the inclusion of a space into the appropriate Postnikov section).

The topology on the fundamental groupoid can either be construted with the assumption that $B$ is locally path-connected and semi-locally simply-connected, or be given the quotient topology from the free path space $B^I$. With this inherited topology, the fundamental groupoid is equivalent (in the bicategory of topological groupoids and [[anafunctor]]s) to the same groupoid considered with the discrete topology if and only if $B$ satisfies the usual conditions for the universal covering space to exist. Thus even when $\Pi_1(B)$ is topologised, it still represents a 1-type for nice $B$. One thing which interests me, even though I have no idea about how to approach it, is how for general $B$ the topologised fundamental groupoid can be considered as a pro-homotopy type, that is, the limit of discrete groupoids, taken in the appropriate (bi)category of topological groupoids.

I would like see several expositions of the construction of the universal covering space, since they illustrate different ideas. They seem tautologously related, but things show a bit more of the differences when one passes to bigroupoids.

The universal covering space is

* the source-fibre (at a basepoint) of the topologised fundamental groupoid

* the pullback of the tangent groupoid as described above

* The pullback of the map $(s,t):Mor(\Pi_1(B)) \to Obj(B)\times Obj(B)$ along the inclusion $\{b\}\times B \to B\times B$


=--

[To be continued] 
