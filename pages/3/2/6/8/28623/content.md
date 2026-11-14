
\tableofcontents

## Idea

In [[homotopy type theory]], a fundamental characterization of [[delooping]] is that **any delooping of a group is equivalent to the type of torsors for that group**.

Let $G$ be a set-level group and let $(BG,\mathrm{pt})$ be a pointed connected $1$-type equipped with a group-compatible identification of its loop space with $G$. Then, up to the appropriate universe-level adjustment, there is an equivalence

$$
BG\simeq \mathrm{GTors}_L(G).
$$

Here $\mathrm{GTors}_L(G)$ denotes the moduli type of left $G$-torsors.

The central question is how such an equivalence can be constructed explicitly.

The key observation is that for every point $t:BG$, the path type

$$
P_t:=(\mathrm{pt}=t)
$$

naturally carries a $G$-torsor structure, where the group acts by path concatenation. This gives a map

$$
BG\to \mathrm{GTors}_L(G),
\qquad t\mapsto P_t.
$$

The theorem asserts that this construction is an equivalence.

This characterization reveals a relationship between algebraic symmetries and identity types: the group structure of $G$ is represented by loops in $BG$, while the points of $BG$ can be recovered as torsors for those symmetries.

The following sections explain the construction, its mathematical proof, and its realization in [[Cubical Agda]], with explicit references to the machine-checked declarations.

## Construction

### Left torsors

Let $G$ be a group whose underlying type is a set. A left $G$-action on a set $X$ is an operation

$$
G\times X\to X,\qquad (g,x)\mapsto g\cdot x
$$

satisfying the usual unit and associativity laws.

For $x,y:X$, define the type of transporters by

$$
\operatorname{Trans}_G(x,y)
:=
\sum_{g:G}(g\cdot x=y).
$$

A left $G$-torsor is a left action such that

$$
\|X\|_{-1}
$$

and

$$
\prod_{x:X}\prod_{y:X}
\operatorname{isContr}(\operatorname{Trans}_G(x,y)).
$$

The first condition asserts mere inhabitation without selecting a distinguished element. The second says that every pair of points admits a unique transporter.

For any chosen $x:X$, the orbit map

$$
\operatorname{orb}_x:G\to X,
\qquad g\mapsto g\cdot x
$$

is an equivalence. Thus a choice of origin identifies a torsor with the group, but this identification is not part of the torsor structure.

The **regular left torsor** is $G$ itself, equipped with left multiplication.

### The moduli type

Fix a univalent universe of small sets. Let

$$
\mathrm{GTors}_L(G)
$$

denote the type of small left $G$-torsors.

Its elements consist of carrier sets equipped with group actions and proofs of the torsor conditions. Since the relevant law fields are propositions, the [[structure identity principle]] applies.

For two torsors $T$ and $U$, it identifies their path type with the type of equivariant equivalences:

$$
(T=U)\simeq\operatorname{Equiv}_G(T,U).
$$

Hence identity paths in the moduli type encode the symmetries of torsor structures.

The regular left torsor determines a distinguished point

$$
T_{\mathrm{reg}}:\mathrm{GTors}_L(G).
$$

## Delooping properties

### Connectedness and truncation

The moduli type $\mathrm{GTors}_L(G)$ is connected.

Indeed, any torsor $T$ is merely inhabited. Given a temporary choice $x:T$, the orbit map gives an equivariant equivalence between the regular torsor and $T$. The structure identity principle turns this into a path

$$
T_{\mathrm{reg}}=T.
$$

Since connectedness requires only the propositional truncation of this path, the choice of $x$ can be eliminated.

Moreover, $\mathrm{GTors}_L(G)$ is a $1$-type. By the structure identity principle, its identity types are equivalent to types of equivariant equivalences between sets, which are themselves sets.

Thus the moduli of torsors is a pointed connected $1$-type.

### Recovering the group from loops

At the regular basepoint, the loop type is

$$
\Omega(\mathrm{GTors}_L(G),T_{\mathrm{reg}})
\simeq
\operatorname{Aut}_G(T_{\mathrm{reg}}).
$$

An equivariant automorphism $f:G\to G$ of the regular left torsor satisfies

$$
f(gx)=gf(x).
$$

Taking $x=1$ gives

$$
f(g)=gf(1).
$$

Consequently every such automorphism is a right translation

$$
R_h(x)=xh
$$

for a unique $h:G$. Evaluation at the group unit therefore gives an equivalence

$$
\operatorname{Aut}_G(T_{\mathrm{reg}})\simeq G.
$$

Combining these equivalences yields

$$
\Omega(\mathrm{GTors}_L(G),T_{\mathrm{reg}})
\simeq G.
$$

