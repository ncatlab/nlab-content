
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

In [[type theory]] -- where one understands every piece of data (every "[[term]]") as being of a given *[[type]]* which specifies its operational behaviour -- *identity types* (maybe better: *identification types*) $Id_X$ are the types of those terms which serve as "witnesses" or "certificates" (see at "[[propositions as types]]") of identification of terms of type $X$. 

{#WhatExactlyThisMeansDepends} What exactly this means depends on the nature of the ambient [[type theory]] and the choices for the [[inference rules]] of the identity types (see at *[[extensional type theory|extensional]]* and *[[intensional type theory]]*). In some setups (see  [below](#IdeaStrictIdentityTypes)), having a term of identity type means much the same as having an [[equality]] in [[classical mathematics]], and for this (historical) reason identity types are often denoted simply by equality signs, for better or worse. 

But the power of the notion of identity types goes beyond this classical situation and results from the fact that they may give the notion of equality a [[constructive mathematics|constructive]] meaning ("[[propositional equality]]"). Taking this constructive principle of identity types to its logical conclusion, leads -- notably in [[Martin-Löf dependent type theory]], see [below](#IdeaMLIdentityTypes) -- to identity types which themselves have identity types, reflecting identifications-of-identification, and so on, paralleling the [[higher structure]] of [[homotopies]] and [[homotopies of homotopies]] in [[homotopy theory]], whence one refers to type theories with such identity types also as *[[homotopy type theories]]*.

\linebreak

### Note on terminology

There are many different names used for this particular dependent type, as well as many different names used for the terms of this dependent type. These include the following:

| name of type | name of terms |
|--------------|---------------|
| identity type | identities |
| path type | paths |
| identification type | identifications |
| equality type | equalities |

These four names have different reasons behind the use of the name: 

* The name "identity type" comes from the fact that the identity type is the canonical [[one-to-one correspondence]] $a:A, b:A \vdash \mathrm{Id}_A(a, b)$ of the identity [[equivalence in type theory|equivalence]] $\mathrm{id}_A:A \simeq A$ on a type $A$, as well as philosophically that it represents the notion of "identity" of an object; see [[identity of indiscernibles]].

* The name "path type" comes from either the fact that the identity type is a [[path space object]] in the [[categorical semantics]], or that every term in the identity type is represented by a function from the [[interval type]], just as paths in topology are represented by a function from the [[unit interval]]. 

* The name "identification type" comes from the fact that elements represents identification certificates in computing, as well as philosophically that it represents the notion of "identifying" two objects together. 

* The name "equality type" comes from the fact that it is the typal equivalent of [[propositional equality]] from [[first order logic with equality]]. 

### ML identity types
 {#IdeaMLIdentityTypes}

The [[inference rules]] for identity types in [[Martin-Löf dependent type theory|Martin-Löf-]]/[[homotopy type theory]] (ML identity types) may be understood as follows (exposition and diagrams follow [[schreiber:Topological Quantum Gates in Homotopy Type Theory|Myers et al. 2023]]):

\linebreak

**(0) -- There is a notion of identification.** To start with, for every [[type]] $X$ and any [[pair]] $x_1, x_2 : X$ of its [[terms]], let's denote the *type of identifications* of $x_1$ with $x_2$ by $Id_X(x_1,x_2)$ (other common notation for identity types is "$x_1 =_{{}_X} x_2$" which, when adopted, requires authors to make up new symbols, like $\equiv$, for actual equalities).
In the jargon of [[dependent type theory]] this means that there is a [[type formation]] rule for identity types as shown on the left here:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-0-220927.jpg" width="760">
</center>

> Beware that in type theory generally and specifically in this entry further below, the self-identification certificate $id_X$ is often denoted "$refl$", alluding to [[reflexive relation|reflexivity]] of an equality relation.

On the right we are indicating, here and in the following, the [[categorical semantics]] of the [[judgement]] on the left, under the [[relation between type theory and category theory]], specifically [[categorical model of dependent types|between dependent type theory and LCC category theory]]. The lay reader may take the diagrams shown on the right as intuitive illustrations of [[dependent types]] as [[bundles]] of types, their [[terms]] as [[sections]], etc. Technically, these are [[diagrams]] in some [[locally cartesian closed category|locally cartesian closed]] ([[locally cartesian closed model category|model]]) [[category]]. (Beware that we are showing an actual [[interval object]] $I$ for ease of illustration, but its existence is not required by the rules for ML identity types: $X^I$ may denote an object that does not arise as an [[internal hom]]. Making the interval object syntactically explicit leads to "[[cubical identity types]]", see [below](#CubicalIdentityTypes).)

The archetypical example is the ([[classical model structure on simplicial sets|classical model structure on]]) [[SimplicialSets]] 
(with [[interval object]] $I = \Delta[1]$ the [[1-simplex]]) in which case all [[fibrations]] shown are [[Kan fibrations]] between [[Kan complexes]] which may be thought of as models for ([[left fibration|fibrations of]]) [[infinity-groupoid|$\infty$-groupoids]].
But the power of ML identity types is that they may just as well be interpreted in much more general [[model categories]], such as the [[injective model structure on simplicial presheaves]] over any [[simplicial site]], modelling [[(infinity,1)-topos|$\infty$-toposes]] of [[infinity-stack|$\infty$-stacks]].

\linebreak

Now to consider three "self-evident" properties of the notion of identifications (Latin quotes from [[Gottfried Leibniz]] $\sim$ 1700, [p. 228](https://archive.org/details/diephilosophisc00gerhgoog/page/228/mode/2up) and [p. 230](https://archive.org/details/diephilosophisc00gerhgoog/page/228/mode/2up) in [Gerhard 1890](#Gerhard1890)), expressed in type theoretic language:

\linebreak


\begin{imagefromfile}
    "file_name": "OriginalLeibnizQuote-SelfIdentification.jpg",
    "float": "right",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}



**(I) -- All data is identified with itself.**  

This "[[first law of thought]]" is the [[term introduction]]-rule for identity types:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-1-220927.jpg" width="760">
</center>

\linebreak

\begin{imagefromfile}
    "file_name": "OriginalLeibnizQuote-SalvaVeritate.jpg",
    "float": "right",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}



**(IIa) -- Substitution of identifications preserves computations.**  This is Leibniz's "[[salva veritate]]"-principle phrased operationally/constructively:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-2-220928.jpg" width="760">
</center>

In [[homotopy type theory]] this has come to be known as *[[transport]]*, compatible with the fact that its [[categorical semantics]] is that of  path lifting in [[Kan fibrations]], which in the case of [[discrete fibrations]]  ([[covering spaces]]) underlying [[flat  connection|flat]] [[principal bundles]] or [[flat vector bundles]]  ("[[local systems]]") is the [[parallel transport]]/[[holonomy]]/[[monodromy]] of the corresponding [[flat connection]].

\linebreak

\begin{imagefromfile}
    "file_name": "OriginalLeibnizQuote-Composition.jpg",
    "float": "right",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}


{#UniquenessAxiomInIntroduction} **(IIb) -- An identification identifies itself with a self-identification.** While one may argue that this is still "self-evident", it is more subtle than the previous two principles.  In particular, it concerns an *identification of identifications*, a possibility that was ignored by the logical forefathers (Leibniz highlights at least the [[composition]] of identifications, such as $p \cdot id_x$).

\begin{tikzcd}
  & 
  x
  \ar[
    dl, 
    "{ \scalebox{.6}{\clap{self-identification}} }"{sloped, swap,  pos=.45},
    "{\mathrm{id}_x}"{pos=.4, yshift=2pt},
    "{ }"{name=s,  pos=.82}
  ]
  \ar[
    dr, 
    "{ \scalebox{.6}{\clap{an identification}} }"{sloped,  pos=.45},
    "{p}"{swap, pos=.4, yshift=2pt},
    "{ }"{name=t, swap,  pos=.82}
  ]
  \ar[
    from=s, to=t,
    Rightarrow,
    "{ \scalebox{.6}{ 
      \clap{identification-of-identifications}
    } }"{swap}
  ]
  \\
  x
  \ar[
    rr,
    "{
      p
    }"{swap}
  ]
  &&
  x'
\end{tikzcd}

In type theory language, the existence of these identifications-of-identifications is the following [[judgement]] (with $\underset{x'  : X}{\coprod}$ denoting the [[dependent sum]]-type):

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-3-220928b.jpg" width="760">
</center>

{#SemanticsOfUniquenessAxiomInSimplicialSets} (An intuitive [[categorical semantics]] is schematically indicated on the right, with the certificate $p_*$ pictured as a copy of $p$ on the bottom together with a "path-of-paths" relating the concatenated path $p \bullet id_x$ to $p$.  This is valid when realized in the [[classical model structure on simplicial sets|model structure on simplicial sets]] or any [[model structure on simplicial presheaves]], literally given by triangular diagrams as above, these being [[1-simplices]] in $X^I \underset{ev_0}{\times} \{x\}$ when [[internal hom|hom]]-[[adjoint functor|adjointly]] regarded as [[2-simplices]] in $X$.  However, this is not literally what the principle says when expressed in type theory, where there is no concatenated path $p \bullet id_x$ --- although after we have identity types with all of their rules, it can be proved equivalent.)

\linebreak


**(J) $\Leftrightarrow$ (II) -- Id-induction.** 
Applying the above [[transport]]  rule (IIa) to the identifications-of-identifications provided by the composition rule  (IIb) yields the following  "[[J-rule]]", which was not known to  the forefathers:

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-4-220928.jpg" width="760">
</center>

(This "[[induction]]-rule" for identity types was proposed in [Martin-Löf 1975, §1.7 and p. 94 ](#MartinLof75); its modern rendering as a formal [[inference rule]] is due to [Nordström,  Petersson & Smith 1990,  §8.1](#NordströmPeterssonSmith90). It may be understood as the [[term  elimination rule]] (see [below](identity+type#ExplicitDefinition)) or the [[induction]]-principle (see [further below](identity+type#InTermsOfInductiveTypes)) for identity types, whence also called "Id-elimination" or "Id-induction", or similar.)

While the J-rule is naturally understood as the application of the transport rule (IIa) to the identifications-of-identification provided by the composition rule (IIb), it also implies both these  rules, hence is equivalent to their combination (IIa and IIb). 
(This fact was briefly mentioned by [Coquand 2011, slides 26+28](#Coquand11) and amplified by [Ladyman & Presnell 2015](#LadymanPresnell15);  the detailed proof is spelled out by [Götz 2018, §4.2](#Götz18).) 

Importantly, as indicated on the right above, the [[categorical semantics]]  of the [[J-rule]] is manifestly that of the [[left lifting property]] of $X \xrightarrow{diag} X^I$ against all [[fibrations]], which means that this rule manifestly prescribes the [[categorical semantics|interpretation]] of identity types by "[[very good path space objects]] " in the sense of [[model category theory]] (cf. [Shulman 2012](#Shulman12) [III, Slide 34](http://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=34); [Riehl  2022,  §1.1](#Riehl22)). 
It is this fact which connects ML identity types to the notion of [[homotopy]] in [[homotopy theory]],  hence to the interpretation of [[Martin-Löf dependent type theory]] as  "[[homotopy type theory]]" with [[categorical semantics]] in  [[locally cartesian closed (infinity,1)-category|locally cartesian closed  $\infty$-categories]].
 
\linebreak

{#PathLiftingInIdeaSection}  Incidentally, another immediate  consequence of the [[J-rule]] is the following refinement of the [[transport]] rule (IIa), which is closer to what Leibniz may have recognized:

**(IIa') -- Substitution of identifications preserves identifications.**  

<center>
<img src="/nlab/files/MetaLogicOfIdentifications-5-220928b.jpg" width="760">
</center>



\linebreak

### Cubical identity types
 {#CubicalIdentityTypes}

Besides the Martin-Löf identity types [above](#IdeaMLIdentityTypes)  there are other version of identity types considered in the literature, notably there are variants which share the [[homotopy type theory|homotopy-theoretic]] interpretation but differ in some technical details:

For instance, [[cubical identity types]] (such as Swan identity types) are the identity types in [[cubical type theory]], which are such that that applied to the [[type universe]] they *provably* (computationally) satisfy the [[univalence axiom]].

Namely, the [[J-rule]] in [[Martin-Löf dependent type theory]] [above](#IdeaMLIdentityTypes) still involves an ordinary [[judgmental equality]] in its statement that the lifted term $\widehat{\sigma}$ is *equal* to the given term $\sigma$ after restriction to self-identitfication. Cubical identity types essentially turns this equality itself into a [[typal equality]]. 


Similarly, [[higher observational type theory]] has its appropriate version of higher identity types.

\linebreak

Notice that higher identity types restricted specifically to [[h-sets]] behave again more like ordinary [[equality]] does (by definition of [[h-set]]).

More specifically, there are also *strict* identity types, strictly without an homotopy-theoretic interpretation:

### Strict identity types
  {#IdeaStrictIdentityTypes}

Since there are two notions of [[equality]] in type theory, there are similarly two notions of the J-rule in type theory. The **judgmental J-rule** states that $J(x, x, \mathrm{refl}(x))$ is judgmentally equal to $c(x)$ (i.e. $J(x, x, \mathrm{refl}(x)) = c(x)$). This is in  contrast to the **typal J-rule** above,  which states that there is a dependent term 
$$q(x):Id_{C(x,x,\mathrm{refl}(x))}(J(x, x, \mathrm{refl}(x)), c(x))$$

Identity types which satisfy the judgmental J-rule can be called **strict identity types**, while identity types which only satisfy the typal J-rule can be called **weak identity types**, in parallel with similar definitions for a (weak and strict) [Tarski universe](type+universe#TarskiStyle). Martin-Löf identity types come in both strict and weak flavours. However, most other identity types in the literature, such as cubical path types and higher observational identity types, are only weak identity types.


\linebreak


## Definition in Martin-Löf type theory
 {#Definition}

The definition of identity types was originally given in explicit form by [[Per Martin-Löf|Martin-Löf]], in terms of [[inference rules]].  Later, it was realized that this was a special case of the general notion of [[inductive type]].  We will discuss both formulations.

* [with inference rules](#ExplicitDefinition).

* [in terms of inductive types](#InTermsOfInductiveTypes) 

### With inference rules
 {#ExplicitDefinition}

The [[inference rules]] for forming identity types and terms are as follows.  

First the rule that defines the identity type itself, as a [[dependent type]], in some [[context]] $\Gamma$.

**[[type formation]]**

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A, y:A \vdash Id_A(x,y):Type}$$

Now the basic "introduction" rule, which says that everything is equal to itself in a canonical way.

**[[term introduction]]**

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A \vdash r(x) : Id_A(x,x)}$$

To a category theorist, it might be more natural to call this $1_X$.  The traditional notation $r(x)$ indicates that this is a canonical proof of the *[[reflexive relation|reflexivity]]* of equality.

Then there are the "elimination" rule and the "computation" or [[beta-reduction]] rule of identity types, which together result in the induction principle of identity types. There are two different ways to express the elimination and computation rule of identity types, depending on whether one fixes a particular term $x:A$ for the rules or whether one leaves $x:A$ as a [[free variable]] throughout the rules (Cf [UFP13](#UFP13)). The latter results in the usual induction principle of identity types, known as **path induction** ([UFP13](#UFP13)) or the **standard J rule** ([Kraus and Raumer (2019)](#KrausRaumer19)), while the former results in **based path induction** ([UFP13](#UFP13)) or the **Paulin-Mohring J rule** ([Kraus and Raumer (2019)](#KrausRaumer19)), since the principle is based at a particular $x:A$ and was first defined in [Paulin-Mohring (1993)](#PaulinMohring93). 

The following rules may seem a little ad-hoc, but they are actually a particular case of the general notion of [[inductive type]].

#### Standard J rule

Then we have the “elimination” rule, which is easily the most subtle and powerful.

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \quad \Gamma, x:A, \Delta(x,x,r(x)) \vdash t(x):C(x,x,r(x))}
{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash J^{\underline{ }.t}(x,y,p) : C(x,y,p)}$$

Ignore the presence of the additional context $\Delta$ for now; it is unnecessary if we also have [[dependent product types]]. The elimination rule then says that if:

1. for any $x,y:A$ and any reason $p:Id_A(x,y)$ why they are the same, we have a type $C(x,y,p)$
1. for any $x:A$ we have a $t(x):C(x,x,r(x))$,

we can construct a canonically defined term $J^{\underline{ }.t}(x,y,p):C(x,y,p)$ for *any* $x$, $y$, and $p:Id_A(x,y)$, by "[[transport|transporting]]" the family of terms $t(x)$ dependent upon $x:A$ along the proof of equality $p$. In homotopical or categorical models, this can be viewed as a "path-lifting" property, i.e. that the [[display map]]s are some sort of [[fibration]], which can be made precise with the [[identity type weak factorization system]]. 

A particular case is when $C$ is a term representing a proposition according to the propositions-as-types philosophy. In this case, the elimination rule says that in order to prove a statement is true about all $x,y,p$, it suffices to prove it in the special case for $x,x,r(x)$.

Finally, we have the "computation" or [[beta-reduction]] rule. There are two possible computation rules, which result in strict and weak identity types respectively. The computation rule for strict identity types says that if we substitute along a [[reflexive relation|reflexivity]] proof, nothing happens. 

**[[computation rule]] for strict identity types**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, \Delta(x,x,r(x)) \vdash t(x):C(x,x,r(x))}
{\Gamma, x:A, \Delta(x,x,r(x)) \vdash J^{\underline{ }.t}(x,x,r(x)) = t(x)}$$

Note that the equality $=$ in the conclusion of this computation rule is [[judgmental equality]], not an instance of the identity/equality type itself.

The computation rule for weak identity types says that there is a witness that the substitution along a [[reflexive relation|reflexivity]] proof is equal to the original $t(x)$. 

**[[computation rule]] for weak identity types**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, \Delta(x,x,r(x)) \vdash t(x):C(x,x,r(x))}
{\Gamma, x:A, \Delta(x,x,r(x)) \vdash \beta^{\underline{ }.t}(x):Id_{C(x,x,r(x))}(J^{\underline{ }.t}(x,x,r(x)),t(x))}$$

If we have [[dependent product types]], we can directly use the [[dependent function]] $\Gamma \vdash t:\prod_{x:A} C(x,x,r(x))$ instead of the family of terms $t(x)$ dependent upon $x:A$ in the hypothesis. Then the canonically defined term is given by $J(t,x,y,p):C(x,y,p)$ and is dependent upon dependent function $t:\prod_{x:A} C(x,x,r(x))$ rather than annotated with the family $t(x)$. 

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \quad \Gamma \vdash t:\prod_{x:A} C(x,x,r(x))}
{\Gamma, x:A, y:A, p:Id_A(x,y) \vdash J(t,x,y,p) : C(x,y,p)}$$

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma \vdash t:\prod_{x:A} C(x,x,r(x))}
{\Gamma, x:A, \Delta(x,x,r(x)) \vdash J(t,x,x,r(x)) = t(x)}$$

The original inference rules using the family of terms $t(x)$ dependent upon $x:A$ is then given by $J(\lambda x:A.t(x),x,y,p):C(x,y,p)$ and $J(\lambda x:A.t(x),x,x,r(x)) \equiv t(x):C(x,x,r(x))$. . 

Similarly, the canonically defined term in the propositional computation rule is given by the identification $\beta(t,x):Id_{C(x,x,r(x))}(J(t,x,x,r(x)),t(x))$ and is dependent upon dependent function $t:\prod_{x:A} C(x,x,r(x))$ rather than annotated with the family $t(x)$.

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma \vdash t:\prod_{x:A} C(x,x,r(x))}
{\Gamma, x:A, \Delta(x,x,r(x)) \vdash \beta(t,x):Id_{C(x,x,r(x))}(J(t,x,x,r(x)),t(x))}$$

The original inference rules using the family of terms $t(x)$ dependent upon $x:A$ is then given by $\beta(\lambda x:A.t(x),x):\mathrm{Id}_{C(x,x,r(x))}(J(\lambda x:A.t(x),x,x,r(x)),t(x))$. . 

#### Paulin-Mohring J rule

There is another way to express the elimination and computation rules of identity types:

**[[term elimination]]**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y) \vdash C(x,y,p):Type \quad \Gamma \vdash x:A \quad \Gamma \vdash t:C(x,x,r(x))}
{\Gamma, y:A, p:Id_A(x,y) \vdash J(x,t,y,p) : C(x,y,p)}$$

The elimination rule then says that if:

1. for any $x,y:A$ and identification $p:Id_A(x,y)$ why $y$ is the same as $x$, we have a type $C(x,y,p)$, and 
1. for any $x:A$ and $t:C(x,x,r(x))$ 

we can construct a canonically defined term $J(x,t,y,p):C(x,y,p)$ for *any* $y:A$, and $p:Id_A(x,y)$, by "[[transport|transporting]]" the term $t$ along the proof of equality $p$. In homotopical or categorical models, this can be viewed as a "path-lifting" property, i.e. that the [[display map]]s are some sort of [[fibration]], which can be made precise with the [[identity type weak factorization system]]. 

According to [[propositions as types]], the elimination rule says that for all $x$, in order to prove a statement is true about all $y,p$, it suffices to prove it in the special case for $x,r(x)$.

Finally, we have the "computation" or [[beta-reduction]] rule. There are two possible computation rules, which result in strict and weak identity types respectively. The computation rule for strict identity types says that if we substitute along a [[reflexive relation|reflexivity]] proof, nothing happens. 

**[[computation rule]] for strict identity types**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y) \vdash C(x,y,p):Type \quad \Gamma \vdash x:A \quad \Gamma \vdash t:C(x,x,r(x))}
{\Gamma \vdash J(x,t,x,r(x)) = t}$$

Note that the equality $=$ in the conclusion of this computation rule is [[judgmental equality]], not an instance of the identity/equality type itself.

The computation rule for weak identity types says that there is a witness that the substitution along a [[reflexive relation|reflexivity]] proof is equal to the original term $t$. 

**[[computation rule]] for weak identity types**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(y,p) \vdash C(x,y,p):Type \quad \Gamma \vdash x:A \quad \Gamma \vdash t:C(x,x,r(x))}
{\Gamma \vdash \beta(x,t):Id_{C(x,x,r(x))}(J(x,t,x,r(x)) ,t)}$$

#### Identity types as a negative type

If one has [[dependent sum types]], there is a way of defining the identity type as a [[negative type]]. The idea is that using the inference rules for dependent sum types, the standard J-rule states that the dependent sum type $\sum_{x:A} \sum_{y:A} x =_A y$ is a [[positive copy]] of $A$ with respect to the [[diagonal function]] 
$$\Delta_{A}(x) \coloneqq (x, (x, \mathrm{refl}_A(x))):\sum_{x:A} \sum_{y:A} x =_A y$$
However, there is also a negative version of [[copy types]], whose elimination, computation, and uniqueness rules state that the [[diagonal function]] is a [[definitional isomorphism]]: 

* Elimination rules for negative identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash \Delta_A^{-1}(z):A}$$

* Computation rules for negative identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \Delta_A^{-1}(\Delta_{A}(x)) \equiv x:A}$$

* Uniqueness rules for negative identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash \Delta_{A}(\Delta_A^{-1}(z)) \equiv z:\sum_{x:A} \sum_{y:A} x =_A y}$$

\begin{theorem}
The standard J-rule holds: given any type $A$, and any type family $C(z)$ indexed by elements $z:\sum_{x:A} \sum_{y:A} x =_A y$, and given any dependent function $t:\prod_{x:A} C(\Delta_A(x))$ which says that for all elements $x:A$,  there is an element of the type defined by substituting the diagonal at $x:A$ into $C$, $C(\Delta_A(x))$, one can construct a dependent function $\mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(t):\prod_{z:\sum_{x:A} \sum_{y:A} x =_A y} C(z)$ such that for all $x:A$, $\mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(\Delta_A(x)) \equiv t(x):C(\Delta_A(x))$. 
\end{theorem}

\begin{proof}
$\mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(t)$ is defined to be

$$\mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(t) \equiv \lambda z:\sum_{x:A} \sum_{y:A} x =_A y.t(\Delta_A^{-1}(z))$$

and by the computation rules of path types as negative copies, one has that for all $x:A$, 

$$\Delta_A^{-1}(\Delta_A(x)) \equiv x$$

and so by definition of $\mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(t)$ and the judgmental congruence rules for substitution, one has

$$\mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(t, \Delta_A(x)) \equiv t(\Delta_A^{-1}(\Delta_A(x))) \equiv t(x)$$
\end{proof}

### Induction using functions instead of type families

There is a version of the induction principle which uses a type $C$ and a function $f:C \to \sum_{x:A} \sum_{y:A} x =_A y$ into the type of all identity types in $A$, instead of a type family $C(x, y, p)$ indexed by $x:A$, $y:A$, and $p:x =_A y$. 

Let 
$$\Delta_A \coloneqq \lambda x:A.(x, x, \mathrm{refl}_A(x)):A \to \sum_{x:A} \sum_{y:A} x =_A y$$ 
be the [[diagonal function]] of $A$. 

The induction principle for the identity type says that given any type $C$ and function 
$$f:C \to \sum_{x:A} \sum_{y:A} x =_A y$$ 
into the type of all identity types in $A$, and given a function $c:A \to C$ and a homotopy 
$$p:\prod_{x:A} f(c(x)) =_{\sum_{x:A} \sum_{y:A} x =_A y} \Delta_A(x)$$
which states that the composite of $f$ and $c$ is the diagonal, one can construct 

* a function

$$g:\left(\sum_{x:A} \sum_{y:A} x =_A y\right) \to C$$

* a homotopy witnessing that $g$ is a [[section]] of $f$:

$$\mathrm{sec}_g:\prod_{z:\sum_{x:A} \sum_{y:A} x =_A y} f(g(z)) =_{\sum_{x:A} \sum_{y:A} x =_A y} z$$

such that for all $x:A$, $g(\Delta_A(x)) \equiv c(x)$ and $\mathrm{sec}_g(\Delta_A(x)) \equiv p(x)$.

By [[currying]] this is the same as saying that one can construct 

* a family of functions

$$g:\prod_{x:A} \prod_{y:A} (x =_A y) \to C$$

* a family of functions:

$$\mathrm{sec}_g:\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} f(g(x, y, p)) =_{\sum_{x:A} \sum_{y:A} x =_A y} (x, y, p)$$

such that for all $x:A$, $g(x, x, \mathrm{refl}_A(x)) \equiv c(x)$ and $\mathrm{sec}_g(x, x, \mathrm{refl}_A(x)) \equiv p(x)$.

### In terms of inductive types
 {#InTermsOfInductiveTypes}

Using [[inductive types]] the notion of identity types is encoded in a single line (see [Licata 11](#Licata11), [Shulman 12](#Shulman12)). 

In [[Coq]] notation we can say

    Inductive id {A} : A -> A -> Type := idpath : forall x, id x x.   

In other words, the identity type of $A$ is inductively generated by [[reflexive relation|reflexivity]] $x = x$ (the "[[first law of thought]]"), in the same way that the [[natural numbers]] are inductively generated by [[zero]] and [[successor]].  From this, the above introduction, elimination, and computation rules are all derived automatically.

This is the approach to Martin-Lof identity types taken by implementations of [[homotopy type theory]] in [[proof assistants]] such as [[Coq]] or [[Agda]].  See, for instance, [Overture.v](#Overturev)

An essentially equivalent way to give the definition, due to Paulin-Mohring, is

    Inductive id {A} (x:A) : A -> Type := idpath : id x x.   

The difference here is that now $x$ is a *parameter* of the inductive definition rather than an *index*.  In other words, the first definition says "for each type $A$, we have a type $Id_A$ dependent on $A\times A$, inductively defined by a constructor $idpath$ which takes an element $x\colon A$ as input and yields output in $Id_A(x,x)$" while the second definition says "for each type $A$ and each element $x\colon A$, we have a type $Id_A(x)$ dependent on $A$, inductively defined by a constructor $idpath$ which takes *no* input and yields output in $Id_A(x)(x)$."  The two formulations can be proven equivalent, but sometimes one is more convenient than the other.

### $\eta$-conversion and the reflection rule
 {#EtaConversion}

Almost all types in type theory can be given both [[beta-reduction]] and [[eta-reduction]] rules.  $\beta$-reduction specifies what happens when we apply an eliminator to a term obtained by a constructor; $\eta$-reduction specifies the reverse.  Above we have formulated only the $\beta$-reduction rule for identity types; the $\eta$-conversion rule would be the following:

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,x,r(x)) \vdash t : C(x,y,p)}
{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash J(t[x/y, r(x)/p];x,y,p) = t}$$

This says that if $C$ is a type which we can use the eliminator $J$ to construct a term of, but we already *have* a term $t$ of that type, then if we restrict $t$ to [[reflexive relation|reflexivity]] inputs and then apply $J$ to construct a term of type $C$, the result is the same as the term $t$ we started with.  As in the $\beta$-reduction rule, the $=$ in the conclusion refers to [[judgmental equality]].

This $\eta$-conversion rule has some very strong consequences.  For instance, suppose $x\colon A$, $y\colon A$, and $p\colon Id_A(x,y)$, and let $C \coloneqq A$.  Then with $t=x$, the $\eta$-conversion rule tells us that $x = J(x[x/y,r(x)/p];x,y,p)$.  And with $t=y$, the $\eta$-conversion rule tells us that $y = J(y[x/y,r(x)/p];x,y,p)$.  But substituting $x$ for $y$ (and $r(x)$ for $p$) in the term $y$ simply yields the term $x$, which is the same as the result of substituting $x$ for $y$ and $r(x)$ for $p$ in the term $x$.  Thus, we have

$$x = J(x;x,y,p) = y$$

In other words, if $Id_A(x,y)$ is inhabited (that is, $x$ and $y$ are typally equal) then in fact $x$ and $y$ are judgmentally equal.  Moreover, by a similar argument we can show that

$$p = J(p[x/y, r(x)/p];x,y,p) = J(r(x)[x/y,r(x)/p];x,y,p) = r(x).$$

(Here we are eliminating into the type $C(x,y,p) \coloneqq Id_A(x,y)$.  The term $r(x)$ may be regarded as belonging to this type, because we have already shown that $x$ and $y$ are *judgmentally* equal.)

Thus, the judgmental $\eta$-conversion rule for identity types implies the "reflection rule" for identity types, which in turn implies that the type theory is [[set-level type theory|set-level]].  (This was observed already in ([Streicher](#Streicher)).)  In particular, in [[homotopy type theory]] we cannot assume the $\eta$-conversion rule for identity types.

However, the reflection rule for identity types is also problematic for non-homotopical reasons: since type-checking in dependent type theory depends on judgmental equality, but the above rule implies that judgmental equality depends on inhabitation of identity types, this makes judgmental equality and hence type-checking *undecidable* in the formal computational sense.  Thus, $\eta$-conversion for identity types is often omitted even in set-level type theories (e.g. [[Coq]] and [[Agda]]).

On the other hand, it is possible to prove a *typal* version of $\eta$-conversion using only the identity types as defined above without judgmental $\eta$-conversion.  In other words, given the hypotheses of the above $\eta$-conversion rule, we can construct a term belonging to the type

$$ Id_{C(x,y,p)}(J(t[x/y, r(x)/p];x,y,p), t). $$

This has none of the bad consequences of judgmental $\eta$-conversion, and in particular does not imply that the type theory is extensional.  The argument that $p\colon Id_A(x,y)$ implies $x=y$ becomes the tautologous statement that if $p\colon Id_A(x,y)$ then $p\colon Id_A(x,y)$, while the subsequent argument that $p= r(x)$ fails because $x$ and $y$ are no longer *judgmentally* equal, so $r(x)$ does not have type $Id_A(x,y)$.  We can *[[transport]]* it along $p$ to obtain a term of this type, but then we obtain only that $p$ is equal to the transport of $r(x)$ along $p$, which is a perfectly intensional/homotopical statement.

### Dependent universal property

The identity types in Martin-Löf type theory satisfy the typal $\beta$-conversion and typal $\eta$-conversion rules, regardless if the original $\beta$-conversion and $\eta$-conversion rules used [[typal equality]] or [[judgmental equality]]. The elimination rule in conjunction with the typal $\beta$-conversion and typal $\eta$-conversion rules state that identity types satisfy the **dependent universal property of identity types**. If the dependent type theory also has [[dependent sum types]] [[product types]], [[dependent product types]], and [[dependent function types]], allowing one to define the [[uniqueness quantifier]], the dependent universal property of the natural numbers can be simplified to the following rule: 

$$
\frac{\Gamma, x:A, y:A, p:\mathrm{Id}_A(x, y) \vdash C(x, y, p) \; \mathrm{type} \quad \Gamma \vdash t:\prod_{c:A} C(c, c, \mathrm{Id}_A(c)) \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{up}_{\mathrm{Id}_A}(t, a):\exists!J:\left(\prod_{c:A} C(c, c, \mathrm{id}_A(c))\right) \to \left(\prod_{x:A} \prod_{y:A} \prod_{p:\mathrm{Id}_A(x, y)} C(x, y, p)\right).\mathrm{Id}_{C(a, a, \mathrm{id}_A(a))}(J(t, a, a, \mathrm{id}_A(a)), t(a))}
$$

### Variants of the identity type

Given a type $A$, two elements $x:A$ and $y:A$ is equivalently 

* a function $\mathrm{rec}_\mathbb{2}^A(x, y):\mathbb{2} \to A$ from $\mathbb{2}$ to $A$ by the recursion and uniqueness principle of the [[boolean domain]] $\mathbb{2}$, 

* a [[pair]] $\mathrm{in}(x, y):A \times A$ by the introduction rule of [[pair types]] $A \times A$. 

From the other side, a function $f:\mathbb{2} \to A$ is equivalently two elements $f(0):A$ and $f(1):A$, and by the negative recursion and uniqueness rules of [[pair types]], a pair $z:A \times A$ is equivalently two elements $\pi_1(z):A$ and $\pi_2(z)$. This implies that one can define two variants of the identity type, 

* a variant $\mathrm{Id}_A(f)$ indexed by functions $f:\mathbb{2} \to A$ out of the boolean domain, where the usual identity type is then defined as 
$$x =_A y \coloneqq \mathrm{Id}_A(\mathrm{rec}_\mathbb{2}^A(x, y))$$

* a variant $\mathrm{Id}_A(z)$ indexed by pairs $z:A \times A$, where the usual identity type is then defined as 
$$x =_A y \coloneqq \mathrm{Id}_A(\mathrm{in}(x, y))$$

#### Identity types indexed by functions from the booleans

The inference rules for identity types indexed by functions from the booleans is given as follows:

First the rule that defines the identity type itself, as a [[dependent type]], in some [[context]] $\Gamma$.

**[[type formation]]**

$$\frac{\Gamma \vdash A:Type}{\Gamma, f:\mathbb{2} \to A \vdash Id_A(f):Type}$$

Now the basic "introduction" rule, which says that the elements of $A$ encoded in the [[constant function]] $\lambda b:\mathbb{2}.x$ which sends every boolean $b:\mathbb{2}$ to $x:A$ are equal in a canonical way.

**[[term introduction]]**

$$\frac{\Gamma \vdash A:Type}{\Gamma, x:A \vdash r(x) : Id_A(\lambda b:\mathbb{2}.x)}$$

Then we have the “elimination” rule:

$$\frac{\Gamma, f:\mathbb{2} \to A, p:Id_A(f), \Delta(f,p) \vdash C(f,p):Type \quad \Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash t(x):C(\lambda b:\mathbb{2}.x,r(x))}
{\Gamma, f:\mathbb{2} \to A, p:Id_A(f) \vdash J^{\underline{ }.t}(f,p) : C(f,p)}$$

The elimination rule then says that if:

1. for any $f:\mathbb{2} \to A$ and any reason $p:Id_A(f)$ why the two elements of $A$ encoded in the functions are the same, we have a type $C(f,p)$
1. for any $x:A$ we have a $t(x):C(\lambda b:\mathbb{2}.x,r(x))$,

we can construct a canonically defined term $J^{\underline{ }.t}(f,p):C(f,p)$ for *any* $f$ and $p:Id_A(f)$, by "[[transport|transporting]]" the family of terms $t(x)$ dependent upon the element $x:A$ along the proof of equality $p$. The elimination rule alternatively says that in order to prove a statement is true about all $f,p$, it suffices to prove it in the special case for $\lambda b:\mathbb{2}.x,r(x)$.

Finally, we have the "computation" or [[beta-reduction]] rule. There are two possible computation rules, which result in strict and weak identity types respectively. The computation rule for strict identity types says that if we substitute along a [[reflexive relation|reflexivity]] proof, nothing happens. 

**[[computation rule]] for strict identity types**

$$\frac{\Gamma, f:\mathbb{2} \to A, p:Id_A(f), \Delta(f,p) \vdash C(f,p):Type \quad \Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash t(x):C(\lambda b:\mathbb{2}.x,r(x))}
{\Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash J^{\underline{ }.t}(\lambda b:\mathbb{2}.x,r(x)) = t(x)}$$

Note that the equality $=$ in the conclusion of this computation rule is [[judgmental equality]], not an instance of the identity/equality type itself.

The computation rule for weak identity types says that there is a witness that the substitution along a [[reflexive relation|reflexivity]] proof is equal to the original $t(x)$. 

**[[computation rule]] for weak identity types**

$$\frac{\Gamma, f:\mathbb{2} \to A, p:Id_A(f), \Delta(f,p) \vdash C(f,p):Type \quad \Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash t(x):C(\lambda b:\mathbb{2}.x,r(x))}
{\Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash \beta^{\underline{ }.t}(x):Id_{C(\lambda b:\mathbb{2}.x,r(x))}(J^{\underline{ }.t}(\lambda b:\mathbb{2}.x,r(x)),t(x))}$$

If we have [[dependent product types]], we can directly use the [[dependent function]] $\Gamma \vdash t:\prod_{x:A} C(\lambda b:\mathbb{2}.x,r(x))$ instead of the family of terms $t(x)$ dependent upon $x:A$ in the hypothesis. Then the canonically defined term is given by $J(t,f,p):C(f,p)$ and is dependent upon dependent function $t:\prod_{x:A} C(\lambda b:\mathbb{2}.x,r(x))$ rather than annotated with the family $t(x)$. 

$$\frac{\Gamma, f:\mathbb{2} \to A, p:Id_A(f), \Delta(f,p) \vdash C(f,p):Type \quad \Gamma \vdash t:\prod_{x:A} C(\lambda b:\mathbb{2}.x,r(x))}
{\Gamma, f:\mathbb{2} \to A, p:Id_A(f) \vdash J(t,f,p) : C(f,p)}$$

$$\frac{\Gamma, f:\mathbb{2} \to A, p:Id_A(f), \Delta(f,p) \vdash C(f,p):Type \qquad
\Gamma \vdash t:\prod_{x:A} C(\lambda b:\mathbb{2}.x,r(x))}
{\Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash J(t,\lambda b:\mathbb{2}.x,r(x)) = t(x)}$$

The original inference rules using the family of terms $t(x)$ dependent upon $x:A$ is then given by $J(\lambda x:A.t(x),f,p):C(f,p)$ and $J(\lambda x:A.t(x),\lambda b:\mathbb{2}.x,r(x)) \equiv t(x):C(\lambda b:\mathbb{2}.x,r(x))$. . 

Similarly, the canonically defined term in the propositional computation rule is given by the identification $\beta(t,x):Id_{C(\lambda b:\mathbb{2}.x,r(x))}(J(t,\lambda b:\mathbb{2}.x,r(x)),t(x))$ and is dependent upon dependent function $t:\prod_{x:A} C(\lambda b:\mathbb{2}.x,r(x))$ rather than annotated with the family $t(x)$.

$$\frac{\Gamma, f:\mathbb{2} \to A, p:Id_A(f), \Delta(f,p) \vdash C(f,p):Type \qquad
\Gamma \vdash t:\prod_{x:A} C(\lambda b:\mathbb{2}.x,r(x))}
{\Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash \beta(t,x):Id_{C(\lambda b:\mathbb{2}.x,r(x))}(J(t,\lambda b:\mathbb{2}.x,r(x)),t(x))}$$

The original inference rules using the family of terms $t(x)$ dependent upon $x:A$ is then given by $\beta(\lambda x:A.t(x),x):\mathrm{Id}_{C(\lambda b:\mathbb{2}.x,r(x))}(J(\lambda x:A.t(x),\lambda b:\mathbb{2}.x,r(x)),t(x))$.  

#### Identity types indexed by pairs

The inference rules for identity types indexed by pairs is given as follows:

First the rule that defines the identity type itself, as a [[dependent type]], in some [[context]] $\Gamma$.

**[[type formation]]**

$$\frac{\Gamma \vdash A:Type}{\Gamma, z:A \times A \vdash Id_A(z):Type}$$

Now the basic "introduction" rule, which says that the elements encoded in the non-dependent [[diagonal]] $\Delta_A(x) \coloneqq \lambda x:A.(x, x)$ at $x:A$ are equal in a canonical way.

**[[term introduction]]**

$$\frac{\Gamma \vdash A:Type}{\Gamma, x:A \vdash r(x) : Id_A(\Delta_A(x))}$$

Then we have the “elimination” rule:

$$\frac{\Gamma, z:A \times A, p:Id_A(z), \Delta(z,p) \vdash C(z,p):Type \quad \Gamma, x:A, \Delta(\Delta_A(x),r(x)) \vdash t(x):C(\Delta_A(x),r(x))}
{\Gamma, z:A \times A, p:Id_A(z) \vdash J^{\underline{ }.t}(z,p) : C(z,p)}$$

The elimination rule then says that if:

1. for any $z:A \times A$ and any reason $p:Id_A(z)$ why the two elements of $A$ encoded in the pair are the same, we have a type $C(z,p)$
1. for any $x:A$ we have a $t(x):C(\Delta_A(x),r(x))$,

we can construct a canonically defined term $J^{\underline{ }.t}(z,p):C(z,p)$ for *any* $z$ and $p:Id_A(z)$, by "[[transport|transporting]]" the family of terms $t(x)$ dependent upon the element $x:A$ along the proof of equality $p$. The elimination rule alternatively says that in order to prove a statement is true about all $z,p$, it suffices to prove it in the special case for $\Delta_A(x),r(x)$.

Finally, we have the "computation" or [[beta-reduction]] rule. There are two possible computation rules, which result in strict and weak identity types respectively. The computation rule for strict identity types says that if we substitute along a [[reflexive relation|reflexivity]] proof, nothing happens. 

**[[computation rule]] for strict identity types**

$$\frac{\Gamma, z:A \times A, p:Id_A(z), \Delta(z,p) \vdash C(z,p):Type \quad \Gamma, x:A, \Delta(\Delta_A(x),r(x)) \vdash t(x):C(\Delta_A(x),r(x))}
{\Gamma, x:A, \Delta(\Delta_A(x),r(x)) \vdash J^{\underline{ }.t}(\Delta_A(x),r(x)) = t(x)}$$

Note that the equality $=$ in the conclusion of this computation rule is [[judgmental equality]], not an instance of the identity/equality type itself.

The computation rule for weak identity types says that there is a witness that the substitution along a [[reflexive relation|reflexivity]] proof is equal to the original $t(x)$. 

**[[computation rule]] for weak identity types**

$$\frac{\Gamma, z:A \times A, p:Id_A(z), \Delta(z,p) \vdash C(z,p):Type \quad \Gamma, x:A, \Delta(\Delta_A(x),r(x)) \vdash t(x):C(\Delta_A(x),r(x))}
{\Gamma, x:A, \Delta(\Delta_A(x),r(x)) \vdash \beta^{\underline{ }.t}(x):Id_{C(\Delta_A(x),r(x))}(J^{\underline{ }.t}(\Delta_A(x),r(x)),t(x))}$$

If we have [[dependent product types]], we can directly use the [[dependent function]] $\Gamma \vdash t:\prod_{x:A} C(\Delta_A(x),r(x))$ instead of the family of terms $t(x)$ dependent upon $x:A$ in the hypothesis. Then the canonically defined term is given by $J(t,z,p):C(z,p)$ and is dependent upon dependent function $t:\prod_{x:A} C(\Delta_A(x),r(x))$ rather than annotated with the family $t(x)$. 

$$\frac{\Gamma, z:A \times A, p:Id_A(z), \Delta(z,p) \vdash C(z,p):Type \quad \Gamma \vdash t:\prod_{x:A} C(\Delta_A(x),r(x))}
{\Gamma, z:A \times A, p:Id_A(z) \vdash J(t,z,p) : C(z,p)}$$

$$\frac{\Gamma, z:A \times A, p:Id_A(z), \Delta(z,p) \vdash C(z,p):Type \quad \Gamma \vdash t:\prod_{x:A} C(\Delta_A(x),r(x))}
{\Gamma, x:A, \Delta(\Delta_A(x),r(x)) \vdash J(t,\Delta_A(x),r(x)) = t(x)}$$

The original inference rules using the family of terms $t(x)$ dependent upon $x:A$ is then given by $J(\lambda x:A.t(x),z,p):C(z,p)$ and $J(\lambda x:A.t(x),\Delta_A(x),r(x)) \equiv t(x):C(\Delta_A(x),r(x))$. . 

Similarly, the canonically defined term in the propositional computation rule is given by the identification $\beta(t,x):Id_{C(\Delta_A(x),r(x))}(J(t,\Delta_A(x),r(x)),t(x))$ and is dependent upon dependent function $t:\prod_{x:A} C(\Delta_A(x),r(x))$ rather than annotated with the family $t(x)$.

$$\frac{\Gamma, z:A \times A, p:Id_A(z), \Delta(z,p) \vdash C(z,p):Type \quad \Gamma \vdash t:\prod_{x:A} C(\Delta_A(x),r(x))}
{\Gamma, x:A, \Delta(\lambda b:\mathbb{2}.x,r(x)) \vdash \beta(t,x):Id_{C(\lambda b:\mathbb{2}.x,r(x))}(J(t,\lambda b:\mathbb{2}.x,r(x)),t(x))}$$

The original inference rules using the family of terms $t(x)$ dependent upon $x:A$ is then given by $\beta(\lambda x:A.t(x),x):\mathrm{Id}_{C(\Delta_A(x),r(x))}(J(\lambda x:A.t(x),\Delta_A(x),r(x)),t(x))$. 

### Identity types between types
{#IdentityTypesBetweenTypes} 
{#IdentityTypeBetweenTypes}

Suppose that we have a [[dependent type theory with type variables]], presented using a single type judgment. Type variables allow for the definition of [[identity types]] between types: 

* Formation rule for identity types between types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type}, B \; \mathrm{type} \vdash A = B \; \mathrm{type}}$$

* Introduction rule for identity types between types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type} \vdash \mathrm{refl}(A):A = A}$$

* Elimination rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash \mathrm{ind}_=^{C, t}(A, B, p):C(A, B, p)}$$

* Judgmental computation rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A ; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash \mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) \equiv t(A):C(A, A, \mathrm{refl}(A))}$$

* Typal computation rule for identity types between types

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B, \Delta(A, B, p) \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma, A \; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash t(A):C(A, A, \mathrm{refl}(A))}{\Gamma, A ; \mathrm{type}, \Delta(A, A, \mathrm{refl}(A)) \vdash \beta_{=}^{C, t}(A):\mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) =_{C(A, A, \mathrm{refl}(A))} t(A)}$$

If the dependent type theory has [[impredicative polymorphism]], then the $\Delta$ contexts can be removed from the elimination and computation rules of the identity types between types, simplifying the rules down to the following: 

* Elimination rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma \vdash t:\Pi A.C(A, A, \mathrm{refl}(A))}{\Gamma \vdash \mathrm{ind}_=^{C}(t):\Pi A.\Pi B.\Pi (p:A = B).C(A, B, p)}$$

* Judgmental computation rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma \vdash t:\Pi A.C(A, A, \mathrm{refl}(A))}{\Gamma, A \; \mathrm{type} \vdash \mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) \equiv t(A):C(A, A, \mathrm{refl}(A))}$$

* Typal computation rule for identity types between types:

$$\frac{\Gamma, A \; \mathrm{type}, B \; \mathrm{type}, p:A = B \vdash C(A, B, p) \; \mathrm{type} \quad \Gamma \vdash t:\Pi A.C(A, A, \mathrm{refl}(A))}{\Gamma \vdash \beta_{=}^{C}(t):\Pi A.\mathrm{ind}_=^{C}(t, A, A, \mathrm{refl}(A)) =_{C(A, A, \mathrm{refl}(A))} t(A)}$$

## Definition from an interval type

Suppose that one has an [[interval type]] $\mathbb{I}$, with elements $0:\mathbb{I}$ and $1:\mathbb{I}$. 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{I} \; \mathrm{type}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{I}} \quad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{I}}$$

Usually, the [[recursion principle]] of the [[interval type]] is interpreted as a way to construct, from elements $x:A$ and $y:A$ and identification $p:x =_A y$, paths $p:\mathbb{I} \to A$, aka functions from the interval type to $A$. Interpreted another way, the recursion principle of the interval type are the negative elimination and computation rules for [[identity types]], allowing one to define identity types as [[negative types]]. Thus, these identity types can be called **negative identity types**, in contrast to the Martin-Löf identity types, which can be called **positive identity types**.

### Inference rules

* The formation rule of identity types state that given a type $A$ and elements $x:A$ and $y:A$, one can form the identity type $x =_A y$. Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \; \mathrm{type}}$$

