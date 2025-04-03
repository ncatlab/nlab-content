
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $C$ a [[small category]], its **category of presheaves** is the [[functor category]] 

$$
  PSh(C) := [C^{op}, Set]
$$

from the [[opposite category]] of $C$ to [[Set]].  An object in this category is a [[presheaf]]. See there for more details. Since any category of the form $PSh(C)$ is a [[topos]], such a category is often called a **presheaf topos**.

## Properties

### General
 {#GeneralProperties}

For $\mathcal{C}$ any [[category]], consider $PSh(\mathcal{C})$ its category of [[Set]]-valued presheaves.

\begin{proposition}\label{LimitsOfPresheavesAreComputedObjectwise}
  $PSh(\mathcal{C})$ has all [[limits]] and [[colimits]] (over [[small diagrams]]), and these are computed objectwise: For $\mathcal{I}$ any [[diagram]] (a [[small category]]) we have:
$$
  X_{\bullet} \,\colon\, \mathcal{I} \longrightarrow PSh(\mathcal{C})
  \;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;
  \underset{c \in Obj(\mathcal{C})}{\forall}
  \;\;\;\;
  \big(
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim} X_i
  \big)
  (c)
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim} 
  \big(
     X_i(c)
  \big)
  \;\;\;\;\text{and}\;\;\;\;
  \big(
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim} X_i
  \big)
  (c)
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim} 
  \big(
     X_i(c)
  \big)
$$
\end{proposition}
\begin{proof}
  The defining [[universal property]] readily follows from that of the objectwise (co-)limits.
\end{proof}

\begin{proposition}\label{EpimorphismsOfPresheavesAreDetectedObjectwise}
  A morphism $X \xrightarrow{\;f\;} Y$ of presheaves $X,Y \,\in\, PSh(\mathcal{C})$ is an [[epimorphism]] or [[monomorphism]] precisely if it is so over each [[object]] of $\mathcal{C}$, hence precisely if it is object-wise a [[surjection]] or [[injection]], respectively.
