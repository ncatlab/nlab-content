
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

An _orbispace_ is a [[space]], specifically a [[topological stack]],  that is locally modeled on the [[homotopy quotient]]/[[action groupoid]] of a [[locally compact topological space]] by the  [[action]] of a [[compact topological group]]. Thus orbispaces are to [[topological spaces]] roughly  what [[orbifolds]] are to [[manifolds]]. 

As to what this means precisely, there is a good deal of variance in the literature:

Following [Haefliger 90](#Haefliger90), early references on orbispaces essentially mean just the [[topological space|topological]] version of _[[orbifold]]_ (i.e. without considering [[smooth structure]]), which, in the language of [[étale stacks]], means to consider [[topological groupoids]]/[[topological stacks]] instead of [[Lie groupoids]]/[[differentiable stacks]]  ([Haefliger 84](#Haefliger84), [Haefliger 91, 5](#Haefliger91), [Chen 01](#Chen01), [Henriques 01](#Henriques01), [Henriques 05](#Henriques05)). Hence this use of the term "orbispace" is such as to complete the following patter:

$$
  \array{
    \text{smooth manifold} 
    & 
    \text{topological manifold}    
    \\
    \text{orbifold} & {\color{blue}\text{orbispace}}
    \\ 
    \text{Lie groupoid} & \text{topological groupoid}
    \\ 
    \text{differentiable stack} & \text{topological stack}
  }
$$

However, in [Henriques-Gepner 07](#HenriquesGepner07) it was suggested that orbispaces should be these topological groupoids but regarded in [[global homotopy theory]] as the [[(∞,1)-presheaves]] on a [[global orbit category]] which they represent:

$$
  \array{
    TopologicalGroupoids
    &\overset{\prec}{\longrightarrow}&
    Orbispaces
    \\
    \mathcal{X}
    &\mapsto&
    (G \mapsto Maps(\mathbf{B}G, \mathcal{X}))
  }
$$

This use of the term has become adopted among ([[equivariant homotopy theory|equivariant]]) [[homotopy theory|homotopy theorists]] (e.g. [Rezk 14](#Rezk14), [Koerschgen 16](#Koerschgen16), [Schwede 17](#Schwede17), [Lurie EllIII](#LurieEllIII), [Juran 20](#Juran20)). But even here there are at least two variants of the definition to be distinguished, depending on whether the morphisms in the [[global orbit category]] are taken to be general or only [[injective map|injective]] [[group homomorphisms]].



## Definition

Write $Orb$ for the [[global orbit category]]. Then its [[(∞,1)-presheaf (∞,1)-category]] $PSh_\infty(Orb)$ is the [[(∞,1)-category]] of _orbispaces_. ([Henriques-Gepner 07](#HenriquesGepner07), [Rezk 14, remark 1.5.1](#Rezk14))



## Properties

### Relation of global equivariant homotopy theory

By the main theorem of ([Henriques-Gepner 07, (4)](#HenriquesGepner07)) the [[(∞,1)-presheaves]] on the global [[orbit category]] are equivalently "cellular" [[topological stacks]]/[[topological groupoids]] ("[[orbispaces]]"), we might write this as

$$
  TopGrpd^{cell} \simeq PSh_\infty(Orb)
  \,.
$$

Hence cellular topological stacks are equivalently the objects of [[equivariant homotopy theory]].

See also ([Rezk 14, p. 4 and section 7](#Rezk14))


### Relation to $G$-equivariant homotopy theory

Fixing a [[compact topological group]] $G$ and writing $\mathbf{B}G \simeq \ast // G$ for its [[delooping]] stack (the moduli stack of $G$-[[principal bundles]]), then the [[slice (infinity,1)-category|slice]] homotopy theory of topological stacks over $\mathbf{B}G$ on the [[representable morphisms]] (those inducing closed monos on isotropy groups) is equivalently that of [[topological G-spaces]] (with their G-equivariant homotoy theoretical structure, see at _[[equivariant Whitehead theorem]]_):

$$
  TopGrpd_{/\mathbf{B}G}^{reprs.} \simeq G Spaces
$$

([Henriques-Gepner 07, p.7](#HenriquesGepner07))



## Related concepts

* [[Elmendorf's theorem]]

* [[orbispace cohomology]]

[[!include equivariant homotopy theory -- table]]


## References

Orbispaces as the topological version of [[orbifolds]] (in particular as [[topological groupoids]]/[[topological stacks]]):

* {#Haefliger84} [[André Haefliger]], _Groupoides d'holonomie et classifiants_, Astérisque no. 116  (1984), p. 70-97 ([numdam:AST_1984__116__70_0](http://www.numdam.org/item/?id=AST_1984__116__70_0))

* {#Haefliger90} [[André Haefliger]], _Orbi-Espaces_,  In: E. Ghys, P. de la Harpe (eds.), _Sur les Groupes Hyperboliques d’après Mikhael Gromov_, Progress in Mathematics, vol 83. Birkhäuser 1990 ([doi:10.1007/978-1-4684-9167-8_11](https://doi.org/10.1007/978-1-4684-9167-8_11))

  (apparently the term is first used here?)

* {#Haefliger91} [[André Haefliger]], _Complexes of Groups and Orbihedra_, in: E. Ghys, A. Haefliger, A Verjovsky (eds.), _Proceedings of the Group Theory from a Geometrical Viewpoint_, ICTP, Trieste, Italy , 26 March – 6 April 1990_, World Scientific 1991 ([doi:10.1142/1235](https://doi.org/10.1142/1235))


* {#Chen01} [[Weimin Chen]], _A homotopy theory of orbispaces_ ([arXiv:math/0102020](http://arxiv.org/abs/math/0102020))

* {#Henriques01} [[André Henriques]], _Orbispaces and orbifolds from the point of view of the Borel construction, a new definition_ ([arXiv:0112006](http://arxiv.org/abs/math/0112006))

* {#Henriques05} [[André Henriques]], _Vector bundles on orbispaces_ (2005) ([pdf](http://andreghenriques.com/PDF/orbiabstract.pdf), [[HenriquesVectorBundlesOnOrbispaces.pdf:file]])

The idea to regard these topological groupoids as in [[global homotopy theory]] via the [[(infinity,1)-presheaves]] on a [[global orbit category]] which they represent is due to

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

developed further in

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)
 
* {#Koerschgen16} [[Alexander Körschgen]]: _A Comparison of two Models of Orbispaces_, Homology, Homotopy and Applications **20** 1  (2018) 329--358 &lbrack;[arXiv:1612.04267](https://arxiv.org/abs/1612.04267), [doi:10.4310/HHA.2018.v20.n1.a19](https://doi.org/10.4310/HHA.2018.v20.n1.a19)&rbrack;

* {#Schwede17} [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_, Mathematische Zeitschrift 294 (2020), 71-107 ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019))

* {#Juran20} [[Branko Juran]], _Orbifolds, Orbispaces and Global Homotopy Theory_ &lbrack;[arXiv:2006.12374](https://arxiv.org/abs/2006.12374)&rbrack;

See also

* {#LurieEllIII} [[Jacob Lurie]], Section 3 of _Elliptic cohomology III: Tempered Cohomology_, 2019 ([pdf](http://www.math.harvard.edu/~lurie/papers/Elliptic-III-Tempered.pdf))

[[!redirects orbispaces]]
