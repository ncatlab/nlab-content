
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The notion of  _reflective $(\infty,1)$-subcategory_ is the generalization of the notion of [[reflective subcategory]] from [[category theory]] to [[(∞,1)-category]] theory.

## Definition 


### Reflective $(\infty,1)$-subcategory

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


The [[(∞,1)-functor]] $R$ or its composite 

$$
  Loc := R \circ L : C \to C
$$ 

may be understood as exhibiting a [[localization of an (∞,1)-category|localization]] of $C$ at those morphisms that $L$ sends to [[equivalence in a quasi-category|equivalence]]s in $D$.


### Local objects and local morphisms

One finds, as discussed [below](#Properties), that reflective subcategories may be entirely characterized by the class of morphisms that the localization functor $Loc : C \to C$ sends to weak equivalences.


+-- {: .un_def}
###### Definition
**(local objects, local equivalences)**

Let $S \subset Mor(C)$ be a class of morphisms. 

* An object $c \in C$ is called an **$S$-[[local object]]** if for all morphisms $f : x \to y$ in $C$ the induced morphism

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

+-- {: .un_def}
###### Definition
**(strongly saturated class of morphisms)**


For $C$ an [[(∞,1)-category]] with small [[limit in a quasi-category|colimits]], a class $S \subset C_1$ of morphisms in $C$ is said to be **strongly saturated** if its satisfies the following three conditions

1. It is stable under [[pushout]]s;

1. The full [[sub-quasi-category|subcategory]] of the [[(∞,1)-category of (∞,1)-functors]] $Func(\Delta[1], C)$ on $S$ has all colimits;

1. it satisfies the [[category with weak equivalences|2-out-of-3 property]].

=--

Notice that this definition has some immediate consequences:

The identity $Id_\emptyset$ on the [[initial object]] of $C$, which is the initial object in $Func(\Delta[1],C)$ is in $S$, since it is the colimit of the empty diagram. Moreover, every [[equivalence in a quasi-category|equivalence]] is a [[pushout]] of $Id_{\emptyset}$$ so

* A strongly saturated class contains every [[equivalence in a quasi-category|equivalence]].

Given any collection $\{S_i\}_i$ of strongly saturated classes of morphisms in $C$, their intersection is clearly also strongly saturated. Therefore for every collection $S$ of morphisms, there is a smallest strongly saturated class $\bar S$ containing it. We say that $S$ **generates** the strongly saturated class $\bar S$. If $S$ is a [[small set]], then $\bar S$ is said to be **of small generation**. 

The smallest strongly saturated class of morphism in $C$ is that containing only the equivalences of $C$.

Of importance are the strongly saturated classes arising as follows.

+-- {: .un_lemma}
###### Lemma


For $C$ and $D$ two $(\infty,1)$-categories that have small colimits, and for $F : C \to D$ an [[(∞,1)-functor]] that preserves small colimits, given a strongly saturated class of morphisms $S$ in $D$, its preimage $F^{-1}(S)$ is a strongly saturated class in $C$.


In particular the class of morphisms in $C$ sent to equivalences by $F$ is strongly saturated.

=--


+-- {: .un_lemma}
###### Lemma

The class of $S_0$-[[local equivalence]]s for $S_0$ any class of morphisms is strongly saturated.

=--

+-- {: .proof}
###### Proof


For each object $c \in C$ let $j(c) : C \to \infty Grpd^{op}$ be the functor [[representable functor|represented]] by $c$. Let $S_c$ be the class of morphisms sent by $j(c)$ to weak equivalences in [[∞Grpd]]. Since $j(c)$ preserves small colimits, this is a strongly saturated class, by the above lemma. Now observe that $S$ is the intersection $S = \cap_c S_c$ where $c$ ranges over the $S_0$-[[local object]]s.

=--


In the following this language of local morphisms is used to characterize reflective $(\infty,1)$-subcategories.

## Properties {#Properties}

The following proposition characterizes the _reflectors_ of a reflective $(\infty,1)$-subcategory.
 
+-- {: .un_lemma}
###### Lemma

Let $C$ be an [[(∞,1)-category]] and $D \hookrightarrow C$ a full [[sub-quasi-category|sub (∞,1)-category]]. Then this inclusion has a left [[adjoint (∞,1)-functor]] precisely if 

* for every object $c \in C$ there is a _localization_ or _reflection_ : a morphism $f : c \to d$ such that $d \in D$ and such that for all $e \in D$ we have that 

  $$
    Hom_C(f,e) : Hom_C(d,e) \to Hom_C(c,e)
  $$

  is an equivalence (of [[∞-groupoid]]s).

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 5.2.7.8]].


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

