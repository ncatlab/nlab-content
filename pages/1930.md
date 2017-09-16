##Special $\lambda$-ring##

For any commutative ring $A$ we can consider the set $\Phi(A)$ of power-series in an indeterminate $t$ with coefficients in $A$ whose constant term is $1$: 

  $f(t) = 1 + a_1t + a_2t^2 + \ldots$

These form an abelian group under multiplication with the constant power-series 1 as unit. What may be less familiar is that there is a commutative associative binary operation $\circ$ on this set that distributes over multiplication making $\Phi(A)$ into a commutative ring, for which the function $\epsilon_A: \Phi(A) \rightarrow A$ taking $f(t)$ to $f'(0)$ is a homomorphism. So what is usually called multiplication of power-series becomes _addition_ in this ring, with $1$ as zero; very confusing. Of course, $\Phi$ is a functor from rings to rings and $\epsilon$ is a natural transformation. In fact it is the counit of a comonad.

How is $\circ$ defined? We impose the condition

$(1 + at)\circ f(t) = f(at)$

for $a\in A$ and $f(t)\in \Phi(A)$. It is now clear from distributivity that if $g(t) = \Pi_j(1+a_j t)$ then $g(t)\circ f(t) = \Pi_j f(a_j t)$. But what happens if $g(t)$ is not a product of linear factors? Newton's theorem on symmetric polynomials comes to the rescue. For we note that the coefficient of $t^n$ in $\Pi_j f(a_j t)$ is a symmetric function in the $a_j$ and so can be expressed as a polynomial over the integers in the first $n$ coefficients of $g(t)$ and of $f(t)$. In this way we have indicated that a universal formula for multiplication in $\Phi(A)$ exists, though we may not have written it down explicitly.

We use the same trick in defining the comultiplication

$\mu_A : \Phi(A) \rightarrow \Phi(\Phi(A))$

but now our old-fashioned notation and use of indeterminates starts to cause trouble. A power-series in
$\Phi(A)$ is really just a sequence $(a_1, a_2, \ldots)$.
We demand that 

$\mu_A (a,0,0, \ldots) = ((a,0,0, \ldots),(0,0, \ldots), \ldots )$

Again, to define $\mu_A$ on an arbitrary power-series, factorize it formally into linear factors, apply the rule and distributivity, and apply Newton's theorem.

A **special $\lambda$-ring** is a coalgebra for the comonad $\Phi$ above. If $\xi : A \rightarrow \Phi(A)$ is the costructure map for such a coalgebra, we define unary operations $\lambda^n$ on $A$ by the formula

$\xi(a) = 1 + \lambda^1(a)t + \lambda^2(a)t^2 + \ldots$

The counit condition forces $\lambda^1(a) = a$. It is also traditional to denote $\xi(a)$ by $\lambda_t (a)$. Note that $\lambda_t(a_1 + a_2) = \lambda_t(a_1)\lambda_t(a_2)$ and that $\lambda_t(a_1 a_2) = \lambda_t(a_1)\circ\lambda_t(a_2)$.

The functor $\Phi$ is representable by a commutative Hopf algebra $\Lambda$, and so has a left adjoint. The underlying ring of $\Lambda$ is $\mathbb{Z}[\lambda^1,\lambda^2, \ldots ]$, the free special $\lambda$-ring on one generator ($\lambda^1$).

In the terminology of [bimodels](bimodel) $\Phi = \Lambda\Rightarrow?$ and its left adjoint is $\Lambda\otimes?$.
So the theory of special $\lambda$-rings is a monadic extension of the theory of rings.

