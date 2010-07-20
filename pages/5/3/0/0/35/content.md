<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>

#Contents#
* autmatic table of contents goes here
{:toc}

## Definition

A Lie groupoid is an [[internal category|internal groupoid]] in [[Diff]]. One can define a Lie groupoid to be an [[Ehresmann internal category|internal groupoid in the sense of Ehresmann]], which includes as data the manifold of composable pairs, or take the conventional route and specify that the source and target maps are submersions. This ensures the pullback exists to define said manifold or composable pairs.

Note that originally Lie groupoids were called _differentiable groupoids_ (and also one considered differentiable _categories_). Sometime in the 1980s there was a change of terminology. (reference?)

## Specialisations

One definition which Ehresmann introduced in his paper _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_ (see below) is that of [[locally trivial category|locally trivial groupoid]]. It is defined more generally for topological categories, and extends in an obvious way to topological groupoids, and Lie categories and groupoids. For a topological (resp. Lie) category $X$, let $X_1^{iso}$ denote the subspace (resp. submanifold) of invertible arrows . (This always exists, by general abstract nonsense - I should look up the reference, it's in Bunge-Pare I think - [[David Roberts|DR]])

+-- {: .un_defn}
###### Definition 
A topological groupoid $X_1 \rightrightarrows X_0$ is **locally trivial** if for every point $p\in X_0$ there is a neighbourhood $U$ of $p$ and a lift of the inclusion $\{p\} \times U \hookrightarrow X_0 \times X_0$ through $(s,t):X_1^{iso}\to X_0 \times X_0$. 
=--

Clearly for a Lie groupoid $X_1^{iso} = X_1$. It is simple to show from the definition that for a transitive Lie groupoid, $(s,t)$ has local sections. Ehresmann goes on to show a link between smooth [[principal bundles]] and transitive, locally trivial Lie groupoids. See [[locally trivial category]] for details.

## Literature

Topological and differentiable (or smooth, "Lie") groupoids (and more generally categories) were introduced in

* C. Ehresmann, _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_ Colloque de G&eacute;ometrie Differentielle Globale (Bruxelles, 1958), 137--150, Centre Belge Rech. Math., Louvain, 1959; 

Reviews and developments of the theory of Lie groupoids include

* Pradines, ....

* K. C. H. Mackenzie, _General Theory of Lie Groupoids and Lie Algebroids,_ Cambridge University Press, 2005, xxxviii + 501 pages 
([website](http://kchmackenzie.staff.shef.ac.uk/gt.html))

* K. C. H. Mackenzie, _Lie groupoids and Lie algebroids in differential geometry_, London Mathematical Society Lecture Note Series, 124. Cambridge University Press, Cambridge, 1987. xvi+327 pp ([MathSciNet](http://www.ams.org/mathscinet-getitem?mr=896907))

##Further discussion

John Baez talks about various kinds of Lie groupoids in [TWF](http://math.ucr.edu/home/baez/TWF.html) [256](http://math.ucr.edu/home/baez/week256.html).


[[!redirects Lie groupoids]]