
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Lie's three theorems

There is an obvious [[functor]]
$$
  Lie \;\colon\; Lie Gp \to Lie Alg
$$
from [[LieGroups]] to [[LieAlgebras]] -- *[[Lie differentiation]]* -- which sends any [[Lie group]] to its [[Lie algebra]] and every [[group homomorphism]] of Lie groups to the corresponding [[algebra homomorphism]] of Lie algebras. 

Lie's three theorems can be understood as establishing salient properties of this functor. More exactly, Lie's theorems provide a foundation establishing an [[equivalence of categories|equivalence]] between [[local Lie groups]] and [[Lie algebras]]; subsequent work by [[Élie Cartan]] and others extended the theorems to give information on actual ("global") [[Lie groups]] via the functor $Lie$. 

  1. **Lie's first theorem** is purely local; see the [Encyclopedia of Math](http://www.encyclopediaofmath.org/index.php/Lie_theorem) for a statement. (Here one lacks a good notion of [[differentiable manifold]] for extending this to a global result.) 

  2. **Lie II** 
     Let $G$ and $H$ be Lie groups 
     with Lie algebras $\mathfrak{g} = Lie(G)$ and $\mathfrak{h} = Lie(H)$, 
      such that $G$ is [[simply connected space|simply connected]]. 
      If $f : \mathfrak{g} \to \mathfrak{h}$ is a morphism of Lie algebras,
      then there is a unique morphism $F : G \to H$ of Lie groups lifting $f$, i.e. such that $f = Lie(F)$.  

  3. **Lie III** (Cartan-Lie theorem) The functor $Lie$ **is [[essentially surjective functor|essentially surjective on objects]]**: for every [[finite-dimensional vector space|finite dimensional]] [[real vector space|real]] [[Lie algebra]]  $\mathfrak{g}$ there is a real Lie group $G$ such that $\mathfrak{g} \cong Lie(G)$. Moreover, there exists such $G$ which is simply connected. 

For a classical account see:

