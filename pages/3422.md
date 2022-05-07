
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The **$(\infty,1)$-Grothendieck construction** is a generalization of the [[Grothendieck construction]] -- which establishes an equivalence

$$
  Fib(C) \simeq 2Func(C^{op}, Cat)
$$

and

$$
  Fib_{Grpd}(C) \simeq 2Func(C^{op}, Grpd)
$$

between [[fibered category|fibered categories]]/[[categories fibered in groupoids]] and [[pseudofunctor]]s to [[Cat]]/to [[Grpd]] -- from [[category theory]] to [[(∞,1)-category]]-[[higher category theory|theory]].

The Grothendieck construction for [[∞-groupoid]]s constitutes an equivalence of [[(∞,1)-categories]]

$$
  RFib(C) \simeq \infty Func(C^{op}, \infty Grpd)
$$

between [[right fibration]]s [[fibrations of quasi-categories|of quasi-categories]] and [[(∞,1)-functor]]s to [[∞Grpd]], while the full Grothendieck construction for [[(∞,1)-categories]] constitutes an equivalence 

$$
  CartFib(C) \simeq \infty Func(C^{op}, (\infty,1)Cat)
$$

between [[Cartesian fibration]]s [[fibrations of quasi-categories|of quasi-categories]] and [[indexed (∞,1)-categories]], that is, [[(∞,1)-functor]]s to [[(∞,1)Cat]].


This correspondence may be [[model category|modeled]] 

* in the case of $\infty$-groupoids by a [[Quillen equivalence]] between the [[model structure for right fibrations]] and the projective [[global model structure on simplicial presheaves]] 

* in the case of $(\infty,1)$-categories by a Quillen equivalence between the [[model structure for Cartesian fibrations]] and the [[global model structure on functors]] with values in the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]].


## For fibrations in $\infty$-groupoids

The generalization of a [[category fibered in groupoids]] to [[quasi-category]] theory is a [[right fibration|right]] [[fibrations of quasi-categories|fibration of quasi-categories]].

+-- {: .un_theorem}
###### Theorem 
**($(\infty,0)$-Grothendieck construction)**

Let $C$ be an [[(∞,1)-category]]. There is an equivalence of [[(∞,1)-categories]]

$$
  RFib(C) \simeq Func(C^{op}, \infty Grpd)
$$

where 

* on the left we have the [[right fibration|(∞,1)-category of right fibrations]] $RFib(C)$ -- incarnated as the full [[SSet]]-[[subcategory]] of the [[overcategory]] $SSet/C$ on [[right fibration]]s;

* and on the right the [[(∞,1)-category of (∞,1)-functors]] from the [[opposite category]] $C^{op}$ to [[∞Grpd]], i.e. the [[(∞,1)-category of (∞,1)-presheaves]] on $C$.

=--


In the next section we discuss how this statement is presented in terms of [[model categories]].



### Model category presentation {#GrpdModelCatVersion}

We discuss a [[presentable (∞,1)-category|presentation]] of the $(\infty,0)$-Grothendieck construction by a [[simplicial Quillen adjunction]] between [[simplicial model categories]]. ([[Higher Topos Theory|HTT, section 2.2.1]]).

