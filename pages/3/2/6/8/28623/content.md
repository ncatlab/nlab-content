
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea
 {#Idea}

In [[homotopy type theory]], a fundamental characterization of [[delooping]] is that **the delooping of a [[group]] is [[type equivalence|equivalent]] to the [[type]] of [[torsors]] for that group**:

For  $G$ a [[group]] [[internalization|internal]] to [[Set]] ([[0-truncated]] [[types]]) there is (up to appropriate [[universe-level]] adjustment) an [[type equivalence|equivalence]]


$$
  \mathbf{B}G \simeq G\mathrm{Tors}_L(G).
$$

between:

1. the [[delooping groupoid]] $(\mathbf{B} G,\mathrm{pt})$ (a [[pointed type|pointed]] [[connected type|connected]] [[1-type]] equipped with a group-compatible identification of its [[loop space]]/[[identity]] with $G$, $Id_{pt,pt} \mathbf{B}G \simeq G$

2. the [[moduli type]] of left $G$-[[torsors]].

We make this explicit below.

The key observation is that for every [[term]] $t \colon \mathbf{B}G$, the [[path type]]

$$
  P_t
    \coloneqq
  (\mathrm{pt} = t)
$$

naturally carries a $G$-[[torsor]] [[mathematical structure|structure]], where the group [[group action|acts]] by path [[concatenation]]. This gives a [[function]]

$$
  \begin{array}{ccc}
    \mathbf{B}G &\longrightarrow& G\mathrm{Tors}_L(G)
    \\
    t & \mapsto&  P_t
    \mathrlap{\,.}
  \end{array}
$$

and the theorem asserts that this function exhibits an [[type equivalence|equivalence]].

This characterization reveals a relationship between algebraic [[symmetries]] and [[identity types]]: the [[group]] [[mathematical structure|structure]] of $G$ is represented by loops in $\mathbf{B}G$, while the points of $\mathbf{B}G$ can be recovered as torsors for those symmetries.

The following sections explain the construction, its mathematical proof, and its implementation in [[Cubical Agda]], with explicit references to the machine-checked declarations.


## Construction

### Left torsors

Let $G$ be a [[group]] whose [[underlying]] [[type]] is a [[set]] (meaning: an [[h-set]]). A left $G$-[[group action|action]] on a set $X$ is an operation

$$
  \begin{array}{ccc}
    G\times X &\longrightarrow& X
    \\
    (g,x) &\mapsto& g\cdot x
  \end{array}
$$

satisfying the usual [[unitality|unit]] and [[associativity]] laws.

For $x,y:X$, define the *type of transporters* by

$$
  \mathrm{Trans}_G(x,y)
  \coloneqq
  \sum_{g:G}(g\cdot x=y).
$$

A *left $G$-[[torsor]]* is a left action on a set $X$ equipped with a term of type $\|X\|_{-1}$ and a proof of

$$
  \prod_{x:X}\prod_{y:X}
  \operatorname{isContr}(\mathrm{Trans}_G(x,y)).
$$

The first condition $\|X\|_{-1}$ asserts mere [[inhabited type|inhabitation]] without selecting a distinguished element. The second says that every pair of points admits a unique transporter; one should verify that this is indeed the HoTT presentation of [[free action|free]] and transitive.

For any chosen $x:X$, the orbit map

$$
  \begin{array}{ccc}
    G &\longrightarrow& X
    \\
    g &\mapsto& g\cdot x
  \end{array}
$$

is an [[equivalence]]. Given $y:X$, consider the [[fiber]] of the orbit map over $y$:

$$
\begin{aligned}
\mathrm{fib}_{\mathrm{orb}_x}(y)
  &= \sum_{g:G}(\mathrm{orb}_x(g)=y) \\
  &= \sum_{g:G}(g\cdot x=y) \\
  &= \mathrm{Trans}_G(x,y).
\end{aligned}
$$

In [[homotopy type theory]], a function is an equivalence if and only if every fiber is [[contractible type|contractible]]. Therefore we have

$$
\left(
\prod_{y:X}\operatorname{isContr}(\mathrm{Trans}_G(x,y))
\right)
\to
\operatorname{isEquiv}(\mathrm{orb}_x).
$$

Thus a choice of origin identifies a torsor with the group, but this identification is not part of the torsor structure.

The **regular left torsor** is $G$ itself, equipped with left multiplication.


### The moduli type

Fix a [[univalent universe]] of small sets. Let

$$
G Tors_L
\coloneqq
\sum_{X:\mathrm{hSet}_{\ell}}
\operatorname{LeftTorsorStructure}_G(X)
$$

denote the [[moduli type]] of small left $G$-[[torsor]]s.

Its elements consist of carrier sets equipped with [[group action]]s and proofs of the torsor conditions. Since the relevant law fields are [[proposition]]s, the [[structure identity principle]] applies.

For two torsors $T$ and $U$, it identifies their [[path type]] with the type of equivariant equivalences:

$$
(T=U)\simeq\operatorname{Equiv}_G(T,U).
$$

Hence identity paths in the moduli type encode the symmetries of torsor structures.

The regular left torsor determines a distinguished point

$$
T_{\mathrm{reg}}:G Tors_L.
$$



## Delooping properties

### Connectedness and truncation

The [[moduli type]] $G Tors_L$ is [[connected space|connected]].

Indeed, any [[torsor]] $T$ is merely [[inhabited type|inhabited]]. Given a temporary choice $x:T$, the orbit map gives a $G$-equivariant [[equivalence]] between the regular torsor and $T$. The [[structure identity principle]] turns this into a [[path type|path]]

$$
T_{\mathrm{reg}}=T.
$$

Since [[connected space|connectedness]] requires only the [[propositional truncation]] of this path, the choice of $x$ can be eliminated.

Moreover, $G Tors_L$ is a [[1-type]]. By the [[structure identity principle]], its [[identity type]]s are equivalent to types of $G$-equivariant equivalences between [[set]]s, which are themselves sets.

Thus the moduli type of torsors is a [[pointed type|pointed]] connected $1$-type.

### Recovering the group from loops

At the regular basepoint, the [[loop space|loop type]] is

$$
\Omega(G Tors_L,T_{\mathrm{reg}})
\simeq
\operatorname{Aut}_G(T_{\mathrm{reg}}).
$$

An equivariant [[automorphism]] $f:G\to G$ of the regular left torsor satisfies

$$
f(gx)=gf(x).
$$

Taking $x=1$ gives

$$
f(g)=gf(1).
$$

Consequently, every such automorphism is a *right translation*

$$
R_h(x)\coloneqq xh
$$

for a unique $h:G$. Evaluation at the group unit therefore gives an equivalence

$$
\operatorname{Aut}_G(T_{\mathrm{reg}})\simeq G.
$$

Combining these equivalences yields

$$
\Omega(G Tors_L,T_{\mathrm{reg}})
\simeq G.
$$

This is an equivalence of underlying types. Compatibility with the group structure requires additional coherence between composition of equivariant automorphisms and [[path concatenation]].

In particular, if $p(g)$ is the loop corresponding to the right translation $R_g$ under the [[structure identity principle]], the composition convention used here gives

$$
p(gh)=p(g)\cdot p(h),
$$

where the right-hand operation is path concatenation.

This explains how the multiplication of $G$ is represented by composition of identity paths in the moduli type of torsors.



## Path-torsor characterization

The central result of the [[delooping via torsors|torsor delooping]] construction is that **any [[delooping]] of a [[group]] is equivalent to the type of [[torsor]]s for that group**.

This is the content of [Myers, Sati & Schreiber 2024, Lem 5.8](#MyersSatiSchreiber2024).

### Statement

**Lemma (Any delooping is equivalent to the type of torsors).**

Let $G$ be a [[group]], and let $(\mathbf{B}G,\mathrm{pt})$ be a [[delooping]] of $G$: a [[pointed type|pointed]] [[connected space|connected]] $1$-type equipped with a looping [[equivalence]]

$$
\ell:\Omega_{\mathrm{pt}}\mathbf{B}G\simeq G
$$

compatible with the group structures.

Then the assignment

$$
\begin{array}{ccc}
\mathbf{B}G &\xrightarrow{\simeq}& G Tors_L
\\
t &\mapsto& \operatorname{Id}_{\mathbf{B}G}(\mathrm{pt},t)
\end{array}
$$

defines an equivalence between $\mathbf{B}G$ and the type of left $G$-torsors.

The group action on the [[identity type]] is induced by [[path concatenation|concatenation of identifications]], using the inverse of the given looping equivalence.

### Construction of the group action

Fix $t:\mathbf{B}G$ and define the *path torsor*

$$
P_t\coloneqq\operatorname{Id}_{\mathbf{B}G}(\mathrm{pt},t).
$$

For $g:G$, the inverse looping equivalence determines a loop $\ell^{-1}(g):\operatorname{Id}_{\mathbf{B}G}(\mathrm{pt},\mathrm{pt})$.

Concatenation with this loop defines a left $G$-[[group action|action]]:

$$
\begin{array}{ccc}
G\times P_t &\longrightarrow& P_t
\\
(g,p) &\mapsto& \ell^{-1}(g)\cdot p
\end{array}
$$

Here the operation on the right is [[path concatenation]]. The compatibility of the looping equivalence with the group structure ensures the unit and associativity laws.

This is the construction described in equation (160) of [Myers, Sati & Schreiber 2024](#MyersSatiSchreiber2024).

### Proof that the path type is a torsor

We first verify that $P_t$ is a left $G$-torsor.

**Mere inhabitation.**

Since $\mathbf{B}G$ is [[connected space|connected]], for every $t:\mathbf{B}G$ there merely exists an identification from $\mathrm{pt}$ to $t$, expressed by $\|P_t\|_{-1}$.

This establishes mere [[inhabited type|inhabitation]] without choosing a distinguished path.

**Existence of a transporter.**

Let $p,q:\operatorname{Id}_{\mathbf{B}G}(\mathrm{pt},t)$. We wish to construct a group element $g:G$ satisfying $g\cdot q=p$.

By path inversion and concatenation of identifications, the composite $p\cdot q^{-1}$ is a loop at $\mathrm{pt}$. Applying the looping equivalence gives

$$
g\coloneqq\ell(p\cdot q^{-1}):G.
$$

By construction, $\ell^{-1}(g)\cdot q=p$, up to the canonical identification supplied by the equivalence and the groupoid laws for paths. Hence $g$ transports $q$ to $p$.

This corresponds to the explicit construction in equation (161) of [Myers, Sati & Schreiber 2024](#MyersSatiSchreiber2024).

**Uniqueness of the transporter.**

Suppose another group element $g':G$ also satisfies $g'\cdot q=p$. By definition of the action, we have $\ell^{-1}(g)\cdot q=p=\ell^{-1}(g')\cdot q$.

Concatenating with $q^{-1}$ and using the groupoid laws for paths gives $\ell^{-1}(g)=\ell^{-1}(g')$. Since $\ell$ is an equivalence, it follows that $g=g'$.

More precisely, the type of transporters is

$$
\operatorname{Trans}_G(q,p)
\coloneqq
\sum_{g:G}(\ell^{-1}(g)\cdot q=p).
$$

This is the fiber over $p$ of the orbit map $g\mapsto\ell^{-1}(g)\cdot q$. Since this map is the composite of the looping equivalence $\ell^{-1}$ with concatenation by $q$, both of which are equivalences, its fibers are contractible.

Thus $P_t$ satisfies the unique-transporter condition and, together with mere inhabitation, is a left $G$-torsor.

This is the uniqueness argument corresponding to equation (162) of [Myers, Sati & Schreiber 2024](#MyersSatiSchreiber2024).

### Proof that the construction is an equivalence

We have shown that the assignment $t\mapsto P_t$ defines a map $F:\mathbf{B}G\to G Tors_L$. It remains to prove that $F$ is an equivalence.

The source $\mathbf{B}G$ is a pointed connected $1$-type by assumption. As established above, the [[moduli type]] $G Tors_L$ is also a pointed connected $1$-type, with the regular torsor as its distinguished point.

At $t=\mathrm{pt}$, the associated torsor is $P_{\mathrm{pt}}=\operatorname{Id}_{\mathbf{B}G}(\mathrm{pt},\mathrm{pt})$. The looping equivalence identifies this torsor with the regular left $G$-torsor, giving the required basepoint identification.

Moreover, a path $r:s=t$ induces a $G$-equivariant equivalence by concatenation:

$$
\begin{array}{ccc}
P_s &\xrightarrow{\simeq}& P_t
\\
q &\mapsto& q\cdot r
\end{array}
$$

Its inverse is given by concatenation with $r^{-1}$. Equivariance follows from associativity of path concatenation.

By the [[structure identity principle]], this equivariant equivalence corresponds to a path $F(s)=F(t)$ in the moduli type.

At the basepoint, this construction induces an equivalence on [[loop space|loop types]]. Indeed, equivariant automorphisms of $P_{\mathrm{pt}}$ are determined by their value at the identity path, and the induced action on loops agrees with this identification.

We now apply the fundamental lemma for [[pointed type|pointed]] [[connected space|connected]] types: a pointed map between connected types that induces an equivalence on loop types is itself an equivalence, in the present $1$-truncated setting.

Consequently,

$$
\boxed{\mathbf{B}G\simeq G\mathrm{Tors}_L.}
$$

This completes the proof of the torsor characterization of deloopings.


## Formalization in Cubical Agda

The constructions described above have been formalized in [[Cubical Agda]], using existing library interfaces for [[univalence]], the [[structure identity principle]], and [[Eilenberg-Mac Lane space|Eilenberg--Mac Lane types]].

The verified development consists of twelve modules, all checked with Agda's `--safe` option. The source code and mathematical exposition are available in the [[nLab materials]] index:

* [Delooping via Torsors — nLab Materials](https://ncatlab.org/nlab/show/nLab+materials#TorsorDelooping)
* [Verified Cubical Agda source, v0.1](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/tree/torsor-delooping-v0.1/src/TorsorDelooping)
* [Mathematical companion paper](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/papers/TorsorDelooping/main.pdf)

The following declarations are local to this development; the underlying Cubical library provides the general-purpose type-theoretic interfaces.

### Torsor structures

* [LeftAction.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/LeftAction.agda) defines `LeftAction` and `Equivariant`.

* [LeftTorsor.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/LeftTorsor.agda) defines `IsLeftTorsor` and `LeftTorsor`, using mere inhabitation and contractible transporters.

* [Regular.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/Regular.agda) constructs the regular left torsor `regularLeftTorsor`.

* [Morphisms.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/Morphisms.agda) establishes that equivariant maps between left torsors are equivalences.

### Moduli and loops

* [Moduli.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/Moduli.agda) constructs `LeftTorsorModuli` and establishes `torsorPathEquiv` through the [[structure identity principle]].

* [Delooping.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/Delooping.agda) proves connectedness, the $1$-type property, and `torsorLoopEquivGroup`.

* [LoopGroup.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/LoopGroup.agda), [SIPPathEmbedding.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/SIPPathEmbedding.agda), and [SIPCoherence.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/SIPCoherence.agda) establish the composition coherence for regular-torsor loops, including `regularTorsorLoop-comp`.

### Comparison and classification

* [EM1Comparison.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/EM1Comparison.agda) constructs a comparison map from the library's $EM_1(G)$ to $G Tors_L$ and proves its basepoint loop-equivalence property.

* [UniverseLiftedComparison.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/UniverseLiftedComparison.agda) proves `liftedEm1ToTorsorEquiv`, a universe-lifted equivalence between $EM_1(G)$ and the torsor moduli type.

* [PathTorsor.agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/src/TorsorDelooping/PathTorsor.agda) formalizes the path-torsor characterization associated with [Myers, Sati & Schreiber 2024, Lem 5.8](#MyersSatiSchreiber2024).

The last module introduces `PointedLoopGroupData`, consisting of connectedness, $1$-truncation, a loop equivalence, and explicit unit and multiplication coherences.

It constructs `pathTorsorAction`, `pathTorsorOrbitEquiv`, `pathTorsor`, and `pathTorsorModuli`, together with the basepoint comparison and the equivalence induced on loop types.

Its main result, `liftedPathTorsorModuliEquiv`, establishes the universe-lifted equivalence

$$
\operatorname{Lift}_{\ell+1}(\mathbf{B}G)
\simeq
G Tors_L.
$$

Here the formalization uses a chosen loop equivalence $G\simeq(\mathrm{pt}=\mathrm{pt})$, inverse in direction to the equivalence used in the mathematical exposition above.

The universe lifting accounts for the universe level of the torsor moduli type. The final declaration is an equivalence of underlying types, with basepoint comparison paths established separately; no additional pointed-equivalence or group-isomorphism package is claimed.

All twelve modules pass Agda's `--safe` type-checking mode with the pinned Cubical library.

The development concerns set-level groups and their homotopy-theoretic deloopings. The construction of particular groups, such as the multiplicative group of invertible complex numbers, and their subsequent applications to topological quantum gates remain future work.

For the complete mathematical explanation, statement-to-declaration index, and reproducibility information, see the accompanying [mathematical companion paper](#WangTorsorDelooping2026).

## Related concepts

* [[torsor]]
* [[group action]]
* [[delooping]]
* [[classifying space]]
* [[homotopy type theory]]
* [[univalence]]
* [[structure identity principle]]
* [[Eilenberg-Mac Lane space]]

## References
{#References}

* {#MyersSatiSchreiber2024} [[David Jaz Myers]], [[Hisham Sati]], [[Urs Schreiber]]; §5.2, esp. Lem. 5.5--5.8 of: *[[schreiber:Topological Quantum Gates in Homotopy Type Theory]]*, Comm. Math. Phys. **405**, 172 (2024) &lbrack;[doi:10.1007/s00220-024-05020-8](https://doi.org/10.1007/s00220-024-05020-8), [arXiv:2303.02382](https://arxiv.org/abs/2303.02382)&rbrack;

* The [Cubical Agda library](https://github.com/agda/cubical), providing [[univalence]], the [[structure identity principle]], [[higher inductive type|higher inductive]] [[Eilenberg-Mac Lane space|Eilenberg--Mac Lane types]], and connected-type equivalence results;

* {#WangTorsorDelooping2026} [[Hongwei Wang]]: *Torsors, Univalence, and Delooping: A Mathematical Companion to a Cubical Agda Formalization* (2026), version 0.1 &lbrack;[pdf](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/blob/torsor-delooping-v0.1/papers/TorsorDelooping/main.pdf), [sources](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/tree/torsor-delooping-v0.1/papers/TorsorDelooping), [github](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda/tree/torsor-delooping-v0.1), [nLab materials](https://ncatlab.org/nlab/show/nLab+materials#TorsorDelooping)&rbrack;

[[!redirects deloopings via torsors]]

[[!redirects torsor delooping]]

[[!redirects torsor deloopings]]
