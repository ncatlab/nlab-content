
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Any [[free loop space]] $\mathcal{L}X$ has a canonical [[action]] ([[infinity-action]]) of the [[circle group]] $S^1$. The [[homotopy quotient]] $\mathcal{L}(X)/S^1$ of this action might be called the _cyclic loop space_ of $X$, and is also known as the *string space* of $X$ ([Chataur 2005. 4.8.1](#Chataur05), [B&ouml;kstedt & Ottosen 05, p. 1](#BokstedtOttosen05)).

If $X = Spec(A)$ is an [[affine variety]] regarded in [[derived algebraic geometry]], then $\mathcal{O}(\mathcal{L}Spec(A))$ is the [[Hochschild homology]] of $A$ and $\mathcal{O}((\mathcal{L}Spec(A))/S^1)$ the corresponding [[cyclic homology]], see the discussion at _[[Hochschild cohomology]]_.

If $X = Y//G$ is the [[homotopy quotient]] of a [[topological space]] by a [[topological group]] action, regarded as a locally constant $\infty$-stack, so that the $S^1$-action on $\mathcal{L}(X//G)$ is an $B \mathbb{Z}$-action, then the restriction of the cyclic loop space to the constant loops $\mathcal{L}_{const}Y//G \to \mathcal{L}(Y//G)$ has been called the _twisted loop space_ in ([Witten 88](#Witten88)). This terminology has been widely adopted, for example in the context of the [[transchromatic character]] map ([Stapleton 11](#Stapleton11))

## Properties

### As right base change along $\ast \to \mathbf{B} S^1$
 {#AsRightBaseChange}

The cyclic loop space $\mathcal{L}X  \sslash S^1$ is equivalently the right [[base change]]/[[dependent product]] along the canonical point inclusion $\ast \to B S^1$ ([this prop.](base+change#CyclicLoopSpace)) into the [[delooping]] of $S^1$ (the [[classifying space]] of the [[circle group]] when realized in the [[classical model structure on topological spaces|homotopy theory of]] [[topological spaces]]). See also at _[[double dimensional reduction]]_ ([BMSS 19, Sec. 2.2](#BMSS19), following [FSS 18, Sec. 3](#FSS18)).

### Ordinary cohomology of $\mathcal{L}X \sslash S^1$ as cyclic cohomology of $X$

Let $X$ be a [[simply connected topological space|simply connected]] [[topological space]]. 

The [[ordinary cohomology]] $H^\bullet$ of its [[free loop space]] is the [[Hochschild homology]] $HH_\bullet$ of its [[singular cohomology|singular chains]] $C^\bullet(X)$:

$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( C^\bullet(X) )
  \,.
$$

Moreover the $S^1$-equivariant cohomology of the loop space, hence the ordinary cohomology of the cyclic loop space $\mathcal{L}X \sslash S^1$ is the [[cyclic homology]] $HC_\bullet$ of the singular chains:

$$
  H^\bullet(\mathcal{L}X \sslash S^1)
    \simeq
  HC_\bullet( C^\bullet(X) )
$$

([Jones 87, Thm. A](#Jones87), review in [Loday 92, Cor. 7.3.14](#Loday92), [Loday 11, Sec. 4](#Loday11))

If the [[coefficients]] are [[rational numbers|rational]], and $X$ is of [[finite type]] then this may be computed by the _[[Sullivan model for free loop spaces]]_, see there the section on _[Relation to Hochschild homology](Sullivan+model+of+free+loop+space#RelationToHochschildHomology)_.


In the special case that the [[topological space]] $X$ carries the structure of a [[smooth manifold]], then the singular cochains on $X$ are equivalent to the [[dgc-algebra]] of [[differential forms]] (the [[de Rham algebra]]) and hence in this case the statement becomes that 


$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( \Omega^\bullet(X) )
  \,.
$$

$$
  H^\bullet(\mathcal{L}X \sslash S^1)
    \simeq
  HC_\bullet( \Omega^\bullet(X) )
  \,.
$$

This is known as _[[Jones' theorem]]_ ([Jones 87](#Jones87))

An [[(infinity,1)-category theory|infinity-category theoretic]] proof of this fact is indicated at _[Hochschild cohomology -- Jones' theorem](Hochschild+cohomology#JonesTheorem)_.



### Stable splitting
 {#StableSplitting}

\begin{proposition}
For $X \in TopSpaces^{\ast/}$ a [[pointed topological space]] with [[reduced suspension]] denoted $\Sigma X$, the [[stabilization]] of its cyclic loop spaces splits as a [[direct sum]] of [[suspension spectra]], hence the underlying [[infinite loop space]] of that as a [[product space]], of the following form:

$$
  \Omega^\infty \Sigma^\infty 
  \big(
    Maps(S^1, \Sigma X) \sslash S^1
  \big)
  \;\;
  \simeq
  \;\;
  \big(
    \Omega^\infty \Sigma^\infty B S^1
  \big)
  \times 
  \underset{
    k \in \mathbb{N}_+
  }{\prod}
  \Omega^\infty \Sigma^\infty 
  \big(
    (E (\mathbb{Z}/k))_+
    \wedge_{\mathbb{Z}/k}
    X^{\wedge^n}
  \big)
$$

In terms of the [[suspension spectra]] themselves:

$$
  \Sigma^\infty
  \Big(
    \underset{
      \frac{
        E S^1 \times_{S^1} Maps(S^1, \Sigma X)
      }
      {
        E S^1 \times_{S^1} \ast \,=\, B S^1
      }
    }{
    \underbrace{
      Maps
      \big(
        S^1, \, \Sigma X
      \big)
        \wedge_{S^1} 
      (E S^1)_+ 
    }
    }
  \Big)
  \;\;
  \simeq
  \;\;
  \underset{ k \in \mathbb{N}_{\geq 1} }{\vee}
  \Sigma^\infty
  \big(
    (E \mathbb{Z}/k)_+  \wedge_{\mathbb{Z}/k} X^{\wedge^k}
  \big)
$$

\end{proposition}

([Carlsson & Cohen 1987, Cor. C](#CarlssonCohen1987), announced in [Cohen 1985, p. 194](#Cohen1985)) See also at *[[stable splitting of mapping spaces]]*.

Here 

* $\wedge$ denotes the [[smash product]], 

* $\mathbb{Z}/k$ a [[cyclic group]], 

* $B G$ the [[classifying space]] of a [[Lie group]] $G$
  and $E G$ its [[universal principal bundle]], 

* $(-)_+$ the [adjoining of a base point](pointed+topological+space#ForgettingAndAdjoiningBasepoints) 

* and $(-)\wedge_{G} (-) \;\coloneqq\; \big((-) \wedge (-)\big)/G $.


\begin{example}
  For $X = S^n$ the [[n-sphere]], we have $\Sigma X \,=\, S^{n+1}$ and hence 
$$
  \Omega^\infty \Sigma^\infty 
  \big(
    Maps(S^1, S^{n+1}) \sslash S^1
  \big)
  \;\;
  \simeq
  \;\;
  \big(
    \Omega^\infty \Sigma^\infty B S^1
  \big)
  \times 
  \underset{
    n \in \mathbb{N}_{\geq 1}
  }{\prod}
  \Omega^\infty \Sigma^\infty 
  \big(
    (E (\mathbb{Z}/n))_+
    \wedge_{\mathbb{Z}/n}
    (S^{n})^{\wedge^n}
  \big)
$$
\end{example}
More on this case in [Hingston 1992](#Hingston92).


### Rational homotopy

For the [[rational homotopy type]] of cyclic loop spaces see at _[[Sullivan model for free loop space]]_.



## Related concepts

* [[double dimensional reduction]]

* [[string topology]]

* [[cyclic loop stack]]

* [[free loop space]], [[free loop stack]]

## References

The notion of the cyclic loop space of a topological space appears as:

* {#Cohen1985} [[Ralph Cohen]], p. 194 of: *A Model for the Free Loop Space of a Suspension*, in: [[Haynes Miller]], [[Douglas Ravenel]] (eds.), *Algebraic Topology*, Lecture Notes in Mathematics **1286**, Springer 1985 ([doi:10.1007/BFb0078743](https://link.springer.com/chapter/10.1007/BFb0078743))

* {#Jones87} [[John D.S. Jones]], _Cyclic homology and equivariant homology_, Invent. Math. __87__, 403-423 (1987) ([pdf](https://math.berkeley.edu/~nadler/jones.pdf), [doi:10.1007/BF01389424](https://doi.org/10.1007/BF01389424))

* {#CarlssonCohen1987} [[Gunnar Carlsson]], [[Ralph Cohen]], *The cyclic groups and the free loop space*, Commentarii Mathematici Helvetici **62** (1987) 423–449  ([doi:10.1007/BF02564455](https://doi.org/10.1007/BF02564455), [dml:140092](https://eudml.org/doc/140092))

* {#Witten88} [[Edward Witten]], _The index of the Dirac operator in loop space_. In Elliptic curves and modular forms in algebraic topology (Princeton, NJ, 1986), volume 1326 of Lecture Notes in Math., pages 161&#8211;181. Springer, Berlin, 1988 ([doi:10.1007/BFb0078045](https://doi.org/10.1007/BFb0078045))

* {#Loday92} [[Jean-Louis Loday]], *Cyclic Spaces and $S^1$-Equivariant Homology* ([doi:10.1007/978-3-662-21739-9_7](https://link.springer.com/chapter/10.1007/978-3-662-21739-9_7))

  Chapter 7 in: *Cyclic Homology*, Grundlehren **301**, Springer 1992 ([doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9))

* {#Chataur05} [[David Chataur]], *A bordism approach to string topology*, International Mathematics Research Notices **2005** 46, (2005)  ([arXiv:math/0306080](https://arxiv.org/abs/math/0306080), [doi:10.1155/IMRN.2005.2829](https://doi.org/10.1155/IMRN.2005.2829))


* {#Loday11}[[Jean-Louis Loday]], Section 4 of: _Free loop space and homology_, Chapter 4 in: Janko Latchev, Alexandru Oancea (eds.): *Free Loop Spaces in Geometry and Topology*, IRMA Lectures in Mathematics and Theoretical Physics **24**, EMS 2015 ([arXiv:1110.0405](https://arxiv.org/abs/1110.0405), [ISBN:978-3-03719-153-8](https://bookstore.ams.org/emsilmtp-24/))

* {#Stapleton11} [[Nathaniel Stapleton]], _Transchromatic generalized character maps_, Algebr. Geom. Topol. 13 (2013) 171-203 ([arXiv:1110.3346](https://arxiv.org/abs/1110.3346))

Specifically on cyclic loop spaces of [[n-spheres]]:

* {#Hingston92} [[Nancy Hingston]], *An Equivariant Model for the Free Loop Space of $S^N$*, American Journal of Mathematics **114** 1 (1992) 139-155 ([doi:10.2307/2374740](https://doi.org/10.2307/2374740), [jstor:2374740](https://www.jstor.org/stable/2374740))

See also:

* [[Urs Frauenfelder]], *Dihedral homology and the moon*, J. Fixed Point Theory Appl. **14** (2013) 55–69 ([arXiv:1204.4549](https://arxiv.org/abs/1204.4549), [doi:10.1007/s11784-013-0146-z](https://doi.org/10.1007/s11784-013-0146-z))



A version of the [[cyclic loop stack]] of [[orbifolds]], or at least its restriction to constant loops, namely [[Huan's inertia orbifold]], is discussed in the context of [[equivariant elliptic cohomology]] via [[Tate K-theory]] in:

* {#Huan18} [[Zhen Huan]], Def. 2.14 of: _Quasi-Elliptic Cohomology I_, Advances in Mathematics, Volume 337, 15 October 2018, Pages 107-138 ([arXiv:1805.06305](https://arxiv.org/abs/1805.06305), [doi:10.1016/j.aim.2018.08.007](https://doi.org/10.1016/j.aim.2018.08.007))

following 

* [[Zhen Huan]], Section 2.1.2 of: _Quasi-elliptic cohomology_, 2017 ([hdl](http://hdl.handle.net/2142/97268))

and recalled/expanded on in several followup articles, such as in

* [[Zhen Huan]], Section 2 of *Quasi-theories* ([arXiv:1809.06651](https://arxiv.org/abs/1809.06651))

The above formulation of cyclic loop spaces, in the generality of [[∞-stacks]], as right [[base change]] to the [[delooping]] of the [[circle group]], and its relation to [[double dimensional reduction]] in [[brane]]-physics, is due to:

* {#BMSS19} [[Vincent Braunack-Mayer]], [[Hisham Sati]], [[Urs Schreiber]]: Section 2.2 of _[[schreiber:Gauge enhancement of Super M-Branes|Gauge enhancement of Super M-Branes via rational parameterized stable homotopy theory]]_, Communications in Mathematical Physics, **371** 197 (2019) ([doi:10.1007/s00220-019-03441-4](https://doi.org/10.1007/s00220-019-03441-4), [arXiv:1806.01115](https://arxiv.org/abs/1806.01115))

following the analogous discussion in [[rational homotopy theory]] in 

* {#FSS18} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3 of: *[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes|T-Duality from super Lie $n$-algebra cocycles for super $p$-branes]]*, [ATMP Volume 22 (2018) Number 5](http://www.intlpress.com/site/pub/pages/journals/items/atmp/content/vols/0022/0005/), [doi:10.4310/ATMP.2018.v22.n5.a3](http://dx.doi.org/10.4310/ATMP.2018.v22.n5.a3), [arXiv:1611.06536](https://arxiv.org/abs/1611.06536))

with exposition in

* [[Urs Schreiber]], [Section 4](https://ncatlab.org/schreiber/show/Super+Lie+n-algebra+of+Super+p-branes#DoubleDimensionalReduction) of:  *[[schreiber:Super Lie n-algebra of Super p-branes]]* (2016)

[[!redirects cyclic loop spaces]]

[[!redirects string loop space]]
[[!redirects string loop spaces]]

[[!redirects twisted loop space]]
[[!redirects twisted loop spaces]]


