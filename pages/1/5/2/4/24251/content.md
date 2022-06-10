
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An *$\omega$-complete poset*, in the following sense, is a [[poset]] with [[countable set|countable]] [[joins]], hence a countably [[cocomplete category|cocomplete]] poset.


## Definition ##

A __$\omega$-complete poset__ is a [[poset]] $(P, \leq)$ with

* an [[initial object|initial]] [[element]] $\bot \in P$ ([[bottom]]), hence such that for every element $a \in P$ we have $\bot \leq a$;

* a [[function]]

  $$
    \Vee_{n \colon \mathbb{N}} (-)(n) \;\colon\; 
    (\mathbb{N} \to P) \to L
  $$

  [[universal property|exhibiting]] the existence of [[countable set|denumerable/countable]] [[joins]] in the poset, namely such that 

  1. for every [[natural number]] $n \in \mathbb{N}$ and every [[sequence]] $s \colon \mathbb{N} \to P$ we have

     $$
       s(n) 
         \leq 
       \Vee_{n \colon \mathbb{N}} s(n)
       \,;
     $$

  1. for every element $a \in P$ and sequence $s \colon \mathbb{N} \to P$ of elements $\leq a$,

     $$
       \prod_{n \colon \mathbb{N}}
       (s(n) \leq a)
       \,,
     $$

     we have

     $$
       \Vee_{n \colon \mathbb{N}} 
       s(n) \leq a
       \,.
     $$ 

   

## See also ##

* [[poset]]

* [[join-semilattice]]

* [[sigma-complete lattice]]

* [[partial function classifier]]

* [[directed-complete poset]]

## References ##

* *Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type* ([arXiv:1610.09254](https://arxiv.org/abs/1610.09254))