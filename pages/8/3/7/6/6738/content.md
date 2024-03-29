
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Well-quasi-orders
* table of contents
{: toc}

## Definition 

In [[classical mathematics]], a __well-quasi-order__ is a [[preorder]] $(P, \leq)$ such that for any infinite sequence $x_i$ in $P$, there exist $i, j$ with $i \lt j$ and $x_i \leq x_j$. Another way of expressing this condition is: 

* There are no infinite [[antichain|antichains]] in $P$: if $x_i$ is a sequence in $P$, then there exist some pair of elements $x_i$, $x_j$ that are comparable, i.e., either $x_i \leq x_j$ or $x_j \leq x_i$, and 

* There is no strictly decreasing sequence in $P$: if $x_0 \geq x_1 \geq \ldots$ in $P$, then there exists $n$ such that $x_i \leq x_{i+1}$ for all $i \geq n$. 

One motivation for this notion is given by the following theorem: 

+-- {: .un_thm} 
###### Theorem 
Let $(X, \leq)$ be a quasi-order (i.e., a [[preorder]]). Define a [[partial order]] on the [[power set]] $P(X)$ by $A \leq^+ B$ if $\forall_{a\colon A} \exists_{b\colon B} (a \leq b)$. Then $\leq^+$ is a [[well-founded relation]] if and only if $\leq$ is a well-quasi-ordering. 
=-- 


## Example 

The collection of [[graph|finite simple graphs]] is well-quasi-ordered by the [[graph minor]] relation. This is the celebrated _Robertson-Seymour Graph Minor Theorem_. 

## Related entries

* [[well-order]]

## References 

* [Wikipedia article](http://en.wikipedia.org/wiki/Well-quasi-ordering) 


[[!redirects well-quasi-order]]
[[!redirects well-quasi-orders]]
[[!redirects well-quasiorder]]
[[!redirects well-quasiorders]]
[[!redirects well quasiorder]]
[[!redirects well quasiorders]]
[[!redirects well-quasi-ordering]]
[[!redirects well-quasi-orderings]]
[[!redirects well-quasiordering]]
[[!redirects well-quasiorderings]]
[[!redirects well quasiordering]]
[[!redirects well quasiorderings]]

[[!redirects well-preorder]]
[[!redirects well-preorders]]
[[!redirects well preorder]]
[[!redirects well preorders]]

[[!redirects well-quasi-ordered set]]
[[!redirects well-quasi-ordered sets]]
[[!redirects well-quasiordered set]]
[[!redirects well-quasiordered sets]]
[[!redirects well quasiordered set]]
[[!redirects well quasiordered sets]]

[[!redirects well-preorderered set]]
[[!redirects well-preorderered sets]]
[[!redirects well preorderered set]]
[[!redirects well preorderered sets]]
