
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

In [[computer science]], a [[data type]] is often defined by an [[isomorphism]] of types $X\cong T(X)$ for some construction $T$. For a simple example, the [[natural numbers]] are defined by $N\cong N+1$. However, in a language with general recursion (including [[partial recursive functions]]), the data types have properties in addition to as the usual inductive ones, which allow [[coinduction|coinductive]] reasoning. For example, in a lazy language such as [[Haskell]], there is an infinity element in $N$, which is a fixed point for successor. 

In general, it is common to allow the construction $T$ to be mixed-variance. For example, $X\cong (X\to X)$ is a recursive data type whose inhabitants are expressions of the [[lambda-calculus#pure_lambda_calculus|untyped lambda calculus]]. Thus recursive data types are a generalization of [[reflexive object|reflexive objects]]. On the semantic side, recursive data types are sometimes called "recursive domain equations".  


## Definition

+-- {: .num_defn}
###### Definition

A [[category]] is _algebraically complete_ if every [[endofunctor]] $F$ has an [[initial algebra of an endofunctor|initial algebra]] $F(A)\to A$. A category is _algebraically cocomplete_ if every endofunctor $F$ has a [[final coalgebra]] $Z\to F(Z)$.

By [[initial algebra of an endofunctor#LambeksTheorem|Lambek's lemma]], an initial algebra is an [[isomorphism]], and so is a final coalgebra, thus they can be regarded as [[coalgebra for an endofunctor|coalgebras]] and [[algebra for an endofunctor|algebras]] respectively. This gives rise to a canonical morphism from the initial algebra to the final coalgebra, $A\to Z$. 

An algebraically complete and cocomplete category $C$ is _algebraically compact_ if this canonical morphism from the initial algebra to the final coalgebra is an [[isomorphism]].
=--

+-- {: .num_remark}
###### Remark

In [[classical mathematics|classical]] [[set theory]], very few categories are algebraically compact. Thus it is common to restrict attention to certain endofunctors.
One might then say that this class of endofunctors is algebraically compact. 
A leading example is where $C$ is $V$-[[enriched category|enriched]], in which case we might restrict attention to $V$-endofunctors. For example, the $\mathbf{cpo}$-enriched category of pointed [[cpo]]'s and strict maps is $\mathbf{cpo}$-algebraically compact.
=--

## Mixed variance domain equations and minimal solutions

Let $T:C^{op}\times C\to C$ be a [[bifunctor]]. A _solution_ for $T$ is an object $X$ together with an isomorphism 

$$a:X \cong T(X,X)$$ 

In general there may be many solutions. One approach to comparing them is via retractions. If an object $Y$ is a [[retract]] of $X$, and $Y$ forms a solution $b:Y\cong T(Y,Y)$, then we can ask that the retraction respects the solution, i.e.
$$
  \array{& Y & \overset{i}\rightarrow & X & \\
          b & \downarrow &&\downarrow & a&\\
          &T(Y,Y) & \underset{T(r,i)}\rightarrow& T(X,X) & \\
}
\quad and \quad
  \array{& X & \overset{r}\rightarrow & Y & \\
          a & \downarrow &&\downarrow & b&\\
          &T(X,X) & \underset{T(i,r)}\rightarrow& T(Y,Y) & \\
}
$$


+-- {: .num_proposition}
###### Proposition  ([Freyd](#Freyd))

If $C$ and $D$ are algebraically compact, so is $C\times D$. If $C$ is algebraically compact, so is the dual category $C^{op}$. 
=--

As a result of this proposition, we solve a mixed-variance domain equation 
$X \cong T(X,X)$ 
for $T:C^{op}\times C\to C$ on an algebraically compact category
by considering the initial algebra / final coalgebra of the endofunctor $\bar{T}:C^{op}\times C\to C^{op}\times C$ 
given by $\bar{T}(X,Y)=(T(Y,X),T(X,Y))$. 

+-- {: .num_proposition}
###### Proposition ([Freyd](#Freyd), [Fiore](#fiore))

For a bifunctor $T:C^{op}\times C\to C$ on an algebraically compact category, the solution from the initial algebra / final coalgebra is minimal in the sense that it is uniquely a retract of every solution. 
=--

## References

The notion is due to:

* [[Peter Freyd]], _Algebraically complete categories_, Category Theory in Como, 1990 ([dpi:10.1007/BFb0084215](https://doi.org/10.1007/BFb0084215)){#Freyd}

Barr proposed to look at certain functors as algebraically compact, and gave basic facts about building algebraically compact functors and numerous examples. Fiore and Plotkin looked enriched functors and proved "adequacy" results about data types in programming languages.

* [[Michael Barr]], _Algebraically compact functors_, Journal of Pure and Applied Algebra Volume 82, Issue 3, 26 October 1992, Pages 211-231 (<a href="https://doi.org/10.1016/0022-4049(92)90169-G">doi:10.1016/0022-4049(92)90169-G</a>)

* [[Marcelo Fiore]]. _Axiomatic domain theory in categories of partial maps_. CUP 1996. {#fiore}

* [[Marcelo Fiore]] and [[Gordon Plotkin]]. _An axiomatization of computationally adequate domain theoretic models of FPC_. In Proc. LICS, 1994. [pdf](http://homepages.inf.ed.ac.uk/gdp/publications/Ax_FPC.pdf).

Pitts gives a survey and discussion, together with further reasoning principles.

* [[Andrew Pitts]], _Relational properties of domains_, Information and Computation, 1996. [pdf](https://www.cl.cam.ac.uk/~amp12/papers/relpod/relpod.pdf). 
