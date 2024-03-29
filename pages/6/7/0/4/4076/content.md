
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **universal element** of a [[functor]] $F: C \to Set$ is an element $\theta \in F(x)$, where $x$ is some [[object]] of $C$, which exhibits [[representable functor|representability]] of $F$ via the [[Yoneda lemma]]. That is, any element $\theta \in F(x)$ induces, in natural bijective fashion, a [[natural transformation]]

$$\hat{\theta}: \hom(x, -) \to F$$ 


$$\hat{\theta}_y(f: x \to y) \stackrel{def}{=} F(f)(\theta)$$ 

and $\theta$ is _universal_ if $\hat{\theta}$ is an isomorphism. 

Thus, universal elements are part and parcel of any discussion involving representability. Well-known examples include [[adjoint functor]]s, where one has representability 

$$\hom(F(c), -) \cong \hom(c, G-),$$ 

the [[Brown representability theorem]], and there are many others. A few more examples are discussed below. 

## Examples

### Internal logic in toposes 

Quite often, logical constructions that work for arbitrary [[topos|toposes]] can be deduced by arguing from universal elements. Some simple examples follow. 

Consider first the construction of internal conjunction $\wedge: \Omega \times \Omega \to \Omega$. 

### Colimits of nerves 

A [question](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1284) was brought to the nForum on [[colimit]]s of [[nerve]]s, conjecturing the following which we state as a proposition (proof below): 

+-- {: .un_prop}
###### Proposition

If $C$ is a [[small category]], then the [[colimit]] of the composite 

$$C^{op} \stackrel{(- \downarrow C)}{\to} Cat \stackrel{Nerve}{\to} Set^{\Delta^{op}}$$ 

is equivalent to the [[nerve]] of $C$.

=--

As a warm-up: 

+-- {: .un_lemma}
###### Lemma

The colimit of 

$$C^{op} \stackrel{(- \downarrow C)}{\to} Cat$$ 

is [[isomorphic]] to $C$. 

=--

+-- {: .proof}
###### Proof


The objects of $colim_{c: C^{op}} (c \downarrow C)$  are equivalence classes of arrows or [[generalized element|generalized elements]] $c \to d$ where the equivalence $\sim$ is generated by 

$$(c \stackrel{f}{\to} d) \sim (c' \stackrel{g}{\to} c \stackrel{f}{\to} d)$$ 

and it is immediate that every generalized element $g: c \to d$ is equivalent to the universal generalized element $1_d: d \to d$; in spirit, this is the [[Yoneda lemma]] in disguise. 

=--


Now we prove the proposition on colimits of nerves. 

+-- {: .proof}
###### Proof


[[limits and colimits by example|Since]] colimits in $Set^{\Delta^{op}}$ ([[sSet]]) are computed pointwise, we just have to show the colimit of 

$$C^{op} \stackrel{(c \downarrow C)}{\to} Cat \stackrel{nerve}{\to} Set^{\Delta^{op}} \stackrel{ev_n}{\to} Set,$$ 

where $ev_n$ is evaluation at an object $n$, agrees with $nerve(C)_n$. This is 

$$C^{op} \stackrel{(c \downarrow C)}{\to} Cat \stackrel{\hom([n], -)}{\to} Set$$ 

Now an $n$-[[simplex]] in the [[comma category]] $(c \downarrow C)$, which is an element of this composite, is the same as an $(n+1)$-simplex beginning with the vertex $c$, and the colimit (in $Set$) consists of equivalence classes of $(n+1)$-simplices where a simplex beginning with $c$ is deemed equivalent to a simplex beginning with $c'$ obtained by pulling back along any $g: c' \to c$. And again, it is a triviality that each $(n+1)$-simplex 

$$c \to (d_0 \to \ldots \to d_n)$$ 

is equivalent to 

$$d_0 \stackrel{1_{d_0}}{\to} (d_0 \to \ldots \to d_n)$$

but the collection of such $d_0 \to \ldots \to d_n$ is the same as $nerve(C)_n$. This completes the verification.

=--

[[!redirects universal elements]]
