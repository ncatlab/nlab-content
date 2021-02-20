
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--



# Lawvere--Tierney topologies
* table of contents
{: toc}


## Idea

A _Lawvere--Tierney topology_ (or _operator_, or _[[modal logic|modality]]_, also called _[geometric modality](modal+type+theory#GeometricModality)_) on a [[topos]] is a way of saying that something is 'locally' [[true]].  Unlike a [[Grothendieck topology]], this is done directly at the stage of [[logic]], defining a _[[geometric logic]]_.  In fact, it is a generalisation of Grothendieck topology in this sense: If $C$ is a [[small category]], then choosing a Grothendieck topology on $C$ is equivalent to choosing a Lawvere--Tierney topology in the [[presheaf topos]] $\Set^{C^\op}$ on $C$.

The use of "topology" for this and the related Grothendieck concept is regarded by some people as unfortunate; see the [historical note](https://ncatlab.org/nlab/show/Grothendieck+topology#historical_note_on_terminology) at [[Grothendieck topology]] for some reasons why.  A proposed replacement for "Grothendieck topology" is [[coverage|(Grothendieck) coverage]]; see the afore-mentioned historical note for some possible replacements for "Lawvere--Tierney topology."


## Definition

Let $E$ be a [[topos]], with [[subobject classifier]] $\Omega$. 


### The closure operator

+-- {: .num_defn #LTTopologyDef}
###### Definition

A __Lawvere--Tierney topology__ in $E$ is ([[internalization|internally]]) a [[closure operator]] given by a [[exact functor|left exact]] [[idempotent monad]] on the internal meet-[[semilattice]] $\Omega$. 

This means that: a Lawvere--Tierney topology in $E$ is a [[morphism]] 

$$
  j: \Omega \to \Omega
$$ 

such that

1. $j true = true$, equivalently $\id_\Omega \leq j: \Omega \to \Omega$ ('if $p$ is true, then $p$ is locally true')

   $$
     \array{
       * &\stackrel{true}{\to}& \Omega
       \\
       & {}_{\mathllap{true}}\searrow & \downarrow^{\mathrlap{j}}
       \\
       && \Omega
     }
   $$

1. $j j = j$ ('$p$ is locally locally true iff $p$ is locally true');

   $$
     \array{
       \Omega &\stackrel{j}{\to}& \Omega
       \\
       & {}_{\mathllap{j}}\searrow & \downarrow^{\mathrlap{j}}
       \\
       && \Omega
     }
   $$

1. $j \circ \wedge = \wedge \circ (j \times j)$ ('$p \wedge q$ is locally true iff $p$ and $q$ are each locally true')

   $$
     \array{
       \Omega \times \Omega &\stackrel{\wedge}{\to}& \Omega
       \\
       {}^{\mathllap{j \times j}}\downarrow && \downarrow^{\mathrlap{j}}
       \\
       \Omega \times \Omega &\underset{\wedge}{\to}& \Omega
     }
     \,.
   $$

=--

Here $\leq$ is the internal [[partial order]] on $\Omega$, and $\wedge: \Omega \times \Omega \to \Omega$ is the internal [[meet]].

This appears for instance as ([MacLaneMoerdijk, V 1.](#MacLaneMoerdijk)).

+-- {: .num_remark #LTTopologyAsSubobject}
###### Remark

By the definition of [[subobject classifier]] $j$ is equivalently a [[subobject]]

$$
  J \hookrightarrow \Omega
$$

satisfying three conditions. This perspective gives the direct relation to [[Grothendieck topologies]], as discussed [below](RelationToGrothendieckTopology).

=--

+-- {: .num_remark}
###### Remark

Equivalently, the third axiom in def. \ref{LTTopologyDef} can be replaced with the (internal) statement that $j$ is order-preserving.

The equivalence amounts to the fact that, within the [[internal logic]] of [[topoi]], one can demonstrate that every [[monad]] on the [[preorder]] of [[truth values]] is in fact [[strong monad|strong]] (a special case of the fact that, for an [[endofunctor]] on some [[closed monoidal category|monoidal closed]] $V$, [[tensorial strength|tensorial strengths]] are the same as $V$-[[enriched category|enrichments]], as described in the article on the former), and therefore _automatically_ preserves finite meets. 

Thus, a Lawvere-Tierney topology is the same thing as an internal [[closure operator]] on the preorder $\Omega$ (aka, a [[Moore closure]] on the one-element set), which amounts to the same thing as a natural closure operator on subobjects.

Specifically, given any [[subobject]] inclusion $X \hookrightarrow Y$ in $E$, consider its [[characteristic morphism]] $\chi_X: Y \to \Omega$. Then $j \circ \chi_X$ is another morphism $Y \to \Omega$, which defines another subobject $j_*(X)$ of $Y$, taken as the closure of our original subobject. The elements of $j_*(X)$ are those elements of $Y$ that are 'locally' in $X$.

=--


+-- {: .num_defn #TheClosureOperator}
###### Definition

The **[[closure operator]]** induced by $j$ is the [[natural transformation|transformation]]

$$
  \overline{(-)}_X : Sub(X) \to Sub(X)
$$

on the [[subobject]] lattice of $X \in E$, [[natural transformation|natural]] in $X$, that is given by the [[commuting diagram]]

$$
  \array{
    Hom(X, \Omega) &\stackrel{\simeq}{\to}& Sub(X)
    \\
    {}^{\mathllap{Hom(1,j)}}\downarrow && \downarrow^{\mathrlap{\overline{(-)}}}
    \\
    Hom(X,\Omega) &\stackrel{\simeq}{\to}& Sub(X)
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This means that for $U \hookrightarrow X$ a [[subobject]], with characteristic morphism $char U : X \to \Omega$, its closure is the subobject classified by

$$
  char \overline{U} : X \stackrel{char U}{\to} \Omega \stackrel{j}{\to} \Omega
  \,.
$$

=--

This appears for instance as ([MacLaneMoerdijk, p. 220](
MacLaneMoerdijk)).

+-- {: .num_prop}
###### Proposition

A morphism $j : \Omega \to \Omega$ is a Lawvere-Tierney topology, def. \ref{LTTopologyDef} precisely if the corresponding closure operator, def. \ref{TheClosureOperator} satisfies for all $X, Y \in E$

1. $A \subset \overline{A}$;

1. $\overline{\overline{A}} = \overline{A}$;

1. $\overline{A \cap B} = \overline{A} \cap \overline{B}$.

=--

This appears as 
([MacLaneMoerdijk, V 1., prop 1](#MacLaneMoerdijk)).


### Sheaves

Using Lawvere--Tierney topologies, 
the notion of [[sheaf]] and [[sheafification]] generalizes from [[Grothendieck topos|Grothendieck topoi]] to arbitrary topoi. 

Let $E$ be a [[topos]] with Lawvere-Tierney topology $j$, def. \ref{LTTopologyDef} and associated closure operator $\overline{(-)} : Sub(-) \to Sub(-)$, def. \ref{TheClosureOperator}.

+-- {: .num_defn #DenseMonos}
###### Definition

A subobject $U \in Sub(X)$ is called **dense** if $\overline{U} = X$.

The corresponding [[monomorphism]] $U \hookrightarrow X$ is called a **[[dense monomorphism]]**.

=--

+-- {: .num_defn #JSheaf} 
###### Definition

An object $F \in E$ is called a **$j$-[[sheaf]]** if it is a [[local object]] with respect to the dense monomorphisms.

This means that $F$ is a $j$-sheaf if for every dense $U \hookrightarrow X$ the induced morphism

$$
  Hom(X,F) \to Hom(U,F)
$$

is an [[isomorphism]].

$F$ is a **$j$-[[separated presheaf]]** if this morphism is itself a [[monomorphism]].

=--

This is for instance in ([MacLaneMoerdijk, p. 223](#MacLaneMoerdijk)).


## Properties

### $j$-Sheaf subtoposes
 {#SheafSubtoposes}

+-- {: .num_prop #RelationToCoveringSieves}
###### Proposition

For $E$ a [[topos]] and $j$ a Lawvere-Tierney topology on $E$, the inclusion

$$
  Sh_j(E) \hookrightarrow E
$$

of [j-sheaves](#JSheaf) is a [[geometric embedding]]. 

So in particular $Sh_j(E)$ is itself a [[topos]] and the embedding is a [[full and faithful functor]] which has a [[exact functor|left exact]] [[left adjoint]] functor $E \to Sh_j(E)$: this is called the **[[sheafification]]** functor.


=--


This appears for instance as ([MacLaneMoerdijk V 3., theorem 1](#MacLaneMoerdijk)).


### Equivalence with Grothendieck topologies
 {#RelationToGrothendieckTopology}


+-- {: .num_prop #RelationToCoveringSieves}
###### Proposition

For $C$ a [[small category]] and $E := [C^{op}, Set]$ its [[presheaf topos]], Lawvere--Tierney topologies in $E$ are equivalent to [[Grothendieck topology|Grothendieck topologies]] on $C$.  

=--

+-- {: .proof}
###### Proof

The [[subobject classifier]] in a [[presheaf topos]] is the  presheaf that assigns to $U \in C$ the set of all [[sieve]]s in $C$ on $U$

$$
  \Omega : U \mapsto Sieves_C(U)
  \,.
$$

since we have

$$Sieves_C (U)=Sub_C(y(U))=hom(y(U),\Omega)=\Omega(U)$$

A [[subobject]] $J \hookrightarrow \Omega$ is therefore precisely a choice of a collection of sieves on each object, which is closed under pullback. The proof therefore amounts to checking that the condition that such a collection of sieves is a [[Grothendieck topology]] on $C$ is equivalent to the statement that the characteristic map $j : \Omega \to \Omega$ of $J \hookrightarrow \Omega$ (see remark \ref{LTTopologyAsSubobject}) is a Lawvere-Tierney topology. 

=--

Here is more discussion of this point:

Suppose that $C$ is a small site.  Then given a [[subpresheaf]] inclusion $F \hookrightarrow G$ in $\Set^{C^\op}$, an object $X$ of $C$, and an element $f$ of $G(X)$, we say $f$ is locally in $F$ (that is, $f \in j_*(F)(X)$) if and only if, for some [[cover|covering family]] $c = (c_i: U_i \to X)_i$ on $X$, the restriction $c^*(f)$ of $f$ to $c$ is in $F$ (that is, each $c_i^*(f) \in F(U_i)$).  This intuitively defines the "local" modality that is the Lawvere--Tierney topology corresponding to the given Grothendieck topology on $C$.

As a specific example, take the usual Grothendieck topology on [[Top]], given by the usual notion of open cover. Taking real-valued functions on a space defines a presheaf (in fact a sheaf) $G: X \mapsto [X,R]$ on $\Top$; the constant functions form a subpresheaf $F$ of $G$. A real-valued function $f: X \to R$ belongs to $j_*(F)$ iff it is *locally* constant; that is, for some open cover $(U_i)_i$ of the domain $X$, each restriction $f|U_i$ is constant.

To make this precise in terms of the above definition, we need to understand the subobject classifier in $E = Set^{C^{op}}$.  But according to the definition, $\Omega$ is simply the representing object for the functor 
$$Sub: E^{op} \to Set$$ 
which takes an object $F$ of $E$ to the collection of subobjects of $F$, $Sub(F)$. In other words, $Sub(F) \cong \hom_E(F, \Omega)$. Applied to $F = \hom_C(-, c)$, we have then 
$$Sub(\hom_C(-, c)) \cong \hom_{Set^{C^{op}}}(\hom_C(-, c), \Omega) \stackrel{Yoneda}{\cong} \Omega(c)$$ 
In other words, we find that the functor $\Omega: C^{op} \to Set$ is defined by 
$$\Omega(c) = \{sieves\,on\,c\}$$ 

Next, if $J$ is a Grothendieck topology on $C$, then the collection of $J$-covering sieves on $c$ (which we denote by $J(c)$( is a subcollection of all sieves on $c$, and so we have an inclusion 
$$J(c) \hookrightarrow \Omega(c)$$ 
and this inclusion is natural in $c$, by virtue of the first axiom on covering sieves. Thus we have a subobject
$$J \hookrightarrow \Omega$$ 
and again, by definition of subobject classifier, this subobject corresponds to a uniquely determined element 
$$j \in \hom_E(\Omega, \Omega)$$ 
which is just the Lawvere--Tierney operator $j: \Omega \to \Omega$.

Conversely, any morphism $j:\Omega\to\Omega$ determines a subobject $J$ of $\Omega$, which therefore associates to every object $c$ a set of sieves on $c$.  It is easy to check that the axioms for covering sieves in a Grothendieck topology correspond exactly to the required properties of the operator $j$.



+-- {: .num_prop }
###### Observation

For $C$ a [[small site]] and $j$ the Lawvere-Tierney topology on the [[presheaf topos]] $E = [C^{op}, Set]$ given by prop. \ref{RelationToCoveringSieves} the [j-sheaves](#SheafSubtoposes) are precisely the [[sheaves]] in the ordinary sense of Grothendieck topologies.

=--

### Relation to lex reflectors
 {#ClosureOperation}

As discussed there, [[categories of sheaves]] are also characterized as being [[reflective subcategories]] of the given ambient topos

$$
  Sh_j(\mathcal{E})
   \stackrel{\overset{L}{\leftarrow}}{\underset{}{\hookrightarrow}}
  \mathcal{E}
 \,.
$$

Here we discuss explicit translations between the structure given by the [[localization|reflector]] $L$ and the corresponding Lawvere-Tierney topology $j : \Omega \to \Omega$ in a way that makes the relation to [[modal type theory]] and [[monads (in computer science)]] most manifest.

+-- {: .num_defn #ClosureOperatorOfReflection}
###### Definition

Given a reflector $\sharp : \mathcal{E} \stackrel{L}{\to} Sh_j(\mathcal{E}) \hookrightarrow \mathcal{E}$, define for each object $X \in \mathcal{E}$ a **closure operator**,
being a [[functor]] on the [[poset of subobjects]] of $X$

$$
  c_L : Sub(X) \to Sub(X)
  \,,
$$

by sending any [[monomorphism]] $A \hookrightarrow X$ classified by a [[characteristic function]] $\chi_A : X \to \Omega$ to the [[pullback]] $c_L(A)$ in

$$
  \array{
    c_L(A) &\to& \sharp A
    \\
    \downarrow && \downarrow
    \\
    X &\to& \sharp X
  }
  \,,
$$

where $X \to \sharp X$ is the [[unit of an adjunction|adjunction unit]].

=--

+-- {: .num_prop }
###### Proposition

This is well defined. Moreover, $c_L$
commutes with [[pullback]] ([[change of base]]).

=--

This appears as ([Johnstone, lemma A4.3.2](#Johnstone)).

+-- {: .num_defn }
###### Definition

A family of functors $Sub(X) \to Sub(X)$ for all objects $X$ that commutes with [[change of base]] is called a **[[universal closure operation]]**.

=--

+-- {: .num_prop }
###### Proposition

Given a [[left exact functor|left exact]] reflector $\sharp$ as above with induced closure operation $c_L$, the corresponding Lawvere-Tierney operator $j : \Omega \to \Omega$ is given as the composite

$$
  j : \Omega \to \sharp \Omega \stackrel{\chi_{\sharp true}}{\to} \Omega  
  \,,
$$

where 

* $\Omega \to \sharp \Omega$ is the [[unit of an adjunction|adjunction unit]];

* $\chi_{\sharp true} : \sharp \Omega \to \Omega$ is the [[characteristic function]] of the result of applying $\sharp$ to the [[subobject classifier|universal subobject]]

  $$
    (* \stackrel{\sharp true}{\hookrightarrow} \sharp \Omega)
     :=
    \sharp (* \stackrel{true}{\hookrightarrow} \Omega)
  $$

  (which is again a [[monomorphism]] since $\sharp$ preserves [[pullbacks]]).

=--

+-- {: .proof}
###### Proof

For $A \hookrightarrow X$ any [[subobject]] with [[characteristic function]] $\chi_A : X \to \Omega$, we need to show that we have a [[pullback]] [[diagram]]

$$
  \array{
    c_L(A) &\to& &\to& &\to& *
    \\
    \downarrow && && && \downarrow
    \\
    X &\stackrel{\chi_A}{\to}& \Omega
    &\stackrel{}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
  \,.
$$

The pullback along the rightmost morphism is by definition $# * \to \sharp \Omega$

$$
  \array{
    c_L(A) &\to& &\to& # * = * &\to& *
    \\
    \downarrow && && \downarrow && \downarrow
    \\
    X &\stackrel{\chi_A}{\to}& \Omega
    &\stackrel{}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
  \,.
$$

Moreover, by the [[natural transformation|naturality]] of the [[unit of an adjunction|adjunction unit]] we have a [[commuting diagram]]


$$
  \array{
    X &\to& \sharp X
    \\
    {}^{\mathllap{\chi_A}}\downarrow && \downarrow^{\mathrlap{\sharp \chi_A}}
    \\
    \Omega &\to& \sharp \Omega
  }
  \,.
$$

Using this in the remaining bottom morphism of our would-be pullback square we find that equivalently

$$
  \array{
    c_L(A) &\to& &\to& # * = * &\to& *
    \\
    \downarrow && && \downarrow && \downarrow
    \\
    X &\stackrel{}{\to}& \sharp X
    &\stackrel{\sharp \chi_A}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
$$

needs to be a pullback diagram. Since $\sharp$ preserves pullbacks we have that also the middle square in 

$$
  \array{
    c_L(A) &\to& \sharp A &\to& # * = * &\to& *
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    X &\stackrel{}{\to}& \sharp X
    &\stackrel{\sharp \chi_A}{\to}&
    \sharp \Omega
    &\stackrel{}{\to}&
    \Omega
  }
$$

is a pullback. But then also the left square is a pullback, by def. \ref{ClosureOperatorOfReflection}. This finally means, by the [[pasting law]], that also the total rectangle is a pullback.

=--

+-- {: .num_remark }
###### Remark

Equivalently, by the [[pasting law]], we have that $j : \Omega \to \Omega$ is the [[characteristic function]] of the $L$-closure, def. \ref{ClosureOperatorOfReflection}, of the universal subobject $* \to \Omega$, because we have a [[pasting diagram]] of [[pullback]] squares

$$
  \array{
    c_L(*) &\to& \sharp * = * &\to & * 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \Omega &\to& \sharp \Omega &\stackrel{\chi_{\sharp true}}{\to} & \Omega
  }
  \,.
$$

In this form the statement appears in the proof of ([Johnstone, Theorem A4.3.9](#Johnstone)).

=--


## Enriched generalization

* [[Francis Borceux]], _Algebraic localizations and elementary toposes_, Cah. Top. G&#233;om. Diff. Cat. **21** (1980), no. 4, 393&ndash;401. ([MR82g:18002](http://www.ams.org/mathscinet-getitem?mr=606384), [pdf](http://archive.numdam.org/article/CTGDC_1980__21_4_393_0.pdf))

* [[Francis Borceux]], _Sheaves of algebras for a commutative theory_, Ann. Soc. Sci. Bruxelles S&#233;r. I **95** (1981), no. 1, 3&ndash;19. ([MR83c:18006](http://www.ams.org/mathscinet-getitem?mr=628032))

Let $\mathcal{C}$ be a small category enriched over $Set^{\mathbf{T}}$ where $\mathbf{T}$ is a [[commutative algebraic theory]]. Then $[\mathcal{C}^{op},\text{Set}^{\mathbf{T}}]$. A $\mathbf{T}$-sieve as an enriched subfunctor of $\mathcal{C}(-,x)\colon\mathcal{C}^{op}\rightarrow\text{Set}^{\mathbf{T}}$. A $\mathbf{T}$-topology is a set $J(x)$ of $\mathbf{T}$-sieves for every $x$, satisfying some axioms. Borceux defines the notion of a sheaf over such enriched site and proves the existence and exactness of the associated sheaf functor. 

He proves that there is an object $\Omega_{\mathbf{T}}$ in $[\mathcal{C}^{op},\text{Set}]$ which classifies subobjects in $[\mathcal{C}^{op},\text{Set}^{\mathbf{T}}]$. Moreover, there is a correspondence between

1. localizations of $[\mathcal{C}^{\text{op}},\text{Set}^{\mathbf{T}}]$ 

2. $\mathbf{T}$-topologies on $\mathcal{C}$

3. morphisms $j\colon\Omega_{\mathbf{T}}\rightarrow\Omega_{\mathbf{T}}$ satisfying the Lawvere-Tierney axioms for a topology 

## Related concepts

* [[modality]]

* [[modal type theory]]

* [[monad (in programming theory)]]


## References

The notion is introduced as a [[geometric modality]] on p. 3 of 

* {#Lawvere} [[William Lawvere]], _Quantifiers and sheaves_, Actes, Congr&#232;s intern, math., 1970. Tome 1, p. 329 &#224; 334 ([pdf](http://www.mathunion.org/ICM/ICM1970.1/Main/icm1970.1.0329.0334.ocr.pdf))
 

Detailed discussion of Lawvere-Tierney operators as [[geometric modalities]] is in 

* {#Goldblatt} [[Robert Goldblatt]], _Grothendieck topology as geometric modality_, Mathematical Logic Quarterly, Volume 27, Issue 31-35, pages 495&#8211;529, (1981)
 

Textbook accounts include section V.1 of

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_,

(the notion of sheaves in section V.3, the sheafification functor in section V.3 and the relation to Grothendieck topologies in section V.4);

and section A4.4 of

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 
Discussion in [[homotopy type theory]] is in

* {#QuirinTabareau16} Kevin Quirin, Nicolas Tabareau, _Lawvere-Tierney sheafification in Homotopy Type Theory_, Journal of Formalized Reasoning, Vol 9, No 2, (2016) ([web](https://jfr.unibo.it/article/view/6232))


[[!redirects sheafification in a Lawvere-Tierney topos]]
[[!redirects sheafification in a Lawvere–Tierney topos]]
[[!redirects sheafification in a Lawvere--Tierney topos]]
[[!redirects Lawvere-Tierney topology]]
[[!redirects Lawvere–Tierney topology]]
[[!redirects Lawvere--Tierney topology]]
[[!redirects Lawvere-Tierney topologies]]
[[!redirects Lawvere–Tierney topologies]]
[[!redirects Lawvere--Tierney topologies]]

[[!redirects Lawvere-Tierney operator]]
[[!redirects Lawvere–Tierney operator]]
[[!redirects Lawvere--Tierney operator]]
[[!redirects Lawvere-Tierney operators]]
[[!redirects Lawvere–Tierney operators]]
[[!redirects Lawvere--Tierney operators]]

[[!redirects local modality]]
[[!redirects local modalities]]
