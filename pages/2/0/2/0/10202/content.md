
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Deduction and induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea 

A **partial recursive function** (often "[[computable function]]", but see there for disambiguation) is a [[partial function]] of [[natural numbers]] which can be [[definition|defined]] by an [[algorithm]] or computer [[program]] (e.g., a [[Turing machine]]), taking finitely many [[natural numbers]] as inputs, and which on input may run forever, but otherwise eventually halts and returns a natural number as output. 

This idea as described is vague until it is circumscribed by a specific notion of computer program (Turing machines, register machines, abaci, etc.). There is a standard article of faith called the "[[Church-Turing thesis]]", identifying functions on natural numbers that are algorithmically computable with those that are computable using a Turing machine (or some variant class of machines that is Turing-complete). 

A purely mathematical definition of the intended class of functions is given below. 


## Definition 

+-- {: .num_defn #recursive} 
###### Definition 
A _partial recursive function_ is a [[partial function]] from $\mathbb{N}^k$ to $\mathbb{N}$ (where $\mathbb{N}$ is the [[set]] of [[natural numbers]] and $k \geq 0$ is finite) that belongs to the smallest [[class]] $\mathcal{C}$ of partial functions that 

* includes all [[constant functions]] $1 \to \mathbb{N}$; 

* includes all [[projection]] maps $\pi_i: \mathbb{N}^k \to \mathbb{N}$, $i = 1, \ldots, k$; 

* includes the successor function $s: \mathbb{N} \to \mathbb{N}$; 

* is closed under [[composition]]: if $f_1: \mathbb{N}^{k} \to \mathbb{N}, \ldots, f_n: \mathbb{N}^{k} \to \mathbb{N}$ and $g: \mathbb{N}^n \to \mathbb{N}$ belong to $\mathcal{C}$, then so does $g \circ (f_1, \ldots, f_n): \mathbb{N}^{k} \to \mathbb{N}$; 

* is closed under primitive [[recursion]]: if $g: \mathbb{N}^k \to \mathbb{N}$ and $h: \mathbb{N}^{k+2} \to \mathbb{N}$ belong to $\mathcal{C}$, then the function $f: \mathbb{N}^{k+1} \to \mathbb{N}$ defined recursively by the equations (for $y \in \mathbb{N}$ and $\mathbf{x} \in \mathbb{N}^k$) 
$$f(0, \mathbf{x}) = g(\mathbf{x})$$ 
$$\,$$
$$f(y+1, \mathbf{x}) = h(y, f(y, \mathbf{x}), \mathbf{x})$$ 
also belongs to $\mathcal{C}$; 

* is closed under minimization: given any _[[total function|total]]_ function $f: \mathbb{N}^{k+1} \to \mathbb{N}$ belonging to $\mathcal{C}$, the partial function $g: \mathbb{N}^k \to \mathbb{N}$, defined by $g(\mathbf{x}) = c$ iff $f(c, \mathbf{x}) = 0$ and $f(d, \mathbf{x}) \gt 0$ whenever $0 \leq d \leq c-1$, also belongs to $\mathcal{C}$. 
=-- 


+-- {: .num_defn} 
###### Definition 
A _primitive recursive function_ is a function that belongs to the smallest class of functions of the form $\mathbb{N}^k \to \mathbb{N}$ that contains constants, projection maps, the successor map, is closed under composition, and is closed under primitive recursion. 
=-- 

Clearly the primitive recursive functions are a subclass of partial recursive functions. Notice that primitive recursive functions are not merely partial functions, but actual (*total*) functions. 

+-- {: .num_remark #Lawvere} 
###### Remark 
Both the class of partial recursive functions and the class of primitive recursive functions yield [[Lawvere theories]] $Th(Comp)$ and $Th(PrimRec)$, where a morphism $k \to 1$ of the Lawvere theory is a function $\mathbb{N}^k \to \mathbb{N}^1$ belonging to the class. It is straightforward to check that in either case, the generating object $1$ of the Lawvere theory (or $\mathbb{N}$ if you prefer) is a parametrized [[natural numbers object|NNO]] in that category: this is the essence of primitive recursion. 
=-- 

+-- {: .num_defn} 
###### Definition 
A _recursive relation_ (or what is more usual nowadays, a *computable relation*) is a subset of $\mathbb{N}^k$ whose characteristic function $\chi: \mathbb{N}^k \to \{0, 1\}$ is recursive. Similarly, a primitive recursive relation is a relation whose characteristic function is primitive recursive. 
=-- 


## Properties

We may build up a stock of functions and relations that are primitive recursive as follows. (All closure properties mentioned will clearly also apply to partial recursive functions and relations.) 

1. Addition, multiplication, and exponentiation on $\mathbb{N}$. The factorial function $n \mapsto n!$ is primitive recursive. Binomial coefficients. 

1. The predecessor function $Pred: \mathbb{N} \to \mathbb{N}$, defined by the recursion $Pred(0) = 0$, $Pred(n+1) = n$. 

1. *Truncated subtraction*, where $x \stackrel{\cdot}{-} y = x - y$ if $x \geq y$, else $0$, is primitive recursive. It is defined by the recursion $x \stackrel{\cdot}{-} 0 = x$, $x \stackrel{\cdot}{-} (y+1) = Pred(x \stackrel{\cdot}{-} y)$. 

1. The distance function ${|x-y|} = (x \stackrel{\cdot}{-} y) + (y \stackrel{\cdot}{-} x)$. The function $\alpha(x) = 1 \stackrel{\cdot}{-} x$; this is the characteristic function of the unary relation or predicate "equals zero". So "equals zero" is a computable relation. So is "doesn't equal zero", since this has characteristic function $\alpha(\alpha(x))$. 

1. Therefore the equality relation ${|x-y|} = 0$ is a primitive recursive relation. So is $x \lt y$, being the relation "$y \stackrel{\cdot}{-} x$ doesn't equal zero". If $f$ is a (primitive) recursive function, then its graph defined by the relation $y = f(x)$ is a (primitive) recursive relation. 

1. (Boolean combinations) Similarly, if $R$ is a primitive recursive relation (so that its characteristic function $\chi_R$ is primitive recursive), then so is its negation $\neg R$, since $\chi_{\neg R} = \alpha(\chi_R)$. If $P$, $Q$ are primitive recursive relations, so is $P \wedge Q$, since $\chi_{P \wedge Q} = \chi_P \cdot \chi_Q$. Hence Boolean combinations of primitive recursive relations are primitive recursive. 

1. If $f(x, y, \mathbf{z})$ and $h(y)$ are primitive recursive, so is 
$$g(y, \mathbf{z}) \coloneqq \sum_{x=0}^{h(y)} f(x, y, \mathbf{z})$$ 
and similarly with the sum replaced by a product. It follows that primitive recursive predicates are closed under _bounded quantification_; e.g., if $R(x, y, \mathbf{z})$ is a primitive recursive predicate and $h$ is a primitive recursive function, then the predicate $Q$ defined by  
$$Q(y, \mathbf{z}) = \forall_{0 \leq x \lt y} R(x, y, \mathbf{z}) \coloneqq \bigwedge_{x=0}^{y-1} R(x, y, \mathbf{z})$$ 
is primitive recursive since $\chi_Q(y, \mathbf{z}) = \prod_{x=0}^{y-1} \chi_R(x, y, \mathbf{z})$. 

1. (Bounded least choice operator) If $R(x, y, \mathbf{z})$ is a primitive recursive relation and $h$ is a primitive recursive function, then the function $f(y, \mathbf{z})$ defined to be "the least $x \leq h(y)$ such that $R(x, y, \mathbf{z})$ if such $x$ exists, else $y$" is primitive recursive. Indeed, 
$$f(y, \mathbf{z}) = [\sum_{x=0}^{h(y)} (x \cdot \chi_R(x, y, \mathbf{z}) \cdot (\prod_{w=0}^{x-1} \chi_{\neg R}(w, y, \mathbf{z}))] + y \cdot \prod_{x=0}^{h(y)} \chi_{\neg R}(x, y, \mathbf{z}).$$ 

1. (Pairing and unpairing) There is an isomorphism $\mathbb{N}^2 \to \mathbb{N}$ in the Lawvere theory $Th(PrimRec)$, i.e., there is a primitive recursive function $f: \mathbb{N}^2 \to \mathbb{N}$ with a primitive recursive inverse $g: \mathbb{N} \to \mathbb{N}^2$. For example, take $f$ to be the function 
$$f: (m, n) \mapsto \binom{m+n+1}{2} + n$$ 
Its inverse $g$ takes $m$ to the pair 
$$(a \stackrel{\cdot}{-} (m - \binom{a \stackrel{\cdot}{-} 1}{2}+2), m - \binom{a \stackrel{\cdot}{-} 1}{2})$$ 
where $a$ is the least element less than $m+2$ such that $\binom{a}{2} \gt m$. By the aforementioned properties, this $g$ is manifestly primitive recursive. 

As a consequence of this last property, there exist primitive recursive [[isomorphisms]] between $\mathbb{N}$ and $\mathbb{N}^k$ for any $k \gt 0$. Since partial/primitive recursive functions are closed under composition, it is sufficient (and sometimes convenient) to consider only partial/primitive recursive functions on $\mathbb{N}$ itself.  (The exception is the case $k = 0$, but this is trivial, since every partial function $1 \to \mathbb{N}$ is recursive.) 

+-- {: .num_remark} 
###### Remark 
To show that $\mathbb{N}^2 \cong \mathbb{N}$ in the category of primitive recursive functions, it is not enough just to exhibit a primitive recursive bijection $f: \mathbb{N}^2 \to \mathbb{N}$, because it is not true that every primitive recursive bijection possesses a primitive recursive inverse. In other words, it is not true that the forgetful functor $Th(PrimRec) \to Set$ (see Remark \ref{Lawvere}) reflects isomorphisms. See Example \ref{inverse} below. 
=-- 

+-- {: .num_remark} 
###### Remark 
Similarly, it is not always true that if a graph of a function is a primitive recursive relation, then the function itself is primitive recursive. (For example, the graph of the Ackermann function, discussed below, is a primitive recursive relation.) However, we do have a sample theorem as follows. 
=-- 

+-- {: .num_theorem #bound} 
###### Theorem 
If a graph of a function $f$ is a primitive recursive relation, and if $f \leq g$ for some primitive recursive $g$, then $f$ is itself primitive recursive. 
=-- 

The proof can be roughly expressed as follows: if $R(x, y)$ is the functional computable relation, then let $f(x)$ be the least $y \leq g(x)$ such that $R(x, y)$. The bounded least choice property shows that $f(x)$ is primitive recursive. 

The point hovering in the background is that there are some computable functions which grow faster (in fact, much much much faster) than any primitive recursive function. This underscores the important role of the minimization axiom for partial recursive functions, which allows unboundedly large searches to take place. Indeed, we have the following crucial fact: 

+-- {: .num_theorem #graph} 
###### Theorem 
If $R \subseteq{N}^2$ is a graph of a function $f$ and is a recursive relation, then $f$ is a (total) recursive function. (The converse holds by one of the properties listed above.) 
=-- 

+-- {: .proof} 
###### Proof 
According to the minimization axiom in Definition \ref{recursive}, given that $\chi_R: \mathbb{N}^2 \to \{0, 1\}$ is a recursive function, the function that takes $x$ to the least $y \in \mathbb{N}$ such that $1 - \chi_R(x, y) = 0$ is also recursive. But this function is simply $f$. This completes the proof. 
=-- 

+-- {: .num_corollary} 
###### Corollary 
The inverse of a recursive bijection $f$ is also recursive. 
=-- 

+-- {: .proof} 
###### Proof 
The graph of $f$ is a recursive relation, and so is the opposite graph, which is the graph of the function $f^{-1}$. Apply the preceding theorem. 
=-- 

Before passing on to general recursive functions, it is good to have some idea of the scope of primitive recursive functions. Some examples: 

* The function $f(n) = p_n$, the $n^{th}$ prime, is primitive recursive. 


## The Ackermann function 

+-- {: .num_defn} 
###### Definition 
For each $n$, we define a function $A_n: \mathbb{N} \to \mathbb{N}$ by 

* $A_0(m) = 2 m$; 

* $A_{n+1}(m) = (A_n)^m(1)$ 

where $f^m$ denotes the composition of $m$ copies of $f$. The **Ackermann function** $A: \mathbb{N} \to \mathbb{N}$ is defined by $A(m) = A_m(m)$. 
=-- 

(The function is named after [[Wilhelm Ackermann]]. There are several variations of this function around, and one common version actually puts $A_0(m)=m+1$ and $A_{n+1}(m)=(A_n)^m(f(1))$.)

We show that while each $A_n$ is primitive recursive, the function $A$ grows faster than any primitive recursive function on $\mathbb{N}$, hence is not itself primitive recursive. It does however belong to the class of partial recursive functions. 

By property 1 above, $A_0$ is primitive recursive. Supposing that $A_n$ is primitive recursive, $\phi = A_{n+1}$ is also primitive recursive because it satisfies the recursion $\phi(0) = 1$, $\phi(m+1) = A_n (\phi(m))$. 

By induction one may easily show $A_n(1) = 2$ for all $n$ and $A_n(2) = 4$ for all $n$. We have $A_{n+1}(3) = A_n(A_n(A_n(1))) = A_n(A_n(2)) = A_n(4)$ for all $n$. The function $A_1$ gives $n^{th}$ powers of $2$, the function $A_2$ gives tetrations (iterated exponentials stacked $n$ high) of $2$, the function $A_3$ gives iterated tetrations, and so on. 

Some routine inductions establish the following facts: 

* For all $n$, the function $A_n$ is strictly increasing, and with the sole exception of $A_0(0) = 0$, we have $m \lt A_n(m)$ for all $m$, i.e. $A_n$ is strictly inflationary in arguments $m \gt 0$. We also have $n \lt A_n(3)$ for all $n$. 

+-- {: .num_lemma} 
###### Lemma 
If $f: \mathbb{N}^k \to \mathbb{N}$ is primitive recursive, then there exists $n$ such that $f(x_1, \ldots, x_k) \leq A_n(\max \{3, x_1, \ldots, x_k\})$ for all $x_1, \ldots, x_k$. (We say $f$ is **dominated** by $A_n$, for short.) 
=-- 

+-- {: .proof} 
###### Proof 
In the case where $f$ is constant with value $m$, take $n=m$. For $f$ the successor, use $n = 0$. For each projection $\pi_i: \mathbb{N}^k \to \mathbb{N}$, again use $n = 0$: 

$$x_i = \pi_i(x_1, \ldots, x_k) \leq A_0(\max \{3, x_1, \ldots, x_k\}).$$ 

Now proceed by induction on the construction of primitive recursive functions. Given that $f: \mathbb{N}^k$ is dominated by $A_n$ and $g_1, \ldots, g_k: \mathbb{N}^m \to \mathbb{N}$ are dominated by $A_{n+1}$, we calculate that $h = f \circ (g_1, \ldots, g_k): \mathbb{N}^m \to \mathbb{N}$ is dominated by $A_{n+2}$: 

$$\array{
h(x_1, \ldots, x_m) & = & f(g_1(x_1, \ldots, x_m), \ldots, g_k(x_1, \ldots, x_m)) \\ 
 & \leq & A_n(\max \{3, g_1(x_1, \dots, x_m), \ldots, g_k(x_1, \ldots, x_m)\}) \\ 
 & \leq & A_n(A_{n+1}(\max\{3, x_1, \ldots, x_m\})) \\ 
 & = & A_{n+1}(\max\{3, x_1, \ldots, x_m\} + 1) \\ 
 & \leq & A_{n+2}(\max\{3, x_1, \ldots, x_m\}). 
}$$ 

And given that $g: \mathbb{N}^k \to \mathbb{N}$ is dominated by $A_{n+1}$ and $h: \mathbb{N}^{k+2} \to \mathbb{N}$ is dominated by $A_n$, if we define $f: \mathbb{N}^{k+1} \to \mathbb{N}$ by recursion by $f(0, x_1, \ldots, x_k) = g(x_1, \ldots, x_k)$ and $f(y+1, x_1, \ldots, x_k) = h(y, f(y, x_1, \ldots, x_k), x_1, \ldots, x_k)$, we calculate that $f$ is dominated by $A_{n+3}$, in two steps. First we claim 

$$f(y, x_1, \ldots, x_k) \leq A_{n+1}(y + \max\{3, x_1, \ldots, x_k\}).$$ 

Indeed, this is true by assumption for $y=0$. And then 

$$\array{
f(y+1, x_1, \ldots, x_k) & = & h(y, f(y, x_1, \ldots, x_k), x_1, \ldots, x_k) \\ 
 & \leq & A_n(\max\{3, y, f(y, x_1, \ldots, x_k), x_1, \ldots, x_k)\}) \\ 
 & \leq & A_n(\max\{3, y, A_{n+1}(y + \max\{3, x_1, \ldots, x_k\}), x_1, \ldots, x_k\}) \\ 
 & \leq & A_n(A_{n+1}(y + \max\{3, x_1, \ldots, x_k\})) \\ 
 & = & A_{n+1}(y+1+\max\{3, x_1, \ldots, x_k\})
}$$ 

which justifies the claim. Finally, we have 

$$\array{
f(y, x_1, \ldots, x_k) & \leq & A_{n+1}(y + \max\{3, x_1, \ldots, x_k\}) \\ 
 & \leq & A_{n+1}(2\max\{3, y, x_1, \ldots, x_k\}) \\ 
 & \leq & A_{n+1}(A_{n+2}(\max\{3, y, x_1, \ldots, x_k\})) \\ 
 & = & A_{n+2}(\max\{3, y, x_1, \ldots, x_k\} + 1) \\ 
 & \leq & A_{n+3}(\max\{y, x_1, \ldots, x_k\})
}$$ 

so that $f$ is dominated by $A_{n+3}$. This completes the proof. 
=-- 

+-- {: .num_corollary} 
###### Corollary 
The Ackermann function $A$ is not primitive recursive. 
=-- 

+-- {: .proof} 
###### Proof 
If $A: x \mapsto A_x(x)$ were recursive, then so would be the function $\phi: x \mapsto A_x(x) + 1$. In that case, $\phi$ is dominated by $A_n$ for some $n \geq 3$. We then arrive at the contradiction 

$$A_n(n) + 1 = \phi(n) \leq A_n(\max\{3, n\}) = A_n(n).$$ 
=-- 

+-- {: .num_prop} 
###### Proposition 
The _graph_ of the Ackermann function _is_ a primitive recursive relation. 
=-- 

+-- {: .proof} 
###### Proof 
The rough idea is to let $z$ bound the search for solutions $(x, y)$ to $A_x(y) = z$. For $x, y \gt 0$ we have $A_x(y) = A_{x-1}(A_x(y-1)) = A_x(y')$ where $y' \coloneqq A_x(y-1)$. We have $y' \lt A_{x-1}(y') = z$. Starting with $y_0 = y \lt z$, iterate this procedure so that 

$$z = A_x(y_0) = A_{x-1}(y_1) = A_{x-2}(y_2) = \ldots = A_0(y_x) = 2 y_x$$ 

with each $y_i$ less than $z$. (Explicitly, the iteration is $y_{i+1} \coloneqq A_{x-i}(y_i - 1)$.) 

Thus, after disposing of some trivial low number cases, WLOG we may take $z \gt 4$, where the ternary predicate 

$$(z \gt 4) \wedge (A_x(y) = z)$$ 

is equivalent to 

$$(x \gt 0) \wedge (y \gt 2) \wedge (x \lt z) \wedge \exists_{y_0, y_1, \ldots y_x \lt z} (y = y_0) \wedge (\forall_{i \lt x} y_{i+1} = A_{x-i}(y_i - 1)) \wedge (2 y_x = z)$$ 

where the quantifications are manifestly bounded by $z$. This shows that the ternary predicate $A_x(y) = z$ is primitive recursive. 

From this it follows that the binary relation $A_x(x) = z$ is also primitive recursive, as claimed. 
=-- 

Combining this result with Theorem \ref{graph}, we have 

+-- {: .num_corollary} 
###### Corollary
The Ackermann function $A: x \mapsto A_x(x)$ is recursive. 
=-- 

+-- {: .num_example #inverse} 
###### Example 
Here we exhibit a primitive recursive bijection whose inverse is not primitive recursive. The graph $y = A_x(x)$ of the Ackermann function is primitive recursive binary predicate, and the image $I = \{y: \exists_x y = A_x(x)\}$ is a primitive recursive unary predicate, because the existential quantifier is a bounded quantifier applied to a primitive recursive relation: 

$$I = \bigvee_{x=0}^{y-1} [A_x(x) = y].$$ 

Observe that both $I$ and its complement $\neg I$ in $\mathbb{N}$ are infinite. 

For any infinite set $J \subseteq \mathbb{N}$, let $p_J: \mathbb{N} \to \mathbb{N}$ be the function taking $n$ to the $n^{th}$ element of $J$ (with respect to the usual order $\lt$). For example, $p_I(x) = A_x(x)$. Now define 
a function $f: \mathbb{N} \to \mathbb{N}$ by 

$$\array{
f(m) & = & 2p_I^{-1}(m) & \text{if} \; m \in I \\ 
     & = & 2p_{\neg I}^{-1}(m) + 1 & \text{if} \; m \in \neg I
}$$ 

Then $f(m) \leq 2m + 1$ and the graph of $f$ is primitive recursive, so by Theorem \ref{bound}, $f$ is a primitive recursive function. It is a bijection by construction. But $f^{-1}$ is not primitive recursive, because $f^{-1}(2x) = p_I(x) = A(x)$, and $A$ is not primitive recursive. 
=-- 

## Busy Beaver function 


## Related concepts

* [[recursive subset]] 

[[!include computable mathematics -- table]]

## References 

A standard textbook in recursive functions is

* Hartley Rogers, Jr., _Theory of recursive functions and effective computability_, McGraw-Hill, 1967.

Quite a bit of the arrangement and proofs above were taken from clear and useful lecture notes of Stephen Simpson, 

* Stephen G. Simpson, _Foundations of Mathematics_ (Lecture Notes), October 1, 2009. ([pdf](http://www.math.psu.edu/simpson/notes/fom.pdf)) 

Of course, there is always good old Wikipedia: 

* Wikipedia, _[Computable function](http://en.wikipedia.org/wiki/Computable_function)_ 


[[!redirects partial recursive function]]
[[!redirects partial recursive functions]]
[[!redirects recursive partial function]]
[[!redirects recursive partial functions]]

[[!redirects Ackermann function]]
[[!redirects Ackermann functions]]

[[!redirects primitive recursive function]]
[[!redirects primitive recursive functions]]
