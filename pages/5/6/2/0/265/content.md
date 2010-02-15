#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[category with weak equivalences]] $C$ serves as a presentation for an [[(∞,1)-category]] $\mathbf{C}$. Accordingly, a [[functor]] $F : C \to D$ should induce an [[(∞,1)-functor]] between the corresponding [[(∞,1)-categories]] $\mathbf{C} \to \mathbf{D}$. From the [[nPOV]], this is a **derived functor**.

If $F$ is a [[homotopical functor]] in that it respects the weak equivalences in $C$ and $D$, then by the universal property of [[simplicial localization]] it extends to a functor of [[(∞,1)-category|(∞,1)-categories]] and this is the corresponding _derived functor_ .

However, typically functors of interest do not respect weak equivalences and hence do not uniquely or even naturally give rise to an [[(∞,1)-functor]]. In general, they contains too little information to accomplish this. Notably, to objects $x, y \in C$ that are [[homotopy equivalence|equivalent]] in $\mathbf{C}$ but not [[isomorphism|isomorphic]] in $C$, the functor will in general not assign objects $F(x)$ and $F(y)$ that are equivalent in $\mathbf{D}$, as an [[(∞,1)-functor]] would. So it matters on which representatives of a $\mathbf{C}$-equivalence class of objects the functor $F$ is applied. 

Remembering that by Dwyer-Kan [[simplicial localization]] the morphisms in $\mathbf{C}$ and $\mathbf{D}$ are zig-zags of morphisms in $C$ and $D$, a very general notion of derived functor therefore takes a derived functor of $F$ to be a functor $\mathbb{D}F : \mathbf{C} \to \mathbf{D}$ to be a functor induced from the universal property of the localization by a functor of the form $F \circ Q : C \to D$, where $Q : C \to C$ is an endofunctor which is naturally connected to the identity by a zig-zag of weak equivalences. 

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

> ...please add some mentioning of more exotic examples here...

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

+--{: .query}
[[Mike Shulman|Mike]]: I personally hold the opinion that it is better to _define_ a derived functor to be the result of applying $F$ to a fibrant and/or cofibrant replacement of some sort.  I have come to view the fact that sometimes (when a fibrant _or_ cofibrant replacement alone suffices) this happens to be a left or right Kan extension as merely an accident, which is of little practical or conceptual use.  I think this is borne out by the fact that these Kan extension are not "pointwise," that they are basically the _only_  non-pointwise Kan extensions that I have seen arise anywhere in mathematics, and that many of the nice properties of Kan extensions apply only to pointwise ones (in fact, Kelly _defines_ Kan extension to refer only to pointwise ones).  But I would be very interested to hear alternate points of view.

[[Zoran Skoda]]: This is very interesting; maybe it suggests that one needs to choose sort of factorization system or something, so that still thing has some universal property: among functors of special kind with respect to the factorization system of a sort. I would like to hear your examples and insight in more detail. Surely in homological 
algebra osmetimes one does not have sufficiently many projective or injectives so there is an appeal in something universal. Most interestingly, satelites make sense sometimes when derived functors don't but still satelites in very general (nonabelian) context are themselves still sort of Kan extensions. I do not understand why total derived functor would have kind of universality as one step in forming it has. 

[[Tim Porter|Tim]]: The 'homotopy Kan extensions' are weighted Kan extensions and can handle quite a few of the 'derived functor' cases.  As they are enriched versions they seem to generalise the pointwise case, yet manage to do more. Perhaps that neaeds airing as an idea.  I suspect it does not handle all the derived functors we might want.

[[Mike Shulman|Mike]]: It's not so much that I have lots of examples of derived functors that are not Kan extensions, as that I think the fact that they are Kan extensions is irrelevant and misleading.  Can you point to any situation in which the fact that a derived functor is a Kan extension is important or useful?  In my experience whenever you want to prove something about a derived functor, you need to invoke its construction as a composite of the original functor with fibrant and/or cofibrant replacement.

(The observation that sometimes the functor you are taking a derived functor of is itself a "Kan extension" _functor_ (that is, a functor on a diagram category which takes a diagram to its Kan extension), so that the derived functor is a "homotopy Kan extension" _functor_, is a completely different question from whether the derived functor is _a_ Kan extension along the localization functor.  But maybe I misunderstood what Tim said.)

