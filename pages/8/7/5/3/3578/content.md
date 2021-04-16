

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

For ordinary [[categories]] there is the notion of 

1. [[Grothendieck fibration]] between two categories. 

2. and the special case of a [[fibration fibered in groupoids]].

The analog of this for [[quasi-categories]] are

1. [[Cartesian fibration]]s

2. the special case of left/right (Kan-) [[fibrations of quasi-categories]]

respectively. 


## Definition

A [[morphism]] of [[simplicial set]]s $f : X \to S$ is a **left fibration** or **left Kan fibration** if it has the [[right lifting property]] with respect to all [[horn]] inclusions $\Lambda[n]_k \to \Delta[n]$ except possibly the right outer ones: $0 \leq k \lt n$. 

It is a **right fibration** or **right Kan fibration** if its extends against all horns except possibly the left outer ones: $0 \lt k \leq n$.

So $X \to S$ is a left fibration precisely if for all commuting squares

$$
  \array{
    \Lambda[n]_{k} &\to& X
    \\
    \downarrow &{}^{\exists}\nearrow& \downarrow
    \\
    \Delta[n] &\to& S
  } 
$$

for $n \in \mathbb{N}$ and $0 \leq k \lt n$, a diagonal lift exists as indicated.

Morphisms with the [[left lifting property]] against all left/right fibrations are called **left/right anodyne** maps.

Write

$$
  RFib(S) \subset sSet/S
$$

for the full [[SSet]]-[[subcategory]] of the [[overcategory]] of [[sSet]] over $S$ on those morphisms that are right fibrations.

This is a [[Kan complex]]-enriched category and as such an incarnation of the **[[(∞,1)-category]] of right fibrations**. 
It is modeled by the [[model structure for left fibrations|model structure for right fibrations]]. For details on this see the discussion at [[(∞,1)-Grothendieck construction]].


## Motivation: ordinary fibrations in groupoids are right Kan fibrations {#GrothGrpdFibsAreRightKanFibs}

Ordinary [[fibration fibered in groupoids|categories fibered in groupoids]] have a simple characterization in terms of their [[nerve]]s. Let $N : Cat \to sSet$ be the [[nerve]] functor and for $p : E \to B$ a morphism in [[Cat]] (a [[functor]]), let $N(p) : N(E) \to N(B)$ be the corresponding morphism in [[sSet]].

Then

+-- {: .num_prop }
###### Proposition

The functor $p : E \to B$ is an  [[fibration fibered in groupoids|fibration in groupoids]] precisely if the morphism $N(p) : N(E) \to N(B)$ is a right Kan fibration of simplicial sets
=--

To see this, first notice the following facts:

+-- {: .num_lemma }
###### Lemma 1

For $C$ a [[category]], the [[nerve]] $N(C)$ is [[coskeletal|2-coskeletal]]. In particular all $n$-spheres for $n \geq 3$ have unique fillers

$$
  \array{
    \partial \Delta[n] &\stackrel{\forall}{\to}& N(C)
    \\
    \downarrow & \nearrow_{\mathrlap{\exists !}}
    \\
    \Delta[n]
  }
    \;\;\;\;\;
    (n \geq 3)
$$

and (implied by that) all $n$-horns for $n \gt 3$ have fillers

$$
  \array{
    \partial \Lambda[n] &\stackrel{\forall}{\to}& N(C)
    \\
    \downarrow & \nearrow_{\mathrlap{\exists }}
    \\
    \Delta[n]
  }
  \;\;\;\;\;
  (n \gt 3)
  \,.
$$


=--

This is discussed at [[nerve]].

+-- {: .num_lemma }
###### Lemma 2

If $p : E \to B$ is an ordinary [[functor]], then $N(f) : N(E) \to N(B)$ is an [[inner fibration]], meaning that its has the [[right lifting property]] with respect to all _inner_ horn inclusions $\Lambda[n]_i \hookrightarrow \Delta[n]$ for $0 \lt i \lt n$.

=--

This is discussed at [[inner fibration]].

+-- {: .proof}
###### Proof of the proposition

From the above lemmas it follows that $N(p) : N(E) \to N(B)$ is a right fibration already precisely if it has the right lifting property with respect only to the three horn inclusions 