* The introduction rule of identity types state that given a type $A$ and a path $p:\mathbb{I} \to A$, one can construct an [[identification]] $\mathrm{toId}_A(f):f(0) =_A f(1)$. Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:\mathbb{I} \to A}{\Gamma \vdash \mathrm{toId}_A(f):f(0) =_A f(1)}$$

Normally, this would be [[function application to identifications|function application]] to the canonical identification $\mathcal{p}:0 =_\mathbb{I} 1$, but here we haven't defined $\mathcal{p}$ yet since we haven't defined the identity type yet, and with this rule one can define said identification to be the identification of the identity function on the interval type
$$\mathcal{p} \equiv \mathrm{toId}_\mathbb{I}(\mathrm{id}_\mathbb{I}):0 =_\mathbb{I} 1$$
In addition, reflexivity of an element $x:A$ is given by sending the constant path of $x:A$ to its equality

$$\mathrm{refl}_A(x) \equiv \mathrm{toId}_{A}(\lambda i:\mathbb{I}.x):x =_A x$$

* The elimination rule of identity types state that given a type $A$, elements $x:A$ and $y:A$, and identification $p:x =_A y$, one can construct a path $\mathrm{topath}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$. Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A}$$

This is just another name for the recursor of the interval type $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$.

* The three computation rules of identity types state that given a type $A$, elements $x:A$ and $y:A$, and identification $p:x =_A y$, 
$$\mathrm{topath}_\mathbb{I}^A(x, y, p)(0) \equiv x \quad \mathrm{topath}_\mathbb{I}^A(x, y, p)(1) \equiv y \quad \mathrm{toId}_{A}(\mathrm{topath}_\mathbb{I}^A(x, y, p)) \equiv p$$
Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p)(0) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p)(1) \equiv y:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{toId}_{A}(\mathrm{topath}_\mathbb{I}^A(x, y, p)) \equiv p:x =_A y}$$

