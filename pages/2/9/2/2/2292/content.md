
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given any [[generalized (Eilenberg-Steenrod) cohomology theory]] $E$, then for each [[topological space]] $X$, there is, by definition, the [[graded abelian group]] 

$$
  E^\bullet(X) \in Ab^{\mathbb{Z}}
  \,.
$$

This is the _$E$-[[cohomology group]]_ of $X$. Now if $E$ is a [[multiplicative cohomology theory]], then these groups inherit the structure of [[rings]]. As such

$$
  E^\bullet(X) \in Ring^{\mathbb{Z}}
$$  

is the **$E$-cohomology ring** of $X$.

Analogously for various suitable generalizations of the nature of $E$ and $X$  (see at _[[generalized cohomology]]_).

## Related concepts

* [[quantum cohomology ring]]

* [[genus]]

* [[orientation in generalized cohomology]]

## References

Implementation of [[ordinary cohomology|ordinary]]$\;$[[cohomology rings]] in [[cubical agda]]:

* [[Thomas Lamiaux]], [[Axel Ljungström]], [[Anders Mörtberg]], _Computing Cohomology Rings in Cubical Agda_, CPP 2023: Proceedings of the 12th ACM SIGPLAN International Conference on Certified Programs and Proofs (2023) &lbrack;[arxiv:2212.04182] (https://arxiv.org/abs/2212.04182), [doi:10.1145/3573105.3575677](https://doi.org/10.1145/3573105.3575677)&rbrack;

* [[Thomas Lamiaux]]: *Computing Cohomology Rings in Cubical Agda*, [talk at](CQTS#LamiauxApr2024) *[Running HoTT 2024](CQTS#RunningHoTT2024)*, [[CQTS]]@NYUAD (April 2024) &lbrack;video:[kt](https://cdnapisec.kaltura.com/p/1674401/sp/167440100/embedIframeJs/uiconf_id/23435151/partner_id/1674401?iframeembed=true&playerId=kaltura_player&entry_id=1_2bxmtp75)&rbrack;


[[!redirects cohomology rings]]

[[!redirects homology ring]]
[[!redirects homology rings]]