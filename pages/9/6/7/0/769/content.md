
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The notion of _comma object_ or _comma square_ is a generalization of the notion of [[pullback]] or _pullback square_ from [[category theory]] to [[2-category]] [[higher category theory|theory]]: it is a special kind of _[[2-limit]]_.

Where a [[pullback]] involves a [[commuting diagram|commuting square]], for a comma object this square is filled by a [[2-morphism]].


## Definition

The **comma object** of two morphisms $f:A\to C$ and $g:B\to C$ in a [[2-category]] is an object $(f/g)$ equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ and a 2-cell

$$
\array{
  (f/g) & \overset{p}{\to} & A \\
  \mathllap{\scriptsize{q}} \downarrow & \swArrow \alpha & \downarrow   \mathrlap{\scriptsize{f}} \\
  B & \underset{g}{\to} & C
}
$$

which is universal in the sense of a [[2-limit]].  Comma objects are also sometimes called **lax pullbacks**, but this term more properly refers to the [[lax limit]] of a cospan.

Part of this (to be explicit) is the statement that for any object $D$, 1-morphisms $p':D\to A$, $q':D\to B$ and 2-cell $\sigma:f p'\Rightarrow g q'$ there is a 1-morphism $u:D\to(f/g)$ and isomorphisms $p u\cong p'$, $q u\cong q'$ such that modulo these isomorphisms, we have $\sigma=\alpha u$.  There is also an additional "2-dimensional universality" saying that given $u:D\to (f/g)$ and $v:D\to (f/g)$ and 2-cells $\mu:p u \to p v$ and $\nu:q u \to q v$ such that $\alpha v. f \mu = g\nu . \alpha u$, there exists a unique 2-cell $\beta:u\to v$ such that $p\beta = \mu$ and $q \beta = \nu$.  Note that the 2-dimensional property implies that in the 1-dimensional property, [[generalized the|the]] 1-morphism $u$ is unique up to unique isomorphism.  A square containing a 2-cell with this property is sometimes called a **comma square**.

A **strict comma object** is analogous but has the universal property of a [[strict 2-limit]].  This means that given $p'$, $q'$, and $\sigma$ as above, there exists a _unique_ $u:D\to (f/g)$ such that $p u = p'$, $q u = q'$, and $\sigma u = \alpha$.  Note that any strict comma object is a comma object, but the converse is not in general true.


## Properties

### Construction

The comma object $f/g$ can be constructed by means of [[pullbacks]] and [[cotensors]]:
$$
\array{
f/g & \to & P & \to & A \\
\downarrow & & \downarrow & & \downarrow \mathrlap{\scriptsize{f}} \\
Q & \to & C^{\mathbf{2}} & \underset{dom}{\to} & C \\
\downarrow & & \downarrow \mathrlap{\scriptsize{cod}} \\
B & \underset{g}{\to} & C
}
$$
where $C^{\mathbf{2}}$ is the cotensor of $C$ with the arrow category $\mathbf{2} = \bullet \to \bullet$.


### Pasting lemma

Suppose given a diagram
$$
\array{
  P & \to & Q & \to & A \\
  \downarrow & & \mathllap{\scriptsize{p}} \downarrow & \swArrow & \downarrow   \mathrlap{\scriptsize{f}} \\
  D & \underset{h}{\to} & C & \underset{g}{\to} & B
}
$$
where the right-hand square is a comma square.  Then the following are equivalent:

* the whole diagram is a comma square
* the left-hand square is a (2-)pullback square

The proof is analogous to that at [[pullback]].


## Examples

* In [[Cat]], a [[comma category]] is a comma object (in fact a strict one, as normally defined); these give their name to the general notion.

* In the 2-category of [[virtual double categories]], a comma object is a [[comma double category]].  If the virtual double categories are (pseudo) [[double categories]] and the domain functor $f$ in $f/g$ is strong (while $g$ might be only lax), then the comma object is also a pseudo double category and the comma object lives in the 2-category of pseudo double categories and lax functors.

## Related pages

* [[oplax/lax comma object]]

[[!include notions of pullback -- contents]]



[[!redirects comma object]]
[[!redirects comma objects]]
[[!redirects comma square]]
[[!redirects comma squares]]
[[!redirects lax pullback]]
[[!redirects lax pullbacks]]
