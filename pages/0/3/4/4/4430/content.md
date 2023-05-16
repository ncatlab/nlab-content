
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

Where the [[center of a category]] is in general just a [[commutative monoid]] (the [[endomorphism monoid]] of its [[identity functor]] formed in the [[functor category]]), for [[additive categories]] this commutative monoid carries the further [[structure]] of a [[commutative ring]]: the [[endomorphism ring]] of its identity functor.

## Properties

* In general, the construction of centers is not [[functor|functorial]] (except with respect to [[equivalence of categories]]); but it is functorial in some important special circumstances, such as certain reconstruction theorems. 

> (namely?)

## Examples

\begin{proposition}\label{CenterOfRModIsR}
Let [[Mod|$R Mod$]] denote the [[category]] of [[modules]] over a [[commutative ring]] $R$.  Then the center of $R Mod$ is $R$.  
\end{proposition}
\begin{proof}
First note that for any $r \in R$, [[multiplication]] by $r$ acts as an [[endomorphism]] of each $R$-module (because $R$ is commutative), and this endomorphism is [[natural transformation|natural]]. This gives a [[ring homomorphism]] from $R$ to the center of $R Mod$ which is [[injective]] because distinct elements of $r$ act differently as multiplication on the $R$-module given by $R$ itself. To see that it is also [[surjective]] and [hence](balanced+category#SetIsBalanced) [[bijective]], suppose $\alpha$ is a [[natural transformation]] of the [[identity functor]] on $R \Mod$.  Then $\alpha_R \colon R \to R$ must be [[multiplication]] by some $r \in R$, since every endomorphism of the $R$-module $R$ is given by multiplication by some $r \in R$.  More generally, for any module $M$ and any $m \in M$ there is a module [[homomorphism]] $f \colon R \to M$ with $f(1) = m$, which by [[natural transformation|naturality]] implies
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

\begin{corollary}
Suppose $X$ and $Y$ are [[compact Hausdorff spaces]] such that [[Vect(X)|$Vect(X)$]] and [[Vect(X)|$Vect(Y)$]] are equivalent as $\mathbb{C}$-linear categories. Then $X$ and $Y$ are [[homeomorphism|homeomorphic]].
\end{corollary}

\begin{proof}
By Prop. \ref{CenterOfVectXisCX}, if $Vect(X)$ and $Vect(Y)$ are equivalent as $\mathbb{C}$-linear categories then $C(X)$ and $C(Y)$ are isomorphic as complex algebras.  The [[Gelfand-Naimark theorem]] implies that when $X$ is compact Hausdorff, it is homeomorphic to the set of algebra [[homomorphisms]] $C(X) \to \mathbb{C}$, given the [[topology of pointwise convergence]].   Thus the isomorphism of algebras $C(X) \cong C(Y)$ implies that $X$ and $Y$ are homeomorphic.  (Note that we did not need to show $C(X) \cong C(Y)$ as $C^\ast$-algebras here, but this follows.)
\end{proof}

## Related concepts

* [[center]], [[center of a category]]

* [[Drinfeld center]]

## References

Early occurrence of the definition of the center of an additive category: 

* [[Pierre Gabriel]], section 5.d of: *[[Des catégories abéliennes]]*, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __90__ (1962) 323-448 &lbrack;[numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0)&rbrack;


[[!redirects center of an abelian category]]
