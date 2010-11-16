
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

[[simplicial set|Simplicial sets]] are the archetypical combinatorial "[[model category|model]]" for the [[(∞,1)-category]] of (compactly generated weakly Hausdorff) [[topological space]]s and equivalently that of [[∞-groupoid]]s, as well as a standard model for the [[(∞,1)-category of (∞,1)-categories]] [[(∞,1)Cat]] itself.

This statement is made precise by the existence of the structure of a [[model category]] on [[sSet]], called the **classical model structure**  that is a [[presentable (infinity,1)-category|presentation]] for the [[(infinity,1)-category]] [[Top]], as well as the **Joyal model structure** which similarly is a presentation of the $(\infty,1)$-category $(\infty,1)Cat$.



## Classical Model Structure

The classical [[model category|model structure]] -- or **Quillen model structure** $sSet_{Quillen}$ on [[sSet]] has the following distinguished classes of morphisms:

* The **cofibrations** $C$ are simply the [[monomorphism]]s $f : X \to Y$ which are precisely the levelwise injections, i.e. the morphisms of simplicial sets such that $f_n : X_n \to Y_n$ is an injection of sets for all $n \in \mathbb{N}$.

* The **weak equivalences** $W$ are **weak homotopy equivalences**, i.e., morphisms whose [[simplicial set|geometric realization]] is a weak homotopy equivalence of topological spaces.

It follows from this that

* This model structure is [[cofibrantly generated model category|cofibrantly generated]] by 

  * the set $I$ of is the set of boundary inclusions of simplices
    $$
      i_n : \partial \Delta[n] \hookrightarrow \Delta[n]
    $$ 

  * the set $J$ of generating cofibrations is the set of [[horn]] inclusions
    $$
      j^k_n : \Lambda^k[n] \hookrightarrow \Delta^n
      \,.
    $$


* The **fibrations** $F$ are the **[[Kan fibration]]s**, i.e., maps $f : X \to Y$ which have the [[right lifting property]] with respect to all [[horn]] inclusions.
  $$
    \array{
      \Lambda^k[n] &\to& X
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^f 
      \\
      \Delta[n] &\to& Y
    }
    \,.
  $$

* A morphism $f : X \to Y$ of fibrant simplicial sets / [[Kan complex]]es is a weak equivalence precisely if it induces an [[isomorphism]] on all [[simplicial homotopy group]]s.

* All simplicial sets are cofibrant with respect to this model structure. 

* The fibrant objects are precisely the [[Kan complex|Kan complexes]].

+-- {: .un_theorem}
###### Theorem

* The **acyclic fibrations** (i.e. the maps that are both fibrations as well as weak equivalences) between [[Kan complex]]es are precisely the morphisms $f : X \to Y$ that have the [[right lifting property]] with respect to all inclusions $\partial \Delta[n] \hookrightarrow \Delta[n]$ of boundaries of $n$-simplices into their $n$-simplices
  $$
    \array{
      \delta \Delta[n] &\to& X
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^f 
      \\
      \Delta[n] &\to& Y
    }
    \,.
  $$

=--

+-- {: .proof}
###### Proof

This is theorem 11.2 on p. 61 of _GoerJar_ (theorem 7.10, page 34 in the online version below).

=--



Importantly, this model structure is [[Quillen equivalence|Quillen equivalent]] to the [[model structure on topological spaces]] with weak homotopy equivalences as weak equivalences and Serre fibrations as fibrations via the geometric realization and total singular complex functors described [[simplicial set|here]].


### Relation to the model structure on strict $\infty$-groupoids 

> [[Urs Schreiber|Urs]] it would be nice to eventually have a discussion of the following

Recall the [[model structure on strict omega-groupoids]] and the [[omega-nerve]] operation

$$
  N : Str \infty Grpd \to Kan Complx
  \,.
$$

>this ought to be a Quillen functor, but is it? is there a reference?

As a warmup, let $C, D$ be ordinary [[groupoid]]s and $N(C)$, $N(D)$ their ordinary [[nerve]]s. We'd like to show in detail that 

+-- {: .un_theorem}
###### Theorem

A [[functor]] $F : C \to D$ is 

* [[k-surjective functor|k-surjective]] for all $k$ and hence a surjective [[equivalence of categories]] precisely if under the [[nerve]] $N(F) : N(C) \to N(D)$ it induces an acyclic fibration of Kan complexes;

=--

+-- {: .proof}
###### Proof

We know that both $N(C)$ and $N(D)$ are Kan complexes. By the above theorem it suffices to show that $N(f)$ being a surjective equivalence is the same as having all lifts

$$
  \array{
    \delta \Delta[n] &\to& N(C)
    \\
    \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
    \\
    \Delta[n] &\to& N(D)
  }
  \,.
$$


We check successively what this means for increasing $n$:

