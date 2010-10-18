[[!redirects (∞,1)-cohesive site]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

An _$(\infty,1)$-cohesive site_ is a [[site]] such that the [[(∞,1)-category of (∞,1)-sheaves]] over it is a [[cohesive (∞,1)-topos]].




## Definition

+-- {: .un_def}
###### Definition

An **$(\infty,1)$-cohesive** over [[∞Grpd]] is

* a [[site]] -- a [[small category]] $C$ equipped with a [[coverage]];

* with the property that

  * it has finite [[product]]s, in particular a [[terminal object]] $*$;
  
  * for every [[covering]] family $\{U_i \to U\}$ in $C$ 

    * the [[Cech nerve]] $C(U) \in [C^{op}, sSet]$ is degreewise 
      a [[coproduct]] of [[representable functor|representables]];

    * the [[simplicial set]] obtained by replacing each copy of a representable by a point is [[contractible]] (weakly equivalent to the 
      point in the standard [[model structure on simplicial sets]])

      $$
        \lim_\to C(U) \stackrel{\simeq}{\to} *
      $$

    * the simplicial set of points in $C(U)$ is weakly equivalent to the set of points of $U$:

      $$
        Hom_C(*, C(U)) \stackrel{\simeq}{\to} Hom_C(*,U)
        \,.
      $$
  
=--

+-- {: .un_remark}
###### Remark

These conditions are stronger that for a [[cohesive site]], which only guarantees cohesiveness of the 1-topos over it.

This definition is supposed to model the following ideas:

* every object $U$ has an underlying set of points $Hom_C(*,U)$. We may think of each $U$  as specifying one way in which there can be cohesion on this underlying set of points;

* in view of the [[nerve theorem]] the condition that $\lim_\to C(U)$ is contractible means that $U$ itself is contractible, as seen by the [[Grothendieck topology]] on $C$. This reflects the _local_ aspect of cohesion: we only specify cohesive structure on contractible lumps of points;

* in view of this the remaining condition that $Hom_C(*,C(U))$ is contractible is just the $\infty$-analog of the condition on a [[concrete site]] that $Hom_C(*.\coprod_i U_i) \to Hom_C(*, U)$ is surjective.  This just expresses that the notion of topology on $C$ and its concreteness over [[Set]] are consistent.

=--


## Examples

+-- {: .un_example}
###### Example

The site for a [[presheaf topos]], hence with trivial topology, is $\infty$-cohesive if it has finite [[product]]s.

=--

+-- {: .proof}
###### Proof

All covers $\{U_i \to U\}$ consist of only the [[identity]] morphism $\{U \stackrel{Id}{\to} U\}$. The Cech $C\{U\}$ is then the [[simplicial object]] constant on $U$ and hence satisfies its two conditions above trivially.

=--

+-- {: .un_example}
###### Examples/Proposition

The following [[site]]s are $\infty$-cohesive:

* the category [[CartSp]] with covering families given by open covers $\{U_i \hookrightarrow U\}$ by [[geodesically convex|convex]] subsets $U_i$;

  we can take the morphisms $\mathbb{R}^k \to \mathbb{R}^l$ in $CartSp$ to be 

  * [[continuous maps]] 

    -- in which case the sheaf topos over it models generalized [[topological space]]s, the [[2-sheaf]] [[2-topos]] contains for instance [[topological stack]]s; 

  * or [[smooth maps]]

    -- in which case the sheaf topos models generalized [[smooth space]]s such as [[diffeological space]]s, the [[(∞,1)-sheaf (∞,1)-topos]] is that of [[∞-Lie groupoid]]s;


* the site [[ThCartSp]] $ \subset \mathbb{L}$ of [[smooth loci]] consisting smoth loci of the form $R^n \times D^l_{(k)}$ with the second factor infinitesimal, where covering families those of the form $\{U_i \times D^l_{(k)} \to U \times D^l_{(k)}\} with $\{U_i \to U\}$ a covering family in $CartSp$ as above. 

  This is a site of definition for the [[Cahiers topos]].

More discussion of these two examples is at [[∞-Lie groupoid]] and [[∞-Lie algebroid]].

=--


+-- {: .proof}
###### Proof



Since every [[star-shaped]] region in $\mathbb{R}^n$ is [[diffeomorphic]] to an [[open ball]] (see there for details) we have that the covers $\{U_i \to U\}$ on [[CartSp]] by convex subsets are [[good open covers]] in the strong sens that all finite non-empty interseciton is [[diffeomorphic]] to an [[open ball]] and hence diffeomorphic to a [[Cartesian space]]. Therefore these are [[good open cover]]s in the strong sense of the word and their [[Cech nerve]]s $C(U)$ are degreewise coproducts of representables.

The fact that $\lim_\to C(U) \simeq *$ follows from the [[nerve theorem]], using that a [[Cartesian space]] regarded as a [[topological space]] is [[contractible]].


=--



## Properties

+-- {: .un_theorem}
###### Theorem

Let $C$ be an $(\infty,1)$-cohesive site. Then the [[(∞,1)-sheaf (∞,1)-topos]] $(\infty,1)Sh(C)$ is a [[cohesive (∞,1)-topos]]. 

=--

Since the [[(n,1)-topos]] over a site for any $n \in \mathbb{N}$ arises as the full [[sub-(∞,1)-category]] of the $(\infty,1)$-topos on the $n$-[[truncated]] objects and since the definition of cohesive $(n,1)$-topos is compatible with such truncation, it follows that

+-- {: .un_corollary}
###### Corollary

Let $C$ be [site of cohesion](#SiteOfCohesion). Then for all $n \in \mathbb{N}$ the [[(n,1)-topos]] $(n,1)Sh(C)$ is cohesive. 

=--

We prove this in a sequence of propositions, checking the conditions item-by-item. 

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

The first since all objects are cofibrant. The second by general statements about the global [[model structure on functors]], the third because [[Bousfield localization of model categories|Bousfield localization]] preserves left propernes.

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

If the site $C$ has the property that for all $U \in C$ $\Gamma(U)$ is not empty, then:

for $S \in \infty Grpd$ the natural morphisms

$$
  Disc S \to Codisc S
$$

is a [[monomorphism in an (∞,1)-category]].

=--

This is evident. 

+-- {: .un_prop}
###### Proposition

If the site $C$ has the property that for all $U \in C$ $\Gamma(U)$ is not empty, then:

for $S \in \infty Grpd$ the natural morphisms

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


## Related concepts

* [[locally connected site]] / [[locally ∞-connected site]]

* [[cohesive site]] / **$(\infty,1)$-cohesive site**


[[!redirects (infinity,1)-cohesive sites]]