
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A [[model category]] structure on the [[category]] [[Operad]] of [[Set]]-enriched coloured [[symmetric operads]] which generalizes the [[canonical model structure]] on [[Cat]].

## Definition

+-- {: .num_defn}
###### Definition

Call a [[morphism]] of [[operads]] $f : P \to Q$  a **[[weak equivalence]]**  if 

1. its underlying [[functor]] of [[categories]] is an [[essentially surjective functor]];

1. for every collection $(c_1, \cdots, c_n; c)$ of colours it induces an [[isomorphism]]

   $$
     P(c_1, \cdots, c_n; c) \to Q(f(c_1), \cdots, f(c_n); f(c))
   $$

   (the operadic analog of being [[full and faithful functor|full and faithful]]).

Call a morphism $f : P \to Q$ a **fibration** if for every [[isomorphism]] in $Q$ and a lift of its source object to $P$ there is an isomorphism in $P$ covering it under $f$.

Call a morphism a **cofibration** if it is an injection on objects (on colours)

=--

+-- {: .num_theorem}
###### Theorem

This defines a [[cofibrantly generated model category]] structure on [[Operad]].

=--

This is due to ([Weiss 07](#Weiss)).


## Related concepts

* [[canonical model structure on Cat]]

* [[model structure on operads]]

* [[model structure on dendroidal sets]]


## References

* [[Ittay Weiss]], _Dendroidal sets_, PhD thesis ([web](http://igitur-archive.library.uu.nl/dissertations/2007-0918-200833/UUindex.html))
 {#Weiss}

[[!redirects canonical model structure on operads]]
