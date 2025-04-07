
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model category theory
+-- {: .hide}
[[!include model category theory - contents]]
=--
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## The canonical model structure on $Cat$

The [[canonical model structure]] on [[Cat]] is a [[model structure]] which encapsulates part of [[category theory]] as a version of [[homotopy theory]].  It is a special case of the general notion of [[canonical model structure]] on categorical structures, and is also called the **trivial model structure** or the **categorical model structure**.  Its [[weak equivalences]] are the [[equivalences of categories]] and its [[homotopy category]] is [[Ho(Cat)]], the category obtained from the 1-category $Cat$ by identifying naturally isomorphic functors. See the
_[[joyalscatlab:Model structures on Cat|Catlab]]_ for the theory of this structure. 

Assuming the [[axiom of choice]], the canonical model is the _unique_ model structure on $Cat$ such that the weak equivalences are categorical equivalences (thus justifying the word 'canonical').  It is different from the [[Thomason model structure]], where weak equivalences are functors that give a weak equivalence of simplicial sets when we take the [[nerve]].

On this page we give a concise construction of the canonical model structure, as well as two variants that make sense in the absence of the full [[axiom of choice]].


### The classical version

For purposes of this page, [[Cat]] will denote the [[1-category]] of [[small categories]] and [[functors]], and our categories are all [[strict categories]] as in ordinary set-theoretic [[foundations]].  We write $C_0$ for the set of [[objects]] of a [[small category]] $C$.  

\begin{definition}
\label{ClassesOfMorphisms}
Declare a functor to be:

* a [[weak equivalence]] if it is an [[equivalence of categories]], 

  (equivalently: [[fully faithful functor|fully faithful]] and [[essentially surjective functor|essentially surjective]]),

* a [[cofibration]] if it is [[injective-on-objects functor|injective on objects]], i.e. an [[isocofibration]],

* a [[fibration]] if it is an [[isofibration]].

\end{definition}

\begin{proposition}
\label{ExistenceOfTheCanonicalModelStructure}
The classes in Def. \ref{ClassesOfMorphisms} constitute a [[model category]]-[[structure]] $Cat_{can}$ on [[Cat]].
\end{proposition}  
\begin{proof}
It is easy to verify that the weak equivalences satisfy the [[2-out-of-3 property]]; thus it remains to show that (acyclic cofibrations, fibrations) and (cofibrations, acyclic fibrations) are [[weak factorization systems]].

Suppose given a square
$$\array{A & \overset{f}{\to} & C\\
  ^i\downarrow && \downarrow^p\\
  B& \underset{g}{\to} & D}$$
in which $i$ is a cofibration and $p$ a fibration.

Suppose first that $p$ is acyclic.  It is easy to see that the acyclic fibrations are precisely the equivalences of categories that are surjective on objects.  Thus, since (mono, epi) is a [[weak factorization system on Set]], we can define $h_0\colon B_0\to C_0$ filling the square, and then full-faithfulness of $p$ gives a unique definition of $h$ on arrows.

Now suppose that $i$ is acyclic, so that $i_0 \colon A_0 \to B_0$ is injective.  Since $i$ is essentially surjective, we can choose, for each $b\in B_0 \setminus A_0$, an isomorphism $\phi_b\colon i(a_b) \cong b$.  We then have $g(\phi_b)\colon p(f(a_b)) = g(i(a_b)) \cong g(b)$, so since $p$ is an isofibration, we can also choose, for each $b\in B_0$, an isomorphism $\psi_b\colon f(a_b) \cong c_b$ such that $p(\psi_b) = g(\phi_b)$.  Define $h_0\colon B_0\to C_0$ to be $f_0$ on the image of $i_0$ and to take $b\in B_0 \setminus A_0$ to $c_b$.  We can define $h$ on arrows by composing with the isomorphisms $\psi$ to make it a lifting.

