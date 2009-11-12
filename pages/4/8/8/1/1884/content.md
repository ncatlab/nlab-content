#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##


What is called _topological_ [[K-theory]] is a collection of  [[generalized (Eilenberg-Steenrod) cohomology]] theories whose cocycles in degree 0 on a space $X$ can be represented by pairs of [[vector bundle]]s, real or complex ones, on $X$ modulo a certain equivalence relation.

Notice that "ordinary cohomology" is the [[generalized (Eilenberg-Steenrod) cohomology]] that is represented by the [[Eilenberg-MacLane spectrum]] which, as a stably abelian [[infinity-groupoid]] is just the additive [[group]] 

$$
  \mathbb{Z}
$$ 

of integers.

To a large extent K-theory is the [[cohomology]] theory obtained by [[vertical categorification|categorifying]] this   once:

$$
  \mathbb{Z} \;\; \mapsto something like \mathbf{Vect}
  \,.
$$

### Motivational example: "nonabelian K-cohomology" ###

To see how this works, first consider the task of generalizing the "[[nonabelian cohomology]]" or [[cohomotopy]] theory given by the coefficient object $\mathbb{N}$, the additive semi-group of  $\mathbb{N}$ of [[natural number]]s.

This does have arbitrarily high [[delooping]]s in the context of [[omega-category|omega-categories]], but not in the context of [[infinity-groupoid]]s. So for the purposes of [[cohomology]] $\mathbb{N}$ is just the [[monoid]]al [[0-groupoid]] $\mathbb{N}$ which as a coefficient object induces a very boring [[cohomology]] theory: the $\mathbb{N}$-cohomology of anything is just the monoidal set $\mathbb{N}$ itself. While we cannot [[delooping|deloop]] it, we can [[vertical categorification|categorify]] it and do obtain an interesting [[nonabelian cohomology]] theory:
 
Namely the [[category]] $Core(Vect)$ of finite dimensional vector spaces with invertible linear maps between them would serve as a [[vertical categorification|categorification]] of $\mathbb{N}$: isomorphism classes of finite dimensional vector spaces $V$ are given by their dimension $d(V) \in \mathbb{N}$, and [[direct sum]] of vector spaces corresponds to addition of these numbers.

If we want to use the category $Core(Vect)$ as the coefficient for a [[cohomology]] theory, we should for greater applicability equip it with its natural topological or smooth structure,  so that it makes sense to ask what the $Vect$-cohomology of a [[topological space]] or a [[smooth space]] would be. The canonical way to do this is to regard $Vect$ as a [[generalized smooth space]] called a [[smooth infinity-stack]] and consider it as the assignment

$$
  \mathbf{Vect} : Diff \to \infty Grpd
$$

$$
  U \mapsto Core(VectBund(U))
$$

that sends each smooth test space $U$ (a smooth manifold, say), to [[groupoid]] of smooth [[vector bundle]]s over $U$ with [[bundle]] [[isomorphism]]s betweem them. We regard here a vector bundle $V \to U$ as a smooth $U$-parametrized family of vector spaces (the [[fiber]]s over each point) and thus as a smooth _probe_ or _plot_  of the category $Core(Vect)$.

The [[nonabelian cohomology]] theory with coefficients in $\mathbf{Vect}$ has no [[cohomology group]]s, but at least cohomology [[monoid]]s

$$
  H(X,\mathbf{Vect}) := \pi_0 \mathbf{H}_{diff}(X, \mathbf{Vect})
  \,.
$$

It is equivalent to the [[nonabelian cohomology]] with coefficients the [[delooping]] $\mathbf{B} U$ of the stable unitary group $U := colim_n U(n)$.


### K-theory as a groupoidification of $\mathbf{Vect}$ ###

The integers $\mathbb{Z}$ are obtained from the natural numbers $\mathbb{N}$ by including "formal inverses" to all elements under the additive operation. Another way to think of this is that the [[delooping|delooped]] [[groupoid]] $\mathbf{B} \mathbb{Z}$ is obtained from $\mathbf{B} \mathbb{N}$ by groupoidification (under the [[nerve]] operation this is fibrant replacement in the [[model structure on simplicial sets]]).

The idea of K-cohomology is essentially to apply this groupoidification process to not just to $\mathbb{N}$, but to its [[vertical categorification|categorification]] $\mathbf{Vect}$.

Just as an integer $k = n-m \in \mathbb{Z}$  may be regarded as an equivalence class of natural numbers $(n,m) \in \mathbb{N} \times \mathbb{N}$  under the relation

$$
  [(n,m)] = [(n+r, m+r)] \;\; \forall r \in \mathbb{N}
$$

one can similarly look at equivalence classes of pairs $(V,W) \in \mathbf{Vect}(U) \times \mathbf{Vect}(U)$ of [[vector bundle]]s.

This perspective on K-theory was originally realized by Atiyah and Hirzebruch. The resulting cohomology theory is usually called [[topological K-theory]].

As one of several variations, it is useful to regard a pair of [[vector bundle]]s as a single $\mathbb{Z}_2$-[[graded vector space|graded vector bundle]].

One version of $\mathbb{Z}_2$-graded vector bundles, which lead to a description of [[twisted cohomology|twisted]] $K$-theory are [[vectorial bundle]]s.


## Spectrum ##

Being a [[generalized (Eilenberg-Steenrod) cohomology]] theory, toplogical K-theory is represented by a [[spectrum]]: the [[K-theory spectrum]].


## References ##

An introductory reference is

* Allen Hatcher, _Vector bundles and K-theory_ ([web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

More advanced material is in ...



## Discussion ##

The above idea section was originally at [[K-theory]] where it triggered the following discussion

+--{ .query}
_Zoran_ What do you mean by originally ?? K-theory was invented by Grothendieck in algebraic geometry and over there it does NOT correspond to an Eilenberg-Steenrod setup. It seems this entry belongs much more to title "topological K-theory" (as opposed to algebraic). Second even for topological case there are real and complex K-theory etc. so not "a cohomology". One of the nlab entries should also put emphasis on the K-theory of OPERATOR algebras (and also to the subject of K-homology, which is not known in geometric terms but in terms of operators), what corresponds to a rather central part of K-theory today, including most of the work in nc geometry. 

[[Urs Schreiber]]: right, I have briefly modified the sentence now and then moved the entire paragraph here to "topological K-theory". Eventually we need a more exhaustive and more comprehensive discussion here and need something general at [[K-theory]].

I made a blog comment about that [here](http://golem.ph.utexas.edu/category/2009/07/being_tentative_on_nlab.html#c025451).

=--

