

$$
  H 
    \coloneqq
  B_{a b} \wedge e^a \wedge e^b
$$

$$
  \partial_{B_{ab}}\partial_{e^a}\partial_{e^b}
$$

$$
  \begin{aligned}
    & 
    \partial_{B_{a' b'}}\partial_{e^{a'}}\partial_{e^{b'}}
    B_{a b} \wedge e^a \wedge e^b\wedge (-)
    +
    B_{a b} \wedge e^a \wedge e^b\wedge 
    \partial_{B_{a' b' }}\partial_{e^{a'}}\partial_{e^{b'}}
    (-)
    \\
    & 
    =
    2
    \partial_{B_{a' b}}\partial_{e^{a'}}
    B_{a b} \wedge e^a \wedge (-)
    -
    \partial_{B_{a' b'}}\partial_{e^{a'}}
    B_{a b} \wedge e^a \wedge e^b\wedge \partial_{e^{b'}} (-)
    +
    B_{a b} \wedge e^a \wedge e^b\wedge 
    \partial_{B_{a' b'}}\partial_{e^{a'}}\partial_{e^{b'}}(-)
    \\
    & =
    -
    2
    \partial_{B_{a b}}
    B_{a b} \wedge  (-)
    +
    \underset{
      = 
      4
      \partial_{B_{a' b}}
      B_{a b} \wedge e^a\wedge \partial_{e^{a'}} (-)
    }{
    \underbrace{
    2
    \partial_{B_{a' b}}
    B_{a b} \wedge e^a\wedge \partial_{e^{a'}} (-)
    +
    2
    \partial_{B_{a b'}}
    B_{a b} \wedge e^b\wedge \partial_{e^{b'}} (-)
    }}
    +
    \partial_{B_{a' b'}}
    B_{a b} \wedge e^a \wedge e^b\wedge \partial_{e^{a'}}\partial_{e^{b'}} (-)
    +
    B_{a b} \wedge e^a \wedge e^b\wedge 
    \partial_{B_{a' b'}}\partial_{e^{a'}}\partial_{e^{b'}}
    (-)
    \\   
    & =
    -
    110 \cdot
    (-)
    +
    40
    e^a \partial_{e^a}(-)
    +
    4 B_{a b} \wedge e^a \partial_{B_{a' b}} \partial_{e^{a'}}(-)
    +
    e^a \wedge e^b\wedge \partial_{e^a}\partial_{e^b} (-)
    \\
    & =
    ( - 110 + 40 n_e - n_e(n_e - 1) - 4 n_e n_B) \cdot (-)
    \\   
    & =
    ( - 110 + 40 n_e - n_e(n_e - 1) - 2 n_e (n_e - n_tot)) \cdot (-)
  \end{aligned}
$$

$$
  n_{tot} \coloneqq n_e - 2 n_B
$$

$$
  b_B = \tfrac{1}{2}\left( n_e - n_tot \right)
$$

this gives a map

$$
  CFields
  \coloneqq
  \left\{
    \hat G_5
    \;\vert\;
    \beta Sq^3([G_4])
  \right\}
$$

$$
  CFields
  \overset{}{\longrightarrow}
  H^7_{dR}
$$


$$
  \array{
    \mathbb{Z}
      &\overset{\cdot 2}{\longrightarrow}&
    \mathbb{Z}
      &\overset{mod\, 2}{\longrightarrow}&
    \mathbb{Z}/2\mathbb{Z}
      &\simeq&
    \mathbb{Z}/2\mathbb{Z}
      &\overset{\beta}{\longrightarrow}&
    B \mathbb{Z}
    \\
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{\mathrlap{mod\, 4}}
      &&
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{ id }
      &&
    \downarrow^{\mathrlap{B(mod\, 2)}}
    \\
    \mathbb{Z}/2\mathbb{Z}
      &\underset{\cdot 2 }{\longrightarrow}&
    \mathbb{Z}/4\mathbb{Z}
      &\underset{mod\, 2}{\longrightarrow}&
     \mathbb{Z}/2\mathbb{Z}
      &\simeq&
     (\mathbb{Z}/4\mathbb{Z})/(\mathbb{Z}/2\mathbb{Z})
       &\underset{Sq^1}{\longrightarrow}&
     B (\mathbb{Z}/2\mathbb{Z})
  }
$$


$$
  \array{
    \mathbb{Z}
      &\overset{\cdot 2}{\longrightarrow}&
    \mathbb{Z}
      &\overset{mod\, 2}{\longrightarrow}&
    \mathbb{Z}/2
      &\simeq&
    \mathbb{Z}/2\mathbb{Z}
      &\overset{\beta}{\longrightarrow}&
    B \mathbb{Z}
    \\
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{\mathrlap{\cdot \pi}}
      &&
    \downarrow^{\mathrlap{\cdot \pi}}
      &&
    \downarrow^{\mathrlap{\cdot \pi}}
      &&
    \downarrow^{\mathrlap{id}}
    \\
    \mathbb{Z}
      &\underset{\cdot 2 \pi}{\longrightarrow}&
    \mathbb{R}
      &\underset{mod\, 2\pi}{\longrightarrow}&
     U(1)
      &\simeq&
     \mathbb{R}/2\pi\mathbb{Z}
       &\underset{\delta}{\longrightarrow}&
     B \mathbb{Z}
  }
$$


$$
  \array{
    \mathbb{Z}/2
    &\hookrightarrow&
    U(1)
    \simeq
    \mathbb{R}/\mathbb{Z}
    &\longrightarrow&
    B \mathbb{Z}
  }
$$

$$
  \exp( \underset{j'}{\sum} b^A_{(j')} b^B_{(j')} )  \exp( \underset{j}{\sum} b_{(j)}^B ) \omega
$$

$$
  \begin{aligned}
  \mathbf{L}
    & =
    \tfrac{1}{2 g^2}
    k_{\alpha \beta} 
    f^\alpha_{\mu \nu} 
    \tfrac{1}{2}
 
    \left(
      \tilde a^\alpha_{\nu,\mu}
      -
      \tilde a^\alpha_{\mu,\nu}
      +
      \gamma^{\alpha}{}_{\beta' \gamma'}
      \tilde a^{\beta'}_{\mu} \tilde a^{\gamma'}_{\nu}
    \right)
    \tfrac{1}{2}
    \left(
      \tilde a^{\beta\nu,\mu}
      -
      \tilde a^{\beta \mu,\nu}
      +
      \gamma^{\beta}{}_{\beta'' \gamma''}
      \tilde a^{\beta''}_{\mu} \tilde a^{\gamma''}_{\nu}
    \right)
    \,dvol_\Sigma
  \end{aligned}
  \,,
$$



$$
  \frac{\delta}{\delta \phi}
  \Gamma(\phi)
  _{\vert \phi = \langle \mathbf{\Phi}_{int}\rangle}
  = 
  0
$$

$$
  \langle \mathbf{\Phi}_{int}\rangle
  =
  \frac{\delta}{\delta J} W(J)
$$

[[GravityVertexCorrectionsForQED.png:file]]

In conclusion this shows that a consistent choice of [[counterterms]] $\mathcal{Z}_\Lambda$ exists to produce
_some_ S-matrix $\mathcal{S} = \underset{\Lambda \to \infty }{\lim} (\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda)$.
It just remains to see that for _every_ other S-matrix $\widetilde{\mathcal{S}}$ there exist counterterms
$\widetilde{\mathcal{Z}}_\lambda$ such 
that $\widetilde{\mathcal{S}} = \underset{\Lambda \to \infty }{\lim} (\mathcal{S}_\Lambda \circ \widetilde{\mathcal{Z}}_\Lambda)$.

But by the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}) 
we know that there exists a [[vertex redefinition]] $\mathcal{Z}$ such that 

$$
  \begin{aligned}
    \widetilde{\mathcal{S}} 
    & = \mathcal{S} \circ \mathcal{Z}
    \\
    & =
    \underset{\Lambda \to \infty}{\lim} 
    \left(
      \mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda
    \right)
    \circ
    \mathcal{Z}
    \\
    & = 
    \underset{\Lambda \to \infty}{\lim}
    (
      \mathcal{S}_\Lambda 
        \circ 
      (
        \underset{
          \widetilde{\mathcal{Z}}_\Lambda
        }{
        \underbrace{
        \mathcal{Z}_\Lambda
          \circ
        \mathcal{Z}
        }
        }
      )
    )
  \end{aligned}  
$$

and hence counterterms for any $\widetilde{\mathcal{S}}$ are given by the composite $\widetilde{\mathcal{Z}}_\Lambda \coloneqq \mathcal{Z}_\Lambda \circ \mathcal{Z}$.



I think that it would be fair to say that string vacua that can be described in terms of [[N=1 D=4 supergravity]] with a low scale of [[supersymmetry|SUSY]] breaking *generically* contain heavy sfermions and trilinear couplings but light gauginos (KKLT with warped sequestering is a non-generic counterexample). In addition, the masses of the lightest moduli are *generically* of the order the gravitino mass. These statementes would not be controversial among string theorists who know about moduli stabilization. On top of that, cosmological constraints imply that the moduli must be very heavy >O(10-100) TeV to preserve the success of the BBN. When you combine all of the above you may conclude that in such vacua even with low scale SUSY the lightest sfermions must be very heavy. What that means for the lightest Higgs in the context of the MSSM is that its mass will receive large radiative corrections mainly due to the heavy stop and will get pushed into the range above 120 GeV but below 130 GeV. Now, the exact value does, of course, depend on tan beta. With regard to tan beta being $\mathcal{O}(10)$ I’d recommend reading this paper: [arxiv.org/abs/1105.3765](http://arxiv.org/abs/1105.3765) . Basically, $tan \beta \sim \mathcal{O}(10)$ is needed to reduce the so-called little hierarchy problem when the scalars and trilinears are heavy, as can be seen from eq. 6 in that paper. So, the value of 127 GeV seems rather natural is such a scenario. Kane’s optimism about the gluino presumably stems from the same considerations, namely, in eq. 2, there is a quantity denoted as R(t), that depends on M3 (related to the gluino mass) as you can see in the expression in the paragraph below eq. 2. So, the relatively light gluino is needed if one wants to keep the little hierarchy problem under control.
So I think that this is all definitely very interesting and in my mind compelling.

As for the G2-MSSM, this is definitely the simplest model of moduli stabilization out there – a strongly coupled hidden sector (SQCD with a single family of vector like matter) dynamically generates a non-perturbative potential that stabilizes all the moduli and generates a hierarchically small scale (there are no fluxes, no warping, no antibranes). And these guys did it for the most general Kahler potential compatible with G2 holonomy with an arbitrary number of moduli, found closed expressions for the moduli and derived soft terms in the MSSM largangian!