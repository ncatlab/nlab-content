+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

The Chu-Vandermonde identity is a basic identity in the [[combinatorics]] of [[binomial coefficients]]. It can be summarized as a [[polynomial]] identity 

$$\sum_{j=0}^n \binom{x}{j} \binom{y}{n-j} = \binom{x+y}{n}$$ 

in the polynomial ring $\mathbb{C}[x, y]$, where we recall $\binom{x}{k} = \frac{x^{\underline{k}}}{k!} \coloneqq \frac{x (x-1) \ldots (x - k + 1)}{k!}$. 

To prove it, it suffices to verify it for the values $(x, y) = (p, q)$ ranging over $\mathbb{N} \times \mathbb{N}$ (as $\mathbb{N}^2$ is [[Zariski topology|Zariski-dense]] in the [[affine space|affine plane]] $\mathbb{C}^2$). There one can resort to a structural proof or so-called "[[bijective proof]]", where we count the number of $n$-element [[subsets]] $N$ of a finite set $P + Q$, with ${|P|} = p$ and ${|Q|} = q$. Regarding $P$ and $Q$ as subsets of the [[coproduct]] $P + Q$, if the subset $N \cap P$ of $P$ has $j$ elements, then the subset $N \cap Q$ of $Q$ has $n-j$ elements. The subset $N$ determines and is uniquely determined by the pair $(N \cap P, N \cap Q)$. The number of such pairs is $\sum_{j=0}^n \binom{p}{j} \binom{q}{n-j}$, exactly as claimed. 

(Structurally, we are relying on the fact that the category of [[finite sets]] is an [[extensive category]].) 

There is more to be written on this in terms of [[species]], [[coalgebras]], etc. 
 
[[!redirects Chu-Vandermonde formula]] 

[[!redirects Chu-Vandermonde identity]]

[[!redirects Vandermonde identity]] 
[[!redirects Vandermonde formula]] 
[[!redirects Vandermonde convolution identity]] 
[[!redirects Vandermonde convolution formula]]