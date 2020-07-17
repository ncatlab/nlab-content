
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[computer science]], a [[data type]] is often defined by an [[isomorphism]] of types $X\cong D(X)$ for some construction $D$. For a simple example, the [[natural numbers]] are defined by $N\cong N+1$. However, in a language with general recursion (including [[partial recursive functions]]), the data types have properties as well as the usual inductive ones. For example, in a lazy language such as [[Haskell]], there is an infinity element in $N$, which is a fixed point for successor. 

In general, it is common to allow the construction $D$ to be mixed-variance. For example, $X\cong (X\to X)$ is a recursive data type whose inhabitants are expressions of the [[lambda-calculus#pure_lambda_calculus|untyped lambda calculus]]. Thus recursive data types are a generalization of [[reflexive object|reflexive objects]]. On the semantic side, recursive data types are sometimes called "recursive domain equations".  


## Definition

+-- {: .num_defn}
###### Definition

A [[category]] $C$ is _algebraically complete_ if every [[endofunctor]] $F$ has an [[initial algebra of an endofunctor|initial algebra]] $F(A)\to A$ and a [[final coalgebra]] $Z\to F(Z)$.

By [[initial algebra of an endofunctor#LambeksTheorem|Lambek's lemma]], the initial algebra is an [[isomorphism]], and so is the final coalgebra, thus they can be regarded as [[coalgebra for an endofunctor|coalgebras]] and [[algebra for an endofunctor|algebras]] respectively. This gives rise to a canonical morphism from the initial algebra to the final coalgebra, $A\to Z$. 

An algebraically complete category $C$ is _algebraically compact_ if this canonical morphism from the initial algebra to the final coalgebra is an [[isomorphism]].
=--

+-- {: .num_remark}
###### Remark

In [[classical mathematics|classical]] [[set theory]], very few categories are algebraically compact. Thus it is common to restrict attention to certain endofunctors. 
One might then say that this class of endofunctors is algebraically compact. 
=--

## Mixed variance domain equations and minimal invariance

Let $D:C^{op}\times C\to C$ be a [[bifunctor]]. A _solution_ for $D$ is an object $X$ together with an isomorphism 

$$X \cong D(X,X)$$ 

In general there may be many solutions. One approach to finding a canonical one is in terms of _minimal invariance_.

An [[idempotent]] $e:X\to X$ is said to be _invariant_ for a solution $a:X\to D(X,X)$ if 
$$
  \array{& X & \overset{e}\rightarrow & X & \\
          a & \downarrow &&\downarrow & a\\
          &D(X,X) & \underset{D(e,e)}\rightarrow& D(X,X) & \\
}$$
Notice that any [[split idempotent|splitting]] of this idempotent is again a solution. 
A _minimal invariant_ solution is one for which there are no non-trivial invariant idempotents. 


+-- {: .num_proposition}
###### Proposition  ([Freyd](#Freyd))

If $C$ and $D$ are algebraically compact, so is $C\times D$. If $C$ is algebraically compact, so is the dual category $C^{op}$. 
=--

As a result of this proposition, we solve a mixed-variance domain equation 
$X \cong D(X,X)$ 
for $D:C^{op}\times C\to C$ on an algebraically compact category
by considering the initial algebra / final coalgebra of the endofunctor $\bar{T}:C^{op}\times C\to C^{op}\times C$ 
given by $\bar{T}(X,Y)=(T(Y,X),T(X,Y))$. 

In an algebraically compact category, this solution from the initial algebra / final coalgebra is minimal invariant, by the universal property. 

## References

The notion is due to:

* [[Peter Freyd]], _Algebraically complete categories_, Category Theory in Como, 1990 ([dpi:10.1007/BFb0084215](https://doi.org/10.1007/BFb0084215)){#Freyd}

Barr proposed to look at certain functors as algebraically compact, and gave basic facts about building algebraically compact functors and numerous examples. 

* [[Michael Barr]], _Algebraically compact functors_, Journal of Pure and Applied Algebra Volume 82, Issue 3, 26 October 1992, Pages 211-231 (<a href="https://doi.org/10.1016/0022-4049(92)90169-G">doi:10.1016/0022-4049(92)90169-G</a>)

Pitts gives a survey and discussion, together with further reasoning principles.

* [[Andrew Pitts]], _Relational properties of domains_, Information and Computation, 1996. [pdf](https://www.cl.cam.ac.uk/~amp12/papers/relpod/relpod.pdf). 
