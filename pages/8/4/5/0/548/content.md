
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[group]]

* **2-group**

* [[n-group]]

* [[∞-group]]

***

#Contents#

* automatic table of contents goes here
{:toc} 


## Idea

A $2$-group is a [[vertical categorification]] of the idea of [[group]]. 

It is the special case of an [[n-group]] for $n=2$.


## Definition 

A __$2$-group__ is a groupal [[groupoid]], that is a groupoid whose objects have been made into a [[group]].  Equivalently, it is a [[monoidal category]] in which each every [[object]] and [[morphism]] is invertible.  Also equivalently, it is a $2$-[[2-groupoid|groupoid]] with one object, a very basic case of a [[k-tuply groupal n-groupoid]].

Like other notions of [[higher category theory]], $2$-groups come in weak and strict forms, depending on how you interpret the above.


### Strict $2$-groups

The earliest version studied is that of [[strict 2-group]]s.

A __strict $2$-group__ consists of:

* a collection of [[group]] homomorphisms of the form
  $$
    C_1 \stackrel{s,t}{\to} C_0 \stackrel{i}{\to} C_1
  $$
such that the composites $s\cdot i$ and $t\cdot i$ are the identity morphisms on $C_0$, and
  such that, writing  $C_1 \times_{t,s} C_1$ for the pullback, 
  $$
    \array{
      C_1 \times_{t,s} C_1 &\to& C_1
      \\
      \downarrow && \downarrow^{t}
      \\
      C_1 &\stackrel{s}{\to}& C_0
    }
  $$
  there is, in addition,  a homomorphism
  $$
     C_1 \times_{t,s} C_1 \stackrel{comp}{\to} C_1
  $$
  "respecting $s$ and $t$";

* such that the _composition_ $comp$ is associative
  and unital with respect to $i$ "in the obvious way".

See [[strict 2-group]] for further discussion and examples.


### Weak $2$-groups 

A __weak $2$-group__, or simply __$2$-group__, is a (weak) [[monoidal category]] *such that*:

*  given any object $x$, there exists an object $x^{-1}$ such that the monoidal products $x \otimes x^{-1}$ and $x^{-1} \otimes x$ are each [[isomorphism|isomorphic]] to the monoidal unit $1$.

A __coherent $2$-group__ is a monoidal category *equipped with*:

*  for each object $x$ a specific object $x^{-1}$ and specific [[isomorphism]]s from $x \otimes x^{-1}$ and $x^{-1} \otimes x$ to $1$ which form an [[adjoint equivalence]].

A theorem in HDA5 shows that every weak $2$-group may be made coherent.  For purposes of [[internalization]], one probably wants to use the coherent version.

We can also write this out in detail ... later.


## Examples 

### Strict 2-groups

Since strict 2-groups are equivalent to [[crossed module]]s, see the examples listed there.

### Automorphism 2-groups 

For $C$ any [[2-category]] and $c \in C$ any object of it, the category $Aut_C(c) \subset Hom_C(c,c)$ of auto-equivalences of $c$ and invertible 2-morphisms between these is naturally a 2-group, whose group product comes from the horizontal composition in $C$.

If $C$ is a [[strict 2-category]] there is the notion of strict [[automorphism 2-group]]. See there for more details on that case.

For instance if $C = Grp_2 \subset Grpd$ is the 2-category of [[group]] obtained by regarding groups as one-object [[groupoid]]s, then for $H \in Grp$ a group, its automorphism 2-group obtained this way is the strict 2-group

$$
  AUT(H) := Aut_{Grp_2}(H)
$$

corresponding to the [[crossed module]] $(H \stackrel{Ad}{\to} Aut(H))$, where $Aut(H)$ is the ordinary [[automorphism group]] of $H$.

### Inner automorphism 2-groups

See [[inner automorphism 2-group]].

### String 2-group

See [[string 2-group]].


## References 

*  [[John Baez]] and [[Aaron Lauda]], _HDA V: 2-Groups_ ([arXiv](http://arxiv.org/abs/math.QA/0307200)).


[[!redirects 2-groups]]
