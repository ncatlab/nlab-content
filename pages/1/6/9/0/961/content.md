
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Congruences
* table of contents
{: toc}


## Definitions

+-- {: .num_defn}
###### Definition

In a [[finitely complete category]] $C$, a **congruence** on an object $X$ is an [[internalization|internal]] [[equivalence relation]] on $X$.

This means that it consists of a [[subobject]] $R\stackrel{(p_1,p_2)}\hookrightarrow X \times X$ equipped with the following [[morphisms]]:
* internal [[reflexive relation|reflexivity]]: $r: X \to R$ which is a [[section]] both of $p_1$ and of $p_2$;
* internal [[symmetric relation|symmetry]]: $s: R \to R$ which interchanges $p_1$ and $p_2$, namely $p_1\circ s = p_2$ and $p_2\circ s = p_1$;
* internal [[transitive relation|transitivity]]: $t: R \times_X R \to R$; where with the notation for the projections in the [[cartesian square]]
$$\array{
R \times_X R & \stackrel{q_2}\rightarrow & R\\
\downarrow^{q_1} && \downarrow^{p_2}\\
R & \stackrel{p_1}\rightarrow & X
}$$
the following holds: $p_1\circ q_1 = p_1\circ t$ and $p_2\circ q_2 = p_2\circ t$.

=--

+-- {: .num_remark}
###### Remark

Since $(p_1,p_2)$ is a [[monomorphism]], the maps $r$, $s$, and $t$ are necessarily unique if they exist.

=--

+-- {: .num_example}
###### Example

Every [[kernel pair]] is a congruence.

=--

+-- {: .num_defn}
###### Definition

A congruence which is the kernel pair of some morphism is called **effective**.  

=--

+-- {: .num_defn}
###### Definition

The [[coequalizer]] of a congruence is called a **[[quotient object]]**.  

=--

+-- {: .num_prop}
###### Proposition

An effective congruence is always the kernel pair of its quotient if that quotient exists.

=--

+-- {: .num_defn}
###### Definition

The quotient of an effective congruence is an **effective quotient**.  

=--

+-- {: .num_defn}
###### Definition

A [[regular category]] is called an [[exact category]] if every congruence is effective.

=--


## Examples

+-- {: .num_example}
###### Example

An [[equivalence relation]] is precisely a congruence in [[Set]].

=--

+-- {: .num_example}
###### Example

The eponymous example is congruence modulo $n$ (for a fixed [[natural number]] $n$), which can be considered a congruence on $\mathbb{N}$ in the category of [[rigs]], or on $\mathbb{Z}$ in the category of [[rings]].

=--

+-- {: .num_example}
###### Example


A [[quotient group]] by a  [[normal subgroup]] $K \hookrightarrow G$ is the quotient of the relation $G \times K \stackrel{(p_1,p_2)}{\hookrightarrow} G \times G$, where $p_1$ is projection on the first factor and $p_2$ is multiplication in $G$ (these are source and target maps in the [[action groupoid]] $G \sslash K$).

A special case of this is that of a _[[quotient module]]_.

=--

## Related pages

* The notions of [[regular category]] and [[exact category]] can naturally be formulated in terms of congruences.  A "higher arity" version, corresponding to [[coherent categories]] and [[pretoposes]] is discussed at [[familial regularity and exactness]].

* A [[Mal'cev category]] is a [[finitely complete category]] in which every internal relation satisfying reflexivity is thereby actually a congruence.

* [[higher category theory|Higher-categorical]] generalizations are that of a [[2-congruence]] and of a [[groupoid object in an (∞,1)-category]]. See also [[(n,r)-congruence]].


[[!redirects congruences]]
[[!redirects internal equivalence relation]]