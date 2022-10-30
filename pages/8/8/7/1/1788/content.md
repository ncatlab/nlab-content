+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***

$$
  \mu \colon \mathbb{g} \longrightarrow \mathbb{R}[n]
$$

be a [[super L-∞ algebra]] [[L-∞ cocycle]]. Let 

$$
  \mathbf{c} \colon \mathbf{B}G \longrightarrow \mathbf{B}^{n+1}(\mathbb{R}/\Gamma)
$$

be its [[Lie integration]] in [[smooth super ∞-groupoids]], according to ([Fiorenza-Schreiber-Stasheff 10](#FiorenzaSchreiberStasheff10)). 

Observe that the [[smooth ∞-group]] $G$ has, by [[cohesion]], a canonical higher [[Maurer-Cartan form]]

$$
  \theta \;\colon \; G \longrightarrow \flat_{dR}\mathbf{B}G
  \,. 
$$

This is a [[cocycle]] in the nonabelian de Rham [[hypercohomology]] of $G$. We want an [[schreiber:∞-Wess-Zumino-Witten theory]] model with a _globally defined_ [[curvature]] $(n+1)$-form. Therefore consider the [[universal construction|universal]] solution $\tilde G$ of making $\theta$ globally well defined, hence the [[homotopy pullback]]

$$
  \array{
    \tilde G &\stackrel{\theta_{global}}{\to}& \Omega_{flat}(-,\mathfrak{g})
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{\theta_G}{\to}& \flat_{dR} \mathbf{B}G
  }
  \,.
$$

Then one observes that by [[cohesion]] the [[pasting]] diagram on the right of the following exists, and hence defines a [[local action functional]] $\exp(i S_{WZW})$ by the universal factorization on the left. This is the [[schreiber:∞-Wess-Zumino-Witten theory]] induced by the [[L-∞ cocycle]] $\mu$:

$$
  \array{
    && \tilde G
    \\
    & \swarrow &\downarrow^{\exp(i S_{WZW})}& \searrow^{\mathrlap{\mu(\theta_{global})}}
    \\
    \ast &\leftarrow& \mathbf{B}^n U(1)_{conn} &\rightarrow& \Omega_{cl}^{n+1}
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow
    \\
    && \flat \mathbf{B}^{n+1}U(1)
  }
  \;\;\coloneqq\;\;
  \array{
    && && \tilde G
    \\
    && & \swarrow && \searrow^{\mathrlap{\theta_{global}}}
    \\
    && G && && \Omega_{flat}(-,\mathfrak{g})
    \\
    & \swarrow && \searrow^{\mathrlap{\theta_G}} && \swarrow && \searrow^{\mathrlap{\mu}}
    \\
    \ast && && \flat_{dR}\mathbf{B}G && && \Omega^{n+1}_{cl}
    \\
    & \searrow && \swarrow && \searrow^{\mathrlap{\flat_{dR}\mathbf{c}}} && \swarrow
    \\
    && \flat \mathbf{B}G && &&\flat_{dR} \mathbf{B}^{n+1}U(1)
    \\
    && & {}_{\mathllap{\exp(i S_{CS}^{flat})}}\searrow^{\mathrlap{\flat \mathbf{c}}} && \swarrow
    \\
    && && \flat \mathbf{B}^{n+1}U(1)
  }
  \,.
$$

One then shows ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)) that for $\mu$ the exceptional  cocycles on the [[super Poincare Lie algebra]] and their higher extensions such as notably the [[supergravity Lie 3-algebra]] and [[supergravity Lie 6-algebra]]
that the [[schreiber:∞-Wess-Zumino-Witten theory]] models obtained this way reproduce the [[Green-Schwarz action functional]] "old [[brane scan]]" including for instance the [[heterotic string]] [[sigma-model]] and the [[M2-brane]] [[sigma-model]], and ols encodes the branes with tensor multiplet fields such as the [[D-branes]] and the single (abelian) [[M5-brane]].

So now one just needs to put the pieces toghether with the nonabelian [[7d Chern-Simons theory]] correctio  and apply holographic boundary motivic quantization. This however is to be disucssed elsewhere. 


***

category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects ??? ????]]
[[!redirects Featured math : Quora]]