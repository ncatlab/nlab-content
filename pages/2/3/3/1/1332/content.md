
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For a class $S$ of morphisms in a category (or higher category) $C$, we can consider the localization functor into the category of fractions $L: C\to C[S^{-1}]$ which is universal with respect to all functors inverting $S$; this defines its (external) saturation, the class $S'\subset Mor(C)$ of _all_ morphisms which are sent to isomorphisms by $L$, or more generally to equivalences.
One also defined a collection of objects $c$ which are _local_ with respect to these morphisms, in that these morphisms behave as isos/equivalences with respect to homming into $c$. If $L: C\to C[S^{-1}]$ has a right adjoint then it is a [[reflective localization]], and in particular the right adjoint is fully faithful; we can abstractly consider reflective localizations of the form $L: C\to C'$ and start with internally saturated class $S$ of all morphisms inverted by $L$. Then the collection of $S$-local objects characterizes the localization. Moreover, $S$ can itself be enlarged to its external saturation, the collection of $S$-local morphisms, that is _all_ morphisms which are isomorphisms with respect to homing into all $S$-local objects. In the reflective case, external and internal saturation coincide and in general external saturation is a subclass of internal saturation.

Gabriel-Zisman used the term "left-closed object for $S$". This terminology is still widely used in the context of abelian categories with or without "left"; $J$-closed is then closed in the sense of any kind of localization data $J$ (for example, $J$ being a [[torsion theory]] or a [[Gabriel filter]]). Sheaves and stacks are examples of closed objects in presheaf categories on sites/spaces. 


## Definition for ordinary categories

### Local objects 

Let $C$ be a [[category]] and $S$ a collection of [[morphisms]] in $C$. Then an [[object]] $c \in C$ is **$S$-local** if the [[hom-functor]]
$$
  C(-,c) : C^{op} \to Set
$$
sends morphisms in $S$ to [[isomorphisms]] in [[Set]], i.e. if
for every $s : a \to b$ in $S$, the function
$$
  C(s,c) : C(b,c) \to C(a,c)
$$
is a [[bijection]].


### Local morphisms

Conversely, a **morphism** $f : x \to y$ is **$S$-local if for every $S$-local object $c$ the induced morphism

$$
  C(f,c) : C(y,c) \to C(x,c)
$$

is an isomorphism.



## Definition for $(\infty,1)$-categories 



### Local objects 

+-- {: .num_defn}
###### Definition 


Let $C$ be an [[(∞,1)-category]] and $S$ a collection of morphisms in $C$. Then an [[object]] $c \in C$ is **$S$-local** if the [[hom-functor]]
$$
  C(-,c) : C^{op} \to \infty Top
$$
evaluated on $s \in S$ induces isomorphism in the [[homotopy category]] of [[Top]].
=--

This is [5.5.4.1](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=383) in [[Higher Topos Theory|HTT]]


### Local morphisms 

Conversely, a **morphism** $f : x \to y$ is **$S$-local** if for every $S$-local object $c$ the induced morphism

$$
  C(f,c) : C(y,c) \to C(x,c)
$$

induces an isomorphism in the [[homotopy category]] of [[Top]].

## Definition in model categories 

Let $C$ be a [[model category]] (usefully but not necessarily a [[simplicial model category]]). And let $S \subset Mor(C)$ be a collection of [[morphism]]s in $C$.

Write $\mathbf{R}Hom_C(-,-) : C^{op}\times C \to SSet$ for the [[(infinity,1)-categorical hom-space|derived hom space functor]].

For instance if $C$ is a [[simplicial model category]] then this may be realized in terms of a cofibrant replacement functor $Q : C \to C$ and a fibrant replacement functor $P$ as

$$
  \mathbf{R}Hom_C(X,Y) = C(Q X, P Y)
  \,.
$$

+-- {: .num_defn }
###### Definition 
**(local object, local weak equivalence)**

An object $c \in C$ is a **$S$-local object** if for all $s : a \to b$ in $S$ the induced morphism

  $$
    \mathbf{R}Hom_C(s,c) : \mathbf{R}Hom_C(b,c) \to \mathbf{R}Hom_C(a,c)
  $$

  is a weak equivalence (in the standard [[model structure on simplicial sets]]);
  
