
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[stack]] $X$ on a [[site]] $C$ is **geometric** if, roughly, it is "represented" by a suitably well-behaved [[groupoid]] $\mathcal{G} = (\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0)$ [[internal category|internal]] to $C$, i.e. if to an object $U \in C$ the stack assigns assigns the (ordinary) [[groupoid]]

$$
  X : U \mapsto (C(U,\mathcal{G}_1) \stackrel{\to}{\to} C(U,\mathcal{G}_0))
  \,.
$$

Notice that a crucial difference between the groupoid object $\mathcal{G}$ in $C$ and the geometric stack $X$ is that the equivalence class of the stack in general contains _more_ (geometric) stacks than there are groupoid objects internally equivalent to $\mathcal{G}$: two groupoid objects with equivalent geometric stacks are called **Morita equivalent** groupoid objects. 

With $C$ fixed, instead of "geometric stack" one says, for instance

* for $C = $ [[Top]] -- topological stack;

* for $C = $ [[Diff]] -- [[differentiable stack]];

* for $C = $ [[CRing]]${}^{op}$ -- [[algebraic stack]];


## Definition

There are slight variations in the literature on what particular is required of a [[stack]] $X$ on a [[site]] $C$  with [[subcanonical coverage|subcabonical topology]] in order that it qualifies as **geometric**. 

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

  * $\Delta_X$ is required to be quasicompact and separated

  * for [[Deligne-Mumford stack]]s $p$ is moreover required to be etale

  * for [[Artin stack]]s $p$ is required to be [[smooth morphism of schemes|smooth]].

## Relation to groupoid objects

The _groupoid object_ associated to a geometric stack $X$ with atlas $p : U \to X$ is simply the 2-categorical Cech-nerve of $p$: set $\mathcal{G}_0 := U$ and $\mathcal{G}_1 = U \times_X U$, where the latter is the 2-categorical [[pullback]]

$$
  \array{
   \mathcal{G}_1 &\stackrel{s}{\to}& U
   \\
   \downarrow^{\mathrlap{t}} &{}^{\simeq}\swArrow& \downarrow^{\mathrlap{p}}
   \\
   U &\to& X
  }
$$

## References

A good discussion of topological and differentiable stacks is around definition 2.3 in

* [[Jochen Heinloth]], _Some notes on differentiable stacks_ ([pdf](http://www.uni-due.de/~hm0002/stacks.pdf))


Specifically for the relation to groupoid objects see

3.1 and 3.3 in 

* Metzler, _Topological and smooth stacks_ ([arXiv:math/0306176](http://arxiv.org/abs/math/0306176))

paragraohs 2.4.3, 3.4.3, 3.8, 4.3 in 

* G. Laumon, L. Moret-Bailly, _Champs alg&#233;briques_ , Ergebn. der Mathematik und ihrer Grenzgebiete 39 , Springer-Verlag, Berlin, 2000

paragraph 4.4 in 

* [[Eugene Lerman]], _Orbifolds as stacks?_ ([arXiv:0806.4160](http://arxiv.org/abs/0806.4160))
 
See also

* [[Bertrand Toen]], _Master Course on Stacks_ ([web](http://www.math.univ-toulouse.fr/~toen/m2.html))


Geometric stacks over the site of schemes modeled on [[smooth loci]] is in section 8 of

* [[Dominic Joyce]], _Algebraic geometry over $C^\infty$-rings_ ([arXiv:1001.0023](http://arxiv.org/abs/1001.0023))

## Geometric $\infty$-stacks


Geometric $\infty$-stacks were introduced in 

* [[Bertrand Toen]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219])

in terms of [[model category]] presentations.

More discussion on that is in

* [[Bertrand Toen]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications_ ([arXiv](http://arxiv.org/abs/math/0404373))