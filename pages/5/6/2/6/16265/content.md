In [[set theory]], K&#246;nig's theorem, due to Julius K&#246;nig (Hungarian: Gyula K&#337;nig), is a basic result in [[cardinal]] arithmetic. It uses the [[axiom of choice]]. It is not to be confused however with [[König's lemma]], another result of combinatorial set theory, but using instead the axiom of [[dependent choice]] (and due to the son, D&#233;nes K&#337;nig). 

+-- {: .num_theorem} 
###### Theorem 
**(K&#246;nig)** 
Let ${|X|}$ be the cardinality of a set $X$. If ${|A_i|} \lt {|B_i|}$ for all $i \in I$, then ${|\sum_i A_i|} \lt {|\prod_i B_i|}$. 
=-- 

+-- {: .proof} 
###### Proof 
Given *proper* inclusions $A_i \hookrightarrow B_i$ (which in particular forces every $B_i$ to be [[inhabited set|inhabited]]), we may easily prove ${|\sum_i A_i|} \leq {|\prod_i B_i|}$; we wish to show the inequality is strict. Suppose to the contrary that there exists a surjective function $f: \sum_i A_i \to \prod_i B_i$. The function $f_j: A_j \to B_j$ formed as the composite 

$$A_j \stackrel{i_j}{\hookrightarrow} \sum_i A_i \stackrel{f}{\to} \prod_i B_i \stackrel{\pi_j}{\to} B_j$$ 

is not surjective, by the hypothesis ${|A_j|} \lt {|B_j|}$. Thus for each $j \in I$ we may choose $b_j \in B_j$ such that $b_j \notin Im(f_j)$. By supposition, there exists $a \in \sum_i A_i$ such that $f(a) = (b_j)_{j \in I}$. But $a \in A_j$ for some $j \in I$, whence $\pi_j f(a) = f_j(a)$, i.e., $b_j = f_j(a)$, and this contradicts how we chose $b_j$. 
=-- 

+-- {: .num_cor} 
###### Corollary 
For any infinite cardinal $\kappa$, the cardinal $2^\kappa$ has cofinality greater than $\kappa$. 
=-- 

+-- {: .proof} 
###### Proof 
We have $2^\kappa \leq \kappa^\kappa$ and $\kappa^\kappa \leq 2^{\kappa \times \kappa} = 2^\kappa$, so $2^\kappa = \kappa^\kappa$. If $(\lambda_\alpha)_{\alpha \lt \kappa}$ is an increasing sequence with least upper bound $\kappa^\kappa$, then we have surjection $\sum_{\alpha \lt \kappa} \lambda_\alpha \to \kappa^\kappa$ which immediately contradicts K&#246;nig's theorem. 
=-- 
