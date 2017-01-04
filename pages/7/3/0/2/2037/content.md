
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Cayley--Dickson construction
* table of contents
{: toc}

## Idea

Consider how the [[complex numbers]] are formed from the [[real numbers]].  If generalized carefully, this kind of operation may be performed again to yield the [[quaternions]], then the [[octonions]] (hence the four real [[normed division algebra]]), then the [[sedenions]], and so on.  

This is a special case of a construction which takes a real [[star-algebra]] $A$ to a new star-algebra whose elements are pairs of elements of $A$.  This operation is the __Cayley--Dickson construction__.


## Definitions

Let $A$ be an [[nonassociative algebra|possibly nonassociative]] [[star-algebra]] over the [[field]] $\mathbb{R}$ of [[real numbers]]: an algebra equipped with an [[involution]] $\overline(-) \colon x \mapsto \overline{x}$ which is an [[antiautomorphism]].  (Actually, $\mathbb{R}$ could be replaced by any [[commutative ring]] in the definitions, although some properties may depend on this ring.)

Then one defines a new algebra, the __Cayley--Dickson double__ $A^2$ of $A$ which is the [[direct sum]] $A \oplus A$ as an $\mathbb{R}$-[[vector space]], and with the multiplication rule given by

$$
  (a,b)\cdot(u,v) \coloneqq (a u - \overline{v} b, b \overline{u} + v a),
$$

and the formula

$$
  \widebar{(a,b)} \coloneqq (\overline{a},-b)
$$

defines an involutive antiautomorphism on $A^2$, so the doubling procedure can be iterated.

The map $a\mapsto (a,0)$ is a [[monomorphism]] $A\to A^2$. If $A$ is [[unital algebra|unital]] with unit $1$ then $A^2$ is unital with unit $(1,0)$. In the unital case, the element $\mathrm{i} \coloneqq (0,1)$ has the property $\mathrm{i}^2 = -1 \coloneqq (-1,0)$, and we may write $(a,b)$ as $a + b \mathrm{i}$ (while $a + \mathrm{i} b = (a,\overline{b})$).  For this reason, we may write $A[\mathrm{i}]$ in place of $A^2$, at least when $A$ is unital.


## Properties

Generally speaking, the double $A^2$ of an algebra $A$ has a nice property iff $A$ is one level nicer.  For simplicity, assume that $A$ is unital (so that $\mathbb{R}$ is a subalgebra).  Since $\overline{\mathrm{i}} = -\mathrm{i}$, we see that the involution on $A^2$ is trivial iff the involution on $A$ is trivial and $A$ further has $2 = 0$.  Since $\mathrm{i} a = \overline{a} \mathrm{i}$, $A^2$ is [[commutative algebra|commutative]] iff $A$ is commutative and the involution in $A$ is trivial.  Since $a (b \mathrm{i}) = (b a) \mathrm{i}$, $A^2$ is [[associative algebra|associative]] iff $A$ is associative and commutative. Finally, $A^2$ is [[alternative algebra|alternative]] iff $A$ is associative (and hence also alternative).


## Examples

The standard example is the sequence of consecutive doubles starting with $\mathbb{R}$ itself (with the [[identity map]] as involution); these are the __Cayley--Dickson algebras__: the [[real numbers]] $\mathbb{R}$, the [[complex numbers]] $\mathbb{C}$, the [[quaternions]] $\mathbb{H}$, the [[octonions]] (or Cayley numbers) $\mathbb{O}$, the [[sedenions]] $\mathbb{S}$, etc. These are the [[normed division algebras]] ($\mathbb{R}$, $\mathbb{C}$, $\mathbb{H}$, and $\mathbb{O}$), followed by further algebras which are not [[division algebras]].  All of these algebras are [[power-associative algebra|power-associative]] and unital and have all [[inverse elements]]; the subalgebra with $\overline{x} = x$ is always just $\mathbb{R}$.

## Related concepts 

* [[composition algebra]]

## References

*  [[M M Postnikov]], _Lectures on geometry, Semester V: Lie groups and Lie algebras_, Lec. 14 (russian and english editions)

* {#Baez02} [[John Baez]], _[The Cayley--Dickson construction](http://math.ucr.edu/home/baez/octonions/node5.html)_, in _[The octonions](http://math.ucr.edu/home/baez/octonions/)_, Bull. Amer. Math. Soc. 39 (2002), 145-205, [doi](http://dx.doi.org/10.1090/S0273-0979-01-00934-X)


* [[John Baez]], _[This Week's Finds --- Week 59](http://math.ucr.edu/home/baez/week59.html)_

* Wikipedia, _[Cayley&#8211;Dickson construction](https://en.wikipedia.org/wiki/Cayley%E2%80%93Dickson_construction)_

[[!redirects Cayley-Dickson construction]]
[[!redirects Cayley–Dickson construction]]
[[!redirects Cayley--Dickson construction]]

[[!redirects Cayley-Dickson constructions]]
[[!redirects Cayley–Dickson constructions]]
[[!redirects Cayley--Dickson constructions]]

[[!redirects Cayley-Dickson double]]
[[!redirects Cayley–Dickson double]]
[[!redirects Cayley--Dickson double]]

[[!redirects Cayley-Dickson doubles]]
[[!redirects Cayley–Dickson doubles]]
[[!redirects Cayley--Dickson doubles]]

[[!redirects Cayley-Dickson double algebra]]
[[!redirects Cayley–Dickson double algebra]]
[[!redirects Cayley--Dickson double algebra]]

[[!redirects Cayley-Dickson double algebras]]
[[!redirects Cayley–Dickson double algebras]]
[[!redirects Cayley--Dickson double algebras]]

[[!redirects double of an algebra with involution]]
[[!redirects double of algebra with involution]]
[[!redirects doubles of algebras with involution]]

[[!redirects double of a star-algebra]]
[[!redirects doubles of star-algebras]]
[[!redirects double of a *-algebra]]
[[!redirects doubles of *-algebras]]

[[!redirects Cayley-Dickson algebra]]
[[!redirects Cayley-Dickson algebras]]
[[!redirects Cayley–Dickson algebra]]
[[!redirects Cayley–Dickson algebras]]
[[!redirects Cayley--Dickson algebra]]
[[!redirects Cayley--Dickson algebras]]

[[!redirects Cayley–Dickson algebra]]
[[!redirects Cayley–Dickson algebras]]