+-- {: .un_def #UnmarkedStraighteningFunctor}
###### Definition 
**(extracting a simplicial presheaf from a fibration)**

Let 

* $S$ be a [[simplicial set]], $\tau_hc(S)$ the corresponding [[SSet-category]] (under the [[left adjoint]] $\tau_{hc} : SSet \to SSet Cat$ of the [[homotopy coherent nerve]], denoted $\mathfrak{C}$ in [[Higher Topos Theory|HTT]]);

* $C$ an [[SSet-category]];

* $\phi : \tau_{hc}(S) \to C$ a morphism of [[SSet-categories]].

> In particular we will be interested in the case that $\phi$ is the identity, or at least an equivalence, identifying $C$ with $\tau_{hc}(S)$.

For any object $(p : X\to S)$ in $sSet/S$ consider the [[sSet-category]] $K(\phi,p)$ obtained as the (ordinary) [[pushout]] in [[SSet Cat]]
 
$$
  \array{
    \tau_{hc}(X) &\stackrel{}{\to}& \tau_{hc}(X^{\triangleright})
    \\
    {}^{\mathllap{\phi(p)}}\downarrow && \downarrow
    \\
    C &\to& K(\phi,p) 
  }
  \,,
$$

where $X^{\triangleright} = X \star \{v\}$ is the [[join of simplicial sets]] of $X$ with a single vertex $v$.

Using this construction, define a functor, the **[[straightening functor]]**,

$$
  St_\phi : sSet/S \to [C^{op}, sSet]
$$

from the [[overcategory]] of [[sSet]] over $S$ to the [[enriched functor category]] of [[sSet]]-[[enriched functor]]s from $C^{op}$ to $sSet$ by defining it on objects $(p : X \to S)$ to act as

$$
  St_\phi(X) := K(\phi,p)(-,v) : C^{op} \to SSet
  \,.  
$$

=--


+-- {: .un_example}
###### Example 

The straightening functor effectively computes the fibers of a [[Cartesian fibration]] $(p : X \to C)$ over every point $x \in C$. As an illustration for how this is expressed in terms of morphisms in that pushout, consider the simple situation where

* $C = *$ only has a single point;

* $X = \left\{ a \to b \;\;\; c\right\}$ is a category with three objects, two of them connected by a morphism

* $p : X\to C$ is the only possible functor, sending everything to the point.

Then 

* $X^{\triangleright} = 
    \left\{
      \array{
         a &\to& b && c
         \\
         & \searrow \Leftarrow& \downarrow & \swarrow
         \\
         && v
      }
    \right\}
  $

and

* $X^{\triangleright} \coprod_{X} C = 
    \left\{
      \array{
         && \bullet
         \\
         & \swarrow & \downarrow & \searrow
         \\
         \downarrow& \Leftarrow & \downarrow
         \\
         & \searrow & \downarrow & \swarrow
         \\
         && v
      }
    \right\}
  $


Therefore the category of morphisms in this pushout from $*$ to $v$ is indeed again the category $\{a \to b \;\;\; c\}$.

More on this is at [[Grothendieck construction]] in the section of adjoints to the Grothendieck construction.

=--

+-- {: .un_prop}
###### Proposition

With the definitions [as above](#UnmarkedStraighteningFunctor), let $\pi : C \to C'$ be an [[sSet]]-[[enriched functor]] between [[sSet-categories]]. Write

$$
  \pi_! : [C^{op}, sSet] \to [{C'}^{op}, sSet] 
$$

for the left [[sSet]]-[[Kan extension]] along $\pi$.

There is a [[natural isomorphism]] of the straightening functor for the composite $\pi \circ \phi$ and the original straightening functor for $\phi$ followed by left [[Kan extension]] along $\pi$:

$$
  St_{\pi \circ \phi} \simeq \pi_! \circ St_\phi
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 2.2.1.1.]]. The following proof has kindly been spelled out by [[Harry Gindi]].

+-- {: .proof}
###### Proof

We unwind what the [[sSet-categories]] with a single object adjoined to them look like:

let 

$$
  F : C^{op} \to sSet
$$

be an [[sSet]]-[[enriched functor]]. Define from this a new [[sSet-category]] $C_F$ by setting

* $Obj(C_F) = Obj(C) \coprod \{\nu\}$

* $C_F(c,d) = \left\{
    \array{
      C(c,d) & for c,d \in Obj(C)
      \\
      F(c) & for c \in Obj(c) and d = \nu
      \\
      \emptyset & for c = \nu and d \in Obj(C)
      \\
      * & for c = d = \nu
    }
  \right.$

The composition operation is that induced from the composition in $C$ and the enriched functoriality of $F$.

Observe that the [[sSet-category]]
$K(\phi,p)$ appearing in the [definition of the straightening functor](#UnmarkedStraighteningFunctor)  is

$$
  K(\phi,p) \simeq C_{St_\phi(X)}
$$

(because $K(\phi,p)$ is $C$ with a single object $\nu$ and some morphisms to $\nu$ adjoined, such that there are no non-degenerate morphisms originating at $\nu$, we have that $K(\phi,p)$ is of form $C_F$ for some $F$; and $St_\phi(X)$ is that $F$ by definition).

To prove the proposition, we need to compute the pushout

$$
  \array{
    \tau_{hc}(X) &\to& \tau_{hc}(X^{\triangleright})
    \\
    \downarrow && \downarrow
    \\
    C &\to& K(\phi,p) = C_{St_\phi(X)} 
    \\
   {}^{\mathllap{\pi}}\downarrow && \downarrow
   \\
   C' &\to& Q 
  }
$$

and show that indeed $Q \simeq C'_{\pi_! St_\phi(X)}$.


Using the pasting law for [[pushout]]s (see [[pullback]]) we just have to compute the lower square pushout. Here the statement is a special case of the following statement: for every [[sSet-category]] of the form $C_F$, the pushout of the canonical inclusion $C\to C_F$ along any $sSet$-functor $\pi : C \to C'$ is $C'_{\pi_! F}$.

This follows by inspection of what a cocone

$$
  \array{
     C &\stackrel{\iota}{\to}& C_F
     \\
     {}^{\mathllap{\pi}}\downarrow && \downarrow^{\mathrlap{d}}
     \\
     C' &\underset{r}{\to}& Q 
  }
$$

is like: by the nature of $C_F$ the functor $d$ is characterized by a functor $d|_C : C \to Q$, an object $d(\nu) \in Q$ together with a [[natural transformation]] 

$$
  F(c) \to  Q(d|_C(c), d(\nu))
$$

being the component $F_{c,\nu} : C_F(c,\nu) \to Q(d(c), d(\nu))$ of the $sSet$-functor.

We may write this natural transformation as

$$
  F \to (d|_C)^* Q(-,d(\nu)) = \iota^* d^* \nu Q(-,d(\nu))
  \,,
$$

where $d^*$ etc. means precomposition with the functor $d$.

By commutativity of the diagram this is

$$
  \cdots \simeq \pi^* r^* Q(-,d(\nu))
  \,.
$$

Now by the definition of left [[Kan extension]] $\pi_!$ as the [[left adjoint]] to prescomposition with a functor, this is bijectively a transformation

$$
  \eta : \pi_! F \to r^* Q(-,d(\nu))
  \,.
$$

Using this we see that we may find a universal cocone by setting 
$Q := C'_{\pi_! F}$ with $r : C' \to Q$ the canonical inclusion and
$C_{F} \to C'_{\pi_! F}$ given by $\pi$ on the restriction to $C$ and by the [[unit of an adjunction|unit]] $F \to \pi^* \pi_! F$ on $C_F(c,\nu)$. For this the [[adjunct]] transformation $\eta$ is the identity, which makes
this universal among all cocones.


=--

+-- {: .un_prop}
###### Proposition

This functor has a [[right adjoint]]

$$
  Un_\phi : [C^{op}, sSet] \to sSet/S
  \,,
$$

that takes a [[simplicial presheaf]] on $C$ to a simplicial set over $S$ -- this is the **unstraightening functor**.

=--

+-- {: .proof}
###### Proof

One checks that $St_\phi$ preserves [[colimit]]s. The claim then 
follows with the [[adjoint functor theorem]].

=--


+-- {: .un_theorem}
###### Theorem 
**(presentation of the $(\infty,0)$-Grothendieck construction)**


The straightening and the unstraightening functor constitute a [[Quillen adjunction]]

$$
  (St_\phi \dashv Un_\phi) : sSet/S
  \stackrel{\overset{Un_{\phi}}{\leftarrow}}{\underset{St_\phi}{\to}}
  [C^{op}, sSet]
$$

between the [[model structure for right fibrations]] and the global projective [[model structure on simplicial presheaves]] on $S$.

If $\phi$ is a weak equivalence in the [[model structure on simplicial categories]] then this Quillen adjunction is a [[Quillen equivalence]].

=--

This is [[Higher Topos Theory|HTT, theorem 2.2.1.2]].


This models the Grothendieck construction for [[∞-groupoid]]s in the following way:

* the [[presentable (∞,1)-category|(∞,1)-category presented by]] $sSet/S$ is $RFib(S)$
 
  ([[Higher Topos Theory|HTT, lemma 2.2.3.9]])

* the [[presentable (∞,1)-category|(∞,1)-category presented by]]
  the global [[model structure on simplicial presheaves]] 
  $[C^{op}, SSet]$ is [[(∞,1)-category of (∞,1)-presheaves]] 
  $PSh_{(\infty,1)}(N_{hc}(C))$

Hence the unstraightening functor is what models the [[Grothendieck construction]] proper, in the sense of a construction that generalizes the construction of a [[fibered category]] from a [[pseudofunctor]].


### Remark: $(\infty,0)$-fibrations over an $\infty$-groupoid {#GrpdFibsOverGrpds}

+-- {: .un_lemma}
###### Observation

Let $C$ itself be an $\infty$-groupoid. Then $RFib(C) \simeq \infty Grpd/C$ and hence

$$
  \infty Grpd/C \simeq [C^{op}, \infty Grpd]
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the fact that there is the standard [[model structure on simplicial sets]] we have that every morphism of $\infty$-groupoids $X \to C$ factors as

$$
  \array{
     X &&\stackrel{\simeq}{\to}&& \hat X
     \\
     & \searrow && \swarrow_{\mathrlap{fib}}
     \\
     && C
  }
  \,,
$$

where the top morphism is an equivalence and the right morphism a [[Kan fibration]]. Moreover, as discussed at [[right fibration]], over an $\infty$-groupoid the notions of left/right fibrations and Kan fibrations coincide.  This shows that the full [[sub-(∞,1)-category]] of $\infty Grpd/X$ on the right fibrations is equivalent to all of $\infty Grpd/X$.

=--

## For general fibered $(\infty,1)$-categories

The generalization of a [[fibered category]] to [[quasi-category]] theory is a [[Cartesian fibration|Cartesian]] [[fibrations of quasi-categories|fibration of quasi-categories]].


+-- {: .un_theorem}
###### Theorem 
**($(\infty,1)$-Grothendieck construction)**

Let $C$ be an [[(∞,1)-category]]. There is an equivalence 

$$
  Cart(C) \simeq Func(C^{op}, (\infty,1) Cat)
$$

where 

* on the left we have the $(\infty,1)$-category of [[Cartesian fibration]]s over $C$ -- incarnated as a [[sSet]]-[[subcategory]]
of the [[overcategory]] $sSet/C$ on [[Cartesian fibration]]s;

* and on the right the [[(∞,1)-category of (∞,1)-functors]] from $C^{op}$ to the [[(∞,1)-category of (∞,1)-categories]].

=--


In the next section we discuss how this statement is presented in terms of [[model categories]].


### Model category presentation {#ModCatCart}


Regard the [[(∞,1)-category]] $C$ in its incarnation as a [[simplicially enriched category]].

Let $S$ be a [[simplicial set]], $\tau_{hc}(S)$ the corresponding [[simplicially enriched category]] (where $\tau_{hc}$ is the [[left adjoint]] of the [[homotopy coherent nerve]]) and let $\phi : \tau_{hc}(S) \to C$ be an [[sSet]]-[[enriched functor]].

+-- {: .un_def}
###### Definition 
**(extracting a marked simplicial presheaf from a marked fibration)**
(HTT, section 3.2.1)

The **straightening functor**

$$
  St_\phi : sSet^+/S \to [C^{op}, sSet^+]
$$

from [[marked simplicial set]]s over $S$ to marked [[simplicial presheaves]] on $C^{op}$ is on the underlying simplicial sets (forgetting the marking) the same straightening functor as [above](#GrpdModelCatVersion).  

On the markings the functor acts as follows. 

Each edge $f: d \rightarrow e$ of $X \in sSet/S$ gives rise to an edge $\tilde f \in St_\phi (X)(d) = K(\phi,p)(d,v)$: the [[join of simplicial sets|join]] 2-simplex $f \star v$ of $X^{\triangleright}$                

$$                                                                              
  \array{                                                                   
    d && \stackrel{f}{\to} && e                                            
    \\                                                                     
    & {}_{\mathllap{\tilde d}}\searrow 
   & \stackrel{\tilde f}{\Rightarrow} 
   & \swarrow_{\mathrlap{\tilde e}}                                    
    \\                                                                     
    && v                                                                   
  }                                                                         
$$                                                                              

with image $\tilde f : \tilde d \to f^* \tilde e$ 
in the pushout $K(\phi,p)(d,v)=St_\phi X(d)$.

We define the straightening functor to assign that
marking of edges which is the minimal one such that all
such morphisms $\tilde f$ are marked in 
$St_\phi X(d)$, for all marked $f : d \to e$
in $X$: 
this means that this marking is being completed under the constraint
that $St_\phi(X)$ be [[sSet]]-[[enriched functor|enriched functorial]]. 

For that, [[marked simplicial set|recall]] that the hom simplicial sets of $sSet^+$ are  the spaces $Map^\sharp(X,Y)$, which consist of those simplices of the [[internal hom]] $Map(X,Y) := Y^X$ whose edges are all marked:

$$
  Map(X,Y)_n = Hom_{sSet^+}(X \times \Delta[n]^#, Y)
  \,.
$$

So we need to find a marking on the $St_\phi(X)(-)$ such that for all
$g : \Delta[1] \to C(c,d)$ the composite

$$
  \Delta[1]
  \stackrel{g}{\to}
  C(c,d)
  \stackrel{St_\phi(X)(c,d)}{\to}
  Map(St_\phi(X)(d), St_\phi(X)(c))
$$

is a marked edge of the mapping complex. By the internal hom-adjunction this edge corresponds to a morphism

$$
  St_\phi(X)(g)
  :
  St_\phi(X)(d) \times \Delta[1] \rightarrow St_\phi(X)(c)
$$

and to be marked needs to carry edges of the form $\tilde f \times \{0 \to 1\}$ i.e. 1-cells  $(\tilde f , Id) : \Delta[1] \to St_\phi(X)(d) \times \Delta[1]$ to marked edges 

$$
  g^* \tilde f : \Delta[1] \stackrel{(\tilde f,Id)}{\to}
  St_\phi(X)(d)\times \Delta[1] \stackrel{St_\phi(X)(g)}{\to}
  St_{\phi}(X)(c)
$$

in $St_\phi(X)(c)$. So we need to ensure that the edges of this form are marked:

we define that the straightening functor marks an edge in $St_\phi(X)(c)$ iff it is of this form $g^* \tilde f$, for $f : d \to e$ a marked edge of $X$ and $g \in C(c,d)_1$.


As in the unmarked cae, the straightening functor has an [[sSet]]-[[right adjoint]], the **unstraightening functor**

$$
  n_\phi :  [C^{op}, sSet^+] \to sSet^+/S 
  \,.
$$


=--

This functor $Un_\phi$ exhibits the $(\infty,1)$-Grothendieck-construction proper, in that it constructs a [[Cartesian fibration]] from a given $(\infty,1)$-functor:


+-- {: .un_theorem}
###### Theorem 
**(presentation of $(\infty,1)$-Grothendieck construction)**

This induces a [[Quillen adjunction]]

$$
  (St_\phi \dashv Un_\phi) : SSet^+/S
  \stackrel{\overset{Un_{\phi}}{\leftarrow}}{\underset{St_\phi}{\to}}
  [C^{op}, SSet^+]
$$

between the [[model structure for Cartesian fibrations]] and the projective [[global model structure on functors]] with values in the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]].


If $\phi$ is an equivalence in the [[model structure on simplicial categories]] then this Quillen adjunction is a [[Quillen equivalence]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 3.2.0.1]].

=--

#### Over an ordinary category {#OverCat}

In the case that $C$ happens to be an ordinary [[category]], the $(\infty,1)$-Grothendieck construction can be simplified and given more explicitly.

This is [[Higher Topos Theory|HTT, section 3.2.5]].


+-- {: .un_def}
###### Definition
**(relative nerve functor)**

Let $C$ be a small category and let $f : C \to sSet$ be a functor. The simplicial set $N_f(C)$, the **relative nerve** of $C$ under $f$ is defined as follows:

an $n$-cell of $N_f(C)$ is

1. a functor $\sigma : [n] \to C$;

1. for every $[k] \subset [n]$ a morphism $\tau(k) : \Delta[k] \to f(\sigma(k))$;

1. such that for all $[j] \subset [k] \subset [n]$ the diagram

   $$
     \array{
       \Delta[j] &\stackrel{\tau(j)}{\to}& f(\sigma(j))
       \\
       \downarrow && \downarrow^{\mathrlap{f(\sigma(j\to k))}}
       \\
       \Delta[k] &\stackrel{\tau(k)}{\to}& f(\sigma(k))
     }
   $$

   commutes.

There is a canonical morphism

$$
  N_f(C) \to N(C)
$$

to the ordinary [[nerve]] of $C$, obtained by forgetting the $\tau$s.

=--

This is [[Higher Topos Theory|HTT, def. 3.2.5.2]].

+-- {: .un_remark}
###### Remark

When $f$ is constant on the point, then $N_f(C) \to N(C)$ is an isomorphism of simplicial sets, so $N_f(C)$ this is the ordinary [[nerve]] of $C$.

The [[fiber]] of $N_f(C) \to N(C)$ over an object $c \in C$ is given by taking $\sigma$ to be constant on $C$. Then all the $\tau$s are fixed by the maximal $\tau(n) : \Delta[n] \to f(c)$. So the fiber of $N_f(C)$ over $c$ is $f(c)$.

=--


+-- {: .un_def}
###### Definition
**(marked relative nerve functor)**

Let $C$ be a small [[category]]. Define a functor

$$
  sSet^+/N(C) \leftarrow [C, sSet^+] : N^+
$$

by 

$$
  (C \stackrel{F}{\to} sSet^+)
  \mapsto
  (N_f(C), E_F)
  \,,
$$

where $f : C^{op} \stackrel{F}{\to} sSet^+ \to sSet$ is $F$ with the marking forgotten, where $N_f(C)$ is the relative nerve of $C$ under $f$, and where the marking $E_F$ is given by ...


=--

This is [[Higher Topos Theory|HTT, def. 3.2.5.12]].

This functor has a [[left adjoint]] $\mathcal{F}^+$. The value of $\mathcal{F}^+(F)$ on some $c \in C$ is equivalent to the value of $St(F)$.

This is [[Higher Topos Theory|HTT, Lemma 3.2.5.17]].



+-- {: .un_prop}
###### Proposition
**($(\infty,1)$-Grothendieck construction over a category)**

The adjunction

$$
  (\mathcal{F}^+ \dashv N^+)
  : 
  sSet^+_{/N(C)} \stackrel{\overset{\mathcal{F}^+}{\to}}{\underset{N^+}{\leftarrow}}
  [C,sSet^+]
  \,.
$$

is a [[Quillen equivalence]] between the [[model structure for Cartesian fibrations|model structure for coCartesian fibrations]] and the projective [[global model structure on functors]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 3.2.5.18]].

=--



### Relation beween the model structures

+-- {: .un_theorem}
###### Theorem (HTT, section 3.1.5)

Let $S$ be a [[simplicial set]].

There is a sequence of [[Quillen adjunction]]s

$$
  (sSet/S)_{Joyal}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  sSet^+/S
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet^+/S)^{loc}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet/S)_{rfib}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet/S)_{Quillen}
  \,.