+-- {: .un_prop}
###### Proposition

Let 

$$
  D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}} C
$$

be a localization of the $(\infty,1)$-category $C$ and let 

$$
  Loc : C \stackrel{L}{\to} D \overset{R}{\hookrightarrow} C
$$

be the corresponding localization [[(∞,1)-monad]]. Write $S \subset Mor(C)$ for the collection of morphisms that $Loc$ sends to [[equivalence in a quasi-category|equivalences]].

Then

* an object $c \in C$ is an $S$-[[local object]] precisely if it is in essential image of $Loc$ (equivalent to an object of the form $Loc x$);

* every $S$-[[local morphism]] is already in $S$.



=--


+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, prop 5.5.4.2]]. The reasoning is entirely analogous to the 1-categorical case (see for instance [[localization]], [[reflective subcategory]] and [[geometric embedding]]).


First notice that because $D \hookrightarrow C$ is a [[full and faithful (∞,1)-functor]] we have that the counit $L R \stackrel{\simeq}{\to} Id_D$ is an equivalence. From this it follows that precomposition with the unit $i_z : z \to Loc z$ of morphisms in the image of $L$ is a weak equivalence: for all $z,x \in C$ we have

$$
    Hom_C(i, Loc z)
    :
    Hom_C(Loc z, Loc x)
    \simeq
    Hom_C(z, Loc x)
  \,.
$$

If $z$ is itself in the image of $Loc$, then this means that precomposition with the unit $z \to Loc z$ is an isomorphism on [[hom-set]]s in the [[homotopy category of an (infinity,1)-category|homotopy category]] of $Loc C$, hence by the [[Yoneda lemma]] is itself an isomorphism in the homotopy category, hence $i_z : z \to Loc z$ is a weak equivalence if $z$ is itself in the image of $Loc$.

Applying this statement to the commuting square

$$
  \array{
    s &\stackrel{i_s}{\to} & Loc s
    \\
    \downarrow && \downarrow^{\mathrlap{Loc i_s}}
    \\
    Loc s &\stackrel{i_{Loc s}}{\to}& Loc Loc s
  }
$$

and using that precomposition with $i_s$ gives an equivalence here (by the above) we find that $Loc i_s \simeq i_{Loc s}$, hence that $Loc i_s$ is a weak equivalence, and hence that $i_s$ is in $S$, for all $s \in C$.

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

Here the vertical morphisms are equivalences by the above remark, and the top morphism is an equivalence by the assumoption that $f$ in in $S$. It follows that the bottom morphism is an equivalence. This says that $Loc x$ is $S$-local, for all $x \in C$.

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

By the above we know now that the vertical morphisms here are also $S$-local. It follows that the image of $Loc f : Loc x \to Loc y$ on the homtopy category of $Ho(Loc C)$ corepresents an isomorphism, hence by the [[Yoneda lemma]] that $Lof f$ is a weak equivalence. Hence $f$ is indeed in $S$.


=--


One can turns this around and define or construct reflective $(\infty,1)$-subcategories by specifying collections of local morphisms.


+-- {: .un_prop}
###### Proposition
**(localization proposition)**

Let $C$ be a [[presentable (∞,1)-category]] and $S_0$  be a [[small set]] of morphisms of $C$. 

Then the full [[sub-quasi-category|sub-(∞,1)-category]] 

$$
  R : D \hookrightarrow C
$$ 

