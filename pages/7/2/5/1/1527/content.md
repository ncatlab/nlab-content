
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Coinduction is [[duality|dual]] to [[induction]].  It generalises to [[corecursion]].

It is a method of [[proof]] which relies on the fact that any two states of the [[terminal coalgebra]] [[algebra for an endofunctor|for an endofunctor]] $H$ must be equal if they are indistinguishable under repeated operations of $H$. That is, there are no proper coalgebra [[quotient objects]]. Generally, we show the existence of a [[bisimulation]] between states of terminal coalgebra, that is a relation between states, such that when the coalgebra function is
applied, the respective outputs are still related. Since any bisimulation must be contained within the identity relation, we can then conclude that the states are equal.

## Examples {#Examples}

+-- {: .num_example} 
###### Example 
Let $\bar{\mathbb{N}}$ be the set of [[conatural numbers]] and take $add\colon \bar{\mathbb{N}} \times \bar{\mathbb{N}} \to 1 + \bar{\mathbb{N}} \times \bar{\mathbb{N}}$. We can then establish a bisimulation between the terms $(n + m)$ and $(m + n)$, from which we can conclude that this addition is commutative. (See p. 52 of Rutten [Universal coalgebra: a theory of systems](http://homepages.cwi.nl/~janr/papers/files-of-papers/universal_coalgebra.pdf).) 
=-- 

+-- {: .num_example} 
###### Example 
Many theorems of calculus involving formal [[power series]] $f(x) = \sum_{n \geq 0} \frac{a_n x^n}{n!}$ are naturally viewed as proofs by coinduction. The collection of power series $k[ [x] ]$ over a [[field]] $k$ (say of [[characteristic]] $0$) may be viewed as a *stream coalgebra* $k^\mathbb{N}$, i.e., the [[terminal coalgebra of the endofunctor]] $k \times -:\; Set \to Set$, with the coalgebra structure 

$$\array{
\langle eval_0, D = \frac{d}{d x} \rangle: k[ [x] ] & \to & k \times k[ [x] ] \\ 
\sum_{n \geq 0} \frac{a_n x^n}{n!} & \mapsto & (a_0, \sum_{n \geq 0} \frac{a_{n+1} x^n}{n!})
}$$ 

Thus if we set up a bisimulation $\sim$ between two power series $f, g$, establishing $f(0) = g(0)$ and $(D f) \sim (D g)$, we may conclude by coinduction that $f = g$ (else, $k[ [x] ]/\sim$ would be a proper quotient). 

As an illustration: consider a field $k$ of characteristic $0$ and, for $r \in k$, define $(1 + x)^r$ to be the power series expansion of $\exp(r \cdot \log(1 + x))$, where $\exp(x) = \sum_{n \geq 0} \frac{x^n}{n!}$ and $\log(1 + x) = \sum_{n \geq 1} (-1)^{n+1}\; \frac{x^n}{n}$ is the inverse of $\exp(x)-1$. To prove the generalized [[binomial theorem]] 

$$(1 + x)^r = f(r) \coloneqq \sum_{k \geq 0} \frac{r^\underline{k} x^k}{k!}$$ 

where $r^\underline{k}$ is the [[falling factorial|falling power]] $r(r-1)\ldots (r-k+1)$, we introduce a bisimilarity  

$$\sum_{k \geq 0} \frac{r^\underline{k} x^k}{k!}\; \sim\; \exp(r \cdot \log(1 + x))$$ 

and observe first that the [[constant coefficients]] of $f(x)$ and $(1+x)^r$ are both $1$, and that 

$$D\left(\sum_{k \geq 0} \frac{r^\underline{k} x^k}{k!}\right) = r \sum_{k \geq 0} \frac{(r-1)^\underline{k} x^k}{k!}$$ 

(because $r^{\underline{k+1}} = r \cdot (r-1)^{\underline{k}}$) and similarly 

$$D\left(\exp(r \cdot \log(1 + x))\right) = r \cdot \exp((r-1) \cdot \log(1 + x))$$ 

by the [[chain rule]], whence $D(f/r) \sim D((1+x)^r/r)$. Hence $f/r$ is bisimilar to $(1+x)^r/r$, and we conclude in the terminal coalgebra that $f(x) = (1+x)^r$. 
=-- 

## See also

* [[directed (n,r)-graph]]

* [[bisimulation]]

## References
 {#References}

* [[Bart Jacobs]], [[Jan Rutten]], _A tutorial on (Co)Algebras and (Co)Induction_ ([pdf](http://www.cs.ru.nl/~bart/PAPERS/JR.pdf))

* Davide Sangiorgi, _Introduction to Bisimulation and Coinduction_, Cambridge Universtity Press (2012)  ([web](http://www.cs.unibo.it/~sangio/IntroBook.html))

* Davide Sangiorgi, Jan Rutten (eds.), _Advanced Topics in Bisimulation and Coinduction_, Cambridge Universtity Press (2012) ([web](http://www.cs.unibo.it/~sangio/AdvancedBook.html))

On [[differential calculus]] via coinduction:

* [[Martín Escardó]], [[Duško Pavlović]]: *Calculus in coinductive form*, in *Proceedings of Thirteenth Annual IEEE Symposium on Logic in Computer Science* (1998) 408-417 &lbrack;[doi:10.1109/LICS.1998.705675](https://doi.org/10.1109/LICS.1998.705675), [pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=705675)&rbrack;

About coinduction in [[cubical type theory]]:

* Magnus Baunsgaard Kristensen, [[Rasmus Ejlers Møgelberg]], [[Andrea Vezzosi]], *Greatest HITs: Higher inductive types in coinductive definitions via induction under clocks* ([arXiv:2102.01969](https://arxiv.org/abs/2102.01969))

[[!redirects coinductions]]

[[!redirects coinductive]]

[[!redirects coinductive definition]]

[[!redirects coinductively]]
