
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

Given a [[differentiable map]] $f:M\to N$ of [[differentiable manifold | differentiable manifolds]], for each $p \in M$ we have the differential $d f_p : T_p M \to T_{f(p)} N$ of $f$ at $p$. These maps define a unique _tangent map_ $T f : T M \to T N$ of [[tangent bundles]] (as [[vector bundles]]) such that the [[diagram]]

$$\array{
T_p M &\stackrel{d_p f}\to & T_{f(p)}N\\
\downarrow &&\downarrow
\\
T M &\stackrel{T f}\to & T N
}$$

[[commuting diagram|commutes]] for each $p$. The differential $d f_p$ of $f$ at $p$ (or sometimes the composition $T_p M\stackrel{d_p f}\rightarrow T_{f(p)}N\hookrightarrow  T N$) is then denoted $T_p f$,
making $T$ into a [[functor]] (see *[[differentiation]]*).

category: geometry, differential geometry
[[!redirects tangent maps]]