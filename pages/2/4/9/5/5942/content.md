
> This article is about [[homomorphisms]] between [[schemes]] which are locally of finite type. For the notion of locally finite type in [[dependent type theory]], see [[locally finite type]]. 

---

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[algebraic geometry]], a [[morphism]] between [[schemes]] is said to be _of finite type_ if it behaves like a [[map]] with [[finite number|finite]] [[dimension|dimensional]] [[fibers]], and is said to be _locally of finite type_ if each of its fibers can built by gluing together a (potentially very large) family of finite dimensional pieces.

## For schemes

A morphism $f \colon X \to Y$ of [[schemes]] is **locally of finite type** if

* for every [[open cover]] $\{U_i \to Y\}$ by [[affine schemes]], $U_i \simeq Spec B_i$;

* and every open cover $\{U_{i j_i} \to X\}$ by affine schemes $U_{i j_i} = Spec A_{i j_i}$, fitting into a [[commuting diagram]] (this always exists, cf. *[[coverage]]*)

  $$
    \array{
      U_{i j_i} &\to& U_i
      \\
      \downarrow && \downarrow
      \\
      X &\stackrel{f}{\to}& Y
    }
  $$

  for all $i,j$, 

we have that the [[homomorphism]] of [[associative algebras|algebras]] $B_i \longrightarrow A_{i j}$ [[duality between algebra and geometry|formally dual]] to $U_{i j} \to U_i$ exhibits $A_{i j}$ as a [[finitely generated algebra]] over $B_i$.

If for fixed $i$ the $j_i$ range only over a [[finite set]], then the morphism is said to be of **finite type**.

## Related concepts

* [[morphism of finite presentation]]

## References

Introductory disucssoon over the [[complex numbers]] (with an eye towards [[GAGA]]):

* {#Neeman07} [[Amnon Neeman]], section 3.10 of: _Algebraic and analytic geometry_, London Math. Soc. Lec. Note Series __345__, Cambridge University Press (2007) &lbrack;[ISBN:9780521709835](http://www.cambridge.org/us/academic/subjects/mathematics/geometry-and-topology/algebraic-and-analytic-geometry)&rbrack;


[[!redirects locally of finite type]]

[[!redirects morphisms of finite type]]

[[!redirects morphism locally of finite type]]
[[!redirects morphisms locally of finite type]]

[[!redirects finite type morphism]]
[[!redirects finite type morphisms]]

[[!redirects scheme of finite type]]
[[!redirects schemes of finite type]]
