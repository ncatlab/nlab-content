"Approximation of the identity" is a rubric for a general technique in functional analysis for proving that certain inclusions of [[topological vector space]]s are dense. It refers to the fact that an identity for a convolution product (aka "Dirac distribution") may not literally exist in a particular TVS, but is virtually there in the sense that it can be approximated by elements in the subspace which is being included. 

## Examples ## 

We illustrate the technique with two examples. 

+-- {: .num_example}
###### Example

Consider first the problem of showing that restrictions of polynomials to $[-1, 1]$ are dense in $L^p([-1, 1])$ (under Lebesgue [[measure space|measure]]). The idea is to take the formula 

$$ f(y) = (f * \delta)(y) = \int_{-1}^1 f(x) \delta(y - x) d x $$ 

(which literally makes no sense because $\delta$ is not an actual integrable function) and then replace $\delta$ by polynomial functions $p_n$ which "approximate" to it (so each $p_n$ has "mass" 1 and is vanishingly small outside a given neighborhood of 0, if $n$ is sufficiently large). 

Put for example $f_n(x) = (1 - x^2)^n$ and "normalize" it, putting 

$$p_n = \frac{f_n}{\|f_n\|_1}$$ 

where $\|g\|_1$ indicates $L^1$ norm. By "differentiating under the integral sign", we have 

$$ D^j (f * p_n) = (-1)^j f * D^j(p_n) $$ 

so that for each $n$, the $j^{th}$ derivative of $f * p_n$ is identically zero for $j$ sufficiently large. Hence $f * p_n$ is polynomial. Next, the claim is that for $f \in L^p$, we have 

$$lim_{n \to \infty} \|f - (f * p_n)\|_p = 0$$ 

Intuitively, the idea is that $ f - (f * p_n) = f * (\delta - p_n) $ and that (because $L^p$ is a module over the [[Banach algebra]] $L^1$) 

$$\|f * (\delta - p_n)\|_p \leq \|f\|_p \|\delta - p_n\|_1 \to 0$$ 

as $n \to \infty$. For a more careful proof, see theorem 9.6 in Wheeden and Zygmund (referenced below). 
=--

+-- {: .num_example}
###### Example

For a second example, consider how to prove that the functions $z^n$, with $n$ ranging over integers, forms an orthonormal basis of the [[Hilbert space]] $L^2(S^1)$ where $S^1$ is the unit circle in the complex plane, where the inner product is given by 

$$\langle f, g \rangle = \frac1{2\pi i} \int_{S^1} \overline{f(z)} g(z) \frac{d z}{z}$$ 

The monomials $z^n$ are clearly orthonormal, so again the idea is to use appropriate linear combinations of the $z^n$ (i.e., Laurent polynomials) to approximate a Dirac mass concentrated at the identity $z = 1$ in $S^1$. 
There are various ways of doing that; one of the most useful is by taking the F&#233;jer kernel 

$$F_n(z) = \frac1{n+1} (\sum_{-n \leq k \leq n} z^{k/2})^2 = \frac1{n+1}(z^{-n} + 2z^{-n+1} + \ldots + (n+1)z^0 + \ldots + 2z^{n-1} + z^n)$$ 

Each Laurent polynomial $F_n(z)$ is real-valued, nonnegative, and its $L^1$ norm is 1. Putting $z = e^{i x}$, we have 

$$F_n(e^{i x}) = \frac1{n+1} \frac{\sin^2((n+1)x/2)}{\sin^2(x/2)}$$ 

which makes it clear that $F_n(e^{i x})$ becomes very small outside a neighborhood of 0 (in $\mathbb{R}/2\pi\mathbb{Z}$) as $n$ grows large. Thus $F_n$ approximates the identity; therefore for any $L^2$ function $f$ on $S^1$, we have 

$$\lim_{n \to \infty} \|(F_n * f) - f\|_2 = 0$$ 

Finally, $F_n * f$ is itself a Laurent polynomial; this follows from the fact that for the function $e_n(z) = z^n$, one has 

$$ (e_n * f)(w) = \frac1{2\pi i}\int_{S^1} (w/z)^n f(z) \frac{d z}{z} = e_n(w)\langle e_n, f \rangle$$ 

It follows from all this that the Laurent polynomials on $S^1$ are dense in $L^2(S^1)$. 

A similar technique applies to any compact Hausdorff abelian group $G$ equipped with its normalized Haar measure $d\mu$, in place of the measure space $(S^1, \frac1{2\pi i}\frac{d z}{z})$, and shows that the characters on the group span a dense subspace in $L^2$ norm. In other words, the characters form an orthonormal basis of $L^2(G, d\mu)$. 
=--