$$

Where from left to right we have

1. the [[model structure on an overcategory]] for the Joyal [[model structure for quasi-categories]];

1. the [[model structure for Cartesian fibrations]];

1. some localizaton of the model structure for Cartesian fibrations;

1. the [[model structure for right fibrations]] 

1. the [[model structure on an overcategory]] for the Quillen [[model structure on simplicial sets]];

The first and third Quillen adjunction here is a [[Quillen equivalence]] if $S$ is a [[Kan complex]].

=--

## Properties

### As an (op)lax $\infty$-colimit

The $(\infty,1)$-Grothendieck construction on an $\infty$-functor is equivalently its [[lax (infinity,1)-colimit]] ([Gepner-Haugseng-Nikolaus 15](#GepnerHaugsengNikolaus15)).

See also at _[[Grothendieck construction]]_  _[as a lax colimit](Grothendieck%20construction#AsALaxColimit)_.



## Examples

### Cartesian fibrations over the point

For the base category $S$ being the point $S = {*}$, the  $(\infty,1)$-Grothendieck construction naturally becomes essentially trivial. However, its model by the Quillen functor

$$
  St_\phi : sSet/* \simeq sSet \to [*,sSet] \simeq sSet 
$$

is not entirely trivial and in fact produces a Quillen auto-equivalence of $sSet_{Quillen}$ with itself that plays a central role in the proof of the corresponding Quillen equivalence over general $S$.

**Definition**

Let $Q : \Delta \to sSet$ be the [[cosimplicial object|cosimplicial]] [[simplicial set]] given by

$$
  Q[n] := |J^n|(x,v)
  \,,
$$

where

$$
  J^n = C^{\triangleleft}(\Delta[n] \to \{x\})
  \,.
$$

Then: [[nerve and realization]] associated to $Q$ yield a [[Quillen equivalence]] of $sSet_{Quillen}$ with itself.

[[Higher Topos Theory|HTT, section 2.2.2]].

...

### Cartesian fibrations over the interval {#FibsOverInterval}

A [[Cartesian fibration]] $p : K \to \Delta[1]$ over the 1-[[simplex]] corresponds to a morphism 
$\Delta[1]^{op} \to $ [[(∞,1)Cat]], hence to an [[(∞,1)-functor]] $F : D \to C$.

By the above  procedure we can express $F$ as the image of $p$ under the straightening functor. The characterization via lax colimits leads to describing $K$ as the mapping cylinder $(\Delta^1 \times B) \amalg_{\Delta^{\{0\}} \times B} A$.

However, there is a more immediate way to extract this functor, which we now describe. This construction also provides additional strictness properties in the quasicategory model.

First recall the situation for the ordinary [[Grothendieck construction]]: given a [[Grothendieck fibration]] $K \to \{0 \to 1\}$, we obtain a functor $f : K_1 \to K_0$ between the fibers, by _choosing_ for each object $d \in K_1$ a [[Cartesian morphism]] $e_d \to d$. Then the universal property of Cartesian morphism yields for every  morphism $d_1 \to d_2$ in $K_1$ the unique left vertical filler in

$$
  \array{
    e_{d_1} &\to& d_1
    \\
    \downarrow && \downarrow
    \\
    e_{d_2} &\to& d_2
  }
  \,.
$$

And again by universality, this assignment is functorial: $K_1 \to K_0$.

Diagrammatically, the choice of Cartesian morphisms here is a lift $e$ in the diagram

$$
  \array{
    K_1 &\hookrightarrow& K
    \\
    \downarrow &\nearrow_e& \downarrow
    \\
    K_1 \times \{0 \to 1\} &\to& \{0 \to 1\}
  }
  \,.
$$

This diagrammatic way of encoding the functor associated to a Grothendieck fibration over the interval generalizes straightforwardly to the [[quasi-category]] context.

+-- {: .un_defn}
###### Definition


Given a [[Cartesian fibration]] $p : K \to \Delta[1]$ with fibers the [[quasi-categories]] $C := K_{0}$ and $D := K_{1}$, an **$(\infty,1)$-functor associated to the Cartesian fibration** $p$ is a functor $f : D \to C$ such that there exists a commuting diagram in [[sSet]]

$$
  \array{
    D \times \Delta[1] &&\stackrel{F}{\to}&& K
    \\
    & \searrow && \swarrow_{\mathrlap{p}}
    \\
    && \Delta[1]
  }
$$

such that 

* $F|_{1} = Id_D$;

* $F|_{0} = f$;

* and for all $d \in D$, $F(\{d\}\times \{0  \to 1\})$ is a [[Cartesian morphism]] in $K$.

More generally, if we also specify possibly nontrivial [[equivalence of quasi-categories|equivalences of quasi-categories]] $h_0 : C \stackrel{\simeq}{\to} K_{0}$  and $h_1 : D \stackrel{\simeq}{\to} K_{1}$, then a functor is associated to $K$ and this choice of equivalences if the first twoo conditions above are generalized to

* $F|_{1} = h_1$;

* $F|_{0} = h_0 \circ f$;


=--

This is [[Higher Topos Theory|HTT, def. 5.2.1.1]].

+-- {: .un_prop}
###### Proposition

For $p : K \to \Delta[1]$ a Cartesian fibration, the associated functor exists and is unique up to equivalence in the [[(∞,1)-category of (∞,1)-functors]] $Func(K_{0}, K_{1})$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.1.5]].

Set $C := K_{0}$ and $D := K_{1}$.

With the notation described at [[model structure for Cartesian fibrations]], consider the commuting diagram

$$
  \array{
    D^\flat \times \{1\} &\hookrightarrow& K^{\sharp}
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    D^{\flat} \times \Delta[1]^{#} &\to&
    \Delta[1]^#
  }
$$

in the category $sSet^+$ of marked simplicial sets.

Here the left vertical morphism is [marked anodyne](http://ncatlab.org/nlab/show/model+structure+for+Cartesian+fibrations#MarkedAnodyne): it is the [[smash product]] of the marked cofibration (monomorphism) $Id : D^\flat \to D^\flat$ with the marked anodyne morphism $\Delta[1]^# \to \Delta[0]$. By the stability properties discussed at [Marked anodyne morphisms](http://ncatlab.org/nlab/show/model+structure+for+Cartesian+fibrations#MarkedAnodyne), this implies that the morphism itself is marked anodyne.

As discussed there, this means that a lift $d : D^\flat \times \Delta[1]^# \to K^{\sharp}$ against the Cartesian fibration in 

$$
  \array{
    D^\flat \times \{1\} &\hookrightarrow& K^{\sharp}
    \\
    \downarrow &\nearrow_{s}& \downarrow^{\mathrlap{p}}
    \\
    D^{\flat} \times \Delta[1]^{#} &\to&
    \Delta[1]^#
  }
$$

exists. This exhibits an associated functor $f := s_0$.

Suppose now that another associated functor $f'$ is given. It will correspondingly come with its diagram

$$
  \array{
    D^\flat \times \{1\} &\hookrightarrow& K^{\sharp}
    \\
    \downarrow &\nearrow_{s'}& \downarrow^{\mathrlap{p}}
    \\
    D^{\flat} \times \Delta[1]^{#} &\to&
    \Delta[1]^#
  }
  \,.
$$

Together this may be arranged to a diagram

$$
  \array{
    D^\flat \times \Lambda[2]_2 
     &\stackrel{(s,s')}{\to}& K^{\sharp}
    \\
    \downarrow &\nearrow_{q}& \downarrow^{\mathrlap{p}}
    \\
    D^{\flat} \times \Delta[2]^{#} &\to&
    \Delta[1]^#
  }
  \,,
$$

where the top horizontal morphism picks the 2-[[horn]] in $K$ whose two edges are labeled by $s$ and $s'$, respectively. 

Now, the left vertical morphism is still marked anodyne, and hence the lift $k$ exists, as indicated. Being a morphism of marked simplicial sets, it must map for each $d \in D$ the edge $\{d\}\times \{0\to 1\}$ to a [[Cartesian morphism]] in $K$, and due to the commutativity of the diagram this morphism must be in $K_0$, sitting over $\{0\}$. But as discussed there, a [[Cartesian morphism]] over a point is an equivalence. This means that the restriction 

$$
  k|_{D \times \{0 \to 1\}} \to K_0
$$

is an invertible [[natural transformation]] between $f$ and $f'$, hence these are equivalent in the functor category.


=--

Conversely, every functor $f : D \to C$ gives rise to a Cartesian fibration that it is associated to, in the above sense.

+-- {: .un_prop}
###### Proposition

Every $(\infty,1)$-functor $f : D \to C$ is associated to some Cartesian fibration $p : K \to \Delta[1]$, and this is unique up to equivalence.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.1.3]].

The idea is that we obtain $K$ from first forming the cylinder $D \times \Delta[1]$ and the identifying the left boundary of that with $C$, using $f$.

Formally this means that we form the [[pushout]]

$$
  N := (D^\sharp \times \Delta[1]^#) \coprod_{D^\sharp \times \{0\}^#} C^\sharp
$$

in $sSet^+$, where $C^\sharp$ and $D^\sharp$ are $C$ and $D$ with precisely the [[equivalence in a quasi-category|equivalences]] marked. This comes canonically with a morphism 

$$
  N \to \Delta[1]
$$

and does have the property that $N_0 = C$, $N_1 = D$ and that $f$ is associated to it in that the restriction of the canonical morphism $D \times \Delta[1] \to K$ to the 0-fiber is $f$.  But it may fail to be a Cartesian fibration.

To fix this, use the [[small object argument]] to factor $N \to \Delta[1]$ as

$$
  N \to K \to \Delta[1]^#
  \,,
$$

where the first morphism is [marked anodyne](http://ncatlab.org/nlab/show/model+structure+for+Cartesian+fibrations#MarkedAnodyne) and the second has the [[right lifting property]] with respect to all marked anodyne morphisms and is hence (since every morphism in $\Delta[1]^#$ is marked) a Cartesian fibration.

It then remains to check that $f$ is still associated to this $K \to \Delta[1]^#$. This is done by observing that in the small object argument $K$ is built succesively from [[pushout]]s of the form

$$
  \array{
    A &\to& N_\alpha
    \\
    \downarrow && \downarrow & \searrow 
    \\
    B &\to& N_{\alpha+1} &\to& \Delta[1]
  }
  \,,
$$

where the morphisms on the left are the generators of marked anodyne morphisms (see [here](http://ncatlab.org/nlab/show/model+structure+for+Cartesian+fibrations#MarkedAnodyne)). from this one checks that if the fiber $N_\alpha \times_{\Delta[1]} \{0\}$ is equivalent to $C$, then so is $N_{\alpha +1} \times_{\Delta[1]} \{0\}$ and similarly for $D$. By induction, it follows that $f$ is indeed associated to $K \to \Delta[1]$.

To see that the $K$ obtained this way is unique up to equivalence, consider...

=--



### Cartesian fibrations over simplices {#CartOverSimplex}


... for the moment see [[Higher Topos Theory|HTT, section 3.2.2]] ...


### The universal Cartesian fibration

for the moment see

* [[universal fibration of (∞,1)-categories]]. 

## Related concepts

* [[operadic (∞,1)-Grothendieck construction]]

* [[Grothendieck construction for model categories]]

## References

The construction for $\infty$-groupoid fibrations i.e. left/right fibrations is the content of section 2.2.1, that of quasi-category fibrations i.e. Cartesian fibrations that 

* [[Jacob Lurie]], section 3.2 _[[Higher Topos Theory]]_

More on model-category theoretic construction of the $\infty$-Grothendieck construction with values in $\infty$-groupoids is in 

* {#HeutsMoerdijk13} [[Gijs Heuts]], [[Ieke Moerdijk]], _Left fibrations and homotopy colimits_ ([arXiv:1308.0704](http://arxiv.org/abs/1308.0704))

Discussion in terms of [[lax (infinity,1)-colimits]] is in

* {#GepnerHaugsengNikolaus15} [[David Gepner]], [[Rune Haugseng]], [[Thomas Nikolaus]], _Lax colimits and free fibrations in $\infty$-categories_ ([arXiv:1501.02161](http://arxiv.org/abs/1501.02161))

Section 1 of this paper reviews properties of the Grothendieck construction for quasicategories:

* [[Aaron Mazel-Gee]], _All about the Grothendieck construction_ ([arXiv:1510.03525](https://arxiv.org/abs/1510.03525))

Another review is

* Anders Jess Pedersen, Magnus Baunsgaard Kristensen, _Straightening and Unstraightening_ [(Dropbox)](https://www.dropbox.com/s/alys3wg59rir3gt/Grothendieck_construction.pdf?dl=0)

[[!redirects (∞,1)-Grothendieck construction]]