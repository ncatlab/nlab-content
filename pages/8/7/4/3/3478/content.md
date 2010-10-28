[[!redirects locally contractible space]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A [[topological space]] $X$ is said to be **locally contractible** 
if it has a [[basis for a topology|basis]] of open sets $U$ such that the spaces $U$ are [[contractible]].

Sometimes one requires just that the inclusions $U \to X$ are [[null-homotopic maps]]. This might be called **semi-locally contractible**.



One could also consider a basis of open sets such that the opens $U$ have trivial homotopy groups, but this does not seem to crop up in practice.



## Examples 

* Any [[CW-complex]] is locally contractible.
* Any [[paracompact]] [[manifold]] is locally contractible
* Any [[contractible]] space is semi-locally contractible
* The [[cone]] on the [[Hawaiian earring space]] is contractible, hence semi-locally contractible, but is not locally contractible, as any neighbourhood of the 'bad point' is not simply connected.

## Other viewpoints

If one considers [[fundamental ∞-groupoid]]s, the inclusion $U\to X$ being null-homotopic is equivalent to the induced [[(∞,1)-functor]] $\Pi(U) \to \Pi(X)$ being naturally isomorphic to the trivial functor sending everything to a single point.

+--{: .query}
[[David Roberts]]: The following may be straightforwardly obvious, but I have couched it as a conjecture, because I haven't seen it in print.
=--

**Conjecture:** If the space $X$ is semi-locally contractible then every locally constant $n$-stack on the site of open sets of $X$ is locally trivial.

See also [[locally ∞-connected (∞,1)-topos]]. There a converse to this conjecture is stated:

**Propositon** Let $C$ be a [[site]] coming from a [[coverage]] such that constant [[(∞,1)-presheaf|(∞,1)-presheaves]] satisfy [[descent]] over objects of $C$ with respect to the generating [[covering]] families. Then the [[(∞,1)-category of (∞,1)-sheaves]] $\mathbf{H} = Sh_{(\infty,1)}(C)$ is a [[locally ∞-connected (∞,1)-topos]].