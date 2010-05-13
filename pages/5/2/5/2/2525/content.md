
#Contents#
* automatic table of contents goes here
{:toc}

## Idea
The **Euler-Lagrange equations** of a [[functional]] characterize in [[variational calculus]] the _extrema_ of that functional.

The originates from and is mainly used in [[physics]], where the functional in question is the [[action functional]] of a physical system, and where its critical points encode the physically observable configurations.

## Details 

Given a [[Lagrangian]] $L = L(q,\stackrel{\cdot}q,t)$ of a [[classical mechanics|classical mechanical]] system the corresponding action principle can be expressed as **Euler-Lagrange equations**: for all $i$, 

$$
\frac{d}{dt} \left( \frac{\partial L}{\partial \stackrel{\cdot}{q}_i} \right) - \frac{\partial L}{\partial {q}_i}  = 0
$$

If there is only one degree of freedom then one talks in singular: Euler-Lagrange equation. 

Unlike in the usual [[classical mechanics|classical mechanical] systems, in some other problems of [[calculus of variations]] one has Lagrangians involving higher time derivatives; the Euler-Lagrange equations have then correspondingly more terms. Similarly, one can have dependence on more parameters than a single time parameter, what can also be easily incorporated. 

For examples etc. see [wikipedia](http://en.wikipedia.org/wiki/Euler%E2%80%93Lagrange_equation).

[[!redirects Euler-Lagrange equations]]