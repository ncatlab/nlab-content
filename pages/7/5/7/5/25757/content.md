\tableofcontents 

## Statement 

The infinite product formula for the [[sine]] function, due to Euler, is 

$$\sin x = x \prod_{n=1}^\infty (1 - \frac{x^2}{\pi^2 n^2}).$$ 

Taking logarithms and then derivatives, this is equivalent to the formula 

$$\pi \cot \pi x = \frac1{x} + \sum_{n=1}^\infty \left(\frac1{x+n} + \frac1{x-n} \right)$$ 

and this is what we shall prove, below. 

## Proof 

Various proofs are known, some relating the product formula to the theory of the Gamma function, some using complex analysis, among others. Below we prove the corresponding identity for the [[cotangent]] (stated above), using an ingenious argument due to Herglotz. 

+-- {: .num_theorem #OrderOfZero} 
###### Lemma 
$\underset{x \to 0}{\lim} \pi \cot \pi x - \frac1{x} = 0$. 
=-- 

\begin{proof} In the right-hand side of the equation 

$$\pi \cot \pi x - \frac1{x} = \frac{\pi x\cos \pi x - \sin \pi x}{x \sin{\pi x}},$$ 
the numerator has a zero of order $3$ at $x = 0$, and the denominator has a zero of order $2$ at $x = 0$, by MacLaurin expansions. 
\end{proof} 

\begin{lemma} Let $f(x) = \pi \cot \pi x$ and $g(x) = \frac1{x} + \sum_{n=1}^\infty \left(\frac1{x+n} + \frac1{x-n} \right)$. Then 

$$f\left(\frac{x}{2}\right) + f\left(\frac{x+1}{2}\right) = 2f(x); \qquad g\left(\frac{x}{2}\right) + g\left(\frac{x+1}{2}\right) = 2g(x).$$ 
\end{lemma} 

\begin{proof} The first follows from $\cos\frac{\pi(x+1)}{2} = -\sin\frac{\pi x}{2}$, $\sin\frac{\pi(x+1)}{2} = \cos\frac{\pi x}{2}$, and double-angle formulas. To prove the second identity, put 

$$g_N(x) = \frac1{x} + \sum_{n=1}^N \left(\frac1{x+n} + \frac1{x-n} \right)$$ 
and note that 

$$g_N\left(\frac{x}{2}\right) + g_N\left(\frac{x+1}{2}\right) = 2g_{2N}(x) + \frac{2}{x + 2N + 1}.$$ 
Taking the limit as $N \to \infty$, the result follows. 
\end{proof}  

\begin{lemma} The function $h$, defined by $h(x) = f(x) - g(x)$ for $x \in \mathbb{R} \setminus \mathbb{Z}$ and $h(x) = 0$ for $x \in \mathbb{Z}$, is a continuous odd function of period $1$. 
\end{lemma} 

\begin{proof} The oddness and periodicity assertions are obvious, as is continuity at points $x \notin \mathbb{Z}$. Continuity at points $x \in \mathbb{Z}$ follows from Lemma \ref{OrderOfZero} and periodicity. 
\end{proof} 

Now we prove the cotangent identity: 

\begin{proof} By continuity and periodicity, $h(x)$ attains a maximum value $M$, say at $x_0$. Since $h\left(\frac{x}{2}\right) + h\left(\frac{x+1}{2}\right) = 2h(x)$ by Lemma 2, $h\left(\frac{x_0}{2}\right) = M$ follows (else, $h\left(\frac{x_0}{2}\right) \lt M$ implies $h\left(\frac{x_0+1}{2}\right) \gt M$). By iterating, $h\left(\frac{x_0}{2^m}\right) = M$ for all $m$. By continuity, 

$$M = \underset{m \to \infty}{\lim} h\left(\frac{x_0}{2^m}\right) = h(0) = 0.$$ 
Thus $h(x) \leq M = 0$ for all $x$. From $h(x) \leq 0$ and oddness we get that $h(x) = 0$ identically, and so $f(x) = g(x)$ identically. This completes the proof. 
\end{proof} 

