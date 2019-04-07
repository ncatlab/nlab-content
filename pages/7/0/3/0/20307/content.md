[[!redirects metrisable spaces have countably locally discrete bases]]


## Definitions

+-- {: .num_defn #LocallyFiniteCover}
###### Definition
**([[locally finite cover]])**

Let $(X,\tau)$ be a [[topological space]].

An [[open cover]] $\{U_i \subset X\}_{i \in I}$ of $X$ is called  _locally finite_ if for each point $x \in X$, there exists a  [[neighbourhood]] $U_x \supset \{x\}$ such that it [[intersection|intersects]] only finitely many elements of the cover, hence such that  $U_x \cap U_i \neq \emptyset$ for only a [[finite number]] of $i \in I$.

=--

+-- {: .num_defn #RefinementOfOpenCovers}
###### Definition
**([[refinement]] of [[open covers]])


Let $(X,\tau)$ be a [[topological space]], and let $\{U_i \subset X\}_{i \in I}$ be a [[open cover]].
 
Then a _[[refinement]]_ of this open cover is a set of open subsets $\{V_j \subset X\}_{j \in J}$ which is still an [[open cover]] in itself and such that for each $j \in J$ there exists an $i \in I$ with $V_j \subset U_i$.

=--


## Statement

\begin{theorem}
Every open cover of a metric space has a [[countably locally discrete set of subsets|$\sigma$-locally discrete]] [[refinement]]. 
\end{theorem}

\begin{corollary}
Every metric space $X$ has a $\sigma$-locally discrete base.
\end{corollary}

\begin{proof}
Set $\mathcal{U}_n \coloneqq \{ \text{open ball of radius }\; 1/n \;\text{ around }\;\, x \mid x \in X \}$. For each $N$ let $\mathcal{V}_n$ be a $\sigma$-locally discrete refinement of $\mathcal{U}_n$. By a diagonal argument the family $\mathcal{V} \coloneqq \bigcup_n \mathcal{V}_n$ is also $\sigma$-locally discrete. Moreover $\mathcal{V}$ is a base since for each point $x$ the balls of radius $1/n$ form a [[neighborhood base]].
\end{proof}


## Related statements

* [[metrization theorem]]

* [[metric spaces are paracompact]]

* [[paracompact Hausdorff spaces are normal]]

* [[locally compact and sigma-compact spaces are paracompact]]

* [[second-countable regular spaces are paracompact]]

* [[regular Lindelöf spaces are paracompact]]

* [[CW-complexes are paracompact Hausdorff spaces]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]

## References

* [[Ryszard Engelking]], _General Topology_, Heldermann Verlag Berlin, 1989.

* K. Kuratowski, _Topology_, 2014, vol. 1.