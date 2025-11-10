
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#

* table of contents
{:toc}

## Idea 

In traditional [[differential geometry]] a [[smooth manifold]] may be thought of as a "locally linear space": a space that is locally isomorphic to a 
[[vector space]] $\simeq \mathbb{R}^n$.

In the broader context of [[synthetic differential geometry]]  there may exist [[spaces]] --- in a [[smooth topos]] $\mathcal{T}$ with line object $R$ ---
considerably more general than manifolds. While for all of them  there is a notion of [[tangent bundle]] $T X : = X^D$ (sometimes called a _[[synthetic tangent bundle]]_, with $D$ the [[infinitesimal space|infinitesimal interval]]), not all such tangent bundles 
necessarily have $R$-linear fibers! 

A _microlinear space_  is essentially an object $X$ in a [[smooth topos]],  such that its [[tangent bundle]] does have $R$-linear fibers.

In fact the definition is a bit stronger than that, but the main point in practice of microlinearity is that the linearity of the fibers of the tangent bundle allows to apply most of the familiar constructions in [[differential geometry]] to these spaces.

## Definition 

+-- {: .num_defn}
###### Definition
**(microlinear space)**


Let $\mathcal{T}$ be a [[smooth topos]] with line object $R$.  An object $X \in \mathcal{T}$ is a __microlinear space__ if for each [[diagram]] $\Delta : J \to \mathcal{T}$ of [[infinitesimal spaces]] in $\mathcal{T}$ and for each [[colimit|cocone]] $\Delta \to \Delta_c$ under it such that homming into $R$ produces a [[limit]] diagram , $R^\Delta_c \simeq \lim_{j \in J} R^{\Delta_j}$, also homming into $X$ produces a limit diagram: $X^\Delta_c \simeq \lim_{j \in J} X^{\Delta_j}$.

=--


The main point of this definition is the following property.

+-- {: .num_prop}
###### Proposition
**(fiberwise linearity of tangent bundle)**

For every microlinear space $X$, the [[tangent bundle]] $X^D \to X$ has a natural fiberwise $R$-[[module]]-structure.

=--

+-- {: .proof}
###### Construction and Proof

We describe first the addition of tangent vectors, then the $R$-action on them and then prove that this is a [[module]]-structure.

* **Addition** With $D \coloneqq \{\epsilon \in R| \epsilon^2 = 0 \}$ the [[infinitesimal space|infinitesimal interval]] and  $D(2) \coloneqq \big\{(\epsilon_1, \epsilon_2) \in R \times R | \epsilon_i \epsilon_j = 0\big\}$ we have a [[cocone]]
  
  $$
    \array{
      D(2) &\leftarrow& D
      \\
      \uparrow && \uparrow
      \\
      D &\leftarrow& {*}
    }
  $$

  such that  

  $$
    \array{
      R^{D(2)} &\to & R^D
      \\
      \downarrow && \downarrow
      \\
      R^D &\to& R
    }
  $$

  is a [[limit]] [[cone]], by the [[Kock-Lawvere axiom]] satisfied in the [[smooth topos]] $\mathcal{T}$. Since $X$ is microlinear, also the canonical map
  
  $$
    r \;\colon\; X^{D(2)} \to X^D \times_X X^D
  $$

  is an [[isomorphism]]. With $\Id \times Id \colon D \to D(2)$ the [[diagonal map]], we then define the fiberwise [[addition]] $X^D \times_X X^D \to X^D$ in  the [[tangent bundle]] $X^D$ to be given by the map
  
  $$  
    + \;\colon\; X^D \times_X X^D \stackrel{r^{-1}}{\to} X^{D(2)} \stackrel{X^{Id \times Id}}{\to}
    X^D
    \,.
  $$

  On elements, this sends a pair $v_1, v_2 \in X^D$ in the same fiber to the element $v_1 + v_2$ of $X^D$ given by the map $(v_1 + v_2) \;\colon\; d \mapsto r^{-1}(v_1,v_2)(d,d)$.

*  **Multiplication** $ \cdot \;\colon\; R \times X^D \to X^D$ is defined componentwise by

   $(\alpha \cdot v) \;\colon\; d \mapsto v (\alpha \cdot d)$.
  
One checks that this is indeed [[unitality|unital]], [[associativity|associative]] and [[distributivity|distributive]]. ...

=--


## Examples 
  
A large class of examples is implied by the following proposition.

+-- {: .num_prop}
###### Proposition
**(closedness of the collection of microlinear spaces)**

In every [[smooth topos]] $(\mathcal{T},R)$ we have:

1. The standard line $R$ is microlinear.

1. The collection of microlinear spaces is closed under [[limits]] in $\mathcal{T}$:

   for $X = \lim_i X_i$ a [[limit]] of microlinear spaces $X_i$, also $X$ is microlinear.
  
1. [[mapping space|Mapping spaces]] into microlinear spaces are microlinear: for $X$ any microlinear space and $\Sigma$ any space, also the [[internal hom]] $X^\Sigma$ is microlinear.

=--


+-- {: .proof}
###### Proof

