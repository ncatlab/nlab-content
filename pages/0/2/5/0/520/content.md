
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A __pointed set__ is a [[pointed object]] in [[Set]], hence a [[set]] $S$ equipped with a chosen element $s$ of $S$. (Compare [[inhabited set]], where the element is not specified.)

Since we can identify a (set-theoretic) element of $S$ with a (category-theoretic) [[global element]] (a morphism $s: {\ast} \to S$ from the [[terminal object]] ${\ast}$), we see that a pointed set is an object of the [[under category]] $\pt \downarrow \Set$, or coslice category ${\ast}/\Set$, of objects under the [[singleton set]] ${\ast}$.

## The category of pointed sets

### Definition

+-- {: .un_defn}
###### Definition

The [[category]] $\Set_{\ast}$ of pointed sets is the [[under category]] ${\ast}/\Set$ of [[Set]] under the [[singleton set]] ${\ast}$.

=--


So a morphism $(S_1, s_1) \to (S_2, s_2)$ is a map between sets which maps these chosen elements to each other, i.e., commuting triangles

$$
  \array{
    && {\ast}
    \\
    & ^{s_1}\swarrow && \searrow^{s_2}
    \\
    S_1
    &&\to&&
    S_2
  }
 \,.
$$

The category $\Set_{\ast}$ naturally comes with a [[forgetful functor]] $p : \Set_{\ast} \to \Set$ which forgets the tip of these triangles.

### Properties

+-- {: .un_prop}
###### Proposition

Equipped with the [[smash product]] ${\otimes} := {\wedge}$ of pointed sets, $(\Set_{\ast}, {\wedge})$ is a [[closed monoidal category|closed]] [[symmetric monoidal category]].

The [[internal hom]] $\Set_{\ast}(X,Y)$ is the [[hom-set]] in ${\ast}/\Set$ pointed by the morphism $X \to Y$ that sends everything to the basepoint in $Y$.

=--

See at _[[pointed object]]_ for more details.

#### Pointed objects in the category of pointed sets

The [[tensor unit]] of pointed sets is the [[boolean domain]] $\mathbb{2}$, and [[pointed object in a monoidal category|pointed objects]] in the category of pointed sets are [[bi-pointed sets]]. 

#### Natural numbers object

In [[classical mathematics]], the [[natural numbers object]] in $Set_*$ is the [[set]] of [[extended natural numbers]] $\overline{\mathbb{N}} = \mathbb{N} + \{\infty\}$, and comes with point-preserving functions $z_0:\mathbb{2} \to \overline{\mathbb{N}}$ and $z_s:\overline{\mathbb{N}} \to \overline{\mathbb{N}}$ such that for all pointed sets $A$ and point-preserving functions $f:\mathbb{2} \to A$, $g: A \to A$, there is a unique point-preserving function $\phi_{f, g}:\overline{\mathbb{N}} \to A$ making the following diagram commute: 

$$\array{
\mathbb{2} & \stackrel{z_0}{\to} & \overline{\mathbb{N}} & \stackrel{z_s}{\leftarrow} & \overline{\mathbb{N}} \\
 & \mathllap{f} \searrow & \downarrow \mathrlap{\phi_{f, g}} & & \downarrow \mathrlap{\phi_{f, g}} \\
 & & A & \underset{g}{\leftarrow} & A
}$$ 

The point-preserving function $z_0$ represents the function which takes the [[boolean]] [[true]] to $\infty$ and [[false]] to zero, and $z_s$ represents the point-preserving function which takes a natural number to its successor and $\infty$ to $\infty$.

The [[absorption monoid]] structure on $\overline{\mathbb{N}}$ is defined by double [[induction]] on $\overline{\mathbb{N}}$, we define 

$$(-)+(-):\overline{\mathbb{N}} \times \overline{\mathbb{N}} \to \overline{\mathbb{N}} \wedge \overline{\mathbb{N}} \to \overline{\mathbb{N}}$$ 

by 

$$z_0(p) + z_0(q) = z_0(p \vee q) \qquad z_s(m) + z_0(q) = z_s(m + z_0(q))$$ 
$$z_0(p) + z_s(n) = z_s(z_0(p) + n) \qquad z_s(m) + z_s(n) = z_s(z_s(m + n))$$ 

