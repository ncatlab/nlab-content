
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The [[model category]] structure on the [[category]] $SSet^+/S$ of [[marked simplicial set]]s over a given [[simplicial set]] $S$ is a [[presentable (infinity,1)-category|presentation]] for the [[(∞,1)-category]] of [[Cartesian fibration]]s over $S$.
Every object is cofibrant and the fibrant objects of $SSet^+/S$ are precisely the [[Cartesian fibration]]s over $S$.

Notably for $S = {*}$ this is a presentation of the [[(∞,1)-category of (∞,1)-categories]]: as a plain [[model category]] this is [[Quillen equivalence|Quillen equivalent]] to the [[model structure for quasi-categories]], but it is indeed an $sSet_{Quillen}$-[[enriched model category]] (i.e. enriched over the ordinary [[model structure on simplicial sets]] that models [[∞-groupoid]]s).


The $(\infty,1)$-categorical [[Grothendieck construction]] that exhibits the correspondence between [[Cartesian fibration]]s and [[(∞,1)-presheaf|(∞,1)-presheaves]] is in turn modeled by a [[Quillen equivalence]] between the model structure on marked simplicial over-sets and the projective [[global model structure on simplicial presheaves]].















## Marked simplicial sets



Marked simplicial sets are [[simplicial set]]s with a little bit of extra [[stuff, structure, property|structure]]: a marking that remembers which edges are supposed to be [[Cartesian morphism]]s. 


### Definition 


#### In components

+-- {: .un_def }
###### Definition 


A **marked simplicial set** is 

* a pair $(S,E)$ consisting of 

  * a [[simplicial set]] $S$ 

  * and a subset $E \subset S_1$ of edges of $S$, called the _marked edges_, 

* such that

  * all degenerate edges are marked edges.

A morphism $(S,E) \to (S',E')$ of marked simplicial sets is a morphism $f : S \to S'$ of [[simplicial set]]s that carries marked edges to marked edges in that $f(E) \subset E'$.

=--

+-- {: .un_def }
###### Notation

* The category of marked simplicial sets is denoted $sSet^+$.

* for $S$ a [[simplicial set]] let

  * $S^\flat$ or $S^{min}$ be the minimally marked simplicial set: only the degenerate edges are marked;

  * $S^\sharp$ or $S^{max}$ be the maximally marked simplicial set: every edge is marked.

* for $p : X \to S$ a [[Cartesian fibration]] of [[simplicial set]]s let

  * $X^\natural$ or $X^{cart}$ be the cartesian marked simplicial set: precisely the $p$-[[cartesian morphism]]s are marked



=--

#### As a quasi-topos

Simple as the above definition is, for seeing some of its properties it is useful to think of $sSet^+$ in a more abstract way.

+-- {: .un_def }
###### Definition 

Let $\Delta^+$ be the [[category]] defined as the [[simplex category]] $\Delta$, but with one more object $[1^+]$ that factors the unique morphism $[1] \to [0]$ in $\Delta$ 

$$
  \array{
    [0] &\stackrel{\to}{\to}& [1]
    \\
    {}^{\mathllap{=}}\downarrow &\swarrow& \downarrow^{\mathrlap{p}}
    \\
    [0] &\leftarrow& [1^+]  
}
  \,.
$$

Equip this category with a [[coverage]] whose only non-trivial covering family is  $\{p : [1] \to [1]^+\}$.

=--

