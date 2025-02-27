
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

A theorem in [[Galois cohomology]] due to [[David Hilbert]].

## Statement

There are actually two versions of Hilbert's theorem 90, one multiplicative and the other additive. We begin with the multiplicative version. 

+-- {: .num_theorem #mult90} 
###### Theorem 
**(Hilbert)** 
Suppose $K$ be a [[finite set|finite]] [[Galois extension]] of a [[field]] $k$, with a [[cyclic group|cyclic]] [[Galois group]] $G = \langle g \rangle$ of [[order]] $n$. Regard the [[multiplicative group]] $K^\ast$ as a $G$-[[module]]. Then the [[group cohomology]] of $G$ with [[coefficients]] in $K^\ast$ -- the [[Galois cohomology]] -- satisfies 

$$
  H^1(G, K^\ast) = 0
  \,.
$$ 

=-- 

Before embarking on the proof, we recall from the article [projective resolution](http://ncatlab.org/nlab/show/projective+resolution#CohomologyOfCyclicGroups) that if $G = C_n$ is a finite cyclic group of order $n$, then there is a projective resolution of $\mathbb{Z}$ as trivial $G$-module: 

$$\ldots \stackrel{N}{\to} \mathbb{Z}G \stackrel{D}{\to} \mathbb{Z}G \stackrel{N}{\to} \mathbb{Z}G \stackrel{D}{\to} \mathbb{Z}G \to \mathbb{Z} \to 0$$ 

where the map $\mathbb{Z}G \to \mathbb{Z}$ is induced from the trivial group homomorphism $G \to 1$ (hence is the map that forms the sum of all [[coefficients]] of all group elements), and where $D$, $N$ are multiplication by special elements in $\mathbb{Z}G$, also denoted $D$, $N$: 

$$D \coloneqq g - 1,$$

$$\,$$ 

$$N \coloneqq 1 + g + g^2 + \ldots + g^{k-1}$$ 

The calculations in the proof that follows implicitly refer to this resolution as a means to defining $H^n(G, A)$ (in the case $A = K^\ast$), by taking cohomology of the induced cochain complex 

$$0 \to \hom_{\mathbb{Z}G}(\mathbb{Z}, A) \to \hom_{\mathbb{Z}G}(\mathbb{Z}G, A) \to \hom_{\mathbb{Z}G}(\mathbb{Z}G, A) \to \ldots$$ 

+-- {: .proof} 
###### Proof 

Let $\sigma \in \mathbb{Z}G$ be an element of the [[group algebra]], and denote the [[action]] of $\sigma$ on an [[element]] $\beta \in K$ by exponential notation $\beta^\sigma$. The action of the element $N \in \mathbb{Z}G$ is 

$$\beta^N = \beta^{1 + g + \ldots + g^{n-1}} = \beta \cdot \beta^g \cdot \ldots \beta^{g^{n-1}}$$ 

which is precisely the _[[norm]]_ $N(\beta)$. We are to show that if $N(\beta) = 1$, then there exists $\alpha \in K$ such that $\beta = \alpha/g(\alpha)$. 

By lemma \ref{XYZ} below, the [[homomorphisms]] $1, g, \ldots, g^{n-1}: K^\ast \to K^\ast$ are, when considered as elements in a vector space of $K$-valued functions, $K$-[[linear independence|linearly independent]]. It follows in particular that 

$$1 + \beta g + \beta^{1+g}g^2 + \ldots + \beta^{1 + g + \ldots + g^{n-2}}g^{n-1}$$ 

is not identically zero, and therefore there exists $\theta \in K^\ast$ such that the element 

$$\alpha = \theta + \beta \theta^g + \beta^{1+g}\theta^{g^2} + \ldots + \beta^{1 + g + \ldots + g^{n-2}}\theta^{g^{n-1}}$$ 

is non-zero. Using the fact that $N(\beta) = 1$, one may easily calculate that $\beta \alpha^g = \alpha$, as was to be shown. 
=-- 

Now we give the additive version of Hilbert's theorem 90: 

+-- {: .num_theorem #add90} 
###### Theorem 
Under the same hypotheses given in \ref{mult90}, and regarding the additive group $K$ as a $G$-module, we have 

$$
H^1(G, K) = 0
  \,.
$$ 

=-- 

+-- {: .proof} 
The _trace_ of an element $\alpha \in K$ is defined by  

$$Tr(\alpha) \coloneqq N \cdot \alpha = \alpha + g(\alpha) + \ldots + g^{n-1}(\alpha).$$ 

We want to show that if $Tr(\beta) = 0$, then there exists $\alpha \in K$ such that $\beta = \alpha - g(\alpha)$. By the theorem on linear independence of characters (following section), there exists $\theta$ such that $Tr(\theta) \neq 0$; notice $Tr(\theta)$ belongs to the ground field $k$ since $g \cdot N = N$. Put 

$$\alpha \coloneqq \frac1{Tr(\theta)}(\beta g(\theta) + (\beta + g(\beta))g^2(\theta) + \ldots + (\beta + g(\beta) + \ldots + g^{n-2}(\beta))g^{n-1}(\theta).$$ 

One may then calculate that 

$$\array{
\alpha - g(\alpha) & = & \frac1{Tr(\theta)}(\beta g(\theta) + \beta g^2(\theta) + \ldots + \beta g^{n-1}(\theta) - (g(\beta) + \ldots + g^{n-1}(\beta))\theta \\ 
 & = & \frac1{Tr(\theta)}(\beta g(\theta) + \beta g^2(\theta) + \ldots + \beta g^{n-1}(\theta) + \beta \theta) \\
 & = & \beta 
}$$ 

where in the second line we used $Tr(\beta) = 0$. 

=-- 



## Independence of characters

The next result may be thought of as establishing "independence of characters" (where "[[group character|characters]]" are valued in the [[multiplicative group]] of a field): 

+-- {: .num_lemma #XYZ} 
###### Lemma 

Let $K$ be a [[field]], let $G$ be a [[monoid]], and let $\chi_1, \ldots, \chi_n \colon G \to K^\ast$ be distinct monoid [[homomorphisms]]. Then the [[functions]] $\chi_i$, considered as functions valued in $K$, are $K$-[[linear independence|linearly independent]]. 

=-- 

+-- {: .proof} 
###### Proof 
A single $\chi \colon G \to K^\ast$ obviously forms a [[linear independence|linearly independent]] set. Now suppose we have an [[equation]] 

\[a_1 \chi_1 + \ldots + a_n \chi_n = 0\]

where $a_i \in K$, and assume $n$ is as small as possible. In particular, no $a_i$ is [[equality|equal]] to $0$, and $n \geq 2$. Choose $g \in G$ such that $\chi_1(g) \neq \chi_2(g)$. Then for all $h \in G$ we have 

$$a_1 \chi_1(g h) + \ldots + a_n \chi_n(g h) = 0$$ 

so that 

\[a_1 \chi_1(g) \chi_1 + \ldots + a_n \chi_n(g)\chi_n = 0.\] 

Dividing equation 2 by $\chi_1(g)$ and subtracting from it equation 1, the first term cancels, and we are left with a shorter relation 

$$(a_2\frac{\chi_2(g)}{\chi_1(g)} - a_2)\chi_2 + \ldots = 0$$ 

which is a [[contradiction]]. 

=-- 

A corollary of this result is an important result in its own right, the **normal basis theorem**. 

(Will write this out later. I am puzzled that all the proofs I've so far looked at involve determinants. What happened to the battle cry, "Down with determinants!"?) 

## Related concepts

* [[Kummer theory]]

## References

A modern version of Hilbert's Theorem 90 is explained as part of a general theory of Galois descent on page 29 here:

* Philippe Gille and Tam&aacute;s Szamuely, *Central Simple Algebras and Galois Cohomology*, Cambridge U. Press, 2017.   ([pdf](http://www.math.ens.fr/~benoist/refs/Gille-Szamuely.pdf))

They show this result:

+-- {: .num_theorem #mult90modern} 
###### Theorem  
Suppose $K$ be a [[finite set|finite]] [[Galois extension]] of a [[field]] $k$ with Galois group $G$. Regard the [[group]] $GL(n,K)$ as a $G$-[[module]]. Then

$$
  H^1(G, GL(n,K)) = 0
  \,.
$$ 

=-- 

An attempt to understand the Galois descent approach more conceptually can be found here:

* John Baez, Group cohomology and homotopy fixed points, *The n-Category Caf&eacute;*.  ([web](https://golem.ph.utexas.edu/category/2020/04/crossed_homomorphisms_part_2.html)).

Also see:

* [[Günter Tamme]], section II 4.3 of _[[Introduction to Étale Cohomology]]_


[[!redirects Hilbert Theorem 90]]
[[!redirects Hilbert theorem 90]]

[[!redirects Hilbert's theorem 90]]
