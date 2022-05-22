
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of [[persistent homology]], the _well group_ ([EMP 11](#EMP11)) of a [[continuous function]] $f$ into a [[metric space]] is a [[homology|homological]] measure of how robust the [[level sets]] of $f$ are against [[deformations]] of $f$. Concretely, the Well group at [[radius]] $r$ of a given point in the [[codomain]] consists of all those [[ordinary homology|homology]]-classes of the domain which are reflected in the [[level sets]] of _every_ [[continuous function]] whose values differ from those of $f$ at most by $r$.

As the level varies, the collection of well groups form a [[zigzag persistence module]], also called a *well module* ([EMP 11, Sec. 3](#EMP11)).

## Definition

Given a [[continuous function]] $f$ to a [[Euclidean space]] and a choice of [[topological subspace]] $A$ of the latter 

$$
  \array{
    f^{-1}(A) &\subset & X
    \\
    \downarrow && \big\downarrow {}^{\mathrlap{f}}
    \\
    A &\subset& \mathbb{R}^n
  } 
$$

the _well groups_ at [[radius]] $r \in (0,\infty)$ are the [[intersections]] of the [[ordinary homology|ordinary]] [[homology groups]] of the [[pre-images]] $g^{-1}(A) \subset X$ for all [[continuous functions]] $X \overset{g}{\to} \mathbb{R}^n$ whose [[maximum|maximal]] [[distance]] from $f$ is $\left \vert g-f\right \vert \leq r$.

$$
  W_\bullet(f,r)
  \;\coloneqq\;
  \underset{
    {X \overset{g}{\to} \mathbb{R}^n}
    \atop
    {\left \vert g-f\right \vert \leq r}
  }{\bigcap}
  image
  \Big(
    H_\bullet\big(
      g^{-1}(A) 
    \big)
    \overset{
      H_\bullet\big(  g^{-1}(A) \subset X \big)
    }{\longrightarrow}
    H_\bullet
    \big(
      X
    \big)
  \Big)
$$

(e.g. [Franek-Krčál 16, p. 2](#FranekKrcal16))

## Related concepts

* [[persistence module]]

* [[zigzag persistence]]

* [[stability of persistence diagrams]]


## References

The concept of [[well groups]] was introduced in

* {#EMP11} [[Herbert Edelsbrunner]], [[Dmitriy Morozov]], [[Amit Patel]], *Quantifying Transversality by Measuring the Robustness of Intersections*, Foundations of Computational Mathematics, **11** 3  (2011) 345–361 $[$[arXiv:0911.2142](https://arxiv.org/abs/0911.2142)$]$

* [[Paul Bendich]], [[Herbert Edelsbrunner]], [[Dmitriy Morozov]], [[Amit Patel]], *The Robustness of Level Sets*, In: M. de Berg, U. Meyer (eds.) _Algorithms – ESA 2010_. ESA 2010. Lecture Notes in Computer Science **6346** Springer (2010)  $[$[doi:10.1007/978-3-642-15775-2_1](https://doi.org/10.1007/978-3-642-15775-2_1)$]$ 

* [[Paul Bendich]], [[Herbert Edelsbrunner]], [[Dmitriy Morozov]], [[Amit Patel]], *Homology and Robustness of Level and Interlevel Sets*, Homology, Homotopy and Applications, **15** (2013) 51-72 $[$[euclid:1383943667](https://projecteuclid.org/euclid.hha/1383943667)$]$

Review in:

* [[Sara Kališnik]], Section 4.2.2 of: _Persistent homology and duality_ (2013) ([pdf](http://www.matknjiz.si/doktorati/2013/Kalisnik-14521-4.pdf), [[KalisnikPersistent.pdf:file]])

Review, computational analysis and discussion of ([[persistent Cohomotopy|persistent]]) [[Cohomotopy]] as an improvement over homology well groups: 

* {#FranekKrcal16} [[Peter Franek]], [[Marek Krčál]], _On Computability and Triviality of Well Groups_, Discrete Comput Geom (2016) 56: 126 ([arXiv:1501.03641](https://arxiv.org/abs/1501.03641), [doi:10.1007/s00454-016-9794-2](https://doi.org/10.1007/s00454-016-9794-2))

* [[Peter Franek]], [[Marek Krčál]], _Persistence of Zero Sets_, Homology, Homotopy and Applications, Volume 19 (2017) Number 2 ([arXiv:1507.04310](https://arxiv.org/abs/1507.04310), [doi:10.4310/HHA.2017.v19.n2.a16](http://dx.doi.org/10.4310/HHA.2017.v19.n2.a16))


* [[Peter Franek]], [[Marek Krčál]], _Cohomotopy groups capture robust Properties of Zero Sets via Homotopy Theory_, talk at [ACAT meeting 2015](https://www2.ist.ac.at/acat) ([pfd slides](https://www2.ist.ac.at/fileadmin/user_upload/events_pages/acat/ACAT2015_Marek_Krcal.pdf))

* [[Peter Franek]], [[Marek Krčál]], [[Hubert Wagner]], _Solving equations and optimization problems with uncertainty_, J Appl. and Comput. Topology (2018) 1: 297 ([arxiv:1607.06344](https://arxiv.org/abs/1607.06344), [doi:10.1007/s41468-017-0009-6](https://doi.org/10.1007/s41468-017-0009-6))


[[!redirects well groups]]

[[!redirects well module]]
[[!redirects well modules]]
