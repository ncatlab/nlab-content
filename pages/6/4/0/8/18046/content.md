



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


  For $\mathfrak{g}$ a [[Lie algebra]], then the  Lie algebra of its [[automorphism Lie group]] 

  $$
    Aut(\mathfrak{g})
   \,,
  $$

called the the _automorphism Lie algebra_ of $\mathfrak{g}$ (or _derivation Lie algebra_), is the Lie algebra whose [[underlying]] [[vector space]] is that of those [[linear maps]] $\Delta \colon \mathfrak{g} \to \mathfrak{g}$
which satisfy the [[derivation]] property:

$$
  \Delta([x,y]) = [\Delta(x), y] + [x, \Delta(y)]
$$

for all $x,y \in \mathfrak{g}$. The Lie bracket on $\mathfrak{aut}(\mathfrak{g})_{\mathrm{even}}$ is the [[commutator]] operation:

$$
  [\Delta_1, \Delta_2] \coloneqq \Delta_1 \circ \Delta_2 - \Delta_2 \circ \Delta_1
  \,.
$$

## Related concepts

* [[endomorphism Lie algebra]]

* [[automorphism infinity-Lie algebra]]

[[!redirects derivation Lie algebras]]


[[!redirects Lie algebra derivation]]
[[!redirects Lie algebra derivations]]
