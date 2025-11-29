We want to re-prove that:

\begin{proposition}
\label{FundamentalGroupOfMapsFromTorusToSphere}
 The [[fundamental group]] of the [[mapping space]] from the [[2-torus]] to the [[2-sphere]] is the [[integer Heisenberg group]] at level=2:
$$
  \pi_1 Map(T^2, S^2)
  \;\simeq\;
  \widehat{\mathbb{Z}^2}
  \,,
$$
\end{proposition}
Here the [[underlying set]] is
$$
  \widehat{\mathbb{Z}^2} 
  \;\coloneqq_{Set}\;
  \mathbb{Z}^2 \times \mathbb{Z}
$$
with generators
\[
  \label{GeneratorsOfIntegerHeisenbergGroup}
  \begin{aligned}
  W_a 
    &\coloneqq 
  \big((1,0),0\big) \in \mathbb{Z}^2 \times \mathbb{Z}
  \\
  W_b 
    &\coloneqq
  \big((0,1),0\big) \in \mathbb{Z}^2 \times \mathbb{Z}
  \\
  \zeta
    &\coloneqq
  \big((0,0),1\big) \in \mathbb{Z}^2 \times \mathbb{Z}
  \end{aligned}
\] 
whose single nontrivial [[group commutator]] is
$$
  [W_a, W_b] \,=\, \zeta^2
  \mathrlap{\,.}
$$

We will prove this proposition after establishing a couple of simple lemmas and recalling a basic fact about the [[Whitehead bracket]] of $S^2$. To that end, write

* $T^2_+ \coloneqq T^2 \sqcup \ast$ for the result of freely adjoining a [[base point]],

  so that $Map(T^2, S^2) \simeq Map^\ast(T^2_+, S^2)$,

* $\Sigma \dashv \Omega$ for the [[reduced suspension]] $\dashv$ [[loop space]]-[[adjoint functor|adjunction]] on [[pointed topological spaces]],

* $\widetilde{f} \colon X \longrightarrow \Omega Y$ for the [[adjunct]] of a pointed map $\Sigma X \longrightarrow Y$ under this [[adjunction]].

\begin{lemma}
  The [[suspension]] of the torus is [[homotopy equivalence|homotopy equivalent]] to the [[wedge sum]]
\[
  \label{StableSplittingOfTorus}
  \Sigma T^2_+
  \;\underset{hmtp}{\simeq}\;
  S^1
    \vee
  S^2_a 
    \vee 
  S^2_b
    \vee
  S^3
  \mathrlap{\,.}
\]
\end{lemma}
Here the subscripts are just to [[indexed set|index]] [[wedge sum|wedge summands]] with corresponding projection maps
$$
  \begin{array}{ccc}
  \Sigma T^2_+ &\xrightarrow{ pr_a }& S^2_a,
  \,,
  \Sigma T^2_+ &\xrightarrow{ pr_b }& S^2_b,
  \,,
  \Sigma T^2_+ &\xrightarrow{ pr_c }& S^3
  \mathrlap{\,.}
  \end{array}
