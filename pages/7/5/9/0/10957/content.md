

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Traditionally in [[ontology]]/[[metaphysics]], a _category of being_ is, vaguely, a "kind or way of being" (e.g [WP](#Wikipedia)).

In ([Lawvere 91](#Lawvere91)) is a proposal for a formalization of this idea. Lawvere starts from the [[metaphysics]] as laid out in  ([Hegel 12](#Hegel12)) and first observes that the concept of [[unity of opposites]] which controls the discussion there is usefully formalized by the concept of [[adjoint modalities]]. In a way the simplest example of such is that given by the [[monad]] constant on the [[terminal object]]

$$
  (\emptyset \dashv \ast)
  \,.
$$

One observes that under the identification of Hegelian [[unity of opposites]] with [[adjoint modalities]], this adjoint pair serves well as a formalization of what ([Hegel 12](#Hegel12)) calls the moments of _Nichts_ ([[nothing]]) and _reines Sein_ (pure [[being]]).

Therefore any other [[adjoint modality]] of the form

$$
  \Box \dashv \bigcirc
$$

which necessarily includes the former (as an inclusion of [[modal types]])

$$
  \array{
     \emptyset &\subset& \Box
     \\
     \bot && \bot
     \\
     \ast &\subset& \bigcirc
  }
$$

formalizes a more "determinate" [[being]] ( _[[Dasein]]_ , _F&#252;rsichsein_ in the language of ([Hegel 12](#Hegel12))). See also at _[[Aufhebung]]_.


## Definition

Therefore, following  ([Lawvere 91, p. 7](#Lawvere91)):

+-- {: .num_defn}
###### Definition

A _category of being_ is a [[category]] with [[initial object]] and [[terminal object]] and equipped with an [[adjoint modality]] $\Box \dashv \bigcirc$, hence with an [[idempotent monad]] $\bigcirc$ on the category which has a [[left adjoint]] $\Box$.

=--

+-- {: .num_remark}
###### Remark

In [[geometry|geometric]] language these are categories equipped with a notion of [[discrete objects]] and [[codiscrete objects]].

=--

+-- {: .num_example}
###### Example


Examples include [[cohesive toposes]], and these are the examples considered in ([Lawvere 91](#Lawvere91)).

=--

## Related concepts

* [[category (philosophy)]]

## References

* Wikipedia, _[Category of being](http://en.wikipedia.org/wiki/Category_of_being)_
 {#Wikipedia}

* [[Georg Hegel]], _[[Science of Logic]]_ (1812)
 {#Hegel12}

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ (1991)
 {#Lawvere91}

[[!redirects categories of being]]