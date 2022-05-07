
\begin{prop}\label{PontrajginDualOfCompactGroupAsSecondGroupCohomologyGroup}
  **(Pontrjagin dual of compact group as second group cohomology group)**
  \linebreak
  If $G$ is a [[finite group]] (more generally: a [[compact Lie group]]) then its Pontrjagin dual is equivalently its [[cohomology group]] in degree-2 [[group cohomology]] (more generally: refined [[Lie group cohomology]]) with [[integer]] [[coefficients]]:
  $$
    \widehat{G}
    \;\simeq\;
    H^2_{grp}
    \big(
      G
      ;\,
      \mathbb{Z}
    \big)
    \;=\;
    H^2
    \big(
      B G
      ;\,
      \mathbb{Z}
    \big)
    \,.
  $$
\end{prop}
\begin{proof}
  The key point is that, by assumption on $G$, we have
  \[
    \label{RealGroupCohomologyOfCompactGroupVanishes}
    H^{\bullet \geq 1}_{grp}
    \big(
      G;\, \mathbb{R} 
    \big)
    \;=\;
    0
    \,.
  \]

Using this, the conclusion is obtained as follows:
The defining [[short exact sequence]] of [[groups]]
$$
  \mathbb{Z} \xhookrightarrow{\;} \mathbb{R} \twoheadrightarrow S^1
$$
extends to a [[homotopy fiber sequence]] of [[2-groups]] (and further of [[n-groups]])
$$
  \mathbb{Z}
    \xrightarrow{\;\;}
  \mathbb{R}
    \xrightarrow{\;\;}
  S^1 
    \xrightarrow{\;\;} 
  B \mathbb{Z}
    \xrightarrow{\;\;} 
  B \mathbb{R}
    \xrightarrow{\;\;} 
  \cdots
  \,.
$$

This induces a [[long exact sequence]] of [[cohomology groups]] induced from the [[long exact sequence of homotopy groups]] of image under this fiber sequence under the [[derived hom-space]] $\mathbf{H}(B G,-) \coloneqq Maps(B G;\, -)$:
$$
  \array{
  \cdots
  &\to&
  \pi_1
  \left(
    \mathbf{H}(B G, \, B^2 \mathbb{R})
  \right)
  &\xrightarrow{\;\;}&
  \pi_1
  \left(
    \mathbf{H}(B G, \, B^2 S^1)
  \right)
  &\xrightarrow{\;\;}&
  \pi_0
  \left(
    \mathbf{H}(B G, \, B^2 \mathbb{Z})
  \right)
  &\xrightarrow{\;\;}&
  \pi_0
  \left(
    \mathbf{H}(B G, \, B^2 \mathbb{R})
  \right)
  &\to&
  \cdots
  \\
  &&
  =
  &&
  =
  &&
  =
  &&
  =
  \\
  \cdots
  &\to&
  \underset{
    = 0
  }{
  \underbrace{
  H^1
  \big(
    B G
    \;,
    \mathbb{R}
  \big)
  }
  }
  &\xrightarrow{\;\;}&
  H^1
  \big(
    B G
    \;,
    S^1
  \big)
  &\xrightarrow{\;\simeq\;}&
  H^2
  \big(
    B G
    \;,
    \mathbb{Z}
  \big)
  &\xrightarrow{\;\;}&
  \underset{
    = 0
  }{
  \underbrace{
  H^2
  \big(
    B G
    \;,
    \mathbb{R}
  \big)
  }
  }
  &\to&
  \cdots
  \,.
  }
$$
Using the assumption (eq:RealGroupCohomologyOfCompactGroupVanishes) under the braces, this implies the middle isomorphism, as shown.

Now the claim follows by re-expressing $H^1(G;\, S^1)$ as follows:

$$
  \begin{aligned}
  H^2(B G;\, \mathbb{Z})
  \;\simeq\;
  H^1(B G;\, S^1)
  &
  \;\simeq\;
  \pi_0 \mathbf{H}\big( B G, \, B S^1 \big)
  \\
  &
  \;\simeq\;
  \pi_0 Groupoids\big( G \rightrightarrows \ast, \, S^1 \rightrightarrows \ast \big)
  \\
  & \;\simeq\;
  \pi_0 
  \Big(
    Groups\big(G,S^1\big) \sslash S^1
  \Big)
  \\
  & \;\simeq\;
  \pi_0 
  \Big(
    Groups\big(G,\,S^1\big) \times B S^1
  \Big)
  \\
  & \;\simeq\;
  Groups(G,S^1)
  \;\simeq\;
  \widehat G
  \,,
  \end{aligned}