* The uniqueness rule of identity types state that given a type $A$ and a path $p:\mathbb{I} \to A$,
$$\mathrm{topath}_\mathbb{I}^A(p(0), p(1), \mathrm{toId}_A(p)) \equiv p$$

Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:\mathbb{I} \to A}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(f(0), f(1), \mathrm{toId}_A(f)) \equiv f:\mathbb{I} \to A}$$

### Path induction

The associated path induction rule then says that the function type $\mathbb{I} \to A$ is a [[positive copy]] of $A$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathbb{I} \to A \vdash C(z) \; \mathrm{type} \quad t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)}{\Gamma \vdash \mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{z:\mathbb{I} \to A} C(z)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathbb{I} \to A \vdash C(z) \; \mathrm{type} \quad t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)}{\Gamma, x:A \vdash \mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)}$$

\begin{theorem}
Suppose that path induction for function types out of the interval type is true. Then the J-rule is true: given a type $A$ and given a type family $C(x, y, p)$ indexed by $x:A$, $y:A$, and $p:x =_A y$, and a dependent function $t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))$, one can construct a dependent function

$$\mathrm{ind}_{=, A}(t):\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} C(x, y, p)$$

such that for all $x:A$, 

$$J(t, x, x, \mathrm{refl}_A(x)) \equiv t(x)$$
\end{theorem}

