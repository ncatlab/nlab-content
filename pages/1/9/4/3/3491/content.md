
> under construction


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

* categorical fibrations;

* inner fibrations.




## Definition

We list the different definitions in the order of their generality. The examples of each definition are also examples of the following definitions.

All morphisms in the following are morphisms of [[simplicial set]]s.

### Trivial fibration

A **trivial fibration** (trivial [[Kan fibration]]) is a morphism that has the [[right lifting property]] with respect to all boundary inclusions $\partial \Delta[n] \hookrightarrow \Delta[n]$.

### Kan fibration

* for the moment see [[Kan fibration]]

A morphism with [[left lifting property]] against all Kan fibrations is called **anodyne**.

### (Left/)Right fibration

A [[morphism]] of [[simplicial set]]s $f : X \to S$ is a **left fibration** or **left Kan fibration** if its has the [[right lifting property]] with respect to all [[horn]] inclusions except the right outer ones. It is a **right fibration** or **right Kan fibration** if its extends against all horns except the left outer ones.


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

### Trivial fibration


### Kan fibration

### (Left/)Right fibration

All properties of right fibrations hold for left fibrations in the suitably dualized form, and vice versa. We often state explicitly just one of the two.

#### Homotopy lifting property

**Proposition** A morphism $p : X \to X$ of simplicial sets is a left fibration precisely if the canonical morphism

$$
  X^{\Delta[1]} \to X^{\{0\}} \times_{S^{\{0\}}} S^{\Delta^1}
$$

is a trivial fibration.

**Proof** This is a corollary of the characterization of left anodyne morphisms in [Properties of left anodyne maps](#PropRightAnodyne) by [[Andre Joyal]], recalled in [[Higher Topos Theory|HTT, corollary 2.1.2.10]].

#### As fibrations in $\infty$-groupoids

The notion of right fibration of quasi-categories generalizes the notion of [[category fibered in groupoids]]. This follows from the following properties.

**Proposition** For $C \to *$ a right (left) fibration over the [[point]], $C$ is a [[Kan complex]], i.e. an [[∞-groupoid]].

**Proof** Due to [[Andre Joyal]]. Recalled at [[Higher Topos Theory|HTT, prop. 1.2.5.1]].

**Proposition** Right (left) fibrations are preserved by [[pullback]] in [[sSet]]. 

**Corollary** It follows that the fiber $X_c$ of every right fibration $X \to C$ over every point $c \in C$, i.e. the [[pullback]]

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

**Proposition** For $C$ and $D$ quasi-categories that are ordinary [[categories]] (i.e. simplicial sets that are [[nerve]]s of ordinary categories), a morphism $C \to D$ is a right fibration precisely if the correspunding ordinary [[functor]] exhibits $C$ as a [[category fibered in groupoids]] over $D$.

**Proof** This is [[Higher Topos Theory|HTT, prop. 2.1.1.3]].

A canonical class of examples of a [[fibered category]] is the [[codomain fibration]]. This is actually a [[bifibration]]. For an ordinary category, a bifiber of this is just a set. For an $(\infty,1)$-category it is an $\infty$-groupoid. Hence fixing only one fiber of the bifibration should yield a fibration in $\infty$-groupoids. This is asserted by the following statement.

**Proposition** Let $p : K \to C$ be an arbitrary morphism to a [[quasi-category]] $C$ and let $C_{p/}$ be the corresponding [[over quasi-category|under quasi-category]]. Then the canonical propjection $C_{p/} \to C$ is a left fibration.

**Proof** Due to [[Andre Joyal]]. Recalled as [[Higher Topos Theory|HTT, prop 2.1.2.2]].


#### (Left/)Right anodyne moprphisms {#PropRightAnodyne}

**Proposition** The collection of left anodyne morphisms (those with [[left lifting property]] agains left fibrations) is equivalently $LAn = LLP(RLP(LAn_0))$ for the following choices of $LAn_0$:

$LAn_0 =$

* the collection of all left [[horn]] inclusions

  $\{ \Lambda[n]_{i} \to \Delta[n] | 0 \leq i \lt n \}$;

* blah-blah

* blah-blah

**Proof** This is due to [[Andre Joyal]], recalled as [[Higher Topos Theory|HTT, prop 2.1.2.6]].


### (co)Cartesian fibration


### Categorical fibration


### Inner fibration







## References

chapter 2 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects fibrations of simplicial sets]]
[[!redirects left Kan fibration]]
[[!redirects inner Kan fibration]]
[[!redirects right Kan fibration]]
[[!redirects weak Kan fibration]]
[[!redirects left fibration]]
[[!redirects inner fibration]]
[[!redirects right fibration]]
[[!redirects weak fibration]]
