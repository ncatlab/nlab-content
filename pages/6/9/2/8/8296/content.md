
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
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

The notion of _$\infty$-group extension_ generalizes the notion of [[group extension]] to [[homotopy theory]]/[[(∞,1)-category theory]] and from [[groups]] to [[∞-groups]]. It is also a generalization to [[nonabelian cohomology]] of the shifted group extensions that are classified by [[Ext]]-groups.

Under forming [[loop space objects]], $\infty$-group extensions are the special case of [[principal ∞-bundles]] whose base space is the [[moduli ∞-stack]] of the group being extended.

## Definition

Let $\mathcal{H}$ an [[(∞,1)-topos]] and $G, A, \hat G \in Grp(\mathbf{H})$ be [[∞-groups]] with [[deloopings]] $\mathbf{B}G$, $\mathbf{B}A$ and $\hat \mathbf{G}$, respectively.

+-- {: .num_defn}
###### Definition

An **extension** $\hat G$ of $G$ by $A$ is a [[fiber sequence]] of the form

$$
  \mathbf{B}A \stackrel{i}{\to} \mathbf{B}\hat G \stackrel{p}{\to} \mathbf{B}G
$$

such that the this exhibits $\Omega i \colon A \hookrightarrow \hat G$ as a [normal morphism](normal+subgroup#NormalMorphismOfInfinityGroups), hence such that $G \simeq \hat G \sslash G$.

=-- 

In the case that $A$ is at least [[En-algebra|E2]], hence in the case that the double [[delooping]] $\mathbf{B}^2 A$ exists, this is equivalent to the 

+-- {: .num_defn #E2Extensions}
###### Definition


For $A$ an [[En-algebra|E-2]] [[∞-group]], an extension $\hat G$ of $G$ by $A$ is a [[fiber sequence]] in $\mathbf{H}$ of the form

$$
  \array{
     \mathbf{B} A
     &
     \stackrel{\Omega \mathbf{c}}{\to}
     &
     \mathbf{B}\hat G
     \\
     && \downarrow
     \\
     && \mathbf{B}G
     &\stackrel{\mathbf{c}}{\to}&
     \mathbf{B}^2 A
     \,.
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Def. \ref{E2Extensions} equivalently says that

* $\mathbf{B}\hat G \to \mathbf{B}G$ is an $\mathbf{B} A$-[[principal ∞-bundle]] over $\mathbf{B}G$;

* the extension is classified by the [[group cohomology]] class

  $$
    [\mathbf{c}] \in \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^2 A) 
    =
    H^2_{Grp}(G,A)
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

If here $A$ is an [[Eilenberg-MacLane object]] $A = \mathbf{B}^{n}\mathcal{A}$, then the above says that extension of $G$ by the $n$-fold [[delooping]]/[[suspension]] $\mathbf{B}^n\mathcal{A}$ is classified by degree-$n$ [[group cohomology]]

$$
  H_{Grp}(G, \mathbf{B}^n\mathcal{A})
  =
  \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^{n+1}\mathcal{A})
  =
  H_{Grp}^{n+1}(G, \mathcal{A})
  \,.
$$

In particular if $G$ here is [[n-truncated object in an (infinity,1)-category|0-truncated]] (hence a plain [[group object]] in the underlying 1-[[topos]]) then this reproduces the traditional theory of [[group extensions]] of 1-groups by 1-groups.


=--


## Properties

Notably for abelian $A$, by the main classification result at _[[principal ∞-bundles]]_, the [[∞-groupoid]] of $\infty$-group extensions is equivalent to

$$
  \mathbf{Ext}^n(G, A)
  \coloneqq
  \mathbf{H}(\mathbf{B}G, \mathbf{B}^{n+1}A)
  \,.
$$

In particular they are classified by the intrinsic $n+1$st $A$-[[cohomology]] of $\mathbf{B}G$.

## Examples

* For $\mathbf{H} = Sh_\infty(C)$ the [[(∞,1)-category of (∞,1)-sheaves]] on some [[site]] $C$ the [[Dold-Kan correspondence]] embeds [[chain complexes]] of [[abelian sheaves]] over $C$ into $\mathbf{H}$. Under this embedding ordinary [[Ext]]-groups and the shifted extensions that they classify (see [here](http://ncatlab.org/nlab/show/Ext#RelationToGroupExtensions)) identify with $\infty$-group extensions in the above sense.
 
* The [[string 2-group]] is an extension in $\mathbf{H} = $ [[Smooth∞Grpd]] of the [[spin group]] by the [[circle 2-group]].

* The [[fivebrane 6-group]] is an extension in $\mathbf{H} = $ [[Smooth∞Grpd]] of the [[string 2-group]] by the [[circle n-group|circle 6-group]].

## References

The general concept is discussed in section 4.3 of 

* [[Thomas Nikolaus]], [[Danny Stevenson]], [[Urs Schreiber]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_

Extensions by [[braided 2-groups]] are discussed in 

* Evan Jenkins, _Extensions of groups by braided 2-groups_ ([arXiv:1106.0772](http://arxiv.org/abs/1106.0772))


[[!redirects ∞-group extension]]
[[!redirects infinity-group extensions]]
[[!redirects ∞-group extensions]]

