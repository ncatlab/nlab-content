
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

An [[(∞,1)-topos]] $\mathcal{X}$ has **homotopy dimension** $\leq n \in \mathbb{N}$ if every $(n-1)$-[[connected]] object $A$ has a [[global element]], a [[morphism]]  $* \to A$ from the 
[[terminal object in an (∞,1)-category|terminal object]] into it.

=--

This appears as [[Higher Topos Theory|HTT, def. 7.2.1.1]].


+-- {: .un_defn}
###### Definition

An [[(∞,1)-topos]] $\mathcal{X}$ is **locally of homotopy dimension** $\leq n \in \mathbb{N}$ if there exists a collection $\{U_i \in \mathcal{X}\}$ of [[object]]s such that 

* the $\{U_i\}$ generate $\mathcal{X}$ under [[(∞,1)-colimit]]s;

* each [[over-(∞,1)-topos]] $\mathcal{X}/U_i$ has homotopy dimension $\leq n$.

=--

This appears as [[Higher Topos Theory|HTT, def. 7.2.1.8]].


## Properties

+-- {: .un_prop}
###### Proposition

If an [[(∞,1)-topos]] $\mathcal{X}$ is locally of homotopy dimension $\leq n$ for some $n \in \mathbb{N}$ then it is a [[hypercomplete (∞,1)-topos]].

=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.1.12]].

+-- {: .un_prop}
###### Proposition

If $\mathcal{X}$ has homotopy dimension $\leq n$ then it also has [[cohomological dimension]] $\leq n$.

The converse holds if $\mathcal{X}$ has finite homotopy dimension an $n \geq 2$. 

=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.2.30]].


## Examples

+-- {: .un_prop}
###### Proposition

Up to [[equivalence in an (∞,1)-category|equivalence]], the unique [[(∞,1)-topos]] of homotopy dimension $\leq -1$ is the the [[terminal category]] $ * \simeq Sh_{(\infty,1)}(\emptyset)$. 

=--

This is [[Higher Topos Theory|HTT, example. 7.2.1.2]].



+-- {: .un_prop}
###### Proposition

For $C$ any [[(∞,1)-category]] with a [[terminal object in an (∞,1)-category|terminal object]], the 
[[(∞,1)-presheaf (∞,1)-category]] $PSh_{(\infty,1)}(C)$ is an [[(∞,1)-topos]] of homotopy dimension $\leq 0$.

In particular [[Top]] $\simeq$ [[∞Grpd]] $\simeq PSh_{(\infty,1)}(*)$ has homotopy dimension $\leq 0$.

=--

This is [[Higher Topos Theory|HTT, example. 7.2.1.3]].


+-- {: .un_prop}
###### Proposition

Every [[(∞,1)-category of (∞,1)-presheaves]] is an [[(∞,1)-topos]] of local homotopy dimension $\leq 0$.

=--

This appears as [[Higher Topos Theory|HTT, example. 7.2.1.9]].

+-- {: .un_theorem}
###### Theorem

If a [[paracompact topological space]] $X$ has [[covering dimension]] $\leq n$, then the [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(X) := Sh_{(\infty,11)}(Op(X))$ is an [[(∞,1)-topos]] of homotopy dimension $\leq n$.

=--

This is [[Higher Topos Theory|HTT, theorem 7.2.3.6]].


+-- {: .un_prop}
###### Proposition

For $X \in $ [[∞Grpd]] $\simeq$ [[Top]] an object, the [[over-(∞,1)-topos]] $\infty Grpd/X$ has homotopy dimension $\leq n$ precisely if $X \in Top$ a [[retract]] in the [[homotopy category of an (∞,1)-category|homotopy category]] $Ho(Top)$ of a [[CW-complex]] of [[dimension]] $\leq n$.

=--

This is [[Higher Topos Theory|HTT, example 7.2.1.4]].


## Related concepts

* [[dimension]]

  * **homotopy dimension**

  * [[cohomological dimension]] 

  * [[covering dimension]]

  * [[Heyting dimension]]


## References

The [[(∞,1)-topos theory|(∞,1)-topos theoretic]] notio is discuss in section  7.2.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_