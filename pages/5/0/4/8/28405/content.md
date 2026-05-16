+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

\tableofcontents

## Idea

*Wall's theorems* are four related results connecting the [[smooth structure]], [[automorphism|auto]]-[[diffeomorphisms]] and the [[intersection form]] of a [[smooth manifold|smooth]] [[4-manifolds]] with [[h-cobordisms]], stably [[diffeomorphisms]] and induced form [[automorphisms]].

## Wall's theorem on h-cobordisms

\begin{proposition}
**(Wall's theorem on h-cobordisms)**
[[Simply connected]] [[smooth manifold|smooth]] [[4-manifolds]] with isomorphic [[intersection forms]] are [[h-cobordant]].
\end{proposition}

([Scorpan 05, p. 155](#Scorpan74))

## Wall's theorem on stabilization

\begin{proposition}
**(Wall's theorem on stabilization)**
For [[h-cobordant]] [[simply connected]] [[smooth manifold|smooth]] [[4-manifolds]] $M$ and $N$, there exists a [[natural number]] $n\in\mathbb{N}$ and a [[diffeomorphism]]:
$$
M\#n\left(S^2\times S^2\right)
\cong N\#n\left(S^2\times S^2\right).
$$
\end{proposition}

([Scorpan 05, p. 149](#Scorpan74)) 

Becoming [[diffeomorphic]] after [[connected sums]] with $S^2\times S^2$ is also called *stably diffeomorphic*. Combining Wall's theorem on [[h-cobordisms]] with Wall's theorem on stabilization directly yields:
\begin{proposition}
[[Simply connected]] [[smooth manifold|smooth]] [[4-manifolds]] with isomorphic [[intersection forms]] are stably [[diffeomorphic]].
\end{proposition}

## Wall's theorem on automorphisms

\begin{proposition}
**(Wall's theorem on automorphisms)**
For a symmetric unimodular bilinear form $Q\colon\mathbb{Z}^n\times\mathbb{Z}^n\rightarrow\mathbb{Z}$ with $rk(Q)-|\sigma(Q)|\geq 4$ and for two elements $x,y\in\mathbb{Z}^n$ with same divilibility, self-intersection $Q(x,x)=Q(y,y)$ and type, there exists an [[automorphism]] $f\colon\mathbb{Z}^n\rightarrow\mathbb{Z}^n$ with $f(x)=y$.
\end{proposition}

([Scorpan 05, p. 152](#Scorpan74))

Divisibility is the largest [[integer]] able to divide the element. Type refers to whether the element is characteristic or not.

$rk(Q)-|\sigma(Q)|$ is always even, hence the above condition excludes only definite forms with $rk(Q)-|\sigma(Q)|=0$ and "near-definite" forms with $rk(Q)-|\sigma(Q)|=2$. According to Serre's classification theorem, the "near-definite" forms only include $H=\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}$ as well as $[+1]\oplus n[-1]$ and $n[+1]\oplus[-1]$.

## Wall's theorem on diffeomorphisms

\begin{proposition}
**(Wall's theorem on diffeomorphisms)**
For a [[simply connected]] [[smooth manifold|smooth]] [[4-manifolds]] $M$ with indefinite [[intersection form]] $Q_M$, every [[automorphism]] of $Q_{M\#(S^2\times S^2)}\cong Q_M\oplus H$ (with the hyperbolic form $H=Q_{S^2\times S^2}=\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}$) comes from a self-[[diffeomorphism]] on $M\#(S^2\times S^2)$.
\end{proposition}

([Scorpan 05, p. 153](#Scorpan74)) 

For [[topological manifolds]], no stabilization is necessary:
\begin{proposition}
For a [[simply connected]] [[topological manifold|topological]] [[4-manifolds]] $M$ with indefinite [[intersection form]] $Q_M$, every [[automorphism]] of $Q_M$ comes from a self-[[homeomorphism]] on $M$, which is unique up to [[isotopy]].
\end{proposition}

([Scorpan 05, p. 153](#Scorpan74))

## References

Named after:

* [[C. T. C. Wall]]: *Diffeomorphisms of 4-Manifolds* Journal of  London Mathematical Society **s1--39** 1 (1964) 131--140 \[<a href="https://doi.org/10.1112/jlms/s1-39.1.131">doi:10.1112/jlms/s1-39.1.131</a>\]

* [[C. T. C. Wall]]: *On simply-connected 4-manifolds*, Journal of the London Mathematical Society **s1--39** 1 (1964) 141–-149 &lbrack;[doi:10.1112/jlms/s1-39.1.141](https://doi.org/10.1112/jlms/s1-39.1.141), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/w4.pdf)&rbrack;

 
See also:

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;

[[!redirects Wall theorems]]
[[!redirects Wall's theorem]]
[[!redirects Wall's theorems]]

[[!redirects Wall theorem on h-cobordism]]
[[!redirects Wall theorem on h-cobordisms]]
[[!redirects Wall's theorem on h-cobordism]]
[[!redirects Wall's theorem on h-cobordisms]]

[[!redirects Wall theorem on stabilization]]
[[!redirects Wall theorem on stabilizations]]
[[!redirects Wall's theorem on stabilization]]
[[!redirects Wall's theorem on stabilizations]]

[[!redirects Wall theorem on automorpism]]
[[!redirects Wall theorem on automorpisms]]
[[!redirects Wall's theorem on automorpism]]
[[!redirects Wall's theorem on automorpisms]]

[[!redirects Wall theorem on diffeomorphism]]
[[!redirects Wall theorem on diffeomorphisms]]
[[!redirects Wall's theorem on diffeomorphism]]
[[!redirects Wall's theorem on diffeomorphisms]]