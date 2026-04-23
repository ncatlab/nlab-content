+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

\tableofcontents

## Idea

*Rokhlin's theorem* states that the [[signature]] of a [[smooth manifold|smooth]] [[orientable]] [[closed manifold|closed]] [[spin manifold|spin]] [[4-manifold]] is divisible by $16$. It therefore serves as an obstruction for the existence of [[smooth structures]]. A famous example is the [[E₈ manifold]] with [[intersection form]] the [[E₈ lattice]] and therefore [[signature]] $8$. Since it is an [[orientable]] [[closed manifold|closed]] [[spin manifold|spin]] [[4-manifold]], Rokhlin's theorem states that it cannot carry a [[smooth structure]].

## Formulation

For a [[smooth manifold|smooth]] [[orientable]] [[closed manifold|closed]] [[spin manifold|spin]] [[4-manifold]] $M$, hence with vanishing second [[Stiefel-Whitney class]] $w_2(M)=0$, one has:
$$
\sigma(M)
\equiv 0 mod 16.
$$

## Generalizations

### Kervaire-Milnor theorem

\begin{proposition}
**(Kervaire-Milnor theorem)**
For a [[smooth manifold|smooth]] [[compact]] [[4-manifold]] $M$ and a characteristic sphere $S^2\hookrightarrow M$, one has:
$$
\sigma(M)
=S^2\cdot S^2 mod 16.
$$
\end{proposition}
A characteristic sphere $i\colon S^2\hookrightarrow M$ represents the second [[Stiefel-Whitney class]] $w_2(TM)=PD(i_*[S^2])\in H^2(M,\mathbb{Z}_2)$ using [[Poincaré duality]] $PD\colon H_2(M,\mathbb{Z}_2)\rightarrow H^2(M,\mathbb{Z}_2)$ and the [[fundamental class]] $[S^2]\in H_2(S^2,\mathbb{Z}_2)\cong\mathbb{Z}_2$, which is the unique generator.

### Freedman-Kirby theorem

\begin{proposition}
**(Smooth Freedman-Kirby theorem)**
For a [[smooth manifold|smooth]] [[compact]] [[4-manifold]] $M$ and a characteristic surface $\Sigma\hookrightarrow M$, one has:
$$
\sigma(M)
=\Sigma\cdot\Sigma
+8 Arf(M,\Sigma) mod 16
$$
with the [[Arf invariant]].
\end{proposition}
A characteristic surface $i\colon\Sigma\hookrightarrow M$ represents the second [[Stiefel-Whitney class]] $w_2(TM)=PD(i_*[\Sigma])\in H^2(M,\mathbb{Z}_2)$ using [[Poincaré duality]] $PD\colon H_2(M,\mathbb{Z}_2)\rightarrow H^2(M,\mathbb{Z}_2)$ and the [[fundamental class]] $[\Sigma]\in H_2(\Sigma,\mathbb{Z}_2)\cong\mathbb{Z}_2$, which is the unique generator.
\begin{proposition}
**(Topological Freedman-Kirby theorem)**
For a [[topological manifold|topological]] [[compact]] [[4-manifold]] $M$ and a characteristic surface $\Sigma\hookrightarrow M$, one has:
$$
\sigma(M)
=\Sigma\cdot\Sigma
+8 Arf(M,\Sigma)
+8 KS(M) mod 16
$$
with the [[Arf invariant]] and [[Kirby-Siebenmann invariant]].
\end{proposition}

## References

See also:

* Wikipedia, _[Rokhlin's theorem](https://en.wikipedia.org/wiki/Rokhlin%27s_theorem)_

[[!redirects Kervaire-Milnor theorem]]
[[!redirects Freedman-Kirby theorem]]