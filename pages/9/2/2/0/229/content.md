
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

An _abelian group_ (named after [[Niels Henrik Abel]]) is a [[group]] $A$ where the multiplication satisfies the commutative law: for all elements $x, y\in A$ we have

$$
  x y = y x
  \,.
$$

The [[category]] with abelian groups as [[object|objects]] and group homomorphisms as [[morphism|morphisms]] is called [[Ab]]. 

Every abelian group has the canonical structure of a [[module]] over the [[commutative ring]] $\mathbf{Z}$.  That is, [[Ab]] = $\mathbf{Z}$-[[Mod]].

### With subtraction and unit only

This definition of abelian group is based upon [[Toby Bartels]]'s definition of an [[associative quasigroup]]:

An **abelian group** is a [[pointed set]] $(A, 0)$ with a binary operation $(-)-(-):A \times A \to A$ called **subtraction** such that 

* for all $a \in A$, $a - a = 0$

* for all $a \in A$, $0 - (0 - a) = a$

* for all $a \in A$ and $b \in A$, $a - (0 - b) = b - (0 - a)$

* for all $a \in A$, $b \in A$, and $c \in A$, $a - (b - c) = (a - (0 - c)) - b$

For every element $a \in A$, the inverse element is defined as $-a \coloneqq 0 - a$ and addition is defined as $a + b \coloneqq a - (-b)$. 

Addition is commutative: 

$$a + b = a - (0 - b) = b - (0 - a) = b + a$$

and associative

$$(a + b) + c = (a - (0 - b)) - (0 - c)$$
$$(a + b) + c = (b - (0 - a)) - (0 - c)$$
$$(a + b) + c = b - ((0 - c) - a)$$
$$(a + b) + c = b - ((0 - c) - (0 - (0 - a)))$$
$$(a + b) + c = b - ((0 - a) - (0 - (0 - c)))$$
$$(a + b) + c = b - ((0 - a) - c)$$
$$(a + b) + c = (b - (0 - c)) - (0 - a)$$
$$(a + b) + c = a - (0 - (b - (0 - c)))$$
$$(a + b) + c = a + (b + c)$$

and has left identities

$$0 + a = 0 - (0 - a) = a$$

and right identities

$$a + 0 = 0 + a = a$$

and has left inverses

$$-a + a = (0 - a) - (0 - a) = 0$$

and right identities

$$a + (-a) = -a + a = 0$$

Thus, these axioms form an abelian group. 

## Properties

### In homotopy theory

From the [[nPOV]], just as a [[group]] $G$ may be thought of as a ([[pointed object|pointed]]) [[groupoid]] $\mathbf{B}G$ with a single object -- as discussed at [[delooping]] -- an abelian group $A$ may be understood as a (pointed) [[2-groupoid]] $\mathbf{B}^2 A$ with a single object and a single morphism: the delooping of the delooping of $A$.

$$
  \mathbf{B}^2 A
  =
  \left\{
    \array{
      & \nearrow \searrow^{\mathrlap{Id}}
      \\
      \bullet
      &\Downarrow^{a \in A}&
      \bullet
      \\
      & \searrow \nearrow_{\mathrlap{Id}}
    }
  \right\}
  \,.
$$ 

The [[exchange law]] for the composition of [[2-morphisms]] in a [[2-category]] forces the product on the $a \in A$ here to be commutative. This reasoning is known as the [[Eckmann-Hilton argument]] and is the same as the reasoning that finds that the second [[homotopy group]] of a space has to be abelian.

So the identitfication of abelian groups with one-object, one-morphism 2-groupoids may also be thought of as an identification with 2-[[truncated]] and 2-[[connected]] [[homotopy types]].

### Relation to other concepts

A [[monoid]] in [[Ab]] with its standard [[monoidal category]] structure, equivalently a ([[pointed object|pointed]]) [[Ab]]-[[enriched category]] with a single object, is a [[ring]].

## Generalizations

Generalizations of the notion of abelian group in [[higher category theory]] include 

* abelian [[group object in an (infinity,1)-category|group objects in an (∞,1)-category]]

* notably abelian [[simplicial groups]]

* and [[spectrum|spectra]].

An abelian group may also be seen as a [[discrete category|discrete]] [[compact closed category]].

## Related entries

* [[commutative magma]]

* [[commutative invertible semigroup]]

* [[tensor product of abelian groups]], [[direct sum of abelian groups]]

* [[free abelian group]], [[finite abelian group]]

* [[theory of abelian groups]]

* [[abelianization]]

* [[anabelian group]]

* [[module]], [[ring]]

* [[commutative ring]], [[commutative algebra]]

* [[super abelian group]], [[super module]]

* [[quadratic abelian group]]

* [[tensor ring]], [[Clifford ring]]

* [[Ab]]

* [[sheaf of abelian groups]]

* [[Ab-enriched category]], [[abelian category]]

* [[abelian ∞-group]]

  * [[symmetric 2-group]]

  * [[symmetric 3-group]]

* [[halving group]]

* [[symmetric midpoint group]]

## References

Textbook account:

* [[László Fuchs]], *Abelian Groups*, Springer (2015) &lbrack;[doi:10.1007/978-3-319-19422-6](https://doi.org/10.1007/978-3-319-19422-6)&rbrack;

    

Formalization of abelian groups in [[univalent foundations of mathematics]] ([[homotopy type theory]] with the [[univalence axiom]]): 

* [[Univalent Foundations Project]], Section 6.11 of: *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], Section 4.12 of: **[[Symmetry]]** (2021) 

[[!redirects abelian groups]]
[[!redirects Abelian group]]
[[!redirects Abelian groups]]