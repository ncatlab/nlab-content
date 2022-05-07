

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[unitary group]] on an infinite-dimensional [[separable Hilbert space|separable]] [[complex vector space|complex]] [[Hilbert space]] $\mathcal{H}$ is traditionally denoted $U(\mathcal{H})$. It does not quite have an established prose name, but is often referred to by some combination of the words "unitary group" and "strong topology".

Its [[quotient]] by the [[circle group|circle]] [[subgroup]] [[U(1)]] is the corresponding [[projective unitary group]] [[PU(ℋ)]].

## Definition
 {#Definition}

Throughout, let $\mathcal{H}$ be any [[separable Hilbert space|separably]] infinite-dimensional [[complex numbers|complex]] [[Hilbert space]].

\begin{definition}\label{TheTopologies}
The set $B(\mathcal{H})$ of [[bounded operators]] carries the following [[topological space|topologies]], characterized by the conditions under which a [[sequence]] $\{ T_k \,\in\, B(\mathcal{H}) \}_{k \in \mathbb{N}}$ [[convergence|converges]] to a fixed operator $T \,\in\, B(\mathcal{H})$:

The [[limit of a sequence|limit]] of this sequence is $\underset{k \to \infty}{lim} T_k \;=\; T$

* {#NormTopology} ...in the **[[norm topology]]** or *[[topology of uniform convergence]]* if
   
  $$
    \underset{
      { x \in \mathcal{H} }
      \atop
      { \vert x \vert \leq 1 }
    }{sup}
    \big(
      \vert T_k(x) - T(x)
    \big)
    \;\to\; 0
    \,;
  $$

* {#StrongOperatorTopology} ...in the **[[strong operator topology]]** or *[[topology of pointwise convergence]]* if

  $$
    \underset{ x \in \mathcal{H} }{\forall}  \; T_k(x) \to T(x)
    \,;
  $$

* {#WeakOperatorTopology} ...in the **[[weak operator topology]]** if

  $$
    \underset{ x, y \in \mathcal{H}  }{\forall}
    \;
    \big\langle
      T_k(x), \, y
    \big\rangle
    \to
    \big\langle
      T_k(x), \, y
    \big\rangle
    \,;
  $$

* {#CompactOpenTopology} ...in the **[[compact-open topology]]** if

  uniform convergence [above](#NormTopology) holds for the restrictions $T_k\vert_{C}$ and $T\vert_C$ to any [[compact subset]] $C \subset \mathcal{H}$.

\end{definition}
(This list follows [Espinoza & Uribe 2014, p. 2](#EspinozaUribe14).)


## Properties


\begin{prop}\label{WithNormTopology}
  The [norm topology](#NormTopology) makes $U(\mathcal{H})$ a [[topological group]], in fact a [[Banach Lie group]].
\end{prop}
(e.g. [Schottenloher 2013 p. 4/Sec. 3](#Schottenloher13))

\begin{prop}\label{WithOperatorTopology}
  On $U(\mathcal{H})$ the [weak operator topology](#WeakOperatorTopology) and [strong operator topology](#StrongOperatorTopology) agree and make it a [[topological group]].
\end{prop}
([Hilgert & Neeb 1993, Cor. 94](#HilgertNeeb93); [Schottenloher 2013, Prop. 1](#Schottenloher13); [Espinoza & Uribe 2014, Lem. 1.5](#EspinozaUribe14))

\begin{prop}\label{WithNormTopology}
  The [compact-open topology](#CompactOpenTopology) coincides with the [strong operator topology](#StrongOperatorTopology)
\end{prop}
([Schottenloher 2013 Prop. 2](#Schottenloher13); [Espinoza & Uribe 2014, Lem. 1.8](#EspinozaUribe14))

\begin{prop}
  The [norm topology](#NormTopology) on $U(\mathcal{H})$ (from Prop. \ref{WithNormTopology}) is strictly finer than the (weak or strong) [[operator topology]] (from Prop. \ref{WithOperatorTopology}).
\end{prop}
(e.g. [Espinoza & Uribe 2014, p. 5-6](#EspinozaUribe14), see also [Schottenloher 2013, p. 4](#Schottenloher13))

In **summary**:

\[
  \label{DiagramOfAllTheTopologies}
  U(\mathcal{H})_{norm}
    \xrightarrow{ \;\;\; \neq \;\;\; }
  U(\mathcal{H})_{strong}
    \overset{ \phantom{AA} = \phantom{AA} }{\leftrightarrow}
  U(\mathcal{H})_{weak}  
    \overset{ \phantom{AA} = \phantom{AA} }{\leftrightarrow}
  U(\mathcal{H})_{compop}  
\]

(also [Espinoza & Uribe 2014, Thm. 1.2](#EspinozaUribe14))

\begin{prop}
  Equipped with the strong topology (Prop. \ref{WithOperatorTopology}), $U(\mathcal{H})$ 
is [[complete metric space|completely metrizable]].
\end{prop}
([Neeb 1997, Prop. II.1](#Neeb97), [Schottenloher 2013 Prop. 3](#Schottenloher13), [Espinoza & Uribe 2014, Lem. 1.6](#EspinozaUribe14))

\begin{prop}
  Equipped with the strong topology (Prop. \ref{WithOperatorTopology}), $U(\mathcal{H})$ 
is *not* [[locally compact topological space|locally compact]].
\end{prop}
([Grigorchuk & de la Harpe 2014, Sec. 5](#GrigorchukHarpe2014))


\begin{theorem}\label{KuiperTheorem}
**(Kuiper's theorem)**
\linebreak
The [[topological group|topological]] [[unitary group]] [[U(ℋ)|$\mathrm{U}(\mathcal{H})$]] in either the

* [norm topology](#NormTopology) 

or the

* [strong operator topology](#StrongOperatorTopology)

* [weak operator topology](#WeakOperatorTopology)

* [compact-open topology](#CompactOpenTopology)

is [[contractible]] in that there is a [[left homotopy]] between the [[identity]] $id \;\colon\; U(\mathcal{H}) \to U(\mathcal{H})$  and the [[constant function]] $const_{\mathrm{e}} \;\colon\; U(\mathcal{H}) \to U(\mathcal{H})$.
\end{theorem}
See the [references](Kuiper's+theorem#References) at *[[Kuiper's theorem]]*.


\begin{proposition}\label{UHCircleFiberBundle}
  The [[U(1)]]-[[quotient space]] [[coprojection]] of [[U(ℋ)]]  over [[PU(ℋ)]] -- both in their strong [[operator topology]] -- is a [[circle group|circle]]-[[principal bundle]]:
$$
  \array{
    S^1 &\hookrightarrow& \mathrm{U}(\mathcal{H})
    \\
    && \big\downarrow
    \\
    && PU(\mathcal{H})
    \mathrlap{ \; \simeq \; \mathrm{U}(\mathcal{H})/S^1 }
  }
$$
\end{proposition}
([Simms 1970, Thm. 1](#Simms70))
\begin{remark}
  Prop. \ref{UHCircleFiberBundle} means in particular that $\mathrm{U}(\mathcal{H}) \xrightarrow{\;} PU(\mathcal{H})$ is [[locally trivial bundle|locally trivial]], hence that the [[coset space]] [[coprojection]] $\mathrm{U}(\mathcal{H}) \xrightarrow{\;} \mathrm{U}(\mathcal{H})/S^1$ admits [[local sections]]. See also at *[[coset space coprojection admitting local sections]]*.
\end{remark}

## Related concepts

* [[stable unitary group]]

* [[PU(ℋ)]]

* [[universal equivariant PU(ℋ)-bundle]]


## References

Early discussion in relation to [[PU(ℋ)]]:

* {#Simms70} [[David John Simms]], *Topological aspects of the projective unitary group*, Math. Proc. Camb. Phil. Soc. **68** 1 (1970) 57-60  ([doi:10.1017/S0305004100001043](https://doi.org/10.1017/S0305004100001043))

Proof that the the weak- and strong- [[operator topologies]] agree on $U(\mathcal{H})$:

* {#HilgertNeeb93} [[Joachim Hilgert]], [[Karl-Hermann Neeb]], Cor. 9.4 in: *Lie Semigroups and their Applications*. Lecture Notes in Mathematics **1552**, Springer 1993 ([doi:10.1007/BFb0084640](https://link.springer.com/book/10.1007/BFb0084640))


Proof that weak-, strong- as well as the [[compact-open topology]] all agree on $U(\mathcal{H})$:

* {#Schottenloher13} [[Martin Schottenloher]], _The Unitary Group In Its Strong Topology_ ([arXiv:1309.5891](https://arxiv.org/abs/1309.5891)), Advances in Pure Mathematics **08** 05 (2018) ([doi:10.4236/apm.2018.85029](https://www.scirp.org/html/4-5301487_84967.htm))

* {#EspinozaUribe14} [[Jesus Espinoza]], [[Bernardo Uribe]], _Topological properties of the unitary group_, JP Journal of Geometry and Topology **16** 1 (2014) 45-55 ([arXiv:1407.1869](https://arxiv.org/abs/1407.1869), [journal](http://www.pphmj.com/abstract/8730.htm))

Previous influential but wrong claim that they do not:

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], Appendix of: _Twisted K-theory_, Ukrainian Math. Bull. **1**, 3 (2004) ([arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf))

  > This paper made the mistake of assuming that because various topologies were distinct on $GL(\mathcal{H})$, they remain distinct on $U(\mathcal{H})$.

Further properties:

Proof of complete metrizability:

* {#Neeb97} [[Karl-Hermann Neeb]], *On a Theorem of S. Banach*, Journal of Lie Theory **8**  (1997) 293–300 ([pdf](https://www.heldermann-verlag.de/jlt/jlt07/NEEBPL.PDF))

Proof of failure of local compactness:

* {#GrigorchukHarpe2014} Rostislav Grigorchuk, Pierre de la Harpe, *Amenability and ergodic properties of topological groups: from Bogolyubov onwards*, in: *Groups, Graphs and Random Walks*, Cambridge University Press 2017 ([arXiv:1404.7030](https://arxiv.org/abs/1404.7030), [doi:10.1017/9781316576571.011]( https://doi.org/10.1017/9781316576571.011))

Proof of [[Kazhdan's property (T)]] for $U(\mathcal{H})$:

* [[Bachir Bekka]], *Kazhdan's Property (T) for the unitary group of a separable Hilbert space*, Geom. funct. anal. 13, 509–520 (2003) ([doi:10.1007/s00039-003-0420-0](https://doi.org/10.1007/s00039-003-0420-0))

    

[[!redirects U(H)]]
[[!redirects UH]]

[[!redirects infinite unitary group with strong topology]]



