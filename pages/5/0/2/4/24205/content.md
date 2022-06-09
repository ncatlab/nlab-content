
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##
Let $G$ be an [[abelian group]], and $n$ a [[natural number]]. The [[Eilenberg-MacLane space]] $K(G,n)$ is the unique space that has $\pi_n(K(G,n))\cong G$ and its other [[homotopy groups]] trivial. These spaces are a basic tool in classical algebraic topology, they can be used to define [[cohomology]]. 

There is an analogous construction in [[homotopy type theory]]. 

## Definition ##
Let $G$ be a group. The **Eilenberg-MacLane space type** $K(G,1)$ is the [[higher inductive type|higher inductive 1-type]] with the following constructors:

 * $base : K(G,1)$
 * $loop : G \to (base = base)$
 * $id   : loop(e) = refl_{base}$
 * $comp : \prod_{(x,y:G)} loop(x \cdot y) = loop(y) \circ loop(x)$

$base$ is a point of $K(G,1)$, $loop$ is a function that constructs a [[path]] from $base$ to $base$ for each element of $G$. $id$ says the path constructed from the identity element is the [[identity type|trivial loop]]. Finally, $comp$ says that the path constructed from group multiplication of elements is the concatenation of paths.

It should be noted that this type is 1-[[truncated]] which could be added as another constructor:

 * $\displaystyle \prod_{x,y:K(G,1)} \prod_{p,q:x=y} \prod_{r,s:p=q} r = s$

### Recursion principle ###

To define a function $f : K(G,1) \to C$ for some type $C$, it suffices to give

 * a point $c : C$
 * a family of loops $l : G \to (c = c)$
 * a path $l(e)=id$
 * a path $l(x \cdot y) = l(y) \circ l(x)$
 * a proof that $C$ is a 1-type.

Then $f$ satisfies the equations

$$f(base) \equiv c$$
$$ap_{f} (loop(x))=l(x)$$

It should be noted that the above can be compressed, to specify a function $f : K(G,1) \to C$, it suffices to give:

 * a proof that $C$ is a 1-type
 * a point $c : C$
 * a group homomorphism from $G$ to $\Omega(C,c)$

## See also

* [[higher inductive type]]

* [[Eilenberg-MacLane space]]

* [[cohomology in homotopy type theory]]

## References

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* {#LicataFinster14} [[Dan Licata]], [[Eric Finster]], _Eilenberg-MacLane spaces in homotopy type theory_, LICS 2014 ([pdf text](http://dlicata.web.wesleyan.edu/pubs/lf14em/lf14em.pdf), [Agda HoTT code](https://github.com/dlicata335/hott-agda/blob/master/homotopy/KGn.agda), [web discussion](http://homotopytypetheory.org/2014/04/15/eilenberg-maclane-spaces-in-hott/))