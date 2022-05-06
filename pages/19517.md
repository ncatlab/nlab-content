


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Let $\mathcal{C}$ and $\mathcal{D}$ be [[model categories]], and let

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longleftarrow}}
      {\bot_{Qu}}
  \mathcal{D}
$$

be a [[Quillen adjunction]]. Then 

1. a _derived adjunction unit_ at an [[object]] $d \in \mathcal{D}$ is a [[composition]] of the form

   $$
     Q(d) 
       \overset{\eta_{Q(d)}}{\longrightarrow}
     R(L(Q(d)))
       \overset{R( j_{L(Q(d))} )}{\longrightarrow}
     R(P(L(Q(d)))
   $$

   where

   1. $\eta$ is the ordinary [[adjunction unit]];

   1. $\emptyset \underoverset{\in Cof_{\mathcal{D}}}{i_{Q(d)}}{\longrightarrow} Q(d) \underoverset{\in W_{\mathcal{D}} \cap Fib_{\mathcal{D}}}{p_{Q(d)}}{\longrightarrow} d$ is a [[cofibrant resolution]] in $\mathcal{D}$;

   1. $L(Q(d)) \underoverset{\in W_{\mathcal{C}} \cap Cof_{\mathcal{C}}}{j_{L(Q(d))}}{\longrightarrow} P(L(Q(d))) \underoverset{\in Fib_{\mathcal{C}}}{q_{L(Q(d))}}{\longrightarrow} \ast$ is a [[fibrant resolution]] in $\mathcal{C}$;

1. a _derived adjunction counit_ at an object $c \in \mathcal{C}$ is a composition of the form

   $$
     L(Q(R(P(c))))
       \overset{ L( p_{R(P(c))} ) }{\longrightarrow}
     L R(P(c)) 
       \overset{\epsilon_{P(c)}}{\longrightarrow}
     P(c)
   $$

   where

   1. $\epsilon$ is the ordinary [[adjunction counit]];

   1. $c \underoverset{\in W_{\mathcal{C}} \cap Cof_{\mathcal{C}}}{j_c}{\longrightarrow} P c \underoverset{\in Fib_{\mathcal{C}}}{q_c}{\longrightarrow} \ast$ is a [[fibrant resolution]] in $\mathcal{C}$;

   1. $\emptyset \underoverset{\in Cof_{\mathcal{D}}}{i_{R(P(c))}}{\longrightarrow} Q(R(P(c))) \underoverset{\in W_{\mathcal{D}} \cap Fib_{\mathcal{D}}}{p_{R(P(c))}}{\longrightarrow} R(P(c))$ is a [[cofibrant resolution]] in $\mathcal{D}$. 

=--

## Properties

* A [[Quillen adjunction]] is a [[Quillen equivalence]] precisely if both its derived adjunction units and derived adjunction counit at [[weak equivalences]].

* A [[Quillen adjunction]] is a [[Quillen reflection]] precisely if the components of its derived adjunction counit are [[weak equivalences]].

* A [[Quillen adjunction]] is a [[Quillen co-reflection]] precisely if the components of its derived adjunction unit are [[weak equivalences]].



## Related concepts

* [[adjunction unit]]

* [[derived functor]]

* [[Quillen equivalence]], [[Quillen reflection]]

[[!redirects derived adjunction units]]

[[!redirects derived adjunction counit]]
[[!redirects derived adjunction counits]]

[[!redirects derived unit of a Quillen adjunction]]
[[!redirects derived units of Quillen adjunctions]]

[[!redirects derived counit of a Quillen adjunction]]
[[!redirects derived counits of Quillen adjunctions]]

