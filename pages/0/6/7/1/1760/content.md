

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _delooping_ of an object $A$ is, if it exists, a uniquely [[pointed object]] $\mathbf{B} A$ such that $A$ is the [[loop space object]] of $\mathbf{B} A$:

$$
  A \simeq \Omega(\mathbf{B} A)
$$

In particular, if $A = G$ is a [[group]] then its delooping 

* in the context [[Top]] is the [[classifying space]] $\mathcal{B}G$

* in the context [[∞-Grpd]] is the one-object groupoid $\mathbf{B}G$.

Under the [[homotopy hypothesis]] these two objects are identified: the [[geometric realization]] of the groupoid $\mathbf{B}G$ is the classifying space $\mathcal{B}G$:

$$
  |\mathbf{B}G| \simeq \mathcal{B}G
  \,.
$$

See [[looping and delooping]].

## Definition

Loop space objects are defined in any [[(∞,1)-category]] $\mathbf{C}$ with [[homotopy pullbacks]]: for $X$ any [[pointed object]] of $\mathbf{C}$ with point ${*} \to X$, its [[loop space object]] is [[generalized the|the]] [[homotopy pullback]] $\Omega X$ of this point along itself:

$$
  \array{
    \Omega X &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& X
  }
  \,.
$$

Conversely, if $A$ is given and a [[homotopy pullback]] diagram 

$$
  \array{
    A &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& \mathbf{B}A
  }
$$

exists, with the point ${*} \to \mathbf{B} A$ being essentially unique, by the above $A$ has been realized as the [[loop space object]] of $\mathbf{B} A$

$$
  A = \Omega \mathbf{B} A
$$

and we say that $\mathbf{B} A$ is the **delooping** of $A$.

See the section <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity%2C1)-category#Delooping">delooping</a> at [[groupoid object in an (∞,1)-category]] for more.

## Remarks

If $\mathbf{C}$ is even a [[stable (∞,1)-category]] then all deloopings exist and are then also denoted $\Sigma A$ and called the **[[suspension]]** of $A$.


## Characterization of deloopable objects

In section 6.1.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

a definition of 
[[groupoid object in an (infinity,1)-category]] $\mathbf{C}$ is given
as a homotopy simplicial object, i.e. a [[(infinity,1)-functor]]

$$
  C  : \Delta^{op} \to \mathbf{C}
$$
$$
  \cdots
  C_2 \stackrel{\to}\rightrightarrows
  C_1 
  \rightrightarrows 
 C_0
$$

satisfying certain conditions (prop. 6.1.2.6) which are such that if $C_0 = {*}$ is the [[point]] we have an internal _group_ in a homotopical sense, given by an object $C_1$ equipped with a coherently associative multiplication operation  $C_1 \times C_1 \to C_1$ generalizing that of [[Jim Stasheff|Stasheff]] [[H-space]] from the $(\infty,1)$-category [[Top]] to arbitrary $(\infty,1)$-categories.

Lurie calls the groupoid object $C$ an 
_effective_ [[groupoid object in an (infinity,1)-category]] precisely if it arises as the delooping, in the above sense, of some object $\mathbf{B}C$.

One of the characterizing properties of an [[(infinity,1)-topos]] is that _every_ groupoid object in it is effective.

This is the analog of [[Jim Stasheff|Stasheff]]'s classical result about [[H-spaces]].

See the remark at the very end of section 6.1.2 in [[Higher Topos Theory|HTT]].




## Examples


### Topological loop spaces 

For $C = $ [[Top]] the [[(infinity,1)-category]]
of [[topological spaces]], a space is deloopable if it is an [[A-infinity-space]] and hence homotopy equivalent to a [[loop space]].


### Delooping of a group to a groupoid 

Let $G$ be a [[group]] regarded as a [[discrete category|discrete groupoid]] in the [[(∞,1)-topos]] [[∞Grpd]] of [[∞-groupoids]].

Then $\mathbf{B} G$ exists and is, up to equivalence, the [[groupoid]]

* with a single object $\bullet$,

* with $Hom_{\mathbf{B} G}(\bullet, \bullet) = G$, or equivalently $Aut_{\mathbf{B}G}(\bullet) = G$,

* and with composition of morphisms in $\mathbf{B} G$ being given by the product operation in the group.

More informally but more suggestively we may write

$$
  \mathbf{B} G = \{ \bullet \stackrel{g}{\to} \bullet | g \in G\}
$$

or

$$
  \mathbf{B}G = \{ 
     \bullet \righttoleftarrow g \;|\; g \in G 
  \}
$$

to emphasize that there is really only a single object.

Notice how the [[homotopy pullback]] works in this simple case:

the universal 2-cell $\eta$

$$
  \array{
    G &\to& {*}
    \\
    \downarrow &\Downarrow^{\eta}& \downarrow
    \\
    {*} &\to& \mathbf{B}G
  }
$$

filling this [[2-limit]] diagram is the [[natural transformation]] from the constant [[functor]]

$$
  G \to {*} \to \mathbf{B}G
$$

to itself, whose component map

$$
  \eta : Obj(G) \to Mor(\mathbf{B}G)
$$ 

is just the identity map, using that $Obj(G) = G$ and $Mor(\mathbf{B}G) = G$.


## Deloopings of higher categorical structures 

There is also a notion of delooping which takes a pointed $(n, k+1)$-category $C$ to a pointed $(n+1, k)$-category $\mathbf{B} C$ in which $\mathbf{B} C$ has a single $0$-cell $\bullet$, and where $\hom(\bullet, \bullet) = C$. This is a tautological construction if one accepts the [[delooping hypothesis]], which views a $(n, k+1)$-category $C$ as a special type of $(n+k+1)$-category, namely a pointed $k$-connected $(n+k+1)$-category: by viewing such as *a fortiori* a pointed $(k-1)$-connected $(n+k+1)$-category, we get the delooping $\mathbf{B} C$. 

This is just a generalization of the fact that a [[monoid]] $M$ gives rise to a one-object category (which we are denoting $\mathbf{B} M$). For an important example: a [[monoidal category]] $M$ has an associated **delooping [[bicategory]]** $\mathbf{B} M$, where 

* $\mathbf{B} M$ has a single $0$-cell $\bullet$, 

* the $1$-cells $\bullet \to \bullet$ of $\mathbf{B} M$ are named by objects of $M$, and the composite of $\bullet \stackrel{a}{\to} \bullet \stackrel{b}{\to} \bullet$ is $\bullet \stackrel{a \otimes b}{\to} \bullet$ (using the monoidal product $\otimes$ of $M$), 

* the $2$-cells of $\mathbf{B} M$ are similarly named by morphisms of $M$; the vertical composition of $2$-cells in $\mathbf{B} M$ is given by composition of morphisms of $M$, and the horizontal composition of $2$-cells in $\mathbf{B} M$ is given by taking the monoidal product of the morphisms that name them in $M$. 

Along similar lines, the delooping of a [[braided monoidal category]] produces a [[monoidal bicategory]], and delooping of *that* is a [[tricategory]] or (weak) $3$-category. See [[delooping hypothesis]] for more. 

## Related concepts

* [[loop space object]], [[free loop space object]],

  * **delooping**

  * [[loop space]], [[free loop space]], [[derived loop space]]


* [[suspension object]]

  * [[suspension]], [[reduced suspension]]




[[!redirects deloopings]]
[[!redirects delooped group]]

[[!redirects delooped]]

