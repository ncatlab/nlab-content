
In a [[closed monoidal homotopical category]] with a notion of [[homotopy]] in terms of [[path object]]s, an _interval object_ $I$ should be an object which

* represents the [[cylinder functor]] (if any) in that for any object $B$ the tensor product $B \otimes I$ is indeed a cyclinder object

* co-represents the [[path object]] in that $[I,B]$ is indeed a path object of $B$.


#Discussion#

This discussion started at [[homotopy]], but it really deserves a place of its own where it can eventually materialize into a definition.

_[[Urs Schreiber|Urs]]:_ Let me chat a bit about what I am looking for here. It seems very useful to have a good notion of what it means in a context like a [[closed category|closed]] [[category of fibrant objects]] to say that _[[path object]]s are compatibly corepresented_.

By this should be meant: there exists an object $I$ such that

* for $B$ any other object, $[I,B]$ is a path object;

* and such that $I$ has some structure and property which makes it "nice".

In something I am thinking about the main point of $I$ being _nice_ is that it can model compositon: it must be possible to put two intervals end-to-end and get an interval of twice the length. In some private notes [[schreiber:Nonabelian homotopical cohomology and fiber bundles|here]] I suggest that:

a "category with interval object" should be

* a [[closed monoidal homotopical category]]

* with a compatible structure of a [[category of fibrant objects]]

* and equipped with an **internal co-categoy** on $\sigma, \tau : pt \to I$ for $I$ the _interval object_;

* such that $I$ co-represents path objects, in that for all objects $B$, $[I,B]$ is a path object for $B$.

I think there are a bunch of obvious examples: all familiar models of higher groupoids (Kan complexes, $\omega$-groupoids etc.) with the interval object being the obvious cellular interval $\{a \stackrel{\simeq}{\to} c\}$.

I also describe one class of applications which I think this is needed/useful for: recall how Kenneth Brown in section 4 of his article on [[category of fibrant objects]] (see theorems recalled there and reference given there) describes fiber bundles in the abstract homotopy theory of a _pointed_ category of fibrant objects. This is pretty restrictive. In order to describe things like $\infty$-vector bundles in an context of [[enriched homotopy theory]] one must drop this assumption of the ambient category being pointed. The structure of it being a category with an interval object is just the necessary extra structure to still allow to talk of (principal and associated) fiber bundles in abstract homotopy theory. It seems.

Comments are very welcome.