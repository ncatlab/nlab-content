
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

\tableofcontents

## Idea

An *$\omega$-complete poset*, in the following sense, is a [[poset]] with [[countable set|countable]] [[joins]], hence a countably [[cocomplete category|cocomplete]] poset.


## Definition ##

A **$\omega$-complete poset** or a **$\omega$-[[cpo]]** is a [[poset]] $(P, \leq)$ with

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

* {#ADK16} [[Thorsten Altenkirch]], [[Nils Anders Danielsson]], [[Nicolai Kraus]], Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type ([abs:1610.09254](https://arxiv.org/abs/1610.09254))

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

[[!redirects omega-complete poset]]
[[!redirects omega-complete posets]]

[[!redirects ω-complete poset]]
[[!redirects ω-complete posets]]

[[!redirects omega complete poset]]
[[!redirects omega complete posets]]

[[!redirects ω complete poset]]
[[!redirects ω complete posets]]

[[!redirects omega-cpo]]
[[!redirects omega-cpos]]

[[!redirects ω-cpo]]
[[!redirects ω-cpos]]

[[!redirects omega cpo]]
[[!redirects omega cpos]]

[[!redirects ω cpo]]
[[!redirects ω cpos]]