$$
\begin{proof}
The main point is, by *stable splitting of product spaces* (cf. [this Prop.](reduced+suspension#StableSplittingOfProductSpaces)),
that the reduced suspension of the pointed torus is:
$$
  \Sigma T^2 
  \;\simeq\;
  \Sigma(S^1 \times S^1)
  \underset{hmtp}{\simeq}
  \Sigma S^1 \vee \Sigma S^1 \vee \Sigma S^2
  \simeq
  S^2_a \vee S^2_b \vee S^3_c
  \mathrlap{\,.}
$$

From this the claim follows by
$$
  \Sigma(T^2_+)
  \simeq
  \Sigma(T^2 \vee S^0)
  \simeq
  \Sigma(T^2) \vee \Sigma(S^0)
  \simeq
  (S^2_a \vee S^2_b \vee S^3_c) \vee S^1
  \mathrlap{\,.}
$$
\end{proof}

As a corollary we obtain:
\begin{lemma}
The [[underlying set]] of the [[fundamental group]] of the [[mapping space]] from the [[2-torus]] to the [[2-sphere]] is:
$$
  \pi_1
  \mathrm{Map}\big(
    T^2
    ,\,
    S^2
  \big)
  \;\simeq_{Set}\;
  \mathbb{Z}^2 \times \mathbb{Z}
  \mathrlap{\,.}
$$  
\end{lemma}
\begin{proof}
Using (eq:StableSplittingOfTorus):
$$
  \begin{aligned}
  \pi_1
  \mathrm{Map}^\ast\big(
    T^2_+
    ,\,
    S^2
  \big)
  &
  \simeq
  \pi_0
  \mathrm{Map}^\ast\big(
    T^2_+
    ,\,
    \Omega
    S^2
  \big)
  \\
  &
  \simeq
  \pi_0
  \mathrm{Map}^\ast\big(
    \Sigma T^2_+
    ,\,
    S^2
  \big)
  \\
  & \simeq
  \pi_0
  \mathrm{Map}^\ast\big(
    S^2 \vee S^2 \vee S^3 \vee S^1
    ,\,
    \Omega
    S^2
  \big)
  \\
  & \simeq
  \pi_2(S^2)^2
    \times 
  \pi_3(S^2) 
    \times 
  \pi_1(S^2)
  \\
  & \simeq
  \mathbb{Z}^2 \times \mathbb{Z}
  \mathrlap{\,.}
  \end{aligned}
$$
In the last step we inserted the well-known [[homotopy groups of spheres|homotopy groups of]] the [[2-sphere]]. 
\end{proof}

For the generators of these homotopy groups, write:

* $\iota_n \,\coloneqq\, 1 \in \mathbb{Z} \simeq \pi_2(S^2)$

  (represented by the [[identity map]]),

* $\eta \,\coloneqq\, 1 \in \mathbb{Z} \simeq \pi_3(S^2)$

  (represented by the [[complex Hopf fibration]]).

\begin{lemma}
\label{SamelsonProductInOmegaOfSphere}
The [[Whitehead bracket]] on $\pi_\bullet(S^2)$ satisfies
\[
  \label{WhiteheadBracketInS2}
  \big[
    \iota_2
    ,\,
    \iota_2
  \big]
  =
  2 \eta
  \,.
\]
Under the [[isomorphism]]
$$
  \tau
  \;\colon\;
  \pi_{\bullet+ 1}(S^2)
  \xrightarrow{ \sim }
  \pi_\bullet(\Omega S^2)
$$
this is the [[Samelson product]] $\langle -,-\rangle$ on $\pi_\bullet(\Omega S^2)$, given by the [[group commutator]] of the [[grouplike space]] $\Omega S^2$:
$$
  \big\langle
    \tau \iota_2,
    \tau \iota_2
  \big\rangle
  \,=\,
  2 \tau[\iota_2, \iota_2]
  \,=\,
  2 \tau \eta
  \mathrlap{\,.}
$$
\end{lemma}
For the first statement see at *[[Whitehead bracket]]* ([this example](Whitehead+product#WhiteheadProductCorrespondingToComplexHopfFibration)), for the second see at *[[Samelson product]]*.

Now we are ready for the proof:

\begin{proof}
of Prop. \ref{FundamentalGroupOfMapsFromTorusToSphere}.

The group generators (eq:GeneratorsOfIntegerHeisenbergGroup) 
are evidently represented by
$$
  \begin{array}{ccc}
    \mathbb{Z}^2 \times \mathbb{Z}
    &\xrightarrow{ \phantom{-} \sim \phantom{-} }&
    \pi_1 Map^\ast\big(T^2_+, S^2\big)
    \\
    W_a &\mapsto& pr_a^\ast \iota_2\,,
    \\
    W_b &\mapsto& pr_b^\ast \iota_2\,,
    \\
    \zeta &\mapsto& pr_c^\ast \eta\,.
  \end{array}
$$
and the group commutator $[W_a, W_b]$ is represented by the [[Samelson product]] map:
$$
  T^2_+
  \xrightarrow{ diag }
  T^2_+ 
    \wedge 
  T^2_+ 
  \xrightarrow{ 
    (pr_a)_+ 
    \wedge
    (pr_b)_+
  }
  S^1 \wedge S^1
  \xrightarrow{  \widetilde{id} \wedge \widetilde{id}  }
  (\Omega S^2) 
    \wedge 
  (\Omega S^2)
  \xrightarrow{ \langle-,-\rangle }
  \Omega S^2
  \mathrlap{\,.}
$$


By Lem. \ref{SamelsonProductInOmegaOfSphere}, the second half of this composite map represents
$$
  \big\langle \tau(\iota_2), \tau(\iota_2) \big\rangle
  \,=\,
  \tau [\iota_2, \iota_2] 
  \,=\,
  2 \tau(\eta)
  \mathrlap{\,,}
$$
while the first half is clearly [[homotopy|homotopic]] to $pr_c$, whence $[W_a, W_b]$ is represented by
$$
  T^2_+
  \xrightarrow{ pr_c }
  S^2
  \xrightarrow{ 2\widetilde{\eta} }
  \Omega S^2
  \mathrlap{\,.}
$$
This shows that
$$
  [W_a, W_b] = \zeta^2
  \,.
$$

To conclude it is now sufficient to see that $\zeta$ is [[center|central]]. But the group commutator $[W_a, \zeta]$ is represented by
$$
  T^2_+
  \xrightarrow{ diag }
  T^2_+ 
    \wedge 
  T^2_+ 
  \xrightarrow{ 
    (pr_a)_+ 
    \wedge
    (pr_c)_+
  }
  S^1 \wedge S^2
  \xrightarrow{  \widetilde{id} \wedge \widetilde{\eta}  }
  (\Omega S^2) 
    \wedge 
  (\Omega S^2)
  \xrightarrow{ \langle-,-\rangle }
  \Omega S^2
  \mathrlap{\,,}
$$
where the first part of this map is [[null homotopy|null-homotopic]], since $\pi_0 Map^\ast(T^2_+, S^3) = \ast$ (e.g. by the [[cellular approximation theorem]]). Analogously we have $[W_b, \zeta] = \mathrm{e}$.
\end{proof}

\begin{remark}
This proof strategy immediately generalizes to a computation of
$$
  \pi_1 Map\big(
    (S^{2k+1})^2
    ,
    S^{2k+2}
  \big)
$$
for all $k \in \mathbb{N}$. For example, for $k = 1$ it yields
$$
  \pi_1 Map\big(
    (S^3)^2
    ,
    S^4
  \big)
  \;\simeq\;
  \widehat{\mathbb{Z}^2}
  \times
  \mathbb{Z}_{12}
  \mathrlap{\,.}
$$
\end{remark}
