
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

## Definition

### Vertical vector fields

Let $\pi : P \to X$ be a [[bundle]] in the [[category]] of [[SmoothManifolds]]. A [[vector field]] $v \in \Gamma(T P)$ is _vertical_ with respect to this bundle if it is in the [[kernel]] of the [[derivative]] $d \pi \colon T P \to T X$.

### Vertical tangent bundle
 {#VerticalTangentBundle}

The collection of vertical vectors forms the _vertical tangent bundle_ inside the full [[tangent bundle]], typically denoted $T_\pi P$.

For $\pi \colon P \to B$ a [[smooth function]] between [[smooth manifolds]], its _vertical tangent bundle_ is the [[fiber]]-wise [[kernel]] of the [[differential]] $d \pi$, as shown in the following diagram (e.g [Tu 17 (27.4)](#Tu17),  [Berglund 20, p. 16](#Berglund20)):

\begin{tikzcd}[column sep=normal, row sep=small]
  T_{\pi} P
  \ar[
   r,
   "
    \mathrm{ker}(d \pi)
   "
  ]
  &
  T P 
  \ar[
    r,
    dashed,
    "d \pi"
  ]
  \ar[ddr]
  &
  \pi^\ast
  \big(
    T B 
  \big)
  \ar[
    r
  ]
  \ar[
    ddr,
    phantom,
    "
      \mbox{\tiny\rm(pb)}
    "{
      description
    }
  ]
  \ar[dd]  
  &
  T B
  \ar[
    dd
  ]
  \\
  \\
  &
  &
  P
  \ar[
    r,
    "\pi"{
      below
    }
  ]
  &
  B
\end{tikzcd}



### Horizontal differential forms

A [[differential form]] on $P$ is a [[horizontal differential form]] with respect to $P \to X$ it it _vanishes_ on vertical vector fields.

## Properties



\begin{proposition}\label{SplittingOfTotalSpaceTangentBundle}
  If $P \overset{\pi}{\longrightarrow} X$ is a [[surjective submersion]] (for instance a [[smooth manifold|smooth]] [[fiber bundle]]) then the full [[tangent bundle]] of its total space $P$ is [[isomorphism|isomorphic]] to the [[direct sum of vector bundles|direct sum]] of the vertical tangent bundle ([above](#VerticalTangentBundle)) with the [[pullback bundle|pullback]] of the [[tangent bundle]] of the base space:

$$
  T P
  \;\simeq\;
  \big(
    \pi^\ast T B
  \big)
  \oplus_P
  \big(
    T_\pi P
  \big)
$$
 
\end{proposition}

\begin{proof}
The assumption that $\pi$ is a [[surjective submersion]] implies that $d \pi \colon T P \longrightarrow \pi^\ast T B$ is a [[surjection]] and hence that 

$$
  0
    \to 
  T_\pi P
    \longrightarrow
  T P 
   \overset{d \pi}{\longrightarrow}
  \pi^\ast T B
    \to
  0
$$

is a [[short exact sequence]] of smooth [[real vector bundles]]. 

Now all [[short exact sequences]] of [[real vector bundles]] over [[paracompact topological spaces]] (such as [[smooth manifolds]]) [[split exact sequence|split]] (by a choice of fiberwise metric, e.g. Prop. 3.5 [here](http://www.math.ubc.ca/~cautis/math428/notes-bundles.pdf)), which is the statement to be shown.
\end{proof}

## Examples

\begin{proposition}\label{VerticalTangentBundleOfRealVectorBundle}
**([[vertical tangent bundle]] of a [[real vector bundle]])**
  Let $\pi \colon \mathcal{V} \longrightarrow M$ be a [[real vector bundle]]. Then its [[vertical tangent bundle]] is [[isomorphism|isomorphic]] to the its [[pullback bundle|pullback]] along itself:

$$
  T_\pi \mathcal{V}
  \;\simeq_{{}_{\mathcal{V}}}\;
  \pi^\ast \mathcal{V}
  \,.
$$
\end{proposition}

(e.g. [tomDieck 00 (6.9)](#tomDieck00), [tomDieck 08 (15.6.7)](#tomDieck2008), [Gollinger 16, inside the proof of Prop. 1.1.9](#Gollinger16))


\begin{prop}\label{StableTangentBundleOfUnitSphereBundle}
**([[stable tangent bundle]] of [[unit sphere bundle]])** \linebreak
  The once-[[stable tangent bundle|stabilized]] [[tangent bundle]] of a [[unit sphere bundle]] $S(\mathcal{V})$ in a [[real vector bundle]] $\mathcal{V} \overset{p}{\longrightarrow} M$ (Example \ref{UnitSphereBundles}) over a [[smooth manifold]] $M$ is [[isomorphism|isomorphic]] to the [[pullback bundle|pullback]]  of the [[direct sum of vector bundles|direct sum]] of the [[stable tangent bundle]] of the base manifold with that vector bundle:

$$
  T S(\mathcal{V}) \times \mathbb{R}
  \;
  \simeq_{{}_M}
  \;
  S(p)^\ast
  \big(
    T M 
    \oplus_M
    \mathcal{V}
  \big)
  \,.
$$
\end{prop}

This is stated without proof as [Crowley-Escher 03, Fact. 3.1](#CrowleyEscher03), apparently reading between the lines in [Milnor 56, p. 403](#Milnor1956). The key sub-statement that 

$$
  T_{S(p)} S(\mathcal{V}) \times \mathbb{R}
  \;\simeq_{{}_M}\;
  \mathcal{V}
$$

is made explicit in [Gollinger 16, Prop. 1.1.9](#Gollinger16)

\begin{proof}\label{ProofOfStableTangentBundleOfUnitSphereBundle}
  Consider first the actual [[tangent bundle]] but to the [[open ball]]/[[disk]]-[[fiber bundle]] $D(\mathcal{V})$ that fills the given sphere-fiber bundle: By the standard splitting ([this Prop.](vertical+vector+field#SplittingOfTotalSpaceTangentBundle)) this is the [[direct sum of vector bundles|direct sum]]

$$
  T 
  \big(
   D(\mathcal{V})
  \big)
  \;\simeq\;
  \big(
     D(p)^\ast T M
  \big)
  \oplus_M
  T_p D(\mathcal{V})
  \,,
$$

where $T_p D(\mathcal{V})$ is the [[vertical tangent bundle]] of the disk bundle. But, by definition of disk bundles, that is the restriction of the vertical tangent bundle of the vector bundle $\mathcal{V}$ itself, and that is just the pullback of that vector bundle along itself (by [this Example](vertical+vector+field#SplittingOfTotalSpaceTangentBundle)):

$$
  \begin{aligned}
  \cdots
  & 
  \simeq\;
  \big(
    D(p)^\ast T M
  \big)
  \oplus_M
  \big(
    D(p)^\ast \mathcal{V}
  \big)
  \\
  & \simeq\;
  D(p)^\ast
  \big(
    T M \oplus_M \mathcal{V}
  \big)
  \,.
  \end{aligned}
$$

To conclude, it just remains to observe that the [[normal bundle]] of the [[n-sphere]]-boundary inside the $(n+1)$-ball is manifestly [[trivial bundle|trivial]], so that the restriction of the tangent bundle of $D(\mathcal{V})$ to $S(\mathcal{V})$ is the [[stable tangent bundle]] of $S(\mathcal{V})$.
\end{proof}


## Related concepts

* [[evolutionary vector field]]


## References

Textbook accounts:


* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]],  Section VII.1 in Volume 1 _De Rham Cohomology of Manifolds and Vector Bundles_, in: _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)  ([ISBN:978-0-12-302701-6](https://www.elsevier.com/books/connections-curvature-and-cohomology-v1/greub/978-0-12-302701-6))

*  {#Tu17} [[Loring Tu]], Section 27.5 in: _Differential Geometry -- Connections, Curvature, and Characteristic Classes_, Springer 2017 ([ISBN:978-3-319-55082-4](https://www.springer.com/gp/book/9783319550824), [pdf](http://www.math.nagoya-u.ac.jp/~richard/teaching/f2018/Tu_geometry.pdf))


See also:

* [[Manifold Atlas]], _<a href="http://www.map.mpim-bonn.mpg.de/Tangent_bundles_of_bundles_(Ex)">Tangent bundles of bundles</a>_

* {#tomDieck00} [[Tammo tom Dieck]], around Satz 6.9 in: _Topologie_, De Gruyter (2000)([doi:10.1515/9783110802542](https://doi.org/10.1515/9783110802542))

* {#tomDieck2008} [[Tammo tom Dieck]],  around (15.6.7) _Algebraic topology_, European Mathematical Society, Zürich (2008) ([doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/diecktop.pdf))


* {#Gollinger16} William Gollinger, Section 1.1.4 in: _Madsen-Tillmann-Weiss Spectra and a Signature Problem for Manifolds_, M&uuml;nster 2016 ([pdf](https://repositorium.uni-muenster.de/document/miami/7369e8b5-6ae4-4e42-b6f3-4602ec24427a/diss_gollinger.pdf), [[GollingerMTWSpectra.pdf:file]])

* {#Berglund20} Alexander Berglund, _Characteristic classes for families of bundles_ ([arXiv:2012.12170](https://arxiv.org/abs/2012.12170))

* [MO discussion](https://math.stackexchange.com/a/251668/58526)

[[!redirects vertical vector fields]]

[[!redirects vertical vector]]
[[!redirects vertical vectors]]

[[!redirects vertical tangent bundle]]
[[!redirects vertical tangent bundles]]

[[!redirects vertical vector bundle]]
[[!redirects vertical vector bundles]]

[[!redirects vertical cotangent bundle]]
[[!redirects vertical cotangent bundles]]

