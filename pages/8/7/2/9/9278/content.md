
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

For $\mathfrak{g}$ a [[Lie algebra]] the underlying [[dual vector space]] $\mathfrak{g}^*$ canonically inherits the structure of a [[Poisson manifold]] whose Poisson [[Lie bracket]] reduces on linear functions $\mathfrak{g} \hookrightarrow C^\infty(\mathfrak{g}^*)$ to the original Lie bracket on $\mathfrak{g}$. This is the **Lie-Poisson structure** on $\mathfrak{g}^*$.

More generally, for $\mathfrak{a}$ a [[Lie algebroid]] the fiberwise dual $\mathfrak{a}^*$ inherits such a Poisson manifold structure.

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

(...)

## Properties

### Symplectic groupoid

The [[symplectic groupoid]] [[Lie integration|integrating]] the Lie-Poisson structure on $\mathfrak{g}^*$ is the [[action groupoid]] $\mathfrak{g}^* //G$ of the [[coadjoint action]]. For more see at _[[symplectic groupoid]]_ in the section _[Examples -- Of Lie-Poisson stucture](symplectic+groupoid#OfLiePoissonStructure)_.

### Symplectic leaves

The [[symplectic leaves]] of the Lie-Poisson structure on $\mathfrak{g}^*$ are the [[coadjoint orbits]].

## Related concepts

* a _[[moment map]]_ is often expresses as a Poisson homomorphism into a Lie-Poisson structure.

## References

The notion of Lie-Poisson structures was originally found by [[Sophus Lie]] and then rediscovered by [[Felix Berezin]] and by [[Alexander Kirillov]], [[Bertram Kostant]] and [[Jean-Marie Souriau]]. 

General accounts include

*  Izu Vaisman, section 3.1 of _Lectures on the Geometry of Poisson Manifolds_, Birkh&#228;user 1994

The [[strict deformation quantization]] of Lie-Poisson structures was considered in 

* [[Marc Rieffel]], _Lie group convolution algebras as deformation quantization of linear Poisson structures_, American Journal of Mathematics
Vol. 112, No. 4 (Aug., 1990), pp. 657-685 ([jstor]( http://www.jstor.org/stable/2374874))
 {#Rieffel90

The [[symplectic Lie groupoid]] [[Lie integration|Lie integrating]] Lie-Poisson structures is discussed as example 4.3 in

* {#BursztynCrainic} [[Henrique Bursztyn]], [[Marius Crainic]], _Dirac structures, momentum maps and quasi-Poisson manifolds_ ([pdf](http://www.preprint.impa.br/FullText/Bursztyn__Fri_Dec_23_11_24_19_BRDT_2005.html/alanfestimpa.pdf))
 

See also

* [[Victor Ginzburg]], [[Alan Weinstein]], _Lie-Poisson structure on some Poisson Lie groups_, Journal of the AMS, volume 5, number 2 (1992) ([pdf](http://www.ams.org/journals/jams/1992-05-02/S0894-0347-1992-1126117-8/S0894-0347-1992-1126117-8.pdf))



[[!redirects Lie-Poisson structures]]
