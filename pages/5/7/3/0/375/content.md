
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A __cartesian closed category__ (sometimes: __ccc__) is a category with finite [[products]] which is [[closed monoidal category|closed]] with respect to its [[cartesian monoidal category|cartesian monoidal structure]].

The [[internal hom]] $[S,X]$ in a cartesian closed category is often called [[exponentiation]] and is denoted $Y^S$.

## Examples

* Any [[topos]] or [[quasitopos]], such as [[Set]], is cartesian closed.

  See also [[closed monoidal structure on presheaves]].

* [[Cat]] is also cartesian closed.

* Many [[nice category of spaces|nice categories of topological spaces]] are also cartesian closed, particularly the [[convenient category of topological spaces|convenient categories of spaces]].

## Some basic consequences 

A category is cartesian closed if it has finite products and if for any two objects $X$, $Y$, there is an object $Y^X$ (thought of as a "space of maps from $X$ to $Y$") such that for any object $Z$, there is a bijection between the set of maps $Z \to Y^X$ and the set of maps $Z \times X \to Y$, and this bijection is natural in $Z$. 

There is an evaluation map $ev_{X, Y}: Y^X \times X \to Y$, which by definition is the map corresponding to the identity map $Y^X \to Y^X$ under the bijection. Using the naturality, it may be shown that the bijection $\hom(Z, Y^X) \to \hom(Z \times X, Y)$ takes a map $\phi: Z \to Y^X$ to the composite 

$$Z \times X \stackrel{\phi \times 1_X}{\to} Y^X \times X \stackrel{ev_{X, Y}}{\to} Y$$ 

and the universal property of $Y^X$ may be phrased thus: given any $\psi: Z \times X \to Y$, there exists a unique map $\phi: Z \to Y^X$ for which $\psi = ev_{X, Y} \circ (\phi \times 1_X)$. 

Taking $Z = 1$ (the terminal object), maps $1 \to Y^X$ (or "points" of $Y^X$) are in bijection with maps $X \stackrel{\pi_{2}^{-1}}{\to} 1 \times X \to Y$. So the "underlying set" of $Y^X$, namely $\hom(1, Y^X)$, is identified with the set of maps from $X$ to $Y$. Let us denote the point corresponding to $f: X \to Y$ by $[f]: 1 \to Y^X$. Then, by definition,  

$$(1 \times X \stackrel{[f] \times 1_X}{\to} Y^X \times X \stackrel{ev_{X, Y}}{\to} Y) = (1 \times X \stackrel{\pi_2}{\to} X \stackrel{f}{\to} Y)$$

The following lemma says that the internal evaluation map $ev_{X, Y}$ indeed behaves as an evaluation map at the level of underlying sets. 

+-- {: .un_lem}
######Lemma
Given a map $f: X \to Y$ and a point $x: 1 \to X$, the composite 
$$1 \stackrel{\langle [f], x \rangle}{\to} Y^X \times X \stackrel{ev_{X, Y}}{\to} Y$$ 
is the point $f x: 1 \to Y$. 
=-- 

+-- {: .proof} 
######Proof 
We have 
$$\array{
1 \stackrel{\langle [f], x \rangle}{\to} Y^X \times X \stackrel{ev_{X, Y}}{\to} X & = & 1 \stackrel{\delta_1}{\to} 1 \times 1 \stackrel{[f] \times x}{\to} Y^X \times X \stackrel{ev_{X, Y}}{\to} Y\\
 & = & 1 \stackrel{\delta_1}{\to} 1 \times 1 \stackrel{1 \times x}{\to} 1 \times X \stackrel{[f] \times 1_X}{\to} Y^X \times X \stackrel{ev_{X, Y}}{\to} Y\\
 & = & 1 \stackrel{\delta_1}{\to} 1 \times 1 \stackrel{1 \times x}{\to} 1 \times X \stackrel{\pi_2}{\to} X \stackrel{f}{\to} Y\\
 & = & 1 \stackrel{\delta_1}{\to} 1 \times 1 \stackrel{\pi_2}{\to} 1 \stackrel{x}{\to} X \stackrel{f}{\to} Y\\
 & = & 1 \stackrel{x}{\to} X \stackrel{f}{\to} Y
}$$
where the penultimate equation uses naturality of the projection map $\pi_2$. 
=-- 

+-- {: .un_def}
######Definition 
**Internal composition** $c_{X, Y, Z}: Z^Y \times Y^X \to Z^X$ is the unique map such that 
$$(Z^Y \times Y^X \times X \stackrel{c \times 1_X}{\to} Z^X \times X \stackrel{ev_{X, Z}}{\to} Z) = (Z^Y \times Y^X \times X \stackrel{1 \times ev_{X, Y}}{\to} Z^Y \times Y \stackrel{ev_{Y, Z}}{\to} Z)$$ 
=-- 

