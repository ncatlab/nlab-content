
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[category with weak equivalences]] $C$ serves as a presentation for an [[(∞,1)-category]] $\mathbf{C}$. Accordingly, a [[functor]] $F : C \to D$ should induce an [[(∞,1)-functor]] between the corresponding [[(∞,1)-categories]] $\mathbf{C} \to \mathbf{D}$. From the [[nPOV]], this is a **derived functor**.

If $F$ is a [[homotopical functor]] in that it respects the weak equivalences in $C$ and $D$, then by the universal property of [[simplicial localization]] it extends to a functor of [[(∞,1)-category|(∞,1)-categories]] and this is the corresponding _derived functor_ .

However, typically functors of interest do not respect weak equivalences and hence do not uniquely or even naturally give rise to an [[(∞,1)-functor]]. In general, they contains too little information to accomplish this. Notably, to objects $x, y \in C$ that are [[homotopy equivalence|equivalent]] in $\mathbf{C}$ but not [[isomorphism|isomorphic]] in $C$, the functor will in general not assign objects $F(x)$ and $F(y)$ that are equivalent in $\mathbf{D}$, as an [[(∞,1)-functor]] would. So it matters on which representatives of a $\mathbf{C}$-equivalence class of objects the functor $F$ is applied. 

Remembering that by Dwyer-Kan [[simplicial localization]] the morphisms in $\mathbf{C}$ and $\mathbf{D}$ are zig-zags of morphisms in $C$ and $D$, a very general notion of derived functor therefore takes a derived functor of $F$ to be a functor $\mathbb{D}F : \mathbf{C} \to \mathbf{D}$ induced from the universal property of the localization by a functor of the form $F \circ Q : C \to D$, where $Q : C \to C$ is an endofunctor which is naturally connected to the identity by a zig-zag of weak equivalences. 

$$
  X \stackrel{\simeq}{\leftarrow}
  X_1 
   \stackrel{\simeq}{\to}
  X_2
  \cdots
  \stackrel{\simeq}{\leftarrow}
  Q X
  \,.
$$

Here if this zig-zag consists just of one morphism to the left one would speak of a **left derived functor**. If it consistis of just one morphism to the right, one would speak of a **right derived functor**. In general, it is just a derived functor.

In highly structured situation where $C$ and $D$ are equipped not just with weak equivalences but with the full structure of a [[model category]] and if $F$ is a left or right [[Quillen adjunction|Quillen functor]] with respect to these model structures, there are accordingly more structured ways to solve this problem:


the **left derived functor** $\mathbb{L}F : \mathbf{C} \to \mathbf{D}$ of a left Quillen functor $F : C \to D$ is obtained by applying $F$ to _cofibrant_ objects of $C$. Similarly a **right derived functor** $\mathbb{R}G : \mathbf{D} \to \mathbf{C}$ of a right Quillen functor $G : D \to C$ is obtained by applying $G$ to _fibrant_ objects. 

Recalling that the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by a [[simplicial model category]] $C$ may be identified with the full [[sSet]]-[[subcategory]] $C^\circ$ of fibrant-cofibrant objects, this may be understood as ensuring that the derived functor indeed respects the $(\infty,1)$-categorical structure. More precisely, for

$$
  (F \dashv G) : C \stackrel{\leftarrow}{\to} D
$$

an [[sSet]]-[[enriched category theory|enriched]] [[Quillen adjunction]] between [[simplicial model categories]], combining $F$ and $G$ with cofibrant-fibrant replacement induces a pair of [[adjoint (∞,1)-functor]]s

$$
  \mathbb{L}F : \mathbf{C} \stackrel{\leftarrow}{\to} \mathbf{D}
  : 
  \mathbb{R}G
$$

between [[quasi-category|quasi-categories]] $\mathbf{C} = N(C^\circ)$, $D = N(D^\circ)$, where $N$ is the [[homotopy coherent nerve]] functor. 

Often a simplified version of this situation is considered, where instead of the [[(∞,1)-categories]] $\mathbf{C}$ and $\mathbf{D}$ only [[homotopy category of an (∞,1)-category|their homotopy categories]] are remembered, equivalently the [[homotopy category|homotopy categories]] of $C$ and $D$. The above [[adjoint (∞,1)-functor]]s restrict to functors

$$
  L F : Ho(C) \stackrel{\leftarrow}{\to} Ho(D)
  : 
  R G
