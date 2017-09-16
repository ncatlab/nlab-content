
#Definition#

For $C$ an [[(infinity,1)-category]], a **prespectrum object**  of $C$ is 

* a $(\infty,1)$-functor $X : \mathbb{Z} \times \mathbb{Z} \to C$

* such that for all integers $i \neq j$ we have $X(i,j) = 0$ a [[zero object]] of $C$

Notice that this definition is highly redundant. The point is that writing $X[n] := X(n,n)$ a spectrum object is for all $n \in \mathbb{Z}$ a (homotopy) commuting diagram

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

A spectrum object is

* a **spectrum below $n$** of $\beta_m$ is an equivalence for all $m \leq n$;

* a **suspension spectrum above $n$** if $\alpha_m$ is an equivalence for all $m \geq n$

* a **spectrum object** if it is a spectrum object below $n$ for all $n \in \mathbb{Z}$.

One writes

* $Sp(C)$ for the full sub-$(\infty,1)$-category on spectrum objects in $C$;

* $Stab(C) := Sp(C_*)$ -- the **stabilization of $C$** for the $(\infty,1)$-category of spectrum objects in the $(\infty,1)$-category $C_*$ of [[pointed object]]s of $C$.

#Properties#

* If $C$ is a pointed $(\infty,1)$-category with finite [[limit in quasi-categories|limits]], then $Sp(C)$ is a [[stable (infinity,1)-category]].

#Examples#

For $C = Top$, $Stab(C)$ is the $(\infty,1)$-category version of the classical stable homotopy category of spaces: the [[stable (infinity,1)-category of spectra]].


#References#

section 8 of

* [[Jacob Lurie]], [[Stable Infinity-Categories]]