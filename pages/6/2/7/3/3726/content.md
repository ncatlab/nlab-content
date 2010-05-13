<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An **$n$-connected object** is an object all whose [[homotopy group]]s _equal to or below_ degree $n$ are trivial.

More precisely, an object in an [[∞-stack]] [[(∞,1)-topos]] is $n$-connected if its [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] equal to or below degree $n$ are trivial.

The complementary notion is that of an [[n-truncated object of an (∞,1)-category]].

The [[Whitehead tower]] construction produces $n$-connected objects.


## Definition

+-- {: .un_defn}
###### Definition

An object $X$ in an [[(∞,1)-topos]] $\mathbf{H}$ is called **$n$-connected** for $n \in \mathbb{N}$ if

* the [[terminal object|terminal]] morphism $X \to *$ is an [[effective epimorphism]];

* all [[homotopy groups in an (∞,1)-topos|categorical homotopy group]]
  equal to or below degree $n$ are trivial.

=--

By convention every object is $(-2)$-connected.

This appears as [[Higher Topos Theory|HTT, def. 6.5.1.10]], but under the name "$(n+1)$-connective."

+-- {: .un_prop}
###### Proposition

An object $X$ is $n$-connected (for $n \geq -2$) precisely if its [[n-truncated object in an (∞,1)-category|n-truncation]] $\tau_{\leq n} X$ is [[generalized the|the]] [[terminal object]] of $\mathbf{H}$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 6.5.1.12]]

=--



## Examples

### In $Top$

In the the [[(∞,1)-category]] [[Top]] we have

* a 0-connected object is a [[connected space]].

* a 1-connected object is a [[simply connected space]].



[[!redirects connected]]
[[!redirects n-connected object of an (∞,1)-category]]
[[!redirects n-connected object of an (∞,1)-topos]]
[[!redirects n-connected object of an (infinity,1)-category]]


[[!redirects 0-connected]]
[[!redirects 1-connected]]
[[!redirects 2-connected]]
[[!redirects 3-connected]]
[[!redirects 4-connected]]
[[!redirects 99-connected]]