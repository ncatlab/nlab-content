
\tableofcontents

## Definition

Let $(X,\rightarrow)$ be an [[abstract rewriting system]], i.e., a [[set]] equipped with a [[binary relation]] $\rightarrow$. Write $\rightarrow^{*}$ for the [[reflexive-transitive closure]] of $\rightarrow$. We say that $\rightarrow$ is __confluent__ iff for every $a,b,c \in X$ such that $a \rightarrow^* b$ and $a \rightarrow^* c$, there exists $d \in X$ such that $b \rightarrow^{*} d$ and $c \rightarrow^{*} d$.

## Strong normalization 

Say that an abstract rewriting system $(X, \rightarrow)$ is *strongly normalizing* if every sequence 

$$x_0 \rightarrow x_1 \rightarrow \ldots$$ 

is eventually stable: there is some $i$ such that $x_i = x_{i+1} = \ldots$. An element $x$ is *normal* if $x \rightarrow y$ implies $x = y$. 

Define $y \prec x$ to mean $x \rightarrow^{*} y$ and $x \neq y$. The condition of being strongly normalizing is that all downward chains 

$$\ldots \prec x_1 \prec x_0$$ 

terminate after finitely many steps (no infinite descent), i.e., that $\prec$ is a [[well-founded relation]]. 

\begin{proposition} 
In a confluent strongly normalizing abstract rewriting system $(X, \rightarrow)$, for every element $x$ there is a unique normal $y$ such that $x \rightarrow^{*} y$. 
\end{proposition}

\begin{proof} 
Of course, for every $x$ there is *some* normal $y$ for which $x \rightarrow^{*} y$. If that were not true for some $x$, then by [[dependent choice]], we can construct a sequence $(x_n)$ with $x_0 = x$ and for which $x_{n+1} \prec x_n$ (since by hypothesis no $x_n$ in the chain is normal). But this violates "no infinite descent". 

Now suppose $x \rightarrow^{*} t$ and $x \rightarrow^{*} t'$ for normal $t, t'$. By confluence, there is some $u$ such that $t \rightarrow^{*} u$ and $t' \rightarrow^{*} u$. By normality of $t, t'$, we have $t = u = t'$, establishing uniqueness. 
\end{proof} 

With a little extra care, the word "confluent" in the proposition can be replaced by "locally confluent", in the sense of [[locally confluent relation]]. 

## Related concepts

* [[locally confluent relation]]

* [[confluent category]]

* [[Church-Rosser theorem]] 

## References

* Franz Baader, Tobias Nipkow: _Term Rewriting and All That_, Cambridge University Press (1998)  &lbrack;[doi:10.1017/CBO9781139172752](https://doi.org/10.1017/CBO9781139172752)&rbrack;

[[!redirects confluence]]
[[!redirects confluent]]
