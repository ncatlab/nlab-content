
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In fundamental physics, notably in [[quantum field theory]] and [[string theory]] one often says that a non-trivial [[equivalence]] between two [[models (in theoretical physics)]] is a [[duality]]. 

## Examples

* [[Seiberg duality]], [[AGT conjecture]]

* [[S-duality]]

  * [[electro-magnetic duality]], [[Montonen-Olive duality]], [[geometric Langlands duality]]

* [[T-duality]]
  
  * [[mirror symmetry]]

* [[U-duality]]

* [[open/closed string duality]]

  * [[AdS/CFT|AdS/CFT duality]]

  * [[KLT relations]]

While most of these dualities refer to equivalences between [[quantum field theories]], they find their conceptual explanation in [[string theory]]. See at 

* [[duality in string theory]] 

for more.

## Relation to mathematical duality

In some cases such as _[[Montonen-Olive duality]]/[[S-duality]]_ the equivalence involves some actual [[duality]] in the mathematical sense, as in replacing the [[gauge group]] by its [[Langlands dual group]]. In [[T-duality]] only simple cases exhibit such obviously "dual" behaviour and in general cases such as [[U-duality]] really only the notion of _[[equivalence]]_ remains.

## Formalization
 {#Formalization}

One way to pseudo-formalize accurately most of what is usually meant by "duality" in physics might be the following.


Write $LagrangianData$ for a [[moduli stack]] of [[prequantum field theory]] data consisting of species of [[field (physics)|fields]] and of [[Lagrangians]]/[[action functionals]] defined  on these.

For instance for well-understood [[mirror symmetry]] this would be the usual [[moduli space]] of [[Calabi-Yau manifolds]] regarded as the Lagrangian data for the [[2d (2,0)-superconformal QFT]].

One imagines that [[quantization]] gives a map from such [[prequantum field theory|prequantum data]] to a moduli stack $QFTs$ of actual [[quantum field theories]]

$$
  quantization \;\colon\; LagrangianData \longrightarrow QFTs
  \,.
$$

For instance, in the case of mirror symmetry this would be the [[TCFT]]-construction that takes a Calabi-Yau manifold to the corresponding [[Calabi-Yau category]].

The [[essential image]] of this map would be the moduli space of [[Lagrangian field theory]]

$$
  quantization \;\colon\; LagrangianData \longrightarrow LagrangianQFTs
  \,.
$$

By assumption this is now a [[1-epimorphism]] and hence an [[atlas]] of [[moduli stacks]].

The physical concept of duality, such as in [[mirror symmetry]], says that two points $L_1, L_2 \colon \ast \to LagrangianData$ in the space of Lagrangian data are "dual" to each other, if they become equivalent as quantum field theories after [[quantization]].

Mathematically this means that the space of such "dualities" is the [[homotopy fiber product]]

$$
  \array{
     && Dualities 
     \\
     & \swarrow && \searrow
     \\
     LagrangianData && \swArrow_{\simeq} && LagrangianData
     \\
     & {}_{\mathllap{quantization}}\searrow && \swarrow_{\mathrlap{quantization}}
     \\
     && LagrangianQFTs
  }
$$

By definition, an element of $Dualities$ is two Lagrangians and a choice of equivalence of their associated quantum field theories:

$$
  quantization(L_1) \simeq quantization(L_2)
  \,.
$$

This construction is the first step in associating the [[groupoid object in an (infinity,1)-category]] which is induced by the [[atlas]] "quantization" via [[Giraud's theorem]] of [[Higher Topos Theory]].

This groupoid has as moduli stack of objects $LagrangianData$ and as moduli stack of 1-morphisms $Dualities$. Its corresponding [[stack]] realization is $LagrangianQFTs$

$$
  \array{
     \vdots
     \\
     \downarrow\downarrow\downarrow
     \\
     Dualities
     \\
     \downarrow \downarrow
     \\
     LagrangianData
     \\
     \downarrow 
     \\
     LagrangianQFTs
  }
  \,.
$$

## Related concepts

* [[parent action functional]]

There is also a duality in the _description_ of physics:

[[!include Isbell duality - table]]

[[!redirects dualities in physics]]
