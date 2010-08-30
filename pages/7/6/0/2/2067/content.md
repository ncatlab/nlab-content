
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
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

Given a [[functor]] $p\colon  X \to Y$ between categories one may ask for each [[morphism]] $f\colon  y_1 \to y_2$ if given a lift of its target
$$
  \array{
    X &&& && \hat y_2
    \\
    \downarrow^p 
    \\
    Y &&& y_1 &\stackrel{f}{\to}& y_2
  }
$$

there is a _universal_ lift of $f$

$$
  \array{
    X &&& \hat y_1 &\stackrel{\hat f}{\to}& \hat y_2
    \\
    \downarrow^p 
    \\
    Y &&& y_1 &\stackrel{f}{\to}& y_2
  }
  \,.
$$

There may also be other lifts of $f$, but the universal one is essentially unique, as usual for anything having a [[universal property]].  Specifically, $\hat f$ in $X$ is essentially uniquely determined by its source $\hat y_1$ and its image $f = p(\hat f)$ in $Y$, and is called a __cartesian morphism__.  A morphism which is cartesian relative to $p^{op}\colon X^{op}\to Y^{op}$ is called __opcartesian__ or __cocartesian__.

If there are enough cartesian morphisms in $Y$, they may be used to define [[functor]]s

$$
  f^* : X_{y_2} \to X_{y_1}
$$

between the [[fiber]]s of $p$ over $y_1$ and $y_2$. 

This way a functor $p : X \to Y$ with enough Cartesian morphisms -- called a [[Cartesian fibration]] or [[Grothendieck fibration]] -- determines and is determined by a fiber-assigning functor $Y \to Cat^{op}$.

This has its analog in [[higher category theory|higher categories]].


## Definition

### In categories

#### Traditional definition

+-- {: .un_defn}
###### Definition
**(cartesian morphism)**

Let $p : X \to Y$ be a [[functor]]. A [[morphism]] $f : x_1 \to x_2$ in the [[category]] $X$ is _**cartesian** with respect to $p$, or **$p$-cartesian** . If it satisfies the following property:

