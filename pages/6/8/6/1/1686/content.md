Let $A$ be an [[abelian category]] . A spectral sequence in $A$ is given by 

* a family $E^{p,q}_r$ of objects in $A$, for all integers $p,q,r$ where only $r\geq 1$ (these are said to form an $r$-th page of spectral sequence)

* for each $p,q,r$ as above a map (called differential) $d^{p,q}_r:E^{p,q}_r\to E^{p+r,q-r+1}_r$ satisfying $d_r^2 = 0$ (more precisely, $d_r^{p=r,q-r+1}\circ d_r^{p,q} = 0$

* isomorphisms $\alpha_r^{p,q}: H^{p,q}(E_r)\to E^{p,q}_{r+1}$ where the cohomology is given by

$$H^{p,q}(E_r) = \mathrm{ker} d^{p,q}_r/ \mathrm{im} d^{p-r,q+r-1}_r$$

There is one requirement on the sequence $(\alpha_r^{p,q})_{r\in Z}$: the limit groups $E^{p,q}_\infty$ exist; typically a stronger requirement: for each pair $(p,q)$ exists an $r_0$ so that for all $r\geq r_0$ $d_r^{p-r,q+r-1} = 0$.

Usually one lists yet another $r = \infty$-page -- a family $E^n$ for all integers $n$ (with a copy of $E^n$ on each place $(p,q)$ of the $n$-th diagonal $p+q = n$) and we say that a spectral sequence $(E^{p,q}_r)$ **converges** to $(E^n)$ if for each $n$ there is a decreasing filtration $E_n \cdots \supset F^p E^n \supset F^{p+1} E^n \supset \cdots$ and isomorphisms $E^{p,q}_\infty \to F^p E^{p+q}/F^{p+1} E^{p+q}$. A spectral sequence is said to **degenerate** in $E_r$-term if $d^{p,q}_{r'} = 0$ for all $r'\geq r$. Then clearly $E_\infty^{p,q} = E_r^{p,q}$.

Spectral sequences are usually graphically presented. They are a standard computational tool in algebraic topology and homological algebra. Some of the standard sources of spectral sequences are [[exact couple]]s, filtered complexes, spectral sequences for (say &#268;ech) cohomology constructed from space covers, and there is a [[Grothendieck spectral sequence]] of a composition of functors. 