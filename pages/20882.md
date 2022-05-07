
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _[[Lie algebra]]_ may be formulated [[internalization|internal to]] general [[linear category|linear]] [[monoidal categories]] ([[tensor categories]]). This general definition of _Lie algebra objects internal to tensor categories_ subsumes variants of Lie algebras such as [[super Lie algebras]]. 

## Definition

### As internal Lie algebras
 {#AsInternalLieAlgebras}

Consider a [[commutative unital ring]] $k$, and a (strict for simplicity) [[symmetric monoidal category|symmetric monoidal]] $k$-[[linear category]] $(\mathcal{C},\otimes,1)$ with [[braiding]] $\tau$.

A **[[Lie algebra object]]** in $(\mathcal{C},\otimes,1,\tau)$ is 

1. an [[object]] 

   $$
     L \in \mathcal{C}
   $$

1. [[morphism]] (the [[Lie bracket]])

   $$
     [-,-] \;\colon\; L \otimes L \to L
   $$

such that the following conditions hold:

1. [[Jacobi identity]]:

   $$
     \left[-,\left[-,-\right]\right]
       +
     \left[-,\left[-,-\right]\right]
     \circ(id_L\otimes\tau_{L,L})
     \circ(\tau\otimes id_L)
     +
     \left[-,\left[-,-\right]\right]
       \circ 
     (\tau_{L,L}\otimes id_L)\circ (id_L\otimes\tau_{L,L}) = 0
   $$ 

1. skew-symmetry:

   $$
     \begin{aligned}
       & 
       \phantom{+}
       [-,-]
       \\
       &
       +
       [-,-]\circ \tau_{L,L} 
       \\
       & = \phantom{+} 0
     \end{aligned}
   $$

Equivalently, in [[string diagram]]-notation in the ambient [[tensor category]], the [[Lie action property]] looks as follows:

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

where the last line shows the equivalence to the [[Jacobi identity]] on the [[Lie algebra object]] itself in the case that the Lie action is the [[adjoint action]].

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

In the language of [[Jacobi diagrams]] this is called the _[[STU-relation]]_.
and is the reason behind the existence of [[Lie algebra weight systems]] in [[knot theory]]. For more see also at _[[metric Lie representation]]_.


### As algebras over the Lie operad

Equivalently, Lie algebra objects  are the [[algebras over an operad]] over a certain quadratic [[operad]], called the [[Lie operad]], which is the [[Koszul dual]] of the [[commutative algebra operad]].



## Examples
 {#Examples}

Examples of types of [[Lie algebra objects]]:

* If $k$ is the ring $\mathbb{Z}$ of [[integers]] and $\mathcal{C} = $ $k$[[Mod]] = [[Ab]] is the [[category]] of [[abelian groups]] equipped with the [[tensor product of abelian groups]], then a Lie algebra object is called a _[[Lie ring]]_.

* If $k$ is a [[field]] and $\mathcal{C} =$ [[Vect]] is the [[category]] of [[vector spaces]] over $k$ equipped with the [[tensor product of vector spaces]] then a Lie algebra object is an ordinary _[[Lie algebra|Lie k-algebra]]_. 

* If $k$ is a [[field]] and $\mathcal{C}$ = [[sVect]] is the [[category]] of [[super vector spaces]] over $k$, then a Lie algebra object is a  _[[super Lie algebra]]_.

* A [[Leibniz algebra]] is an internal Lie algebra in the [[Loday-Pirashvili category]] ([Loday-Pirashvili 98](#LodayPirashvili98))

* [[Rozansky-Witten weight systems]] are [[Lie algebra weight systems]] for [[Lie algebra objects]] in the [[derived category of quasi-coherent sheaves]] ([Roberts-Willerton 10](#RobertsWillerton10))

## Related concepts

* [[super Lie algebra]]

* [[Lie algebra weight system]]

## References

### General

(...)

### Examples
 {#ReferencesExamples}

On [[Leibniz algebras]] as Lie algebra objects in suitable [[tensor categories]] of [[linear maps]]:

* {#LodayPirashvili98} [[Jean-Louis Loday]], [[Teimuraz Pirashvili]], _The tensor category of linear maps and Leibniz algebras_, Georg. Math. J. vol. 5, n.3 (1998) 263--276 ([doi:10.1023/B:GEOR.0000008125.26487.f3](https://doi.org/10.1023/B:GEOR.0000008125.26487.f3))

On [[Rozansky-Witten weight systems]] as [[Lie algebra weight systems]] for [[Lie algebra objects]] in the [[derived category of quasi-coherent sheaves]], and unified [[Wheels theorem]]:

* {#RobertsWillerton10} [[Justin Roberts]], [[Simon Willerton]], _On the Rozansky-Witten weight systems_, Algebr. Geom. Topol. 10 (2010) 1455-1519 ([arXiv:math/0602653](https://arxiv.org/abs/math/0602653))




[[!redirects Lie algebra objects]]

[[!redirects internal Lie algebra]]
[[!redirects internal Lie algebras]]

[[!redirects Lie ring]]
[[!redirects Lie rings]]

