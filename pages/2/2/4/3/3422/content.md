<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


#Contents#
* automatic table of contents
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

between [[right fibration]]s [[fibrations of quasi-categories|of quasi-categories]] and [[(∞,1)-functor]]s to [[? Grpd]], while the full Grothendieck construction for [[(∞,1)-categories]] constitutes an equivalence 

$$
  CartFib(C) \simeq \infty Func(C^{op}, (\infty,1)Cat)
$$

between [[Cartesian fibration]]s [[fibrations of quasi-categories|of quasi-categories]] and [[(∞,1)-functor]]s to [[(∞,1)Cat]].


This correspondence is [[model category|modeled]] 

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


+-- {: .un_def}
###### Definition 
**(extracting a simplicial presheaf from a fibration)**
([[Higher Topos Theory|HTT, section 2.2.1]])

Let 

* $S$ be a [[simplicial set]], $tau_hc(S)$ the corresponding [[SSet-category]] (under the [[left adjoint]] $\tau_{hc} : SSet \to SSet Cat$ of the [[homotopy coherent nerve]]);

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

Using this construction, define a functor -- the **straightening functor** 
--

$$
  St_\phi : sSet/S \to [C^{op}, sSet]
$$

from the [[overcategory]] of [[sSet]] over $S$ to the [[enriched functor category]] of [[sSet]]-[[enriched functor]]s from $C^{op}$ to $sSet$ by defining it on objects $(p : X \to S)$ to act as

$$
  St_\phi(X) := K(\phi,p)(-,v) : C^{op} \to SSet
  \,.  
$$

This functor has a [[right adjoint]]

$$
  Un_\phi : [C^{op}, sSet] \to sSet/S
  \,,
$$

that takes a [[simplicial presheaf]] on $C$ to a simplicial set over $S$ -- this is the **unstraightening functor**.

=--

+-- {: .un_example}
###### Example 

The straightening functor effectively computes the fibers of a [[Cartesian fibration]] $(p : X \to C)$ over every point $x \in C$. As an illustration for how this is expressed in terms of morphisms in that pushout, consider the simple situation where

* $C = *$ only has a single point;

* $X = \left\{ a \to b \;\;\; c\right\}$ is a category with three objects, two of them connected by a morphism

* $p : X\to C$ is the only possible functor, sending everything to the point.

Then 

* $C^{\triangleright} = 
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



+-- {: .un_theorem}
###### Theorem 
**(presentation of $(\infty,0)$-Grothendieck construction)**


The straightening and the unstraightening functor constitute a [[Quillen adjunction]]

$$
  (St_\phi \dashv Un_\phi) : sSet/S
  \stackrel{\overset{Un_{\phi}}{\leftarrow}}{\overset{St_\phi}{\to}}
  [C^{op}, sSet]
$$

between the [[model structure for right fibrations]] and the global projective [[model structure on simplicial presheaves]] on $S$.

If $\phi$ is an equivalence in the [[model structure on simplicial categories]] then this Quillen adjunction is a [[Quillen equivalence]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 2.2.1.2]].

=--

This models the Grothendieck construction for $\infty$-groupoids in the following way:

* the [[presentable (∞,1)-category|(∞,1)-category presented by]] $sSet/S$ is $RFib(S)$
 
  (HTT, lemma 2.2.3.9)

* the [[presentable (∞,1)-category|(∞,1)-category presented by]]
  the global [[model structure on simplicial presheaves]] 
  $[C^{op}, SSet]$ is [[(∞,1)-category of (∞,1)-presheaves]] 
  $PSh_{(\infty,1)}(N_{hc}(C))$

Hence the unstraightening functor is what models the [[Grothendieck construction]] proper, in the sense of a construction that generalizes the construction of a [[fibered category]] from a [[pseudofunctor]].






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

* on the left we have the $(\infty,1)$-category of [[Cartesian fibration]]s over $C$ -- incarnated as the full [[sSet]]-[[subcategory]]
of the [[overcategory]] $sSet/C$ on [[Cartesian fibration]]s;

* and on the right the [[(∞,1)-category of (∞,1)-functors]] from $C^{op}$ to the [[(∞,1)-category of (∞,1)-categories]].

=--


In the next section we discuss how this statement is presented in terms of [[model categories]].


### Model category presentation


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

Each edge $f: d \rightarrow e$ of 
$X \in sSet/S$ gives rise to an edge in 
$St_\phi (X)(d) = K(\phi,p)(d,v)$: the 
[[join of simplicial sets|join]] 2-simplex 
$f \star v$ of $X^{\triangleright}$                

$$                                                                              
  \array{                                                                   
    d && \stackrel{f}{\to} && e                                            
    \\                                                                     
    & \searrow & \stackrel{\tilde f}{\Leftarrow} & \swarrow                                    
    \\                                                                     
    && v                                                                   
  }                                                                         
$$                                                                              

corresponds to an edge $\tilde{f} \in K(\phi,p)(d,v)=St_\phi X(d)$. 


We define the image of the straightening functor to assign that
marking of edges which is the minimal 
[[sSet]]-[[enriched functor|enriched functorial]] marking such
that with te above notation all edges of the form 
$\tilde f$ are marked in $St_\phi X(d)$, for all marked $f : c \to d$
in $X$.

The hom simplicial sets of $sSet^+$ are the spaces $Map^\sharp(X,Y)$, which consist of those simplices of the [[internal hom]] $Y^X$ whose edges are all marked. By the definition of the simplicial homs in the category of [[marked simplicial set]]s, we must also mark the edges $g^*(\tilde{f})$ defined as follows. Because $St_\phi(X)$ is a simplicial functor, each $g \in C(c,d)_1$ gives rise to a map $St_\phi(X)(d) \times \Delta^1 \rightarrow St_\phi(X)(c)$. Let $g^*(\tilde{f})$ be the 1-simplex of $St_\phi(X)(c)$ given by precomposing this map with $(\tilde{f},id) : \Delta^1 \rightarrow St_\phi(X)(d)\times \Delta^1$. An edge of $St^+_\phi(X)(c)$ is marked iff it is of the form $g^*(\tilde{f})$ for $g \in C(c,d)_1$ and $f$ a marked edge of $X$.

As before, this has an [[sSet]]-[[right adjoint]], the **unstraightening functor**

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
  \stackrel{\overset{Un_{\phi}}{\leftarrow}}{\overset{St_\phi}{\to}}
  [C^{op}, SSet^+]
$$

between the [[model structure for Cartesian fibrations]] and the projective [[global model structure on functors]] with values in the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]].


If $\phi$ is an equivalence in the [[model structure on simplicial categories]] then this Quillen adjunction is a [[Quillen equivalence]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 3.2.0.1]].

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





## Examples

### The construction over the point

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


### Cartesian fibrations over simplices {#CartOverSimplex}


... for the moment see [[Higher Topos Theory|HTT, section 3.2.2]] ...


### The universal Cartesian fibration

for the moment see

* [[universal fibration of (∞,1)-categories]]. 



[[!redirects (∞,1)-Grothendieck construction]]