It remains to prove the factorization axioms.  Suppose given a functor $f\colon A\to B$.  First, define $C_0 = A_0 + B_0$, and make $C$ into a category in the unique way such that the map $C\to B$ induced by $f$ and $1_B$ is fully faithful.  Since it is surjective on objects, it is an acyclic fibration, and clearly the induced map $A\to C$ is injective on objects, i.e. a cofibration.

Next, define $D$ to be the category of triples $(a,b,\phi)$ where $\phi\colon f(a)\cong b$ is an isomorphism in $B$.  In other words, it is the [[comma object|strict iso-comma category]] $(f/_\cong 1_b)$.  The projection $D\to B$ is easily shown to be an isofibration, while the functor $A\to D$ defined by $a \mapsto (a, f(a), 1_{f(a)})$ is an injective equivalence.

This completes the proof.  
\end{proof}

\begin{remark}
The two factorizations constructed above are in fact [[functorial factorizations]]. 
 
While this model structure is [[cofibrantly generated model category|cofibrantly generated]] (Prop. \ref{CofibrantGeneration}), the above factorizations are not those constructed from the [[small object argument]] (though they are closely related to the [[algebraic weak factorization systems]] produced by the [[algebraic small object argument]].
\end{remark}




### Without choice

In the absence of the [[axiom of choice]], one must distinguish between *strong equivalences of categories*, which come with an inverse up to isomorphism, and *weak equivalences of categories*, which are merely fully faithful and essentially surjective on objects.  Since weak equivalences of categories still "preserve all categorical information," we might hope to find a model structure on $Cat$ whose weak equivalences are the *weak* equivalences of categories.  The notion of [[anafunctor]] also suggests such an approach, since an anafunctor (the "right" replacement for a functor in the absence of choice) is a particular sort of generalized morphism: a [[span]] $A\leftarrow F \to B$ of functors in which $F\to A$ is a surjective equivalence.

If there is to be such a model structure, however, then since generalized morphisms between fibrant-and-cofibrant objects are all represented by ordinary ones, there must exist "cofibrant categories" and "fibrant categories" such that every anafunctor between fibrant-and-cofibrant categories is equivalent to an honest functor, and every category can be replaced by a fibrant and cofibrant one.  It seems unlikely that this would be true without *any* choice-like axioms, but notably weaker axioms than full AC do suffice.


#### The projective model structure

For the existence of the model structure in this case, we assume [[COSHEP]], aka the "presentation axiom," namely that the category [[Set]] has enough [[projective objects]].  Define a functor $f\colon A\to B$ to be:

* a [[weak equivalence]] if it is a weak equivalence of categories, i.e. [[fully faithful functor|fully faithful]] and [[essentially surjective functor|essentially surjective on objects]].

* a [[cofibration]] if it is injective on objects, and $B_0\setminus f(A_0)$ is a projective object in $Set$.

* a [[fibration]] if it is an [[isofibration]].

As before, the acyclic fibrations are precisely the weak equivalences that are literally surjective on objects.  Now recall that assuming COSHEP, (monics with projective complement, epics) is a [[weak factorization system on Set]].  This supplies the lifting of cofibrations against acyclic fibrations.  Likewise, the factorization of $f\colon A\to B$ into a cofibration followed by an acyclic fibration is given by first factoring $f_0$ as $A_0 \to A_0 + B_0' \to B_0$, where $B_0'\to B_0$ is a projective cover.

The other factorization works exactly as before, while for lifting acyclic cofibrations against fibrations, we notice that in the original proof, we only needed to apply choice for sets indexed by $B_0\setminus i(A_0)$, which we have assumed to be projective when $i\colon A\to B$ is a cofibration.

Weak equivalences of categories are easily seen to satisfy the 2-out-of-3 property, so we have a model category.  Note that all categories are fibrant in this model structure, while the cofibrant categories are those whose set of objects is projective.

The existence of this model structure implies, in particular, that under COSHEP the category $Ana(C,D)$ is [[essentially small category|essentially small]], being in fact equivalent to the category $Fun(C',D)$ of ordinary functors where $C'$ is a cofibrant replacement for $C$.


#### The injective model structure

Is there a dual model structure in which all categories are cofibrant?  This seemingly has to do with [[stack]] completion: the fibrant objects would be *stacks* for the [[regular coverage]] of $Set$.  (Without AC, not all small categories are stacks.)  Is Makkai's [[axiom of small cardinality selection]] (which he uses, instead of COSHEP, to prove that $Ana(C,D)$ is essentially small) sufficient for the existence of an "injective" model structure on Cat?

## Properties

### Basic properties
 {#BasicProperties}

\begin{remark}\label{CategoryOfBifibrantObjects}
**(category of bifibrant objects)**
\linebreak
  It is obvious that all objects in the canonical model structure (Prop. \ref{ExistenceOfTheCanonicalModelStructure}) are [[bifibrant object|bifibrant]], i.e.:

* both [[cofibrant object|cofibrant]] 

  since a functor $\varnothing \to \mathcal{C}$ from the [[empty category]] is evidently an [[injective function]] $\varnothing \to Obj(\mathcal{C})$ on objects,

* and [[fibrant objects|fibrant]], 

  since a functor $\mathcal{C} \to \ast$ to the [[terminal category]] is evidently an [[isofibration]] since the only morphism in the terminal category to lift is an [[identity morphism]].

Hence, in particular, $Cat_{can}$ is a [[category of fibrant objects]] and a [[cofibration category]].
\end{remark}

\begin{remark}\label{TheAcyclicFibrations}
**(acyclic (co)fibrations)**
\linebreak
In the canonical model structure (of Prop. \ref{ExistenceOfTheCanonicalModelStructure}):

* the [[acyclic cofibrations]] are precisely the [[injective-on-objects functor|injective-on-objects]] [[equivalences of categories]]

* the [[acyclic fibrations]] are precisely the [[surjective-on-objects functor|surjective on objects]] [[equivalences of categories]].

  Namely, being [[equivalences of categories]] makes them be [[essentially surjective functor|essentially surjective]] and [[fully faithful functor|fully faithful]] ([this Prop.](equivalence+of+categories#ViaSplitEssentiallySurjectiveAndFullyFaithful)), but being also [[isofibrations]] then clearly requires them to actually be [[surjective on objects functor|surjective on objects]], which by [[fully faithful functor|fully faithfulness]] is then already sufficient for isofibrancy.  

\end{remark}

\begin{proposition}\label{Properness}
**(properness)**
\linebreak
 The canonical model structure (Prop. \ref{ExistenceOfTheCanonicalModelStructure}) is a [[proper model category]].
\end{proposition}
\begin{proof}
  In view of Rem. \ref{CategoryOfBifibrantObjects} this follows by [this Prop.](proper+model+category#AllObjectsFibrantImpliesRightProper).
\end{proof}

\begin{proposition}\label{CofibrantGeneration}
**(cofibrant generation)**
\linebreak
  The canonical model structure $Cat_{can}$ (Prop. \ref{ExistenceOfTheCanonicalModelStructure}) is [[cofibrantly generated model category|cofibrantly generated]].
The sets $I$ of generating cofibrations and $J$ of generating acyclic cofibrations may be taken to consist of the following evident functors:
$$  
  I
  \;\coloneqq\;
  \left\{
    \begin{array}{ccc}
      \varnothing &\longrightarrow& \{ 0 \}
      \,,
      \\
      \{0\} \sqcup \{1\} &\longrightarrow& \{ 0 \to 1 \}
      \,,
      \\
      \big\{
        0 \rightrightarrows 1
      \big\}
      &\longrightarrow& \{ 0 \to 1\}
    \end{array}
  \right\}
  \,,
$$
$$
 J
 \;\coloneqq\;
 \left\{
   \array{
     \{ 0 \} 
      &\longrightarrow& 
   \{ 0 \xleftrightarrow{\sim} 1\}
   }
 \right\} 
  \,.
$$
\end{proposition}
([Rezk 1996, Prop. 4.1](#Rezk96))
\begin{proof}
  The functors in $I$ are evidently cofibrations. Hence by [this Prop](cofibrantly+generated+model+category#RetractsOfCellComplexesExchaustLLPOfRLP) we need to show that:

1. [[right lifting property|$RLP(I)$]] is the class of [[acyclic fibrations]].

   One sees immediately that:

   1. right lifting against $\varnothing \to \{0\}$ characterizes [[surjective on objects functors]],

   1. right lifting against $\{0\} \sqcup \{1\} \longrightarrow \{ 0 \to 1 \}$ characterizes [[full functors]],

   1. right lifting against $\big\{0 \rightrightarrows 1 \big\}\longrightarrow \{ 0 \to 1\}$ characterizes [[faithful functors]].

   Together this characterizes the acyclic fibrations, by Rem. \ref{TheAcyclicFibrations}.

1. [[right lifting property|$RLP(J)$]] is the class of [[fibrations]].

   But right lifting against $\{0\} \longrightarrow \{0 \xleftrightarrow{\sim} 1\}$ is immediately the condition of path lifting which defines [[isofibrations]].

\end{proof}

\begin{proposition}\label{CartesianMonoidalModelStructure}
**(cartesian monoidal model structure)**
\linebreak
  The canonical model structure $Cat_{can}$ (from Prop. \ref{ExistenceOfTheCanonicalModelStructure}) is a [[cartesian monoidal model category]].
\end{proposition}
([Rezk 1996, Thm. 5.1](#Rezk96), [Joyal 2010, Thm. 1.3](#Joyal10))
\begin{proof}
Since forming [[product categories]] with a fixed category $\mathcal{C}$ evidently preserves [[equivalence of categories|equivalences of categories]] and hence the canonical weak equivalences, the [unit axiom](monoidal+model+category#UnitAxiom) follows immediately. It remains to check the [pushout-product axiom](monoidal+model+category#PushoutProductAxiom).


So consider a diagram in $Cat$ of this form:
\begin{tikzcd}
  & 
  \mathcal{C} \times \mathcal{D}
  \ar[
    dl,
    "{ F \times \mathrm{Id} }"{swap}
  ]
  \ar[
    dr,
    "{ \mathrm{Id} \times G }"
  ]
  \ar[
    dd,
    phantom,
    "{ \scalebox{.7}{ (po) } }"
  ]
  \\
  \mathcal{C}' \times \mathcal{D}
  \ar[
    ddr,
    "{ \mathrm{Id} \times G }"{swap}
  ]
  \ar[
    dr,
    "{ q_l }"{swap}
  ]
  &&
  \mathcal{C} \times \mathcal{D}'
  \ar[
    ddl,
    "{ F \times \mathrm{Id} }"
  ]
  \ar[
    dl,
    "{ q_r }"
  ]
  \\
  &
  \mathcal{C}' \!\times\! \mathcal{D}
  \underset{ 
    \mathclap{
      \mathcal{C} \times \mathcal{D}
    }
  }{\coprod}
  \mathcal{C} \!\times\! \mathcal{D}'
  \ar[
    d, 
    dashed, 
    "{ F \widehat \times G }"{description}
  ]
  \\
  &
  \mathcal{C}' \times \mathcal{D}'
\end{tikzcd}

First we need to show that the [[pushout-product]] $F \widehat{\times} G$ is a cofibration if both $F$ and $G$ are. By the definition of cofibrations, this means to show that on objects $(F \widehat{\times} G)_0$ is an injective map if both $F_0$ and $G_0$ are injective maps.

Now, observe (see [here](Cat#OrdinaryLimitsAndColimits)) that the [[underlying]]-object functor
$$
  (-)_0
    \,\colon\,
  Cat \to Set
$$
[[preserved limit|preserves]] both [[limits]] and [[colimits]] and hence in particular preserves [[pushout products]]. Therefore the first statement we are after is that pushout-products of injections of sets are themselves injections, and that is the case, by [this example](pushout-product#InjectionsOfSets).

Second, if $F$ is in addition a weak equivalence, we need to show that then also $F \widehat{\times} G$ is a weak equivalence. 

But with $F$ certainly also $F \times \mathrm{Id}$ is an injective-on-objects equivalence of categories, hence an [[acyclic cofibration]] in the canonical model structure. By the model category properties, it follows that also the [[pushout]] $q_r$ (in the above diagram) is an acyclic cofibration, hence in particular a weak equivalence; and by [[2-out-of-3]] applied to the bottom right triangle in the above diagram it follows that with $F \times Id$ and $q_r$ also $F \widehat{\times} G$ is a weak equivalence.
\end{proof}



### Uniqueness of the model structure 

Remarkably:[^fine]

\begin{proposition}\label{Uniqueness}
The model structure $Cat_{can}$ (from Prop. \ref{ExistenceOfTheCanonicalModelStructure}) is the unique model structure on $Cat$ whose [[weak equivalences]] are the usual [[equivalences of categories]]. 
\end{proposition}

This result justifies the term "canonical". 

The following **proof** is adapted (with minor changes) from [Schommer-Pries 2012](#Schommer-Pries12). See also this MathOverflow [thread](http://mathoverflow.net/questions/18744/is-model-structure-on-catset-unique), particularly the [answer](http://mathoverflow.net/a/46471/2926) given by [[Steve Lack]] (with a pertinent comment by [[Denis-Charles Cisinski]]). 

[^fine]: Along similar lines, one can [prove](https://www.matem.unam.mx/~omar/notes/modelcatsets.html) (assuming [[axiom of choice|AC]]) that there are nine -- count 'em, nine -- Quillen model structures on [[Set|$Set$]]. 

Let $\mathbf{M}$ denote any model structure on $Cat$ whose weak equivalences are categorical equivalences. We will prove that $\mathbf{M}$-fibrations are exactly canonical fibrations and that $\mathbf{M}$-cofibrations are exactly canonical cofibrations. 

+-- {: .num_lemma} 
###### Lemma 
The terminal object $1$ is $\mathbf{M}$-cofibrant, i.e., the inclusion $0 \to 1$ in $Cat$ is an $\mathbf{M}$-cofibration. 
=-- 

+-- {: .proof} 
###### Proof 
Let $C$ be any noninitial category; by a standard result of model category theory, there is an $\mathbf{M}$-cofibrant replacement $\tilde{C} \to C$, a weak equivalence such that $0 \to \tilde{C}$ is a cofibration. This $\tilde{C}$ is noninitial and therefore has $1$ as a retract; thus $1$ is $\mathbf{M}$-cofibrant since cofibrant objects are closed under retracts. 
=-- 

+-- {: .num_prop #canonical} 
###### Proposition 
Each acyclic $\mathbf{M}$-fibration is a canonical acyclic fibration. 
=-- 

+-- {: .proof} 
Each acyclic $\mathbf{M}$-fibration $f: E \to X$ has the right lifting property with respect to $\mathbf{M}$-cofibrations. The right lifting property with respect to the $\mathbf{M}$-cofibration $0 \to 1$ is exactly the condition of being surjective on objects. Thus acyclic $\mathbf{M}$-fibrations are necessarily categorical equivalences that are surjective on objects, i.e., are necessarily canonical acyclic fibrations. 
=-- 

Before giving the next result, we recall that the lifting relation on morphisms gives a [[Galois connection]]. Specifically, suppose $c: A \to B$ and $f: c \to d$ are functors, and define $c \perp f$ if for every morphism from $c$ to $f$ in the arrow category $Cat^\mathbf{2}$, i.e., for every commutative diagram 

$$\array{
A & \to & C \\ 
_\mathllap{c} \downarrow & & \downarrow_\mathrlap{f} \\ 
B & \to & D
}$$ 

of functors, there is a lifting $B \to C$ filling in to make two commutative triangles. As any relation does, this lifting relation $\perp$ gives a Galois connection on subclasses of $Mor(Cat)$. General facts about Galois connections may then be applied. 

+-- {: .num_cor #sub} 
###### Corollary 
Every canonical cofibration is an $\mathbf{M}$-cofibration. Every $\mathbf{M}$-fibration is a canonical fibration. 
=-- 

+-- {: .proof} 
###### Proof 
By the Galois connection induced by the lifting relation, Proposition \ref{canonical} implies that canonical cofibrations form a subset of $\mathbf{M}$-cofibrations, and therefore that canonical acyclic cofibrations are a subset of acyclic $\mathbf{M}$-cofibrations. Again by the Galois connection, this in turn implies that $\mathbf{M}$-fibrations form a subset of canonical fibrations. 
=-- 

At this point, we would like to show conversely that every $\mathbf{M}$-cofibration is a canonical cofibration (i.e., is injective on objects); another appeal to Galois connections would then allow us to deduce that every canonical fibration is an $\mathbf{M}$-fibration, and we would be done. Let us suppose otherwise, that there exists an $\mathbf{M}$-cofibration that is not injective on objects, and derive a contradiction. 

For a set $S$, let $K(S)$ be the category whose objects are the elements of $S$, with exactly one morphism $x \to y$ for any $x, y \in S$. This gives the _codiscrete_ (or *chaotic*) functor 
$K: Set \to Cat$, which is right adjoint to the forgetful functor $U: Cat \to Set$ that takes a category to its underlying set of objects. For each inhabited set $S$, we have that $K(S)$ is equivalent to $1$, and conversely any category equivalent to $1$ is isomorphic to some $K(S)$. 

+-- {: .num_prop #key} 
###### Proposition 
If there is any $\mathbf{M}$-cofibration $f: A \to B$ that is not injective on objects, then the map $K(2) \to 1$ ($2 = \{0, 1\}$) is an (acyclic) $\mathbf{M}$-cofibration. 
=-- 

+-- {: .proof} 
###### Proof 
First we observe that for any category $E$, the unit map $\eta_E: E \to K U(E)$ for the adjunction $U \dashv K$ is an $\mathbf{M}$-cofibration. For, the map $\eta_E$ is an isomorphism on objects and therefore a canonical cofibration; it is an $\mathbf{M}$-cofibration by Corollary \ref{sub}. 

By hypothesis, $f$ maps two objects $a, a'$ of $A$ to the same object $b$ of $B$, so there is a commutative diagram 

$$\array{
2 & \stackrel{(a, a')}{\hookrightarrow} & U A \\ 
\downarrow & & \downarrow_\mathrlap{f} \\ 
1 & \underset{b}{\to} & U B.
}$$ 

Let $r: U A \to 2$ be a retraction of the injection $2 \to U A$. By the adjunction $U \dashv K$, the map $r$ corresponds to a map $s: A \to K(2)$. We form a pushout square 

$$\array{
A & \stackrel{s}{\to} & K(2) & & \\ 
_\mathllap{f} \downarrow & & \downarrow_\mathrlap{g} & & \\ 
B & \underset{h}{\to} & E & \underset{\eta_E}{\to} & K U(E)
}$$ 

where $g$ is an $\mathbf{M}$-cofibration (being the pushout of a cofibration $f$). Thus we have a composite cofibration $t \coloneqq \eta_E \circ g: K(2) \to K U(E)$. It may be verified that $K(2) \to 1$ is a retract of $t$, i.e., there is a commutative square 

$$\array{
K(2) & \stackrel{id}{\to} & K(2) \\ 
_\mathllap{t} \downarrow & & \downarrow \\ 
K U(E) & \underset{j}{\leftarrow} & 1
}$$ 

where $j = \eta_E \circ h \circ b$; this diagram commutes on objects by construction, and it commutes on morphisms because all diagrams commute in $K U(E)$. Thus $K(2) \to 1$, being a retract of an $\mathbf{M}$-cofibration, is also an $\mathbf{M}$-cofibration. 
=-- 

The conclusion of Proposition \ref{key} now leads to a contradiction: 

+-- {: .num_prop} 
###### Proposition 
If $K(2) \to 1$ is an acyclic $\mathbf{M}$-cofibration, then for any category $C$, every automorphism of $C$ is an identity (which is absurd!). 
=-- 

+-- {: .proof} 
###### Proof 
The object $C$ of $Cat$ has an $\mathbf{M}$-fibrant replacement $\hat{C}$ equivalent to $C$. For any isomorphism $\phi$ of $\hat{C}$, let $e: K(2) \to \hat{C}$ be the unique functor taking $0 \to 1$ in $K(2)$ to $\phi$. Then we have a commutative diagram 

$$\array{
K(2) & \stackrel{e}{\to} & \hat{C} \\ 
_\mathllap{acyc.\; cof.} \downarrow & & \downarrow _\mathrlap{fib.} \\ 
1 & \to & 1
}$$ 

and the existence of a lift $1 \to \hat{C}$ filling in this diagram means that $\phi$ is an identity. In particular, every automorphism of $\hat{C}$ is an identity; since $C \simeq \hat{C}$, the same is true of $C$. 
=-- 



### Relation with bisimplicial sets

Recall that Rezk's classifying diagram for a (small) category $C$ is the [[bisimplicial set]] $N (C)$ defined by $N (C)_{n, m} = Fun ([n] \times \mathbf{I}[m], C)$, where $[n]$ is the standard $n$-[[simplex]] considered as a category and $\mathbf{I}$ is the [[localization|groupoid completion]] functor (i.e. $D \mapsto D [D^{-1}]$). There is then an [[adjunction]]
$$\tau_1 \dashv N : Cat \to ssSet$$
and it can be shown that the canonical model structure on Cat is the model structure obtained by [[transferred model structure|transferring]] the [[model structure on simplicial presheaves|projective model structure]] on $ssSet$. 


## Related concepts

* [[canonical model structure]]

* **canonical model structure on $Cat$**

* [[canonical model structure on groupoids|canonical model structure on Grpd]]

* [[canonical model structure on Operad]]

* [[weak equivalence of internal categories]]

## References

Original discussion in the generality of [[internal category|categories internal to]] [[topoi]] (hence of [[2-sheaves]]):

* {#JoyalTierney91} [[André Joyal]], [[Myles Tierney]], Thm. 4 (p. 232) of: *Strong stacks and classifying spaces*, in: *Category Theory* Lecture Notes in Mathematics **1488**, Springer (1991) 213-236 &lbrack;[doi:10.1007/BFb0084222](https://doi.org/10.1007/BFb0084222)&rbrack;

More on the ordinary case (categories internal to [[Sets]]):

* {#Rezk96} [[Charles Rezk]], *A model category for categories* (1996) &lbrack;[[Rezk_ModelCategoryForCategories.pdf:file]]&rbrack;

* {#Joyal10} [[André Joyal]], *[[joyalscatlab:Model structures on Cat]]* (2010)

and proof of the uniqueness of the model structure:

* {#Schommer-Pries12} [[Chris Schommer-Pries]], *[The canonical model structure on Cat](https://sbseminar.wordpress.com/2012/11/16/the-canonical-model-structure-on-cat/)*, Secret Blogging Seminar (2012)

Discussion for [[internal categories]] more generally in [[finitely complete categories]]:

* [[Tomas Everaert]], [[Rudger W. Kieboom]], [[Tim Van der Linden]], _Model structures for homotopy of internal categories_, Theory and Applications of Categories **15** 3 (CT2004) 66-94 &lbrack;[tac:15-03](http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html)&rbrack;

(insert description of article here):

* {#Hughes25} [[Calum Hughes]], *The algebraic internal groupoid model of Martin-Löf type theory* ([arXiv:2503.17319](https://arxiv.org/abs/2503.17319))

[[!redirects canonical model structure on Cat]]
[[!redirects canonical model structure on categories]]
[[!redirects natural model structure on Cat]]
[[!redirects natural model structure on categories]]
[[!redirects folk model structure on Cat]]
[[!redirects folk model structure on categories]]
