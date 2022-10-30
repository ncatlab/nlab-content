
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For ordinary [[categories]] there is the notion of 

* [[Grothendieck fibration]] between two categories. 

* and the special case of a [[category fibered in groupoids]].

The analog of this for [[quasi-categories]] are

* [[Cartesian fibration]]s

* left/right fibrations of quasi-categories.

There are more types of fibrations between the [[simplicial set]]s underlying the [[quasi-category]]

* inner fibrations -- these correspond to **bundles of [[quasi-categories]]** : an inner fibration $E \to \Delta[1]$ over the interval characterizes the fibers $C, D$ over the endpoints $0,1 \in \Delta[1]$ as [[quasi-categories]]. Notably havingg an inner fibration $C \to \Delta[0]$ over the point says precisely that $C$ is a [[quasi-category]].

* categorical fibrations -- these appear as the fibrations in the sense of [[model category]] theory in the Joyal [[model structure for quasi-categories]] $sSet_{Joyal}$ . But they have no particular intrinsic meaning in [[higher category theory]]. In fact, there is also the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]] which is [[Quillen equivalence|Quillen equivalent]] to $sSet_{Joyal}$ and in which the model-theoretic fibrations coincide precisely with the [[Cartesian fibration]]s that do have an intrinsic category theoretic meaning.



## Definition

We list the different definitions in the order of their generality. The examples of each definition are also examples of the following definitions.

All morphisms in the following are morphisms of [[simplicial set]]s.

### Trivial fibration

A **trivial fibration** (trivial [[Kan fibration]]) is a morphism that has the [[right lifting property]] with respect to all boundary inclusions $\partial \Delta[n] \hookrightarrow \Delta[n]$.

### Kan fibration

* for the moment see [[Kan fibration]]

A morphism with [[left lifting property]] against all Kan fibrations is called **anodyne**.

### (Left/)Right fibration

A [[morphism]] of [[simplicial set]]s $f : X \to S$ is a **left fibration** or **[[left Kan fibration]]** if it has the [[right lifting property]] with respect to all [[horn]] inclusions except the right outer ones. It is a **right fibration** or **right Kan fibration** if its extends against all horns except the left outer ones.


$$
  \array{
    \Lambda[n]_{k \gt 0} &\to& X
    \\
    \downarrow &{}^{\exists}\nearrow& \downarrow
    \\
    \Delta[n] &\to& S
  } 
  \,.
$$

Morphisms with the [[left lifting property]] against all left/right fibrations are called **left/right anodyne** maps.

Write

$$
  RFib(S) \subset sSet/S
$$

for the full [[SSet]]-[[subcategory]] of the [[overcategory]] of [[SSet]] over $S$ on those morphisms that are right fibrations.

This is a [[Kan complex]]-enriched category and as such an incarnation of the **[[(∞,1)-category]] of right fibrations**. 
It is modeled by the [[model structure for left fibrations|model structure for right fibrations]]. For details on this see the discussion at [[(∞,1)-Grothendieck construction]].





### (co)Cartesian fibration

A [[Cartesian fibration]] is an [[inner fibration]] $p : X \to S$ such that 

* for every edge $f : X \to Y$ of $S$ 

* and every lift $\tilde{y}$ of $y$ (that is, $p(\tilde{y})=y$), 

there is a [[cartesian morphism|Cartesian edge]] $\tilde{f} : \tilde{x} \to \tilde{y}$ in $X$ lifting $f$.

(HTT, def 2.4.2.1)

see also

* [[model structure for Cartesian fibrations]]

* [[(∞,1)-Grothendieck construction]]


### Categorical fibration

A **categorical fibration** is a fibration in the [[model structure for quasi-categories]]: morphism $f : X \to S$ with the [[right lifting property]] against all monomorphic _categorical equivalences_ .

(HTT, p. 81).

### Inner fibration

A [[morphism]] of [[simplicial set]]s $f : X \to S$ is an **inner fibration** or **[[inner Kan fibration]]** if its has the [[right lifting property]] with respect to all inner [[horn]] inclusions.


The morphisms with the [[left lifting property]] against all inner fibrations are called **inner anodyne**.




## Properties

+-- {: .un_remark}
###### Remark

By the [[small object argument]] we have that every morphism $f : X \to Y$ of simplicial sets may be factored as

$$
  f : X \to Z \to Y
$$

with $X \to Z$ a left/right/inner anodyne cofibraiton and $Z \to Y$ accordingly a left/right/inner Kan fibration.


=--



### Trivial fibration

...

### Kan fibration

...

### (Left/)Right fibration

+-- {: .un_remark}
###### Remark

Under the operation of forming the [[opposite quasi-category]], left fibrations turn into right fibrations, and vice versa: if $p : C \to D$ is a left fibration then $p^{op} : C^{op} \to D^{op}$ is a right fibration.

Therefore it is sufficient to list properties of only one type of these fib rations, that for the other follows.

=--

#### Homotopy lifting property

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
commuting square

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

+-- {: .un_prop}
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


#### As fibrations in $\infty$-groupoids

The notion of right fibration of quasi-categories generalizes the notion of [[category fibered in groupoids]]. This follows from the following properties.

