
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Idea

A _monad with arities_ is a [[monad]] that admits a generalized [[nerve]] construction. This allows us to view its [[algebra over a monad|algebras]] as [[presheaves]]-with-[[properties]] in a canonical way.

This generalized nerve construction also generalizes the construction of the [[syntactic category]] of a [[Lawvere theory]].

##Definition##

Let $\mathcal{C}$ be a [[category]], and $i_A : \mathcal{A} \subset \mathcal{C}$ a [[subcategory]]. As explained at [[dense functor]], for any [[object]] $X$ of $\mathcal{C}$, there is a canonical [[cocone]] over the [[forgetful functor]] $(\mathcal{A} \downarrow X) \to \mathcal{C}$, which we call the **canonical $\mathcal{A}$-cocone at $X$**. The subcategory $\mathcal{A} \subset \mathcal{C}$ is called _dense_ if this cocone is [[colimit|colimiting]] for every object $X$ of $C$.

 If $\mathcal{C}$ be a category and $i_A : \mathcal{A} \subset \mathcal{C}$ is a dense subcategory, then the **$\mathcal{A}$-[[nerve|nerve functor]]** is given by

\[ 
  \begin{aligned} 
     \nu_{\mathcal{A}} : \mathcal{C} 
       &\to [\mathcal{A}^{op}, \mathrm{Set}] 
     \\
     X &\mapsto \mathcal{C}(i_A, X)
   \end{aligned} 
 \,.
\]

A [[monad]] $(T,\mu,\eta)$ on $\mathcal{C}$ is said to **have arities $\mathcal{A}$** if $\nu_{\mathcal{A}} \circ T$ sends canonical $\mathcal{A}$-cocones to [[colimit|colimiting cocones]].

##Nerve Theorem##
 {#NerveTheorem}

The nerve theorem consists of two statements:

**I.** If $\mathcal{A}$ is dense in $\mathcal{C}$ and if $T$ is a monad with arities $\mathcal{A}$ on $\mathcal{C}$, then $\mathcal{C}^T$ has a dense subcategory $\Theta_T$ given by the [[free functor|free]] $T$-[[algebra over a monad|algebras]] on objects of $\mathcal{A}$.

By definition of density, this means that the nerve functor $\nu_{\Theta_T} : \mathcal{C}^T \to [\Theta_T^{op}, \mathrm{Set}]$ is [[full and faithful functor|full and faithful]]. This allows us to view $T$-algebras as [[presheaves]] (on $\Theta_T$) with a certain [[stuff, structure, property|property]]. The second part of the nerve theorem tells us what this property is.

**II.** Let $j: \mathcal{A} \to \Theta_T$ be the restricted free algebra functor. A presheaf $P : \Theta_T^{op} \to \mathrm{Set}$ is in the essential image of $\nu_{\Theta}$ if and only if the restriction along $j$,
\[ P\circ j : A^{op} \to \Set \]
 is in the essential image of $\nu_A$.

The proof of the nerve theorem, following [BMW](#BMW), is fairly straightforward.  Consider the adjunction $j_! : [\mathcal{A}^{op},Set] \rightleftarrows [\Theta_T^{op},Set] : j^*$ given by restriction and [[left Kan extension]].  The assumption that $T$ has arities $\mathcal{A}$ can be reformulated to say that the nerve $\nu_{\mathcal{A}} : \mathcal{C} \to  [\mathcal{A}^{op},Set]$ is a strong [[monad morphism]] from $T$ to $j^* j_!$, i.e. there is a coherent isomorphism $\nu_{\mathcal{A}} T \cong j^* j_! \nu_{\mathcal{A}}$.  Since $\nu_{\mathcal{A}}$ is fully faithful, this means that if we identify $\mathcal{C}$ with the image of $\nu_{\mathcal{A}}$, then the monad $T$ gets identified with $j^* j_!$.  But the adjunction $j_! \dashv j^*$ is also monadic (since $j$ is bijective on objects), so the category of $T$-algebras gets identified with the full subcategory of $j^* j_!$-algebras, i.e. presheaves on $\Theta_T$, whose underlying presheaf on $\mathcal{A}$ is in the image of $\nu_{\mathcal{A}}$.  This is exactly the two statements of the nerve theorem.

##Examples##

* Every [[p.r.a. monad]] has arities.  In particular, therefore, every [[polynomial monad]] has arities.

* The free [[groupoid]] monad on the category of [[directed graphs]] with [[involution]] has arities, although it is not p.r.a.

See [BMW](#BMW) for more.

## Related pages

* A monad with arities is equivalently an internal [[monad]] in the [[2-category]] of [[categories with arities]].

##References##

See the discussion at 

* [[Tom Leinster]], _How I learned to love the nerve construction_ (2008) ([blog](http://golem.ph.utexas.edu/category/2008/01/mark_weber_on_nerves_of_catego.html))

The associated paper is 

* [[Mark Weber]], _Familial 2-functors and parametric right adjoints_ (2007) ([tac](http://www.tac.mta.ca/tac/volumes/18/22/18-22abs.html))

These ideas are clarified and expanded on in 

* [[Paul-André Melliès]]. _Segal condition meets computational effects._ (2010, 25th Annual IEEE Symposium on Logic in Computer Science).

* {#BMW} [[Clemens Berger]], [[Paul-André Melliès]], [[Mark Weber]], _Monads with Arities and their Associated Theories_ (2011) ([arXiv:1101.3064](http://arxiv.org/abs/1101.3064))
 

[[!redirects monads with arities]]
