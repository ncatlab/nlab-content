

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ with [[field bundle]] $E \overset{fb}{\to} \Sigma$ over some [[spacetime]] $\Sigma$ and [[local Lagrangian density]] $\mathbf{L}$, then its _local BV-BRST complex_ (or _local BRST complex_, for short) is the realization of the [[BV-BRST complex]] not on [[local observables]] $A = \tau_{\Sigma} \alpha$ given by [[functionals]] on the [[space of field histories]] $\Gamma_{\Sigma}(E)_{\delta_{EL} = 0}$ which are [[transgression of variational differential forms|transgressions]] $\tau_{\Sigma}$ of [[variational differential forms]] $\alpha \in \Omega^{\bullet, \bullet}_\Sigma(E)$ on the jet bundle, but on these variational differential forms themselves (whence "local", i.e. before [[transgression of variational differential forms|transgression]]).

If $s$ denotes the [[BV-BRST differential]] in a BV-resolution $\Omega^{\bullet,\bullet}_\Sigma(E)\vert_{\mathcal{E}_{BV}}$ of the restriction to the [[shell]] $\mathcal{E} \hookrightarrow J^\infty_\Sigma(E)$ of the [[variational bicomplex]] $\Omega^{\bullet,\bullet}_\Sigma(E)$ with its [[total spacetime derivative]] $d$ (horizontal derivative), then the _local BV-BRST cohomology_ is the [[cochain cohomology]] of $s + d$, hence of the [[total complex]] of the [[double complex]] given by $s$ and $d$. 

Generally, considering [[variational differential forms]] up to $d$-exact terms is the "local" incarnation  of what under the [[integration of differential forms|integration]] involved in the [[transgression of variational differential forms|transgression]] is [[integration by parts]] and it is in this way that "local BV-BRST cohomology" knows about the actual BV-BRST cohomology on [[local observables]].

## Example

Consider local coordinates $(\phi^a)$ on the [[fibers]] of the [[field bundle]]. The corresponding [[antifield]] coordinates are to be denoted $\overline{\phi}_a$ and the [[BV-BRST differential]] takes them to the corresponding component 

$$
  s(\overline{\phi}_a) = \frac{\delta_{El} L}{\delta \phi^a}
$$ 

of the [[Euler-Lagrange form]].



