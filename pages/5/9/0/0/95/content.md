#Idea#

...

#Definition#

The **cardinality** of a [[groupoid]] $X$ is
$$|X| = \sum_{[x]} \frac{1}{|Aut(x)|}$$
where the sum is over isomorphism classes of objects of $X$ and $|Aut(x)|$ is the cardinality of the [[automorphism group]] of an object $x$ in $X$. If this sum diverges, we say $|X| = \infty$. If the sum converges, we say $X$ is **tame**.

This is the special case of a more general definition:

The groupoid cardinality of an [[∞-groupoid]] $X$ -- equivalently the **Euler characteristic** of a [[topological space]] $X$ (that's the same, due to the [[homotopy hypothesis]]) -- is, if it converges, the alternating product of cardinalities of the ([[simplicial homotopy group|simplicial]]) [[homotopy group]]s

$$
  |X| := \sum_{[x]}\prod_{k = 1}^\infty |\pi_k(X,x)|^{(-1)^k}
  =
  \sum_{[x]}
  \frac{1}{|\pi_1(X,x)|}
  |\pi_2(X,x)|
  \frac{1}{|\pi_3(X,x)|}
  |\pi_4(X,x)|
  \cdots
  \,.
$$

+--{: .query}
[[Tim Porter]] This looks to be more or less the same as what is referred to as the total homotopy order of a space, introduced by Quinn in notes on TQFTs :

F. Quinn, 1995, Lectures on axiomatic topological quantum field theory , in D. Freed and 
K. Uhlenbeck, eds., Geometry and Quantum Field Theory , volume 1 of IAS/Park City Mathematics Series , AMS/IAS.

This may explain why the link between Yetter's invariant and groupoid cardinality that [[Urs]] noted on the Caf&#233;, comes about in my work with Joao.
=--

#Examples#

* Let $X$ be a [[discrete category|discrete groupoid]] on a finite [[set]] $S$ with $n$ elements. Then the groupoid cardinality of $X$ is just the ordinary cardinality of the set  $S$

  $$
    |X| = n
    \,. 
  $$

* Let $\mathbf{B}G$ be the [[delooping]] of a finite [[group]] $G$ with $k$ elements. Then

  $$
    |\mathbf{B}G| = \frac{1}{k}
  $$

* Let $A$ be an abelian group with $k$ elements. Then we can [[delooping|deloop]] arbitrarily often and obtain the [[Eilenberg?Mac Lane objects]] $\mathbf{B}^n A$ for all $n \in \mathbb{N}$. (Under the [[Dold?Kan correspondence]] $\mathbf{B}^n A$ is the [[chain complex]] $A[n]$ (or $A[-n]$ depending on notational convention) that is concentrated in degree $n$, where it is the group $A$). Then

  $$
    |\mathbf{B}^n A| = 
    \left\{
     \array{ k & if n is \; even
          \\ \frac{1}{k} & if n is \; odd
       }
    \right.
  $$

* Let $E$ be the groupoid of finite sets and bijections. Its groupoid cardinality is the Euler number

  $$
    |E| = \sum_{n\in \mathbb{N}} \frac{1}{|S_n|} = \sum_{n\in \mathbb{N}} \frac{1}{n!} = e
   \,.
  $$

#References#

* [[John Baez]], [[Alexander Hoffnung]], and [[Christopher Walker]], _Groupoidification Made Easy_ ([web](http://math.ucr.edu/home/baez/groupoidification.pdf), [blog](http://golem.ph.utexas.edu/category/2008/12/groupoidification_made_easy.html))

* John C. Baez, [[James Dolan]], _From Finite Sets to Feynman Diagrams_ ([arXiv](http://arxiv.org/abs/math.QA/0004133))

* [[Tom Leinster]], _The Euler characteristic of a category_ ([arXiv](http://arxiv.org/abs/math.CT/0610260), [TWF](http://math.ucr.edu/home/baez/week244.html), [blog](http://golem.ph.utexas.edu/category/2007/02/this_weeks_finds_in_mathematic_5.html), [blog](http://golem.ph.utexas.edu/category/2006/10/euler_characteristic_of_a_cate.html))