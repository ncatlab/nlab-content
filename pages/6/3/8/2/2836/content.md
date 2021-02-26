
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Stable homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}


## Definition

In a [[(∞,1)-category]] $C$ admitting a [[final object]] ${*}$, for any object $X$ its **suspension object** $\Sigma X$ is the [[homotopy pullback|homotopy pushout]]

$$
  \array{
     X &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     {*} &\to& \Sigma X
  }
  \,,
$$

This is the [[mapping cone]] of the terminal map $X \to {*}$. See there for more details.

This concept is dual to that of [[loop space object]].

## Suspension functor

### As an (infinity,1)-functor

Let $C$ be a [[pointed (infinity,1)-category]].  Write $M^\Sigma$ for the [[(infinity,1)-category]] of [[pushout|cocartesian squares]] of the form

$$
  \array{
     X &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     {*} &\to& Y
  }
  \,,
$$

where $X$ and $Y$ are [[objects]] of $C$.  Supposing that $C$ admits [[cofibres]] of all [[morphisms]], then one sees that the functor $M^\Sigma \to C$ given by evaluation at the initial vertex ($X$) is a [[trivial fibration]].  Hence it admits a [[section]] $s : C \to M^\Sigma$.  Then the **suspension functor** $\Sigma_C : C \to C$ is the [[composite]] of $s$ with the functor $M^\Sigma \to C$ given by evaluating at the final vertex ($Y$).

$\Sigma_C$ is [[left adjoint]] to the [[loop space functor]] $\Omega_C$.

For $X$ a pointed object of a [[Grothendieck (∞,1)-topos]] ${\mathcal{H}}$, the suspension object $\Sigma X$ is homotopy equivalent to $B{\mathbb{Z}}\wedge X$, the smash product by the classifing space of the discrete group of integers.

We outline a proof below. For $X$ a pointed object of a Grothendieck (∞,1)-topos ${\mathcal{H}}$, its _reduced free group_, denoted by $F[X]$, is the left adjoint to the functor $\Omega {\mathbf{B}}:Grp(\mathcal{H})\to \mathcal{H}_*$ which sends a [[groupoid object in an (∞,1)-category|group object internal]]  to ${\mathcal{H}}$ to the loop space of its delooping object.