* $n= 0$. In degree 0 the boundary inclusion is that of the empty set into the [[point]] $\emptyset \hookrightarrow {*}$. The lifting property in this case amounts to saying that every point in $N(D)$ lifts through $N(F)$. 
  $$
    \array{
      \emptyset &\to& N(C)
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \Leftrightarrow
    \array{
      && N(C)
      \\
      &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \,.
  $$
  This precisely says that $N(F)$ is surjective on 0-cells and hence that $F$ is surjective on objects.

* $n=1$. In degree 1 the boundary inclusion is that of a pair of points as the endpoints of the interval
  $\{\circ, \bullet\} \hookrightarrow \{\circ \to \bullet\}$. The lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ all elements in $Hom(F(a),F(b))$ are hit. Hence that $F$ is a [[full functor]].

* $n=2$. In degree 2 the boundary inclusion is that of the triangle as the boundary of a filled triangle. It is sufficient to restrict attention to the case that the map $\partial \Delta[2] \to N(C)$ sends the top left edge of the triangle to an identity. Then the lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ the map $F_{a,b} : Hom(a,b) \to Hom(F(a),F(b))$ is injective. Hence that $F$ is a [[faithful functor]].
  $$
    \left(
    \array{
      && b 
      \\
      & {}^{Id_a}\nearrow && \searrow^{f}
      \\
      a &&\stackrel{g}{\to}&& b
    }
    \right)
    \stackrel{N(F)}{\mapsto}
    \left(
    \array{
      && b 
      \\
      & {}^{Id_a}\nearrow &\Downarrow^=& \searrow^{F(f)}
      \\
      a &&\stackrel{F(g)}{\to}&& b
    }
    \right)
  $$


=--



## Joyal's Model Structure

There is a second model structure on $sSet$ -- the **[[model structure for quasi-categories]]** $sSet_{Joyal}$ -- which is different (not [[Quillen equivalence|Quillen equivalent]]) to the classical one, due to [[Andre Joyal]], with the following distinguished classes of morphisms:

* The cofibrations $C$ are monomorphisms, equivalently, levelwise injections.

* The weak equivalences $W$ are **[[equivalence of quasi-categories|weak categorical equivalences]]**, which are morphisms $u : A \rightarrow B$ of simplicial sets such that the induced map $u^* : X^B \rightarrow X^A$ of internal-homs for all [[quasi-category|quasi-categories]] $X$ induces an isomorphism when applying the functor $\tau_0$ that takes a simplicial set to the set of isomorphism classes of objects of its fundamental category.

* The fibrations $F$ are called variously **isofibrations** or **[[Kan fibration|quasi-fibration]]s**. As always, these are determined by the classes $C$ and $W$.
Quasi-fibrations between Kan complexes they have a relatively simple description; they are precisely the maps that have the right lifting property with respect to the inner [[horn] inclusions and also the inclusion $j_0 : * \rightarrow J$ where $*$ is the terminal simplicial set and $J$ is the nerve of the groupoid on two objects with one non-trivial isomorphism. 

All objects are cofibrantly generated. The fibrant objects are precisely the quasi-categories.

This model structure is cofibrantly generated. The generating cofibrations are the set $I$ described above. There is no known explicit description for the generating trivial cofibrations.

Importantly, this model structure is Quillen equivalent to several alternative model structures for the ''homotopy theory of homotopy theories" such as that on the category of [[simplicially enriched category|simplicially enriched categories]].

### Comparison

Every weak categorical equivalences is a weak homotopy equivalence. Since both model structures have the same cofibrations, it follows that the classical model structure is a [[Bousfield localization]] of Joyal's model structure.

The Quillen model structure is the left [[Bousfield localization of model categories|Bousfield localization]] of $sSet_{Joyal}$ at the outer [[horn]] inclusions.

## Fibrant replacement 

Fibrant replacemennt in $sSet_{Quillen}$ models the process of _$\inftty$-groupoidification_ , of freely inverting all [[k-morphism]]s in a simplicial set. Techniques for fibrant replacements $sSet_{Quillen}$ are discussed at

* [[Kan fibrant replacement]].

## References 

[[Dan Quillen]]'s original proof (in *Homotopical Algebra*, LNM 43, Springer, 1967) is purely combinatorial (i.e. does not use topological spaces): he uses the theory of minimal Kan fibrations, the fact that the latter are fiber bundles, as well as the fact that the classifying space of a simplicial group is a Kan complex. This proof has been rewritten several times in the literature: at the end of

* S.I. Gelfand and Yu. I. Manin, *Methods of Homological Algebra*, Springer, 1996

as well as in

* [[Andre Joyal]] and M. Tierney _An introduction to simplicial homotopy theory_ ([web](http://hopf.math.purdue.edu/cgi-bin/generate?/Joyal-Tierney/JT-chap-01))

A proof (in fact two variants of it) using Kan's $Ex^\infty$ functor (see [[Kan fibrant replacement]]) is given in  

* [[Denis-Charles Cisinski]], _Ast&#233;risque 308_

the fun part is not that much about the existence of model structure, but to prove that the fibrations are precisely the [[Kan fibration]]s (and also to prove all the good properties of $Ex^\infty$ without using topological spaces); for two different proofs of this fact using $Ex^\infty$, see Prop. 2.1.41 as well as Scholium 2.3.21 for an alternative). For the rest, everything was already in the book of Gabriel and Zisman, for instance.

Another standard reference for the classical model structure is

* [[Paul Goerss]], Jardine, _Simplicial homotopy theory_ (Birkh&#228;user) ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)).

A reference with lots of details on Joyal's model structure is

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
