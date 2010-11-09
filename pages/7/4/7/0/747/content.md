
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

Various interrelated flavors of model structures on the category of simplicial presheaves on $C$ have been introduced and studied since the 1970s, originally by K. Brown and [[Andre Joyal]] and then developed in detail by Jardine.

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

* Jardine, _Intermediate model structures for simplicial presheaves_ , Canad. Math. Bull. 49(3) (2006), 407&#8211;413.

  a review in on [p. 12](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=12) of [Field Lectures: Simplicial presheaves](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf)

### Dependence on the underlying site


+-- {: .un_prop }
###### Proposition

Let $C,D$ be [[site]]s and let $f : C \to D$ be a [[functor]] that induces a 
morphism of [[site]]s in that $f_* : PSh(D) \to PSh(C)$ preserves [[sheaf|sheaves]]
and its [[left adjoint]] $f^* : PSh(C) \to PSh(D)$ (given by left [[Kan extension]])
is left [[exact functor]] in that it preserves finite [[limit]]s.

Then the induced [[adjunction]]
$$
  f_* : SPSh(D)_{inj}^{loc} \stackrel{\leftarrow}{\to} SPSh(C)_{inj}^{loc} : f^*
$$
is a [[Quillen adjunction]] for the local injective model structure on presheaves
on both sides.

=--

+-- {: .proof}
###### Proof

This is "little fact 5)" on page 10, 11 of

* Jardine, _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

=--


#### Examples 


+-- {: .un_prop }
###### Proposition


Let $C = $ [[CartSp]], $D = $ [[Diff]] and let $f : CartSp \hookrightarrow Diff$ be
the canonical inclusion of a [[subcategory]]. 

Then there is a [[Quillen equivalence]]

$$
  f_* : SPSh(Diff)_{inj}^{loc} \stackrel{\leftarrow}{\to}
      SPSh(CartSp)_{inj}^{loc} : f^*
  \,.
$$

=--


+-- {: .proof}
###### Proof

>[[Urs Schreiber]]: this is what I came up with, check

The functor

$$
  f_* : PSh(Diff) \to PSh(CartSp)
$$

that simply restricts a sheaf on the category of all [[manifold]]s to those on just [[cartesian space]]s clearly respects the [[sheaf]] condition.

Its [[left adjoint]] is given by the left [[Kan extension]] formula

$$
  f^* A : (X \in Diff) \mapsto \lim_{\to}_{(X \to \mathbb{R}^n)} A(\mathbb{R}^n)
  \,.
$$

Since [[CartSp]] has [[terminal object]] also the [[comma category]] $(X/f)$ has a [[terminal object]] and is hence a [[filtered category]]. Therefore this is a [[filtered colimit]] and therefore commutes with finite [[limit]]s. Since [[limit]]s of [[sheaf|sheaves]] are computed objectwise (see [[limits and colimits by example]]) it follows that $f^*$ preserves finite [[limit]]s.

So $f$ does induce a morphism of [[site]]s and thus satisfies the assumptions of the above theorem, which tells us that

$$
  f_* : SPSh(Diff)_{inj}^{loc} \stackrel{\leftarrow}{\to} SPSh(CartSp)_{inj}^{loc} : f^*
$$

is a [[Quillen adjunction]]. 

But we know more: as discussed in 

* Daniel Dugger, _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

the [[Grothendieck topos]] $Sh(Diff)$ has [[point of a topos|enough topos points]], 

$$
  (p_n)_* : Set \stackrel{\leftarrow}{\to} Sh(Diff) : (p_n)^*
$$

one for each $n \in \mathbb{N}$, which are given by taking [[colimit]]s over the evaluation of simplicial presheaves on the [[poset]] of open $n$-disks $D(r) = \{x \in \mathbb{R}^n | |x| \lt r\}$ centered at the origin of $\mathbb{R}^n$

$$
  (p_n)^* A  = \lim_\to_{r \in \mathbb{R}} A(D(r))
  \,.
$$

Since the open $n$-disk is [[diffeomorphism|diffeomorphic]] to $\mathbb{R}^n$, we may think of these [[stalk]]s actually as colimits over diagrams in [[CartSp]]. It follows that the functor $f_* : SPSh(Diff)_{inj}^{loc} \to SPSh(CartSp)_{inj}^{loc}$ preserves all weak equivalences.