$$

on [[homotopy category|homotopy categories]], and often its is these functors that are called (total) **derived functor**s in the literature

More generally, derived functors in this sense may be considered in situations where less than the above extra structure is available (no [[model category]] structure or not [[Quillen adjunction]]).

If one forgets the [[nPOV]] and that a [[category with weak equivalences]] should be regarded as presentation for an [[(∞,1)-category]], then it might seem as if all one wants when deriving a [[homotopical functor]] $f : C \to D$ is to extend it to a diagram

$$
  \array{
    C &\stackrel{F}{\to}& D
    \\
    \downarrow^{\mathrlap{Q_C}} &(?)& \downarrow^{\mathrlap{Q_D}}
    \\
    Ho(C) &\to& Ho(D)
  }
  \,,
$$

where $Q_C : C \to Ho(C)$ is the universal morphism characterizing the [[homotopy category]] and similarly for $Q_D$.

There is a general method of ordinary [[category theory]] to solve such problems universally: one may take $Ho(C) \to Ho(D)$ to be either the left or right [[Kan extension]] of $Q_d \circ F$ along $Q_C$.

This is often in the literature given as the _definition_ of, respectively , total left and right derived functors. Unfortunately, it is not clear how this definition by Kan extension relates to what should be the right [[(∞,1)-category]] theory picture. Moreover, the examples of derived functors that play any practical role are effectively always constructed instead rather by combining $F$ with cofibrant/fibrant or similar replacement functors. It then also happens that the functors so obtained are left or right Kan extensions.


## Definition

We first give the [[decategorification|decatergorified]] definition of total derived functors on [[homotopy category|homotopy categories]] in 