\begin{proof}
By path induction on the type family $C(f(0), f(1), \mathrm{toId}_A(f))$ indexed by $f:\mathbb{I} \to A$, we can construct a dependent function

$$\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{f:\mathbb{I} \to A} C(f(0), f(1), \mathrm{toId}_A(f))$$

such that for all $x:A$,

$$\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$$ 

since by definition of constant function and reflexivity, one has

$$(\lambda i:\mathbb{I}.x)(0) \equiv x \quad (\lambda i:\mathbb{I}.x)(1) \equiv x \quad \mathrm{ap}_{\lambda i:\mathbb{I}.x}(\mathcal{p}) \equiv \mathrm{refl}_A(x)$$

We define 

$$J(t, x, y, p) \equiv \mathrm{ind}_{\mathbb{I} \to A}(t, \mathrm{rec}_\mathbb{I}^A(x, y, p))$$

since by interval recursion one has a path $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$ such that

$$\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(0) \equiv x \quad \mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(1) \equiv y \quad \mathrm{ap}_{\mathrm{rec}_\mathbb{I}^{A}(x, y, p)}(0, 1, \mathcal{p}) \equiv p$$
\end{proof}

Alternatively, one can say that $\mathbb{I} \to A$ is a [[negative copy]] of $A$ with respect to constant functions, or equivalently that every type $A$ is definitionally $\mathrm{I}$-[[localization of a type|local]], or that 
$$\mathrm{const}_{A, \mathbb{I}} \equiv \lambda x:A.\lambda i:\mathbb{I}.x:A \to (\mathbb{I} \to A)$$
is a definitional [[isomorphism]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \mathrm{const}_{A, \mathrm{I}}^{-1}(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \mathrm{const}_{A, \mathrm{I}}^{-1}(\lambda i:\mathbb{I}.x) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \lambda i:\mathbb{I}.\mathrm{const}_{A, \mathrm{I}}^{-1}(p) \equiv p:\mathbb{I} \to A}$$

This is called *definitional [[interval type localization]]*. 

Then, one can prove path induction (positive copy induction rules):

\begin{theorem}
Suppose that every type $A$ is definitionally $\mathbb{I}$-local.

Then path induction holds: given any type $A$, and any type family $C(p)$ indexed by paths $p:\mathbb{I} \to A$ in $A$, and given any dependent function $t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)$ which says that for all elements $x:A$,  there is an element of the type defined by substituting the constant path of $x:A$ into $C$, $C(\lambda i:\mathbb{I}.x)$, one can construct a dependent function $\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{z:\mathbb{I} \to A} C(z)$ such that for all $x:A$, $\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$. 
\end{theorem}

