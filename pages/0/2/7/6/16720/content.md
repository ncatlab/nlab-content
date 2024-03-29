##Informal definition##

Toda-Smith complexes are [[finite spectra]] characterized by having a particularly simple homology, and are used in stable homotopy theory.

Toda-Smith complexes provided examples of [[periodic map]]s. Thus, they led to the construction of the [[nilpotent and periodicity theorems]], which provided the first organization of the [[stable homotopy groups of spheres]] (localized at a prime) into families of maps via [[chromatic homotopy theory]].

## Mathematical Context ##
The story begins with the degree p map on $S^1$  (as a circle in the complex plane):

$$S^1 \to S^1$$
$$z \mapsto z^p$$

The degree p map is well defined for $S^k$ in general, where $k \in math{N}$. 
If we apply the infinite suspension functor to this map, $\Sigma^{\infty}S^1 \to \Sigma^{\infty}S^1 =: \mathbb{S}^1 \to \mathbb{S}^1$ and we take the cofiber of the resulting map: 

$$S \xrightarrow{p} S \to S/p$$

We find that $S/p$ has the remarkable property of coming from a Moore space (i.e., a designer (co)homology space: $H^n(X) \simeq Z/p$, and $\tilde{H}^*(X)$ is trivial for all $* \neq n$).

## Formal definition ##
The $n$th Toda-Smith complex, $V(n)$ where $n \in \{-1, 0, 1, 2, 3, ... \}$, is a finite spectrum which satisfies the property that its BP-homology, $BP_*(V(n)) \text{:=} [\mathbb{S}^0, BP \wedge V(n)]$, is isomorphic to $BP_*/(p, ..., v_n)$. 

That is, Toda-Smith complexes are completely characterized by their $BP$-local properties, and are defined as any object $V(n)$ satisfying one of the following equations:

* $BP_*(V(-1)) \simeq BP_*$
* $BP_*(V(0)) \simeq BP_*/p$
* $BP_*(V(1)) \simeq BP_*/(p, v_1)$
*  etc.


## Examples of Toda-Smith complexes ##

* the sphere spectrum, $BP_*(S^0) \simeq BP_*$, which is $V(-1)$.
* the mod p Moore spectrum, $BP_*(S/p) \simeq BP_*/p$, which is $V(0)$

## Relevance to stable homotopy theory ##

It may help the reader to recall that that $BP_* = \mathbb{Z}_p[v_1, v_2, ...]$, $|v_i| = 2(p^i-1)$.

The periodic maps, $\alpha_t, \beta_t,$ and $\gamma_t$, come from degree maps between the Toda-Smith complexes, $V(0)_k, V(1)_k,$ and $V(2)_k$ respectively.

(... add in their relation to the $v_2$ periodic elements, and the reasoning behind the shift $2(p^i-1)$)