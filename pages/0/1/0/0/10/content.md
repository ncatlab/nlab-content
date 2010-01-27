
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

For a given [[geometric theory]] $T$, a **classifying [[topos]]** for $T$ is a [[Grothendieck topos]] $S[T]$ equipped with a "universal model $U$ of $T$".  This means that for any Grothendieck topos $E$ together with a model $X$ of $T$ in $E$, there exists a unique (up to isomorphism) [[geometric morphism]] $f: E \to S[T]$ such that $f^*$ maps the $T$-model $U$ to the model $X$.  More precisely, for any Grothendieck topos $E$, the category of $T$-models in $E$ is equivalent to the category of geometric morphisms $E \to S[T]$.

If $C_T$ is the [[syntactic category]] of $T$, so that $T$-models are the same as [[geometric category|geometric functors]] out of $C_T$, then this universal model can be identified with a certain geometric functor
$$
  U : C_T \to S[T]
  \,.
$$
Its universality property means that any geometric functor
$$
  X : C_T \to E
$$
factors essentially uniquely as
$$
  X : C_T \stackrel{U}{\to} S[T] \stackrel{f^*}{\to} E
$$
for $U$ the universal model and $f^*$ the [[left adjoint]] part of a [[geometric morphism]].  More precisely, composition with $U$ defines an equivalence between the category of geometric morphisms $E\to S[T]$ and the category of geometric functors $C_T\to E$.

Classifying toposes can also be defined over any base topos $S$ instead of [[Set]].  In that case "Grothendieck topos" is replaced by "bounded $S$-topos."

## Properties

Any [[Grothendieck topos]] can be thought of as a 'classifying topos'. A useful discussion of this idea starts
[here](http://golem.ph.utexas.edu/category/2007/10/geometric_representation_theor_2.html#c012724).


## Background on the theory of theories


The notion of _classifying topos_ is part of a trend, begun by [[Bill Lawvere|Lawvere]], of viewing a mathematical [[theory]] as a category with suitable exactness properties and which contains a "generic model", and a model of the theory as a functor which preserves those properties. The original example is that of finitary [[algebraic theory]], which was reformulated in terms of categories with finite products (see [[Lawvere theory]]). 

* **algebraic theory** Roughly speaking, an algebraic theory is any theory which can be formulated in the language of categories with finite [[product]]s. An example would be the theory of groups. As explained in the entry for [[Lawvere theory]], each algebraic theory has a Lawvere theory which is a "classifying category" for that theory, in that models for the theory correspond precisely to product-preserving functors coming out of the Lawvere theory.

* **essentially algebraic theory** Next up the line is the notion of (finitary) [[essentially algebraic theory]]. This is any theory which can be formulated in the language of [[finitely complete category|categories with finite limits]]. An example would be the theory of categories. Again, every essentially algebraic theory admits a classifying category: a [[finitely complete category]] with a "generic model", such that models of the theory correspond to left exact functors coming out of that category. 

* **geometric theory** Further up the line (and speaking roughly), a [[geometric theory]] is a theory which can be formulated in that fragment of first-order logic that deals in finite limits and arbitrary (small) colimits. Certain exactness properties which come into play here, but there are two basic ideas to keep in mind. One is that a geometric theory has a classifying category: a category having those exactness properties (viz., a Grothendieck topos) and possessing a "generic object" for that theory. The other is that a geometric morphism $ f_*: E \to S[T] $ is tantamount to a left exact left adjoint $ f^*: S[T] \to E $, which preserves such finite limits and small colimits ($ f_* $ is the right adjoint of $ f^* $). The left exact left adjoint would thus be a model of that theory, much as models of an essentially algebraic theory are left exact functors out of the classifying category for that theory. 

## Examples 

### The classifying topos for groups. 

As a warm-up, we first discuss the classifying category for the theory of groups $T$ _qua_ essentially algebraic theory, i.e., we give a finitely complete category $Lex[T]$ equipped with a "generic group". This works much the same way as the [[Lawvere theory]] for groups, which is the category opposite to the category of finitely generated free groups, except that we have to "close up" the Lawvere theory under all finite limits. 

Thus, we take $Lex[T]$ to be the category opposite to the category of _finitely presented groups_: those groups $G$ which arise as coequalizers of diagrams 

$$F(m) \rightrightarrows F(n)$$ 

between finitely generated free groups. It may be shown that $Lex[T]$ is finitely complete, and the "generic group" inside $Lex[T]$ is $F(1)$, the free group on one generator, just as it is for the [[Lawvere theory]] (see the discussion at that entry). 


### Classifying toposes for cover-preserving flat functors on a site


Any small [[site]] of definition for a
[[Grothendieck topos]] $E$ can be considered as a 
[[geometric theory]]: the theory of a
cover-preserving flat functors on that site. 

The classifying topos of this theory is
$E$.  

Moreover, for any object $X$ of $E$, there is a small site of definition
for $E$ which includes $X$, and thus for which $X$ is (part of) the universal object.  

> [[Urs Schreiber|Urs]]: check if the following paragraph is correct

The [[vertical categorification]] of this to the context of [[(∞,1)-category]] theory is the notion of [[structured (∞,1)-topos]] and of [[geometry (for structured (∞,1)-toposes)]]:

The geometry $\mathcal{G}$ is the [[(∞,1)-category]] that plays role of the syntactic theory. For $\mathcal{X}$ an [[(∞,1)-topos]], a model of this theory is a limits and covering-preserving [[(∞,1)-functor]]

$$
  \mathcal{G} \to \mathcal{X}
  \,.
$$

The [[Yoneda embedding]] followed by [[∞-stackification]] 


$$
  \mathcal{G} \stackrel{Y}{\to} PSh_{(\infty,1)}(\mathcal{G})
  \stackrel{\bar(-)}{\to} Sh_{(\infty,1)}(\mathcal{G})
$$

constitutes a model of $\mathcal{G}$ in the (Cech) [[∞-stack]] [[(∞,1)-topos]] $Sh_{(\infty,1)}(\mathcal{G})$ and exhibits it as the classifying topos for such models (geometries):

This is _[[Structured Spaces]]_ [prop 1.4.2](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.0459v1.pdf#page=26).

### The classifying topos for intervals. 

...

### The classifying topos for local rings

The classifying topos for [[local ring|local rings]] is ... 


[[!redirects Another page]]