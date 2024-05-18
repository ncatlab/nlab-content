
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
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

Let $f \colon X \to Y$ be a [[differentiable function]]
between [[smooth manifolds]] (or just [[differentiable manifolds]]) of [[finite number|finite]] [[dimension]].

We denote by $T X$,  $T Y$ the [[tangent bundles]] and by $(-)\times_Y (-)$ the [[fiber product]] of [[differentiable functions]] into $Y$. In particular, $f^\ast T Y \,=\, X \times_Y T Y$ is the [[pullback bundle]] of $T Y$ along $f$ to a [[real vector bundle]] over $X$.

+-- {: .num_defn}
###### Definition


The [[differentiable function]] $f : X \to Y$ is called an **immersion** precisely if the canonical [[map]]

$$
  T X \longrightarrow X \times_Y T Y \eqqcolon f^* T Y
$$

is a [[monomorphism]]. 

=--

This map is the one induced from the [[universal property]] of the [[pullback]] by the [[commuting diagram]]

$$
  \array{
    T X &\overset{d f}{\longrightarrow}& T Y
    \\
    \big\downarrow 
      && 
    \big\downarrow
    \\
    X &\underset{f}{\longrightarrow}&  Y
  }
$$

given by the [[differential]] of $f$ going between the [[tangent bundles]].

Equivalently this means the following:

+-- {: .num_defn}
###### Definition

The function $f : X \to Y$ is an immersion precisely if for every point $x \in X$ the [[differential]] 

$$
  d f|_x \;\colon\; T_x X \to T_{f(x)} Y
$$ 

between the [[tangent space]] of $X$ at $x$ and the tangent space of $Y$ at $f(y)$ is an [[injection]].

=--

+-- {: .num_defn #EmbeddingOfSmoothManifolds}
###### Definition
**([[embedding of smooth manifolds]])**

An immersion whose underlying [[continuous function]] is an [[embedding of topological spaces]] is called an an _[[embedding of smooth manifolds]]_.

=--

+-- {: .num_example #ImmersionsThatAreNotEmbeddings}
###### Example
**(immersions that are not embeddings)**

<div style="float:right;margin:0px 10px 10px 10px;">
<img src="https://ncatlab.org/nlab/files/Immersion.png" width="150">
</div>

Consider an immersion $f \;\colon\; (a,b) \to \mathbb{R}^2$ of an [[open interval]] into the [[Euclidean plane]] (or the [[2-sphere]]) as shown on the right. This is not an [[embedding of smooth manifolds]]: around the points where the image crosses itself, the function is not even [[injective]], but even 
at the points where it just touches itself, the pre-images under $f$ of open subsets of $\mathbb{R}^2$ do not exhaust the open subsets of $(a,b)$, hence do not yield the [[subspace topology]].

<div style="float:left;margin:10px 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/Figure8Immersion.png" width="400">
</div>

Concretely, consider the function $\big($[[sin]]$(2-),$ [[sin]]$(-)\big) \;\colon\; (-\pi, \pi) \longrightarrow \mathbb{R}^2$. While this is an immersion and [[injective]], it fails to be an [[embedding of smooth manifolds|embedding]] due to the points at $t = \pm \pi$ "touching" the point at $t = 0$.

> figure from [Lee (2012, Fig. 4.3)](#Lee12)

=--

\linebreak

## Properties

### Relation to embeddings

Immersion are precisely the  "local embeddings": 

\begin{proposition}
\label{ImmersionsAreLocalEmbeddings}
A smooth map $f \colon X \to Y$ of [[smooth manifolds]] is an immersion precisely if for every point $x \in X$ there is an [[open neighbourhood]] $x \in U \subset X$ such that $f|_U \colon U \to Y$ is an [[embedding of smooth manifolds]].
\end{proposition}
(e.g. [Boothby, III Thm. 4.12](#Boothby))

Since moreover the [[embeddings of smooth manifolds]] admit local slice charts (see [there](embedding+of+differentiable+manifolds#ExistenceOfSiceCharts)) so do immersions.

In the generality of [[supermanifolds]] this is [Varadarajan 2004, Thm. 4.4.3](#Varadarajan04).




### Relation to formal immersions

The related concept of [[formal immersion of smooth manifolds]], defined as an injective bundle morphism $T M \to T N$ between tangent bundles, is in some ways easier to study, in the sense that the collection of all such formal immersions, $Imm^f(M, N)$, is simpler to analyze. Then under some conditions on $M$ and $N$ (see there), it is the case that the map $Imm(M, N) \to \Imm^f(M, N)$ is a [[weak homotopy equivalence]]. This is a case of the [[h-principle]].


### Characterization in differential cohesion
 {#InDifferentialCohesion}

A [[smooth function]] $f : X \to Y$ between [[smooth manifolds]] is canonically regarded as a morphism in the [[cohesive (∞,1)-topos]] [[SynthDiff∞Grpd]]. With respect to the canonical [[infinitesimal cohesion|infinitesimal neighbourhood inclusion]] $i : $ [[Smooth∞Grpd]] $\hookrightarrow$ [[SynthDiff∞Grpd]] there is a notion of [[formally unramified morphism]] in $SynthDiff\infty Grpd$.

$f$ is an immersion precisely if it is formally unramified with respect to this infinitesimal cohesion.

See the discussion at [[SynthDiff∞Grpd]] for details.

## Variants

The [[algebraic geometry]] analogue of a submersion is a [[smooth morphism of schemes|smooth morphism]].

The analogue between arbitrary [[topological spaces]] (not manifolds) is simply an [[open map]]. There is also [[topological submersion]], of which there are two versions.


## Related concepts

* [[formal immersion of smooth manifolds]]

* [[submersion]]

* [[local diffeomorphism]]

* [[embedding of smooth manifolds]]

* [[isometric immersion]]

* [[regular value]]


## References

* {#Boothby} [[William M. Boothby]], Def. III 4.3 in: *An introduction to differentiable manifolds and Riemannian geometry*, Academic Press (1975, 1986), Elsevier (2002) &lbrack;[ISBN:9780121160517](https://shop.elsevier.com/books/an-introduction-to-differentiable-manifolds-and-riemannian-geometry-revised/boothby/978-0-08-057475-2), [pdf](https://aetemad.iut.ac.ir/sites/aetemad.iut.ac.ir/files/files_course/william_m._boothby_an_introduction_to_differentibookfi.org_.pdf)&rbrack;


* {#Lee12} [[John Lee]], Chapter 4 of: *Introduction to Smooth Manifolds*, Springer (2012) &lbrack;[doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://math.berkeley.edu/~jchaidez/materials/reu/lee_smooth_manifolds.pdf)&rbrack;

Discussion in the generality of [[supermanifolds]]:

* {#Varadarajan04} [[Veeravalli Varadarajan]], pp. 148 in: _[[Supersymmetry for mathematicians]]: An introduction_, Courant Lecture Notes in Mathematics **11**, American Mathematical Society (2004) &lbrack;[doi:10.1090/cln/011](http://dx.doi.org/10.1090/cln/011)&rbrack;




[[!redirects immersion of differentiable manifolds]]
[[!redirects immersions of differentiable manifolds]]
