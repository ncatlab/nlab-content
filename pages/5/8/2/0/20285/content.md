[[!redirects topology - global countability axioms]]

\begin{tikzcd}[row sep=huge, column sep=huge]
	& & \scriptsize \text{metrisable} 
	&
	\\
	& \text{second countable}  
	& \sigma\text{-locally discrete base}                      
	& \sigma\text{-locally finite base} 
	\\  
	\text{separable space} 
	& \text{Lindel\"of}  
	& \substack{\text{weakly Lindel\"of} \wedge \\ \sigma\text{-locally finite base}} 
	& \text{first countable}
	\\
	& \text{weakly Lindel\"of} & 
	& \text{sequential}
	\\
	& & & \text{Fr\'echet-Urysohn}
	\\
	& & &  \text{countably tight}
	\arrow[Rightarrow, from=2-2, to=3-1, 
	"\substack{\text{countable}\\ \text{choice}}"above left] 
	\arrow[Rightarrow, from=2-2, to=3-2,
	"\substack{\text{countable}\\ \text{choice}}"] 
	\arrow[Rightarrow, from=3-1, to=3-2, "\text{if $X$ metacompact}"] 
	\arrow[Rightarrow, from=3-2, to=4-2]
	\arrow[Rightarrow, from=3-1, to=4-2, "\text{AC}"]
	\arrow[Rightarrow, from=3-3, to=4-2]
	\arrow[Rightarrow, from=3-3, to=2-4]
	\arrow[Rightarrow, from=2-2, to=2-3]
	\arrow[Rightarrow, from=2-3, to=2-4]
	\arrow[Rightarrow, from=3-3, to=2-2]
	\arrow[Rightarrow, from=2-4, to=3-4]
	\arrow[Rightarrow, from=3-4, to=4-4]
	\arrow[Rightarrow, from=4-4, to=5-4]
	\arrow[Rightarrow, from=5-4, to=6-4]
	\arrow[Rightarrow, from=1-3, to=2-3]
	\arrow[Rightarrow, from=2-4, to=1-3, bend right, "\text{if $X$ regular and } \mathrm{T}_2"above right, "\substack{\text{Nagata-Smirnov}\\\text{metrization theorem}}"below left]
\end{tikzcd}


| properties | implications |
|--|--|
| [[metrisable topological space|metrisable]]: topology is induced by a metric | a metric space has a $\sigma$-locally discrete base as a corollary of the fact that [[open covers of metric spaces have open countably locally discrete refinements|open covers of metric spaces have open $\sigma$-locally discrete refinements]]: take $\sigma$-locally discrete refinements of the covers by $1/n$-balls for $n=1,2,\ldots$. |
| [[second-countable space|second-countable]]: there is a [[countable set|countable]] [[topological base|base]] of the topology. | a second-countable space has a [[countably locally finite set of subsets|$\sigma$-locally finite]] [[topological base|base]]: take the the collection of singeltons of all elements of countable cover of $X$. |
| $\sigma$-locally discrete base, i.e. $X$ has a [[countably locally discrete set of subsets|$\sigma$-locally discrete]] [[topological base|base]]. | [[Nagata-Smirnov metrization theorem]] |
| $\sigma$-locally finite base, i.e. $X$ has a [[countably locally finite set of subsets|countably locally finite]] [[topological base|base]]. | second-countable spaces are separable: [[countable choice|choose]] a point in each set of countable cover. |
| [[separable space|separable]]: there is a countable [[dense subspace|dense]]  subset. | [[second-countable spaces are Lindelöf]] |
| [[Lindelöf topological space|Lindelöf]]: every [[open cover]] has a [[countable cover|countable]] sub-cover. | [[weakly Lindelöf spaces with countably locally finite base are second countable]] |
| [[weakly Lindelöf topological space|weakly Lindelöf]]: every [[open cover]] has a [[countable set|countable]] subcollection the union of which is dense. | [[separable metacompact spaces are Lindelöf]] |
| [[countable choice]]: the [[natural number]]s is a [[projective object]] in [[Set]]. | separable spaces are weakly Lindelöf: given a countable dense subset and an open cover [[axiom of choice|choose]] for each point of the subset an open from the cover.  |
| [[metacompact space|metacompact]]: every open cover has a point-finite open refinement. | Lindelöf spaces are trivially also weakly Lindelöf. |