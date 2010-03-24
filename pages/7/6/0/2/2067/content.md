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

The relevance of the notion of cartesian morphism is as an ingredient in the following definition.

+-- {: .un_defn}
###### Definition
**(Grothendieck fibration)**

If for every morphism in $Y$ there is at least one lift through $p$ that is a $p$-cartesian morphism , one says that $p$ is a [[Grothendieck fibration]].

=--

The above definition may equivalently be formulated as follows.

Let 

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

* similarly $Y/p(f)$.



+-- {: .un_defn}
###### Observation

The condition that $f$ is cartesian with respect to $p$ 
is equivalently the condition that the functor

$$
  X/f \to X/{x_2} \times_{Y/{p(x_2)}} Y/p(f)
$$

into the [[pullback]] of the obvious projection $X/{x_2} \to S/p(x_2)$ along the projection $S/p(f) \to S/p(x_2)$ is a [[k-surjective functor|surjective equivalence]]

$$
  \array{
    X/f &\to& Y/p(f)
    \\
    \downarrow && \downarrow
    \\
    X/{x_2} &\to& Y/{p(x_2)}
  }
  \,.
$$

=--


### In $(\infty,1)$-categories

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

The morphism $f : x \to y$ as above is $p$-cartesian precisely if for all $n \geq 2$ and all right outer [[horn]] inclusions

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


## Examples and properties

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

The second statement is [[Higher Topos Theory| prop. 2.4.1.5]].

=--



## Variants

+--{: .query}
[[David Roberts]]: There would surely be an [[anafunctor]] version of this, that would require no choices whatsoever. It is unlikely that I would be able to find time to write this up, so my plea goes out to those in the know...

I imagine that there would then be an $(\infty,1)$-version using whatever passes as anafunctors in that setting (dratted memory, failing at the first gate)

[[Mike Shulman]]: Yes, there would surely be such a version.  (-:  The simplest way would be to take the specifications $|f^*|$ for the anafunctor $f^*$ to be the cartesian morphisms over $f$, with domain and codomain giving the functions $\sigma$ and $\tau$.  Unique factorization would give you the values of morphisms.
=--



## References 

For the 1-categorical case see the references at [[Grothendieck fibration]].

The $(\infty,1)$-categorical version is in section 2.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects Cartesian morphism]]
[[!redirects cartesian morphisms]]
[[!redirects opcartesian morphism]]
[[!redirects opcartesian morphisms]]
[[!redirects cocartesian morphism]]
[[!redirects cocartesian morphisms]]
