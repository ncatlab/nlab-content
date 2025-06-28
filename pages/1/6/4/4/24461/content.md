
\tableofcontents

## Definition

Let $(X,\rightarrow)$ be an [[abstract rewriting system]], i.e., a [[set]] equipped with a [[binary relation]] $\rightarrow$. Write $\rightarrow^{*}$ for the [[reflexive-transitive closure]] of $\rightarrow$. We say that $\rightarrow$ is __locally confluent__, alternatively is *Church-Rosser*, iff for every $a,b,c \in X$ such that $a \rightarrow b$ and $a \rightarrow c$, there exists $d \in X$ such that $b \rightarrow^{*} d$ and $c \rightarrow^{*} d$.

## Relation to inductive sets 

Given an abstract rewriting system, notated as above, let $\prec$ denote the relation whereby $t \prec x$ if $x \rightarrow^{*} t$ and $x \neq t$. This relation is transitive if $\rightarrow^{*}$ is [[antisymmetric relation|antisymmetric]]. 

Recall that a subset $A \subseteq X$ is $\prec$-[[well-founded relation|inductive]] if 
$$ \forall (x\colon X),\; (\forall (t\colon X),\; t \prec x \;\Rightarrow\; t \in A) \;\Rightarrow\; x \in A.$$

Define an element $x$ to be *normal* if $x \rightarrow^{*} y$ implies $x = y$. Write $Norm(x)$ for the predicate "$x$ is normal". 

+-- {: .num_prop #NormInductive} 
###### Proposition 
In a locally confluent rewriting system $(X, \rightarrow)$, and under the assumption that $\rightarrow^{*}$ is antisymmetric, the set 
$$A = \{x \in X|\exists ! y\; (x \rightarrow^{*} y) \wedge Norm(y)\}$$
is a $\prec$-inductive set.  
=--

\begin{proof} 
For given $x \in X$, suppose the inductive hypothesis is true: that for every $t \neq x$ with $x \rightarrow^{*} t$, there is a unique normal $y$ such that $t \rightarrow^{*} y$. Then by transitivity $x \rightarrow^{*} y$, so $x \rightarrow^{*} y$ for at least one normal $y$. If $x \rightarrow^{*} y$ and $x \rightarrow^{*} z$ and $y, z$ are normal, then there are chains 

$$y \prec \ldots \prec b \prec x, \qquad z \prec \ldots \prec c \prec x.$$ 

Note that $b = c$ implies $y = z$ by inductive hypothesis, so assume instead $b \neq c$. Then by local confluence, there is $d$ with $d \prec b$ and $d \prec c$. We have $d \prec x$ by transitivity, hence $\exists ! w\; d \rightarrow^{*} w \wedge Norm(w)$ by inductive hypothesis. Since also $b \rightarrow^{*} w$, we have $y = w$ by the uniqueness clause for $y$. Similarly $y = z$. Hence $x \rightarrow{*} y$ for a unique normal $y$, and the induction goes through. 
\end{proof} 

Call an abstract rewriting system $(X, \rightarrow)$ *strongly normalizing* if $\rightarrow^{*}$ satisfies the [[ascending chain condition]], i.e., if any countably infinite chain 

$$x_0 \rightarrow^{*} x_1 \rightarrow^{*} x_2 \rightarrow^{*} \ldots$$ 
eventually stabilizes (for some $N$, $x_i = x_{i+1}$ for all $i \geq N$). For such $N$, clearly $x_N$ is normal, so all such chains terminate in a normal element. It is also clear that strong normalization implies antisymmetry. Again writing $y \prec x$ if $x \rightarrow^{*} y$ and $x \neq y$, strong normalization implies there are no infinite descending chains (no infinite descent) 
$$\ldots \prec x_2 \prec x_1 \prec x_0.$$
In other words, $\prec$ is a [[well-founded relation]] (assuming [[classical logic]]). 

+-- {: .num_thm #NewmanLemma} 
###### Theorem 
**(Newman's lemma)**
An abstract rewriting system that is locally confluent and strongly normalizing has the property that for every element $x$ there is a unique normal element $y$ for which $x \rightarrow^{*} y$. 
=--

\begin{proof} 
By Proposition \ref{NormInductive}, the set $\{x \in X|\exists ! y\; (x \rightarrow^{*} y) \wedge Norm(y)\}$ is $\prec$-inductive, and since $\prec$ is well-founded under the strong normalization hypothesis, this set is the entirety of $X$. 
\end{proof} 


## Related concepts

* [[confluent relation]]

* [[well-founded relation]]

* [[Bergman's diamond lemma]] (for now, see Zoran Skoda's notes [here](https://ncatlab.org/zoranskoda/show/diamond+lemma)) 

## References

* Franz Baader, Tobias Nipkow: _Term Rewriting and All That_, Cambridge University Press (1998)  &lbrack;[doi:10.1017/CBO9781139172752](https://doi.org/10.1017/CBO9781139172752)&rbrack;

* M.H.A. Newman, *On theories with a combinatorial definition of “equivalence”*, Annals of
Mathematics, 43(2):223–243, 1942.

* Wikipedia, *Newman's lemma*. [link](https://en.wikipedia.org/wiki/Newman%27s_lemma)

[[!redirects local confluence]]
[[!redirects locally confluent]]
