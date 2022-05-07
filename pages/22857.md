
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *simplicial mapping complex* or *simplicial hom complex* of two [[simplicial set]] is the collection of [[maps]], [[left homotopies]] and [[higher homotopies]] between them, all itself organized into a simplicial set.

More formally, [[SimplicialSets]] is a [[Cartesian monoidal category]] and the corresponding [[internal hom]] is what is traditionally known as the simplicial mapping complex.

## Definition

Since [[SimplicialSets]] is the [[category of presheaves]] over the [[simplex category]], its [[internal hom]] has the general form discussed at *[[closed monoidal structure on presheaves]]*:

\begin{definition}
For $X, Y \,\in\, sSet$, their [[internal hom]] or *simplicial mapping complex* is the simplicial set

$$
  [X,Y]_\bullet
  \;=\;
  Hom_{sSet}
  \big(
    X \times \Delta[\bullet],
    \,
    Y
  \big)
  \;\;\;
  \in
  sSet
  \,.
$$

whose 

* component set in degree $k$ is the [[hom-set]] of simplicial sets 

  * from the [[product of simplicial sets]] of $X$ with the standard [[n-simplex]] $\Delta[n]$ 

  * to $Y$, 

* and whose face maps $d_i$ and degeneracy maps $s_i$ are given by precomposition with $id_X \times \delta_i$ and $id_X \times \sigma_i$, respectively ($\delta_i$ and $\sigma_i$ denoting the generating morphisms of the [[simplex category]]).

\end{definition}

## Examples

\begin{example}\label{MappingComplexBetweenNervesOfGroupoids}
**([[simplicial mapping complex]] between [[nerves]] of [[groupoids]])**
For $N(\mathcal{G}_i)$ the [[nerves]] of [[groupoids]], their simplicial mapping complex is [[isomorphism|isomorphic]] to the [[nerve]] of the [[functor groupoid]] from $\mathcal{G}_1$ to $\mathcal{G}_2$:

$$
  \big[
    N(\mathcal{G}_1),
    \,
    N(\mathcal{G}_2)
  \big]
  \;\;
  \simeq
  \;\;
  N
  \big(
    Func(\mathcal{G}_1, \, \mathcal{G}_2)
  \big)
  \;\;\;
  \in
  \;
  SimplicialSets
$$
\end{example}


## Related concepts

* [[mapping space]], [[mapping complex]]

* [[derived mapping space]]

[[!redirects simplicial mapping complexes]]

[[!redirects simplicial hom complex]]
[[!redirects simplicial hom complexes]]
[[!redirects simplicial hom-complex]]
[[!redirects simplicial hom-complexes]]