One may show that internal composition behaves as the usual composition at the underlying set level, in that given maps $g: Y \to Z$, $f: X \to Y$, we have 

$$(1 \stackrel{\langle [g], [f] \rangle}{\to} Z^Y \times Y^X \stackrel{c_{X, Y, Z}}{\to} Z^X) = [g f]: 1 \to Z^X$$

## Properties

* In a cartesian closed category, the product functors $A \times -$ have [[right adjoints]], so they preserve all [[colimits]].  In particular, a cartesian closed category that has finite [[coproducts]] is a [[distributive category]].

* The [[internal logic]] of cartesian closed categories is the [[typed lambda-calculus]].

### Inheritance by reflective subcategories

In showing that a given category is cartesian closed, the following theorem is often useful (cf. A4.3.1 in the [[Elephant]]):

+-- {: .un_theorem}
###### Theorem
If $C$ is cartesian closed, and $D\subseteq C$ is a [[reflective subcategory]], then the reflector $L\colon C\to D$ preserves finite [[products]] if and only if $D$ is an [[exponential ideal]] (i.e. $Y\in D$ implies $Y^X\in D$ for any $X\in C$).  In particular, if $L$ preserves finite products, then $D$ is cartesian closed.
=--

### Exponentials of cartesian closed categories

The following observation was taken from a post of Mike Shulman at [MathOverflow](http://mathoverflow.net/questions/104152/exponentials-in-functor-categories/104178#104178). 

If $\mathcal{C}$ is small and $\mathcal{D}$ is complete and cartesian closed, then $\mathcal{D}^{\mathcal{C}}$ is also complete and cartesian closed. Completeness is clear since limits in $D^C$ are computed pointwise. As for cartesian closure, we can compute exponentials in essentially the same way as for presheaves, motivated by $\mathcal{D}$-enriched category theory:
$$
G^F(x) = \int_{y\in \mathcal{C}} \prod_{\mathcal{C}(x,y)} G(y)^{F(y)}.
$$
Then we can compute
<p>
$$
\array{
  \mathcal{D}^{\mathcal{C}}\left(H,G^F\right)
  &=& \int_{x\in \mathcal{C}} \mathcal{D}\left(H(x), G^F(x)\right)\\
  &=& \int_{x\in \mathcal{C}} \mathcal{D}\left(H(x), \int_{y\in \mathcal{C}} \prod_{\mathcal{C}(x,y)} G(y)^{F(y)}\right)\\
  &=& \int_{x\in \mathcal{C}} \int_{y\in \mathcal{C}} \prod_{\mathcal{C}(x,y)} \mathcal{D}\left(H(x), G(y)^{F(y)}\right)\\
  &=& \int_{y\in \mathcal{C}} \mathcal{D}\left( \int^{x\in \mathcal{C}} \sum_{\mathcal{C}(x,y)} H(x), G(y)^{F(y)}\right)\\
  &=&  \int_{y\in \mathcal{C}} \mathcal{D}\left(H(y), G(y)^{F(y)}\right)\\
  &=&  \int_{y\in \mathcal{C}} \mathcal{D}\left(H(y)\times F(y), G(y)\right)\\
  &=& \mathcal{D}^{\mathcal{C}}(H\times F, G).
}
$$
</p>

Here the antepenultimate step uses the [[co-Yoneda lemma]].  This appears to involve colimits in $\mathcal{D}$ as well, but the existence of these colimits is not actually an extra assumption: the co-Yoneda lemma tells us that $\int^{x\in \mathcal{C}} \sum_{\mathcal{C}(x,y)} H(x)$ _exists and is isomorphic to_ $H(y)$.

Similarly, the above argument can be interpreted to say that even if $\mathcal{D}$ is not complete, then the exponential $G^F$ in $\mathcal{D}^{\mathcal{C}}$ exists if and only if the particular limits above exist, and in that case they are isomorphic.

## Related concepts

* **cartesian closed category**, [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]

* [[cartesian closed model category]], [[locally cartesian closed model category]]

* [[cartesian closed (∞,1)-category]] [[locally cartesian closed (∞,1)-category]]



[[!redirects cartesian closed category]]
[[!redirects cartesian closed categories]]
[[!redirects cartesian closed]]
[[!redirects closed cartesian category]]
[[!redirects closed cartesian categories]]