+-- {: .un_lemma #Quasitopos}
###### Observation

The category $sSet^+$ is the [[quasi-topos]] of [[separated presheaves]] on $\Delta^+$:

$$
  sSet^+ \simeq SepPSh(\Delta^+)
  \,.
$$

=--

+-- {: .proof}
###### Proof

A [[presheaf]] $X : (\Delta^+)^{op} \to Set$ is separated precisely if the morphism

$$
  X(p) : X_{1^+} \to X_1
$$

is a [[monomorphism]], hence if $X_{1^+}$ is a subset of $X_1$. By functoriality this subset contains all the degenerate 1-cells

$$
  \array{
      X_0
      \\
      \downarrow & \searrow^{\mathrlap{\sigma}}
      \\
      X_{1^+} &\hookrightarrow& X_1
  }
  \,.
$$

Therefore we may naturally identify $X$ as a simplicial set equipped with a subset of $X_1$ that contains all degenerate 1-cells.

Moreover, a morphism of separated preseheaves on $\Delta^+$ is by definition just a [[natural transformation]] between them, which means it is under this interpretation precisely a morphism of simplicial sets that respects the marked 1-simplices.

=--

Notice that $sSet^+$ is a genuine quasi-topos:

+-- {: .un_lemma}
###### Observation

$sSet^+$ is not a [[topos]].

=--

+-- {: .proof}
###### Proof

The canonical morphisms $X^\flat \to X^\sharp$ are [[monomorphism]]s and [[epimorphism]]s, but not [[isomorphism]]s. Therefore $sSet^+$ is not a [[balanced category]], hence cannot be a topos.

=--

### Cartesian closure {#CartesianClosure}

+-- {: .un_lemma }
###### Lemma


The category $sSet^+$ is a [[cartesian closed category]].

=--

+-- {: .proof}
###### Proof

This is an immediate consequence of the above [observation](#Quasitopos) that $sSet^+$ is a [[quasitopos]]. But it is useful to spell out the Cartesian closure in detail.

By the general logic of the [[closed monoidal structure on presheaves]] we have that $PSh(\Delta^+)$ is cartesian closed. It remains to check that if $X,Y \in PSh(\Delta^+)$ are marked simplicial sets in that $X_{1^+} \to X_1$ is a monomorphism and similarly for $Y$, that then also $Y^X$ has this property.

We find that the marked edges of $Y^X$ are

$$
  (Y^X)_{1^+} \simeq
  Hom_{PSh(\Delta^+)}([1^+], Y^X) \simeq Hom_{PSh(\Delta^+)}([1^+] \times X, Y)
$$

and the morphism $(Y^X)_{1^+} \to (Y^X)_1$ sends $X \times [1^+] \stackrel{\eta}{\to} Y$ to 

$$
  X \times [1] \stackrel{(Id,p)}{\to} X \times [1^+]
  \stackrel{\eta}{\to} Y
  \,.
$$

Now, by construction, every non-identity morphism $U \to [1^+]$ in $\Delta^+$ factors through $U \to [1]$, which implies that if the components of $p^* \eta_1$ and $p^* \eta_2$ coincide on $U \neq [1^+]$, then already the components of $\eta_1$ and $\eta_2$ on $U$ coincided. By assumption on $X$ the values of $\eta_1$ and $\eta_2$ on $U = [1^+]$ are already fixed, due to the inclusion $X_{1^+} \times [1^+]_{1^+} \hookrightarrow X_{1} \times [1^+]_{1}$. Hence $p^*$ is injective, and so $Y^X$ formed in $PSh(\Delta^+)$ is itself a marked simplicial set.

=--

+-- {: .un_def }
###### Definition


* For $X$ and $Y$ marked simplicial sets let

  * $Map^\flat(X,Y)$ be the [[simplicial set]] underlying the [[cartesian closed category|cartesian]] [[internal hom]] $Y^X \in sSet^+$

  * $Map^\sharp(X,Y)$ the simplicial set consisting of all simplices $ \sigma \in Map^\flat(X,Y)$ such that every edge of $\sigma$ is a marked edge of $Y^X$.

=--

+-- {: .un_corolary }
###### Corollary

These mapping complexes are characterized by the
fact that we have natural bijections

$$
  Hom_{sSet}(K, Map^\flat(X,Y)) 
  \simeq
  Hom_{sSet^+}(K^\flat, Y^X)
  \simeq
  Hom_{sSet^+}(K^\flat \times X, Y)
$$

and

$$
  Hom_{sSet}(K, Map^\sharp(X,Y)) 
   \simeq 
  Hom_{sSet^+}(K^\sharp, Y^X)
   \simeq
  Hom_{sSet^+}(K^\sharp \times X, Y)
$$

for $K \in sSet$ and $X,Y \in sSet^+$. In particular

$$
  Map^\flat(X,Y)_n = Hom_{sSet^+}(X \times \Delta[n]^\flat, Y)
$$

and

$$
  Map^\sharp(X,Y)_n = Hom_{sSet^+}(X \times \Delta[n]^\sharp, Y)
  \,.
$$

=--

In words we have

* The $n$-simplices of the internal hom $Y^X$ are simplicial maps $X \times \Delta[n] \rightarrow Y$ such that when you restrict $X_1 \times \Delta[n]_1 \rightarrow Y_1$ to $E \times \Delta[n]_0$ (where $E$ is the set of marked edges of $X$), this morphism factors through the marked edges of $Y$.

* The marked edges of $Y^X$ are those simplicial maps $X \times \Delta[1] \rightarrow Y$ such that the restriction of $X_1 \times \Delta[1]_1 \rightarrow Y_1$ to $E \times \Delta[1]_1$ factors though the marked edges of $Y$. In the presence of the previous condition, this says that when you apply the homotopy $X \times \Delta[1] \rightarrow Y$ to a marked edge of $X$ paired with the identity at $[1]$, the result should be marked.

+-- {: .un_corolary }
###### Corollary

$Map^\flat(X,Y)$ is full simplicial subset of the internal hom of the underlying simplicial sets spanned by the vertices giving mark preserving maps, in the sense that $\Map^\flat(X,Y)$ contains precisely the simplices whose vertices are mark-preserving.

=--

+-- {: .proof}
###### Proof

The $n$-simplices of this type are the simplicial maps
$X \times \Delta[n] \to Y$ such that, for each point $\Delta[0] \to \Delta[n]$,
the composite $X \times \Delta[0] \to X \times \Delta[n] \to Y$ is mark-preserving.

=--

+-- {: .un_def }
###### Definition

We generalize all this notation from $sSet^+$ to the [[overcategory]] $sSet^+/S := sSet^+/(S^\sharp)$ for any given (plain) simplicial set $S$, by declaring

$$
  Map_S^\flat(X,Y) \subset Map^\flat(X,Y)
$$

and

$$
  Map_S^\sharp(X,Y) \subset Map^\sharp(X,Y)
$$

to be the subcomplexes spanned by the cells that respect that map to the base $S$.

=--


+-- {: .un_lemma }
###### Observation

Let $Y \to S$ be a [[Cartesian fibration]] of simplicial sets, and $X^\natural$ as above the marked simplicial set with precisely the [[Cartesian morphism]]s marked.

Then 

* $Map_S^\flat(X,Y^\natural)$ is an [[quasi-category]];

* $Map_S^\sharp(X, Y^\natural)$ is its [[core]], the maximal [[Kan complex]] inside it.


=--

This is [[Higher Topos Theory|HTT, remark 3.1.3.1]].

+-- {: .proof}
###### Proof

The $n$-cells of $Map_S^\flat(X,Y^\natural)$ are morphisms $X \times \Delta[n]^\flat \to Y^\natural$ over $S$.  This means that for fixed $x \in X_0$, $\Delta[n]$ maps into a [[fiber]] of $Y\to S$. But fibers of Cartesian fibrations are fibers of [[inner fibration]]s, hence are quasi-categories.

Similarly, the $n$-cells of $Map_S^\sharp(X,Y^\natural)$ are morphisms $X \times \Delta[n]^\sharp \to Y^\natural$ over $S$.  Again for fixed $x \in X_0$, $\Delta[n]$ maps into a [[fiber]] of $Y\to S$, but now only hitting Cartesian edges there. But (as discussed at [[Cartesian morphism]]), an edge over a point is Cartesian precisely if it is an equivalence.

=--




+-- {: .un_prop }
###### Proposition


We have a sequence of [[adjoint functor]]s

$$
  (-)^{\flat} \dashv (-)_{\flat} \dashv (-)^{\sharp} \dashv (-)_{\sharp}
  :
  \array{ 
    & \stackrel{(-)^{\flat}}{\to} & 
    \\ 
    & \stackrel{(-)_{\flat}}{\leftarrow} & 
    \\ 
    sSet & \stackrel{(-)^{\sharp}}{\to} & sSet^+ 
    \\ 
    & \stackrel{(-)_{\sharp}}{\leftarrow} & 
  }
$$
 


=--

## Model structure on marked simplicial sets


### Cartesian weak equivalences

Observe that weak equivalences in the [[model structure for quasi-categories]] may be characterized as follows.

+-- {: .un_lemma }
###### Lemma

A morphism $f : C \to D$ between simplicial sets that are [[quasi-categories]] is a weak equivalence in the [[model structure for quasi-categories]] precisely if the following equivalent coditions hold:

* For every simplicial set $K$, the morphism $sSet(K,f) : sSet(K,C) \to sSet(K,D)$ is a weak equivalence in the model structure for quasi-categories.

*  For every simplicial set $K$, the morphism $Core(sSet(K,f)) : Core(sSet(K,C)) \to Core(sSet(K,D))$ on the [[core]]s, the maximal [[Kan complex]]es inside, is a weak equivalence in the standard [[model structure on simplicial sets]], hence a [[homotopy equivalence]].

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 3.1.3.2]].

