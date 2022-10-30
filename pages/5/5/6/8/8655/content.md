
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

In fundamental physics, notably in [[quantum field theory]] and [[string theory]] one often says that a non-trivial [[equivalence]] of [[quantum field theories]] between two [[models (in theoretical physics)]] is a "[[duality]]". 

## Examples

* [[Kramers-Wannier duality]]

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



## Formalization and Relation to mathematical duality
 {#Formalization}

One should beware that the use of the word "duality" in physics is in general different from concepts called "[[duality]]" in [[mathematics]].

For instance in [[T-duality]] only simple cases exhibit such obviously "dual" behaviour and in general cases such as [[U-duality]] really only the notion of _[[equivalence]]_ remains. In some cases such as _[[Montonen-Olive duality]]/[[S-duality]]_ the equivalence involves some actual [[duality]] in the mathematical sense, as in replacing the [[gauge group]] by its [[Langlands dual group]]. 

One way to pseudo-formalize accurately most of what is usually meant by "duality" in physics might instead be the following.


Write $LagrangianData$ for a [[moduli stack]] of [[prequantum field theory]] data consisting of species of [[field (physics)|fields]] and of [[Lagrangians]]/[[action functionals]] defined  on these.

+-- {: .num_example #LagrangianDataInCaseOfMirrorSymmetry}
###### Example

For the well-understood case of [[mirror symmetry]] this would be the usual [[moduli space]] of [[Calabi-Yau manifolds]] regarded as the Lagrangian data for the [[2d (2,0)-superconformal QFT]].

=--

One imagines that [[quantization]] gives a map from such [[prequantum field theory|prequantum data]] to a moduli stack $QFTs$ of actual [[quantum field theories]]

$$
  quantization \;\colon\; LagrangianData \longrightarrow QFTs
  \,.
$$


+-- {: .num_example #}
###### Example

Continuing example \ref{LagrangianDataInCaseOfMirrorSymmetry} 
in the case of [[mirror symmetry]] this would be the [[TCFT]]-construction that takes a [[Calabi-Yau manifold]] to its [[Calabi-Yau A-∞ category]] ("of branes") which defines the corresponding [[2d TQFT]] via the [noncompact version](cobordism%20hypothesis#ForNoncompactCobordisms) of the [[cobordism hypothesis]].

=--

The [[1-image]] of this map would be the moduli space of [[Lagrangian field theory|Lagrangian quantum field theories]] 

$$
  quantization 
    \;\colon\; 
  LagrangianData \longrightarrow LagrangianQFTs
  \hookrightarrow
  QFTs
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

This construction is the first step in associating the [[groupoid object in an (∞,1)-category]] which is induced by the [[atlas]] "quantization" via [[Giraud's theorem]] of [[Higher Topos Theory]].

It continues in the way that [[Cech covers]] do (whence one speaks of the _[[Cech nerve]]_ construction of the quantization map $LagrangianData \to LagrangianQFTs$): above "$Dualities$" there is the space of triples of Lagrangian data that all have the same quantization, equipped with dualities between any two of them, and equipped with an equivalence of dualities (hence a "duality of dualities") between the composite of two of these and the third:

$$
  \array{
    && \vdots
   \\
  DualitiesOfdualities &\simeq& LagrangianData \underset{LagrangianQFT}{\times} LagrangianData \underset{LagrangianQFT}{\times} LagrangianDat
   \\
    && \downarrow \downarrow \downarrow
    \\
  Dualities &\simeq& LagrangianData \underset{LagrangianQFT}{\times} LagrangianData
   \\
   && \downarrow \downarrow
   \\
   && LagrangianData
  }
$$

It continues this way through all $n$-fold dualities of dualities.
The resulting $\infty$-groupoid object has as moduli stack of objects $LagrangianData$ and as moduli stack of 1-morphisms $Dualities$. Its corresponding [[stack]] realization is $LagrangianQFTs$ and so the corresponding [[augmented simplicial set|augmented]] [[simplicial object]] looks as

$$
  \array{
     \vdots
     \\
     \downarrow\downarrow\downarrow\downarrow
     \\
     DualitiesOfDualities
     \\
     \downarrow\downarrow\downarrow
     \\
     Dualities
     \\
     \downarrow \downarrow
     \\
     LagrangianData
     \\
     \downarrow^{\mathrlap{quantization}}
     \\
     LagrangianQFTs
  }
  \,.
$$


Such towers are to be thought of as the incarnation of [[equivalence relations]] as we pass to [[(∞,1)-category theory]]: A plain [[equivalence relation]] is just the first stage of such a tower


$$
  \array{
     Dualities 
     \\
     \downarrow \downarrow
     \\
     Lagrangians
  }
$$

The conditions on an equivalence relation -- reflexivity, transitivity, symmetry -- may be read as those on a [[groupoid object]] -- identity, composition, inverses. So now in homotopy logic this is boosted to an [[groupoid object in an (∞,1)-category]] by relaxing all three to hold only up to higher coherent homotopies.

The bottom-most arrow 

$$
  \array{
     LagrangianData
     \\
     \downarrow^{\mathrlap{quantization}}
     \\
     LagrangianQFTs
  }
$$

is the quotient projection of the equivalence relation. In 1-logic this would be its [[cokernel]], here in homotopy logic it is the [[homotopy colimit]] over the full [[simplicial object|simplicial]] diagram.

So the perspective of the full diagram gives the usual way of speaking in QFT also a reverse:

instead of saying 

a) that two Lagrangians are dual if there is an equivalence between the QFTs which they induce under quantization, 

we may turn this around and say that therefore 

b) quantization is the result of forming the [[homotopy quotient]] of the space of Lagrangian data by these duality relations.

It is one of the clauses of the [[Giraud theorem]] in [[(∞,1)-topos theory]] that these two perspectives are equivalent.

## Related concepts

* [[parent action functional]]

There is also a duality in the _description_ of physics:

[[!include Isbell duality - table]]

## References

* {#Polchinski14} [[Joseph Polchinski]], _Dualities_ ([arXiv:1412.5704](http://arxiv.org/abs/1412.5704))

* [[Cumrun Vafa]], sround 12:00 of _On Mathematical Aspects of String Theory_ ([video](https://www.youtube.com/watch?v=yreUdrIbt2Q))

[[!redirects dualities in physics]]