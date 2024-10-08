
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _$Q$-category_ is nothing but a [[coreflective subcategory]] and a _$Q^\circ$-category_ is nothing but a [[reflective subcategory]]. Since both of these encode (co)reflective [[localization]]s, following [Rosenberg](#Rosenberg) the "Q" is for _quotient_ and is (in a manner of a [[concept with an attitude]]) to indicate that in this context one is interested in notions similar to, but different from, the standard notion of [[sheaves]]:

for $\mathbb{A} := (A \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}} \bar A)$ a $Q^\circ$-category there is canonically induced a quadruple of [[adjoint functor]]s between the corresponding [[presheaf categories]]

$$
  PSh(\bar A)
   \stackrel{\overset{u_!}{\to}}{\stackrel{}{\stackrel{\overset{u^*}{\leftarrow}}{\stackrel{\overset{u_*}{\to}}{\underset{u^!}{\leftarrow}}}}}
  PSh(A) 
$$

and a presheaf $F \in PSh(A)$ is called an _$\mathbb{A}$-sheaf_ if the canonical morphism

$$
  u^* F \to u^! F
$$

is an [[isomorphism]] in $PSh(\bar A)$. More generally, there are generalizations of this condition where presheaves of sets can be replaced with presheaves with values in other categories, notably in [[abelian categories]].

In a central motivating class of examples $\mathbb{A}$ is a category of [[sieve]]s on objects in a [[small category]] $C$ that are regarded as being [[covering]] but which do not necessarily satisfy the axioms of a [[Grothendieck topology]] and not even of a [[coverage]].


## Motivation

The [[Yoneda embedding]] is continuous but not cocontinuous functor. Hence the Grothendieck topologies are used to define smaller codomain of Yoneda, a sheaf subcategory of the category of presheaves such that for that [[corestriction|corestricted]] Yoneda embedding (into sheaves) a desired class of covering cones will stay covering cones. More general families of diagrams than the sieves of a Grothendieck topology may be involved in achieving this. The important properties of the categories of diagrams for doing the sheaf theory can be expressed in terms of an adjoint pair of functors; this adjoint pair gives an example of a $Q$-category. This generalization of sheaf theory can rephrase categorically also properties like formal smoothness and formal etaleness of functors. The sheafification and the construction of a Gabriel localization of an Abelian category can in this formalism be seen as special cases of the same construction. 

## Definition

