
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

> For diambiguation see at *[[wreath product]]*.

# Wreaths

* table of contents
{:toc}

## Idea

A **wreath** is a generalisation of a [[distributive law]] between two [[monads]] in a [[2-category]]. While a distributive law in a [[2-category]] $K$ can be seen as an object of $Mnd(Mnd(K))$, a wreath can be seen as an object of $EM(EM(K))$, where $EM$ denotes the completion of a 2-category under [[Eilenberg–Moore objects]]. Since $EM$ is a [[2-monad]], the multiplication $EM \circ EM \to EM$ produces from every wreath a **composite monad**, called its [[wreath product of wreaths|wreath product]].

## Definition
Let $\mathcal{K}$ be a [[2-category]]. A *wreath* in $\mathcal{K}$ consists of:

1. A [[monad]] $(A,t, \eta, \mu)$ in $\mathcal{K}$,
2. A 1-cell $(s,\lambda):(A,t) \to (A,t)$ in $EM(\mathcal{K})$, that is a 1-cell $s:A \to A$ in $\mathcal{K}$ and a 2-cell $\lambda : ts \to st$ satisfying the axioms:

\begin{tikzcd}
	tts & tst & stt && s \\
	ts && st & ts && st
	\arrow["{t\lambda}", from=1-1, to=1-2]
	\arrow["{\mu s}"', from=1-1, to=2-1]
	\arrow["{\lambda t}", from=1-2, to=1-3]
	\arrow["{s\mu}", from=1-3, to=2-3]
	\arrow["{\eta s}"', from=1-5, to=2-4]
	\arrow["{s\eta}", from=1-5, to=2-6]
	\arrow["\lambda"', from=2-1, to=2-3]
	\arrow["\lambda"', from=2-4, to=2-6]
\end{tikzcd}

3. Two 2-cells $\sigma : 1 \to (s,\lambda)$ and $\mu : (s, \lambda)(s,\lambda) \to (s, \lambda)$ in $EM(\mathcal{K})$, which amount to two 2-cells in $\mathcal{K}$, $\sigma : 1 \to st$ and $nu : ss \to st$, such that

\begin{tikzcd}
	t && stt & tss & sts & sst & stt \\
	tst & stt & st & tst && stt & st
	\arrow["{\sigma t}", from=1-1, to=1-3]
	\arrow["{t\sigma}"', from=1-1, to=2-1]
	\arrow["{s\mu}", from=1-3, to=2-3]
	\arrow["{\lambda s}", from=1-4, to=1-5]
	\arrow["{t\nu}"', from=1-4, to=2-4]
	\arrow["{s\lambda}", from=1-5, to=1-6]
	\arrow["{\nu t}", from=1-6, to=1-7]
	\arrow["{s\mu}", from=1-7, to=2-7]
	\arrow["{\lambda t}"', from=2-1, to=2-2]
	\arrow["{s\mu}"', from=2-2, to=2-3]
	\arrow["{\lambda t}"', from=2-4, to=2-6]
	\arrow["{s\mu}"', from=2-6, to=2-7]
\end{tikzcd}

\begin{tikzcd}
	sss & sst & stt && s & sst & sts & s \\
	sts &&&&& stt \\
	sst & stt & st &&& st
	\arrow["{s\nu}", from=1-1, to=1-2]
	\arrow["{\nu s}"', from=1-1, to=2-1]
	\arrow["{\nu t}", from=1-2, to=1-3]
	\arrow["{s\mu}", from=1-3, to=3-3]
	\arrow["{s\sigma}", from=1-5, to=1-6]
	\arrow["{s\eta}"', from=1-5, to=3-6]
	\arrow["{\nu t}"', from=1-6, to=2-6]
	\arrow["{s\lambda}"', from=1-7, to=1-6]
	\arrow["{\sigma s}"', from=1-8, to=1-7]
	\arrow["{s\eta}", from=1-8, to=3-6]
	\arrow["{s\lambda}"', from=2-1, to=3-1]
	\arrow["{s\mu}", from=2-6, to=3-6]
	\arrow["{\nu t}"', from=3-1, to=3-2]
	\arrow["{s\mu}"', from=3-2, to=3-3]
\end{tikzcd}

## Duality
A *cowreath* (for lack of better terminology) in a 2-category $\mathcal{K}$ is an object of $KL(KL(\mathcal{K}))$, where $KL(\mathcal{K}) = EM(\mathcal{K}^{op})^{op}$ is the free Kleisli completion of $\mathcal{K}$.

It consists of

1. A [[monad]] $(A,t, \eta, \mu)$ in $\mathcal{K}$,
2. A 1-cell $(s,\lambda):(A,t) \to (A,t)$ in $KL(\mathcal{K})$, that is a 1-cell $s:A \to A$ in $\mathcal{K}$ and a 2-cell $\lambda : st \to ts$ satisfying axioms as above.
3. Two 2-cells $\sigma : 1 \to (s,\lambda)$ and $\mu : (s, \lambda)(s,\lambda) \to (s, \lambda)$ in $KL(\mathcal{K})$, which amount to two 2-cells in $\mathcal{K}$, $\sigma : 1 \to ts$ and $nu : ss \to ts$, satisfying axioms as above.

A *morphism of cowreaths* is a 1-cell $(f,\phi, \bar \phi) : (A,t,s) \to (A',t',s')$ in $KL(KL(\mathcal{K}))$. It consists of

1. A [[colax morphism]] of monads $(f,\phi):(A,t) \to (A',t')$, which is a 1-cell $f:A \to A'$ in $\mathcal{K}$ plus a comparison 2-cell $\phi : tf \to ft'$ (satisfying analogous laws to a [[monad#BicategoryOfMonads|lax morphism of monads]])
2. A 2-cell $\bar \phi : (f,\phi)(s, \lambda) \to (s,\lambda)(f,\phi)$ in $KL(\mathcal{K})$, which amounts to a 2-cell ${\bar{\phi}} : fs \to t's'f$, suitably commuting with $\phi$ and $\lambda$:
\begin{tikzcd}
	fst & fts & {t'fs} & {t't's'f} \\
	{t's'ft} & {t's't'f} & {t't's'f} & {t's'f}
	\arrow["{f\lambda}", from=1-1, to=1-2]
	\arrow["{\bar \phi t}"', from=1-1, to=2-1]
	\arrow["{\phi s}", from=1-2, to=1-3]
	\arrow["{t'\bar \phi}", from=1-3, to=1-4]
	\arrow["{\mu's'f}", from=1-4, to=2-4]
	\arrow["{t's'\phi}"', from=2-1, to=2-2]
	\arrow["{t'\lambda'f}"', from=2-2, to=2-3]
	\arrow["{\mu's'f}"', from=2-3, to=2-4]
\end{tikzcd}

The pair $((f,\phi), \bar \phi)$ is then required to satisfy the axioms of 1-cell in $KL$.

## Related concepts

* [[distributive law]]

## Literature

* [[Steve Lack]], [[Ross Street]], _The formal theory of monads II_, Special volume celebrating the 70th birthday of Professor Max Kelly.
J. Pure Appl. Algebra 175 (2002), no. 1-3, 243--265. 

* Dimitri Chikhladze, _A note on warpings of monoidal structures_, [arXiv:1510.00483](https://arxiv.org/abs/1510.00483) (2015).

[[!redirects wreaths]]
