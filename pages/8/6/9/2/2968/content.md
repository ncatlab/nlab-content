A [[continuous map]] $p:E\to B$ of [[topological spaces]] satisfies the **homotopy lifting property** (or *covering homotopy property*) with respect to a space $Y$ if for every [[commuting square]] in $Top$

$$
  \array{
    Y &\stackrel{f}\to& E
    \\
    \downarrow^{\sigma_0} &{}^{\tilde{F}}\nearrow&  \downarrow^p
    \\
    Y\times I &\stackrel{F}{\to}& B
  }
  \,.
$$

there is a diagonal such that the entire diagram commutes. The map $\sigma_0:Y\to Y\times I$ is given by $y\mapsto (y,0)$ for $y\in Y$.

A map $p$ is a **[[Hurewicz fibration]]** if it satisfies the homotopy lifting property with respect to all spaces $X$. A map $p$ is a **[[Serre fibration]]** if it satisfies the homotopy lifting property with respect to all disks (equivalently, all topological [[cube]]s). 

The homotopy lifting property is an instance of a [[right lifting property]]. 

The [[Eckmann-Hilton duality|Eckmann–Hilton dual]] of the homotopy lifting property is the [[homotopy extension property]].


[[!redirects covering homotopy property]]