$$
where the last step uses that the [[circle group]], being [[abelian]], has [[trivial action|trivial]] [[conjugation action]] on the [[hom-set]] of [[group homomorphisms]].
\end{proof}


$$
    \left(
      \big(
        \mathcal{B} PU(\mathcal{H})
      \big)^H
    \right)
$$

[[higher gauge theory of the Green-Schwarz mechanism -- references]]

$\infty$

$$
  \langle{g}\rangle 
    \hookrightarrow 
  C_G(g)
    \twoheadrightarrow 
  G/\langle{g}\rangle
$$

$$
  \array{
    B \langle{g}\rangle
    &\longrightarrow& 
    \ast
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    X^g \!\sslash\! C_G(g)
    &\xrightarrow{\;}&
    X^g \!\sslash\! \frac{C_G(g)}{\langle{g}\rangle}
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    B G
    &\xrightarrow{\;}&
    B \frac{C_G(g)}{\langle{g}\rangle}
  }
$$

$$
  \array{
    (W H) / H
    &\longrightarrow&
    (Y \times \overline{W} G)/G
    \\
    && \big\downarrow
    \\
    &&
    \big(Y \times \overline{W} (G/H) \big) / (G/H)      
  }
$$


$$
 \begin{array}{cc}
  a & b
 \end{array}
$$

* Let $G$ be a [[finite group]].

  * For $g \in G$ any [[element]], write $C_G(g) \,\subset\, G$ for [[centralizer subgroup]].

  * Write $C_G(g) \times \mathbb{Z}$ for the [[direct product group]] with the additive [[abelian group]] of [[integers]].

