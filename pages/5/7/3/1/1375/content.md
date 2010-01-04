<div class="rightHandSide toc">
[[!include stable homotopy theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Every [[(∞,1)-category]] with finite [[limit]]s has a [[stabilization]] to a [[stable (∞,1)-category]] $Stab(C)$. This stabilization may be defined by abstract properties, but it may also be constructed explicitly as the category of **spectrum object**s in $C$.

In the special case that $C = $ [[Top]], as spectrum object in $C$ is just an ordinary [[spectrum]]. There is an evident generalization of the notion of spectrum from [[Top]] to any $(\infty,1)$-category $C$ with finite limits: a spectrum object $X_\bullet$ is essentially a list of [[pointed object]]s $X_i$ together with equivalences $X \to \Omega X_{i+1}$, from every object in the list to the [[loop space object]] of its successor. 

## Definition

For $C$ an [[(infinity,1)-category]], a **prespectrum object**  of $C$ is 

* a $(\infty,1)$-functor $X : \mathbb{Z} \times \mathbb{Z} \to C$

* such that for all integers $i \neq j$ we have $X(i,j) = 0$ a [[zero object]] of $C$

Notice that this definition is highly redundant. The point is that writing $X[n] \coloneqq X(n,n)$ a spectrum object is for all $n \in \mathbb{Z}$ a (homotopy) commuting diagram

$$
  \array{
    X[n+1] &\to& 0
    \\
    \downarrow && \downarrow
    \\
    0 &\to& X[n]
  }
    \,.
$$

Recalling that in an [[(infinity,1)-category]] with [[zero object]]

* $\Omega X[n+1]$ denotes the pullback of such a diagram;

* $\Sigma X[n]$ denotes the pushout of such a diagram

this induces maps

$$
  \alpha_n : \Sigma X[n] \to X[n+1]
$$

$$
  \beta_{n+1} : X[n] \to \Omega X[n+1]
  \,.
$$

A prespectrum object is

* a **spectrum object** if $\beta_m$ is an equivalence for all for all $m \in \mathbb{Z}$ (a __spectrum below $n$__, if $\beta_m$ is an equivalence for all $m \leq n$);

* a **suspension spectrum** if $\alpha_m$ is an equivalence for all $m \in \mathbb{Z}$ (a __suspension spectrum above $n$__, if $\alpha_m$ is an equivalence for all $m \geq n$).


One writes

* $Sp(C)$ for the full sub-$(\infty,1)$-category of $Fun(\mathbb{Z} \times \mathbb{Z},C)$ on spectrum objects in $C$;

* $Stab(C) \coloneqq Sp(C_*)$ -- the **stabilization of $C$** for the $(\infty,1)$-category of spectrum objects in the $(\infty,1)$-category $C_*$ of [[pointed object]]s of $C$.

## Properties

* If $C$ is a pointed $(\infty,1)$-category with finite [[limit in quasi-categories|limits]], then $Sp(C)$ is a [[stable (infinity,1)-category]].

## Examples

For $C = Top$, $Stab(C)$ is the $(\infty,1)$-category version of the classical stable homotopy category of spaces: the [[stable (infinity,1)-category of spectra]].


## References

section 8 of

* [[Jacob Lurie]], [[Stable Infinity-Categories]]