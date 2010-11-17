
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
* automatic table of contents goes here
{:toc}

## Idea

The notion of adjunction between two [[(∞,1)-functors]] generalizes the notion of [[adjoint functors]] from [[category theory]] to [[(infinity,1)-category|(∞,1)-category theory]].


There are many equivalent definitions of the ordinary notion of [[adjoint functor]]. Some of them have more evident generalizations to some parts of [[higher category theory]] than others. 

* One definition of ordinary adjoint functors says that a pair of functors $C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ is an adjunction if there is a [[natural transformation|natural isomorphism]]

  $$
    Hom_C(L(-),(-) \simeq Hom_D(-,R(-))
    \,.
  $$

  The analog of this definition makes sense very generally in [[(∞,1)-category theory]], where $Hom_C(-,-) : C^{op} \times C \to \infty Grpd$ is the $(\infty,1)$-categorical hom-object.

* One other characterization of adjoint functors  in terms of their [[cograph of a functor|cographs]]: the [[Cartesian fibration]]s to which the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-Grothendieck+construction#FibsOverInterval">functor is associated</a>. At [[cograph of a functor]] it is discussed how two functors $L : C \to D$ and $R : D \to C$ are adjoint precisely if the cograph of $L$ coincides with the cograph of $R$ up to the obvious reversal of arrows

$$
  (L \dashv R) \Leftrightarrow
  (cograph(L) \simeq cograph(R^{op})^{op})
  \,.
$$

Using the [[(∞,1)-Grothendieck construction]] the notion of cograph of a functor has an evident generalization to $(\infty,1)$-categories.



## Definition 

### In terms of hom-equivalences

+-- {: .un_defn}
###### Definition
**(in terms of hom equivalence induced by unit map)**

A pair of [[(∞,1)-functors]] 

$$ 
  C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} 
  D
$$

is an adjunction, if there exists a _unit transformation_ 
$\epsilon : Id_C \to R \circ L$ -- a morphism in the [[(∞,1)-category of (∞,1)-functors]] $Func(C,C)$ -- such that for all $c \in C$ and $d \in D$ the induced morphism

$$
  Hom_C(L(c),d)
   \stackrel{R_{L(c), d}}{\to}  
  Hom_D(R(L(c)), R(d))
  \stackrel{Hom_D(\epsilon, R(d))}{\to}
  Hom_D(c,R(d))
$$

is an equivalence of [[∞-groupoids]].

=--

In terms of the concrete incarnation of the notion of $(\infty,1)$-category by the notion of [[quasi-category]], we have that $Hom_(C)(L(c),d)$ and $Hom_D(c,R(d))$ are incarnated as [[hom-object in a quasi-category|hom-objects in quasi-categories]], which are [[Kan complexes]], and the above equivalence is a [[homotopy equivalence]] of Kan complexes.

In this form this definition appears as [[Higher Topos Theory|HTT, def. 5.2.2.7]].

### In terms of cographs

We make use here of the explicit realization of the [[(∞,1)-Grothendieck construction]] in its incarnation for [[quasi-categories]]: here an [[(∞,1)-functors]] $L : D \to C$ may be regarded as a map $\Delta[1]^{op} \to $ [[(∞,1)Cat]], which corresponds under the Grothendieck construction to a [[Cartesian fibration]] of [[simplicial sets]] $coGraph(L) \to \Delta[1]$. 

+-- {: .un_defn}
###### Definition
**(in terms of Cartesian/coCartesian fibrations)**

Let $C$ and $D$ be [[quasi-categories]]. An **adjunction** between $C$ and $D$ is 

* a morphism $K \to \Delta[1]$ of [[simplicial sets]], which is both a [[Cartesian fibration]] as well as a coCartesian fibration.

* together with [[equivalence of quasi-categories]] $C \stackrel{\simeq}{\to} K_{\{0\}}$ and $D \stackrel{\simeq}{\to} K_{\{1\}}$.

