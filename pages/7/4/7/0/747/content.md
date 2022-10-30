
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* tic
{:toc}


## Idea

[[model category|Model structures]] on [[simplicial presheaf|simplicial presheaves]] [[presentable (∞,1)-category|present]] [[(∞,1)-category of (∞,1)-presheaves|(∞,1)-categories of (∞,1)-presheaves]] and [[localization of an (∞,1)-category|localizations of these]], such as notably the left exact localizations that are [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-categories of (∞,1)-sheaves]]: these model structures are [[models for ∞-stack (∞,1)-toposes]].


Recall that

* a [[model category]] is a way to [[presentable (infinity,1)-category|present]] an [[(∞,1)-category]];

* in the context of [[(∞,1)-categories]] [[presheaf|presheaves]] on an $(\infty,1)$-category $C$ are given by [[(∞,1)-functors]] $C^{op} \to$ [[SSet]].

This suggests that the [[(∞,1)-category of (∞,1)-sheaves]] on some [[site]] $C$ can be 
[[presentable (infinity,1)-category|presented]]
by a [[model category]] structure on the ordinary
[[functor category]] 

$$
  [C^{op},SSet] \simeq [\Delta^{op}, PSh(C)]
$$ 

-- the category of [[simplicial presheaf|simplicial presheaves]] .

Various interrelated flavors of model structures on the category of simplicial presheaves on $C$ have been introduced and studied since the 1970s, originally by K. Brown and [[Andre Joyal]] and then developed in detail by [[Rick Jardine]].

Notice that when regarded as a presentation of an [[(∞,1)-sheaf]], i.e. of an [[∞-stack]], a simplicial presheaf -- being an ordinary functor instead of a [[pseudofunctor]] -- corresponds to a [[rectified ∞-stack]]. It might therefore seem that a model given by simplicial presheaves is too restrictive to capture the full expected flexibility of a notion of [[∞-stack]].
But this is not so. 

In 

* [[Jacob Lurie]], [[Higher Topos Theory]]

a fully general definition of a [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-category of ∞-stacks]] is given it is shown -- proposition 6.5.2.1 --
that, indeed, the Brown--Joyal--Jardine model is a [[presentable (infinity,1)-category|presentation]] of that.

More precisely

* the [[global model structure on simplicial presheaves]] on a category is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-presheaves]];

* the [[?ech model structure on simplicial presheaves]] on a [[site]] is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-sheaves]];

* the [[local model structure on simplicial presheaves]] on a [[site]] is a [[presentable (infinity,1)-category|presentation]] of the _hypercompletion_ of the [[(∞,1)-category of (∞,1)-sheaves]] (see the discussion at [[hypercover]]).

* the [[Bousfield localization]] of the global [[model category]] structure to the local one presents the corresponding [[localization of an (∞,1)-category]] from presheaves to sheaves, mimicking the corresponding statement for a [[category of sheaves]].

Originally K. Brown had considered in [[BrownAHT]] not a model structure on simplicial presheaves but

* a [[category of fibrant objects]] structure on locally Kan simplicial sheaves (see there for details)

and Joyal had originally considered a 

* [[local model structure on simplicial sheaves]].

Joyal's [[local model structure on simplicial sheaves]] is [[Quillen equivalence|Quillen equivalent]] to the injective [[local model structure on simplicial presheaves]]. 

By repackaging [[Kan complex]]es as [[simplicial groupoids]] one obtains a [[model structure on presheaves of simplicial groupoids]] which is also Quillen equivalent to the above.

If K. Brown's [[category of fibrant objects]] on locally Kan simplicial sheaves is restricted to globally Kan simplicial sheaves on a [[topos]] with [[point of a topos|enough point]] then it is the full subcategory on the fibrant objects in the projective [[local model structure on simplicial sheaves]].


But since in all cases the weak equivalences are the same (where they apply, for Brown's model if the topos has enough points), all these local [[homotopical category|homotopical categories]] define equivalent [[homotopy category|homotopy categories]].

By Lurie's result these are in each case in turn equivalent to the [[homotopy category of an (infinity,1)-category|homtopy category of]] the [[(∞,1)-topos]] of [[∞-stacks]]. So in particular they serve as a home for general [[cohomology]].


Various old results appear in a new light this way. For instance using the old result of [[BrownAHT]] on the way ordinary [[abelian sheaf cohomology]] is embedded in the [[homotopy theory]] of simplicial sheaves, one sees that the old right derived functor definition of [[abelian sheaf cohomology]] really computes the [[∞-stackification]] of a sheaf of [[chain complex]]es regarded under the [[Dold?Kan correspondence]] as a simplicial sheaf.


## The different model structures and their interrelation 

It is the very point of [[model category]] structures on a given [[homotopical category]] that there may be several of them: each [[presentable (infinity,1)-category|presenting]] the same [[(∞,1)-category]] but also each suited for different computational purposes.

So it is good that there are many model structures on simplicial (pre)sheaves, as there are. 

### Injective/projective - local/global - presheaves/sheaves 

The following diagram is a map for part of the territory:

<div style="overflow:auto" markdown="1">
$$
  \array{
     &amp;&amp;
       (\infty,1)Sh(C)
     &amp;&amp;&amp;
       (\infty,1)PSh(C)
     &amp;&amp;&amp;
       (\infty,1)Sh(C)
     \\
     &amp;&amp; 
       \uparrow^{presentation}
     &amp;&amp;&amp;
       \uparrow^{presentation}
     &amp;&amp;&amp; 
       \uparrow^{presentation}
     \\
     SSh(C)^{l loc}_{inj} &amp; 
     \stackrel{\stackrel{sheafification}{\leftarrow}}
       {\stackrel{embedding}{\to}}&amp; 
     SPSh(C)^{l loc}_{inj} 
     &amp;\stackrel{}{\leftarrow}|&amp;
     SPSh(C)_{inj}
     &amp;\stackrel{\stackrel{Id}{\leftarrow}}
       {\stackrel{Id}{\rightarrow}}&amp;
     SPSh(C)_{proj}
     &amp;\stackrel{}{\mapsto}&amp;
     SPSh(C)_{proj}^{l loc}
     &amp;
     \stackrel{\stackrel{sheafification}{\to}}
       {\stackrel{embedding}{\leftarrow}}&amp; 
     SSh(C)_{proj}^{l loc}
     \\
     Joyal
     &amp;\stackrel{Quillen equivalence}{\leftrightarrow}&amp;
     Jardine
     &amp;\stackrel{left Bousf. localization}{\leftarrow|}&amp;
     Heller
     &amp;\stackrel{Quillen equivalence}{\leftrightarrow}&amp;
     Bousfield-Kan 
    &amp;\stackrel{left Bousf. localization}{\mapsto}&amp;
     Blander
     &amp;\stackrel{Quillen equivalence}{\leftrightarrow}&amp; 
     Brown-Gersten    
     \\
     \\
     &amp;
     everything cofibrant;
     \\
     &amp; fibrant = global injective fib...     
     \\
     \;\;\; 
     &amp; ...satisfying descent
     &amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;
     cofibrant = global projective cofib;
     \\
     &amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;
     fibrant = Kan valued and...    
     \\
     &amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;
     \;\;\; 
     ...satisfying descent

  }
$$
</div>

Here 

* "inj" denotes the injective model structure: cofibrations are objectwise cofibrations

* "proj" denotes the projective model structure: fibrations are objectwise fibrations

* no "loc" subscript means global model structure: weak equivalences are the objectwise weak equivalences:

* "l loc" denotes **left** [[Bousfield localization]] at [[hypercovers]] (at [[stalk]]wise acyclic fibrations if the [[point of a topos|topos has enough points]])

The identity functor on the category $SPSh(C)$ of [[simplicial presheaves]] is a [[Quillen adjunction]] for the projective and injective [[global model structure on simplicial presheaves|global model structure]] and this is a [[Quillen equivalence]].

The [[local model structure on simplicial sheaves|local model structures on simplicial sheaves]] are just the restrictions of [[local model structure on simplicial presheaves|those on simplicial presheaves]]. 

These are related by a [[Quillen adjunction]] given by the usual [[geometric embedding]] of the [[category of sheaves]] as a full [[subcategory]] of that of presheaves -- with [[sheafification]] the [[left adjoint]] -- and this is also  [[Quillen equivalence]].

The characteristic of the _left_ Bousfield localizations is that for them the fibrant objects are those that satisfy
[[descent]]: see [[descent for simplicial presheaves]].

In either case 

* the global model structures [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-presheaves]]

