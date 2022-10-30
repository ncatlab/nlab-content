## Idea

An abelian model category is an [[abelian category]] with a compatible [[model structure]].

## Definition

An **abelian model category** is an [[abelian category]] $\mathcal{A}$ that is [[complete category|complete]] and [[cocomplete category|cocomplete]], together with a [[model structure]] such that

* (AMC1) A [[morphism]] $i : A \to B$ is a [[cofibration]] if and only if it is a [[monomorphism]] with [[cofibrant object|cofibrant]] [[cokernel]].
* (AMC2) A [[morphism]] $p : X \to Y$ is a [[fibration]] if and only if it is an [[epimorphism]] with [[fibrant object|fibrant]] [[kernel]].

## Relation to cotorsion pairs

[Hovey](#Hovey) has shown that, roughly speaking, [[model structures]] on [[abelian categories]] correspond to [[cotorsion pairs]].

In one direction we have

+-- {: .num_prop}
###### Proposition
Let $\mathcal{A}$ be an [[abelian model category]], i.e. an [[abelian category]] with a compatible [[model structure]].  Let $\mathcal{C}$, $\mathcal{F}$, and $\mathcal{W}$ denote the classes of cofibrant, fibrant, and trivial objects, respectively.

Then $(\mathcal{C} \cap \mathcal{W}, \mathcal{F})$ and $(\mathcal{C}, \mathcal{F} \cap \mathcal{W})$ are complete [[cotorsion pairs]].
=--

And under some more assumptions we have a converse

+-- {: .num_theorem}
###### Theorem
Let $\mathcal{A}$ be an [[abelian category]] that is [[complete category|complete]] and [[cocomplete category|cocomplete]].  Let $\mathcal{C}$, $\mathcal{F}$, and $\mathcal{W}$ denote three classes of objects in $\mathcal{A}$, such that $\mathcal{W}$ is a [[thick subcategory]], and $(\mathcal{C} \cap \mathcal{W}, \mathcal{F})$ and $(\mathcal{C}, \mathcal{F} \cap \mathcal{W})$ are complete [[cotorsion pairs]].

Then there exists a unique [[abelian model structure]] on $\mathcal{A}$ such that $\mathcal{C}$, $\mathcal{F}$, $\mathcal{W}$ are the classes of [[cofibrant]], [[fibrant]], and trivial objects, respectively.
=--

Under certain assumptions on the cotorsion pair we can further guarantee that the associated model structure is [[monoidal model category|monoidal]].

+-- {: .num_theorem}
###### Theorem
Under the assumptions of the previous theorem, suppose further that $\mathcal{A}$ is [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]], and that

* Every object in the class $\mathcal{C}$ is [[flat]] ($X \otimes \cdot$ is an [[exact functor]]).
* For any two objects $X$ and $Y$ in $\mathcal{C}$, the tensor product $X \otimes Y$ is also in $\mathcal{C}$.  If one of $X$ and $Y$ is further in $\mathcal{W}$ then $X \otimes Y$ is also in $\mathcal{W}$.
* The unit is in $\mathcal{C}$.

Then $\mathcal{A}$ is a [[monoidal model category]] (with the model structure given by the previous theorem).
=--

## References

* [[Mark Hovey]], _Cotorsion pairs, model category structures, and representation theory_, Math. Z. 241 (2002), no. 3, 553&#8211;592. MR 2003m:55027
{#Hovey}

An overview is in

* [[Mark Hovey]], _Cotorsion pairs and model categories_, 2006 ([pdf](http://homepages.math.uic.edu/~bshipley/hovey.pdf))


[[!redirects abelian model categories]]
[[!redirects abelian model structure]]
[[!redirects abelian model structures]]