## Definition

Let $(X,\rightarrow)$ be an [[abstract rewriting system]], i.e., a [[set]] equipped with a [[binary relation]] $\rightarrow$. Write $\rightarrow^{*}$ for the [[reflexive-transitive closure]] of $\rightarrow$. We say that $\rightarrow$ is __locally confluent__ iff for every $a,b,c \in X$ such that $a \rightarrow b$ and $a \rightarrow c$, there exists $d \in X$ such that $b \rightarrow^{*} d$ and $c \rightarrow^{*} d$.

## Related concepts

* [[confluent relation]]

## References

* Franz Baader, Tobias Nipkow, _Term Rewriting and All That_, Cambridge University Press, 1998.  [doi](https://doi.org/10.1017/CBO9781139172752).

[[!redirects local confluence]]
[[!redirects locally confluent]]
