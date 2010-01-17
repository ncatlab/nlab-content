##Idea

A very interesting discussion took place at the **nForum** involving [[André Joyal]], [[Urs Schreiber]], and others:

* [The nLab in the eyes of others](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=548)

It was there that the germ of a potentially exciting idea arose. Just as the **nLab** itself arose out of the needs of a community built up around the **[nCafe](http://golem.ph.utexas.edu/category/)**, could a new **CatLab** be built around the **[Category Theory Mailing List](http://blog.gmane.org/gmane.science.mathematics.categories)**?

The **CatLab** would be pari passu with the **nLab** and serve as a model for other mathematics communities. 

Here is the specific invitation extended by Andr&#233;:

>First, I thank Urs for inviting me to join your discussion. I was surprised, and pleased, by your interest in my potential collaboration. I will have to learn some MathML before actually contributing. As you know, I have suggested creating a CatLab not subordinated to the nLab. Let me try to explain my position clearly. It is partly a question of image, but as you know, the image can be important, since it carries a message about the nature and the goal of an organisation. The nLab is already successful and it will probably inspire other peoples in other fields into creating something similar. Let us try to think about the future. Mathematics is divided into branches and there is a social aspect attached to the division. Most mathematicians feel at lost outside their field. Nothing can stop them from creating a Lab for working in their field if they want to. They will chose the name of their lab according to the name of their field and its steering committee will reflect the sociology of their field. But the division of mathematics into fields is somewhat artificial and it can be an obstacle to progress. Assuming that everybody will eventually have a Lab in their field, these labs should be connected. In other words there should be a network of interconnected labs. The payoff of such a network could be enormous in terms of expansion and better efficiency of research and education in mathematics. The name of the network should probably be generic (like MathLabs ?). The lab devoted to category theory could be called CatLab. Category theory and higher category theory could emerge as unifying disciplines by the number of connections to them.

>In other words, I am inviting you to think about the future now.

After being reassured that there was no need to learn MathML (**CatLab** would be based on [itex](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html), a close cousin to LaTeX), he continued:

>The unity and diversity of mathematics are complementary, not contradictory. It would be very good for mathematics to have a neutral network of interconnected labs reflecting this unity and diversity.

>I think that category theory and higher category theory could prosper enormously in such a network. Everyone should feel at home in his lab, without having to submit to a global ideology of category theory, or of higher category theory, or of constructive mathematics, or anything else.

Before rushing into the creation of **CatLab**, it is the purpose of this page to serve as a seed for its creation. The virtual ribbon cutting should be orchestrated by an active member of the **Category Theory Mailing List** and this page may serve as something of a **CatLab** sandbox to help potential  contributors get familiar with the possibilities.

##Discussion

## Definition

A _category_ $C$ consists of 

* a [[set]] $C_0$ of _[[objects]]_;

* for each pair of objects $a,b\in C_0$, a set $C(a,b)$ of _[[morphisms]]_ (or _arrows_) $a\to b$; when the context is clear, we write $f:a\to b$ to indicate that $f\in C(a,b)$;

* for each triples of objects $a,b,c\in C_0$, a [[composition|composition law]] $C(b,c)\times C(a,b)\to C(a,c)$; when the context is clear, we write
 $g f:a\to c$ for the composite of $f:a\to b$ with $g:b\to c$;

* for each objet $a\in C_0$, an arrow $1_a:a\to a$ called the _unit_ or the
_identity_ of $a$.


* such that the following properties are satisfied:

  * ( _associativity law_) $h (g f)=(h g) f$ for every triple of arrows $f:a\to b$, $g:b\to c$ and $h:c\to d$;

  * (the _left and right unit laws_) $1_b f=f 1_a =f$ for every arrow $f:a\to b$.

## Notation

The set $C_0$ of objects of a category $C$ is often denoted $Ob(C)$.
But we shall often write $a\in C$ instead of $a\in Ob(C)$;
the set $C(a,b)$ is often denoted $hom_C(a,b)$, or just $hom(a,b)$
if the context is clear. A morphism $f:a\to a$ is said to be
an _endomorphism_ of the object $a$. The composition law
gives the set $hom(a,a)$ the structure of a monoid.

## Size issues 

The sets involved in the definition of a category can be small or 
large. A category $C$ is said to be _[[locally small category|locally small]]_ if the set 
$C(a,b)$ is small for every pair of objects $a,b\in C$. 
A category $C$ is said to be _[[small category|small]]_ if it is locally small and its set of objects $Ob(C)$ is small.
A category is said to be _[[large category|large]]_ if it is not small. 

## Examples

* We shall denote by [[Set]], the _[[Set|category of small sets]]_: an object of this category is a small set $S$ and an arrow $S\to T$ is a map $f:S\to T$; Composition of arrows is defined by composing the maps, and the units
arrows are the identity maps. The category $Set$ is large but locally small.


* Let $R$ be a ring. We shall denote by $Mat(R)$ the 
_category of matrices with coefficients in_ $R$; an object of this category is a natural number $n\geq 0$ and a morphism $m\to n$
is a $n\times m$ matrix with coefficients in $R$; the composite of
a matrix $A:m\to n$ with a matrix $B:n\to p$ is their product $B A:m\to p$;
the unit of $n$ is the $n\times n$ unit matrix. The category $Mat(R)$
is small.


* Let $R$ be a ring. We shall denote by $Mat(R)$ the 
_category of matrices with coefficients in_ $R$; an object of this category is a natural number $n\geq 0$ and a morphism $m\to n$
is a $n\times m$ matrix with coefficients in $R$; the composite of
a matrix $A:m\to n$ with a matrix $B:n\to p$ is their product $B A:m\to p$;
the unit of $n$ is the $n\times n$ unit matrix. The category $Mat(R)$
is small.

* [[Grp]] - [[group]]s as objects, homomorphisms as morphisms.

* [[Ab]] - [[abelian group]]s as objects, homomorphisms as morphisms.

* [[Top]] - [[topological space]]s as objects, continuous functions as morphisms.


* [[Ring]] - [[ring]]s as objects, ring homomorphisms as morphisms.
 
These classic examples are the original motivation for the term "category": all of the above categories encapsulate one "kind of mathematical structure".  These are often called "concrete" categories (that term also has a [[concrete category|technical definition]] that these examples all satisfy).  


* **Poset** A [[partial order|poset]] can be thought of as a category with its elements as objects and one morphism in each $hom(x,y)$ if $x$ is less than or equal to $y$, but none otherwise.  


* **Monoid** A category with a single object $\star$
is a monoid $Hom(\star,\star)$.
In fact, this is one way to motivate the concept of categories: categories are the [[horizontal categorification|many object version]] of monoids.


## Definition

* A morphism $f:a\to b$ is a category is said to be _inversible_ ,
or to be an _isomorphism_ if there exists a morphism $h:b\to a$ such that $h f=1_a$ and $f h=1_b$, in which
case $h$ is said to be the _inverse_ of $f$ and we write $h=f^{-1}$
(the inverse is unique when it exists).  The composite
of two isomorphisms $f: a \to b$ and $g:b\to c$
is an isomorphism and we have $(g f)^{-1}=f^{-1}g^{-1}$.    

* A _groupoid_ is a category in which every morphism is inversible.


## Examples

* A map $f:S\to T$ in the category [[Set]] invertible iff it is
_bijective_. 

* An isomorphism in the category [[Top]] is said to be a _homeomorphism_.

* The isomorphisms of a category $C$ are closed under composition.
They form a category $Iso(C)$ having the same objects as $C$. The
category $Iso(C)$ is a groupoid. 



* **Group** A [[group]] is a groupoid with a single object.
In fact, groupoids are the [[horizontal categorification|many object version]] of groups.



## Definition

* 

##Reference

* [[HowTo]]
* [[Sandbox]]
* [itex Command Summary](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html)
* [[FAQ]]
* [The nLab in the eyes of others](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=548)


category: meta