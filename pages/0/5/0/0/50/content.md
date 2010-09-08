
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
* automatic table of contents goes here
{:toc}

## Lie's three theorems

There is an obvious [[functor]]
$$
  Lie : Lie Gp \to Lie Alg
$$
which sends every [[Lie group]] to its [[Lie algebra]] and every homomorphism of Lie groups to the corresponding homomorphism of Lie algebras. 

Lie's three theorems establish the following properties of this functor.

  1. **Lie's first theorem** is today regarded as lacking a good notion of differentiable [[manifold]];

  2. **Lie II** 
     If $G$ and $H$ are Lie groups 
     with Lie algebras $\mathfrak{g} = Lie(G)$ and $\mathfrak{h} = Lie(H)$;
      such that $G$ is simply connected;
      and if $f : \mathfrak{g} \to \mathfrak{h}$ is a morphism of Lie algebras;
      then there is a unique morphism $F : G \to H$ of Lie groups lifting $g$, i.e. such that $f = Lie(F)$.  

  3. **Lie III** **$Lie$ is surjective on objects**: to every Lie algebra  $\mathfrak{g}$ there is a Lie group $G$ such that $\mathfrak{g} = Lie(G)$. Moreover, there exists such $G$ which is simply connected.


##Restriction to simply connected Lie groups

Let $LieGroups_{simpl}$ be the [[full subcategory]] of $LieGroups$ on simply connected Lie groups. Then the above implies that restricted to $LieGroups_{simpl}$ the functor $diff$ becomes a surjective [[equivalence of categories]]

## Generalization of Lie's theorems to Lie groupoids

The [[horizontal categorification]] of Lie's theorems for Lie groups leads to analogous statements for [[Lie groupoid|Lie groupoids]]: in this case $diff$ becomes the differentiation functor
from [[Lie groupoid|Lie groupoids]] to [[Lie algebroid|Lie algebroids]]
$$
  diff : LieGroupoids \to LieAlgebroids
  \,.
$$

In the case of Lie groupoids, the condition of a group being simply connected which plays an important role in the above statements is generalized to the condition that _source fibers_ of the Lie groupoid  (the preimages $s^{-1}(x)$ of the source map $s : C_1 \to C_0$ at every object $x \in C_0$ of the Lie groupoid $C$) are simply connected. One says 
$$
  (C is source-simply connected)
  \Leftrightarrow
  (\forall x \in C_0 : 
    \pi_1(s^{-1}(x)) = 0
  )
  \,.
$$


**_Lie II_ for Lie groupoids** now reads exactly as _Lie II_ for Lie groups, with "simply connected" replaced by "source simply connected". 

Lie II for Lie groupoids was proven in

* K. C. H. Mackenzie and P. Xu, _Integration of Lie bialgebroids_, Topology, 39(3):445-467

and

* I. Moerdijk and J Mr&#269;un, _On integrability of infinitesimal actions_, Amer. J. Math. 124(3):567-593, 2002

**_Lie III_ for Lie groupoids** does _not_ hold in direct generalization: 

by the general mechanism of [[Lie integration]] the space of morphisms of the source simply-connected _topological_ groupoid $G$ integrating a Lie algebroid $\mathfrak{g}$ is a _quotient_ space. This quotient may fail to be a _manifold_ due to singularities.

The precise conditions under which Lie algebroids do have Lie groupoids integrating them were found in

* Crainic and Fernandes, _Integrability of Lie brackets_ ([arXiv](http://arxiv.org/abs/math.DG/0105033)).

A comprehensive review is in

* Rui Loja Fernandes, Marius Crainic,
_Lectures on Integrability of Lie Brackets_,
([arxiv](http://aps.arxiv.org/abs/math.DG/0611259))

A review of Lie theory of Lie groupoids in on pages 3-5 of

* Marius Crainic, Rui Loja Fernandes
Lectures on Integrability of Lie Brackets
([arxiv](http://aps.arxiv.org/abs/math.DG/0611259))

and in the introduction of

 * Chenchang Zhu, _Lie II theorem for Lie algebroids via stacky Lie groupoids_, ([arXiv](http://arxiv.org/abs/math/0701024)).


## Motivation for generalized smooth groupoids

This failure of Lie III for [[Lie groupoid|Lie groupoids]], i.e. for [[internal category|internal groupoids]] in [[Diff]] seems to suggest that the category of manifolds is not the natural home for general [[Lie theory]]. More concretely, it seems to suggest that [[Lie theory]] ought to be practiced internal to some category of [[generalized smooth space]]s.

One such choice is given by replacing manifolds by [[differentiable stack]]s.

## Generalization of Lie's theorems to stacky Lie groupoids

The generalization of Lie's theorems from Lie groups to to [[Lie theory for stacky Lie groupoids|stacky Lie groupoids]] is discussed
in 

* Chenchang Zhu, _Lie II theorem for Lie algebroids via stacky Lie groupoids_, ([arXiv](http://arxiv.org/abs/math/0701024)).



[[!redirects Lie's three theorems]]
[[!redirects Lie's theorem]]
[[!redirects Lie's theorem]]
[[!redirects Lie's theorems]]
[[!redirects Lie's theorems]]
[[!redirects Lie's first theorem]]
[[!redirects Lie's first theorem]]
[[!redirects Lie's second theorem]]
[[!redirects Lie's second theorem]]
[[!redirects Lie's third theorem]]
[[!redirects Lie's third theorem]]