In degree $(p+1,0)$ the $s+d$-closed elements in vanishing [[ghost]] degree are [[pairs]] $(v,J_v)$ consisting of an [[infinitesimal symmetry of the Lagrangian]] $v$, regarded as an [[antifield]] [[density]] $v^a \overline{\phi}_a dvol_\Sigma$, together with a corresponding [[conserved current|conserved]] [[Noether's theorem|Noether current]] $J_v$:

$$
  \array{
    \{J_v\} &\overset{d}{\longrightarrow}& \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \uparrow\mathrlap{-s}
    \\
    && \{ v^a \overline{\phi}_a dvol_\Sigma\}
  }
$$

Such pairs are $(s+d)$-exact if [[on-shell]] the infintiesimal symmetry coincides with an [[infinitesimal gauge symmetry]]. To see this, recall:

An  [[infinitesimal gauge symmetry]] $v_\epsilon$  of [[gauge parameter]] $(\epsilon^\alpha)$ is a vector field on the jet bundle with components of the form

$$
  \mathcal{L}_{v_\epsilon} \phi^a
   \;\coloneqq\;
  R^a_\alpha \epsilon^\alpha
    +
  R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
$$

such that this is an [[infinitesimal symmetry of the Lagrangian]] in that

$$
  \begin{aligned}
    \iota_{v_\epsilon} \delta_{EL} \mathbf{L}
    & =
    v^a \frac{\delta_{EL} L}{\delta \phi^a} dvol_\Sigma
    \\
    & =
    \epsilon^\alpha
    \left(
       R^a_\alpha \frac{\delta_{EL} L}{ \delta \phi^a}
       -
       \frac{d}{d x^\mu} 
       \left(
          R^{a \mu}_\alpha \frac{\delta_{EL} L}{\delta \phi^a}
       \right)
    \right)
    dvol_\Sigma
    +
    d\left(
       \epsilon^\alpha R^{a \mu}_\alpha \frac{\delta_{EL} L}{\delta \phi^a}
    \right)
    \iota_{\partial_\mu} dvol_\Sigma
    \\
    & =
    0 + d(...)
  \end{aligned}
$$

for all $(\epsilon^\alpha)$.

The corresponding [[antighosts]] $\overline{c}_\alpha$ are taken by the BV-BRST differential to the antifield-preimage of the term on the left:

$$
  s\left(\overline{c}_\alpha\right)
  \;=\;
  R^a_\alpha \overline{\phi}_a
  -
  \frac{d}{d x^\mu} 
  \left(
    R^{a \mu}_\alpha \overline{\phi}_a
  \right)  
  \,.
$$

Moreover, an [[on-shell]] vanishing [[infinitesimal symmetry of the Lagrangian]] is a vector field with components of the form

$$
  \kappa^{a b} \frac{\delta_{EL} L}{\delta \phi^a}
$$

for $\kappa^{a b} = - \kappa^{b a}$ a skew-symmetric system of smooth functions on the jet bundle.

The linear combination of such an infinitesimal gauge symmetry and an on-shell vanishing infinitesimal symmetry is $(s+d)$-exact:


$$
  \begin{aligned}
    v^a dvol_\Sigma
    & =
    \left(
      R^a_\alpha \epsilon^\alpha
      +
      R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
      +
      \kappa^{a b} \frac{\delta_{EL} L }{ \delta \phi^a }
    \right)
    dvol_\Sigma
    \\
    & =
    s
    \left( 
      \epsilon^\alpha \overline{c}_\alpha 
      - 
      \tfrac{1}{2}\kappa^{a b} \overline{\phi}_a \overline{\phi}_b  
    \right) dvol_\sigma
    +
    d\left(
      \epsilon^\alpha R^{a \mu}_\alpha 
    \right)
    \iota_{\partial_\mu} dvol_\Sigma
  \end{aligned}
$$

([Barnich-Brandt-Henneaux 94, p. 20](#BarnichBrandtHenneaux94))


It may be useful to organize this expression into the $s+d$-[[bicomplex]] like so:

$$
  \array{
    \{K\}
     &\overset{d}{\longrightarrow}&
     \{ d K 
       + 
     \epsilon^\alpha R^{a \mu}_\alpha \frac{\delta_{EL}\mathbf{L}}{ \delta \phi^a}
     \} 
     &\overset{d}{\longrightarrow}& 
    \{ \overset{= 0}{\overbrace{ d J_v - \iota_v \delta_{EL}\mathbf{L} }} \}
    \\
    && \mathllap{s}\uparrow && \uparrow\mathrlap{-s}
    \\
    && 
    \epsilon^\alpha R^{a \mu}_\alpha \overline{\phi}_a
    \iota_{\partial_\mu} dvol_\Sigma
      &\underset{d}{\longrightarrow}&
    \left\{  
      d\left(
        \epsilon^\alpha R^{a \mu}_\alpha \overline{\phi}_a
      \right)
      \iota_{\partial_\mu} dvol_\Sigma
      +
      \left(
        R^a_\alpha \epsilon^\alpha
        +
        R^{a \mu}_\alpha \frac{d \epsilon^\alpha}{d x^\mu}
        +
        \kappa^{a b} \frac{\delta_{EL} L }{ \delta \phi^a }
      \right)
      \overline{\phi}_a
      \,
      dvol_\Sigma
    \right\}
    \\
    && && \uparrow\mathrlap{-s}
    \\
    &&
    &&
    \left(
       - \epsilon^\alpha \overline{c}_\alpha
       + 
      \tfrac{1}{2}\kappa^{a b } \overline{\phi}_a \overline{\phi}_b 
    \right)
    dvol_\Sigma
  }
$$


## Related concepts

* [[variational BV-BRST bicomplex]]


## References
 {#References}


The general theory:

* {#BarnichBrandtHenneaux94} [[Glenn Barnich]], [[Friedemann Brandt]], [[Marc Henneaux]], _Local BRST cohomology in the antifield formalism: I. General theorems_, Commun. Math. Phys. **174** (1995) 57-92 &lbrack;[arXiv:hep-th/9405109](https://arxiv.org/abs/hep-th/9405109), [doi:10.1007/BF02099464](https://doi.org/10.1007/BF02099464)&rbrack;

Review:

* {#BarnichBrandtHenneaux00} [[Glenn Barnich]], [[Friedemann Brandt]], [[Marc Henneaux]], _Local BRST cohomology in gauge theories_, Phys. Rept. **338** (2000) 439-569 &lbrack;<a href="https://doi.org/10.1016/S0370-1573(00)00049-1">doi:10.1016/S0370-1573(00)00049-1</a>[arXiv:hep-th/0002245](https://arxiv.org/abs/hep-th/0002245)&rbrack;

Details on the [[local antibracket]]:

* {#BarnichHenneaux96} [[Glenn Barnich]], [[Marc Henneaux]], section 2 and appendix B of: _Isomorphisms between the Batalin-Vilkovisky antibracket and the Poisson bracket_, J. Math. Phys. **37** (1996) 5273-5296 &lbrack;[arXiv:hep-th/9601124](https://arxiv.org/abs/hep-th/9601124), [doi:10.1063/1.531726](https://doi.org/10.1063/1.531726)&rbrack;

Application to [[gravity]] and/or [[Yang-Mills theory]] ([[Einstein-Yang-Mills theory]]) is discussed in

* [[Glenn Barnich]], [[Friedemann Brandt]], [[Marc Henneaux]], _Local BRST cohomology in Einstein-Yang-Mills theory_, Nucl. Phys. B **455** (1995) 357-408 &lbrack;<a href="https://doi.org/10.1016/0550-3213(95)00471-4">doi:10.1016/0550-3213(95)00471-4</a>[arXiv:hep-th/9505173](https://arxiv.org/abs/hep-th/9505173)&rbrack;

[[!redirects local BV-BRST cohomology]]

[[!redirects local BRST complex]]
[[!redirects local BRST complexes]]

[[!redirects local BV-BRST complex]]
[[!redirects local BV-BRST complexes]]


[[!redirects local BV complex]]
[[!redirects local BV complexes]]

[[!redirects local BV-complex]]
[[!redirects local BV-complexes]]

[[!redirects local BRST differential]]
[[!redirects local BRST differentials]]

[[!redirects local BV-BRST differential]]
[[!redirects local BV-BRST differentials]]

[[!redirects local BV-cohomology]]
[[!redirects local BV cohomology]]