The identification is compatible with the group structure when the appropriate composition coherences are taken into account. In particular, if $p(g)$ is the loop corresponding to the right translation $R_g$, the convention used here gives

$$
p(gh)=p(g)\cdot p(h),
$$

where the right-hand operation is path concatenation.

This explains how the multiplication of $G$ is represented by composition of identity paths in the torsor moduli type.


## Path-torsor characterization

The central result of the torsor delooping construction is that **any delooping of a group is equivalent to the type of torsors for that group**.

This is the content of Lemma 5.8 in Myers--Sati--Schreiber, *Topological Quantum Gates in Homotopy Type Theory*.

### Statement

**Lemma (Any delooping is equivalent to the type of torsors).**

Let $G$ be a group, and let $(BG,\mathrm{pt})$ be a delooping of $G$: a pointed connected $1$-type equipped with a looping equivalence

$$
\ell:\Omega_{\mathrm{pt}}BG\simeq G
$$

compatible with the group structures.

Then the assignment

$$
F:BG\to\mathrm{GTors}_L(G),
\qquad
t\mapsto
\operatorname{Id}_{BG}(\mathrm{pt},t)
$$

defines an equivalence between $BG$ and the type of left $G$-torsors.

The group action on the identity type is induced by concatenation of identifications, using the inverse of the given looping equivalence.

### Construction of the group action

Fix a point $t:BG$, and define

$$
P_t:=\operatorname{Id}_{BG}(\mathrm{pt},t).
$$

Given $g:G$, the inverse looping equivalence determines a loop

$$
\ell^{-1}(g):
\operatorname{Id}_{BG}(\mathrm{pt},\mathrm{pt}).
$$

Concatenation with this loop defines the action

$$
G\times P_t\to P_t
$$

by

$$
g\cdot p:=\ell^{-1}(g)\cdot p.
$$

Here the operation on the right is concatenation of identifications.

The compatibility of the looping equivalence with the group structure ensures the unit and associativity laws.

This is the construction described in equation (160) of the cited paper.

### Proof that the path type is a torsor

We first verify that $P_t$ is a left $G$-torsor.

**Mere inhabitation.**

Since $BG$ is connected, for every $t:BG$ there merely exists an identification from $\mathrm{pt}$ to $t$:

$$
\|P_t\|_{-1}.
$$

This establishes the inhabitation condition without choosing a distinguished path.

**Existence of a transporter.**

Let

$$
p,q:\operatorname{Id}_{BG}(\mathrm{pt},t).
$$

We wish to construct a group element $g:G$ satisfying

$$
g\cdot q=p.
$$

By inversion and concatenation of identifications, the composite

$$
p\cdot q^{-1}
$$

is a loop at $\mathrm{pt}$.

Applying the looping equivalence gives

$$
g:=\ell(p\cdot q^{-1}):G.
$$

By construction,

$$
\ell^{-1}(g)\cdot q=p,
$$

up to the canonical identification supplied by the equivalence and the groupoid laws for paths.

Hence $g$ transports $q$ to $p$.

This corresponds to the explicit construction in equation (161) of the cited paper.

**Uniqueness of the transporter.**

Suppose that another group element $g':G$ also satisfies

$$
g'\cdot q=p.
$$

By definition of the action, we have

