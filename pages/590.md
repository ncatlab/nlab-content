

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _colimit_ is that [[duality|dual]] to a [[limit]]:

a colimit of a [[diagram]] in a [[category]] is, if it exists, the [[representable functor|co-classifying space]] for morphisms _out_ of that diagram. 

The intuitive general idea of a colimit is that it defines an object obtained by sewing together the objects of the diagram, according to the instructions given by the morphisms of the diagram.  

We have

* the notion of _colimit_ generalizes the notion of [[direct sum]];

* the notion of _[[weighted colimit]]_ generalizes the notion of _weighted (direct) sum_.

Sometimes colimits (or some colimits) are called _[[inductive limits]]_ or _[[direct limits]]_; see the discussion of terminology at [[limit]].


## Definition

A [[colimit]] in a [[category]] $C$ is the same as a [[limit]] in the [[opposite category]], $C^{op}$.

More in detail, for $F : D^{op} \to C^{op}$ a functor, its [[limit]] $\lim F$ is the colimit of 
$F^{op} : D \to C$.


## Examples

Here are some important examples of colimits:

* A colimit of the [[diagram|empty diagram]] is an [[initial object]].
* A colimit of a diagram consisting of two (or more) objects and no nontrivial morphisms is their [[coproduct]].
* A colimit of a [[span]] is a [[pushout]].
* A colimit of two (or more) [[parallel morphisms]] is a [[coequalizer]].

## Weighted colimits

A [[weighted colimit]] in $C$ is a 
[[weighted limit]] in $C^{op}$.

## Properties

The properties of colimits are of course [[duality|dual]] to those of [[limit]]s. It is still worthwhile to make some of them explicit.

+-- {: .un_prop}
###### Contravariant Hom sends colimits to limits

For $C$ a [[locally small]] category,
for $F : D \to C$ a functor, for $c \in C$ and object and writing $C(F(-), c) : C \to Set$, we have
$$
  C(colim F, c) \simeq lim C(F(-), c)
  \,.
$$
=--
Depending on how one introduces limits this holds by definition or is an easy consequence. In fact, this is just rewriting the respect of the covariant Hom  of [[limit]]s (as described there) in $C^{op}$ in terms of $C$:

$$
  \begin{aligned}
    C(colim F, c) & \simeq C^{op}(c, colim F)
    \\
    & \simeq C^{op}(c, lim F^{op})
    \\
    & \simeq lim C^{op}(c, F^{op}(-))
    \\
    & \simeq lim C(F(-), c)
  \end{aligned}
$$

Notice that this actually says that $C(-,-) : C^{op} \times C \to Set$ is a [[continuous functor]] in both variables: in the first it sends limits in $C^{op}$ and hence equivalently colimits in $C$ to limits in $Set$.



+-- {: .un_prop}
###### Proposition -- left adjoints commute with colimits

Let $L : C \to C'$ be a functor that is [[left adjoint]] to some functor $R : C' \to C$. Let $D$ be a [[small category]] such that $C$ admits limits of shape $D$. Then $L$ commutes with $D$-shaped colimits in $C$ in that

for $F : D \to C$ some diagram, we have
$$
  L(colim F) \simeq colim (L \circ F)
  \,.
$$
=--

+-- {: .proof}
######Proof

Using the adjunction isomorphism and the above fact that commutes with limits in both arguments, one obtains for every $c' \in C'$
$$
\begin{aligned}
  C'(L (colim F), c) & \simeq C(colim F, R(c'))
  \\
  & \simeq lim C(F(-), R(c')) 
  \\
  & \simeq lim C'(L \circ F(-), c')
  \\
  & \simeq C'(colim (L \circ F), c') 
  \,.
\end{aligned}
  \,.
$$

Since this holds naturally for every $c'$, the [[Yoneda lemma|Yoneda lemma, corollary II]] on uniqueness of representing objects implies that $R (lim F) \simeq lim (R \circ F)$.
=--

## Related concepts

* [[filtered colimit]]

  * [[directed colimit]]

    * [[sequential colimit]]

* [[sifted colimit]]

* [[direct sum]]

* [[homotopy colimit]], [[(∞,1)-colimit]]

* [[lax colimit]]

## Reference

[[limit|Limits]] and colimits were defined in [[Daniel M. Kan]] in Chapter II of the paper that also defined [[adjoint functors]] and [[Kan extensions]]:

* [[Daniel M. Kan]], _Adjoint functors_, Transactions of the American Mathematical Society 87:2 (1958), 294–294 ([doi:10.1090/s0002-9947-1958-0131451-0](https://doi.org/10.1090/s0002-9947-1958-0131451-0)).

This paper refers to colimits as _direct limits_.

[[!redirects colimits]]
[[!redirects colimit functor]]
[[!redirects colimit functors]]
