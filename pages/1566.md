
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### In Sets

A _commutative monoid_ is a [[monoid]] where the multiplication satisfies the commutative law:
$$x y = y x.$$

Alternatively, just as a [[monoid]] can be seen as a [[category]] with one object, a commutative monoid can be seen as a [[bicategory]] with one object and one morphism (or equivalently, a [[monoidal category]] with one object).

Commutative monoids with [[homomorphisms]] between them form a _[[category of commutative monoids]]_.

Every commutative monoid has the canonical structure of a [[module]] over the commutative [[rig]] $\mathbb{N}$. That is, [[CMon]] = $\mathbb{N}$-[[Mod]].

### In any symmetric monoidal category


More generally, the concept makes sense [[internalization|internal]] to any [[symmetric monoidal category]]. See at _[[commutative monoid in a symmetric monoidal category]]_ for details.


## Examples

* An [[abelian group]] is a commutative monoid that is also a [[group]].

* The [[natural numbers]] (together with 0) form a commutative monoid under addition.

* Every bounded [[semilattice]] is an _idempotent_ commutative monoid, and every idempotent commutative monoid yields a semilattice, (see that entry).

Examples of [[commutative monoids in a symmetric monoidal category]]:

1. A commutative monoid in the [[symmetric monoidal category|symmetric monoidal]] [[category of vector spaces]] is a [[commutative algebra]];

1. A commutative monoid in the [[symmetric monoidal category|symmetric monoidal]] [[category of chain complexes]] of vector spaces is a [[differential graded-commutative algebra]];

1. A commutative monoid in the [[symmetric monoidal category|symmetric monoidal]] [[category of chain complexes of super vector spaces]] is a [[differential graded-commutative superalgebra]].

## Results on commutative monoids in Set


1. If a commutative monoid is finitely generated it is finitely presented.

2. Finitely generated commutative monoids have decidable word problems, the isomorphism problem for them is decidable, and indeed the first-order theory of finitely generated commutative monoids is decidable (see [KharlampovichSapir](#KharlampovichSapir)).

3. If a finitely generated commutative monoid is **cancellative** ($a + b = a' + b \Rightarrow a = a'$) then it embeds in a finitely generated abelian group.  

4.  If a finitely generated commutative monoid is cancellative and **torsion-free** ($a + a + \cdots + a = 0 \Rightarrow a = 0$) then it embeds in a finitely generated free abelian group (or more concretely, $\mathbb{Z}^n$).   Conversely any submonoid of $\mathbb{Z}^n$ is cancellative and torsion-free (but not necessarily finitely generated).  A commutative monoid is called an **affine monoid** if it is isomorphic to a finitely generated submonoid of $\mathbb{Z}^n$, and there is an extensive theory of these, connected to [[toric variety|toric varieties]] (see [BrunsGubeladze](#BrunsGubeladze)).

5.  If a finitely generated commutative monoid is cancellative and **nonnegative** ($a + b = 0 \Rightarrow a,b = 0$), it embeds in a finitely generated free commutative monoid, or more concretely, $\mathbb{N}^n$ 
(Thm. 3.11, [RosalesGarcía-Sánchez](#RosalesGarcía-Sánchez).   Conversely, any finitely generated submonoid of $\mathbb{N}^n$ is cancellative and nonnegative (but not necessarily finitely generated). 


## Related concepts

* [[commutative magma]]

* [[CMon]]

* [[group completion]]

* [[category of monoids]]

* [[cocommutative comonoid]]

* [[symmetric monoidal category]]

* [[model structure on commutative monoids in a symmetric monoidal model category]]

* [[commutative ∞-monoid]]

* [[E-infinity algebra]]

* [[periodic table]]

[[!redirects abelian monoids]]
[[!redirects commutative monoid]]
[[!redirects commutative monoids]]

[[!redirects abelian monoid]]

[[!redirects commutative monoid object]]
[[!redirects commutative monoid objects]]

## References

The word problem for commutative monoids is discussed here:

* {#KharlampovichSapir} Olga G. Kharlampovich and Mark V. Sapir. Algorithmic problems in varieties, International Journal of Algebra and Computation 5.04n05 (1995), 379-602.   ([pdf](http://www.math.vanderbilt.edu/~msapir/ftp/pub/survey/survey.pdf))

For affine monoids and other finitely generated commutative monoids see:

* {#BrunsGubeladze} Winfried Bruns and Joseph Gubeladze, *Polytopes, Rings, and K-theory*, Springer, Berlin, 2009.   ([pdf of preliminary incomplete version](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.126.2385&rep=rep1&type=pdf))

* {#RosalesGarcía-Sánchez} José Carlos Rosales and Pedro A. García-Sánchez, *Finitely Generated Commutative Monoids*, Nova Publishers, 1999. 
