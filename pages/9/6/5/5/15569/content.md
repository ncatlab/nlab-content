
> under construction

#Contents#
* table of contents
{:toc}

## Introduction

A fruitful approach to mathematical theory is what might be called "inter-geometric", meaning that definitions and theorems make sense and hold when interpreted in different flavors of geometry. Examples are the [[GAGA principle]], the [[function field analogy]], the [[geometric Langlands correspondence|geometric]] [[Langlands correspondence]] and absolute [[F1]]-geometry. While in these examples the [[analogy]]  between different theories of geometry has been established case-by-case, there is by and large no meta-theory which would systematically imply the analogy. 

This is of practical concern for instance in the [[Langlands program]], where it is an open problem how the methods and insights which are deeply on the side of [[complex analytic geometry]], such as involving [[mirror symmetry]], might have incarnations on the [[arithmetic geometry]]-side. And vice-versa, the complex-analytic version of the conjecture was obtained by educated guessing via analogy from the arithmetic side in the first place, but this guesswork has been questioned ([[Problems in the theory of automorphic forms -- 45 years later|Langlands 14]]). Both of these issue would be resolved if one had an "inter-geometric" from which the correspondence both in [[arithmetic geometry]] and in [[complex-analytic geometry]] would both follow by restriction.

Another example, which maybe hasn't been duly recognized as such yet, is the construction of the refined [[Witten genus]] in the guise of the [[string orientation of tmf]]: here what is initially a concept in [[complex analytic geometry|complex analytic]] ([[supergeometry|super]]-)geometry is constructed by passage (via the construction of [[tmf]]) to the [[moduli stack of elliptic curves]] all the way down in [[arithmetic geometry]], and in fact then via the [[fracture theorems]] by its [[base change|base changes]] to [[p-adic geometry]] and to [[rational homotopy theory]] (and further to [[K(n)-local stable homotopy theory]]). There is thus a kind of [[p-adic string theory]] appearing here, which is however not of the kind that existing literature with such title would shed any light on. The construction is a ground-breaking accomplishment in [[algebraic topology]], but at least in view of the origin of the [[Witten genus]] in [[string theory]] it maybe raises more questions than it solves: from the perspective of physics the Witten genis is but the first example of a tower of similar phenomena, the next instance being the [[partition function]] of the [[M5-brane]] and then that of 10d [[string theory]] itself (see e.g. at _[[self-dual higher gauge theory]]_).  Finding the higher analog of the [[string orientation of tmf]] for these cases is as desirable as it would seem to be intractable without some more inter-geometric theory to guide one.

Here we will not present solutions to these rather deep questions. But we do want to discuss something that looks like steps in the right direction.

Notice that the idea of "inter-geometric theory" is ancient, it originates with the [[synthetic geometry]] of Euclid which, with the parallel axiom removed, subsumes Euclidean, spherical and hyperbolic geometry. The idea of refining such a [[synthetic mathematics|synthetic reasoning]] to [[differential geometry]] is not as ancient, but far from new, this is known as _[[synthetic differential geometry]]_. For the kinds of applications as mentioned above we need something a bit more expressive, we consider _[[differential cohesion|differentially]] [[cohesive (infinity,1)-topos|cohesive homotopy theory]]_.

We discuss how arithmetic concepts such as [[adeles]], [[ideles]], the [[idele class group]] etc. have structural analogs in any context of [[differential cohesion]]. We show that specifically in the context of [[complex analytic infinity-groupoid|complex analytic cohesion]] these reproduce the correct analogs of the arithmetic concepts as predicted by the [[function field analogy -- table|function field analogy table]].


## Preliminaries on differential cohesion

Consider [[homotopy cofiber sequence]] of  [[cohesive (∞,1)-toposes]] 

$$
  \mathbf{H}_{red}
  \hookrightarrow
  \mathbf{H}
  \longrightarrow
  \mathbf{H}_{inf}
$$

where the inclusion on the left exhibits [[differential cohesion]] and where $\mathbf{H}_{inf}$ has [[infinitesimal cohesion]].


+-- {: .num_example }
###### Example

Let

* $CplMfd$ be the [[site]] of [[complex analytic manifolds]] with the standard [[open cover]] topology

* $InfPt$ the site of [[infinitesimally thickened points]] with the trivial topology;

* $CplMfd_{sd}$ the site of [[formal manifold|formal]] complex analytic manifolds with the local product topology.

The evident projection and inclusion functors then form a 
[[fiber sequence]] of 1-categories

$$
  CplMfd \longleftarrow CplMfd_{sd} \longleftarrow InfPt
  \,.
$$
 
Under forming [[hypercomplete (∞,1)-topos|hypercomple]] [[(∞,1)-sheaf (∞,1)-topos]] this yields

$$
  \mathbb{C}Analytic\infty Grpd
  \longrightarrow
  \mathbb{C}Analytic\infty Grpd_{sd}
  \longrightarrow
  Inf\infty Grpd
$$

from left to right

* [[complex analytic ∞-groupoids]];

* complex analytic [[synthetic differential ∞-groupoids]]:;

* infinitesimal $\infty$-groupoids

Here the last item is essentially [[formal moduli problems]] but without the condition of $\Gamma(-) = \ast$ and without the condition of [[cohesive (∞,1)-presheaf on E-∞ rings|Lurie-infinitesimal cohesion]] (beware the terminology clash), see at [differential cohesion -- Lie theory](differential+cohesive+%28infinity%2C1%29-topos#LieTheory) for more on this.


=--
