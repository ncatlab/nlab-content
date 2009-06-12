[[!redirects wrapping space]]


A **covering space** (or **wrapping space**) is a [[bundle]] $p: E \to B$ in [[Top]] which is locally trivial and with [[discrete space|discrete]] fiber. That is, a map $p: E \to B$ is a covering space over $B$ if for each point $x \in B$, there exists an open neighborhood $U$ of $x$ **evenly covered** by $p$: the [[pullback]] of $p$ over $U$ is isomorphic to a product bundle with discrete fiber $E_x = p^{-1}(x)$: 

$$\array{
U \times E_x & \cong & p^{-1}(U) & \to & E\\
& \pi \searrow & \downarrow & & \downarrow p\\
& & U & \hookrightarrow & B
}$$

(the square is a pullback and the isomorphism maps $(x, e \in E_x) \mapsto e$). 

Covering spaces over $B$ form an evident [[full subcategory]] $Cov/B \hookrightarrow Top/B$. These can be put together to form a [[replete subcategory|replete]], [[wide subcategory|wide]] subcategory $Cov$ of $Top$, so that $Cov/B$ is an [[over category]], just as the notation suggests.

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

To go in the reverse direction, we take an abstract "highbrow" approach which is formulated with a hoped-for view of higher-dimensional considerations, based on "Trimble fundamental n-groupoids". We need a key tautological construction: given a space $B$, let $|B|$ be $B$ retopologized with the discrete topology, and consider the pullback in $Top$ 

$$\array{
Path(B) & \to & B^I & \\
\downarrow & & \downarrow & \langle ev_0, ev_1 \rangle\\
|B| \times B & \overset{id \times id}{\to} & B \times B & 
}$$ 

The key tautological construction is $\overline{Path}(B)$, the quotient of $Path(B)$ by the equivalence relation "homotopy rel boundary". The underlying set of $\overline{Path}(B)$ can be thought of as 

$$\sum_{b \in B} \Pi_1(B, b)$$ 

fibered in the obvious way over $|B|$ (the set of all basepoints $b$), where $\Pi_1(B, b)$ here denotes the object set of the "tangent groupoid" at the point $b \in B$ (as it is called by Roberts and Schreiber; the tangent groupoid at $b$ is by definition the coslice category $b/ \Pi_1(B)$ of the fundamental groupoid). An object of $\Pi_1(B, b)$ can be thought of as an element $e$ in the universal covering space that lies over the connected component of a basepoint $b$. 

Hence, we have a span

$$\array{
& & \overline{Path}(B) & & \\
& \swarrow & & \searrow & \\
|B| & & & & B
}$$

with an obvious (contravariant) composition action $comp$ of the fundamental groupoid $\Pi_1(B)$, itself regarded as a span 

$$\array{
& & \Pi_1(B) & & \\
& \swarrow & & \searrow & \\
|B| & & & &  |B|
}$$ 

with a monad structure in the bicategory of spans. The action gives a map 

$$comp: \Pi_1(B) \times_{|B|} \overline{Path}(B) \to \overline{Path}(B),$$ 

of spans from $|B|$ to $B$. 

Now suppose given an object $F$ of $Set^{\Pi_1(B)}$, i.e., a covariant action of the fundamental groupoid, that is to say a span $F: 1 \to |B|$ equipped with an action $\alpha$ of the monad $\Pi_1(B): |B| \to |B|$ in $Span(Top)$. The data of a right-handed action $comp$ and the left-handed action gives rise to a two-sided [[bar construction]] $B(\overline{Path}(B), \Pi_1(B), F)$, which here is a simplicial object in the category of spans from $1$ to $B$, whose two face maps from degree 1 to degree 0 take the form: 

$$\array{
& F \times_{|B|} \Pi_1(B) \times_{|B|} \overline{Path}(B) & \\ 
F \times_{|B|} comp & \downarrow \downarrow & \alpha \times_{|B|} \overline{Path}(B) \\ 
& F \times_{|B|} \overline{Path}(B) & 
}$$ 

The coequalizer of this pair provides a canonical augmentation of the two-sided bar construction, and may be called the tensor product 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} F$$ 

(the seemingly opposite placement of the two tensor factors, seen against the span constructions above, is simply an artifact of the discrepancy between diagrammatic order of composition, and the traditional order in which right actions are covariant and left actions contravariant).  

As a span from $1$ to $B$, that is as a bundle over $B$, this tensor product is indeed a covering space over $B$, assuming that $B$ is locally connected and semi-locally simply connected. The functor 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} -: Set^{\Pi_1(B)} \to Cov/B$$ 

is under these conditions quasi-inverse to the fiber functor 

$$Fiber: Cov/B \to Set^{\Pi_1(B)}$$ 

## Special case: the universal covering space ##  

As a special case, consider the permutation representation $\Pi_1(B) \to Set$ given by the discrete fibration 

$$cod: \Pi_1(B) \to |B|$$ 

(as a span from $1$ to $|B|$) equipped with the obvious (covariant) action of the monad $\Pi_1(B)$ (as a span from $|B|$ to $|B|$). This is essentially the "regular representation" of the fundamental groupoid. The tensor product of the previous section, 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} cod,$$ 