$$
  \array{
    x'
    \\
    \downarrow^{\mathrlap{\exists!}} & \searrow^{\mathrlap{\forall h}}
    \\
    x_1 &\stackrel{f}{\to}& x_2
  }
  \;\;\;
  \;\;\;
  \stackrel{p}{\mapsto}
  \;\;\;
  \;\;\;
  \array{
    p(x')
    \\
    \downarrow^{\mathrlap{\forall g}} & \searrow^{\mathrlap{p(h)}}
    \\
    p(x_1) &\stackrel{p(f)}{\to}& p(x_2)
  }
$$

In words: for all commuting triangles in $Y$ and all lifts through $p$ of its 2-[[horn]] to $X$, there is a unique refinement to a lift of the entire commuting triangle.

If we pass to the [[nerve]] $N(X)$ and $N(Y)$ of the categories, then in terms of diagrams in [[sSet]] this means that the morphism $f : x \to y$ is $p$-cartesian precisely if for all [[horn]] inclusions

$$
  \array{
    \Delta^{\{1,2\}}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda_2[2] &\to& N(X)
    \\
    \downarrow && \downarrow
    \\
    \Delta[2] &\to& N(Y)
  }
$$

such that the last edge of the 2-[[horn]] is the given egde $f$, a lift $\sigma$

$$
  \array{
    \Delta^{\{1,2\}}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda_2[2] &\to& N(X)
    \\
    \downarrow &{}^\sigma\nearrow& \downarrow
    \\
    \Delta[2] &\to& N(Y)
  }
$$

exists. 


=--


#### Reformulations {#CartInOrdCatReformulation}

We discuss equivalent reformulations of the above definition of Cartesian
morphism that lend themselves better to generalization to 
[[higher category theory]].

For the following, we need this notionation: let 

* $X/x_2$ by the [[overcategory]] of $X$ over the object $x_2$;

* $Y/p(x_2)$ the corresponding [[overcategory]] of $Y$ over $p(x_2)$;

* $X/f$ the category whose objects 

  $$
    Obj(X/f) = 
    \left\{
    \array{
       && a
       \\
       &\swarrow && \searrow
       \\
       x_1 &&\stackrel{f}{\to}&& x_2
    }
    \right\}
  $$
 
  are objects $a$ of $X$ eqipped with morphisms to $x_1$ and $x_2$ such that the obvious triangle commutes, and whose morphisms are morphisms between these tip objects such that all diagrams in sight commute.

* similarly for $Y/p(f)$.



+-- {: .un_prop}
###### Proposition

The condition that $f \in Mor X$ is a Cartesian morphism with respect to $p : X \to Y $  is equivalent to the condition that the functor

$$
  \phi : X/f \to X/{x_2} \times_{Y/{p(x_2)}} Y/p(f)
$$

into the (strict) [[pullback]] of the obvious projection $X/{x_2} \to Y/p(x_2)$ along the projection $Y/p(f) \to Y/p(x_2)$ induced by the commutativity of

$$
  \array{
    X/f &\stackrel{\phi_2}{\to}& Y/p(f)
    \\
    {}^{\mathllap{\phi_1}}\downarrow && \downarrow
    \\
    X/{x_2} &\to& Y/{p(x_2)}
  }
$$

is a [[k-surjective functor|surjective equivalence]], and this in turn is equivalent to it being an [[isomorphism]] of categories.

=--

+-- {: .proof}
###### Proof

It is immediate to see that $\phi$ being an isomorphism of categories is equivalent to the condition that $f$ is a Cartesian morphism. We discuss that that just the condition that $\phi$ is a surjective equivalence already implies that it is an isomorphism of categories.

So assume now that $\phi$ is a surjective equivalence.

Notice that objects in the pullback category are compatible pairs

$$
  \left(
  \left(
  \array{
     && a 
     \\
     &&& \searrow
     \\
     x_1 &&\stackrel{f}{\to}&& x_2
  }
  \right) \in X/_{x_2}
  \;\;\;\;\;\;\,,\;\;\;\;\;\;
  \left(
  \array{
     && b 
     \\
     & \swarrow && \searrow
     \\
     p(x_1) &&\stackrel{p(f)}{\to}&& p(x_2)
  }
  \right)
   \in Y/p(f)
  \right)
  \,.
$$

We have a $\phi$ being _surjective_ on object means that every such pair is in the image of some object 

$$
  \left(
  \array{
     && a 
     \\
     &{}^{\mathllap{g}}\swarrow&& \searrow
     \\
     x_1 &&\stackrel{f}{\to}&& x_2
  }
  \right)
  \in X_{f}
  \,,
$$

and hence that every filler _exists_ . Assume two such fillers $g$ and $g'$. Then by the fact that an [[equivalence of categories]] is an isomorphism on corresponding hom-sets, it follows that there must be a unique morphism in $X/f$ connecting them 

$$
  \array{
     && a
     \\
     &{}^{\mathllap{g}}\swarrow & \downarrow^{\mathrlap{h}} & \searrow
     \\
     && a
    \\
     \downarrow & {}^{\mathllap{g'}}\swarrow && \searrow & \downarrow
     \\
     x_1 &&\stackrel{f}{\to}&& x_2
  }
$$

such that this maps under $\phi$ to the identity morphism in the pullback category. But in particular this maps to the morphism

$$
  \array{
     && a
     \\
     && \downarrow^{\mathrlap{h}} & \searrow
     \\
     && a
    \\
     & && \searrow & \downarrow
     \\
      &&&& x_2
  }
$$

in $X/{x_2}$ and evidently is the identity there if and only if $h$ is the identity. Hence this maps also to the identity in the pullback category if and only if $h$ is the identity. So $h$ must be the identity. So if two lifts of an object through the surjective equivalence $\phi$ exist, they must already be equal. Hence the surjective equivalence $\phi$ is even an isomorphism on objects and hence an isomorphism of categories.

=--



+-- {: .un_defn}
###### Definition
**(Grothendieck fibration)**

If for every morphism in $Y$ there is at least one lift through $p$ that is a $p$-cartesian morphism , one says that $p$ is a [[Grothendieck fibration]].

=--


### In $(\infty,1)$-categories

The notion of cartesian morphism generalizes from [[category theory]] to [[(∞,1)-category theory]]. We describe it for two different incarnations of the notion of [[(∞,1)-category]]: [[quasi-categories]] and [[simplicially enriched categories|sSet categories]].

#### In quasi-categories

We formulate a notion **cartesian edge** or _cartesian morphism_ in a [[simplicial set]] $X$ relative to a morphism $p : X \to Y$ of simplicial sets. In the case that these simplicial sets are [[quasi-category|quasi-categories]] -- i.e. simplicial set incarnations of [[(∞,1)-category|(∞,1)-categories]] -- this yields a notion of cartesian morphisms in $(\infty,1)$-categories.

Let $p : X \to Y$ be a morphism of [[simplicial set]]s.
Let $f : x_1 \to x_2$ be an edge in $X$, i.e. a morphism $f : \Delta^1 \to X$.

Recall the notion of [[over quasi-category]] obtained from the notion of [[join of quasi-categories]]. Using this we obtain [[simplicial set]]s $X/f$, $X/{x_2}$, $S/p(f)$ and $S/p(x_2)$ in generalization of the categories considered in the above definition of cartesian morphisms in categories.

+-- {: .un_defn}
###### Definition
**(cartesian edge in a simplicial set)**

Let $p : X \to Y$ be an [[inner Kan fibration]] of simplicial sets.

Then a [[morphism]] $f : x \to y$ in $X$ is **$p$-cartesian** if the induced morphism

$$
  X_{/f} \to X_{/y} \times_{Y_{/p(y)}} Y_{/p(f)}
$$

into the [[pullback]] in [[sSet]]
is an acyclic [[Kan fibration]].

=--


This is [[Higher Topos Theory|HTT, def 2.4.1.1]].

+-- {: .un_prop}
###### Proposition

The morphism $f : x \to y$ as above, for $p : X \to Y$ an [[inner fibration]], is $p$-cartesian precisely if for all $n \geq 2$ and all right outer [[horn]] inclusions

$$
  \array{
    \Delta^{\{n-1,n\}}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda[n]_n &\to& X
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& Y
  }
$$

(with $\Lambda[n]_n$ the $n$th [[horn]] of the $n$-[[simplex]]) such that the last edge of the horn is the given egde $f$, a lift $\sigma$

$$
  \array{
    \Delta^{\{n-1,n\}}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda[n]_n &\to& X
    \\
    \downarrow &{}^\sigma\nearrow& \downarrow
    \\
    \Delta[n] &\to& Y
  }
$$

exists. 

=--


This is [[Higher Topos Theory|HTT remark 2.4.1.4]].


+-- {: .un_remark}
###### Remark

This means that an [[inner fibration]] $p : X \to Y$ with a collection of $p$-cartesian morphisms in $X$ specified satisfies the same kind of condition as a _[[right fibration]]_ , the only difference being that not _all_ right outer horns inclusion are required to have lifts, but only those where the last edge of the horn maps to a cartesion morphism.

In this sense a [[Cartesian fibration]] is a generalization of a [[right fibration]].

=--


+-- {: .un_prop}
###### Proposition

If $p : X \to Y$ is an [[inner fibration]] of [[quasi-categories]] then a morphism $f : x \to y$ in $X$ is $p$-Cartesian precisely if
for all objects $a$ in $X$ the diagram

  $$
    \array{
      Hom_X(a,x) &\stackrel{Hom_X(a,f)}{\to}& Hom_X(a,y)
      \\
      \downarrow && \downarrow
      \\
      Hom_Y(p(a), p(x)) &\stackrel{Hom_Y(p(a), p(f))}{\to}& 
      Hom_Y(p(a), p(y))
    }
  $$

  of [[hom-object in a quasi-category|hom-objects in a quasi-category]] is 
  a [[homotopy pullback]] square (in [[sSet]] equipped with its [[model structure on simplicial sets|standard model structure]]).


=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 2.4.4.3]].

=--


#### In $sSet$-categories

Let $C$ and $D$ be [[simplicially enriched categories]] and $F : C \to D$ an [[sSet]]-[[enriched functor]].

+-- {: .un_definition}
###### Definition

A morphism $f : x \to y \in C$ is **$F$-cartesian** if it is so under the [[homotopy coherent nerve]] $N : sSet Cat \to sSet$ in the sense of quasi-categories above, i.e. if 

$$
  N(C)_{/f} \to N(C)_{/y} \times_{N(D)_{/F(y)}} N(D)_{/F(f)}
$$

is an acyclic [[Kan fibration]].

=--

+-- {: .un_prop}
###### Proposition

If $C$ and $D$ are enriched in [[Kan complex]]es and if $F$ is hom-wise a [[Kan fibration]], then

* $N(F) : N(C) \to N(D)$ is an [[inner fibration]];

* a morphism $f :x \to y$ in $N(C)$ is an $N(F)$-cartesian morphism precisely if for all objects $a$ in $C$ the diagram

  $$
    \array{
      C(a,x) &\stackrel{C(a,f)}{\to}& C(a,y)
      \\
      \downarrow && \downarrow
      \\
      D(F(a), F(x)) &\stackrel{C(F(a), F(f))}{\to}& 
      D(F(a), F(y))
    }
  $$

  is a [[homotopy pullback]] square in [[sSet]] equipped with its [[model structure on simplicial sets|standard model structure]].


=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 2.4.1.10]].

