+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _classifying topos of a localic groupoid_ $\mathcal{G}$ is a an incarnation of a [[localic groupoid]] (possibly a [[topological groups]]) in the category of [[toposes]]. At least in good cases, [[geometric morphisms]] into it classify $\mathcal{G}$-[[groupoid principal bundles]], whence the name.

## Definition

A [[localic groupoid]] is a [[groupoid object]] $\mathcal{G} = (\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0)$ [[internalization|internal to]] [[locales]]/Grothendieck-[[(0,1)-toposes]]. If both $\mathcal{G}_0$ and $\mathcal{G}_1$ happen to be [[spatial locales]], hence [[topological spaces]], then this is a _[[topological groupoid]]_.

Let $N_\bullet \mathcal{G} : \Delta^{op} \to Locales$ be the [[simplicial object]] in locales given by the [[nerve]] of $\mathcal{G}$. By applying the [[sheaf topos]] functor  $Sh : Locale \to Topos$ to this, we obtain  a [[simplicial object|simplicial]] [[topos]] $Sh(N \mathcal{G}) : [n] \mapsto Sh(N_n \mathcal{G})$. Let $tr_2 Sh(N \mathcal{G})$ be its [[simplicial skeleton|2-truncation]], then the [[2-limit|2-colimit]]

$$
  Sh(\mathcal{G})
   \coloneqq
  \underset{\longrightarrow}{\lim}_n tr_2 Sh(N_\bullet \mathcal{G})
$$

in the 2-category [[Topos]] is called the [[classifying topos]] of $\mathcal{G}$.

This has a more explicit description along the lines discussed at [[sheaves on a simplicial topological space]]:

For $E \in Sh(\mathcal{G}_0)$ a [[sheaf]] on the [[topological space]] of its [[objects]], say that a _$\mathcal{G}_1$-action_ on $E$ is a continuous [[groupoid action]] of $\mathcal{G}_\bullet$ on the [[etale space]] $Sp(E) \to \mathcal{G}_0$ over $\mathcal{G}_0$ that corresponds to the sheaf $E$, hence for each morphisms $f \colon x \to y$ in $\mathcal{G}$ a continuous function $\rho(f) \colon Sp(E)_x \to Sp(E)_y$ that satisfies the usual [[action]] property. These sheaves with $\mathcal{G}_1$-action and with the evident [[homomorphisms]] between them form a [[category]], and this is $Sh(\mathcal{G})$.


## Properties

### Exhaustion of the category of all toposes

**Proposition** ([Joyal-Tierney 84](#JoyalTierney84))

For every [[Grothendieck topos]] $\mathcal{E}$ there is a [[localic groupoid]] $\mathcal{G}$ such that $\mathcal{E} \simeq Sh(\mathcal{G})$.

**Proposition** ([Moerdijk 88, theorem 5](#Moerdijk88))

This construction extends to an [[equivalence of 2-categories]] between that of Grothendieck toposes [[Topos]] and a [[localization]] of that of localic groupoids.

**Proposition** ([Butz-Moerdijk 98](#ButzMoerdijk98)) If $\mathcal{E}$ has [[point of a topos|enough points]], then there exists in fact a [[topological groupoid]] $\mathcal{G}$ such that $\mathcal{E} \simeq Sh(\mathcal{G})$.



## References

The original result for localic groupoids and arbitrary Grothendieck toposes is due to 

* {#JoyalTierney84} [[Andre Joyal]], [[Myles Tierney]], _An extension of the Galois theory of Grothendieck_ Mem. Amer. Math. Soc. no 309 (1984)

The above equivalence of categories can in fact be lifted
to an equivalence between the bicategory of localic groupoids, complete flat bispaces, and their morphisms and the bicategory of Grothendieck toposes, geometric morphisms, and natural transformations. The equivalence is implemented by the classifying topos functor, as explained in

* {#Moerdijk88} [[Ieke Moerdijk]], _The classifying topos of a continuous groupoid I_ , Trans. Amer. Math. Soc. Volume 310, Number 2, (1988) ([pdf](http://www.ams.org/journals/tran/1988-310-02/S0002-9947-1988-0973173-9/S0002-9947-1988-0973173-9.pdf))

* [[Ieke Moerdijk]], _The classifying topos of a continuous groupoid II_, 
Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle cat&#233;goriques 31, no. 2 (1990), 137&#8211;168.

The restriction to topological groupoids and Grothendieck toposes with enough points is due to

* {#ButzMoerdijk98} [[Carsten Butz]], [[Ieke Moerdijk]], _Representing topoi by topological groupoids_, Journal of pure and applied algebra 130 (1998) 223-235 ([pdf](http://ns.synrc.com/publications/cat/Topology/Representing%20Topoi%20by%20Topological%20Groupoids.pdf))



[[!redirects classifying topos of a topological groupoid]]
