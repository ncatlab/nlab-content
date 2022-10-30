+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Lie groupoid_ is a [[groupoid]] [[internal groupoid|internal]] to [[smooth manifolds]]. This is a joint generalization of [[smooth manifolds]] and [[Lie groups]] to [[higher differential geometry]].

Regarded in the more general context of [[smooth groupoids]]/[[smooth stacks]], Lie groupoids present certain well-behaved such objects, often called _[[differentiable stacks]]_.

## Definition

A _Lie groupoid_ $X$ is an [[internal groupoid]] in the [[category]] [[Diff]] of [[smooth manifolds]].

Since [[Diff]] does not have all [[pullbacks]], to ensure that this definition makes sense, one needs to ensure that the space $Mor(X) \times_{s,t} Mor(X)$ of composable [[morphism]]s is an object of [[Diff]]. This is achieved either by adopting the definition of [[internal groupoid]] in the sense of Ehresmann, which includes as data the [[smooth manifold]] of [[composable pairs]], or by taking the conventional route and demanding that the source and target maps $s,t : Mor(X) \to Obj(X)$ are [[submersion]]s. This ensures the [[pullback]] exists to define said manifold or composable pairs.

But for most practical purposes, the apparently evident [[2-category]] $Grpd(Diff)$ of such internal groupoids, [[internal functor]]s and internal [[natural transformation]]s is _not_ the correct 2-category to consider. One way to see this is that the [[axiom of choice]] fails in [[Diff]], which means that an internal functor $X \to Y$ of internal groupoids which is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]] may nevertheless not be an equivalence, in that it may not have a weak inverse in $Grpd(Diff)$.