=--


## Properties

### Pullback along Cartesian morphisms

+-- {: .un_lemma}
###### Lemma

For $p : \mathcal{E} \to \mathcal{C}$ a functor, if in a diagram

$$
  \array{
    A &\stackrel{f}{\to}& B
    \\
    {}^{\mathllap{g}}\downarrow && \downarrow^{\mathrlap{h}}
    \\
    C &\stackrel{k}{\to}& D
  }
$$

in $\mathcal{E}$ the two vertical morphisms are vertical with respect to $p$ (meaning that $p(g) = Id_p(A)$ and $p(h) = Id(B)$) and if the two horizontal morphisms are $p$-Cartesian morphisms, then this square is a [[pullback]] square.

=--

+-- {: .proof}
###### Proof

If 

$$
  \array{
    Q &\stackrel{}{\to}& B
    \\
    \downarrow && \downarrow^{\mathrlap{h}}
    \\
    C &\stackrel{k}{\to}& D
  }
$$

is another cone over $C \to D \leftarrow B$, then its image under $p$
is 

$$
  \array{
    p(Q)
    \\
    \downarrow & \searrow
    \\
    p(C) &\stackrel{p(k)}{\to}& D
  }
  \,.
$$

Since $p(f) = p(k)$, another lift of the right horn of this is given by

