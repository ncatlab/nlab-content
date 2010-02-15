
> under construction


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For ordinary [[categories]] there is the notion of 

* [[Grothendieck fibration]] between two categories. 

* and the special case of a [[category fibered in grouopoids]].

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

### Left/Right fibration

A [[morphism]] of [[simplicial set]]s $f : X \to S$ is a **left fibration** of **[[left Kan fibration]]** if its has the [[right lifting property]] with respect to all [[horn]] inclusions except the right outer ones.

It is a **right fibration** or **[[right Kan fibration]]** if its extends agains all horns except the left outer ones

**Proposition** For $S \in sSet$ there is a [[model category]] structure on the [[overcategory]] $sSet/S$ whose cofibrant-fibrant objects are left fibrations over $S$, given by

... (section 2.1.4 , main prop 2.1.4.7).

The morphisms with the [[left lifting property]] against all left/right fibrations are called **left/right anodyne**.


### (co)Cartesian fibration

A [[Cartesian fibration]] is an [[inner fibration]] $p : X \to S$ such that 

* for every edge $f : X \to Y$ of $S$ 

* and every lift $\tilde{y}$ of $y$ (that is, $p(\tilde{y})=y$), 

there is a [[cartesian morphism|Cartesian edge]] $\tilde{f} : \tilde{x} \to \tilde{y}$ in $X$ lifting $f$.

(HTT, def 2.4.2.1)


### Categorical fibration

A **[[categorical fibration]]** is a fibration in the [[model structure for quasi-categories]]: morphism $f : X \to S$ with the [[right lifting property]] against all monomorphic _categorical equivalences_ .

(HTT, p. 81).

### Inner fibration

A [[morphism]] of [[simplicial set]]s $f : X \to S$ is an **inner fibration** or **[[inner Kan fibration]]** if its has the [[right lifting property]] with respect to all inner [[horn]] inclusions.


The morphisms with the [[left lifting property]] against all inner fibrations are called **inner anodyne**.




## Properties

### Trivial fibration


### Kan fibration

### Left/Right fibration

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
