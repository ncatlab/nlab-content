Let $X$ and $Y$ be [[topological spaces]]. The set $Map(X,Y)$ (often denoted also $C(X,Y)$) of [[continuous maps]] from $X$ to $Y$ has a natural topology called the __compact-open topology__: a basis of that topology consists of sets of the form $U_{K,V}$, where $K\subset X$ is [[compact space|compact]] and $V\subset Y$ is [[open subpsace|open]], which consists of all continuous maps $f:X\to Y$ such that $f(K)\subset V$. 

For the special case of the function spaces (that is when $Y$ is the [[real line]] or [[complex plane]]) where the domain is a [[metric space]], the compact-open topology is also known as the _topology of uniform convergence on compact subsets_, or if the domain $X$ is also compact, as the _topology of uniform convergence_. 

The compact-open topology is most sensible when the topology of $X$ is [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]], for in this case $Map(X,Y)$ with the compact-open topology is an [[exponential object]] $Y^X$ in the category $Top$ of all topological spaces.  This implies that we have an [[exponential law for spaces]] $Top(X,Map(Y,Z))\cong Top(X\times Y,Z)$ whenever $Y$ is locally compact Hausdorff.  See also [[convenient category of topological spaces]].


[[!redirects compact open topology]]
