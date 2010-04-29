In a [[concrete category]], an **injective hull** of an object $A$ is an extension $A \stackrel{m}{\longrightarrow} B$ of $A$ such that $B$ is [[injective object|injective]] and $m$ is an [[essential embedding]]. It is the dual concept to [[projective cover]].

In general, there is no way of making the assignment of the injective hull to an object into a functor such that there is a natural transformation between the identity functor and that functor.


## Examples 

* In [[Vect]] every object $A$ has an injective hull, $A \stackrel{id_A}{\longrightarrow} A$.  In other words, every vector space is already an [[injective object]].
* In [[Pos]] every object has an injective hull, its [[MacNeille completion]].
* In [[Ab]] every object has an injective hull. The embedding $\mathbb{Z} \hookrightarrow \mathbb{Q}$ is an example.
* In the category of fields and algebraic field extensions, every object has an injective hull, its [[algebraic closure]].
* In the category of metric spaces and [[short map]]s, the injective hull is a standard construction also known as the [[tight span]] (see [Wikipedia](http://en.wikipedia.org/wiki/Tight_span)).

## Generalization

Given a class $\mathcal{E}$ of objects in a category, an **$\mathcal{E}$-hull**
(or $\mathcal{E}$-envelope) of an object $A$ is a map $h\colon A\longrightarrow E$
such that the following two conditions hold:

1. Any map $k\colon A\longrightarrow E'$ to an object in $\mathcal{E}$ factors
through $h$ via some map $f: E\longrightarrow E'$.

2. Whenever a map $f\colon E\longrightarrow E$ satisfies $f\circ h = h$ then it
must be an automorphism.

##References##

* [[Jiri Adamek|Jiří Adámek]], [[Horst Herrlich]], [[George Strecker]]; 2004; [[The Joy of Cats]], Definition 9.16 (page 156)
* Ad&#225;mek, Herrlich, Rosick&#253;, Tholen; 2002; [Injective hulls are not natural](http://www.iti.cs.tu-bs.de/~adamek/injective.hulls.AHRT.ps)
* Jinzhog Xu; 1996; Flat Covers of Modules, SLNM 1634.