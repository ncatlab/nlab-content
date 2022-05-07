
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In a [[locally ∞-connected (∞,1)-topos]] with [[full and faithful (∞,1)-functor|fully faithful]] [[inverse image]] (such as a [[cohesive (∞,1)-topos]]), the extra [[left adjoint]] $\Pi$ to the [[inverse image]] $Disc$ of the [[global sections]] [[geometric morphism]] $\Gamma$ induces a  [[higher modality]] $\esh \coloneqq Disc \circ \Pi$, which sends an [[object]] to something that may be regarded equivalently as its [[geometric realization]] or its [[fundamental ∞-groupoid]] (see at _[[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]]_ and at _[[shape via cohesive path ∞-groupoid]]_). In either case $\esh X$ may be thought of as the _[[shape]]_ of $X$ and therefore one may call $\esh$ the _shape modality_.  It forms an [[adjoint modality]] with the [[flat modality]] $\flat \coloneqq Disc \circ \Gamma$.




## Properties

### Relative shape and factorization system

Generally, given an [[(∞,1)-topos]] $\mathbf{H}$ (or just a 1-[[topos]]) equipped with an [[idempotent monad]] $\esh \colon \mathbf{H} \to \mathbf{H}$ (a [[modal type theory|(higher) modality]]/[[closure operator]]) which preserves [[(∞,1)-pullbacks]] over objects in its [[essential image]], one may call a [[morphism]] $f \colon X \to Y$ in $\mathbf{H}$ _$\esh$-closed_ if the [[unit of an adjunction|unit]]-diagram

$$
  \array{
    X &\stackrel{\eta_X}{\to}& \esh(X)
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{\esh(f)}}
    \\
    Y &\stackrel{\eta_Y}{\to}& \esh(Y)
  }
$$

is an [[(∞,1)-pullback]] diagram. These $\esh$-closed morphisms form the right half of an [[orthogonal factorization system]], the left half being the morphisms that are sent to [[equivalence in an (∞,1)-category|equivalences]] in $\mathbf{H}$.




+-- {: .num_defn}
###### Definition

Let $(\Pi\dashv \Disc\dashv \Gamma):H\to\infty\Grpd$ be an [[infinity-connected (infinity,1)-topos]], let $\esh:=\Disc \Pi$ be the geometric path functor / geometric homotopy functor, let $f:X\to Y$ be a $H$-morphism, let $c_{\esh} f$ denote the ∞-pullback


$$\array{c_{\esh} f&\to& {\esh} X\\\downarrow&&\downarrow^{{\esh}_f}\\Y&\xrightarrow{1_{(\Pi\dashv \Disc)}}&{\esh}Y}$$

$c_{\esh} f$ is called $\esh$**-closure of** $f$.

$f$ is called $\esh$**-closed** if $X\simeq c_{\esh}f$.
=--

If a morphism $f:X\to Y$ factors into $f=g\circ h$ and $h$ is a $\esh$-equivalence then $g$ is $\esh$-closed; this is seen by using that $\esh$ is idempotent.



$\Pi$-closed morphisms are a right class of an [[orthogonal factorization system]] ([[orthogonal factorization system in an (∞,1)-category|in an (∞,1)-category]]) and hence, as discussed there, are closed under [[limits]], [[composition]], [[retracts]] and satisfy the left cancellation property.

### As open maps

A consequence of the previous property is that the class of $\esh$-closed morphisms gives rise to an admissible structure in the sense of [[structured (infinity,1)-topos|structured spaces]] on an (∞,1)-connected (∞,1)-topos, hence they serve as a class of a kind of [[open maps]].

### Shape via cohesive path ∞-groupoid

See at _[[shape via cohesive path ∞-groupoid]]_.

## Examples

### Internal locally constant $\infty$-stacks
 {#LocallyConstantStacks}

In a [[cohesive (∞,1)-topos]] $\mathbf{H}$ with an [[∞-cohesive site]] of definition, the [[fundamental ∞-groupoid]]-functor $\esh$ satisfies the above assumptions (this is the example gives this entry its name). The $\esh$-closed morphisms into some $X \in \mathbf{H}$ are canonically identified with the [[locally constant ∞-stacks]] over $X$. The correspondence is effectively what is called [[categorical Galois theory]].

+-- {: .num_prop}
###### Proposition

Let $H$ be a [[cohesive (∞,1)-topos]] possessing a [[∞-cohesive site]] of definition.
Then for $X\in H$ the locally constant ∞-stacks $E\in \L\Const(X)$, regarded as ∞-bundle morphisms $p:E\to X$ are precisely the $\esh$-closed morphisms into $X$

=--


### Formally &#233;tale morphisms
 {#EtaleMorphisms}

If a [[differential cohesive (∞,1)-topos]] $\mathbf{H}_{th}$, the [[de Rham space]] functor $\Im$ satisfies the above assumptions. The $\Im$-closed morphisms are precisely the [[formally étale morphisms]].

## Related entries

* [[shape]], [[shape of an (∞,1)-topos]]

* [[shape via cohesive path ∞-groupoid]]

* [[reflective subuniverse]]

[[!include cohesion - table]]

* [differential cohesion - cotangent bundles](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#CotangentBundles)


## References

### General

* [[Urs Schreiber]], Sec. 3.4.5 in: _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](https://arxiv.org/abs/1310.7930))

* {#Shulman15} [[Mike Shulman]], Sec. 9.7 in: _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

### In Smooth∞Grpd

For the case of [[Smooth∞Grpd]]:

On [[shape via cohesive path ∞-groupoids]]:

* {#Pavlov14} [[Dmitri Pavlov]], _Structured Brown representability via concordance_, 2014 ([pdf](https://dmitripavlov.org/concordance.pdf), [[Pavlov_Concordance.pdf:file]])

* {#BEBP19} [[Daniel Berwick-Evans]], [[Pedro Boavida de Brito]], [[Dmitri Pavlov]], _Classifying spaces of infinity-sheaves_ ([arXiv:1912.10544](https://arxiv.org/abs/1912.10544))

Discussion for [[orbifolds]], [[étale groupoids]] and, generally, [[étale ∞-groupoids]]:

* {#Carchedi15} [[David Carchedi]], _On The Homotopy Type of Higher Orbifolds and Haefliger Classifying Spaces_ ([arXiv:1504.02394](http://arxiv.org/abs/1504.02394))





[[!redirects Pi-closed morphisms]]

[[!redirects cohesive shape]]
[[!redirects cohesive shapes]]

[[!redirects Pi modality]]
[[!redirects Pi-closed morphism]]

