#Contents#
* automatic table of contents goes here
{:toc}


##Definition##

A **Hurewicz fibration** $p:E\to B$ is a [[continuous map]] of [[topological spaces]] that satisfies the [[right lifting property]] with respect to maps $\sigma_0:X\cong X\times\{0\}\hookrightarrow X\times I$ for *all* topological spaces $X$. 

This right lifting property is in this context called the [[homotopy lifting property]], because the maps from $X\times I$ are understood as [[homotopies]]. In more detail, for every space $X$, any homotopy $F:X\times I\to B$, and a continuous map $f:X\to E$, there is a homotopy $\tilde{F}:X\times I\to E$ such that $f =\tilde{F}
\circ\sigma_0 :=\tilde{F}_0$ and $F=p\circ\tilde{F}$: 

$$
  \array{
    X &\stackrel{f}\to& E
    \\
    \downarrow^{\sigma_0} &{}^{\tilde{F}}\nearrow&  \downarrow^p
    \\
    X\times I &\stackrel{F}{\to}& B
  }
  \,.
$$

Instead of checking the homotopy lifting property, one can instead solve a universal problem, see [[Hurewicz connection]].

## Appearance in a model structure ##

There is a [[Quillen model category]] structure on [[Top]] where fibrations are Hurewicz fibrations, cofibrations are [[Hurewicz cofibration]]s and weak equivalences are [[homotopy equivalences]]; see [[model structure on topological spaces]]. There is a version of Hurewicz fibrations for [[pointed spaces]], as well as in the [[slice category]] $Top/B_0$ where $B_0$ is a fixed base.

##References

The historical paper of Hurewicz is

* Witold Hurewitz, _On the concept of fiber space_, Proc. Nat. Acad. Sci. USA __41__ (1955) 956--961; MR0073987 (17,519e) [PNAS,pdf](http://www.pnas.org/content/41/11/956.full.pdf).

Hurewicz fibrations are nowdays a standard topic in textbooks of algebraic topology (Whitehead, Spanier, Hatcher...). 