This is obvious from the standard properties
of [[limits]] and the fact that the [[internal hom]]-functor
$(-)^Y \colon \mathcal{T} \to \mathcal{T}$ preserves limits.
(See [[limits and colimits by example]] if you don't find it obvious.)

1. by definition

1. Let $\Delta$ be the tip of a cocone $\Delta_j$ of infinitesimal spaces such 
   that $\lim_j R^{\Delta_j} = R^\Delta$. Then 
   
   $$
     \begin{aligned}
       X^{\Delta} 
        &= (\lim_i X_i)^\Delta 
        \\
        &\simeq \lim_i X_i^{\Delta}
        \\
        & \simeq \lim_i \lim_j X_i^{\Delta_j} 
        \\
        & \simeq \lim_j \lim_i X_i^{\Delta_j}
        \\
        & \simeq \lim_j X^{\Delta_j}
      \end{aligned}
   $$
  
1. with $\Delta$ as above we have (writing $[A,B]$ for the [[internal hom]] otherwise
   equivalently denoted $B^A$)

   $$
     \begin{aligned}
       [\Delta, [\Sigma, X]] & \simeq [\Delta \times \Sigma, X]  
       \\ 
       & \simeq [\Sigma, [\Delta, X]] 
       \\
       & \simeq [\Sigma, \lim_j [\Delta_j, X]]
       \\
       & \simeq \lim_j [\Sigma, [\Delta_j, X]]
       \\
       & \simeq  \lim_j [\Delta_j, [\Sigma, X]]
     \end{aligned}
   $$

=--

+-- {: .num_prop}
###### Proposition
**(microlinear loci)**

Let $\mathcal{F}$, $\mathcal{G}, \mathcal{Z}, \mathcal{B}$ be the [[smooth toposes]] of the same name that are discussed in detail in [[Models for Smooth Infinitesimal Analysis|MSIA, capter III]]. These are constructed there as [[category of sheaves|categories of sheaves]] on a [[subcategory]] of the category $\mathbb{L} = (C^\infty Ring^{fin})$ of [[smooth loci]].

All [[representable functor|representable objects]] in these [[smooth toposes]] are microlinear. 

=--

+-- {: .proof}
###### Proof

For $\mathcal{F}$ and $\mathcal{G}$ this is the statement of [[Models for Smooth Infinitesimal Analysis|MSIA, chapter V, section 7.1]]. 

For $\mathcal{Z}$ and $\mathcal{B}$ the argument is similarly easy:

These are categories of sheaves on the full category $\mathbb{L} = (C^\infty Ring^{fin})^{op}$.  The line object $R$ is representable in each case, $R = \ell C^\infty(\mathbb{R})$.  Every object in $\mathbb{L}$ is a limit (not necessarily finite) over copies of $R$ in $\mathbb{L}$. Accordingly, every object $\ell A$ of $\mathbb{L}$ satisfies the microlinearity axioms in $\mathbb{L}$ in that for each cocone $\Delta \to \Delta_c : J \to \mathbb{L}$ of [[infinitesimal objects]] such that $R^{\Delta_c} \simeq \lim_{j \in J} R^{\Delta_j}$ we also have $(\ell A)^{\Delta_c} \simeq \lim_{j \in J} (\ell A)^{\Delta_j}$.  Now, the [[Yoneda embedding]] $Y : \mathbb{L} \to PSh(C)$ preserves limits and exponentials.  Since the [[Grothendieck topology]] in question is [[subcanonical coverage|subcanonical]], $Y((\ell A)^{\Delta_j})$ is in $Sh(C)$ and hence is the exponential object $Y(\ell A)^{Y \Delta_j}$ there.  Finally, the _finite_ limit over $J$ is preserved by the reflection $PSh(C) \to Sh(C)$ (sheafification, which acts trivially on our representables), so $Y(\ell A)^{\Delta_c} \simeq \lim_{j \in J}  Y(\ell A)^{Y(\Delta_j)}$ and hence all $Y(\ell A)$ are microlinear in $\mathcal{Z}$ and $\mathcal{B}$.

=--


## References

The notion of microlinear space in the above fashion is due to

* F. Bergeron, *Objet infinitésimal en géométrie différentielle synthétique*, Exposé 10 in Rapport de Recherches du Dépt. de Math. et de Stat. 80-11 and 80-12, Université de Montréal (1980)

and was studied further under the name _strong infinitesimal linearity_

* [[Anders Kock]], [[René Lavendhomme]]: *Strong infinitesimal linearity, with applications to strong difference and affine connections*, [[Cahiers]] de topologie et géométrie différentielle catégoriques, tome 25, no 3 (1984) 311-324 &lbrack;[numdam:CTGDC_1984__25_3_311_0](http://www.numdam.org/item?id=CTGDC_1984__25_3_311_0)&rbrack;

This is similar to but stronger than the earlier "condition (E)" given in

* Demazure (1970)

which apparently was also called "infinitesimal linearity" (without the "strong").

Spaces satisfying this condition were called _infinitesimally linear spaces_, for instance in the original version of:

*  {#Kock81} [[Anders Kock]]: _Synthetic Differential Geometry_, Cambridge University Press (1981, 2006) &lbrack;[pdf](http://home.imf.au.dk/kock/sdg99.pdf), [doi:10.1017/CBO9780511550812](https://doi.org/10.1017/CBO9780511550812)&rbrack;

The 2006 revision of this book contains in its appendix D the definition of microlinearity as above.

A comprehensive discussion of microlinearity is in chapter V, section 1 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_, Springer (1991) &lbrack;[doi:10.1007/978-1-4757-4143-8](https://link.springer.com/book/10.1007/978-1-4757-4143-8)&rbrack;


[[!redirects microlinear spaces]]

[[!redirects microlinearity]]
