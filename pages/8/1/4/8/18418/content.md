
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[topology]], the _[[fundamental theorem of covering spaces]]_ asserts that for $X$ a [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply-connected topological space]], then the [[functor]] given by sending a [[covering space]] over $X$ to its [[monodromy]] [[permutation representation|permutation]] [[groupoid representation]] of the [[fundamental groupoid]] $\Pi_1(X)$ of $X$ 

$$
  Fib
    \;\colon\;
  Cov(X) \longrightarrow Set^{\Pi_1(X)}
$$ 

is an [[equivalence of categories]] between the [[category of covering spaces]] and that of [[permutation representation|permutation]] [[groupoid representations]] of $\Pi_1(X)$. This means that there exists a functor the other way around

$$
  Rec 
    \;\colon\;
  Set^{\Pi_1(X)}
    \longrightarrow
  Cov(X)
$$

which is an [[inverse functor]] up to [[natural isomorphism]]. This functor "reconstructs" a covering space $Rec(\rho)$ from a [[permutation representation]] $\rho$ of the [[fundamental groupoid]], such that the [[monodromy]] of $Rec(\rho)$ is [[natural isomorphism|naturally isomorphic]] to the original representation $Fib(Rec(\rho)) \simeq \rho$.


## Details
 {#Details}

We give several equivalent discussions:

1. An [Elementary description](#ElementaryDescription) using just basic [[point-set topology]];

1. A [Description via Coends](#InTermsOfACoend) using [[category theory|category theoretic]] tools.

### Elementary description
 {#ElementaryDescription}

The following is a description of the reconstruction in terms of elementary [[point-set topology]].

+-- {: .num_defn #ElementaryReconstructionCoveringSpace}
###### Definition

Let 

1. $(X,\tau)$ be a [[locally path-connected topological space|locally path-connected]] [[semi-locally simply connected topological space|semi-locally simply connected]] [[topological space]],

1. $\rho \in Set^{\Pi_1(X)}$ a [[permutation representation]] of its [[fundamental groupoid]].

Consider the [[disjoint union]] [[set]] of all the sets appearing in this representation

$$
  E(\rho) \;\coloneqq\;  \underset{x \in X}{\sqcup} \rho(x)
$$

For an [[open subset]] $U \subset X$ which is [[path-connected topological space|path-connected]] and for which every element of the [[fundamental group]] $\pi_1(U,x)$ becomes trivial under $\pi_1(U,x) \to \pi_1(X,x)$, and for $\hat x \in \rho(x)$ with $x \in U$ consider the subset

$$
  V_{U,\hat x}
    \coloneqq
  \left\{
    \rho(\gamma)(\hat x)
    \;\vert\;
    x' \in U
    \,,\phantom{A}
    \gamma \,\text{path from}\, x \,\text{to}\, x'
  \right\}
  \;\subset\;
  E(\rho)
  \,.
$$

The collection of these defines a [[base for a topology]] (prop. \ref{ElementaryReconstructedCoveringSpaceWellDefined} below). Write $\tau_{\rho}$ for the corresponding topology. Then 

$$
  (E(\rho), \tau_{\rho})
$$

is a [[topological space]]. It canonically comes with the function

$$
  \array{
    E(\rho) &\overset{p}{\longrightarrow}& X
    \\
    \hat x \in \rho(x) &\mapsto& x
  }
  \,.
$$

Finally, for 

$$
  f \;\colon\; \rho_1 \longrightarrow \rho_2
$$

a [[homomorphism]] of permutation representations, there is the evident induced function

$$
  \array{
    E(\rho_1)
     &\overset{Rec(f)}{\longrightarrow}&
    E(\rho_2)
    \\
    (\hat x \in \rho_1(x)) &\mapsto& (f_x(\hat x) \in \rho_2(x))
  }
  \,.
$$

=--

+-- {: .num_prop #ElementaryReconstructedCoveringSpaceWellDefined}
###### Proposition

The construction $\rho \mapsto E(\rho)$ in def. \ref{ElementaryReconstructionCoveringSpace} 
is well defined and yields a [[covering space]] of $X$.

Moreover, the construction $f \mapsto Rec(f)$ yields a homomorphism of covering spaces.

=--

+-- {: .proof}
###### Proof

First to see that we indeed have a [[topological space|topology]], we need to check  (by [this prop.](topological+base#Recognition)) that every point is contained in some base element, and that every point in the intersection of two base elements has a base neighbourhood that is still contained in that intersection. 

So let $x \in X$ be a point. By the assumption that $X$ is [[semi-locally simplc connected space|semi-locally simply connected]] there exists an [[open neighbourhood]] $U_x \subset X$ such that every loop in $U_x$ on $x$ is contractible in $X$. By the assumption that $X$ is [[locally path-connected topological space]], this contains an open neighbourhood $U'_x \subset U_x$ which is [[path-connected topological space|path connected]]. As every subset of $U_x$, it still has the property that every loop in $U'_x$ based on $x$ is contractible as a loop in $X$. Now let $\hat x \in E$ be any point over $x$, then it is contained in the base open $V_{U'_x,x}$. 

The argument for the base open neighbourhoods contained in intersections is similar.

 
Then we need to see that $p \colon E(\rho) \to X$ is a [[continuous function]]. Since taking pre-images preserves unions ([this prop.](interactions+of+images+and+pre-images+with+unions+and+intersections#PreImagePreservesUnionsAndIntersections)), and since by semi-local simply connectedness every neighbourhood contains an open $U \subset X$ that labels a base open, it is sufficient to see that $p^{-1}(U)$ is a base open. But by the very assumption on $U$, there is a unique morphism in $\Pi_1(X)$ from any point $x \in U$ to any other point in $U$, so that $\rho$ applied to these paths establishes a bijection of sets 

$$
  p^{-1}(U) 
    \;\simeq\; 
  \underset{\hat x \in \rho(x)}{\sqcup} V_{U,\hat x}
    \;\simeq\;
  U \times \rho(x)
  \,,
$$ 

thus exhibiting $p^{-1}(U)$ as a union of base opens.

Finally we need to see that this continuous function $p$ is a covering projection, hence that every point $x \in X$ has a neighbourhood $U$ such that $p^{-1}(U) \simeq U \times \rho(x)$. But this is again the case for those $U$ all whose loops are contractible in $X$, by the above identification via $\rho$, and these exist around every point by semi-local simply-connetedness of $X$.

This shows that $p \colon E(\rho) \to X$ is a covering space. It remains to see that $Rec(f) \colon E(\rho_1) \to E(\rho_2)$ is a homomorphism of covering spaces. Now by construction it is immediate that this is a function over $X$, in that this [[commuting diagram|diagram commutes]]:

$$
  \array{
    E(\rho_1) && \overset{Rec(f)}{\longrightarrow}&& E(\rho_2)
    \\
    & \searrow && \swarrow
    \\
    && X
  }
  \,.
$$

So it only remains to see that $Rec(f)$ is a [[continuous function]]. So consider $V_{U, y_2 \in \rho_2(x)}$ a base open of $E(\rho_2)$. By [[natural transformation|naturality]] of $f$ its pre-image under $Rec(f)$ is

$$
  Rec(f)^{-1}(V_{U, y_2 \in \rho_2(x)})
  =
  \underset{y_1 \in f^{-1}(y_2)}{\sqcup} V_{U,y_1}
$$

and hence a union of base opens.

=--

### In terms of a coend
 {#InTermsOfACoend}

The following is a description of the reconstruction functor in terms of tolls from [[category theory]].

Given a space $B$, let $|B|$ be $B$ retopologized with the discrete topology, and consider the [[pullback]] in [[Top]] of the [[path space]] $B^I$ to the [[product space]] ${\vert B \vert} \times B$:

$$\array{
Path(B) & \to & B^I & \\
\downarrow & (pb) & \downarrow & \langle ev_0, ev_1 \rangle\\
|B| \times B & \underset{id \times id}{\to} & B \times B & 
}$$ 

Let $\overline{Path}(B)$ be the [[quotient space]] of $Path(B)$ by the [[equivalence relation]] "[[homotopy]] relative to the [[boundary]]". We can think of $\overline{Path}(B)$ as a sum of spaces 

$$\sum_{b \in B} \tilde{B}_b,$$ 

fibered in the obvious way over $|B|$ (the set of all basepoints $b$), where $\tilde{B}_b$ is the space of paths in $B$ which begin at $b$, modulo homotopy-rel-boundary. The space $\tilde{B}_b$ can be thought of the universal covering space over the connected component of a point $b \in B$, considered as a space based at $b$. 

We have a [[span]]

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

with a [[monad]] structure in the [[bicategory]] of [[span]]s. The [[action]] gives a map 

$$comp: \Pi_1(B) \times_{|B|} \overline{Path}(B) \to \overline{Path}(B),$$ 

of spans from $|B|$ to $B$. 

Now suppose given an object $F$ of $Set^{\Pi_1(B)}$, i.e., a covariant action of the fundamental groupoid, that is to say a span $F: 1 \to |B|$ equipped with an action $\alpha$ of the monad $\Pi_1(B): |B| \to |B|$ in $Span(Top)$. The data of a right-handed action $comp$ on $\overline{Path}(B)$ and the left-handed action $\alpha$ on $F$ gives rise to a two-sided [[bar construction]] 

$$B(\overline{Path}(B), \Pi_1(B), F),$$ 

which here is a [[simplicial object]] in the category of spans from $1$ to $B$, whose two face maps from degree 1 to degree 0 take the form: 

$$\array{
  & F \times_{|B|} \Pi_1(B) \times_{|B|} \overline{Path}(B) & 
  \\ 
  & 
  {}^{\mathllap{F \times_{|B|} comp}}\downarrow \downarrow^{\mathrlap{\alpha \times_{|B|} \overline{Path}(B)}} 
  &  
  \\ 
  & 
  F \times_{|B|} \overline{Path}(B) & 
}$$ 

The [[coequalizer]] of this pair provides a canonical augmentation of the two-sided bar construction, and may be called the tensor product 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} F$$ 

(the seemingly opposite placement of the two tensor factors, as compared against the span constructions above, is simply an artifact of the discrepancy between [[diagrammatic order]] of composition, and the traditional order in which right actions are covariant and left actions contravariant).  

As a span from $1$ to $B$, that is as a bundle over $B$, this tensor product is indeed a covering space over $B$, assuming that $B$ is [[locally connected topological space|locally connected]] and [[semi-locally simply connected topological space|semi-locally simply connected]]. Finally, the functor 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} -: Set^{\Pi_1(B)} \to Cov/B$$ 

is under these conditions quasi-inverse to the fiber functor 

$$Fiber: Cov/B \to Set^{\Pi_1(B)}$$ 

and thus establishes the [[equivalence of categories]] known as the [[fundamental theorem of covering spaces]].

+-- {: .un_remark}
###### Remark

An abstract way of considering the functor $Fiber$ is that it is obtained by homming: 

$$Fiber(p: E \to B)(b) = (Cov/B)(\tilde{B}_b, p)$$ 

and this forces its [[left adjoint]] to be given by the tensor product construction described above. 

=--

## Examples

### The universal covering space 

As a special case, consider the [[permutation representation]] $\Pi_1(B) \to Set$ given by the discrete fibration 

$$cod: \Pi_1(B) \to |B|$$ 

+-- {: .query}
[[David Roberts]]: shouldn't such a discrete fibration then give rise to a functor $|B| \to Set$? If you mean $Mor(\Pi_1(B))$, then this could probably be described as the total tangent groupoid, which is the action groupoid for the action of $\Pi_1(B)$ on itself. 

[[Todd Trimble]]: I didn't make myself clear then. Recall that if $C$ is an internal category in a category $E$ (with $E = Set$ in this discussion), then one defines $E^C$ by taking its objects to be internal discrete fibrations, defined as arrows $F \to C_0$ equipped with the data of an action by the internal category $C$, considered as a monoid in spans from $C_0$ to $C_0$. (This is a standard usage of the term "discrete fibration"; see Johnstone's Topos Theory for instance.) Looking over this again, I guess I really should have had $F = Mor(\Pi_1(B))$, and $|B|$ here means the underlying set of $B$. But hopefully my meaning is now clear. 

[[David Roberts]]: Yes, I see now.
=--

(as a span from $1$ to $|B|$) equipped with the obvious (covariant) action of the monad $\Pi_1(B)$ (as a span from $|B|$ to $|B|$). This is essentially the "[[regular representation]]" of the fundamental groupoid. The tensor product of the previous section, 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} cod,$$ 

is a way of realizing the [[universal covering space]] over $B$. 

Here is a way of thinking of this construction which links it to the description of universal bundles by Roberts and Schreiber, which is based on considering tangent spaces of the fundamental groupoid. If the fundamental groupoid $G = \Pi_1(B)$ is connected, its universal bundle (as a fibration of groupoids) may be realized as the "tangent groupoid at $b$" or slice 

$$T_b(G) := (b/G) \to  G$$

 for a chosen basepoint $b \in B$. Note that this slice groupoid is the pullback

$$\array{
(b/G) & \to & G^I & \\
\downarrow & & \downarrow & ev_0\\
\{b\}  & \to & G & 
}$$ 

with $I$ the groupoid $(0 \overset{\sim}{\to} 1)$. This is then a groupoid over $G$ by the restriction of $ev_1$.

Since the set of arrows of $G$ is obtained as a quotient of the set of paths in $B$, it inherits naturally a topology (a quotient of the compact-open topology on $B^I$) which, together with the given topology on $G_0 = B$, makes $G$ a topological groupoid. Then we recover the universal covering space $B^{(1)}_b$ (I prefer this notation for the 1-connected cover, rather than the usual $\tilde{B}$, because it generalises to $B^{(n)}$ for $n$-connected covers - DR) over $B$ by pulling back along the functor $B \to G$, where we consider $B$ as a topological groupoid with only identity arrows. The assumptions on the topology of $B$ mean that $G$ is a [[locally trivial groupoid]] with discrete hom-spaces, which implies that $B^{(1)}_b$ is a locally trivial bundle with discrete fibres.  Local path-connectedness implies that it is locally trivial, and the local condition on $\pi_1$ holds if and only if the fibres are discrete - this last result is due to Daniel Bliss.
 
+--{: .un_remark}
###### Remark

Another way to consider the topological conditions on $B$ is to realise that $\Pi_1(B)$, with its inherited topology, is equivalent to a topologically discrete groupoid (in some appropriate localisation of the 2-category of topological groupoids) if and only if $B$ is locally path-connected and semi-locally simply-connected. Otherwise one has to consider the pro-homotopy 1-type of $B$, as in the theory of algebraic fundamental groups (recall that varieties with appropriate topologies - e.g Zariski - are topologically badly behaved).
=--

+--{: .query}
[[David Roberts]]: Is there a prodiscrete completion of a topological groupoid? Maybe we need to assume it is locally trivial, so it is weakly equivalent (in the said localised 2-category) to a groupoid enriched in $Top$, considered as being internal to $Top$. We could then talk about quotients by wide subgroupoids being topologically discrete. Or even quotients being discrete and having finite Leinster cardinality?? Hmm...
=--

In this analysis, the universal covering space $E_b$ of (path-connected) $B$ is retrieved as the quotient of the space of paths which start at the basepoint $b$, modulo homotopy-rel-boundary; the projection to $B$ takes a class of a path $\phi$ to its terminal point $\phi(1)$. This last description is what one would find in any textbook on algebraic topology dealing with covering spaces. This covering space is, strictly speaking, universal among *connected* covering spaces 

More generally, if $S \subset |B|$ is a set of basepoints (Thanks, Ronnie Brown! - DR), we can form the pullback

$$\array{
(S/G) & \to & G^I & \\
\downarrow & & \downarrow & ev_0\\
S  & \to & G & 
}$$ 

which is again a groupoid over $G$ by restriction of $ev_1$. Then pullback of $(S/G) \to G$ along the inclusion $B \to G$ is a covering space which is the sum 
$$
B^{(1)}\langle S\rangle = \sum_{b\in S} B^{(1)}_b
$$
of connected, 1-connected covering spaces based at the points in $S$. Thus for not-necessarily-connected $B$, taking $S$ such that it intersects each component of $B$ once we can get a universal covering space of $B$ (universal among covering spaces $E \to B$ that induce isomophisms $\Pi_0(E) \to \Pi_0(B)$).

This construction is functorlal (for general $S\subset |B|$), since a map $(B,S) \to (B',S')$ of pairs (remember we are giving $S,S'$ the discrete topology, not the subspace topology) induces a functor of (topological) groupoids $\Pi_1(B) \to \Pi_1(B')$, which by universality of the pulbacks in the above construction gives a map 
$$
B^{(1)}\langle S\rangle \to B'^{(1)}\langle S'\rangle
$$
covering the given map $B \to B'$.

The dependence on basepoints is of course spurious; we can make this explicit by considering the colimit obtained by pasting together the universal covering spaces $B^{(1)}_b$ along isomorphisms induced by paths $b \to c$. But this is in effect how our tensor product construction of the universal covering space works: $\overline{Path}(B)$ is precisely the sum 

$$\sum_{c \in |B|} B^{(1)}_c$$ 

which can be viewed as a topological span from $|B|$ to $B$. The fundamental groupoid acts contravariantly on this sum, and the tensor product 

$$\overline{Path}(B) \otimes_{\Pi_1(B)} (cod: \Pi_1(B) \to |B|)$$ 

is the same thing as the coequalizer of the pair of arrows 

$$\sum_{[\phi]: b \to c} \sum_c B^{(1)}_c \overset{\to}{\to} \sum_c B^{(1)}_c$$ 

in $Top/B$, where one arrow is projection and the other is given by the action of pulling back along classes of paths; this coequalizer is a precise description of the pasting colimit alluded to above. It should be noted that this coequaliser is isomorphic to the covering space $B^{(1)}\langle S\rangle$ when $S$ has one point in each component of $B$, but the description as the tensor product is a priori functorial without reference to a set of basepoints. 

+-- {: .query}
[[David Roberts]]: I think, though, due to the lifting theorems for covering spaces, that given a map $f:B \to B'$ and basepoint sets $S \subset |B|$, $S' \subset |B'|$ that are not necessarily preserved by $f$, there should be a unique lift of $B^{(1)}\langle S\rangle \to B'$ to $B'^{(1)}\langle S'\rangle$ anyway. This would also make this construction independent, up isomorphism, of the choice of basepoints and probably also functorial.

[[David Roberts]]: It won't be functorial - the lift referred to isn't unique. The up-to-isomorphism is a non-canonical isomorphism.
=--



(David or Urs: please feel free to sprinkle your own sugar over this, by adapting or even copying what David wrote below based on your paper.) 

([[David Roberts]]: unless someone feels the discussion below is essential, it can be deleted.)

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



[[!redirects reconstructing covering spaces from monodromy]]
[[!redirects reconstructing a covering space from monodromy]]