$$
\ell^{-1}(g)\cdot q
=
p
=
\ell^{-1}(g')\cdot q.
$$

Concatenating both sides with $q^{-1}$ gives

$$
\ell^{-1}(g)=\ell^{-1}(g').
$$

Since $\ell$ is an equivalence, it follows that

$$
g=g'.
$$

More precisely, the type of group elements together with proofs that they transport $q$ to $p$ is contractible.

Thus $P_t$ is a left $G$-torsor.

This is the uniqueness argument corresponding to equation (162) of the cited paper.

### Proof that the construction is an equivalence

We have shown that the assignment

$$
t\mapsto P_t
$$

defines a map

$$
F:BG\to\mathrm{GTors}_L(G).
$$

It remains to prove that $F$ is an equivalence.

The source $BG$ is a pointed connected $1$-type by assumption. The type of left $G$-torsors is also a pointed connected $1$-type, with the regular torsor as its distinguished point.

At $t=\mathrm{pt}$, the associated torsor is

$$
P_{\mathrm{pt}}
=
\operatorname{Id}_{BG}(\mathrm{pt},\mathrm{pt}).
$$

The looping equivalence identifies this torsor with the regular left $G$-torsor.

Moreover, a path $r:s=t$ induces an equivariant equivalence

$$
P_s\to P_t,
\qquad
q\mapsto q\cdot r.
$$

In a univalent setting, the [[structure identity principle]] identifies this equivariant equivalence with a path between the corresponding torsors.

At the basepoint, this construction induces an equivalence on loop types.

We now apply the fundamental lemma for pointed connected types: a pointed map between pointed connected types that induces an equivalence on loop types is itself an equivalence, under the relevant truncation hypotheses.

Consequently,

$$
BG\simeq\mathrm{GTors}_L(G).
$$

This completes the proof of the torsor characterization of deloopings.

## Formalization in Cubical Agda

A corresponding machine-checked construction is developed in `src/TorsorDelooping/PathTorsor.agda`.

The main declarations are:

* `PointedLoopGroupData`: the pointed connected $1$-type, loop equivalence, and explicit unit and multiplication coherences.
* `pathTorsorAction`: the left action induced by concatenation of paths.
* `pathTorsorOrbitEquiv`: the equivalence expressing existence and uniqueness of transporters.
* `pathTorsor`: the resulting left $G$-torsor.
* `pathTorsorModuli`: the map sending a point to its path torsor.
* `pathTorsorModuli-base`: the basepoint comparison.
* `pathTorsorTransportEquiv`: the equivariant equivalence induced by concatenation with a path.
* `isEquiv-pathTorsorModuli-loop`: the equivalence induced on loop types.
* `liftedPathTorsorModuliEquiv`: the global equivalence obtained after universe lifting.

The formalization uses a loop equivalence in the direction

$$
G\simeq(\mathrm{pt}=\mathrm{pt}),
$$

rather than the direction of $\ell$ above. These formulations correspond by inversion of the chosen equivalence.

The checked theorem also makes the required universe adjustment explicit:

$$
\operatorname{Lift}_{\ell+1}(BG)
\simeq
\mathrm{GTors}_L(G).
$$

This is an equivalence of underlying types. The basepoint comparison is checked separately; no additional pointed-equivalence or group-isomorphism package is claimed.

The difference between the paper's mathematical presentation and the Cubical Agda declaration is therefore one of explicit formal assumptions, universe bookkeeping, and packaging, rather than a different path-torsor construction.



### Torsor structures

* `LeftAction.agda` defines `LeftAction` and `Equivariant`.
* `LeftTorsor.agda` defines `IsLeftTorsor` and `LeftTorsor`.
* `Regular.agda` constructs `regularLeftTorsor`.
* `Morphisms.agda` establishes that equivariant maps between torsors are equivalences.

### Moduli and loops

* `Moduli.agda` constructs `LeftTorsorModuli` and establishes `torsorPathEquiv` using the structure identity principle.
* `Delooping.agda` proves connectedness, the $1$-type property, and `torsorLoopEquivGroup`.
* `LoopGroup.agda`, `SIPPathEmbedding.agda`, and `SIPCoherence.agda` establish the composition coherence required for regular-torsor loops.

### Comparison and classification

* `EM1Comparison.agda` constructs the comparison map from the library's $EM_1(G)$ and proves its basepoint loop-equivalence property.
* `UniverseLiftedComparison.agda` proves `liftedEm1ToTorsorEquiv`, giving an equivalence between the universe-lifted $EM_1(G)$ and the torsor moduli type.
* `PathTorsor.agda` defines `PointedLoopGroupData`, constructs path torsors, and proves `liftedPathTorsorModuliEquiv`.

The last theorem requires explicit connectedness, $1$-truncation, loop equivalence, and unit/multiplication compatibility data.

All twelve modules have been reported to pass Agda's `--safe` type-checking mode using the pinned Cubical library.

The final declarations are equivalences of underlying types. Basepoint comparison paths are available separately, but the results are not additionally packaged as pointed equivalences or group isomorphisms.

This development formalizes the set-level homotopy-theoretic construction. It does not yet implement topological or cohesive group structures, geometric principal torsors, computational transport, or the dependent-type construction required for topological quantum gates.

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

* D. J. Myers, H. Sati, U. Schreiber, *Topological Quantum Gates in Homotopy Type Theory*, Communications in Mathematical Physics 405 (2024), especially the discussion of torsor deloopings and path torsors. [arXiv:2303.02382](https://arxiv.org/abs/2303.02382).

* The [Cubical Agda library](https://github.com/agda/cubical), providing univalence, the structure identity principle, higher inductive Eilenberg--Mac Lane types, and connected-type equivalence results.

* H. Wang, *Torsors, Univalence, and Delooping: A Mathematical Companion to a Cubical Agda Formalization*, 2026, draft in preparation. Associated source: [Topological Quantum Programming in Cubical Agda](https://github.com/HongweiWang42/TopologicalQuantumProgramming-CubicalAgda).
