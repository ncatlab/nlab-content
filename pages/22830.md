
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Any [[free loop stack]] $[S^1, \mathcal{X}]$ carries a canonical [[group action]] of the [[circle group]] $S^1$, given by rigid rotation of loops (explicit models are discussed in [Lupercio & Uribe 01, Sec. 3.6](free+loop+orbifold#LupercioUribe01)). This allows to form the further [[homotopy quotient]]/[[quotient stack]] by this action:

\[
  \label{CyclicLoopStack}
  Cyc(\mathcal{X})
  \;\coloneqq\;
  [S^1, \mathcal{X}] \!\sslash\! S^1
  \,.
\]

In analogy with [[cyclic loop spaces]], this may be called the *cyclic loop stack* of $\mathcal{X}$.

## Properties

### Groupoid presentations

While this is a basic and canonical construction, there seems to be little to no explicit discussion of it in the literature (as of summer 2021). However, the concrete groupoid-presentations considered in [Huan 18, Def. 2.5, 2.9](#Huan18), following [Ganter 07, Sec. 2.1](#Ganter07), may be understood as plausible proposals for models of (eq:CyclicLoopStack).

Motivated from these definitions is, in turn, that of [[Huan's inertia orbifolds]], whose [[orbifold K-theory]] defines a form of [[equivariant elliptic cohomology]] of $\mathcal{X}$.


### General abstract characterization
 {#GeneralAbstractPresentations}

Regarding 

* the stack $\mathcal{X} \in \mathbf{H}$ as an object in the [[(∞,1)-topos]] of [[Smooth∞Groupoids]] (or [[DTopological∞Groupoids]] or whatever is appropriate), 

* the [[circle group]] $S^1 \in Groups(SmoothManifolds) \xhookrightarrow{ Cdfflg } Groups(\mathbf{H})$ as a ([[smooth ∞-group|smooth]]) [[∞-group]] with [[delooping]]/[[moduli ∞-stack]] $\mathbf{B}S^1$,

then ([BMSS 19, Sec. 2.2](cyclic+loop+space#BMSS19)) the cyclic loop stack is equivalently the right [[base change]] ([[dependent product]]) of $\mathcal{X}$ along the point inclusion $pt_{\mathbf{B}S^1} \colon \ast \to \mathbf{B}S^1$ followed by left [[base change]] ([[dependent sum]]) back to the absolute context:

$$
  Cyc
  \big(
    \mathcal{X}
  \big)
  \;\;
  \simeq
  \;\;
  \underset{\mathbf{B}S^1 \to \ast}{\sum}
  \underset{\ast \to \mathbf{B}S^1}{\prod}
  (\mathcal{X})
  \,.  
$$

<center>
<a href="https://ncatlab.org/schreiber/show/Twisted+Equivariant+Differential+non-abelian+generalized+cohomology"
<img src="https://ncatlab.org/nlab/files/GeneralAbstractCyclicLoopStacks.jpg" width="460">
</a>
</center>


From this one may extract component models by invoking the right [[Quillen adjunction]] which encodes the derived co-free $\infty$-action, discussed [here](Borel+model+structure#RelationToModelStructureOnPlainSimplicialSets).


## Related concepts

* [[Huan's inertia orbifold]]

* [[double dimensional reduction]]

## References

Groupoid models that plausibly represent cyclic loop stacks are discussed (under the notation "$Loops^{ext}$") in 

* {#Huan18} [[Zhen Huan]], Def. 2.5, 2.9 in: _Quasi-Elliptic Cohomology I_, Advances in Mathematics, Volume 337, 15 October 2018, Pages 107-138 ([arXiv:1805.06305](https://arxiv.org/abs/1805.06305), [doi:10.1016/j.aim.2018.08.007](https://doi.org/10.1016/j.aim.2018.08.007))

following

* {#Ganter07} [[Nora Ganter]], Section 2.1 in: *Stringy power operations in Tate K-theory* ([arXiv:math/0701565](https://arxiv.org/abs/math/0701565))

[[!redirects cyclic loop stacks]]

