
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Topos theory
+-- {: .hide}
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A [[topos]] may be thought of as a generalized [[topological space]]. Accordingly, the notions of 

* [[locally connected space]]

* [[locally simply connected space]]

* locally $2$-connected space

* locally $n$-connected space

* [[locally contractible space]]

have analogs for [[topos]]es, [[(n,1)-toposes]] and [[(∞,1)-topos]]es

* [[locally connected topos]]

* [[locally simply connected (2,1)-topos]]
 
* **locally $n$-connected $(n+1,1)$-topos**

* **locally $\infty$-connected $(\infty,1)$-topos**

The numbering mismatch is traditional from [[topology]]; see [[n-connected space]].  It reads a bit better if we say _locally $n$-simply connected_ for _locally $n$-connected_, since _locally $1$-(simply) connected_ is _locally simply connected_, but being locally $n$-simply connected is still a property of an $(n+1,1)$-topos.


## Definitions

+-- {: .num_defn}
###### Definition

A [[(∞,1)-sheaf (∞,1)-topos]] $\mathbf{H}$ is called 
**locally $\infty$-connected** if the (essentially unique) 
[[global section]] [[(∞,1)-geometric morphism]] 

$$
  (\Delta\dashv\Gamma):
  \mathbf{H} \xrightarrow{\Gamma}\infty\Grpd
$$ 

extends to an __[[essential geometric morphism]] $(\infty,1)$-geometric morphism__, i.e. there is a further [[left adjoint]] $\Pi$

$$
  (\Pi \dashv \Delta \dashv \Gamma) : 
  \mathbf{H}
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
  \,.
$$

If in addition $\Pi$ preserves the [[terminal object]] we say that $\mathbf{H}$ is an **[[∞-connected (∞,1)-topos]]**. 

If $\Pi$ preserves even all [[finite limit|finite]] [[(∞,1)-product]]s we say that $\mathbf{H}$ is a [[strongly ∞-connected (∞,1)-topos]].

If $\Pi$ preserves even all [[finite limit|finite]] [[(∞,1)-limit]]s we say that $\mathbf{H}$ is a [[totally ∞-connected (∞,1)-topos]].

=--

+-- {: .num_remark}
###### Remark

