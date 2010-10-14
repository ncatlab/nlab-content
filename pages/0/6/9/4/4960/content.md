

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}
 
## Idea

The definition of _cohesive topos_ or _category of cohesion_ aims to axiomatize properties of a [[topos]] that make it a [[gros topos]] of [[space]]s inside of which [[geometry]] may take place.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] geometric morphism $\Gamma : E \to Set$ of a cohesive topos over [[Set]] may be thought of as sending a space $X$ to its underlying set of points $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten)

Conversely, the [[left adjoint]] and [[right adjoint]] of $\Gamma$

$$
  E 
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  S
$$

send a set $S$ either to the [[discrete space]] $Disc(S)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space]] $Codisc(S)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]) .

Moreover, the idea is that cohesion makes points lump together to _connected pieces_ . This is modeled by one more functor $\Pi : E \to S$ [[left adjoint]] to $Disc$. In the context of 1-[[topos theory]] this sends a cohesive space to its [[connected topos|connected componets]] $(\Pi = \pi_0)$. More generally in an [[(n,1)-topos]]-theory context, $\Pi$ sends a cohesive space $X$ to the $n$-[[truncated|truncation]] of its [[geometric homotopy groups in an (∞,1)-topos|geometric fundamental ∞-groupoid]] $\Pi(X)$.

