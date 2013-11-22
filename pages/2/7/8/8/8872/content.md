
#Contents#
* table of contents
{:toc}

## Idea

The [[tangent bundle]] to an [[algebraic variety]] $X$ is abstractly defined by the methods of [[synthetic differential geometry]] as the space of maps

$$
  D \longrightarrow X
  \,,
$$

where $D$ is the [[spectrum of a commutative ring|spectrum]] of the [[ring of dual numbers]].

If $X$ is sufficiently regular, then this is the naive "Zariski [[tangent space]]". More generally the correct construction is given by the _tangent cone_ construction.

## Definition

+-- {: .num_defn}
###### Definition

For $X \hookrightarrow \mathbb{A}^n$ an [[affine algebraic variety]] definied by an [[ideal]] $I \hookrightarrow R[x_1, \cdots, x_n]$, hence $X \simeq Spec(R[x_1, \cdots, x_n]/I)$,then  its _tangent cone_ is 

$$
  C X \coloneqq Spec(R[x_1, \cdots, x_n]/I_\ast)
$$

where $I_\ast$ is the [[ideal]] obtained from $I$ by truncating each [[polynomial]] $f \in I \hookrightarrow R[x_1, \cdots, x_n]$ to its homogeneous part of lowest monomial degree.

=--

## Properties

### Relation to &#233;tale morphisms

A [[homomorphism]] $f \colon X \longrightarrow Y$ of [[algebraic varieties]] over an [[algebraically closed field]] is an [[étale morphism]] if for all points $x \in X$ it induces an [[isomorphism]] of tangent cones

$$
  C_x X \longrightarrow C_{f(x)} Y
  \,.
$$

e.g. ([Costa, def. 1.1.8](#Costa)).

+-- {: .num_remark}
###### Remark

This is the same kind of characterization as for [[local diffeomorphisms]] (see there) in terms of [[tangent spaces]].

More generally, both cases are special cases of the definition of [[formally étale morphisms]] in terms of an [[infinitesimal shape modality]] $\Pi_{inf}$ as those morphisms $f \colon X \to Y$ such that the [[unit of a monad|unit]] [[natural transformation|naturality square]]

$$
  \array{
    X &\longrightarrow& \Pi_{inf}(X)
    \\
    \downarrow && \downarrow
    \\
    Y &\longrightarrow& \Pi_{inf}(Y)
  }
$$

is a [[pullback]].

=--


## References

Reviews include

* [[James Milne]], p. 18 of _[[Lectures on Étale Cohomology]]_

* Edgar Costa, around def. 1.1.6  of _&#201;tale cohomology_ ([pdf](https://dspace.ist.utl.pt/bitstream/2295/686086/1/tese.pdf))
  {#Costa}

See also

* [[Igor Shafarevich|Igor R. Shafarevich]], _Basic algebraic geometry_ 

* Wikipedia [Tangent cone](http://en.wikipedia.org/wiki/Tangent_cone)

* [[eom]]: [tangent cone](http://www.encyclopediaofmath.org/index.php/Tangent_cone)

[[!redirects tangent cones]]