while

* the local model structures [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-sheaves]] (i.e. [[∞-stacks]]).


The following diagram collection [[model category|model categories]] that are [[presentable (infinity,1)-category|presentations]] for the [[(∞,1)-category of (∞,1)-sheaves]]. All indicated morphism pairs are [[Quillen equivalences]].

<div style="overflow:auto" markdown="1">
$$
  \array{
     PSh(X, SGrpd)
     &amp;\stackrel{\stackrel{embedding}{\leftarrow}}
       {\stackrel{sheafification}{\to}}&amp;
     Sh(X,SGrpd)
     &amp;\stackrel{}{\leftrightarrow}&amp;
     Sh(X, SSet)^{l loc}_{inj}
     &amp;\stackrel{\stackrel{sheafification}{\leftarrow}}
        {\stackrel{embedding}{\to}}&amp;
     PSh(X, SSet)^{l loc}_{inj}
     &amp;\stackrel{\stackrel{Id}{\leftarrow}}
        {\stackrel{Id}{\to}}&amp;
     PSh(X, SSet)^{l loc}_{proj}
     &amp;\stackrel{\stackrel{embedding}{\leftarrow}}
       {\stackrel{sheafification}{\to}}&amp;
     Sh(X, SSet)^{l loc}_{proj}
     \\
     \\
     Luo-Bubenik-Tim
     &amp;&amp;
     Joyal-Tierney
     &amp;&amp;
     Joyal
     &amp;&amp;
     Jardine
     &amp;&amp;
     Blander
     &amp;&amp;
     Brown-Gersten     
  }
$$
</div>

On the right this lists the model structures on simplicial (pre)sheaves, here displayed as (pre)sheaves with values in [[simplicial sets]], using $SPSh(C) \simeq PSh(C,SSet)$.

On the left we have the Joyal--Tierney and Luo--Bubenik--Tim [[model structures on presheaves of simplicial groupoids]].

(...have to check here the relation $Sh(X,SGrpd)\leftrightarrow PSh(X, SGrpd)$)

### Reedy and intermediate model structures

To some extent the injective and projective model structures on simplicial presheaves are the two extremes of a larger family of model structures on simplicial presheaves that all have the same weak equivalences but different classes of cofibrations.

Notably if the domain $C$ has the special property that it is a [[Reedy category]] there is the  [[Reedy model structure]] on $[C, sSet]$. Its class of cofibrations is intermediate that of the projective and the injective [[model structure on functors]] and we have [[Quillen equivalence]]s

$$
  [C,sSet]_{proj} \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [C,sSet]_{Reedy}
  \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [C,sSet]_{inj}
  \,.
$$

For general $C$, there is still a whole family of model structures on $[C^{op}, sSet]$ that interpolates between the injective and the projective model structure. This is discussed in

* [[Rick Jardine]], _Intermediate model structures for simplicial presheaves_ , Canad. Math. Bull. 49(3) (2006), 407&#8211;413.

  a review in on [p. 12](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=12) of [Field Lectures: Simplicial presheaves](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf)


### Dependency on the underlying site {#DependencyOnSite}