In total this gives a quadruple of [[adjoint functor]]s

   $$
    (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
    E
     \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
    S
    \;
   $$

A cohesive topos is a topos whose terminal [[geometric morphism]] admits an extenson to such a quadruple of adjoints, satisfying some further properties.

## Definition

### Cohesive topos

+-- {: .un_defn}
###### Definition

A [[topos]] $E$ over some base topos $S$, i.e. equipped with a [[geometric morphism]]

$$
  (f^* \dashv f_*) E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  S
$$

is **cohesive** or  **a topos of cohesion** if it has the following [[stuff, structure, property|properties]]:

1. it is _local_ and _connected_ in the following sense:

   1. it is a [[locally connected topos]]: there exists a further [[left adjoint]] $(f_! \dashv f^*)$ satisfying a suitable condition;

   1. it is a [[connected topos]]: the functor $f_!$ preserves the [[terminal object]], or equivalently $f^*$ is [[fully faithful functor|fully faithful]];

   1. it is _strongly connected_ : $f_!$ preserves even all [[finite]] [[product]]s;

   1. it is a [[local topos]]: there exists a further [[right adjoint]] $(f_* \dashv f^!)$ (this is sufficient for $f$ to be local, since we have already assumed it to be connected);

   so that in total we have a quadruple of [[adjoint functor]]s
   
   $$
    (f_! \dashv f^* \dashv f_* \dashv f^!) : 
    E
     \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    S
    \;
   $$

   Note that $f$ being local implies, in particular, that $S \stackrel{f^!}{\hookrightarrow} E$ is a [[subtopos]]: $f^!$ is a [[full and faithful functor]];

1. $f_!$ is "continuous" in that for all $s \in S$ and $e \in E$ the natural morphism

   $$
     f_! (e^{f^* s}) \stackrel{\simeq}{\to} (f_!(e))^s
   $$

   is an [[isomorphism]]

   (this morphism is the [[internal hom]]-[[adjunct]] of 
   $
     s \times f_!(e^{f^* s}) 
      \stackrel{\simeq}{\to}
     f_!f^*(s) \times f_!(e^{f^* s})
      \stackrel{\simeq}{\to}
     f_!(f^*(s) \times e^{f^* s})
     \to
     f_!(e)
   $
   where we use that by definition $f^*$ is full and faithful and then that $f_!$ preserves products); 

1. the [[natural transformation]]

   $$
     f_*  
       \stackrel{\simeq}{\to} 
     f_* ( f^*  f_* )
       \stackrel{}{\to}
     f_* ( Id ) 
       \stackrel{}{\to}
     f_*( f^* f_! )
       \stackrel{\simeq}{\to}
     f_!
   $$

   is an [[epimorphism]], equivalently the transformation

   $$
     f^* \to f^!
   $$

   is a [[monomorphism]].

=--

### Cohesive $(\infty,1)$-topos


The above definition has a straightforward generalization to [[(∞,1)-topos]]-theory: adjoint functors are generalized to [[adjoint (∞,1)-functor]]s, full and faithful functors to [[full and faithful (∞,1)-functor]]s and monomorphisms to [[regular monomorphism]]s.



## Examples

A trivial class of examples is:

* Every topos is cohesive over itself.

In the following we describe more interesting examples.

### Sites of cohesion {#SitesOfCohesion}

We define extra [[stuff, structure, property|property]] on a [[site]] $C$ such that 

* the [[sheaf topos]] over $C$ is cohesive over [[Set]];

* the [[(∞,1)-sheaf (∞,1)-topos]] over $C$ is cohesive over [[∞Grpd]];

* and generally the [[(n,1)-topos]] over $C$ is cohesive over [[nGrpd]].

{#SiteOfCohesion}
+-- {: .un_def}
###### Definition

A **site of cohesion** over [[Set]] is

* a [[site]] -- a [[small category]] $C$ equipped with a [[coverage]];

* with the property that

  * it is a [[concrete site]];

  * it has finite [[product]]s;
  
  * for every [[covering]] family $\{U_i \to U\}$ in $C$ 

    * the [[Cech nerve]] $C(U) \in [C^{op}, sSet]$ is degreewise 
      a [[coproduct]] of [[representable functor|representables]];

    * the [[simplicial set]] obtained by replacing each copy of a representable by a point is a [[contractible]] [[Kan complex]]:

      $$
        \lim_\to C(U) \stackrel{\simeq}{\to} *
      $$

    * the simplicial set of points in $C(U)$ is a [[Kan complex]] [[homotopy equivalence|homotopy equivalent]] to the set of points of $U$:

      $$
        Hom_C(*, C(U)) \stackrel{\simeq}{\to} Hom_C(*,U)
        \,.
      $$
  
=--

+-- {: .un_remark}
###### Remark

This definition is supposed to model the following ideas:

* since the site is concrete, every object $U$ has an underlying set of points $Hom_C(*,U)$. We may think of each $U$  as specifying one way in which there can be cohesion on this underlying set of points;

* in view of the [[nerve theorem]] that $\lim_\to C(U)$ is contractible means that $U$ itself is contractible, as seen by the [[Grothendieck topology]] on $C$. This reflects the _local_ aspect of cohesion: we only specify cohesive structure on a contractible lumps of points;

* in view of this the remaining condition that $Hom_C(*,C(U))$ is contractible is just the $\infty$-analog of the condition on a [[concrete site]] that $Hom_C(*.\coprod_i U_i) \to Hom_C(*, U)$ is surjective.  This just expresses that the notion of topology on $C$ and its concreteness over [[Set]] are consistent.

=--

+-- {: .un_example}
###### Examples/Proposition

The following [[site]]s are sites of cohesive objects.

* the category [[CartSp]] with covering families given by the 
  [[good open cover]]s $\{U_i \to U\}$;

* the site [[ThCartSp]] $ \subset \mathbb{L}$ of [[smooth loci]] consisting smoth loci of the form $R^n \times D^l_{(k)}$ with the second factor infinitesimal, where covering families are projections of the
  form $\mathbb{R}^n \times D^l_{(k)} \to \mathbb{R}^n$ together with
  families of the form $\{U_i \times D^l_{(k)} \to U \times D^l_{(k)}\}$
  with $\{U_i \to U\}$ a covering family in $CartSp$. 

More discussion of these two examples is at [[∞-Lie groupoid]] and [[∞-Lie algebroid]].

=--


+-- {: .proof}
###### Proof

That $\lim_\to C(U) \simeq *$ follows from the [[nerve theorem]], using that a [[Cartesian space]] regarded as a [[topological space]] is [[contractible]].

=--



### Cohesive $(\infty,1)$-toposes over sites of cohesion {#InfTopOverSiteOfCohesion}


+-- {: .un_theorem}
###### Theorem

Let $C$ be [site of cohesion](#SiteOfCohesion). Then the [[(∞,1)-sheaf (∞,1)-topos]] $(\infty,1)Sh(C)$ is cohesive. 

=--

Since the [[(n,1)-topos]] over a site for any $n \in \mathbb{N}$ arises as the full [[sub-(∞,1)-category]] of the $(\infty,1)$-topos on the $n$-[[truncated]] objects and since the definition of cohesive $(n,1)$-topos is compatible with such truncation, it follows that

+-- {: .un_corollary}
###### Corollary

Let $C$ be [site of cohesion](#SiteOfCohesion). Then for all $n \in \mathbb{N}$ the [[(n,1)-topos]] $(n,1)Sh(C)$ is cohesive. 

=--



We prove this in a sequence of propositions, checking the conditions item-by-item. 

> (for the moment the following checks everything except the condition $\Pi(X^{Disc S}) \simeq \Pi(X)^S$)

The general strategy is that we [[presentable (∞,1)-category|present]] the [[(∞,1)-categories]] in terms of [[combinatorial simplicial model categories]] as reviewed at [[models for ∞-stack (∞,1)-toposes]]. Specifically, we use the left [[Bousfield localization of model categories|Bousfield localization]] $[C^{op}, sSet]_{proj,loc}$ of the  projective [[model structure on simplicial presheaves]] $[C^{op}, sSet]_{proj}$ at the [[Cech nerve]] projections $C(U) \to U$ to model the [[topological localization]] / Cech localization

$$
  (\infty,1)Sh(C) \stackrel{\leftarrow}{\hookrightarrow} (\infty,1)PSh(C)
  \,.
$$

See <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#LocalizationAtCoverage">Model structure on simplicial presheaves -- Localization at a coverage</a> for background.


+-- {: .un_lemma}
###### Standard fact

The model categories

* standard [[model structure on simplicial sets]] $sSet_{Quillen}$;

*  global [[model structure on simplicial presheaves]]  $[C^{op}, sSet]_{proj,loc}$;


*  local [[model structure on simplicial presheaves]]  $[C^{op}, sSet]_{proj,loc}$

are all  [[left proper model categories]].

=--

+-- {: .proof}
###### Proof

The first since all objects are cofibrant. The second by general statements about the global [[model structure on functors]], the third becuase [[Bousfield localization of model categories|Bousfield localization]] preserves left propernes.

=--


+-- {: .un_lemma}
###### Lemma

For $\{U_i \to U\}$ a [[covering]] family in the site of cohesion $C$, the [[Cech nerve]]
$C(U) \in [C^{op}, sSet]$ is a cofibrant [[resolution]] of $U$ both in the projective model structure $[C^{op}, sSet]_{proj}$ as well as in the Cech local model structure $[C^{op}, sSet]_{proj,loc}$.

=--

+-- {: .proof}
###### Proof

Being a Cech nerve we have that $C(U)$ is a [[split hypercover]]. By assumption on $C$,we have that $C(U)$ is degreewise a coproduct of representables. By <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects">Dugger's theorem on cofibrant objects</a> in the projective model structure this implies that $C(U)$ is cofibrant in the global model structure. By general properties of left [[Bousfield localization of model categories|Bousfield localizations]] we have that the cofibrations in the local model structure as the same as in the global one. Finally that $C(U) \to U$ is a weak equivalence in the local model structure holds effectively by definition (since we are localizing at these morphisms).

=--


+-- {: .un_prop}
###### Proposition

The [[global section]] geometric $(\infty,1)$-morphism

$$  
  (Disc \dashv \Gamma) : (\infty,1)Sh(C) 
  \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

is [[presentable (∞,1)-category|presented]] by the 
[[sSet]]-[[enriched functor|enriched]] [[Quillen adjunction]]

$$
  (Const \dashv \Gamma) :  [C^{op}, sSet]_{proj,loc}
  \stackrel{\leftarrow}{\to}
  sSet_{Quillen}
  \,,
$$

where $\Gamma$ is the functor that evaluates on the point ,$\Gamma X = X(*)$, and $Const$ is the functor that sends a simplicial set $S$ to the presheaf constant on that value, $Const S : U \mapsto S$.

=--

+-- {: .proof}
###### Proof

We use (as described there) that [[adjoint (∞,1)-functor]]s are modeled by [[sSet]]-enriched [[Quillen adjunction]]s between the [[simplicial model categories]] that model the $(\infty,1)$-categories in question.

That we have an [[adjunction]] $(Const \dashv \Gamma)$ follows for instance by observing that since $C$ has a [[terminal object]] we may think of $\Gamma$ as being the functor $\Gamma = \lim_\leftarrow$ that takes the [[limit]]. 

To see that we have a [[Quillen adjunction]] first notice that we have a Quillen adjunction

$$
  (Const \dashv \Gamma) :  [C^{op}, sSet]_{proj}
  \stackrel{\leftarrow}{\to}
  sSet_{Quillen}
$$

on the global model structure, since $\Gamma$ manifestly preserves fibrations and acyclic fibrations there. Since $[C^{op}, sSet]_{proj,loc}$ is left [[proper model category|proper]] and has the same cofibrations as the global model structure, it follows with [[Quillen adjunction|HTT, corollary A.3.7.2]] (see the discussion of <a href="http://ncatlab.org/nlab/show/Quillen+adjunction#sSet">sSet-Quillen adjunctions</a>) that for a Quillen adjunction on the local model structure it is sufficient that $\Gamma$ preserves fibrant objects. But every fibrant object in the local structure is in particular fibrant in the global structure, hence in particular fibrant over the terminal object of $C$.

That this indeed presents the $(\infty,1)$-adjunction in question follows by observing that the $(\infty,1)$-[[global section]] functor $\Gamma$ is given by the [[(∞,1)-limit]] operation on [[(∞,1)-presheaves]]. Since $C$ has a terminal object, it follows here, too, that this is just evaluation on the point.

=--


+-- {: .un_prop}
###### Proposition

The [[(∞,1)-topos]] over a site of cohesion is a [[locally ∞-connected (∞,1)-topos]] in that the [[constant (∞,1)-sheaf]]-functor $Const$ has a [[left adjoint|left]] [[adjoint (∞,1)-functor]]

$$
  (\Pi \dashv Const) : Sh_{(\infty,1)}(C)
    \stackrel{\leftarrow}{\to}
  \infty Grpd
$$


In fact, it is even a [[∞-connected (∞,1)-topos]] in that in addition the $(\infty,1)$-functor $LConst$ is a [[full and faithful (∞,1)-functor]].

=--


+-- {: .proof}
###### Proof

We use (as described there) that [[adjoint (∞,1)-functor]]s are modeled by [[sSet]]-enriched [[Quillen adjunction]]s between the [[simplicial model categories]] that model the $(\infty,1)$-categories in question.

By general abstract facts the [[sSet]]-functor $Const : sSet \to [C^{op}, sSet]$ given on $S \in sSet$ by $Const_S : U \mapsto S$ for all $U \in C$ has an  [[sSet]]-[[left adjoint]] 

$$
  \Pi : X \mapsto \int^U X(U) = \lim_\to X
$$ 

naturally in $X$ and $S$, given by the [[colimit]] operation. Notice that since $sSet$ is itself a category of presheaves, these colimits are degreewise colimits in [[Set]]. Also notice that the colimit over a [[representable functor]] is the point.

Regarded as a functor  $sSet_{Quillen} \to [C^{op}, sSet]_{proj}$ the functor $Const$ manifestly preserves fibrations and acyclic fibrations and hence

$$
  (\Pi \dashv Const) : [C^{op}, sSet]_{proj} \stackrel{\leftarrow}{\to}
    sSet_{Quillen} 
$$

is a [[Quillen adjunction]], in particular $\Pi : [C^{op},sSet]_{proj} \to sSet_{Quillen}$ preserves cofibrations. Since by general properties of left [[Bousfield localization of model categories]] the cofibrations of $[C^{op},sSet]_{proj,loc}$ are the same, also $\Pi : [C^{op}, sSet]_{proj,loc} \to sSet_{Quillen}$ preserves cofibrations. 

Since $sSet_{Quillen}$ is a [[left proper model category]] it follows with [[Quillen adjunction|HTT, corollary A.3.7.2]] (see the discussion of <a href="http://ncatlab.org/nlab/show/Quillen+adjunction#sSet">sSet-Quillen adjunctions</a>) that for 

$$
  (\Pi \dashv Const) : [C^{op}, sSet]_{proj,loc}
   \stackrel{\leftarrow}{\to}
   sSet_{Quillen}
$$

to be a [[Quillen adjunction]], it suffices to show that $Const$ preserves fibrant objects. That means that constant simplicial presheaves satisfy descent along covering families in the site of cohesion $C$: for every covering family $\{U_i \to U\}$ in $C$ and every simplicial set $S$ it must be true that

$$
  [C^{op}, sSet](U, Const S) \to [C^{op}, sSet](C(U), Const S)
$$

is a [[homotopy equivalence]] of [[Kan complexes]]. Here we use that $U$, being a representable, is cofibrant, that $C(U)$ is cofibrant by the above lemma and that $Const S$ is fibrant in the projective structure by the assumption that $S$ is fibrant. So the simplicial hom-complexes in the above really are the correct [[derived hom-space]]s.

But that this is the case follows by the condition on the site of cohesion $C$ by which $\lim_\to C(U) \simeq *$: using this it follows that

$$
  [C^{op}, sSet](C(U), Const S) = sSet(\lim_\to C(U), S) \simeq sSet(*, S) = S
  \,.
$$

So we have established that

$$
  (\Pi \dashv Const) : [C^{op}, sSet]_{proj,loc} \stackrel{\leftarrow}{\to}
  sSet_{Quillen}
$$

is a [[Quillen adjunction]].

It is evident that $\Pi \circ Const = Id$ and $\Gamma Const = Id$ and that these relations pass to the composition of the corresponding [[derived functor]]s. This says that 

the comoposite adjunction

$$
  (\Pi Const \dashv \Gamma LConst)
  \; : \;
  \infty Grpd
  \stackrel{\overset{LConst}{\to}}{\underset{\Gamma}{\leftarrow}}
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{\Pi}{\to}}{\underset{LConst}{\leftarrow}}
  \infty Grpd
$$

is (equivalent to) the identity adjunction $(\Id \dashv Id)$. In particular the counit $\Pi Const \to Id$  is an equivalence, which implies by general properties of [[adjoint (∞,1)-functor]]s that $Const$ is a [[full and faithful (∞,1)-functor]]. 

=--

+-- {: .un_remark}
###### Remark

This implies in particular that

* the [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $\infty Grpd \stackrel{\overset{\Pi}{\leftarrow}}{\underset{LConst}{\hookrightarrow}} Sh_{(\infty,1)}(C)$ exhibits [[nLab:∞Grpd]] as a [[reflective sub-(∞,1)-category]] of $Sh_{(\infty,1)}(C)$, hence as a [[nLab:localization of an (∞,1)-category|localization]] of $Sh_{(\infty,1)}(C)$ at those morphisms that induce equivalences on geometric realizations, hence isomorphisms on geometric [[nLab:homotopy groups in an (∞,1)-topos]].

* the _shape_ of $Sh_{(\infty,1)}(C)$ in the sense of [[shape of an (∞,1)-topos]] is that of the point.

=--




+-- {: .un_prop}
###### Proposition

The functor $Pi : (\infty,1)Sh(C) \to \infty Grpd$ whose existence is guaranteed by the above proposition preserves [[product]]s:

$$
  \Pi(A \times B) \simeq \Pi(A) \times \Pi(B)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Notice from the discussion at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#MonoidalStructure">model structure on simplicial presheaves -- closed monoidal structure</a> that for $X \in [C^{op}, sSet]_{proj,cov}$ cofibrant, the [[closed monoidal structure on presheaves]]-adjunction $(X \times (-) \dashv [X,-])$ is a [[Quillen adjunction]].

Let $A$ and $B$ be representatives in the model $[C^{op}, sSet]_{proj,cov}$. By <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantReplacement">Dugger's cofibrant replacement operation</a> we have that a cofibrant replacement for $A \times B$ is given by

$$
  \int^{[n] \in \Delta}
    \Delta[n] \cdot (\coprod_{U_n \to \cdots \to A_n \times B_n} U_n)
$$

with the $U_\cdot$ being representables, and similarly for $A$ and $B$ themselves. By the above discussion, the functor $\Pi$ is given by the left [[derived functor]] of the [[colimit]] $\lim_\to$. This commutes with the above [[coend]] and [[coproduct]]s, so that we have

$$
  \begin{aligned}
    \Pi(A \times B)
    &\simeq
    \lim_\to 
      \int^{[n] \in \Delta}
    \Delta[n] \cdot (\coprod_{U_n \to \cdots \to A_n \times B_n} U_n)
    \\
    & =
      \int^{[n] \in \Delta}
    \Delta[n] \cdot (\coprod_{U_n \to \cdots \to A_n \times B_n} \lim_\to U_n)
    \\
    & =
      \int^{[n] \in \Delta}
    \Delta[n] \cdot (\coprod_{U_n \to \cdots \to A_n \times B_n} *)
  \end{aligned}
  \,.
$$

Since maps into $A_n \times B_n$ are pairs of maps into $A_n$ and $B_n$ this is 

$$
  \cdots = 
     \left(
      \int^{[n] \in \Delta}
    \Delta[n] \cdot (\coprod_{U_n \to \cdots \to A_n} *) \right)
    \times
     \left(
      \int^{[n] \in \Delta}
    \Delta[n] \cdot (\coprod_{U_n \to \cdots \to B_n} *) \right) 
  \,,
$$

as the [[nLab:product]] in [[nLab:sSet]] is taken degreewise. This is by the same reasoning the value of $(\mathbb{L} \lim_\to A) \times (\mathbb{L} \lim_\to B)$.


=--




+-- {: .un_prop}
###### Proposition

We have a pair of [[adjoint (∞,1)-functor]]s 

$$  
  (\infty,1)Sh(C) \stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}} 
  \infty Grpd
$$

=--

+-- {: .proof}
###### Proof

At the level of simplicial presheaves the right $sSet$-adjoint to $\Gamma$ is

$$
  Codisc S : U \mapsto sSet(\Gamma(U), S)
$$

as confirmed by the following computation:

$$
  \begin{aligned}
    [C^{op}, sSet](X, Codisc(S))
    & =
    \int_{U \in C} sSet(X(U), sSet(\Gamma(U), S)
    \\
    & = \int_{U \in C} sSet(X(U) \times \Gamma(U), S)
    \\
    & = sSet( \int^{U \in C} X(U) \times \Gamma(U), \;\; S )
    \\
    & = sSet( \int^{U \in C } X(U) \times Hom_C(*, U), \;\; S)
    \\
    & = sSet(X(*), S)
    \\
    & = sSet(\Gamma(X), S)
  \end{aligned}
  \,,
$$

where in the second but last step we used the [[co-Yoneda lemma]].

It is clear that 

$$
  (\Gamma \dashv Codisc) : [C^{op}, sSet]_{proj} \stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}
  sSet_{Quillen}
$$

is a [[Quillen adjunction]], since $Codisc$ manifestly preserves fibrations and acyclic fibrations. As before, to see that this descends to a Quillen adjunction on the local model structure it is  to check that $Codisc : sSet_{Quillen} \to  [C^{op}, sSet]_{proj,loc}$ preserves fibrant objects, in that for $S$ a [[Kan complex]] we have that $Cosidc S$ satisfies [[descent]] along Cech-nerves of covering families. 

This following from the second defining condition on the site of cohesion $C$, that $Hom_C(*,C(U)) \simeq Hom_C(*,U)$. Using this we have the descent equivalence

$$
  [C^{op}, sSet](U, Codisc S)
   =
  sSet(Hom_C(*,U), S)  
   \simeq
  sSet(Hom_C(*,C(U)), S)
   =
  [C^{op}, sSet](C(U), Codisc S)
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

The [[(∞,1)-functor]] $Codisc : \infty Grpd \to (\infty,1)Sh(C)$ established by the above proposition is a [[full and faithful (∞,1)-functor]].

=--

+-- {: .proof}
###### Proof

By the standard properties of [[adjoint (∞,1)-functor]]s this is equivalent to an equivalence of $(\infty,1)$-functors $\Gamma \circ Codisc \simeq Id$.

By the above propositions we have that $\Gamma$ is both a left as well as a right Quillen functor. Therefore the composite $(\infty,1)$-functor is modeled (as described at [[derived functor]]) on a Kan complex simply by the composition of the corresponding simplicial Quillen functors. This is manifestly equal to the identity.

=--


+-- {: .un_prop}
###### Proposition

For $S \in \infty Grpd$ the natural morphisms

$$
  Disc S \to Codisc S
$$

are $(\infty,1)$-[[regular monomorphism]]s.

=--

+-- {: .proof}
###### Proof

We have to show that for $S$ a [[Kan complex]] and $U \in C$ with underlying set $\Gamma(U)$ the morphism

$$
  S \to S^{\Gamma(U)}
$$

is the [[homotopy limit]] over some cosimplicial diagram. Take that diagram to be

$$
  sSet({C(\Gamma(U) \to *)},S)
  =
  \left(
    sSet(\Gamma(U),S)
    \stackrel{\to}{\to}
    sSet(\Gamma(U) \times \Gamma(U), S)
    \stackrel{\to}{\stackrel{\to}{\to}}
    sSet(\Gamma(U) \times \Gamma(U) \times \Gamma(U), S)
    \cdots
  \right)
  \,.
$$

We claim that this is fibrant in the [[Reedy model structure]] on [[cosimplicial object]]s in $sSet_{Quillen}$: in degree $k$ the map into the matching  object is

$$
  sSet(\Gamma(U)^k, S) \to 
  \lim_{\leftarrow_i} sSet(\Gamma(U)^i, S)
  =
  sSet(\lim_{\to_i} \Gamma(U)^i, S)
  \,.
$$ 

Since $S$ is fibrant in $sSet_{Quillen}$ and using that
$sSet_{Quillen}$ is a [[simplicial model category]], we have that this
is a fibration if

$$
  \lim_{\to_i} \Gamma(U)^i \to \Gamma(U)^k
$$

is a coffibration. But this is the inclusion 
into all $k$-tuples of elements of $U$ of those $k$-tuples for which 
an entry repeats. So this is a monomorphism, hence a cofibration.

Therefore the [[homotopy limit]] over $sSet({C(\Gamma(U) \to *)},S)$
is the ordinary limit, which is

$$
  \lim_{\leftarrow_k} sSet(\Gamma(U)^k, S)
  =
  sSet(\lim_{\to_k} \Gamma(U)^k, S)
  = sSet(*, S)
  = S
  \,.
$$

=--



#### Smooth sets

Here we go in detail through a 1-categorical version of the above arguments, over the site of cohesion [[CartSp]]. Below in [infinity-Lie groupoids](#InfLieGrpd) we look at the full $(\infty,1)$-topos over this site.

+-- {: .un_theorem}
###### Theorem

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a cohesive topos over [[Set]].

=--

We first show that it is a [[locally connected topos]] in that the terminal [[global section]] [[geometric morphism]] to [[Set]] is an [[essential geometric morphism]]

$$
  Sh(CartSp)
  \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{L Const}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
$$

and show that the extra [[left adjoint]] $\Pi_0 : Sh(CartSp) \to Set$ sends diffeological spaces to the set of path-[[connected]] components of their underlying [[topological space]]s.


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]].

=--

+-- {: .proof}
###### Proof

The following argument works for every [[site]] $C$ which is such that constant presheaves on $C$ are already sheaves.

Notice that this is the case for $C = CartSp$ because every Cartesian space is connected: for $S \in Set$ a compatible family of elements of $Const S$ on a cover $\{U_i \to \mathbb{R}^n\}$ of some $\mathbb{R}^n$ is an element of $S$ on each patch, such that their restriction maps to intersections of patches coincide. But the restriction maps are all identities, so this says that all these elements coincide. Therefore the set of compatible families is just the set $S$ itself, hence the presheaf $Const S$ is a sheaf.

So with $L : PSh(C) \to Sh(C)$ the [[sheafification]] functor we have that $L Const S \simeq Const S$.

Whenever this is the case the [[left adjoint]] to the constant presheaf functor, which always exists for presheaves and is given by the [[colimit]] functor, is also left adjoint on the level of sheaves, because for each $X \in Sh(C)$ and $S \in Set$ we have natural bijections

$$
  \begin{aligned}
    Hom_{Sh(C)}(X, L Const S)
    & =
    Hom_{PSh(C)}(X, L Const S)
    \\
    & \simeq
    Hom_{PSh(C)}(X, Const S)
    \\
    & \simeq
    Hom_{Set}(\lim_\to X, S)
  \end{aligned}
  \,.
$$

=--

+-- {: .un_def}
###### Definition

Write $\Pi_0 := \lim_\to : Sh(CartSp) \to Set$
for the [[left adjoint]] to $LConst : Set \stackrel{Const}{\to} PSh(C) \stackrel{L}{\to} Sh(C)$.

=--

+-- {: .un_prop}
###### Proposition

For $X \in Sh(C)$ a diffeological space, $\Pi_0(X)$ is the set of path-connected components of the topological space underlying $X$.

=--

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]] we may write 

