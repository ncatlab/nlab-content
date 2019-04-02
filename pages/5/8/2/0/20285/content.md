\begin{centre}
  \begin{tikzcd}[row sep=huge, column sep=huge]
	 & \text{second countable} & & \sigma\text{-locally finite base} \\
	\text{separable space} & \text{Lindelöf} & & \substack{\text{weakly Lindelöf} \wedge \\ \sigma\text{locally finite base}} \\
    &  \text{weakly Lindelöf} & &
    \arrow[Rightarrow, from=1-2, to=2-1, 
        "\substack{\text{countable}\\ \text{choice}}"above left] 
    \arrow[Rightarrow, from=1-2, to=2-2,
        "\substack{\text{countable}\\ \text{choice}}"] 
    \arrow[Rightarrow, from=2-1, to=2-2, "\text{if $X$ metacompact}"] 
    \arrow[Rightarrow, from=2-2, to=3-2]
    \arrow[Rightarrow, from=2-1, to=3-2]
    \arrow[Rightarrow, from=2-4, to=3-2]
    \arrow[Rightarrow, from=2-4, to=1-4]
    \arrow[Rightarrow, from=1-2, to=1-4]
    \arrow[Rightarrow, from=2-4, to=1-2]
\end{tikzcd}
\end{centre}


| properties | implications |
|--|--|
| [[second-countable space|second-countable]]: there is a [[countable set|countable]] [[topological base|base]] of the topology. |  |
|[[separable space|separable]]: there is a countable [[dense subspace|dense]]  subset.| [[second-countable spaces are Lindelöf]] |
| [[Lindelöf topological space|Lindelöf]]: every [[open cover]] has a [[countable cover|countable]] sub-cover. | |
| [[weakly Lindelöf topological space|weakly Lindelöf]]: every [[open cover]] has a [[countable set|countable]] subcollection the union of which is dense.| |
| $\sigma$-locally finite base, i.e. $X$ has a [[countably locally finite set of subsets|countably locally finite]] [[topological base|base]] | |
| [[metacompact space|metacompact]]: every open cover has a point-finite open refinement which covers $X$ | |