$$
  \{  \Lambda[n]_n \hookrightarrow \Delta[n] | n = 1,2,3\}
  \,.
$$

So we check explicitly what these three conditions amount to

* $n=1$ -- The existence of all fillers

  $$
    \array{
      \Lambda[1]_1 = \Delta^{\{1\}} &\stackrel{e}{\to}& N(E)
      \\
      \downarrow & {}^{{\hat f}}\nearrow  & \downarrow^{\mathrlap{N(p)}}
      \\
      \Delta^{\{0 \to 1\}} &\stackrel{f}{\to}& N(B)
    }
  $$

  means that for all objects $e \in E$ and morphism $f : b \to p(e) $ in $B$, there exists a morphism $\hat f : \hat b \to e$ in $E$ such that $p(\hat f) = f$.

* $n=2$ -- The existence of fillers

  $$
    \array{
      \Lambda[2]_2 &\stackrel{e}{\to}& N(E)
      \\
      \downarrow & {}^{{\hat f}}\nearrow  & \downarrow^{\mathrlap{N(p)}}
      \\
      \Delta[2] &\stackrel{f}{\to}& N(B)
    }
  $$

  means that for all diagrams

  $$
    \array{
       && e_1 
       \\
       &&& \searrow^{\mathrlap{\epsilon_{12}}}
       \\
       e_0 &&\stackrel{\epsilon_{02}}{\to}&& e_2
    }
  $$
  
  in $E$ and commuting triangles

  $$
    \array{
       && p(e_1) 
       \\
       & {}^{\mathllap{f}}\nearrow&& \searrow^{\mathrlap{p(\epsilon_{12}})}
       \\
       p(e_0) &&\stackrel{p(\epsilon_{02})}{\to}&& p(e_2)
    }
  $$
 
  in $B$, there is a commuting triangle

  $$
    \array{
       && e_1 
       \\
       &{}^{\mathllap{\hat f}}\nearrow&& \searrow^{\mathrlap{\epsilon_{12}}}
       \\
       e_0 &&\stackrel{\epsilon_{02}}{\to}&& e_2
    }
  $$

  in $E$, such that $p(\hat f ) = f$.

* $n=3$ -- ...

  Consider first the case of degenrate 3-simplices on $N(B)$, 
  on 2-simplices as above. 

  Suppose in the above situation two lifts $(\hat f)_1$ and $(\hat f)_2$
  are found. Together these yield a $\Lambda[3]_3$-horn in $N(E)$.
  The filler condition says this can be filled, which implies 
  that $(\hat f)_1 = (\hat f)_2$.

  So the $n=3$-condition implies that the lift 
  whose existence is guaranteed by the 
  $n=2$-condition is unique.

  By similar reasoning one sees that this is all the $n=3$-condition yields.

In total, these three lifting conditions are precisely those
for a Grothendieck fibration in groupoids.

=--


## Properties

+-- {: .num_remark}
###### Remark

Under the operation of forming the [[opposite quasi-category]], left fibrations turn into right fibrations, and vice versa: if $p : C \to D$ is a left fibration then $p^{op} : C^{op} \to D^{op}$ is a right fibration.

Therefore it is sufficient to list properties of only one type of these fib rations, that for the other follows.

=--

### Homotopy lifting property

In classical [[homotopy theory]], a continuous map $p : E \to B$ of [[topological spaces]] is said to have the [[homotopy lifting property]] if it has the [[right lifting property]] with respect to all morphisms $Y \stackrel{(Id, 0)}{\to} Y \times I$ for $I = [0,1]$ the standard [[interval]] and every commuting diagram

$$
  \array{
    Y &\to& E
    \\
    \downarrow && \downarrow
    \\
    Y \times I &\to& B
  }
$$

there exists a lift $\sigma : Y \times I \to E$ making the two triangles

$$
  \array{
    Y &\to& E
    \\
    \downarrow &{}^\sigma\nearrow& \downarrow
    \\
    Y \times I &\to& B
  }
$$

commute. For $Y = *$ the [[point]] this can be rephrased as saying that the 
universal morphism $E^I \to B^I \times_B E$ induced by the commuting square

