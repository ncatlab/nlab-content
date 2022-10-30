
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _spin structure_ on a [[manifold]] $X$ with an [[orientation]] is a lift $\hat g$ of the classifying map $g : X \to \mathcal{B} S O(n)$ of the [[tangent bundle]] through the second step $\mathcal{B}Spin(n) \to \mathcal{B}S O(n)$ in the [[Whitehead tower]] of $O(n)$.

$$
  \array{
    && \mathcal{B}Spin(n)
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}&
    \mathcal{B}S O(n)
  }
$$

Spin structures derive their name from the fact that their existence on a space $X$ make the [[quantum anomaly]] for spinning particles propagating on $X$ vanish. See there.

The next steps correspond to 

* [[String structure]]

* [[Fivebrane structure]].

## Definition

For $X$ a [[manifold]], the [[groupoid]]/[[homotopy n-type|homotopy 1-type]] $Spin(X)$ of **spin structures** over $X$ is the [[homotopy fiber]] in [[∞Grpd]] $\simeq$ [[Top]]  of the second [[Stiefel-Whitney class]]

$$
  \array{
    Spin(X) &\to& *
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    Top(X,B SO) &\stackrel{(w_2)_*}{\to}& Top(X, B^2 \mathbb{Z}_2)
  }
  \,.
$$

Here an [[object]] $s \in Spin(X)$ over an $SO$-[[principal bundle]] $\eta(s)$ on $X$ is called a **spin structure on $\eta(s)$** ($SO$ is the [[special orthogonal group]]).

For $\eta(s)$ the $SO$-principal bundle for which the [[tangent bundle]] $T X$ is the canonically [[associated bundle]], one says that a spin-structure on $\eta(s)$ is a **spin structure on the manifold** $X$.

## As quantum anomaly cancellation condition  {#QuantumAnomaly}

In the context of [[quantum field theory]] the existence of a spin structure on a [[Riemannian manifold]] $X$ arises notably as the condition for [[quantum anomaly]] cancellation of the [[sigma-model]] for the spinning particle -- the superparticle -- propagating on $X$. 

Discussions of spin structures along these lines date back to

* [[Edward Witten]], _Global anomalies in String theory_ in _Symposium on anomalies, geometry, topology_ , World Scientific Publishing, Singapore (1985)

* L. Alvarez-Gaum&#233; Communications in Mathematical Physics 90 (1983) 161

* D. Friedan, P. Windey, Nucl. Phys. B235 (1984) 395

It is the generalization of this anomaly computation from the worldlines of superparticles to super[[string theory|string]]s that leads to [[string structure]], and then further the generalizaton to the worldvolume anomaly of fivebranes that leads to [[fivebrane structure]].


## Related concepts

* [[twisted differential c-structure|(twisted differential) c-structure]]

  * [[orientation]]

  * **spin structure**, [[twisted spin structure]], [[differential spin structure]]

    [[spin^c structure]], [[twisted spin^c structure]]

  * [[2-framing]]

  * [[string structure]], [[differential string structure]]

  * [[fivebrane structure]], [[differential fivebrane structure]]

## References

A disccussion of the full [[groupoid]] of spin structures is in 

* [[Johannes Ebert]], _Characteristic classes of spin surface bundles:
Applications of the Madsen-Weiss theory_ Phd thesis (2006) ([pdf](http://wwwmath.uni-muenster.de/wwwmath.uni-muenster.de/u/jeber_02/papers/thesis.pdf))

[[!redirects Spin structure]]
[[!redirects Spin-structure]]
[[!redirects spin-structure]]

[[!redirects Spin structures]]
[[!redirects Spin-structures]]
[[!redirects spin structures]]
[[!redirects spin-structures]]