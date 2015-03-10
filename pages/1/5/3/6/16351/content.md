
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

+-- {: .num_theorem}
###### Theorem

The [[functor]]

$$
  C^\infty(-) \colon SmoothMfd \longrightarrow Alg_{\mathbb{R}}^{op}
$$

which sends a [[smooth manifold]] to (the [[formal dual]] of) its $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth functions]] is a [[full and faithful functor]].


In other words, for two [[smooth manifolds]] $X,Y$ there is a [[natural bijection]] between the [[smooth functions]] $X \to Y$ and the algebra homomorphisms $C^\infty(X)\leftarrow C^\infty(Y)$.


=--

(e.g. [Kolav-Slovak-Michor 93, corollary 35.10](#KolavSlovakMichor93))

+-- {: .num_remark}
###### Remark

This statement serves as the stepping-stone for generalizations of [[differential geometry]] such as to [[supergeometry]]. On the other hand, for transporting various applications familiar from [[algebraic geometry]] to [[differential geometry]] (such as [[Kähler differentials]], see there) the above embedding is insufficient, and instead of just remembering the [[associative algebra]] structure, one needs to remember the _[[smooth algebra]]_-structure on algebras of smooth functions. See also at _[[synthetic differential geometry]]_.

=--

## Related theorems

* [[Borel's theorem]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]


## References

A proof of the statement appears for instance in 

* {#KolavSlovakMichor93} Ivan Kolav, [[Jan Slovák]], [[Peter Michor]], _Natural operations in differential geometry_, Springer (1993)

Discussion that takes the dual algebraic formulation as the very definition of [[smooth functions]] is in

* {#Nestruev03} [[Jet Nestruev]], section 6 of _Smooth manifolds and Observables_, Graduate texts in mathematics 218, 2003