Two [[(∞,1)-functors]] $L : C \to D$ and $R : D \to C$ are called **adjoint** -- with $L$ _left adjoint_ to $R$ and $R$ _right adjoint_ to $L$ if

* there exists an adjunction $K \to I$ in the above sense

* and $L$ and $K$ are the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-Grothendieck+construction#FibsOverInterval">associated functors to</a> the Cartesian fibation $p : K to \Delta[1]$ and the Cartesian fibration $p^{op} : K^{op} \to \Delta[1]^{op}$, respectively. 

=--


## Properties

The two different definition above are indeed equivalent:

+-- {: .un_prop}
###### Proposition

For $C$ and $D$ [[quasi-categories]], the two definitions of adjunction, in terms of Hom-equivalence induced by unit maps and in terms of Cartesian/coCartesian fibrations are equivalent.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.2.8]].

First we discuss how to produce the unit for an adjunction from the data of a correspondence $K \to \Delta[1]$ that encodes an $\infty$-adjunction $(f \dashv g)$.

For that, define a morphism $F' : \Lambda[2]_2 \times C \to K$ as follows:

* on $\{0,2\}$ it is the morphism $F : C \times \Delta[1] \to K$ that exhibits $f$ as associated to $K$, being $Id_C$ on $C \times \{0\}$ and $f$ on $C \times \{2\}$;

* on $\{1,2\}$ it is the morphism $C \times \Delta[1] \stackrel{f \times Id}{\to} D \times \Delta[1] \stackrel{G}{\to} K$, where $G$ is the morphism that exhibits $g$ as associated to $K$;

Now observe that $F'$ in particular sends $\{1,2\}$ to [[Cartesian morphism]]s in $K$ (by definition of functor associated to $K$). By one of the equivalent characterizations of [[Cartesian morphism]]s, this means that the lift in the diagram

$$ 
  \array{
    \Lambda[2]_2 &\stackrel{F'}{\to}& K
    \\
    \downarrow &{}^{F''}\nearrow& \downarrow
    \\
    \Delta[2] \times C &\to & \Delta[1] 
  }
$$

exists. This defines a morphism $C \times \{0,1\} \to K$ whose components may be regarded as forming a [[natural transformation]] $u : d_C \to g \circ f$.

To show that this is indeed a unit transformation, we need to show that the maps of [[hom-object in a quasi-category]] for all $c \in C$ and $d \in D$

$$
  Hom_D(f(f), d) \to Hom_C(g(f(c)), g(d)) \to Hom_C(c, g(d))
$$

is an equivalence, hence an isomorphism in the [[homotopy category]]. Once checks that this fits into a commuting diagram

$$
  \array{
    Hom_D(f(c), d) &\to& Hom_C(g(f(c)), g(d)) &\to& Hom_C(c, g(d))
    \\
    \downarrow &&&& \downarrow
    \\
    Hom_K(C,D) &&=&& Hom_K(C,D)
  }
  \,.
$$

For illustration, chasing a morphism $f(c) \to d$ through this diagram yields

$$
  \array{
    (f(c) \to d) &\mapsto& (g(f(c)) \to g(d)) &\mapsto& 
    (c \to g(f(c)) \to g(d))
    \\
    \downarrow && && \downarrow
    \\
    (c \to g(f(c)) \to f(c) \to d)
    &&=&&
    (c \to g(f(c)) \to g(d) \to d)
  }
 \,,
$$

where on the left we precomposed with the Cartesian morphism 

$$
  \array{
    && g(f(c))
    \\
    & \nearrow &\Downarrow^{\simeq}& \searrow
    \\
    c &&\to&& f(c)
  }
$$

given by $F''|_{c} : \Delta[2] \to K$, by ...

=--

### Uniqueness of adjoints

The adjoint of a functor is, if it exists, essentially unique:

+-- {: .un_prop}
###### Proposition

If the $(\infty,1)$-functor between quasi-categoris $L : D \to C$ admits a right adjoint $R : C \to D$, then this is unique up to homotopy.

Moreover, even the choice of homotopy is unique, up to ever higher homotopy, i.e. the collection of all right adjoints to $L$ forms a [[contractible]] [[∞-groupoid]], in the following sense:

Let $Func^L(C,D), Func^R(C,D) \subset Func(C,D)$ be the full sub-quasi-categories on the [[(∞,1)-category of (∞,1)-functors]] between $C$ and $D$ on those functors that are left adjoint and those that are right adjoints, respectively. Then there is a canonical [[equivalence of quasi-categories]] 
$$
  Func^L(C,D) \stackrel{\simeq}{\to}
  Func^R(C,D)^{op}
$$

(to the [[opposite quasi-category]]), which takes every left adjoint functor to a corresponding right adjoint.

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.1.3]] (also remark 5.2.2.2), and [[Higher Topos Theory|HTT, prop. 5.2.6.2]].

