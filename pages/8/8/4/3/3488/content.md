

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
=--
=--
=--




#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[topos]] may be thought of as a generalized [[topological space]]. Accordingly, the notions of 

* [[locally connected space]]

* locally 2-connected space

* etc. ...

* [[locally contractible space]]

have analogs for [[topos]]es, [[(n,1)-toposes]] and [[(∞,1)-topos]]es

* [[locally connected topos]]
 
* **locally $n$-connected $(n,1)$-topos**

* **locally $\infty$-connected $(\infty,1)$-topos.

## Definition



+-- {: .un_defn}
###### Definition

A [[(∞,1)-sheaf (∞,1)-topos]] $\mathbf{H}$ is called 
**locally $\infty$-connected** if the (essentially unique) 
[[global section]] [[(∞,1)-geometric morphism]] is an [[essential (∞,1)-geometric morphism]]

$$
  (\Pi \dashv \Delta \dashv \Gamma) : 
  \mathbf{H}
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
  \,.
$$

If in addition $\Pi$ preserves the [[terminal object]] we say that $\mathbf{H}$ is an **[[∞-connected (∞,1)-topos]]** . 

If $\Pi$ preserves even all [[finite limit|finite]] [[(∞,1)-product]]s we say that $\mathbf{H}$ is a [[strongly ∞-connected (∞,1)-topos]].

If $\Pi$ preserves even all [[finite limit|finite]] [[(∞,1)-limit]]s we say that $\mathbf{H}$ is a [[totally ∞-connected (∞,1)-topos]].


=--

+-- {: .un_defn}
###### Definition

For $\mathbf{H}$ a locally $\infty$-connected $(\infty,1)$-topos and $X \in \mathbf{H}$ an [[object]], we call $\Pi X \in $ [[∞Grpd]] the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] of $X$. The ([[categorical homotopy groups in an (∞,1)-topos|categorical]]) [[homotopy group]]s of $\Pi(X)$ we call the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of $X$

$$
  \pi_\bullet^{geom}(X) := \pi_\bullet(\Pi (X))
  \,.
$$

=--

Similarly we have:

+-- {: .un_defn}
###### Definition

For $n \in \mathbb{N}$ an [[(n,1)-topos]] $\mathbf{H}$ is called 
**locally $n$-connected** if the (essentially unique) 
[[global section]] geometric morphism is has an extra left adjoint.

=--

For $n = 1$ this reproduces the case of a [[locally connected topos]].


## Examples {#LocallyContractibleExamples}


### Over $\infty$-connected sites

The follow proposition gives a large supply of examples.

+-- {: .un_prop}
###### Proposition

Let $C$ be a locally and globally [[∞-connected site]]. Then the 
[[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(C)$ is a 
locally $\infty$-connected $(\infty,1)$-topos.

=--

See [[∞-connected site]] for the proof.

+-- {: .un_remark}
###### Remark

In ([SimpsonTeleman, prop. 2.18](#SimpsonTeleman))
is stated essentially what the above proposition asserts at the level of [[homotopy category|homotopy categories]]: if $C$ has contractible objects, then there exists a [[left adjoint]] $Ho(\Pi):Ho(Sh_{(\infty,1)}(C)) \to Ho(\infty Grpd)$. 

=--

This includes the following examples.

+-- {: .un_exampe}
###### Example

For $X$ a [[locally ∞-connected site]] its [[category of open subsets]] $Op(X)$ is a locally $\infty$-connected site.


=--

+-- {: .un_exampe}
###### Example

The sites [[CartSp]], [[ThCartSp]] are locally $\infty$-connected. 
The corresponding $(\infty,1)$-topos is [[?LieGrpd]].

=--

### Locally $\infty$-connected over-$(\infty,1)$-toposes

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ a locally $\infty$-connected $(\infty,1)$-topos, also all its objects $X \in \mathbf{H}$ are locally $\infty$-connected, in that their [[petit topos|petit]] [[over-(∞,1)-toposes]] $\mathbf{H}/X$ are locally $\infty$-connected.

The two notions of fundamental $\infty$-groupoids of $X$ induced this way do agree, in that there is a natural equivalence
$$
  \Pi_X(X \in \mathbf{H}/X) \simeq \Pi(X \in \mathbf{H})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the general facts recalled at [[etale geometric morphism]] we have a composite [[essential geometric morphism]]

$$
  (\Pi_X \dashv \Delta_X \dashv \Gamma_X) : 
  \mathbf{H}_{/X}
   \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{\X_*}{\to}}}
  \mathbf{H}
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}  
   \infty Grpd
$$

and $X_!$ is given by sending $(Y \to X) \in \mathbf{H}/X$ to $Y \in \mathbf{H}$.

=--

+-- {: .un_remark}
###### Remark

If in the above $X$ is contractible in that $\Pi X \simeq *$ then $\mathbf{H}/X$ is even an [[∞-connected (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

By the discussion there we need to check that $\Pi_X$ preserves the terminal object:

$$
  \Pi_X (X \to X) \simeq \Pi X_! (X \to X) \simeq \Pi X \simeq *
  \,.
$$

=--

## Properties {#LocInfConnProperties}



## Further structures

The fact that the terminal geometric morphism is essential gives rise to various induced structures of interest. For instance it induces a notion of 

* [[Whitehead tower in an (∞,1)-topos]].

For a more exhaustive list of extra structures see [[cohesive (∞,1)-topos]].

## Related concepts

* [[locally connected topos]] / **locally ∞-connected (∞,1)-topos**

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]



## References

Some discussion of the [[homotopy category of an (∞,1)-category|homotopy category]] of locally $\infty$-connected $(\infty,1)$-toposes is around proposition 2.18 of

* [[Carlos Simpson]], [[Constantin Teleman]], _de Rham's theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))
{#SimpsonTeleman}

For related references see 

* [[geometric homotopy groups in an (∞,1)-topos]]

* [[cohesive (∞,1)-topos]].


[[!redirects locally infinity-connected (infinity,1)-topos]]
[[!redirects locally infinity-connected (infinity,1)-toposes]]
[[!redirects locally infinity-connected (infinity,1)-topoi]]


[[!redirects locally n-connected (∞,1)-topos]]
[[!redirects locally contractible (infinity,1)-topos]]
[[!redirects locally contractible (∞,1)-topos]]
[[!redirects n-connected (∞,1)-topos]]

[[!redirects locally infinity-connected (∞,1)-topos]]

[[!redirects locally ∞-connected (∞,1)-topos]]
[[!redirects locally ∞-connected (∞,1)-toposes]]
[[!redirects locally ∞-connected (∞,1)-topoi]]


[[!redirects contractible (infinity,1)-topos]]
[[!redirects contractible (∞,1)-topos]]
[[!redirects contractible (infinity,1)-toposes]]
[[!redirects contractible (∞,1)-toposes]]

[[!redirects locally n-connected (infinity,1)-topos]]
[[!redirects locally n-connected (infinity,1)-tops]]



[[!redirects locally connected (∞,1)-geometric morphism]]
[[!redirects connected (∞,1)-geometric morphism]]
[[!redirects essential (∞,1)-geometric morphism]]