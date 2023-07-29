

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

Consider the [[functor]]

$$
  C(-,\mathbb{R})
  \;\colon\;
  Top \longrightarrow \mathbb{R}Alg^{op}
$$

from the [[category]] [[Top]] of [[topological spaces]] to the [[opposite category]] of [[associative algebras]] over the [[real numbers]] given by forming [[algebras of functions|algebras of]] [[continuous functions]] with values in the [[real numbers]].

If $X,Y \in Top_{cptHaus} \hookrightarrow Top$ are two [[compact Hausdorff spaces]], then every [[morphism]] in $\mathbb{R}Alg$ ([[algebra homomorphism]]) of the form $C(Y,\mathbb{R}) \overset{\simeq}{\to} C(X,\mathbb{R})$ arises as pre-composition with a [[morphism]] in [[Top]] ([[homeomorphism]]) of the form $f \;\colon\; X \overset{\simeq}{\to} Y$.

In other words, the [[restriction]] 

$$
  C(-,\mathbb{R})
  \;\colon\;
  Top_{cptHaus} \overset{\phantom{AAAA}}{\hookrightarrow} \mathbb{R}Alg^{op}
$$

is a [[fully faithful functor]].


It follows in particular that [[compact Hausdorff spaces]] $X$ and $Y$ are [[homeomorphism|homeomorphic]] precisely if the algebras $C(X,\mathbb{R})$ and $C(Y,\mathbb{R})$ are isomorphic. 

In the literature, it is often this corollary alone which is referred to as the _Gelfand-Kolmogorov theorem_, but its proof by Gelfand-Kolmogorov, using a lemma by Stone, actually shows the full faithfulness of $C(-,\mathbb{R})$.

## Related statements

[[!include Isbell duality - table]]

## References

Original reference:

* [[И. М. Гельфанд]], [[А. Н. Колмогоров]], _О кольцах непрерывных функций на топологических пространствах_, Доклады Академии наук СССР 22:1 (1939), 11–15.

Reprinted in:

* [[А. Н. Колмогоров]], _Избранные труды.  Математика и механика_, Наука, 1985, 264–269.

English translation:

* [[I. M. Gel'fand]], [[A. N. Kolmogorov]], _On rings of continuous functions on topological spaces_, In: Selected Works of A. N. Kolmogorov.  Volume I.  Mathematics and Mechanics.  Edited by V. M. Tikhomirov, translated from the Russian by V. M. Volosov.  Kluwer, 1991.

See also

* {#GarridoJaramillo02} M. Garrido, J. Jaramillo , theorem 18 in _Variations on the Banach-Stone theorem_, 2002 ([web](http://eprints.ucm.es/21378/))