+-- {: .un_prop}
###### Proposition

For $C \to *$ a right (left) fibration over the [[point]], $C$ is a [[Kan complex]], i.e. an [[∞-groupoid]].

=--

+-- {: .proof}
###### Proof

Due to [[Andre Joyal]]. Recalled at [[Higher Topos Theory|HTT, prop. 1.2.5.1]].

=--


+-- {: .un_prop}
###### Proposition

Right (left) fibrations are preserved by [[pullback]] in [[sSet]]. 

=--


+-- {: .un_corollary}
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


+-- {: .un_prop}
###### Proposition

For $C$ and $D$ quasi-categories that are ordinary [[categories]] (i.e. simplicial sets that are [[nerve]]s of ordinary categories), a morphism $C \to D$ is a right fibration precisely if the correspunding ordinary [[functor]] exhibits $C$ as a [[category fibered in groupoids]] over $D$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 2.1.1.3]].

=--

A canonical class of examples of a [[fibered category]] is the [[codomain fibration]]. This is actually a [[bifibration]]. For an ordinary category, a bifiber of this is just a set. For an $(\infty,1)$-category it is an $\infty$-groupoid. Hence fixing only one fiber of the bifibration should yield a fibration in $\infty$-groupoids. This is asserted by the following statement.

+-- {: .un_prop}
###### Proposition

Let $p : K \to C$ be an arbitrary morphism to a [[quasi-category]] $C$ and let $C_{p/}$ be the corresponding [[over quasi-category|under quasi-category]]. Then the canonical propjection $C_{p/} \to C$ is a left fibration.

=--


+-- {: .proof}
###### Proof

Due to [[Andre Joyal]]. Recalled as [[Higher Topos Theory|HTT, prop 2.1.2.2]].

=--


#### (Left/)Right anodyne moprphisms {#PropRightAnodyne}

+-- {: .un_prop}
###### Proposition

The collection of left anodyne morphisms (those with [[left lifting property]] against left fibrations) is equivalently $LAn = LLP(RLP(LAn_0))$ for the following choices of $LAn_0$:

$LAn_0 =$

* the collection of all left [[horn]] inclusions

  $\{ \Lambda[n]_{i} \to \Delta[n] | 0 \leq i \lt n \}$;

* blah-blah

* blah-blah


=--

+-- {: .proof}
###### Proof

This is due to [[Andre Joyal]], recalled as [[Higher Topos Theory|HTT, prop 2.1.2.6]].

=--


### (co)Cartesian fibration


### Categorical fibration

### Inner fibrations


+-- {: .un_prop}
###### Proposition

A [[simplicial set]] $K$ is the [[nerve]] of an ordinary [[category]] $C$, $K \simeq_{iso} N(C)$ precisely if the terminal morphism $K \to \Delta[0]$ is an inner fibration with _unique_ inner [[horn]] fillers, i.e. precisely if for all morphisms 

$$
   \Lambda[n]_i \to K
$$

with $n \in \mathbb{N}$ and $0 \lt i \lt n$ there is a _unique_ morphism $\Delta[n] \to K$ making the diagram

$$
  \array{
    \Lambda[n]_i &\to& K
    \\
    \downarrow & \nearrow
    \\
    \Delta[n]
  }
$$

commute.
=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 1.1.2.2]]

=--

+-- {: .un_corollary}
###### Corollary

It follows that under the [[nerve]] _every_ functor $f : C \to D$ between ordinary [[categories]] is an inner fibration.

=--

+-- {: .proof}
###### Proof

This is immediate, but let's spell it out:

In any commutative diagram

$$
  \array{
    \Lambda[n] &\to& N(C)
    \\
    \downarrow && \downarrow^{\mathrlap{N(f)}}
    \\
    \Delta[n] && \to& N(D)
  }
$$

by the above the bottom morphism is already unqiely specified by the remaining diagram. 

$$
  \array{
    \Lambda[n] &\to& N(C)
    \\
    \downarrow && \downarrow^{\mathrlap{N(f)}}
    \\
    \Delta[n] && N(D)
  }
  \,.
$$

By the above there exists a unique lift into $N(C)$

$$
  \array{
    \Lambda[n] &\to& N(C)
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{N(f)}}
    \\
    \Delta[n] && N(D)
  }
$$

and by uniqueness of lifts into $N(D)$ this must also make the lower square commute

$$
  \array{
    \Lambda[n] &\to& N(C)
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{N(f)}}
    \\
    \Delta[n] &\to& N(D)
  }
  \,.
$$


=--







## References

chapter 2 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects fibration of quasi-categories]]
[[!redirects fibrations of quasi-categories]]
[[!redirects fibration of simplicial sets]]
[[!redirects fibrations of simplicial sets]]
[[!redirects inner Kan fibration]]
[[!redirects inner Kan fibrations]]
[[!redirects right Kan fibration]]
[[!redirects right Kan fibrations]]
[[!redirects weak Kan fibration]]
[[!redirects weak Kan fibrations]]
[[!redirects inner fibration]]
[[!redirects inner fibrations]]
[[!redirects right fibration]]
[[!redirects right fibrations]]
[[!redirects weak fibration]]
[[!redirects weak fibrations]]
