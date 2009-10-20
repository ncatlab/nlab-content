A _generating function_ is an element of $R[\![z]\!]$, the [[rig]] of formal [[power series]] over the rig $R$ (which is often taken to be the [[natural numbers]] or the [[rational number]]s), used for purposes of [[combinatorics]].  A general element takes the form
\[f(z) = \sum_{n=0}^{\infty}f_n z^n.\]
If $R$ is taken to be the [[real numbers]] or the [[complex numbers]] (or any subrig), then we can ask whether the power series has a radius of convergence $r \ge 0$ and if there's an [[analytic continuation]]; if so, then we also say that the continuation is the generating function.

When $R = \mathbb{N},$ we can think of the coefficients on $z^n$ as counting the number of ways to put a particular structure on the [[finite set]] $n$.  (You get [[structure types]] if you take this literally.)  

Multiplying generating functions in the same variable gives
\[ \left(\sum_{n=0}^{\infty}f_n z^n\right)\left(\sum_{n=0}^{\infty}g_n z^n\right) = \sum_{n=0}^{\infty}\sum_{k=0}^n f_k g_{n-k} z^n,\]
which effectively says to split up the set into two parts, put the $f$ structure on the first part and the $g$ structure on the second part.

_Ordinary_ generating functions describe structures on [[totally ordered sets]], while _exponential_ generating functions apply to unordered [[sets]].  For example, the generating function for being an unordered finite set is
\[ e^z = 1 + z + \frac{z^2}{2!} + \frac{z^3}{3!} + \cdots ,\]
while the generating function for being a finite ordered set is
\[ \frac{1}{1-z} = 1 + z + z^2 + z^3 + \cdots .\]

If we assume that the zeroth term is $1$, then multiplying generating functions in different variables gives
\[ \left(\sum_{n=0}^{\infty}f_n x^n\right)\left(\sum_{n=0}^{\infty}g_n z^n\right) = 1 + (f_1 x + g_1 z) + (f_2 x^2 + f_1 g_1 x z + g_2 z^2) + \cdots\]
If we take the product of countably many generating functions $f^i(x_i)$ and then set $x_i = p_i^{-s},$ where $p_i$ is the $i$th prime, then we get
\[ 1^{-s} + f^1_1 2^{-s} + f^2_1 3^{-s} + f^1_2 4^{-s} + f^3_1 5^{-s} + f^1_1 f^2_1 6^{-s} + \cdots + \prod_{i} f^i_{e_i} (p_i^{e_i})^{-s} + \cdots, \]
which is called the _Dirichlet_ generating function for the family $f^i.$

The product of two Dirichlet generating functions gives
\[ \left(\sum_{n=1}^{\infty}f_n n^{-s}\right)\left(\sum_{n=1}^{\infty}g_n n^{-s}\right) = \sum_{n=1}^{\infty} \sum_{d|n} f_d g_{n/d} n^{-s},\]
which effectively says to _factor_ the term into two dimensions, apply $f$ to the first and $g$ to the second.

Generating functions often appear as [[partition functions]].

Sometimes we take the *exponents* on $z$ to be in a rig other than the natural numbers.  For example, we might set $z^a \cdot z^b = z^{\max(a,b)}$ and $(z^a)^b = z^{a+b};$ such a system lets us talk about the [[rig of costs|cost]] of operations done in parallel (max) or sequentially (+).  Similarly, we could take the exponents to be [[binary string]]s when considering instantaneous codes, or [[finite field]] elements when considering structures on a finite collection of objects.