on $S_0$-[[local object]]s is a reflective $(\infty,1)$-subcategory. 

If $L : C \to D$ denotes the left [[adjoint (∞,1)-functor]] of the inclusion, then for $f \in Mor(C)$ a morphism, the following are equivalent

1. $f$ is an $S_0$-[[local equivalence]];

1. $f$ belongs to the strongly saturated class $S$ generated by $S_0$;

1. the morphism $L f$ is an equivalence.


=--

The main ingredient in the proof of this assertion is the following lemma, whose prove we give below in [Proof of the localization lemma](#ProofOfLocalization).


+-- {: .un_prop}
###### Proposition
**(localization lemma)**

Let $C$ be a [[locally presentable (∞,1)-category]], and let $S \subset Mor(C)$ be a strongly saturated collection of morphisms, generated from a [[small set]] $S_0$. 

Then for every object $c \in C$ there exists a reflector, i.e. a morphism  $f : c \to d$ such that $d$ is an $S$-[[local object]] and $f \in S$.

=--

With that in hand we look at the proof of the above proposition:

+-- {: .proof}
###### Proof

The localization lemma gives for each object $c \in C$ a reflector $f : c \to d$ with $d$ $S$-local. By one of the above lemmas, this already gives the reflective embedding

$$
  D \stackrel{\leftarrow}{\hookrightarrow} C
$$

of the full subcateory of $S$-local objects in $C$.

it remains to prove the statements about the role of $S$ in the localization:

First, by one of the above lemmas, we have that the $S_0$-local equivalences are a strongly saturated class of morphisms containong $S_0$. Hence they in particular contain $S$. So the second claim implies the first. 

Next...


=--



### Proof of the localization lemma {#ProofOfLocalization}

We here spell out the proof of 

+-- {: .un_prop}
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

in $C$, regarded as a morphism in $Func(\Delta[1], C)$. By the universality of the pushout, one finds that this is a [[coCartesian morphism|coCartesian lift]]. Hence $D \to Func(\{0\}, C) \simeq C$ is a [[coCartesian fibration]].

From this the proof proceeds in two further steps:

1. Show that $D_c$ is itself an locally presentable $(\infty,1)$-category. 
   From that it follows that $D_c$ has all small limits and hence in 
   particular contains a 
   [[terminal object in a quasi-category|terminal object]], $f : c \to d$;

  

1. Show that $f : c \to d$ being terminal in $D_c$ 
   implies that $d$ is $S$-local.


...

Consider now the second point, showing that $f : c \to d$ being terminal in $D_c$ implies that $d$ is $S$-local. This is equivalent to showing that for $t : a \to b$ any element in $S$, composition with $t$ induces an equivalence

$$
  Hom_C(t,d) : Hom_C(b,d) \to Hom_C(a,d)
  \,.
$$

This in turn may be checked by checking that all its [[homotopy fiber]]s are [[contractible]]. Thre homotopy fiber of $Hom_C(t,d)$ over a point $g : a \to d$ of $Hom_C(a,d)$ is $Hom_{C_{a/}}(t,g)$. To show that this is contractible, form the $\infty$-categorical pushout

$$
  \array{
    a &\stackrel{t}{\to}& b
    \\
    \downarrow && \downarrow 
    \\
    d &\to& d \coprod_a b
  }
$$

in $C$. This gives an equivalence $Hom_{C_{a/}}(t,g) \simeq Hom_{c_{d/}, Id_d}$, so it suffices to show that the latter is contractible. 

Since $d \to d \coprod_a b$ is a pushout of $t$, it is itself in $S$.


> (... left incomplete ...)


=--



## Examples {#Examples}

### Inclusion of the terminal object

If $C$ has a [[terminal object in a quasi-category|terminal object]], then the full subcategory on terminal objects is a reflective subcategory of $C$.


### coCartesian fiber over a reflective subcategory



+-- {: .un_prop}
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


[[!redirects reflective (infinity,1)-subcategories]]
[[!redirects reflective (∞,1)-subcategory]]
[[!redirects reflective (∞,1)-subcategories]]