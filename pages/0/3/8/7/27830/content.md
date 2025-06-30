\tableofcontents

## Definition

A [[quasicategory]] $C$ is __confluent__ if for every [[cospan]] $Q\colon\Lambda^2_0\to C$ the quasicategory $I_{Q/}$ of [[cocones]] under $Q$ is weakly contractible.

## Properties

If $C$ has [[pushouts]], then $C$ is confluent because the quasicategory of cocones has an [[initial object]].

A [[quasicategory]] $C$ is confluent if and only if for every morphism $f\colon A\to B$, the induced functor $f^*\colon C_{B/}\to C_{A/}$ is a [[final functor]].

If $\pi\colon T\to B$ is a [[left fibration]] and $B$ is confluent, then so is $T$.

\begin{theorem}
(Sattler–Wärn.)
A quasicategory $C$ is confluent if and only if $C$-indexed [[colimits]] commute with [[pullbacks]] in the quasicategory of [[∞-groupoids]].
\end{theorem}

A quasicategory is [[filtered (∞,1)-category|filtered]] if and only if it is confluent and weakly contractible.

## Related concepts

* [[confluent category]], [[confluent relation]]

* [[filtered colimit]], [[commutativity of limits and colimits]]

## References

* [[Christian Sattler]], David Wärn, [A better synthetic argument that confluent colimits commute with pullbacks](https://www.cse.chalmers.se/~sattler/docs/confluent/new-2025.txt), February 2025.

Expository account:

* [[Rune Haugseng]], Yet another introduction to ∞-categories, 2025.  [PDF](https://runegha.folk.ntnu.no/naivecat_web.pdf).
