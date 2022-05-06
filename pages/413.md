
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of superdifferential form is the generalization of the notion of [[differential form]] from [[manifolds]] to [[supermanifolds]].


## Definition
 {#Definition}


+-- {: .num_defn #DifferentialFormsOnSuperCartesianSpace}
###### Definition
**([[differential forms]] on [[super Cartesian space]])**

For $n,q \in \mathbb{N}$, the _de Rham algebra_ $\Omega^\bullet(\mathbb{R}^{n\vert q})$ of super-differential forms on 
the [[super Cartesian space]] $\mathbb{R}^{n\vert q}$ is the [[free construction|free]] [[differential graded-commutative superalgebra]] over the [[supercommutative algebra]] 

$$
  C^\infty(\mathbb{R}^{n\vert q})
  \;=\;
  \underset{
    even
  }{
  \underbrace{
    C^\infty(\mathbb{R}^n)
  }} \otimes_{\mathbb{R}} 
  \underset{
    odd
  }{
  \underbrace{
    \wedge^\bullet \mathbb{R}^q 
  }}
$$

on 

1. $n$ [[generators and relations|generators]] $\mathbf{d} x^a$ in [bi-degree](chain+complex+in+super+vector+spaces#ChainComplexesOfSuperVectorSpaces) $(1,even)$ (the canonical bosonic 1-forms) 

1. $q$ generators $\mathbf{d} \theta^\alpha$ in [bi-degree](chain+complex+in+super+vector+spaces#ChainComplexesOfSuperVectorSpaces) $(1,odd)$

hence:

\[
  \label{SuperCartSpDiffForms}
  \Omega^\bullet( \mathbb{R}^{n\vert q} )
  \;\coloneqq\;
  C^\infty(\mathbb{R}^{n\vert q})
  \left[
    \underset{deg = (1,even)}{\underbrace{
    \left\langle 
      \mathbf{d} x^a 
    \right\rangle_{a = 1}^{n}
    }},\;\;\;\;\;
    \underset{
      deg = (1,odd)
    }{
    \underbrace{
    \left\langle
      \mathbf{d} \theta^\alpha
    \right\rangle_{\alpha = 1}^q
    }}
  \right]
\]

with [[nLab:differential]] having the evident definition on generators, and extended from there as a [[derivation]] of bi-degree $(1, even) \in \mathbb{Z} \times (\mathbb{Z}/2)$

=--

+-- {: .num_example #SignRulesForDifferentialFormsOnSuperCartesianSpaces}
###### Example
**([[signs in supergeometry|sign rule]] for [[differential forms]] on [[super Cartesian spaces]])**

For $n,q \in \mathbb{N}$, the generators of the [[differential graded-commutative superalgebra]] $\Omega^\bullet(\mathbb{R}^{n\vert q})$ of differential forms on the [[super Cartesian space]] (Def. \ref{DifferentialFormsOnSuperCartesianSpace}) have the following [bi-degree](chain+complex+in+super+vector+spaces#ChainComplexesOfSuperVectorSpaces)

| $\phantom{A}$generator$\phantom{A}$ | $\phantom{A}$[bi-degree](chain+complex+in+super+vector+spaces#ChainComplexesOfSuperVectorSpaces)$\phantom{A}$ |
|--|--|
| $\phantom{A}$$x^a$$\phantom{A}$ | $\phantom{A}$(0,even)$\phantom{A}$ |
| $\phantom{A}$$\theta^\alpha$$\phantom{A}$ | $\phantom{A}$(0,odd)$\phantom{A}$ |
| $\phantom{A}$$\mathbf{d}x^a$$\phantom{A}$ | $\phantom{A}$(1,even)$\phantom{A}$ |
| $\phantom{A}$$\mathbf{d}\theta^\alpha$$\phantom{A}$ | $\phantom{A}$(1,odd)$\phantom{A}$ |
{: style='margin:auto}

and satisfy the following graded-commutation relations, depending on one of the two equivalent (see [here](chain+complex+in+super+vector+spaces#EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect)) [[signs in supergeometry|sign rules]]:

| $\phantom{A}$[[signs in supergeometry|sign rule]]$\phantom{A}$  | $\phantom{A}$[Deligne's](signs+in+supergeometry#TheSignRuleFromInternalization)$\phantom{A}$ | [Bernstein's](signs+in+supergeometry#SuperOddConvention)$\phantom{A}$ | 
|---|------------------|-------------------|
| $\phantom{A}$$x^{a} \; x^{b} =$ | $\phantom{A}$$+ x^{b} \; x^{a}$$\phantom{A}$ | $\phantom{A}$$+ x^{b} \; x^{a}$$\phantom{A}$ | 
| $\phantom{A}$$x^a \;\theta^\alpha =$$\phantom{A}$ | $\phantom{A}$$+ \theta^\alpha \; x^a$$\phantom{A}$ | $\phantom{A}$$+ \theta^\alpha \; x^a$$\phantom{A}$ | 
| $\phantom{A}$$\theta^{\alpha} \; \theta^{\beta} =$$\phantom{A}$ | $\phantom{A}$$- \theta^{\beta} \; \theta^{\alpha}$$\phantom{A}$ | $\phantom{A}$$ - \theta^{\beta} \; \theta^{\alpha}$$\phantom{A}$ | 
| $\phantom{A}$$x^{a} (\mathbf{d}x^{a}) =$$\phantom{A}$ | $\phantom{A}$$+ (\mathbf{d}x^{b}) x^{a}$$\phantom{A}$ | $\phantom{A}$$+ (\mathbf{d}x^{b}) x^{a}$$\phantom{A}$ |
| $\phantom{A}$$\theta^\alpha (\mathbf{d}x^a) =$$\phantom{A}$ | $\phantom{A}$$+ (\mathbf{d}x^a) \theta^\alpha$$\phantom{A}$ | $\phantom{A}$${\color{blue}{-}} (\mathbf{d}x^a) \theta^\alpha$$\phantom{A}$ | 
| $\phantom{A}$$\theta^{\alpha} (\mathbf{d}\theta^{\beta})  = $$\phantom{A}$ | $\phantom{A}$$- (\mathbf{d}\theta^{\beta}) \theta^{\alpha}$$\phantom{A}$ | $\phantom{A}$${\color{blue}{+}} (\mathbf{d}\theta^{\beta}) \theta^{\alpha}$$\phantom{A}$ | 
| $\phantom{A}$$ (\mathbf{d}x^{a}) (\mathbf{d} x^{b}) =$$\phantom{A}$ |  $\phantom{A}$$- (\mathbf{d} x^{b}) (\mathbf{d} x^{a})$$\phantom{A}$ | $\phantom{A}$$ - (\mathbf{d} x^{b}) (\mathbf{d} x^{a})$$\phantom{A}$ |
| $\phantom{A}$$ (\mathbf{d}x^a) (\mathbf{d} \theta^{\alpha}) =$$\phantom{A}$ | $\phantom{A}$$ - (\mathbf{d}\theta^{\alpha}) (\mathbf{d} x^a) $$\phantom{A}$ | $\phantom{A}$$ {\color{blue}{+}} (\mathbf{d}\theta^{\alpha}) (\mathbf{d} x^a) $$\phantom{A}$ |
| $\phantom{A}$$(\mathbf{d}\theta^{\alpha}) (\mathbf{d} \theta^{\beta}) =$ | $\phantom{A}$$ + (\mathbf{d}\theta^{\beta}) (\mathbf{d} \theta^{\alpha})$$\phantom{A}$ | $\phantom{A}$$ + (\mathbf{d}\theta^{\beta}) (\mathbf{d} \theta^{\alpha})$$\phantom{A}$ |
{: style='margin:auto}

=--

+-- {: .num_defn #SuperCartSpaPullbackOfSuperDifferentialForms}
###### Definition
**([[pullback of differential forms|pullback]] over [[super Cartesian spaces]])**

Let 

$$
  \array{
    \mathbb{R}^{n_1 \vert q_1}
    &\overset{f}{\longrightarrow}&
    \mathbb{R}^{n_2 \vert q_2}
    \\
    C^\infty(\mathbb{R}^{n_1\vert q_1})
    &\overset{f^\ast}{\longleftarrow}&
    C^\infty(\mathbb{R}^{n_2\vert q_2})
  }
$$

be a morphism of [[super Cartesian spaces]], hence [[formal duality|formally dually]] a [[algebra homomorphism]] $f^\ast$ of [[supercommutative superalgebras]].

By the fact that $\Omega^\bullet(\mathbb{R}^{n \vert q})$ (Def. \ref{DifferentialFormsOnSuperCartesianSpace}) is [[free construction|free]] over $C^\infty(\mathbb{R}^{n\vert q})$ on generators $\mathbf{d}x^a$, $\mathbf{d}\theta^\alpha$ (eq:SuperCartSpDiffForms) this extends to a unique homomorphism on the de Rham [[dgc-superalgebra]]

$$
  \Omega^\bullet(\mathbb{R}^{n_1\vert q_1})
    \overset{f^\ast}{\longleftarrow}
  \Omega^\bullet(\mathbb{R}^{n_2\vert q_2})
$$

subject to the condition that $f^\ast \circ \mathbf{d}_2 = \mathbf{d}_1 \circ f^\ast$:


$$
  \array{
    \Omega^\bullet(\mathbb{R}^{n_1\vert q_1})
    &\overset{\phantom{AA}f^\ast\phantom{AA}}{\longleftarrow}&
    \Omega^\bullet(\mathbb{R}^{n_2\vert q_2})
    \\
    {}^{\mathbf{d}_1}\Big\downarrow
    &&
    \Big\downarrow{}^{\mathbf{d}_2}
    \\
    \Omega^\bullet(\mathbb{R}^{n_1\vert q_1})
    &\overset{\phantom{AA}f^\ast\phantom{AA}}{\longleftarrow}&
    \Omega^\bullet(\mathbb{R}^{n_2\vert q_2})
  }
$$

This operation is called _[[pullback of differential forms]]_ along maps of [[super Cartesian spaces]].

=--

+-- {: .num_prop #SuperDifferentialFormClassifying}
###### Proposition
**(classifing [[super formal smooth set]] of [[super differential forms]])**

The operation of [[pullback of differential forms]] (Def. \ref{SuperCartSpaPullbackOfSuperDifferentialForms}) over [[super Cartesian spaces]] respects [[identity morphisms]] and [[composition]]. Hence the assignment of [[differential forms]] on [[super Cartesian spaces]] (Def. \ref{DifferentialFormsOnSuperCartesianSpace}) is a [[presheaf]] on [[SuperCartSp]]:

$$
  \mathbf{\Omega}\bullet
  \;\colon\;
  SuperCartSp^{op}
    \longrightarrow
  dgcsAlg
$$

with values in [[differential graded-commutative superalgebras]], in fact a [[sheaf]] and hence a [[differential graded algebra]] [[internalization|internal]] to the [[sheaf topos]] over [[SuperCartSp]]:

$$
  \mathbf{\Omega}^n
  \;\in\;
  Sh(SuperCartSp)
  \,.
$$

The construction generalizes in an evident way also to sheaves over [[super formal Cartesian spaces]], hence to [[super formal smooth sets]]:

$$
  \mathbf{\Omega}^n
  \;\in\;
  SuperFormalSmoothSet \;\coloneqq\; Sh(SuperFormalCartSp)
  \,.
$$


=--

We may now proceed as in the discussion of [[differential forms]] on [[smooth sets]] ([here](geometry+of+physics+--+smooth sets#DifferentialForms)):

+-- {: .num_defn #SuperDifferentialFormsOnGeneralSuperFormalSmoothSets}
###### Definition
**([[super differential forms]] on general [[super formal smooth sets]])**

Let $X$ be a [[supermanifold]] or more generally a [[super formal smooth set]]

$$
  X \;\in\; SuperFormalSmoothSet
$$

Then _[[super differential forms]]_ on $X$ are morphisms 

$$
  X \longrightarrow \mathbf{\Omega}^\bullet
$$

into the classifying sheaf $\mathbf{\Omega}^\bullet$ from Def. \ref{SuperDifferentialFormClassifying}.


=--



## Properties

### Integral top-forms and Picture number

If a choice of _integral top-forms_ is made, needed for a notion of _[[integration over supermanifolds]]_, then there is an additional grading by "[[picture number]]" ([Belopolsky 97b](#Belopolsky97b), [Witten 12](#Witten12)), see ([Catenacci-Grassi-Noja 18 (5.8) to (5.12)](#CatenacciGrassiNoja18)).


## Examples {#Examples}

Let $\mathbf{X} = \mathbb{R}^{1|1}$. The [[superalgebra]] of functions on $\mathbf{X}$ is the [[exterior algebra]] that is generated over $C^\infty(\mathbf{R})$ from a single generator $\theta$ in odd degree (the canonical odd coordinate). 

The algebra of superdifferential forms on $\mathbb{R}^{1|1}$ is the [[exterior algebra]] generated over $C^\infty(\mathbb{R})$ from 

* a generator $\theta$ in odd degree (the canonical odd coordinate);

* a generator $d x$ in odd degree (the differential of the canonical even coordinate);

* a generator $d \theta$ in even degree (the differential of the canonical odd coordinate).

Notice in particular that while $ d x \wedge d x = 0$
the wedge product $d \theta \wedge d\theta$ is non-vanishing, since $d \theta$ is in even degree. In fact all higher wedge powers of $d \theta$ with itself exist.


## Remarks

* Being a $\mathbb{Z}_2$-graded locally free algebra itself, one can regard $\Omega^\bullet(X)$ itself (even for $X$ a usual manifold!) as the "algebra of functions" (more precisely [[inner hom]], i.e. mapping space into the line) on another supermanifold. That supermanifold is called $T[1] X$, the **[[shifted tangent bundle]]** of $X$. By definition we have $C^\infty(T[1]X) = \Omega^\bullet(X)$. From this point of view, the existence of the differential $d$ on the graded algebra $\Omega^\bullet(X)$ translates into the existence of a special odd vector field on $T[1]X$. This is a **homological vector field** in that it is odd and the super Lie bracket of it with itself vanishes: $[d,d] = 0$.

* In the context of [[L-infinity algebroids]], where one may regard $C^\infty(X)$ as the [[Chevalley-Eilenberg algebra]] of an $L_\infty$-[[Lie infinity-algebroid|algebroid]] it is useful to notice that $\Omega^\bullet(X)$ is the corresponding [[Weil algebra]]. If $X$ is a Lie $n$-algebroid then $T[1]X$ is a Lie $(n+1)$-algebroid.

## Related concepts

* [[signs in supergeometry]]

* [[picture changing operator]]

* [[super Lie algebroid]]

## References

Discussion in view of [[Lie algebra cohomology]] of [[super Lie algebras]]:

* [[Roberto Catenacci]], [[C. A. Cremonini]], [[Pietro Antonio Grassi]], [[Simone Noja]], _Cohomology of Lie Superalgebras: Forms, Integral Forms and Coset Superspaces_ ([arXiv:2012.05246](https://arxiv.org/abs/2012.05246))

Discussion with an eye towards [[quantization]] of the [[superstring]] is in 

* [[Alexander Belopolsky]], _De Rham Cohomology of the Supermanifolds and Superstring BRST Cohomology_, Phys.Lett. B403 (1997) 47-50 ([arXiv:hep-th/9609220](http://arxiv.org/abs/hep-th/9609220))

Geometric discussion of [[picture number]] appearing in the context of [[integration over supermanifolds]] (and originally seen in the [[quantization]] of the [[NSR superstring]], crucial in [[superstring field theory]]) is due to 

* {#Belopolsky97b} [[Alexander Belopolsky]], _Picture changing operators in supergeometry and superstring theory_ ([arXiv:hep-th/9706033](https://arxiv.org/abs/hep-th/9706033))

and further amplified in 


* {#Witten12} [[Edward Witten]], appendix D of _Notes On Super Riemann Surfaces And Their Moduli_ ([arXiv:1209.2459](http://arxiv.org/abs/1209.2459))

* {#CatenacciGrassiNoja18} [[Roberto Catenacci]], [[Pietro Antonio Grassi]], [[Simone Noja]], _Superstring Field Theory, Superforms and Supergeometry_ ([arXiv:1807.09563](https://arxiv.org/abs/1807.09563))


[[!redirects differential forms on a supermanifold]]

[[!redirects differential form on supermanifold]]
[[!redirects differential forms on supermanifolds]]

[[!redirects super differential form]]
[[!redirects super differential forms]]

[[!redirects superdifferential form]]
[[!redirects superdifferential forms]]


