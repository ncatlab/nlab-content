
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The notion of  _reflective $(\infty,1)$-subcategory_ is the generalization of the notion of [[reflective subcategory]] from [[category theory]] to [[(∞,1)-category]] theory.

## Definition 


### Reflective sub-$(\infty,1)$-category

+-- {: .num_defn}
###### Definition
**(local objects, local equivalences)**


A [[full and faithful (∞,1)-functor]]

$$
  R : D \hookrightarrow C
$$

exhibits $D$ as a **reflective [[sub-(∞,1)-category]]** (of $C$) if it has a left [[adjoint (∞,1)-functor]] $L : C \to D$.

$$
  (L \dashv R) : D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}}
  C
  \,.
$$

If $L$ moreover is a left [[exact functor]] in that it preserves [[finite limit|finite]] [[(∞,1)-limits]], then the embedding is called **exact**.

=--


The [[(∞,1)-functor]] $R$ or its composite 

$$
  Loc := R \circ L : C \to C
$$ 

may be understood as exhibiting a [[localization of an (∞,1)-category|localization]] of $C$ at those morphisms that $L$ sends to [[equivalence in an (∞,1)-category|equivalence]]s in $D$. If $L$ preserves [[finite limit]]s (is a left [[exact functor]]), then this is an **exact localization**


### Local objects and local morphisms {#LocalObjects}

