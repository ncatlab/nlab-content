
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop }
###### Proposition
**(a countable union of countable sets is countable, aka the countable union theorem)**

Assuming the [[axiom of countable choice]] then:

Let $I$ be a [[countable set]] and let 
$\{S_i\}_{i \in I}$ be an $I$-[[dependent type|dependent set]] of [[countable sets]] $S_i$. Then the [[disjoint union]]

$$
  \underset{i \in I}{\cup} S_i
$$

is itself a countable set. 

=-- 

+-- {: .proof} 
###### Proof 

[[classical mathematics|Classical]] proof: we may assume all the $S_i$ are [[nonempty set|nonempty]]. For each $i \in I$, choose a [[surjection]] $f_i: \mathbb{N} \to S_i$ (this requires the [[axiom of countable choice]]) and also a surjection $f: \mathbb{N} \to I$. Then we have a composite surjection 

$$\mathbb{N} \stackrel{pair}{\to} \mathbb{N} \times \mathbb{N} \stackrel{f \times 1}{\to} I \times \mathbb{N} \cong \underset{i \in I}{\cup} \mathbb{N} \stackrel{\underset{i \in I}{\cup} f_i}{\to} \underset{i \in I}{\cup} S_i$$ 

where for $pair: \mathbb{N} \to \mathbb{N} \times \mathbb{N}$ we may take for example the function that is inverse to $(x, y) \mapsto \binom{x+y+1}{2} + y$. 

For [[constructive mathematics|constructive mathematicians]] who accept the [[axiom of countable choice]], the proof is only slightly more elaborate. Here we define a set to be *countable* if it is a [[quotient]] of (is enumerated by) a [[decidable subset]], i.e., a [[complemented subobject]] of $\mathbb{N}$. Thus, supposing we have chosen surjections out of decidable subsets $(f_i: J_i \to S_i)_{i \in I}$, and a surjection $J \to I$ out of a decidable subset $J$, we have a diagram (switching to $\sum$ to denote disjoint sums) 

$$\array{
 & & & & J \cdot \mathbb{N} & \hookrightarrow & \mathbb{N} \cdot \mathbb{N} \cong \mathbb{N} \times \mathbb{N} & \stackrel{pair^{-1}}{\to} & \mathbb{N} \\ 
 & & & & \downarrow \mathrlap{f \cdot \mathbb{N}} & & & & \\ 
\sum_{i \in I} J_i & \hookrightarrow & \sum_{i \in I} \mathbb{N} & \cong & I \cdot \mathbb{N} & & & & \\ 
\mathllap{\sum_{i \in I} f_i} \downarrow & & & & & & & & \\ 
\sum_{i \in I} S_i & & & & & & & & 
}$$

whose [[limit]] might be denoted $\sum_{j \in J} K_j$ where $K_j \coloneqq J_{f(j)}$. This is certainly a complemented subobject of $\mathbb{N}$, the complement being formed as $\left(\sum_{j \in J} \neg K_j\right) + (\neg J) \cdot \mathbb{N}$, and the limit obviously maps surjectively onto $\sum_{i \in I} S_i$, as desired. 
=--

The implication countable choice $\Rightarrow$ countable union theorem cannot be reversed, as there are models of [[ZF]] where the latter holds, but countable choice fails. Further, the countable union theorem implies countable choice for countable sets, but this implication also cannot be reversed.


## Related statements

* [[images of unions are unions of images]]

* [[pre-images preserve unions and intersections]]

## References

* ProofWiki, _[Countable Union of Countable Sets is Countable](https://proofwiki.org/wiki/Countable_Union_of_Countable_Sets_is_Countable)

* _Countable Unions And The Axiom Of Countable Choice_, [MathOverflow discussion](https://mathoverflow.net/questions/74743/countable-unions-and-the-axiom-of-countable-choice)

[[!redirects countable union of countable sets is countable]]
[[!redirects countable union theorem]]
[[!redirects countable union axiom]]