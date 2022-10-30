+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[stack]] $X$ on a [[site]] $C$ is **geometric** if, roughly, it is [[representable functor|represented]] by a suitably well-behaved [[groupoid]] object $\mathcal{G} = (\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0)$ [[internal category|internal]] to $C$, i.e. if to an object $U \in C$ the stack assigns the (ordinary) [[groupoid]]

$$
  X : U \mapsto (C(U,\mathcal{G}_1) \stackrel{\to}{\to} C(U,\mathcal{G}_0))
  \,.
$$

A crucial difference between the groupoid object $\mathcal{G}$ in $C$ and the geometric stack $X$ is that the [[equivalence class]] of the stack in general contains _more_ (geometric) stacks than there are groupoid objects internally equivalent to $\mathcal{G}$: two groupoid objects with equivalent geometric stacks are called **Morita equivalent** groupoid objects. 

## Special cases

Geometric stacks for the following choices of sites $C$ are called

* for $C = $ [[Top]] -- [[topological stack]];

* for $C = $ [[Diff]] -- [[differentiable stack]];

* for $C = $ [[CRing]]${}^{op}$ -- [[algebraic stack]];

* for $C = $ [[complex manifold|CplxMfd]] -- [[complex analytic stack]];


## Definition

There are slight variations in the literature on what precisely is required of a [[stack]] $X$ on a [[site]] $C$  with [[subcanonical coverage|subcanonical topology]] in order that it qualifies as **geometric**. 

A general requirement is that

1. the diagonal morphism $\Delta : X \to X \times X$ is a [[representable morphism of stacks]]

1. there exists an _atlas_ for the stack, in that there is a [[representable functor|representable]] $U \in C$ and a surjective morphism

  $$ 
    p : U \to X
    \,.
  $$

  This is necessarily itself representable, precisely if $\Delta_X$ is.

Further conditions are the following

* for $C = Sch_{et}$ the [[site]] of [[scheme]]s with the [[etale topology]]

  * $\Delta_X$ is required to be [[quasicompact]] and [[separated]]

  * for [[Deligne-Mumford stack]]s $p$ is moreover required to be etale

  * for [[Artin stack]]s $p$ is required to be [[smooth morphism of schemes|smooth]].

## Relation to groupoid objects

The _groupoid object_ associated to a geometric stack $X$ with atlas $p : U \to X$ is the [[Cech groupoid of a functor|Cech groupoid]] of $p$ (this is simply the Cech groupoid of $p$ seen as a singleton cover) defined by $\mathcal{G}_0 := U$ and $\mathcal{G}_1 = U \times_X U$, where the latter is the 2-categorical [[pullback]]

$$
  \array{
   \mathcal{G}_1 &\stackrel{s}{\to}& U
   \\
   \downarrow^{\mathrlap{t}} &{}^{\simeq}\swArrow& \downarrow^{\mathrlap{p}}
   \\
   U &\to& X
  }
$$

## Related concepts

* **geometric stack**

* [[geometric ∞-stack]]


## References

A good discussion of topological and differentiable stacks is around definition 2.3 in

* [[Jochen Heinloth]], _Some notes on differentiable stacks_ ([pdf](http://www.uni-due.de/~hm0002/stacks.pdf))

Differentiable stacks are discussed in

* [[Kai Behrend]], [[Ping Xu]], _Differentiable Stacks and Gerbes_ ([arXiv](http://front.math.ucdavis.edu/0605.5694)).

Specifically for the relation to groupoid objects see

3.1 and 3.3 in 

* Metzler, _Topological and smooth stacks_ ([arXiv:math/0306176](http://arxiv.org/abs/math/0306176))

paragraphs 2.4.3, 3.4.3, 3.8, 4.3 in 

* G. Laumon, L. Moret-Bailly, _Champs alg&#233;briques_ , Ergebn. der Mathematik und ihrer Grenzgebiete 39 , Springer-Verlag, Berlin, 2000

paragraph 4.4 in 

* [[Eugene Lerman]], _Orbifolds as stacks?_ ([arXiv:0806.4160](http://arxiv.org/abs/0806.4160))
 
See also

* [[Bertrand Toen]], _Master Course on Stacks_ ([web](http://ens.math.univ-montp2.fr/~toen/m2.html))

* [[Aise Johan de Jong]],  _[[The Stacks Project]]_ ([pdf](http://www.math.columbia.edu/algebraic_geometry/stacks-git/book.pdf)) ([project website](http://www.math.columbia.edu/algebraic_geometry/stacks-git/))
{#deJong}


Geometric stacks over the site of schemes modeled on [[smooth loci]] is in section 8 of

* [[Dominic Joyce]], _Algebraic geometry over $C^\infty$-rings_ ([arXiv:1001.0023](http://arxiv.org/abs/1001.0023))

 

[[!redirects geometric stack]]
[[!redirects geometric stacks]]
[[!redirects presentable stack]]
[[!redirects presentable stacks]]