One finds, as discussed [below](#Properties), that reflective subcategories may be entirely characterized by the class of morphisms that the localization functor $Loc : C \to C$ sends to weak equivalences.


+-- {: .num_defn}
###### Definition
**(local objects, local equivalences)**

Let $S \subset Mor(C)$ be a class of morphisms. 

* An object $c \in C$ is called an **$S$-[[local object]]** if for all morphisms $f : x \to y$ in $S$ the induced morphism

  $$
    Hom_C(f,c) : Hom_C(y,c) \to Hom_C(x,c)
  $$

  is an equivalence (of [[∞-groupoid]]s).

* An morphism $f : x \to y$ in $C$ is called an **$S$-[[local morphism]]** or **$S$-[[local equivalence]]** if for all $S$-[[local object]]s $c  \in C$ we have that 

  $$
    Hom_C(f,c) : Hom_C(y,c) \to Hom_C(x,c)
  $$

  is an equivalence (of [[∞-groupoid]]s).


=--

Notice that the class of $S$-equivalences always contains $S$ itself. Hence passing from a collection $S$ to its class $\bar S$ of $S$-equivalences is a kind of saturation procedure. This is formalized by the following definition, whose justification is given by the propositions [below](#Properties).

+-- {: .num_defn}
###### Definition
**(strongly saturated class of morphisms)**


For $C$ an [[(∞,1)-category]] with small [[(∞,1)-colimits]], a class $S \subset C_1$ of morphisms in $C$ is said to be **strongly saturated** if its satisfies the following three conditions

1. It is stable under [[pushout]]s along arbitrary morphisms of $C$;

1. The full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] $Func(\Delta[1], C)$ on $S$ has all [[(∞,1)-colimit]]s;

1. it satisfies the 
   [[category with weak equivalences|2-out-of-3 property]].

=--

Notice that this definition has some immediate consequences:

The identity $Id_\emptyset$ on the [[initial object]] of $C$, which is the initial object in $Func(\Delta[1],C)$ is in $S$, since it is the colimit of the empty diagram. Moreover, every [[equivalence in an (∞,1)-category|equivalence]] is a [[pushout]] of $Id_{\emptyset}$ so

* A strongly saturated class contains every [[equivalence in an (∞,1)-category|equivalence]].

Given any collection $\{S_i\}_i$ of strongly saturated classes of morphisms in $C$, their intersection is clearly also strongly saturated. Therefore for every collection $S$ of morphisms, there is a smallest strongly saturated class $\bar S$ containing it. We say that $S$ **generates** the strongly saturated class $\bar S$. If $S$ is a [[small set]], then $\bar S$ is said to be **of small generation**. 

The smallest strongly saturated class of morphism in $C$ is that containing only the equivalences of $C$.

Of importance are the strongly saturated classes arising as follows.

+-- {: .num_lemma}
###### Lemma


For $C$ and $D$ two $(\infty,1)$-categories that have small [[(∞,1)-colimit]]s, and for $F : C \to D$ an [[(∞,1)-functor]] that preserves small $(\infty,1)$-colimits, given a strongly saturated class of morphisms $S$ in $D$, its preimage $F^{-1}(S)$ is a strongly saturated class in $C$.


In particular the class of morphisms in $C$ sent to equivalences by $F$ is strongly saturated.

=--


+-- {: .num_lemma}
###### Lemma

The class of $S_0$-[[local equivalence]]s for $S_0$ any class of morphisms is strongly saturated.

=--

+-- {: .proof}
###### Proof


For each object $c \in C$ let $j(c) : C \to \infty Grpd^{op}$ be the functor [[representable functor|represented]] by $c$. Let $S_c$ be the class of morphisms sent by $j(c)$ to weak equivalences in [[∞Grpd]]. Since $j(c)$ preserves small colimits, this is a strongly saturated class, by the above lemma. Now observe that $S$ is the intersection $S = \cap_c S_c$ where $c$ ranges over the $S_0$-[[local object]]s.

=--


In the following this language of local morphisms is used to characterize reflective $(\infty,1)$-subcategories.


## Properties {#Properties}

### Characterization of reflectors
 {#CharacterizationOfReflectors}

The following proposition characterizes the _reflectors_ of a reflective $(\infty,1)$-subcategory. (You may read this proposition as the characterization of [[adjoint functors]] via [[universal arrows]] (via [this prop.](adjoint+functor#CollectionOfUniversalArrowsEquivalentToAdjointFunctor)), but maybe as a preparation for the proofs to come there is some value in looking at its concrete proof in this special case of an $(\infty,1)$-adjunction.)
 
+-- {: .num_lemma #UniversalityOfReflectionCounit}
###### Lemma
**(universality of reflection counit)**

Let $C$ be an [[(∞,1)-category]] and $D \hookrightarrow C$ a full [[sub-(∞,1)-category]]. Then this inclusion has a left [[adjoint (∞,1)-functor]] precisely if 

* for every object $c \in C$ there is a _localization_ or _reflection_: a morphism $f : c \to \bar c$ such that $\bar c \in D\hookrightarrow C$ and such that for all $e \in D \hookrightarrow C$ we have that 

  $$
    Hom_C(f,e) : Hom_C(\bar c,e) \to Hom_C(c,e)
  $$

  is an equivalence (of [[∞-groupoid]]s).

=--

This appears as [[Higher Topos Theory|HTT, prop. 5.2.7.8]].

+-- {: .proof}
###### Proof

We produce an evident [[cograph of a functor|cograph]] realization $K$ of the inclusion and check that it being also a [[coCartesian fibration]], hence exhibiting $R$ as a right adjoint, is equivalent to the second statement.

Let $K \subset C \times \Delta[1]$ be the full subcategory on those objects $(c,i)$ for which $c \in D$ if $i = 1$. Let $p : K \to \Delta[1]$ be the induced projection.  One checks that this is the correspondence which is <a href="http://ncatlab.org/nlab/show/(infinity,1)-Grothendieck+construction#FibsOverInterval">associated to the inclusion functor</a> $D \hookrightarrow C$. 

Therefore by the properties of [[adjoint (∞,1)-functor]]s, we have that the inclusion functor has a left adjoint precisely if $p$ is not only a [[Cartesian fibration]] but also a [[coCartesian fibration]].

To see that this is the case precisely if every $c$ has a reflection $f : c \to d$, recall the characterization of [[coCartesian morphism]]s $\tilde f : (c,0) \to (d,1)$ as those making the squares

$$
  \array{
    Hom_K((d,1),(e,i)) &\stackrel{Hom_K(\tilde f,(e,i))}{\to} & Hom_K((c,0),(e,i))
    \\
    \downarrow && \downarrow
    \\
    Hom_{\Delta[1]}(1, i)
    &\stackrel{}{\to}&
    Hom_{\Delta[1]}(0, i)
  }
$$

being [[homotopy pullback]] squares, for all $(e,i) \in K$. Now in $\Delta[1]$ all [[hom-object in a quasi-category|hom-objects]] are either empty or are points, so that the bottom morphism becomes the identity on the point if $i = 1$. Since for $i = 0$ everything becomes entirely trivial we consider the case that $i =1$ and hence $e \in D$.

In that case the homotopy-pullback property is equivalent to the top morphism being an equivalence, hence to

$$
    Hom_C(d,e) \stackrel{Hom_C(f,e)}{\to}  Hom_C(c,a)
$$

being an equivalence. This way the reflectors are identified precisely with the coCartesian morphisms in $K \to \Delta[1]$ that exhibit the left [[adjoint (∞,1)-functor]] to the inclusion functor.


=--



The following proposition asserts that localizations are entirely determined by the corresponding [[local object]]s.

+-- {: .num_prop}
###### Proposition

Let 

$$
  D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}} C
$$

be a localization of the $(\infty,1)$-category $C$ and let 

$$
  Loc : C \stackrel{L}{\to} D \overset{R}{\hookrightarrow} C
$$

be the corresponding localization [[(∞,1)-monad]]. Write $S \subset Mor(C)$ for the collection of morphisms that $Loc$ sends to [[equivalence in an (∞,1)-category|equivalences]].

Then

* an object $c \in C$ is an $S$-[[local object]] precisely if it is in the essential image of $Loc$ (equivalent to an object of the form $Loc x$);

* every $S$-[[local morphism]] is already in $S$.



=--

This is [[Higher Topos Theory|HTT, prop 5.5.4.2]].

+-- {: .proof}
###### Proof


The reasoning is entirely analogous to the 1-categorical case (see for instance [[localization]], [[reflective subcategory]] and [[geometric embedding]]).


First notice that because $D \hookrightarrow C$ is a [[full and faithful (∞,1)-functor]] we have that the counit $L R \stackrel{\simeq}{\to} Id_D$ is an equivalence. From this it follows that precomposition with the unit $i_z : z \to Loc z$ of morphisms in the image of $Loc$ is a weak equivalence: for all $z,x \in C$ we have

$$
    Hom_C(i_z, Loc z)
    :
    Hom_C(Loc z, Loc x)
    \stackrel{\simeq}{\to}
    Hom_C(z, Loc x)
  \,.
$$

If $z$ is itself in the image of $Loc$, then this means that precomposition with the unit $z \to Loc z$ is an isomorphism on [[hom-set]]s in the [[homotopy category of an (infinity,1)-category|homotopy category]] of $Loc C$, hence by the [[Yoneda lemma]] is itself an isomorphism in the homotopy category, hence $i_z : z \to Loc z$ is a weak equivalence if $z$ is itself in the image of $Loc$.

Applying this statement to the naturality square for the [[natural transformation]] $Id \to Loc$ on $i_s$

$$
  \array{
    s &\stackrel{i_s}{\to} & Loc s
    \\
    \downarrow^{\mathrlap{i_s}} && \downarrow^{\mathrlap{Loc i_s}}
    \\
    Loc s &\stackrel{i_{Loc s}}{\to}& Loc Loc s
  }
$$

we find that $Loc i_s \simeq i_{Loc s}$, hence that $Loc i_s$ is a weak equivalence, and hence that $i_s$ is in $S$, for all $s \in C$.

Now to show that for all $x \in X$ the object $Loc x$ is $S$-local, let $f : y \to z$ be in $S \subset Mor(C)$ and consider the induced square

$$
  \array{
    Hom_C(Loc z, Loc x) &\stackrel{\simeq}{\to}& Hom_C(Loc y, Loc x)
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_C(z, Loc x) &\to& Hom_C(y, Loc x)
  }
  \,.
$$

Here the vertical morphisms are equivalences by the above remark, and the top morphism is an equivalence by the assumption that $f$ in in $S$. It follows that the bottom morphism is an equivalence. This says that $Loc x$ is $S$-local, for all $x \in C$.

Conversely, to show that for $s \in C$ an $S$-local object, we have that $s$ is in the essential image of $Loc$ use that since $i_s : s \to Loc s$ is in $S$, we have an equivalence  $Hom_C(i_s, s) : Hom_C(Loc s, s) \stackrel{\simeq}{\to} Hom_C(s,s)$.  The pre-image of the identity under this equivalence is hence a left-inverse $Loc s \to s$ of $s \to Loc s$. But this means that $Loc s \to s$ is itself in $S$ (since the morphisms in $S$ evidently satisfy [[category with weak equivalences|2-out-of-three]]), hence by applying the same argument again, we find that the left inverse $Loc s \to s$ has itself a left inverse. That implies that it is actually an inverse of $s \to Loc s$, hence that this is an equivalence. So this shows that the $S$-local $s$ is indeed in the essential iamge of $Loc$.


Finally, to show that every $S$-local morphism is already in $S$, let $f : x \to y$ be such an $S$-local morphism and consider the square

$$
  \array{
    x &\stackrel{f}{\to}& y
    \\
    \downarrow^{\mathrlap{i_x}} && \downarrow^{\mathrlap{i_y}}
    \\
    Loc x &\stackrel{Loc f}{\to}& Loc y
  }
  \,.
$$

By the above we know now that the vertical morphisms here are also $S$-local. It follows that the image of $Loc f : Loc x \to Loc y$ on the homotopy category of $Ho(Loc C)$ corepresents an isomorphism, hence by the [[Yoneda lemma]] that $Lof f$ is a weak equivalence. Hence $f$ is indeed in $S$.


=--

### Reflective localization at a set of morphisms

Above is discussed that every reflective subcategory is the localization at the collection local morphisms, those which the left adjoint functor inverts.
One can turn this around and define or construct reflective $(\infty,1)$-subcategories by specifying collections of local morphisms.


+-- {: .num_prop #LocalizationProposition}
###### Proposition
**(localization proposition)**

Let $C$ be a [[presentable (∞,1)-category]] and $S_0$  be a [[small set]] of morphisms of $C$. 

Then the full [[sub-(∞,1)-category]] 

$$
  R : D \hookrightarrow C
$$ 

on $S_0$-[[local object]]s is a reflective $(\infty,1)$-subcategory. 

If $L : C \to D$ denotes the left [[adjoint (∞,1)-functor]] of the inclusion, then for $f \in Mor(C)$ a morphism, the following are equivalent

1. $f$ is an $S_0$-[[local equivalence]];

1. $f$ belongs to the strongly saturated class $S$ generated by $S_0$;

1. the morphism $L f$ is an equivalence.


=--

This is [[Higher Topos Theory|HTT, prop. 5.5.4.15]].

The main ingredient in the proof of this assertion is the following lemma, whose proof we give below in [Proof of the localization lemma](#ProofOfLocalization).


+-- {: .num_prop}
###### Proposition
**(localization lemma)**

Let $C$ be a [[locally presentable (∞,1)-category]], and let $S \subset Mor(C)$ be a strongly saturated collection of morphisms, generated from a [[small set]] $S_0$. 

Then for every object $c \in C$ there exists a reflector, i.e. a morphism  $f : c \to d$ such that $d$ is an $S$-[[local object]] and $f \in S$.

=--

With that in hand we look at the proof of the above proposition:

+-- {: .proof}
###### Proof 
(localization proposition)

The localization lemma gives for each object $c \in C$ a reflector $f : c \to d$ with $d$ $S$-local. By lemma \ref{UniversalityOfReflectionCounit}, this already gives the reflective embedding

$$
  D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}} C
$$

of the full subcateory of $S$-local objects in $C$.

It remains to prove the statements about the role of $S$ in the localization:

First, by one of the above lemmas, we have that the $S_0$-local equivalences are a strongly saturated class of morphisms containong $S_0$. Hence they in particular contain $S$. So the second claim implies the first. 

That the first and the third condition are equivalent follows from noticing that for any local object $d \in D$  the morphism $Hom_C(f,R d)$ is an equivalence precisely if $Hom_D(L f, d)$ is and then applying the [[Yoneda lemma]] (for instance in the [[homotopy category of an (infinity,1)-category|homotopy category]]), which implies that if a morphism produces an equivalence when hommed into all objects, then it is itself an equivalence.

It remains to show that the third item implies the second. Let $f : c \to d$ be a morphism such that $L f : L c \to Ld$ is an equivalence. Consider the commuting triangle

$$
  \array{
    c &\stackrel{f}{\to}& d
    \\
    \downarrow &\searrow& \downarrow
    \\
    L c &\stackrel{L f}{\to}& L d
  }
  \,.
$$


Since every reflector is in $S$ and the reflectors are the units of the reflective adjunction constructed from them, we have that the vertical morphisms in this diagram are in $S$, and the bottom morphism is, since it is an equivalence by assumption. By applying the 2-out-of-3 property of $S$ twice it follows that $f$ is in $S$.

=--



### Proof of the localization lemma {#ProofOfLocalization}

We here spell out the proof of 

+-- {: .num_prop}
###### Proposition
**(localization lemma)**

Let $C$ be a [[locally presentable (∞,1)-category]], and let $S \subset Mor(C)$ be a strongly saturated collection of morphisms, generated from a [[small set]] $S_0$. 

Then for every object $c \in C$ there exists a reflector, i.e. a morphism  $f : c \to d$ such that $d$ is an $S$-[[local object]] and $f \in S$.

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.5.14]]. 

+-- {: .proof}
###### Proof

Regard all $(\infty,1)$-categories as [[quasi-categories]] for the purpose of this proof. Write $D \subset Func(\Delta[1], C)$ for the full sub-quasicategory on the elements of $S$.  Consider the [[pullback]] (in [[sSet]])

$$
  \array{
    D_c &\to& D
    \\
    \downarrow && \downarrow
    \\
    \{c\} &\to& Func(\{0\}, C)
  }
  \,.
$$

Since $S$ is by assumption closed under pushouts in $C$, we have for each morphism $x \to y$ in $D \simeq Func(\{0\}, C)$ and each lift 

$$
  \array{
    x &\to& y
    \\
    \downarrow
    \\
    x'
  }
$$

of its source to $Func(\Delta[1], C)$ a lift of this morphism with this source, given by the the pushout square

$$
  \array{
    x &\to& y
    \\
    \downarrow && \downarrow
    \\
    x' &\to& x' \coprod_x y
  }
$$

in $C$, regarded as a morphism in $Func(\Delta[1], C)$. By the universality of the pushout, one finds that this is a [[coCartesian morphism|coCartesian lift]]. Hence $D \to Func(\{0\}, C) \simeq C$ is a [[coCartesian fibration]]. Moreover, by the [behaviour under pullback](http://ncatlab.org/nlab/show/Cartesian+fibration#BehaviourUnderPullback) of [[Cartesian fibration]]s it follows that the above diagram is a [[homotopy pullback]] diagram in the [[model structure for quasi-categories|Joyal model structure]] $sSet_{Joyal}$.


Use now that [[accessible (infinity,1)-category|accessible quasi-categories]] are stable under [[homotopy pullback]] to conclude that $D_c$ is accessible. Moreover, one can check that $D_c$ has all small colimits. Together this means that $D_c$ is a [[locally presentable (∞,1)-category]].  This implies in particular that $D_c$ also has all small [[(∞,1)-limits]] and hence contains a [[terminal object in a quasi-category|terminal object]], $f : c \to d$.

We now complete the proof by showing that $f : c \to d$ being terminal in $D_c$ implies that $d$ is an $S$-local object. This is equivalent to showing that for $t : a \to b$ any element in $S$, composition with $t$ induces an equivalence

$$
  Hom_C(t,d) : Hom_C(b,d) \to Hom_C(a,d)
  \,.
$$

This in turn may be checked [by](http://ncatlab.org/nlab/show/fiber+sequence#CharOfEquivalences) checking that all its [[homotopy fiber]]s are [[contractible]]. By general statements about the [homotopy fiber of functor categories](http://ncatlab.org/nlab/show/fiber+sequence#OfFuncCats) the homotopy fiber of $Hom_C(t,d)$ over a point $g : a \to d$ of $Hom_C(a,d)$ is equivalent to the [[hom-object in a quasi-category|hom-object]] $Hom_{C_{a/}}(t,g)$ in the [[over quasi-category|under-quasi-category]] $C_{a/}$. 

This in turn can be checked to be equivalent to $Hom_{C_{d/}}(g_* t, Id_d)$, where $g_* t$ is the $(\infty,1)$-categorical pushout

$$
  \array{
    a &\stackrel{t}{\to}& b
    \\
    \downarrow^{\mathrlap{g}} && \downarrow 
    \\
    d &\underset{g_* t}{\to}& d \coprod_a b
  }
$$

in $C$. Notice that $g_* t$, being a pushout of $t \in S$, is itself in $S$. 

Now pick a composite

$$
  \array{
    && d
    \\
    & {}^{\mathllap{f}}\nearrow &\Downarrow^\sigma& \searrow^{\mathrlap{g_* t}}
    \\
    c &&\underset{g_* t \circ f}{\to}&& d \coprod_a b
  }
$$

and observe that we have an isomorphism of simplicial sets

$$
  Hom_{C_{d/}}(g_* t, Id_{d})
  \simeq
  Hom_{C_{f/}}(\sigma, s_1(f))  
$$

(where $s_1$ is the corresponding degeneracy map).

Applying the expression for [homotopy fibers of functor categories](http://ncatlab.org/nlab/show/fiber+sequence#OfFuncCats) once again, this is found to be the homotopy fiber of

$$
  Hom_{C_{c/}}(g_* t \circ f, f)
  \to 
  Hom_{C_{c/}}(f,f)  
  \,,
$$

because $Hom_{(C_{c/})_{f/}}(\sigma , s_1(f)) = Hom_{C_{f/}}(\sigma , s_1(f))$.


Finally we can use that $f$ is terminal in the full subcategory $D_c$ of $C_{c/}$ that contains $g_* t \circ f$. This implies that the above morphism goes between [[contractible]] $\infty$-groupoids and hence has contractible homotopy fibers. 


=--

### Transport of reflective subcategories
 {#TransportOfReflectiveSubcategories}

+-- {: .num_prop #TransportOfReflectionAlongAdjunction}
###### Proposition

Let $f \colon \mathcal{C} \to \mathcal{D}$ be an [[(∞,1)-functor]] between [[presentable (∞,1)-categories]], and let $\mathcal{C}^0 \hookrightarrow \mathcal{C}$ be a reflective sub-$(\infty,1)$-category. If $f$ has a [[right adjoint|right]] [[adjoint (∞,1)-functor]] $f^*$, then 

$$
  \mathcal{D}^0 \coloneqq (f^*)^{-1}(\mathcal{C}^0) \hookrightarrow \mathcal{D}
$$

is also a reflective sub-$(\infty,1)$-category.

$$
  \array{
    \mathcal{C}^0 &\hookrightarrow& \mathcal{C}
    \\
    {}^{\mathllap{f^*}}\uparrow 
   && {}^{\mathllap{f^*}}\uparrow\downarrow^{\mathrlap{f}}
    \\
    \mathcal{D}^0 &\hookrightarrow& \mathcal{D}
  }
  \,.
$$

=--

This is ([Lurie, lemma 5.5.4.17](#Lurie)).

+-- {: .proof}
###### Proof

By prop. \ref{LocalizationProposition}, $\mathcal{C}^0 \hookrightarrow \mathcal{C}$ is the inclusion of the $S$-[[local objects]] for some class $S$ of morphisms of $\mathcal{C}$. By adjunction it follows that $\mathcal{D}^0$ is precisely the class of $f(S)$-[[local objects]], and hence is a reflective subcategory, again by prop. \ref{LocalizationProposition}.

=--

### Model category presentation
 {#ModelCategoryPresentation}

+-- {: .num_prop }
###### Proposition

Let $C$ be a [[left proper model category|left proper]] [[combinatorial simplicial model category]] which [[presentable (∞,1)-category|presents]] an [[(∞,1)-category]] $\mathcal{C} \simeq C^\circ$. 

Then if $\mathcal{C}^0 \hookrightarrow \mathcal{C}$ is an [[accessible (∞,1)-functor|accessible]] reflective inclusion with reflector $L \colon \mathcal{C} \to \mathcal{C}^0$, then there exists a corresponding [[Bousfield localization of model categories|left Bousfield localization]]

$$
  C' \stackrel{\overset{id}{\leftarrow}}{\underset{id}{\to}}
  C
$$

of the [[model category]] $C$ which presents this inclusion in that

1. an object in $C'$ is a [[fibrant object]] precisely if it is fibrant as an object of $C$ and in addition its image in the [[homotopy category]] $Ho(C) \simeq Ho(\mathcal{C})$ is in the inclusion $Ho(\mathcal{C}^0) \hookrightarrow Ho(\mathcal{C})$;

1. a morphism in $C'$ is a [[weak equivalence]] precisely if under $Ho(L) \colon Ho(C) \simeq Ho(\mathcal{C}) \to Ho(\mathcal{C}^0)$ is an [[isomorphism]].

=--

This is ([Lurie, prop. A.3.7.8](#Lurie)).

+-- {: .proof}
###### Proof

Use that by the above discussion $\mathcal{C}^0$ is the full subcategory on $S$-[[local objects]] for a [[small set]] of morphisms. By the discussion at [[Bousfield localization of model categories]] this presents precisely such localizations.

=--

## Extra conditions
 {#ExtraConditions}

Extra conditions on a reflective sub-$(\infty,1)$-category of relevance are

* _[Accessible reflective subcategories](#AccessibleReflectiveSubcategory)_

* _[Exact reflective subcategories](#ExactLocalizations)_

### Accessible reflective subcategories
 {#AccessibleReflectiveSubcategory}

The following proposition characterizes when a reflective subcategory of an [[accessible (∞,1)-category]] $C$ is accessible


+-- {: .num_prop #LocalizationAndAccessibility}
###### Proposition

Let $C$ be an [[accessible (∞,1)-category]] and 

$$
  D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}}
  C
$$

a reflective subcategory.  Then the following conditions are equivalent:

1. $D$ is itself accessible;

1. The localization $Loc : R\circ L : C \to C$ is an [[accessible (∞,1)-functor]].

1. There exists a [[small set]] $S_0 \subset S := L^{-1}(equiv.)$ such that every $S$-[[local object]] is also $S_0$-local.

=--


This is ([Lurie, prop. 5.5.1.2 and prop. 5.5.4.2, part 3](#Lurie)).

+-- {: .proof}
###### Proof

This is work...

=--


### Exact localizations 
 {#ExactLocalizations}

Recall that the reflective subcategory $D \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow} C$ is **exact** -- or $L$ an **exact localization** -- if $L$ is a left [[exact functor]] in that it preserves [[finite limit|finite]] [[limit in a quasi-category|limits]]. Accordinly we say:

+-- {: .num_defn}
###### Definition

An **exact reflective sub-$(\infty,1)$-category** is a reflective sub-$(\infty,1)$-category whose reflector is a [[left exact (∞,1)-functor]], hence preserves [[finite limit|finite]] [[(∞,1)-limits]].

=--

Recall also that by the above results, a reflective subcategory is characterized by the collection $S = L^{-1}(equiv) \subset Mor(C)$ of those morphisms, that $L$ sends to equivalences in $D$.



The following propositions say how the property that $L$ preserves finite limits is characterized by pullback-stability properties of $S$.

+-- {: .num_prop}
###### Proposition
**(recognition of exact localization)**


A reflective sub-$(\infty,1)$-category 
$D \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow} C$
such that $C$ has all finite [[limit in a quasi-category|limits]]
is exact precisely if the collection $S := L^{-1}(equiv) \subset Mor(C)$ of morphisms that $L$ sends to equivalences is stable under [[pullback]].

So if for every pullback diagram

$$
  \array{
     X' &\to& X
     \\
     \downarrow^{\mathrlap{f'}} && \downarrow^{\mathrlap{f}}
     \\
     Y' &\to& Y
  }
$$

we have that if $L(f)$ is an equivalence then also $L(f')$ is
an equivalence.

=--

This is [[Higher Topos Theory|HTT, prop. 6.2.1.1]].

+-- {: .proof}
###### Proof

If $L$ preserves [[finite limit]]s, then it preserves [[pullback]]s,
so that $L(f')$ is a pullback of the equivalence $L(f)$, hence itself
an equivalence.

So it remains to check that, conversely, stability of $S$ under pullback
implies that $L$ preserves [[finite limits]]. By a general characterization of left [[exact functor]]s (see there) it suffices to check that $L$ preserves the [[terminal object]] and all [[pullback]]s.

Since the terminal object is evidently $S$-local, we have $L * \simeq *$.

Next we check that $L$ preserves [[product]]s, because we will need this to show that all binary pullbacks are preserved. For that it is sufficient to check that the morphism $L(x \times y) \to L(x) \times L(y)$ induced from the units $i_x : x \to L x$ and $i_y : y \to L y$ is in $S$. From inspection of the diagram

$$
  \array{
    x &\stackrel{i_x}{\to}& L x
    \\
    \uparrow && \uparrow
    \\
     x \times y &\stackrel{(i_x,Id)}{\to}& L x \times y
    \\
    \downarrow && \downarrow
    \\
    y &\stackrel{Id}{\to}& y
  }
$$

one finds that $x \times y \to L x \times L y$ is a [[pullback]] of $i_x$. Hence is in $S$, by assumption. Similarly in

$$
  \array{
    L x &\stackrel{Id}{\to}& L x
    \\
    \uparrow && \uparrow
    \\
    L x \times y &\to& L x \times L y
    \\
    \downarrow && \downarrow
    \\
    y &\stackrel{i_y}{\to}& L y
  }
$$

one see that $L x \times y \to L x \times L y$ is a pullback of $i_y$ and hence in $S$. The composite of these two morphisms is a morphism $x \times y \to L x \times L y$, which is in $S$ since $S$ is closed under composition. Applying $L$ hence yields an equivalence $L(x \times y) \stackrel{\simeq}{\to} L x \times L y$.

We now apply the same kind of argument to show that $L$ respects more generally pullbacks.

For that, first notice that for $x \to y \leftarrow z$ a diagram in $C$, the pullback $L x \times_{L_y} L_z$ of the image exists in $C$, by assumption, but is easily seen to be $S$-local and hence lands in $D$. Therefore to show that we have an equivalence $L(x \; \times_y z) \simeq L x \; \times_{L y} \times L z$ it is sufficient to show that the natural morphism, $x \times_y z \to L x \times_{L y} L z$ induced from the morphism of diagrams

$$
  \array{
    x &\stackrel{i_x}{\to}& L x
    \\
    \downarrow && \downarrow
    \\
    y &\stackrel{i_y}{\to}& L y
    \\
    \uparrow && \uparrow
    \\
    z &\stackrel{i_z}{\to}& L z
  }
$$

in $C$ with the adjunction unit morphism  on the horizonatals, is in $S$. By passing along these units one at a time

$$
  \array{
    x &\stackrel{Id}{\to}& x &\stackrel{i_x}{\to}& L x
    &\stackrel{Id}{\to}&
    L x
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{i_y f}} && 
    \downarrow^{L f}
    &&
    \downarrow^{L f}
    \\
    y &\stackrel{i_y}{\to}& L y &\stackrel{Id}{\to}& L y
    &\stackrel{Id}{\to}&
    L y
    \\
    \uparrow_{\mathllap{g}} && \uparrow_{\mathrlap{i_y g}} 
    && 
    \uparrow_{\mathrlap{i_y g}} && \uparrow_{\mathrlap{L g}}
    \\
    z &\stackrel{Id}{\to}& z &\stackrel{Id}{\to}& z
    &\stackrel{i_z}{\to}&
    L z
  }
$$

this may be decomposed as a composite of three morphisms

$$
  x \times_y z \to x \times_{L y} z 
  \to L x \times_{L y} z \to  
  L x \times_{L y} L z
  \,.
$$

If we equivalently reformulate these [[pullback]]s as [[equalizer]]s then this is

$$
  \array{
    x \times_y z
    &\to&
    x \times z
    &
    \stackrel{\overset{g p_2}{\to}}{\underset{f p_1 }{\to}}
    &
    y
    \\
    \downarrow && \downarrow^{\mathrlap{Id}} && 
    \downarrow^{\mathrlap{i_y}}
    \\
    x \times_{L y} z
    &\to&
    x \times z
    &\stackrel{\overset{i_y f}{\to}}{\underset{i_y g}{\to}}&    
    L y
    \\
    \downarrow && \downarrow^{\mathrlap{(i_x, Id)}} &&  \downarrow^{Id}
    \\
    L x \times_{L y}  z
    &\to&
    L x \times z
    &\stackrel{\overset{L f}{\to}}{\underset{i_y g}{\to}}&    
    L y
    \\
    \downarrow && \downarrow^{\mathrlap{(Id, i_z)}}   
    && \downarrow^{\mathrlap{Id}}
    \\
    L x \times_{L y} L z
    &\to&
    L x \times L z
    &\stackrel{\overset{L f}{\to}}{\underset{L g}{\to}}&        
    L y
  }
$$

It is immediate to check that the two bottom left squares are [[pullback]] squares. So the two left vertical morphisms are pullbacks of $(Id, i_z)$ and $(i_x, Id)$, respectively. Of morphisms of this form we had seen above that they are in $S$. Hence by the assumed pullback-stability of $S$ also $x \times_{L y} z \to L x \times_{L y} z \to L x \times_{L y} L z$ is in $S$.


So it remains to show that $x \times_y z \to x \times_{L y} z$ is in $S$. 
We claim that this morphism in turn may be expressed as a pullback 

$$
  \array{
    x \times_y z &\to& y
    \\
    \downarrow && \downarrow
    \\
    x \times_{L y} z &\to& \times_{L y} y
  }
$$

of the diagonal $y \to y \times_{L y} y$. To see this notice that cones $q$ over the corresponding pullback diagram are equivalently diagrams

$$
  \array{
     &&  q
     \\
     & \swarrow &\downarrow& \searrow
     \\
     x &\to& y &\leftarrow& z
     \\
     & \searrow &\downarrow& \swarrow
     \\
     && L y
  }
  \,.
$$

So now we need to show that the diagonal $y \to y \times_{L y} y$ is in $S$. 

To see this, notice that it has a left inverse $y \times_{L y} y \to y$, given by any one of the two projections. So if finally we show that _this_ is in $S$, we are done, since $S$ satisfies 2-out-of-3. But this follows now from pullback stability of $S$, because this projection is the pullback of $y \to L y$ along itself.

=--


+-- {: .num_prop}
###### Proposition
**(accessibility of exact localizations)**

Let $C$ be a [[locally presentable (∞,1)-category]] with [[universal colimits]]. Assume moreover that finite limits commute with filtered colimits in $C$ (this holds for example if $C$ is an [[(∞,1)-topos]]). Let $S_0 \subset Mor(C)$ be a small set of morphisms, and $S$ the smallest strongly saturated class containing $S_0$ and stable under pullbacks. Then $S$ is strongly generated by a small set of morphisms.

=--

This is [[Higher Topos Theory|HTT, Prop. 6.2.1.2]]. This proposition is used to construct pullbacks of [[(∞,1)-topoi]], c.f. [[HTT|HTT Prop. 6.3.4.6]].

## Examples {#Examples}

### Inclusion of the terminal object

If $C$ has a [[terminal object in a quasi-category|terminal object]], then the full subcategory on terminal objects is a reflective subcategory of $C$.


### coCartesian fiber over a reflective subcategory



+-- {: .num_prop}
###### Proposition

let $p : C_1 \to C_0$ be a [[coCartesian fibration]] and $D_0 \stackrel{\leftarrow}{\hookrightarrow} C_0$ a reflective $(\infty,1)$-subcategory of the base. 

The restriction $D_1 \hookrightarrow C_1$ of $C_1$ over $D_0$, i.e. the strict (say in [[sSet]] if everything is modeled by [[quasi-categories]]) pullback

$$
  \array{
    D_1 & \stackrel{}{\hookrightarrow} & C_1
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    D_0 &\hookrightarrow& C_0
  }
$$

is itself a reflective $(\infty,1)$-subcategory of $C_1$.


=--

+-- {: .proof}
###### Proof

By the above proposition on reflectors, it is sufficient to produce for every $c \in C_1$ there is a reflection morphism $f : c \to d$ with $d \in D_1$.

Such $f$ is obtained by choosing any [[coCartesian morphism|coCartesian lift]] of a reflector $p(f) : p(c) \to \bar d$.

To see this, consider for every object $e \in D_1$ the diagram

$$
  \array{
    Hom_{C_1}(d,e) 
     &\stackrel{Hom_{C_1}(f,e)}{\to}&
     Hom_{C_1}(c,e)
    \\
    \downarrow && \downarrow
    \\
    Hom_{C_0}(p(d), p(e))
     &\stackrel{Hom_{C_0}(p(f) ,p(e))}{\to}&
    Hom_{C_0}(p(c), p(e))
  }
  \,.
$$

By assumption $p(f)$ is a reflector, hence the bottom morphism is an equivalence. By one of the characterizations of [[coCartesian morphism]]s, the fact that $f$ is a coCartesian lift means that this diagram is a (homotopy) pullback diagram.  This means that also the top horizontal morphism is an equivalence.


=--


### Locally presentable $(\infty,1)$-categories

If $C = PSh_{(\infty,1)}(K)$ is the [[(∞,1)-category of (∞,1)-presheaves]] on some small $(\infty,1)$-category $K$, then _accessibly embedded_ reflective subcategory

$$
  D \stackrel{\leftarrow}{\hookrightarrow}
  PSh_{(\infty,1)}(K)
$$ 

(i.e. one where the inclusion is an [[accessible (∞,1)-functor]]) is a [[locally presentable (∞,1)-category]].

### $(\infty,1)$-Toposes

If $C = PSh_{(\infty,1)}(K)$ is the [[(∞,1)-category of (∞,1)-presheaves]] on some small $(\infty,1)$-category $K$, then an [[accessible (∞,1)-functor|accessibly embedded]] _exact_ reflective subcategory

$$
  Sh_{(\infty,1)}(K) \stackrel{\overset{L}{\leftarrow}}{\underset{}{\hookrightarrow}}
  PSh_{(\infty,1)}(K)
$$

is an [[(∞,1)-category of (∞,1)-sheaves]] on $K$ -- an [[(∞,1)-topos]]. We have:

* the collection of morphism $S = L^{-1}(equiv.)$ that are sent to weak equivalences are the analog of **[[local isomorphism]]s** of ordinary [[sheaf and topos theory|sheaf theory]];

* the $S$-[[local object]]s are the **[[∞-stack]]s** ;

* the localizaton functor $Loc = R \circ L : PSh_{(\infty,1)}(K) \to PSh_{(\infty,1)}(K)$ is **[[∞-stackification]]** .


### $\infty$-Lie algebroids inside all $\infty$-Lie groupoids

Let $K = Alg_k^{op}$ be the opposite of the category of $k$-[[associative algebra]]s, regarded as a site with the [[fpqc-topology]]. Then an object in $Sh_{(\infty,1)}(Alg_k^{op})$ may be regarded as an algebraic $\infty$-groupoid. The [[infinitesimal object|infinitesimal]] version is an [[Lie ∞-algebroid]], which may be identified with an object in $(Alg_k^\Delta)^{op} \simeq (dgAlg_k)^{op}$ -- the opposite of the category of [[cosimplicial algebra]]s. The [[simplicial model category|simplicial]] [[model structure on cosimplicial algebras]], [[locally presentable (∞,1)-category|presents]] this as an $(\infty,1)$-category $(Alg_k^\Delta)^\circ$

The [[Yoneda embedding]] induces an inclusion

$$
  ((Alg_k^\Delta)^{op})^\circ
  \stackrel{}{\hookrightarrow}
  Sh_{(\infty,1)}(Alg_k^{op})
  \,.
$$

which is a reflective embedding. It exhibits localization at $A^1$-[[cohomology]], where $A^1 = Spec k[x]$ is the algebraic line object.

This is discussed at [[rational homotopy theory in an (∞,1)-topos]].


## Related concepts

* [[idempotent (∞,1)-monad]]

* [[reflective subuniverse]]

* [[Quillen reflection]]

## References

The general theory is discussed in section 5.2.7 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

A [[Coq]]-formalization of left-exact reflective sub-$(\infty,1)$-categories in [[homotopy type theory]] is in 

* [[Mike Shulman]], _[HoTT/Coq/Subcategories/LexReflectiveSubcategory.v](https://github.com/mikeshulman/HoTT/blob/master/Coq/Subcategories/LexReflectiveSubcategory.v)_
 {#Shulman}



[[!redirects reflective sub-(∞,1)-category]]
[[!redirects reflective sub-(∞,1)-categories]]
[[!redirects reflective sub-(infinity,1)-categories]]

[[!redirects reflective (infinity,1)-subcategory]]
[[!redirects reflective (infinity,1)-subcategories]]

[[!redirects reflective (∞,1)-subcategory]]
[[!redirects reflective (∞,1)-subcategories]]

[[!redirects coreflective sub-(∞,1)-category]]
[[!redirects coreflective sub-(∞,1)-categories]]
[[!redirects coreflective sub-(infinity,1)-category]]
[[!redirects coreflective sub-(infinity,1)-categories]]


[[!redirects coreflective (∞,1)-subcategory]]
[[!redirects coreflective (∞,1)-subcategories]]
[[!redirects coreflective (infinity,1)-subcategory]]
[[!redirects coreflective (infinity,1)-subcategories]]