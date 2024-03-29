+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

The concept of **dominance** is a weakening of the concept of [[surjective geometric morphism|surjectivity]] for [[geometric morphism|geometric morphisms]]. It generalizes the concept of a continuous function whose image is a [[dense subspace]] of its codomain in topology.

## Definition

A geometric morphism $f:\mathcal{F}\to\mathcal{E}$ is called _dominant_ if the following equivalent conditions hold:

* The [[direct image]] satisfies: $f_\ast(\emptyset_\mathcal{F})\cong\emptyset_\mathcal{E}$.

* The [[inverse image]] satisfies: from $f^\ast(Z)\cong\emptyset_\mathcal{F}$ follows $Z\cong\emptyset_\mathcal{E}$.

* The [[inverse image]] satisfies: from $f^\ast(Z)\cong\emptyset_\mathcal{F}$ follows $Z\cong\emptyset_\mathcal{E}$ for $Z$ a [[subterminal object]].

## Examples

* A geometric morphism $f:Sh(X)\to Sh(Y)$  between the toposes of sheaves on two topological spaces $X, Y$  is dominant iff the corresponding continuous map $f:X\to Y$  has a [[dense subspace|dense]] image $f(X)$ in $Y$.

* A geometric embedding $i:\mathcal{E}\hookrightarrow\mathcal{F}$ is dominant precisely when it exhibits $\mathcal{E}$ as a [[dense subtopos]].

## Properties

+-- {: .num_prop #dominant_surjection}
###### Proposition
If $f:\mathcal{F}\to\mathcal{E}$ is a surjection (i.e. $f^\ast$ is [[faithful]]) then $f$  is dominant.
=--

**Proof**: 
Suppose $f^\ast(Z)\cong \emptyset_\mathcal{F}$ is initial, then $Hom_\mathcal{F}(\emptyset_\mathcal{F},f^\ast(Y))=Hom_\mathcal{F}(f^\ast(Z),f^\ast(Y))$ is a singleton for all $Y\in\mathcal{E}$ , but by faithfulness of $f^\ast$ this implies that $Hom_\mathcal{E}(Z,Y)$ is a singleton for all $Y\in\mathcal{E}$ , which says that $Z$ is initial in $\mathcal{E}$. $\qed$

+-- {: .num_prop #dominant_dense}
###### Proposition
Let $f:\mathcal{F}\to\mathcal{E}$ be a geometric morphism and $i\circ s$ its [[(geometric surjection, embedding) factorization system|surjection-inclusion factorization]]. $f:\mathcal{F}\to\mathcal{E}$ is dominant iff $i:Im(f)\hookrightarrow\mathcal{E}$ is a [[dense subtopos|dense inclusion]].
=--

**Proof**: Suppose $i$ is dense, hence dominant. $s$ as a surjection is dominant as well, and so is their composition $f$.

Conversely, suppose $f:\mathcal{F}\to\mathcal{E}$ is dominant and $i^\ast(Z)\cong \emptyset_{Im(f)}$. Since $s^\ast$ preserves colimits, $\emptyset_\mathcal{F}\cong s^\ast (\emptyset_{Im(f)})\cong s^\ast\circ i^\ast (Z)=f^\ast(Z)$ but $f$ is dominant by assumption, therefore $Z\cong \emptyset_\mathcal{E}$, hence $i$ is dense. $\qed$

The following is a slight generalization of the [[(dense,closed)-factorization]] employing dominant geometric morphisms:

+-- {: .num_prop #dominant-closed}
###### Proposition
Let $f:\mathcal{F}\to\mathcal{E}$ be a geometric morphism. Then $f$ factors as a [[dominant geometric morphism]] $d$ followed by a [[closed subtopos|closed inclusion]] $c$.
=--

**Proof**: Let $i\circ d_1$ be the [[(geometric surjection, embedding) factorization system|surjection-inclusion factorization]] of $f$. Since $d_1$ is surjective, it is dominant (cf. [above](#dominant_surjection)). Then we use the [[(dense,closed)-factorization]] to factor $i$ into $c\circ d_2$. Since both $d_i$ are dominant, so is $d:=d_2\circ d_1$ and $c\circ d$ yields the demanded factorization of $f$. $\qed$

## Remark

The concept can be generalized to morphisms _in_ a topos $\mathcal{E}$ by calling $f:X\to Y$ _dominant_ if the induced geometric morphism $f^\ast\dashv\prod_f:\mathcal{E}/X\to\mathcal{E}/Y$ is dominant, where $f^\ast$ denotes the pullback functor.

## Related entries

* [[dense subtopos]]

* [[skeletal geometric morphism]]

* [[open geometric morphism]]

* [[(dense,closed)-factorization]]

* [[dense functor]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (pp.429-430, 462)