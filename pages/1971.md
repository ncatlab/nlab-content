##Idea##

A symmetric function is more-or-less a [[polynomial]] that is invariant under permutation of the variables.  This is only strictly correct if the number of variables is finite; the only symmetric *polynomials* in infinitely many variables are the constants.  To fix this, we allow infinitely many terms, as long as the *degree* is finite.  By default, the number of variables is countably infinite, indexed by [[natural numbers]].

For example, there is a $1$-dimensional space of homogeneous symmetric functions of degree $1$, with basis

$$ x_1 + x_2 + \cdots = \sum_i x_i .$$

There is a $2$-dimensional space of homogeneous symmetric functions of degree $2$, with basis

$$ x_1^2 + x_2^2 + \cdots = \sum_i x_i^2 $$

and 

$$ \sum_{i \lt j} x_i x_j .$$

(The homogeneous symmetric functions of degree $0$ are just the constants, as usual.)


##Definition##

Let $\Lambda_n$ be the [[ring]] consisting of polynomials in $n$ variables $x_1, \dots, x_n$ that are invariant under all permutations of the variables; these are the **symmetric functions in $n$ variables** or **symmetric polynomials** in $n$ variables.   There is an inclusion of rings

$$ \Lambda_n \hookrightarrow \Lambda_{n+1} ,$$

given by adding in new terms with the new variable to make the result symmetric.

Taking a suitable limit (or really [[colimit]]) of the rings $\Lambda_n$ as $n \to \infty$, we get $\Lambda_\infty$ or $\Lambda$, the ring of **symmetric functions in countably many variables**, or simply **symmetric functions** (sometimes also called **symmetric polynomials**, even though very few of them are really polynomials).

The definition depends on the ground [[field]] (or [[commutative ring]] or [[rig]]) $k$, so we may write $\Lambda(k)$ to be precise.


##Properties##

Symmetric functions play a fundamental role throughout [[representation theory]], [[combinatorics]] and [[algebraic topology]].  $\Lambda$ is the free $\lambda$-[[lambda-ring|ring]] on one generator (a coincidence of notation that has not been ignored). It is also the [[Grothendieck ring]] of the [[free object|free]] [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] on one generator.  There are various bases of $\Lambda$ whose elements are in natural one-to-one correspondence with [[Young diagram|Young diagrams]].  

We may also obtain $\Lambda(\mathbb{C})$ by taking the [[Grothendieck group]] of the symmetric monoidal abelian category of $\mathbb{C}$-linear [[species]].  This category is defined to be the functor category

$$ [S, Fin Vect_{\mathbb{C}}] $$

where $S$ is the groupoid of [[finite sets]] and bijections, and $\FinVect_{\mathbb{C}}]$ is the category of finite-dimensional complex vector spaces and linear maps.  This becomes a symmetric monoidal category thanks to [[Day convolution]].

+-- {: .query}
[[John Baez]]: Do we need the complex numbers in the previous paragraph, or will any field do equally well?  Maybe just any field of characteristic zero?  I really want to know!  Another way to put my question: take the category of representations of the permutation group $S_n$ in finite-dimensional vector spaces over the field $k$.  Take the Grothendieck group of this.  Does this depend on $k$?  Does something weird happen when $n$ is divisible by $char k$? 

_Toby_:  Since this is all algebra, any algebraically complete field of characteristic zero must work.  Do you know a reference for the proof?; can we see what it depends on?
=--