A morphism $f : x \to y$ in $C$ is an **$S$-local morphism** or **$S$-equivalence** if for every $S$-local object $c$ the induced morphism

  $$
    \mathbf{R}Hom_C(f,c) : SSet \to SSet
  $$

  is a weak equivalence.

An **$S$-localization of an object** $c$ is an $S$-local object $\hat c$ and an $S$-local equivalence $c \to \hat c$.

An **$S$-localization of a morphism** $f : c \to d$ is a pair of $S$-localizations $c \to \hat c$ and $d \to \hat d$ of objects, and a commuting square

$$
  \array{
    c &\stackrel{f}{\to}& d
    \\
    \downarrow && \downarrow
    \\
    \hat c &\to & \hat d
  }
  \,.
$$ 

=--


### Properties {#PropInModCat}

In [[proper model category|left proper model categories]] there is an equivalent stronger characterization of $S$-locality of cofibrations $i : A \hookrightarrow B$.

+-- {: .num_prop }
###### Proposition 
**(characterization of $S$-local cofibrations)**

Let $C$ be a [[proper model category|left proper]] [[simplicial model category]] and $S \subset Mor(C)$, a collection of morphisms. 

Then a cofibration $i : A \hookrightarrow B$ is an $S$-local weak equivalence precisely if for all fibrant $S$-local objects $X$ the morphism

$$
  C(B,X) \to C(A,X)
$$

is an acyclic fibration in the standard [[model structure on simplicial sets]].

=--

+-- {: .num_remark }
###### Remark

Notice that this is stronger than the statement that $\mathbf{R}Hom(B,X) \to \mathbf{R}Hom(A,X)$ is a weak equivalence not only in that it asserts in addition a fibration, but also in that it deduces this without first passing to a cofibrant replacement of $A$ and $B$.

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma A.3.7.1]].

The proof makes use of the following general construction: for $f : A \to B$ any morphism let $\emptyset \hookrightarrow A' \stackrel{\simeq}{\to} A$ be a cofibrant replacement, factor $A' \to B$ as 
$A' \stackrel{i'}{\hookrightarrow} B' \stackrel{\simeq}{\to} B$ and consider the [[pushout]] diagram

