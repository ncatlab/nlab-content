
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **[[Grothendieck]] fibration fibered in groupoids** -- usually called a **category fibered in groupoids** -- is a [[Grothendieck fibration]] $p : E \to B$ all whose [[fiber]]s are [[groupoid]]s.

## Definition

+-- {: .num_defn }
###### Definition

A **fibration fibered in groupoids** is a [[functor]] $p : E \to B$ such that the corresponding (strict) functor $B^{op} \to $ [[Cat]] classifying $p$ under the [[Grothendieck construction]] factors through the inclusion [[Grpd]] $\hookrightarrow$ [[Cat]].

=--

Under forming [[opposite categories]] we obtain the notion of an **op-fibration fibered in groupoids**. In old literature this is sometimes called a "cofibration in groupoids" but that terminology collides badly with the notion of *[[cofibration]]* in [[homotopy theory]] and [[model category]] theory.

## Properties

Fibrations in groupoids have a simple characterization in terms of their [[nerve]]s. Let $N : Cat \to sSet$ be the [[nerve]] functor and for $p : E \to B$ a morphism in [[Cat]], let $N(p) : N(E) \to N(B)$ be the corresponding morphism in [[sSet]].

Then

+-- {: .num_prop }
###### Proposition

The functor $p : E \to B$ is an  op-fibration in groupoids precisely if the morphism $N(p) : N(E) \to N(B)$ is a [[left Kan fibration]] of simplicial sets, i.e. precisely if for all [[horn]] inclusion 

$$
  \Lambda[n]_i \hookrightarrow \Delta[n]
$$

for all $n \in \mathbb{N}$ and all $i$ _smaller_ than $n$ ($0 \leq i \lt n$), we have that every commuting diagram

$$
  \array{
    \Lambda[n]_i &\to& N(E)
    \\
    \downarrow && \downarrow^{\mathrlap{N(p)}}
    \\
    \Delta[n] &\to& N(B)
  }
$$

has a lift

$$
  \array{
    \Lambda[n]_i &\to& N(E)
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{N(p)}}
    \\
    \Delta[n] &\to& N(B)
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

For instance [[Higher Topos Theory|HTT, prop. 2.1.1.3]].

=--

## Related concepts

* [[Grothendieck fibration]], [[Grothendieck construction]]

* [[discrete fibration]]

* [[left fibration]], [[right fibration]], [[Cartesian fibration]], [[Kan fibration]]

## References

Review:

* [[Angelo Vistoli]], §3.3 in: *Grothendieck topologies, fibered categories and descent theory*, in: *[[Fundamental algebraic geometry -- Grothendieck's FGA explained]]*, Mathematical Surveys and Monographs **123**, Amer. Math. Soc. (2005) 1-104 &lbrack;[ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [math.AG/0412512](http://arxiv.org/abs/math/0412512)&rbrack;



[[!redirects category fibered in groupoids]]
[[!redirects category fibred in groupoids]]
[[!redirects categories fibered in groupoids]]
[[!redirects categories fibred in groupoids]]

[[!redirects category fibered in groupoids]]
[[!redirects category fibred in groupoids]]
[[!redirects categories fibered in groupoids]]
[[!redirects categories fibred in groupoids]]
[[!redirects category cofibered in groupoids]]

[[!redirects category cofibred in groupoids]]
[[!redirects categories cofibered in groupoids]]
[[!redirects categories cofibred in groupoids]]

[[!redirects fibration in groupoids]]
[[!redirects opfibration in groupoids]]
[[!redirects fibrations in groupoids]]
[[!redirects opfibrations in groupoids]]

[[!redirects fibrations fibered in groupoids]]
