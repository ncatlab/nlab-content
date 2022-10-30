Projection (or: projective) measures are operator-valued [[measures]] of a special type. They appear for example in the theory of reproducing kernel [[Hilbert spaces]], [[coherent states]] and the foundations of [[quantum mechanics]]. A projection measure is used to parametrize a complete family of [[projection operator]]s by subsets of some parameter space.  

Given a set $X$ and some $\sigma$-algebra $B$ of subsets of $X$, with $X\in B$, and a complex Hilbert space $H$, a map $P: B\to End H$ is called a __projective (projection) measure__ on $B$ with values in $End H$ if

* all operators in the image are selfadjoint $P(A) = P(A)^*$

* $P(A_1\cap A_2) = P(A_1) P(A_2)$ for all $A_1,A_2\in B$ where the product is the composition of the operators

* $P(A_1\cup A_2) = P(A_1)+P(A_2)$ for all $A_1,A_2\in B$ such that $A_1\cap A_2 = \emptyset$

* if $A_n\to A$, in the sense of coinciding upper and lower limit of sets, $A= \cap_n \cup_{k\geq n} A_k = \cup_n \cap_{k\geq n} A_k$, then $P(A_n)\to P(A)$ in the strong  [[operator topology]]. (note: check if strong)

Typical example is that $(X,\tau)$ is a [[topological space]] and $B$ is the $\sigma$-[[sigma-algebra|algebra]] $\mathcal{B}(X)$ of [[Borel set|Borel subsets]] of $X$.

* Gerald B. Folland, _A course in abstract harmonic analysis_, Studies in Adv. Math. CRC Press 1995, [Zbl] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0857.43001&format=complete)
* A. A. Kirillov, A. D. Gvi&#353;iani, &#1058;&#1077;&#1086;&#1088;&#1077;&#1084;&#1099; &#1080; &#1079;&#1072;&#1076;&#1072;&#1095;&#1080; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1086;&#1085;&#1072;&#1083;&#1100;&#1085;&#1086;&#1075;&#1086; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;&#1072; (theorems and exercises in functional analysis), Moskva, Nauka 1979, 1988
[[!redirects projective measure]]