By the same logic, for $A \in SPSh(Diff)$ and $B \in SPSh(CartSp)$ we find that if a morphism

$$
  f^* A \to B
$$

is a weak equivalence precisely if it is one on all the above disk-[[stalk]]s, which is the same condition that its [[adjunct]]

$$
  A \to f_* B
$$

is a weak equivalence, simply because testing on the [[point of a topos|topos points]] $p_n$ takes place entirly in [[CartSp]].

=--

+-- {: .un_remark}
###### Remark

This fact is noteworthy for the following reason: 

By the result of ([DuggerHollanderIsaksen](#DuggerHollanderIsaksen)) which is described at [[descent for simplicial presheaves]],
the fibrant objects in $SPSh(C)^{loc}_{proj}$ are those that are objectwise [[Kan complex]]es and satisfy [[descent]] along all [[hypercover]]s of [[representable functor|representables]]. But [[descent]] on the contractible $\mathbb{R}^n$s is a drastically simpler condition than on an arbitrary [[manifold]] $X$.

For instance, let $G$ be a [[Lie group]] and write $\mathbf{B}G$  for its corresponding degreewise representable simplicial presheaf $(\mathbf{B}G)_n = G^{\times n}$. 

Then regarded as an object of $SPSh(Diff)^{loc}_{proj}$ the object $\mathbf{B}G$ of course does not satisfy descent. Instead, its fibrant replacement is (the recified version of) $G Bund$, the [[stack]] of $G$-[[principal bundle]]s.

But regarded as an object in $SPSh(CartSp)^{loc}_{proj}$ the object $\mathbf{B}G$ does satisfy descent, because every $G$-[[principal bundle]] on $\mathbb{R}^n$ is [[isomorphism|isomorphic]] to the trivial one, and the [[automorphism group]] of the trivial $G$-bundle is just $C(\mathbb{R}^n,G)$.

So there are considerably more fibrant objects in $SPSh(CartSp)^{loc}_{proj}$ than there are in $SPSh(Diff)^{loc}_{proj}$. Accordingly, there must be less cofibrant objects in $SPSh(CartSp)^{loc}$ to compensate this.

Indeed, notice that every [[representable functor|representable]] in any of the model structures on $SPSh(C)$ is cofibrant. So an arbitrary [[manifold]] $X$ is cofibrant in $SPSh(Diff)^{loc}_{proj}$ and therefore there we have

$$
  Ho_{SPSh(Diff)^{loc}}(X, \mathbf{B}G )
  \simeq
  \pi_0 SPSh(X, G Bund)
  \simeq
  G Bund(X)_\sim
$$ 

as expected. In $SPSh(CartSp)^{loc}_{proj}$, however, $X$ is in general not representable, hence in general not cofibrant. But by the proposition below, that all objects which are degreewise coproducts of representables are cofibrant in all the model structures, we have that the [[?ech nerve]] $C(U)$ of any _[[good cover]]_ $U = \coprod_i U_i$ of $X$ (one for which each pathc and all intersections and higher intersections are contractible) is cofibrant. Hence here we find the above result by a different intermediate step

$$
  Ho_{SPSh(Cart)^{loc}}(X, \mathbf{B}G )
  \simeq
  \pi_0 SPSh(C(U), \mathbf{B}G)
  \simeq
  G Bund(X)_\sim
  \,.
$$

=--



## Fibrant and cofibrant objects {#FibAndCofibObjects}


### Fibrant objects

The fibrant objects in the [[local model structure on simplicial presheaves]] are those that 

* are fibrant with respect to the respective [[global model structure on simplicial presheaves|global model structure]]

* and satisfy [[descent for simplicial presheaves]]. See there for more details.

This descent condition is the analog in this model of the [[sheaf]]-condition and the [[stack]]-condition. In fact, it reduces to these for truncated simplicial presheaves.

Since the fibrancy condition in the global projective model structure is simple -- it just requires that the [[simplicial presheaf]] is in fact a presheaf of [[Kan complex]]es -- the local projective model structure has slightly more immediate characterization of fibrant objects than the local injective model structures. (In fact, for suitable choices of [[site]]s it may become very simple, as the above discussion of site dependence of the model structure shows).

On the other hand the cofibrancy condition on objects is entirly _trivial_ in the global and local injective model structure: since a cofibration there is just an objectwise cofibration, and since every [[simplicial set]] is cofibrant, every object is injective cofibrant.

But the cofibrant objects in the projective structure are not too nasty either: every object that is degreewise a coproduct of representables is cofibrant. In particular the [[?ech nerve]]s of any _[[good cover]]_ (see below for more details) is a projectively cofibrant object.

A **cofibrant replacement** functor in the local projective structure  is discussed in 

* [[Daniel Dugger]], _Universal homotopy theories_  ([pdf](http://hopf.math.purdue.edu/Dugger/dduniv.pdf))


Something related to a **fibrant replacement** functor ("$\infty$-stackification") is discussed in section 6.5.3 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]


### Cofibrant objects {#CofibrantObjects}

In the injective [[local model structure on simplicial presheaves]] all objects are cofibrant. For the projective local structure we have the following useful statement.


+-- {: .un_def }
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


+-- {: .un_prop }
###### Proposition

In the _projective_ [[local model structure on simplicial presheaves|local model structure]] all objects that are 

1. degreewise [[coproduct]]s of [[representable functor|representable]]s 

1. and whose degenerate cells split off

are cofibrant.

=--

This is in the proof of lemma 2.7 in section 9 of

* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_  


+-- {: .un_example }
###### Example
**(split hypercovers)**

If $Y \to X$ is an acyclic fibration in the local projective model structure with $X$ a representable and $Y$ cofibration in the above way, it is called a **[[split hypercover]]** .

All [[?ech nerve]]s $C(\{U_i\})$ coming from an [[open cover]] have split degeneracies. The condition that the Cech nerve be degreewise a coproduct of representables is a condition akin to that of [[good open cover]]s (which is precisely the special case for $C = $ [[CartSp]]). This is then a split hypercover of _height_ 0.

=--


+-- {: .un_def }
###### Definition
**(good cover)**

A [[?ech nerve]] $U$  with a weak equivalence $U \stackrel{\simeq}{\to} X$ in $SPSh(C)^{loc}$ is a **[[good cover]]** if it is degreewise a coproduct of [[representable functor|representable]]s.

=--

+-- {: .un_remark }
###### Remark

This reduces to the ordinary notion of [[good cover]] as an open cover by contractible spaces such that all finite intersections of these are again contractibe when using a [[site]] like $C = $ [[CartSp]].

=--






### Cofibrant replacement {#CofibrantReplacement}

In 

* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_  

a useful cofibrant replacement functor for the projective local model structure is discussed.

+-- {: .un_def }
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

+-- {: .un_prop }
###### Proposition

For all $A \in SPSh(C)$ the object $Q A$ is cofibrant and is weakly equivalent to $A$ in $SPSh(C)_{proj}^{loc}$. 

=--

This is in prop 2.8 of

* [[Daniel Dugger]], _[[Universal Homotopy Theories]]_  


## Localization and descent {#Descent}

### Cech localization at Grothendieck (pre)topologies {#CechLocalization}

We discuss some aspects of the [[Bousfield localization of model categories|left Bousfield localization]] of the projective global model structure on simplicial presheaves at [[Grothendieck topologies]] and [[covering]] families. By the discussion at [[topological localization]] these are models for [[topological localization]]s leading to [[(∞,1)-categories of (∞,1)-sheaves]].

The central reference is ([DuggerHollanderIsaksen](#DuggerHollanderIsaksen)) with the central theorem being this one:

+-- {: .un_theorem}
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

+-- {: .un_def}
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

+-- {: .un_prop}
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

+-- {: .un_prop}
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

+-- {: .un_cor}
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

+-- {: .un_lemma}
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


+-- {: .un_lemma}
###### Conclusion

In total this shows that the localization at the [[coverage]] produces the [[topological localization]] at the [[Grothendieck topology]] generated by that coverage.


=--


## Closed monoidal structure {#MonoidalStructure}

If the underlying site has finite [[product]]s, then both the injective and the projective, the global and the local model structure on simplicial presheaves becomes a [[monoidal model category]] with respect to the standard [[closed monoidal structure on presheaves]].

See for instance [here](http://www.math.univ-toulouse.fr/~toen/crm-2008.pdf#page=24).

+-- {: .un_lemma}
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


+-- {: .un_lemma}
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


## Homotopy (co)limits

Properties of [[homotopy limit]]s and [[homotopy colimit]]s of simplicial presheaves are discussed at

* [Homotopy (co)limits of simplicial (pre)sheaves](http://ncatlab.org/nlab/show/homotopy+limit#SimpSheaves)


## Examples

* A discussion of simplicial presheaves on $C = $ [[CartSp]] is at [[∞-Lie groupoid]].

* A discussion of simplicial presheaves on $C = $ [[ThCartSp]]/[[smooth loci]] is at [[∞-Lie algebroid]].




## References

A nicely helpful introduction and survey is provided in the notes

* Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

This in particular gives a detailed account on the relation and difference between the "&#268;ech model structure" (section 3) which localizes (only) at &#268;ech [[covers]], and the Jardine model structure (section 4), which localizes at all [[stalk]]wise weak equivalences ([[hypercovers]]). The latter is what in [[Higher Topos Theory|HTT]] is called the _hypercompletion_ .

The standard lecture notes are

* **Jardine07** J. Jardine, _Field Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

based on

* **Jardine01** J. Jardine, _Stacks and the homotopy theory of simplicial sheaves_, Homology, homotopy and applications, vol. 3 (2), 2001, pp.361--384

and ...

See also

* Benjamin Blander, _Local projective model structures on simplicial presheaves_,  K-Theory, Volume 24, Number 3, November 2001 , pp. 283--301(19) ([journal](http://www.ingentaconnect.com/content/klu/kthe/2001/00000024/00000003/00384649?crawler=true))

A detailed study of [[descent]] for simplicial presheaves is given in

* [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], 
_Hypercovers and simplicial presheaves_ , Math. Proc. Cambridge
Philos. Soc. 136 (2004), no. 1, 9&#8211;51 ([web](http://www.math.uiuc.edu/K-theory/0563/)) 
{#DuggerHollanderIsaksen}

* **DI02** [[Daniel Dugger]], [[Daniel Isaksen]], _Weak equivalences of simplicial presheaves_ ([arXiv](http://arxiv.org/abs/math/0205025))

A survey of many of the model structures together with a treatment of the left local projective one is in

* [[Benjamin Blander]], _Local projective model structure on simplicial presheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0462/combination2.pdf))

See also

* [[Daniel Isaksen]], _Flasque model structure for simplicial presheaves_  ([web](http://www.math.uiuc.edu/K-theory/0679/), [pdf](http://www.math.uiuc.edu/K-theory/0679/flasque.pdf))

The characterization of the model category of simplicial presheaves as the canonical [[presentable (infinity,1)-category|presentation]] of the (hypercompletion of) the [[(∞,1)-category of (∞,1)-sheaves]] on a site is in

* [proposition 6.5.2.1](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=528) of 

  * [[Jacob Lurie]], [[Higher Topos Theory]]

A set of lecture notes on simplicial presheaves with an eye towrads algebraic sites and [[derived algebraic geometry]] is

* [[Bertrand Toen]], _Simplicial presheaves and derived algebraic geometry_ , lecture at [Simplicial methofs in higher categories](http://www.crm.es/HigherCategories/)  ([pdf](http://www.crm.cat/HigherCategories/hc1.pdf))

Last not least, it is noteworthy that the idea of localizing simplicial sheaves at stalkwise weak equivalences is already described and applied in 

* [[Kenneth Brown]], _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf cohomology]]_ ,

using instead of a full [[model category]] structure the more lightweight one of a Brown [[category of fibrant objects]].

A comparison between Brown-Gersten and Joyal-Jardine approach:

* V. Voevodsky, _Homotopy theory of simplicial presheaves in completely decomposable topologies_, [arxiv/0805.4578](http://arxiv.org/abs/0805.4578)

[[!redirects model structures on simplicial presheaves]]