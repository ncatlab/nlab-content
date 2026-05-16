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

*van der Blij's lemma* is a fundamental insight about the connections between characteristic elements of a symmetric unimodular bilinear form and its [[signature]].

If the manifold is additionally smoothable and [[closed manifold|closed]], van der Blij lemma improves to the more well-known [[Rokhlin theorem]], which features another factor of $2$ corresponding to the [[Kirby-Siebenmann invariant]]

## Statement

\begin{proposition}
For a symmetric unimodular bilinear form $Q\colon\mathbb{Z}^n\times\mathbb{Z} ^n\rightarrow\mathbb{Z}$, a characteristic element $c\in\mathbb{Z}^n$ (fulfilling $Q(x,x) mod 2=Q(c,x) mod 2$ for all $x\in\mathbb{Z}^n$) fulfills:
$$
Q(c,c)
=\sigma(Q)mod 8.
$$
\end{proposition}
\begin{proof}
Let $c,d\in\mathbb{Z}^n$ be characteristic elements, then there exists an element $s\in\mathbb{Z}^n$ with $c=d+2s$, which causes:
$$
Q(c,c)
=Q(d,d)
+4(Q(d,s)+Q(s,s)).
$$
Since $d\in\mathbb{Z}^n$ is characteristic, $Q(d,s)+Q(s,s)\in\mathbb{Z}$ is even, which causes $Q(c,c)=Q(d,d) mod 8$. Without loss of generality, let $Q$ be odd and indefinite. (Otherwise consider the odd and indefinite form $Q'=Q\oplus[+1]\oplus[-1]$ on $\mathbb{Z}^{n+2}$ with characteristic elements $(c,\pm 1,\pm 1)\in\mathbb{Z}^{n+2}$ for every characteristic element $c\in\mathbb{Z}^n$ of $Q$ and $\sigma(Q')=\sigma(Q)$.) According to Serre's classification theorem, $Q\cong m[+1]\oplus n[-1]$ for some $m,n\in\mathbb{N}$. With characteristic elements $c=(\pm 1,\ldots,\pm 1)\in\mathbb{Z}^n$, one has $Q(c,c)=m-n$ and $\sigma(Q)=m-n$.
\end{proof}

([Scorpan 05, p. 170](#Scorpan74))

If the form is even, then $0$ is a characteristic element, which yields:

\begin{proposition}
An even symmetric unimodular bilinear form $Q$ fulfills:
$$
\sigma(Q)
=0 mod 8.
$$
\end{proposition}

If the [[intersection]] form of a [[topological manifold|topological]] [[4-manifold]] is considered, then the manifold being [[spin manifold|spin]] implies that its [[intersection form]] is even according to [[Wu's formula]]. If the manifold is [[simply connected]], then the reverse holds:

\begin{proposition}
The [[signature]] of a [[spin manifold|spin]] [[topological manifold|topological]] [[4-manifold]] fulfills:
$$
\sigma(Q)
=0 mod 8.
$$
\end{proposition}

If the manifold is additionally [[smooth manifold|smooth]] and [[closed manifold|closed]], then [[Rokhlin's theorem]] even assures $\sigma(Q)=0 mod 16$.

## References

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;