That said, here is a general situation in which you get derived functors that are not necessarily Kan extensions.  Let $V$ be a [[monoidal model category]] and $M,N$ be $V$-[[enriched model category|model categories]].  Then _any_ $V$-enriched functor $F:M\to N$, whether or not it has an adjoint or preserves cofibrations or fibrations, has a "derived functor" $Ho M \to Ho N$ represented by the composite $F \circ Q R$, where $Q R$ is a cofibrant _and_ fibrant replacement functor on $M$.  This is because in a $V$-model category, weak equivalences between fibrant-cofibrant ("bifibrant"?) objects are necessarily "$V$-equivalences," which are preserved by all $V$-functors.  (When $V$ is $Top$, $sSet$, or $Ch$ then $V$-equivalences are homotopy equivalences, simplicial homotopy equivalences, or chain homotopy equivalences, respectively.)

Such "derived functors" are not Kan extensions because $Q R$ does not come equipped with a single weak equivalence to or from the identity functor, but rather a zigzag $Q R \to R \leftarrow Id$ (or $Q R \leftarrow Q \to Id$).  If you generalize the definition of "derived functor" to allow replacement by such zigzags, there is no longer any universal property or uniqueness, since left and right derived functors are now both examples and they don't need to be the same.  But for that very reason, this generalization can be important in proving commutation relations between left and right derived functors.  See [my paper](http://arxiv.org/abs/math/0610194), sections 4 and 17-18, and [May-Sigurdsson](http://arxiv.org/abs/math/0411656) for some applications (in more classical language).

I don't know what a "satellite" is.

_Zoran_ Cartan-Eilenberg book has the whole chapter on satelites. If you have derivd functors then they can be expressed via satelites; but satelites may exist even when the functor is not half exact. It is also instructive to look at satelites in nonabelian setup, for eample the small note by Janelidze, from 1970-s reprinted on the arXiv.

[[Mike Shulman|Mike]]: Thanks!  Looking at the definition in Cartan-Eilenberg, it seems that the left satellites of an additive functor $F:A\to B$ are the homology of $F$ applied to a projective resolution, and the right satellites are the homology of $F$ applied to an injective resolution.  These make sense and are homotopy invariant for any additive functor $F$, and apparently if $F$ is 'half exact' (preserves exactness in the middle of short exact sequences) then its left and right satellites fit together into a bi-infinite long exact sequence, generalizing the more familiar cases of left and right derived functors.

Now there are two (well, more than that, but two that seem most relevant) model structures on the category of chain complexes: the projective one, where projective resolutions are cofibrant and every object is fibrant, and the injective one, which is dual (although harder to construct, because of the non-duality between cofibrant generation and fibrant generation).  Thus, it seems that the left (right) satellites are the homology of the generalized derived functor with respect to the projective (injective) model structure, which turns out to actually be a left (right) derived functor since every object is fibrant (cofibrant).  Does that make sense?

_Toby_:  Excuse me, but maybe this discussion could use a link: [[satellite]].
=--


#### Remarks

* By the universal property of $Ho_C$, functors $Ho_C \to D$ are equivalent to functors $C\to D$ which take weak equivalences to isomorphisms.  If $F$ itself takes weak equivalences to isomorphisms, then its left and right derived functors are both (isomorphic to) its unique extension along $p$.  In general, however, $L F$ and $R F$ are not extensions of $F$ even up to isomorphism.


* The Kan extensions involved here are _not_ "pointwise" ones, meaning that they are not computed by limits and colimits objectwise.  This means that they lack many of the good properties of ordinary Kan extensions.  

* In practice, derived functors are usually computed using fibrant and cofibrant replacements (see the entries on [[homotopy theory]] and [[model category]]) or, more generally, [[deformation retract of a homotopical category|deformation retracts]].

* The connection to the 
more elementary notion of [[derived functor on a derived category]] in [[homological algebra]] that is as follows. A functor $F:A \to B$ between [[abelian category|abelian categories]] induces a functor $Ch(F):Ch(A) \to Ch(B)$ between [[category of chain complexes|categories of chain complexes]], each of which can be equipped with the class of [[quasi-isomorphism|quasi-isomorphisms]] as weak equivalences.  We obtain the usual derived functors of $F$ by taking the derived functor of $Ch(F)$ in the above sense, evaluating it at an object of $A$ regarded as a chain complex concentrated in degree zero, and then taking the [[homology]] of the resulting chain complex in $B$.






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



## Examples

* The (total) derived functor of the [[limit]] functor is the [[homotopy limit]].  The functors $lim^{(i)}$ often called the derived functors of Lim are then given by the (co)homology of that 'total' form.  


[[!redirects derived functors]]