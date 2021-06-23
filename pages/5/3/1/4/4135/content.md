
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

Given a finite dimensional (pseudo)-[[Riemannian manifold]] $(X,g)$, the _Hodge star operator_ "completes" a $k$-[[differential form]] to the [[volume form]] of $(X,g)$. 


## Definition

Let $(X,g)$ be an [[orientation|oriented]] $n$-[[dimension]]al [[smooth manifold]] $X$ endowed with a ([[pseudo-Riemannian metric|pseudo]])-[[Riemannian metric]] $g$.  For $0 \leq k \leq n$, write $\Omega^k(X)$ for the [[vector space]] of $k$-[[differential forms|forms]] on $X$.

### Hodge inner product

The metric $g$ naturally induces a nondegenerate symmetric [[bilinear form]]  

$$
  (-\mid-) 
   \;\colon\;
  \Omega^k(X) \otimes \Omega^k(X)
    \to 
  \Omega^0(X)
  \,.
$$

If $X$ is [[compact space|compact]] then the [[integral]] of this against the [[volume form]] $vol_g$ exists. This is the _Hodge inner product_ 

$$
  \langle - , - \rangle 
  \;\colon\;
  \Omega^k(X)\otimes \Omega^k(X)
  \to 
  \mathbb{R}
$$

$$
  \langle \alpha, \beta \rangle
  :=
  \int_X (\alpha\mid \beta) vol
 \,.
$$

### Hodge star operator

The **Hodge star operator** is the unique 
[[linear function]] 

$$
  {\star}\colon \Omega^k (X) \to \Omega^{n-k} (X)
$$ 

defined by the identity

$$
  \alpha \wedge \star\beta 
  = 
  (\alpha \mid \beta) vol_g, 
  \qquad 
  \forall \alpha,\beta \in \bigwedge^k X
  \,,
$$

where $vol_g \in \Omega^n X$ is the [[volume form]] induced by $g$.

Therefore in terms of the Hodge operator the [[Hodge inner product]] reads

$$
  \langle \alpha , \beta\rangle
  = 
  \int_X \alpha \wedge \star \beta
  \,.
$$

### Generalizations

The [[Riemannian metric|metric]] $g$ is used in two places in the specification of the Hodge operator: in the inner product on forms and in the volume form.  If $X$ is equipped only with a [[volume form]] (not necessarily coming from a metric), then the Hodge operator still takes $k$-forms to $(n-k)$-[[multivector field|vector fields]].  If the manifold is not oriented, then the metric only gives a [[volume pseudoform]], but the Hodge operator still takes $k$-forms to $(n-k)$-[[pseudoforms]].  Finally, if $X$ is equipped with only a volume pseudoform (which is equivalent to an [[absolutely continuous measure|absolutely continuous]] [[Radon measure]] on $X$), then the Hodge operator takes $k$-forms to $(n-k)$-pseudovector fields.  (Of course, in every case, one might apply the operator to pseudoforms or multivector fields to begin with.)


## Properties

