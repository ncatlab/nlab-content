
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

The [[Denis-Charles Cisinski|Cisinski]]--[[Ieke Moerdijk|Moerdijk]] [[model category]] structure on the [[category]] $dSet$ of [[dendroidal sets]] models [[(∞,1)-operads]] in generalization of the way the [[Andre Joyal|Joyal]] [[model structure on simplicial sets]] models [[(∞,1)-category|(∞,1)-categories]].

## Overview

We have the following diagram of [[model category|model categories]]:

$$
  \array{
    SSet\text{-}Operad 
     &\stackrel{\simeq}{\to}& 
    dSet
     &\stackrel{\simeq}{\to}& 
    dSpaces
    &&&&& models\;for\;(\infty,1)\text{-}operads
    \\
    \uparrow && \uparrow && \uparrow
    \\
    SSet\text{-}Cat 
     &\stackrel{\simeq}{\to}& 
    sSet
     &\stackrel{\simeq}{\to}& 
    sSpaces   
    &&&&&
    models\;for\;(\infty,1)\text{-}categories
  }
  \,,
$$

where the entries are

* the category $SSet Cat$ of [[simplicially enriched category|simplicially enriched categories]] equipped with the [[Julie Bergner|Bergner]] model structure;

* the category [[SSet]] of [[simplicial set]]s equipped with the [[model structure on simplicial sets|Joyal model structure]] for [[quasi-category|quasi-categories]];

* the category $dSet$ of [[dendroidal set]]s

and where 

* the horizontal morphisms are [[Quillen equivalence]]s

* the vertical morphisms are [[reflective sub-(infinity,1)-category|homotopy full embeddings]].

## Definition


### Special morphisms ###

Recall from the entry on [[dendroidal set]]s the definition of inner and outer faces, boundaries and inner and outer horns.

The following definition are the obvious generalizations of the corresponding notions for the [[model structure on simplicial sets]], in particular for the [[model structure for quasi-categories]].

