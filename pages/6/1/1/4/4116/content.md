

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

Let [[Top]] be the [[category]] of [[topological space]]s, and let $\Sigma$ be the [[full subcategory]] whose only two [[object]]s are a one-point space and $\mathbb{N}^+$, the [[one-point compactification]] of the [[discrete space]] of [[natural number]]s. Let $J$ be the [[canonical Grothendieck topology]] on $\Sigma$. 

Johnstone's **topological topos** (specifically, the one described in the eponymous paper referenced below) is the [[topos]] of canonical [[sheaves]] $Sh_J(\Sigma)$ on $\Sigma$. The functor 

$$Top \to Set^{\Sigma^{op}}: X \mapsto Top(-, X)$$ 

is [[faithful functor|faithful]] and factors through $Sh_J(\Sigma)$, and its restriction to the category of [[sequential space]]s is full.

The category of [[subsequential spaces]] can also be found as a full subcategory of this topos (in fact, it consists of the separated objects for a [[Lawvere-Tierney topology]]).  A general object of the topos can be thought of as like a subsequential space, but such that a given sequence can converge to a given point in "more than one way."

Importantly, following an idea by Joyal, the topological topos $\mathcal{E}:=Sh_J(\Sigma)$ allows one to represent the [[geometric realization]] functor as the inverse image of a [[geometric morphism]] from $\mathcal{E}$ to the topos of [[simplicial set]]s. As Johnstone points out, this approach fails for the [[big topos]] on $Top$ and also for Lawvere's topos for [[continuum mechanics]].


## Reference 

* [[Peter Johnstone]], _On a topological topos_, Proc. London Math. Soc. (3) 38 (1979) 237&#8211;271. ([PDF](http://plms.oxfordjournals.org/content/s3-38/2/237.full.pdf))

n-cafe [blog](https://golem.ph.utexas.edu/category/2014/04/on_a_topological_topos.html) about this paper.

[[!redirects topological topos]]