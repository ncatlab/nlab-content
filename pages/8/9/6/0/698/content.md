#Idea#

A _strict model 2-category_ is a [[strict 2-category]] $C$ -- hence a category [[enriched category|enriched over]] [[Cat]] -- whose underlying [[category]] $C_1$ is equipped with the structure of a [[model category]] which is compatible, in some sense, with the [[folk model structure]] on the enrichment category [[Cat]].

The compatibility is such that in particular the notion of [[homotopy limit]] and of [[strict 2-limit|pseudo-limit]] coincide in such model 2-category.

To state the definition of a strict model 2-category, we need the following notation:

##Notation##

For $C$ a [[enriched category|category enriched over]] [[Cat]] and for
$$
  u : X \to Y
$$
$$
  v : V \to W
$$
two morphisms in $C$, let 

$$
  [u,v] : C(Y,V) \to C(Y,W) \times_{C(X,W)} C(X,V)
$$
be the unique morphism induced from the commutativity of the diagram
$$
  \array{
    C(Y,V) &\stackrel{C(u,V)}{\to}& C(X,V)
    \\
    \downarrow^{C(Y,v)} && \downarrow^{C(X,v)}
    \\
    C(Y,W) &\stackrel{C(u,W)}{\to}& C(X,W)
  }
  \,.
$$

#Definition#

The structure of a **model 2-category** on a [[strict 2-category]] $C$ with finite limits and colimits is

* a [[model category]] structure on the underlying 1-category $C_1$;

* such that

  * if $u : X \to Y$ is a cofibration and $v : V \to W$ is a fibration in $C_1$ then the functor $[u,v]$ defined above is an [[isofibration]] in [[Cat]];

  * and $[u,v]$ is a weak equivalence (in the [[folk model structure]] on [[Cat]], i.e. a categorical [[equivalence]]) if either of $u$ or $v$ is.


#Remarks#

* In a strict model 2-category the notion of 2-categorical [[strict 2-limit|pseudo-limit]] and that of  [[model category|model theoretic]] [[homotopy limit]] coincide. 

#References#

The definition of (strict) model 2-category is on [p. 3](http://www.lacim.uqam.ca/~gambino/homotopy.pdf#page=3) of

* Nicola Gambino, _Homotopy limits for 2-categories_ ([pdf](http://www.lacim.uqam.ca/~gambino/homotopy.pdf)).

The relaton between pseudo-limits and homotopy limits is dicussed in [section 6](http://www.lacim.uqam.ca/~gambino/homotopy.pdf#page=3)