$$
  X = {\lim_\to}_{(U \to X) \in y/X} U
$$

and since $\Pi_0$ commutes with colimits we have

$$
  \Pi_0(X) \simeq 
  \Pi_0 {\lim_\to}_{(U \to X)} U
  \simeq
  {\lim_\to}_{(U \to X)} \Pi_0(U)
  \,.
$$

But also by the co-Yoneda lemma we have that the [[colimit]] over any [[representable functor|representable]] is the singleton set, hence our expression

$$
  \cdots \simeq 
  {\lim_\to}_{(U \to X)} *
$$

is the colimit over the category of plots of $X$ of the functor that is constant on the point. This colimit is the [[coproduct]] of points over the connected components of the [[diagram]] category.

The connected components of the category of plots $y/X$ are the path-connected (or "plot-connected") components of the underlying topological space of $X$.



=--


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is even a [[connected topos]].

=--

+-- {: .proof}
###### Proof

Since $CartSp$ is a [[connected category]] it is immediate that $Const : Set \to PSh(CartSp)$ is a [[full and faithful functor]]. By the above this equals $L Const$, which is hence also full and faithful.

By the discussion at [[connected topos]] we could equivalently convince ourselves that $\Pi_0$ preserves the terminal object. The terminal object of $Sh(CartSp)$ is $y(\mathbb{R}^0)$, hence representable. By the above, $\Pi_0$ sends all representable objects to the singleton set, which is the terminal object of $Set$. 

