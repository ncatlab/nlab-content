
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_$Ab$_ denotes the [[category]] of [[abelian group|abelian groups]]: it has abelian groups as [[object|objects]] and [[group homomorphisms]] between these as [[morphism|morphisms]].

The archetypical example of an abelian group is the group $\mathbb{Z}$ of integers, and for many purposes it is useful to think of $Ab$ equivalently as the [[category of modules]] over $\mathbb{Z}$

$$
  Ab \simeq \mathbb{Z} Mod
 \,.
$$

The category $Ab$ serves as the basic [[enriched category theory|enriching]] category in [[homological algebra]]. There [[Ab-enriched categories]] play much the same role as [[Set]]-enriched categories ([[locally small categories]]) play in general. 

In this vein, the analog of $Ab$ in [[homotopy theory]] -- or rather in _[[stable homotopy theory]]_ -- is the category of [[spectra]], either regarded as the [[stable homotopy category]] or rather refined to the [[stable (infinity,1)-category of spectra]]. A spectrum is much like an abelian group up to [[coherence law|coherent]] [[homotopy]] and the role of the archetypical abelian group $\mathbb{Z}$ is the played by the [[sphere spectrum]] $\mathbb{S}$.


## Properties

### Free abelian groups

+-- {: .num_remark #FreeForgetful}
###### Remark

The category $Ab$ is a [[concrete category]], the [[forgetful functor]]

$$
  U : Ab \to Set
$$

to [[Set]] sends a group, regarded as a [[set]] $A$ equipped with the [[structure]] $(+,0)$ of a chosen element $0 \in A$ and a binary, associative and 0-unital operation $+$ to its underlying set

$$
  (A, +, 0) \mapsto A
  \,.
$$

This functor has a [[left adjoint]] $F : Set \to Ab$ which sends a set $S$ to the [[free abelian group]] $\mathbb{Z}[S]$ on this set: the group of [[formal linear combinations]] of elements in $S$ with [[coefficients]] in $\mathbb{Z}$.

=--

### Direct sum, direct product and tensor product
 {#DirectSumEtc}

We discuss basic properties of binary operations on the category of abelian groups: [[direct product]], [[direct sum]] and [[tensor product]]. Below in _[Monoidal and bimonoidal structure](#MonoidalAndBipermutativeStructure)_ we put these structures into a more abstract context.

+-- {: .num_prop }
###### Proposition

For $A, B \in Ab$ two [[abelian groups]], their
[[direct product]] $A \times B$ is the abelian group whose elements are pairs $(a, b)$ with $a \in A$ and $b \in B$, whose 0-element is $(0,0)$ and whose addition operation is the componentwise addition

$$
  (a_1, b_1) + (a_2, b_2) = (a_1 + a_2, b_1 + b_2)
  \,.
$$

This is at the same time [[generalized the|the]] [[direct sum]] $A \oplus B$.

Similarly for $I \in $[[FinSet]]$\hookrightarrow$ [[Set]] a [[finite set]], we have

$$
  \oplus_{i \in I} A_i \simeq \prod_i A_{i}
  \,.
$$

But for $I \in Set$ a set which is not finite, there is a difference: the [[direct sum]] $\oplus_{i \in I} A_i$ of an $I$-indexed family ${A_i}_{i \in I}$ of abelian groups is the sub-group of the direct product on those elements for which only finitely many components are non-0

$$
  \oplus_{i \in I} A_i \hookrightarrow \prod_i A_i
  \,.
$$

=--

+-- {: .num_example }
###### Example

The [[trivial group]] $0 \in Ab$ (the group with a single element) is a [[unit]] for the direct sum: for every abelian group we have

$$
  A \oplus 0 \simeq 0 \oplus A \simeq A
  \,.
$$

=--

+-- {: .num_example }
###### Example

In view of remark \ref{FreeForgetful} this means that the direct sum of ${\vert I \vert}$ copies of the additive group of [[integers]] with themselves is equivalently the [[free abelian group]] on $I$:

$$
  \oplus_{i \in I} \mathbb{Z} \simeq \mathbb{Z}[I]
  \,.
$$

=--


+-- {: .num_defn }
###### Definition

For $A$ and $B$ two [[abelian groups]], their [[tensor product of abelian groups]] is the group $A \otimes B$ with the property that a group homomorphism $A \otimes B \to C$ is equivalently a [[bilinear map]] out of the _set_ $A \times B$.

=--

See at _[[tensor product of abelian groups]]_ for details.

+-- {: .num_example }
###### Example

The [[unit]] for the tensor product of abelian groups is the additive group of [[integers]]: 

$$
  A \otimes \mathbb{Z} \simeq \mathbb{Z} \otimes A \simeq A
  \,.
$$

=--


+-- {: .num_prop }
###### Proposition

The [[tensor product of abelian groups]] [[distributivity law|distributes]] over arbitrary [[direct sums]]: 

$$
  A \otimes (\oplus_{i \in I} B_i) \simeq \oplus_{i \in I} A \otimes B_i
  \,.
$$

=--

+-- {: .num_example }
###### Example

For $I \in Set$ and $A \in Ab$, the [[direct sum]] of ${\vert I\vert}$ copies of $A$ with itself is equivalently the [[tensor product of abelian groups]] of the [[free abelian group]] on $I$ with $A$:

$$
  \oplus_{i \in I} A \simeq (\oplus_{i \in I} \mathbb{Z}) \otimes A
  \simeq (\mathbb{Z}[I]) \otimes A
  \,.
$$ 

=--


### Symmetric monoidal and bimonoidal structure
 {#MonoidalAndBipermutativeStructure}

With the definitions and properties discussed above in _[Direct sum, etc.](#DirectSumEtc)_ we have the following

+-- {: .num_prop }
###### Proposition

The category $Ab$ becomes a [[monoidal category]]

1. under [[direct sum]] $(Ab, \oplus, 0)$;

1. under [[tensor product of abelian groups]] $(Ab, \otimes, \mathbb{Z})$.

Indeed with both structures combined we have

* $(Ab, \oplus, \otimes, 0, \mathbb{Z})$ 

is a [[bimonoidal category]] (and can be made a [[bipermutative category]]).

=--

It's also easy to see that under direct sum or tensor product, Ab can be turned into a [[symmetric monoidal category]] by equipping it with the appropriate braiding map. For example, under $\oplus$, the braiding is $\sigma_{A, B}(a, b) = (b, a)$.

+-- {: .num_remark }
###### Remark

A [[monoid]] [[internalization|internal to]] $(Ab, \otimes, \mathbb{Z})$ is equivalently a [[ring]]. 

=--

+-- {: .num_remark }
###### Remark

A [[monoid]] in $(Ab, \oplus, 0)$ is equivalently just an abelian group again (since $\oplus$ is the [[coproduct]] in $Ab$, so every object has a unique monoid structure with respect to it).

=--

### Pointed objects 

$Ab$ is a [[monoidal category]] with [[tensor unit]] $\mathbb{Z}$, so the [[pointed objects in a monoidal category|pointed objects]] in $Ab$ are the objects $A$ with a [[group homomorphism]] $\mathbb{Z} \to A$. 

### Closed monoidal structure

Abelian groups are equivalently $\mathbb{Z}$-modules. Because the [[Mod|category of $R$-modules]] $Mod_R$ is closed monoidal for all [[commutative rings]] $R$, $Ab = Mod_{\mathbb{Z}}$ is also closed monoidal. 

### Natural numbers object

The [[natural numbers object]] in $Ab$ is the [[free abelian group]] $\mathbb{Z}[\mathbb{N}] = \bigoplus_{n \in \mathbb{N}} \mathbb{Z}$ on the [[natural numbers]], and comes with group homomorphisms $z_0:\mathbb{Z} \to \mathbb{Z}[\mathbb{N}]$ and $z_s:\mathbb{Z}[\mathbb{N}] \to \mathbb{Z}[\mathbb{N}]$ such that for all abelian groups $A$ and group homomorphisms $f:\mathbb{Z} \to A$, $g: A \to A$, there is a unique group homomorphism $\phi_{f, g}:\mathbb{Z}[\mathbb{N}] \to A$ making the following diagram commute: 

$$\array{
\mathbb{Z} & \stackrel{z_0}{\to} & \mathbb{Z}[\mathbb{N}] & \stackrel{z_s}{\leftarrow} & \mathbb{Z}[\mathbb{N}] \\
 & \mathllap{f} \searrow & \downarrow \mathrlap{\phi_{f, g}} & & \downarrow \mathrlap{\phi_{f, g}} \\
 & & A & \underset{g}{\leftarrow} & A
}$$ 

Abelian groups are $\mathbb{Z}$-[[modules]], so the free $\mathbb{Z}$-module $\mathbb{Z}[\mathbb{N}]$ has a function $v:\mathbb{N} \to \mathbb{Z}[\mathbb{N}]$ representing the [[basis of a free module|basis]] of $\mathbb{Z}[\mathbb{N}]$; it has the property that for all integers $m \in \mathbb{Z}$, $m \cdot v(0) = z_0(m)$ and for all $n \in \mathbb{N}$, $m \cdot v(s(n)) = z_s(m \cdot v(n))$, where $m \cdot v$ is the scalar multiplication of an element $v$ by an integer $m$ in a $\mathbb{Z}$-module.

The [[ring]] structure on $\mathbb{Z}[\mathbb{N}]$ is defined by double [[induction]] on $\mathbb{Z}[\mathbb{N}]$, we define 

$$(-)(-):\mathbb{Z}[\mathbb{N}] \times \mathbb{Z}[\mathbb{N}] \to \mathbb{Z}[\mathbb{N}] \otimes \mathbb{Z}[\mathbb{N}] \to \mathbb{Z}[\mathbb{N}]$$ 

by 

$$z_0(m)z_0(n) = z_0(m \cdot n) \qquad z_s(v)z_0(n) = z_s(v z_0(n))$$ 
$$z_0(m)z_s(w) = z_s(z_0(m) w) \qquad z_s(v)z_s(w) = z_s(z_s(vw))$$ 

for all $m, n \in \mathbb{Z}$ and $v, w \in \mathbb{Z}[\mathbb{N}]$ (recall the definition of [[addition]] in the [[natural numbers]], inductively defined by $0(p) + 0(q) = 0(p \cdot q)$, $s(m) + 0(p) = s(m + 0(p))$, $0(p) + s(n) = s(0(p) + n)$, and $s(m) + s(n) = s(s(m + n))$ for all $p, q \in \mathbb{1}$ and $m, n \in \mathbb{N}$). It is a [[commutative ring]] and represents multiplication in the [[polynomial ring]] $\mathbb{Z}[X]$; the group homomorphism $z_0$ represents the function which takes integers to constant polynomials, and $z_s$ represents the function which takes a polynomial and multiplies it by the indeterminate $X$. 

### Enrichment over $Ab$

Categories [[enriched category|enriched]] over $Ab$ are called [[additive category|pre-additive categories]] or sometimes just additive categories.  If they satisfy an extra exactness condition they are called [[abelian category|abelian categories]]. See at _[[additive and abelian categories]]_.

## Related concepts

* [[CMon]]

* [[Mod]]

* [[sAb]]


category: category

[[!redirects AbGrp]]

[[!redirects category of abelian groups]]
[[!redirects categories of abelian groups]]

[[!redirects AbelianGroups]]

[[!redirects ZMod]]
[[!redirects Z Mod]]
[[!redirects Z-Mod]]

[[!redirects category of Z-modules]]
[[!redirects categories of Z-modules]]

[[!redirects category of integer modules]]
[[!redirects categories of integer modules]]

[[!redirects ZModules]]
[[!redirects Z Modules]]
[[!redirects Z-Modules]]

[[!redirects IntegerModules]]



