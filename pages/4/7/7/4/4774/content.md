
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $V$ a  [[space]], $G$ a [[group]] and $\rho : G\times V \to V$ a  [[action]] of $G$ on $V$, we have the corresponding [[action groupoid]]. If everything is sufficiently smooth, this is a [[Lie groupoid]] denoted $V//_\rhoG$.

The _action Lie algebroid_ of $\rho$ is the [[Lie algebroid]] that corresponds to this Lie Lie groupoid (under [[Lie integration]]).

The [[Chevalley-Eilenberg algebra]] of an action Lie algebroid is in [[physics]] known as a [[BRST complex]].

## Details

Let $G$ be a [[Lie group]], $V$ a [[smooth manifold]] and $\rho : G \times V \to V$ a smooth [[action]]. Write $V//G$ for the corresponding [[action groupoid]], itself a Lie groupoid.  The [[Lie algebroid]] $Lie(V//G)$ corresponding to this is the [[action Lie algebroid]].

The [[Chevalley-Eilenberg algebra]] of the action Lie algebroid is

$$
  CE(Lie(V//G)) = (\wedge^\bullet_{C^\infty(V)} \mathfrak{g}^*, d_{\rho})
  \,,
$$

where the differential acts on functions $f \in C^\infty(V)$ by

$$
  d_\rho : f \mapsto \rho(-)(-)^* f \in C^\infty(V)\otimes \mathfrak{g}^*
  \,.
$$

Explicitly, for $t \in \mathfrak{g}$ this sends $f$ to the function
$(d_\rho f)(t)$ which is the derivative along $t \in T_e G$ of the function $G \times V \stackrel{\rho}{\to}V \stackrel{f}{\to} \mathbb{R}$.

Even more explicitly, if we choose local coordinates $\{v^k\} : \mathbb{R}^{dim V} \to V$ on a patch, and choose a basis $\{t^a\}$ of $\mathfrak{g}^*$ then we have that restricted to this patch the differential is on generators by

$$
  d_\rho : f \mapsto \rho^\mu{}_a t^a \wedge \partial_k f
$$

$$
  d_\rho : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
  \,.
$$

Specifically for $V$ a finite dimensional [[vector space]], $\rho : G$ a _linear_ action, $\{v^k\}$ a choice of basis of that vector space and $f$ a _[[linear function]]_ $f= f_k v^k$ , we have that $(f_k := \partial_k f) \in \mathbb{R}^{dim V}$ are the components vector of the dual vector given by $V$ in this basis, and the above gives the [[matrix multiplication]] form of the action

$$
  d_\rho : v^k \mapsto t^a \rho_a{}^k{}_l  v^l
  \,.
$$

Notice for completeness that the equation $(d_\rho)^2 = 0$ is equivalent to the [[Jacobi identity]] of the Lie bracket and the action property of $\rho$:

$$
  d_\rho d_\rho v^k = 
   (t^a \wedge t^b \rho_a{}^k{}_r \rho_b{}^r{}_l
    -
    \frac{1}{2}C^a{}_{b c}t^b \wedge t^c \rho_a{}^k{}_l )
     v^l
  \,.
$$

These local formulas shall be useful below for recognizing from our general abstract definition of covariant derivative the formulas traditionally given in the literature. For that notice that in the above local coordinates further restricting attention to linear actions, the [[Weil algebra]] of the action Lie algebroid is given by

$$
  W(Lie(V//G)) = (\wedge^\bullet_{C^\infty(\mathbb{R}^{dim V})} ( \Gamma(T^* \mathbb{R}^{dim V}) \oplus \mathfrak{g}^* \oplus \mathfrak{g}^*[1]), d_{W_\rho})
$$

where the differential is given on generators by

$$
  d_{W_\rho} : v^k \mapsto \rho_a{}^k{}_l t^a \wedge v^l + d_{dR} v^k
$$

$$
  d_{W_\rho} : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a
$$

and where the uniquely induced differential on the shifted generators -- the one encoding [[Bianchi identities]] -- is

$$
  d_{W_\rho}  : d_{dR} v^k 
      \mapsto 
        \rho_a{}^k{}_k r^a \wedge v^l 
      - \rho_a{}^k{}_l t^a \wedge  d_{dR} v^l
$$

and 

$$
  d_{W} : r^a \mapsto C^a{}_{b c} t^b \wedge r^c
  \,.
$$



Notice that we may identify the [[delooping]] Lie groupoid $\mathbf{B}G$ of $G$ with the action groupoid of the trivial action on the point, $\mathbf{B}G \simeq *//G$.  On Lie algebroids this morphism is dually the inclusion

$$
  CE(Lie(V//G)) \leftarrow CE(\mathfrak{g})
$$

that is the identity on $\mathfrak{g}^*$.





## Applications

* A [[covariant derivative]] is the 1-form [[curvature]] of [[∞-Lie algebra valued forms|Lie algebroid valued differential forms]] with values in an actoin Lie algebroid.

[[!redirects action Lie algebroids]]