=--

#### Diffeological spaces

A _reflective localization_ at a collection of morphisms $W$ is a [[reflective subcategory]] on [[local object]]s, those $A$ for which for all $w \in W$ we have that $A^w$ is an isomorphism.

We say a **quasi-localization** is similarly a full subcategory on objects such that $A^w$ in a [[monomorphism]].



+-- {: .un_prop}
###### Proposition

The [[quasitopos]] of [[diffeological space]]s 

$$
  Diffeol \hookrightarrow Sh(CartSp)
$$

is the reflective quasi-localization at the counits  $Disc \Gamma U \to U$ for $U \in CartSp$.

=--

+-- {: .proof}
###### Proof

For $X \in Sh(CartSp)$ we have

$$
  Hom(Disc \Gamma U , X) 
    \simeq
  Hom_{Set}(\Gamma U , \Gamma X)
  \,.
$$

So we need to check for which $X$ we have for all $U\in CartSp$ that

$$
  Hom(U,X) \to Hom_{Set}(\Gamma(U), \Gamma(X))
$$

is a monomorphism.

The [[image]] of this morphism is $Hom(U, Conc(X))$, the plots of the [[concrete sheaf|concretization]] of $X$: the [[diffeological space]] underlying $X$. So we have a factorization of our morphism as

