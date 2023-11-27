
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $\mathfrak{g}$ a [[Lie algebra]], the [[underlying]] [[dual vector space]] $\mathfrak{g}^*$ canonically inherits the structure of a [[Poisson manifold]] whose Poisson [[Lie bracket]] reduces on [[linear functions]] $\mathfrak{g} \hookrightarrow C^\infty(\mathfrak{g}^*)$ to the original [[Lie bracket]] on $\mathfrak{g}$. This is the **Lie-Poisson structure** on $\mathfrak{g}^*$. 

More generally, for $\mathfrak{a}$ a [[Lie algebroid]] the fiberwise dual $\mathfrak{a}^*$ inherits such a Poisson manifold structure.

[[Poisson manifold]] structures of this form are also called _[[linear Poisson structures]]_.

## Definition

### Abstractly

First notice that for $f \in C^\infty(\mathfrak{g}^\ast)$ as smooth function on the dual of a Lie algebra, then its [[de Rham differential]] 1-form at some $\alpha \in \mathfrak{g}^\ast$, being a linear map

$$
  \mathbf{d} f|_{\alpha}
  \colon
  T_\alpha \mathfrak{g}^\ast
  =
  \mathfrak{g}^\ast
  \longrightarrow
  \mathbb{R}
$$

is canonically identified with a Lie algebra element itself.

With this understood, then for $f,g \in C^\infty(\mathfrak{g}^*)$ two [[smooth functions]] on $\mathfrak{g}^*$ their Poisson [[Lie bracket]] in the Lie-Poisson structure is defined by

$$
  \{f,g\} \;\colon\; \theta \mapsto -\theta ([\mathbf{d} f, \mathbf{d} g])
  \,.
$$

Notice that for $v\in \mathfrak{g}$ regarded as a linear function $\langle -,v\rangle$ on $\mathfrak{g}^\ast$, then under the above identification we have $\mathbf{d} \langle -,v\rangle = v$. This means that on linear functions the Lie-Poisson bracket is simply the original Lie bracket:

$$
  \left\{
    \langle -, v_1\rangle,
    \langle -, v_2\rangle,
  \right\}
  = 
  \langle - ,[v_1,v_2]\rangle
  \,.
$$

This Lie-Poisson structure may be thought of as the unique smooth extension of this bracket on linear functions to all smooth functions on $\mathfrak{g}^\ast$.