+-- {: .num_defn #QCategory}
###### Definition

An __almost quotient category__, or a __$Q$-category__ is 

* a pair of [[adjoint functor]]s

  $$
    \mathbb{A} : (u^* \dashv u_*) :  \bar A \stackrel{\overset{u^*}{\leftarrow}}{\underset{u_*}{\to}} A
    \,,
  $$

  with $u^*$ the [[left adjoint]];

* such that $u^*$ is [[full and faithful functor|full and faithful]] 

In other words, $A$ is equipped with an equivalence with a [[coreflective subcategory]] of $\bar{A}$. 

=--

+-- {: .num_note #QTerminology}
###### Note

* In motivating classes of examples $\bar A$ and $A$ are [[topos]]es and $\mathbb{A}$ is a [[geometric morphism]] between them. Therefore one generally speaks of $u_*$ as the **[[direct image]]** and of $u^*$ as the **[[inverse image]]** of the Q-category.

* The definition \ref{QCategory} is nothing but the definition of a [[coreflective subcategory]]. However the term _$Q$-category_ is used when the pair is used in a specific meaning useful to constructions in (generalized) sheaf theory (similarly like presheaf of objects in $D$ and contravariant functor to $D$ are synonyms, but a different word refers to a different context and intuition).

* One sometimes write the above data as $\bar A \stackrel{\overset{u}{\leftarrow}}{\to} A$. 

=--

+-- {: .num_defn #QCategoryMorphism}
###### Definition


A __[[morphism]] of Q-categories__ from 
$\mathbb{A} : (u^* \dashv u_*) :  \bar A \stackrel{\overset{u^*}{\leftarrow}}{\underset{u_*}{\to}} A$ to $\mathbb{B} : (v^* \dashv v_*) :  \bar B \stackrel{\overset{v^*}{\leftarrow}}{\underset{v_*}{\to}} B$ is a triple $(\Phi,\bar{\Phi},\phi)$ where $\Phi : A\to B$, $\bar{\Phi}:\bar{A}\to\bar{B}$ are functors and $\phi:\Phi u_*\Rightarrow v_*\bar{\Phi}$ is a [[natural isomorphism]] of functors. The composition is given by
$$
(\Phi,\bar{\Phi},\phi)\circ(\Phi',\bar{\Phi}',\phi') = (\Phi\Phi',\bar{\Phi}\bar{\Phi}',\phi\bar{\Phi}' \circ \Phi\phi')
$$

A __transformation of morphisms of Q-categories__ is a pair $(\alpha,\bar{\alpha}):(\Phi,\bar{\Phi},\phi)\to (\Psi,\bar{\Psi},\psi)$ of [[natural transformation]]s $\alpha:\Phi\to\Psi$ and $\bar{\alpha}:\bar{\Phi}\to\bar{\Psi}$ such that the diagram
$$\array{
\Phi u_* & \stackrel{\phi}\longrightarrow & v_* \bar{\Psi}\\
\alpha u_*\downarrow && \downarrow v_*\bar{\alpha}\\
\Psi u_* &\stackrel{\psi}\longrightarrow& v_* \bar{\Psi}

}$$
[[commuting diagram|commutes]].

=--

Small Q-categories, morphisms of Q-categories and natural transformations of morphisms form a [[2-category]] of small Q-categories.

+-- {: .num_defn #QopCategory}
###### Definition

A $Q^\circ$-category is a pair of functors $Q: A\leftrightarrow\bar{A}: I$,
where $Q$ is fully faithful and right adjoint to $I$. In other words, $A$ is equipped with an equivalence with a [[reflective subcategory]] of $\bar{A}$.

=--


## Examples


### (Co)Presheaves on a $Q$-category
 {#PresheafQCategory}

The [[category of presheaves]] over any $Q$-category canonically inherits itself the structure of a Q-category. 

+-- {: .num_prop #PresheafQCategories}
###### Proposition

Let $\mathbb{A} = \bar A \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} A$ be a $Q$-category. 
Let $C$ be any category.

Then forming [[copresheaves]] with values in $C$ yields a Q-category of the form

$$
  [\mathbb{A},C] :
   [\bar A, C]
     \stackrel{\overset{C^R = (-)\circ R}{\leftarrow}}{\underset{C^L = (-)\circ L}{\to}}
   [A,C]
  \,.
$$


=--

+-- {: .proof}
###### Proof

The $(C^R \dashv C^L)$-[[unit of an adjunction|unit]] is $C^\eta$  induced by the original unit $\eta: 1_A\to R L$

$$
  C^{\eta} : Id_{C^A} \to C^L \circ C^R = C^{R L}
$$ 

and the counit $C^\epsilon$ is induced by the original counit $\epsilon: L R\to 1_{\bar{A}}$

$$
  C^\epsilon : C^R\circ C^L = C^{L R}\to Id_{C^{\bar{A}}}
  \,.
$$ 

The only thing is who is adjoint -- now $C^R$ is the left adjoint. 

The triangle identities for $C^R\dashv C^L$ can be obtained by expanding.  For $R: \bar{A}\to A$, one has $C^R : C^A\to C^{\bar{A}}$ is given by $C^R : G\mapsto GR$, and for $L:A\to\bar{A}$ one has $C^L:F\mapsto F L$. Then $C^\eta : Id_{C^A}\to C^R C^L = C^{LR}$ has the components $(C^\eta)_G : (Id_{C^A})(G) \Rightarrow C^R C^L (G)$ given by $G \eta : G\to G L R$. Thus for each functor $G\in C^{\bar{A}}$, the composition

$$G R\stackrel{G\eta R}\longrightarrow G R L R \stackrel{G R \eta}\longrightarrow G R$$

is the identity by the triangle identity for $L\dashv R$, but this is precisely the $G$-component of the transformation 

$$
C^R \stackrel{C^R C^\eta}\longrightarrow C^R C^L C^R \stackrel{C^\epsilon C^R}\longrightarrow C^R.
$$
 
Similarly the $F$-component of 

$$
C^{L} \stackrel{C^\eta C^L}\longrightarrow C^L C^R C^L \stackrel{C^L C^\epsilon}\longrightarrow C^L,
$$

for a functor $F\in C^A$ reads 

$$ F L \stackrel{F L \eta}\longrightarrow F L R L  \stackrel{F \epsilon L}\longrightarrow F L $$

and this composition equals $Id_{F L}$ by another triangle identity for $L\dashv R$.

It is clear that if $\eta$ is iso then the composition with $\eta$ is also iso. Thus we obtain a $Q$-categories.

In other words, since the [[left adjoint]] being a [[full and faithful functor]] is equivalent to the unit of the [[adjunction]] being an [[isomorphism]], it follows from $L$ being full and faithful that $C^R$ is full and faithful.

=--

This appears as ([Kontsevich-Rosenberg, 2.7](#KontsevichRosenbergSpaces)).

+-- {: .num_note #ExtraAdjointsForPresheafQCategories}
###### Note

Assume in the context of prop. \ref{PresheafQCategories} that

* $A$ and $\bar A$ are [[small categories]];

* $C$ has all small [[limit]]s and [[colimit]]s (for instance $C$ = [[Set]]).

Then there is an [[adjoint quadruple]]

$$
  (u_! \dashv u^* \dashv u_* \dashv u^!) : 
  [\bar A, C]
    \stackrel{\overset{u_! = Lan R}{\to}}{\stackrel{\overset{u^* = C^R}{\leftarrow}}{\stackrel{\overset{u_* = C^L}{\to}}{\underset{u^! = Ran L}{\leftarrow}}}}
  [A,C]
  \,,
$$

where $Lan R$ denotes the left [[Kan extension]] along $R$ and $Ran L$ the right Kan extension along $L$.

=--

+-- {: .proof}
###### Proof

By general properties of [[Kan extension]]s.

=--

+-- {: .num_defn #SubcategoryOfPresheafQCategories}
###### Proposition

Any subcategory $B\subset C^{\bar{A}}$ containing $Im(C^R)$ determines a Q-subcategory $C^A\leftrightarrow B$. 

=--

### Domain and codomain fibration 
 {#DomainAndCodomainFibration}

+-- {: .num_defn #DomainAndCodomainFibration}
###### Proposition

For any [[category]] $A$, write $\bar A := A^I$ for its [[arrow category]].
This comes equipped with the [[codomain fibration]] $cod : \bar A \to A$ and the [[domain cofibration]] $dom : \bar A \to A$. Both have a joint [[section]] $\epsilon : A \to \bar A$ by a [[full and faithful functor]] that assigns identity morphisms. These form a triple of [[adjoint functor]]s

$$
  (codom \dashv \epsilon \dashv dom) :
  A^I
    \stackrel{\overset{codom}{\to}}{\stackrel{\overset{\epsilon}{\leftarrow}}{\underset{dom}{\to}}}
  A
  \,.
$$


Taking this apart, we have that

$$
  A^{dom} : A^I \stackrel{\overset{\epsilon}{\leftarrow}}{\underset{dom}{\to}}
  A
$$

is a $Q$-category and 

$$
  A^{dom} : A^I
    \stackrel{\overset{cod}{\to}}{\underset{\epsilon}{\leftarrow}}
  A
$$

is a $Q^o$-category.

=--

This appears as ([Kontsevich-Rosenberg, 2.5](#KontsevichRosenbergSpaces)).

Several classes of examples of Q-categories of interest arise as sub-Q-categories of those of this form. For instance the Q-categories of infinitesimal thickenings [below](#InfinitesimalThickening).

+-- {: .num_note #PresheavesOnCodomainFibration}
###### Note

Passing to copresheaf Q-categories as in prop. \ref{PresheafQCategories}
we have the Q-category

$$
  [A^I,Set]
   \stackrel{\overset{u^* = (-)\circ dom}{\leftarrow}}{\stackrel{\overset{u_* = (-)\circ \epsilon}{\to}}{\overset{u^! = (-)\circ codom}{\leftarrow}}}
  [A,Set]
$$

where the extra [[right adjoint]] is given by precomposition with the domain evaluation.



=--


### Q-category of cones

Let $C$ be a category and $LC$ be the category whose objects are [[cones]] $\alpha: x\to d$ over (small) diagrams $d: D\to C$ where $D$ are variable small categories; and the morphisms from $x\stackrel{\alpha}\to d$ to $x'\stackrel{\alpha'}\to d'$ are triples of the form $(f,\rho,\bar{f})$ where $f:x\to x'$ is a morphism in $C$, $\rho : D' \to D$ is a diagram (= functor), and $\bar{f}:d \circ\rho \to d'$ is a morphism of diagrams (= natural transformation) such that 
$$\array{
x & \stackrel{f}\to & x'\\
\alpha \star\rho \downarrow && \downarrow\alpha'\\
d \circ \rho&\stackrel{\bar{f}}\to & d' 
}$$
commutes and $\alpha \star \rho$ denotes the horizontal composition (= [[Godement product]]) of natural transformations. 

Then one defines composition of morphisms by the formula
$$
(f_1, \rho_1,\bar{f_1})\circ(f_2, \rho_2,\bar{f_2})
\stackrel{def}{=}(f_1\circ f_2, \rho_2\circ\rho_1, \bar{f_1} \circ (\bar{f_2} \star \rho_1)).
$$

There is a fully faithful functor $Q_C:C\to LC$ that to any $x\in C$ assigns the trivial cone $id_x :x\to x$ and to any morphism the corresponding morphism of trivial cones. Its right adjoint is the morphism $I_C:LC\to C$ defined by sending the cone $\alpha: x\to d$ over a diagram $d:D\to C$ its vertex $x$ and to a cone morphism $(f,\rho,\bar{f})$, the morphism of vertices $f$. Then $I_C\circ Q_C = Id_C$. The identity transformation can be thus taken as the unit of the adjunction. The counit of the adjunction $\epsilon: Q_C\circ I_C \to Id_{LC}$ is constructed as follows: to a cone $\alpha:x\to d$ assign the morphism $(1_x, const, \alpha)$ where $const: D\to C$ is the constant diagram which is the unique diagram from $D = dom(d)$ to the final category $1=\{\star\}$. One can check that these data indeed define an adjoint pair $Q_C\dashv I_C$ of functors. 
$Q_C: C\leftrightarrow I_C: LC$ is therefore a Q-category, and it is called the __Q-category of cones__. 

If $\mathcal{L}\subset Cat$ is a family of small categories, then one considers the full subcategory $L_{\mathcal{L}}C$ of cones whose domains are in $\mathcal{L}$; the rest of the construction restricts to obtain a Q-category $Q^{\mathcal{L}}_C : C\leftrightarrow L_{\mathcal{L}}C : I_C^{\mathcal{L}}$. 

The most classical case is when $\mathcal{L}$ is the (say skeletal) category $Dis$ of small discrete categories (=just identity morphisms), one obtains then the Q-category $Q^{Dis}_C: C\leftrightarrow L_{Dis}C$. 
A __semicosite__ (or semicositus pl. semicositi) is a Q-category of the form $C\leftrightarrow \bar{C}$ where $\bar{C}$ is a full subcategory of $L_{Dis}C$ and the adjoint pair is obtained by the restriction. A semicosite is a __precosite__ (=Grothendieck precotopology) if 

(i) $id_x\in Ob(\bar{C})$ whenever $x\in Ob(C)$.

(ii) $\{x\stackrel{\phi_i}\to x_i\}_{i\in I}\in Ob(\bar{C})$ and $\{x_i\stackrel{\phi_{ij}}\to x_{ij}\}_{j\in J_i}\in Ob(\bar{C})$ then $\{x\stackrel{\phi_{ij}\circ\phi_i}\to x_{ij}\}\in Ob(\bar{C})$

(iii) $\{x\to x_i\}_{i\in I}\in Ob(\bar{C})$ and $g\in C(x,y)$, then the family of pushouts $\{y\mapsto x_i\coprod_x y\}_{i\in I}$ exists and belongs to $Ob(\bar{C})$.

An example of a cosite is a cosite of closed sets of a topological space. 


### Sieves



The $Q$-category of [[sieves]].

The $Q$-subcategory of the $Q$-category of (all) sieves corresponding to the subcategory of sieves corresponding to the Grothendieck topology...

(needs explanation)

### The Q-category factoring a fully faithful factor

Any fully faithful functor among small categories $F: A\to B$ factors canonically into the composition $A\stackrel{u^*}\to \bar{A}\hookrightarrow B$ where $\bar{A}\subset B$ is the full subcategory of $B$ whose objects are all $b$ in $Ob B$ such that $a\mapsto B(F(a),b)$ is a representable functor $A^{op}\to Set$, and $u^*$ is the [[corestriction]] of $F$ to $\bar{A}$. This corestriction makes sense: $F$ is fully faithful, hence $B(F(a),F(a)) = B(a,a)$, i.e. $F(a)\in \bar{A}$ for all $a$ in $Ob A$. For each $b\in \bar{A}$, define now $u_*(b)$ as the functor representing $B(F(-),b)$, i.e. by $\bar{A}(u^*(a),b) = B(F(a),b) \cong B(a,u_*(b))$
(KR NcSpaces A1.1.1). This relation on objects extends to an adjunction $u^*\dashv u_*$ with $u^*$ fully faithful. 


### Quasi-(co)-sites

(...)

+-- {: .num_defn #QuasiCoSite}
###### Definition

Let $A$ be a [[category]] and $\mathcal{T}$ a map that assigns to every [[object]] a collection of co[[sieve]]s on that object ([[subfunctor]]s of $A(x,-)$), which includes maximal cosieve (functor $A(x,-)$).

Write $\bar A_{\mathcal{T}}$ for the category whose objects are co[[sieve]]s on $A$, and whose morphisms are morphisms in $A$ that respect the corresponding cosieves. This yields a Q-category

$$
  \bar A_{\mathcal{T}}
   \stackrel{\leftarrow}{\to}
  A
  \,.
$$

Call this a **quasi-cosite** if

1. for any two cosieves in $\mathcal{T}$ their intersection is also in $\mathcal{T}$;

1. for any cosive in $\mathcal{T}$ any cosieve containing it is also in $\mathcal{T}$.


=--

This is ([KontsevichRosenberg, 2.2](#KontsevichRosenberg)).

+-- {: .num_defn #QuasiCoSiteAssociatedToQCategory}
###### Definition

For any Q-category $\mathbb{A}$, the **quasi-cosite associated** with $\mathbb{A}$ is the Q-category $\mathcal{T}\mathbb{A}$ defined by...

=--

The following is supposed to be the standard quasi-cosite for non-commutative geometry.

+-- {: .num_defn #NCQuasiCosite}
###### Definition

Let $k$ be a [[ring]] and $A := Alg_k$ the category of [[associative algebra]]s over $k$. Let $\bar A \subset A^I$ be the [[full subcategory]] of the [domain fibration](DomainAndCodomainFibration) whose objects are the **faithfully flat** morphisms, i.e. those morphisms $\phi : R \to T$ in $Alg_k$ such that the induced

$$
  \phi^* : R Mod \to T Mod
$$

is an [[exact functor|exact]] and [[full and faithful functor]]. This forms a Q-category.

Write $\mathcal{T}Alg_k$ for the quasi-cosite associated with this Q-category by def. \ref{QuasiCoSiteAssociatedToQCategory}. This is the **standard quasi-cosite for [[noncommutative geometry]]**.

=--

This is ([KontsevichRosenberg, A.1.9.2](#KontsevichRosenberg)).


### Infinitesimal thickenings
 {#InfinitesimalThickening}

Generally, [[infinitesimal object|infinitesimal thickenings]] are characterized by [[coreflective subcategory|coreflective embeddings]]:

A characteristic property of an [[infinitesimally thickened point]] $D$ is that for any object $X$ without infinitesimal thickening, there are in general nontrivial morphisms $D \to X$, but there is only a unique morphism $X \to D$, reflecting the fact that $D$ has only a single global point. Thus if by $i : C \to \bar C$ we denote the inclusion of objects $X$ without infinitesimal thickening into the collection of possibly infinitesimally thickened objects, and by $p : \bar C \to C$ the projection that contracts away the infinitesimal extension, we have indeed an [[adjunction]]

$$
  \bar C(i(X), D) \simeq C(X, p(D)) \simeq C(X,*) \simeq *
  \,.
$$

This general concept is described at <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalNeighBourhoodSite">infinitesimal neighbourhood site</a>. See also the discussion below at [Relation to cohesive toposes](#RelationToCohesiveToposes).

The following is one realization of this general concept. 

+-- {: .num_prop #InfinitesimalThickening}
###### Proposition

Let $k$ be a [[field]] and $A := CAlg_k$ be the category of commutative [[associative algebra]]s over $k$. 

Let $\bar A \subset A^I$ be the [[full subcategory]] of the [[codomain fibration]] Q-category from prop. \ref{DomainAndCodomainFibration} on those morphisms of commutative algebras which are [[epimorphism]]s and whose [[kernel]] is nilpotent. Then

$$
  CAlg_k^{inf} = (\epsilon \dashv dom) : \bar A \stackrel{\overset{\epsilon}{\leftarrow}}{\underset{dom}{\to}} A
$$

is a Q-category.

The analogous statement is true with $A = Alg_k$ the category of all [[associative algebra]]s, not necessarily commutative.

=--

This appears as ([Kontsevich-Rosenberg, 2.6](#KontsevichRosenbergSpaces)).

+-- {: .num_remark #DiscussionOfTheInfinitesimalThickeningFormalization}
###### Remark

Here we think of an algebra epimorphism $\phi : \mathbf{B} \to B$ with nilpotent kernel -- an [[infinitesimal ring extension]] -- as the infinitesimal thickening of $Spec B$ by $Spec ker \phi$ to $Spec \mathbf{B}$.

The functor $\epsilon$ builds the trivial (empty) infinitesimal thickenings

$$
  \epsilon B : B \stackrel{id_B}{\to} B
  \,.
$$

The functor $dom$ remembers the _thickened_ algebra

$$
  dom (\mathbf{B} \to B) = \mathbf{B}
  \,.
$$

But notice that we also have the codomain-functor, which is the functor that forgets the thickening

$$
  cod (\mathbf{B} \to B) = B
$$

and that the [[adjoint pair]] $(\epsilon \dashv dom)$ does extend to an [[adjoint triple]]

$$
  CAlg_k^{inf} : \bar A \stackrel{\overset{cod}{\to}}{\stackrel{\overset{\epsilon}{\leftarrow}}{\underset{dom}{\to}}} A
  \,.
$$

In the discussion at <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">Infinitesimal cohesion</a> it is the pair $(cod \dashv \epsilon)$ that appears in the axiomatization, or rather its version on the opposite categories

$$
  (\epsilon^{op} \dashv cod^{op}) : \bar A^{op} \stackrel{\overset{\epsilon^{op}}{\leftarrow}}{\underset{cod^{op}}{\to}} A^{op}
  \,,
$$

not the other adjoint pair $(\epsilon \dashv dom)$ used here.

This is the reason for the shift in adjoint triples that is mentioned in <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos+--+infinitesimal+cohesion#RelationToRK">this remark</a> over at _[[cohesive (infinity,1)-topos -- infinitesimal cohesion|infinitesimal cohesion]]_ .

=--

## $\mathbb{A}$-Sheaves
  {#ASheaves}

We discuss the notion of a _$\mathbb{A}$-sheaves_ on a Q-category $\mathbb{A}$.


+-- {: .num_defn #BareSheafCondition}
###### Definition

Let $\mathbb{A} = (\bar A \stackrel{\overset{u^*}{\leftarrow}}{\underset{u_*}{\to}}A)$ be a [Q-category](#QCategory). An object $x \in A$ is called an **$\mathbb{A}$-sheaf** if for all $y \in \bar A$ the canonical morphism

$$
  \bar A(y, u^*(x)) \to A(u_*(y), x)
$$

is an [[isomorphism]] (in [[Set]], hence a [[bijection]]).

This morphism is given by

$$
  g \mapsto \eta_x^{-1} \circ u_*(g)
$$

where $\eta_x : x \to u_* u^*(x)$ is the $x$-component of the $(u^* \dashv u_*)$-[[unit of an adjunction|counit]] (which is an [[isomorphism]] because $u^*$ is a [[full and faithful functor]]).


=--

This appears as ([Kontsevich-Rosenberg, 3.1.1](#KontsevichRosenbergSpaces)).



+-- {: .num_prop #SheafConditionByExtraRightAdjoint}
###### Proposition

Let $\mathbb{A}$ be a Q-category with an extra [[right adjoint]] $u^! : A \to \bar A$

$$
  \mathbb{A}
  : 
  \bar A
    \stackrel{\overset{u^*}{\leftarrow}}{\stackrel{\overset{u_*}{\to}}{\underset{u^!}{\leftarrow}}}
  A
  \,.
$$

Then an object $x \in A$ is an $\mathbb{A}$-sheaf in the sense of def. \ref{BareSheafCondition} precisely if the canonical morphism

$$
  (u^*(x) \to u^!(x))
  :=
  u^*(X) 
    \stackrel{}{\to}
  u^! u_* u^* (x)
    \stackrel{\simeq}{\to}
  u^! (x)
$$

is an [[isomorphism]] in $\bar A$. 

=--

This appears as ([Kontsevich-Rosenberg, 3.1.3](#KontsevichRosenbergSpaces)).

For more details on the canonical morphism appearing here see the section <a href="http://nlab.mathforge.org/nlab/show/cohesive+topos#AdjointQuadruples">Adjoint quadruples</a> at [[cohesive topos]].

+-- {: .proof}
###### Proof

Using the $(u_* \dashv u^!)$-[[adjunction]]-[[isomorphism]] we have that the canonical morphism from def. \ref{BareSheafCondition} is isomorphic to

$$
  \phi : \bar A(y, u^* x) \to A(u_* y, x) \stackrel{\simeq}{\to}
   \bar A(y, u^! x)
  \,,
$$

for all $y \in \bar A$, where the second map sends every morphism to its [[adjunct]]. Using the definition of the first morphism from def. \ref{BareSheafCondition} and the expression of [[adjunct]]s (as discussed there) by composition with (co)-units, we find that the composite map here sends any morphism

$$
  g : y \to u^* x
$$

to the composite

$$
  \array{
     y 
     \\
     \downarrow
     \\
     u^! u_* y &\stackrel{u^! u_* g}{\to}& u^! u_* u^* x
     \\
     && \downarrow
     \\
     && u^! x
  }
  \,.
$$

Using that [[unit of an adjunction|adjunction units]] are [[natural transformation]]s, we can complete this to a [[commuting diagram]]

$$
  \array{
     y &\stackrel{g}{\to}& u^* x
     \\
     \downarrow && \downarrow
     \\
     u^! u_* y &\stackrel{u^! u_* g}{\to}& u^! u_* u^* x
     \\
     && \downarrow
     \\
     && u^! x
  }
  \,.
$$

This shows that $\phi$ acts on any $g$ by postcomposition with the canonical morphism $u^* x \to u^! x$. By the [[Yoneda lemma]] it follows that $\phi$ is an [[isomorphism]] for all $y$ precisely if $u^* x \to u^!$ is an isomorphism.

=--

+-- {: .num_def #MonoAndEpiPresheaves}
###### Definition

Let $\mathbb{A} = (u^* \dashv u_* \dashv u^!): \bar A \to A$ be a  Q-category with an extra right adjoint as in prop. \ref{SheafConditionByExtraRightAdjoint}.

We say

* an object $x \in A$ is **$\mathbb{A}$-monopresheaf** if $u^* x \to u^! x$ is a [[monomorphism]] in $\bar A$.

* an object $x \in A$ is **$\mathbb{A}$-epipresheaf** if $u^* x \to u^! x$ is an [[strict epimorphism]] in $\bar A$.

=--

This appears as [Kontsevich-Rosenberg, 3.1.2, 3.1.4](#KontsevichRosenbergSpaces).


+-- {: .num_note #PresheafSheafCondition}
###### Note

Let $\mathbb{A} : \bar A \stackrel{\overset{u^*}{\leftarrow}}{\underset{u_*}{\to}} A$ be a Q-category where $A$ is a [[small category]], and let $C$ be a category with all small [[limit]]s. Then the Q-category of presheaves from prop \ref{PresheafQCategories} has an extra right adjoint $u^!_C := Ran_{u^*}$

$$
  C^{\mathbb{A}} : 
   C^{\bar A} 
    \stackrel{\overset{f^* := C^{u_*}}{\leftarrow}}{\stackrel{\underset{f_* := C^{u^*}}{\to}}{\underset{f^! := u^!_C}{\leftarrow}}}
   C^{A}
$$

given by the right [[Kan extension]] along $u^*$, which exists by the assumption that $C$ has all small limits.

Therefore by prop. \ref{SheafConditionByExtraRightAdjoint} a presheaf $F \in C^{A}$ is a $C^{\mathbb{A}}$-sheaf, def. \ref{BareSheafCondition}, precisely if the canonical morphism

$$
  f^* F \to f^! F
$$

is an [[isomorphism]].

=--

This appears as ([Kontsevich-Rosenberg, 3.5](#KontsevichRosenbergSpaces)).


## Examples


### Formal smoothness and $Alg_k^{inf}$-sheaves
 {#FormalSmoothness}

Let 

$$
  CAlg_k^{inf} : \bar A \stackrel{\overset{i}{\leftarrow}}{\underset{p}{\to}}
   CAlg_k
$$

be the Q-category of infinitesimal thickenings from prop. \ref{InfinitesimalThickening}. Write

$$
  [CAlg_k^{inf},Set] : [\bar A,Set] 
    \stackrel{\overset{u^*}{\leftarrow}}{\stackrel{\overset{u_*}{\to}}{\underset{u^!}{\leftarrow}}}  
  [CAlg_k,Set]  
$$

be the corresponding Q-category of copresheaves from prop. \ref{PresheafQCategories}. Notice that $[CAlg_k, Set]$ is the [[presheaf topos]] that contains [[scheme]]s over $k$. Recall the notion of 
[[formally smooth scheme]], [[formally étale morphism]] and
[[formally unramified morphism]] of schemes.


+-- {: .num_prop #FormalSmoothnessByASheaves}
###### Proposition

An object $X \in [CAlg_k, Set]$ is

* [[formally étale morphism|formally étale]] precisely if it is an $CAlg_k^{inf}$-sheaf in the sense of def. \ref{BareSheafCondition}, hence precisely if the canonical morphism

  $$
    u^* F \to u^! F
  $$

  from prop. \ref{SheafConditionByExtraRightAdjoint} is an [[isomorphism]];

* [[formally unramified]] precisely if it is a $CAlg_k^{inf}$ monopresheaf, def. \ref{MonoAndEpiPresheaves}, hence precisly if $u^* F \to u^! F$ is a [[monomorphism]];

* [[formally smooth]] precisely if it is a strict epipresheaf, def. \ref{MonoAndEpiPresheaves}, hence precisely if $u^* F \to u^! F$ is a [[strict epimorphism]].

=--

This appears as ([Kontsevich-Rosenberg, 4.1](#KontsevichRosenbergSpaces)).


This [[category theory|category theoretic]] reformulation of these three properties therefore admits straightforward generalization of these notions to other contexts. See the section <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalPaths">Infinitesimal paths</a> at [[cohesive (∞,1)-topos]].

For instance we have the following direct generalization is of interest in [[noncommutative geometry]].


+-- {: .num_defn #FormalNCSmoothnessByASheaves}
###### Definition

Let $Alg_k$ be the full category of [[associative algebra]]s over $k$, not necessarily commutative. Write $Alk_k^{inf} : \bar A \to Alg_k$ for the Q-category of infinitesimal thickenings as in def. \ref{InfinitesimalThickening}. Notice that $[Alg_k, Set]$ is the [[presheaf topos]] that contains [[noncommutative scheme]]s.


We then say an object $X \in [Alg_k, Set]$ is

* [[formally étale morphism|formally étale]] precisely if it is an $Alg_k^{inf}$-sheaf in the sense of def. \ref{BareSheafCondition}, hence precisely if the canonical morphism

  $$
    u^* F \to u^! F
  $$

  from prop. \ref{SheafConditionByExtraRightAdjoint} is an [[isomorphism]];

* [[unramified|formally unramified]] precisely if it is a $Alg_k^{inf}$ monopresheaf, hence precisly if $u^* F \to u^! F$ is a [[monomorphism]];

* [[formally smooth]] precisely if $u^* F \to u^! F$ is a [[strict epimorphism]].

=--

This appears as ([Kontsevich-Rosenberg, section 4.2](#KontsevichRosenbergSpaces)).

+-- {: .num_prop #CharacterizationOfFormalNCSmoothness}
###### Proposition

Let $R \in Alg_k$ and write $Spec R \in [Alg_k, Set]$ for the corresponding [[representable functor]]. We have that

1. $Spec R$ is an $Alg_k^{inf}$ epipresheaf (formally smooth) precisely if $R$ is Quillen-Cuntz quasi-free: the $R \otimes_k R^{op}$-[[module]] $\Omega^1_{R|k}$, being the [[kernel]] of the multiplication morphism

   $$
     \Omega^1_{R|k} := ker(R \otimes_k R \stackrel{mult}{\to} R)
     \,,
   $$

   is a [[projective object|projective]] in $R \otimes R^{op}$[[Mod]];

1. $Spec R$ is an $Alg_k^{inf}$-monopresheaf (formally unramified) precisely if $\Omega^1_{R|k} = 0$.

=--

This appears as ([Kontsevich-Rosenberg, prop. 4.3](#KontsevichRosenbergSpaces)).


## Relation to other concepts


### Relation to cohesive toposes
  {#RelationToCohesiveToposes}

If a Q-category $\mathbb{A}$ has the extra [[right adjoint]] of prop. \ref{SheafConditionByExtraRightAdjoint} and in addition an extra left adjoint to a total of a quadruple of [[adjoint functor]]s

$$
  \mathbb{A} : 
   \bar A
     \stackrel{\overset{u_!}{\to}}{\stackrel{\overset{u^*}{\leftarrow}}{\stackrel{\overset{u_*}{\rightarrow}}{\underset{u^!}{\leftarrow}}}}
   A
$$

then essential axioms characterizing a [[cohesive topos]] are satisfied, in particular if for instance $\bar A$ and $A$ are [[presheaf topos]]es as in \ref{PresheafQCategories} (this is considered around [Kontsevich-Rosenberg, 3.5.1](#KontsevichRosenbergSpaces)).

Notably in this case the canonical [[natural transformation]]

$$
  u^* \to u^!
$$

from prop. \ref{SheafConditionByExtraRightAdjoint} is the one appears in the axioms of a [[cohesive topos]]: if this transformation is a [[monomorphism]] in a cohesive topos -- hence if in the language of Q-categories all objects are monopresheaves -- one says that _discrete objects are concrete_ in the cohesive topos.

Moreover, due to the extra left adjoint $u_!$ there is a canonical dual morphism

$$
  u_* \to u_!
  \,.
$$ 

In ([Lawvere](#Lawvere)) is the suggestion that it is interesting to consider the full subcategory of $\bar A$ on which $u_* \to u_!$ is an isomorphism. This is dual to the statement of the above section on [A-Sheaves](#ASheaves) which asserts that it is interesting to consider the full subcategory of $A$ on which $u^* \to u^!$ is an isomorphism.

More concretely, the axioms of <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">Infinitesimal cohesion</a> are an abstraction of the situation of prop. \ref{InfinitesimalThickening}. In every cohesive $(\infty,1)$-topos equipped with an _infinitesimal neighbourhood_ there is an analog of the characterization of formal smoothness from prop. \ref{FormalSmoothnessByASheaves}. See the section <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalPaths">Infinitesimal paths and de Rham spaces</a>.


### Sheafification versus the Gabriel localization $G_{\mathcal{F}} = H^2_{\mathcal{F}}$

(...)

## References

The term _$Q$-category_ originally was short for _almost quotient category_ , presumably because of its role in the theory of [[Gabriel localization]]. The sheaf formalism in terms of $Q$-categories has been introduced in the mimeographed notes

* [[Alexander Rosenberg]], _Q-categories, sheaves and localization_, (in Russian) Seminar on supermanifolds __25__, Leites ed. Stockholms Universitet 1988 (there is a recent partial English translation)
 {#Rosenberg}

The formalism is used (and briefly surveyed) in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([[KontsevichRosenbergNCSpaces.pdf:file]], [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}

and also used in the general definition of "noncommutative" stacks in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative stacks_, preprint MPI-2004-37 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305))
 {#KontsevichRosenbergStacks}


The [[epipresheaf]] condition for the Q-category of nilpotent (infinitesimal) thickenings is in the Kontsevich-Rosenberg paper interpreted as [[formally smooth morphism|formal smoothness]] what is further studied in 

* [[T. Brzezinski]], _Notes on formal smoothness_, *in*: Modules and Comodules (series _Trends in Mathematics_). T Brzezi&#324;ski, JL Gomez Pardo, I Shestakov, PF Smith (eds), Birkh&#228;user, Basel, 2008, pp. 113--124 ([doi](http://dx.doi.org/10.1007/978-3-7643-8742-6), [arXiv:0710.5527](http://arxiv.org/abs/0710.5527))
 {#Brzezinski}

The condition that $u_* x \to u_! x$ is an isomorphism, dual to the condition for $\mathbb{A}$-sheaves considered above, has been considered in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories __19__:3, 2007, pp. 41--49 ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
{#Lawvere}


[[!redirects Q-categories]]