$$
   Hom(U,X) 
    \hookrightarrow
   Hom(U, Conc(X))
   \hookrightarrow
  Hom_{Set}(\Gamma U , \Gamma X)
  \,,
$$

where the second morphims is a monomorphism. So for the total morphism to be a monomorphism we need that the image-projection is. But since that is already an epimorphism, it follows that we need that the image projection is an isomorphism, hence that $X$ is already a [[concrete sheaf]].

So the concrete sheaves on $CartSp$, hence the [[diffeological space]]s, are precisely the quasi-localization at the morphisms $Disc \Gamma U \to U$.

=--



#### $\infty$-Lie groupoids {#InfLieGrpd}

As a special case of the above theorem, the [[(∞,1)-category of (∞,1)-sheaves]] $(\infty,1)Sh(CartSp) = $ [[?LieGrpd]] on [[CartSp]] is a cohesive $(\infty,1)$-topos over [[∞Grpd]]. (See there for the moment.)


### Interpretation of cohesive $(\infty,1)$-toposes

We list the geometric meaning of the various morphisms and structures in
a cohesive [[(∞,1)-topos]] over [[∞Grpd]]. (We follow the entries [[schreiber:structures in an (∞,1)-topos]] and [[schreiber:differential cohomology in an (∞,1)-topos]] where more motivation and justification for these interpretations can be found.)

