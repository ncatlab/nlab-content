
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_theorem #Embedding}
###### Theorem
**(Milnor's exercise)**


The [[functor]]

$$
  C^\infty(-) \colon SmoothMfd \longrightarrow Alg_{\mathbb{R}}^{op}
$$

which sends a [[smooth manifold]] ([[finite number|finite]] [[dimension|dimensional]], [[paracompact topological space|paracompact]], [[second countable topological space|second countable]]) to (the [[formal dual]] of) its $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth functions]] is a [[full and faithful functor]].


In other words, for two [[smooth manifolds]] $X,Y$ there is a [[natural bijection]] between the [[smooth functions]] $X \to Y$ and the $\mathbb{R}$-[[associative algebra|algebra]] [[homomorphisms]] $C^\infty(X)\leftarrow C^\infty(Y)$.


=--

Proof is for instance in ([Kolar-Slovak-Michor 93, lemma 35.8, corollaries 35.9, 35.10](#KolarSlovakMichor93)).

+-- {: .num_remark}
###### Remark

The statement of theorem \ref{Embedding} serves as the stepping-stone for generalizations of [[differential geometry]] such as to [[supergeometry]]. On the other hand, for transporting various applications familiar from [[algebraic geometry]] to [[differential geometry]] (such as [[Kähler differentials]], see there) the above embedding is insufficient, and instead of just remembering the [[associative algebra]] structure, one needs to remember the _[[smooth algebra]]_-structure on algebras of smooth functions. See also at _[[synthetic differential geometry]]_.

=--

+-- {: .num_remark}
###### Remark

If one drops standard regularity assumptions on manifolds then theorem \ref{Embedding} may break. For instance allowing [[countable set|uncountably]] many connected components, then there are counterexamples ([MO discussion](http://mathoverflow.net/a/91445)).

=--

## Related theorems

* [[Borel's theorem]]

* [[Hadamard's lemma]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]

* [[smooth Serre-Swan theorem]]

* [[derivations of smooth functions are vector fields]]

The analogous statement in [[topology]] is:

* [[Gelfand duality]]

[[!include Isbell duality - table]]




## References

A proof of the statement appears in

* {#KolarSlovakMichor93} Ivan Kolar, [[Jan Slovák]], [[Peter Michor]], _Natural operations in differential geometry_, Springer (1993) ([book webpage](http://www.emis.de/monographs/KSM/), [doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3))

Discussion that takes the dual algebraic formulation as the very definition of [[smooth functions]] is in

* {#Nestruev03} [[Jet Nestruev]], section 6 of: _Smooth manifolds and Observables_, Graduate Texts in Mathematics 218, Springer 2003 ([doi:10.1007/b98871](https://link.springer.com/book/10.1007/b98871))

The analog of the statement for real algebras refined to [[smooth algebras]] is theorem 2.8 in

* [[Ieke Moerdijk]], [[Gonzalo Reyes|Gonzalo E. Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)

[[!redirects Milnor's exercise]]