$$
  \array{
    E^I &\to& E
    \\
    \downarrow && \downarrow
    \\
    B^I &\to& B
  }
$$

is an [[epimorphism]]. If it is even an [[isomorphism]] then the lift $\sigma$ exists _uniquely_ . This is the situation that the following proposition generalizes:

+-- {: .num_prop}
###### Proposition

A morphism $p : X \to S$ of simplicial sets is a left fibration precisely if the canonical morphism

$$
  X^{\Delta[1]} \to X^{\{0\}} \times_{S^{\{0\}}} S^{\Delta^1}
$$

is a trivial Kan fibration.

=--


+-- {: .proof}
###### Proof

This is a corollary of the characterization of left anodyne morphisms in [Properties of left anodyne maps](#PropRightAnodyne) by [[Andre Joyal]], recalled in [[Higher Topos Theory|HTT, corollary 2.1.2.10]].

=--


### As fibrations in $\infty$-groupoids
 {#AsFibrationsInInfinityGroupoids}

The notion of right fibration of quasi-categories generalizes the notion of [[category fibered in groupoids]]. This follows from the following properties.

+-- {: .num_prop #OverKanComplex}
###### Proposition

Over a [[Kan complex]] $T$, left fibrations $S \to T$ are automatically [[Kan fibration]]s.

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, prop. 2.1.3.3]].

=--

As an important special case of this we have

+-- {: .num_corollary}
###### Corollary

For $C \to *$ a right (left) fibration over the [[point]], $C$ is a [[Kan complex]], i.e. an [[∞-groupoid]].

=--

+-- {: .proof}
###### Proof

This is originally due to [[Andre Joyal]]. Recalled at [[Higher Topos Theory|HTT, prop. 1.2.5.1]].

=--


+-- {: .num_prop #PreservationByPullback}
###### Proposition

Right (left) fibrations are preserved by [[pullback]] in [[sSet]]. 

=--


+-- {: .num_corollary}
###### Corollary

It follows that the fiber $X_c$ of every right fibration $X \to C$ over every point $c \in C$, i.e. the [[pullback]]

$$
  \array{
    X_c &\to& X
    \\
    \downarrow && \downarrow
    \\
    \{c\} &\to& C
  }
$$

is a [[Kan complex]].

=--


+-- {: .num_prop}
###### Proposition

For $C$ and $D$ quasi-categories that are ordinary [[categories]] (i.e. simplicial sets that are [[nerve]]s of ordinary categories), a morphism $C \to D$ is a right fibration precisely if the correspunding ordinary [[functor]] exhibits $C$ as a [[category fibered in groupoids]] over $D$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 2.1.1.3]].

=--

A canonical class of examples of a [[fibered category]] is the [[codomain fibration]]. This is actually a [[bifibration]]. For an ordinary category, a bifiber of this is just a set. For an $(\infty,1)$-category it is an $\infty$-groupoid. Hence fixing only one fiber of the bifibration should yield a fibration in $\infty$-groupoids. This is asserted by the following statement.

+-- {: .num_prop}
###### Proposition

Let $p : K \to C$ be an arbitrary morphism to a [[quasi-category]] $C$ and let $C_{p/}$ be the corresponding [[over quasi-category|under quasi-category]]. Then the canonical propjection $C_{p/} \to C$ is a left fibration.

=--

Due to [[Andre Joyal]]. Recalled as [[Higher Topos Theory|HTT, prop 2.1.2.2]].



### (Left/)Right anodyne morphisms {#PropRightAnodyne}

+-- {: .num_prop}
###### Proposition

The collection of left anodyne morphisms (those with [[left lifting property]] against left fibrations) is equivalently $LAn = LLP(RLP(LAn_0))$ for the following choices of $LAn_0$:

$LAn_0 =$

1. the collection of all left [[horn]] inclusions

  $\{ \Lambda[n]_{i} \to \Delta[n] | 0 \leq i \lt n \}$;

1. the collection of all inclusions of the form

   $$
     (\Delta[m] \times \{0\})
     \coprod_{\partial \Delta[m] \times \{0\}}
     (\partial \Delta[m] \times \Delta[1])
     \hookrightarrow
     \Delta[m] \times \Delta[1]
   $$

