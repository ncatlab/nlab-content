## Definition ##

Let $R$ be an [[Archimedean integral domain]] and let $[0, 1]_R$ be the [[unit interval]] in $R$. The __infinite decimal representation__ of $[0, 1]_R$ is a function $\mathcal{I}:[0, 1]_R \to (\mathbb{N} \to [0, 9]_\mathbb{N})$ from the unit interval in $R$ to the type of sequences in the [[natural numbers]] that are bounded below by $0$ and bounded above by $9$, such that $r$ is equal to the [[limit of a sequence|limit of the following sequence]]

$$\prod_{r:[0, 1]_R} r = \lim_{n \to \infty} \sum_{i=0}^{n} \frac{\mathcal{I}(r)_i}{10^i}$$

## Properties ##

* The infinite decimal representation of the unit interval in the [[rational numbers]] consist of all the eventually periodic sequences in the [[natural numbers]] that are bounded below by $0$ and bounded above by $9$. 
  Every rational number in the unit interval could be represented by two natural numbers $m:\mathbb{N}$ and $n:\mathbb{N}$ such that $p:m \leq n$. Let us define the sequences $\delta:\mathbb{N} \to \mathbb{N}$ and $\rho:\mathbb{N} \to \mathbb{N}$ inductively as 
$$\delta_0 \coloneqq m \div n$$
$$\rho_0 \coloneqq m\ \%\ n$$
$$\delta_{s(i)} \coloneqq (\rho_i \cdot 10) \div n$$
$$\rho_{s(i)} \coloneqq (\rho_i \cdot 10)\ \%\ n$$
The sequence $\delta$ is the infinite decimal representation of the rational number $m/n$. 

* The infinite decimal representation of the unit interval in the [[decimal numbers]] consist of all the sequences such that there is a natural number $N$ such that for all decimal number $i$ and natural numbers $n \geq N$, $\mathcal{I}(i)(n) = 0$ or $\mathcal{I}(i)(n) = 9$. 

## See also ## 

* [[real numbers]]

* [[pre-algebra real numbers]]

* [[sequence]] 

* [[limit of a sequence]]

* [[unit interval]]