\end{proposition}
\begin{proof}
  Using for instance the characterization of epimorphisms by [[pushouts]] ([this Prop.](epimorphism#BasicCharacterizationOfEpimorphisms)) and of monomorphism by [[pullbacks]] ([this Prop.](monomorphism#BasicCharacterizationOfMonomorphisms)), the statement follows by Prop. \ref{LimitsOfPresheavesAreComputedObjectwise}.
\end{proof}

Now assume that $\mathcal{C}$ is a [[small category]]. 

\begin{proposition}
  $PSh(\mathcal{C})$ is a [[cartesian closed category]].
\end{proposition}
\begin{proof}
  This is spelled out at *[[closed monoidal structure on presheaves]]*.
\end{proof}

\begin{proposition}
  $PSh(\mathcal{C})$ is a [[topos]].
\end{proposition}
\begin{proof}
  This is the base case of *[[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]]*.
\end{proof}



* The category of presheaves $PSh(\mathcal{C})$ is the [[free cocompletion]] of $\mathcal{C}$.

* the [[Yoneda lemma]] says that the [[Yoneda embedding]] $j \colon \mathcal{C} \to PSh(\mathcal{C})$ is -- in particular -- a [[full and faithful functor]].


* The construction of forming (co)-presheaves extends to a [[2-functor]]

  $$
    [-,Set] : Cat \to Topos
  $$

  from the [[2-category]] [[Cat]] to the [[2-category]] [[Topos]]. (See at [[geometric morphism]] the section [Between presheaf toposes](geometric+morphism#BetweenPresheafToposes) for details.)

* A [[reflective subcategory]] of a category of presheaves is a [[locally presentable category]] if it is closed under $\kappa$-[[directed colimit]]s for some [[regular cardinal]] $\kappa$ (the embedding is an [[accessible functor]]).

* A [[geometric embedding|sub-topos]] of a category of presheaves is a [[Grothendieck topos]]: a [[category of sheaves]] (see there for details).

### (Co-)Monadicity over families

There is a functor from presheaves to families of sets $U : Psh(C) \to Set^{Ob(C)} \cong Set/Ob(C)$ given by "forgetting" the functorial action on morphisms of $C$. This functor is both [[monadic functor|monadic]] and [[comonadic functor|comonadic]].

### Functoriality

See [[functoriality of categories of presheaves]].

### Characterization

The following [[Giraud theorem|Giraud like]] theorem stems from [[Marta Bunge|Marta Bunge's]] dissertation (1966)

+-- {: .num_theorem #bunge_theorem}
###### Theorem 

A category is equivalent to a presheaf topos if and only if it is [[cocomplete]], [[well-powered category|well-powered]], [[well-powered category|co-well-powered]], [[atomic category|atomic]], and [[regular category|regular]]. 

=--

This characterisation was proven for [[enriched categories|enriched]] presheaf categories in Theorem 4.16 of [Bunge 1969](#Bunge69) (Corollary 4.19 for the unenriched statement).  

In the unenriched case, a much sharper result was later proved in [Centazzo-Rosický-Vitale 2004](#Centazzo-Rosický-Vitale04):


+-- {: .num_theorem #CentazzoRosickýVitale_theorem}
###### Theorem 

A category is equivalent to a presheaf topos if and only if it is cocomplete and atomic. 

=--

Another characterization, using [[exact completion|exact completions]], can be found in Carboni-Vitale ([1998](#CarboniVitale98)) or Centazzo-Vitale ([2004](#Centazzo-Vitale04)):

+-- {: .num_theorem #carboni_vitale_theorem}
###### Theorem 

A category is equivalent to a presheaf topos if and only if it is [[locally small category|locally small]], [[extensive category|extensive]], [[exact category|exact]] and has a small set of projective and indecomposable [[separator|generators]].

=--


([1998](#CarboniVitale98)) has also an interesting comparison to a classical characterization of categories [[monadic category|monadic]] over Set.


### Presheaves on over-categories and over-categories of presheaves {#RelWithOvercategories}

Let $C$ be a [[category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. Write
$PSh(C/c) = [(C/c)^{op}, Set]$ for the category of [[presheaf|presheaves]] on $C/c$ and write
$PSh(C)/Y(c)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(C)$ is the [[Yoneda embedding]]. 

+-- {: .num_prop #representable_case}
###### Proposition


There is an [[equivalence]] of categories

$$
  e : PSh(C/c) \stackrel{\simeq}{\to} PSh(C)/Y(c)
  \,.
$$

=--


+-- {: .proof}
###### Proof

The functor $e$ takes $F \in PSh(C/c)$ to the presheaf
$F' : d \mapsto \sqcup_{f \in C(d,c)} F(f)$ which is equipped with the natural transformation $\eta : F' \to Y(c)$ with component map $\eta_d \sqcup_{f \in C(d,c)} F(f) \to C(d,c)$.

A weak inverse of $e$ is given by the functor 
$$
  \bar e : PSh(C)/Y(c) \to PSh(C/c)
$$
which sends
$
  \eta : F' \to Y(C))
$ to $F \in PSh(C/c)$ given by
$$
  F : (f : d \to c) \mapsto F'(d)|_c
  \,,
$$
where $F'(d)|_c$ is the [[pullback]]
$$
  \array{
     F'(d)|_c &\to& F'(d)
     \\
     \downarrow && \downarrow^{\eta_d}
     \\
     pt &\stackrel{f}{\to}& C(d,c)
  }
  \,.
$$ 

=--


+-- {: .un_example}
###### Example

Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphisms to $C$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
$$
  F : (C/c)^{op} \to C^{op} \to Set
  \,.
$$

Then
$
  F'(d) = \sqcup_{f \in C(d,c)} F(f)
  = \sqcup_{f \in C(d,c)} F(d)
  \simeq
  C(d,c) \times F(d) 
$
and hence $F ' = Y(c) \times F$ with respect to the [[closed monoidal structure on presheaves]].

=--

See also [[functors and comma categories]].

For the analog statement in [[(∞,1)-category]] theory see

* <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-category+of+(infinity%2C1)-presheaves#interaction_with_forming_overcategories_19">(∞,1)-category of (∞,1)-presheaves -- Interaction with overcategories</a>

+-- {: .un_remark}
###### Remark

Consider $\int_C Y(c)$ , the [[category of elements]] of $Y(c):C^{op}\to Set$. This has objects $(d_1,p_1)$ with $p_1\in Y(c)(d_1)$, hence $p_1$ is just an arrow $d_1\to c$ in $C$. A map from $(d_1, p_1)$ to $(d_2, p_2)$ is just a map $u:d_1\to d_2$ such that $p_2\circ u =p_1$ but this is just a morphism from $p_1$ to $p_2$ in $C/c$.

Hence, the above proposition \ref{representable_case} can be rephrased as $PSh(\int_C Y(c))\simeq PSh(C)/Y(c)$ which is an instance of the following formula:

=--

+-- {: .num_prop}
###### Proposition

Let $P:C^{op}\to Set$ be a presheaf. Then there is an [[equivalence of categories]]

$$
  PSh(\int_C P) \simeq PSh(C)/P
  \,.
$$

=--

On objects this takes $F : (\int_C P)^{op} \to Set$ to 
$$i(F)(A \in C) = \{ (p,a) | p \in P(A), a \in F(A,p) \} = \Sigma_{p \in P(A)} F(A,p)$$
with obvious projection to $P$. The inverse takes $f : Q \to P$ to
$$i^{-1}(f)(A, p \in P(A)) = f_A^{-1}(p)\;.$$

For a proof see [Kashiwara-Schapira (2006, Lemma 1.4.12, p. 26)](#KS06). For a more general statement involving slices of Grothendieck toposes see [Mac Lane-Moerdijk (1994, p.157)](#MacLaneMoerdijk).

In particular, this equivalence shows that _slices of presheaf toposes are presheaf toposes_. 


### Artin gluings 

The statements of the preceding [subsection](#RelWithOvercategories) may be generalized further:  

+-- {: .num_theorem} 
###### Theorem 
Let $T: Set^{C^{op}} \to Set^{D^{op}}$ be a functor that preserves [[wide pullbacks]]. Then the [[Artin gluing]] $(Set^{D^{op}} \downarrow T)$ is also a presheaf topos. 
=-- 

+-- {: .proof} 
###### Proof 
The functor $T$ is [[parametric right adjoint|familially representable]]: there is a functor $D^{op} \to Fam(Set^{C^{op}})$ into the small [[free coproduct completion|coproduct cocompletion]] of $Set^{C^{op}}$, taking $d \in Ob(D)$ to a formal coproduct $\sum_{x \in T(1)(d)} W_{(d, x)}$ of presheaves $W_{(d, x)}: C^{op} \to Set$, such that $T(F)$ is given by the formula 

$$T(F)(d) = \sum_{x \in T(1)(d)} Set^{C^{op}}(W_{(d, x)}, F).$$ 

The Artin gluing itself is then describable as the presheaf category over the [[collage]] of the [[profunctor]] $W: C \nrightarrow (y_D \downarrow T(1))$ defined by the formula 

$$W(c; (d, x: D(-, d) \to T(1))) = W_{(d, x)}(c).$$ 
For details, see for example Appendix C.3 of [Leinster](#Lein). The result is due to [Carboni and Johnstone](#cj). 
=-- 

In passing, we note that the small coproduct cocompletion $Fam(Set^{C^{op}})$ is itself a presheaf topos: there are [[equivalence of categories|equivalences]] 

$$Fam(Set^{C^{op}}) \simeq Set^{C^{op}} \downarrow \Delta \simeq Set^{C_+^{op}}$$ 

where $\Delta: Set \to Set^{C^{op}}$ is the [[diagonal functor]], and $C_+$ is the result of freely adjoining an [[initial object]] to $C$, i.e., the [[ordinal sum of categories]] $1 +_\sigma C$ of categories ($1$ being [[terminal object|terminal]]), aka the [[cone]] of $C$. 

### Finite presheaves

A _finite presheaf_ on a category $C$ is a functor $C^{op}\to FinSet$ valued in the [[FinSet|category of finite sets]]. Categories of finite presheaves will hardly be [[Grothendieck toposes]] for want of infinite limits but they still can turn out to be [[elementary toposes]] as e.g. in the case of $FinSet$ itself.

By going through the proof that ordinary categories of presheaves are toposes, one observes that the constructions stay within finite presheaves when applied to a finite category $C$ i.e. one with only a finite set of morphisms. Hence, one has the following

+-- {: .num_prop}
###### Proposition

Let $C$ a finite category. Then the category of finite presheaves $[C^{op},FinSet]$ is a topos. $\qed$
=--

Note, that the category $[G,FinSet]$ of finite $G$-sets is a topos even when the group $G$ is infinite! In this case it is crucial that $\Omega =\{\emptyset , G\}$ in $[G,Set]$ is a finite set.

(Cf. [Borceux (1994, p.299)](#Borceux3))

### Models in presheaf toposes

See at _[[models in presheaf toposes]]_.

## Related concepts

For [[(∞,1)-category]] theory see [[(∞,1)-category of (∞,1)-presheaves]].

[[!include locally presentable categories - table]]

## References

Original discussion:

* [[Marta Bunge]], *Categories of Set-Valued Functors*, PhD thesis, University of Pennsylvania (1966) &lbrack;[[Bunge-SetValuedFunctors.pdf:file]]&rbrack;

  Reprints in Theory and Applications of Categories, **30** (2024) 1-84 &lbrack;[tac:tr30](http://www.tac.mta.ca/tac/reprints/articles/30/tr30abs.html)&rbrack;



* {#SGA4} [[Michael Artin|M.Artin]], [[Alexander Grothendieck|A.Grothendieck]], [[J. L. Verdier]] (eds.), *Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas - [[SGA 4]]*, LNM 269 Springer (1972)




Basic exposition:

* [[Michael Barr]], [[Colin McLarty]], [[Charles Wells]],  *Variable set theory*, prepared for *Scientific American* but unpublished (~1985) &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/vst.pdf), [[BarrMcLartyWells-VariableSetTheory.pdf:file]]&rbrack;


Introduction:

* [[Marie La Palme Reyes]], [[Gonzalo E. Reyes]], [[Houman Zolfaghari]], _Generic figures and their glueings.  A constructive approach to functor categories_, Polimetrica (2008) &lbrack;[pdf](https://marieetgonzalo.files.wordpress.com/2004/06/generic-figures.pdf), ISBN:8876990046&rbrack;

See also most accounts of general [[topos theory]], such as:

* {#Borceux3} [[Francis Borceux]], *Handbook of Categorical Algebra 3 : Categories of Sheaves*, Cambridge UP 1994.

* {#KS06} [[Masaki Kashiwara]], [[Pierre Schapira]], _Categories and Sheaves_ , Springer Heidelberg 2006.

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_, Springer Heidelberg 1994.

The characterizations of categories of presheaves are discussed in

* {#Bunge69} [[Marta Bunge]], *Relative functor categories and categories of algebras*, J. of Algebra 11, Issue 1 (1969), 64--101. [web](https://www.sciencedirect.com/science/article/pii/0021869369901021), [MR236238](https://mathscinet.ams.org/mathscinet-getitem?mr=236238) <a href="https://doi.org/10.1016/0021-8693(69)90102-1">doi</a>

* {#CarboniVitale98} [[Aurelio Carboni|A. Carboni]], [[Enrico Vitale|E. M. Vitale]], *Regular and exact completions*, JPAA 125 (1998), 79-116.

* {#CentazzoVitale04} C. Centazzo, [[Enrico Vitale|E. M. Vitale]], *Sheaf theory*, pp. 311-358 in Pedicchio, Tholen (eds.), *Categorical Foundations*, Cambridge UP 2004. ([draft](https://perso.uclouvain.be/enrico.vitale/chapter7.pdf)) 

* {#Centazzo-Rosický-Vitale} Claudia Centazzo, [[Jiří Rosický]], [[Enrico M. Vitale]]: *A characterization of locally $D$-presentable categories*, [[Cahiers]] de topologie et géométrie différentielle catégoriques **45** 2 (2004) 141-146 &lbrack;[numdam:CTGDC_2004__45_2_141_0](https://www.numdam.org/item/CTGDC_2004__45_2_141_0), [pdf](https://perso.uclouvain.be/enrico.vitale/ClaudiaJiri.pdf)&rbrack;

The result about Artin gluings of presheaf toposes is due to Carboni and Johnstone, 

* {#cj} [[Aurelio Carboni]] and [[Peter Johnstone]], *Connected limits, familial representability and Artin glueing*, Mathematical Structures in Computer Science, Volume 5, Issue 4 (December 1995), 441-459. ([link](https://www.cambridge.org/core/journals/mathematical-structures-in-computer-science/article/connected-limits-familial-representability-and-artin-glueing/54E93903F7D7321B98B64AE7CB3E7AE0))  

and is explained in section C.3 of Tom Leinster's book, 

* {#Lein} [[Tom Leinster]], *Higher Categories, Higher Operads* &lbrack;[arXiv:math/0305049](https://arxiv.org/abs/math/0305049)&rbrack;

[[!redirects categories of presheaves]]
[[!redirects presheaf category]]
[[!redirects presheaf categories]]
[[!redirects presheaf-category]]
[[!redirects presheaf-categories]]

[[!redirects presheaf topos]]
[[!redirects presheaf toposes]]
[[!redirects presheaf topoi]]

[[!redirects Presheaves]]