is a way of realizing the [[universal covering space]] over $B$. 

Here is a way of thinking of this construction which links it to the description of Roberts and Schreiber, which is based on considering tangent spaces of the fundamental groupoid. Here, if the fundamental groupoid $G = \Pi_1(B)$ is connected, its universal covering space may be realized as a "tangent groupoid" or slice 

$$T_b(G) := B(b/G) \to B G$$

induced from the projection $b/G \to G$, for a chosen basepoint $b \in B$. (There may be some discrepancy with the variance conventions chosen by Roberts and Schreiber; possibly they work with slices instead of coslices, but this makes no essential difference. We will work with coslices.) Then we recover the universal covering space over $B$ by pulling back along a universal classifying map $B \to B G$. More precisely, in their analysis the universal covering space $E_b$ of (path-connected) $B$ is retrieved as the quotient of the space of paths which start at the basepoint $b$, modulo homotopy-rel-boundary; the projection to $B$ takes a class of a path $\phi$ to its terminal point $\phi(1)$. Then of course if $B$ is locally path-connected, its universal covering space can be obtained as the sum of universal covering spaces over each of its path components. 

The dependence on basepoints is of course spurious; we can make this explicit by considering the colimit obtained by pasting together the universal covering spaces $E_b$ along isomorphisms induced by paths $b \to c$. But this is in effect how our tensor product construction of the universal covering space works: $\overline{Path}(B)$ is precisely the sum of tangent groupoids 

$$\sum_{b \in |B|} E_b$$ 

which can be viewed as a topological span from $|B|$ to $B$. The fundamental groupoid acts contravariantly on this sum, and the tensor product 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} (cod: \Pi_1(B) \to |B|)$$ 

is the same thing as the coequalizer of the pair of arrows 

$$\sum_{[\phi]: b \to c} \sum_c E_c \overset{\to}{\to} \sum_c E_c$$ 

in $Top/B$, where one arrow is projection and the other is given by the action of pulling back along classes of paths; this coequalizer is a precise description of the pasting colimit alluded to above. 

(David or Urs: please feel free to sprinkle your own sugar over this, by adapting or even copying what David wrote below based on your paper.) 

+-- {: .query}
[[David Roberts]]: My personal favourite way of doing this is to topologise the fundamental groupoid, then form the following strict pullback of topological groupoids 
$$
\array{
\widetilde{B} & \to & T_b\Pi_1(B) \\
\downarrow && \downarrow\\
B & \to &\Pi_1(B)
}
$$
where $b\in B$ is a chosen basepoint and $T_b\Pi(B)$ is the tangent groupoid at the object $b$. This links the ideas that the tangent groupoid is the contractible cover of a groupoid, that the fundamental groupoid is the 1-type of a space and the Whitehead construction of connected covers (pull back the path-fibration along the inclusion of a space into the appropriate Postnikov section).

The topology on the fundamental groupoid can either be constructed with the assumption that $B$ is locally path-connected and semi-locally simply-connected, or be given the quotient topology from the free path space $B^I$. With this inherited topology, the fundamental groupoid is equivalent (in the bicategory of topological groupoids and [[anafunctor]]s) to the same groupoid considered with the discrete topology if and only if $B$ satisfies the usual conditions for the universal covering space to exist. Thus even when $\Pi_1(B)$ is topologised, it still represents a 1-type for nice $B$. One thing which interests me, even though I have no idea about how to approach it, is how for general $B$ the topologised fundamental groupoid can be considered as a pro-homotopy type, that is, the limit of discrete groupoids, taken in the appropriate (bi)category of topological groupoids.

I would like see several expositions of the construction of the universal covering space, since they illustrate different ideas. They seem tautologously related, but things show a bit more of the differences when one passes to bigroupoids.

The universal covering space is

* the source-fibre (at a basepoint) of the topologised fundamental groupoid

* the pullback of the tangent groupoid as described above

* The pullback of the map $(s,t):Mor(\Pi_1(B)) \to Obj(B)\times Obj(B)$ along the inclusion $\{b\}\times B \to B\times B$

[[Todd Trimble|Todd]] I'll get back to writing more of what I had planned soon. I haven't had a chance to digest what you're writing yet, but I prefer to proceed without having to choose basepoints. I'd like to get you and Urs to have a look though when I get back to this within a few days. 

[[David Roberts|David]]: Of course - hence the theorem about functors from the fundamental groupoid and not the fundamental group. This is where the full tangent groupoid comes in: it is the pullback
$$
\array{
TG & \to & G^I & \\
\downarrow && \downarrow& dom\\
Obj(G) & \to & G &
}
$$
or equivalently the slice $Obj(G)\downarrow id_G$ for an internal groupoid $G$ (internal in $Top$, but extensions to other categories work too). The tangent groupoid at a point $g$ is just the subgroupoid of this gotten by pulling back $TG \to Obj(G)$ along the inclusion $\{g\} \to Obj(G)$. I hadn't thought about applying this construction to my personal universal covering space recipe, so maybe we need to take the discrete topology on $Obj(G)$. That's what your pullback square above seems to indicate. Urs' and my paper [arXiv:0708.1741] has stuff on tangent groupoids for anyone who interested in pitching in.
=--

[To be continued] 
