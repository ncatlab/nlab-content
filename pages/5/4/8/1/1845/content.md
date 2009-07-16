
# Idea #


In its original form, _K-theory_ is a [[generalized (Eilenberg-Steenrod) cohomology]] theory whose cocycles in degree 0 on a space $X$ can be represented by pairs of [[vector bundle]]s on $X$ modulo a certain equivalence relation.

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

## Motivational example: "nonabelian K-cohomology" ##

To see how this works, first consider the task of generalizing the "[[nonabelian cohomology]]" or [[cohomotopy]] theory given by the coefficient object $\mathbb{N}$, the additive semi-group of  $\mathbb{N}$ of [[natural number]]s.

This does have arbitrarily high [[delooping]]s in the context of [[omega-category|omega-categories]], but not in the context of [[infinity-groupoid]]s. So for the purposes of [[cohomology]] $\marthbb{N}$ is just the [[monoid]]al [[0-groupoid]] $\mathbb{N}$ which as a coefficient object induces a very boring [[cohomology]] theory: the $\mathbb{N}$-cohomology of anything is just the monoidal set $\mathbb{N}$ itself.

So $\mathbb{N}$ itself is rather boring as a coefficient object. But while we cannot [[delooping|deloop]] it, we can [[vertical categorification|categoriy]] it and do obtain an interesting [[nonabelian cohomology]] theory:
 
Namely the [[category]] $Core(Vect)$ of finite dimensional vector spaces with invertible linear maps between them would serve as a [[vertical categorification|categorification]] of $\mathbb{N}$: isomorphism classes of finite dimensional vector spaces $V$ are given by their dimension $d(V) \in \mathbb{N}$, and [[direct sum]] of vector spaces corresponds to addition of these numbers.

If we want to use the category $Core(Vect)$ as the coefficient for a [[cohomology]] theory, we should for greater applicability equip it with its natural topological or smooth structure,  so that it makes sense to ask what the $Vect$-cohomology of a [[topological space]] or a [[smooth space]] would be. The canonical way to do this is to regard $Vect$ as a [[generalized smooth space]] called a [[smooth infinity-stack]] and vonsider it as the assignment

$$
  \mathbf{Vect} : Diff \to \infty Grpd
$$

$$
  U \mapsto Core(VectBund(U))
$$

that sends each smooth test space $U$ (a smooth manifold, say), to [[gropupoid]] of smooth [[vector bundle]]s over $U$ with [[bundle]] [[isomorphism]]s betweem them. We regard here a vector bundle $V \to U$ as a smooth $U$-parameterized family of vector spaces (the [[fiber]]s over each point) and thus as a smooth _probe_ or _plot_  of the category $Core(Vect)$.

The [[nonabelian cohomology]] theory with coefficients in $\mathbf{Vect}$ has no [[cohomology group]]s, but at least cohomology [[monoid]]s

$$
  H(X,\mathbf{Vect}) := \pi_0 \mathbf{H}_{diff}(X, \mathbf{Vect})
  \,.
$$

It is equivalent to the [[nonabelian cohomology]] with coefficients the [[delooping]] $\mathbf{B} U$ of the stable unitary group $U := colim_n U(n)$.


## K-theory as an groupoidification of $\mathbf{Vect}$ ##

The integers $\mathbb{Z}$ are obtained from the natural numbers $\mathbb{N}$ by including "formal inverses" to all elements under the additive operation. Another way to think of this is that the [[delooping|delooped]] [[groupoid]] $\mathbf{B} \mathbb{Z}$ is obtained from $\mathbf{B} \mathbb{N}$ be groupoidification (under the [[nerve]] operation this is fibrant replacement in the [[model structure on simplicial sets]]).

The idea of K-cohomology is essentially to apply this groupoidification process to not just to $\mathbb{N}$, but to its [[vertical categorification|categorification]] $\mathbf{Vect}$.

Just as a, integer $k = n-m \in \mathbb{Z}$  may be regarded as an equivalence class of natural numbers $(n,m) \in \mathbb{N} \times \mathbb{N}$  under the relation

$$
  [(n,m)] = [(n+r, m+r)] \;\; \forall r \in \mathbb{N}
$$

one can similarly look at equivalence classes of pairs $(V,W) \in \mathbf{Vect}(U) \times \mathbb{Vect}(U)$ of [[vector bundle]]s.

This perspective on K-theory was originally realized by Atiyah and Hirzebruch. The resulting cohomology theory is usually called [[topological K-theory]].

There are several variations on this theme. In particular it turns out to be useful to regard a pair of [[vector bundle]]s as a single $\mathbb{Z}_2$-[[graded vector space|graded vector bundle]].

One version of $\mathbb{Z}_2$-graded vector bundles, which lends itself to the description of [[twisted cohomology|twisted]] $K$-theory are [[vectorial bundle]]s.


# Related entries #
 

* [[K-theory spectrum]]

* [[topological K-theory]]

* [[algebraic K-theory]]

* [[Karoubi K-theory]]

...