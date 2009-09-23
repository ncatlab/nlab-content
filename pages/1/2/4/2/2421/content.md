
<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>


#Contents#

* automatic toc goes here
{:toc}


#Super Lie groups#

##Definition##
A _super Lie group_ is a [[group object]] in the [[category]] of [[supermanifold]]s, that is a super [[Lie group]].

...

##Examples##


### the super-translationn group ###

also called the **super-Heisenberg group**

The additive group structure on $\mathbb{R}^{1|1}$ is given on [[generalized element]]s in (i.e. in the logic internal to) the [[topos]] of [[sheaf|sheaves]] on the category [[SCartSp]] of [[cartesian space|cartesian]] superspaces by

$$
  \mathbb{R}^{1|1} \times \mathbb{R}^{1|1} \to 
  \mathbb{R}^{1|1}
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

Recall how the notation works here: by the [[Yoneda embedding]] we have a [[full and faithful functor]]

> [[SDiff]] $\hookrightarrow$ $Fun(SDiff^{op}, Set)$

and we also have the theorem, discussed at [[supermanifold]]s, that maps from some $S \in SDiff$ into $\mathbb{R}^{p|q}$ is given by a tuple of $p$ even section $t_i$ and $q$ odd sections $\theta_j$. The above notation specifies the map of supermanifolds by displaying what map of sets of maps from some test object $S$ it corresponds to under the [[Yoneda embedding]].

Now,  or each $S \in $ [[SDiff]] there is a [[group]] structure on the [[hom-set]] $SDiff(S, \mathbb{R}^{1|1}) \simeq C^\infty(S)^{ev} \times C^\infty(X)^{odd}$ given by precisely the above formula for this given $S$

$$
  \mathbb{R}^{1|1}(S) \times \mathbb{R}^{1|1}(S) \to 
  \mathbb{R}^{1|1}(S)
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

where $(t_i, \theta_i) \in C^\infty(S)^{ev} \times C^\infty(S)^{odd}$ etc and where the addition and product on the right takes place in the function [[super algebra]] $C^\infty(S)$.

Since the formula looks the same for all $S$, one often just writes it without mentioning $S$ as above.


[[!redirects super Lie group]]