+-- {: .num_prop #SiteDependence}
###### Proposition

Let $C,D$ be [[site]]s and let $f : C \to D$ be a [[functor]] that induces a 
morphism of [[site]]s in that $f_* : PSh(D) \to PSh(C)$ preserves [[sheaf|sheaves]]
and its [[left adjoint]] $f^* : PSh(C) \to PSh(D)$ (given by left [[Kan extension]])
is left [[exact functor]] in that it preserves [[finite limit]]s.

Then the induced [[adjunction]]
$$
  f_* : SPSh(D)_{inj}^{loc} \stackrel{\leftarrow}{\to} SPSh(C)_{inj}^{loc} : f^*
$$
is a [[Quillen adjunction]] for the local injective model structure on presheaves
on both sides.

=--

+-- {: .proof}
###### Proof

This is "little fact 5)" on page 10, 11 of ([JardineLectures](#JardineLecture)).

=--


+-- {: .num_prop}
###### Proposition


Let $C$ be a [[site]] and $f : D \hookrightarrow$ a [[full subcategory|full]] [[dense sub-site]]. Then right [[Kan extension]] $f_* : [D^{op}, sSet] \to [C^{op}, sSet]$ along $f$ yields a [[simplicial Quillen adjunction]]

$$
  (f^* \dashv f_*) 
   : 
  [D^{op}, sSet]_{inj,loc} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} 
  [C^{op}, sSet]_{inj,loc}
$$

between the [[Bousfield localization of model categories|left Bousfield localizations]] of the projective model structures at the [[sieve]] inclusions $S(\{U_i\}) \to U$ for each [[covering]] family $\{U_i \to U\}$.

=--

+-- {: .proof}
###### Proof

It is immediate that we have a simplicial Quillen adjunction on the global injective model structure: by definition of right [[Kan extension]] we have an [[sSet]]-[[adjunction]] and the [[left adjoint]] restriction functor $f^*$ trivially preserves injective cofibrations and acyclic cofibrations.

Since we have [[left proper model categories]] it is  sufficient (by the discussion at <a href="http://nlab.mathforge.org/nlab/show/simplicial%20Quillen%20adjunction#Recognition">recognition of simplicial Quillen adjunctions</a>) for deducing that the Quillen adjunction descends to the local strucuture to check that $f_*$ preserves locally fibrant objects, which in turn by properties of [[Bousfield localization of model categories|left Bousfield localization]] is equivalent to checking that $f^*$ sends covering sieve inclusions to weak equivalences in $[D^{op}, sSet]_{proj,loc}$.

By the [result on generalized covers](#GeneralizedCover), for this it is sufficient to check that for every covering sieve $S(\{U_i\}) \to X$ and every representable $K \in D$ and morphism $K \to f^* X$, there is a [[covering]] $\{K_j \to K\}$ in $D$ and local lifts

$$
  \array{
    K_j &\to& f^*(S(\{U_i\}))
    \\
    \downarrow && \downarrow
    \\
    K &\to& f^* X
  }
  \,.
$$

This follows directly from the single defining condition on a [[coverage]] on $C$.

=--

## Presentation of $(\infty,1)$-toposes {#PresentationOfInfiniToposes}


+-- {: .num_def}
###### Definition

Let $C$ be a [[site]].
Let $[C^{op}, sSet]_{proj}$ be the projective [[model structure on simplicial presheaves]] over $C$. 

Let $W = \{C(\{U_i\}) \to U\}$ be the set of [[Cech nerve]] projections in $[C, sSet]$ for each [[covering]] $\{U_i \to U\}$ in $C$.

Write

$$
  (Id \dashv Id)
  : 
  [C^{op}, sSet]_{proj,loc}
  \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [C^{op}, sSet]_{proj}
$$

for the [[Bousfield localization of model categories|left Bousfield localization]] at $W$.

Write $([C^{op}, sSet]_{proj})^\circ$ for the full sub-[[simplicially enriched category]] on the fibrant-cofibrant objects, similarly for
$([CartSp^{op}, sSet]_{proj,loc})^\circ$.

=--

+-- {: .num_prop #PresentationOfTheInfinTopos}
###### Proposition

We have an [[equivalence of (∞,1)-categories]]

$$
  \array{
    Sh_{(\infty,1)}(C)
    &\stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}& 
    PSh_{(\infty,1)}(C)
    \\
    \uparrow^{\mathrlap{\simeq}} &&
    \uparrow^{\mathrlap{\simeq}}
    \\
    ([C^{op}, sSet]_{proj,loc})^\circ
    &
    \stackrel
       { \overset{\mathbb{L} Id}{\leftarrow} }
       { \underset{\mathbb{R}Id}{\to} }
    &
    ([C^{op}, sSet]_{proj})^\circ
  }
  \,,
$$

where at the bottom we have the left and right [[derived functor]]s of the identity functors, as discussed at [[simplicial Quillen adjunction]].

=--

+-- {: .proof}
###### Proof

This follows using the arguments in the proof of [[Higher Topos Theory|HTT, 6.5.2.14]] and [[Higher Topos Theory|HTT, prop. A.3.7.6]].

=--


## Fibrant and cofibrant objects {#FibAndCofibObjects}


### Fibrant objects

The fibrant objects in the [[local model structure on simplicial presheaves]] are those that 

* are fibrant with respect to the respective [[global model structure on simplicial presheaves|global model structure]]

* and satisfy [[descent for simplicial presheaves]]. See there for more details.

This descent condition is the analog in this model of the [[sheaf]]-condition and the [[stack]]-condition. In fact, it reduces to these for truncated simplicial presheaves.

Since the fibrancy condition in the global projective model structure is simple -- it just requires that the [[simplicial presheaf]] is in fact a presheaf of [[Kan complex]]es -- the local projective model structure has slightly more immediate characterization of fibrant objects than the local injective model structures. (In fact, for suitable choices of [[site]]s it may become very simple, as the above discussion of site dependence of the model structure shows).

On the other hand the cofibrancy condition on objects is entirely _trivial_ in the global and local injective model structure: since a cofibration there is just an objectwise cofibration, and since every [[simplicial set]] is cofibrant, every object is injective cofibrant.

But the cofibrant objects in the projective structure are not too nasty either: every object that is degreewise a coproduct of representables is cofibrant. In particular the [[?ech nerve]]s of any _[[good cover]]_ (see below for more details) is a projectively cofibrant object.

A **cofibrant replacement** functor in the local projective structure  is discussed in 

* [[Daniel Dugger]], _Universal homotopy theories_  ([pdf](http://hopf.math.purdue.edu/Dugger/dduniv.pdf))


Something related to a **fibrant replacement** functor ("$\infty$-stackification") is discussed in section 6.5.3 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]


### Cofibrant objects {#CofibrantObjects}

In the injective [[local model structure on simplicial presheaves]] all objects are cofibrant. For the projective local structure we have the following useful statement (see also _[[projectively cofibrant diagram]]_).


+-- {: .num_defn }
###### Definition

A simplicial presheaf $X \in sPSh(C)$ is said to have **free degeneracies** or the **degenerate cells split off** if in each degree there is a [[subobject|sub]]-presheaf  $N_k \hookrightarrow X_k$ such that the canonical mophism

$$
  \coprod_{\underset{surj.}{\sigma : [k] \to [n]}} 
  N_n \stackrel{\coprod_{\underset{surj.}{\sigma : [k] \to [n]}} \sigma^*}{\to} 
  F_k
$$ 

is an [[isomorphism]].

=--

So if degenerate cells split off we have in particular that 

$$
  X_k = X_k^{nd} \coprod X_k^{dg}
  \,,
$$

where $X_k^{nd}$ is the presheaf of non-degenerate $k$-cells and $X_k^{dg}$ is a separate presheaf containing all the degenerate cells (and itself a coproduct over separate presheaves for each degree and order of degeneracy).


+-- {: .num_prop }
###### Proposition

In the _projective_ [[local model structure on simplicial presheaves|local model structure]] all objects that are 

1. degreewise [[coproduct]]s of [[representable functor|representable]]s 

1. and whose degenerate cells split off

are cofibrant.

=--

This is in the proof of lemma 2.7 in section 9 of

* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_  


+-- {: .num_example }
###### Example
**(split hypercovers)**

If $Y \to X$ is an acyclic fibration in the local projective model structure with $X$ a representable and $Y$ cofibration in the above way, it is called a **[[split hypercover]]** .

All [[?ech nerve]]s $C(\{U_i\})$ coming from an [[open cover]] have split degeneracies. The condition that the Cech nerve be degreewise a coproduct of representables is a condition akin to that of [[good open cover]]s (which is precisely the special case for $C = $ [[CartSp]]). This is then a split hypercover of _height_ 0.

=--


+-- {: .num_defn }
###### Definition
**(good cover)**

A [[?ech nerve]] $U$  with a weak equivalence $U \stackrel{\simeq}{\to} X$ in $SPSh(C)^{loc}$ is a **[[good cover]]** if it is degreewise a coproduct of [[representable functor|representable]]s.

=--

+-- {: .num_remark }
###### Remark

This reduces to the ordinary notion of [[good cover]] as an open cover by contractible spaces such that all finite intersections of these are again contractibe when using a [[site]] like $C = $ [[CartSp]].

=--






### Cofibrant replacement {#CofibrantReplacement}

In 

* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_  

a useful cofibrant replacement functor for the projective local model structure is discussed.

+-- {: .num_defn }
###### Definition

For $A  \in PSh(C) \hookrightarrow SPSh(C)$ an ordinary presheaf (simplicially discrete simplicial presheaf) let $\tilde Q A$ be the simplicial presheaf which in degree $k$ is

$$
  (\tilde Q A)_k := \coprod_{U_k \to U_{k-1} \to \cdots \to U_0 \to A} U_k
  \,,
$$ 

where the $U_k$ range over the representables, i.e. the objects in $C \hookrightarrow SPSh(C)$. The face and degeneracy maps are the obvious ones coming from composing maps and inserting identity maps in the labels over which the coproduct ranges.

For $A \in SPSh(C)$ an arbitrary simplicial presheaf let $Q A$ be the diagonal of  the bisimplicial presheaf obtained by applying $\tilde Q$ degreewise

$$
  Q A =
  \left(
    \cdots
    \coprod_{U_1 \to U_0 \to A_1}
     U_1
    \stackrel{\to}{\to}\coprod_{U_0 \to A_0} U_0
  \right)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

For all $A \in SPSh(C)$ the object $Q A$ is cofibrant and is weakly equivalent to $A$ in $SPSh(C)_{proj}^{loc}$. 

=--

This is in prop 2.8 of

* [[Daniel Dugger]], _[[Universal Homotopy Theories]]_  


## Local fibrations

A _local fibration_ or _local weak equivalence_ of simplicial (pre)sheaves is defined to be one whose lifting property is satisfied after refining to some cover.

**Warning**. Notice that this is a priori unrelated to equivalences and fibrations with respect to any local model structure. 

If the [[site]] $C$ has [[point of a topos|enough points]], then local fibrations of simplicial presheaves are equivalently those that are  [[stalk]]wise fibrations of simplicial sets.

This is discussed in ([Jardine 96](#Jardine96)).

## Localization and descent {#Descent}

### Cech localization at Grothendieck (pre)topologies {#CechLocalization}

We discuss some aspects of the [[Bousfield localization of model categories|left Bousfield localization]] of the projective global model structure on simplicial presheaves at [[Grothendieck topologies]] and [[covering]] families. By the discussion at [[topological localization]] these are models for [[topological localization]]s leading to [[(∞,1)-categories of (∞,1)-sheaves]].

The central reference is ([DuggerHollanderIsaksen](#DuggerHollanderIsaksen)) with the central theorem being this one:

+-- {: .num_theorem}
###### Theorem

Let $C$ be a [[site]] given by a [[Grothendieck topology]]. The left [[Bousfield localization of model categories|Bousfield localization]] of $sPSh(C)_{proj}$ and $sPSh(C)_{inj}$, respectively, at the following classes of morphisms exist and coincide:

1. the set of all [[covering]] [[sieve]] [[subfunctor]]s $R \hookrightarrow j(X)$;

1. the set of all morphisms $hocolim_R \to U \to X$ for $R$ a covering sieve of $X$;

1. the set of all [[Cech nerve]] projections $C(\{U_i\}) \to X$ for $\{U_i \to X\}$ a covering sieve;

1. the class of all bounded [[hypercover]]s $U \to X$;

1. the class of morphisms $F \to \bar F$ from a [[simplicial presheaf]] $F$ to the simplicial [[sheaf]] obtained by degreewise [[sheafification]].

1. if the topology is generated from a [[basis for a topology|basis]], then: the set of covering sieve subfunctors $R_U \to X$ for each covering family $\{U_i \to X\}$ in the basis.

=--

This is theorem A5 in [DugHolIsak](http://front.math.ucdavis.edu/0205.5027).

This localization $sPSh(C)_{proj,cov}$ is the **Cech localization** of $sPSh(C)$ with respect to the given [[Grothendieck topology]]. It is a presentation of [[topological localization]] of an [[(∞,1)-category of (∞,1)-presheaves]] to an [[(∞,1)-category of (∞,1)-sheaves]].

$$
  \array{
    Sh_{(\infty,1)}(C) &\stackrel{\overset{L}{\to}}{\hookrightarrow}&
    Psh_{(\infty,1)}(C)
    \\
    \uparrow^{\mathrlap{\simeq}}
    &&
    \uparrow^{\mathrlap{\simeq}}
    \\
    (sPSh(C)_{proj,cov})^\circ
    &\stackrel{\overset{left. Bousf.}{\leftarrow}}{\underset{}{\to}}&
    (sPSh(C)_{proj})^\circ
  }
  \,.
$$

The following definition and proposition provides information on what the general morphisms are which become weak equivalences after localization at 

+-- {: .num_def #GeneralizedCover}
###### Defintion

Let $C$ be a [[site]]. A **[[local epimorphism]]** (or **generalized cover**) in $sPSh(C)$ is a morphism $f : E \to B$ of simplicial presheaves with the property that for every [[nab:representable functor|representable]] $U$ and every morphism $j(U) \to B$ there exists a [[covering]] [[sieve]] $\{U_i \to U\}$ such that for every $U_i \to U$ the composite $U_i \to U \to B$ has a lift $\sigma$ through $f$ 

$$
  \array{
    j(U_i) &\stackrel{\exists \sigma}{\to}& F
    \\
    \downarrow && \downarrow
    \\
    j(U) &\stackrel{\forall}{\to} & B
  }
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $f : E \to B$ a [[local epimorphism]] in $sPSh(C)$ in the above sense, its [[Cech nerve]] projection

$$
  C(E) \to B
$$

is a weak equivalence in $sPSh(C)_{prof, cov}$.

=--

This is [DugHolIsa, corollary A.3](http://front.math.ucdavis.edu/0205.5027).


### Cech localization at a coverage {#LocalizationAtCoverage}


In the literature localization of categories of simplicial presheaves is typically discussed with respect to a [[Grothendieck topology]] or a [[basis for a topology]]. Here we discuss aspects of localization at a  [[coverage]].


Let $C$ be a category equipped with a [[coverage]], i.e. a collection of families of morphisms $\{U_i \to U\}$ for each object $U$ in $C$, called _covering families_ such that for any morphism $f : V \to U$ there exist diagrams

$$
  \array{
    V_j &\to& U_{i(j)}
    \\
    \downarrow && \downarrow
    \\
    V &\stackrel{f}{\to}& U
  }
$$ 

such that $\{V_i \to V\}$ is itself a covering family.

Write $S(\{U_i\}) \to j(U)$ for the [[sieve]] corresponding to a covering family, regarded as a [[subfunctor]] of the [[representable functor]] $j(U)$, which we both regard as simplicially discrete objects in $sPSh(C)$.

Write $sPSh(C)_{inj,cov}$ for the left [[Bousfield localization of model categories|Bousfield localization]] of $sPSh(C)_{inj}$ at these morphisms $S(\{U_i\}) \to j(U)$ corresponding to covering families.

+-- {: .num_prop}
###### Proposition

A subfunctor inclusion $\tilde S \hookrightarrow j(U)$ corresponding to a sieve that _contains_ a covering sieve $S(\{U_i\})$ is a weak equivalence in $sPSh(C)_{inj,cov}$
 
=--

+-- {: .proof}
###### Proof

Write $J$ for the set of morphisms in $\tilde S$ but not in $S$.

Let $j(V_j) \to j(U)$ be a morphism not in $S(\{U_i\})$. By assumption we can find a covering family $\{V_{j,k} \to V_j\}$ such that for all $j,i$ we have commuting diagrams 

$$
  \array{
    V_{j,k} &\to& U_{i}
    \\
    \downarrow && \downarrow
    \\
    V_j &\stackrel{f}{\to}& U
  }
  \,.
$$ 

Consider the commuting diagram

$$
  \array{
    \coprod_j S(\{V_{j,k}\}) &\hookrightarrow& S(\{U_i\} \cup \{V_{j,k}\})
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow
    \\
    \coprod_j j(V_j) &\to& S(\{U_i\} \cup \{V_j\})
  }
  \,.
$$

Observe that this is a [[pushout]] in $sPSh(C)$, that the top morphism is a cofibration in $sPSh(C)_{inj}$ and hence in $sPSh(C)_{inj,cov}$, 
that the left morphism is a local weak equivalence, that by general properties of [[Bousfield localization of model categories|left Bousfield localization]] the localization $sPSh(C)_{inj,cov}$ is [[proper model category|left proper]]. Therefore the morphism $S(\{U_i\} \cup \{V_{j,k}\}) \to S(\{U_i\} \cup \{V\}) = \tilde S$ is a weak equivalence.

Next observe that from the horizontal morphisms of the above commuting diagrams that defined the covers $\{V_{j,k} \to V_j\}$ we have an induced morphism $S(\{U_i\} \cup \{V_{j,k}\}) \to S(\{U_i\})$, and this exhibits $S(\{U_i\})$ as a [[retract]]

$$
  \array{
    S(\{U_i\}) &\to& S(\{U_i\} \cup \{V_{j,k}\}) &\to& S(\{U_i\})
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \tilde S &=& \tilde S &=& \tilde S 
  }
  \,.
$$

By closure of weak equivalences under retracts, this shows that the inclusion $S(\{U_i\}) \to \tilde S$ is a weak equivalence.  By 2-out-of-3 this finally means that $\tilde S \hookrightarrow j(U)$ is a weak equivalence.

=--

+-- {: .num_cor}
###### Corollary

For $S(\{U_i\}) \to j(U)$ a covering sieve, its [[pullback]] $f^*S(\{U_i\}) \to j(V)$ in $sPSh(C)$ along any morphism $j(f) : j(V) \to j(U)$ 

$$
  \array{
    f^* S(\{U_i\}) &\to& S(\{U_i\})
    \\
    \downarrow && \downarrow
    \\
    j(V) &\stackrel{j(f)}{\to}& j(U)
  }
$$

is also a weak equivalence.
 
=--

+-- {: .num_lemma}
###### Lemma

If $S(\{U_i\}) \to j(U)$ is the sieve of a covering family and $\tilde S \hookrightarrow j(U)$ is any sieve such that for every $f_i : U_i \to U$ the pullback $f_i^* \tilde S$ is a weak equivalence, then $\tilde S \to j(U)$ becomes an [[isomorphism]] in the [[homotopy category]].

=--


+-- {: .proof}
###### Proof


First notice that if $f_i^* \tilde S$ is a weak equivalence for all $i$, then the pullback of $\tilde S$ to any element of the sieve $S(\{U_i\})$ is a weak equivalence. 
Use the [[co-Yoneda lemma]] to write 

$$
  S(\{U_i\}) = \lim_{\underset{V \to U_i \to U}{\to}} j(V)
  \,.
$$

Now consider these objects in the [[(∞,1)-category of (∞,1)-presheaves]] that is presented by $sPSh(C)_{inj}$.

Since that has [[universal colimits]] we have the pullback square

$$
  \array{
    i^* \lim_\to j(V)
    &\simeq& \lim_{\to} f_V^* \tilde S
    &\to& \tilde S
    \\
    && \downarrow && \downarrow^{\mathrlap{i}}
    \\
    S(\{U_i\}) &=& 
    \lim_{\underset{f_V : V \to U_i \to U}{\to}} j(V)
    &\stackrel{(f_V)}{\to}&
    j(U)
  }
$$

and the left vertical morphism is a colimit over morphisms that are weak equivalences in $sPSh(C)_{inj,loc}$. By the general properties of [[reflective sub-(∞,1)-categories]] this means that the total left vertical morphism becomes an isomorphism in the homotopy category of $sPSh(C)_{inj,cov}$. Also the bottom morphism is an isomorphism there, and hence the right vertical one is.


=--


+-- {: .num_lemma}
###### Conclusion

In total this shows that the localization at the [[coverage]] produces the [[topological localization]] at the [[Grothendieck topology]] generated by that coverage.


=--


### For values in strict and abelian $\infty$-groupoids   
  {#DescentForStrictInf}



Many simplicial presheaves appearing in practice are (equivalent) to objects in [[sub-(∞,1)-categories]] of $Sh_{(\infty,1)}(C)$ of abelian or at least [[strict ∞-groupoid]]s. These subcategories typically offer convenient and desireable contexts for formulating and proving statements about special cases of general simplicial presheaves.  

One well-known such notion is given by the [[Dold-Kan correspondence]]. This identifies [[chain complex]]es of [[abelian group]]s with strict and strictly [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] $\infty$-groupoids.

Dropping the condition on symmetric monoidalness we obtain a more general such inclusion, a kind of non-abelian Dold-Kan correspondence: 

the identification of [[crossed complex]]es of groupoids as precisely the [[strict omega-groupoid|strict ∞-groupoid]]s. This has been studied in particular in [[nonabelian algebraic topology]].

So we have a sequence of inclusions

$$
  \array{
     ChainCplx &\hookrightarrow& CrsCpl &\hookrightarrow& KanCplx
     \\
     \downarrow^{\mathrlap{simeq}} && \downarrow^{\mathrlap{simeq}} && \downarrow^{\mathrlap{simeq}}
     \\
     StrAb Str\infty Grpd &\hookrightarrow&
     Str \infty Grpd
     &\hookrightarrow&
     \infty Grpd 
  }
$$

of strict $\infty$-groupoids into all $\infty$-groupoids. See also the [[cosmic cube]] of [[higher category theory]]. 

Among the special tools for handling $\infty$-stacks on $C$ that factor at some point through the above inclusion are the following:

* **restriction to abelian sheaf cohomology** -- Using the fact that the objects of $Sh_{(\infty,1)}(C)$ are modeled by [[simplicial presheaves]] symmetric monoidal $\infty$-Lie groupoids are identified under the [[Dold-Kan correspondence]] with $\mathbb{N}$-graded [[chain complex|chain complexes]] of sheaves. To these the rich set of tools for [[abelian sheaf cohomology]] apply. 

* **descent for strict $\infty$-groupoid valued sheaves** -- There is a good theory of [[descent]] for (presheaves) with values in strict $\infty$-groupoids (more restrictive than the fully general theory but more general than [[abelian sheaf cohomology]]). This goes back to [[Ross Street]] and its relation to the full theory has been clarified by [[Dominic Verity]] in [Verity09](#Verity).


We state a useful theorem for the computation of [[descent]] for presheaves with values in [[strict ∞-groupoid]]s. Recall the standard terminology for [[descent]], i.e. for the $(\infty,1)$-categorical [[sheaf]]-condition:

For $U \in C$ a representable, $Y,A \in [C^{op}, sSet]$ simplicial presheaves and $p : Y \to U$ a morphism, we say that $A$ _satisfies [[descent]]_ along $p$ or equivalently that $A$ is a $p$-[[local object]] if the canonical morphism

$$
  A(U) \stackrel{=}{\to}
  [C^{op}, sSet](U,A) 
  \to 
  [C^{op}, sSet](Y,A)
$$

is a weak equivalence. Here the first equality is the enriched [[Yoneda lemma]]. By the [[co-Yoneda lemma]] we may decompose $Y$ into its cells as

$$
  Y = \int^{[n] \in \Delta} \Delta[n] \cdot Y_n
  \,,
$$

where in the integrand we have the [[copower|tensoring]] of $[C^{op}, sSet]$ over [[sSet]]. Using that the enriched [[hom-functor]] sends coends to ends, the enriched [[hom-functor]] on the right we may equivalently write out as an [[end]]

$$
  \begin{aligned}
    [C^{op}, sSet](Y,A) 
    & =
    [C^{op}, sSet](\int^{[n] \in \Delta} \Delta[n] \cdot Y_n ,A)
    \\
    & = 
    \int_{[n] \in \Delta}[C^{op}, sSet](\Delta[n] \cdot Y_n ,A)
    \\
    & =
    \int_{[n] \in \Delta} sSet(\Delta[n], [C^{op}, sSet](Y_n, A))
    \\
    & =
    \int_{[n] \in \Delta} sSet(\Delta[n], A(Y_n))
    \\
    & =:Desc(Y,A)
  \end{aligned}  
$$

(equality signs denote [[isomorphism]]s), where in the second but last line we again used the [[copower|tensoring]] of [[simplicial presheaves]] $[C^{op}, sSet]$ over [[sSet]].

In the last line we have the _[[totalization]]_ of the cosimplicial [[simplicial object]]

$$
  A(Y_\bullet) : \Delta \to sSet
  \,,
$$

sometimes called the _descent object_ of $A$ relative to $Y$, even though in this case it is really nothing but the hom-object of $Y$ into $A$. If $A$ is fibrant and $Y$ cofibrant, then $Desc(Y,A)$ is  a Kan complex: the _descent $\infty$-groupoid_ .

Now suppose that $\mathcal{A} : C^{op} \to Str \infty Grpd$ is a presheaf with values in [[strict ∞-groupoid]]s. In the context of strict $\infty$-groupoids the standard $n$-[[simplex]] is given by the $n$th [[oriental]] $O(n)$. This allows to perform a construction that looks like a descent object in $Str\infty Grpd$:

+-- {: .num_defn }
###### Definition
**(Ross Street)**

The descent object for $\mathcal{A} \in [C^{op}, Str \infty Grpd]$ relative to $Y \in [C^{op}, sSet]$ is

$$
  Desc(Y,\mathcal{A}) := \int_{[n] \in \Delta} Str\infty Cat(O(n), \mathcal{A}(Y_n))
  \;\in Str \infty Grpd
  \,,
$$

where the [[end]] is taken in $Str \infty Grpd$. 

=--

This objects had been suggested by [[Ross Street]] to be the right descent object for strict $\infty$-category-valued presheaves in [Street03](#Street03) 

Under the [[∞-nerve]] functor $N_O : Str\infty Grpd \to sSet$ this yields a [[Kan complex]] $N_0 Desc(Y,\mathcal{A})$. On the other hand, applying the $\omega$-nerve directly to $\mathcal{A}$ yields a simplicial presheaf $N_O\mathcal{A}$ to which the above simplicial descent applies. 

The following theorem asserts that under certain conditions both notions coincide.

+-- {: .num_theorem }
###### Theorem
**(Dominic Verity)**

If $\mathcal{A} : C^{op}, Str \infty Grpd$ and $Y : C^{op} \to sSet$ are such that $N_O \mathcal{A}(Y_\bullet) : \Delta \to sSet$ is fibrant in the [[Reedy model structure]] $[\Delta, sSet_{Quillen}]_{Reedy}$, then 

$$ 
  N_O Desc(Y,\mathcal{A}) \stackrel{\simeq}{\to} Desc(Y, N_O \mathcal{A})
$$

is a [[weak homotopy equivalence]] of [[Kan complex]]es.

=--

This is proven in [Verity09](#Verity).


+-- {: .num_corollary }
###### Corollary

If $Y \in [C^{op}, sSet]$ is such that $Y_\bullet : \Delta \to [C^{op}, Set] \hookrightarrow [C^{op}, sSet]$ is cofibrant in $[\Delta, [C^{op}, sSet]_{proj}]_{Reedy}$ then for $\mathcal{A} : C^{op} \to Str \infty Grpd$ we have

$$ 
  N_O Desc(Y,\mathcal{A}) \stackrel{\simeq}{\to} Desc(Y, N_O \mathcal{A})
  \,.
$$

=--

+-- {: .proof}
###### Proof

If $Y_\bullet$ is Reedy cofibrant, then by definition the canonical morphisms

$$
  \lim_{\to}( ([n] \stackrel{+}{\to} [k]) \mapsto Y_k ) \to Y_n
$$

are cofibrations in $[C^{op}, sSet]_{proj}$. Since the latter is an $sSet_{Quillen}$ [[enriched model category]] and $N_O \mathcal{A}$ is fibrant, it follows that the [[hom-functor]] $[C^{op}, sSet](-, N_O \mathcal{A})$ sends cofibrations to fibrations, so that

$$
  N_O\mathcal{A}(Y_n)
  \to
  \lim_{\leftarrow}( [n]\stackrel{+}{\to} [k] \mapsto N_O\mathcal{A}(Y_k))
$$ 

is a [[Kan fibration]]. But this says that $N_O \mathcal{A}(Y_\bullet)$ is Reedy fibrant, so that the assumption  of Verity's theorem is met.

=--

+-- {: .num_corollary }
###### Corollary

For $Y$ the [[Cech nerve]] of a [[good open cover]] $\{U_i \to X\}$ of a [[manifold]] $X$ and any $\mathcal{A} : CartSp^{op} \to Str \infty Grpd$ we have that

$$
  [C^{op}, sSet](Y,N_O \mathcal{A})
  \simeq
  N_O Desc(Y_\bullet, \mathcal{A})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the above is sufices to note that $Y_\bullet$ is cofibrant in $[\Delta^{op}, [C^{op}, sSet]_{proj}]_{Reedy}$ if $Y$ is the [[Cech nerve]] of a good open cover. By the assumption of good open cover we have that $Y$ is degreewise a coproduct of representables and that the inclusion of all degenerate $n$-cells into all $n$-cells is a full inclusion into a coproduct, i.e. an inlusion of the form

$$
  \coprod_{i \in I} U_i \to \coprod_j U_{j \in J}
$$

induced from an inclusion of subsets $I \hookrightarrow J$. Since all representables are cofibrant in $[C^{op}, sSet]_{proj}$ such an inclusion is a cofibration.

=--

In conclusion we find that for determining the $\infty$-stack condition for _strict_ $\infty$-Lie groupoids we may equivalently use Street's formula for strict $\infty$-groupid valued presheaves. This is sometimes useful for computations in low categorical degree. 





## Properness
 {#Properness}

The global model structures on simplicial presheaves are
all [[left proper model categories|left]] and [[right proper model categories]].
Since left [[Bousfield localization of model categories]] preserves
left properness (as discussed there), the local model structures are
also left proper. 

But the local model structures are not in general right proper anymore.

+-- {: .num_prop }
###### Proposition

A sufficient condition for an injective or projective local model structure
of simplicial presheaves over a [[site]] $C$ to be right proper is that
the weak equivalences are precisely the [[stalk]] wise weak equivalences of
simplicial sets.

=--

This is true for instance for the injective Jardine model structure when $C$ has [[point of a topos|enough points]].

+-- {: .proof}
###### Proof

The key is that forming [[stalks]] is, being the [[inverse image]] of a [[point of a topos|geometric morphism]]

$$
  (x^* \dashv x_*)  :=
  Set
  \stackrel{\overset{x^*}{\leftarrow}}{\underset{x_*}{\to}}
  Sh(C)
$$

an operation that preserves [[finite limits]]. 

Let therefore $f : X \to A$ be a stalkwise weak equivalence of simplicial presheaves and let $g : A \to B$ be a fibration. Notice that in all the model structures (injective, projective, global, local) the fibrations are always _in particular_ objectwise fibrations.

Then the pullback $g^* f$ in

$$
  \array{
    g^* X &\to& X
    \\
    \downarrow^{\mathrlap{g^* f}} && \downarrow^{\mathrlap{f}} 
    \\
    A &\stackrel{g}{\to}& B
  }
$$

is a weak equivalence if for all topos points $x$ the stalk $x^* (g^* f)$ is a weak equivalence of simplicial sets. But since stalks preserve finite limits, we have a pullback diagram of simplicial sets

$$
  \array{
    x^*(g^* X) &\to& x^*( X)
    \\
    \downarrow^{\mathrlap{x^*(g^* f)}} && \downarrow^{\mathrlap{x^*(f)}} 
    \\
    x^*(A) &\stackrel{x^*(g)}{\to}& x^*(B)
  }
  \,.
$$

It is now sufficient to observe that $x^* g$ is a [[Kan fibration]],
this implies the result then by the fact that the standard
[[model structure on simplicial sets]] is right proper. 

To see this, notice that  $x^*(g)$ is a Kan fibration precisely if for all $1 \leq k $ and $0 \leq i \leq k$ the morphism

$$
  (x^* A)^{\Delta[k]}
  \to
  (x^* A)^{\Lambda[k]^i} \times_{(x^* B)^{\Lambda[k]^i} } (x^* B)^{\Delta[k]}
$$

is an [[epimorphism]] of sets. Since stalks commute with finite limits, this is equivalent to 

$$
  x^* 
  \left(
  A^{\Delta[k]}
   \to
  A^{\Lambda[k]^i} \times_{ B^{\Lambda[k]^i}   }  B^{\Delta[k]}  
  \right)
$$

being an epimorphism. Now the morphism in parenthesis is an epimorphism since the fibration $f$ is in particular an objectwise Kan fibration, and [[left adjoint]] functors such as $x^*$ preserve epimorphisms.

=--

This is mentioned for instance in ([Olsson, remark 4.3](#Olsson)).


## Closed monoidal structure {#MonoidalStructure}

If the underlying site has finite [[product]]s, then both the injective and the projective, the global and the local model structure on simplicial presheaves becomes a [[monoidal model category]] with respect to the standard [[closed monoidal structure on presheaves]].

See for instance [here](http://www.math.univ-toulouse.fr/~toen/crm-2008.pdf#page=24).

+-- {: .num_lemma}
###### Lemma

Let $C$ be a category with [[products]]. Then the [[closed monoidal structure on presheaves]] makes $[C^{op}, sSet]_{proj}$ a [[monoidal model category]].

=--


+-- {: .proof}
###### Proof

It is sufficient to check that the Cartesian product of presheaves

$$
  \otimes : sPSh(C)_{proj} \times sPSh(C)_{proj} \to sPSh(C)_{proj}
$$

is a left [[Quillen bifunctor]]. As discussed at [[Quillen bifunctor]], since $sPSh(C)$ is a [[cofibrantly generated model category]] for that it is sufficient to check that $\otimes$ satisfies the pushout-prodct axiom on generating (acyclic) cofibrations. 

As discussed at [[model structure on functors]], these are those morphisms of the form

$$
  Id \times i : U \cdot S \to U \cdot T
$$

for $U \in C$ representable and $i : S \to T$ an (acylic) cofibration in $sSet_{Quillen}$. For these morphisms checking the pushout-product axiom amounts to checking it in $sSet$, where it is evident. 

=--


+-- {: .num_lemma}
###### Lemma

Let $C$ be a [[site]] with [[product]]s and let $[C^{op}, sSet]_{proj,cov}$ be the left [[Bousfield localization of model categories|Bousfield localization]] at the [[Cech nerve]] projections. 

Then for $X$ any cofibrant object, the [[closed monoidal structure on presheaves]]-adjunction

$$
  (X \times (-) \dashv [X,-]) : [C^{op}, sSet]_{proj,cov}
  \to 
  [C^{op}, sSet]_{proj,cov}
$$

is a [[Quillen adjunction]].

=--

+-- {: .proof}
###### Proof

The above lemma implies that the [[left adjoint]] $X \times (-)$ preserves cofibrations. As discussed in the <a href="http://ncatlab.org/nlab/show/Quillen+adjunction#sSet">section on sSet-enriched adjunctions</a> at [[Quillen adjunction]] since the adjunction is $sSet$-enriched and since $[C^{op}, sSet]_{proj,cov}$ is a [[proper model category|left proper]] [[simplicial model category]] it suffices to check that $[X,-]$ preserves fibrant objects. 

For that let $\{U_i \to U\}$ be a covering family and $C(\{U_i\})$ the corresponding [[Cech nerve]]. We need to check that if $A \in [C^{op}, sSet]_{proj,cov}$ is fibrant, then 

$$
  [C^{op}, sSet](U, [X,A]) \to [C^{op},sSet](C(\{U_i\}), [X,A])
$$

is an equivalence of [[Kan complex]]es.

Writing $C(\{U_i\}) = \int^{[n]} \Delta[n] \cdot \coprod U_{i_0, \cdots, i_n}$ and using that the [[hom-functor]] preserves [[end]]s, this is eqivalent to 

$$
  [C^{op},sSet]( X \times C(\{U_i\}) \to X \times U , A)
$$

being an equivalence. Now we observe that $X \times C(\{U_i\}) \to X\times U$ is a [[local epimorphism]] in the above sense, namely a morphism such that for every morphism $V \to X \times U$ out of a representable, there is a lift $\sigma$

$$
  \array{
     && X \times C(\{U_i\})
     \\
     & {}^{\mathllap{\sigma}}\nearrow & \downarrow
     \\
     V &\to& X \times U
  }
  \,.
$$

By the above discussion of the Cech-localization of $[C^{op}, sSet]_{proj}$, this is a local morphism, hence does produce an equivalence when hommed into the fibrant object $A$.

=--


## Homotopy (co)limits {#HomotopyLimits}

Properties of [[homotopy limit]]s and [[homotopy colimit]]s of simplicial presheaves are discussed at

* [Homotopy (co)limits of simplicial (pre)sheaves](http://ncatlab.org/nlab/show/homotopy+limit#SimpSheaves)

Let $C$ be a [[site]].

+-- {: .num_prop}
###### Proposition

Let $F : D \to [C^{op}, sSet]$ be a [[finite limit|finite]] diagram.

Write $\mathbb{R}_{glob}\lim_{\leftarrow} F \in [C^{op}, sSet]$ for any representative of the [[homotopy limit]] over $F$ computed in the global model structure $[C^{op}, sSet]_{proj}$, well defined up to [[isomorphism]] in the [[homotopy category]]. 

Then $\mathbb{R}_{glob}\lim_{\leftarrow} F \in [C^{op},sSet]$ presents also the [[homotopy limit]] of $F$ computed in the local model structure $[C^{op}, sSet]_{proj,loc}$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[(∞,1)-limit]] the [[homotopy limit]] 
$\mathbb{R}\lim_{\leftarrow}$ computes the corresponding [[(∞,1)-limit]]
and [[(∞,1)-sheafification]] $L $ is a left
[[exact (∞,1)-functor]] and preserves these finite [[(∞,1)-limit]]s:

$$
  \array{
     ([D, [C^{op}, sSet]_{proj, loc}]_{inj})^\circ
     &\stackrel{L_*}{\leftarrow}&
     ([D, [C^{op}, sSet]_{proj}]_{inj})^\circ
     \\
     \downarrow^{\mathrlap{\mathbb{R} \lim_\leftarrow}}
     &&
     \downarrow^{\mathrlap{\mathbb{R} \lim_\leftarrow}}
     \\
     ([C^{op}, sSet]_{proj,loc})^\circ
     &\stackrel{L \simeq \mathbb{L} Id}{\leftarrow}&
     ([C^{op}, sSet]_{proj})^\circ
  }
 \,.
$$

Here $L \simeq \mathbb{L} Id$ is the left [[derived functor]] of the identity for the [above](#PresentationOfTheInfinTopos) left Bousfield localization. Since left Bousfield localization does not change the cofibrations and includes the global weak equivalences into the local weak equivalences, the postcomposition of the diagram $F$ with $\mathbb{L} Id$ is given by cofibrant replacement in the local structure, too. But the [[homotopy limit]] of the diagram is invariant, up to equivalence, under cofibrant replacement, and hence a finite homotopy limit diagram in the global structure is also one in the local structure.

=--


## Inclusion of chain complexes of sheaves {#InclusionOfChainComplexes}

We discuss how [[chain complex]]es of presheaves of [[abelian group]]s
embed into the model structure on simplicial presheaves. Under passing to the intrinsic [[cohomology]] of the [[(∞,1)-topos]]
[presented by](#PresentationOfInfiniToposes) by $[C^{op}, sSet]_{loc}$, this realizes traditional [[abelian sheaf cohomology]] over $C$ and generalizes it to general base objects.

Observe from the discussion at [[model structure on simplicial abelian groups]] that the degreewise [[free functor]]-[[forgetful functor]] [[adjunction]] $(F \dashv U) : Ab \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} Set$ (see [[algebra over a Lawvere theory]] for details) induces a [[Quillen adjunction]]

$$
  (F \dashv U) : 
 sAb_{Quillen } 
   \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} 
  sSet_{Quillen}
$$

between the [[model structure on simplicial abelian groups]] and the 
standard [[model structure on simplicial sets]], which exhibits
$sAb_{Quillen}$ as the corresponding [[transferred model structure]].

Moreover, the [[Dold-Kan correspondence]] constitutes in particular a [[Quillen equivalence]]

$$
  (N_\bullet \dashv \Gamma) 
   : 
  Ch_\bullet^+_{proj} 
   \stackrel{\overset{N_\bullet}{\leftarrow}}{\underset{\Gamma}{\to}} 
  sAb_{Quillen}
$$

between the projective [[model structure on chain complexes]] of [[abelian group]]s in non-negative degree and simplicial abelian groups.

We write

$$
  (N_\bullet F \dashv \Xi) 
  : 
  Ch_\bullet^+_{proj} 
   \stackrel{\overset{N_\bullet}{\leftarrow}}{\underset{\Gamma}{\to}} 
  sAb_{Quillen}
   \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} 
  sSet_{Quillen}  
$$

for the composite [[Quillen adjunction]]. For $C$ any [[category]], postcomposition with $\Xi$ induces a Quillen adjunction 

$$
  (N_\bullet F \dashv \Xi)
  : 
  [C^{op}, Ch_\bullet^+_{proj}]_{proj}
   \stackrel{\overset{N_\bullet F}{\leftarrow}}{\underset{\Xi}{\to}}
  [C^{op}, sSet]_{proj}
$$

between the projective [[model structure on functors]] $[C^{op}, Ch_\bullet^+_{proj}]_{proj}$ and  the global projective model structure on simplicial presheaves, which by convenient abuse of notation we denote by the same symbols.



## Related concepts

* [[local fibration]]

* **model structure on simplicial presheaves**

* [[model structure on simplicial sheaves]]

* [[model structure for (2,1)-sheaves]]

## References

A nice introduction and survey is provided in the notes

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))


Detailed discussion of the injective model structures on simplicial presheaves is in

* [[Rick Jardine]], _Simplicial presheaves_ Journal of Pure and Applied Algebra 47 (1987), 35-87 ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))
{#JardineLecture}

* [[Rick Jardine]], _Stacks and the homotopy theory of simplicial sheaves_, Homology, homotopy and applications, vol. 3 (2), 2001, pp.361--384

* [[Rick Jardine]], _Boolean localization, in practice_ ([web](http://www.math.uni-bielefeld.de/documenta/vol-01/13.html))
  {#Jardine96}

* [[Rick Jardine]], _Local homotopy theory_ (2011) ([pdf](http://www.math.uwo.ca/~jardine/papers/preprints/book.pdf))


The projective model structure is discussed in

* [[Dan Dugger]], _[[Universal Homotopy Theories]]_

See also

* Benjamin Blander, _Local projective model structures on simplicial presheaves_,  K-Theory, Volume 24, Number 3, November 2001 , pp. 283--301(19) ([journal](http://www.ingentaconnect.com/content/klu/kthe/2001/00000024/00000003/00384649?crawler=true))

A brief review in the context of [[nonabelian Hodge theory]] is in section 4 of

* Martin Olsson, _Towards non-abelian $p$-adic Hodge theory in the good reduction case_ ([pdf](http://math.berkeley.edu/~molsson/PHT3-24-08.pdf))
 {#Olsson}


A detailed study of [[descent]] for simplicial presheaves is given in

* [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], 
_Hypercovers and simplicial presheaves_ , Math. Proc. Cambridge
Philos. Soc. 136 (2004), no. 1, 9&#8211;51 ([web](http://www.math.uiuc.edu/K-theory/0563/)) 
{#DuggerHollanderIsaksen}

* [[Daniel Dugger]], [[Daniel Isaksen]], _Weak equivalences of simplicial presheaves_ ([arXiv](http://arxiv.org/abs/math/0205025))

A survey of many of the model structures together with a treatment of the left local projective one is in

* [[Benjamin Blander]], _Local projective model structure on simplicial presheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0462/combination2.pdf))

See also

* [[Daniel Isaksen]], _Flasque model structure for simplicial presheaves_  ([web](http://www.math.uiuc.edu/K-theory/0679/), [pdf](http://www.math.uiuc.edu/K-theory/0679/flasque.pdf))

The characterization of the model category of simplicial presheaves as the canonical [[presentable (infinity,1)-category|presentation]] of the (hypercompletion of) the [[(∞,1)-category of (∞,1)-sheaves]] on a site is in

* [proposition 6.5.2.1](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=528) of 

  * [[Jacob Lurie]], _[[Higher Topos Theory]]_

A set of lecture notes on simplicial presheaves with an eye towrads algebraic sites and [[derived algebraic geometry]] is

* [[Bertrand Toen]], _Simplicial presheaves and derived algebraic geometry_ , lecture at [Simplicial methofs in higher categories](http://www.crm.es/HigherCategories/)  ([pdf](http://www.crm.cat/HigherCategories/hc1.pdf))

Last not least, it is noteworthy that the idea of localizing simplicial sheaves at stalkwise weak equivalences is already described and applied in 

* [[Kenneth Brown]], _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf cohomology]]_ ,

using instead of a full [[model category]] structure the more lightweight one of a Brown [[category of fibrant objects]].

A comparison between Brown-Gersten and Joyal-Jardine approach:

* V. Voevodsky, _Homotopy theory of simplicial presheaves in completely decomposable topologies_, [arxiv/0805.4578](http://arxiv.org/abs/0805.4578)

The proposal for descent objects for strict $\infty$-groupoid-valued presheaves discussed in [Descent for strict infinity-groupoids](#DescentForStrictInf) appeared in 

* [[Ross Street]], _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math/0303175)) {#Street03}

The relation to the general descent condition is discussed in

* [[Dominic Verity]], _[[Verity on descent for strict omega-groupoid valued presheaves|Relating descent notions]]_ {#Verity}


[[!redirects model structures on simplicial presheaves]]