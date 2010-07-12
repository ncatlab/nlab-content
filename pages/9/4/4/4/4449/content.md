
> under construction -- am being interrupted...

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _classifying topos of a localic groupoid_ $\mathcal{G}$ is a an incarnation of a [[localic groupoid]] in the world of [[topos]]es. At least in good cases, [[geometric morphism]]s into it classify $\mathcal{G}$-[[principal bundle]]s.

Recall that a [[localic groupoid]] is a [[groupoid]] $\mathcal{G} = (\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0)$ [[internalization|internal to]] [[locale]]s/Grothendieck-[[(0,1)-topos]]es.

Let $N_\bullet \mathcal{G} : \Delta^{op} \to Locales$ be the [[simplicial object]] in locales given by the [[nerve]] of $\mathcal{G}$. By applying the [[sheaf topos]] functor  $Sh : Locale \to Topos$ to this, we obtain  a [[simplicial object|simplicial]] [[topos]] $Sh(N \mathcal{G}) : [n] \mapsto Sh(N_n \mathcal{G})$. Let $tr_2 Sh(N \mathcal{G})$ be its [[simplicial skeleton|2-truncation]], then the [[2-limit|2-colimit]]

$$
  Sh(\mathcal{G})
  :=
  \lim_{\to_{[n]}} tr_2 Sh(N_\bullet \mathcal{G})
$$

in the [[2-category of toposes]] is called the [[classifying topos]] of $\mathcal{G}$.

This has an explicit description along the lines discussed at [[sheaves on a simplicial topological space]].

**Proposition** (Joyal-Tierney)

For every [[Grothendieck topos]] $E$ there is a [[localic groupoid]] $\mathcal{G}$ such that $E \simeq Sh(\mathcal{G})$.


## References

The original result appears in 

* [[Andre Joyal]], M. Tierney, _An extension of the Galois theory of Grothendieck_ Mem. Amer. Math. Soc. no 309 (1984)

An extension of the equivalence to morphisms is discussed in

* [[Ieke Moerdijk]], _The classifying topos of a continuous groupoid I_ , Trans. Amer. Math. Soc. Volume 310, Number 2, (1988)