See the section [2-Category of Lie groupoids](#2CatOfGrpds) below.

A bit more general than a Lie groupoid is a [[diffeological groupoid]].


### Terminology

Originally Lie groupoids were called (by Ehresmann) _differentiable groupoids_ (and also one considered differentiable _categories_). Sometime in the 1980s there was a change of terminology to _Lie groupoid_ and [[differentiable stack]]s. (reference?)



### Specialisations

One definition which Ehresmann introduced in his paper _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_ (see below) is that of [[locally trivial category|locally trivial groupoid]]. It is defined more generally for topological categories, and extends in an obvious way to topological groupoids, and Lie categories and groupoids. For a topological (resp. Lie) category $X$, let $X_1^{iso}$ denote the subspace (resp. submanifold) of invertible arrows . (This always exists, by general abstract nonsense - I should look up the reference, it's in Bunge-Pare I think - [[David Roberts|DR]])

+-- {: .num_defn}
###### Definition 
A topological groupoid $X_1 \rightrightarrows X_0$ is **locally trivial** if for every point $p\in X_0$ there is a neighbourhood $U$ of $p$ and a lift of the inclusion $\{p\} \times U \hookrightarrow X_0 \times X_0$ through $(s,t):X_1^{iso}\to X_0 \times X_0$. 
=--

Clearly for a Lie groupoid $X_1^{iso} = X_1$. It is simple to show from the definition that for a transitive Lie groupoid, $(s,t)$ has local sections. Ehresmann goes on to show a link between smooth [[principal bundles]] and transitive, locally trivial Lie groupoids. See [[locally trivial category]] for details.

### The (2,1)-category of Lie groupoids {#2CatOfGrpds}


As usual for internal categories, the naive 2-category of internal groupoids, [[internal functor]]s and internal [[natural transformation]]s is not quite "correct". One sign of this is that the [[axiom of choice]] fails in [[Diff]] so that an internal functor which is an [[essentially surjective functor]] and a [[full and faithful functor]] may still not have an internal weak inverse.

One way to deal with this is to equip the 2-category with some structure of a [[homotopical category]] and allow morphisms of Lie groupoids to be [[anafunctor]]s, i.e. [[span]]s of internal functors $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$.

Such generalized morphisms -- called _[[Morita morphisms]]_ or _generalized morphisms_ in the literature -- are sometimes modeled as [[bibundle]]s and then called [[Hilsum-Skandalis morphism]]s.

Another equivalent approach is to embed Lie groupoids into the context of [[2-topos]] theory:

The [[2-topos|(2,1)-topos]] $Sh_{(2,1)}(Diff)$ of [[stack]]s/[[2-sheaves]] on [[Diff]] may be understood as a nice [[2-category]] of general groupoids _modeled on_ [[smooth manifold]]s. The degreewise [[Yoneda embedding]] allows to emebed groupoids internal to $Diff$ into stacks on $Diff$. this wider context contains for instance also [[diffeological groupoid]]s.

Regarded inside this wider context, Lie groupoids are identified with [[differentiable stack]]s. The [[(n,r)-category|(2,1)-category]] of Lie groupoids is then the full sub-$(2,1)$-category of $Sh_{(2,1)}(Diff)$ on differentiable stacks.

For more comments on this, see also the beginning of [[∞-Lie groupoid]].

## Lie algebroids

As the [[infinitesimal space|infinitesimally]] approximation to a [[Lie group]] is a [[Lie algebra]], so the infinitesimal approximation to a Lie groupoid is a [[Lie algebroid]].

## Higher Lie groupoids

See

* [[internal ∞-groupoid]]

* [[∞-Lie groupoid]]

## Examples

* Every [[smooth manifold]] $X$ is a 0-[[0-groupoid|truncated]] Lie groupoid.

* For every [[Lie group]] $G$ the one-object [[delooping]] groupoid $\mathbf{B}G$ is a Lie groupoid.

* The Lie group $G$ itself is a 0-[[truncated]] [[group object]] in the 2-category or Lie groupoids.

* Every [[Lie 2-group]] is in particular a Lie groupoid: a [[group object]] in the category of Lie groupoids.

* The [[inner automorphism 2-group]] $\mathbf{E}G = INN(G) = G//G$ is a Lie groupoid. There is an obvious morphism $\mathbf{E}G \to \mathbf{B}G$.

* For every $G$-[[principal bundle]] $P \to X$ there is its [[Atiyah Lie groupoid]] $At(P)$.


* The [[fundamental groupoid]] $\Pi_1(X)$ of a smooth manifold is naturally a Lie groupoid.

* The [[path groupoid]] of a smooth manifold is naturally a [[diffeological groupoid]].

* The [[Cech groupoid]] $C(U)$ of a [[cover]] $\{U_i \to X\}$ of a smooth manifold is a Lie groupoid. 

* Every [[foliation]] gives rise to its [[holonomy groupoid]].

* An [[orbifold]] is a Lie groupoid.

* An [[anafunctor]] $X \stackrel{\simeq}{\leftarrow} C(U) \to \mathbf{B}G$ from a smooth manifold $X$ to $\mathbf{B}G$ is a [[Cech cohomology|Cech cocycle]] in degree 1 with values in $G$, classifying $G$-[[principal bundle]] $P$.

* The (1-categorical) [[pullback]]

  $$
    \array{
       P &\stackrel{\simeq}{\leftarrow}& \mathbf{P} &\to& \mathbf{E}G
       \\
       && \downarrow && \downarrow
       \\
       && C(U) &\stackrel{}{\to}& \mathbf{B}G
       \\
       && \downarrow^{\mathrlap{\simeq}}
       \\
       && X
    }
  $$

  is a Lie groupoid equivalent to this principal bundle $P$.

  (For more on the general phenomenon of which this is a special case see [[principal ∞-bundle]] and [[universal principal ∞-bundle]].)

* Similarly an anafunctor from $P_1(X)$ to $\mathbf{B}G$ is a [[connection on a bundle]] (see there for details).

## Related concepts

* [[smooth groupoid]]

* [[bisection of a Lie groupoid]]

* [[orbifold]]

* [[effective Lie groupoid]], [[proper Lie groupoid]], [[etale groupoid]]

* [[homotopy groups of a Lie groupoid]]

* [[Morita morphism]], [[Hilsum-Skandalis morphism]]

* [[Tannaka duality for Lie groupoids]]

* [[double Lie groupoid]]

* [[higher differential geometry]]

## References

Topological and differentiable (or smooth, "Lie") groupoids (and more generally categories) were introduced in

* [[Charles Ehresmann]], _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_ Colloque de G&#233;ometrie Differentielle Globale (Bruxelles, 1958), 137--150, Centre Belge Rech. Math., Louvain, 1959; 

Reviews and developments of the theory of Lie groupoids include

* Pradines, ....

* [[Kirill Mackenzie]], _General Theory of Lie Groupoids and Lie Algebroids,_ Cambridge University Press, 2005, xxxviii + 501 pages 
([website](http://kchmackenzie.staff.shef.ac.uk/gt.html))

* [[Kirill Mackenzie]], _Lie groupoids and Lie algebroids in differential geometry_, London Mathematical Society Lecture Note Series, 124. Cambridge University Press, Cambridge, 1987. xvi+327 pp ([MathSciNet](http://www.ams.org/mathscinet-getitem?mr=896907))

Discussion in the context of [[foliation theory]] ([[foliation groupoids]]) is in 

* [[Ieke Moerdijk]], Janez Mr&#269;un _Introduction to Foliations and Lie Groupoids_ , Cambridge Studies in Advanced Mathematics 91, Cambridge University Press, Cambridge, (2003)

The relation to [[differentiable stacks]] is discussed/reviewed in section 2 of

* [[Christian Blohmann]], _Stacky Lie groups_, Int. Mat. Res. Not. (2008) Vol. 2008: article ID rnn082 ([arXiv:math/0702399](http://arxiv.org/abs/math/0702399))
 {#Blohmann}


Lie groupoids as a source for [[groupoid convolution algebras|groupoid convolution]] [[C*-algebras]] are discussed in 

* [[Alain Connes]], _[[Noncommutative Geometry]]_

Expository discussion of various kinds of groupoids is also in 

* [[John Baez]]  _[TWF](http://math.ucr.edu/home/baez/TWF.html) [256](http://math.ucr.edu/home/baez/week256.html)_.


[[!redirects Lie groupoids]]