
Recall from the discussion at [[models for ∞-stack (∞,1)-toposes]] that [[simplicial presheaf|simplicial presheaves]] model generalized spaces, in the form of [[∞-groupoid]]s with extra structure (smooth structure, for instance, in the case of [[smooth ∞-stack]]s).

In the sense of [[space and quantity]] the [[duality|concrete dual]] notion obtained by homming into objects of the underlying site should be tought of as $(\infty,1)$-quantities.

We call a _model for $(\infty,1)$-quantities_ a category of cosimplicial copresheaves

$$
  [[C,[\Delta, Set]]]
  \,.
$$

For $C =$ [[CartSp]] those copresehaves that respect [[product]]s in $C$ are [[generalized smooth algebra]]s. By the  dual [[Dold-Kan correspondence]] cosimplicial smooth algebras are equivalent to **differential graded smooth algebras** (in non-negative degree), namely [[differential graded algebra]]s in the context of [[generalized smooth algebra]]s.


# Definition #


+-- {: .un_defn}
###### Definition (homotopical category of $(\infty,1)$-quantities)

Let $C = $ [[CartSp]]. Write 

$$
  CoSCoSh(C) \subset [C,[\Delta,Set]]
$$

for the full [[subcategory]] of [[simplicial object|cosimplicial]] [[presheaf|copresheaves]] on $C$ that respect [[product]]s. This are the [[simplicial object|cosimplicial objects]] in the category of [[generalized smooth algebra]]s.

We regard $CoSCoSh(C)$ as a [[category with weak equivalences]] by declaring a morphism to be a weak equivalence if objectwise under the dual [[Dold-Kan correspondence]] it induces a [[quasi-isomorphism]] of [[cochain complex]]es.

=--

In more detail this means that a morphism $f : A \to B$ is a weak equivalence if for all $\mathbb{R}^n \in C$ the morphism $f(U) : A(U) \to B(U)$ of cosimplicial abelian groups (using the additive structure of [[generalized smooth algebra]]s) induces under the dual normalized [[Moore complex]] a morphism $N^\bullet f(U) : N^\bullet A(U) \to N^\bullet(B(U))$ that induces an isomorphism on cochain complex cohomology.



+-- {: .un_defn}
###### Definition (quantities on an $\infty$-stack)

Recall that for $X$ a [[presheaf]] on $C$ its [[generalized smooth algebra]] is its [[dualizing object|Isbell dual]] copresheaf

$$
  C^\infty(X) : U \mapsto PSh_C(X, Y(U))
  \,,
$$ 

where $Y$ is the [[Yoneda embedding]].

This extends to a functor

$$
  C^\infty(-) : SPSh(C)  \to CoSSh(C)
$$

from simplicial presheaves to cosimplicial smooth algebras by degreewise application: for $X_\bullet \in SPSh(X)$ we have 

$$
  C^\infty(X_\bullet)^k = C^\infty(X_k)
  \,.
$$

=--


# Examples #

## Singular cohomology and differential forms ##

Given [[smooth space]] $X$ let $C^\infty(X^{\Delta_{inf}^k})$ be the [[generalized smooth algebra]] of functions on the space of infinitesimal $k$-[[simplex|simplices]] in $X$. This naturally forms a cosimplicial smooth algebra $C^\infty(X^{\Delta_{inf}^\bullet})$. The corresponding dual normalized [[Moore complex]] is the [[cochain complex]] of [[differential forms in synthetic differential geometry]].

Now let $\Pi(X)$ be the [[path infinity-groupoid]] of $X$. Then the Moore complex associated with the cosimplicial smooth algebra $C^\infty(\Pi(X)) := C^\infty(X^{\Delta^\bullet_C})$ is the one that computes **singular cohomology**.

By the deRham theorem (see section 4.3 of [[Models for Smooth Infinitesimal Analysis|SmoothMod]] for the synthetic version) the functor 

$$
  \int : C^\infty(X^{\Delta^\bullet_{inf}}) 
  \stackrel{\simeq}{\to}
  C^\infty(\Pi(X))
$$

that integrates differential forms over simplices is an isomorphism on the cohomologies of the corresponding [[Moore complex]]es, hence by the [[Dold-Kan correspondence]] is a weak equivalence of cosimplicial smooth algebras.


## Group cohomology and Chevalley-Eilenberg algebra of a Lie algebra ##

Let $G$ be a [[Lie group]] and let $\mathbf{B}G$ be its [[delooping]] regarded as a [[Kan complex]] valued [[simplicial presheaf]] (on [[Diff]] or [[CartSp]] or the like). The cosimplicial smooth algebra $C^\infty(\mathbf{B}G)$ has in degree $k$ the smooth algebra of $\mathbb{R}$-valued functions on $G^{\times_k}$. The differential of the corresponding dual [[Moore complex]] $N^\bullet(C^\infty(\mathbf{B}G))$ is the one that computes [[group cohomology]] on $G$ with coefficients in $mathbb{R}$ with the trivial module structure.

Let $g$ be the [[Lie algebra]] of $G$ and let $CE(g)$ denote the [[Chevalley-Eilenberg cochain complex]] that computes [[Lie algebra cohomology]] with coefficients in the corresponding trivial Lie algebra module.

There is a canonical cochain map

$$
  diff : N^\bullet(C^\infty(\mathbf{B}G)) 
  \stackrel{\simeq}{\to} CE^\bullet(g)
  \,,
$$

the vanEst morphism, that sends a function on $G^{\times k}$ to its differential at the identity. If $G$ is $k$-connected, this morphism is an isomorphism on degree $(n \leq k+1)$-cohomology. Hence the cosimplicial algebra $C^\infty(\mathbf{B}G)$ is weakly equivalent to that truncation to the (cosimplicial version of) the Chevalley-Eilenberg algebra.


## Lie algebra valued differential forms ##

Let $X$ be a manifold and $G$ a [[Lie group]] with [[Lie algebra]] $g$. A _flat $g$-valued differential 1-form_ $A \in \Omega^1(X,g)$ with $d A + [A \wedge A ] = 0$ is the same as

* a smooth functor 

  $$
    \Pi(X) \to \mathbf{B}G
  $$ 

  from the [[path infinity-groupoid]] to $\mathbf{B}G$ (as described at [[connection on a bundle]])

* a morphism of [[differential graded algebra]]s 

  $$
    \Omega^\bullet(X) \leftarrow CE(g)
    \,.
  $$

(The emphasis of this simple but far-reaching observation goes back to Cartan. For a detailed account of this in its wider context see for instance [LInfCon](http://arxiv.org/abs/0801.3480))

Using the above we find that the systematic relation between these two points of view is that the latter is the image under $C^\infty(-) [C^{op},[\Delta^{op}, Set]] \to [C,[\Delta, Set]]$ in that

$$
  \array{
     \Pi(X) &\stackrel{P exp(\int_{-} A)}{\to}& 
      \mathbf{B}G
     \\
     \\
     C^\infty(\Pi(X)) &\leftarrow& 
     C^\infty(\mathbf{B}G)
     \\
     {}^\simeq\uparrow^\int && {}^{diff}\downarrow
     \\
     \Omega^\bullet(X)
     &\stackrel{A}{\leftarrow}&
     CE(g)
  }
$$

[[!redirects (infinity,1) quantity]]
[[!redirects (∞,1)-quantity]]
[[!redirects (∞,1) quantity]]