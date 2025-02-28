
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A type of theorem in [[Galois cohomology]] due to [[David Hilbert]].

## Statements

There are several versions referred to as *Hilbert's theorem 90*. 

### Multiplicative version 

+-- {: .num_theorem #mult90} 
###### Theorem 
**(Hilbert)** 
Suppose $K$ be a [[finite set|finite]] [[Galois extension]] of a [[field]] $k$, with a [[cyclic group|cyclic]] [[Galois group]] $G = \langle g \rangle$ of [[order]] $n$. Regard the [[multiplicative group]] $K^\ast$ as a $G$-[[module]]. Then the [[group cohomology]] of $G$ with [[coefficients]] in $K^\ast$ -- the [[Galois cohomology]] -- satisfies 

$$
  H^1(G; K^\ast) = 0
  \,.
$$ 

=-- 



+-- {: .proof} 
###### Proof 

For the following,  note (see [here](projective+resolution#CohomologyOfCyclicGroups)), that if $G = C_n$ is a finite [[cyclic group]] of [[order of a group|order]] $n$, then there is a [[projective resolution]] of $\mathbb{Z}$ as a [[trivial action|trivial]] $G$-[[module]]: 

$$
  \ldots \stackrel{N}{\to} \mathbb{Z}G \stackrel{D}{\to} \mathbb{Z}G \stackrel{N}{\to} \mathbb{Z}G \stackrel{D}{\to} \mathbb{Z}G \to \mathbb{Z} \to 0
 \,,
$$ 

where the map $\mathbb{Z}G \to \mathbb{Z}$ is induced from the [[trivial group|trivial]] [[group homomorphism]] $G \to 1$ (hence is the map that forms the sum of all [[coefficients]] of all group elements), and where $D$, $N$ are multiplication by special elements in $\mathbb{Z}G$, also denoted $D$, $N$: 

$$D \coloneqq g - 1,$$

$$\,$$ 

$$
  N \coloneqq 1 + g + g^2 + \ldots + g^{k-1}
  \,.
$$ 

The calculations that follow refer to this resolution as a means of defining $H^n(G; A)$ (in the case $A = K^\ast$), by forming the [[cochain cohomology]] of the induced [[cochain complex]] 

$$
 0 \to \hom_{\mathbb{Z}G}(\mathbb{Z}, A) \to \hom_{\mathbb{Z}G}(\mathbb{Z}G, A) \to \hom_{\mathbb{Z}G}(\mathbb{Z}G, A) \to \ldots
  \,.
$$ 

With that understood, let now $\sigma \in \mathbb{Z}G$ be an element of the [[group algebra]], and denote the [[action]] of $\sigma$ on an [[element]] $\beta \in K$ by exponential notation $\beta^\sigma$. The action of the element $N \in \mathbb{Z}G$ is 

$$
  \beta^N 
    = 
  \beta^{1 + g + \ldots + g^{n-1}} 
    = 
  \beta \cdot \beta^g \cdot \ldots \beta^{g^{n-1}}
  \,,
$$ 

which is precisely the _[[norm]]_ $N(\beta)$. We are to show that if $N(\beta) = 1$, then there exists $\alpha \in K$ such that $\beta = \alpha/g(\alpha)$. 

By lemma \ref{XYZ} below, the [[homomorphisms]] $1, g, \ldots, g^{n-1}: K^\ast \to K^\ast$ are, when considered as elements in a vector space of $K$-valued functions, $K$-[[linear independence|linearly independent]]. It follows in particular that 

$$1 + \beta g + \beta^{1+g}g^2 + \ldots + \beta^{1 + g + \ldots + g^{n-2}}g^{n-1}$$ 

is not identically zero, and therefore there exists $\theta \in K^\ast$ such that the element 

$$\alpha = \theta + \beta \theta^g + \beta^{1+g}\theta^{g^2} + \ldots + \beta^{1 + g + \ldots + g^{n-2}}\theta^{g^{n-1}}$$ 

is non-zero. Using the fact that $N(\beta) = 1$, one may easily calculate that $\beta \alpha^g = \alpha$, as was to be shown. 
=-- 


### Additive version

+-- {: .num_theorem #add90} 
###### Theorem 
Under the same hypotheses as in Thm. \ref{mult90}, and regarding the additive group $K$ as a $G$-module, we have 

$$
  H^1(G; K) = 0
  \,.
$$ 

=-- 

\begin{proof}

The _trace_ of an element $\alpha \in K$ is defined by  

$$
  Tr(\alpha) \coloneqq N \cdot \alpha 
  \;=\; 
  \alpha + g(\alpha) + \ldots + g^{n-1}(\alpha)
  \,.
$$ 

We want to show that if $Tr(\beta) = 0$, then there exists $\alpha \in K$ such that $\beta = \alpha - g(\alpha)$. By lemma \ref{XYZ} below, there exists $\theta$ such that $Tr(\theta) \neq 0$; notice that $Tr(\theta)$ belongs to the [[ground field]] $k$ since $g \cdot N = N$. Put 

$$
  \alpha 
    \;\coloneqq\; 
  \frac1{Tr(\theta)}(\beta g(\theta) 
    + 
  \big(
   \beta 
     + 
    g(\beta)
  \big)g^2(\theta) 
  + 
  \ldots 
  + 
  \big(
    \beta 
    + 
    g(\beta) 
    + 
    \ldots 
    + 
    g^{n-2}(\beta)
  \big)
  g^{n-1}(\theta)
  \,.
$$ 

One may then calculate that 

$$\array{
\alpha - g(\alpha) & = & \frac1{Tr(\theta)}(\beta g(\theta) + \beta g^2(\theta) + \ldots + \beta g^{n-1}(\theta) - (g(\beta) + \ldots + g^{n-1}(\beta))\theta \\ 
 & = & \frac1{Tr(\theta)}(\beta g(\theta) + \beta g^2(\theta) + \ldots + \beta g^{n-1}(\theta) + \beta \theta) \\
 & = & \beta \mathrlap{\,,}
}
$$ 

where in the second line we used $Tr(\beta) = 0$. 

\end{proof}



### Modern version

+-- {: .num_theorem #mult90modern} 
###### Theorem  
Suppose $K$ be a [[finite set|finite]] [[Galois extension]] of a [[field]] $k$ with Galois group $G$. Regard the [[general linear group]] $GL(n,K)$ as a $G$-[[module]]. Then

$$
  H^1\big(
   G; GL(n,K)
  \big)  
   \;=\; 
  0
  \,.
$$ 

=-- 

([Gille & Szamuely 2017 p. 29](#GilleSzamuely17))



## Independence of characters

The next result establishes the lemma of "independence of characters" used in the above proofs (where "[[group character|characters]]" are valued in the [[multiplicative group]] of a field): 

+-- {: .num_lemma #XYZ} 
###### Lemma 

Let $K$ be a [[field]], let $G$ be a [[monoid]], and let $\chi_1, \ldots, \chi_n \colon G \to K^\ast$ be distinct monoid [[homomorphisms]]. Then the [[functions]] $\chi_i$, considered as functions valued in $K$, are $K$-[[linear independence|linearly independent]]. 

=-- 

+-- {: .proof} 
###### Proof 
A single $\chi \colon G \to K^\ast$ obviously forms a [[linear independence|linearly independent]] set. Now suppose we have an [[equation]] 

\[a_1 \chi_1 + \ldots + a_n \chi_n = 0\]

where $a_i \in K$, and assume $n$ is as small as possible. In particular, no $a_i$ is [[equality|equal]] to $0$, and $n \geq 2$. Choose $g \in G$ such that $\chi_1(g) \neq \chi_2(g)$. Then for all $h \in G$ we have 

$$a_1 \chi_1(g h) + \ldots + a_n \chi_n(g h) = 0\,,$$ 

so that 

\[a_1 \chi_1(g) \chi_1 + \ldots + a_n \chi_n(g)\chi_n = 0.\] 

Dividing equation 2 by $\chi_1(g)$ and subtracting from it equation 1, the first term cancels, and we are left with a shorter relation 

$$(a_2\frac{\chi_2(g)}{\chi_1(g)} - a_2)\chi_2 + \ldots = 0$$ 

which is a [[contradiction]]. 

=-- 

A corollary of this result is an important result in its own right, the **normal basis theorem**. 



## Related concepts

* [[Kummer theory]]

## References

* [[Günter Tamme]], section II 4.3 of: _[[Introduction to Étale Cohomology]]_, Springer (1994) &lbrack;[doi:10.1007/978-3-642-78421-7](https://doi.org/10.1007/978-3-642-78421-7)&rbrack;

The modern version, Thm. \ref{mult90modern}, 
of Hilbert's Theorem 90, explained as part of a general theory of [[Galois descent]]:

* {#GilleSzamuely17} Philippe Gille, Tam&aacute;s Szamuely, p. 29 of: *Central Simple Algebras and Galois Cohomology*, Cambridge U. Press, (2017)  &lbrack;[doi:10.1017/CBO9780511607219](https://doi.org/10.1017/CBO9780511607219), [pdf](http://www.math.ens.fr/~benoist/refs/Gille-Szamuely.pdf)&rbrack;

An attempt to understand the Galois descent approach more conceptually:

* [[John Baez]]: *Group cohomology and homotopy fixed points*, *The n-Category Caf&eacute;*.  &lbrack;[web](https://golem.ph.utexas.edu/category/2020/04/crossed_homomorphisms_part_2.html)&rbrack;





[[!redirects Hilbert Theorem 90]]
[[!redirects Hilbert theorem 90]]

[[!redirects Hilbert's theorem 90]]
