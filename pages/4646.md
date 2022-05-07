
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A [[connection on a bundle]] $\nabla$ for $\pi : P \to X$ a $G$-[[principal bundle]] encodes data that assigns to each path $\gamma : [0,1] \to X$ a [[homomorphism]]

$$
  tra_\nabla(\gamma) : P_{\gamma(0)} \to P_{\gamma(1)}
$$

between the [[fiber]]s of the bundle, such that this assignment depends well (e.g. smoothly) on the choice of path and is compatible with composition of paths.

This assignment is called the _parallel transport_ of the connection.


### The idea of parallelism

The term "parallel" comes from one of the many equivalent definitions of the notion of [[connection on a bundle]]: the original formulation of [[Ehresmann connection]]s.

In that formulation, the connection is encoded at each point $p \in P$ in the total space by a decomposition of the [[tangent space]] $T_p P$ as a [[direct sum]] $T_p P \simeq V_p \oplus H_p$ of [[vector space]]s, such that

* $V_p = \ker \pi_*|_p$ is the [[kernel]] of the projection map that sends vectors in the total space to vectors in base space (this part is fixed by the choice of $p : P \to X$);

* $H_p \subset T_p P$ is a _choice_ of complement, such that this choice varies smoothly over $P$ in an evident sense and is compatible with the $G$-[[action]] on $P$.

The vectors in $V_p$ are called _vertical_ , the vectors in $H_p$ are called _horizontal_ . One may think of this as defining locally in which way the base space sits horizontally in the total space, equivalently as identifying locally a "smoothly varying local trivialization" of $P$.

More precisely, given such a choice of horizontal subspaces, there is for every path $\gamma : [0,1] \to X$ and every choice of lift $\hat \gamma(0) \in P$ of the start point $\gamma(0)$ to the total space of the bundle, a _unique lift_ $\hat \gamma : [0,1] \to P$ of the entire path to the total space:

$$
  \array{
     \hat \gamma(0) &\stackrel{\hat \gamma}{\to}& \hat \gamma(1)
     && \in & P
     \\
     && &&& \downarrow^{\mathrlap{\pi}}
     \\
     \gamma(0) &\stackrel{\gamma}{\to}& \gamma(1) 
     && \in & X
  }
  \,
$$

such that $\hat \gamma$ is everywhere _parallel_ (to $X$) in that all its tangent vectors sit in the horizontal subspaces chosen:

$$
  (\partial_\sigma \hat \gamma)(\sigma) \in H_{\gamma(\sigma)} \subset T_{\gamma(\sigma)} P
  \,.
$$

In other words, this means that given a path $\gamma$ down in $X$, we may _transport_ any point $p \in P_{\gamma(0)}$ above its start point _parallely_ (with respect to the notion of parallelism determined by $\nabla$) along $\gamma$, to find a uniquely determined point $tra_\nabla(\gamma)(p) \in P_{\gamma(1)}$ over the endpoint.


### The category-theoretic perspective

The parallel transport-assignment of fiber-homomorphisms to paths

$$
  (x \stackrel{\gamma}{\to} y) \mapsto ( P_x \stackrel{tra_\nabla(\gamma)}{\to} y ) 
$$

enjoys the following properties:

* it is invariant under [[thin homotopy]] of paths;

* it is compatible with composition of paths and sends constant paths to identity homomorphisms;

* it sends smooth families of paths to compatible smooth families of homomorphisms.

This may be equivalently but more succinctly be formulated as follows:

We say _diffeological groupoid_ for an [[internal groupoid]] in the category of [[diffeological space]]s. 

The smooth paths in a smooth manifold $X$ naturally form the diffeological groupoid called the [[path groupoid]] $P_1(X)$.  Objects are points in $X$, morphsims are [[thin homotopy]]-classes of smooth paths which are constant in a neighbourhood of their boundary, composition is concatenation of paths.

For $P \to X$ any $G$-bundle, there is also naturally the diffeological groupoid $At(P)$ -- the [[Atiyah Lie groupoid]]  of $P$. Objects are points in $X$, morphisms are homomorphisms of $G$-[[torsor]]s between the [[fiber]]s over these points.

Then the above properties of parallel transport are equivalent to saying that we have an [[internal functor]]

$$
  tra : P_1(X) \to At(P)
$$

