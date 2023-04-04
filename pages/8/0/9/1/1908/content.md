
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Decategorification is the reverse of [[vertical categorification]] and turns an $n$-[[n-category|category]] into an $(n-1)$-category.  

It corresponds in [[homotopy theory]] to [[truncated|truncation]].


## Definitions

Given a ([[small category|small]] or [[essentially small category|essentially small]]) [[category]] $C$, the [[set]] of __[[isomorphism classes]]__ $K(C)$ of objects of $C$ is called the **decategorification** of $C$.

This is a [[functor]]

$$
  K : Cat \to Set
$$

from the category (or even $2$-[[2-category|category]]) [[Cat]] of (small) categories to the category (or [[locally discrete 2-category]]) [[Set]] of sets. Notice that we may think of a [[set]] as [[0-category]], so that this can be thought of as

$$
  K : 1Cat \to 0Cat
  \,.
$$


Decategorification decreases categorical degree by forming equivalence classes. Accordingly for all $n \gt m $ and all suitable notions of [[higher category theory|higher categories]] one can consider decategorifications

$$
  n Cat \to m Cat
  \,.
$$

For instance forming the [[homotopy category of an (∞,1)-category]] means decategorifying as

$$
  (\infty,1)Cat \to 1 Cat
  \,.
$$

Therefore one way to think of [[vertical categorification]] is as a [[right inverse]] to decategorification.

## Decategorification of a 2-category ##

A precise way to define the decategorification of a 2-category in the above sense is to identify all 1-arrows which are 2-isomorphic (note that this defines an equivalence relation on 1-arrows and respects composition), and to discard the 2-arrows.


## Extra structure ##

If the category in question has extra structure, then this is usually inherited in some decategorified form by its decategorification. For instance if $C$ is a [[monoidal category]] then $K(C)$ is a [[monoid]].

A famous example are [[fusion category|fusion categories]] whose decategorifications are called _[[Verlinde ring]]s_.

There may also be extra structure induced more directly on $K(C)$. For instance the [[K-theory|K-group]] of an [[abelian category]] is the decategorification of its category of bounded [[chain complexes]] and this inherits a group structure from the fact that this is a [[triangulated category]] (a [[stable (∞,1)-category]]) in which there is a notion of [[fibration sequence|homotopy exact sequences]].

## Examples

* The decategorifications of [[finite sets]] and [[finite dimensional vector spaces]] (over any [[ground field]]) are [[natural numbers]]

  $$
    FinSet_{/\sim} \simeq \mathbb{N}
  $$
 
  $$
    FinDimVect_{/\sim} \simeq \mathbb{N}
  $$

  For instance the [[rank-nullity theorem]] is the decategorification of the [[splitting lemma]] in the category [[FinDimVect]].

* The decategorification of the 2-category [[Grpd]] of (small) [[groupoids]] is equivalent to the [[homotopy category]] of [[homotopy 1-types]].

* The decategorification in the same sense of the 2-category of ([[small category|small]]) [[categories]] is equivalent to the full [[homotopy category of topological spaces|homotopy category]]. (explain...)






## Parable ##
From John Baez, https://math.ucr.edu/home/baez/week121.html

 If one studies categorification one soon discovers an amazing fact: many deep-sounding results in mathematics are just categorifications of facts we learned in high school! There is a good reason for this. All along, we have been unwittingly "decategorifying" mathematics by pretending that categories are just sets. We "decategorify" a category by forgetting about the morphisms and pretending that isomorphic objects are equal. We are left with a mere set: the set of isomorphism classes of objects.

To understand this, the following parable may be useful. Long ago, when shepherds wanted to see if two herds of sheep were isomorphic, they would look for an explicit isomorphism. In other words, they would line up both herds and try to match each sheep in one herd with a sheep in the other. But one day, along came a shepherd who invented decategorification. She realized one could take each herd and "count" it, setting up an isomorphism between it and some set of "numbers", which were nonsense words like "one, two, three,..." specially designed for this purpose. By comparing the resulting numbers, she could show that two herds were isomorphic without explicitly establishing an isomorphism! In short, by decategorifying the category of finite sets, the set of natural numbers was invented.

According to this parable, decategorification started out as a stroke of mathematical genius. Only later did it become a matter of dumb habit, which we are now struggling to overcome by means of categorification. While the historical reality is far more complicated, categorification really has led to tremendous progress in mathematics during the 20th century. For example, Noether revolutionized algebraic topology by emphasizing the importance of homology groups. Previous work had focused on Betti numbers, which are just the dimensions of the rational homology groups. As with taking the cardinality of a set, taking the dimension of a vector space is a process of decategorification, since two vector spaces are isomorphic if and only if they have the same dimension. Noether noted that if we work with homology groups rather than Betti numbers, we can solve more problems, because we obtain invariants not only of spaces, but also of maps. 

[[!redirects decategorifications]]

[[!redirects decategorification]]
[[!redirects decategorified]]
[[!redirects decategorifies]]
[[!redirects decategorify]]
[[!redirects decategorifying]]

[[!redirects de-categorification]]
[[!redirects de-categorifications]]

[[!redirects de-categorified]]
[[!redirects de-categorifies]]
[[!redirects de-categorify]]
[[!redirects de-categorifying]]