=--

This may be taken as motivation for the following definition.

+-- {: .un_def }
###### Definition/Proposition

For every [[Cartesian fibration]] $Z \to S$, we have that

$$
  Map_S^\flat(X, Z^{\natural})
$$

is a [[quasi-category]] and

$$
  Map_S^\sharp(X,Z^\natural) = Core(Map_S^\flat(X,Z^\natural))
$$

is the maximal Kan complex inside it.

A morphism $p : X \to Y$ in $sSet^+/S$ is a **Cartesian equivalence** if for every Cartesian fibration $Z$ we have

* The induced morphism $Map_S^\flat(Y,Z^{\natural}) \to Map_S^\flat(X,Z^{\natural})$ is  an [[equivalence of quasi-categories]];

Or equivalently:

* The induced morphism $Map_S^\sharp(Y,Z^{\natural}) \to Map_S^\sharp(X,Z^{\natural})$ is a [[model structure on simplicial sets|weak equivalence of Kan complexes]].


=--

This is [[Higher Topos Theory|HTT, prop. 3.1.3.3]] with [[Higher Topos Theory|HTT, remark 3.1.3.1]].


+-- {: .un_prop }
###### Proposition

Let

$$
  \array{
    X &&\stackrel{p}{\to}&& Y
    \\
    & \searrow && \swarrow
    \\
    && S
  }