* Let $X \in G Actions(SmthMfds)$ be a proper smooth [[G-manifold]], hence a [[smooth manifold]] equipped with a [[proper action]] (from the right, say) of $G$ by [[diffeomorphisms]].

  * Notice that for $g \in G$ the [[fixed locus]] 

    $$
      X^g \xhookrightarrow{\;i_g\;} X
    $$ 

    is a smooth [[submanifold]] (by [this Prop.](equivariant+differential}topology#FixedLociOfSmoothProperActionsAreSubmanifolds)).

For $g \in G$ consider the right [[group action]] of the [[direct product group]] $C_G(g) \times \mathbb{Z}$ on the [[fixed locus]] $X^g$ given by

\[
  \label{ActionOfCentralizerTimesIntegersOnFixedLocus}
  \array{
    X^g \times C_G(g) \times \mathbb{Z}
    &\xrightarrow{\;\;\;\;}&
    x
    \\
    \big(
      x, \, (h, n)
    \big)
    &\mapsto&
    x \cdot h \cdot g^n
    \mathrlap{\,.}
  }
\]

and notice that the following [[function]] is a [[group homomorphism]] (by the fact that all elements of $C_G(g)$ commute with $g$ in $G$):

\[
  \label{GroupHomomorphismFromCentralizerTimesIntegersIntoG}
  \array{
    C_G(g) \times \mathbb{Z}
    &\xrightarrow{\;\;\phi_g\;\;}&
    G
    \\
    (h,n) &\mapsto& h \cdot g^n
    \mathrlap{\,.}
  }
\]

In view of the action (eq:ActionOfCentralizerTimesIntegersOnFixedLocus), the homomorphism (eq:GroupHomomorphismFromCentralizerTimesIntegersIntoG) induces a map of [[Borel constructions]]

$$
  \big(
    X^g \sslash C_G(g)
    \times 
    B \mathbb{Z}
  \big)
  \;\simeq\;
  X^g 
    \sslash   
  \big(
    C_G(g) \times \mathbb{Z}
  \big)
  \xrightarrow{ \;\; i_g \sslash \phi_g \;\; }
  X 
    \sslash 
  G
  \,,
$$

(where the [[homotopy equivalence]] shown on the left follows since the [[group action]] of  $\mathbb{Z}$ on $X^g$ is the [[trivial action]], by definition (eq:ActionOfCentralizerTimesIntegersOnFixedLocus), and using that the [[Borel construction]] on a point is the [[classifying space]] $ \ast \sslash \mathbb{Z} \,\simeq\, B \mathbb{Z} \simeq S^1$, hence the [[circle]], in the present case)

and hence the corresponding [[pullback in cohomology|pullback in]] [[integral cohomology]]:

\[
  \label{PullbackInCohomologyAlongMorphismOfBorelConstructions}
  \begin{array}{rrl}
  H^\bullet
  \big(
    X \sslash G
    \;
    \, 
    \mathbb{Z}
  \big)
  &
  \xrightarrow{ \; (i_g \sslash \phi_g)^\ast \; }
  & 
  H^\bullet
  \big(
    ( X^g \sslash C_G(g) )
    \times
    B \mathbb{Z}
    \;
    \, 
    \mathbb{Z}
  \big)
  \\
  &
  \,\simeq\,
  &
  H^\bullet
  \big(
    ( X^g \sslash C_G(g) )
    \;
    \, 
    \mathbb{Z}
  \big)
    \otimes_{\mathbb{Z}}
  \underset{
    \mathclap{
      \simeq 
      \left\{
      \array{
        \mathbb{Z} &\vert& \bullet \in \{0,1\}
        \\
        0 &\vert& else
      }
      \right.
    }
  }{
    \underbrace{
      H^\bullet
      \big(
        B \mathbb{Z}
        ;\,
        \mathbb{Z}
      \big)
    }
  }
  \\
  &\simeq &
  H^\bullet
  \big(
    ( X^g \sslash C_G(g) )
    \;
    \, 
    \mathbb{Z}
  \big)
  \,\oplus\,
  H^{\bullet-1}
  \big(
    ( X^g \sslash C_G(g) )
    \;
    \, 
    \mathbb{Z}
  \big)
  \,,
  \end{array}
\]

where the second line uses the [[Künneth theorem]].

(The following definition becomes a proposition if one uses conceptualization of [[transgression]] as laid out in *[[transgression in group cohomology]]*.)

\begin{definition}\label{TransgressionOntoFixedLocus}
  For $g \in G$ write 
  $$
    \tau_g
    \;\colon\;
    H^\bullet
    \big(
      X \sslash G
      \;
      \, 
      \mathbb{Z}
    \big)
    \xrightarrow{\;\;}
    H^{\bullet-1}
    \big(
      ( X^g \sslash C_G(g) )
      \;
      \, 
      \mathbb{Z}
    \big)
  $$ 
  for the [[composition|composite]] of (eq:PullbackInCohomologyAlongMorphismOfBorelConstructions) with [[projection]] onto the second [[direct sum|direct summand]].
\end{definition}

\begin{prop}
  The [[image]] of the transgression map $\tau_g$ (Def. \ref{TransgressionOntoFixedLocus}) is in the [[torsion subgroup]].
\end{prop}
\begin{proof}
  The group homomorphism (eq:GroupHomomorphismFromCentralizerTimesIntegersIntoG) factors through the [[cyclic group]] $\mathbb{Z} \to \langle g\rangle \to G$ which is generated by $g \in G$. By the assumption that $G$ is a [[finite group]], so that its [[integral cohomology]] is entirely torsion. Since the transgression map factors through a tensor product with pullback along this factorization, by definition, the claim follows. 
\end{proof}


* $\mathcal{X}$ an [[orbifold]], 

* $\tau \,\in\, H^3\big( &#643;\subset(\mathcal{X}); \, \mathbb{Z} \big) $ a class in the degree-3 [[integral cohomology]] of its [[geometric realization]];

* 


$\epsilon$

$\ldots$

[$[14]$](mass+gap#JaffeWitten00)

$\doubleheadarrow$

$\rfloor$ $\lfloor$

[[Skyrmions from rational maps -- references]]

* [[A. N. Schellekens]], [[Nicholas P. Warner]], *Anomalies, characters and strings*, Nuclear Physics B Volume 287, 1987, Pages 317-361 (<a href="https://doi.org/10.1016/0550-3213(87)90108-8">doi:10.1016/0550-3213(87)90108-8</a>)

* [[A. N. Schellekens]], [[Nicholas P. Warner]], *Anomalies and modular invariance in string theory*, Physics Letters B 177 (3-4), 317-323, 1986 (<a href="https://doi.org/10.1016/0370-2693(86)90760-4">doi:10.1016/0370-2693(86)90760-4</a>)

* [[Wolfgang Lerche]], [[Bengt Nilsson]], [[A. N. Schellekens]],  [[Nicholas P. Warner]], *Anomaly cancelling terms from the elliptic genus*, Nuclear Physics B Volume 299, Issue 1, 28 March 1988, Pages 91-116 (<a href="https://doi.org/10.1016/0550-3213(88)90468-3">doi:10.1016/0550-3213(88)90468-3</a>)


