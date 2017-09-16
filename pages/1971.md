##Idea##

A symmetric function is a 'polynomial' in countably many variables $x_i$ that is invariant under permutation of the variables.  For example, there is a 1-dimensional space of homogeneous symmetric functions of degree 1, with basis

$$ x_1 + x_2 + \cdots $$

There is a 2-dimensional space of homogeneous symmetric functions of degree 2, with basis

$$ x_1^2 + x_2^2 + \cdots $$

and 

$$ \sum_{i \lt j} x_i x_j  $$

These examples explain why we need to put the word 'polynomial' in quotes: unlike ordinary polynomials, symmetric functions are typically _infinite_ sums of monomials.

##Definition##

Let $\Lambda_n$ be the ring consisting polynomials in $n$ variables $x_1, \dots, x_n$ that are invariant under all permutations of the variables: so-called **symmetric functions in $n$ variables**.   There is an obvious inclusion of rings

$$ \Lambda_n \hookrightarrow \Lambda_{n+1} $$

Taking a suitable limit (or really [[colimit]]) of the rings $\Lambda_n$ as $n \to \infty$, we get $\Lambda$, the ring of **symmetric functions in countably many variables**, or simply **symmetric functions**.

##Properties##

Symmetric functions play a fundamental role throughout representation theory, combinatorics and algebraic topology.  $\Lambda$ is the free [[lambda-ring]] on one generator. It is also the [[Grothendieck ring]] of the free symmetric monoidal abelian category on one generator is the free $\lambda$-ring on one generator.  There are various bases of $\Lambda$ whose elements are in natural one-to-one correspondence with [[Young diagram|Young diagrams]].  

We may also obtain $\Lambda$ by taking the Grothendieck group of the symmetric monoidal abelian category of $\mathbb{C}$-linear [[species]].  This category is defined to be the functor category

$$ [S, \FinVect_{\mathbb{C}}] $$

where $S$ is the groupoid of finite sets and bijections, and
$\FinVect_{\mathbb{C}}]$ is the category of finite-dimensional complex vector spaces and linear maps.  This becomes a symmetric monoidal category thanks to [[Day convolution]].

+-- {: .query}
[[John Baez]]: Do we need the complex numbers in the previous paragraph, or will any field do equally well?  Maybe just any field of characteristic zero?  I really want to know!  Another way to put my question: take the category of representations of the permutation group $S_n$ in finite-dimensional vector spaces over the field $k$.  Take the Grothendieck group of this.  Does this depend on $k$?  Does something weird happen when $n$ is divisible by $char k$? 
=--