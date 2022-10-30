
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}


## Idea

In a context of [[differential cohesion]], with [[infinitesimal shape modality]] $\Im$, then for every object $X \in \mathbf{H}$ its _infinitesimal disk bundle_ $T_{inf}X$ is the [[homotopy fiber product|homotopy]] [[fiber product]]

$$
  \array{
    T_{inf} X &\stackrel{ev}{\longrightarrow}& X
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\stackrel{i}{\longrightarrow}& \Im(X)
  }
$$

of the $X$ component $i \colon X \to \Im X$ of the [[unit of a monad|unit]]  of the $\Im$-[[monad]] with itself.

By the [[pasting law]], the [[fibers]] of $p \colon T_{inf}X \to X$ over [[global points]] of $X$ are indeed the [[infinitesimal disks]] around these points.

More generally, for $(E \to X) \in \mathbf{H}_{/X}$ a [[bundle]] over $X$, then $T_{inf}E \coloneqq T_{inf} X \times_{\Im X} E \simeq X\times_{\Im X} E$, sitting in the [[pasting]] composite of pullbacks

$$
  \array{
    T_{inf} E &\longrightarrow& E
    \\
    \downarrow && \downarrow
    \\
    T_{inf} X &\stackrel{ev}{\longrightarrow}& X
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\stackrel{i}{\longrightarrow}& \Im(X)
  }
  \,.
$$

Stated more abstractly, this means that forming infinitesimal disk bundles is the [[monad]]

$$
  T_{inf} X \times_X (-)
  =
  i^\ast i_!
$$

induced by the [[adjoint triple]] of [[base change]] along $i$

$$
  (i_! \dashv i^\ast \dashv i_\ast)
  \;\colon\;
  \mathbf{H}_{/X}
   \stackrel{\overset{i_!}{\longrightarrow}}{\stackrel{\overset{i^\ast}{\longleftarrow}}{\underset{i_\ast}{\longrightarrow}}}
  \mathbf{H}_{/\Im X}
  \,.
$$

## Properties

### Relation to de Rham stacks

Regarding $i \colon X \to \Im(X)$ as the canonical [[atlas]] of the [[de Rham stack]] $\Im X$, then $T_{inf} X$ is the object of morphisms in the corresponding [[groupoid object in an (infinity,1)-category|groupoid object]].

### Relation to jet bundles

The infinitesimal disk bundle construction is [[left adjoint]] to the [[jet comonad]]

$$
  T_{inf} \dashv Jet
  \,.
$$

In the context of [[synthetic differential geometry]] this is ([Kock 80, prop. 2.2](#Kock80)). In terms of [[differential cohesion]] this is simply the adjoint pair induced by the [[base change]] [[adjoint triple]]

$$
  (i_! \dashv i^\ast \dashv i_\ast)
  \;\colon\;
  \mathbf{H}_{/X}
    \stackrel{\overset{i_!}{\longrightarrow}}{\stackrel{\overset{i^\ast}{\longleftarrow}}{\underset{i_\ast}{\longrightarrow}}}
  \mathbf{H}_{/\Im X}
  \,.
$$

### Relation to frame bundles

For $X$ a $V$-[[manifold]], then its infinitesimal disk bundle is a [[fiber bundle]] ([[fiber infinity-bundle]]) with typical fiber $\simeq \mathbb{D}^V_e$. This is the [[associated bundle]] ([[associated infinity-bundle]]) to the [[frame bundle]] $Fr(X) \to X$ (or more generally of the [[higher order frame bundle]] when $(\Re \dashv \Im)$ encodes higher order infinitesimal thickening). 

See at _[differential cohesion -- frame bundles](differential+cohesive+%28infinity%2C1%29-topos#GLnTangentBundles)_.


## Related concepts

* [[frame bundle]]

* [[jet bundle]]

## References

Discussion in [[synthetic differential geometry]] is, under the name "bundles of $k$-monads", in 

* {#Kock80} [[Anders Kock]], above prop. 2.2 _Formal manifolds and synthetic theory of jet bundles_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1980) Volume: 21, Issue: 3 ([Numdam](http://www.numdam.org/item?id=CTGDC_1980__21_3_227_0))

* {#Kock09} [[Anders Kock]], p. 39 of _Synthetic Geometry of Manifolds_, 2009 ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

In terms of [[differential cohesion]]

* _[differential cohesion -- Frame bundles](differential+cohesive+%28infinity%2C1%29-topos#GLnTangentBundles)_

[[!redirects infinitesimal disk bundles]]
