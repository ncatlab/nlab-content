
<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An **$n$-connected object** is an object all whose [[homotopy group]]s _below_ degree $n$ are trivial.

More precisely, and object in an [[∞-stack]] [[(∞,1)-topos]] is $n$-truncated if its [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] below degree $n$ are trivial.

The complementary notion is that of an [[n-truncated object of an (∞,1)-category]].

The [[Whitehead tower]] construction produces $n$-connected objects.


## Definition

+-- {: .un_defn}
###### Definition

An object $X$ in an [[(∞,1)-topos]] $\mathbf{H}$ is called**$n$-connected** for $n \in \mathbb{N}$ if

* the [[terminal object|terminal]] morphism $X \to *$ is an [[effective epimorphism]];

* all [[homotopy groups in an (∞,1)-topos|categorical homotopy group]]
  below degree $n$ are trivial.

=--

By convention every object is $(-1)$-connected

This appears as [[Higher Topos Theory|HTT, def. 6.5.1.10]].

+-- {: .un_prop}
###### Proposition

An object $X$ is $n$-connected (for $n \geq -1$) precisely if its [[n-truncated object in an (∞,1)-category|(n-1)-truncation]] $\tau_{\leq (n-1)} X$ is [[generalized the|the]] [[terminal object]] of $\mathbf{H}$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 6.5.1.12]]

=--



## Examples

### In $Top$

In the the [[(∞,1)-category]] [[Top]] we have

* a 1-connected object is a [[connected space]].

* a 2-connected object is a [[simply connected space]].



[[!redirects connected]]
[[!redirects n-connected object of an (∞,1)-category]]
[[!redirects n-connected object of an (∞,1)-topos]]
[[!redirects n-connected object of an (infinity,1)-category]]