that is the identity on objects. Moreover, this functor _uniquely_ characterizes the [[connection on a bundle|connection]] on $P$ that it comes from. This means that we may identify connections on $P$ with their parallel transport functors. 


But even the bundle $P$ itself is encoded in such functors. If instead of looking at the category of internal groupoids and internal functors, we look at the larger [[2-topos]] of _diffeological stacks_  -- [[stack]]s over [[CartSp]]. 

Then we can take simply the diffeological [[delooping]] groupoid $\mathbf{B}G$, which has a single object and $G$ as its [[hom-set]] and consider morphisms 

$$
  tra : P_1(X) \to \mathbf{B}G
$$
 
in the 2-topos. These are now given by [[anafunctors]] of internal groupoids, and one finds that they encode a [[Cech cohomology|Cech cocycle]] for a $G$-principal bundle $P$ together with the parallel transport of a connection over it.

This is discussed in more detail at

* [[∞-Chern-Weil theory -- preparatory concepts]].

There is also the diffeological groupoid incarnation of the [[fundamental groupoid]] $\Pi_1(X)$ of $X$. Its morphisms are full [[homotopy]]-classes of paths. There is a canonical projection $P_1(X) \to \Pi_1(X)$ that sends a thin-homotopy class of paths to the corresponding full-homotopy class.  

A parallel transport functor $tra : P_1(X) \to G$ factors through $\Pi_1(X)$ precisely if the corresponding connection is _flat_ in that its [[curvature form]] vanishes.


### In physics

In [[physics]], a [[connection on a bundle]] over $X$ models a [[gauge field]] such as the [[electromagnetic field]] or more generally a [[Yang-Mills field]] or the field of [[gravity]] on a [[spacetime]] $X$.

The [[force]]s exerted by such gauge fields on  charged particles propagating on $X$ (i.e. [[electron]]s, [[quark]]s and generally massive particles, respectively) are encoded precisely in the parallel transport assignment of the gauge field connection to their trajectories.

More precisely, the exponentiated [[action functional]] for the electron propagating on $X$ in the presence of an electromagnetic field $\nabla$ is the functional on the space of paths in $X$ given by

$$
  \gamma \mapsto \exp(i S_{kin}(\gamma)) \cdot tra_\nabla(\gamma)
  \,,
$$