\begin{proof}
$\mathrm{ind}_{\mathbb{I} \to A}(t)$ is defined to be

$$\mathrm{ind}_{\mathbb{I} \to A}(t) \equiv \lambda p:\mathbb{I} \to A.t(\mathrm{const}_{A, \mathrm{I}}^{-1}(p))$$

and by the computation rules of path types as negative copies, one has that for all $x:A$, 

$$\mathrm{const}_{A, \mathrm{I}}^{-1}(\lambda i:\mathbb{I}.x) \equiv x$$

and so by definition of $\mathrm{ind}_{\mathbb{I} \to A}(t)$ and the judgmental congruence rules for substitution, one has

$$\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(\mathrm{const}_{A, \mathrm{I}}^{-1}(\lambda i:\mathbb{I}.x)) \equiv t(x)$$
\end{proof}

Thus, everything about identity types in Martin-Löf type theory could be proven in this theory. 

On the other hand, **propositional interval type localization**, which says that 
$$\mathrm{const}_{A, \mathbb{I}} \equiv \lambda x:A.\lambda i:\mathbb{I}.x:A \to (\mathbb{I} \to A)$$
is a weak equivalence of types, only implies the propositional J-rule. 

One has the following analogies between localization at a specific type and the type theoretic letter rule that it proves:

| localization rule | type theoretic letter rule |
|-------------------|----------------------------|
| [[I-localization|$\mathbb{I}$-localization]] | [[J-rule]] |
| [[S1-localization|$S^1$-localization]] | [[K-rule]] |


### Kan operations

Defining identity types in terms of an [[interval type]] gives the type theory a [[cubical type theory|cubical]] flavor, although here the interval $\mathbb{I}$ is an actual type, rather than a pretype in [[cubical type theory]]. In particular, one can use path induction to construct the Kan operations. The following proofs are adapted from [Bentzen2019](#Bentzen2019). 

\begin{theorem}
Given paths $f:\mathbb{I} \to A$ and $g:\mathbb{I} \to A$, one can construct a function 
$$\mathrm{fill}_A(f, g):(f(0) =_A g(0)) \to (f(1) =_A g(1))$$ 
\end{theorem}

This is defined by double path induction by sending the constant path of $x$ in each parameter to its filler of identifications, which is just the identity function on $x =_A x$

$$x:A \vdash \mathrm{fill}_A(\lambda i:\mathbb{I}.x, \lambda i:\mathbb{I}.x) \equiv \mathrm{id}_{x =_A x}:(x =_A x) \to (x =_A x)$$

\begin{theorem}
Given elements $x:A$, $y:A$ and identification $p:x =_A y$, one can construct the inverse identification $p^{-1}:(y =_A x)$. 
\end{theorem}

By interval recursion, there are paths $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$. By evaluating the fillers of the recursively defined path and the identity path on $x$ at reflexivity of $x$, one gets the needed identity:

$$p^{-1} \equiv \mathrm{fill}_A(\mathrm{rec}_\mathbb{I}^A(x, y, p), \lambda i:\mathbb{I}.x, \mathrm{refl}_A(y)):(y =_A x)$$

$$
\begin{array}{ccccc}
     & x & \overset{\mathrm{refl}_A(x)}= & x &  \\
    p & \Vert &  & \Vert & \mathrm{refl}_A(x) \\
     & y & \underset{p^{-1}}= & x & \\
\end{array}
$$

\begin{theorem}
Given elements $x:A$, $y:A$, $z:A$ and identifications $p:x =_A y$ and $q:y =_A z$, one can construct an identification $p \bullet q:(x =_A z)$ called the concatenation of $p$ and $q$.
\end{theorem}

By interval recursion, there is a path $\mathrm{rec}_\mathbb{I}^A(y, z, q):\mathbb{I} \to A$. By evaluating the fillers of the constant path of $x$ and the path of $q$ at $p$, one gets the needed identification:

$$p \bullet q \equiv \mathrm{fill}_A(\lambda i:\mathbb{I}.x, \mathrm{rec}_\mathbb{I}^A(y, z, q), p):(x =_A z)$$

$$
\begin{array}{ccccc}
     & x & \overset{p}= & y &  \\
    \mathrm{refl}_A(x) & \Vert &  & \Vert & q \\
     & x & \underset{p \bullet q}= & z & \\
\end{array}
$$

### Other properties

There are other things which can be defined similarly to cubical type theory. For example, [[function extensionality]] is provable: 

\begin{theorem}
Given dependent functions $f:\prod_{x:A} B(x)$ and $g:\prod_{x:A} B(x)$ and a [[homotopy]] $H:\prod_{x:A} f(x) =_{B(x)} g(x)$, we have an identification $\mathrm{funext}(f, g, H):f =_{\prod_{x:A} B(x)} g$
\end{theorem}

\begin{proof}
This is defined by 

$$\mathrm{funext}(f, g, H) \equiv \mathrm{toId}_{\prod_{x:A} B(x)}(\lambda i:\mathbb{I}.\lambda x:A.\mathrm{topath}_\mathbb{I}^{B(x)}(f(x), g(x), H(x))(i))$$
\end{proof}

Similarly, [[function application to identifications]] can be defined without the use of path induction:

\begin{theorem}
Given types $A$ and $B$, a a function $f:A \to B$, elements $x:A$ and $y:A$ and an identification $p:x =_A y$, one can construct the identification $\mathrm{ap}_f(x, y, p):f(x) =_B f(y)$. 
\end{theorem}

This is defined through the inference rules for identity types and function composition: 

$$\mathrm{ap}_f(x, y, p) \equiv \mathrm{toId}_B(f \circ \mathrm{rec}_\mathbb{I}^A(x, y, p)):f(x) =_B f(y)$$

This is sufficient to prove the recursion and uniqueness rules for the [[interval type]]:

\begin{theorem}
The recursion principle of the interval type:

Given a type $A$, elements $x:A$ and $y:A$ and equality $p:x =_{A} y$, one can construct a function $\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p):\mathbb{I} \to A$ such that 

$$\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(0) \equiv x \quad \mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(1) \equiv y \quad \mathrm{ap}_{\mathrm{rec}_\mathbb{I}^{A}(x, y, p)}^{=}(0, 1, \mathrm{toId}_\mathbb{I}(\mathrm{id}_\mathbb{I})) \equiv p$$
\end{theorem}

\begin{proof}
We define 

$$\mathrm{rec}_{\mathbb{I}}^{A(-)}(x, y, p) \equiv \mathrm{topath}_{\mathbb{I}}^{A(-)}(x, y, p)$$

That $\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(0) \equiv x$ is given by the first computation rule of identity types and that $\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(1) \equiv y$ is given by the second computation rules of identity types. Finally, by definition of function application to identification and the uniqueness rule of identity types, one has the following reduction:

$$\mathrm{ap}_{\mathrm{rec}_\mathbb{I}^{A}(x, y, p)}(0, 1, \mathrm{toId}_A(\mathrm{id}_\mathbb{I})) \equiv \mathrm{toId}_A(\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p) \circ \mathrm{rec}_\mathbb{I}^\mathbb{I}(0, 1, \mathrm{toId}_\mathbb{I}(\mathrm{id}_\mathbb{I}))) \equiv \mathrm{toId}_A(\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p) \circ \mathrm{id}_\mathbb{I})$$

and by function composition and the third computation rule of identity types, one has the following reduction

$$\mathrm{toId}_A(\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p) \circ \mathrm{id}_\mathbb{I}) \equiv \mathrm{toId}_A(\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)) \equiv p$$
\end{proof}

\begin{theorem}
The uniqueness principle of the interval type:

Given a type $A$, elements $x:A$ and $y:A$ and equality $p:x =_{A} y$, and given a function $f:\mathbb{I} \to A$ such that 

$$f(0) \equiv x \quad f(1) \equiv y \quad \mathrm{ap}_{f}(0, 1, \mathrm{toId}_\mathbb{I}(\mathrm{id}_\mathbb{I})) \equiv p$$

one has that $f \equiv \mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)$. 
\end{theorem}

\begin{proof}
By definition of the recursor of the interval type, 

$$\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p) \equiv \mathrm{topath}_{\mathbb{I}}^{A(-)}(x, y, p)$$

and by the judgmental congruence rules for substitution, one has that 

$$\mathrm{topath}_{\mathbb{I}}^{A(-)}(x, y, p) \equiv \mathrm{topath}_\mathbb{I}^A(f(0), f(1), \mathrm{toId}_A(f))$$

and by the uniqueness rule for identity types, one has that 

$$\mathrm{topath}_\mathbb{I}^A(f(0), f(1), \mathrm{toId}_A(f)) \equiv f$$
\end{proof}

The recursion and uniqueness principles of the interval type are in turn sufficient to prove the induction principle of the interval type.

## Definition in observational type theory

Identity types in [[observational type theory]] and [[higher observational type theory]] are defined in a different manner than they are in [[Martin-Löf type theory]]. 

In higher observational type theory, identity types have the same formation rule as Martin-Löf identity types do:

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A, y:A \vdash Id_A(x,y):Type}$$

However, it does not have global elimination or computation rules. Instead, it has a local computation rule for each particular type. For example, the identity type of the product type $A \times B$ has the following computation rule:

$$Id_{A \times B} (s, t) \equiv Id_A(\pi_1 s, \pi_1 t) \times Id_B (\pi_2 s, \pi_2 t)$$

### For types in universes 

We are working in a [[dependent type theory]] with Tarski-style [[universes]].

The [[identity types]] in a universe in higher observational type theory have the following formation rule:

$$\frac{A:\mathcal{U} \quad a:\mathcal{T}_\mathcal{U}(A) \quad b:\mathcal{T}_\mathcal{U}(A)}{\mathrm{id}_A(a, b):\mathcal{U}}$$

We define a general congruence term called ap

$$\frac{x:A \vdash f:B \quad p:\mathrm{id}_A(a, a^{'})}{\mathrm{ap}_{x.f}(p):\mathrm{id}_B(f[a/x], f[a^{'}/x])}$$

and the reflexivity terms:

$$\frac{a:A}{\mathrm{refl}_{a}:\mathrm{id}_A(a, a)}$$

and computation rules for identity functions

$$\mathrm{ap}_{x.x}(p) \equiv p$$

and for constant functions $y$

$$\mathrm{ap}_{x.y}(p) \equiv \mathrm{refl}_{y}$$

Thus, ap is a higher dimensional explicit substitution. There are judgmental equalities

$$\mathrm{ap}_{x.f}(\mathrm{refl}_{a}) \equiv \mathrm{refl}_{f[a/x]}$$

$$\mathrm{ap}_{y.g}(\mathrm{ap}_{x.f}(p)) \equiv \mathrm{ap}_{x.g[f/y]}(p)$$

$$\mathrm{ap}_{x.t}(p) \equiv \mathrm{refl}_{t}$$

for constant term $t$. 

### For universes

Let $A \cong_\mathcal{U} B$ be the type of [[bijective correspondences]] between two terms of a universe $A:\mathcal{U}$ and $B:\mathcal{U}$, and let $\mathrm{id}_\mathcal{U}(A, B)$ be the identity type between two terms of a universe $A:\mathcal{U}$ and $B:\mathcal{U}$. Then there are rules

$$\frac{R:A \cong_\mathcal{U} B}{\Delta(R):\mathrm{id}_\mathcal{U}(A, B)} \qquad \frac{P:\mathrm{id}_\mathcal{U}(A, B)}{\nabla(P):A \cong_\mathcal{U} B} \qquad \frac{R:A \cong_\mathcal{U} B}{\nabla(\Delta(R)) \equiv R}$$

### Identity types in universes and singleton contractibility ###

Given a term of a universe $A:\mathcal{U}$

$$\mathrm{id}_{\mathcal{T}_\mathcal{U}(A)} \equiv \pi_1(\nabla(\mathrm{refl}_A))$$

