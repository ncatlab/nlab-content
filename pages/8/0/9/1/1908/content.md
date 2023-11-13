
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
 {#Idea}

In [[category theory]], by "decategorification" one means (see [below](#Definition)) the process which turns a [[category]] into a [[set]], namely into its set of [[isomorphism classes]]. 

Typically one is interested in the case where the category is equipped with extra [[higher structure|higher]] [[structure]] (see [further below](#ExtraStructure)), whence its set of isomorphism classes will carry the corresponding ordinary [[structure]]. For example: the decategorification of a [[monoidal category]] is canonically a [[monoid]], the decategorification of a [[rig category]] is canonically a [[rig]], the decategorification of a [[2-group]] is canonically a plain [[group]], etc. 

(Combined with [[group completion]], decategorification of [[monoidal categories]] is often known as a form of [[K-theory]] in degree 0, see for instance at *[[K-theory of a permutative category]]*.)

In this sense decategorification is a "[[left inverse]]" to ([[vertical categorification|vertical]]) "[[categorification]]" (see there for more), namely to the process of asking for [[category theory|category theoretic]] [[higher structures]] analogous to given  [[set theory|set theoretic]] [[structures]]. 

Crucially, though, decategorification is a systematic process (in fact a [[2-functor]], see [below](#Definition)) while [[categorification]], being a (local) [[section]] of this functor involves making choices: There are in general several categorical structures which have the same decategorification. For instance, the [[rig category|rig]] [[monoidal categories]] [[FinSet]] (with its [[cartesian product]]) and [[FinDimVect]] (with its [[tensor product of vector spaces]]) both decategorify to the [[rig]] [[monoid]] of [[natural numbers]] (see further examples [below](#Examples)).

More generally, in [[higher category theory]] there are higher sequences of "higher decategorification" functors which incrementally discard non-invertible [[higher morphisms]] and [[quotient]] by remaining invertible [[higher morphisms]] up to some degree (see [below](#DefinitionForHigherCategories)).

In particular, in the [[homotopy theory]] of [[groupoids]], [[higher groupoids]] and [[infinity-groupoid|$\infty$-groupoids]], namely in [[(infinity,0)-category|$(\infty,0)$-category]]-theory, decategorification is nothing but [[truncated object in an (infinity,1)-category|truncation]] and the tower of decategorifications/[[n-truncation|$n$-truncations]] is known as the *[[Postnikov tower]]*.


## Definitions
 {#Definition}

### For categories
 {#DefinitionForCategories}

Given an ([[essentially small category|essentially]] [[small category|small]]) [[category]] $\mathcal{C}$, its decategorification is the [[set]] $K(C)$ of [[isomorphism classes]] of [[objects]] of $\mathcal{C}$.

This construction extends to a [[2-functor]]

\[
  \label{PlainDecategorification}
  \begin{array}{rcl}
  \mathllap{K \;\colon\; }
   Cat &\longrightarrow& Set
   \\
   \mathcal{C} &\mapsto& Obj(\mathcal{C})_{/iso}
  \end{array}
\]

from the ([[2-category|2-]])[[category]]  [[Cat]] of ([[essentially small categories|essentially]] [[small category|small]]) [[categories]] to the category (or [[locally discrete 2-category]]) [[Set]] of [[sets]]. 

Notice that we may think of [[sets]] as [[0-categories]], so that (eq:PlainDecategorification) may equivalently be thought of as being of the form

$$
  K \colon 1Cat \longrightarrow 0Cat
  \,,
$$

which makes manifest that and how decategorification indeed *decreases categorical degree*.

For generalization of decategorification to [[higher category theory]] ([below](#DefinitionForHigherCategories)) it is useful to make explicit that the decategorification 2-functor (eq:PlainDecategorification) factors as 

\[
  \label{PlainDecategorificationFactoredThroughCore}
  K 
  \,\colon\,
  Cat
    \overset{Core}{\longrightarrow}
  Grpd
    \overset{\tau_0}{\longrightarrow}
  Set
  \,,
\]

where

1. $Core$ assigns the "[[core]]" of a category, namely the maximal [[groupoid]] inside it, hence $Core$ "discards" all non-invertible morphisms;

2. $\tau_0$ is the [[0-truncation]] functor which turns a [[1-groupoid]] into its [[0-groupoid]] of [[connected components]].

It may be interesting to notice here that:

* [[core|Core]] is *[[right adjoint]]* to the [[fully faithful 2-functor|embedding]] $Grpd \hookrightarrow Cat$, hence is a [[coreflective subcategory|co-reflection]],

* [[0-truncation|$\tau_0$]] is *[[left adjoint]]* to the [[fully faithful functor|embedding]] $Set \hookrightarrow Grpd$, hence is a [[reflective subcategory|reflection]].


### For higher categories
 {#DefinitionForHigherCategories}

For any sensible notion of [[higher categories]] one will have corresponding analogs of the [[core]]- and the [[truncation]]-operations used in (eq:PlainDecategorificationFactoredThroughCore), which allows to define decategorification of higher categories.

For example, for [[2-categories]] there are the evident notions of *[[core in a 2-category]]*.

More generally, for any of the models of [[(infinity,n)-categories|$(\infty,n)$-categories]] we have a [[coreflection]]

$$
  (\infty,n) Cat
    \underoverset
      {\underset{Core_n}{\longleftarrow}}
      {\hookrightarrow}
      {\;\; \bot \;\;}
  (\infty,n+1)Cat
$$

which together with the [[truncated object in an (infinity,1)-category|$m$-truncation]]-operation to [[homotopy n-types|homotopy $m$-types]] yields towers of higher decategorification functors

$$
  (\infty,n+1)Cat
  \overset{Core_n}{\longrightarrow}
  (\infty,n)Cat  
  \to 
  \cdots
  \to
  (\infty,0)Cat  
  \;\simeq\;
  \infty Grpd
  \overset{ \tau_m }{\longrightarrow}
  m Grpd
  \to 
  \cdots 
  \to
  0 Grpd 
  \;\simeq\; 
  Set
  \,,
$$

any stage of which may reasonably be addressed as an intermediate stage of higher decategorification.



## Extra structure
 {#ExtraStructure}

If the category in question has [[extra structure|extra]] [[higher structure|higher]] [[structure]], then this is usually inherited in some decategorified form by its decategorification. For instance if $C$ is a [[monoidal category]] then $K(C)$ is a [[monoid]].

A famous example are [[fusion category|fusion categories]] whose decategorifications are called _[[Verlinde ring]]s_.

There may also be extra structure induced more directly on $K(C)$. For instance the [[K-theory|K-group]] of an [[abelian category]] is the decategorification of its category of bounded [[chain complexes]] and this inherits a group structure from the fact that this is a [[triangulated category]] (a [[stable (∞,1)-category]]) in which there is a notion of [[fibration sequence|homotopy exact sequences]].

## Examples
 {#Examples}

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