* [As functors on homotopy categories](#OnHomotopyCat)

and then the [[(∞,1)-category]]-version in

* [Af functors on (∞,1)-categories](#OnInftyCats).



### As functors on homotopy categories {#OnHomotopyCat}



For $Core(C) \hookrightarrow W \hookrightarrow C$ a [[category with weak equivalences]], then for $F : C \to D$ any functor, the __left derived functor__ $L F$ of $F$ is the _right_ [[Kan extension]] of $F$ along the projection $p : C \to Ho_C$ to the [[homotopy category]]

$$
 \array{
   C &&\stackrel{F}{\to}&& D
   \\
   \downarrow^p &\Downarrow& \nearrow_{L F}
   \\
   Ho_C
 }
$$

(if it exists).  Dually, the __right derived functor__ $R F$ of $F$ is its _left_ Kan extension along $p$.  Note the reversal of handedness; this is unfortunate but unavoidable.

More generally, if $D$ is itself a category with weak equivalences, then by derived functors of $F$ we often mean derived functors of the composite

$$ C \stackrel{F}{\to} D \to Ho_D $$



+-- {: .un_remark}
###### Remarks

* By the universal property of $Ho_C$, functors $Ho_C \to D$ are equivalent to functors $C\to D$ which take weak equivalences to isomorphisms.  If $F$ itself takes weak equivalences to isomorphisms, then its left and right derived functors are both (isomorphic to) its unique extension along $p$.  In general, however, $L F$ and $R F$ are not extensions of $F$ even up to isomorphism.


* The Kan extensions involved here are _not_ "pointwise" ones, meaning that they are not computed by limits and colimits objectwise.  This means that they lack many of the good properties of ordinary Kan extensions.  

* In practice, derived functors are usually computed using fibrant and cofibrant [[resolution]] replacements (see the entries on [[homotopy theory]] and [[model category]]) or, more generally, [[deformation retract of a homotopical category|deformation retracts]].

=--




### As functors on $(\infty,1)$-categories {#OnInftyCats}

+-- {: .un_prop}
###### Proposition

Let $C$ and $D$ by [[simplicial model category|simplicial model categories]] and let

$$
  (F \dashv G) : C \stackrel{\overset{G}{\leftarrow}}{\overset{F}{\to}} D
$$

be an [[sSet]]-[[enriched functor|enriched]] [[Quillen adjunction]]. Then there is an [[adjoint (∞,1)-functor|(∞,1)-adjunction]]

$$
  (\mathbb{L}F \dashv \mathbb{R}G) : N(C^\circ) \stackrel{\overset{\mathbb{R} G}{\leftarrow}}{\overset{\mathbb{L}F}{\to}} N(D^\circ)
$$

between [[quasi-categories]] $N(C^\circ)$ and $N(D^\circ)$ otained as the [[homotopy coherent nerve]]s of the full [[sSet]]-[[subcategories]] of fibrant-cofibrant objects. Their image on the [[homotopy category|homotopy categories]] produces the notion of total derived functor between homotopy categories discussed above

$$
  (L F \dashv R G) : Ho(C) \stackrel{\overset{R G}{\leftarrow}}{\overset{L F}{\to}} Ho(D)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is prop. 5.2.4.6 and remark 5.2.4.7 in [[Higher Topos Theory|HTT]].

=--

### In homological algebra {#InHomologicalAlgebra}

Often and traditionally, the concept of derived functors is considered in [[homological algebra]] exclusively in the context of [[categories of chain complexes]] $Ch_\bullet(\mathcal{A})$ in an [[abelian category]] $\mathcal{A}$.

By taking [[quasi-isomorphism]]s as weak equivalences, $Ch_\bullet(\mathcal{A})$ is naturally a [[category with weak equivalences]]. In much of the literature on homological algebra the refinement of this structure to an injective [[model structure on chain complexes]] is implicit. For instance injective [[resolution]] of chain complexes is nothing but fibrant replacement in this model structure.


Now any ordinary functor $F:\mathcal{A} \to \mathcal{B}$ between [[abelian categories]] induces a functor $Ch_\bullet(F):Ch_\bullet(\mathcal{A}) \to Ch_\bullet(\mathcal{B})$ between [[category of chain complexes|categories of chain complexes]].

Suppose $F$ is a [[left exact functor]], then $Ch_\bullet(F)$ is right Quillen. What in the homological algebra literature is called the derived functor 

$$
  R^p F : \mathcal{A} \to \mathcal{A}
$$

is the composite

$$
  \mathcal{A} \stackrel{\mathbf{B}^p (-)}{\hookrightarrow} Ch_\bullet(\mathcal{A})
  \stackrel{\mathbb{R} Ch_\bullet(F)}{\to}
  Ch_\bullet(\mathcal{B})
  \stackrel{H^0(-)}{\to}
  \mathcal{A}
  \,,
$$

where

1. the first map sends an object $A \in \mathcal{A}$ to the corresponding [[Eilenberg-MacLane object]] $\mathbf{B}^p A$: the cochain complex $A[p]$ concentrated on $A$ in degree $p$;

1. the second map is the actual derived functor $\mathbb{R}Ch_\bullet(F)$ of $Ch_\bullet(F)$ in the above sense, so this is itself the composite

   $$
     \mathbb{R}F : Ch_\bullet(\mathcal{A}) \stackrel{P}{\to}
      Ch_\bullet(\mathcal{A})
      \stackrel{Ch_\bullet(F)}{\to}
     Ch_\bullet(\mathcal{A})
     \,,
   $$

   where $P$ denotes a fibrant resolution functor. In the injective [[model structure on chain complexes]] this amounts to the usual [[injective]] resolutions seen in the homological algebra literature;

1. the last morphisms computes the [[cochain cohomology]] of the resulting cochain complex in degree 0.

Here the first and the last steps are considered traditionally, but are not really necessary:

1. Instead of applying the first step and resticting attention to arguments that are chain complexes concentrated in a single degree, one can evaluate $\mathbb{R} Ch_\bullet(F)$ on all chain complexes. In homological algebra one then speaks of [[hyper-derived functor]]s.

1. The last step of taking cohomology groups serves to extract invariant information. It also destroys the simple composition law of functors, though. But there is a computational tool that can be used to recover the derived functor -- in this homological sense -- of the composite of two functors from their individual derivations: this is the [[spectral sequence]] called the  <a href="http://ncatlab.org/nlab/show/spectral+sequence#GrothendieckSpectralSequence">Grothendieck spectral sequence</a>.



## Examples

* The (total) derived functor of the [[limit]] functor is the [[homotopy limit]].  The functors $lim^{(i)}$ often called the derived functors of Lim are then given by the (co)homology of that 'total' form.  

* More generally, the total derived functor of [[Kan extension]] is [[homotopy Kan extension]].

* In the context of a [[model structure on chain complexes]] of [[module]]s the left and right derived functors of the [[tensor product]] functor and the [[hom-functor]] are called [[Tor]]-functor and [[Ext-functor]], respectively.

[[!redirects derived functors]]