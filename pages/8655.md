
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

* [[quark-hadron duality]]


[[!include duality in string theory -- contents]]



## Formalization and Relation to mathematical duality
 {#Formalization}


One should beware that the use of the word "duality" in physics is in general different from concepts called "[[duality]]" in [[mathematics]].

For instance in [[T-duality]] only simple cases exhibit such obviously "dual" behaviour and in general cases such as [[U-duality]] really only the notion of _[[equivalence]]_ remains. This more closely resembles the mathematical concept of [[Morita equivalence]], see [Relation to Morita equivalence](#Morita). However, in some cases such as _[[Montonen-Olive duality]]/[[S-duality]]_ the equivalence involves some actual [[duality]] in the mathematical sense, as in replacing the [[gauge group]] by its [[Langlands dual group]]. 

### General formulation
 {#FormalizationGeneral}

One way to accurately formalize most of what is usually meant by "duality" in physics might instead be the following.

\linebreak

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

### Examples
 {#FormalizationExamples}

For a concrete example of the [above](#FormalizationGeneral), consider the class of [[Chern-Simons theories]] and [[Rozansky-Witten theories]]. As [[Lagrangian field theories]] they are very different, but after [[perturbative quantum field theory|perturbative quantization]], their [[Lagrangian density|Lagrangian data]] maps to the same  abstract vector space of [[quantum observables]]: the [[Vassiliev knot invariants]].

Concretely, in both cases the map from [[Lagrangian density|Lagrangian data]] to [[quantum observables]] is given by the assignment of [[weight systems]] on [[Jacobi diagrams]], namely:

1) [[Lie algebra weight systems]] for [[Chern-Simons theory]]

<center>
<img src="https://ncatlab.org/nlab/files/AssignLieAlgebraWeightSystems.jpg" width="440">
</center>

2) [[Rozansky-Witten weight systems]] for [[Rozansky-Witten theory]]

<center>
<img src="https://ncatlab.org/nlab/files/AssignRozanskyWittenWeightSystems.jpg" width="440">
</center>


The corresponding [[Wilson loop]] [[quantum observables]] are the evaluation of these [[weight systems]] on the [[universal Vassiliev invariant]]

1) [[Chern-Simons theory]] [[Wilson loop observables]]:

<center>
<img src="https://ncatlab.org/nlab/files/TheGrandStoryOfVassilievKnotInvariantsIII.jpg" width="800">
</center>

2) [[Rozansky-Witten theory]] [[Wilson loop observables]]:

<center>
<img src="https://ncatlab.org/nlab/files/TheGrandStoryOfRozanskyWittenKnotInvariantsIII.jpg" width="800">
</center>

Hence in total we have the following quantization map from Lagrangian data to observables:

<center>
<img src="https://ncatlab.org/nlab/files/AssignCSAndRWObservables.jpg" width="440">
</center>

To the extent that all observables of these theories, on the [[3-sphere]], are [[Wilson loop observables]], we must regard as physically equivalent any two elements on the left of this map (Lagrangian field theories) whose image on the right coincides. The space of such pairs is the [[fiber product]] of this quantization map with itself:

<center>
<img src="https://ncatlab.org/nlab/files/DualitiesOfCSAndRWTheories.jpg" width="400">
</center>



### Relation to Morita equivalence
 {#Morita}

According to [Schwarz 04](#Schwarz04):

> I am convinced that the mathematical notion of [[Morita equivalence]] of [[associative algebras]] and its generalization for [[differential algebra|differential associative algebras]] should be regarded as the mathematical foundation of [[duality in string theory|dualities in string/M-theory]]. 

[[Albert Schwarz|Schwarz]] showed that [[KK-compactifications]] on [[Morita equivalence|Morita equivalent]] [[noncommutative tori]] are physically equivalent ([Schwarz98](#Schwarz98)). This work is followed up in relation to [[T-duality]] in [Pioline99](#Pioline99) and [CNS11](#CNS11).

[BMRS08](#BMRS08) discusses an axiomatic definition of [[topological T-duality]] generalizing and refining T-duality between noncommutative spaces in terms of Morita equivalence to a special type of [[KK-theory|KK-equivalence]], which defines a T-duality action that is of order two up to Morita equivalence.

In [Okada09](#Okada09) a variant of [[mirror symmetry]] is shown to be a form of [[derived Morita equivalence]].

Morita theoretic ideas are also involved in [[factorization homology]], the [[blob complex]] and premodular TQFTS, see [MW10](#MW10), [BZBJ15](#BZBJ15), and [Scheimbauer](#Scheimbauer) for the Morita $(\infty, n)$-category of $E_n$-algebras.

## Duality after compactification

Informal comments on a possible general picture of duality in physics arising from [[duality in string theory]], especially after [[KK-compactification]], from [Brennan, Carta &amp; Vafa 17, p. 7](duality+in+string+theory#BrennanCartaVafa17):

> Since we have seen that the full [[string theories]] are all interrelated by a sequence of [[duality in string theory|dualities]], one would expect that their [[KK-compactification|compactifications]] are also related by dualities. As it turns out, these relations are so abundant that we can make the following observation:

> **"Conjecture"**: Whenever the [[dimension]], [[number of supersymmetries|number of preserved supercharges]], and [[chiral fermion|chiralities]] of two different [[string theory vacuum|compactifications of string theory]] match, there are choices of [[KK-compactification|compactification geometries]] such that they are dual descriptions of the same physical theory.

> Surprisingly, we are aware of no known counter examples. In this sense, dualities in lower dimensional theories are not hard to find, but rather are  hard to prevent! One rationale for the existence of dualities is as Sergio Cecotti puts it, “the scarcity of rich structures”. In particular the very existence of quantum systems of gravity is hard to arrange and if we succeed to get more than one theory with a given symmetry, there is a good chance we have landed on the same theory.



## Related concepts

* [[parent action functional]]

There is also a duality in the _description_ of physics:

[[!include Isbell duality - table]]

## References

### General

* {#AlvarezGaume98} [[Luis Alvarez-Gaumé]], Frederic Zamora, _Duality in Quantum Field Theory (and String Theory)_, AIP Conference Proceedings 423, 46 (1998) ([arXiv:hep-th/9709180](https://arxiv.org/abs/hep-th/9709180))

* {#Corfield17} [[David Corfield]], _Duality as a category-theoretic concept_, Studies in History and Philosophy of Modern Physics Volume 59, August 2017, Pages 55-61 ([doi:10.1016/j.shpsb.2015.07.004](https://doi.org/10.1016/j.shpsb.2015.07.004))


### As Morita equivalence

On the idea that duality in physics may be captured by the notion of [[Morita equivalence]]:

* {#Schwarz98} [[Albert Schwarz]], _Morita equivalence and duality_ ([arXiv:hep-th/9805034](http://arxiv.org/abs/hep-th/9805034))

* {#Pioline99} B. Pioline, [[Albert Schwarz]], _Morita equivalence and T-duality (or $B$ versus $\Theta$)_ ([arXiv:hep-th/9908019](http://arxiv.org/abs/hep-th/9908019))

See also

* {#Schwarz04} [[Albert Schwarz]], _My Life In Science_, 2004 ([pdf](https://www.math.ucdavis.edu/~schwarz/bion.pdf), [[AlbertSchwarzLifeInScience.pdf:file]])

Specifically concerning [[T-duality]]:

* {#CNS11} Ee Chang-Young, Hiroaki Nakajima, Hyeonjoon Shin, _Fermionic T-duality and Morita Equivalence_ ([arXiv:1101.0473](http://arxiv.org/abs/1101.0473))

* {#BMRS08} [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-branes, KK-theory and duality on noncommutative spaces_, ([pdf](http://eprints.soton.ac.uk/46524/1/D-branes,_KK-theory_and__duality_on_noncommutative_spaces_BRMS_Published_JoP.pdf))

Specifically concerning [[mirror symmetry]]:

* {#Okada09} So Okada, _Homological mirror symmetry of Fermat polynomials_ ([arXiv:0910.2014](http://arxiv.org/abs/0910.2014))


See also more general discussion of [[Morita equivalence]]:

* {#BZBJ15} [[David Ben-Zvi]], Adrien Brochier, David Jordan, _Integrating quantum groups over surfaces: quantum character varieties and topological field theory_, ([arXiv:1501.04652](http://arxiv.org/abs/1501.04652))

* {#MW10} [[Scott Morrison]], [[Kevin Walker]], _The blob complex_, ([arXiv:1009.5025](http://arxiv.org/abs/1009.5025))

* {#Scheimbauer} Claudia Scheimbauer, _Factorization Homology as a Fully Extended Topological Field Theory_, ([pdf](http://math.unice.fr/~cazanave/Gdt/FH/ScheimbauerThesisJuly4FINAL.pdf))


### Duality in string theory

On [[duality in string theory]] (but see there fore more):

* {#Polchinski14} [[Joseph Polchinski]], _Dualities_ ([arXiv:1412.5704](http://arxiv.org/abs/1412.5704))

* [[Cumrun Vafa]], around 3:30, 12:00 of _On Mathematical Aspects of String Theory_ ([video](https://www.youtube.com/watch?v=yreUdrIbt2Q))

 


[[!redirects dualities in physics]]