* [[Hans Duistermaat]], [[Johan A. C. Kolk]], Chapter 1 of: *Lie groups*, Springer (2000) &lbrack;[doi:10.1007/978-3-642-56936-4](https://doi.org/10.1007/978-3-642-56936-4)&rbrack;

\begin{remark}

In his third theorem, Lie proved only the existence of a [[local Lie group]], but not the global existence (nor the simply connected choice) which were established only a few decades later by [[Élie Cartan]]. Hence the full theorem would properly be called the *Cartan-Lie theorem*. From an [[nPOV]], the third Lie theorem establishes the essential surjectivity of the functor $Lie$ from the category of _local Lie groups_ to the category of finite dimensional real Lie algebras, and similarly the second Lie theorem establishes that this functor is [[fully faithful functor|fully faithful]] (so the two together establish that this functor is an [[equivalence of categories|equivalence]]). The historically incorrect naming of the Cartan-Lie theorem as the "third Lie theorem" is largely due to the influence the lectures of [Serre 1964](#Serre64).

\end{remark}

## Restriction to simply connected Lie groups

Let $LieGroups_{simpl}$ be the [[full subcategory]] of $LieGroups$ consisting of simply connected Lie groups. Then the above implies that restricted to $LieGroups_{simpl}$, the functor $Lie$ becomes an [[equivalence of categories]]. 

## Generalization of Lie's theorems to Lie groupoids

The [[horizontal categorification]] of Lie's theorems for Lie groups leads to analogous statements for [[Lie groupoid|Lie groupoids]]. In other words, there are analogous properties for the differentiation functor 
$$diff : LieGroupoids \to LieAlgebroids.$$
from [[Lie groupoid|Lie groupoids]] to [[Lie algebroid|Lie algebroids]]. 

In the case of Lie groupoids, the condition of a group being simply connected which plays an important role in the above statements is generalized to the condition that _source fibers_ of the Lie groupoid  (the preimages $s^{-1}(x)$ of the source map $s : C_1 \to C_0$ at every object $x \in C_0$ of the Lie groupoid $C$) are simply connected. One says 
$$
  (C is source-simply connected)
  \Leftrightarrow
  (\forall x \in C_0 : 
    \pi_1(s^{-1}(x)) = 0
  ).
$$

**_Lie II_ for Lie groupoids** now reads exactly as _Lie II_ for Lie groups, with "simply connected" replaced by "source simply connected". 


## Related concepts

* [Lie's third theorem for Leibniz algebras](Leibniz+algebra#LieThirdTheorem)


## References

### For Lie groups and Lie algebras

Review:

* {#Serre64} [[Jean-Pierre Serre]]: *Lie Algebras and Lie Groups -- 1964 Lectures given at Harvard University*, Lecture Notes in Mathematics **1500** (1992) &lbrack;[doi:10.1007/978-3-540-70634-2](https://doi.org/10.1007/978-3-540-70634-2)&rbrack;

* [[Sigurdur Helgason]], Thm. 7.5 in: *Differential geometry, Lie groups and symmetric spaces*, Graduate Studies in Mathematics **34** (2001) &lbrack;[ams:gsm-34](https://bookstore.ams.org/gsm-34)&rbrack;


### For Lie groupoids and Lie algebroids


Lie II for [[Lie groupoids]] was proven in

* K. C. H. Mackenzie and P. Xu, _Integration of Lie bialgebroids_, Topology, 39(3):445-467

and

* I. Moerdijk and J Mrčun, _On integrability of infinitesimal actions_, Amer. J. Math. 124(3):567-593, 2002

**_Lie III_ for Lie groupoids** does _not_ hold in direct generalization: 

by the general mechanism of [[Lie integration]] the space of morphisms of the source simply-connected _topological_ groupoid $G$ integrating a Lie algebroid $\mathfrak{g}$ is a _quotient_ space. This quotient may fail to be a _manifold_ due to singularities.

On the precise conditions under which [[Lie algebroids]] do have [[Lie groupoids]] integrating them:

* [[Marius Crainic]], [[Rui Loja Fernandes]], *Integrability of Lie brackets*, Ann. of Math. **157** 2 (2003) 575-620 &lbrack;[arXiv:math.DG/0105033](http://arxiv.org/abs/math.DG/0105033), [doi:10.4007/annals.2003.157.575](https://doi.org/10.4007/annals.2003.157.575)&rbrack;

Enlarging [[Lie groupoids]] to groupoids in the category of [[etale stacks]] and smooth maps results in a Cartan–Lie theorem for [[Lie algebroids]]:

* [[Hsian-Hua Tseng]], [[Chenchang Zhu]], *Integrating Lie algebroids via stacks*, Compositio Mathematica **142** (2006) 251–270 &lbrack;[doi:10.1112/S0010437X05001752](https://doi.org/10.1112/S0010437X05001752)&rbrack;

In particular, a [[Lie algebroid]] can be integrated to an ordinary [[Lie groupoid]] if and only if the integrating groupoid in [[etale stacks]] is [[representable functor|representable]].

Comprehensive review:

* [[Rui Loja Fernandes]], [[Marius Crainic]]: *Lectures on Integrability of Lie Brackets*, Geometry & Topology Monographs **17** (2011) 1–107 &lbrack;[arxiv:math.DG/0611259](https://arxiv.org/abs/math/0611259), [doi:10.2140/gtm.2011.17.1](http://dx.doi.org/10.2140/gtm.2011.17.1)&rbrack;

and in the introduction of

* [[Chenchang Zhu]], _Lie II theorem for Lie algebroids via stacky Lie groupoids_ &lbrack;[arXiv:math/0701024](http://arxiv.org/abs/math/0701024)&rbrack;

### In higher Lie theory 


On [[L-infinity algebras]] related to [[smooth infinity-groups]] in [[higher Lie theory]]:

> (see also references at *[[Lie integration]]*)

* [[Christopher L. Rogers]], [[Jesse Wolfson]]: *Lie's Third Theorem for Lie $\infty$-Algebras* &lbrack;[arXiv:2409.08957](https://arxiv.org/abs/2409.08957)&rbrack;






[[!redirects Lie's theorem]]
[[!redirects Lie's theorems]]
[[!redirects Lie's first theorem]]
[[!redirects Lie's second theorem]]
[[!redirects Lie's third theorem]]
