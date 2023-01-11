
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _Fivebrane structure_ is the next higher analog of that of [[spin structure]] and [[string structure]].

Recall from the discussion there that a [[string structure]] on [[manifold]] $X$ with [[spin structure]] is a lift $\hat g$ of the classifying map $g : X \to B Spin(n)$ of the [[tangent bundle]] associated to a [[Spin group]]-[[principal bundle]] through the next step in the [[Whitehead tower]] of $O(n)$, called $B String(n)$ -- the [[delooping]] of the [[String group]]:

$$
  \array{
    && B String(n)
    \\
    & {\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& B Spin(n)
  }
  \,.
$$

The names "Spin" and "String" both derive from the role these structures play in [[quantum field theory]]: a [[spin structure]] is required on $X$ for it to serve as a target space for spinning particles (superparticles), while a [[string structure]] is required for it to serves as a target for "spinning strings" -- superstrings -- (see [[heterotic string theory]] for more).
Topologists just say (said) $O(n)\langle 2\rangle$ for $Spin(n)$ and $O(n)\langle 6\rangle$ for $String(n)$, respectively. 

They wrote $O(n)\langle 8\rangle$ for the next step in the [[Whitehead tower]] of $O(n)$ (note that this is only the _next_ step for $n \gt 6$; for lower $n$ there are intermediate steps, as can be seen in the table at [orthogonal group](orthogonal+group#HomotopyGroups)).

It was [[Hisham Sati]] who first realized that a lift of the [[tangent bundle]] $T X$ to this highly connected structure group is related to $X$ serving as a target for "spinning 5-branes" -- super-5-branes -- in what is called [[dual heterotic string theory]]. Following the history of the term [[String group]] he gave the topological group $O(n)\langle 8\rangle$ the name [[Fivebrane group]]:  $Fivebrane(n)$.

Accordingly, a **Fivebrane structure(n)** on a manifold $X$ with [[string structure]] is a lift of $\hat g : X \to B String(n)$ to $\hat \hat g$

$$
  \array{
    && B Fivebrane(n)
    \\
    & {\hat \hat g}\nearrow & \downarrow
    \\
    X &\stackrel{\hat g}{\to}& B String(n)
  }
  \,.
$$

The obstruction class to this lift is a fractional multiply of the second [[Pontrjagin class]]. Namely the generator of $H^8(B String, \mathbb{Z})$ is $\frac{1}{6}p_2$, 

$$
  \array{
     B String &\stackrel{\frac{1}{6} p_2}{\to}& B^8 \mathbb{Z}
     \\
     \downarrow && \downarrow^{\mathrlap{\cdot 6}}
     \\
     B SO &\stackrel{p_2}{\to}& B^8 \mathbb{Z}
  }
  \,.
$$

(stated in [SSS2](#SSS2), then in [DHH](#DHH), also follows from the [[index theory]] argument leading to (3.3) in [Witten 96](#Witten96)).

The [[Fivebrane group]] is the [[loop space object]] of the corresponding [[homotopy fiber]]

$$
  \array{
    B Fivebrane &\to& * 
    \\
    \downarrow && \downarrow
    \\
    B String &\stackrel{\frac{1}{6} p_2}{\to}& B^7 U(1)&
  }
$$

and so, by the [[universal property]] of the [[homotopy pullback]], String-structures $\hat g$ lift to Fivebrane structures precisely if $\frac{1}{6}p_2(\hat g)$ is trivial in [[cohomology]]

$$
  \array{
    && B Fivebrane &\to& * 
    \\
    & {}^{\mathllap{\hat \hat g}}\nearrow & \downarrow && \downarrow
    \\
    X &\stackrel{\hat g}{\to}& B String &\stackrel{\frac{1}{6}p_2}{\to}& B^7 U(1)
  }
  \,.
$$

In ([SSS2](#SSS2)) the physical interpretation of this topological lift was established by comparison with known [[quantum anomaly]] cancellation conditions in [[dual heterotic string theory]].

The term "Fivebrane" apparently quickly caught on in the mathematical community, for instance in ([DouglasHenriquesHill](#DHH)).

Since [[gauge theory]] is not just about [[principal bundle]]s, but about principal [[connection on a bundle|bundles with connection]], what matters in physics is not just the topological Spin-, String- and Fivebrane structures, but their refinement to [[schreiber:differential nonabelian cohomology]]. See [[differential fivebrane structure]].

## Related concepts

* [[spin structure]], [[spin connection]];

* [[string structure]], [[differential string structure]];

* **fivebrane structure**, [[differential fivebrane structure]]

[[!include higher spin structure - table]]

## References

The notion was introduced in:

* {#SSS2} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Fivebrane structures]]_, Reviews in Mathematical Physics, **21** 10 (2009) 1197-1240 &lbrack;[arXiv:0805.0564](http://arxiv.org/abs/0805.0564), [doi:10.1142/S0129055X09003840](https://doi.org/10.1142/S0129055X09003840)&rbrack;
 

Brief mentioning in:

* {#DHH} [[Chris Douglas]], [[André Henriques]], [[Michael Hill]], *Homological obstructions to string orientations*, Int. Math. Res. Notices **18** (2011) 4074-4088 &lbrack;[arXiv:0810.2131](http://arxiv.org/abs/0810.2131), [doi:10.1093/imrn/rnq237](https://doi.org/10.1093/imrn/rnq237)&rbrack;

On the differential refinement (the fivebrane version of [[differential string structure]]): 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]],  _[[schreiber:Twisted Differential String and Fivebrane Structures]]_ &lbrack;[arXiv:0910.4001](http://arxiv.org/abs/0910.4001)&rbrack;

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_ &lbrack;[arXiv:1011.4735](http://arxiv.org/abs/1011.4735)&rbrack;

The [[M-theory|M-theoretic]] version of Fivebrane structure ("[[M5-brane]]-structure"), and rigorously derived from 5-brane anomaly cancellation via [[schreiber:Hypothesis H]]:

* [[Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]]: Exp. 3.2, Rem. 4.3, Thm. 4.8 in: *Twisted Cohomotopy implies level quantization of the full 6d Wess-Zumino-term of the M5-brane*, Comm. Math. Phys. **384** 403–432 (2021) &lbrack;[arXiv:1906.07417](https://arxiv.org/abs/1906.07417), [doi:10.1007/s00220-021-03951-0](https://doi.org/10.1007/s00220-021-03951-0)&rbrack;

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: around (12) in *Twisted cohomotopy implies twisted String structure on M5-branes*, J. Mathematical Physics **62** (2021) 042301 &lbrack;[arXiv:2002.11093](https://arxiv.org/abs/2002.11093), [doi:10.1063/5.0037786](https://doi.org/10.1063/5.0037786)&rbrack; 


Applications of Fivebrane structures:

* Boris Botvinnik, [[Mohammed Labbi]], _Highly connected manifolds of positive $p$-curvature_, Transactions of the AMS, Trans. Amer. Math. Soc. 366 (2014), 3405-3424 &lbrack;[arXiv:1201.1849](http://arxiv.org/abs/1201.1849), [doi:10.1090/S0002-9947-2014-05939-4](https://doi.org/10.1090/S0002-9947-2014-05939-4)&rbrack;

[[!redirects fivebrane structure]]

[[!redirects Fivebrane structures]]