### Component expression
 {#ComponentExpression}

Let $X$ be a ([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian manifold]] of [[dimension]] $D$, and locally, on some [[open subset]] $U \subset X$, let

$$
  e^1, \dots, e^D
  \;\in\;
  \Omega^1(U)
$$ 

be a frame of [[differential 1-forms]] (a [[vielbein]]). For example if $\{x^i\}$ is a [[coordinate chart]] on $U$, then $e^i \coloneqq d x^i$ is such a frame.

With this choice, any [[differential p-form]] $\alpha \in \Omega^p(U)$ has a component expansion

$$
  \alpha 
  \;=\; 
  \frac{1}{p!} 
  \alpha_{i_1 \dots i_p} 
  \, e^{i_1} \wedge \cdots \wedge e^{i_p}
$$

for [[smooth function]]-components $\{\alpha_{i_1 \cdots i_p}\}$ (where here and in the following we use the [[Einstein summation convention]]).

In terms of these components, the Hodge dual $\star \alpha$ of $\alpha$ is expressed by the following formula:

\[
  \label{ComponentFormulaForHodgeStar}
  \begin{aligned}
    \star \alpha 
    & = \; 
    \frac{1}{
      p!
     (D-p)!
    } 
    \sqrt{
      \left\vert 
       det\big((g_{i j})\big) 
      \right\vert
    }
    \, 
    \alpha_{
      \color{green} j_1 \dots j_p
    } 
    g^{
     {\color{green} j_1 }
     {\color{cyan} i_1 }
    }
    \cdots 
    g^{
     {\color{green} j_p }
     {\color{cyan} i_p }
    }
    \epsilon_{
      {\color{cyan} i_1 \dots i_p }
      {\color{orange} i_{p+1} \cdots i_D }
    } 
    e^{
      \color{orange} i_{p+1}
    } 
     \wedge 
     \cdots 
     \wedge 
    e^{
      \color{orange} i_D
    }
    \\
    & =
    \frac{1}{
      p! (D-p)!
    } 
    \sqrt{
      \left\vert 
       det\big((g_{i j})\big) 
      \right\vert
    }
    \,
    \alpha^{ \color{green} i_1 \dots i_p }   
    \epsilon_{
      { \color{green} i_1 \dots i_p }
      { \color{orange} i_{p + 1} \cdots i_D }
     } 
     e^{
       \color{orange}
       i_{p + 1}
     } 
     \wedge 
       \cdots 
     \wedge 
     e^{
       \color{orange}
       i_{D}
     } 
  \end{aligned}
\]

Here 

* $p!$, $(D-p)!$ are the [[factorials]] of $p$ and $(D-p)$, respectively, 

* $\epsilon_{i_1,\dots,i_n} \in \{+1, ,-1\}$ (the [[Levi-Civita symbol]]) is the [[signature of a permutation|signature]] of the [[permutation]] $(1,2,\dots,D) \mapsto (i_1,i_2,\dots,i_D)$ 

* $(g_{i j})$ is the [[square matrix]] of components of the [[metric tensor]] in the chosen basis, i.e. such that

  $$
    g \;=\;
    g_{i j} e^i \otimes e^j
  $$

* $det(g)$ is the [[determinant]] of $(g_{i j})$

* $\left\vert g \right\vert$ is the [[absolute value]] of the determinant.


### Basic properties 
 {#BasicProperties}

Let $(X,g)$ be a [[Riemannian manifold]] of [[dimension]] $n$ and let $\omega,\lambda \in \Omega^k(X)$. Then the following holds:

\[
  \label{HodgeSquareOnRiemannian}
  \star(\star\omega) = (-1)^{k(n+1)} \omega = (-1)^{k(n-k)} \omega
\]

\[
  \label{HodgeStarPreservesHodgeInnerProduct}
  \langle\star\omega , \star\lambda\rangle = \langle\omega | \lambda\rangle
\]

\[
  \label{HodgeStarOfUnityIsVolume}
  \star 1 = dvol
  \,,
\]

where $dvol$ denotes the [[volume form]].

## Examples

### Hodge star operator on a K&#228;hler manifold
 {#OnAKahlerManifold}

On a [[Kähler manifold]] $\Sigma$ of [[dimension]] $dim_{\mathbb{C}}(\Sigma) = n$ the Hodge star operator acts on the [[Dolbeault complex]] as

$$
  \star \;\colon\; \Omega^{p,q}(X) \longrightarrow \Omega^{n-q,n-p}(X)
  \,.
$$

(notice the exchange of the role of $p$ and $q$). See e.g. ([Biquerd-H&#246;ring 08, p. 79](#BiquerdHoering08)). See also at _[[Serre duality]]_.



[[!include Hodge star operator on Minkowski spacetime -- section]]







## Related concepts

* [[Laplace-Beltrami operator]]

* [[self-dual higher gauge field]]

## References

Some useful basic formulas are listed in 

* _Hodge theory on Riemannian manifolds_ , lecture notes ([pdf](http://math.uh.edu/~minru/Riemann08/hodgetheory.pdf))

A unified perspective in terms of [[Berezin integration]]:

* [[Leonardo Castellani]], [[Roberto Catenacci]], [[Pietro Antonio Grassi]], _The Hodge Operator Revisited_ ([arXiv:1511.05105](https://arxiv.org/abs/1511.05105))

Discussion in [[complex geometry]] includes

* {#BiquerdHoering08} O. Biquard, A. H&#246;ring, _K&#228;hler geometry and Hodge theory_, 2008 ([pdf](http://math.unice.fr/~hoering/hodge/hodge.pdf))

With an eye towards application in [[supergravity]] and [[string theory]]:

* {#BNS04} [[Igor Bandos]], [[Alexei Nurmagambetov]], [[Dmitri Sorokin]], Appendix A of _Various Faces of Type IIA Supergravity_, Nucl. Phys. B676 (2004) 189-228 ([arXiv:hep-th/0307153](https://arxiv.org/abs/hep-th/0307153))

Discussion of the [[Hodge star operator]] on [[supermanifolds]] (in terms of [[picture changing operators]] and integral top-forms for [[integration over supermanifolds]]):

* [[Leonardo Castellani]], [[Roberto Catenacci]], [[Pietro Antonio Grassi]], _Hodge Dualities on Supermanifolds_, Nuclear Physics B Volume 899, October 2015, Pages 570-593 ([arXiv:1507.01421](https://arxiv.org/abs/1507.01421))

[[!redirects Hodge star]]
[[!redirects Hodge star operator]]
[[!redirects Hodge star operators]]

[[!redirects Hodge inner product]]

[[!redirects Hodge dual]]
[[!redirects Hodge duals]]

[[!redirects Hodge duality]]
[[!redirects Hodge dualities]]

[[!redirects Hodge pairing]]
[[!redirects Hodge pairings]]



