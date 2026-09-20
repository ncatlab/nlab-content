
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

## Idea

A _subgroup_ of a group is a subset equipped with the "same" group operation. As-in, a [[subobject]] in the [[category]] [[Grp]] of [[group]]s; hence a [[monomorphism]] of groups


$$
  K \hookrightarrow G
  \,.
$$

Here $K$ is _a subgroup of $G$_. 

## Definition

A [[subset]] $H$ of the [[set]] $G$ underlying a [[group]] is a *subgroup* of $G$ iff the [[restriction]] of the group operation • to $H$ is a group. For all subgroups $H$ of a group $G$, 

* the [[identity]] [[element]] $e\in G$ is in $H$,

* for all $h\in H$, the [[inverse]] $h^-^1\in G$ is in $H$,

* for non-negative [[integers]] $n$ and $m$ $H$={$g ^n h ^-^m$|$g \in H \wedge h \in H$}.

For $A$ a subset of the [[automorphism|automorphisms]] group $Aut(G)$ of a group $G$, a subgroup $H \subseteq G$ is called an $A$-*invariant subgroup* of $G$ if for $h \in H$ and $\alpha \in A$ then $\alpha (h) \in H$. A subgroup $H$ of a group $G$ is called:

* a *characteristic subgroup* of $G$ if $H$ is $Aut(G)$-invariant.

* a [[normal subgroup|normal]] or *self-conjugate subgroup* of $G$ is $H$ is $Inn Aut(G)$-invariant. As-in, if $g \in G$ and $h \in H$ then $g ^- ^1hg \in H$.

## Special cases

* [[normal subgroup]]

* [[stabilizer subgroup]]

* [[maximal compact subgroup]]

* [[torsion subgroup]]

* [[Borel subgroup]]

* [[parabolic subgroup]]

* [[generalized Fitting subgroup]]

## Properties

### Of free groups

Every subgroup of a [[free group]] is itself free. This is the statement of the _[[Nielsen-Schreier theorem]]_.

### Of Lie groups

For $H \hookrightarrow G$ a sub-[[Lie group]] inclusion write $\mathbf{B}H  \to \mathbf{B}G$ for the induced map on [[delooping]] [[Lie groupoids]]. The [[homotopy fiber]] of this map (in [[Smooth∞Grpd]]) is the [[coset space]] $G/H$: there is a [[homotopy fiber sequence]]

$$
  G/H \to \mathbf{B}H \to \mathbf{B}G
  \,.
$$

Now let $H \hookrightarrow K \hookrightarrow G$ be a sequence of two subgroup inclusions. By the above this yields the [[diagram]]

$$
  \array{
    K/H &\to& G/H &\to& G/K 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}H &\to& \mathbf{B}H &\to& \mathbf{B}K
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}K &\to& \mathbf{B}G &\to& \mathbf{B}G
  }
$$

## Examples

* [[centralizer subgroup]]

* [[normalizer subgroup]]

* [[stabilizer subgroup]]

* [[conjugate subgroup]]

* [[congruence subgroup]]

* [[Young subgroup]]


## Related concepts

* [[lattice of subgroups]]

* [[maximal subgroup]]

* [[index of a subgroup]]

* [[Klein geometry]], [[Cartan geometry]]

* [[BN-pair]]

* [[subring]], [[submodule]]


## References

Discussion in [[univalent foundations of mathematics]] ([[homotopy type theory]] with the [[univalence axiom]], but for 1-groups):


* [[Martín Escardó]], *[Subgroups](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#subgroups-sip)*, §33.12 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;

  > (in [[Agda]])


* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: Chapter 5 of: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$

See also

* Wikipedia, _[Subgroup](https://en.wikipedia.org/wiki/Subgroup)_



[[!redirects subgroup]]
[[!redirects subgroups]]