$$

be a morphism in $sSet/S$ such that both vertical maps to $S$ are
Cartesian fibrations. Then the following are equivalent:

* $p$ is a [[homotopy equivalence]].

* The induced morphism $X^\natural \to Y^\natural$ in $sSet^+/S$ is a Cartesian equivalence.

* The induced morphism on each fiber $X_s \to Y_{p(s)}$ is a 
  weak equivalence in the [[model structure for quasi-categories]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 3.1.3.5]].

=--


### The model structure

The **model structure on marked simplicial over-sets** $Set^+/S$ over $S \in SSet$ -- also called the **Cartesian model structure** since it models [[Cartesian fibration]]s -- is defined as follows.


+-- {: .un_def }
###### Definition/Proposition
**(Cartesian model structure on $sSet^+/S$)**

The category $SSet^+/S$ of [[marked simplicial set]]s over a marked simplicial set $S$ carries a structure of a [[proper model category|left proper]] [[combinatorial simplicial model category]] defined as follows.

The [[SSet]]-[[enriched category|enrichment]] is given by 

$$
  sSet^+/S(X,Y) := Map_S^\sharp(X,Y)
  \,.
$$

A morphism $f : X \to X'$ in $SSet^+/S$ of [[marked simplicial set]]s is 

* a _cofibration_ precisely if underlying morphism of [[simplicial set]]s is a cofibration in the standard [[model structure on simplicial sets]] (i.e. a [[monomorphism]]).

  (def. 3.1.2.2 of [[Higher Topos Theory|HTT]])