$$
  \array{
    Q
    \\
    & \searrow
    \\
    A &\stackrel{f}{\to}& B
  }
$$

which gives a unique filler $Q \to A$ by the fact that $f$ is Cartesian.

But this produces now two fillers -- namely the original $Q \to C$ and the $Q \to A \to C$ just obtained -- of the horn

$$
  \array{
    Q &\to& B
    \\
    && \downarrow
    \\
    C &\stackrel{k}{\to}& D
  }
$$

over 

$$
  \array{
    p(Q)
    \\
    \downarrow & \searrow
    \\
    p(C) &\stackrel{p(k)}{\to}& D
  }
  \,.
$$

Since $k$ is Cartesian, these two fillers must be equal. This means that the morphism $Q \to A$ is a cone morphism and unique as such. Hence the original square is a pullback.

=--

This appears as [[Elephant|Elephant, lemma 1.3.3]].


### Cartesian morphisms and equivalences


+-- {: .un_lemma}
###### Observation

For $C$ a [[category]], a [[morphism]] in $C$ is cartesian with respect to the [[terminal object|terminal]] [[functor]] $C \to *$ precisely if it is an [[isomorphism]].

In particular all [[identity]] morphisms are cartesian.

=--

This is trivial to see. The analog statement holds also for [[quasi-categories]], where it is rather more nontrivial and quite useful:

+-- {: .un_prop}
###### Proposition

For $C$ a [[quasi-category]], a morphism in $C$ is cartesian with respect to the [[terminal object|terminal]] morphism $C \to *$ precisely if it is an [[equivalence in a quasi-category|equivalence]].

More generally, for $p : X \to Y$ an [[inner fibration]], a morphism $f$ in $X$ is an [[equivalence in a quasi-category|equivalence]] precisely if it is $p$-cartesian and $p(f)$ is an equivalence in $Y$.

=--

+-- {: .proof}
###### Proof

The first statement is a proposition of [[Andre Joyal]], slightly reformulated in the language of cartesian morphisms. It appears as [[Higher Topos Theory|HTT, prop 1.2.4.3]]. A proof appears below [[Higher Topos Theory|HTT, corollary 2.1.2.2]].

The second statement is [[Higher Topos Theory|HTT, prop. 2.4.1.5]].

=--



## Variants

+--{: .query}
[[David Roberts]]: There would surely be an [[anafunctor]] version of this, that would require no choices whatsoever. It is unlikely that I would be able to find time to write this up, so my plea goes out to those in the know...

I imagine that there would then be an $(\infty,1)$-version using whatever passes as anafunctors in that setting (dratted memory, failing at the first gate)

[[Mike Shulman]]: Yes, there would surely be such a version.  (-:  The simplest way would be to take the specifications $|f^*|$ for the anafunctor $f^*$ to be the cartesian morphisms over $f$, with domain and codomain giving the functions $\sigma$ and $\tau$.  Unique factorization would give you the values of morphisms.

[[David Roberts]]: just stumbled on this old comment - I'm reading Makkai more closely, and I'm convinced that basically anything defined by a universal property is given by a saturated anafunctor. So this is a heads up for posterity, that a map is a fibration iff the fairly obvious span of functors defines a [[saturated anafunctor]].
=--



## References 

For the 1-categorical case see for instance section B1.3 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

The $(\infty,1)$-categorical version is in section 2.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

See also the references at [[Grothendieck fibration]].


[[!redirects Cartesian morphism]]
[[!redirects Cartesian morphisms]]
[[!redirects cartesian morphism]]
[[!redirects cartesian morphisms]]
[[!redirects opcartesian morphism]]
[[!redirects opcartesian morphisms]]
[[!redirects cocartesian morphism]]
[[!redirects coCartesian morphism]]
[[!redirects cocartesian morphisms]]
