<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of superdifferential form is the generalization of the notion of [[differential form]] from [[manifold]]s to [[supermanifold]]s.


## Definition {#Definition}

Ordinary [[differential form]]s on a [[manifold]] $X$ may be regarded as the functions on the [[supermanifold]] called the [[shifted tangent bundle]]

$$
  \Omega^\bullet(X) = C^\infty(T[1] X)
  \,.
$$

The notion of shifted tangent bundle makes sense also when $X$ itself was already a supermanifold. Superdifferential forms on a [[supermanifold]] $\mathbf{X}$ are similarly the algebra of functions on the shifted tangent bundle $T[1] \mathbf{X}$.


Another way to think of superdifferential forms is using the perspective of Lie theory:

For $\mathbf{X}$ a supermanifold with function algebra $C^\infty(\mathbf{X})$, the [[Lie infinity-algebroid|qDGCA]] $\Omega^\bullet(X)$ of differential forms on $X$ is the [[Weil algebra]] of $C^\infty(\mathbf{X})$, (regarded as a $\mathbb{Z}_2$-graded [[dg-algebra]]).

## Examples {#Examples}

Let $\mathbf{X} = \mathbb{R}^{1|1}$. The [[superalgebra]] of functions on $\mathbf{X}$ is the [[exterior algebra]] that is generated over $C^\infty(\mathbf{R})$ from a single generator $\theta$ in odd degree (the canonical odd coordinate). 

The algebra of superdifferential forms on $\mathbb{R}^{1|1}$ is the [[exterior algebra]] generated over $C^\infty(\mathbb{R})$ from 

* a generator $\theta$ in odd degree (the canonical odd coordinate);

* a generator $d x$ in odd degree (the differential of the canonical even coordinate);

* a generator $d \theta$ in even degree (the differential of the canonical odd coordinate).

Notice in particular that while $ d x \wedge d x = 0$
the wedge product $d \theta \wedge d\theta$ is non-vanishing, since $d \theta$ is in even degree. In fact al higher wedge powers of $d \theta$ with itself exist.


## Remarks

* Being a $\mathbb{Z}_2$-graded locally free algebra itself, one can regard $\Omega^\bullet(X)$ itself (even for $X$ a usual manifold!) as the "algebra of functions" (more precisely inner hom, i.e. mapping space into the line) on another supermanifold. That supermanifold is called $T[1] X$, the **[[shifted tangent bundle]]** of $X$. By definition we have $C^\infty(T[1]X) = \Omega^\bullet(X)$. From this point of view, the existence of the differential $d$ on the graded algebra $\Omega^\bullet(X)$ translates into the existence of a special odd vector field on $T[1]X$. This is a **homological vector field** in that it is odd and the super Lie bracket of it with itself vanishes: $[d,d] = 0$.

* In the context of [[NQ-supermanifolds]], where one may regard $C^\infty(X)$ as the Chevalley-Eilenberg algebra of an $L_\infty$-[[Lie infinity-algebroid|algebroid]] it is useful to notice that $\Omega^\bullet(X)$ is the corresponding [[Weil algebra]]. If $X$ is a Lie $n$-algebroid then $T[1]X$ is a Lie $(n+1)$-algebroid.


[[!redirects differential forms on supermanifolds]]
[[!redirects super differential form]]