### In components
 {#DefinitionInComponents}

Let $\{x^a\}$ be a [[basis]] for the [[vector space]] underlying the given [[Lie algebra]] $\mathfrak{g}$. Write $\{C^{a b}{}_c\}$  for the components of the [[Lie bracket]] $[-,-]$ in this basis (the structure constants), given by

$$
  [x^a,x^b] = \underset{c}{\sum} C^{a b}{}_c x^c
  \,.
$$

Write $\{\partial_a\}$ for the dual basis of the [[dual vector space]] $\mathfrak{g}^\ast$, so that the pairing $\mathfrak{g}^\ast \otimes\mathfrak{g} \to \mathbb{R}$ is given by

$$
  \partial_a x^b = \delta_a^b = 
  \left\{
    \array{
      1 & if\; a=b
      \\
      0 & otherwise
    }
  \right.
$$

As the notation is meant to suggest, dually the $\{x^a\}$ may be regarded as basis for the linear functions on $\mathfrak{g}^\ast$ and the $\{\partial_a\}$ serve as a basis of [[vector fields]] on $\mathfrak{g}^\ast$.

With this identification understood, the [[multivector fields]] on $\mathfrak{g}^\ast$ are spanned by elements of the form

$$
  v^{a_1 \cdots a_q} \partial_{a_1}\wedge \cdots \wedge \partial_{a_q}
$$

(with the sum over indices understood) for $\{v^{a_1 \cdots a_q}\}$ smooth functions on $\mathfrak{g}^\ast$. 

The [[Poisson tensor]] $\pi \in \wedge^2 \Gamma(T\mathfrak{g}^\ast)$ of the Lie-Poisson structure is given by

$$
  \pi = \tfrac{1}{2}\underset{a,b,c}{\sum} C^{a b}{}_c x^c \partial_a \wedge \partial_b
  \,.
$$

The [[Schouten bracket]] on multivector fields is given on linear basis elements by

$$
  \{x^a, x^b\}_{Sch} = 0
$$

$$
  \{\partial_a, x^b\}_{Sch} = \delta_a^b
$$

$$
  \{\partial_a, \partial_b\}_{Sch} = 0
$$

(the [[canonical commutation relations]]) and extended as a graded [[derivation]] in both arguments.


## Properties

### Deformation quantization by universal enveloping algebra

See at _[[deformation quantization]]_ the section _[Relation to universal enveloping algebras](deformation+quantization#RelationToUniversalEnvelopingAlgebras)_.

### Symplectic groupoid

The [[symplectic groupoid]] [[Lie integration|integrating]] the Lie-Poisson structure on $\mathfrak{g}^*$ is the [[action groupoid]] $\mathfrak{g}^* \sslash G$ of the [[coadjoint action]]. For more see at _[[symplectic groupoid]]_ in the section _[Examples -- Of Lie-Poisson stucture](symplectic+groupoid#OfLiePoissonStructure)_.

### Symplectic leaves

The [[symplectic leaves]] of the Lie-Poisson structure on $\mathfrak{g}^*$ are the [[coadjoint orbits]].

### Poisson-Lie algebroid cohomology
 {#PoissonLieAlgebroidCohomology}

We consider the [[Poisson Lie algebroid]] $\mathfrak{P}(\mathfrak{g}^\ast)$ of a Lie-Poisson structure and the [[Lie algebroid cohomology]].

+-- {: .num_remark}
###### Remark

By the discussion at _[[Poisson Lie algebroid]]_, the graded algebra of [[multivector fields]] equipped with the [[differential]] given by the [[Schouten bracket]] with the [[Poisson bivector]]

$$
  d_{CE} = \{\pi, -\}_{Sch}
$$

is the [[Chevalley-Eilenberg algebra]] of this Lie algebroid:

$$
  CE(\mathfrak{P}(\mathfrak{g}^\ast))
  = 
  \left(
    \wedge^\bullet \Gamma(T\mathfrak{g}^\ast),
    d_{CE} = \{\pi, -\}_{Sch}
  \right)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

As for every [[Poisson Lie algebroid]], the [[Poisson bivector]] 
$\pi \in CE(\mathfrak{P}(\mathfrak{g}^\ast))$ is a [[Lie algebroid cocycle]] of degree 2

$$
  d_{CE}\pi = \{\pi,\pi\}_{Sch} = 0
$$

(see also at _[[symplectic Lie n-algebroid]]_).

In view of the fact that here $\pi$ is just another incarnation of the [[Lie bracket]], this condition here is an incarnation of the [[Jacobi identity]] on the Lie algebra $(\mathfrak{g},[-,-])$.

=--

But in the simple case of Lie-Poisson structure, this cocycle is in fact exact:

+-- {: .num_prop #PoissonTensorCoboundary}
###### Proposition

For the Poisson-Lie structure on $\mathfrak{g}^\ast$ the [[Poisson tensor]] $\pi \in CE^2(\mathfrak{P}(\mathfrak{g}))$ has a [[coboundary]] and hence is trivial in [[Lie algebroid cohomology]].

=--

+-- {: .proof}
###### Proof

Consider the component-description from [above](#DefinitionInComponents).
We show that $x^a \partial_a$ is a coboundary.

First notice that 

$$
  \{x^b, x^a \partial_a \}_{Sch} = -x^b
$$ 

and

$$
  \{\partial_b, x^a \partial_a \}_{Sch} = \partial_b
  \,.
$$

From this we get

$$
  \begin{aligned}
    d_{CE} (x^a \partial_a)
    &= 
   \left\{\pi,\;  x^a \partial_a\right\}_{Sch}
    \\
    & = 
    \left\{\frac{1}{2} C^{a b}{}_c x^c \partial_a \wedge \partial_b,\;    
    x^a \partial_a\right\}_{Sch}    
    \\
    & = (2-1) \frac{1}{2} C^{a b}{}_c x^c \partial_a \wedge \partial_b
    \\
    & = 
    \pi
  \end{aligned}
$$

=--

### Poisson Lie group structure

Under addition a Lie-Poisson manifold becomes a _[[Poisson Lie group]]_, see there for more.

## Related concepts

* a _[[moment map]]_ is often expresses as a Poisson homomorphism into a Lie-Poisson structure.

## References

The notion of Lie-Poisson structures was originally found by [[Sophus Lie]] and then rediscovered by [[Felix Berezin]] and by [[Alexander Kirillov]], [[Bertram Kostant]] and [[Jean-Marie Souriau]]. 

General accounts include

*  Izu Vaisman, section 3.1 of _Lectures on the Geometry of Poisson Manifolds_, Birkh&#228;user 1994

* [[Camille Laurent-Gengoux]], _Linear Poisson Structures and Lie Algebras_, chapter 7 pp 179-203 of Camille Laurent-Gengoux, Anne Pichereau, Pol Vanhaecke (eds.) _Poisson Structures_, Grundlehren der mathematischen Wissenschaften book series (GL, volume 347) ([web](https://link.springer.com/chapter/10.1007/978-3-642-31090-4_7))


Review of the [[formal deformation quantization]] of Lie-Poisson structures via transfer of the product on the [[universal enveloping algebra]] of the given Lie algebra is  for instance in 

* {#Gutt11} Simone Gutt, section 2.2. of _Deformation quantization of Poisson manifolds_, Geometry and Topology Monographs 17 (2011) 171-220 ([pdf](http://msp.org/gtm/2011/17/gtm-2011-17-003p.pdf))

and generalization to more general polynomial Poisson algebras is discussed in

* Michael Penkava, Pol Vanhaecke, _Deformation Quantization of Polynomial Poisson Algebras_, Journal of Algebra
227, 365&#241;393 (2000) ([arXiv:math/9804022](https://arxiv.org/abs/math/9804022))

The [[strict deformation quantization]] of Lie-Poisson structures was considered in 

* {#Rieffel90} [[Marc Rieffel]], _Lie group convolution algebras as deformation quantization of linear Poisson structures_, American Journal of Mathematics **112** 4 (1990) 657-685 &lbrack;[jstor:2374874]( http://www.jstor.org/stable/2374874)&rbrack;
 

The [[symplectic Lie groupoid]] [[Lie integration|Lie integrating]] Lie-Poisson structures is discussed as example 4.3 in:

* {#BursztynCrainic} [[Henrique Bursztyn]], [[Marius Crainic]], _Dirac structures, momentum maps and quasi-Poisson manifolds_ ([pdf](http://www.preprint.impa.br/FullText/Bursztyn__Fri_Dec_23_11_24_19_BRDT_2005.html/alanfestimpa.pdf))

 
See also

* [[Victor Ginzburg]], [[Alan Weinstein]], _Lie-Poisson structure on some Poisson Lie groups_, Journal of the AMS, volume 5, number 2 (1992) ([pdf](http://www.ams.org/journals/jams/1992-05-02/S0894-0347-1992-1126117-8/S0894-0347-1992-1126117-8.pdf))



[[!redirects Lie-Poisson structures]]