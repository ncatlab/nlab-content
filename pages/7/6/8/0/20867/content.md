[[!redirects STU relations]]




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[knot theory]], by the _STU-relations_, one means the following [[relations]] in the [[linear span]] of [[Jacobi diagrams]]:


<center>
<img src="https://ncatlab.org/nlab/files/STU-relation.jpg" width="500">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


## Properties

### Relation to weight systems and Lie algebra objects
 {#RelationToLieAlgebraObjects}

By definition, the STU-relations are the relations respected by [[weight systems]] on [[Jacobi diagrams]].

When regarded as relations of [[string diagrams]], the STU relations characterize the [[Jacobi identity]] for [[Lie algebra objects]], or more generally the [[Lie action property]] of [[Lie modules]]: 

<center>
<img src="https://ncatlab.org/nlab/files/LieActionPropertyAsSTURelation.jpg" width="500">
</center>

$$
  \begin{aligned}
    \Leftrightarrow
    &
    \;\;\;\;\;
    \rho(f(x,y),z) \;=\; \rho(y,\rho(x,z)) - \rho(x,\rho(y,z))
    \\
    \underset{
      {f = [-,-]}
      \atop
      {Lie\;bracket}
    }{
      \Leftrightarrow
    }
    &
    \;\;\;\;\;
    \underset{
       {Lie\;action\;property}
    }{
    \underbrace{
      \rho([x,y],z) \;=\; \rho(y,\rho(x,z)) - \rho(x,\rho(y,z))
    }
    }
    \\
    \underset{
      {\rho = -[-,-]}
      \atop
      {adjoint\;action}
    }{
      \Leftrightarrow
    }
    &
    \;\;\;\;\;
    \underset{
       {Jacobi\;identity}
    }{
    \underbrace{
      [[x,y],z] \;=\; - [y,[x,z]] + [x,[y,z]]
    }
    }
  \end{aligned}
$$


This is the reason behind the existence of [[Lie algebra weight systems]].




### Relation to 4T-relations
 {#RelationTo4TRelations}

Under the embedding of the set of [[round chord diagrams]] into the set of [[Jacobi diagrams]], the [[STU-relations]] imply the [[4T relations]] on [[round chord diagrams]]:

<center>
<img src="https://ncatlab.org/nlab/files/STURelationImplies4TRelation.jpg" width="300">
</center>


Using this, one finds that [[chord diagrams modulo 4T are Jacobi diagrams modulo STU]]:

<center>
<img src="https://ncatlab.org/nlab/files/ChordDiagModulo4TAreJAcobiDiagModuloSTU.jpg" width="840">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

### Relation to knot-graph complex

That the STU-relations characterize the [[cochain cohomology]] of the [[knot-graph complex]] in the respective degrees is shown in [Koytcheff-Munson-Volic 13, Section 3.4](#KoytcheffMunsonVolic13)


<center>
<img src="https://ncatlab.org/nlab/files/VolicSTURelation.jpg" width="520">
</center>

> graphics grabbed from [Koytcheff-Munson-Volic 13](#KoytcheffMunsonVolic13)


## Related concepts

* [[weight system]]

* [[4T relation]]

* [[Vassiliev invariant]]


## References

### General

Original articles:

* {#BarNatan95} [[Dror Bar-Natan]], Def. 1.9 in: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

Textbook accounts:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 4 of:  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv/1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* [[David Jackson]], [[Iain Moffat]], Section 11 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

Lecture notes:

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], [[Alexander Stoimenow]]: _The Fundamental Theorem of Vassiliev Invariants_, in: *Geometry and Physics*, Lecture Notes in Pure and Applied Mathematics **184** Marcel Dekker Inc. (1996) &lbrack;[arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009), [ISBN:0-8247-9791-4](https://users-math.au.dk/swann/Aarhus-proceedings-1995/index.html)&rbrack;


### In terms of the knot-graph complex

In terms of the [[knot-graph complex]]:

* {#KoytcheffMunsonVolic13} Robin Koytcheff, Brian A. Munson, [[Ismar Volić]], Section 3.4 of: _Configuration space integrals and the cohomology of the space of homotopy string links_, J. Knot Theory Ramif. 22, no. 11, 73 pp. (2013) ([arXiv:1109.0056](https://arxiv.org/abs/1109.0056))

[[!redirects STU relation]]
[[!redirects STU relations]]
[[!redirects STU-relation]]
[[!redirects STU-relations]]
