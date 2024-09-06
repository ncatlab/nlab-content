

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

\tableofcontents

\section{Idea} 

A **pro-object** of a [[category]] $C$ is a "formal [[filtered category|cofiltered]] [[limit]]" of [[objects]] of $C$.  

The category of pro-objects of $C$ is written $pro$-$C$. Such a category is sometimes called a __pro-category__, but notice that that is *not* the same thing as a pro-object in [[Cat]].

"Pro" is short for "projective" 
([[projective limit]] is an older term for [[limit]]). It is in contrast to "ind" in the dual notion of [[ind-object]], standing for "inductive", (and corresponding to [[inductive limit]], the old term for [[colimit]]).  In some (often older) sources, the term 'projective system' is used more or less synonymously for pro-object.

The definition of arrows in the category of pro-objects in $\mathcal{C}$ is perhaps more intuitive in the dual case of [[ind-object|ind-objects]] (pro-objects in $C^{op}$), where it can be seen as stipulating that the objects of $C$ are [[finitely presentable object|finitely presentable]] in $ind$-$C$.

## Definition

### As formal cofiltered limits
  {#AsFormalCofilteredLimits}

Let $\mathcal{C}$ be a [[small category]]. We write

\[
  \label{YonedaEmbedding}
  \mathcal{C}^{op} 
  \xhookrightarrow{\;\;\; y \;\;\;}
  Func(\mathcal{C}, Sets)
\]

for the [[Yoneda embedding]] of its [[opposite category]], which we will often regard through its [[opposite functor]]

\[
  \label{OppositeYonedaEmbedding}
  \mathcal{C}
  \xhookrightarrow{\;\;\; y^{op} \;\;\;}
  Func(\mathcal{C}, Sets)^{op} 
  \,.
\]

This is still a [[full subcategory]]-inclusion, now of $\mathcal{C}$ itself.

\begin{definition}\label{CategoryOfProObjects}
**(category of pro-objects)** \linebreak

The *category of pro-objects of $\mathcal{C}$*, according to [Grothendieck 1960, Section 2](#Grothendieck1960), is the [[full subcategory]] of the [[functor category]] $Func(\mathcal{C}, Sets)^{op}$ (eq:OppositeYonedaEmbedding)

\[
  \label{ProCAsFullSubcategoryOfOppositeOfCategoryOfPresheaves}
  Pro(\mathcal{C})
  \xhookrightarrow{\;\;}
  Func(\mathcal{C}, Sets)^{op}   
\]

on those functors which are [[cofiltered limits]] of [[representable functors]] under the opposite Yoneda embedding (eq:OppositeYonedaEmbedding), hence of the form

\[
  \label{FilteredLimitOfRepresentablesInOppositeOfPresheafCategory}
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)
  \;\;
  \coloneqq
  \;\;
  \underset{\longleftarrow}{\lim}
  \big(
    \mathcal{I}
    \xrightarrow{\;X_\bullet\;}
    \mathcal{C}
    \xrightarrow{\;y^{op}\;}
    Func(\mathcal{C}, Sets)^{op}
  \big)
  \,,
\]

for $\mathcal{I}$ a [[cofiltered category]]. These objects of $Pro(\mathcal{C})$ are also called the *pro-objects of $\mathcal{C}$*.
\end{definition}

\begin{remark}
Since $Func(\mathcal{C}, Sets)^{op}$ (eq:OppositeYonedaEmbedding) is the [[free completion]] of $\mathcal{C}$, we may think of $Pro(\mathcal{C})$ (Def. \ref{CategoryOfProObjects}) as the *free completion of $\mathcal{C}$ under [[cofiltered limits]].* See also at *[[pro-representable functor]]*.
\end{remark}

\begin{remark}\label{BetweenFilteredLimitsAndFilteredColimits}
Under the identification of the [[objects]] of a category with those of its [[opposite category]], the  pro-objects (eq:FilteredLimitOfRepresentablesInOppositeOfPresheafCategory) are equivalently [[filtered colimits]] of [[presheaves]]:

$$
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  y(X^{op}_i)
  \;\;
  \coloneqq
  \;\;
  \underset{\longrightarrow}{\lim}
  \big(
    \mathcal{I}^{op}
    \xrightarrow{\;X^{op}_\bullet\;}
    \mathcal{C}^{op}
    \xrightarrow{\;y\;}
    Func(\mathcal{C}, Sets)
  \big)
  \,,
$$

since [[generalized the|the]] [[limit]] of a [[functor]] is the [[colimit]] of its [[opposite functor]].

\end{remark}

\begin{remark}\label{ProObjectAsFormalDualOfIndObject}
The category $Pro(\mathcal{C})$ is the [[opposite category]] of that of [[ind-objects]] in the opposite category of $\mathcal{C}$ (e.g. [Kashiwara-Schapira 06, p. 138](#KashiwaraSchapira06)):
$
  Pro(\mathcal{C})
    \simeq
  (Ind(\mathcal{C}^{op}))^{op}
  \,.
$

\end{remark}


\begin{lemma}\label{ProObjectsAsFunctors}
  The pro-objects regarded as functors (eq:FilteredLimitOfRepresentablesInOppositeOfPresheafCategory)
  are objectwise on $c \in \mathcal{C}$ given by 
  $$
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
    y^{op}(X_i)  
    \;\;
    \colon
    \;\;
    c 
    \;\mapsto\;
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
    \mathcal{C}(X_i, c)
    \,.
  $$

\end{lemma}
\begin{proof}
This is the composite of the following sequence of [[natural bijections]]:
$$
  \begin{aligned}
  \Big(
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)  
  \Big)
  (c) 
  &
  \;\simeq\;
  \Big(
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  y(X^{op}_i)  
  \Big)
  (c) 
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  \Big(
    \big(y(X^{op}_i)\big)
    (c)
  \Big)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \;
  Func(\mathcal{C},Sets)
  \big(
    y(c), \, y(X_i)
  \big)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \mathcal{C}^{op}(c, X_i)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \mathcal{C}(X_i, c)
  \mathrlap{\,,}
  \end{aligned}
$$
where

* the first step is Remark \ref{BetweenFilteredLimitsAndFilteredColimits};

* the second step uses that [[colimits of presheaves are computed objectwise]];

* the third step is the [[Yoneda lemma]];

* the fourth step is the [[Yoneda embedding]] (eq:YonedaEmbedding);

* the fifth step is the definition of the [[opposite category]].

\end{proof}

\begin{lemma}\label{HomSetsOfProObjectsAsLimitsOfColimitsOfHomoSetsInC}
**([[hom-sets]] between [[pro-objects]] as limits of colimits of hom-sets in $\mathcal{C}$)** \linebreak
The [[hom-sets]] in $Pro(\mathcal{C})$ (Def. \ref{CategoryOfProObjects})
are in [[natural bijection]] with [[limits]] of [[colimits]] of [[hom-sets]] in $\mathcal{C}$, as follows:

$$
  Pro(\mathcal{C})
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    \mathcal{C}
    \big(
      X_i,
      \,
      Y_j
    \big)
  \Big)
$$

\end{lemma}

\begin{proof}
This is the composite of the following sequence of [[natural bijections]]:
$$
  \begin{aligned}
  Pro(\mathcal{C})
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
  &
  \;\simeq\;
  Func(\mathcal{C},Sets)^{op}
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
  \\
  & 
  \;\simeq\;
  Func(\mathcal{C},Sets)
  \Big(
    \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{lim}
    y(Y^{op}_j),    
    \,
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    y(X^{op}_i),
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \;
  Func(\mathcal{C},Sets)
  \Big(
    y(Y^{op}_j),    
    \,
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    y(X^{op}_i),
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \Big(
    \big(
      \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
      y(X^{op}_i)
    \big)
    \big(
      y(Y^{op}_j)
    \big)    
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    \mathcal{C}
    \big(
      X_i,
      \,
      Y_j
    \big)
  \Big)
  \end{aligned}
$$

Here

* the first step is the [[fully faithful functor|fully faithfulness]] of the defining [[full subcategory]]-inclusion (eq:ProCAsFullSubcategoryOfOppositeOfCategoryOfPresheaves);

* the second step is the definition of the [[opposite category]], using Remark \ref{BetweenFilteredLimitsAndFilteredColimits};

* the third step uses that [[hom-functors preserve limits]], which means that $\mathcal{K}^{op}  \xrightarrow{\;\mathcal{K}(-,k)\;} Sets$ takes *[[colimits]] in $\mathcal{K}$* to *limits in [[Sets]], here for $\mathcal{K} = Func(\mathcal{C},Sets)$;

* the fourth step is the [[Yoneda lemma]];

* the fifth step is Lemma \ref{ProObjectsAsFunctors}.

\end{proof}


\linebreak


### Via spans 
 {#DefinitionViaSpans}

\begin{rmk} We can give an explicit description of the arrows of pro-$\mathcal{C}$ as follows. First, for pro-objects $F: \mathcal{D} \rightarrow \mathcal{C}$ and $G: \mathcal{E} \rightarrow \mathcal{C}$ and for any object $e$ of $\mathcal{E}$, we introduce a relation $\sim$ on arrows with target $G(e)$ which identifies an arrow $f: F(d) \rightarrow G(e)$ with an arrow $f': F(d') \rightarrow G(e)$ for objects $d$ and $d'$ of $\mathcal{D}$ and an object $e$ of $\mathcal{E}$, if there is an object $d''$ of $\mathcal{D}$, an arrow $g: d'' \rightarrow d$ of $\mathcal{D}$, and an arrow $g': d'' \rightarrow d'$ of $\mathcal{D}$, such that $f \circ F(g) = f' \circ F(g')$. 

This relation $\sim$ is in fact an [[equivalence relation]]. Symmetry is obvious. Reflexivity is immediately demonstrated using the identity arrows of $\mathcal{D}$. Transitivity would not hold for an arbitrary category, but follows from the assumption that $\mathcal{D}$ is cofiltered. Indeed, suppose that we have a zig-zag in $\mathcal{D}$ as follows. 

\begin{centre}
  \begin{tikzcd}
          & d'_{0} \ar[dl, "g_{0}", swap] \ar[dr, "g_{1}"] & & d'_{1} \ar[dl, "g_{2}", swap] \ar[dr, "g_{3}"] &       \\
    d_{0} & & d_{1} & & d_{2}
  \end{tikzcd}
\end{centre}

The fact that $\mathcal{D}$ is cofiltered ensures that there is an object $d''$ of $\mathcal{D}$ fitting into the following diagram.

\begin{centre}
  \begin{tikzcd}
          & & d'' \ar[dl, "g'_{0}", swap] \ar[dr, "g'_{1}"] & & \\
          & d'_{0} \ar[dl, "g_{0}", swap] \ar[dr, "g_{1}"] & & d'_{1} \ar[dl, "g_{2}", swap] \ar[dr, "g_{3}"] &       \\
    d_{0} & & d_{1} & & d_{2}
  \end{tikzcd}
\end{centre}

Suppose that we have arrows $f_{0} : F(d_{0}) \rightarrow G(e)$, $f_{1}: F(d_{1}) \rightarrow G(e)$, and $f_{2}: F(d_{2}) \rightarrow G(e)$ such that $g_{0}$ and $g_{1}$ exhibit that $f_{0} \sim f_{1}$, and such that $g_{2}$ and $g_{3}$ exhibit that $f_{1} \sim f_{2}$. Then 

$$
\begin{aligned}
f_{0} \circ F(g_{0} \circ g'_{0}) &= f_{0} \circ F(g_{0}) \circ F(g'_{0}) \\
  &= f_{1} \circ F(g_{1}) \circ F(g'_{0}) \\
  &= f_{1} \circ F(g_{2}) \circ F(g'_{1}) \\
  &= f_{2} \circ F(g_{3}) \circ F(g'_{1}) \\
  &= f_{2} \circ F(g_{3} \circ g'_{1}).
\end{aligned}
$$

This exhibits that $f_{0} \sim f_{2}$, as required. 

With this equivalence relation $\sim$ to hand, we can give our explicit description of the arrows of pro-$\mathcal{C}$: an arrow of pro-$\mathcal{C}$ from a pro-object $F: \mathcal{D} \rightarrow \mathcal{C}$ to a pro-object $G: \mathcal{E} \rightarrow \mathcal{C}$ can be taken to be a set $\left\{ f_{e} : F\left(d_{e}\right) \rightarrow G(e) \right\}$ of arrows of $\mathcal{C}$, one for every object $e$ of $\mathcal{E}$, such that, for every arrow $g: e \rightarrow e'$ of $E$, $G(g) \circ f_{e} \sim f_{e'}$. 

In other words: a set $\left\{ f_{e} : F\left(d_{e}\right) \rightarrow G(e) \right\}$ of arrows of $\mathcal{C}$, one for every object $e$ of $\mathcal{E}$, such that, for every arrow $g: e \rightarrow e'$ of $E$, there is an object $d$ of $\mathcal{D}$, an arrow $g_{e} : d \rightarrow d_{e}$ of $\mathcal{D}$, and an arrow $g_{e'}: d \rightarrow d_{e'}$ of $\mathcal{D}$ such that $G(g) \circ f_{e} \circ F(g_{e}) = \circ f_{e'} \circ F(g_{e'})$.

Two such sets $\left\{ f_{e} \right\}_{e \in Ob(\mathcal{E})}$ and $\left\{ f'_{e} \right\}_{e \in Ob(\mathcal{E})}$ are equal, i.e. define the same arrow from $F$ to $G$, if $f_{e} \sim f'_{e}$ for every object $e$ of $\mathcal{E}$.

\end{rmk}



\section{Characterisations}

In some cases, pro-objects in a category $\mathcal{C}$ can be viewed as actual limits in a certain category. We prove here some results of this kind.

\begin{prpn} \label{PropositionCategoriesEquivalentToProC} Let $\mathcal{C}$ be a category, and let $\mathcal{A}$ be a category with [[cofiltered limit|cofiltered limits]]. Suppose that we have a [[fully faithful functor]] $i: \mathcal{C} \rightarrow \mathcal{A}$ which lands in [[compact object|cocompact objects]]. Then $lim_{\mathcal{A}} \circ (i \circ) : Pro(\mathcal{C}) \to \mathcal{A}$ is fully faithful, and hence defines an equivalence onto its image.

\end{prpn}

\begin{proof} Let $F:\mathcal{D} \to \mathcal{C}$ and $G:\mathcal{E} \to \mathcal{C}$ be pro-objects. We then have a sequence of (natural) bijections:

$Hom_{Pro(\mathcal{C})}(F,G)$

$= \underset{e:\mathcal{E}}{lim} \, \underset{d:\mathcal{D}}{colim} \, Hom_{\mathcal{C}}(F d, G e)$

$\cong \underset{e:\mathcal{E}}{lim} \, \underset{d:\mathcal{D}}{colim} \, Hom_{\mathcal{A}}(i (F d), i (G e))$

$\cong \underset{e:\mathcal{E}}{lim} \, Hom_{\mathcal{A}}(\underset{d:\mathcal{D}}{lim} (i \circ F) d, i (G e))$

$\cong Hom_{\mathcal{A}}(\underset{d:\mathcal{D}}{lim} (i \circ F) d, \underset{e:\mathcal{E}}{lim} (i \circ G) e)$

$= Hom_{\mathcal{A}}(lim (i \circ F), lim (i \circ G))$

With these bijections being by definition of pro-object morphisms, fully faithfulness, cocompactness of $i (G e)$, definition of a limit, and definition respectively.
\end{proof}

\begin{example} \label{ExampleProfiniteGroupsEquivalentToCertainTopologicalGroups} Let $\mathcal{C}$ be the category [[Grp]] of groups, and let $\mathcal{A}$ be the category $\mathsf{Top-Grp}$ of [[topological group|topological groups]]. The fully faithful functor $\mathsf{Set} \rightarrow \mathsf{Top}$ sending a set to the [[discrete topological space]] on this set gives rise to a fully faithful functor $\mathsf{Grp} \rightarrow \mathsf{Top-Grp}$. Then (as finite discrete spaces are cocompact) Proposition \ref{PropositionCategoriesEquivalentToProC} implies that the category pro-$\mathsf{FinGrp}$ of pro-objects in $\mathsf{FinGrp}$, that is to say of [[profinite group|profinite groups]], is equivalent to the full sub-category of topological groups whose objects are obtained as a cofiltered limit of finite groups (viewed as topological groups via the discrete topology). \end{example}

\begin{rmk} \label{RemarkProfiniteGroupsEquivalentToCertainTopologicalGroups} Though it is less well-known, one can in Example \ref{ExampleProfiniteGroupsEquivalentToCertainTopologicalGroups} evidently replace $\mathsf{Top}$ with any category $\mathcal{A}$ for which there is a fully faithful functor $\mathsf{Set} \rightarrow \mathcal{A}$ which preserves finite products and lands in cocompact objects. See [[discrete object]] for one general setting in which finite product preserving functors exist. \end{rmk}

\begin{rmk} Both Example \ref{ExampleProfiniteGroupsEquivalentToCertainTopologicalGroups} and Remark \ref{RemarkProfiniteGroupsEquivalentToCertainTopologicalGroups} generalise from $\mathsf{Grp}$ to any [[finite product theory]], that is to say to the category of models of a [[finite product sketch]]. They generalise further to any [[finite limit theory]], that is to say to the category of models of  a [[finite limit sketch]], if the functor $\mathsf{Set} \rightarrow \mathcal{A}$ moreover preserves finite limits. \end{rmk}


## Examples

* [[profinite set]], [[profinite space]]

* [[profinite group]], [[progroup]]

* [[pro-étale morphism of schemes]], [[pro-étale site]]

* Since every ([[dg-coalgebra|dg-]])[[coalgebra]] is the [[filtered colimit]] of its finite-dimensional subalgebras (see at _[coalgebra -- as filtered colimit](coalgebra#AsFilteredColimits)_), the [[linear dual]] of a (dg-)coalgebra is canonically a pro-object in finite dimensional ([[dg-algebra|dg-]])[[associative algebra|algebras]]. This plays a role for instance for constructing [[model structures for L-infinity algebras]], see [there](model+structure+for+L-infinity+algebras#OnProAlg).

* [[pro-category of towers]]

## Applications

### Etale homotopy theory. 

Procategories were used by Artin and Mazur in their work on [[étale homotopy]] theory. They associated to a scheme a “pro-homotopy type”.  (This is discussed briefly at [[étale homotopy]].) The important thing to note is that this was a pro-object in the _homotopy category_ of simplicial sets, i.e., in the pro-homotopy category. Friedlander rigidified their construction to get an object in the pro-category of simplicial sets, and this opened the door to use of 'homotopy pro-categories'.

### Shape theory. 

The form of [[shape theory]] developed by [[Sibe Mardešić]] and [[Jack Segal]], at about the same time as the work in algebraic geometry, again used an approach equivalent to that of the [[pro-homotopy theory|pro-homotopy category]]. Under the name “Čech homotopy theory”, the use more formally of the pro-homotopy category, was introduced by Porter.  Strong shape, developed by Edwards and Hastings, also by [[Tim Porter]] and then in further work by [[Sibe Mardešić]] and [[Jack Segal]], used various forms of rigidification to get to the pro-category of spaces, or of simplicial sets.  There methods of model category theory could be used.
  
  

## Related concepts

* [[ind-object]] / [[ind-object in an (∞,1)-category]]

* **pro-object** / [[pro-object in an (∞,1)-category]]

* [[pro-representable functor]]

* [[ind-pro-object]]

* [[pro-left adjoint]]

* [[pro-homotopy theory]], [[profinite completion of a group]]

* [[2-pro-object]]

## References

* [[Alexander Grothendieck]], Section A.2 of: [[FGA]] *Technique de descente et théorèmes d'existence en géométrie algébriques. II. Le théorème d'existence en théorie formelle des modules*, Séminaire Bourbaki : années 1958/59 - 1959/60, exposés 169-204, Séminaire Bourbaki, no. 5 (1960), Exposé no. 195, 22 p.  ([numdam:SB_1958-1960__5__369_0](http://www.numdam.org/item/?id=SB_1958-1960__5__369_0), English translation: [web version](https://translations.thosgood.com/fga/fga3.ii.xml))

* (SGA4-1) [[Alexander Grothendieck]], [[Jean-Louis Verdier]], _Pr&#233;faisceaux_, Exp. 1 ([retyped pdf](http://www.math.polytechnique.fr/~orgogozo/SGA4/01/01.pdf)) in _Th&#233;orie des topos et cohomologie &#233;tale des sch&#233;mas. Tome 1: Th&#233;orie des topos_, S&#233;minaire de G&#233;om&#233;trie Alg&#233;brique du Bois-Marie 1963&#8211;1964 ([[SGA 4]]). Dirig&#233; par M. Artin, A. Grothendieck, et J. L. Verdier. Avec la collaboration de N. Bourbaki, P. Deligne et B. Saint-Donat. Lecture Notes in Mathematics __269__, Springer 1972. [pdf of SGA 4, Tome 1](http://www.iecn.u-nancy.fr/~gaillapy/SGA/grothendieck_sga_4.1.pdf)


* {#ArtinMazur69} [[Michael Artin]], [[Barry Mazur]], appendix of _&#201;tale homotopy theory_, Lecture Notes in Maths. 100, Springer-Verlag, Berlin 1969.

* {#KashiwaraSchapira06} [[Masaki Kashiwara]], and [[Pierre Schapira]], Section 6 of: _[[Categories and Sheaves]]_, Grundlehren der mathematischen Wissenschaften 332 (2006)

* [[Peter Johnstone]], Section VI.1 of: _[[Stone Spaces]]_

* {#Isaksen02} [[Dan Isaksen]], _Calculating limits and colimits in pro-categories_, Fund. Math. 175 (2002), no. 2, 175&#8211;194.

* {#Lurie} [[Jacob Lurie]], Section 6.1 in: _Ultracategories_ ([pdf](http://www.math.harvard.edu/~lurie/papers/Conceptual.pdf))

* [[Jean-Louis Verdier]], _Equivalence essentielle des syst&#232;mes projectifs_, C. R.A.S. Paris261 (1965), 4950 - 4953.

* [[John Duskin]], _Pro-objects (after Verdier)_, S&#233;m. Heidelberg- Strasbourg1966 -67, Expos&#233; 6, I.R.M.A.Strasbourg. 

* A. Deleanu, P. Hilton, Borsuk shape and Grothendieck categories of pro-objects, Math. Proc. Camb. Phil. Soc.79-3 (1976), 473-482 [MR400220](http://www.ams.org/mathscinet-getitem?mr=400220)

* Walter Tholen, _Pro-categories and multiadjoint functors_, Canadian J. Math. __36__:1 (1984) 144-155 [doi](https://doi.org/10.4153/CJM-1984-010-2)

See also discussion in [[shape theory]]:

* [[Jean-Marc Cordier]], and [[Tim Porter]],  _Shape Theory_, categorical methods of approximation, Dover (2008) (This is a reprint of the 1989 edition without amendments.)

* [[Sibe Mardesic|S. Marde&#353;i&#263;]], [[Jack Segal|J. Segal]], _Shape theory_, North Holland 1982


[[!redirects pro-objects]]
[[!redirects pro object]]
[[!redirects pro-category]]