+-- {: .num_defn #InnerAnodyneExtension}
###### Definition 

The class of morphisms in $dSet$ generated from the inner horn inclusions $\Lambda^e \Omega[T] \to \Omega[T]$ under

* [[pushout]]

* [[transfinite composition]]

* [[retract]]s

is called the **inner [[anodyne extensions]]**.

=--

+-- {: .num_defn #NormalMonomorphism}
###### Definition 

The class of morphisms in $dSet$ generated from boundary inclusions 
$\delta \Omega[T] \to \Omega[T]$ under

* [[pushout]]

* [[transfinite composition]]

* [[retracts]]

is called the **[normal monomorphisms](http://ncatlab.org/nlab/show/dendroidal%20set#NormalMonomorphisms)**.

=--


+-- {: .num_defn}
###### Definition 

A [[morphism]] $A \to B$ in $dSet$ is an **inner Kan fibration** if it has the [[right lifting property]] with respect to all inner horn inclusions.

$$
  \array{
    \Lambda^e[T] &\to& A
     \\
    \downarrow && \downarrow
    \\
    \Omega[T] &\to& B
  }
$$

or equivalently with respect to the class of inner anodyne extensions.

=--


+-- {: .num_defn #QuasiOperad}
###### Definition 

A dendroidal set $X$ is an **inner Kan complex** or **quasi-operad** if the canonical morphism $X\to {*}$ to the [[terminal object]] is an inner Kan fibration.

=--

+-- {: .num_defn}
###### Definition 

A morphism $A \to B$ of dendroidal sets is an **acyclic fibration** if it has the [[right lifting property]] with respect to all normal monomorphisms.

=--

+-- {: .num_defn #Isofibration}
###### Definition 

A morphism $f : X \to Y$ of dendroidal sets is called an **isofibration** if it 

1. it is an inner Kan fibration;

1. the morphism of operads $\tau_d(f) : \tau_d(X) \to \tau_d(Y)$ is a fibration in the [[canonical model structure on operads]], hence the underlying [[functor]] of categories is an [[isofibration]]. 

=--


### The model structure



+-- {: .num_defn #ModelStructureOnDendroidalSets}
###### Definition 

On the category of [[dendroidal sets]] let

* the cofibrations be the [normal monomorphisms](#NormalMonomorphism);

* the fibrant objects are the weak Kan complexes/[quasi-operads](#QuasiOperad);

* the fibrations between fibrant objects are precisely the [isofibrations](#Isofibration).

* the weak equivalences form the smallest class of maps that satisfy

  * [[category with weak equivalences|2-out-of-3]]

  * every [inner anodyne extension](#InnerAnodyneExtension) is a weak equivalence

  * every acyclic fibration between quasi-operads is a weak equivalence.

=--



## Properties 
  {#Properties}

### Establishing the model structure

#### Statement
 {#StatementOfTheModelStructure}

+-- {: .num_theorem #TheModelStructureExistenceAndBasicProperties}
###### Theorem

The above choices of cofibrations, fibrations and weak equivalences equips the category $dSet$ of dendroidal sets with the structure of a [[model category]] $dSet_{CM}$. This model structure is

* a left [[proper model category]]

* a [[cofibrantly generated model category]]

* a [[combinatorial model category]]

* a [[symmetric monoidal category|symmetric]] [[monoidal model category]] (with respect to the [Boardman-Vogt tensor product](http://ncatlab.org/nlab/show/dendroidal%20set#BoardmanVogtTensorProduct)). 

=--


This is ([Cisinski Moerdijk, theorem 2.4 and prop. 2.6](#CisinskiMoerdijk09)). We indicate the proof [below](#ProofOfTheModelStructure).

+-- {: .num_remark }
###### Remark

The [[cofibrantly generated model category|generating cofibrations]] $I$ are the boundary inclusion of [[trees]]

$$
  I = \{\partial \Omega[T] \hookrightarrow \Omega[T]\}
  \,.
$$

A set of generating acyclic cofibrations is guaranteed to exist, but no good explicit characterization is known to date.

=--


This is ([CisMoe, cor. 6.17](#CisinskiMoerdijk09)).


+-- {: .num_prop }
###### Proposition


A morphism $j : X \to Y$ between cofibrant objects in $dSet$ is a weak equivalence precisely if for all fibrant objects $A$ the morphism 

$$
  \tau : dSet(Y,A) \to \tau dSet(X,A)
$$

is an [[equivalence of categories]], where $\tau : SSet \to Cat$ is the [[left adjoint]] to the [[nerve]].

=--


This is in ([Moerdijk, section 8.4](#Moerdijk)).

#### Proof 
 {#ProofOfTheModelStructure}

We state a list of lemmas to establish theorem \ref{TheModelStructureExistenceAndBasicProperties}.

The **strategy** is the following: we [[over topos|slice]] $dSet$ over a normal [[resolution]] $E_\infty$ (a model of the [[E-∞ operad]]) of the terminal object. Since over a normal object all morphisms are normal, we have a chance to establish a _[[Cisinski model structure]]_ on $dSet_{/E_\infty}$. This indeed exists, prop. \ref{ModelStructureOnSlices} below, and the model structure on $dSet$ itself can then be [[transferred model structure|transferred]] along the [[inverse image]] of the [[etale geometric morphism]] $dSet_{/E_\infty} \to dSet$, prop. \ref{TransferOfTheModelStructure}.

+-- {: .num_prop }
###### Proposition 

For $A \to B$ an inner [[anodyne extension]] and $X \to Y$ a normal monomorphism of [[dendroidal sets]], the [[pushout-product axiom|pushout-product morphism]]

$$
  A \otimes Y \cup B \otimes X \to B\otimes Y
$$

(with "$\otimes$" the [[Boardman-Vogt tensor product]]) is an inner anodyne extension.

=--

This is ([Cis-Moer, prop. 3.1](#CisinskiMoerdijk09)).

+-- {: .num_defn #JFibrations}
###### Definition

Write $J := \{0 \stackrel{\simeq}{\to} 1\}$ for the [[codiscrete groupoid]] on two objects. We use the same symbol for its image along $N_d i_! : Cat \hookrightarrow dSet$.

The **$J$-anodyne extensions** in $dSet$ are the morphisms generated under [[pushouts]], [[transfinite composition]] and [[retracts]] from the the inner [[anodyne extensions]] and from the [[pushout-product axiom|pushout products]] of $\{e\} \to J$ with the tree boundary inclusion

$$
  \{
    \partial \Omega[T] \otimes J \; \cup \;
    \Omega[T] \otimes \{0\}
    \to
    \Omega[T] \otimes J
  \}_{e \in \{0,1\}, T \in \Omega}
  \,.
$$

Call a morphism a **$J$-fibration** if it has the [[right lifting property]] against $J$-anodyne extensions.

=--

This is ([Cis-Moer, 3.2](#CisinskiMoerdijk09)).


+-- {: .num_prop }
###### Proposition 

For $A \to B$ a $J$-anodyne extension and $X \to Y$ a normal monomorphism of [[dendroidal sets]], the [[pushout-product axiom|pushout-product morphism]]

$$
  A \otimes Y \cup B \otimes X \to B\otimes Y
$$

is a $J$-anodyne extension.

=--

This is ([Cis-Moer, prop. 3.3](#CisinskiMoerdijk09)).

+-- {: .num_defn }
###### Definition

For $X \in dSet$, the BV-tensor product with

$$
  \{0\} \coprod \{1\} \to J \to \eta
$$ 

defines an [[interval object]]

$$
  X \coprod X \to J \otimes X \to X
  \,.
$$ 

This is compatible with slicing, in that for any $B \in sSet$ and $a : X \to B$ a given morphism, we have an interval object in the [[over category]] $dSet_{/B}$ given by a diagram

$$  
  \array{
    X \coprod X &\to& J \otimes X &\to& X
    \\
    & {}_{(a,a)}\searrow & \downarrow & \swarrow_{a}
    \\
    && B
  }
  \,.
$$ 



If in the above $B$ is normal and $a : X \to B$ is $J$-anodyne, then the [[left homotopies]] given by the above cylinder
defines a notion of [[left homotopy]] in $dSet_{/B}$.

Say a morphism $f : A \to A'$ in $dSet_{/B}$ is a **$B$-equivalence** if it is a homotopy equivalence with respect to this notion of homotopy, hence if for all $J$-fibrations $X \to B$ the induced morphism

$$
  [A',X]_{\sim_B} \to [A,X]_{\sim B}
$$

is a bijection.

=--


+-- {: .num_prop #ModelStructureOnSlices}
###### Proposition

Let $B \in dSet$ be normal. Then $dSet_{/B}$ carries a [[left proper model category|left proper]] [[cofibrantly generated model category]] for which

* the weak equivalences are the $B$-equivalences;

* the cofibrations are the monomorphisms;

* the fibrant objects are the $J$-fibrations into $B$;

* a morphism between fibrant objects is a fibration precisely if its image in $dSet$ is a $J$-fibration. 

=--

This is ([Cis-Moer, prop. 3.5](#CisinskiMoerdijk09)). 

+-- {: .proof}
###### Proof

Notice that 

1. every monomorphism over a normal object $B$ is normal, 

1. the [[over topos]] (see there) $PSh(\Omega)_{/B}$ may be identified with presheaves on the slice site

   $$
     PSh(\Omega)_{/B} \simeq PSh(\Omega_{/B})
     \,.
   $$

Therefore for normal $B$ the slice $dSet_{/B}$, as opposed to $dSet$ itself, has a chance to carry a [[Cisinski model structure]]. And this is indeed the case: one checks that

* $J \otimes (-)$ is a _functorial cyclinder_ in the sense of _[this definition](http://ncatlab.org/nlab/show/Cisinski+model+structure#FunctorialCylinder)_;

* the class of $J$-anodyne extensions is a class of corresponding anodyne extensions in the sense of _[this definition](http://ncatlab.org/nlab/show/Cisinski+model+structure#AnodyneExtensions)_

* so that together these form a _homotopical structure_ on $dSet_{/B}$ in the sense of _[this definition](http://ncatlab.org/nlab/show/Cisinski+model+structure#HomotopicalStructure)_.

The statement then is a special case of _[this theorem](http://ncatlab.org/nlab/show/Cisinski+model+structure#ModelStructureFromHomotopicalStructure)_ at _[[Cisinski model structure]]_.

=--



Let $E_\infty \in dSet$ be any normal dendroidal set such that the terminal morphism $E_\infty \to *$ is an acyclic fibration in that it has the [[right lifting property]] against the tree boundary inclusions.

By the general discussion at [[over topos]] we have an [[adjunction]]

$$
  (p_! \dashv p^*)
  \,.
  dSet
    \stackrel{\overset{p_!}{\leftarrow}}{\underset{p^*}{\to}}
  dSet_{/E_\infty}
  \,,
$$

where $p_!$ simply forgets the map to $E_\infty$ and where $p^*$ forms the [[product]] with $E_\infty$ 

+-- {: .num_prop #TransferOfTheModelStructure}
###### Proposition

The _[[transferred model structure]]_ on $dSet$ along the [[right adjoint]] $p^*$ of the model structure from prop. \ref{ModelStructureOnSlices} exists.

This is the model structure characterized in theorem \ref{TheModelStructureExistenceAndBasicProperties}.

=--

This appears as ([Cis-Moer, prop. 3.12](#CisinskiMoerdijk09)).


So far this establishes the existence of the model structure and that every dendroidal inner Kan complex is fibrant. Below in _[characterization of the fibrant objects](#CharacterizationOfTheFibrantObjects)_ we consider the converse statement: that the fibrant objects are precisely the inner Kan complexes.

#### Characterization of the fibrations
 {#CharacterizationOfTheFibrantObjects}

+-- {: .num_prop }
###### Proposition

A dendroidal set is $J$-fibrant, def. \ref{JFibrations}, hence fibrant in $dSet_{CM}$, precisely if it is an inner Kan complex.

A morphism $f : X \to Y$ in $dSet$ between inner Kan complexes is a $J$-fibration, hence a fibration in $dSet_{CM}$, precisely if 

1. it is an [[inner Kan fibration]];

1. on [[homotopy categories]] $\tau i^* f$ is an [[isofibration]].

=--

This is ([Cisinski Moerdijk, theorem 5.10](#CisinskiMoerdijk09)).



### Monoidal model category structure
 {#MonoidalModelCategoryStructure}

+-- {: .num_prop }
###### Proposition 

With respect to the [[Boardman-Vogt tensor product]] on [[dendroidal sets]], the model structure $dSet_{CM}$ is a [[symmetric monoidal category|symmetric]] [[monoidal model category]].

=--

This is ([Cis-Moer, prop. 3.17](#CisinskiMoerdijk09)).

+-- {: .num_cor #EnrichmentOverItself}
###### Corollary

With respect to the [[internal hom]] corresponding to the [[Boardman-Vogt tensor product]], $dSet_{CM}$ is a $dSet_{CM}$-[[enriched model category]].

=--


### Other enrichments of the underlying category
 {#Enrichment}

+-- {: .num_prop }
###### Proposition 
**(compatibility with the Joyal model structure)**

Let $|$ be the tree with a single leaf and no vertex. Then the [[overcategory]] $dSet/\Omega[|]$ is canonically isomorphic to [[sSet]].

The model structure on [[sSet]] induced this way as the [[model structure on an overcategory]] from the model structure on $dSet$ coincides with the 
[[model structure for quasi-categories]].

=--


This is for instance ([Moerdijk, proposition 8.4.3](#Moerdijk)).



+-- {: .num_prop }
###### Proposition

This model category is naturally an $sSet_{Joyal}$-[[enriched model category]], where
$sSet_{Joyal}$ is the [[model structure for quasi-categories]].

=--

+-- {: .proof}
###### Proof


This follows from the fact, cor. \ref{EnrichmentOverItself}, that $dSet_{CM}$ is a [[monoidal model category]]
and the fact that the 
functor $i^*: dSet \to sSet_{Joyal}$ is a [[right Quillen functor]].

=--

+-- {: .num_remark }
###### Remark

However, $dSet_{CM}$ is _not_ an [[enriched model category]] over $sSet_{Quillen}$, the _standard_ [[model structure on simplicial sets]] (but see _[[model structure for dendroidal Cartesian fibrations]]_). But it comes close, as the following propositions show. 

=--

+-- {: .num_defn }
###### Definition

Write

$$
  \mathcal{Hom} : dSet^{op} \times dSet \to dSet
$$

for the [[internal hom]] corresponding to the [[Boardman-Vogt tensor product]]. 

For $A$ normal and $X$ an inner Kan dendroidal set, write

$$
  \mathcal{hom}(A,X) := i^* \mathcal{Hom}(A,X)
$$

for the underlying [[quasi-category]], and write

$$
  k(A,X) := Core(\mathcal{hom}(A,X)) \in KanCplx
$$

for the maximal [[Kan complex]] inside the [[quasi-category]] inside the [[internal hom]].

Write 

$$
  -^{(-)} : sSet^{op} \times dSet \to dSet
$$

for the corresponding [[powering]], characterized by the existence of a 
[[natural isomorphism]]

$$
  Hom_{sSet}(K, k(A,X)) \simeq Hom_{dSet}(A, X^{(K)})
  \,.
$$

=--


+-- {: .num_prop }
###### Proposition

For $p : X \to Y$ a fibration between fibrant dendroidal sets (hence an [[inner Kan fibration]] and an [[isofibration]] on the underlying [[homotopy category]]), and for $A \to B$ a normal monomorphism, the induced morphism

$$
  k(B,X) \to k(B,Y) \times_{k(A,Y)} k(A,X)
$$

is a [[Kan fibration]] between [[Kan complexes]].

=--

This is  ([Cis-Moer, prop. 6.7](#CisinskiMoerdijk09)).

+-- {: .num_prop }
###### Proposition

If $A \to B$ is the above is an [[anodyne extension]] (acyclic monomorphism) of simplicial sets, then 

$$
  X^{(B)} \to Y^{(B)} \times_{Y^{(A)}} X^{(A)}
$$

is an acyclic fibration in $dSet_{CM}$.
=--

This is  ([Cis-Moer, cor. 6.9](#CisinskiMoerdijk09)).

+-- {: .num_prop }
###### Proposition

For $A$ normal and $X$ fibrant, the Kan complex 

$$
  k(A,X)
  \simeq
  \mathbb{R}Hom(A,X)
$$ 

is the correct
[[derived hom-space]] of $dSet_{CM}$.

=--

+-- {: .proof}
###### Proof

One checks that $n \mapsto X^{(\Delta[n])}$ is a fibrant resolution of
$X$ in the [[Reedy model structure]] $[\Delta^{op}, dSet_{CM}]_{Reedy}$.
By the discussion at _[[simplicial model category]]_ and _[[derived hom-space]]_ the latter is therefore given by the simplicial set

$$
  n \mapsto Hom_{dSet}(A, X^{(\Delta[n])})
  \,.
$$

By the [[tensoring]]-definition of $X^{(\Delta[n])}$ this is isomorphic to

$$
  \cdots = Hom_{sSet}(\Delta[n], k(A,X)) = k(A,X)_n
  \,.
$$

=--

### Relation to other model structures

We discuss the relation of the model structure on dendroidal sets to other model category structures for operads.

See the _[[table - models for (infinity,1)-operads]]_ for an overview.

#### Model structure for quasi-categories

+-- {: .num_proposition }
###### Proposition

The [[adjunction]]

$$
  (j_! \dashv j^*) : 
   dSet
    \stackrel{\overset{j_!}{\leftarrow}}{\underset{j^*}{\to}}
   sSet
$$

induced from the inclusion $j : \Delta \hookrightarrow \Omega$
constitutes a [[Quillen adjunction]]
between the above model structure on dendroidal sets, and the 
[[model structure for quasi-categories]].

=--

+-- {: .proof}
###### Proof

By the proof of ([Cisinski-Moerdijk, cor. 2.10](#CisinskiMoerdijk09)) the model structure for quasi-categories is in fact the restriction, along $j_!$, of the model structure on dendroidal sets. Therefore $j_!$ is left Quillen.

=--

#### Model structure for dendroidal complete Segal spaces
 {#RelationToModelStructureForDendroidalCompleteSegal}

There is a [[Quillen equivalence]] to the [[model structure for dendroidal complete Segal spaces]] (see there). A crucial step in the proof is the following expression of the acyclic cofibrations on $dSet_{CM}$ in terms of the dendroidal interval $J_d$ as follows.

+-- {: .num_prop}
###### Proposition

The class of acyclic cofibrations between normal dendroidal sets is the smallest
class of morphisms between normal dendroidal sets 

* which contains the $J$-anodyne extensions;

* with left cancellation property: if a composite $\stackrel{i}{\to} \stackrel{j}{\to}$ is in the class and $i$ is, then so is $j$.

=--

([Cis-Moer 09, prop. 3.16](#CisinskiMoerdijk09))

#### Model structure on simplicial operads
 {#RelationToModelStrictureOnSimplicialOperads}

There exists also a [[model structure on simplicial operads]], which is 
[[Quillen equivalence|Quillen equivalent]] to the model structure on dendroidal sets.

This Quillen equivalence is an operadic generalization of the Quillen equivalence between the [[model structure on sSet-categories]] and the [[model structure for quasi-categories]].


+-- {: .num_theorem}
###### Theorem

There exists an [[adjunction]]

$$  
  (W_! \dashv hcN_d) 
   : 
  sSet Operad 
    \stackrel{\overset{W_!}{\leftarrow}}{\underset{hcN_d}{\to}}
  dSet 
  \,,
$$

Whise [[right adjoint]] is the [[dendroidal homotopy coherent nerve]].

This is a [[Quillen equivalence]] between the model structure on dendroidal sets, and the [[model structure on simplicial operads]].


=--

This is  ([Cisinski-Moerdijk 11, theorem 815](#CisinskiMoerdijk11)).

+-- {: .num_remark}
###### Remark

Under the inclusions (see the discussion at _[[dendroidal set]]_)

$$
  \array{
     sSet Cat &\hookrightarrow & sSet Operad
     \\
     && {}^{\mathllap{hcN_d}}\downarrow \uparrow^{\mathrlap{W_!}}
     \\
     sSet \simeq dSet/\eta &\hookrightarrow & dSet
  }
$$

this restricts to the Quillen equivalence 
between the
[[model structure on sSet-categories]] and the [[model structure for quasi-categories]] discussed at _[[relation between quasi-categories and simplicial categories]]_.

=--

#### Model structure on $Set$-Operads

+-- {: .num_remark}
###### Remark

Write [[Operad]] for the category of [[symmetric operads]] over [[Set]].

The [[dendroidal set|dendroidal nerve adjunction]]

$$
  (\tau_d \dashv N_d) : 
  Operad
   \stackrel{\overset{\tau_d}{\leftarrow}}{\underset{N_d}{\to}}
  dSet
$$

is a [[Quillen adjunction]] between the model structure on dendroidal sets, def. \ref{ModelStructureOnDendroidalSets}, and the [[canonical model structure on Operad]].

Moreover, $N_d$ detects and preserves weak equivalences, while $\tau_d$ preserves weak equivalences.

=--

This is ([Cisinski-Moerdijk 09, prop. 2.5](#CisinskiMoerdijk09)).

#### Model structure for symmetric monoidal $(\infty,1)$-categories

+-- {: .num_prop}
###### Proposition

There is a [[Quillen adjunction]]

$$
  dSet_{CM}
   \stackrel{\overset{id}{\leftarrow}}{\underset{id}{\to}}
  dSet_{He}
$$

which exhibits the [[model structure for dendroidal left fibrations]] as a [[Bousfield localization of model categories|left Bousfield localization]] of the Cisinski-Moerdijk model structure on dendroidal sets.

=--

See ([Heuts, remark 6.8.0.2](#Heuts)).

## Related concepts

* [[canonical model structure on Operad]],

* [[model structure on operads]]

* [[model structure for dendroidal complete Segal spaces]]

* [[table - models for (infinity,1)-operads]]

## References


A useful discussion of of the model structure on dendroidal sets is section 8 of

* [[Ieke Moerdijk]], _Lectures on dendroidal sets_ , lectures given at the Barcelona workshop on _[Simplicial methods in higher categories](http://www.crm.es/HigherCategories/)_ (2008) ([preliminary writeup](http://www.crm.es/Publications/quaderns/Quadern45-1.pdf))
 {#Moerdijk}

An expanded and polished version has meanwhile been written up by Javier Guiti&#233;rrez and should appear in print soon. An electronic copy is probably available on request.

The model structure was originally given in 

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets as models for homotopy operads_ ([arXiv:0902.1954](http://arxiv.org/abs/0902.1954))
 {#CisinskiMoerdijk09}

making heavy use of results on [[Cisinski model structures]] from 

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski}

A detailed discussion of the fibrant objects in the model structure is in

* [[Ieke Moerdijk]] [[Ittay Weiss]], _On inner Kan complexes in the category of dendroidal sets_ ([web](http://www.sciencedirect.com/science?_ob=ArticleURL&_udi=B6W9F-4VM2KC8-1&_user=457046&_rdoc=1&_fmt=&_orig=search&_sort=d&_docanchor=&view=c&_searchStrId=1115574112&_rerunOrigin=google&_acct=C000021878&_version=1&_urlVersion=0&_userid=457046&md5=5eb2307e02ed1aa9e6fe2c7809346546))

The proof of the Quillen equivalence between the model structure on dendroidal sets and that on $sSet$-operads is given in 

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets and simplicial operads_ ([arXiv:1109.1004](http://arxiv.org/abs/1109.1004))
 {#CisinskiMoerdijk11}

The relation to the [[model structure for dendroidal Cartesian fibrations]] and the [[model structure for dendroidal left fibrations]] is discussed in 

* [[Gijs Heuts]], _Algebras over infinity-Operads_ ([arXiv:1110.1776](http://arxiv.org/abs/1110.1776))

