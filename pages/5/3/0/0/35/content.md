<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>

#Contents#
* autmatic table of contents goes here
{:toc}

## Idea

A _Lie groupoid_ is a [[groupoid]] with smooth structure The notion of Lie groupoid is the groupoid analog of [[Lie group]].

## Definition

A Lie groupoid is an [[internal category|internal groupoid]] in [[Diff]]. One can define a Lie groupoid to be an [[Ehresmann internal category|internal groupoid in the sense of Ehresmann]], which includes as data the manifold of [[composable pairs]], or take the conventional route and specify that the source and target maps are [[submersion]]s. This ensures the [[pullback]] exists to define said manifold or composable pairs.

Note that originally Lie groupoids were called _differentiable groupoids_ (and also one considered differentiable _categories_). Sometime in the 1980s there was a change of terminology. (reference?)

### Specialisations

One definition which Ehresmann introduced in his paper _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_ (see below) is that of [[locally trivial category|locally trivial groupoid]]. It is defined more generally for topological categories, and extends in an obvious way to topological groupoids, and Lie categories and groupoids. For a topological (resp. Lie) category $X$, let $X_1^{iso}$ denote the subspace (resp. submanifold) of invertible arrows . (This always exists, by general abstract nonsense - I should look up the reference, it's in Bunge-Pare I think - [[David Roberts|DR]])

+-- {: .un_defn}
###### Definition 
A topological groupoid $X_1 \rightrightarrows X_0$ is **locally trivial** if for every point $p\in X_0$ there is a neighbourhood $U$ of $p$ and a lift of the inclusion $\{p\} \times U \hookrightarrow X_0 \times X_0$ through $(s,t):X_1^{iso}\to X_0 \times X_0$. 
=--

Clearly for a Lie groupoid $X_1^{iso} = X_1$. It is simple to show from the definition that for a transitive Lie groupoid, $(s,t)$ has local sections. Ehresmann goes on to show a link between smooth [[principal bundles]] and transitive, locally trivial Lie groupoids. See [[locally trivial category]] for details.

### The (2,1)-category of Lie groupoids {#2CatOfGrpds}


As usual for internal categories, the naive 2-category of internal groupoids, internal [[functor]]s and internal [[natural transformation]]s is not quite "correct". One sign of this is that the [[axiom of choice]] fails in [[Diff]] so that an internal functor which is an [[essentially surjective functor]] and a [[full and faithful functor]] may still not have an internal weak inverse.

One way to deal with this is to equip the 2-category with some structure of a [[homotopical category]] and allow morphisms of Lie groupoids to be [[anafunctor|2-anafunctor]]s, i.e. [[span]]s of internal functors $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$.

Such generalized morphisms -- called _Morita morphisms_ or _generalized morphisms_ in the literature -- are sometimes modeled as [[bibundle]]s and then called [[Hilsum-Skandalis morphism]]s.

Another equivalent approach is to embed Lie groupoids into the context of [[2-topos]] theory:

The [[2-topos|(2,1)-topos]] $Sh_{(2,1)}(Diff)$ of [[stack]]s/[[2-sheaves]] on [[Diff]] may be understood as a nice [[2-category]] of general groupoids _modeled on_ [[smooth manifold]]s. The degreewise [[Yoneda embedding]] allows to emebed groupoids internal to $Diff$ into stacks on $Diff$.

Regarded inside this wider context, Lie groupoids are identified with [[differentiable stack]]s. The [[(n,r)-category|(2,1)-category]] of Lie groupoids is then the full sub-$(2,1)$-category of $Sh_{(2,1)}(Diff)$ on differentiable stacks.

For more comments on this, see also the beginning of [[∞-Lie groupoid]].

## Lie algebroids

As the [[infinitesimal space|infinitesimally]] approximation to a [[Lie group]] is a [[Lie algebra]], so the infinitesimal approximation to a Lie groupoid is a [[Lie algebroid]].

## Higher Lie groupoids

See

* [[internal ∞-groupoid]]

* [[∞-Lie groupoid]]

## References

Topological and differentiable (or smooth, "Lie") groupoids (and more generally categories) were introduced in

* [[Charles Ehresmann]], _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_ Colloque de G&eacute;ometrie Differentielle Globale (Bruxelles, 1958), 137--150, Centre Belge Rech. Math., Louvain, 1959; 

Reviews and developments of the theory of Lie groupoids include

* Pradines, ....

* K. C. H. Mackenzie, _General Theory of Lie Groupoids and Lie Algebroids,_ Cambridge University Press, 2005, xxxviii + 501 pages 
([website](http://kchmackenzie.staff.shef.ac.uk/gt.html))

* K. C. H. Mackenzie, _Lie groupoids and Lie algebroids in differential geometry_, London Mathematical Society Lecture Note Series, 124. Cambridge University Press, Cambridge, 1987. xvi+327 pp ([MathSciNet](http://www.ams.org/mathscinet-getitem?mr=896907))

* John Baez talks about various kinds of Lie groupoids in [TWF](http://math.ucr.edu/home/baez/TWF.html) [256](http://math.ucr.edu/home/baez/week256.html).


[[!redirects Lie groupoids]]