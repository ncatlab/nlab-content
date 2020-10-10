
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
#### Topos Theory
+--{: .hide}
[[!include type theory - contents]]
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects theory of infinite decidable object]]
[[!redirects theory of infinite decidable objects]]

## Idea
The _theory of decidable objects_ is the logical [[theory]] $\mathbb{D}$ whose models in a [[coherent category]] are precisely the [[decidable object|decidable objects]].

##Definition##
The _theory of decidable objects_ is the theory $\mathbb{D}$ over the signature with one sort and one binary relation $#$ besides equality with axioms $(x#x)\vdash_x\perp$ and $\top\vdash_{x,y} ((x#y)\vee(x=y))$.

## Properties

* For a [[topos]] $\mathcal{E}$ the category of models $Mod_{\mathbb{D}}(\mathcal{E})$ is the category of [[decidable object|decidable objects]] in $\mathcal{E}$. The _[[classifying topos]]_ $Set[\mathbb{D}]$ for the theory of decidable objects is the functor category $[FinSet_{mono},Set]$ where $FinSet_{mono}$ is the category of finite sets and monomorphisms. $Set[\mathbb{D}]$ is a [[locally decidable topos]].

## The quotient theory of infinite decidable objects

* The theory of _infinite decidable objects_ $\mathbb{D}_\infty$ adds to $\mathbb{D}$ the axioms $\top\vdash_{x_1,\dots,x_n} (\exists y)\bigwedge_{i=1}^{n}(y#x_i)$ for all $n$ with $\top\vdash(\exists y)\top$ for $n=0$. The models of $\mathbb{D}_\infty$ are precisely the infinite decidable objects and its classifying topos $Set[\mathbb{D}_\infty]$ is the [[Schanuel topos]].

## Related entries

* [[theory of objects]]

* [[decidable object]]

* [[locally decidable topos]]

* [[Schanuel topos]]

##References##

* [[Peter Johnstone]], _Sketches of an [[Elephant]] II_, Oxford UP 2002. (pp.906,925)