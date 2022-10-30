
> This entry discusses the concept of derived functors in full generality. For the dedicated discussion of the traditional case see at [[derived functors in homological algebra]].

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
* table of contents
{:toc}

## Idea

A _derived functor_ is a [[functor]] in [[homotopy theory]] induced from, "derived from" or _[[presentable (infinity,1)-category|presented by]]_ an ordinary [[functor]] on a [[category with weak equivalences]].

Historically the concept first arose in the special context of [[homological algebra]] on [[categories of chain complexes]] and is often still understood by default in this special sense. The relation to the general case is discussed below in the section _[In homological algebra](#InHomologicalAlgebra)_. For a dedicated discussion of this case see the entry _[[derived functor in homological algebra]]_.


### General idea

A [[category with weak equivalences]] $C$ serves as a presentation for an [[(∞,1)-category]] $\mathbf{C}$ by [[simplicial localization]]. Accordingly, a [[functor]] $F : C \to D$ should induce an [[(∞,1)-functor]] between the corresponding [[(∞,1)-categories]] $\mathbf{C} \to \mathbf{D}$. From the [[nPOV]], this is a **derived functor**.

If $F$ is a [[homotopical functor]] in that it respects the weak equivalences in $C$ and $D$, then by the [[universal property]] of [[simplicial localization]] it extends to a functor of [[(∞,1)-category|(∞,1)-categories]] and this is the corresponding _derived functor_ .

However, typically functors of interest do not respect weak equivalences and hence do not uniquely or even naturally give rise to an [[(∞,1)-functor]]. In general, they contain too little information to accomplish this. Notably, to objects $x, y \in C$ that are [[homotopy equivalence|equivalent]] in $\mathbf{C}$ but not [[isomorphism|isomorphic]] in $C$, the functor will in general not assign objects $F(x)$ and $F(y)$ that are equivalent in $\mathbf{D}$, as an [[(∞,1)-functor]] would. So it matters on which representatives of a $\mathbf{C}$-[[equivalence class]] of objects the functor $F$ is applied. 

Remembering that by Dwyer-Kan [[simplicial localization]] the morphisms in $\mathbf{C}$ and $\mathbf{D}$ are [[zig-zags]] of morphisms in $C$ and $D$, a very general notion of derived functor therefore takes a derived functor of $F$ to be a functor $\mathbb{D}F : \mathbf{C} \to \mathbf{D}$ induced from the [[universal property]] of the localization by a functor of the form $F \circ Q : C \to D$, where $Q : C \to C$ is an [[endofunctor]] which is naturally connected to the identity by a [[zig-zag]] of [[weak equivalences]]: 

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

Here if this zig-zag consists just of one morphism to the left one would speak of a **left derived functor**. If it consists of just one morphism to the right, one would speak of a **right derived functor**. In general, it is just a derived functor.

### On model categories

In highly structured situations where $C$ and $D$ are equipped not just with weak equivalences but with the full structure of a [[model category]] and if $F$ is a left or right [[Quillen adjunction|Quillen functor]] with respect to these model structures, there are accordingly more structured ways to solve this problem:

The **left derived functor** $\mathbb{L}F : \mathbf{C} \to \mathbf{D}$ of a [[left Quillen functor]] $F : C \to D$ is obtained by applying $F$ to _[[cofibrant objects]]_ of $C$. Similarly a **right derived functor** $\mathbb{R}G : \mathbf{D} \to \mathbf{C}$ of a [[right Quillen functor]] $G : D \to C$ is obtained by applying $G$ to _[[fibrant objects]]_. 


Recalling that the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by a [[simplicial model category]] $C$ may be identified with the full [[sSet]]-[[subcategory]] $C^\circ$ of fibrant-cofibrant objects, this may be understood as ensuring that the derived functor indeed respects the $(\infty,1)$-categorical structure. More precisely, for

$$
  (F \dashv G) : C \stackrel{\leftarrow}{\to} D
$$

an [[sSet]]-[[enriched category theory|enriched]] [[Quillen adjunction]] between [[simplicial model categories]], combining $F$ and $G$ with cofibrant-fibrant replacement induces a pair of [[adjoint (∞,1)-functors]]

$$
  \mathbb{L}F 
    \colon 
    \mathbf{C} \stackrel{\longleftarrow}{\longrightarrow} \mathbf{D}
  \colon
  \mathbb{R}G
$$

between [[quasi-category|quasi-categories]] $\mathbf{C} = N(C^\circ)$, $D = N(D^\circ)$, where $N$ is the [[homotopy coherent nerve]] functor. 

Often a simplified version of this situation is considered, where instead of the [[(∞,1)-categories]] $\mathbf{C}$ and $\mathbf{D}$ only [[homotopy category of an (∞,1)-category|their homotopy categories]] are remembered, equivalently the [[homotopy category of a model category|homotopy categories of the model categories]]  $C$ and $D$. The above [[adjoint (∞,1)-functors]] restrict to functors

$$
  L F \colon 
    Ho(C) \stackrel{\longleftarrow}{\longrightarrow} Ho(D)
  \colon
  R G
$$

on [[homotopy category of a model category|homotopy categories]], and often it is these functors that are called ([[total derived functor|total]]) **derived functors** in the literature. For more on this see at _[[homotopy category of a model category]]_ the section _[derived functors](homotopy+category+of+a+model+category#DerivedFunctors)_.

More generally, derived functors in this sense may be considered in situations where less than the above extra structure is available (no [[model category]] structure or not [[Quillen adjunction]]).

### On homotopy categories

If one forgets the [[nPOV]] and that a [[category with weak equivalences]] should be regarded as presentation for an [[(∞,1)-category]], then it might seem as if all one wants when deriving a [[homotopical functor]] $f \colon C \longrightarrow D$ is to [[extension|extend]] it to a diagram

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

where $Q_C \colon C \longrightarrow Ho(C)$ is the universal morphism characterizing the [[homotopy category]] and similarly for $Q_D$.

There is a general method of ordinary [[category theory]] to solve such problems universally: one may take $Ho(C) \to Ho(D)$ to be either the left or right [[Kan extension]] of $Q_d \circ F$ along $Q_C$.

In the literature this is often takes as the _definition_ of [[total derived functor|total]] left or right derived functors. Unfortunately, it is not clear how this definition by Kan extension relates to what should be the right [[(∞,1)-category theory|(∞,1)-category theoretic]] situation above. Moreover, the examples of derived functors that play a role in practice are effectively always constructed instead rather by combining $F$ with cofibrant/fibrant or similar replacement functors. It is then but a happy byproduct that the functors so obtained also happen to be left or right Kan extensions.


## Definition

We first give the [[decategorification|decategorified]] definition of total derived functors on [[homotopy category|homotopy categories]] in 

* [As functors on homotopy categories](#OnHomotopyCat)

and then the [[(∞,1)-category]]-version in

* [As functors on (∞,1)-categories](#OnInftyCats).

The special case of derived functors in the context of [[homological algebra]] is discussed from this general perspective in 

* [In homological algebra](#InHomologicalAlgebra).

A dedicated discussion of this case is at [[derived functors in homological algebra]].


### As functors on homotopy categories 
 {#OnHomotopyCat}


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


+-- {: .num_remark}
###### Remark

By the universal property of $Ho_C$, functors $Ho_C \to D$ are equivalent to functors $C\to D$ which take weak equivalences to isomorphisms.  If $F$ itself takes weak equivalences to isomorphisms, then its left and right derived functors are both (isomorphic to) its unique extension along $p$.  In general, however, $L F$ and $R F$ are not extensions of $F$ even up to isomorphism.

=--

+-- {: .num_remark}
###### Remark

In practice, derived functors are usually computed using fibrant and cofibrant [[resolution]] replacements (see the entries on [[homotopy theory]] and [[model category]]) or, more generally, [[deformation retract of a homotopical category|deformation retracts]].

=--

+-- {: .num_remark}
###### Remark

If the codomain admits sufficiently many [[limits]] and [[colimits]], a [[Kan extension]] can be computed in terms of those, and that such Kan extensions are called *[pointwise](Kan%20extension#Pointwise)*.  Homotopy categories generally do not admit even small limits and colimits, and moreover the domains of the functors in question are generally large, so such a *construction* of a derived functor is not possible.

  However, when derived functors are constructed using fibrant and cofibrant replacements, as above, it turns out *a posteriori* that they are actually pointwise: they are preserved by all representable functors, and hence their individual object values have the universal property of the (generally large) limits that would have been used to compute them, even though not all limits exist in the homotopy category.  In fact, derived functors constructed in this way are actually [[absolute colimit|absolute]] Kan extensions: preserved by any functor whatsoever.

=--

### As functors on $(\infty,1)$-categories 
  {#OnInftyCats}

+-- {: .num_prop}
###### Proposition

Let $C$ and $D$ by [[simplicial model category|simplicial model categories]] and let

$$
  (F \dashv G) : C \stackrel{\overset{G}{\leftarrow}}{\underset{F}{\to}} D
$$

be an [[sSet]]-[[enriched functor|enriched]] [[Quillen adjunction]]. Then there is an [[adjoint (∞,1)-functor|(∞,1)-adjunction]]

$$
  (\mathbb{L}F \dashv \mathbb{R}G) : 
   N(C^\circ) 
    \stackrel{\overset{\mathbb{R} G}{\leftarrow}}{\underset{\mathbb{L}F}{\to}}  
    N(D^\circ)
$$

between [[quasi-categories]] $N(C^\circ)$ and $N(D^\circ)$ otained as the [[homotopy coherent nerve]]s of the full [[sSet]]-[[subcategories]] of fibrant-cofibrant objects. Their image on the [[homotopy category|homotopy categories]] produces the notion of total derived functor between homotopy categories discussed above

$$
  (L F \dashv R G) : 
  Ho(C) 
   \stackrel{\overset{R G}{\leftarrow}}{\underset{L F}{\to}} 
  Ho(D)
  \,.
$$

=--

This is prop. 5.2.4.6 and remark 5.2.4.7 in ([Lurie](#Lurie)). For more along these lines see also at _[Quillen adjunction - Associated infinity-adjunction](Quillen+adjunction#AssociatedInfinityAdjunction)_.


### In homological algebra 
 {#InHomologicalAlgebra}

Often and traditionally, the concept of derived functors is considered in [[homological algebra]] exclusively in the context of [[categories of chain complexes]] $Ch_\bullet(\mathcal{A})$ in an [[abelian category]] $\mathcal{A}$. The definitions in this case are disucssed in detail at 

* **[[derived functor in homological algebra]]**

Here put that special case a bit more into the general perspective.

By taking [[quasi-isomorphism]]s as weak equivalences, $Ch_\bullet(\mathcal{A})$ is naturally a [[category with weak equivalences]]. In much of the literature on homological algebra, the refinement of this structure to a projective or injective [[model structure on chain complexes]] is implicit.  For instance, an injective [[resolution]] of chain complexes is nothing but a fibrant replacement in the injective model structure.  Dually, a projective resolution is a cofibrant replacement in the projective model structure.  (Note, though, that hypotheses on $\mathcal{A}$ are required in order for these model structures to exist.)


Now, any ordinary [[additive functor]] $F\colon \mathcal{A} \to \mathcal{B}$ between [[abelian categories]] induces a functor $Ch_\bullet(F)\colon Ch_\bullet(\mathcal{A}) \to Ch_\bullet(\mathcal{B})$ between [[category of chain complexes|categories of chain complexes]].  We can therefore ask about derived functors of $Ch_\bullet(F)$.

Note first that $Ch_\bullet(F)$ automatically preserves [[chain homotopies]], and therefore also preserves [[chain homotopy equivalence]]s.  Since the projective (resp. injective) model structure on chain complexes has the property that weak equivalences (that is, quasi-isomorphisms) between cofibrant (resp. fibrant) objects are chain homotopy equivalences, it follows that $Ch_\bullet(F)$ automatically preserves weak equivalences between projective-cofibrant objects, and also between injective-fibrant objects.  Thus, it has a left derived functor if the projective model structure on $Ch_\bullet(\mathcal{A})$ exists, and a right derived functor if the injective model structure exists.

In the homological algebra literature, what is called the $p$th right derived functor 

$$
  R^p F \colon \mathcal{A} \to \mathcal{B}
$$

is the composite

$$
  \mathcal{A} \stackrel{\mathbf{B}^p (-)}{\hookrightarrow} Ch_\bullet(\mathcal{A})
  \stackrel{\mathbb{R} Ch_\bullet(F)}{\to}
  Ch_\bullet(\mathcal{B})
  \stackrel{H^0(-)}{\to}
  \mathcal{B}
  \,,
$$

1. The first map sends an object $A \in \mathcal{A}$ to the corresponding [[Eilenberg-MacLane object]] $\mathbf{B}^p A$: the cochain complex $A[p]$ concentrated on $A$ in degree $p$.

1. The second map is the actual right derived functor $\mathbb{R}Ch_\bullet(F)$ of $Ch_\bullet(F)$ in the sense used previously on this page.  Thus, this is itself the composite

   $$
     \mathbb{R}F : Ch_\bullet(\mathcal{A}) \stackrel{P}{\to}
      Ch_\bullet(\mathcal{A})
      \stackrel{Ch_\bullet(F)}{\to}
     Ch_\bullet(\mathcal{B})
     \,,
   $$

   where $P$ denotes a fibrant resolution functor in the injective [[model structure on chain complexes]].  Applied to an Eilenberg-MacLane object, this amounts to the usual [[injective resolutions]] seen in the homological algebra literature.

1. The last morphism computes the [[cochain cohomology]] of the resulting cochain complex in degree 0.

Of course, it is equivalent to instead regard $A$ as concentrated in degree $0$, and then take the $p$th homology group at the last step.  Left derived functors are dual, using the projective model structure.

The first and the last steps are traditionally included, but are not really necessary:

1. Instead of applying the first step and restricting attention to arguments that are chain complexes concentrated in a single degree, one can evaluate $\mathbb{R} Ch_\bullet(F)$ on all chain complexes (and then, if desired, take homology groups). In homological algebra one then speaks of [[hyper-derived functors]].

1. The last step of taking cohomology groups serves to extract invariant and computable information. It also destroys the simple composition law of functors, though. But there is a computational tool that can be used to recover the derived functor -- in this homological sense -- of the composite of two functors from their individual derivations: this is the [[spectral sequence]] called the  <a href="http://ncatlab.org/nlab/show/spectral+sequence#GrothendieckSpectralSequence">Grothendieck spectral sequence</a>.

#### Long exact sequences

Traditionally, in homological algebra, one only takes left derived functors of right exact functors, and right derived functors of left exact ones.  As we saw above, both left and right derived functors can be *defined* without these hypotheses, but it is only in the presence of these hypotheses that we obtain [[long exact sequences]].

Specifically, suppose we have a [[short exact sequence]]
$$ 0 \to A \to B \to C \to 0$$
in $\mathcal{A}$.  Assuming $\mathcal{A}$ has [[enough projectives]], we may then find [[projective resolutions]] $Q A$, $Q B$, and $Q C$ of $A$, $B$, and $C$, respectively, such that
$$ 0 \to Q A \to Q B \to Q C \to 0 $$
is a short exact sequence of chain complexes.  But since $Q C$ is projective, this short exact sequence is split, and therefore preserved by any additive functor.  Thus we have another short exact sequence
$$ 0 \to F Q A \to F Q B \to F Q C \to 0 $$
which therefore gives rise to a long exact sequence in homology:
$$ \cdots \to H_1(F Q A) \to H_1(F Q B) \to H_1(F Q C) \to H_0 (F Q A) \to H_0(F Q B) \to H_0(F Q C). $$
Of course, these homology groups are precisely the left derived functors of $F$, in the traditional homological algebra sense, applied to $A$, $B$, and $C$.

All of this works without hypothesis on $F$.  However, if $F$ is [[right exact functor|right exact]], then it preserves the exactness of the sequence
$$ Q A_1 \to Q A_0 \to A \to 0 $$
(and the analogous ones for $B$ and $C$).  This implies that $F A \cong H_0 (F Q A)$ and so on, so that the above long exact sequence actually finishes
$$ \cdots \to H_1(F Q A) \to H_1(F Q B) \to H_1(F Q C) \to F A \to F B \to F C \to 0. $$
This is how derived functors are traditionally introduced in homological algebra: as a way to continue the right half of a short exact sequence preserved by a right exact functor into a long exact sequence.  The case of left exact functors and right derived functors is dual.


## Examples

* The (total) derived functor of the [[limit]] functor is the [[homotopy limit]].  The functors $lim^{(i)}$ often called the derived functors of Lim are then given by the (co)homology of that 'total' form.  

* More generally, the total derived functor of [[Kan extension]] is [[homotopy Kan extension]].

* In the context of a [[model structure on chain complexes]] of [[module]]s the left and right derived functors of the [[tensor product]] functor and the [[hom-functor]] are called [[Tor]]-functor and [[Ext-functor]], respectively.

* A [[derived direct image]] functor computes [[abelian sheaf cohomology]]. See also _[[derived inverse image]]_.

## Functoriality

Passage to left derived functors is a [[pseudofunctor]] from a [[2-category]] of model categories, left Quillen functors, and natural transformations to [[Cat]], and similarly for right derived functors.  These can be combined into a [[double pseudofunctor]] from the [[double category]] [[double category of model categories|of model categories]] to the double category of [[quintets]] in [[Cat]], which implies that some [[mates]] are also preserved by deriving, even when they relate composites of left and right Quillen functors; see [(Shulman)](#Shulman).


## Related concepts

* [[hyper-derived functor]], [[total derived functor]]

* [[delta-functor]]

* [[adjoint  (∞,1)-functor]]

* [[homotopy limit]], [[homotopy colimit]], [[homotopy Kan extension]]

* [[derived category]]

* [[satellite]]

## References

### General

General discussion of derived functors in [[homotopy theory]] is for instance in 

* {#Adams74} [[Frank Adams]], part III, section 8 of _[[Stable homotopy and generalised homology]]_, 1974

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]],  [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories and Homotopical Categories]]_, volume 113 of Mathematical Surveys and Monographs

* [[Bruno Kahn]], [[Georges Maltsiniotis]], _[[Structures de Dérivabilité]]_

Discussion in the context of [[(∞,1)-categories]] is in section 5.2.4 of 

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_

The double-categorical functoriality is in

* {#Shulman} [[Mike Shulman]], _Comparing composites of left and right derived functors_, [NYJM](http://nyjm.albany.edu/j/2011/17-5.html)
 

### In homological algebra

An standard textbook introduction to [[derived functors in homological algebra]] is in 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_.

A systematic discussion of this case from the point of view of [[localization]] and [[homotopy theory]] is in section 13 of 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

and, similarly, in section 7 of 

* {#Schapira} [[Pierre Schapira]], _Categories and homological algebra_ (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))
 




[[!redirects derived functors]]

[[!redirects left derived functor]]
[[!redirects right derived functor]]
[[!redirects left derived functors]]
[[!redirects right derived functors]]