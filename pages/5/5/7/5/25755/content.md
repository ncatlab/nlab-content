\tableofcontents 

## Idea 

Stirling's approximation, or Stirling's formula, gives an asymptotic approximation to the [[factorial|factorial function]] in terms of [[elementary function|elementary functions]]. 

## Statement 

Define $n!$ for $n \in \mathbb{N}$ as usual by [[recursion]]: $0! = 1$ and $(n+1)! = (n+1) \cdot n!$. Stirling's approximation says 

$$n! \sim \frac{n^n \sqrt{2\pi n}}{e^n}$$ 

or in other words that 

$$\underset{n \to \infty}{\lim}\; \frac{n^n \sqrt{2\pi n}}{e^n \cdot n!} = 1.$$ 

## Proof 

Many proofs are known. The following is meant to bring out the essential kinship between this formula and the famous formula 

$$\int_{-\infty}^\infty e^{-x^2}\; d x = \sqrt{2\pi}.$$ 

First we establish an elementary fact, accessible to a student of elementary calculus. 

\begin{proposition} For some [[constant function|constant]] $C$, 

$$n! \sim C\frac{n^n \sqrt{n}}{e^n}.$$ 
\end{proposition} 

\begin{proof} 
Consider a [[trapezoidal sum estimate]] for the integral 

$$I_n = \int_1^n \log x\; dx = \left. x\log x - x\right|_1^n = n \log n - n + 1 = 1 + \log \frac{n^n}{e^n}.$$ 
Partitioning the interval $[1, n]$ into subintervals of unit length, the corresponding trapezoidal sum is 

$$T_n = \frac{\log 1 + \log 2}{2} + \frac{\log 2 + \log 3}{2} + \cdots + \frac{\log (n-1) + \log n}{2} = \log (n!) - \frac1{2} \log n = \log \frac{n!}{\sqrt{n}}.$$ 
$T_n$ underestimates $I_n$ because the graph of $\log$ is "concave down" (meaning $-\log x$ is a [[convex function]]). In other words, the error terms 

$$\int_k^{k+1} \log x\; dx - \frac{\log k + \log (k+1)}{2}  $$ 
are positive, so that the sum of these error terms from $k=1$ to $n-1$, which is $I_n - T_n$, increases with $n$. However, using the error term estimate for the trapezoidal rule, the term (1) is on the order of $1/k^2$ (the maximum value of $|(\log)''(x)| = 1/x^2$ over $[k, k+1]$). Since $\sum 1/k^2$ converges, we see that the increasing sequence $I_n - T_n$ has a uniform upper bound and therefore a limit. Hence the limit 

$$\underset{n \to \infty}{\lim} (I_n - 1) - T_n = 
\underset{n \to \infty}{\lim} \log \frac{n^n}{e^n} - \log \frac{n!}{\sqrt{n}} = 
\underset{n \to \infty}{\lim} \log \frac{n^n \sqrt{n}}{e^n \cdot n!}$$ 
exists, and therefore $n! \sim C\frac{n^n \sqrt{n}}{e^n}$ for some constant $C$. 
\end{proof} 

The following lemma makes reference to the [[Gamma function]]. 

\begin{lemma} 
$\frac{\sqrt{2\pi}}{C} = \underset{n \to \infty}{\lim} \frac{\Gamma(n + (1/2))}{\Gamma(n) \cdot \sqrt{n}}$; in particular, this limit exists. 
\end{lemma} 

\begin{proof} 
From $n! \sim C\frac{n^n \sqrt{n}}{e^n}$, we easily derive 

$$\frac{(2n)!}{n! \cdot n!} \sim \frac{2^{2n} \sqrt{2n}}{C n}$$ 
so that 

$$\frac1{C} \sim \frac{(2n)!}{2^{2n} n! \cdot n!} \cdot \frac{n}{\sqrt{2n}} = \frac{(2n-1)(2n-3) \ldots 3 \cdot 1}{2 \cdot (2n-2)(2n-4) \ldots 2} \cdot \frac1{\sqrt{2n}}.$$ 
Then, using $\Gamma\left(\frac1{2}\right) = \int_0^\infty e^{-x^2} dx = \sqrt{\pi}$, we have 

$$\frac{\sqrt{2\pi}}{C} \sim \frac{(2n-1)(2n-3) \ldots 3 \cdot 1}{2 \cdot (2n-2)(2n-4) \ldots 2} \cdot \frac{\sqrt{\pi}}{\sqrt{n}} = \frac{\left(n-\frac1{2}\right)\left(n-\frac{3}{2}\right) \ldots \left(\frac1{2}\right) \Gamma\left(\frac1{2}\right)}{(n-1)! \cdot \sqrt{n}} = \frac{\Gamma\left(n + \frac1{2}\right)}{\Gamma(n) \cdot \sqrt{n}}.$$
\end{proof} 

\begin{proposition} 
$\underset{n \to \infty}{\lim} \frac{\Gamma(n + (1/2))}{\Gamma(n) \cdot \sqrt{n}}  = 1$. 
\end{proposition}  

\begin{proof} 
From log-convexity of $\Gamma$, we may derive 

$$\frac{\Gamma(x-1/2)}{\Gamma(x - 1)} \leq \frac{\Gamma(x)}{\Gamma(x-1/2)} \leq \frac{\Gamma(x+1/2)}{\Gamma(x)}$$ 
which implies that the values of $\frac{\Gamma(x+1/2)}{\Gamma(x) \cdot \sqrt{x}}$, with $x$ ranging over half-integers, tend to the same limit $L$ as with $x$ ranging over whole integers. Therefore 

$$L^2 = \underset{n \to \infty}{\lim} \frac{\Gamma(n+1)}{\sqrt{n+(1/2)}\cdot \Gamma(n + (1/2))} \cdot \frac{\Gamma(n + (1/2))}{\sqrt{n}\Gamma(n)} 
= \underset{n \to \infty}{\lim} \frac{n\Gamma(n)}{\sqrt{(n+1/2)n}\cdot \Gamma(n)},$$ 
whence $L^2 = 1$, and therefore $L = 1$. 
\end{proof} 

## References 

* [n-Category Caf&eacute; post](https://golem.ph.utexas.edu/category/2021/10/stirlings_formula.html) 

* Dan Romik, *Stirling's Approximation for n!: the Ultimate Short Proof?*,
The American Mathematical Monthly
Volume 107 Issue 6 (2000), 556-557. doi.org/10.1080/00029890.2000.12005235 
