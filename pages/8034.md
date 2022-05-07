
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

## p-torsion of abelian groups

Since any [[abelian group]] $G$ is a $\mathbb{Z}$-[[module]] we can form for any  $z\in \mathbb{N}$ the [[torsion subgroup]]

$$
  G[z]
  \,\coloneqq\,
  \big\{
    g
    \,\vert\, 
    g \in G,  
    \,
    z g = 0
  \big\}
  \,.
$$

Of particular interest in this article are those cases where $z = p^n$ for a [[prime number]] $p$ and a [[natural number]] $n$.

There are two important constructions to perform with these $G[p^n]$ namely taking [[limits]] and [[colimits]]:

$$
  S_p(G)
  \,\coloneqq\,
  colim_n G[p^n]
$$


$$
  T_p(G)
  \,\coloneqq\,
  lim_n G[p^n]
  \,.
$$



Here $S_p(G)$ is sometimes called the *$p$-[[torsion subgroup]]*; if $G$ is [[finite group|finite]] then $S_p(G)$ is also called *[[Sylow p-subgroup]] of $G$*.

$T_p(G)$ is called [[Tate module|p-adic Tate module]] of $G$.

Note that sometimes by "the Tate module" is meant a specific example of a Tate module. This example is mentioned [below](#PAdicTateModule).

## p-torsion of fields

$G[p]$ is obviously the [[kernel]] of the [[Frobenius]] [[endomorphism]] of $G$:

$$
  G[p]
  \,=\,
  \big(
    ker \, (g \mapsto g^p)
  \big)
  \,.
$$

In this form we can extend the Frobenius and hence this notion of $p$-torsion from [[abelian groups]] to [[fields]], if we require our field to be of [[characteristic]] $p$ such that we have $(a+b)^p = a^p + b^p$.

In fact the definition of $p$-torsion via the Frobenius has the advantage that we get additionally an adjoint notion to $p$-torsion which is sometimes called *Verschiebung*; this is explained at [[nLab:Demazure, lectures on p-divisible groups, I.9, the Frobenius morphism
]].

## p-torsion of schemes

If $X$ denotes some [[scheme]] over a $k$-[[ring]] for $k$ being a [[field]] of [[characteristic]] $p$, we define its $p$-torsion component-wise by $X^{(p)}(R) \coloneqq X(s_* R)$.

## p-torsion of group schemes

Let $G$ is a commutative group scheme over a scheme $S$.  Define the multiplication by $p$ map as follows -   $[p] \colon G \xrightarrow{\Delta} G \times_S .... \times_S G \to G$.

  Because $G$ is a commutative group scheme, this is a map in the category of group schemes.  The $[p]$ torsion, $G[p]$, is then the pullback along the identity section of the multiplication by $[p]$ map.

The fiber of $G[p]$ at a given $s \in S$ is a group.  (Its a group scheme over the residue field of $s$).   And it is the $p$-torsion in the fiber of $G$ at $s$.

The notions of $S_p$, (as an Ind-scheme) and $T_p$ (as a scheme) readily generalize using this notion of $p$-torsion.

+-- {: .num_example #PAdicTateModule}
###### Example
(*the* $p$-adic [[Tate module]])

Let $G$ be a commutative group scheme over a field $k$ with separable closure $k^{sep}$.

Then $T_p\big(G(k^{sep})\big)$ is called *the $p$-adic Tate module of $G$*.
=--

This Tate module enters the [[Tate conjecture]].

If $G$ is an abelian variety $T_p(G(k^{sep}))$ is equivalently the first homology group of $G$.

## p-divisible groups

(main article: [[nLab:p-divisible group]])

Sometimes the information encoded in the colimit $T_p(G)=colim_n G[p^n]$ (we passed a contravariant functor from rings to schemes) is considered to be not sufficient and one wants more generally to study the codirected system

$$0\to G[p]\stackrel{p}{\to}G[p^2]\stackrel{p}{\to}\dots \stackrel{p}{\to}G[p^{n}]\stackrel{p}{\to}G[p^{n+1}]\stackrel{p}{\to}\dots$$

itself. This system is called *$p$-divisible group of $G$*. Here $p$ denotes the multiplication-with-$p$ map.

We have

(1) The $G[p^i]$ are finite group schemes.

(2) The sequences of the form

$$0\to ker\, p^j\xhookrightarrow{\iota_j} ker p^{j+k}\stackrel{p^j}{\to}ker p^k\to 0$$

are exact.

(3) $G=\cup_j ker\, p^j\cdot id_G$

We have as cardinality (in group theory also called "rank") of the first item of the sequence $card \ker \,p=p^h$ for some natural number $h$. By pars pro toto we call $p^h$ also the rank of the whole sequence and $h$ we call its *height*.

Conversely we can define a $p$-divisible group to be a codirected diagram

$$G_1\stackrel{i_1}{\to}G_2\stackrel{i_2}{\to}\dots$$

satisfying (1)(2)(3).

## Related concepts

* [[torsion approximation]]

## References

see the references at [[nLab:p-divisible group]], in particular the notes 

* Richard Pink, *Shatz Group Schemes, Formal Groups, and $p$-Divisible Groups*

[[!redirects p-torsion subgroup]]
[[!redirects p-torsion subgroups]]
