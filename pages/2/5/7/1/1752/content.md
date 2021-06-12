
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
* table of contents
{:toc}

## Idea ##

See [[model structure on simplicial presheaves]].


## Definition ##

There are many [[model category]] structures on the category of [[simplicial presheaf|simplicial presheaves]] derived from the [[model structure on simplicial sets]]. 

The _local_ such model structures are of interest in that they model [[infinity-stack homotopically|infinity-stacks]] so that they are a [[presentable (infinity,1)-category|presentation]] of the [[(infinity,1)-category of (infinity,1)-sheaves]] on the given [[site]].

They can be thought of as being obtained from global model structures, of which there are two:

* the  **[[global model structure on simplicial sheaves|global projective]]** model structure has weak equivalences and fibrations being _objectwise_ those of [[simplicial set]]s;

* the  **[[global model structure on simplicial sheaves|global injective]]** model structure has weak equivalences and cofibrations being _objectwise_ those of [[simplicial set]]s;

These two model structures are Quillen equivalent 
(*DHI04* [p. 5](http://www.math.uiuc.edu/K-theory/0563/spre.pdf#page=5) with the Quillen equivalence given by the identity functor). They can be defined on any domain category $S$, not necessarily a [[site]]. If we do have a structure of a [[site]] on $S$ then there is a  notion of _local weak equivalences_ of simplicial presheaves on $S$, defined below.
One gets _local_ projective and _local_ injective model structures by applying left [[Bousfield localization]] of the above model structures at local weak equivalences (see [p. 6](http://arxiv.org/PS_cache/math/pdf/0205/0205027v2.pdf#page=6) of *DHI04*)

* the  **local projective** model structure (weak equivalences are locally (usually stalkwise) and cofibrations are those that have the left [[lifting property]] against objectwise acyclic fibrations);

* the **local injective** (weak equivalences are locally (usually stalkwise) and fibrations are those that have the right [[lifting property]] against the objectwise acyclic cofibrations).

**Warning** Since the (homotopy classes) of weak equivalences do not form a [[small set]], the general existence theorem recalled at [[Bousfield localization of model categories]] does not apply. The existence of the Bousfield localization has to be shown by hand. For the injective structure this is what Joyal and Jardine accomplished.


Again, the injective and projective local model structures are Quillen equivalent by the identity functors between the underlying categories and hence provide projective and injective versions of the corresponding homotopy theory of [[infinity-stack homotopically|infinity-stacks]].

In the local injective structure all objects are cofibrant, so that the [[opposite category]] of simplicial presheaves with the local injective model structure is a [[category of fibrant objects]].

Both local model structures are proper [[enriched category|simplicially enriched]] categories (*DHI04* [p. 5](http://www.math.uiuc.edu/K-theory/0563/spre.pdf#page=6)). 

The _local injective_ model structure on simplicial presheaves is originally due to Jardine, following the construction of the Quillen equivalent local [[model structure on simplicial sheaves]] by Joyal. It was only later realized in _DHI04_ as a left [[Bousfield localization]] of the global injective model structure.


In between the injective and the projective model structures there are many other model structures obtained by varying the class of generating global cofibrations.


In the following let $S$ be a small [[site]] and denote by $SimpPr(S)$ be the category of [[simplicial presheaf|simplicial presheaves]] on $S$.


## Local model structures ##

One usually says that a **local model structure** on a category of [[presheaf|presheaves]] is one whose weak equivalences are not defined objectwise but on [[cover]]s and/or on [[stalk]]s.

### Local weak equivalences ###

There are different equivalent ways to define local weak equivalences of simplicial presheaves on a site $S$.


###In terms of sheaves of homotopy groups###

(see section 2 of _Jardine07_)

We want to say that a local weak equivalence of simplicial presheaves is one which is "over each point" an isomorphism of homotopy groups.

we need the following terminology about sheaves of simplicial homtopy groups:

* for $X$ a [[simplicial set]], write $\pi_0(X)$ for its set of connected components and $\pi_n(X,x)$, $n \geq 1$, $x \in X_0$, for its $n$th simplicial homotopy group at $x$ (the homotopy group of its [[geometric realization]]), $\pi_n(X,x) = \pi_n(|X|, x)$. This yields functors 
$\pi_0 : SimpSet \to Set$ and $\pi_n : SimpSet \to Grps$.

* By postcomposition these functors induce functors
$
  \pi_0 : SimpSet^{S^{op}} \to Set^{S^{op}}
$
and
$
  \pi_n : SimpSet^{S^{op}} \to Grps^{S^{op}}
$. 

* By postcomposition with the sheafification functor this yields functors
$
  \tilde \pi_0 : SimpSet^{S^{op}} \to Sh(S)
$
and
$
  \tilde \pi_n : SimpSet^{S^{op}} \to Sh(S,Grps)
$.

+-- {: .un_defn}
###### Definition

A **local weak equivalence** of simplicial presheaves is a morphism $f : X \to Y$ such that 

1. the morphism $\tilde \pi_0(f) : \tilde \pi_0 X \to \tilde \pi_0 Y$ is an isomorphism in $Sh(S)$;

2. the diagrams
$$
  \array{
     \tilde \pi_n X &\to& \tilde \pi_n Y
     \\
     \downarrow && \downarrow 
     \\
     \tilde X_0
     &\to&
     \tilde Y_0
  }
$$
are pullback diagrams in $Sh(S,SimpSet)$, for all $n \geq 1$, where $\tilde X_0$ denotes the sheaf associated to $X_0$.
=--

Equivalently a morphism $f : X \to Y$ of simplicial presheaves is, equivalently, a local weak equivalence if all induced morphisms of sheaves 
$$
  \tilde \pi_n (X|_U, x) \to \tilde \pi_n Y|_U, f(x)
$$
are isomorphisms for all $U \in S$, for $X|_U, Y|_U$ the pullbacks to the over-category site $S/U$, for all $x \in X_0(U)$ and all $n \geq 0$.

If the site $S$ _has enough points_ then this condition is equivalent to saying that $f$ is a weak equivalence in the [[model structure on simplicial sets]] over every stalk (see [p. 363](http://www.intlpress.com/HHA/v3/n2/a5/v3n2a5.pdf#page=3) of _Jardine01_).



###In terms of local liftings###

(see _DI02_, i.e. Dugger and Isaksen, Weak equivalences of simplicial presheaves )

If $X$ and $Y$ are local fibrations there is a characterisation in terms of local homotopy liftings. Write $P$ for the pushout of the diagram $\partial \Delta^n \leftarrow \partial \Delta^n\times \Delta^1 \rightarrow \Delta^n\times \Delta^1$. Then there are two maps $\Delta^n\rightarrow P$ by restriction of $\Delta^n\times \Delta^1\rightarrow P$ along the cofaces.

Then a local weak equivalence is a morphism $f : X \to Y$ such that for all commuting diagrams

$$
  \array{
    \partial \Delta^n \otimes U &\to& X
    \\
    \downarrow^{i_U} && \downarrow^f
    \\
    \Delta^n \otimes U &\to& Y
  }
$$

with $U$ simplicially constantly representable there exists a covering sieve $R$ of $U$ such that for every $V\in R$ there are morphisms $g:\Delta^n \otimes V\rightarrow X$ and $h:P\otimes V\rightarrow Y$ for which $g\circ i_V=\partial\Delta^n \otimes V\rightarrow \partial\Delta^n \otimes U \rightarrow X$ and $\Delta^n\otimes V \rightarrow \Delta^n \otimes U\rightarrow Y= \Delta^n\otimes V\rightarrow P\otimes V\rightarrow Y$ and in addition the square

$$
\array{
    \Delta^n\otimes V &\to& X
    \\
    \downarrow && \downarrow^f
    \\
    P \otimes U &\to& Y
  }
$$

commutes.

## Examples ###

* Every object-wise weak equivalence is in particular a local weak equivalence.





## Local injective model structure ##


The **local injective model structure** on simplicial presheaves on a [[site]] $C$ is the **left** [[Bousfield localization]] 
$SPr(C)_{loc inj}$
of the [[global model structure on simplicial presheaves|injective global model structure]] $SPr(C)_{inj}$ at the class of local weak equivalences described above.

So

* cofibrations are precisely the objectwise cofibrations of simplicial sets, i.e. the monomorphisms in $SPr(S)$;

* weak equivalences are the _local weak equivalences_ from above.



+-- {: .un_theorem }
###### Theorem 

The inclusion of sheaves into simplicial presheaves
$SimpSh(S) \hookrightarrow SimpPr(S)$ and the [[sheafification]] functor 
$SimpPr(S) \to SimpSh(S)$ constitute a 
[[Quillen equivalence]] with respect to the above
_local injective model structure_ on $SimpPr(S)$ ans the local [[model structure on simplicial sheaves]].

=--

+-- {: .proof}
###### Proof

See _Jardine07_, theorem 5.

=--


+-- {: .un_theorem }
###### Theorem 

The fibrant objects in the local injective model 
structure $SPr(C)_{loc inj}$ are those simplicial presheaves that

1. are fibrant in the global injective model structure;

2. satisfy [[descent]] for all [[hypercover]]s.

=--

+-- {: .proof}
###### Proof

_DHI04_, theorem 1.1

=--


## Local projective model structure ##

The **local projective model structure** on simplicial presheaves on a [[site]] $C$ is the **left** [[Bousfield localization]] 
$SPr(C)_{loc proj}$
of the [[global model structure on simplicial presheaves|projective global model structure]] $SPr(C)_{proj}$ at the class of local weak equivalences described above.

So

* cofibrations are precisely the cofibrations in the global projective structure (defined by left lifting property with respect to global Kan fibrations)

* weak equivalences are the _local weak equivalences_ from above.


**Remark**. Notice that this is still using **left** Bousfield localization. If we used right Bousfield localization the local projective fibrations would simply be the global Kan fibrations. Instead we have the following.


+-- {: .un_theorem }
###### Theorem 

The local injective model structure $SPr(C)_{loc inj}$ is [[Quillen equivalence|Quillen equivalent]] to the 
"universal homtopy thepory" $U C/S$ constructed by

1. formally adding [[homotopy limit|homotopy colimits]] to the category $C$ to create the category $U C$.

1. imposing relations requiring that for every [[hypercover]] $U \to X$, the morphism $hocolim_n U_n \to X$ is a weak equivalence.

=--

+-- {: .proof}
###### Proof

_DHI04_, theorem 1.2

=--

In $U C/S$ the fibrant objects have a simpler description 
than in $SPr(C)_{loc inj}$: they still need to satisfy [[descent]] but the implicit fibrancy condition with respect to the global injective structure is replaced by the fibrancy condition with respect to the global projective structure

+-- {: .un_theorem }
###### Theorem 

The fibrant objects in $U C/S$ are those simplicial presheaves $A$ that

1. are objectwise fibrant (i.e. take values in [[Kan complex]]es)

1. satisfy [[descent]] for all [[hypercover]]s.

=--

+-- {: .proof}
###### Proof

_DHI04_, theorem 1.3

=--





## Intermediate model structures ##

One can regard the projective and the injective model structure as two extrema of a poset of model structures on simplicial presheaves; see [[intermediate model structure]].

#References#

See *[[model structure on simplicial presheaves]]*.

The local projective model structure on simplicial presheaves appears as theorem 1.6 in

* Benjamin Blander, _Local projective model structure on simplicial presheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0462/combination2.pdf))

Its analog for sheaves, theorem 2.1 there, is due to 

* K. Brown, Gersten, ...

That the local projective model structure (directly defined) is indeed the left Bousfield localization of the global projective model structure is lemma 4.3 there.

[[!redirects local model structures on simplicial presheaves]]

[[!redirects injective local model structure on simplicial presheaves]]
[[!redirects injective local model structures on simplicial presheaves]]

[[!redirects projective local model structure on simplicial presheaves]]
[[!redirects projective local model structures on simplicial presheaves]]