$$
  \array{
    A' &\stackrel{i'}{\hookrightarrow}& B'
    \\
    \downarrow^{\mathrlap{f \in W}}
    && \downarrow_{\mathrlap{g\in W}}
    &
    \searrow^{\mathrlap{f' \in W}}
    \\
    A &\stackrel{}{\hookrightarrow}& A \coprod_{A'} B 
    &\stackrel{j \in W}{\to}&
    B
  }
  \,.
$$

By [[proper model category|left properness]] the pushout $g$ of the weak equivalence $f$ along the cofibration $i'$ is again a weak equivalence and by [[category with weak equivalences|2-out-of-3]] the morphism $j$ is a weak equivalence.


Now assume that $i$ is an $S$-local equivalence. We need to show that $i^* : C(B,X) \to C(A,X)$ is an acyclic Kan fibration for all fibrant $S$-local $X$. By the very definition of [[enriched model category]] it follows from $i$ being a cofibration and $X$ being fibrant that this is a Kan fibration. So it remains to show that it is a [[weak homotopy equivalence]] of [[simplicial set]]s. We know that the corresponding induced morphism 

$$
  ({i'}^* : C(B',X) \to C(A',X))
  \simeq
  (\mathbf{R}Hom(B,X) \to \mathbf{R}Hom(A,X))
$$ 

on the cofibrant replacement is a weak equivalence, by the assumption that $X$ is $S$-local, and also, as before, a fibration, since $i'$ is still a cofibration.

By homming the entire diagram above into $X$, and using that the [[hom-functor]] $C(-,X)$ sends [[colimit]]s to [[limit]]s, we find the [[pullback]] diagram

$$
  \array{
    C(A \coprod_{A'} B', X)
    &\to&
    C(B',X)
    \\
    {}^{q}\downarrow^{\mathrlap{\in (W\cap fib)_{SSet}}}
    &&
    {}^{{i'}^*}\downarrow^{\mathrlap{\in (W\cap fib)_{SSet}}}
    \\
    C(A,X) 
    &\to&
    C(A',X)
  }
$$

in [[SSet]], which shows that $q$ is an acyclic fibration, being the pullback of an acyclic fibration.

To show that $i^*: C(B,X) \to C(A,X)$ is a weak equivalence it suffices to show that all its fibers $(i^*)^{-1})(t)$ over elements $t : A \to X$ are [[contractible]] [[Kan complex]]es. These fibers map to the corresponding fibers $q^{-1}(t)$ by precomposition with $j$. By the fact that $j$, regarded as a morphism

$$
  \array{
   && A
   \\
   & {}\swarrow 
    && \searrow
   \\
   A \coprod_{A'} B' &&\stackrel{j}{\to}&& B
  }
$$

in the [[model structure on an over category|model structure on the undercategory]] $A/C$ is a weak equivalence between cofibrant objects (because $A \hookrightarrow B$ is a cofibration by assumption and $A \to A \coprod_{A'} B'$ as being the pushout of the cofibration $i'$) we have that precomposition $C(j,X)$ with $j$ is the image under the [[SSet]]-[[enriched functor|enriched]] [[hom-functor]] of a weak equivalence between cofibrant objects mapping into a fibrant object

$$
  \array{
    && A
    \\
    & \swarrow & \downarrow & \searrow^{t}
    \\
    A \coprod_{A'} B' 
    &\stackrel{j}{\to}&
    B
    &\to&
    X
  }
$$

and hence, by the general properties of [enriched homs between cofibrant/fibrant objects](http://ncatlab.org/nlab/show/%28infinity,1%29-categorical+hom-space#enriched_homs_between_cofibrantfibrant_objects_6) a weak equivalence. $j^* : (i^*)^{-1}(t) \stackrel{\simeq}{\to} q^{-1}(t)$, so that indeed $(i^*)^{-1}(t)$ is contractible.


This proves the first part of the statement. For the converse statement, assume now that...



=--



## Saturated class of morphisms

Every morphism in $S$ is $S$-local. 

There are two notions of saturation in the literature. Following [Casacuberta, Frei 2000](#CasacubertaFrei2000) we distinguish them as internal and external. Internal saturation of a class $S$ of morphisms is simply the class of all $S$-local morphisms. External saturation of a class $S$ of morphisms is the class of all morphisms which are inverted in the category of fractions (localization) at class $S$. 

In both variants, the collection $S$ of morphisms is called **saturated** if $S$ coincides with its saturation.

$S$ is contained in its external saturation which is in turn contained in its internal saturation; the external and internal saturation coincide if the localization in $S$ has either left or right adjoint (coreflective or reflective case).



## Remarks 


* a [[reflective subcategory]] as well as a [[reflective (∞,1)-subcategory]] can be realized as the full ($(\infty,1)$-)subcategory on $S$-local objects, where $S$ is the collection of morphisms sent by the corresponding [[localization of an (∞,1)-category]] to equivalences. For details on this see the discussion at [[geometric embedding]].

## References

Local objects are treated, under the name of left-closed objects, in  I.4.1 of

* [[Pierre Gabriel]], [[Michel Zisman]], _[[Calculus of fractions and homotopy theory]]_, _Ergebnisse der Mathematik und ihrer Grenzgebiete_, Band 35. Springer, New York (1967) &lbrack;[doi:10.1007/978-3-642-85844-4](https://link.springer.com/book/10.1007/978-3-642-85844-4), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf)&rbrack;

A classical textbook reference is section 3.2 of

* Hirschhorn, _Model categories and their localization_

A useful reference with direct ties to the [[(∞,1)-category]] story in the background is section A.3.7 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

1-categorical picture 

* {#CasacubertaFrei2000} [[Carles Casacuberta]], Armin Frei, _On saturated classes of morphisms_, Theory and Applications of Categories __7__:4 (2000) 43--46 [pdf](https://www2.math.ethz.ch/EMIS/journals/TAC/volumes/7/n4/n4.pdf)

* [[Carles Casacuberta]], Georg Peschke, Markus Pfenniger, _On orthogonal pairs in categories and localization_, J. Pure & Applied Algebra __142__:1 (1999) 25--33

Relation to the categorical [[shape theory]]

* Luciano Stramaccia, _Orthogonality, saturation and shape_, Glasnik Matematički 2007, [pdf](https://hrcak.srce.hr/file/27927)

[[!redirects local objects]]
[[!redirects local morphism]]
[[!redirects local morphisms]]