* a weak equivalences precisely if it is a Cartesian equivalence, as defined above.
=--
+-- {: .proof}
###### Proof
The model structure is proposition 3.1.3.7 in [[Higher Topos Theory|HTT]]. The simplicial enrichment is corollary 3.1.4.4.
=--

+-- {: .un_remark}
###### Remark
Using $Map_S^\flat(X,Y)$ for the mapping objects makes $sSet^+/S$ a
$sSet_{Joyal}$-[[enriched model category]] (i.e. enriched in the [[model structure for quasi-categories]]).  This is [[Higher Topos Theory|HTT, remark 3.1.4.5]].
=--

Notice that trivially every object in this model structure is cofibrant.
The following proposition shows that the above model structure indeed
presents the $(\infty,1)$-category $CartFib(S)$ of [[Cartesian fibration]]s.


+-- {: .num_prop #FibrantObjects}
###### Proposition
An object $p : X \to S$ in $sSet^+/S$ is _fibrant_ with respect to the above model structure precisely if it is isomorphic to an object of the
form $Y^\natural$, for $Y \to S$ a [[Cartesian fibration]] in [[sSet]].
=--
+-- {: .proof}
###### Proof
This is [[Higher Topos Theory|HTT, prop. 3.1.4.1]].
=--

In particular, the fibrant objects of $sSet^+ \cong sSet^+/*$ are precisely the quasicategories in which the marked edges are precisely the [[equivalence in a quasi-category|equivalences]].  Note that the Cartesian model structure on $sSet^+/S$ is *not* the [[model structure on an over category]] induced on $sSet^+/S$ from the Cartesian model structure on $sSet^+$!


+-- {: .un_def }
###### Definition/Proposition
**(coCartesian model structure on $sSet^+/S$)**

There is another such model structure, with [[Cartesian fibration]]s replaced everywhere by **coCartesian fibrations.

=--











### Marked anodyne morphisms {#MarkedAnodyne}

A class of morphisms with [[left lifting property]] again some class of fibrations is usually called _anodyne_ . For instance a left/right/inner anodyne morphism of simplicial sets is one that has the left lifting property against all [[left fibration|left/right fibration]]s or [[inner fibration]]s, respectively.

The class of _marked anodyne_ morphisms in $sSet^+$ as defined in the following is something that comes close to having the left lifting property against all Cartesian fibrations. It does not quite, but is still useful for various purposes.

+-- {: .un_defn}
###### Definition ([[Higher Topos Theory|HTT, Def 3.1.1.1]])


The collection of **marked anodyne morphisms** in $SSet^+/S$ is the class of morphisms $An^+ = LLP(RLP(An^+_0))$ where the generating set $An^+_0$ consists of

* for $0 \lt i \lt n $ the minimally marked [[horn]] inclusions

  $$
    (\Lambda[n]_i)^\flat \to \Delta[n]^\flat
  $$

* for $i = n$ the horn inclusion with the last edge marked:

  $$
    (\Lambda[n]_n, \mathcal{E} \cap (\Lambda[n]_n)_1)
    \to 
    (\Delta[n], \mathcal{E} )    
    \,,
  $$
  
  where $\mathcal{E}$ is the union of all degenerate edges in $\Delta[n]$ together with the edge $\Delta^{\{n-1,n\}} \to \Delta[n]$.


* the inclusion

  $$
    (\Lambda[2]_1)^\sharp \coprod_{(\Lambda[2]_1)^\flat}
    (\Delta[2])^\flat
    \to
    (\Delta[2])^\sharp
    \,.
  $$

* for every [[Kan complex]] $K$ the morphism $K^\flat \to K^\sharp$.

=--

The crucial property of marked anodyne morphisms is the following characterization of morphisms that have the right lifting property with respect to them.

+-- {: .un_prop}
###### Proposition 


A morphism $p : X \to S$ in $SSet^+$ has the [[right lifting property]] with respect to the class $An^+$ of marked anodyne maps precisely if

1. $p$ is an [[inner fibration]]

1. an edge $e$ of $X$ is marked precisely if it is a $p$-[[Cartesian morphism]] and $p(e)$ is marked in $S$

1. for every object $y$ of $X$ and every marked edge $\bar e : \bar x \to p(y)$ in $S$ there exists a marked edge $e : x \to y$ of $X$ with $p(e) = \bar e$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 3.1.1.6]]

=--

+-- {: .un_remark}
###### Remark 

Thus, if $(X, E_X) \to (S,E_S)$ is a morphism in $sSet^+$ with RLP against marked anodyne morphisms, then its underlying morphism $X\to S$ in $sSet$ is almost a [[Cartesian fibration]]: it may fail to be such only due to missing markings in $E_S$.

However, if _all_ morphisms in $S$ are marked, then $(X,E_X) \to S^\sharp$ has the RLP against marked anodyne morphisms precisely when the underlying morphism $X\to S$ is a [[Cartesian fibration]] and exactly the [[Cartesian morphism]]s are marked in $X$, $(X,E_X) = X^\natural$ --- in other words, precisely if it is a fibrant object in the model structure on $sSet^+/S$.

=--

See also [[Higher Topos Theory|HTT, remark. 3.1.1.11]].

The following stability property of marked anodyne morphisms is important in applications. Recall that a cofibration in $sSet^+$ is a morphism whose underlying morphism in [[sSet]] is a [[monomorphism]].

+-- {: .un_prop}
###### Proposition 
**(stability under smash product with cofibrations)**

Marked anodyne morphisms are stable under "[[smash product]]" with cofibrations:

for $f : X \to X'$ marked anodyne, and $g : Y \to Y'$ a cofibration, the induced morphism 

$$
  (X \times Y') \coprod_{X \times Y} (X' \times Y)
  \to
  X' \times Y'
$$ 

out of the [[pushout]] in $sSet^+$ is marked anodyne.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 3.1.2.3]].

=--



### As a model for the $(\infty,1)$-category of $(\infty,1)$-categories

The Joyal [[model structure for quasi-categories]] $sSet_{Joyal}$ is an [[enriched category]] enriched over itself. So it is _not_ a [[simplicial model category]] in the standard sense, which means $sSet_{Quillen}$-enriched.

Indeed, the full sSet-enriched subcategory $(sSet_{Joyal})^\circ$ on fibrant-cofibrant objects is a model for the [[(∞,2)-category]] [[(∞,1)Cat]] of [[(∞,1)-categories]]. For many applications it is more convenient to work just with the [[(∞,1)-category of (∞,1)-categories]] inside that, obtained by taking in each [[hom-object]] [[quasi-category]] the maximal [[Kan complex]].

The resulting [[(∞,1)-category]] should have a presentation by a [[simplicial model category]]. And the model structure on marked simplicial sets does accomplish this.


## Related concepts

* [[model structure for dendroidal Cartesian fibrations]]
  
## References 

Marked simplicial sets are introduced in section 3.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The model structure on marked simplicial oversets is described in section 3.1.3


[[!redirects marked simplicial set]]
[[!redirects marked simplicial sets]]
[[!redirects model structure for coCartesian fibrations]]
[[!redirects model structure on marked simplicial over-sets]]
[[!redirects model structure on marked simplicial oversets]]

[[!redirects model structure on marked simplicial sets]]
