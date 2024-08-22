
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents


## Idea

The *reflection* of an [[object]] $d$ in a [[category]] $D$ along a [[functor]] $F \colon  C\to D$ is a [[morphism]] $\eta_d$ in $D$, playing the role of a  would-be [[unit of an adjunction]] $L\dashv F$ (which may not exist in general), satisfying that part of the [[universal property]] of the unit for that component. If a reflection of each object in $D$ along $F$ exists and is chosen then the [[left adjoint]] $L$ to $F$ does exists.

Similarly, one can define a coreflection along a functor by a [[morphism]] $\epsilon_d$ in $D$ playing the role of the would-be [[counit of an adjunction]] $F\dashv R$.

## Definition

Let $F \colon C\to D$ be a [[functor]] and $d$ an object of the [[category]] $D$. 

A __reflection__ of $d$ along $F$ is a [[pair]] $(L_d,\eta_d)$ of 

* an [[object]] $L_d\in C$ 

* a [[morphism]] $\eta_d \colon d\to F(L_d)$ in $D$ 

which is [[universal property|universal]] in the sense that for any [[object]] $c \in C$ and morphism $f \colon d\to F(c)$ there is a unique $\alpha \colon L_d\to c$ such that $F(\alpha)\circ\eta_d = f$. 

In other words this means that a reflection is an [[relative adjunction|adjoint relative to]] the functor $1 \to D$ which picks out $d \in D$.

[[formal duality|Dually]], a  __coreflection__ of $d$ along $F$ is a [[pair]] $(R_d,\epsilon_d)$ of 

* an [[object]] $R_c\in C$ 

* a [[morphism]] $\epsilon_d \colon F(R_d)\to d$ in $D$ 

which is universal in the sense that for any $c\in C$ and a morphism $g \colon F(c)\to d$ there is a unique $\beta \colon c\to R_d$ such that $\epsilon_d\circ F(\beta) = g$. 

In other words this means that a coreflection is a [[relative coadjunction|coadjoint relative to]] the functor $1 \to D$ which picks out $d \in D$.


## Related concepts

* [[relative adjunction]]

## Literature 

*  [[Francis Borceux]], _[[Handbook of Categorical Algebra]]_,  I.3.1

[[!redirects coreflection along a functor]]

