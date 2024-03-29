
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Baer's criterion_ is a criterion for detecting [[injective objects]] in a [[category]] of [[modules]]: [[injective modules]].

## Statement

Let $R$ be a [[ring]] and  $C = R $[[Mod]] the category of $R$-[[modules]].

+-- {: .num_theorem}
###### Proposition 
**([[Baer's criterion]])**
{#Baer}
An [[object]] $Q \in R Mod$ is [[injective object|injective]] precisely if for $I$ any left $R$-[[ideal]] regarded as an $R$-[[module]], any [[morphism]] $g : I \to Q$ in $C$ can be extended to all of $R$ along the inclusion $I \hookrightarrow R$.
=-- 

+-- {: .proof} 
###### Sketch of proof 
Let $i \colon M \hookrightarrow N$ be a mono in $R Mod$, and let $f \colon M \to Q$ be a map. We must extend $f$ to a map $h \colon N \to Q$. Consider the poset whose elements are pairs $(M', f')$ where $M'$ is an intermediate submodule between $M$ and $N$ and $f' \colon M' \to Q$ is an extension of $f$, ordered by $(M', f') \leq (M'', f'')$ if $M''$ contains $M'$ and $f''$ extends $f'$. By an application of [[Zorn's lemma]], this poset has a maximal element, say $(M', f')$. Suppose $M'$ is not all of $N$, and let $x \in N$ be an element not in $M'$; we show that $f'$ extends to a map $M'' = \langle x \rangle + M' \to Q$, contradiction. 

The set $\{r \in R: r x \in M'\}$ is an ideal $I$ of $R$, and we have a module map $g \colon I \to Q$ defined by $g(r) = f'(r x)$. By hypothesis, we may extend $g$ to a module map $k \colon R \to Q$. Writing a general element of $M''$ as $r x + y$ where $y \in M'$, it may be shown that 

$$f''(r x + y) = k(r) + f'(y)$$ 

is well-defined and extends $f'$, as desired. 
=-- 

## Consequences

+-- {: .num_cor}
###### Corollary
{#DirectSumInjectives} 
Let $R$ be a Noetherian ring, and let $\{Q_j\}_{j \in J}$ be a collection of injective modules over $R$. Then the direct sum $Q = \bigoplus_{j \in J} Q_j$ is also injective. 
=-- 

+-- {: .proof}
###### Proof 
By [Baer's criterion](#Baer), it suffices to show that for any ideal $I$ of $R$, a module map $f \colon I \to Q$ extends to a map $R \to Q$. Since $R$ is Noetherian, $I$ is finitely generated as an $R$-module, say by elements $x_1, \ldots, x_n$. Let $p_j \colon Q \to Q_j$ be the projection, and put $f_j = p_j \circ f$. Then for each $x_i$, $f_j(x_i)$ is nonzero for only finitely many summands. Taking all of these summands together over all $i$, we see that $f$ factors through 

$$\prod_{j \in J'} Q_j = \bigoplus_{j \in J'} Q_j \hookrightarrow Q$$ 

for some finite $J' \subset J$. But a product of injectives is injective, hence $f$ extends to a map $R \to \prod_{j \in J'} Q_j$, which completes the proof. 
=-- 

Conversely, a result of Bass and Papp is that $R$ is Noetherian if direct sums of injective $R$-modules are injective. See [Lam](#Lam), Theorem 3.46. 

## References 

* {#Lam} T.-Y. Lam, _Lectures on modules and rings_, Graduate Texts in Mathematics 189, Springer Verlag (1999). 