=--

### Preservation of limits and colimits {#PresOfLims}

Recall that for $(L \dashv R)$ an ordinary pair of [[adjoint functor]]s, the fact that $L$ preserves [[colimit]]s (and that $R$ preserves [[limit]]s) is a formal consequence of 

1. the hom-isomorphism $Hom_C(L(-),-) \simeq Hom_D(-,R(-))$;

1. the fact that $Hom_C(-,-) : C^{op} \times C \to Set$ preserves all limits in both arguments;

1. the [[Yoneda lemma]], which says that two objects are isomorphic if all homs out of (into them) are.

Using this one computes for all $c \in C$ and diagram $d : I \to D$

$$
\begin{aligned}
  Hom_C(L(\lim_{\to} d_i), c) & \simeq 
  Hom_D(\lim_\to d_i, R(c))
  \\
  & \simeq 
  \lim_{\leftarrow} Hom_D(d_i, R(c))
  \\
  & \simeq \lim_{\leftarrow} Hom_C(L(d_i), c)
  \\
  & \simeq Hom_C(\lim_{\to} L(d_i), c)
  \,,
\end{aligned}
$$

which implies that $L(\lim_\to d_i) \simeq \lim_\to L(d_i)$.

Now to see this in $(\infty,1)$-category theory...


### Adjunctions on homotopy categories {#OnHomotopyCat}


+-- {: .un_prop}
###### Proposition

For $(L \dashv R) : C \stackrel{\leftarrow}{\to} D$ an $(\infty,1)$-adjunction, its image under decategorifying to [[homotopy category of an (infinity,1)-category|homotopy categories]] is a pair of ordinary [[adjoint functor]]s 

$$
  (Ho(L) \dashv Ho(R)) : Ho(C) \stackrel{\leftarrow}{\to} Ho(D)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 5.2.2.9]].

This follows from that fact that for $\epsilon : Id_C \to R \circ L$ a unit of the $(\infty,1)$-adjunction, its image $Ho(\epsilon)$ is a unit for an ordinary adjunction.

=--


+-- {: .un_remark}
###### Remark

The converse statement is in general false. 

