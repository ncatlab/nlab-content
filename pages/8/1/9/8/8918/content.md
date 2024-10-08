
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[T-duality]] and in particular of [[differential T-duality]] one considers (as discussed there) [[fiber products]] of [[pairs]] of [[torus]]-[[fiber bundles]] equipped with a [[circle 2-bundle]] ([[circle n-bundle with connection|with connection]]). 

In some disguise, this has been called _$B_n$-geometry_ ([Baraglia](#Baraglia)). The T-duality interpretation is made explicit in [Bouwknegt](Bouwknegt)

Here "$B_n$" refers to the [[special orthogonal group]] of the form $SO(n+1,n)$, which appears as the structure group of a [[generalized tangent bundle]] tensored with a [[line bundle]] (the [[Poincare line bundle]] of the T-duality correspondence).

## Properties

### Interpretation in higher differential geometry

We give the interpretation of $B_n$-geometry in [[smooth infinity-groupoid|higher differential geometry]].

For $c_{conn},c'_{conn} \colon X \to \mathbf{B}U(1)$ modulating two circle principal bundles with conection, a [[differential T-duality]] structure is a choice of trivialization of their [[cup product]] class. From this we get the [[pasting diagram]] of [[homotopy pullbacks]] of smooth $\infty$-stacks

$$
  \array{
    P \times_X \hat P&\stackrel{\tau}{\to}& \mathbf{B}^2 U(1) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X 
     &\to& 
    fib(\cup) 
     &\to& 
    (\mathbf{B}U(1)) \times (\mathbf{B}U(1))
    \\
    &\searrow & \downarrow && \downarrow^{\mathrlap{\cup}}
    \\
    && * &\to& \mathbf{B}^3 U(1)
  }
  \,.
$$

Here $\tau$ is the morphism that modulates the circle 2-bundle on the fiber product of the two circle bundles.

(...)

## Related concepts

* [[differential T-duality]]

* [[generalized complex geometry]]

* [[exceptional generalized geometry]]

## References

The term $B_n$-geometry was introduced in

* {#Baraglia} [[David Baraglia]], _Leibniz algebroids, twistings and exceptional generalized geometry_ ([arXiv:1101.0856](http://arxiv.org/abs/1101.0856))

A review is in

* {#Hitchin} [[Nigel Hitchin]], talks at StringMath2012 &lbrack;[pdf](http://www.hcm.uni-bonn.de/fileadmin/stringmath2012/plenary_talks/03-Hitchin.pdf)&rbrack;
 

The relation to T-duality is made clear around slide 80 of:

* {#Bouwknegt} [[Peter Bouwknegt]], _Courant Algebroids and Generalizations of Geometry_, talk at StringMath2011 &lbrack;[pdf](http://www.math.upenn.edu/StringMath2011/notes/Bouwknegt_StringMath2011_talk.pdf)&rbrack;
 

A discussion of the [[infinity-Lie theory|higher Lie theoretic]] aspects is in 

* [[Ernesto Lupercio]], Camilo Rengifo, [[Bernardo Uribe]], _T-duality and exceptional generalized geometry through symmetries of dg-manifolds_ &lbrack;[arXiv:1208.6048](http://arxiv.org/abs/1208.6048)&rbrack;

[[!redirects geometry of type Bn]]