In ([Lurie, section A.1](#Lurie)) this is called an $(\infty,1)$-topos 
of **locally constant [[shape of an (infinity,1)-topos|shape]]**.

=--

+-- {: .num_defn}
###### Definition

For $\mathbf{H}$ a locally $\infty$-connected $(\infty,1)$-topos and $X \in \mathbf{H}$ an [[object]], we call $\Pi X \in $ [[∞Grpd]] the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] of $X$. The ([[categorical homotopy groups in an (∞,1)-topos|categorical]]) [[homotopy group]]s of $\Pi(X)$ we call the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of $X$

$$
  \pi_\bullet^{geom}(X) := \pi_\bullet(\Pi (X))
  \,.
$$

=--

Similarly we have:

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ an $(n+1,1)$-[[(n,1)-topos|topos]] $\mathbf{H}$ is called **locally $n$-connected** if the (essentially unique) [[global section]] geometric morphism is has an extra left adjoint.
=--

For $n = 0$ this reproduces the case of a [[locally connected topos]].


## Examples
{#LocallyContractibleExamples}

### Over locally $\infty$-connected sites

The follow proposition gives a large supply of examples.

+-- {: .num_prop}
###### Proposition

Let $C$ be a [[locally ∞-connected (∞,1)-site]]/[[∞-connected (∞,1)-site]]. Then the  [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(C)$ is a 
locally $\infty$-connected $(\infty,1)$-topos.
=--

See [[locally ∞-connected (∞,1)-site]]/[[∞-connected (∞,1)-site]] for the proof.

+-- {: .num_remark}
###### Remark

In ([SimpsonTeleman, prop. 2.18](#SimpsonTeleman))
is stated essentially what the above proposition asserts at the level of [[homotopy category|homotopy categories]]: if $C$ has contractible objects, then there exists a [[left adjoint]] $Ho(\Pi):Ho(Sh_{(\infty,1)}(C)) \to Ho(\infty Grpd)$. 
=--

This includes the following examples.

+-- {: .num_example}
###### Example

The sites [[CartSp]]${}_{top}$ $CartSp_{smooth}$ $CartSp_{synthdiff}$ are locally $\infty$-connected. 
The corresponding $(\infty,1)$-toposes are the [[cohesive (∞,1)-topos]]es [[ETop∞Grpd]], [[Smooth∞Grpd]] and [[SynthDiff∞Grpd]].
=--


### Over locally $n$-connected topological spaces
  {#OverLocallynConnectedTopologicalSpaces}

+-- {: .num_example}
###### Example

For $X$ a [[locally contractible space]], such that $Sh_{(\infty,1)}(X)$  is [[hypercomplete (infinity,1)-topos|hypercomplete]], $Sh_{(\infty,1)}(X)$ is a locally $\infty$-connected $(\infty,1)$-topos.

=--

+-- {: .proof}
###### Proof

The full subcategory $cOp(X) \hookrightarrow Op(X)$ of the [[category of open subsets]] on the contractible subsets is another site of definition for $Sh_{(\infty,1)}(X)$. And it is a [[locally ∞-connected (∞,1)-site]].
=--


+-- {: .num_prop}
###### Proposition

For $X$ a [[locally contractible topological space]] we have that the 
[[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]] computes the correct [[homotopy type]] of $X$:

the image of $X$ as the [[terminal object in an (∞,1)-category|terminal object]] in $Sh_{(\inffty,1)}(C)$ under the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]-functor

$$
  \Pi : Sh_{(\infty,1)}(X) \to \infty Grpd
$$

is equivalent to the ordinary [[fundamental ∞-groupoid]] given by the [[singular simplicial complex]]

$$
  \Pi(X) \simeq Sing X
  \,.
$$
=--

+-- {: .proof}
###### Proof

By using the [[presentable (∞,1)-category|presentations]] of $Sh_{(\infty,1)}(X)$ by the [[model structure on simplicial presheaves]] as discussed at [[locally ∞-connected (∞,1)-site]] one finds that this boils down to the old Artin-Mazur theorem. More on this at [[geometric homotopy groups in an (∞,1)-topos]].
=--


### Locally $\infty$-connected over-$(\infty,1)$-toposes

+-- {: .num_prop}
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

+-- {: .num_remark}
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


## Properties 
 {#LocInfConnProperties}

### Relation to slicing

+-- {: .num_prop}
###### Proposition

Let $\mathcal{X}$ be an $(\infty,1)$-topos and $\{U_i\}_i$ a collection of [[objects]] such that

* the canonical morphism $\coprod_i U_i \to *$ out of their [[coproduct]] to the [[terminal object]] is an [[effective epimorphism in an (∞,1)-category|effective epimorphism]];

* all the [[slice-(∞,1)-toposes]] $\mathcal{X}_{/U_i}$ are locally $\infty$-connected.

Then also $\mathcal{X}$ itself is locally $\infty$-connected.

=--

This appears as ([Lurie, corollary A.1.7](#Lurie)).

### Relation to locally connected toposes
 {#RelationToLocallyConnectedToposes}

+-- {: .num_prop}
###### Proposition

For $(\Pi \dashv \Delta \dashv \Gamma) :  \mathbf{H} \to \infty Grpd$ a locally $\infty$-connected $(\infty,1)$-topos, its underlying [[(n,1)-topos|(1,1)-topos]] $\tau_{\leq 0} \mathbf{H}$ is a [[locally connected topos]]. Moreover, if $\mathbf{H}$ is strongly connected (the extra left adjoint preserves finite products), then so is $\tau_{\leq 0} \mathbf{H}$.

=--

+-- {: .proof}
###### Proof

The [[global sections]] [[geometric morphism]]  $\Gamma \simeq \mathbf{H}(*,-)$ is given by homming out of the terminal object and hence preserves [[n-truncated object in an (infinity,1)-category|0-truncated]] objects by definition. Also, by the $(\Pi \dahsv \Delta)$-[[adjunction]] so does $\Delta$: for every $S \in Set \simeq \tau_{\leq }\infty Grpd \hookrightarrow \infty Grpd$ and every $X \in \mathbf{H}$ we have

$$
  \mathbf{H}(X, \Delta(S))
  \simeq
  \infty Grpd(\Pi(X), S)
  \simeq
  Set(\tau_{\leq 0} \Pi(X), S)
  \in 
  Set \hookrightarrow \infty Grpd
  \,.
$$

Therefore by essential uniqueness of [[adjoints]] the restriction $\Delta|_{\leq 0} \colon Set \hookrightarrow \infty Grpd \stackrel{\Delta}{\to} \mathbf{H}$ has a [[left adjoint]] given by 

$$
  \Pi_0 \coloneqq \tau_{\leq 0} \circ \Pi
  \,.
$$

Finally, by the discussion [here](n-truncated+object+of+an+%28infinity%2C1%29-category#PropertiesGeneral), $\tau_{\leq 0}$ preserves finite limits. Hence $\Pi_0$ does so if $\Pi$ does.

=--

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

Under the term _locally constant shape_ the notion appears in section A.1 of

* {#Lurie} [[Jacob Lurie]], _[[Higher Algebra]]_

See also

* {#Hoyois13} [[Marc Hoyois]], _A note on &#201;tale homotopy_, 2013 ([pdf](http://math.northwestern.edu/~hoyois/papers/etalehomotopy.pdf))


For related references see 

* [[geometric homotopy groups in an (∞,1)-topos]]

* [[cohesive (∞,1)-topos]].


[[!redirects locally n-connected (n,1)-topos]]
[[!redirects locally n-connected (n,1)-toposes]]
[[!redirects locally n-connected (n,1)-topoi]]
[[!redirects locally n-connected (n+1,1)-topos]]
[[!redirects locally n-connected (n+1,1)-toposes]]
[[!redirects locally n-connected (n+1,1)-topoi]]
[[!redirects locally n-simply connected (n+1,1)-topos]]
[[!redirects locally n-simply connected (n+1,1)-toposes]]
[[!redirects locally n-simply connected (n+1,1)-topoi]]

[[!redirects locally infinity-connected (n,1)-topos]]
[[!redirects locally infinity-connected (n,1)-toposes]]
[[!redirects locally infinity-connected (n,1)-topoi]]
[[!redirects locally ∞-connected (n,1)-topos]]
[[!redirects locally ∞-connected (n,1)-toposes]]
[[!redirects locally ∞-connected (n,1)-topoi]]
[[!redirects locally contractible (n,1)-topos]]
[[!redirects locally contractible (n,1)-toposes]]
[[!redirects locally contractible (n,1)-topoi]]

[[!redirects locally n-connected (∞,1)-topos]]
[[!redirects locally n-connected (∞,1)-toposes]]
[[!redirects locally n-connected (∞,1)-topoi]]
[[!redirects locally n-connected (infinity,1)-topos]]
[[!redirects locally n-connected (infinity,1)-toposes]]
[[!redirects locally n-connected (infinity,1)-topoi]]
[[!redirects locally n-connected (infinity,1)-tops]]

[[!redirects locally ∞-connected (∞,1)-topos]]
[[!redirects locally ∞-connected (∞,1)-toposes]]
[[!redirects locally ∞-connected (∞,1)-topoi]]
[[!redirects locally ∞-connected (infinity,1)-topos]]
[[!redirects locally ∞-connected (infinity,1)-toposes]]
[[!redirects locally ∞-connected (infinity,1)-topoi]]
[[!redirects locally infinity-connected (∞,1)-topos]]
[[!redirects locally infinity-connected (∞,1)-toposes]]
[[!redirects locally infinity-connected (∞,1)-topoi]]
[[!redirects locally infinity-connected (infinity,1)-topos]]
[[!redirects locally infinity-connected (infinity,1)-toposes]]
[[!redirects locally infinity-connected (infinity,1)-topoi]]
[[!redirects locally contractible (∞,1)-topos]]
[[!redirects locally contractible (∞,1)-toposes]]
[[!redirects locally contractible (∞,1)-topoi]]
[[!redirects locally contractible (infinity,1)-topos]]
[[!redirects locally contractible (infinity,1)-toposes]]
[[!redirects locally contractible (infinity,1)-topoi]]


[[!redirects n-connected (n,1)-topos]]
[[!redirects n-connected (n,1)-toposes]]
[[!redirects n-connected (n,1)-topoi]]
[[!redirects n-connected (n+1,1)-topos]]
[[!redirects n-connected (n+1,1)-toposes]]
[[!redirects n-connected (n+1,1)-topoi]]
[[!redirects n-simply connected (n+1,1)-topos]]
[[!redirects n-simply connected (n+1,1)-toposes]]
[[!redirects n-simply connected (n+1,1)-topoi]]

[[!redirects ∞-connected (n,1)-topos]]
[[!redirects ∞-connected (n,1)-toposes]]
[[!redirects ∞-connected (n,1)-topoi]]
[[!redirects infinity-connected (n,1)-topos]]
[[!redirects infinity-connected (n,1)-toposes]]
[[!redirects infinity-connected (n,1)-topoi]]
[[!redirects contractible (n,1)-topos]]
[[!redirects contractible (n,1)-toposes]]
[[!redirects contractible (n,1)-topoi]]

[[!redirects n-connected (∞,1)-topos]]
[[!redirects n-connected (∞,1)-toposes]]
[[!redirects n-connected (∞,1)-topoi]]
[[!redirects n-connected (infinity,1)-topos]]
[[!redirects n-connected (infinity,1)-toposes]]
[[!redirects n-connected (infinity,1)-topoi]]

[[!redirects ∞-connected (∞,1)-topos]]
[[!redirects ∞-connected (∞,1)-toposes]]
[[!redirects ∞-connected (∞,1)-topoi]]
[[!redirects ∞-connected (infinity,1)-topos]]
[[!redirects ∞-connected (infinity,1)-toposes]]

[[!redirects ∞-connected (infinity,1)-topoi]]
[[!redirects infinity-connected (∞,1)-topos]]
[[!redirects infinity-connected (∞,1)-toposes]]
[[!redirects infinity-connected (∞,1)-topoi]]
[[!redirects infinity-connected (infinity,1)-topos]]
[[!redirects infinity-connected (infinity,1)-toposes]]
[[!redirects infinity-connected (infinity,1)-topoi]]
[[!redirects contractible (∞,1)-topos]]
[[!redirects contractible (∞,1)-toposes]]
[[!redirects contractible (∞,1)-topoi]]
[[!redirects contractible (infinity,1)-topos]]
[[!redirects contractible (infinity,1)-toposes]]
[[!redirects contractible (infinity,1)-topoi]]


[[!redirects locally connected (∞,1)-geometric morphism]]
[[!redirects locally connected (∞,1)-geometric morphisms]]
[[!redirects locally connected (infinity,1)-geometric morphism]]
[[!redirects locally connected (infinity,1)-geometric morphisms]]

[[!redirects connected (∞,1)-geometric morphism]]
[[!redirects connected (∞,1)-geometric morphisms]]
[[!redirects connected (infinity,1)-geometric morphism]]
[[!redirects connected (infinity,1)-geometric morphisms]]

[[!redirects essential (∞,1)-geometric morphism]]
[[!redirects essential (∞,1)-geometric morphisms]]
[[!redirects essential (infinity,1)-geometric morphism]]
[[!redirects essential (infinity,1)-geometric morphisms]]

[[!redirects locally constant shape]]
[[!redirects ((∞,1)-topos of locally constant shape)]]
[[!redirects ((infinity,1)-topos of locally constant shape)]]
[[!redirects ((∞,1)-toposes of locally constant shape)]]
[[!redirects ((infinity,1)-toposes of locally constant shape)]]

[[!redirects locally ∞-connected geometric morphism]]
[[!redirects locally ∞-connected geometric morphisms]]