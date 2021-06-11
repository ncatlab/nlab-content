
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

A _monoidal model category_ is a [[model category]] which is also a [[closed monoidal category]] in a compatible way.  In particular, its [[homotopy category]] inherits a closed monoidal structure, as does the [[(infinity,1)-category]] that it presents.


## Definition 


+-- {: .num_defn #MonoidalModelCategory}
###### Definition

A (symmetric) **monoidal model category** is [[model category]] $\mathcal{C}$
equipped with the structure of a  [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$
such that the following two compatibility conditions are satisfied

1. {#PushoutProductAxiom} ([[pushout-product axiom]]) For every pair of cofibrations $f \colon X \to Y$ and $f' \colon X' \to Y'$, their [[pushout-product]], hence the induced morphism out of the cofibered [[coproduct]] over ways of forming the tensor product of these objects

   $$
     (X \otimes Y') \coprod_{X \otimes X'} (Y \otimes X')
     \longrightarrow
     Y \otimes Y'
     \,,
   $$

   is itself a cofibration, which, furthermore, is acyclic if $f$ or $f'$ is.

   (Equivalently this says that the [[tensor product]] $\otimes : C \times C \to C$ is a left [[Quillen bifunctor]].)

1. (unit axiom) For every cofibrant object $X$ and every cofibrant resolution $\emptyset \hookrightarrow Q I \stackrel{p_I}{\longrightarrow} I$ of the [[tensor unit]] $I$, the resulting morphism

   $$
     Q I \otimes X \stackrel{p_I \otimes X}{\longrightarrow} I\otimes X \stackrel{\simeq}{\longrightarrow} X
   $$ 

  is a weak equivalence.


=--

+-- {: .num_remark #CaseOfCofibrantTensorUnit}
###### Remark

The [[pushout-product axiom]] in def. \ref{MonoidalModelCategory} implies that for $X$ a cofibrant object, then the functor $X \otimes (-)$ is  preserves cofibrations and acyclic cofibrations.

In particular if the [[tensor unit]] $I$ happens to be cofibrant, then the unit axiom in def. \ref{MonoidalModelCategory} is implied by the [pushout-product axiom](#PushoutProductAxiom). (Because then $Q I \to I$ is a weak equivalence between cofibrant objects and such are preserved by functors that preserve acyclic cofibrations, by [[Ken Brown's lemma]]. ) 

=--



+-- {: .num_defn #MonoidAxiom}
###### Definition

We say a [[monoidal model category]], def. \ref{MonoidalModelCategory}, satisfies the **[[monoid axiom]]**, def. \ref{MonoidalModelCategory}, if every morphism that is obtained as a [[transfinite composition]] of [[pushouts]] of [[tensor products]] $X\otimes f$ of acyclic cofibrations $f$ with any object $X$ is a weak equivalence.

=--

([Schwede-Shipley 00, def. 3.3.](#SchwedeShipley00)).

+-- {: .num_remark}
###### Remark

In particular, the axiom in def. \ref{MonoidAxiom} says that for every object $X$ the functor $X \otimes (-)$ sends acyclic cofibrations to weak equivalences.

=--


## Properties 

### Monoidal homotopy category
 {#MonoidalHomotopyCategory}
 
#### Abstractly

+-- {: .num_prop #LocalizationFunctorIsLaxMonoidal}
###### Proposition

For $(\mathcal{C},\otimes)$ a monoidal model category, def. \ref{MonoidalModelCategory}, then the [[derived functor]] $\otimes^L$ of the tensor product makes the [[homotopy category of a model category|homotopy category of the model category]] itself into a [[monoidal category]], such that the [[localization]] functor

$$
  \gamma
   \;\colon\;
  (\mathcal{C},\otimes)
    \longrightarrow
  (Ho(\mathcal{C}), \otimes^L)
$$

is a [[lax monoidal functor]].

=--

+-- {: .proof}
###### Proof

Let $V$ be a monoidal model category, and consider it as a _[[derivable category]]_ in the sense of ([Shulman 11, section 8](#Shulman11)) with $V_Q$ the subcategory of cofibrant objects and $V_R=V$.  Then $\otimes :V\times V\to V$ is left derivable, i.e. it preserves the $Q$-subcategories and weak equivalences.  Since deriving is [[pseudofunctor|pseudofunctorial]] (and product-preserving) on the [[2-category]] of [[derivable categories]] and [[left derived functor|left derivable functors]], it follows immediately that $Ho(V)$ is monoidal; this is ([Shulman 11, example 8.13](#Shulman11)).

Now let $V_0$ denote the category $V$ with its trivial derivable structure: only isomorphisms are weak equivalences, and all objects are both $Q$ and $R$.  Then of course $Ho(V_0) = V$, and $V_0$ is also a pseudomonoid in derivable categories.  The identity functor $Id : V_0 \to V$ is not left derivable, since it does not preserve $Q$-objects; but it is *right* derivable, since we took all objects in $V$ to be $R$-objects (ignoring the fibrant objects in the model structure on $V$).  Of course $Id$ is [[strong monoidal functor|strong monoidal]], and this monoidality constraint can be expressed as a square in the [[double category]] of ([Shulman 11](#Shulman11)) whose vertical arrows are left derivable functors and whose horizontal arrows are right derivable functors; moreover the axioms on a [[monoidal functor]] may be expressed using products and double-categorical pasting in this double category.  Therefore, it is all preserved by the double pseudofunctor $Ho$; but $Ho(Id) = \gamma : V \to Ho(V)$.  The only thing that is not visible to the double category is the invertibility of the monoidal constraint, and hence this is not preserved by the double pseudofunctor; thus $\gamma$ is only [[lax monoidal functor|lax monoidal]].

=--

#### Explicitly

+-- {: .num_prop #MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}
###### Proposition

Let $(\mathcal{C}, \otimes, 1)$ be a [[monoidal model category]] with cofibrant [[tensor unit]]. Then the [[left derived functor]] $\otimes^L$ of the tensor product exists 

$$
  \array{
    \mathcal{C}_c\times \mathcal{C}_c
      &\overset{\otimes}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{\gamma \times \gamma}}\downarrow 
      &\swArrow_{\mu^{-1}}& 
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C})\times Ho(\mathcal{C})
     &\overset{\otimes^L}{\longrightarrow}&
    Ho(\mathcal{C})
  }
$$

and makes the [[homotopy category of a model category|homotopy category]] into a [[monoidal category]] $(Ho(\mathcal{C}), \otimes^L, \gamma(1))$.

Moreover, the [[localization]] functor

$$
  \gamma
  \;\colon\;
  (\mathcal{C}_c, \otimes, 1)
   \longrightarrow
  (Ho(\mathcal{C}), \otimes^L , \gamma(1))
$$

on the [[category of cofibrant objects]] is a [[strong monoidal functor]] with structure morphism the inverse of the above natural isomorpmism

$$
  \mu_{X,Y}
  \;\colon\;
  \gamma(X)\otimes^L \gamma(Y)
    \longrightarrow
  \gamma(X \otimes Y)
  \,.
$$

=--


+-- {: .proof}
###### Proof


For the [[left derived functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#LeftAndRightDerivedFunctorsOnModelCategories)) of the tensor product

$$
  \otimes
  \;
  \mathcal{C}\times \mathcal{C}
    \longrightarrow
  \mathcal{C}
$$

to exist, it is sufficient that its restriction to the subcategory 

$$
  (\mathcal{C} \times \mathcal{C})_c
  \simeq
  \mathcal{C}_c \times \mathcal{C}_c
$$

of cofibrant objects preserves acyclic cofibrations ([[Ken Brown's lemma]], [here](Introduction+to+Stable+homotopy+theory+--+P#KenBrownLemma)).

Every morphism $(f,g)$ in the [[product category]] $\mathcal{C}_{c}\times \mathcal{C}_{c}$ may be written as a composite of a pairing with an identity morphisms

$$
  (f,g)
    \;\colon\;
  (c_1, d_1)
    \overset{(id_{c_1},g)}{\longrightarrow}
  (c_1,d_2)
    \overset{(f,id_{c_2})}{\longrightarrow}
  (c_2,d_2)
  \,.
$$

Now since the [[pushout product]] (with respect to tensor product) with the initial morphism $(\ast \to c_1)$ is equivalently the tensor product

$$
  (\ast \to c_1) \Box_{\otimes} g
    \;\simeq\;
  id_{c_1} \otimes g
$$

and 

$$
  f \Box_{\otimes} (\ast \to c_2)
    \;\simeq\;
  f \otimes id_{c_2}
$$

the [[pushout-product axiom]] (def. \ref{MonoidalModelCategory}) implies that on the subcategory of cofibrant objects the functor $\otimes$ preserves acyclic cofibrations. (This is why one speaks of a _[[Quillen bifunctor]]_, see also [Hovey 99, prop. 4.3.1](#Hovey99)).

Hence $\otimes^L$ exists. 

By the same decomposition and using the [[universal property]] of the [[localization]] of a category ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) one finds that for $\mathcal{C}$ and $\mathcal{D}$ any two [[categories with weak equivalences]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryWithWeakEquivalences)) then the [[localization]] of their [[product category]] is the product category of their localizations:

$$
  (\mathcal{C} \times \mathcal{D})[(W_{\mathcal{C}} \sqcup W_{\mathcal{D}})^{-1}]
  \simeq
  (\mathcal{C}[W^{-1}_{\mathcal{C}}])
  \times
  (\mathcal{D}[W^{-1}_{\mathcal{D}}])
  \,.
$$

With this, the [[universal property]] as a [[localization]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) of the [[homotopy category of a model category]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)) induces [[associators]]: Let 

$$
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{((-)\otimes(-))\otimes (-)}{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{\gamma_{\mathcal{C} \times \mathcal{C} \times \mathcal{C}}}}\downarrow
      &\swArrow_{\eta}&
    \downarrow^{\mathrlap{\gamma_{\mathcal{C}}}}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{((-)\otimes^L(-))\otimes^L (-)}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \;\;\;\,,\;\;\;\;\;
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{ (-) \otimes ( (-) \otimes (-) ) }{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{\gamma_{\mathcal{C} \times \mathcal{C} \times \mathcal{C}}}}\downarrow
      &\swArrow_{\eta'}&
    \downarrow^{\mathrlap{\gamma_{\mathcal{C}}}}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{ (-) \otimes^L ( (-) \otimes^L (-) )  }{\longrightarrow}&
    Ho(\mathcal{C})
  }
$$

be the [[natural isomorphism]] exhibiting the [[derived functors]] of the two possible tensor products of three objects, as shown at the top. By pasting the second with the [[associator]] natural isomorphism of $\mathcal{C}$ we obtain another such factorization for the first, as shown on the left below,

{#DerivedAssociatorFromUniversalPropertyOfLocalization}
$$
  (\star)
  \;\;\;\;\;\;
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{((-)\otimes(-))\otimes (-)}{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{=}}\downarrow 
      &\swArrow_{\alpha}&
    \downarrow^{\mathrlap{=}}
    \\
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{ (-) \otimes ( (-) \otimes (-) ) }{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{\gamma_{\mathcal{C} \times \mathcal{C} \times \mathcal{C}}}}\downarrow
      &\swArrow_\eta&
    \downarrow^{\mathrlap{\gamma_{\mathcal{C}}}}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{ (-) \otimes^L ( (-) \otimes^L (-) )  }{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{((-)\otimes(-))\otimes (-)}{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{\gamma_{\mathcal{C} \times \mathcal{C} \times \mathcal{C}}}}\downarrow
      &\swArrow_{\eta'}&
    \downarrow^{\mathrlap{\gamma_{\mathcal{C}}}}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{((-)\otimes^L(-))\otimes^L (-)}{\longrightarrow}&
    Ho(\mathcal{C})
    \\
    {}^{\mathllap{=}}\downarrow 
      &\swArrow_{\alpha^L}&
    \downarrow^{\mathrlap{=}}
    \\
    Ho(\mathcal{C})\times Ho(\mathcal{C})\times Ho(\mathcal{C})
      &\underset{(-)\otimes^L((-)\otimes^L (-))}{\longrightarrow}&
    Ho(\mathcal{C})
  }
$$

and hence by the [[universal property]] of the factorization through the derived functor, there exists a unique natural isomorphism $\alpha^L$ such as to make this composite of natural isomorphisms equal to the one shown on the right. Hence the [[pentagon identity]] satisfied by $\alpha$ implies a pentagon identity for $\alpha^L$, and so $\alpha^L$ is an [[associator]] for $\otimes^L$.

The above equation on pasting composites of [[natural isomorphism]] is equivalently just the coherence law for a monoidal functor:

$$
  \array{
    (\gamma(X) \otimes^L \gamma(Y)) \otimes^L \gamma(Z)
     &\overset{\alpha^L_{\gamma(X), \gamma(Y), \gamma(Z)}}{\longrightarrow}&
    \gamma(X) \otimes^L (\gamma(Y) \otimes^L \gamma(Z))
    \\
    {}^{\mathllap{\eta'}}\uparrow
      &&
    \uparrow^{\mathrlap{\eta}}
    \\
    \gamma( (X \otimes Y) \otimes Z )
     &\underset{\gamma(\alpha)}{\longrightarrow}&
   \gamma(X \otimes (Y \otimes Z))
  }
  \,.
$$




=--




## Examples 

### Classical homotopy theory

* A [[nice category of spaces|nice category of topological spaces]] with cartesian product and the [[classical model structure on topological spaces]].

* The category of [[simplicial sets]] with cartesian product and the [[classical model structure on simplicial sets]].

* The [[classical model structure on pointed topological spaces]] or pointed simplicial sets with the [[smash product]] of pointed objects.

### Simplicial presheaves
 {#SimplicialPresheaves}

If the underlying [[site]] has [[finite product]], then both the injective and the projective, the global and the local [[model structure on simplicial presheaves]] becomes a (Cartesian) [[monoidal model category]] with respect to the standard [[closed monoidal structure on presheaves]].

See at _[[model structure on simplicial presheaves]]_ the section _[Closed monoidal structure](https://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#MonoidalStructure)_.


### Homological algebra and stable homotopy theory

* The category of [[chain complex]]es with the usual [[tensor product]] of chain complexes and the [[model structure on chain complexes|projective model structure]].

With respect to a [[symmetric monoidal smash product of spectra]]:

* the [[model structure on symmetric spectra]]

* the [[model structure on orthogonal spectra]]

* the [[model structure for excisive functors]]

([Schwede-Shipley 00](#SchwedeShipley00), [MMSS 00, theorem 12.1 (iii) with prop. 12.3](#MMSS00))

The standard example of a monoidal model category whose unit is not cofibrant is the category of EKMM S-modules.

### Categorical model structures

* The category [[Cat]] with cartesian product and the [[folk model structure]].

* The category [[Gray]] of [[strict 2-category|strict 2-categories]] with the [[Gray tensor product]] and the [[model structure on 2-categories|Lack model structure]].



### Model structure on $G$-objects

+-- {: .un_def}
###### Assumption

Let $\mathcal{E}$ be a [[category]] equipped with the structure of

* a [[closed monoidal category|closed]] [[symmetric monoidal category]];

* a [[monoidal model category]];

such that

* the model structure is [[cofibrantly generated model category|cofibrantly generated]];

* the tensor unit $I$ is cofibrant.

=--

+-- {: .un_prop}
###### Proposition

Under these conditions there is for each [[finite group]] $G$ the structure of a [[monoidal model category]] on the category $\mathcal{E}^{\mathbf{B}G}$ of objects in $\mathcal{E}$ equipped with a $G$-[[action]], for which the [[forgetful functor]]

$$
  \mathcal{E}^{\mathbf{B}G} \to \mathcal{E}
$$

preserves and reflects fibrations and weak equivalences.

=--


See for instance ([BergerMoerdijk 2.5](#BergerMoerdijkResolution)).


### Model structure on monoids

See [[model structure on monoids in a monoidal model category]].


## Related concepts

* [[monoidal localization]]

* [[monoidal Quillen adjunction]]

* [[model structure on monoids in a monoidal model category]]

## References 

Textbook accounts:

* {#Hovey99} [[Mark Hovey]], Def. 4.2.6 in: _[[Model Categories]]_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

* [[Jacob Lurie]], Def. A.3.1.2 in: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))


Some relevant homotopy category background is in

* {#Shulman11} [[Mike Shulman]], _Comparing composites of left and right derived functors_, New York Journal of Mathematics Volume 17 (2011) 75-125 ([arXiv:0706.2868](http://arxiv.org/abs/0706.2868), [publisher](http://nyjm.albany.edu/j/2011/17-5.html))


The monoidal structures for a [[symmetric monoidal smash product of spectra]] are due to 

* {#SchwedeShipley00} [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], part III of _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

Further variation of the axiomatics is discussed in

* {#BataninBerger13} [[Michael Batanin]], [[Clemens Berger]], _Homotopy theory for algebras over polynomial monads_ ([arXiv:1305.0086](https://arxiv.org/abs/1305.0086))

The monoidal model structure on $\mathcal{E}^{\mathbf{B}G}$ is discussed for instance in

* {#BergerMoerdijkResolution} [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_, Topology 45 (2006), 807&#8211;849.

Relation to [[symmetric monoidal (infinity,1)-categories]] (in particular, that every locally presentable symmetric monoidal $(\infty,1)$-category arises from a symmetric monoidal model category) is discussed in 

* {#NikolausSagave15} [[Thomas Nikolaus]], [[Steffen Sagave]], _Presentably symmetric monoidal infinity-categories are represented by symmetric monoidal model categories_ ([arXiv:1506.01475](http://arxiv.org/abs/1506.01475))



[[!redirects monoidal model categories]]
[[!redirects monoidal model structure]]
[[!redirects monoidal model structures]]
[[!redirects symmetric monoidal model structure]]
[[!redirects symmetric monoidal model structures]]
[[!redirects symmetric monoidal model category]]
[[!redirects symmetric monoidal model categories]]