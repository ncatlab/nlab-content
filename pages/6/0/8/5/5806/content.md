
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _$(\infty,n)$-category of spans_ in [[∞-groupoid]] is an [[(∞,n)-category]] whose

* [[object]]s are [[∞-groupoid]]s;

* [[morphism]]s $X \to Y$ are [[span]]s 

  $$
    \array{
      && Z
      \\
      & \swarrow && \searrow
      \\
      X &&&& Y
    }
  $$

  in [[∞Grpd]]

* [[2-morphism]]s are spans of spans

  $$
    \array{
      && Z
      \\
      & \swarrow &\uparrow& \searrow
      \\
      X &&Q&& Y
      \\
      & \nwarrow &\downarrow& \nearrow
      \\
      && Z'
    }
  $$

  (where the trianglura sub-[[diagram]]s are filled with [[2-morphism]]s in [[∞Grpd]] which we do not display here)

* and so on up to [[k-morphism|n-morphism]]s

* $k \gt n$-morphisms are equivalences of order $(k-n)$ of higher spans.

Using the symmetric monoidal structure on [[∞Grpd]] this becomes a [[symmetric monoidal (∞,n)-category]].

More generally, for $C$ some [[symmetric monoidal (∞,n)-category]], there is a symmetric monoidal $(\infty,n)$-category of spans over $C$, whose

* [[object]]s are [[∞-groupoid]]s $X$ equipped with an [[(∞,n)-functor]] $X \to C$;

* [[morphism]]s $X \to Y$ are [[span]]s in [[(∞,1)Cat]] over $C$

  $$
    \array{
      && Z
      \\
      & \swarrow && \searrow
      \\
      X &&\swArrow&& Y
      \\
      & \searrow && \swarrow
      \\
      && C
    }
  $$

* and so on.

Even more generally one can allow the [[∞-groupoid]]s $X, Y, \cdots$ to be [[(∞,n)-categories]] themselves.

## References

For references on 1- and 2-categories of spans see [[span]].

An inductive definition of the [[symmetric monoidal (∞,n)-category]] $Span_n(\infty Grpd)/C$ of spans of [[∞-groupoid]] over a symmetric monoidal $(\infty,n)$-category $C$ is in section 3.2 of 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

there denoted $Fam_n(C)$. The generalization to an $(\infty,n)$-category $Span_n((\infty,1)Cat^Adj)$ of spans between [[cobordism hypothesis|(∞,n)-categories with duals]] is discussed on p. 107 and 108.

The application of $Span_n(\infty Grpd)/C$ to the construction of [[FQFT]]s is further discussed in section 3 of 

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], [[Topological Quantum Field Theories from Compact Lie Groups]]

A discussion of a version $Span(B)$for $B$ a [[2-category]] with $Span(B)$ regarded as a [[tricategory]] and then as a 1-object [[tetracategory]] is in

* [[Alex Hoffnung]], _Spans in 2-categories_ ([pdf](http://mysite.science.uottawa.ca/hoffnung/papers_files/spans.pdf)) 


[[!redirects (∞,n)-category of spans]]
[[!redirects (∞,n)-categories of spans]]

[[!redirects (infinity,n)-categories of spans]]
