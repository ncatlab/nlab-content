\begin{centre}
  \begin{tikzcd}[row sep=huge, column sep=huge]
	 & \text{second countable} & & \sigma\text{-locally finite base} \\
	\text{separable space} & \text{Lindelöf} & & \substack{\text{weakly Lindelöf} \wedge \\ \sigma\text{-locally finite base}} \\
    &  \text{weakly Lindelöf} & &
    \arrow[Rightarrow, from=1-2, to=2-1, 
        "\substack{\text{countable}\\ \text{choice}}"above left] 
    \arrow[Rightarrow, from=1-2, to=2-2,
        "\substack{\text{countable}\\ \text{choice}}"] 
    \arrow[Rightarrow, from=2-1, to=2-2, "\text{if $X$ metacompact}"] 
    \arrow[Rightarrow, from=2-2, to=3-2]
    \arrow[Rightarrow, from=2-1, to=3-2, "\text{AC}"]
    \arrow[Rightarrow, from=2-4, to=3-2]
    \arrow[Rightarrow, from=2-4, to=1-4]
    \arrow[Rightarrow, from=1-2, to=1-4]
    \arrow[Rightarrow, from=2-4, to=1-2]
\end{tikzcd}
\end{centre}


| properties | implications |
|--|--|
| [[second-countable space|second-countable]]: there is a [[countable set|countable]] [[topological base|base]] of the topology. | A second-countable space has a [[countably locally finite set of subsets|$\sigma$-locally finite]] [[topological base|base]]: take the the collection of singeltons of all elements of countable cover of $X$. |
| $\sigma$-locally finite base, i.e. $X$ has a [[countably locally finite set of subsets|countably locally finite]] [[topological base|base]], e.g. a [[metrisable topological space]] by [[Nagata-Smirnov metrization theorem]]. | second-countable spaces are separable: [[countable choice|choose]] a point in each set of countable cover. |
| [[separable space|separable]]: there is a countable [[dense subspace|dense]]  subset. | [[second-countable spaces are Lindelöf]] |
| [[Lindelöf topological space|Lindelöf]]: every [[open cover]] has a [[countable cover|countable]] sub-cover. | [[weakly Lindelöf spaces with countably locally finite base are second countable]] |
| [[weakly Lindelöf topological space|weakly Lindelöf]]: every [[open cover]] has a [[countable set|countable]] subcollection the union of which is dense. | [[separable metacompact spaces are Lindelöf]] |
| [[countable choice]]: the [[natural number]]s is a [[projective object]] in [[Set]]. | separable spaces are weakly Lindelöf: given a countable dense subset and an open cover [[axiom of choice|choose]] for each point of the subset an open from the cover.  |
| [[metacompact space|metacompact]]: every open cover has a point-finite open refinement. | Lindelöf spaces are trivially also weakly Lindelöf. |