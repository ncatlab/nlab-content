<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Frequently one encounters an ordinary [[category]] $C$ which is known in some way or other to be the $1$-[[1-category|categorical]] truncation of a [[higher category theory|higher category]] $\hat C$. 

Standard examples include the categories [[SimpSet]] of [[simplicial set]]s (or [[Top]] of [[topological space]]s) and $Ch(Ab)$ of [[chain complex]]es of [[abelian group]]s. Both are obtained from full [[(infinity,1)-category|(infinity,1)-categories]] by forgetting higher morphisms.

The most important information that is lost by forgetting the higher morphisms of a higher category is that about which 1-morphisms are, while not [[isomorphism]]s, invertible up to higher cells, i.e. [[equivalence]]s. 

To the full $(\infty,1)$-category $\hat C$ is canonically associated a 1-category $Ho(\hat C)$ called the [[homotopy category of an (infinity,1)-category]], which is obtained from $\hat C$ not by simply forgetting the higher morphisms, but by quotienting them out, i.e. by remembering the _equivalence classes_ of 1-morphisms. In the $(\infty,1)$-category [[Top]] (restricted to sufficiently nice objects, such as compactly generated weakly Hausdorff topological spaces) these higher morphisms are literally the [[homotopy|homotopies]] between 1-morphisms, and more generally one tends to address higher cells in $(\infty,1)$-categories as homotopies. Therefore the name _homotopy category of an $(\infty,1)$-category_ for $Ho(\hat C)$. In particular $Ho(\hat{Top})$ is the standard homotopy category originally introduced in topology.


Now, given just the truncated 1-category $C$ but equipped with the structure of a [[category with weak equivalences]] which indicates which morphisms in $C$ are to be regarded as equivalences in a higher categorical context, there is a universal solution to the problem of finding a cartegory $Ho(C)$ equipped with a functor $Q : C \to Ho(C)$ such that $Q$ sends all (morphisms labeled as) weak equivalences in 
$C$ to isomorphisms in $Ho(C)$.

In good situations, one may also find an $(\infty,1)$-category $\hat C$ corresponding to $C$, and the notions of homotopy category $Ho(C)$ and $Ho(\hat C)$ coincide. 

This is in particular the case when $C$ is equipped with the structure of a combinatorial [[simplicial model category]] and $\hat C$ is the $(\infty,1)$-category [[presentable (infinity,1)-category|presented]] by $C$ with its model structure. (For instance [[Higher Topos Theory|HTT, remark A.3.1.8]]).



#Definition#

Given a [[category with weak equivalences]] (such as a [[model category]]), its __homotopy category__ $Ho(C)$ is -- if it exists -- the [[category]] which is universal with the property that there is a [[functor]]

$$
 Q :  C \to Ho(C)
$$

that sends every weak equivalence in $C$ to an [[isomorphism]] in $Ho(C)$. 

One also writes $Ho(C) := W^{-1}C$ or $C[W^{-1}]$ and calls it the [[localization]] of $C$ at the collection $W$ of weak equivalences.

More in detail, the universality of $Ho(C)$ means the following:

* for any (possibly [[large category|large]]) category $A$ and functor $F : C \to A$ such that $F$ sends all $w \in W$ to isomorphisms in $A$, there exists a functor $F_Q : Ho(C) \to A$ and a natural isomorphism

$$
  \array{
     C &&\stackrel{F}{\to}& A
     \\
     \downarrow^Q& \Downarrow^{\simeq}& \nearrow_{F_Q}
     \\
     Ho(C)
  }
$$


* the functor $Q^* : Func(Ho(C),A) \to Func(C,A)$ is a [[full and faithful functor]].


The second condition implies that the functor $F_Q$ in the first condition is unique up to unique isomorphism.

#Properties#

* If it exists, the homotopy category $Ho(C)$ is unique up to [[equivalence of categories]].


# Remarks #



* As described at [[localization]], in general, the morphisms of $Ho(C)$ must be constructed using zigzags of morphisms in $C$ in which the backwards-pointing arrows are weak equivalences.  This means that in general, $Ho(C)$ need not be [[locally small category|locally small]] even if $C$ is.  However, in many cases (such as any [[model category]]) there is a more direct description of the morphisms in $Ho(C)$ as [[homotopy]] classes of maps in $C$ between suitably "good" (fibrant and cofibrant) objects.

* In classical topology, _the_ homotopy category refers to the homotopy category of $Top$ with weak homotopy equivalences, which can equivalently be constructed as the category of homotopy classes of maps between [[CW complex|CW complexes]].

* In [[2-limit|2-categorical terms]], the homotopy category $Ho(C)$ is the _coinverter_ of the canonical 2-cell
$$\array{& \to \\ W & \Downarrow & C\\ & \to}$$
where $W$ is the category whose objects are morphisms in $W$ and whose morphisms are commutative squares in $C$.

#Derived category#

What is called a [[derived category]] is the special case of the homotopy category of a [[category of chain complexes]] in an [[abelian category]]. See [[derived category]] for more details.

#References#

See the references at [[model category]].