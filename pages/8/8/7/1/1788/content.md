

$$
  \begin{aligned}
  \Delta(x,y)
  & \coloneqq
  \Delta_+(x,y) - \Delta_-(x,y)
  \\
  & =
      \left\{
       \array{
          \frac{+ i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
            \right)
          d^p \vec k
          & \vert & \text{if} \,  + (x^0 - y^0) \gt 0
          \\
          \frac{(-1) (-1) i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
            \right)
          d^p \vec k
          & \vert & \text{if} \,  - (x^0 - y^0) \gt 0
       }
     \right.
     \\
     & =
          \frac{+ i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
            \right)
          d^p \vec k
  \end{aligned}
$$


+-- {: .proof}
###### Proof

Consider two more Cauchy surfaces $\Sigma_p^\pm \hookrightarrow I^\pm(\Sigma) \hookrightarrow \Sigma$, in the [[future]] $I^+$ and in the [[past]] $I^-$ of $\Sigma$, respectively. Choose a [[partition of unity]] on $\Sigma$ consisting of two elements $\chi^\pm \in C^\infty(\Sigma)$ with [[support]] bounded by these Cauchy surfaces: $supp(\chi_\pm) \subset I^\pm(\Sigma^{\mp})$.

Then define

$$
  \label{SplittingOfGreenExactSequenceType}
  P_\chi 
    \;\colon\; 
  \Gamma_{\Sigma,scp}(E) 
    \longrightarrow 
  \Gamma_{\Sigma,cp}(E^\ast)
$$

by 

$$
  \label{SplittingOfGreenExactSequence}
  \begin{aligned}
    P_\chi(\Phi)
      & \coloneqq
    \phantom{-} P(\chi_+ \Phi) 
    \\
    & =
    -
    P(\chi_- \Phi)
    \,.
  \end{aligned}
$$

Notice that the [[support]] of the partitioned field history is in the compactly sourced future/past cone

$$
  \label{ChipmPhiIsSupportedInPastFuture}
  \chi_\pm  \Phi
  \;\in\;
  \Gamma_{\Sigma,\pm cp}(E)
$$

since $\Phi$ is supported in the compactly sourced causal cone, but that 
$P(\chi_\pm \Phi)$ indeed has [[compact support]] as required by (eq:SplittingOfGreenExactSequenceType): Since $P(\Phi) = 0$ by assumption the support is the intersection of that of $\Phi$ with that of $d \chi_\pm$, and the first is spacelike compact by assumption, while the latter is timelike compact, by definition of partition of unity.

Similarly, the equality in (eq:SplittingOfGreenExactSequence) holds because by [[partition of unity]] $P(\chi_+ \Phi) + P(\chi_-\Phi) = P((\chi_+ + \chi_-)\Phi ) = P(\Phi) = 0$.

It follows that 

$$
  \label{PchiIsRightInverseToGP}
  \begin{aligned}
    \mathrm{G}_P \circ P_\chi (\Phi)
    & =
    \left(
      \mathrm{G}_{P,+} - \mathrm{G}_{P,-}
    \right) P_\chi (\Phi)
    \\
    & =
    \underset{ = \chi_+ \Phi}{\underbrace{\mathrm{G}_{P,+} P(\chi_+ \Phi)}}
    +
    \underset{ = \chi_- \Phi }{\underbrace{\mathrm{G}_{P,-} P(\chi_- \Phi)}}
    \\
    & =
    (\chi_+ + \chi_-)\Phi
    \\
    & = 
    \Phi
    \,,
  \end{aligned}
$$

where in the second line we chose the two equivalent expressions (eq:SplittingOfGreenExactSequence) such that via (eq:ChipmPhiIsSupportedInPastFuture) the defining property of the [[advanced and retarded Green functions|advanced or retarded Green function]], respectively, may be applied, as shown under the braces.

([Khavkine 14, lemma 2.1](Green+hyperbolic+differential+equation#Khavkine14))

Now we apply this to the computation of $\omega_{\Sigma_p}(\mathrm{G}_P(-),-)$:

$$
  \begin{aligned}
    \omega_{\Sigma_P}(\mathrm{G}_P(\alpha^\ast),\vec \Phi)
    & =
    \underset{\Sigma_P}{\int}  K(\mathrm{G}_P(\alpha^\ast), \vec \Phi)
    \\
    & = 
    \underset{\Sigma_P}{\int}  K(\mathrm{G}_P(\alpha^\ast), \chi_+\vec \Phi)
     +
    \underset{\Sigma_P}{\int}  K(\mathrm{G}_P(\alpha^\ast), \chi_-\vec \Phi)
    \\
    & =
    \underset{I^-(\Sigma_P)}{\int}  d K(\mathrm{G}_P(\alpha^\ast), \chi_+\vec \Phi)
     -
    \underset{I^+(\Sigma_P)}{\int}  d K(\mathrm{G}_P(\alpha^\ast), \chi_-\vec \Phi)
    \\
    & =
    \underset{I^-(\Sigma_P)}{\int}  
    \left(
       \underset{= 0}{
       \underbrace{
       P(\mathrm{G}_P(\alpha^\ast))}} \cdot \chi_+\vec \Phi
       \mp   
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi)
    \right)
    dvol_\Sigma
    -
    \underset{I^+(\Sigma_P)}{\int}  
    \left(
       \underset{= 0}{
       \underbrace{
       P(\mathrm{G}_P(\alpha^\ast))}} \cdot \chi_-\vec \Phi
       \mp
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_- \vec \Phi)
    \right)
    dvol_\Sigma
    \\
    & =
    \mp
    \left(
    \underset{I^-(\Sigma_P)}{\int}  
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi)
    dvol_\Sigma
    +
    \underset{I^+(\Sigma_P)}{\int}  
       \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi)
     dvol_\Sigma
    \right)
    \\
    & = 
    \underset{\Sigma}{\int} \mathrm{G}_P(\alpha^\ast) \cdot P(\chi_+ \vec \Phi) dvol_\Sigma
    \\
    & =
    \underset{\Sigma}{\int} \alpha^\ast \cdot \mathrm{G}_{P} (P (\chi_+ \vec \Phi))
    \\
    & = 
    \underset{\Sigma}{\int} \alpha^\ast \cdot \vec \Phi
   \end{aligned}
$$

Here we computed as follows:

1. applied the assumption that $\omega_{\Sigma_p}(-,-) = \underset{\Sigma_p}{\int} K(-,-)$;

1. applied the above partition of unity;

1. used the [[Stokes theorem]] (prop. \ref{StokesTheorem}) for the past and the future of $\Sigma_p$, respectively;

1. applied the definition of $d K$ as the witness  of the formal (anti-) self-adjointness of $P$ (def. \ref{FormallyAdjointDifferentialOperators});

1. used $P\circ \mathrm{G}_p = 0$ on $\Gamma_{\Sigma,cp}(E^\ast)$ (def. \ref{AdvancedAndRetardedGreenFunctions}) and used (eq:SplittingOfGreenExactSequence);

1. unified the two integration domains, now that the integrands are the same;

1. used the formally (anti-)self adjointness of the Green functions (example \ref{CausalGreenFunctionOfFormallyAdjointDifferentialOperatorAreFormallyAdjoint});


1. used (eq:PchiIsRightInverseToGP).



=--