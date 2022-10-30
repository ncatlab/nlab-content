
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[topological homotopy theory]], the _fundamental theorem of covering spaces_ says that for a sufficiently well-behaved [[topological space]] $X$, then the [[functor]] which sends a [[covering space]] of $X$ to the [[Set]]-[[action]] ([[permutation representation]]) of the [[fundamental groupoid]] of $X$ on the [[fibers]] of $E$ is an [[equivalence of categories]]. 

This is a basic instance of the general principle of [[Galois theory]]. 

It follows in particular that for [[connected topological space|connected]] $X$ then the [[automorphism group]] of the [[universal covering space]] of $X$ coincides with the [[fundamental group]] $\pi_1(X,x)$ itself (for any baspoint $x$). This often yields a convient means to determine the [[fundamental group]] of $X$ in the first place.


## Statement

+-- {: .num_theorem #FundamentalTheoremOfCoveringSpaces}
###### Theorem
**(fundamental theorem of covering spaces)**

Let $B$ be a [[topological space]] which is [[locally path-connected space|locally path-connected]] and [[semi-locally simply-connected space|semi-locally simply-connected]].

Then the [[category]] $Cov/B$ of [[covering spaces]] over $B$ is [[equivalence of categories|equivalent]] to the [[category of functors]] $\Pi_1(B) \to Set$ from the [[fundamental groupoid]] of $B$ to [[Set]] ([[permutation representation]]). 

This equivalence is exhibited by the [[functor]]

$$
  Fiber  
    \;\colon\; 
  Cov/B \longrightarrow Set^{\Pi_1(B)}
$$ 

sending a covering space $p: E \to B$ to the functor which maps the object $b \in \Pi_1(B)$ to the fiber $E_b = p^{-1}(b)$. Given a map $[\phi]: b \to c$ in $\Pi_1(B)$, where $\phi$ is a path from $b$ to $c$, the **unique path-lifting lemma** says that for any $e \in E_b$, there exists a unique fill-in $\tilde{\phi}: I \to E$, that is the diagonal arrow making the following diagram commute:

$$\array{
\{0\} & \stackrel{e}{\to} & E\\
i \downarrow & \nearrow & \downarrow p \\ 
I & \overset{\phi}{\to} & B
}$$ 

and we define $Fiber([\phi]): E_b \to E_c$ as the map sending $e \in E_b$ to $\tilde{\phi}(1) \in E_c$. 

=--

(e.g [M&#248;ller 11, theorem 7.8, corollary 7.9](#Moller11))

+-- {: .num_lemma}
###### Lemma
**(path lifting property)**

Let $p \colon E \to X$ be a [[covering space]]. 

Given 

1. $\gamma \colon [0,1] \to X$ a [[path]] in $X$, 

1. $\hat x_0 \in E$ be a lift of its starting point, hence such that $p(\hat x_0) = \gamma(0)$

then there exists a unique path $\hat \gamma \colon [0,1] \to E$ such that

1. it is a lift of the original path: $p \circ \hat \gamma = \gamma$;

1. it starts at the given lifted point: $\hat \gamma(0) = \hat x_0$.

In other words, every [[commuting diagram]] in [[Top]] of the form

$$
  \array{
    \{0\} &\overset{\hat x_0}{\longrightarrow}& E
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{\gamma}{\longrightarrow}& X
  }
$$

has a unique [[lift]]:

$$
  \array{
    \{0\} &\overset{\hat x_0}{\longrightarrow}& E
    \\
    \downarrow &{}^{\mathllap{\hat \gamma}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{\gamma}{\longrightarrow}& X
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof


...

=--


## Applications

* [[fundamental group of the circle is the integers]]

## References

Lecture notes include

* {#Waldhausen} [[Friedhelm Waldhausen]], around p. 122 of  _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

* {#Moller11} [[Jesper Møller]], _The fundamental group and covering spaces_ (2011) ([pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf))


