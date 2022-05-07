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

## Without the axiom of choice

However, it is possible to recover some of König's theorem in the absence of the axiom of choice. For sets $A$, $B$, define $(A \nsucceq B)$ to be the set of assignments $f \mapsto n(f)$ which for each partial function $f:A \rightharpoonup B$ specify an element $n(f) \in B \setminus im(f)$. This set being nonempty imiplies a strong form of "there are no partial surjections $A \twoheadrightarrow B$" (aka $A \ngeq^* B$), and the definition is as one might define $A \ngeq^* B$ using [[propositions as types]]. Conversely, if AC holds, then the $(A \nsucceq B)$ is nonempty iff $A \lt B$.

+-- {: .num_theorem} 
###### Proposition 
Given $n_i \in (A_i \nsucceq B_i)$ for each $i \in I$, then $\sum_i A_i \nsucceq \prod_i B_i$. 
=-- 

+-- {: .proof} 
###### Proof
Let $f: \sum_i A_i \rightharpoonup \prod_i B_i$. We define a member $m(f) \in \prod_i B_i$ as 
$m(f)(i) = n_i(a \mapsto f(i,a)(i))$.
Now, note that it can't be the case that $m(f) = f(i,a)$ for any $i \in I$, $a \in A_i$, as then $f(i,a)(i) = m(f)(i) = n_i(a \mapsto f(i,a)(i)) \notin im(a \mapsto f(i,a)(i))$. This means that $m(f) \in \prod_i B_i \setminus \operatorname{im}(f)$, as required.
=--

Although the preconditions of the theorem are harder to attain, as $(A \nsucceq B)$ is nonempty much less often than $A \lt B$, it still holds in several useful cases:

+-- {: .num_theorem} 
###### Proposition 
The following conditions are each sufficient to construct an element $n$ of $A \nsucceq B$:

1. $m \in (A \nsucceq B')$ and an injection $i:B' \hookrightarrow B$

2. $m \in (A' \nsucceq B)$ and an injection $i:A \hookrightarrow A'$

3. $B = \mathcal{P}(A)$

4. $B$ has a wellorder $\lt$, and there is no partial surjection $A \to B$

5. An element $b \in B$ and, for each total function $f:A \to B$, a specified $m(f) \in B \setminus im(f)$

=-- 

+-- {: .proof} 
###### Proof
1. For $f:A \rightharpoonup B$, $f$ restricts to a partial function $f':A \rightharpoonup B'$ ($f'(a) = b$ iff $f(a) = i(b)$), and $m(f')$ gives an element of $B'\setminus im(f')$, so taking $n(f') = i(m(f'))$ gives $n(f') = i(m(f')) \in B \setminus im(f)$

2. For $f:A \rightharpoonup B$, $f$ extends to a partial function $f':A' \rightharpoonup B$ (defined as $f'(i(a)) = f(a)$), and $m(f') \in B \setminus im(f) = B \setminus im(f')$, so take $n(f) = m(f')$.

3. Immediate from $1 \nsucceq 2$ and the above choiceless variant of K&#246;nig's theorem, but can also be proven directly. Let $f:A \rightharpoonup \mathcal{P}(A)$ be a partial function, and let $n(f) = \{a \in A \mid a \in dom(f) and a \notin f(a)\}$. Then if $f(a) = n(f)$, we have that $a \in n(f)$ iff $a \in dom(f) and a \notin f(a)$, so $a \notin dom(f)$, contradicting $f(a) = n(f)$. Therefore, $n(f) \in \mathcal{P}(A) \setminus im(f)$.

4. For $f:A \rightharpoonup B$, let $n(f) = min \{ \alpha \in B \mid \alpha \notin im(f) \}$. Then $n(f)$ is uniquely defined as $B$ is wellordered and the set is nonempty (otherwise f is a partial surjection), and $n(f) \in B \setminus im(f)$.

5. For $f:A \rightharpoonup B$, extend it to a total function $f':A \to B$ by letting $f'(x) = f(x)$ where defined and $f'(x) = b$ otherwise. Then $m(f') \in B \setminus im(f') \subseteq B \setminus im(f)$, so let $n(f) = m(f')$.

=--
