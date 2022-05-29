
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The definition of the concept of sub-nets of a [[net]] requires some care. The point of the definition is to ensure that in [[classical mathematics]], [[compact spaces equivalently have converging subnets|compact spaces are equivalently those for which every net has a converging subnet]].

## Definition

There are several different definitions of '[[subnet]]' in the literature, all of which intend to generalise the concept of subsequences.  We state them now in order of increasing generality.  Note that it is Definition \ref{AA} which is correct in that it corresponds precisely to refinement of filters.  However, the other two definitions (def. \ref{Willard}, def. \ref{Kelley}) are sufficient (in a sense made precise by theorem \ref{EquivalenceOfDefinitionsOfSubnets} below) and may be easier to work with.


+-- {.num_defn #Willard}
###### Definition
(Willard, 1970).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

We have a [[function]] $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is monotone (that is, for every $\beta_1 \geq \beta_2 \in B$, $f(\beta_1) \geq f(\beta_2)$);
*  $f$ is cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that $f(\beta) \geq \alpha$).
=--

+-- {.num_defn #Kelley}
###### Definition
(Kelley, 1955).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

We have a [[function]] $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is strongly cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$, $f(\beta_1) \geq \alpha$).

=--

+-- {: .num_remark}
###### Remark

Notice that the function $f$ in definitions \ref{Willard} and \ref{Kelley} is _not_ required to be an [[injection]], and it need not be. As a result, a [[sequence]] regarded as a [[net]] in general has more sub-nets than it has sub-sequences.

=--


+-- {.num_defn #AA}
###### Definition
(Smiley, 1957; &#197;rnes & Anden&#230;s, 1972).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

The [[eventuality filter]] of $y$  refines the eventuality filter of $x$.  (Explicitly, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$ there is an $\alpha_1 \geq \alpha \in A$ such that $y_{\beta_1} = x_{\alpha_1}$.)
=--


The equivalence between these definitions is as follows:

+-- {.num_theorem #EquivalenceOfDefinitionsOfSubnets}
###### Theorem
([Schechter, 1996](#Schechter96)).

1.  If $y$ is a (\ref{Willard})-subnet of $x$, then $y$ is also a (\ref{Kelley})-subnet of $x$, using the same function $f$.
2.  If $y$ is a (\ref{Kelley})-subnet of $x$, then $y$ is also a (\ref{AA})-subnet of $x$.
3.  If $y$ is a (\ref{AA})-subnet of $x$, then there is some net $z$ such that
    *  $z$ is equivalent to $y$ in the sense that $y$ and $z$ are (\ref{AA})-subnets of each other, and
    *  $z$ is a (\ref{Willard})-subnet of $x$, using some function.
=--

So from the perspective of definition (\ref{AA}), there are enough (\ref{Willard})-subnets and (\ref{Kelley})-subnets, up to equivalence.

## References

A textbook account is in 

* {#Schechter96} [[Eric Schechter]], sections 7.14--7.21 of _[[Handbook of Analysis and its Foundations]]_, Academic Press (1996)

Lecture notes include

* {#Vermeeren10} [[Stijn Vermeeren]], _Sequences and nets in topology_, 2010 ([pdf](http://stijnvermeeren.be/download/mathematics/nets.pdf))


[[!redirects subnets]]

[[!redirects sub-net]]
[[!redirects sub-nets]]