for all $p, q \in \mathbb{2}$ and $m, n \in \overline{\mathbb{N}}$, where $p \vee q$ is the [[disjunction]] of [[booleans]] $p$ and $q$ (recall the definition of [[addition]] in the [[natural numbers]], inductively defined by $0(p) + 0(q) = 0(p \cdot q)$, $s(m) + 0(p) = s(m + 0(p))$, $0(p) + s(n) = s(0(p) + n)$, and $s(m) + s(n) = s(s(m + n))$ for all $p, q \in \mathbb{1}$ and $m, n \in \mathbb{N}$). It is a [[commutative monoid]] and represents addition in $\overline{\mathbb{N}}$. 

In [[constructive mathematics]], the extended natural numbers $\overline{\mathbb{N}}$ and the [[disjoint union]] $\mathbb{N} + \{\infty\}$ are no longer the same; it is $\mathbb{N} + \{\infty\}$ which remains the natural numbers object in $Set_*$.

#### Interpretation as universal Set-bundle 
 {#InterpretationAsUniversalSetBundle}

The morphism $\Set_{\ast} \to \Set$ is an example of a 
[[generalized universal bundle]]: the _universal [[Set]]-bundle_. 
The entire structure here can be understood as arising from the (strict) pullback diagram

$$
  \array{
    \Set_{\ast} &\to& \pt
    \\
    \downarrow && \downarrow^{\pt \mapsto {\ast}}
    \\
    [I,\Set]
    &\stackrel{d_0}{\to}& \Set
    \\
    \downarrow^{d_1}
    \\
    \Set
  }
$$

in the 1-category [[Cat]], where

* $I = \{0 \to 1\}$ is the [[interval category]];

* $[I, \Set] = Arr(\Set)$ is the [[closed monoidal category|internal hom]] category which here is the [[arrow category]] of $\Set$;

* $d_i := [j_i, \Set]$ are the images of the two injections 
$j_i : \pt \to I$ of the point to the left and the right end of the interval, respectively --- so these functors evaluate on the left and right end of the interval, respectively;

* the square is a pullback;

* the total vertical functor is the forgetful functor $p : \Set_{\ast} \to \Set$.

The way in which $\Set_{\ast} \to \Set$ is the "universal Set-bundle" is discussed pretty explicitly in

* Kathryn Hess, _[[HessLackBundCat.pdf:file]]_ .

(The discussion there becomes more manifestly one of bundles if one regards all morphisms $C \to \Set$ appearing there as being the right legs of [[anafunctor|anafunctors]]. )


#### Interpretation as 2-subobject-classfier

Observing that usual morphism into the [[subobject classifier]] $\Omega$ of the [[topos]] [[Set]] is the 
[[universal truth-value bundle]] 
$\{\top\} \to \TV$, and noticing that $TV = (-1)Cat$ and $Set = 0Cat$ suggests that $Set_* \to Set$ is a [[vertical categorification|categorified]] subobject classifier:
indeed, it is the subobject classifier in the [[2-topos]] [[Cat]].

For discussion of this point see

* David Corfield: _101 things to do with a 2-classifier_ ([blog](http://golem.ph.utexas.edu/category/2008/01/101_things_to_do_with_a_2class.html))

It was David Roberts who pointed out in

* David Roberts, [comment to: 101 things to do with a 2-classifier](http://golem.ph.utexas.edu/category/2008/01/101_things_to_do_with_a_2class.html#c014559)

the relation between these higher classifiers and higher [[generalized universal bundle|generalized universal bundles]], motivated by the observations on principal universal 1- and 2-bundles in 

* David Roberts, Urs Schreiber, _The inner automorphism 3-group of a strict 2-group_, Journal of Homotopy and Related Structures, Vol. 3(2008), No. 1, pp. 193-244, ([arXiv](http://arxiv.org/abs/0708.1741v2)).

## Related concepts

* [[pointed object]]

* [[pointed topological space]]

* [[pointed simplicial set]]

* [[pointed homotopy type]]

[[!redirects pointed sets]]

[[!redirects category of pointed sets]]