with terms representing [[singleton contractibility]]. 

$$\pi_1(\pi_2(\nabla(\mathrm{refl}_A)):\prod_{a:\mathcal{T}_\mathcal{U}(A)} \mathrm{isContr}\left(\sum_{b:\mathcal{T}_\mathcal{U}(A)} \mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(a, b)\right)$$

$$\pi_2(\pi_2(\nabla(\mathrm{refl}_A))):\prod_{b:\mathcal{T}_\mathcal{U}(A)} \mathrm{isContr}\left(\sum_{a:\mathcal{T}_\mathcal{U}(A)} \mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(a, b)\right)$$

## Definition in cubical type theory

The primary identity types are the nondependent [[cubical path types]] in [[cubical type theory]]. Like the identity types in higher observational type theory, they do not satisfy the judgmental version of identification elimination; only the typal version of identification elimination. See [[cubical path type]] for more information on the construction of the cubical path types. 

Some cubical type theories include a second identity type which satisfies the judgmental version of identification elimination. This is called [[Swan's identity type]], and is defined by the following rules:

Identity types in [[cubical type theory]] are called **path types** and are defined using a primitive interval.  

## Categorical semantics

We discuss the [[categorical semantics]] for identity types in the extensional case, and identity types in the [[categorical semantics of homotopy type theory]] in the intensional case.


In categorical models of [[extensional type theory]], generally every [[morphism]] of the category is allowed to represent a [[dependent type]], and the extensional identity types are represented by [[diagonal]] maps $A\to A\times A$.

By contrast, in models of [[intensional type theory]], there is only a particular class of [[display maps]] or [[fibrations]] which are allowed to represent dependent types, and intensional identity types are represented by [[path objects]] $P A \to A \times A$.

Both of these cases apply in particular to models in the [[category of contexts]] of the type theory itself, i.e. the [[term model]].

### Prerequisites

By the standard construction of [[mapping path spaces]] out of 
[[path space objects]], the existence of identity types allows one to construct a [[weak factorization system]].

Conversely, since any weak factorization system gives rise to [[path objects]] by factorization of [[diagonal maps]], one may hope to construct a [[model]] of type theory with identity types in a category equipped with a WFS $(L,R)$.  There are four obstacles in the way of such a construction.

1. In order to handle the additional [[context]] $\Delta$ in the explicit definition above, it turns out to be necessary to assume that $L$-maps are preserved by [[pullback]] along $R$-maps between $R$-objects.  (Such a condition is also necessary in order to interpret type-theoretic [[dependent products]] in a [[locally cartesian closed category]].)

1. This enables us to define identity types with their elimination and computation rules "locally", i.e. for each type individually.  However, every construction in type theory is stable under [[substitution]].  This means that if $y\colon Y\vdash A(y)\colon Type$ is a dependent type and $f\colon X\to Y$ is a morphism, then the identity type $x\colon X \vdash Id_{A(f(x))}(-,-)\colon Type$ is the same whether we first construct $Id_{A(y)}$ and then substitute $f(x)$ for $y$, or first substitute $f(x)$ for $y$ to obtain $A(f(x))$ and then construct its identity type.  In order for this to hold up to isomorphism, we need to require that the WFS have *stable path objects* --- a choice of path object data in each slice category which is preserved by pullback.  In [Warren 2008](#Warren08) it is shown that any [[simplicial model category]] in which the [[cofibrations]] are the [[monomorphisms]] can be equipped with stable path objects, while [Garner & van den Berg 2011](#vdBergGarner11) it is shown that the presence of internal path-categories also suffices.

1. The eliminator term $J$ of identity types in type theory is also preserved by substitution.  This imposes an additional *[[coherence]]* requirement which is tricky to obtain categorically.  See [Warren 2008](#Warren08) and [Garner & van den Berg 2011](#vdBergGarner11) for methods that ensure this, such as by invoking an [[algebraic weak factorization system]].  It can also be handled *a la* [[Vladimir Voevodsky|Voevodsky]] by using a (possibly [[univalence axiom|univalent]]) [[universe]].

1. Finally, substitution in type theory is strictly functorial/[[associativity|associative]], whereas it is modeled categorically by pullback which is generally not strictly so.  This is a general issue with the categorical interpretation of [[dependent type theory]], not something specific to identity types.  It can be resolved by passing to a [[split fibration]] which is equivalent to the [[codomain fibration]], or by making use of a [[universe]].  See [[categorical model of dependent types]].

### Interpretation in a type-theoretic model category

Assume then that a category $\mathcal{C}$ with suitable WFSs has been chosen, for instance a [[type-theoretic model category]]. Then

* The interpretation of a type $ \vdash A : Type$ is as a [[fibrant object]] $[\vdash A : Type]$ which we will just write "$A$" for short. 

* **type formation** 
  
  The identity type $a, b : A \vdash Id_A(a,b) : Type$ is interpreted as [[generalized the|the]] [[path space object]] [[fibration]] 
  
  $$
    \array{
       A^I
       \\
       \downarrow
       \\
       A \times A
    }
  $$

* **term introduction**

  By definition of [[path space object]], there exists a lift $\sigma$ in 
  
  $$
    \array{
       && A^I
       \\
       & {}^{\mathllap{\sigma}}\nearrow& \downarrow
       \\
       A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  By the [[universal property]] of the [[pullback]] this is equivalently a [[section]] of the [[pullback]] of the path space object along the [[diagonal]] morphism $(id,id) : A \to A \times A$.

  $$
    \array{
       && (id,id)^* A^I &\to& A^I
       \\
       &{}^{\mathllap{\sigma}}\nearrow& \downarrow & & \downarrow
       \\
       A &=& A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  Since $(id, id)^* A^I$ is the interpretation of the [[substitution]]  
  $a : A \vdash Id_A (a,a) : Type$ in this sense $\sigma$ is now the interpretation of a term $a : A \vdash r_A : Id_A (a,a)$. 

* **term elimination**

  A type depending on an identity type

  $$
    a, b : A, p : Id_A(a,b) \vdash C(a,b,p)
  $$

  is interpreted as a [[fibration]]

  $$
    \array{
      C
      \\
      \downarrow
      \\
      A^I
    }
    \,.
  $$

  The [[substitution]] $C(a,a,r_a)$ is interpreted by the [[pullback]]

  $$
    \array{
      (id,id)^* C &\to& C
      \\
      \downarrow && \downarrow
      \\
      A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  Therefore a [[term]] $t : C(a,a,r_a)$ is interpreted as a [[section]] of this pullback

  $$
    \array{
      && (id,id)^* C &\to& C
      \\
      &{}^{\mathllap{t}}\nearrow& \downarrow && \downarrow
      \\
      A &=& A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  By the [[universal property]] of the pullback, this is equivalently a morphism $t$ in 

  $$
    \array{
      && C
      \\
      & {}^{\mathllap{t}}\nearrow & \downarrow
      \\
      A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  The elimination rule says that given such $t$, there exists a compatible section of $C \to A^I$. If we redraw the previous diagram as a square, then this section is a _[[lifting problem|lift]]_ in that diagram

  $$
    \array{   
      A &\to& C
      \\
      {}^{\mathllap{r}}\downarrow &\nearrow& \downarrow
      \\
      A^I &=& A^I
    }
    \,.
  $$

  In particular, if $C$ itself is the pullback of a fibration $D \to B$ along a morphism $A^I \to B$, then $r$ has the left lifting property also against that fibration

  $$
    \array{   
      A &\to& C &\to& D
      \\
      {}^{\mathllap{r}}\downarrow &\nearrow& \downarrow && \downarrow
      \\
      A^I &=& A^I &\to& B
    }
    \,.
  $$

  So the term elimination rule says that the interpretation $A \to A^I$ of $a : A \vdash r(a) : Id_A (a,a)$ has the [[left lifting property]] against all fibrations, hence that $A \to A^I$ is to be interpreted as an acyclic cofibration.

 

### Weak $\omega$-groupoids

Some of the first work noticing the homotopical / higher-categorical interpretation of identity types (see below) focused on the fact that the tower of iterated identity types of a type has the structure of an internal *[[algebraic definition of higher categories|algebraic]]* [[∞-groupoid]].

In retrospect, this is roughly an algebraic version of the standard fact that every object of a model category (or more generally a [[category of fibrant objects]] or a category with a weak factorization system) admits a [[simplicial resolution]] which is an [[internalization|internal]] [[Kan complex]], i.e. a nonalgebraic $\infty$-groupoid.  Note, however, that the first technical condition above (stability of $L$-maps under pullback along $R$-maps) seems to be necessary for the algebraic version of the result to go through.

## Related concepts

* [[identity of indiscernibles]]

* [[intensional type theory]], [[extensional type theory]]

* [[judgmental equality]], [[propositional equality]]

* [[objective type theory]]

* [[transport]]

* [[indexed heterogeneous identity type]]

* [[fibered heterogeneous identity type]]

* [[action on identifications]]

* [[dependent identity type]]

* [[axiom K]]

* [[uniqueness of identity proofs]]

* [[identity system]]

* [[cocylinder]]

* [[observational equality]]

* [[loop space type]]

* [[encode-decode method]]

* [[diagonal function]]

## References
 {#References}

The above Latin excerpts by [[Gottfried Leibniz]] are taken from

* {#Gerhard1890} K. Gerhard (ed.), Section XIX, [p. 228](https://archive.org/details/diephilosophisc00gerhgoog/page/228/mode/2up), [230](https://archive.org/details/diephilosophisc00gerhgoog/page/300/mode/2up) in: *Die philosophischen Schriften von Gottfried Wilhelm Leibniz*, Siebenter Band, Weidmannsche Buchhandlung (1890) &lbrack;[archive.org](https://archive.org/details/diephilosophisc00gerhgoog/page/n7/mode/2up)&rbrack;

whose English translation is given in:

* {#Lewis18} [[Clarence I. Lewis]], Appendix ([p. 373](/nlab/files/LewisAppendix-LeibnizIndiscernibles.pdf), [275](/nlab/files/LewisAppendix-CompositionOfIdentifications.jpg)) of: *A Survey of Symbolic Logic*, University of California (1918) 


### Explicit definition
 {#ReferencesExplicitDefinition}

The [[induction principle]] for identity types (also known as "path induction" or the "[[J-rule]]") is first stated in

* {#MartinLof75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80**, Elsevier (1975) 73-118 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926)&rbrack;

and in the modern form of [[inference rules]] in 

* {#NordströmPeterssonSmith90} Bengt Nordström, Kent Petersson, Jan M. Smith, §8.1 of: *Programming in Martin-Löf's Type Theory*, Oxford University Press (1990) &lbrack;[webpage](https://www.cse.chalmers.se/research/group/logic/book/), [pdf](https://www.cse.chalmers.se/research/group/logic/book/book.pdf), [[NordstromPeterssonSmith-TypeTheory.pdf:file]]&rbrack;

with early survey in §1.0.1 of: 

* {#Warren08} [[Michael Warren]], *Homotopy theoretic aspects of constructive type theory*, PhD thesis (2008) &lbrack;[pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf), [[Warren-HomotopyTypeTheory.pdf:file]]&rbrack;

For the two different ways of expressing the elimination and computation rules of identity types, see

* {#UFP13} [[Univalent Foundations Project]], §1.12 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], §5.1 *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#PaulinMohring93} [[Christine Paulin-Mohring]], *Inductive definitions in the system Coq -- Rules and Properties*, in: *Typed Lambda Calculi and Applications* TLCA 1993, Lecture Notes in Computer Science **664** Springer (1993) &lbrack;[doi:10.1007/BFb0037116](https://doi.org/10.1007/BFb0037116)&rbrack;

* {#KrausRaumer19} [[Nicolai Kraus]], [[Jakob von Raumer]], *Path Spaces of Higher Inductive Types in Homotopy Type Theory*. &lbrack;[arXiv:1901.06022](https://arxiv.org/abs/1901.06022)&rbrack;

See also (?):

* [[Per Martin-Löf]], p. 169 (17 of 23) in: *Constructive Mathematics and Computer Programming*, Studies in Logic and the Foundations of Mathematics Volume 104, 1982, Pages 153-175 (<a href="https://doi.org/10.1016/S0049-237X(09)70189-2">doi:10.1016/S0049-237X(09)70189-2</a>)

* [[Per Martin-Löf]], p. 31-34 in: _Intuitionistic type theory_, Lecture notes Padua 1984 (notes by [[Giovanni Sambin]]), Bibliopolis, Napoli (1984) ([pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]])


The observation that the Id-induction principle (the J-rule) is equivalent to [[transport]] ("[[salva veritate]]") together with [[contractible type|contractibility]] of the type of identifications ("composition with self-identifications") is stated in:

* {#Coquand11} [[Thierry Coquand]], slides 26-28 of: *Equality and dependent type theory* (2011) &lbrack;[pdf](https://www.cse.chalmers.se/~coquand/equality.pdf), [[Coquand-EqualityAndDependentTypeTheory.pdf:file]]&rbrack;

further highlighted in

* {#LadymanPresnell15} [[James Ladyman]], [[Stuart Presnell]], §6.3 of: *Identity in Homotopy Type Theory, Part I: The Justification of Path Induction*, Philosophia Mathematica **23** 3 (2015) 386–406 &lbrack;[doi:10.1093/philmat/nkv014](https://doi.org/10.1093/philmat/nkv014), [pdf](http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf)&rbrack;

and the proof of the equivalence is spelled out in:

* {#Götz18} Lennard Götz, §4.2 of: *Martin-Löf's J-rule*, LMU (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Goetz.pdf)&rbrack; 


  
Discussion of issues of [[extensional type theory|extensional]]/[[intensional type theory]]:

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])

* {#Streicher} [[Thomas Streicher]], _Investigations Into Intensional Type Theory_, Habilitationsschrift ([pdf](http://www.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf))

### As inductive types
 {#ReferencesByInductiveTypes}

* {#Licata11} [[Dan Licata]], _[Understanding Identity Elimination in Homotopy Type Theory](https://homotopytypetheory.org/2011/04/10/just-kidding-understanding-identity-elimination-in-homotopy-type-theory/)_, 2011

* {#Shulman12} [[Mike Shulman]], _Inductive types and identity types_, 2012 ([pdf](https://home.sandiego.edu/~shulman/hottseminar2012/03induction-handout1up.pdf))

* {#Overture.v} [https://github.com/HoTT/HoTT/blob/master/theories/Basics/Overture.v](https://github.com/HoTT/HoTT/blob/master/theories/Basics/Overture.v#L169-L170)

### In (higher) observational type theory

* [[Thorsten Altenkirch]] and [[Conor McBride]], _Towards observational type theory_ ([pdf](http://strictlypositive.org/ott.pdf))

* [[Conor McBride]], [Hier Soir, an OTT Hierarchy](http://mazzo.li/epilogue/index.html%3Fp=1098.html)

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 2* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 3* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-12.pdf), [video](https://www.youtube.com/watch?v=9pDddxB7LbE))

### Polymorphism and identity types between types 

Discussion about [[polymorphism]] and identity types between types in a [[dependent type theory with type variables]]:

* *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))

### Weak factorization systems

* [[Michael Warren]], _Homotopy theoretic aspects of constructive type theory_, PhD thesis (2008) ([pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf))

* [[Steve Awodey]] and [[Michael Warren]], _Homotopy theoretic models of identity types_, [arXiv](http://arxiv.org/abs/0709.0248).

* [[Nicola Gambino]], [[Richard Garner]], _The identity type weak factorisation system_, [arXiv](http://arxiv.org/abs/0803.4349)

* [[Richard Garner]], [[Benno van den Berg]], _Topological and simplicial models of identity types_, [arXiv](http://arxiv.org/abs/1007.4638).

### Types as $\infty$-groupoids

The suggestion that identity types witness [[groupoid]] and [[infinity-groupoid]]-structure is due to

* {#HofmannStreicher98} [[Martin Hofmann]], [[Thomas Streicher]]  _The groupoid interpretation of type theory_, in: [[Giovanni Sambin]] et al. (eds.), _Twenty-five years of constructive type theory_, Proceedings of a congress, Venice, Italy, October 19&#8212;21, 1995. Oxford: Clarendon Press. Oxf. Logic Guides. 36, 83-111 (1998).  ([ISBN:9780198501275](https://global.oup.com/academic/product/twenty-five-years-of-constructive-type-theory-9780198501275), [ps](http://www.mathematik.tu-darmstadt.de/~streicher/venedig.ps.gz) [[HofmannStreicherGroupoidInterpretation.pdf:file]])

* {#AwodeyWarren07} [[Steve Awodey]], [[Michael Warren]], _Homotopy theoretic models of identity type_,  Mathematical Proceedings of the Cambridge Philosophical Society vol 146, no. 1 (2009) ([arXiv:0709.0248](http://arxiv.org/abs/0709.0248))

This is ultimately verified by the observation that the [[J-rule]] makes the identity types interpret as  [[very good path space objects]] in a  [[locally cartesian closed model  category]] (such as the [[classical model structure on simplicial sets]]):

* {#Shulman12} [[Mike Shulman]], [Part III,  around slide 34](http://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=34) of: _Minicourse on homotopy type theory_, Swansea, April (2012) ([web](http://home.sandiego.edu/~shulman/hottminicourse2012/))

reviewed in:

* {#Riehl22} [[Emily Riehl]], §1.1 in: *On the $\infty$-topos semantics of homotopy type theory*, lecture at *[Logic and higher structures](https://conferences.cirm-math.fr/2689.html)* CIRM (Feb. 2022) $[$[pdf](https://emilyriehl.github.io/files/semantics.pdf), [[Riehl-InfinityToposSemantics.pdf:file]]$]$

For more see the references at _[[homotopy type theory]]_.

See also

* [Using Yoneda rather than J to present the identity type](https://www.cs.bham.ac.uk/~mhe/yoneda/yoneda.html)
 
* {#vdBergGarner11}[[Benno van den Berg]], [[Richard Garner]], *Types are weak $\omega$-groupoids*, Proceedings of the London Mathematical Society **102** 2 (2011) 370-394 &lbrack;[arXiv:0812.0298](http://arxiv.org/abs/0812.0298), [doi:10.1112/plms/pdq026](https://doi.org/10.1112/plms/pdq026)&rbrack;
 
* [[Peter LeFanu Lumsdaine]], _Weak $\omega$-categories from intensional type theory_ , ([arXiv:0812.0409](http://arxiv.org/abs/0812.0409))

* {#Bentzen2019} [[Bruno Bentzen]], _Naive cubical type theory_, 2019 ([pdf](https://arxiv.org/pdf/1911.05844.pdf))

[[!redirects identification type]]
[[!redirects identification types]]
[[!redirects identity type]]
[[!redirects identity types]]
[[!redirects equality type]]
[[!redirects equality types]]

[[!redirects positive identification type]]
[[!redirects positive identification types]]
[[!redirects positive identity type]]
[[!redirects positive identity types]]
[[!redirects positive equality type]]
[[!redirects positive equality types]]

[[!redirects negative identification type]]
[[!redirects negative identification types]]
[[!redirects negative identity type]]
[[!redirects negative identity types]]
[[!redirects negative equality type]]
[[!redirects negative equality types]]

[[!redirects weak identification type]]
[[!redirects weak identification types]]
[[!redirects strict identification type]]
[[!redirects strict identification types]]

[[!redirects weak identity type]]
[[!redirects weak identity types]]
[[!redirects strict identity type]]
[[!redirects strict identity types]]

[[!redirects weak equality type]]
[[!redirects weak equality types]]
[[!redirects strict equality type]]
[[!redirects strict equality types]]

[[!redirects type of identifications]]
[[!redirects types of identifications]]
[[!redirects type of identities]]
[[!redirects types of identities]]
[[!redirects type of equalities]]
[[!redirects types of equalities]]

[[!redirects intensional identification type]]
[[!redirects intensional identification types]]
[[!redirects extensional identification type]]
[[!redirects extensional identification types]]

[[!redirects intensional identity type]]
[[!redirects intensional identity types]]
[[!redirects extensional identity type]]
[[!redirects extensional identity types]]
[[!redirects identical]]

[[!redirects J rule]]
[[!redirects judgmental J rule]]
[[!redirects propositional J rule]]
[[!redirects typal J rule]]

[[!redirects standard J rule]]
[[!redirects judgmental standard J rule]]
[[!redirects propositional standard J rule]]
[[!redirects typal standard J rule]]

[[!redirects Paulin-Mohring J rule]]
[[!redirects judgmental Paulin-Mohring J rule]]
[[!redirects propositional Paulin-Mohring J rule]]
[[!redirects typal Paulin-Mohring J rule]]

[[!redirects J-rule]]
[[!redirects judgmental J-rule]]
[[!redirects propositional J-rule]]
[[!redirects typal J-rule]]

[[!redirects standard J-rule]]
[[!redirects judgmental standard J-rule]]
[[!redirects propositional standard J-rule]]
[[!redirects typal standard J-rule]]

[[!redirects Paulin-Mohring J-rule]]
[[!redirects judgmental Paulin-Mohring J-rule]]
[[!redirects propositional Paulin-Mohring J-rule]]
[[!redirects typal Paulin-Mohring J-rule]]

[[!redirects identity induction]]
[[!redirects path induction]]
[[!redirects identification induction]]
[[!redirects equality induction]]

[[!redirects identity elimination]]
[[!redirects path elimination]]
[[!redirects identification elimination]]
[[!redirects equality elimination]]

[[!redirects identity computation]]
[[!redirects path computation]]
[[!redirects identification computation]]
[[!redirects equality computation]]

[[!redirects based identity induction]]
[[!redirects based path induction]]
[[!redirects based identification induction]]
[[!redirects based equality induction]]

[[!redirects based identity elimination]]
[[!redirects based path elimination]]
[[!redirects based identification elimination]]
[[!redirects based equality elimination]]

[[!redirects based identity computation]]
[[!redirects based path computation]]
[[!redirects based identification computation]]
[[!redirects based equality computation]]

[[!redirects Id-induction]]
[[!redirects id-induction]]

[[!redirects based Id-induction]]
[[!redirects based id-induction]]

[[!redirects dependent universal property of identity types]]
[[!redirects dependent universal property of identification types]]
[[!redirects dependent universal property of path types]]
[[!redirects dependent universal property of equality types]]

[[!redirects universal property of identity types]]
[[!redirects universal property of identification types]]
[[!redirects universal property of path types]]
[[!redirects universal property of equality types]]