Write

$$
 (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
 \mathbf{H}
  \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
 \infty Grpd
$$

for the given cohesive $(\infty,1)$-topos. Its objects $X,A \in \mathbf{H}$ we ay think of as [[∞-groupoid]]s with cohesive structure. For instance in the case $\mathbf{H} = $ [[?LieGrpd]] they are $\infty$-groupoids with _smooth_ structure. Then

* $\Gamma(X)$ is the _underlying $\infty$-groupoid_ of the cohesive $\infty$-groupoid $X$ (for instance an $\infty$-Lie groupoid with its smooth structure forgotten);

* $\Pi(X)$ is the fundamental [[path ∞-groupoid]] of $X$: its [[k-morphism]]s are generated from $k$-dimensional smooth paths in $X$ and the $k$-morphisms of $X$ itself. Under the equivalence of $(\infty,1)$-toposes 

  $|-| :$  [[∞Grpd]] $\stackrel{\simeq}{\to}$ [[Top]] 


  we may think of $|\Pi(X)|$ as the _geometric realization_ of $X$. For instance if $X \in \infty LieGrpd$ is a [[paracompact manifold]], then $|\Pi(X)|$ is, up to [[weak homotopy equivalence]] its underlying topological space.

Write 

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat})
  = 
  (Disc \Pi \dashv Disc \Gamma) : \mathbf{H} \to \mathbf{H}
  \,.