+-- {: .num_prop #ConstructionOfFreeGroup}
###### Proposition
 For $X$ a pointed object of a Grothendieck (∞,1)-topos ${\mathcal{H}}$, there is a natural equivalence ${\mathbf{B}}F[X]\simeq \Sigma X$.
 =--

+-- {: .proof}
###### Proof
This is due to the adjunction $(\Sigma \vdash \Omega):\mathcal{H}_*\leftrightarrows\mathcal{H}_*$ between suspending and looping and the the adjunction $(\Omega \vdash {\mathbf{B}}):PathConn(\mathcal{H}_*)\leftrightarrows Grp(\mathcal{H})$ between looping and delooping. Indeed, for any group object $H$, the above-mentioned adjunctions imply the following natural equivalences:
$$
  \begin{aligned}
    Grp({\mathcal{H}})(\Omega \Sigma X, H)
    &  \simeq
    PathConn({\mathcal{H}}_*)(\Sigma X, {\mathbf{B}}H)
    \\
    & \simeq
    PathConn({\mathcal{H}}_*)(X, \Omega{\mathbf{B}}H)
    \,,
  \end{aligned}
$$
Hence $\Omega \Sigma X$ has the universal property of the reduced free group. Delooping gives the required result.
 =--

The [[(∞,1)-category]] $Grp(\mathcal{H})$ of group objects internal ${\mathcal{H}}$ is tensored over ${\mathcal{H}}_*$; in particular, for $G$ a group object and $X$ a pointed object, we can form the tensor product $X\otimes G$, which is a group object. Explicitly, this tensor product is required to satisfy a homotopy equivalence $Grp({\mathcal{H}})(\Omega (X\otimes G, H)\simeq PathConn({\mathcal{H}}_*)(X, Grp({\mathcal{H}})(G, H))$, natural in group objects $H$.

+-- {: .num_prop #ConstructionOfTensorProduct}
###### Proposition
 For $X$ a pointed object and $G$ a group object of a Grothendieck (∞,1)-topos ${\mathcal{H}}$, there is a natural equivalence ${\mathbf{B}}(X\otimes G)\simeq X\wedge {\mathbf{B}}G$.
 =--

+-- {: .proof}
###### Proof
This is due to the adjunction $(\Omega \vdash {\mathbf{B}}):PathConn(\mathcal{H}_*)\leftrightarrows Grp(\mathcal{H})$ between looping and delooping and the [[internal hom]] adjunction. Indeed, for any group object $H$, the above-mentioned adjunctions gives the following natural equivalences:
$$
  \begin{aligned}
    Grp({\mathcal{H}})(\Omega (X\wedge {\mathbf{B}}G), H)
    &  \simeq
    PathConn({\mathcal{H}}_*)(X\wedge {\mathbf{B}}G, {\mathbf{B}}H)
    \\
    & \simeq
    PathConn({\mathcal{H}}_*)(X, PathConn({\mathcal{H}}_*)({\mathbf{B}}G, {\mathbf{B}}H))
    \\
    & \simeq
    PathConn({\mathcal{H}}_*)(X, Grp({\mathcal{H}})(G, H))
    \,,
  \end{aligned}
$$
Hence $\Omega (X\wedge {\mathbf{B}}G)$ has the universal property of the tensor product. Delooping gives the required result.
=--

+-- {: .num_lemma #FreeGroupAsTensor}
###### Lemma
 For $X$ a pointed object of a Grothendieck (∞,1)-topos ${\mathcal{H}}$, there is a natural equivalence $F[X]\simeq X\otimes Z$, where $Z$ is the group object whose delooping object is $B {\mathbb{Z}}$, the classifying space of the discrete group of integers. 
 =--

+-- {: .proof}
###### Proof
Since ${\mathcal{H}}$ is a Grothedieck $(\infty,1)$-topos, the $(\infty,1)$-functor $*\to {\mathbf{B}}-:Group(\mathcal{H})\to Func(\Delta^1,\mathcal{H})$ which sends a group object to the map from the terminal object to its delooping object is a $(\infty,1)$-categorial equivalence onto its image, which is the full subcategory of $Func(\Delta^1,\mathcal{H})$ spanned by the effective epimorphisms from the terminal object. Hence, for $H$ a group object, we have 
$$
  \begin{aligned}
    Grp(\mathcal{H})(Z,H)
    &  \simeq
    Func(\Delta^1,{\mathcal{H}})(*\to B{\mathbb{Z}},*\to {\mathbf{B}}H)
    \\
    & \simeq
    {\mathcal{H}}_*(B{\mathbb{Z}},{\mathbf{B}}H)
    \,,
  \end{aligned}
$$
This latter based mapping object is equivalent to the based object of deloopable maps from ${\mathbb{Z}}$ to $\Omega{\mathbf{B}}H$, which is just $\Omega{\mathbf{B}}H$, since ${\mathbb{Z}}$ is the discrete free group on one generator.

Hence, there are the following natural equivalences:
$$
  \begin{aligned}
    Grp({\mathcal{H}})(F[X], H)
    &  \simeq
    PathConn({\mathcal{H}}_*)(X, \Omega{\mathbf{B}}H)
    \\
    & \simeq
    PathConn({\mathcal{H}}_*)(X, Grp(Z, H)
    \,,
  \end{aligned}
$$
Therefore $F[X]$ has the universal property of the tensor product $X\otimes Z$. The required natural equivalence follows by abstract nonsense.
=--

+-- {: .num_theorem #SuspendingAsSmashProd}
###### Theorem
 For $X$ a pointed object of a Grothendieck (∞,1)-topos ${\mathcal{H}}$, there is a natural equivalence $\Sigma X\simeq B{\mathbb{Z}}\wedge X$. 
 =--


+-- {: .proof}
###### Proof
Deloop the natural equivalence in Lemma \ref{FreeGroupAsTensor} to obtain the natural equivalence ${\mathbf{B}}F[X]\simeq {\mathbf{B}}(X\otimes Z)$. By propositions \ref{ConstructionOfFreeGroup} and \ref{ConstructionOfTensorProduct}, this gives the required natural equivalence. 
 =--

### As an ordinary functor

Let $C$ be a [[category]] admitting small [[colimits]].  Let $\Phi$ be a [[graded monoid]] in the [[category]] of [[groups]] and $F : C \to C$ a $\Phi$-symmetric [[endofunctor]] of $C$ that commutes with small [[colimits]].  Let $Spect_F^{\Phi}(C)$ denote the [[category]] of $\Phi$-symmetric $F$-[[spectrum objects]] in $C$.

Following [Ayoub](#Ayoub), the [[evaluation]] functor
  $$ Ev^n : Spect_F^{\Phi}(C) \to C, $$
which "evaluates" a symmetric spectrum at its $n$th component, admits under these assumptions a [[left adjoint]]
  $$ Sus^n : C \to \Spect_F^\Phi(C) $$
called the $n$th **suspension functor**, more commonly denoted $\Sigma_C^{\infty-n}$.

When $C$ is [[symmetric monoidal category|symmetric monoidal]], and in the case $\Phi = \Sigma$ and $F = T \otimes -$ for some object $T$, there is an induced [[symmetric monoidal structure]] on $Spect^\Sigma_T(C)$ as described at [[symmetric monoidal structure on spectrum objects]].

**Proposition.** One has
  $$ Sus^p_T(X) \otimes Sus^q_T(Y) \simeq Sus^{p+q}_T(X \otimes Y) $$
for all $X,Y \in C$.  In particular, $Sus = Sus^0 : C \to \Spect^\Sigma_T(C)$ is a [[symmetric monoidal functor]].

## Examples

* In [[Top]], this is the [[reduced suspension]] of a space.

* In a [[category of chain complexes]] the [[suspension of a chain complex]] is given by shifting the degrees of the chain complex up by one.

## Related concepts

* [[loop space object]], [[free loop space object]],

  * [[delooping]]

  * [[loop space]], [[free loop space]], [[derived loop space]]

* **suspension object**

  * [[suspension type]]

  * [[suspension]], [[reduced suspension]]

## References

A detailed treatment of the 1-categorical case is in the last chapter of

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique, I_. Ast&#233;risque, Vol. 314 (2008). Soci&#233;t&#233; Math&#233;matique de France. ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))
{#Ayoub}


[[!redirects suspension object]]
[[!redirects suspension objects]]
