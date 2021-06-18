In [[set theory]], K&#246;nig's theorem, due to Julius K&#246;nig (Hungarian: Gyula K&#337;nig), is a basic result in [[cardinal]] arithmetic. It uses the [[axiom of choice]]. It is not to be confused however with [[König's lemma]], another result of combinatorial set theory, but using instead the axiom of [[dependent choice]] (and due to the son, D&#233;nes K&#337;nig). 

+-- {: .num_theorem} 
###### Theorem 
**(K&#246;nig)** 
Let ${|X|}$ be the cardinality of a set $X$. If ${|A_i|} \lt {|B_i|}$ for all $i \in I$, then ${|\sum_i A_i|} \lt {|\prod_i B_i|}$. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose we have _proper_ inclusions $f_j: A_j \hookrightarrow B_j$. Choose basepoints $x_j \in B_j \setminus A_j$ and, letting $\prod_i B_i \stackrel{\pi_j}{\to} B_j$ be the product projection and $A_j \stackrel{i_j}{\to} \sum_i A_i$ the coproduct inclusion, define a map $f: \sum_j A_j \to \prod_j B_j$: 

$$\array{
(\pi_j \circ f \circ i_k)(a) & = & f_j(a) & \; if \; a \in A_k \; and \; j = k \\ 
 & = & x_j & \; if \; a \in A_k \; and \; j \neq k
}$$ 

It is immediate that this $f$ is injective, and so ${|\sum_i A_i|} \leq {|\prod_i B_i|}$. 

Now we prove the last inequality is strict. Suppose to the contrary that there exists a surjective function $f: \sum_i A_i \to \prod_i B_i$. The function $f_j = \pi_j \circ f \circ i_j: A_j \to B_j$ is not surjective, by the hypothesis ${|A_j|} \lt {|B_j|}$. Thus for each $j \in I$ we may choose $b_j \in B_j$ such that $b_j \notin Im(f_j)$. By supposition, there exists $a \in \sum_i A_i$ such that $f(a) = (b_j)_{j \in I}$. But $a \in A_j$ for some $j \in I$, whence $\pi_j f(a) = f_j(a)$, i.e., $b_j = f_j(a)$, and this contradicts how we chose $b_j$. 
=-- 

One can see immediately how the axiom of choice enters the result: the product $\prod_i B_i$ might be empty otherwise, hence could not satisfy the required inequality. In fact one can _prove_ the axiom of choice from K&#246;nig's theorem, in the form of "every product of a family of inhabited sets is inhabited", by taking $A_i$ to be empty for each $i$.

The following important corollary deserves to be called _K&#246;nig's corollary_, since it is itself often referred to in the literature, but only ever as a follow-on from the above theorem. Note that we do not need to appeal to the full strength of K&#246;nig's theorem to prove this corollary.

+-- {: .num_cor} 
###### Corollary 
For any infinite cardinal $\kappa$, the cardinal $2^\kappa$ has [[cofinality]] greater than $\kappa$. 
=-- 

+-- {: .proof} 
###### Proof 
We have $2^\kappa = 2^{\kappa \times \kappa} = (2^\kappa)^\kappa$. If $(\lambda_\alpha)_{\alpha \lt \kappa}$ is an increasing sequence with least upper bound $2^\kappa$, then we have surjection $\sum_{\alpha \lt \kappa} \lambda_\alpha \to 2^\kappa = (2^\kappa)^\kappa$ which immediately contradicts K&#246;nig's theorem. 
=-- 

The appeal to the axiom of choice _in the form discussed above_ is unnecessary, since $2^\kappa = \prod_{i\in \kappa} 2$ is obviously inhabited. However, there are other ways in which choice-specific features make themselves known, for instance $2^\kappa$ is a cardinal (i.e. has a well-ordering). And the statement that every infinite cardinal $\kappa$ satisfies $\kappa \simeq \kappa \times \kappa$ is equivalent to the axiom of choice. And lastly, the definition of cofinality is very difficult in the absence of AC, see for instance [this blog post by Karagila](http://karagila.org/2015/cofinality-and-the-axiom-of-choice/).

[[!redirects König’s theorem]]
[[!redirects Konig's theorem]]
