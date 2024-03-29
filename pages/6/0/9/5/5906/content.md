
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $\mathbb{T}$ a [[theory]], the _syntactic site_ of a [[syntactic category]] $\mathcal{C}_{\mathbb{T}}$  is the structure of a [[site]] on $\mathcal{C}_{\mathbb{T}}$ such that [[geometric morphisms]] $\mathcal{E} \to Sh(\mathcal{C}_{\mathbb{T}})$ into the [[sheaf topos]] over the syntactic site are equivalent to [[models]] for the [[theory]] $\mathbb{T}$ in $\mathcal{E}$, hence such that $Sh(\mathcal{C}_{\mathbb{T}})$ is the [[classifying topos]] for $\mathbb{T}$.

## Definition

For $\mathbb{T}$ a [[theory]] and $\mathcal{C}_{\mathbb{T}}$ its [[syntactic category]], we define [[coverage]]s $J$ on $\mathcal{C}_{\mathbb{T}}$. These depend on which type of theory $\mathbb{T}$ is (or is regarded to be).


+-- {: .num_defn #TheCoverage}
###### Definition

* For $\mathbb{T}$ a [[cartesian theory]], $J$ is the trivial coverage: the covering families consist of single [[isomorphism]]s.

* For $\mathbb{T}$ a [[regular theory]], $J$ is the [[regular coverage]]: the [[covering]] families consist of single [[regular epimorphism]]s.

* For $\mathbb{T}$ a [[coherent theory]], $J$ is the [[coherent coverage]]: the [[covering]] families consist of morphisms $\{U_i \to U\}$ such that the union $\cup_i U_i \simeq U$ equals $U$.

* For $\mathbb{T}$ a [[geometric theory]], $J$ is the [[geometric coverage]]

=--

## Properties

+-- {: .num_prop}
###### Proposition

For $\mathcal{T}$ a [[cartesian theory]], [[regular theory]], etc. and $\mathcal{C}_{\mathbb{T}}$ its syntactic site, according to def. \ref{TheCoverage}, we have

* For $\mathbb{T}$ a [[cartesian theory]], left [[exact functor]]s  $\mathcal{C}_{\mathbb{T}} \to \mathcal{E}$ are equivalent to [[geometric morphism]]s $\mathcal{E} \to Sh(\mathcal{C}_{\mathbb{T}})$

  $$
    \mathbb{T}-Model(\mathcal{E})
     \simeq
    Func_\times(\mathcal{C}_{\mathbb{T}}, \mathcal{E})
     \simeq
    Topos(\mathcal{E}, Sh(\mathcal{C}_{\mathbb{T}}))
    \,.
  $$


* For $\mathbb{T}$ a [[regular theory]],  [[regular functor]]s $\mathcal{C}_{\mathbb{T}} \to \mathcal{E}$ are equivalent to [[geometric morphism]]s $\mathcal{E} \to Sh(\mathcal{C}_{\mathbb{T}})$

  $$
    \mathbb{T}-Model(\mathcal{E})
     \simeq
    RegFunc(\mathcal{C}_{\mathbb{T}}, \mathcal{E})
     \simeq
    Topos(\mathcal{E}, Sh(\mathcal{C}_{\mathbb{T}}))
    \,.
  $$

* For $\mathbb{T}$ a [[coherent theory]],  [[coherent functor]]s $\mathcal{C}_{\mathbb{T}} \to \mathcal{E}$ are equivalent to [[geometric morphism]]s $\mathcal{E} \to Sh(\mathcal{C}_{\mathbb{T}})$

  $$
    \mathbb{T}-Model(\mathcal{E})
     \simeq
    CohFunc(\mathcal{C}_{\mathbb{T}}, \mathcal{E})
     \simeq
    Topos(\mathcal{E}, Sh(\mathcal{C}_{\mathbb{T}}))
    \,.
  $$

* For $\mathbb{T}$ a [[geometric theory]],  [[geometric functor]]s $\mathcal{C}_{\mathbb{T}} \to \mathcal{E}$ are equivalent to [[geometric morphism]]s $\mathcal{E} \to Sh(\mathcal{C}_{\mathbb{T}})$

  $$
    \mathbb{T}-Model(\mathcal{E})
     \simeq
    GeomFunc(\mathcal{C}_{\mathbb{T}}, \mathcal{E})
     \simeq
    Topos(\mathcal{E}, Sh(\mathcal{C}_{\mathbb{T}}))
    \,.
  $$


In each case the [[equivalence of categories]] $Topos(\mathcal{E}, Sh(\mathcal{C}_{\mathbb{T}})) \stackrel{\simeq}{\to} \mathbb{T}-Model(\mathcal{E})$ is given by sending a [[geometric morphism]] $f : \mathcal{E} \to Sh(\mathcal{C}_{\mathbb{T}})$ to the precomposition of its [[inverse image]] $f^*$ with the [[Yoneda embedding]] $j$ and [[sheafification]] $L$:

$$
  f \;\; \mapsto \;\;
  ( \mathcal{C}_\mathbb{T} \stackrel{j}{\to} PSh(\mathcal{C}_{\mathbb{T}}) \stackrel{L}{\to} Sh(\mathcal{C}_{\mathbb{T}}) \stackrel{f^*}{\to} \mathcal{E} ) 
  \,.
$$

=--

This appears as ([Johnstone](#Johnstone)), theorem 3.1.1, 3.1.4, 3.1.9, 3.1.12.


+-- {: .un_defn}
###### Definition


For cartesian theories this is the statement of [[Diaconescu's theorem]].

The other cases follow from this by using <a href="http://nlab.mathforge.org/nlab/show/classifying+topos#GeometricMorphismsAndMorphismsOfSites">this discussion</a> at [[classifying topos]], which says that geometric morphism $\mathcal{E} \to Sh(\mathcal{C})$ are equivalent to [[site|morphisms of site]]s $\mathcal{C} \to \mathcal{E}$ (for the [[canonical coverage]] on $\mathcal{E}$). This means that in addition to preserving finite limits, as in [[Diaconescu's theorem]], these functors also send [[cover]]s in $\mathcal{C}$ to [[epimorphism]]s in $\mathcal{E}$. 

In the cases at hand this last condition means precisely that $\mathcal{C}_{\mathbb{T}} \to \mathcal{E}$ is a [[regular functor]] or [[coherent functor]] etc., respectively. 

=--


## References

Section D3.1 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

[[!redirects syntactic sites]]