$$


Then unit and counit of the [[adjunction]]s give canonical natural morphisms

* $X \to \mathbf{\Pi}(X)$ -- this we may think of as the inclusion of $X$ as the constant paths in the [[path ∞-groupoid]] $\mathbf{\Pi}(X)$;

* $\mathbf{\flat}A \to A$ -- if we think of $A$ as the coefficient object for $A$-[[principal ∞-bundle]]s in $\mathbf{H}$, 

  $$  
    A Bund(X) := \mathbf{H}(X,A)
  $$

  then this is the map that takes principal $A$-bundles with [[schreiber:differential cohomology in an (∞,1)-topos|flat connection]] 

   $(X \to \mathbf{\flat}A) \leftrightarrow (\mathbf{\Pi}(X) \to A)$ to the underlying $A$-bundle.

  If $A = \mathbf{B}G$ is the [[delooping]] of an [[∞-group]] object, then we may think of $\mathbf{\flat} \mathbf{B}G$ or rather the corresponding  $Disc(\mathbf{B}G)$ as being $K(G,1)$: the classifying object for $G$-principal bundles where all cohesive structure on $G$ has been forgotten.

  Accordingly, the canonical map

  $$
    Disc(\mathbf{B}G) \to \Pi \mathbf{B}G
  $$

  that apppears in the second clause of the definition of cohesive topos is the inclusion of the topologist's $K(G,1)$ into the topological [[classifying space]] $\mathcal{B}G$. Again, on [[cocycle]]s this is the map from flat bundles to the underlying bundles.



## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* **cohesive topos** / [[cohesive (∞,1)-topos]]




## References

The definition of a category of cohesion was proposed in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))


The observation that $Sh(CartSp)$ is a [[local topos]] and that this serves to characterize [[diffeological space]]s was amplified by [[David Carchedi]].

[[!redirects cohesive toposes]]
[[!redirects cohesive topoi]]

[[!redirects category of cohesion]]
[[!redirects categories of cohesion]]

[[!redirects cohesive (∞,1)-topos]]