

[[BV-BRST complex]] is model in [[higher geometry|higher]] [[synthetic differential geometry|infinitesimal geometry]] of a _[[reduced phase space]]_ in [[higher geometry]]: the [[quotient]] of the [[intersection]] of the [[equations of motion]] by the [[gauge symmetries]]:


| [[homotopy quotient]] | [[derived intersection]] |
|-----------------------|--------------------------|
| [[gauge symmetry]]    | [[equations of motion]]  |
| [[BRST complex]]      |  [[BV complex]]          |


Let 

$$
  X 
  \;\coloneqq\; 
  Spec( \mathbb{R}[ [ \Phi^1, \Phi^2, \cdots ] ] )
$$ 

be the [[formal dual]] to a [[formal power series algebra]] in coordinates $\Phi^a$, the _[[field (physics)|fields]]_


(Really: [[infinitesimal neighbourhood]] of a point in a [[jet bundle]].)

Let

$$
  R 
  \;\colon\;
  \mathfrak{g}
  \longrightarrow
  T X 
$$

a [[Lie algebra action]], given in [[coordinates]] by

$$
  R
  \;=\; 
  C^\alpha R_\alpha^a \partial_{\Phi^a}
$$

where $\langle C^\alpha\rangle = \mathfrak{g}^\ast$ is a [[dual basis]] for.

The corresponding [[homotopy quotient]] 

$$
  X/\mathfrak{g}
$$

has a [[differential graded-commutative algebra|differential graded commutative]] [[algebra of functions]] the [[BRST complex]]

$$
  C^\infty(X/\mathfrak{g})
  \;=\;
  \left( 
     \wedge^\bullet_{C^\infty(X)} \langle C^\alpha\rangle
     ,\,
     d_{BRST}
  \right)
$$

with differential

$$
  \Phi^a \mapsto C^\alpha R_\alpha^a 
$$

$$
  C^\alpha \mapsto \tfrac{1}{2}K^\alpha{}_{\beta \gamma} c^\beta \wedge c^\gamma
$$

If $X = \ast$ then this is the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$

| name |  symbol  | degree |
|------|----------|--------|
| [[field (physics)|field]] | $\Phi^a$ |  0 |
| [[ghost field]] | $C^\alpha$  |  +1  |
| [[antifield]] |  $\overline{\Phi}^a$ | -1 |
| [[antifield|anti ghost field]] | $\overline{C}^\alpha$ | -2 |


Proposition

A function $S\colon X \longrightarrow \mathbb{C}$ descends precisely if it is gauge invariant

$$
  \array{
     X &\overset{S}{\longrightarrow}& \mathbb{C}
     \\
     \downarrow & \nearrow
     \\
     X/\mathfrak{g}
  }
$$


In this case $d S$ it may be regarded as a section

$$
  \array{
    X/\mathfrak{g} 
     &\overset{d S}{\longrightarrow}&
   T^\ast (X/\mathfrak{g})
  }
$$

where the cotangent bundle is defined to have as functions the algebra of derivations

$$
  C^\infty( T^\ast(X/\mathfrak{g}) )
  =
  Sym_{C^\infty(X/\mathfrak{g})}(Der(C^\infty(X/\mathfrak{g})))
$$

with differential $[d_{BRST,-}]$.


The derivation with respect to $$

The [[derived critical locus]] of $S$ is the homotopy pullback

$$
  \array{
    (X/\mathfrak{g})_{d S =0} &\longrightarrow& X/\mathfrak{g}
    \\
    \downarrow
       && 
    \downarrow^{\mathrlap{0}}
    \\
    X/\mathfrak{g} 
     &\underset{dS}{\longrightarrow}&
   T^\ast (X/\mathfrak{g})
  }
$$

Proposition:

This has the same generators as the BRST complex together with the derivations shifted by in degree by -1

$$
  \overline \Phi^a
  \;\coloneqq\;
  \underset{-1}\underbrace{\frac{\partial}{\partial \Phi^a}}
$$

$$
  \overline C^a
  \;\coloneqq\;
  \underset{-2}\underbrace{\frac{\partial}{\partial C^a}}
$$

the BV-BRST differential is given by

$$
  \Phi^a \mapsto C^\alpha K_\alpha^a
$$

$$
  C^\alpha \mapsto \frac{1}{2}K^\alpha{}_{\beta \gamma} C^\beta \wedge C^\gamma
$$

as before, together with

$$
  \frac{\partial}{\partial C^\alpha} 
   \mapsto 
  R_\alpha^a \frac{\partial}{\partial \Phi^a} + K^\alpha{}_{\beta \gamma} C^\gamma 
  \frac{\partial}{\partial C^\beta}
$$

$$
  \frac{\partial}{\partial \Phi^a} \mapsto \frac{\partial S}{\partial \Phi^a}
    + 
    C^\alpha \frac{\partial R_\alpha^b}{\partial \Phi^b} \frac{\partial}{\partial \Phi^b}
$$


**Goal** in field theory: 

Find $R$ so that the BV-BRST complex has no cohomology in negative degee

**Fact**

implies that quantization by causal perturbation theory applies
