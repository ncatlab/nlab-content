
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

A [[topological space]] $X$ is said to be __locally contractible__ if it has a [[basis for a topology|basis]] of [[open subset]]s that consists of [[contractible]] topological spaces $U \hookrightarrow X$.
=--

Sometimes one requires just that the inclusions $U \to X$ are [[null-homotopic map]]s. This might be called **semi-locally contractible**.

+-- {: .un_remark}
###### Remark

One could also consider a basis of open sets such that the opens $U$ have (just) trivial [[homotopy group]]s, but this does not seem to crop up in practice.
=--

+-- {: .un_defn}
###### Definition

A [[locale]] $X$ is __locally contractible__ if, viewing a locale as a $(0,1)$-[[(0,1)-topos|topos]] and hence a (very special kind of) $(\infty,1)$-[[(infinity,1)-topos|topos]], it is [[locally infinity-connected (infinity,1)-topos|locally ∞-connected]].
=--

+-- {: .query}
Is this right?  Do these two definitions correspond in that a [[sober space]] or [[topological locale]] is locally contractible as a topological space iff it\'s locally contractible as a locale?  ---Toby
=--


## Examples 

* Any [[CW-complex]] is locally contractible (see [there](CW+complex#CWComplexesAreLocallyContractible)).

* Any [[paracompact space|paracompact]] [[manifold]] is locally contractible.

* Any [[contractible space]] is semi-locally contractible

* The [[cone]] on the [[Hawaiian earring space]] is contractible, hence semi-locally contractible, but is not locally contractible, as any neighbourhood of the 'bad point' is not simply connected.

## Properties

+-- {: .un_prop}
###### Proposition

For $X$ a locally contractible topological space, the [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(X)$ is a [[locally ∞-connected (∞,1)-topos]].

=--

This is discussed at [[locally ∞-connected (∞,1)-site]].


## Other viewpoints

If one considers [[fundamental ∞-groupoid]]s, the inclusion $U \to X$ being null-homotopic is equivalent to the induced [[(∞,1)-functor]] $\Pi(U) \to \Pi(X)$ being naturally isomorphic to the trivial functor sending everything to a single point.

+--{: .query}
[[David Roberts]]: The following may be straightforwardly obvious, but I have couched it as a conjecture, because I haven't seen it in print.
=--

+-- {: .un_conjecture}
###### Conjecture

If the space $X$ is semi-locally contractible then every locally constant $n$-stack on the site of open sets of $X$ is locally trivial.
=--

See also [[locally ∞-connected (∞,1)-topos]]. There a converse to this conjecture is stated:

+-- {: .un_prop}
###### Propositon

Let $C$ be a [[site]] coming from a [[coverage]] such that constant [[(∞,1)-presheaf|(∞,1)-presheaves]] satisfy [[descent]] over objects of $C$ with respect to the generating [[covering]] families. Then the [[(∞,1)-category of (∞,1)-sheaves]] $\mathbf{H} = Sh_{(\infty,1)}(C)$ is a [[locally ∞-connected (∞,1)-topos]].
=--


[[!redirects locally contractible space]]
[[!redirects locally contractible spaces]]
[[!redirects locally contractible topological space]]
[[!redirects locally contractible topological spaces]]
