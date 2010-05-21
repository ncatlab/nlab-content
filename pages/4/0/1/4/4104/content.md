## Idea 

If $G$ is a topological group, a _Haar measure_ is a translation-invariant measure on the [[Borel set]]s of $G$. The archetypal example of Haar measure is the Lebesgue measure on $\mathbb{R}^n$. 

## Definition 

The proper generality in which to discuss Haar measure is where the topological group $G$ is locally compact Hausdorff, so we restrict to this case. 

Let $C_c(G)$ denote the algebra of continuous real-valued functions with compact support on $G$. As a [[topological vector space]], it is the directed colimit of real [[Banach space]]s $C(K)$ of continuous functions defined on compact subsets of $G$, each equipped with the uniform or sup norm. Recall that a [[Radon measure]] on $G$ may be described as a continuous linear functional 

$$\mu: C_c(G) \to \mathbb{R}$$ 

which is _positive_ in the sense that $\mu(f) \geq 0$ whenever $f \geq 0$. This defines a measure $\hat{\mu}$ on the $\sigma$-algebra of Borel sets in the usual sense of measure, where 

$$\hat{\mu}(B) = sup_{K \subseteq B, f: K \to [0, 1]} \mu(f)$$ 

By abuse of notation, we generally conflate $\mu$ and $\hat{\mu}$. 

A (left) **Haar measure** on $G$ is a nonzero Radon measure $\mu$ such that 

$$\mu(g B) = \mu(B)$$ 

for all $g \in G$ and all Borel sets $B$. 

(This needs work, but I'll have to come back to it later.)


 