1. the collection of all inclusions of the form

   $$
     (S' \times \{0\})
     \coprod_{S \times \{0\}}
     (S \times \Delta[1])
     \hookrightarrow
     S' \times \Delta[1]
   $$

   for all inclusions of simplicial sets $S \hookrightarrow S'$.

=--

This is due to [[Andre Joyal]], recalled as [[Higher Topos Theory|HTT, prop 2.1.2.6]].

+-- {: .proof}
###### Proof

...

=--


+-- {: .num_cor}
###### Corollary

For $i : A \to A'$ left-anodyne and $j : B \to B'$ a cofibration in the [[model structure for quasi-categories]], the canonical morphism

$$
  (A \times B') \coprod_{A \times B} (A' \times B)
  \to 
  A' \times B'
$$

is left-anodyne.

=--

This appears as [[Higher Topos Theory|HTT, cor. 2.1.2.7]].



+-- {: .num_cor}
###### Corollary

For $p : X \to S$ a left fibration and $i : A \to B$ a cofibration of simplicial sets, the canonical morphism

$$
  q : X^B \to X^A \times_{S^A} S^B
$$

is a left fibration. If $i$ is furthermore left anodyne, then it is an acyclic [[Kan fibration]].

=--

This appears as [[Higher Topos Theory|HTT, cor. 2.1.2.9]].


+-- {: .num_prop}
###### Proposition

For $f : A_0 \to A$ and $g : B_0 \to B$ two inclusions of [[simplicial set]]s with $f$ left anodyne, we have that the canonical morphism

$$
  (A_0 \star B ) \coprod_{A_0 \star B_0} (A \star B_0)
  \to
  A \star B
$$

into the [[join of simplicial sets]] is left anodyne.

=--

This is due to [[Andre Joyal]]. It appears as [[Higher Topos Theory|HTT, lemma 2.1.4.2]].

+-- {: .num_prop}
###### Proposition
**(restriction of over-quasi-categories along left anodyne inclusions)**

Let $p : B \to S$ be a morphism of [[simplicial set]]s and $i : A \to B$ a left anodyne morphism, then the restriction morphism of [[over quasi-categories|under quasi-categories]]

$$
  S_{/p} \to S_{/p|_A}
$$

is an acyclic [[Kan fibration]].

=--

This is a special case of what appears as [[Higher Topos Theory|HTT, prop. 2.1.2.5]], which is originally due to [[Andre Joyal]].


+-- {: .num_prop}
###### Proposition

Let $p : X \to S$ be a morphism of simplicial sets with [[section]] $s : S \to X$. If there is a fiberwise simplicial [[homotopy]] $X \times \Delta[1] \to S$ from $s \circ p $ to $Id_X$ then $s$ is left anodyne.

=--

This appears as [[Higher Topos Theory|HTT, prop. 2.1.2.11]].

## Related concepts

* [[Kan fibration]], [[anodyne morphism]]

* **right/left Kan fibration**, [[right/left anodyne map]]

  * [[model structure for left fibrations]]

  * [[universal right fibration]]

* [[inner fibration]]

* [[Cartesian fibration]]  

* [[right/left fibration of simplicial spaces]]


## References

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

* {#AyalaFrancis17} [[David Ayala]], [[John Francis]], _Fibrations of $\infty$-Categories_ ([arXiv:1702.02681](https://arxiv.org/abs/1702.02681))


[[!redirects left/right Kan fibrations]]

[[!redirects left fibration]]
[[!redirects left fibrations]]
[[!redirects left Kan fibration]]
[[!redirects left Kan fibrations]]

[[!redirects right fibration]]
[[!redirects right fibrations]]
[[!redirects right Kan fibration]]
[[!redirects right Kan fibrations]]

[[!redirects left anodyne morphism]]
[[!redirects right anodyne morphism]]

[[!redirects left anodyne morphisms]]
[[!redirects right anodyne morphisms]]


[[!redirects left anodyne map]]
[[!redirects right anodyne map]]

[[!redirects left anodyne maps]]
[[!redirects right anodyne maps]]

[[!redirects right/left anodyne map]]
