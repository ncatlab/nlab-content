
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Where the [[center of a category]] is in general just a [[commutative monoid]] (the [[endomorphism monoid]] of its [[identity functor]] formed in the [[functor category]]), for [[additive categories]] this commutative monoid carries the further [[structure]] of a [[commutative ring]]: the [[endomorphism ring]] of its identity functor.  (In fact this is also true for [[Ab-enriched categories]], which are more general.)



## Definition

\begin{definition}
For $\mathcal{C}$ an [[Ab-enriched category]] (eg. an [[additive category]]) its *center* is

$$
  Z(\mathcal{C})
  \;\coloneqq\;
  [\mathcal{C}, \mathcal{C}]
  \big(id_{\mathcal{C}}, id_{\mathcal{C}}\big)
  \;\;
  \in
  \;
  CRing
  \,,
$$

where

* $[\mathcal{C}, \mathcal{C}]$ denotes the [[enriched functor category]] of [[enriched functor|enriched]] [[endofunctors]] on $\mathcal{C}$,

* $id_{\mathcal{C}}$ denotes the [[identity functor]] on $\mathcal{C}$.

By [[Ab]]-enrichment, this means that $Z(\mathcal{C})$ carries the [[structure]] of a [[commutative monoid|commutative]] [[monoid object]] [[internalization|internal]] to [[Ab]], [hence](monoid+object#Rings): the [[structure]] of a [[commutative ring]].
\end{definition}



## Examples

\begin{proposition}\label{CenterOfRModIsR}
Let [[Mod|$R Mod$]] denote the [[category]] of left [[modules]] of a [[ring]] $R$, and let $Z(R)$ be the [[center]] of $R$.   Then $Z(R Mod) \cong Z(R)$.
\end{proposition}
\begin{proof}
First note that for any $r \in Z(R)$, [[multiplication]] by $r$ acts as an [[endomorphism]] of each $R$-module, and this endomorphism is [[natural transformation|natural]]. This gives a [[ring homomorphism]] from $Z(R)$ to $Z(R Mod)$ which is [[injective]] because distinct elements of $r$ act differently as multiplication on the $R$-module given by $R$ itself. To see that it is also [[surjective]] and [hence](balanced+category#SetIsBalanced) [[bijective]], suppose $\alpha$ is a [[natural transformation]] of the [[identity functor]] on $R \Mod$.  Then $\alpha_R \colon R \to R$ must be right [[multiplication]] by some $r \in R$, since every endomorphism of $R \in R Mod$ is given by right multiplication by some $r \in R$.  Because $\alpha_R$ is natural and right multiplication by any $s \in R$ gives an endomorphism of $R \in R Mod$, we have
$$  (x s) r 
\, = \, 
\alpha_R(x s) 
\, = \, 
\alpha_R(x)s 
\, = \,
(x r) s 
$$
for all $x, s \in R$, so $r \in Z(R)$.  More generally, for any module $M$ and any $m \in M$ there is a module [[homomorphism]] $f \colon R \to M$ with $f(1) = m$, which by [[natural transformation|naturality]] implies
$$
  \alpha_M (m) 
   \,=\, 
  \alpha_M\big(f(1)\big)
   \,=\, 
  f\big(\alpha_R(1)\big) 
    \,=\, 
  f(r) 
    \,=\, 
  r m
  \,,
$$
which shows that $\alpha_M$ is multiplication by $r$. \end{proof}

\begin{remark}
Two rings whose [[categories of modules]] are equivalent as additive categories are said to be [[Morita equivalence|Morita equivalent]].  As a consequence of Prop. \ref{CenterOfRModIsR}, Morita equivalent *commutative* rings are already [[isomorphism|isomorphic]].
\end{remark}

As a further illustration of these ideas we show how the [[topological space|topology]] on a [[compact Hausdorff space]] is determined by the category of [[vector bundles]] over this space.  For any [[compact Hausdorff space]] $X$ let [[Vect(X)|$Vect(X)$]] denote the category of ([[finite-dimensional vector space|finite-]][[rank of a vector bundle|rank]] [[complex vector bundle|complex]]) [[vector bundles]] over $X$.  This category is [[additive category|additive]] and [[linear category|$\mathbb{C}$-linear]], i.e. [[enriched category|enriched]] over the category of [[complex vector spaces]].  Thus, the center of $Vect(X)$ is a [[commutative algebra]] over $\mathbb{C}$. Moreover:

\begin{proposition}\label{CenterOfVectXisCX}
If $X$ is a [[compact Hausdorff space]] then the center of [[Vect(X)|$Vect(X)$]] is $C(X)$, the [[function algebra]] of [[complex numbers|complex]]-valued [[continuous functions]] on $X$.  
\end{proposition}
\begin{proof}
For any [[field]] $k$ suppose $A$ is a commutative $k$-algebra.  Let $A Proj$ be the category of [[finitely generated module|finitely generated]] [[projective modules|projective $A$-modules]]. This is a $k$-linear additive category, and a straightforward extension of the proof of Prop. \ref{CenterOfRModIsR} shows that the center of $A Proj$ is isomorphic to $A$, not merely as a commutative ring, but as a commutative $k$-algebra.  

Let $X$ be a compact Hausdorff space.  By [[Serre-Swan theorem|Swan's theorem]], [[Vect(X)|$Vect(X)$]] is [[equivalence of categories|equivalent]], as a $\mathbb{C}$-linear additive category, to $C(X) Proj$.  Thus the center of $Vect(X)$ is isomorphic to $C(X)$.
\end{proof}

\begin{corollary}\label{CompactHausdorffSpacefromVect}
Suppose $X$ and $Y$ are [[compact Hausdorff spaces]] such that [[Vect(X)|$Vect(X)$]] and [[Vect(X)|$Vect(Y)$]] are equivalent as $\mathbb{C}$-linear categories. Then $X$ and $Y$ are [[homeomorphism|homeomorphic]].
\end{corollary}

\begin{proof}
By Prop. \ref{CenterOfVectXisCX}, if $Vect(X)$ and $Vect(Y)$ are equivalent as $\mathbb{C}$-linear categories then $C(X)$ and $C(Y)$ are isomorphic as complex algebras.  The [[Gelfand-Naimark theorem]] implies that when $X$ is compact Hausdorff, it is homeomorphic to the set of algebra [[homomorphisms]] $C(X) \to \mathbb{C}$, given the [[topology of pointwise convergence]].   Thus the isomorphism of algebras $C(X) \cong C(Y)$ implies that $X$ and $Y$ are homeomorphic.  (Note that we did not need to show $C(X) \cong C(Y)$ as $C^\ast$-algebras here, but this follows.)
\end{proof}

\begin{remark}
Note that it is much easier to recover $C(X)$ and thus $X$ starting from $\Vect(X)$ as a [[symmetric monoidal category|symmetric monoidal]] $\mathbb{C}$-linear category, since then the endomorphism algebra of the unit object, the trivial line bundle over $X$, is $C(X)$.   
\end{remark}

\begin{remark} 
An analogue of Prop. \ref{CompactHausdorffSpacefromVect} also holds for real vector bundles: the center of the $\mathbb{R}$-linear additive category of real vector bundles over $X$ is the algebra of continuous real-valued functions on $X$, and from this we can recover $X$, either by using the real version of the Gelfand-Naimark theorem, or by complexifying this algebra and using the usual complex version of the Gelfand-Naimark theorem.   
\end{remark}


## Properties

* In general, the construction of centers is not [[functor|functorial]] (except with respect to [[equivalence of categories]]); but it is functorial in some important special circumstances, such as certain reconstruction theorems. 

> (namely?)


## Related concepts

* [[center]], [[center of a category]]

* [[Drinfeld center]]

## References

Early occurrence of the definition of the center of an additive category: 

* [[Pierre Gabriel]], section 5.d of: *[[Des catégories abéliennes]]*, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __90__ (1962) 323-448 &lbrack;[numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0)&rbrack;


[[!redirects center of an abelian category]]