One way to find  that an ordinary adjunction of homotopy categories lifts to an $(\infty,1)$-adjunction is to exhibit it as a [[Quillen adjunction]] between [[simplicial model category]]-structures. This is discussed in the Examples-section [Simplicial and derived adjunction](#SimplicialAndDerived) below.

=--


### Full and faithful adjoints

As for ordinary [[adjoint functor]]s we have that given an $(\infty,1)$-adjunction $(L \dashv R) : C \to  D$

* $R$ is a [[full and faithful (∞,1)-functor]] precisely is the counit $L R \stackrel{}{\to} Id$ is an [[equivalence of quasi-categories|equivalence]] of [[(∞,1)-functor]]s;

  In this case $C$ is a [[reflective (∞,1)-subcategory]] of $D$.

* $L$ is a [[full and faithful (∞,1)-functor]] precisely is the unit $Id \to L R$ is an [[equivalence of quasi-categories|equivalence]] of [[(∞,1)-functor]]s;


(see also [[Higher Topos Theory|HTT, p. 308]]).

### On over-$(\infty,1)$-categories {#OnSlices}



+-- {: .un_prop}
###### Proposition

Let

$$
  (L \dashv R) : D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
     C
$$

be a pair of adjoint $(\infty,1)$-functors where the $(\infty,1)$-category $C$ has all [[(∞,1)-pullback]]s. 

Then for every object $X \in C$ there is induced a pair of adjoint $(\infty,1)$-functors between the [[over-(∞,1)-categories]]

$$
  (L/X \dashv R/X) 
   : D/(L X) \stackrel{\overset{L/X}{\leftarrow}}{\underset{R/X}{\to}}
     C/X
$$

where

* $L/X$ is the evident induced functor;

* $R/X$ is the composite

  $$
    R/X : D/{L X} \stackrel{R}{\to} C/{(R L X)} \stackrel{i_{X}^*}{\to}
     C/X
  $$

  of the evident functor induced by $R$ with the [[(∞,1)-pullback]] along the $(L \dashv R)$-[[unit of an adjunction|unit]] at $X$.

=--

This is [[Higher Topos Theory|HTT, prop. 5.2.5.1]].

## Examples

### Simplicial and derived adjunctions {#SimplicialAndDerived}

A large class of examples of $(\infty,1)$-adjunctions arises from adjunctions in [[sSet]]-[[enriched category theory]], and in particular from enriched [[Quillen adjunctions]] between [[simplicial model category|simplicial model categories]].

We want to produce Cartesian/coCartesian fibration $K \to Delta[1]$ froma given [[sSet]]-[[enriched category theory|enriched]] adjunction. For that first consider the following characterization

+-- {: .un_lemma}
###### Lemma

Let $K$ be a [[simplicially enriched category]] whose [[hom-object]]s are all [[Kan complex]]es, regard the [[interval category]] $\Delta[1] := \{0 \to 1\}$ as an $sSet$-category in the obvious way using the embedding $const : Set \hookrightarrow sSet$ and consider an $sSet$-enriched functor $K \to \Delta[1]$. Let $C := K_0$ and $D := K_1$ be the $sSet$-enriched categories that are the fibers of this. Then under the [[homotopy coherent nerve]] $N : sSet Cat \to sSet$ the morphism

$$
  N(p) : N(K) \to \Delta[1]
$$

is a [[Cartesian fibration]] precisely if for all objects $d \in D$ there exists a morphism $f : c \to d$ in $K$ such that postcomposition with this morphism

$$
  C(c',f ) :  C(c',cc) = K(c',c) \to K(c',d)
$$

is a [[homotopy equivalence]] of [[Kan complex]]es for all objects $c' \in C'$.

=--

+-- {: .proof}
###### Proof

[[Higher Topos Theory|HTT, prop.  5.2.2.4]]. 

The statement follows from the characterization of [[Cartesian morphism]]s under homotopy coherent nerves ([[Higher Topos Theory|HTT, prop.  2.4.1.10]]), which says that for an $sSet$-enriched functor $p : C \to D$ between Kan-complex enriched categories that is [[hom-object]]-wise a [[Kan fibration]], a morphim $f : c' \to c''$ in $C$ is an $N(p)$-[[Cartesian morphism]] if for all objects $c \in C$ the diagram

$$
  \array{
    C(c,c') &\stackrel{C(c,f)}{\to}& C(c,c'')
    \\
    \downarrow^{\mathrlap{p_{c,c'}}} &&
    \downarrow^{\mathrlap{p_{c,c''}}}
    \\
    D(p(c),p(c')) &\stackrel{D(p(c),p(f))}{\to}&
    D(p(c), p(c''))
  }
$$

is a [[homotopy pullback]] in the [[model structure on sSet-categories]].

For the case under consideration the functor in question is $p : K \to \Delta[1]$ and the above diagram becomes

$$
  \array{
    K(c,c') &\stackrel{K(c,f)}{\to}& K(c,c'')
    \\
    \downarrow
     &&
    \downarrow    
    \\
    * &\to& *
  }
  \,.
$$

This is clearly a homotopy pullback precisely if the top morphism is an equivalence.

=--

Using this, we get the following.

+-- {: .un_prop}
###### Proposition

For $C$ and $D$ [[sSet]]-[[enriched categories]] whose hom-objects are all [[Kan complexes]], the image 

$$
  N(C) \stackrel{\overset{N(L)}{\to}}{\underset{N(R)}{\leftarrow}}
  N(D)
$$

under the [[homotopy coherent nerve]] of an [[sSet]]-enriched adjunction between $sSet$-[[enriched categories]]

$$
  C \stackrel{\overset{L}{\to}}{\underset{R}{\leftarrow}}
  D
$$

is an adjunction of [[quasi-categories]].

Moreover, if $C$ and $D$ are equipped with the structure of a [[simplicial model category]] then the quasi-categorically [[derived functors]] 

$$
  N(C^\circ) \stackrel{\overset{L}{\to}}{\underset{R}{\leftarrow}}
  N(D^\circ)
$$

form an adjunction of quasi-categories.


=--

+-- {: .proof}
###### Proof

The first part is [[Higher Topos Theory|HTT, cor.  5.2.4.5]], the second
[[Higher Topos Theory|HTT, prop. 5.2.4.6]].

To get the first part, let $K$ be the $sSet$-category which is the join of $C$ and $D$: its set of objects is the disjoint union of the sets of objects of $C$ and $D$, and the [[hom-object]]s are

* for $c,c' \in C$: $K(c,c') := C(c,c')$;

* for $d,d' \in D$: $K(d,d') := D(d,d')$;

* for $c \in C$ and $d \in D$: $K(c,d) := C(L(c),d) = D(c,R(d))$;

  and

  $K(d,c) = \emptyset$

and equipped with the evident composition operation.

Then for every $d \in D$ there is the morphism $Id_{R(d)} \in K(R(d),d)$, composition with which induced an isomorphism and hence an equivalence. Therefore the conditions of the above lemma are satisfied and hence $N(K) \to \Delta[1]$ is a [[Cartesian fibration]].

By the analogous dual argument, we find that it is also a coCartesian fibration and hence an adjunction.

For the second statement, we need to refine the above argument just slightly to pass to the full $sSet$-subcategories on fibrant cofibrant objects:

let $K$ be as before and let $K^\circ$ be the full $sSet$-subcategory on objects that are fibrant-cofibrant (in $C$ or in $D$, respectively). Then for any fibrant cofibrant $d \in D$, we cannot just use the identity morphism $Id_{R(d)} \in K(R(d),d)$ since the right Quillen functor $R$ is only guaranteed to respect fibrations, not cofibrations, and so $R(d)$ might not be in $K^\circ$. But we can use the [[small object argument]] to obtain a functorial cofibrant replacement functor $Q : C \to C$, such that $Q(R(d))$ is cofibrant and there is an acyclic fibration $Q(R(d)) \to R(d)$. Take this to be the morphism in $K(Q(R(d)), d)$ that we pick for a given $d$. Then this does induce a homotopy equivalence

$$
  C(c', Q(R(d))) \to C(c',R(d)) = K(c',d)
$$

because in an [[enriched model category]] the enriched hom out of a cofibrant object preserves weak equivalences between fibrant objects.


=--

### Localizations


A pair of adjoint $(\infty,1)$-functors $(L \dashv R) : C \stackrel{\leftarrow}{\hookrightarrow} D$ where $R$ is a [[full and faithful (∞,1)-functor]] exhibits $C$ as a [[reflective (∞,1)-subcategory]] of $D$. This subcategory and the composite $R \circ L : D \to D$ are a [[localization of an (∞,1)-category|localization]] of $D$.

## References

Section 5.2 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

[[!redirects adjoint (∞,1)-functor]]
[[!redirects adjoint (infinity,1)-functors]]
[[!redirects adjoint (∞,1)-functors]]