where the first term is the standard [[kinetic action]]. If $\nabla$ is a (nontrivial) connection on a trivial bundle, then, as described [below](#Of1Form) it is encoded by a [[differential form]] $A \in \Omega^1(X)$ -- called the _vector potential_  in physics -- and we have

$$
  tra_\nabla(\gamma) = \exp\big(i \int_[0,1] \gamma^* A\big)
  \,.
$$

The [[Euler-Lagrange equations]] induced by this functional express precisely the [[Lorentz force]] encoded by $A$ acting on the particle.

If instead of looking at the [[quantum mechanics]] of the quantum particle charged under a fixed background gauge field look at the [[quantum field theory]] of that gauge field itself, we can use the action functional of particles to _probe_ these background fields and obtain quantum observables for them. 

This converse assignment where we _fix_ a path $\gamma$ and regard the parallel transport then as a functional over the space of all connections over $X$

$$
  tra_{(-)}(\gamma) : connections \to fiber-homomorphisms
$$

is called the **[[Wilson line]]-observable** of the theory. Or rather its expectation value in the [[path integral]] weighted by the action functional of the gauge theory is called such, schematically:

$$
  W_\gamma := \langle tra_{(\nabla)}(\gamma)\rangle
  = 
  \int D \nabla \; \exp(i S_{gauge\;theory}(\nabla)) 
    tra_\nabla(\gamma)
  \,.
$$


## Special cases

### Trivial bundle: parallel transport of a 1-form {#Of1Form}

Of $P \to X$ is a _trivial bundle_ in that $P = X \times G$, then a connection on this is equivalently encoded in a [[Lie-algebra valued 1-form]]

$$
  A \in \Omega^1(X, \mathcal{g})
$$


on $X$.

In terms of this, parallel transport is a solution to a [[differential equation]].

For $\gamma : [0,1] \to X$ we have the pull-back 1-form $\gamma^* A \in \Omega^1([0,1])$. For $f \in C^\infty([0,1], G)$ a smooth function with values in the [[Lie group]] $G$, consider the differential equation

$$
  d f + \rho(f)_*(\gamma^*A) = 0
  \,,
$$

where $d f : T [0,1] \to T G$ is the differential of $f$ and where $\rho : G \times G \to G$ is the left [[action]] of $G$ on itself (i.e. just the multiplication on $G$) and $r(f)_* : T G \to T G$ its differential and using the defining identification $\mathfrak{g} \simeq T_e G$ we take $r(f)_*(A)$ to be the composite $T [0,1] \stackrel{\gamma^* A}{\to} \mathfrak{g} \hookrightarrow T G \stackrel{r(f)_*}{\to} T G$.

If $G$ is a [[matrix Lie group]] such as the [[orthogonal group]] $O(n)$ or the [[unitary group]] $U(n)$, then also its Lie algebra identifies with matrices, and we may write this simply as

$$
  d f + \gamma^*(A) \cdot f  = 0
  \,,
$$

where the dot is matrix multiplication.

By general results on [[differential equations]], this type of equation has a unique solution for each choice of value of $f(0)$.

+-- {: .un_defn}
###### Definition
The parallel transport of $A \in \Omega^1(X,\mathfrak{g})$ along a path $\gamma : [0,1] \to X$ which we write

$$
  tra_A(\gamma) := P \exp(\int_{[0,1]} \gamma^* A) \in G
$$

is the value $f(1) \in G$ for the unique solution of the equation $d f  + \rho(f)_*(A) = 0$ with initial value $f(0) = e$ (the neutral element in $G$).
=--

The notation here is motivated from the special case where $G = \mathbb{R}$ is the group of [[real number]]s. In that case the [[Lie algebra]] $\mathfrak{g} \simeq \mathbb{R}$ is abelian, the differential equation above is simply

$$
  d f = \gamma^*(A) \wedge f
$$

for a real valued function $f \in C^\infty([0,1])$, and the unique solution to that with $f(0) = e = 0$ is literally the exponential of the integral of $A$:

$$
  tra_A(\gamma) = \exp(\int_{[0,1]} \gamma^* A)
  \,.
$$

In the case of general nonabelian $\mathfrak{g}$ this simple exponential formula gives the wrong result. One can see that a slightly better approximation to the correct result is given by

$$
  \exp(\int_{[0,1/2]} \gamma^* A) \cdot \exp(\int_{[1/2,1]} \gamma^* A)
$$

and an even a bit more better approximation by

$$
  \exp(\int_{[0,1/3]} \gamma^* A) \cdot \exp(\int_{[1/3,2/3]} \gamma^* A)
   \cdot \exp(\int_{[2/3,1]} \gamma^* A)
$$

and so on, with the correct result being the limit of this sequence -- if one defines it carefully -- as we integrate piecewise over ever smaller pieces of the path.

This is called a **path-ordered integral**. The "P" in the above formula is short for "path ordering". Possibly this notation originates in [[physics]] where the above is known as the [[Dyson formula]]. 


## Higher parallel transport

The notion of [[connection on a bundle]] generalizes to that of [[connection on a 2-bundle]]. [[connection on a 3-bundle]] and generally to that of [[connection on an ∞-bundle]]. The come with a notion of _higher parallel transport_ over manifolds of dimension greater than 1.

See [[higher parallel transport]] for details.

## Related concepts

* [[connection on a bundle]], [[connection on a 2-bundle]], [[connection on an infinity-bundle]],

* **parallel transport**, [[higher parallel transport]], [[super parallel transport]]

  * [[nonabelian Stokes theorem]]

* [[holonomy]]

  * [[holonomy group]]

  * [[special holonomy]]

## References

There are many equivalent statements of the ordinary definition of a [[connection on a bundle]]. The following lists references related to the statement that the connection is equivalently encoded in terms of its [[parallel transport]].

Apparently one of the oldest occurrences of the idea that a  [[principal bundle]] $P \to X$ with [[connection on a bundle|connection]] $\nabla$ may be reconstructed from its [[holonomy|holonomies]] around all smooth loops for any fixed base point in the connected base space $X$ appears in

* S. Kobayashi, Comptes Rendus, 238, 443-444. (1954). ([web](http://gallica.bnf.fr/ark:/12148/bpt6k31909/f443.item))

A more detailed and more general discussion has then been given in 

* John Milnor, Annals of Mathematics, 63, 272-284.(1956). 

A detailed discussion of the differentiable case appears is

* Costake Teleman  _Généralisation du groupe fondamental_, Annales Scientifiques de l?école Normale Supérieure 3, 77, 195-234. (1960) ([numdam:ASENS_1960_3_77_3_195_0](http://www.numdam.org/item?id=ASENS_1960_3_77_3_195_0))

* Costake Teleman, Annali di Matematica, Pura ed Applicata, LXII, 379-412. (1963). 

This history is recollected in the introduction of

* [[John Barrett]], _Holonomy and path structures in general relativity and Yang-Mills theory_, Int. J. of Theor. Phys., Iiol. 30, No. 9, 1991 ([doi:10.1007/BF00671007](https://doi.org/10.1007/BF00671007))

who himself gives a proof. Barret implicitly uses the  [[diffeological space]] structure on the space of loops.

Followups:

* [[Piotr Hajac]], _Axiomatic holonomy maps and generalized Yang-Mills moduli space_, Letters in Mathematical Physics volume 27, pages301–309 (1993) ([doi:10.1007/BF00777377](https://doi.org/10.1007/BF00777377))

A note on how a 1-form is encoded in the parallel transport that it induces along paths is also in

* [[Daniel Freed]], [appendix B](http://arxiv.org/PS_cache/hep-th/pdf/9206/9206021v1.pdf#page=56) of: _Classical Chern-Simons theory, Part I_ ([arXiv:hep-th/9206021](http://arxiv.org/abs/hep-th/9206021))  


In

* Jerzy Lewandowski _Group of loops, holonomy maps, path bundle and pathconnection_, Class. Quantum Grav. 10 (1993) 879-904 ([pdf](http://ej.iop.org/links/r8XqKR99r/8rbzxFDZ2xGeFw29av5vpA/cq930508.pdf))

the statement of the equivalence is attributed to

* Jeeva Anandan, _Holonomy groups in gavity and gauge fields_, Pmc. Conf Differential Geometric Methods in Plystcs (fieste 1981) ed. G Denardo and H. D. Doebner (Singapore, World Scientific) ([spire:169409](https://inspirehep.net/literature/169409))

Therein it is shown that smoothness of the [[parallel transport]] is a necessary condition for it to come from a smooth bundle with connection. Barrett also shows that this is sufficient.

Lewandowski adds to this a formulation of an equivalence of bundles with connections and the subset of loops around which the corresponding parallel transport is trivial. 

Around the same time appeared

* A. Caetano, [[Roger Picken]], _An axiomatic definition of holonomy_, Int. Journ. Math. 5 (1994) 835 ([scan](http://ccdb4fs.kek.jp/cgi-bin/img_index?9405501), [doi:10.1142/S0129167X94000425](https://doi.org/10.1142/S0129167X94000425))

that generalizes these ideas from loops to general paths. These authors introduced the idea of sitting instants of paths and noticed that the most elegant way to (re)state the maximal equivalence relation on paths which is respected by parallel transport is in terms of [[thin homotopy]].

Barrett originally had something very similar but slightly different. With Caetano and Picken's relation, the space of thin homotopy classes of paths in $X$ becomes an groupoid $\mathbf{P}_1(X)$ -- the [[path groupoid]] -- internal to [[diffeological space]].

Discussion in terms of local functorial data that lends itself to generalization to [[higher parallel transport]] is given in

* [[Urs Schreiber]], [[Konrad Waldorf]], _Parallel Transport and Functors_, J. Homotopy Relat. Struct. 4, 187-244 (2009) ([arXiv:0705.0452](https://arxiv.org/abs/0705.0452))


A quick proof that bundles with connections are encoded in their parallel transport along paths was noted in 

* [[Florin Dumitrescu]], _Connections and Parallel Transport_, Journal of Homotopy and Related Structures, vol. 5(1), 2010, pp.171–175 ([arXiv:0903.0121](http://arxiv.org/abs/0903.0121)).


For more see the references at [[connection on a bundle]].

A discussion of parallel transport in the [[tangent bundle]] in terms of [[synthetic differential geometry]] (motivated by a discussion of [[gravity]]) is in 

* [[Gonzalo Reyes]], _General Relativity: Affine connections, parallel transport and sprays_ ([pdf](https://marieetgonzalo.files.wordpress.com/2009/01/affineconnections.pdf))

