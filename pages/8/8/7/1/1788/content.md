

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

****


For $\vec x \in \mathbb{R}^3$ write

$$
  D_{\vec x}
  \,\colon\,
  \mathbb{C}^2 
    \longrightarrow 
  \mathbb{C}^2
$$

for the [[linear operator]] given by the [[linear combination]] of the  [[Pauli matrices]] (normalized to $\sigma_i^2 = -1 $ and $\sigma_i^\dagger = - \sigma_i$):
$$
  D_{\vec x}
  \;\coloneqq\;
  \mathrm{i}
  \sum_i x^i \sigma_i
  \,.
$$

Restricting their parameter to the [[2-sphere]],
$$
  S^2 
    \,=\,
  \big\{
    \vec x
    \equiv
    (x^1, x^2, x^3)
    \,\in\,
    \mathbb{R}^3 
    \,\big\vert\,
    \textstyle{\sum_i} (x^i)^2
    \,\,
    1
  \big\}
  \,,
$$
these operators satisfy
$$
  \vec x \,\in\, S^2 
  \;\;\;\;\;
  \vdash
  \;\;\;\;\;
  D_x \circ D_x 
    \;=\; 
  \sum_i (x^i)^2 \mathrm{Iid}_{\mathbb{C}^2}
    \;=\;
  \mathrm{id}_{\mathbb{C}^2}
$$
and hence have [[eigenvalues]] $\pm 1$.

As $\vec x$ varies over $S^2$, the $+1$ [[eigenspaces]] of $D_{\vec x}$, hence the [[kernels]] of $D_{\vec x} - \mathrm{id}$ form a [[subbundle]] of the [[trivial bundle|trivial]] [[complex vector bundle]] of [[rank of a vector bundle|rank]]$=2$ over $S^2$.

This bundle is [[isomorphism|isomorphic]] to $\pm$ the [[basic complex line bundle on the 2-sphere]].

(e.g. [Baum 2015, slide 32](#Baum15))


* {#Baum15} [[Paul Baum]], slide 32 of: *Dirac operator*, lecture at TIFR Mumbai, India (2015) &lbrack;[pdf](https://mathweb.tifr.res.in/sites/default/files/conferences/lectures/DiracOperator.pdf), [[Baum-DiracOperator.pdf:file]]&rbrack;



****


